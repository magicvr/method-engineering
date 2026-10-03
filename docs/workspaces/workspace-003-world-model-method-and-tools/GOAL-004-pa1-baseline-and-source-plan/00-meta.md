---
id: GOAL-004-pa1-baseline-and-source-plan
title: PA1 · 基线与来源方案
status: active
parent: GOAL-003-prior-art-replanning
created: 2026-10-04
updated: 2026-10-04
version: 0.1.3
progress: 50%
---

# GOAL-004 · PA1 基线与来源方案

## 概述

承接 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md) 的 PA1，冻结后续 prior-art 调查所需的可追溯基线、约束迁移、来源与访问方案、资源和停止规则。本目标只完成 PA1；PA2 及之后的要素抽取、适用性映射、缺口判断与路线冻结仍由 GOAL-003 或其后续阶段子目标承载。

## 非目标

- 不抽取理论全文要素，不判断理论适用性，不给整理论贴 inherit/adapt/not-applicable 总标签。
- 不完成 §10/§13 与 H1/H2/H3 的理论映射，不形成缺口结论或后续方法路线版本。
- 不处理旧 H 预登记/运行，不闭合旧 H3-SEM-001，不把未核实书目或摘要提升为理论证据。
- 不修改 Charter、VP、runtime record、下游材料或其他工作区。
- 不自行授权付费访问、机构采购、外部模型执行、实验运行或以用量方式扩大的调查预算。

## 成功标准

- [x] 需求源固定为下游提交 `7324bdf`，本地快照、blob/hash 与提取范围可核对。
- [x] 完成通用约束、旧 H 专属约束与 prior-art 调查专属约束的逐条迁移矩阵，明确沿用/不沿用/需新裁决。
- [ ] 完成 PA-S01～PA-S05 来源方案：权威来源与版次、稳定标识、访问路径、开放/受限状态、合法替代来源与缺口处置。
- [ ] 明确调查资源上限、访问权限、付费边界、范围扩展条件、停止规则、责任人与剩余未知；关键选择已获用户书面裁决。
- [ ] Root `I-007` 由可核对证据满足：权限有核实依据，或未知项按用户书面 `accepted-residual` 处理；PA1 退出经阶段审计，无未合法闭合的 required finding。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|---|---|---|---|
| S1 | 基线与需求固定 | 已完成 | `7324bdf` 与 `e9054c9` 的 blob/本地快照一致；R1、旧 H 和提取来源均有固定标识。 |
| S2 | 约束迁移矩阵 | 已完成 | 逐条覆盖 R1 通用条款、旧 H 专属条款和 prior-art 调查专属条款，区分沿用/终止/需新裁决。 |
| S3 | 来源与访问方案 | 进行中 | 五类主范围均有代表性来源/版次及访问方案；受限来源的授权获取或公开一手替代有明确选择路径。 |
| S4 | 资源、裁决与 PA1 退出 | 未开始 | 资源/权限/预算/停止规则冻结；I-007 证据满足（权限 verified 或明确残余获用户接受）；阶段审计完成且无开放 required finding。 |

S1→S2→S3→S4 串行；S1、S2 已完成，S3 进行中。同一阶段的公开元数据核实可并行，但不得在 S4 前把来源识别升级为理论抽取或适用性结论。

## 派生进度展示

S1～S4 四个等权检查点，当前 2/4=50%。S3 已有公开访问事实和待用户裁决选项，但尚未形成冻结来源方案；progress 只作展示，不放行 PA2、不关闭 Root 信息项或 finding。

## 信息门禁引用（非第二台账）

唯一状态与证据权威在 [Root 信息表](../GOAL-001-world-model-method-and-tools/00-meta.md)：`I-007` 约束迁移、调查边界、来源/资源方案与新增执行授权是 PA1 退出前的 required 门禁。`I-008`～`I-010` 分别约束 PA2/PA3/PA5，本目标只在来源方案中为其准备可追溯入口，不提前声称满足。

## 父目标与对齐

父目标 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md)，再沿父链服务 [GOAL-001-world-model-method-and-tools](../GOAL-001-world-model-method-and-tools/00-meta.md) → VP-003 v0.1.1 → Charter `method-engineering@0.1.0`。本目标不复写第二套愿景或 Root 状态。

## 台账布局

`01-decision/`、`02-execution/`、`03-audit/`、`attachments/` 平铺；D/E/A 编号在本目标内从 001 起独立递增，信息状态仍只在 Root。