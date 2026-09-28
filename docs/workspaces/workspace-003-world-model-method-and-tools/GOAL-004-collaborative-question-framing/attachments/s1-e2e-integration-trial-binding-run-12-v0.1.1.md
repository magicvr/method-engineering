---
title: S1 end-to-end integration trial binding · run-12
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.1
id: GOAL-004-collaborative-question-framing
trial_status: prepared-not-run
execution_authorization: not-granted
---

# S1 end-to-end integration trial binding · run-12 · v0.1.1

This control-side binding fixes the exact material identities and separation rules for a possible isolated S1 end-to-end trial. It records preparation only. **Run-12 has not started and is not authorized to run.** Acceptance of this binding and the other requested artifacts, followed by a separate explicit execution authorization, is required before any runner starts.

This v0.1.1 supersedes run-12 binding v0.1.0. The earlier binding SHA-256 `1A7548CECE0832A208150EECE6007522F6479CD3723DAA41219575E7D195A6EC` is obsolete and is not an execution-authorization identity.

## 1. Trial identity and scope

- **Run ID**: `run-12`.
- **Purpose**: one isolated S1 behavior sample of the v0.18.0 integration candidate, combining the v0.17.2 semantic-zoom host line with the previously run-tested S1 research-loop call/return semantics.
- **Probe**: exactly the single question in [raw input card v0.1.0](s1-integration-trial-input-card-v0.1.0.md): “为什么这个世界仍然需要城市？”
- **No setting facts or expected content** are supplied with the probe. No mechanism, taxonomy, candidate answer, source, query, or search direction is fixed.
- **Trial result type**: a single behavior sample only. It cannot establish general validity, target-world truth, exhaustive coverage, method acceptance, or an effective/authorized handoff.

## 2. Immutable artifact manifest

Hashes are SHA-256 over the exact UTF-8 file bytes. `runner-visible` files alone make up the packet; control-side files must not be sent to or opened by the runner.

| Artifact | Exact path relative to this folder | Identity and disposition | SHA-256 |
|---|---|---|---|
| Integrated S1 method source candidate | `stage1-framing-method-integration-candidate-v0.18.0.md` | v0.18.0, draft/unaccepted; control-side review source, not runner input | `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3` |
| Clean execution projection | `stage1-framing-method-v0.18.0-execution-projection-v0.1.0.md` | projection v0.1.0 of the candidate; runner-visible method text | `4C46CB78BC2E13F63CA91FB584D51966642BEFCFD8A8C0613B4C6F9E021CE8E8` |
| Projection map | `stage1-framing-method-v0.18.0-execution-projection-map-v0.1.1.md` | control-side map from candidate sections to projection | `4CB2664DEADC6EE672B3BE3625361A26B0381176A0A3C68DFFE2B63999C89BAE` |
| Raw input card | `s1-integration-trial-input-card-v0.1.0.md` | runner-visible; contains only the probe question | `28E676D6D59459304DD2CF48B31C91B10B71B5DB3106A39DD429A4F7A88CA028` |
| Trial design | `s1-e2e-integration-trial-design-v0.1.1.md` | v0.1.1, control-side observation/evidence boundaries; not runner input | `35011BA1451137AB9BBFCD3CE5FC464A5676ED2830EE8D457F3B828CF61212EC` |
| Shared Research Core | `../../GOAL-005-shared-research-loop/attachments/shared-research-loop-core-v0.1.0.md` | v0.1.0, creator-accepted research-process design baseline; runner-visible dependency; not host integration/validation evidence | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema | `../../GOAL-005-shared-research-loop/attachments/shared-research-record-schema-v0.1.0.md` | v0.1.0, creator-accepted component design baseline per GOAL-005 D-006; runner-visible dependency; not trial validation | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |
| S1 Research Adapter | `../../GOAL-005-shared-research-loop/attachments/s1-research-adapter-v0.1.1.md` | v0.1.1, draft/unaccepted; used for the one accepted run-02 behavior sample under D-015; runner-visible dependency; semantic content carried forward unchanged | `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C` |

### Control-only evaluation/provenance identities

These files establish design lineage, prior evidence, or reviewer-only evaluation criteria; do not show them to the runner or use them as probe context.

