---
title: 按修正与独立复核关闭 A-001/F-001
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-005-shared-research-loop
record_id: D-014
doc: decision-entry
---

# D-014 · 按修正与独立复核关闭 A-001/F-001

## 闭合路径与证据

创作者已在 [D-013](D-013-rule-e-research-relevance-clarification-authorized.md) 选择以实施修正响应 A-001 required finding F-001，并明确要求修正后独立复核。独立 Reviewer 对两份新候选复核为 **ACCEPT**（见 [A-002](../03-audit/A-002-f001-closure-review.md)）；实际文本与受保护基线核对见 [E-017](../02-execution/E-017-f001-correction-and-review.md)。据此，F-001 按 `fixed` 路径闭合。

修正证据：

1. S1 adapter v0.1.1 的调用输入限于调用时已知信息；本轮研究生成的条件候选、来源支持机制及其与输入锚点的关联推理不再倒置为调用前置输入，而在研究返回后映射到 schema 现有字段。
2. S1 host v0.16.3 对齐该调用/回流顺序，并明确条件问题的相关性与目标条件真值不同；入结构须改变必要问题结构或求解依赖，且完成输入否定、已有节点承载及冗余检查。
3. 若准入，记录“问题纳入、答案未定”，目标条件真值由现有 Rule F 归属；Rule F/G 与 shared Core、Schema、S2 adapter 未改。

## 状态与边界

- A-001 原始 verdict `conditional` 保留为历史意见；其 F-001 当前状态为 `fixed`。A-002 只复核该闭合证据，不是 GOAL-005 整体审计。
- S1 adapter v0.1.1 与 S1 host v0.16.3 仍为 `draft/unaccepted`；本决定不接受新版本为基线。
- S1 host v0.16.2、adapter v0.1.0、原试跑设计/绑定包及 run-01 均保持原样；不据此重判 run-01 的任何候选。
- 不授权新的 research call、clean blind trial、S2 试跑、Probe 1 或父层结构确认。若之后认为需要 clean blind trial，应另立后继设计/增量方案，并另行裁决实际版本与执行授权。
