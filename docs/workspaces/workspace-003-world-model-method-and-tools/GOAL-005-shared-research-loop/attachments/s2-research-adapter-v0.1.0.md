---
title: S2 Research Adapter
status: draft
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-005-shared-research-loop
version: 0.1.0
acceptance: unaccepted
---

# S2 Research Adapter · 候选 v0.1.0

> 本 adapter 是 S2 对 [shared core v0.1.0](shared-research-loop-core-v0.1.0.md) 的窄调用/回流契约。共享研究语义和记录字段分别由 [core](shared-research-loop-core-v0.1.0.md) 与 [schema](shared-research-record-schema-v0.1.0.md) 唯一维护；本文件不复制来源评价、迁移、综合或停止规则，也不修改任何 W2/S2 方法版本或 GOAL-003 的结构。

## 1. 调用条件

当 S2 正在构建或验证一个针对目标客观问题的模型，而外部资料可能为机制、参数/范围、约束、已有模型或观测方法提供依据时，可调用 shared core。

若当前未知本质是创作者选择，adapter 将证据回交为选择依据，不把它改写成研究能裁定的问题；若只是基于已知前提的推导缺口，先推理；目标对象自身的事实仍由其建模/观测责任验证，外部资料不能替代目标对象验证。

## 2. 最小输入映射

调用时向 core 提供或引用：

- 待支持或待验证的客观问题及 S2 当前模型构建/验证任务；
- 当前模型候选、机制/参数/约束缺口与目标对象边界；
- 未知的类型、信息 owner、裁定权和可能影响的模型判断；
- 具体研究问题、本轮用途的足够标准；
- 已知单位、定义、范围、观测条件与不可默认的目标世界参数。

Adapter 只把 S2 研究任务映射到共用 schema。来源策略、证据评价、独立性/冲突、迁移与停止均由 [shared core](shared-research-loop-core-v0.1.0.md) 负责。

## 3. 回流到模型构建与验证

Core 输出可作为有出处和适用边界的模型依据候选，包括机制主张、参数取值/范围、约束、已有模型、观测资料或测量方法。Adapter 将其连回对应 S2 模型/判断，并保留源对象与目标对象差异、单位/定义、迁移理由、假设及限制。

S2 既有模型构建与验证负责判断：依据是否适用于目标对象、各项是否在模型内一致、参数/约束如何影响模型，以及还需何种目标对象观测或推导。资料支持模型选择或参数先验不等于目标模型已验证；外来现实常数不能静默成为目标世界参数。Shared core 不决定证据是否采纳，adapter 不改写 S2 裁决规则。

## 4. 留痕与组件身份

调用记录标明实际 core、schema、S2 adapter 与 S2 host 修订身份，并按共享 schema 保存模型任务、研究问题、证据依据、适用性和 S2 处理。S2 host 新版本号与具体插入点待当前 W2 回流形成可用方法基线后单独决定。
