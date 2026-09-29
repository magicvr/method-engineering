---
title: S1 historical-anchor integrated operational trial binding · run-19
status: draft
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-draft-trial-binding
trial_status: not-run
execution_authorization: not-granted
---

# S1 Historical-Anchor Integrated Operational Trial Binding · run-19 · v0.1.0

**PROPOSAL / NOT-RUN / CREATOR REVIEW ONLY.** Control-side preflight proposal for run-19 using the identical frozen v0.18.5 packet and conditions recorded in E-111 and the unchanged run-17 trial design. This is an independent repeatability run; that purpose and any prior outcome remain control-side only. Trial scope, evaluation, relay, stop, and isolation follow that control-only design and the v0.1.3 isolation contract. This file identifies a proposed trial packet and control protocol. It is not an execution authorization. Do not create or prompt the runner from this proposal. If accepted, recompute the complete manifest and final binding SHA-256, submit that exact identity, and wait for separate execution authorization.

## 1. Fixed identity and scope

- Proposed Run ID: `run-19` (new trial identifier; not started).
- Trial kind: historical-anchor integrated operational trial, using the original raw question `世界有多大？`.
- Bound S1 source candidate: `stage1-framing-method-integration-candidate-v0.18.5.md`, 96,103 bytes, SHA-256 `6B991D86F5BAB4EC4DF65825EA3759D566377325A22D21FC97CBA393FEF6BBD6`.
- The source candidate remains unchanged and unaccepted. Runner receives only the clean execution projection, not source, source map, trial design, E-111, prior binding, or this binding.
- Trial scope is the complete natural S1 path to the method's creator-confirmation / S1 stop point. No actual S1→S2 handoff, W2/S2 start, or world-fact solving.
- This sample can support only historical-anchor regression evidence; it is not transfer evidence, formal method acceptance, or S2 authorization.

## 2. Runner-visible packet: exactly five items

SHA-256 covers the complete raw file bytes. Relative paths are from this binding's `attachments/` directory. The input card contains only the exact raw question; the other four items are the materials needed to execute S1.

| Artifact | Relative path | Bytes | SHA-256 |
|---|---|---:|---|
| S1 v0.18.5 clean execution projection v0.1.0 | `stage1-framing-method-v0.18.5-execution-projection-v0.1.0.md` | 58,415 | `CB71BA8A949E775CBD9C8E8FEB4F99CE1EC8E77E4D83A71E3890409D0BC0F13F` |
| Shared Research Core v0.1.0 | `../../GOAL-005-shared-research-loop/attachments/shared-research-loop-core-v0.1.0.md` | 8,094 | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema v0.1.0 | `../../GOAL-005-shared-research-loop/attachments/shared-research-record-schema-v0.1.0.md` | 5,922 | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |
| S1 Research Adapter v0.1.1 | `../../GOAL-005-shared-research-loop/attachments/s1-research-adapter-v0.1.1.md` | 5,812 | `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C` |
| Raw input card v0.1.0 | `s1-raw-question-input-v0.1.0.md` | 19 | `0F055FB9C915E116272BC676EF9BBF5768A752C02C9D6483D9CCF7049FC3ECCE` |

“Only raw Probe” means the raw card is the runner's only **case-specific initial content**. It does not withhold the method materials above. Runtime creator replies are added only if actually requested and are relayed under §5. Any research/tool information is acquired only if the method naturally calls for it.

## 3. Control-only identity and isolation references

These materials are not runner-visible. Their listed paths and hashes are for control-side preflight only.

