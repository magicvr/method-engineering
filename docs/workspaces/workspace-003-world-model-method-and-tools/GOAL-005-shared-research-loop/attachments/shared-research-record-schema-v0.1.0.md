---
title: Shared Research Record Schema
status: draft
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-005-shared-research-loop
version: 0.1.0
acceptance: unaccepted
---

# Shared Research Record Schema · 候选 v0.1.0

> 共用留痕结构供 [Shared Research Core v0.1.0](shared-research-loop-core-v0.1.0.md) 与两个 host adapter 使用。本 schema 只规定可复查记录所需的信息，不规定数据库、JSON/YAML、表格或其他实现格式。字段可按研究规模裁剪；条件字段不适用时须说明原因，不得用空白掩盖未知。

## 1. 研究任务记录

| 字段 | 必需内容 | 条件/边界 |
|---|---|---|
| `research_id` / `date` | 本轮唯一标识与记录日期 | 简单任务可沿用宿主记录编号 |
| `host` / `host_revision` | S1 或 S2、调用时实际宿主方法修订及其状态 | 尚无新正式版时记录实际使用的冻结/候选基线及状态；若实际宿主修订尚不能确定，不得据此启动或记录为试跑 |
| `core_revision` | 实际调用的 shared core 修订标识 | 每轮必填；试跑须可核实 S1/S2 使用的是同一冻结修订 |
| `schema_revision` | 本记录遵循的共享 schema 修订标识 | 每轮必填；填实际版本，不由后续版本回填覆盖 |
| `adapter_revision` | 本轮实际调用的 S1 或 S2 adapter 修订标识 | 每轮必填；与 `host` 匹配 |
| `unknown` | 未知表述、已知/假设/推论状态、未知类型 | 类型与 owner 分开记录 |
| `owner_and_authority` | 信息 owner、对结果有最终裁定权的角色 | 不得把研究者当成事实 owner 或裁决者 |
| `target_and_impact` | 目标对象、可能改变的判断/问题结构/模型/参数/约束/下一步 | 不清楚时不得启动正式搜索 |
| `research_question` | 本轮拟回答的具体问题或主张 | reconnaissance 须写目的与工作量上限 |
| `use_sufficiency` | 当前用途下何种结果足够交回宿主 | 不等同于目标结论接受或阶段门禁通过 |
| `source_strategy` | 来源类别、选择理由、搜索域/版本/时期 | 搜索域须可复查 |
| `effort_bound` | 工作量/时间/查询边界、回看点和停止条件 | 不设统一轮数或来源数 |

## 2. 证据主张记录

每条证据主张至少记录一行/一个条目，不能以整个来源的总评分代替：

| 字段 | 内容 |
|---|---|
| `claim_id` / `claim` | 稳定标识及可判定的具体主张 |
| `source_identity` / `locator` | 作者/机构/作品或数据集身份及 URL、章节/页码、字段/版本等可复查位置 |
| `source_version_date` | 版本、发布日期或访问日期；只在影响复查/含义时要求 |
| `support` | 来源用什么文本、数据、方法、观测或推导支持该主张；也可记未支持部分 |
| `quality_judgment` | 针对此问题的可信度/方法质量/时效性/适切性判断及理由 |
| `independence_and_lineage` | 来源独立性、转引链；多个网页不自动算独立支持 |
| `limits_and_conditions` | 定义、测量口径、样本、方法假设、情境限制 |
| `conflict_or_counterevidence` | 重要反证/冲突及其所挑战的具体主张；无则说明本轮未发现或未检查 |

来源只在其实际支持范围内引用。次级或弱来源可作为线索，但必须标明用途、证据强度和限制。

## 3. 适用性/迁移记录

若来源对象与目标对象不同，逐项记录：

- `source_object` 与 `target_object`；
- 关键差异（定义、规模、制度、环境、机制、时间、单位、测量口径或模型假设）；
- 迁移理由及其支持证据；
- 迁移成立条件与不能外推的内容；
- 迁移不确定性由谁在宿主中验证。

若迁移不适用或不需要，应写明理由。迁移尚未建立时，来源不能表示为目标对象事实。

## 4. 综合与宿主回流

| 字段组 | 内容 |
|---|---|
| `source_statements` | 来源直接陈述/数据直接显示的内容及 claim 引用 |
| `ai_inferences` | AI 综合推论、推理链、依赖的假设与信心限制 |
| `target_hypotheses` | 目标对象/模型使用前待验证的主张、验证 owner 与方法 |
| `bounded_conclusion` | 对当前用途的有界结论、支持范围与未解决冲突 |
| `host_return` | 交回哪个 host adapter、影响哪个既有判断链；研究 core 不记录为准入/模型采纳裁决 |
| `host_disposition` | S1 记录 Rule E/F/G 处理；S2 记录模型构建/验证处理。由宿主填写，不属于 core 代裁决 |

## 5. 结局与剩余未知

`outcome` 至少区分 `sufficient-for-next-step`、`partial-or-insufficient`、`conflicting-evidence`、`not-found-or-inaccessible`、`restate-or-not-researchable`；并记录 `stop_reason`、是否达到预定上限、以及结局是否仅对当前用途成立。

每项未回答内容记录 `residual_unknown`、状态、信息 owner、下一动作及复查日期/触发条件。`not-found-or-inaccessible` 仅陈述本轮资料状况；不得编码或改写成“对象不存在”。若研究揭示目标治理门禁的新未知，另链接目标自身 P-005 信息项；本 schema 不代替该登记。

## 6. 不可省略的来源链

任何会改变宿主判断的结论，至少能沿以下关系回查：

`host decision/model question → research question → claim → source + locator → support/evaluation → applicability/transfer → bounded synthesis → host disposition`。

字段完整度按研究任务裁剪，但不得丢失这条因果与出处链。无来源、无定位、无适用性理由的主张不能作为已查证证据回交。

`core_revision`、`schema_revision`、`adapter_revision`、`host_revision` 构成每轮不可省略的组件身份四元组。版本未正式确定时，记录当时实际使用的候选标识与状态；不得只写“最新版”或省略 schema/core/adapter 修订，也不得事后覆写历史记录。
