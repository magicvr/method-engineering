---
title: S1 end-to-end integration trial design
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.1
id: GOAL-004-collaborative-question-framing
---

# S1 end-to-end integration trial design · v0.1.1

> Control-side design only. Do not provide this file to the runner. It defines observation boundaries for a future isolated trial; it does not authorize execution or add method rules.

## 1. Purpose and evidence boundary

Design one isolated end-to-end S1 behavior sample for the integration candidate composed from semantic zoom and the previously run-tested S1 research-loop line. The trial should show whether the two capabilities can coexist in one S1 run while returning decisions to the host's existing Rule E/F/G.

This is not a repeat single-subsystem test. Observe the actual path from the original question through framing, any naturally triggered local refinement, unknown ownership, any naturally triggered research, evidence return, Rule E/F/G processing, coverage convergence, and creator confirmation. After the runner stops, a reviewer makes a separate trial-only assessment of content fit with the frozen S1→S2 handoff contract.

Semantic zoom and external research are **conditional branches**. Their absence is neither failure nor success for the unobserved capability. The runner must not create a family node, research unknown, search query, mechanism, or candidate answer merely to cover this design. If a branch does not naturally trigger, record that its behavior was not observed.

This one-probe sample cannot establish general method validity, reliable operation across cases, truth of any target-world claim, completeness of a problem structure, accepted status of the integration candidate, or authorization to hand off or start S2.

## 2. Probe and runner-visible packet

The complete raw probe is the single question in [input card v0.1.0](s1-integration-trial-input-card-v0.1.0.md):

> 为什么这个世界仍然需要城市？

No setting facts, mechanisms, taxonomy, candidate answer, source suggestion, search direction, or prior structure are added to that card.

The runner-visible packet consists only of:

1. a clean execution projection that preserves the candidate's operative method text but omits development history and prior-case material;
2. that candidate's explicitly bound Shared Research Core, Shared Research Record Schema, and S1 Research Adapter documents needed to use the method;
3. the raw input card above.

The v0.18.0 integration candidate remains the source identity for review and binding; the projection must map to it by exact section and preserve all normative text. The projection mapping, source candidate, and frozen S1→S2 contract are control-side files, not runner inputs. The runner is not asked to judge contract fit.

After the runner has stopped, the reviewer applies the frozen contract's normative interface rules to the recorded S1 output. Its §1 freeze-time case-status sentence is a historical snapshot, not current case state, per the user's prior direction recorded in [E-064](../02-execution/E-064-clarify-frozen-contract-case-snapshot.md).

The trial design, binding/control file, observation matrix, source candidate and its provenance/history, projection map, frozen contract, E-064, previous transcripts, audits, and other goal files are control-side materials and must not be shown to the runner. The projection retains the method's inline citation to the frozen contract, but the contract file is absent from the runner packet and unavailable in the isolated context; that citation does not authorize reading workspace files, source history, prior cases, the contract, or conversations for probe context.

## 3. Roles and interaction

- **Runner**: starts from a clean session and processes only the runner-visible packet. It may use external research tools when the candidate and adapter's actual conditions call for them; tool availability is not a search requirement. The runner stops after method-required creator confirmation and receives no frozen contract.
- **Supervisor**: binds and verifies the packet, preserves the complete turn and tool trace, and does not add hints, search directions, expected observations, or candidate structures during execution. After the runner stops, the supervisor provides the output and frozen contract to the reviewer only.
- **Creator**: supplies corrections to their intent/context and makes genuine authorial choices. When the method asks for node granularity, the supported choices remain: accept and keep current grain; accept the node and continue one local expansion; or reject the node. The creator is not asked to list child questions. The creator separately confirms or declines a presented candidate structure when required by the method.
- **Reviewer**: after the runner stops, reviews the raw trace and S1 output against the frozen contract to make a trial-only contract-content-fit judgment. The reviewer does not add facts or answers to the runner input.

When the runner needs a real creator decision, it pauses and waits. The supervisor must not answer, supplement world facts, nudge a particular choice, or interpret silence as confirmation. Preserve each actual creator reply verbatim with its time/order and distinguish it from runner inference. If the session is paused for a pending reply, classify the trial as incomplete so far.

## 4. Control-side observation chain

The following are review prompts, not a checklist for the runner and not new execution steps. The actual reasoning may loop or revisit earlier points; do not require a fixed order where the method does not. Contract-content fit is evaluated separately after the runner stops.

| Observation point | Evidence to retain |
|---|---|
| Original question → active framing | Ambiguities/interpretations and consequences, analysis products, exclusions, boundary decisions, and whether necessary creator questions came only after analysis. |
| Node grain and semantic zoom | Whether the runner independently identified a node that might still be a problem family, with its evidence and uncertainty; if relevant, whether it generated, compared, and attacked child structures before asking the creator; the exact creator choice; and any one-layer recursion. |
| Unknown and owner | The actual unknown, why it affects the current problem/model decision, its type and owner, next state, and whether it is external-research-suitable, creator-owned, objective target-world work, or resolvable by reasoning from current inputs. |
| Conditional research call | If called, the pre-call research question, bounded purpose/scope, owner and affected structure location; source choice and collection trace; no hindsight-based requirements added after return. If not called, the observed reason no genuine external gap required the loop. |
| Evidence appraisal and return | Source/claim provenance, source quality, support and limits, applicability/transfer rationale, and remaining unknowns under the bound Schema; external evidence may support candidate relevance, general mechanisms, or analysis, but does not establish the target world's facts. |
| Rule E/F/G processing | Rule E's current-input anchor, explicit relevance link, structural contribution, negation/redundancy/containment checks, and “question admitted, answer unresolved” boundary; Rule F's B1/B2/B3 owner and next state; Rule G's local or global coverage work, incremental changes, convergence evidence, residuals, and return triggers. |
| Creator confirmation | What exact candidate structure and scope were shown, what the creator actually confirmed or declined, and which answers/facts remain unconfirmed. Structural confirmation must not be treated as an answer or objective-world fact. |
| Reviewer-side contract-content fit | After runner stop, whether the recorded S1 output can be checked against the frozen v0.1.1 contract, including confirmed nodes, F.2-form B3 items, B1/B2 boundaries, S1-held context vs non-blocking residuals, coverage/closure evidence, research evidence boundaries, and scope/trigger records. The runner neither reads nor judges the contract. |

