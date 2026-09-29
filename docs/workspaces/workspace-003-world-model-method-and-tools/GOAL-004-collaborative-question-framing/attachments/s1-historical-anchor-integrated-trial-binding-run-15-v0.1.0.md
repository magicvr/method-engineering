---
title: S1 historical-anchor integrated operational trial binding · run-15
status: draft
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-draft-trial-binding
trial_status: not-run
execution_authorization: not-granted
---

# S1 Historical-Anchor Integrated Operational Trial Binding · run-15 · v0.1.0

**DRAFT / CREATOR REVIEW ONLY.** This file identifies a proposed trial packet and control protocol. It is not an execution authorization. Do not create or prompt the runner from this draft. If accepted, recompute the complete manifest and final binding SHA-256, submit that exact identity, and wait for separate execution authorization.

## 1. Fixed identity and scope

- Proposed Run ID: `run-15` (next sequential trial identifier; not started).
- Trial kind: historical-anchor integrated operational trial, using the original raw question `世界有多大？`.
- Frozen S1 source: `stage1-framing-method-integration-candidate-v0.18.2.md`, 83,348 bytes, SHA-256 `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6`.
- The source candidate remains unchanged and unaccepted. Runner receives only the clean execution projection, not source, source map, trial design, or this binding.
- Trial scope is the complete natural S1 path to the method's creator-confirmation / S1 stop point. No actual S1→S2 handoff, W2/S2 start, or world-fact solving.
- This sample can support only historical-anchor regression evidence; it is not transfer evidence, formal method acceptance, or S2 authorization.

## 2. Runner-visible packet: exactly five items

SHA-256 covers the complete raw file bytes. Relative paths are from this binding's `attachments/` directory. The input card contains only the exact raw question; the other four items are the materials needed to execute S1.

| Artifact | Relative path | Bytes | SHA-256 |
|---|---|---:|---|
| S1 v0.18.2 clean execution projection v0.1.0 | `stage1-framing-method-v0.18.2-execution-projection-v0.1.0.md` | 49,257 | `6F8F5467E25ABEFF55B13B79287BFDCB60931CA2F2CB31AD250FD8A914D40904` |
| Shared Research Core v0.1.0 | `../../GOAL-005-shared-research-loop/attachments/shared-research-loop-core-v0.1.0.md` | 8,094 | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema v0.1.0 | `../../GOAL-005-shared-research-loop/attachments/shared-research-record-schema-v0.1.0.md` | 5,922 | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |
| S1 Research Adapter v0.1.1 | `../../GOAL-005-shared-research-loop/attachments/s1-research-adapter-v0.1.1.md` | 5,812 | `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C` |
| Raw input card v0.1.0 | `s1-historical-anchor-input-card-world-size-v0.1.0.md` | 19 | `0F055FB9C915E116272BC676EF9BBF5768A752C02C9D6483D9CCF7049FC3ECCE` |

“Only raw Probe” means the raw card is the runner's only **case-specific initial content**. It does not withhold the method materials above. Runtime creator replies are added only if actually requested and are relayed under §5. Any research/tool information is acquired only if the method naturally calls for it.

## 3. Control-only identity and isolation references

These materials are not runner-visible. Their listed paths and hashes are for control-side preflight only.

| Artifact | Relative path | Bytes | SHA-256 | Use |
|---|---|---:|---|---|
| Frozen v0.18.2 source | `stage1-framing-method-integration-candidate-v0.18.2.md` | 83,348 | `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6` | Method identity |
| Source→projection map v0.1.0 | `stage1-framing-method-v0.18.2-execution-projection-map-v0.1.0.md` | 5,456 | `D89C84D5B4A060F8FBB71F3662C3D32A44B71DF1BF04AE0A338C157E910D71F2` | Projection fidelity; control-side only |
| Trial design v0.1.0 | `s1-historical-anchor-integrated-trial-design-run-15-v0.1.0.md` | 9,326 | `6E78DCAD6E4F5CB24E57B6CD30B530E850925865E1FBB1877DE7D16F48482AFC` | Evaluation and post-run sequence |
| Accepted S1 isolated-trial context contract v0.1.3 | `s1-isolated-trial-context-contract-v0.1.3.md` | 7,285 | `76E2F4B289F32E78520E9D99EA8A84B76E130B970F61F6FB18CD6E0730CC293D` | Fresh-context and contamination rules |
| Audited generic-bootstrap manifest v0.1.1 | `run13-generic-bootstrap-context-manifest-v0.1.1.md` | 3,574 | `D882CBE6F960C6255B1E63BE84D85EFC5B3AA36FC874FC7595E5A02383D36ACC` | Allow-listed generic bootstrap |
| Captured global AGENTS bytes | `run12-global-agents-captured.md` | 13,638 | `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8` | Fixed audited bootstrap identity |

Historical Probe/run/audit records, old creator replies, workspace goal records, and all material that explains why this question is a historical anchor are **post-run-only control/reviewer material**. They are not packet items, must not be shared with or summarized to the runner, and are not to be shown to the creator before the creator's first product judgment. Post-run review may compare the current trace with historical behavior; no historical node list is the expected answer. Exact comparison references can be indexed in the post-run evidence matrix after the trial; this does not change runner inputs.