| Exact source path relative to this folder | Role/status | SHA-256 |
|---|---|---|
| `stage1-framing-method-candidate-v0.17.2.md` | Frozen next S1 trial baseline; draft/unaccepted; sole method base of v0.18.0 | `FA404A5C3DB7265CB2615AF8040C953739006DE1D4F3B1540D5D5A902CB32940` |
| `stage1-framing-method-candidate-v0.16.3.md` | Draft/unaccepted source of the Rule E research-admission and Rule B call/return semantics; used as S1 host only for run-02 under D-015 | `E55C50722A909293B0BA483F0F67D35CE027B8ECBF6518DE1C0190DD83D52D96` |
| `../../GOAL-005-shared-research-loop/attachments/s1-independent-call-trial-run-02.md` | One accepted, bounded behavior sample (D-016; A-003 ACCEPT WITH NOTES), not a general validation claim | `677C815F4B93A63A88F115437B4EB4FCFF80F013615E578820FE82C90FDCA1B3` |
| `../../GOAL-005-shared-research-loop/attachments/s1-independent-call-trial-binding-run-02-v0.1.0.md` | D-015 one-call binding; v0.16.3 and adapter v0.1.1 were run-specific, not general host/adapter baselines | `4AF1DEB60A02BADED98A017F3C2C7B01DD9FD7E419426D7FD68B0A4BB7ECA63D` |
| `../02-execution/E-064-clarify-frozen-contract-case-snapshot.md` | Control-side record that the frozen contract's case-status sentence is a freeze-time snapshot | `DE817BF230C06054B42BD9F16589C1FD20C8918B2A424FFFBA72D81470DE57AB` |
| `s1-to-s2-handoff-contract-v0.1.1.md` | v0.1.1, frozen interface contract; reviewer-only normative evaluation reference, never runner-visible | `E14B6E8CF2824DA1423F5F07B347CDBDE32ADB854000791D50DCD69C8F0B53C9` |

Before any future execution, recompute every manifest hash from the listed exact files. Any mismatch invalidates this binding until it is corrected and re-reviewed. Do not silently follow a same-named replacement file.

## 3. Runner packet and isolation

The runner receives exactly these artifacts:

1. the clean execution projection;
2. Shared Research Core v0.1.0;
3. Shared Research Record Schema v0.1.0;
4. S1 Research Adapter v0.1.1;
5. the raw input card.

The source candidate, projection map, this binding, trial design, E-064, frozen S1→S2 contract, run-11 material, previous probes/transcripts/audits, GOAL-005 run-02 records, other workspace files, and conversation history are control-side and must not be provided as runner context. Start from a fresh isolated runner context containing only the packet above. If such context separation cannot be achieved, do not run and do not relabel a context-contaminated run as isolated. The method projection's inline contract citation is not permission to read the absent contract or any workspace file.

After the runner stops, the reviewer uses the exact frozen contract v0.1.1 for a trial-only content-fit judgment. Apply only its normative interface rules; its §1 sentence describing the case state at the time of freezing is historical, not current state, as directed in E-064. This clarification does not alter contract semantics.

External research tools may be used only if the actual S1/adapter conditions call for a bounded research task. Tool availability is not a trigger. If no material external-knowledge unknown appears, do not search. If research is triggered, record actual tool/source access and preserve the shared schema evidence trail; no predetermined query, source, mechanism, taxonomy, or source count is supplied.

## 4. Required observation coverage

The control-side reviewer uses the design's observation chain over the actual trace:

`original question → active framing → semantic zoom if genuinely needed → unknown and owner → research if genuinely triggered → evidence return → Rule E/F/G → coverage convergence → creator confirmation → reviewer-side contract-content fit`.

Record each branch as `triggered`, `not triggered with trace-grounded reason`, or `unobserved/incomplete`. A non-trigger is not proof that the corresponding capability works; forcing a trigger is a protocol failure. If research occurs, evaluate source quality, provenance, claim support, applicability/transfer, limits, synthesis, and residual unknowns. External evidence may support candidate relevance, general mechanisms, or analysis; it never establishes facts about this probe's target world. All returned material goes back through existing Rule E/F/G, not a parallel structure-adjudication path.

The creator makes only real intent/context decisions, the method's supported three-state node-grain decisions, and the method-required structure confirmation. Do not ask the creator to invent or enumerate child questions. Preserve exact creator replies and pause rather than answer for them.

## 5. Stop and authority boundary

The runner stops at the S1 end-state after method-required creator confirmation. Only then does the reviewer assess content fit with the frozen handoff contract. If creator input is pending, mark the run incomplete. If isolation or artifact identity fails, do not proceed as a valid run.

This binding does **not** authorize or permit:

- starting run-12;
- actual S1→S2 transfer, independent node transfer, or automatic S2 start;
- W2/S2 modeling or an S2 research-loop call/trial;
- accepting v0.18.0 as a method or claiming integrated validation;
- opening another probe or expanding into an unbounded global search.

Execution requires a separate explicit creator authorization after review and acceptance of the audit, candidate, and complete design/binding package with all hashes verified. Until then, trial status remains `prepared-not-run`.
