---
id: GOAL-005-shared-research-loop
doc: decision
status: active
parent: GOAL-002-r2-method-working-version
created: 2026-09-27
updated: 2026-09-28
version: 0.5.14
---

# 决策记录 · GOAL-005

## 信息需求与阶段门禁

当前未登记 P-005 独立信息项。shared component 的集中位置、候选修订标识及窄 adapter 范围已由 D-003 裁决；core、接入方案边界/顺序、schema 与两个 adapter 设计基线已分别由 D-004～D-006 接受。S1 host 参照 v0.16.1 已由 D-007 选定，试跑设计 v0.1 已由 D-008 接受；窄接口 overlay v0.1.0 经复核 ACCEPT（E-010）；其后按 D-009 形成的完整集成方法候选 v0.16.2 经独立 Reviewer 复核 ACCEPT（E-011），并由创作者接受为本轮试跑 host 基线（D-010）。创作者按 D-011 授权调用后，于 D-012 接受 run-01 为有效试跑样本及 Core outcome，但未整体接受 E/F/G 回流。GOAL-005 A-001 对 Rule E 候选问题准入/目标事实边界给出 conditional；创作者按 D-013 授权形成新 S1 adapter v0.1.1 与 host v0.16.3 澄清候选；F-001 已依据 D-014 的修正证据与独立复核 A-002 按 `fixed` 路径闭合。按 D-015，创作者已接受 run-02 设计 v0.2，并仅接受 S1 host v0.16.3 与 adapter v0.1.1 作为本次调用修订，授权执行一次有界隔离试跑；二者仍不替代一般基线，也不构成方法验证。非阻断 `evidence_role` 观察的触发条件见 D-006。

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-09-27 | 用户裁决 GOAL-005 承载共享研究闭环设计 | accepted | `01-decision/D-001-user-approved-scope.md` |
| D-002 | 2026-09-27 | 采用共享 core＋S1/S2 双 adapter 架构并保留版本边界裁决 | accepted | `01-decision/D-002-shared-core-two-adapters.md` |
| D-003 | 2026-09-27 | 裁决 shared components 集中落点、候选修订与宿主最小接入范围 | accepted | `01-decision/D-003-central-shared-boundary.md` |
| D-004 | 2026-09-27 | 接受 shared research core 候选作为设计基线 | accepted | `01-decision/D-004-core-design-baseline.md` |
| D-005 | 2026-09-27 | 接受版本化接入方案作为边界与顺序基线 | accepted | `01-decision/D-005-integration-plan-baseline.md` |
| D-006 | 2026-09-27 | 接受共享记录 schema 与两个 adapter 作为组件设计基线 | accepted | `01-decision/D-006-components-accepted.md` |
| D-007 | 2026-09-27 | 选定 S1 research-loop 试跑设计参照基线 | accepted | `01-decision/D-007-s1-host-design-baseline.md` |
| D-008 | 2026-09-27 | 接受 S1 research-loop 独立调用试跑设计基线并授权窄 host 候选审阅 | accepted | `01-decision/D-008-s1-trial-design-accepted.md` |
| D-009 | 2026-09-27 | 授权进入 S1 research-loop host 正式集成候选 | accepted | `01-decision/D-009-s1-host-v0162-integration.md` |
| D-010 | 2026-09-28 | 接受 S1 research-loop 集成版 v0.16.2 为试跑 host 基线 | accepted | `01-decision/D-010-s1-host-baseline-accepted.md` |
| D-011 | 2026-09-28 | 授权执行一次 S1 research-loop 独立调用试跑 | accepted | `01-decision/D-011-s1-trial-execution-authorized.md` |
| D-012 | 2026-09-28 | 接受 run-01 为有效试跑样本并裁定后续审查边界 | accepted | `01-decision/D-012-run01-sample-accepted-e-f-review-pending.md` |
| D-013 | 2026-09-28 | 授权澄清研究证据与 S1 条件问题准入边界 | accepted | `01-decision/D-013-rule-e-research-relevance-clarification-authorized.md` |
| D-014 | 2026-09-28 | 按修正与独立复核关闭 A-001/F-001 | accepted | `01-decision/D-014-a001-f001-fixed-response.md` |
| D-015 | 2026-09-28 | 接受 run-02 设计并授权一次 S1 research-loop 调用 | accepted | `01-decision/D-015-run02-trial-accepted-and-authorized.md` |
| D-016 | 2026-09-28 | 接受 run-02 为有界行为样本并授权一次候选协调 | accepted | `01-decision/D-016-run02-sample-accepted-and-reconciliation-authorized.md` |
| D-017 | 2026-09-28 | 接受 run-02 两项局部 B3 候选并保留当前粒度 | accepted | [D-017](01-decision/D-017-run02-local-candidates-accepted.md) |
| D-018 | 2026-09-28 | 按独立关门审计通过结项 GOAL-005 | accepted | [D-018](01-decision/D-018-goal-closeout.md) |
