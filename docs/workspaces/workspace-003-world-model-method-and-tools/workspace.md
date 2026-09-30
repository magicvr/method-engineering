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
version: 0.25.0
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

2026-09-26 由 `/govern` 按用户确认开设本区并创建 Root（`active`）。2026-09-30 用户选择「先验证、失败转向」路线（Root `D-002`）；现 R1 进行中（非权威冻结提案草案准备，Root `E-004`），R2/R3/R4 仍未开始，四个纲领阶段仍为 0/4 完成。用户于 2026-09-30 提出 Skills 工具形式（Root `E-005`），并说明下游由维护者共同维护、可简化多数职责划分（Root `E-006`）；R1 第一轮方法范围候选 v0.6.1 已准备并经只读文本复核（Root `E-008`），用户已选择该候选为两仓当前澄清基线（Root `D-004`）。下游已于提交 `WorldModel.ModernCultivation@6cb392e65eb8711f17730eafcf68db3deb295bec` 更新当前指针，本仓执行事实见 Root `E-009`、下游决定与执行见 D-008 / E-009。之后本仓准备 H1/H2/H3 可观察判据候选（Root `E-010`），用户已选择组合观察项路径为下一步澄清基础（Root `D-005`），不更改当前双仓绑定。候选仍为 draft；完整冻结方案无维护者书面确认。具体判据、边界/验收及分发安排待确认，无阶段放行。`I-001` / `I-003` 仍阻断 R1 冻结，`I-002` 阻断 R2b 真实案例使用并约束 R4 检验，`I-005` 阻断 R2c 证据选路，`I-004` 阻断 R4 交付放行；五项均 `open`，权威登记在 Root `00-meta.md`。

2026-09-30：本区另准备 H1/H2/H3 证据充分性候选（Root `E-012`）；用户选择按声明范围判充分（Root `D-006` / `E-013`），仍待逐项确定 H 范围、样本、阈值与资源。截至 E-013 记录时未更改当时的 v0.6.1 绑定；随后 D-012 / E-025 已将当前澄清对象更新为 v0.6.2。未选案例或授权试验。

2026-09-30：用户将下游原始问题指定为 R1 草案程序黑箱探针，排除在草案规划之外；单次演练见 Root `D-008` / `E-016`，不作为方法假设证据或 R2b/R4 案例。针对 `I-003`，用户选择独立于 Goal Governance 包的 Codex 首发 Skill 路径（Root `D-009` / `E-018`）；方法接口、源路径、验收和双仓引用尚未冻结，`I-003` 保持 open，未实现工具或写入下游。

2026-09-30：针对 `I-001` 准备了不依赖具体问题或案例的 H1/H2/H3 范围与有限工作量候选（Root `E-019`）；用户选择小型可行性工作量档（Root `D-010` / `E-020`：H1 最多 4、H2 最多 2、H3 最多 3 个主轮结果格；共同维护组总计最多 3 人时；全项目最多一次定向复验和一个替代方向）。随后用户选择证据清单 + 创作者局部裁决形式（Root `D-011` / `E-022`），本仓据此准备空白预登记工作表候选（Root `E-023`）。工作表没有具体问题、模型、样本或实验结果；各 H 的局部规则、完整停止责任和双仓同版确认仍待冻结，不授权执行。黑箱探针及其结果没有用于候选设计，`I-001` 保持 open。

2026-09-30：另备 H1/H2/H3 检验单元结构候选（Root `E-014`）；用户选择共享背景、分立 H 单元（Root `D-007` / `E-015`）；当时未改变 v0.6.1 绑定，后续 D-012 / E-025 已更新当前引用。未选案例、不授权试验。

前驱 `workspace-002-consumer-response-protocol`（挂已 `closed` 的 VP-002）保留历史绑定，2026-09-26 起 `vision_role` 改为 `delivery`（`VR-006`）。

2026-09-30：本仓将已选 R1 规则整合为独立的本地 v0.6.2 草案（Root `E-024`），保留 v0.6.1 文件和当时的下游当前绑定。截至 E-024 记录时 v0.6.2 尚未写入下游，是否更改当前引用待用户裁决；之后用户按 D-012 选择 v0.6.2 并由 E-025 记录首次绑定。`I-001` / `I-003` 仍 open，无试验或阶段放行。

2026-09-30：用户接受推荐，将下游当前 R1 指针更新为上游 magicvr/method-engineering@8a8ded5ddbdb6f627b00ccf854fb0fe75be44cc7 的 v0.6.2 草案；下游提交为 WorldModel.ModernCultivation@1ddfd75f123ba63676be09a1487b506db1d9bc5e，指针及下游决策/执行见 exchange/README.md 与 D-009 / E-010，本仓记录见 Root D-012 / E-025。此为首次绑定事实，原始提交保留作历史。

2026-09-30：本轮文档卫生同步后，v0.6.2 的现行精确来源更新为上游 `magicvr/method-engineering@0340ee94cd07c4da2ce0f3164ddb56bb9e5fc082`，下游于 `WorldModel.ModernCultivation@f24f83c7150499bef1a103bc99ccdbf712fbde53` 刷新 `exchange/README.md` 指针（Root `E-028`；下游 `E-011`）。候选仍为 `draft`，I-001 / I-003 仍 open，无试验或阶段放行。

2026-09-30：用户选择先整理 I-001 / I-003 未决事项裁决清单；Root D-013 / E-026 及附件列出既有选择、待确认值和书面确认要求。清单不代填答案；R1 状态与门禁不变。

2026-09-30：用户接受创作者主责的方法使用边界候选，见 Root D-014 / E-027 与裁决清单。创作者运行方法并保留最终判断；AI 可选协助。共同维护组的具体职责和对完整方案的书面确认仍待完成，I-001 / I-003 保持 open。
