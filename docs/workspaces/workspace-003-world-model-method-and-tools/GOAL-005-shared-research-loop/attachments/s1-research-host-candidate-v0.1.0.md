---
title: S1 research-loop host 集成候选
status: draft
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-005-shared-research-loop
version: 0.1.0
acceptance: unaccepted
---

# S1 research-loop host 集成候选 · v0.1.0

> **状态：draft / unaccepted / not trialled。** 本文件是可审阅的窄接入增量，不是已接受的 S1 方法版本，不授权研究试跑。

## 1. 宿主基线与身份

- **派生基线**：[S1 阶段一方法候选 v0.16.1](../../GOAL-004-collaborative-question-framing/attachments/stage1-framing-method-candidate-v0.16.1.md)，冻结的 run-10 隔离试跑基线。
- **基线 SHA-256**：`E6C1EF612CEAFB64DDB8C26202D84007405723E19D9647025BF17C6BE5994C34`。
- **候选自身标识**：S1 research-host candidate `v0.1.0`。此版本序列独立于 S1 方法版本，不占用或覆盖已有的 v0.17.0 semantic zoom 草稿。
- **候选组件依赖**：[Shared Research Core v0.1.0](shared-research-loop-core-v0.1.0.md)、[Shared Research Record Schema v0.1.0](shared-research-record-schema-v0.1.0.md)、[S1 Research Adapter v0.1.0](s1-research-adapter-v0.1.0.md)。三项组件基线由 [D-006](../01-decision/D-006-components-accepted.md) 接受。
- **与后续试跑的身份关系**：实际试跑前，须审阅并另行裁定是否接受本候选、是否将其作为正式窄 host 集成版本，以及相应 `host_revision` 的记录方式。试跑前仍须另行授权；本候选自身不构成已集成 host。

本候选不修改 v0.16.1 或 v0.17.0 文件，不含完整方法副本，只提供一个可插入的窄接口段。候选没有吸收 semantic zoom、run-10 过程或任何 Probe 1 / “世界有多大”案例材料。

## 2. 建议插入点

将下列接口段插入 v0.16.1 的 **“规则 B · 按性质路由的主动分析”** 中，紧接“路由要求”段之后、**“规则 D · 有界诊断性探索与假定边界”**标题之前。现有规则 B 的 N3 行保持原文；该接口适用于任何符合 S1 adapter 调用条件的未知，不要求每个未知都调用研究。

### 外部研究调用与回流（候选新增）

当当前未定项满足 [S1 Research Adapter](s1-research-adapter-v0.1.0.md) 的调用条件，且外部资料可能为当前判断提供有用依据时，可通过该 adapter 调用 [Shared Research Core](shared-research-loop-core-v0.1.0.md)，并按 [Shared Research Record Schema](shared-research-record-schema-v0.1.0.md) 留痕。向 adapter 提供当前原问、受影响的局部问题/结构位置和未定项引用；其余调用输入按 adapter 契约映射。研究结果经 adapter 回到当前 S1 分析位置：候选是否进入结构由规则 E 判断，未决项归属由规则 F 处理，coverage、交接相关增量、收束和范围影响由规则 G 处理。研究结局本身不构成上述判断，也不改变创作者与助手既有权责。

## 3. 职责边界与不变项

- **Core** 唯一维护研究适配性、来源策略、主张评价、迁移、综合、有界停止和剩余未知语义；host 只引用 Core，不复制其步骤、清单或停止条件。
- **Schema** 唯一维护研究记录字段与出处链；host 不复制其字段表。
- **S1 adapter** 维护 S1 调用条件、输入映射与回流契约；host 只在该契约下接入，不另造来源评价或迁移规则。
- **S1 host** 仅增加调用入口与回流位置。规则 E/F/G 正文与门禁、规则 D 的假定边界、规则 B 的按性质路由、交接第三态及创作者裁决权均保持不变。
- 资料、taxonomy 或类比本身不自动获得结构准入资格；局部研究不自动重启顶层 coverage；Core 的结局不等于问题成立、问题集充分或 handoff-ready。

## 4. 本候选排除范围

本候选不修改既有规则，不增设“必须搜索”或“搜索后必须新增节点”的通用门禁；不修改 core/schema/adapter；不接入 S2；不选择或执行 S1 试跑案例；不更新任何 Probe 1、run-10 或 GOAL-004 父层案例结论。若 review 发现需要改变 Core、Schema、Adapter 或 Rule E/F/G 才能满足接口，记录缺口并停止本候选，不在本次扩大范围。

## 5. 审阅检查点

1. 基线文件与 SHA-256 是否正确，候选是否清楚地作为 v0.16.1 的窄增量。
2. 插入点是否准确；除新增接口段与必要身份说明外，是否保持单一改动面。
3. 调用条件与输入映射是否只引用 adapter/core/schema，不复制其研究语义。
4. 回流是否明确分派给既有 E/F/G，并保留规则 D 假定边界、创作者权责和局部/全局 coverage 边界。
5. 是否未包含组件变更、semantic zoom、正式案例扩展或试跑执行授权。