## 5. Conditional trigger and non-trigger observations

### Semantic zoom

Observe a trigger only where the runner identifies a current node that may remain a problem family and supports that concern from the current structure. If the creator chooses further expansion, check that the runner generates, compares, and attacks candidate child structures itself, expands only the requested local scope, and reuses the same E/F/G process. Check upward propagation only when the existing G.1.3 relation to the parent is evidenced; local recursion must not restart global coverage without such evidence.

Record non-trigger when the current candidate nodes are already handoff-ready in grain, no supported family concern appears, or the creator chooses to keep the grain. If an unexpanded node remains too coarse, record it as not ready/S1-held as applicable; absence of recursion cannot waive a method or contract boundary.

### Shared research loop

Observe a trigger only when a specific external-knowledge unknown is material to the next S1 judgment, outside inference from the current input, and could be meaningfully informed by appropriate external sources. It must not be merely a creator preference or a target-world fact that evidence about other worlds cannot establish. Before any call, retain the question, affected point, current owner, use standard, and bounded work as supplied by the candidate/adapter.

Record non-trigger when no genuine external gap appears, when current-input reasoning can resolve the S1 framing, when the unresolved matter belongs to creator choice, or when the remaining objective target-world answer belongs to later solving. The rationale should be grounded in the actual trace; the runner need not prove that every conceivable search is unnecessary.

If either conditional branch does not trigger, report **not observed** for that branch. Do not claim the corresponding capability passed, and do not classify the absence itself as method failure.

## 6. Evidence boundaries for any research that occurs

Use the exact Core, Schema and S1 adapter identities in the binding. The runner may use the actual external tools available to it for a triggered, bounded call; record tool/source access honestly. Context isolation is not a claim that platform tools are technically disabled.

When evidence returns, check the distinctions already required by the bound method/components:

- external source claims vs. runner inferences vs. target-world claims;
- support for a candidate question's relevance or a general mechanism vs. proof that a condition holds in the particular target world;
- retrieved evidence vs. host disposition under Rule E;
- Core outcome vs. candidate admission, unresolved-answer ownership, or Rule G convergence.

Research does not establish target-world fact, auto-admit a candidate, resolve a B2 framing question, close a B3 answer, substitute for coverage, or authorize S2. Do not add or require a new schema field.

## 7. Handoff check and stopping boundary

The runner should reach an explainable S1 end state and obtain any method-required creator confirmation, then stop without reading or applying the handoff contract. Afterward, the reviewer makes a trial-only judgment about whether the candidate structure's contents align with the frozen [S1→S2 contract v0.1.1](s1-to-s2-handoff-contract-v0.1.1.md), using its normative rules and treating the freeze-time case-status sentence as historical per E-064. This is not an effective or authorized handoff: the integration candidate remains draft/unaccepted, the trial package is not run-authorized, and the contract requires applicable gates plus separate authorization.

The runner portion ends after the candidate structure has received the method-required creator confirmation. The overall trial assessment is complete only after the reviewer records contract-content fit. Pause as incomplete while awaiting a real creator response or a material access issue. Report separately:

1. **execution state**: completed, paused for creator input, blocked by access, or invalidated by leakage/contamination;
2. **observed behavior**: what worked, deviated, or was not observed, including whether each conditional branch actually triggered;
3. **contract-content fit**: whether candidate material conforms, does not conform, or cannot yet be judged against contract content;
4. **authority boundary**: no actual S1→S2 transfer, no independent node transfer, no W2/S2 start, and no method acceptance from a single run.

No forced number of turns, search calls, or node expansions is introduced. Do not continue into S2 or invent missing confirmations to make the run look complete.

## 8. Explicit exclusions

- No reuse of “世界有多大” as the probe; no prior run-11 case structure or output is runner-visible.
- No fixed research step, required search, predetermined source, query, mechanism, taxonomy, or city explanation.
- No prompt to force semantic zoom or make both conditional branches fire.
- No Rule E/F/G redesign, new child-decomposition method, or extension of the handoff contract.
- No handoff contract in the runner packet; no actual transfer, node-level independent transfer, S2 research-loop call/trial, W2/S2 solving, or second probe.
- No claim that this design or any source version validates the integrated candidate.

## 9. Not authorized by this package

This document and its [run-12 binding](s1-e2e-integration-trial-binding-run-12-v0.1.1.md) are preparations for creator review only. No runner is to be started from this design. Execution requires a separate explicit authorization tied to the completed, hash-verified candidate, execution projection, projection map, dependencies, control-side contract, input, and control binding. If a required issue is identified in the candidate or package before execution, resolve it before asking for run authorization.