| Artifact | Relative path | Bytes | SHA-256 | Use |
|---|---|---:|---|---|
| Bound v0.18.5 source candidate | `stage1-framing-method-integration-candidate-v0.18.5.md` | 96,103 | `6B991D86F5BAB4EC4DF65825EA3759D566377325A22D21FC97CBA393FEF6BBD6` | Method identity |
| Source→projection map v0.1.0 | `stage1-framing-method-v0.18.5-execution-projection-map-v0.1.0.md` | 4,504 | `5525C346A295DC7AA0B21EC1868E2B03B42CEB584D8232B4DFDDD03C90428140` | Projection fidelity; control-side only |
| Unchanged run-17 trial design v0.1.0 | `s1-historical-anchor-integrated-trial-design-run-17-v0.1.0.md` | 10,306 | `73A8752FEC73B8DE6E1F943E29EC059B137B6405B38DF622746799BE5C5E5A21` | Evaluation and post-run sequence |
| Accepted S1 isolated-trial context contract v0.1.3 | `s1-isolated-trial-context-contract-v0.1.3.md` | 7,285 | `76E2F4B289F32E78520E9D99EA8A84B76E130B970F61F6FB18CD6E0730CC293D` | Fresh-context and contamination rules |
| Audited generic-bootstrap manifest v0.1.1 | `run13-generic-bootstrap-context-manifest-v0.1.1.md` | 3,574 | `D882CBE6F960C6255B1E63BE84D85EFC5B3AA36FC874FC7595E5A02383D36ACC` | Audit/capture evidence only; run-13 launch procedure not imported |
| Captured global AGENTS bytes | `run12-global-agents-captured.md` | 13,638 | `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8` | Fixed audited bootstrap identity |
| Current generic bootstrap source (preflight observation) | `~/.codex/AGENTS.md` | 13,638 | `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8` | Reread and rehash before launch |
| Run-17 binding v0.1.0 | `s1-historical-anchor-integrated-trial-binding-run-17-v0.1.0.md` | 13,342 | `89219D7539CDF37B4B797C777AB9AC5165E1FE73EFF363BF2BC7698C5B9C258E` | Control-side precedent only |
| E-111 final preflight record | `../02-execution/E-111-run17-trial-package-preflight.md` | 2,917 | `FAB823B099F2F8C37E71D4B8064D9185E38E5479CD4AB2ED34C00D679FA9CF3F` | Frozen packet/provenance record |

For **run-19 only**, the exact captured content of `~/.codex/AGENTS.md` is allowed as generic bootstrap under S1 Isolated Trial Context Contract v0.1.3 and the accepted generic-bootstrap decision/user instruction. Its source is the current `~/.codex/AGENTS.md`, matched to `run12-global-agents-captured.md`; its permitted scope is general agent, role, and tool instruction, never case-specific Probe or method evidence. The captured 13,638-byte content was reviewed as generic and free of project, Probe, and run-specific facts; its binding SHA-256 is `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`. Before any future launch, control must reread the current `~/.codex/AGENTS.md`, confirm its raw byte length and SHA-256 match the captured identity, and recompute the complete source/projection/packet/design/isolation/bootstrap manifest. Stop on any mismatch. The run-13 manifest is audit/capture evidence for this content identity; its run-13-only launch procedure is not imported into run-19. This allowance adds no sixth runner packet item and permits no other global file. The unchanged run-17 trial design, E-111, and prior binding remain control-only; no new trial-design file is created for run-19.

Historical Probe/run/audit records (including run-15 trace and audits), old creator replies, workspace goal records, and all material that explains why this question is a historical anchor are **post-run-only control/reviewer material**. They are not packet items, must not be shared with or summarized to the runner, and are not to be shown to the creator before the creator's first product judgment. Post-run review may compare the current trace with historical behavior; no historical node list is the expected answer. Exact comparison references can be indexed in the post-run evidence matrix after the trial; this does not change runner inputs.

## 4. Fresh-context runner envelope

If and only if a later exact-hash authorization is granted, control creates one new subagent with a new invocation identity, not a resumed or reused prior runner, using the previously validated architecture and explicitly sets `fork_turns: none`. It is the sole runner and must not delegate. Root remains control/creator relay and does not pass parent conversation history.

Proposed runner task, verbatim:

> Please use the supplied S1 execution materials to process the raw question in the input card. You are the sole runner for this task; do not delegate. Follow the supplied method naturally. If a genuine creator decision is needed, ask control to relay the question to the creator. Stop at the method's S1 creator-confirmation / S1 stop point and preserve the complete available execution trace.

Do not add the trial label, historical context, old Probe/run/audit material, expected dimensions, observed failure modes, scoring criteria, hints to research/semantic zoom/coverage attack, or any other case-specific content. Do not pre-run a web-search smoke. If a research tool is naturally needed and unavailable, record the actual tool-access limitation without substituting a search requirement.

Allowed ambient context follows contract v0.1.3: system/platform context and the already audited generic bootstrap. Before a future launch, control checks that current `~/.codex/AGENTS.md` still matches the manifest hash. A new subagent's `fork_turns: none` is the fresh-context boundary; OS-level filesystem-deny proof is not required. Actual receipt or reading of unauthorized project/history-specific content invalidates the methodological context-isolation claim; theoretical filesystem capability alone does not.

