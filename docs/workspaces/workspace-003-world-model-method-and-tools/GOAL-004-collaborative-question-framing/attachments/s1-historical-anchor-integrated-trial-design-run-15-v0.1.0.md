---
title: S1 historical-anchor integrated operational trial design · run-15
status: draft
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-trial-design-proposal
trial_status: proposal-for-creator-review
---

# S1 Historical-Anchor Integrated Operational Trial Design · run-15 · v0.1.0

> Control-side design only. This document, the binding, source map, and historical records must not enter the runner context. This proposal does not authorize execution.

## 1. Purpose and evidence boundary

Use frozen S1 v0.18.2 to run the original real ambiguous question again as one complete S1 operation. The question is **「世界有多大？」**. The trial asks whether the integrated method can, on this input, frame the creator's actual demand without making the creator do the decomposition, inventing a setting, answering world facts prematurely, changing the demand, or continuing without a bounded stop.

This is a **historical-anchor regression**, not a blind transfer test. It can provide evidence about this method version's behavior on the original question. It cannot establish general transfer to new questions or formal S1 acceptance. Historical runs may be consulted by control/reviewer only after the current runner has stopped and the creator has first judged the current product.

Frozen method identity: `stage1-framing-method-integration-candidate-v0.18.2.md`, SHA-256 `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6`. Do not change the method for this trial.

## 2. Probe and runner input boundary

The runner's **only case-specific initial input** is the exact raw question in the neutral input card: `世界有多大？`. It is not given any prior clarification, creator answer, historical structure, intended dimension, failure description, expected result, or search direction.

The runner must also receive the S1 execution materials required to perform the method: the clean v0.18.2 execution projection, Shared Research Core, Shared Research Record Schema, and S1 Research Adapter. Thus “only raw Probe” means only raw Probe as case-specific content; it does not mean withholding the method packet.

Do not place any prior run, audit, source candidate, source-to-projection map, design, binding, handoff contract, or control-side note in the runner packet. The runner task must not identify this as a historical-anchor/regression trial or show the evaluation criteria.

## 3. Isolated execution and natural method paths

Use the already accepted fresh-context subagent architecture under S1 Isolated Trial Context Contract v0.1.3: one new subagent with `fork_turns: none` is the sole runner and does not delegate. The control agent handles creator relays and preserves the trace. The permitted generic bootstrap is the previously audited, hash-fixed context in the existing bootstrap manifest. Filesystem sharing or theoretical read capability alone is not contamination; judge actual injected or read project/history-specific content from the trace, as the contract specifies.

Run the complete S1 method naturally to its creator-confirmation / S1 stop point. If creator decisions require another method-permitted S1 turn, continue within that method path; stop at its defined S1 endpoint. Do not add an extra iteration for trial completeness. Do not make an actual S1→S2 handoff, invoke W2/S2, or solve the world question.

Research, semantic zoom, coverage attacks, and research-return Demand Preservation are not separate observation targets. Follow v0.18.2's own applicability conditions: perform every step the method requires when its conditions hold, and do not manufacture a condition or add a step only to make it observable. If a conditional path is not applicable or does not arise naturally, record `N/A` / `not observed`; its absence is not a failure. No pre-run research smoke, forced search, mechanism checklist, or hint is allowed.

## 4. Creator interaction

The creator may answer only genuine questions about current creative intent, scope, reading, tradeoffs, or structure confirmation. The control agent must relay each creator reply verbatim and in full, without summary, explanation, rewriting, or additional parent-context material. Preserve both the original question and exact relay.

Do not use old creator replies or historical method corrections. Do not coach B1/B2/B3 classification, suggest research, identify a missing dimension, prescribe a semantic-zoom action, or otherwise help the runner pass. The creator's genuine current correction or rejection is legitimate evidence about product fit. If a reply itself introduces a specific historical structure or method hint, preserve it and mark the affected autonomy judgment as creator-influenced; creator familiarity with the case alone does not invalidate the run.

## 5. Product-level evaluation

Evaluate the final S1 product, not whether particular internal mechanisms fired. The post-run control/reviewer should judge from the trace and creator's first product review whether:

1. AI did the framing and candidate-structure work rather than asking the creator to list subproblems.
2. The structure tracks the creator's actual clarified intent and does not silently substitute a different question.
3. It avoids unsupported setting assumptions and uncontrolled candidate overgeneration.
4. It keeps S1 framing separate from S2's objective modeling/solving and does not assert world facts as established.
5. It notices material structural distinctions that affect what must be answered, without being required to prove exhaustive coverage or reproduce any historical node list.
6. It converges and stops within the method's rules; “not proven exhaustive” alone is not a failure.
7. The creator can understand and confirm the resulting structure, with any genuine correction recorded.
8. The resulting questions make clear what a later solving stage would need to answer, without granting actual handoff or starting S2.

Record Rule E/F/G behavior, semantic zoom, research-loop, coverage attack, and Demand Preservation only as explanatory observations when applicable. A conditional path that does not apply or arise is `N/A` / `not observed`; it is not a negative score. Any v0.18.2 step whose applicability conditions are met remains part of the method and must still be followed. No particular number or shape of nodes is a pass condition.

## 6. Disposition and revision threshold

- **Positive / usable sample:** The trace is sufficient; the runner reaches its S1 endpoint; the creator's first review finds the structure understandable and usable for the intended next solving judgment; and no material S1 boundary or method-rule failure is identified. Minor presentational imperfections do not automatically negate this outcome.
- **Material concern:** The current product cannot serve the creator's actual demand, or a material failure such as unsupported scope change, creator-burdened decomposition, premature world-fact solving, or unbounded continuation is visible. This is a trial concern, not by itself proof that the method text is deficient.
- **Inconclusive:** Missing trace, unavailable evidence, unresolved creator scope, or another limitation prevents the main product judgment. Non-trigger of a conditional mechanism alone does not make the overall trial inconclusive.
- **Invalidated for context contamination:** Trace shows the runner actually received or read unauthorized project/probe/history-specific content. Mere filesystem capability is not sufficient.

If the runner failed to follow an existing v0.18.2 rule, record execution regression. Consider a method revision only if the material product failure is clear and a fresh-context independent review concludes the accepted method is insufficient to prevent it. Do not revise the method for a merely unattractive detail or an untriggered mechanism.

## 7. Post-run order and retained evidence

1. Stop and preserve the full available runner/creator/tool trace without edits.
2. Before showing the creator old runs, audits, or historical comparisons, ask for the creator's product-level judgment on the current final S1 artifact. Preserve the reply verbatim.
3. Only after that judgment, commission a fresh-context independent review. The reviewer may compare the current trace against historical runs and audits to determine whether prior failures recur; historical structures are comparators, not a gold answer or mandatory checklist.
4. Keep trial disposition, execution-regression assessment, and any later method-finding closure separate. No actual handoff, W2/S2, or world-fact solution is part of this trial.

Save the complete available runner task/envelope, packet identities, verbatim creator relay, runner output, available tool trace, and post-run creator/reviewer records. Do not reconstruct unavailable trace after the fact; record visibility limits.

## 8. Status

This v0.1.0 design is submitted for creator review. It is not an execution binding and does not start a runner. The attached draft binding fixes a proposed packet and control boundary for review; it remains `not-run` and `execution_authorization: not-granted` until the creator accepts the final binding identity and separately authorizes execution.
