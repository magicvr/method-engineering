---
title: S1 Research Adapter
status: draft
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-005-shared-research-loop
version: 0.1.0
acceptance: unaccepted
---

# S1 Research Adapter · 候选 v0.1.0

> 本 adapter 是 S1 对 [shared core v0.1.0](shared-research-loop-core-v0.1.0.md) 的窄调用/回流契约。共享研究语义和记录字段分别由 [core](shared-research-loop-core-v0.1.0.md) 与 [schema](shared-research-record-schema-v0.1.0.md) 唯一维护；本文件不复制来源评价、迁移、综合或停止规则，也不修改现行 S1 方法版本。

## 1. 调用条件

当 S1 正在分析的问题结构时，一个明确未知可能改变候选问题/解释、关系/依赖、反例、边界或局部/全局影响，并且相关外部资料可能提供有用依据时，可调用 shared core。

若未知属于创作者偏好/取舍，adapter 将研究回到“提供选项与后果依据”的位置，不让 core 替创作者选。若只是当前前提上的推理缺口，先继续推理；若答案只能由目标世界内部求解或观测得到，外部研究只能提供机制/模型参考并须明确标记其迁移限制。

## 2. 最小输入映射

调用时向 core 提供或引用：

- 当前 S1 原问及受影响的局部节点/结构位置；
- 未知的已知/假设/推论状态、信息 owner 与裁定权；
- 它可能改变的候选问题、关系、反例、边界或下一步；
- 具体研究问题、本轮用途的足够标准和既有候选证据；
- 可用的对象/时期/版本边界和任何不能假定的内容。

Adapter 只做 S1 输入到共用 schema 的映射。进入条件、来源策略、证据评价、有界停止和剩余未知依 [core](shared-research-loop-core-v0.1.0.md) 处理。

## 3. 回流位置

Core 输出作为带出处、证据评价、迁移限制、推论标记和剩余未知的候选包回到 S1 当前原问及其局部结构。后续只进入已有规则：

1. **Rule E**：判断候选是否达到入结构门槛。来源或行业 taxonomy 出现本身不构成准入；反例的前提也须与当前目标相关。
2. **Rule F**：为已讨论的未知确定归属、owner 与下一步状态。
3. **Rule G**：判断对 coverage、收束、残余及局部/全局范围的影响。局部研究不自动重启全局 coverage；只有具体证据依现有规则改变全局所求、必要结构或收束条件时才回流更大范围。

Core 的研究结局不等同于 S1 问题成立、候选准入、coverage 完成或 handoff-ready。所有这些判断仍由 S1 原有规则和创作者协作权责作出。

## 4. 留痕与组件身份

调用记录标明实际 core、schema、S1 adapter 与 S1 host 修订身份，并按共享 schema 保存研究问题、候选回流及 Rule E/F/G 的处理。S1 host 修订和具体插入点待选定可用 S1 基线后单独决定。
