---
id: workspace-003-world-model-method-and-tools
title: 世界模型方法与工具
status: active
root_goal: GOAL-001-world-model-method-and-tools
canonical_scope: docs/workspaces/workspace-003-world-model-method-and-tools/
shared_materials_catalog: none
vision_role: primary
plan_refs: VP-003-world-model-method-and-tools
primary_plan: VP-003-world-model-method-and-tools
parent: null
created: 2026-09-26
updated: 2026-09-30
version: 0.5.0
---

# 工作区上下文 · 世界模型方法与工具

> 本工作区是 VP-003 的实现工作区，也是当前 vision 层唯一 `primary`。
> `workspaces/` 只作统一父容器；工作区根直接保存 `goal-tree.md` 与平铺的 `GOAL-*` 五件套，它不替代这些文件的状态真相。

## 绑定

| 字段 | 当前值 | 说明 |
|------|--------|------|
| 工作区 ID | `workspace-003-world-model-method-and-tools` | 与所有共享资料引用的 `workspace_id` 一致（当前无共享资料引用）。 |
| Root Goal | `GOAL-001-world-model-method-and-tools` | 已存在，`parent: null`。 |
| canonical 范围 | `docs/workspaces/workspace-003-world-model-method-and-tools/` | 本区唯一的目标状态范围。 |
| 共享资料目录 | `none` | 当前不声明共享资料引用。跨仓材料经下游 `exchange/` 交接，不进入本区共享资料机制。 |
| 愿景角色 | `primary` | 2026-09-26 按用户确认开设，为 vision 层唯一 `primary`（`VR-006`）。 |
| 规划对齐 | `plan_refs` / `primary_plan` = `VP-003-world-model-method-and-tools` | 指向 [docs/vision/plans/VP-003-world-model-method-and-tools.md](../../vision/plans/VP-003-world-model-method-and-tools.md)；`vision_ref` 精确对齐 `method-engineering@0.1.0`。 |

## 愿景对齐

完整治理下仓库必有唯一 [docs/vision/](../../vision/) Charter（`method-engineering@0.1.0`，`active`）。本工作区通过必填的 `plan_refs` 与 `primary_plan` 对齐意图 VP-003；VP-003 再经 `vision_ref` 对齐 Charter。细则见 [vision/alignment.md](../../vision/alignment.md) 与 P-006。

本文件不维护 progress%，也不把愿景目录当作第二套目标树。

## 固定共享资料引用

当前为 `none`。后续若需要共享资料，必须先按工作区协议登记完整的 `material_id`、来源、版本、SHA-256、用途和状态；不能仅因文件可读而将其作为事实、证据或 finding 关闭依据。

跨仓交接材料（需求原文、澄清、交付、收件与验收）**不属**本区共享资料机制，按 [`protocols/consumer-response-protocol.md`](../../../protocols/consumer-response-protocol.md) 与下游 `exchange/` 约定承载；本仓只保留引用与去标识化摘要。

## 纲领阶段

本区的纲领阶段、先后关系与退出条件的权威记录在 Root 的 [`00-meta.md`](GOAL-001-world-model-method-and-tools/00-meta.md) 中：**R1 澄清与冻结 → R2 优先验证假设、按证据选路并形成方法工作版 / R3 配套工具界定与形成 → R4 有界检验与交付验收**。VP-003 保留方向级阶段与先后，Root 负责本区可执行纲领、信息门禁与证据。

R1 冻结试验范围、判据、停止规则、限额与责任；R2 内依次操作化 H1/H2/H3、有界试验、证据选路与必要的替代方向验证、形成暂定工作版。失败分支受 R1 限额约束，超限或证据不足时暂停受影响阶段并请用户裁决。真实案例须先由共同维护组书面选定并明确授权范围；路线选择不是假设验证结论。R2 与 R3 的界定可在 R1 后并行，工具实现须等方法接口稳定；R4 等两者就绪后检验最终版端到端闭环，复用前置试验案例只提供该有界案例的证据。同一阶段内若出现具有独立范围、依赖或交付证据的工作，才创建平铺子目标。

## 备注

上游视角：本区承接的是**真实消费需求** `WRK-002-world-model-method-and-tools`（下游 `WorldModel.ModernCultivation` 提报，2026-09-26 本仓受理并形成处理承诺）。运行状态唯一来源是 [`runtime-records/WRK-002-world-model-method-and-tools/record.md`](../../../runtime-records/WRK-002-world-model-method-and-tools/record.md)；本区不建立第二套运行状态源。

2026-09-26 由 `/govern` 按用户确认开设本区并创建 Root（`active`）。2026-09-30 用户选择「先验证、失败转向」路线（Root `D-002`）；现 R1 进行中（非权威冻结提案草案准备，Root `E-004`），R2/R3/R4 仍未开始，四个纲领阶段仍为 0/4 完成。用户于 2026-09-30 提出 Skills 工具形式（Root `E-005`），并说明下游由维护者共同维护、可简化多数职责划分（Root `E-006`）；边界/验收及分发安排待确认。尚无完整冻结方案的维护者书面确认或指向同一版本的两仓记录，无阶段放行。`I-001` / `I-003` 仍阻断 R1 冻结，`I-002` 阻断 R2b 真实案例使用并约束 R4 检验，`I-005` 阻断 R2c 证据选路，`I-004` 阻断 R4 交付放行；五项均 `open`，权威登记在 Root `00-meta.md`。

前驱 `workspace-002-consumer-response-protocol`（挂已 `closed` 的 VP-002）保留历史绑定，2026-09-26 起 `vision_role` 改为 `delivery`（`VR-006`）。
