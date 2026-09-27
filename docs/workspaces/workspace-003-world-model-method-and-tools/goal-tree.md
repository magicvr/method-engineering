---
title: 目标树 · workspace-003-world-model-method-and-tools
status: active
created: 2026-09-26
updated: 2026-09-27
parent: null
version: 0.18.0
---

# 目标树 · 世界模型方法与工具

- 工作区：`workspace-003-world-model-method-and-tools`
- canonical：`docs/workspaces/workspace-003-world-model-method-and-tools/`
- vision_role：`primary`
- primary_plan：`VP-003-world-model-method-and-tools`（`active`，`v0.1.1`，`vision_ref` = `method-engineering@0.1.0`）

## 树

```text
GOAL-001-world-model-method-and-tools [active] 为消费方构建并交付世界模型的方法与工具 · progress 25%
└── GOAL-002-r2-method-working-version [active] 形成《世界模型构建方法（工作版）》与两个最小结构 · progress 25%
    ├── GOAL-003-w3-minimal-structures [blocked] W3 · 两个最小结构形成 · progress 33%（S2 暂停）
    └── GOAL-004-collaborative-question-framing [active] 阶段一协作定界认知方法与 W2 交接 · progress 33%（S1 完成；S2 进行中，run-02 未通过 → v0.10）
```

Root 的 P-001 纲领路线图为 **R1 → R2/R3 → R4**。R1 已完成（2026-09-26）：适用对象、退出形态、限额与责任、工具边界均已冻结（`D-002` / `E-003`）。**R2 进行中**，由子目标 `GOAL-002` 承载（工作包 W1～W4，**1/4**：仅 W1 完成；W2 有界回流，由 GOAL-004 承载，W3 S2 暂停）；R3 经复核无独立形成工作，待交付材料落定后确认；R4 未开始。Root 派生 `progress: 25%`（1/4）——R2 未完成，故不计完成。progress 不推导 `done`。

子目标 `GOAL-002` 的 W4 判据是用户 2026-09-26 提供的真实世界问题（星际时代修真个体伟力及其社会影响），该问题同时作为 `WRK-002` 的有界检验用例（Root `I-002`，已 `verified`）与 R4 的检验输入。其「星际时代」与「为什么可以实现」按该用例的假定切片处理，不裁决下游 `H-003` / `H-004`。

运行状态唯一来源为 [`runtime-records/WRK-002-world-model-method-and-tools/record.md`](../../../runtime-records/WRK-002-world-model-method-and-tools/record.md)（2026-09-26 转为**「响应中」**），本目标不镜像。

跨区引用用限定形式：[workspace-002-consumer-response-protocol](../workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/00-meta.md) 的 Root 已 `done`，其 VP-002 已有界 `closed`；那次关门只验证供需对接流程，不验证任何领域方法。

## 状态表

| id | title | parent | status | progress | notes |
|----|-------|--------|--------|----------|-------|
| `GOAL-001-world-model-method-and-tools` | 为消费方构建并交付世界模型的方法与工具 | `null` | active | 25% | R1 完成；R2 进行中；R3 待交付材料确认；R4 未开始。Root 进度独立计算为 1/4。I-004 仍 open。 |
| `GOAL-002-r2-method-working-version` | 形成《世界模型构建方法（工作版）》与两个最小结构 | `GOAL-001-world-model-method-and-tools` | active | 25% | W1 完成，W2 有界修订，W3 S2 暂停，W4 未开始（1/4）。[D-015](GOAL-002-r2-method-working-version/01-decision/D-015-w2-bounded-reflow.md) 撤回当前 W2 完成/冻结投影；v0.4/A-008 保留历史事实，开放 required audit finding 0。原 W4 正式判据不变；I-202/I-203/I-204 open。 |
| `GOAL-003-w3-minimal-structures` | W3 · 两个最小结构形成 | `GOAL-002-r2-method-working-version` | blocked | 33% | S1 草案保留；S2 暂停，等待 GOAL-004 形成 W2 新版及影响交接；S3 未开始。I-301 open，真实问题“世界有多大”为方法探针；创作者逐字段可填性和填写负担仍待核。见 [D-004](GOAL-003-w3-minimal-structures/01-decision/D-004-real-method-probe-and-pause.md)。 |
| `GOAL-004-collaborative-question-framing` | 阶段一协作定界认知方法与 W2 交接 | `GOAL-002-r2-method-working-version` | active | 33% | [D-005](GOAL-004-collaborative-question-framing/01-decision/D-005-stage1-method-level-correction.md) 纠正方法层级，范围再按 [D-008](GOAL-004-collaborative-question-framing/01-decision/D-008-general-two-stage-method-and-probe-boundary.md) 明确：S1 完成；S2 当前为 [阶段一协作定界方法候选 v0.9.0](GOAL-004-collaborative-question-framing/attachments/stage1-framing-method-candidate-v0.9.md)，第二次试跑的固定基线：v0.6.0 试跑经创作者判定**未通过**（premature elicitation、操作打卡 → [D-009](GOAL-004-collaborative-question-framing/01-decision/D-009-analysis-first-and-non-checklist.md) / [E-016](GOAL-004-collaborative-question-framing/02-execution/E-016-v06-run-failed-analysis-first.md)）；创作者指出根本问题是**认知操作被退化成 elicitation**（[D-010](GOAL-004-collaborative-question-framing/01-decision/D-010-operations-must-produce-structure.md) / [E-017](GOAL-004-collaborative-question-framing/02-execution/E-017-cognitive-ops-anti-elicitation-revision.md)）；v0.8 方向获通过后，按试跑前三项小修形成 v0.9（未定项按性质路由、允许有界诊断性探索、弱化表示命名；[D-011](GOAL-004-collaborative-question-framing/01-decision/D-011-routing-and-bounded-exploration.md) / [E-018](GOAL-004-collaborative-question-framing/02-execution/E-018-prerun-revision-v09.md)）；尚无通过检验的方法证据、未交接 W2。第二次试跑（run-02，v0.9）经创作者判定**未通过**：保留局部正证据（premature elicitation 实质改善、出口退回检查有效），失败机制为**候选过生成／诊断性探索越界／层级混合**（[运行 02](GOAL-004-collaborative-question-framing/attachments/probe-01-stage1-test-v0.9-run-02.md) / [E-019](GOAL-004-collaborative-question-framing/02-execution/E-019-probe01-v09-test-result.md)），案例产物已封存；据此形成 [v0.10](GOAL-004-collaborative-question-framing/attachments/stage1-framing-method-candidate-v0.10.md)（[D-012](GOAL-004-collaborative-question-framing/01-decision/D-012-run02-failure-three-fixes.md) / [E-020](GOAL-004-collaborative-question-framing/02-execution/E-020-v010-structural-fixes.md)）。第一例两次运行证据：v0.5 初次（[运行 01](GOAL-004-collaborative-question-framing/attachments/probe-01-stage1-test-v0.5-run-01.md)）与 v0.6 复测（[运行 01](GOAL-004-collaborative-question-framing/attachments/probe-01-stage1-test-v0.6-run-01.md)、[E-015](GOAL-004-collaborative-question-framing/02-execution/E-015-probe01-stage1-v06-test-result.md)）；第二个不同真实创作问题尚未选定，跨案例验证仍 collecting；没有回答原问、构建世界模型或图工具。案例结果不等于通用方法；I-401 open、I-402 collecting；S3 未开始。 |