## 5. Creator relay protocol

- The runner may ask only about genuine creator-owned decisions concerning intent, scope, interpretation, granularity, tradeoffs, or structure confirmation.
- Control sends the exact full question to the user/creator, then relays the creator's reply verbatim and in full, without summarizing, explaining, editing, or appending other parent context.
- Do not supply a creator answer on the user's behalf. Preserve the runner question, exact creator reply, and exact relay.
- The creator must not use old-run dimensions or prior method corrections as hints. Current genuine clarification or rejection remains valid creator input. If the creator reply itself contains a specific historical/method hint, preserve it and mark the affected autonomy judgment as creator-influenced; do not rewrite the trace or automatically invalidate unrelated behavior.
- At trial completion, first present the current final S1 artifact alone for the creator's product-level judgment. Do not show historical comparisons or prior replies before recording that judgment.

## 6. Run, trace, and post-run review sequence

1. Before any future start, recompute raw byte lengths and SHA-256 of every control/source/projection/packet/design/isolation/bootstrap artifact in §§1–3, including rereading the current `~/.codex/AGENTS.md` and matching the captured bytes. Stop on any mismatch. Recheck the generic bootstrap hash. Confirm the approved isolated context contract remains the applicable version.
2. Start one fresh-context runner and execute the complete S1 method naturally until its S1 endpoint. Research, semantic zoom, coverage attack, and research-return checks are not independent observation targets: follow v0.18.5's applicability conditions, perform any method-required step when applicable, and do not manufacture a condition only to make it observable. A path that does not apply or arise is recorded `N/A` / `not observed`.
3. Preserve the complete available runner task/envelope, packet identities, creator questions/replies/relays, outputs, and actual tool trace in a new run-19 trace record at `s1-historical-anchor-integrated-trial-run-19-runner-output-v0.1.0.md` (control-side archive path; not a runner input). At the normal S1 stop / creator-confirmation point, pause without method coaching. Do not edit or reconstruct missing trace; note visibility limits. If available initial context/tool payload cannot be exported, record that limitation as contract v0.1.3 requires.
4. After stop, obtain the creator's current-product judgment before exposing historical materials.
5. Then commission a fresh-context independent review. Reviewer may inspect current materials plus relevant history to determine whether prior failures recur. Historical structure is a comparator, never a mandated answer or completeness checklist.
6. Keep outcome disposition separate from mechanism observations and separate again from any method revision decision.

## 7. Outcome handling

- **Positive / usable sample:** Trace is sufficient; the runner reaches the S1 endpoint; creator finds the resulting structure understandable and usable for the intended later solving judgment; and independent review finds no material S1 boundary or applicable-rule failure. No particular optional mechanism, node count, research event, dimension, or historical match is required; any v0.18.5 step whose conditions are met remains applicable.
- **Material concern:** A visible failure materially prevents the structure from serving the creator's current intent, or shows unsupported demand change, creator-burdened decomposition, premature world-fact solving, or failure to stop under the method. Review separately whether this is execution regression or a method deficiency.
- **Inconclusive:** Missing evidence, unresolved creator scope, unavailable tool capability, or another limitation prevents a reliable overall product judgment. A conditional method path not occurring is not by itself inconclusive.
- **Invalidated for context contamination:** The runner actually received or read unauthorized project/probe/history-specific content. Preserve trace and identify the content/source. Mere access capability is not enough.

A historical-anchor positive result does not prove transfer, formal method acceptance, or permission to hand off. Revise v0.18.5 only if a material product failure is clear and fresh-context independent review concludes that the method itself is insufficient; an unattractive detail, one historical difference, or an untriggered mechanism is insufficient.

## 8. Binding state

Current state: `proposal / not-run / execution_authorization: not-granted`. This binding does not self-reference its own hash. Its final raw-byte SHA-256 is a separate control-side identity to calculate after writing; any later change requires a new preflight. The run-19 preparation request does not authorize execution. Recompute the entire manifest and binding hash at final preflight and obtain separate explicit creator execution authorization for this run-19 binding SHA. Prior binding SHA values are provenance, not run-19 authorization. Until then, do not spawn or prompt the run-19 runner.
