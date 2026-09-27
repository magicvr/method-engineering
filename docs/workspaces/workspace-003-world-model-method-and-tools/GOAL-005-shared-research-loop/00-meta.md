---
id: GOAL-005-shared-research-loop
title: S1/S2 共享研究闭环机制设计
status: active
parent: GOAL-002-r2-method-working-version
created: 2026-09-27
updated: 2026-09-27
version: 0.1.0
plan_refs: VP-003-world-model-method-and-tools
primary_plan: VP-003-world-model-method-and-tools
---

# GOAL-005 · S1/S2 共享研究闭环机制设计

## 概述

为阶段一（S1）与未来阶段二（S2）设计一个按需调用、有界收束的共享外部研究子过程：从识别未知到登记研究结果与剩余未知，并把证据交回当前宿主方法处理。本目标位于工作区 `workspace-003-world-model-method-and-tools`，承接 VP-003；父目标是 [GOAL-002-r2-method-working-version](../GOAL-002-r2-method-working-version/00-meta.md)。

本目标是 W2 内当前**顺序处理**的共享研究设计切片。GOAL-004 的 Probe 1 与父层结构确认已按用户要求暂停，本目标不与之并行推进，也不替代或放行 GOAL-004、W2 或 W3。

## 范围与成功标准

- [x] 形成一份覆盖未知分类与 owner、进入条件、研究问题、来源策略、逐主张证据评价、适用性迁移、综合、宿主接口、停止结局及最小留痕字段的共享研究闭环候选。
- [x] 候选分别给出 S1 与未来 S2 的宿主接口契约；只定义研究结果如何回交，不改写或接入任一方法版本。
- [ ] 候选经创作者审阅并决定接受或修订。候选在此之前保持 `draft / unaccepted`；该决定不等于授权 S1/S2 集成。

此工作是单一、已有明确边界的方法候选设计，可直接执行，不另设可执行路线图或 W5。GOAL-002 的 W2→W3→W4 顺序及进度分母保持不变。

## 明确边界

- 只设计共享 research loop 的最小候选和宿主接口。
- 不修改、不接入 GOAL-004 的 v0.17.0、GOAL-002 的 W2 v0.4、GOAL-003 的结构或其他 S1/S2 方法版本；具体接入另行裁决。
- 不启动 Probe 1，不修改任何 Probe 1 运行、呈示或案例结论；不启动 S2 求解或模型构建。
- 不进行开放式、无上限资料搜索；不把搜索未发现资料当成对象不存在。
- 不改变 GOAL-001/002/003/004 的 status 或 progress。GOAL-002 保持 `active / 25%`，W2 为 4 个工作包中的一个、完成分母不变。

## 当前状态

候选文档已起草；状态为 `draft / unaccepted`。尚无方法版本集成、实际研究运行或 S1/S2 验证。本目标仍为 `active`，不声明完成。

## 愿景对齐

- `plan_refs` / `primary_plan`：`VP-003-world-model-method-and-tools`，继承工作区绑定。
- 本目标只提供共享研究子过程设计，不重写 Charter、VP、GOAL-002 的交付范围或下游世界观 canon。

## 信息就绪与未知项

当前未新增独立信息项。候选审阅与后续版本接入均须分别作出决定；未审阅不构成接受，方法候选也不构成应用或验证证据。

## 父目标与台账

- 父目标：[GOAL-002-r2-method-working-version](../GOAL-002-r2-method-working-version/00-meta.md)。
- 决策、执行、审计分别记入本目标 `01-decision/`、`02-execution/`、`03-audit/`；新条目使用平铺 ledger 文件。
- 当前候选：[shared-research-loop-candidate-v0.1.md](attachments/shared-research-loop-candidate-v0.1.md)（draft/unaccepted）。
