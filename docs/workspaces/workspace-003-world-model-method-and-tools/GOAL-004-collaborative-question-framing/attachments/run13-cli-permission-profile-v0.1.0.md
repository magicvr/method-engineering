---
title: Run-13 Codex CLI isolated permission profile
status: draft
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-run13-cli-profile
---

# Run-13 Codex CLI permission profile · v0.1.0

## 身份与依据

- Codex CLI binary: `C:\Users\magicvr\AppData\Local\OpenAI\Codex\bin\faa963e871dd422c\codex.exe`
- Installed version observed: `codex-cli 0.158.0-alpha.2.1`.
- Dedicated profile file: `C:\Users\magicvr\.codex\run13-isolated.config.toml`; its exact bytes and SHA-256 must be bound in run-13 v0.1.2.
- Profile schema fields were checked against the official Codex permissions documentation and official config schema retrieved 2026-09-29: `default_permissions`, `[permissions.<name>]`, `workspace_roots`, `filesystem`, filesystem modes `read` / `write` / `deny`, `:root`, `:minimal`, `:workspace_roots`, and `windows.sandbox = "elevated"`.
- Official references: <https://learn.chatgpt.com/docs/permissions> and <https://learn.chatgpt.com/docs/config-schema.json>.
- Codex CLI `exec --help` documents `-C`, `--ignore-user-config`, `--ignore-rules`, `--strict-config`, `--ephemeral`, and `--json`; the root CLI help documents `--search`. The installed parser's `--strict-config` check is the final schema validation; this profile does not rely on guessed or unknown keys.

## Effective profile intent

The formal invocation must pass `--ignore-user-config` so the user's general config containing legacy `sandbox_mode` is not loaded, then select `--profile run13-isolated`. The selected profile file explicitly sets `default_permissions="run13-isolated"`; no broad built-in or fallback profile is permitted. The profile does not extend `:workspace`.

The isolated folder is the sole enabled profile workspace root. The file policy denies `:root`, grants only `:minimal` runtime read, and explicitly denies the original method-engineering repository and prior Codex trial-output area. Inside the sole workspace root, `.` is denied, each of the five named packet files is read-only, and only `trace` is writable.

## Bound CLI configuration arguments

The dedicated `$CODEX_HOME/run13-isolated.config.toml` profile file must contain the following exact TOML, and the ordinary PowerShell launcher must select it with the exact CLI/profile/cwd flags:

```toml
default_permissions = "run13-isolated"

[windows]
sandbox = "elevated"

[permissions.run13-isolated.workspace_roots]
"C:\\Users\\magicvr\\Documents\\Code\\method-engineering-run13-isolated" = true

[permissions.run13-isolated.filesystem]
":root" = "deny"
":minimal" = "read"
"C:\\Users\\magicvr\\Documents\\Code\\method-engineering" = "deny"
"C:\\Users\\magicvr\\Documents\\Codex" = "deny"
"C:\\Users\\magicvr\\Documents\\Code\\method-engineering-run11-isolated" = "deny"
"C:\\Users\\magicvr\\Documents\\Code\\method-engineering-run12-isolated" = "deny"

[permissions.run13-isolated.filesystem.":workspace_roots"]
"." = "deny"
"stage1-framing-method-v0.18.0-execution-projection-v0.1.0.md" = "read"
"shared-research-loop-core-v0.1.0.md" = "read"
"shared-research-record-schema-v0.1.0.md" = "read"
"s1-research-adapter-v0.1.1.md" = "read"
"s1-integration-trial-input-card-run13-v0.1.1.md" = "read"
"trace" = "write"

[permissions.run13-isolated.network]
enabled = false
```

```powershell
Set-Location -LiteralPath 'C:\Users\magicvr\Documents\Code\method-engineering-run13-isolated'
& 'C:\Users\magicvr\AppData\Local\OpenAI\Codex\bin\faa963e871dd422c\codex.exe' --search exec --ignore-user-config --ignore-rules --strict-config --profile run13-isolated --skip-git-repo-check --ephemeral --json -C 'C:\Users\magicvr\Documents\Code\method-engineering-run13-isolated' 'SMOKE PROMPT'
```

The user-level base configuration is deliberately ignored for both sessions; the named file above is still selected through `--profile`. `--strict-config` makes the installed parser reject unrecognized config fields, while the effective profile is additionally proven by the runtime permission block and access tests. `--search` enables hosted web search for the dedicated research-tool smoke and any later natural host-triggered use; the smoke query must be harmless and unrelated to the Probe. Hosted web search is independent of the profile's disabled shell network. No MCP or browser tool is required by the run-13 S1 adapter binding; if the selected runtime adds one as a research dependency, it requires its own disposable availability smoke before Probe execution.

The profile is intentionally restrictive. If `--strict-config` rejects an assignment, the elevated sandbox cannot start, the exact negative canary is readable, or the effective readable roots include the source repository or any old trial/workspace, stop and record failure. Do not widen the profile to make the smoke pass.
