---
id: GOAL-005-shared-research-loop
title: S1/S2 共享研究闭环机制设计
status: active
parent: GOAL-002-r2-method-working-version
created: 2026-09-27
updated: 2026-09-27
version: 0.4.2
plan_refs: VP-003-world-model-method-and-tools
primary_plan: VP-003-world-model-method-and-tools
---

# GOAL-005 · S1/S2 共享研究闭环机制设计

## 概述

为阶段一（S1）与未来阶段二（S2）设计一个按需调用、有界收束的共享外部研究子过程，并提出其版本化接入方案：唯一 shared core 保持研究语义 owner；S1/S2 各有窄 adapter 将研究结果交回各自现有裁决/验证过程。本目标位于工作区 `workspace-003-world-model-method-and-tools`，承接 VP-003；父目标是 [GOAL-002-r2-method-working-version](../GOAL-002-r2-method-working-version/00-meta.md)。

本目标是 W2 内当前**顺序处理**的共享研究设计切片。GOAL-004 的 Probe 1 与父层结构确认已按用户要求暂停，本目标不与之并行推进，也不替代或放行 GOAL-004、W2 或 W3。

## 范围与成功标准

- [x] 形成覆盖未知分类与 owner、进入条件、研究问题、来源策略、逐主张证据评价、适用性迁移、综合、停止结局及最小留痕字段的 shared core 候选，并由创作者接受为设计基线（D-004）。
- [x] 候选分别给出 S1 与未来 S2 的窄宿主接口契约；回交到既有判断链，不改写或接入任一方法版本。
- [x] 形成共享 core＋双 adapter 的版本化接入方案 v0.2；创作者接受其组件边界与流程顺序基线（D-005），含未来 S1、S2 两次独立调用试跑的顺序、验证目标与证据接口。
- [ ] 完成 core/schema/S1 adapter/S2 adapter 四份独立 v0.1.0 组件候选的复核，并由创作者审阅 schema 与两个 adapter 候选。独立复核现已通过，创作者审阅仍待进行。shared components 的集中落点、候选修订标识和宿主最小接入范围已由 D-003 裁决；S1/S2 host 正式版本号和具体插入点待可用基线确定。候选/计划接受不自动授权修改宿主方法版本。

此工作是单一、已有明确边界的方法候选设计，可直接执行，不另设可执行路线图或 W5。GOAL-002 的 W2→W3→W4 顺序及进度分母保持不变。

## 明确边界

- 只设计共享 research loop 的最小候选、版本化接入方案与未来试跑设计；实际方法集成和试跑执行另行授权。
- 不修改、不接入 GOAL-004 的 v0.17.0、GOAL-002 的 W2 v0.4、GOAL-003 的结构或其他 S1/S2 方法版本。shared components 的候选落点与初始修订标识已按 D-003 确定；S1/S2 host 正式版本号与具体插入点仍待可用基线确定。
- 不运行后续 S1/S2 调用试跑；本阶段只写独立试跑的顺序、验证目标和证据接口，不选案例。
- 不启动 Probe 1，不修改任何 Probe 1 运行、呈示或案例结论；不启动 S2 求解或模型构建。
- 不进行开放式、无上限资料搜索；不把搜索未发现资料当成对象不存在。
- 不改变 GOAL-001/002/003/004 的 status 或 progress。GOAL-002 保持 `active / 25%`，W2 为 4 个工作包中的一个、完成分母不变。

## 当前状态

创作者已接受原 core 候选 v0.1 为设计基线（D-004），接受接入方案 v0.2 为组件边界与顺序基线（D-005），并裁决集中落点及宿主最小接口范围（D-003）。Core、schema、S1 adapter、S2 adapter 四份 v0.1.0 候选均已在本目标 `attachments/` 形成并通过独立复核；core 文件映射已接受的设计基线，schema 与两份 adapter 仍为 `draft / unaccepted`，待创作者审阅。S1/S2 host 正式版本号与具体插入点仍待可用基线确定；未修改宿主方法、未运行研究或试跑。本目标保持 `active`，不声明完成。

## 愿景对齐

- `plan_refs` / `primary_plan`：`VP-003-world-model-method-and-tools`，继承工作区绑定。
- 本目标只提供共享研究子过程设计，不重写 Charter、VP、GOAL-002 的交付范围或下游世界观 canon。

## 信息就绪与未知项

当前未新增独立信息项。候选审阅与后续版本接入均须分别作出决定；未审阅不构成接受，方法候选也不构成应用或验证证据。

## 父目标与台账

- 父目标：[GOAL-002-r2-method-working-version](../GOAL-002-r2-method-working-version/00-meta.md)。
- 决策、执行、审计分别记入本目标 `01-decision/`、`02-execution/`、`03-audit/`；新条目使用平铺 ledger 文件。
- 原始 core 候选：[shared-research-loop-candidate-v0.1.md](attachments/shared-research-loop-candidate-v0.1.md)（文件保留 `draft` 状态；其研究语义已由 D-004 接受为设计基线，并映射至下列拆分 Core 候选）。
- 当前接入方案：[shared-research-loop-integration-plan-v0.2.md](attachments/shared-research-loop-integration-plan-v0.2.md)（boundary/sequence baseline accepted；不授权宿主方法编辑）；[v0.1 初稿](attachments/shared-research-loop-integration-plan-v0.1.md)保留为历史。
- Shared Research Core：[shared-research-loop-core-v0.1.0.md](attachments/shared-research-loop-core-v0.1.0.md)（design baseline accepted）。
- 其余组件候选：[shared-research-record-schema-v0.1.0.md](attachments/shared-research-record-schema-v0.1.0.md)、[S1 adapter](attachments/s1-research-adapter-v0.1.0.md)、[S2 adapter](attachments/s2-research-adapter-v0.1.0.md)（draft/unaccepted，独立复核通过，待创作者审阅）。
