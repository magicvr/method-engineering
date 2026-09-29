---
title: run-14 control-side trial inference correction
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-trial-inference-correction
run_id: run-14
---

# run-14 Control-side Trial Inference Correction · v0.1.0

## Purpose and boundary

This control-side correction applies the creator's necessity check to inferences from run-13 and run-14. It does not modify S1, Research Core/Schema/Adapter, either trial binding, or runner behavior. It does not convert a trial observation target into a requirement on the method.

## Corrected inference

| Element | What the record establishes | What it does not establish |
|---|---|---|
| **Goal** | run-14 was a complete S1-path trial with one trial-only Demand Preservation observation target, scored under the accepted design/binding. | That every S1 execution must invoke research, or that research invocation is necessary for a valid S1 result. |
| **run-13 path** | The runner naturally invoked research, received findings, and returned candidate framing conditions to E/F/G; creator corrections exposed a scope-inflation risk in v0.18.0. | Research is required for the same Probe, every related Probe, or every S1 run. A path observed once is not thereby the only legitimate path. |
| **run-14 path** | The runner clarified creator scope, formed and confirmed an existence question, reported no external research, and stopped after creator confirmation. The visible trace has no research-return. | That the runner failed, omitted a required method step, or that v0.18.2 failed the DP check. The check's research-return applicability condition was not observed. |
| **Evidence** | Under the preaccepted binding, run-14 is `not observed / inconclusive` for the sole DP regression target. No pass or fail is supported. | No positive regression evidence for the research-return path; also no negative method finding about non-research S1 paths. |

### Inference under correction

The earlier proposal to select a Probe that was “more likely to trigger research” was motivated by the desire to make the DP behavior observable. That may help produce a scoreable sample, but no accepted method, trial design, or binding made a research-return mandatory. It is therefore not a required next step. “Research might help,” “a past run used it,” and “we cannot rule out an S1-level dependency” do not prove that this Probe must research or that another Probe must be created. The proposal is withdrawn as a requirement; the runtime evidence gap remains a pending evidence limitation.

The experiment's observation condition is about whether this sample permits scoring the named behavior. It is not a requirement that the S1 system produce the target behavior. “To obtain a score, the run would need a research-return” is a statement about score observability under this binding; it cannot be reversed into “the runner must research” or “a new Probe must be constructed to induce research.”

## Operational criterion: S1-level research dependency

This criterion is a control-side test drawn from S1 Research Adapter §1 and v0.18.2's conditional research/Demand Preservation clauses. It is not an added method gate or a fixed runner checklist.

Classify an unknown as a **candidate S1-level external research dependency** only when the evidence supports all of the following:

1. **Specific framing unknown:** identify an unresolved external-factual unknown, not merely an unknown answer to an already well-framed B3.
2. **Structure-sensitive:** show which necessary framing decision could differ if the unknown had different values: candidate problem/node inclusion, a relationship or dependency, a counterexample boundary, the object/scope boundary, or local/global impact.
3. **Not otherwise settled:** current-input reasoning and the creator's genuine intent decision do not settle that framing choice; it is not simply a creator preference or ordinary-language choice. If the matter can be framed as a clear objective B3 and deferred to S2, the fact that its answer needs research does not make it S1-level.
4. **Externally discriminable:** relevant external materials could provide evidence that distinguishes the competing framing possibilities. General domain information that only helps answer B3, or a source that merely lists possible mechanisms, is insufficient by itself.
5. **Necessary to framing:** without resolving this unknown, S1 cannot responsibly specify the necessary question structure or object/boundary for handoff judgment. If more than one route can settle framing and the runner takes a legitimate nonresearch route, research is not a necessary path.

Passing this screen means that research may be an appropriate way to resolve an S1 framing unknown under the existing Adapter; it does **not** require a research call where the accepted method leaves the call conditional. A future run with no research remains a valid path; a DP-specific trial result may still be `not observed / inconclusive` if no research-return opportunity occurs.

## Candidate assessment against this criterion

No reviewed candidate presently demonstrates all five conditions. The reasons below are control-side assessments, not domain facts or content for a runner packet.

| Candidate | Assessment |
|---|---|
| **run-14 raw Probe:** “一个生态系统能长期自我维持吗？” | run-14 established a legitimate nonresearch framing path after creator scope clarification. run-13's research return on the same raw question produced candidate criteria, but the records do not establish that external research was necessary to determine the S1 object or boundary. Under this correction, a repeat or variant is not required merely to make the DP behavior observable. |
| **Withdrawn first suggestions:** “植物能学习吗？” / “病毒算生命吗？” | Both can be answered as ordinary concept/category or objective B3 questions; no evidence showed that external sources are necessary to determine S1 structure rather than the eventual domain answer or a creator-selected meaning. They remain withdrawn. |
| **Control-side hypothesis:** “一棵树能活一万年吗？” | Object continuity and age evidence could conceivably affect framing, but the current evidence does not show that they prevent stating an objective B3. The numerical duration may also make this a direct lifespan question. The S1-dependency claim remains speculative. Do not use as a Probe on the current basis. |
| **Control-side hypothesis:** “一个人能同时睡着和醒着吗？” | The issue may be settled by reasoning about the stated predicate or by an ordinary-language/creator boundary, or remain a B3 factual question. No necessary external contribution to S1 framing is established. Do not use as a Probe on the current basis. |

## Conclusion

At present, no independent regression Probe is justified by the S1-level dependency criterion. The runtime evidence gap for v0.18.2 on an actual research-return DP opportunity remains open as an evidence limitation, not as a method failure or an obligation to manufacture the opportunity.

Revisit only when a future real framing case supplies evidence of a specific unresolved S1-level dependency under the criterion above. Then decide whether research is a useful conditional path and whether a trial is worthwhile. Do not select a Probe solely because it seems more likely to trigger research; do not alter the runner input to induce that path. If no such real case appears, leave the gap pending.

## Traceability

- run-14 disposition and limitations: [E-097](../02-execution/E-097-run14-demand-preservation-not-observed.md), [visible trace](run-14-visible-runner-creator-trace.md), [evidence matrix](run-14-demand-preservation-disposition-and-evidence-matrix.md), [A-019](../03-audit/A-019-run14-demand-preservation-disposition-review.md).
- run-13 observation and creator corrections: [E-088](../02-execution/E-088-run13-e2e-isolated-trial-complete.md), [full visible trace](run-13-full-visible-trace-2026-09-29.md), [A-014](../03-audit/A-014-v018-scope-preservation-review.md).
- Governing host path: [S1 Research Adapter v0.1.1](../../GOAL-005-shared-research-loop/attachments/s1-research-adapter-v0.1.1.md); [v0.18.2 execution projection](stage1-framing-method-v0.18.2-execution-projection-v0.1.0.md).

No new Probe, binding, runner, or trial is created or authorized by this record.
