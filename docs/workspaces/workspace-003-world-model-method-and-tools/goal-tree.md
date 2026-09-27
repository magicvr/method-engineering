---
title: 目标树 · workspace-003-world-model-method-and-tools
status: active
created: 2026-09-26
updated: 2026-09-27
parent: null
version: 0.47.1
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
    ├── GOAL-004-collaborative-question-framing [active] 阶段一协作定界认知方法与 W2 交接 · progress 33%（①-b 已由创作者接受为局部 handoff-ready；presentation-03 / 父层结构待确认；R-1 残余；Probe 1 与父层确认暂停，未继续 W2）
    └── GOAL-005-shared-research-loop [active] S1/S2 共享研究闭环机制设计（候选 draft/unaccepted；W2 当前顺序切片，不与 GOAL-004 并行）
```

Root 的 P-001 纲领路线图为 **R1 → R2/R3 → R4**。R1 已完成（2026-09-26）：适用对象、退出形态、限额与责任、工具边界均已冻结（`D-002` / `E-003`）。**R2 进行中**，由子目标 `GOAL-002` 承载（工作包 W1～W4，**1/4**：仅 W1 完成；W2 有界回流；当前顺序处理 GOAL-005 共享研究闭环设计切片，GOAL-004 的 Probe 1 与父层确认暂停、未并行推进；不增设 W5，W3 S2 暂停）；R3 经复核无独立形成工作，待交付材料落定后确认；R4 未开始。Root 派生 `progress: 25%`（1/4）——R2 未完成，故不计完成。progress 不推导 `done`。

子目标 `GOAL-002` 的 W4 判据是用户 2026-09-26 提供的真实世界问题（星际时代修真个体伟力及其社会影响），该问题同时作为 `WRK-002` 的有界检验用例（Root `I-002`，已 `verified`）与 R4 的检验输入。其「星际时代」与「为什么可以实现」按该用例的假定切片处理，不裁决下游 `H-003` / `H-004`。

运行状态唯一来源为 [`runtime-records/WRK-002-world-model-method-and-tools/record.md`](../../../runtime-records/WRK-002-world-model-method-and-tools/record.md)（2026-09-26 转为**「响应中」**），本目标不镜像。

跨区引用用限定形式：[workspace-002-consumer-response-protocol](../workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/00-meta.md) 的 Root 已 `done`，其 VP-002 已有界 `closed`；那次关门只验证供需对接流程，不验证任何领域方法。

## 状态表

| id | title | parent | status | progress | notes |
|----|-------|--------|--------|----------|-------|
| `GOAL-001-world-model-method-and-tools` | 为消费方构建并交付世界模型的方法与工具 | `null` | active | 25% | R1 完成；R2 进行中；R3 待交付材料确认；R4 未开始。Root 进度独立计算为 1/4。I-004 仍 open。 |
| `GOAL-002-r2-method-working-version` | 形成《世界模型构建方法（工作版）》与两个最小结构 | `GOAL-001-world-model-method-and-tools` | active | 25% | W1 完成；W2 有界修订中，当前顺序处理 GOAL-005 共享研究闭环设计切片（仅候选，不接入版本，不放行 W2/W3）；W3 S2 暂停，W4 未开始。仍按 W1→W2→W3→W4 四个工作包计算，不增设 W5；v0.4/A-008 历史保留，开放 required audit finding 0；I-202/I-203/I-204 open。见 [D-016](GOAL-002-r2-method-working-version/01-decision/D-016-shared-research-loop-slice.md)。 |
| `GOAL-003-w3-minimal-structures` | W3 · 两个最小结构形成 | `GOAL-002-r2-method-working-version` | blocked | 33% | S1 草案保留；S2 暂停，等待 GOAL-004 形成 W2 新版及影响交接；S3 未开始。I-301 open，真实问题“世界有多大”为方法探针；创作者逐字段可填性和填写负担仍待核。见 [D-004](GOAL-003-w3-minimal-structures/01-decision/D-004-real-method-probe-and-pause.md)。 |
| `GOAL-004-collaborative-question-framing` | 阶段一协作定界认知方法与 W2 交接 | `GOAL-002-r2-method-working-version` | active | 33% | ①-b 已由创作者接受为局部 handoff-ready（D-036/E-051）；呈示 03 与父层结构待确认；R-1 保持残余。Probe 1 后续与父层确认暂停，未继续 W2；GOAL-004 status/progress 未变。当前投影据 D-036/E-051、E-052。 |
| `GOAL-005-shared-research-loop` | S1/S2 共享研究闭环机制设计 | `GOAL-002-r2-method-working-version` | active | — | W2 内当前顺序处理的共享研究设计切片；候选 draft/unaccepted，未接入 S1/S2 方法版本；不等于 GOAL-004、W2 或 W3 放行。见 [D-001](GOAL-005-shared-research-loop/01-decision/D-001-user-approved-scope.md)。 |