## 4. Fresh-context runner envelope

If and only if a later exact-hash authorization is granted, control creates one new subagent using the previously validated architecture and explicitly sets `fork_turns: none`. It is the sole runner and must not delegate. Root remains control/creator relay and does not pass parent conversation history.

Proposed runner task, verbatim:

> Please use the supplied S1 execution materials to process the raw question in the input card. You are the sole runner for this task; do not delegate. Follow the supplied method naturally. If a genuine creator decision is needed, ask control to relay the question to the creator. Stop at the method's S1 creator-confirmation / S1 stop point and preserve the complete available execution trace.

Do not add the trial label, historical context, old Probe/run/audit material, expected dimensions, observed failure modes, scoring criteria, hints to research/semantic zoom/coverage attack, or any other case-specific content. Do not pre-run a web-search smoke. If a research tool is naturally needed and unavailable, record the actual tool-access limitation without substituting a search requirement.

Allowed ambient context follows contract v0.1.3: system/platform context and the already audited generic bootstrap. Before a future launch, control checks that current `~/.codex/AGENTS.md` still matches the manifest hash. A new subagent's `fork_turns: none` is the fresh-context boundary; OS-level filesystem-deny proof is not required. Actual receipt or reading of unauthorized project/history-specific content invalidates the methodological context-isolation claim; theoretical filesystem capability alone does not.

## 5. Creator relay protocol

- The runner may ask about actual creator intent, scope, interpretation, tradeoffs, or structure confirmation.
- Control sends the exact full question to the user/creator, then relays the creator's reply verbatim and in full, without summarizing, explaining, editing, or appending other parent context.
- Do not supply a creator answer on the user's behalf. Preserve the runner question, exact creator reply, and exact relay.
- The creator must not use old-run dimensions or prior method corrections as hints. Current genuine clarification or rejection remains valid creator input. If the creator reply itself contains a specific historical/method hint, preserve it and mark the affected autonomy judgment as creator-influenced; do not rewrite the trace or automatically invalidate unrelated behavior.
- At trial completion, first present the current final S1 artifact alone for the creator's product-level judgment. Do not show historical comparisons or prior replies before recording that judgment.

## 6. Run, trace, and post-run review sequence

1. Before any future start, recompute the hashes of all five packet items and the source→projection identities above. Stop on any mismatch. Recheck the generic bootstrap hash. Confirm the approved isolated context contract remains the applicable version.
2. Start one fresh-context runner and execute the complete S1 method naturally until its S1 endpoint. Research, semantic zoom, coverage attack, and research-return checks are not independent observation targets: follow v0.18.2's applicability conditions, perform any method-required step when applicable, and do not manufacture a condition only to make it observable. A path that does not apply or arise is recorded `N/A` / `not observed`.
3. Preserve the complete available runner task/envelope, packet identities, creator questions/replies/relays, outputs, and actual tool trace. Do not edit or reconstruct missing trace; note visibility limits. If available initial context/tool payload cannot be exported, record that limitation as contract v0.1.3 requires.
4. After stop, obtain the creator's current-product judgment before exposing historical materials.
5. Then commission a fresh-context independent review. Reviewer may inspect current materials plus relevant history to determine whether prior failures recur. Historical structure is a comparator, never a mandated answer or completeness checklist.
6. Keep outcome disposition separate from mechanism observations and separate again from any method revision decision.

## 7. Outcome handling

- **Positive / usable sample:** Trace is sufficient; the runner reaches the S1 endpoint; creator finds the resulting structure understandable and usable for the intended later solving judgment; and independent review finds no material S1 boundary or applicable-rule failure. No particular optional mechanism, node count, research event, dimension, or historical match is required; any v0.18.2 step whose conditions are met remains applicable.
- **Material concern:** A visible failure materially prevents the structure from serving the creator's current intent, or shows unsupported demand change, creator-burdened decomposition, premature world-fact solving, or failure to stop under the method. Review separately whether this is execution regression or a method deficiency.
- **Inconclusive:** Missing evidence, unresolved creator scope, unavailable tool capability, or another limitation prevents a reliable overall product judgment. A conditional method path not occurring is not by itself inconclusive.
- **Invalidated for context contamination:** The runner actually received or read unauthorized project/probe/history-specific content. Preserve trace and identify the content/source. Mere access capability is not enough.

A historical-anchor positive result does not prove transfer, formal method acceptance, or permission to hand off. Revise v0.18.2 only if a material product failure is clear and fresh-context independent review concludes that the method itself is insufficient; an unattractive detail, one historical difference, or an untriggered mechanism is insufficient.

## 8. Binding state

Current state: `draft / not-run / execution_authorization: not-granted`. The current file hash identifies this review proposal only. If the creator accepts the design/binding, recompute the entire manifest and binding hash, perform the final control-side preflight, and request explicit authorization for that exact final binding SHA. Until then, do not spawn or prompt the run-15 runner.
