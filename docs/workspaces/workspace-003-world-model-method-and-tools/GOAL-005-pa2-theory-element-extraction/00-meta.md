---
id: GOAL-005-pa2-theory-element-extraction
title: PA2 · 理论来源核实与要素抽取
status: active
parent: GOAL-003-prior-art-replanning
created: 2026-10-04
updated: 2026-10-04
version: 0.1.2
progress: 75%
---

# GOAL-005 · PA2 理论来源核实与要素抽取

## 概述

承接 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md) 的 PA2。按 PA1 冻结的五类主范围和用户裁决的来源/访问/资源边界，核实来源版本与定位，抽取理论要素或局部主张，记录前提、输入/输出、适用范围、限制、反例线索和证据等级。本目标不把理论要素映射到需求 §10/§13 或旧 H 假设，也不判断理论适用性；这些属于 PA3/PA4。

## 非目标

- 不给整理论贴 inherit/adapt/not-applicable/unresolved 总标签。
- 不完成 §10/§13、H1/H2/H3 或最终工作版映射。
- 不宣称理论成熟、充分或对本需求适用；不把未查到写成理论不存在。
- 不新增核心来源、付费访问、外部模型执行或实验运行；超出 J-03-A 来源/费用/人时上限须重新请求用户裁决。
- 不提交受限来源全文或复制超出必要摘录的材料。

## 成功标准

- [x] 每个主来源均有精确版次/稳定标识、原文定位和访问记录；受限权限残余按 PA1 的 `accepted-residual` 执行。
- [x] 每个理论要素/局部主张均有独立 ID、原文定位、前提、输入/输出、适用范围、限制和证据等级。
- [ ] PA-S01～PA-S05 的代表来源均有系统抽取记录；未获得或无法核实的部分保持 unresolved。
- [x] 来源间冲突、解释差异和反向/替代线索单独登记，不强行合并。
- [ ] Root `I-008` 由证据满足；PA2 退出经阶段审计，无未合法闭合的 required finding。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|---|---|---|---|
| S1 | 访问核实与抽取协议 | 已完成 | 主来源路径可读、定位格式、元素 ID/字段、停止规则和证据等级固定。 |
| S2 | 核心来源抽取 A | 已完成 | PA-S01～PA-S03 有系统抽取记录、原文定位、前提/范围/限制与 unresolved 标记。 |
| S3 | 核心来源抽取 B | 已完成（PA-S04-C unresolved） | PA-S04-C/D 与 PA-S05 有系统抽取记录；PA-S04-A/B 仅按历史/细节入口使用。 |
| S4 | 交叉核对与 I-008 退出 | 进行中 | 跨来源冲突/差异登记，覆盖检查完成，Root I-008 证据满足，阶段审计无开放 required。 |

S1→S2/S3 可在访问方案固定后并行，S4 依赖 S2/S3；不得越过 I-008 到期门禁进入 PA3。

## 派生进度展示

S1～S4 四个等权检查点，当前 3/4=75%。S1～S3 完成：37 个来源要素/局部主张已抽取；PA-S04-C 全文 unresolved，S4 正在核对 I-008 与来源覆盖。progress 只作展示，不放行 PA3、不关闭 Root I-008 或 finding。

## 信息门禁引用（非第二台账）

唯一状态/证据权威在 [Root 信息表](../GOAL-001-world-model-method-and-tools/00-meta.md)：`I-008` 约束来源真实性/版本/原文定位及要素抽取充分性，最晚在 PA2 退出、PA3 比较前满足。`I-007` 已为 accepted-residual（非 verified），残余范围仅限 GOAL-003 的 PA2/PA3 内部阅读/引用。`I-009`/`I-010` 不在本目标关闭。

## 父目标与对齐

父目标 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md)，再沿父链服务 [GOAL-001-world-model-method-and-tools](../GOAL-001-world-model-method-and-tools/00-meta.md) → VP-003 v0.1.1 → Charter `method-engineering@0.1.0`。本目标不复写第二套愿景或 Root 状态。

## 台账布局

`01-decision/`、`02-execution/`、`03-audit/`、`attachments/` 平铺；D/E/A 编号在本目标内从 001 起独立递增，信息状态仍只在 Root。