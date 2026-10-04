---
id: GOAL-006-pa3-requirement-mapping
title: PA3 · 需求/旧假设映射与四类处置
status: done
parent: GOAL-003-prior-art-replanning
created: 2026-10-04
updated: 2026-10-04
version: 0.2.0
progress: 100%
---

# GOAL-006 · PA3 需求/旧假设映射与四类处置

## 概述

承接 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md) 的 PA3。以 PA2 的 37 项理论要素/局部主张为输入，逐项映射需求 §10/§13 与旧 H1/H2/H3 的局部主张，明确适用条件、差异、限制、证据等级和 `inherit` / `adapt` / `not-applicable` / `unresolved` 处置。本目标不判定最终缺口、不冻结后续路线、不形成 R2-W 工作版。

## 非目标

- 不给整理论贴总标签；分类对象是要素/局部主张。
- 不把理论来源内容自动等同于对本需求的适用性证据。
- 不新增来源、付费访问、模型运行或实验；S04-C 全文残余继续有效。
- 不形成 PA4 缺口结论、PA5 路线冻结、最终工作版或工具。
- 不关闭 I-010，不修改上层愿景或 runtime record。

## 成功标准

- [x] §10-1～§10-5 与 §13-1～§13-10 均有逐项映射、候选要素 ID、条件/差异、处置和依据。
- [x] H1/H2/H3 拆成局部主张后均有映射、适用条件、限制、处置和依据。
- [x] `inherit` / `adapt` / `not-applicable` / `unresolved` 有可核对定义与逐项证据，不混淆未知和已证限制。
- [x] 冲突、证据不足和需要原创的范围单独登记；不以 unresolved 冒充缺口。
- [x] Root `I-009` 由证据满足：映射覆盖与处置依据已核对；PA3 退出经阶段审计，无未合法闭合的 required finding。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|---|---|---|---|
| S1 | 映射协议与基线 | 已完成 | 需求/旧假设基线、元素 ID 索引、四类处置规则和证据等级固定。 |
| S2 | §10/§13 映射 | 已完成 | 15 个需求项逐项有要素映射、条件/差异、处置和依据。 |
| S3 | H1/H2/H3 映射 | 已完成 | 旧假设拆分为局部主张，逐项映射并记录处置和限制。 |
| S4 | 冲突核对与 I-009 退出 | 已完成 | 冲突/unresolved 登记，覆盖检查完成，Root I-009 证据满足，阶段审计无开放 required。 |

S1→S2/S3→S4 已完成；用户 2026-10-04 确认 PA3 关门。I-010 仍未关闭，不进入 PA4 或路线冻结。

## 派生进度展示

S1～S4 四个等权检查点，4/4=100%。A-002 independent verdict pass；用户 2026-10-04 确认关门；GOAL-006 置 done。I-009 更新为 verified，但关键 unresolved 仍是 PA4 输入；不关闭 I-010、不启动 PA4。

## 信息门禁引用（非第二台账）

唯一状态/证据权威在 [Root 信息表](../GOAL-001-world-model-method-and-tools/00-meta.md)：`I-009` 约束映射及适用性依据，最晚在 PA3 退出满足。`I-008` 为 accepted-residual（S04-C 全文未决）；`I-010` 不在本目标关闭。

## 父目标与对齐

父目标 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md)，再沿父链服务 [GOAL-001-world-model-method-and-tools](../GOAL-001-world-model-method-and-tools/00-meta.md) → VP-003 v0.1.1 → Charter `method-engineering@0.1.0`。本目标不复写第二套愿景或 Root 状态。

## 台账布局

`01-decision/`、`02-execution/`、`03-audit/`、`attachments/` 平铺；D/E/A 编号在本目标内从 001 起独立递增，信息状态仍只在 Root。