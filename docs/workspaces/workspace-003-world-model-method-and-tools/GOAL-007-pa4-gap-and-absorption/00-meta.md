---
id: GOAL-007-pa4-gap-and-absorption
title: PA4 · 缺口判定与吸收方案
status: done
parent: GOAL-003-prior-art-replanning
created: 2026-10-04
updated: 2026-10-04
version: 0.2.0
progress: 100%
---

# GOAL-007 · PA4 缺口判定与吸收方案

## 概述

承接 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md) 的 PA4。以 PA3 的映射矩阵和关键 unresolved 为输入，判断哪些未决属于“尚未查明”、哪些属于“已发现适用限制”，记录替代检查、继承/有限改造不足、可追溯吸收方案、有限原创范围/停止条件和授权门禁。本目标不冻结最终路线、不形成 R2-W 工作版、不启动原创或实验。

## 非目标

- 不把 unresolved 直接写成已证缺口或原创许可。
- 不冻结 PA5 后续路线、R2-W 工作版或工具。
- 不新增来源、付费访问、模型运行、实验或外部执行。
- 不关闭 I-010 以外的信息项，不修改上层愿景或 runtime record。
- S04-C 全文残余、H3-SEM-001 和旧 H 门禁继续有效。

## 成功标准

- [x] 每个关键 unresolved 均登记必要需求、状态（尚未查明/适用限制）、调查边界、替代检查和证据。
- [x] 对 inherit/adapt 不足与可行吸收/有限改造方案有逐项依据、差异风险与验证安排。
- [x] 原创范围（如有）、停止条件、授权/预算/审计门禁和责任明确；无授权不得启动原创。
- [x] 冲突、证据不足与已知限制分开登记，不混淆未知和缺口。
- [x] Root `I-010` 由用户接受的有界残余满足（非 verified）；PA4 退出经阶段审计，无未合法闭合的 required finding。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|---|---|---|---|
| S1 | 缺口协议与基线 | 已完成 | PA3 unresolved/映射索引、必要需求、状态轴、替代检查和证据等级固定。 |
| S2 | 缺口判定 | 已完成 | 逐项区分尚未查明/适用限制，记录证据、反例和替代检查。 |
| S3 | 吸收与有限改造方案 | 已完成 | 对可继承/可改造不足形成吸收方案、差异风险和验证安排；必要时提出原创闸门。 |
| S4 | I-010 核对与 PA4 退出 | 已完成 | 缺口/方案/停止/授权门禁可核对，Root I-010 证据满足，阶段审计无开放 required。 |

S1→S2→S3→S4；不得越过 I-010 到期门禁冻结 PA5 路线或进入 R2-W。

## 派生进度展示

S1～S4 四个等权检查点，4/4=100%。用户按 D-002 接受 I-010 有界残余；A-002 pass；GOAL-007 置 done。I-010 保持 accepted-residual，不放行 PA5 路线冻结、R2-W、原创或实验。

## 信息门禁引用（非第二台账）

唯一状态/证据权威在 [Root 信息表](../GOAL-001-world-model-method-and-tools/00-meta.md)：`I-010` 约束缺口/选路依据，最晚在 PA5 退出前满足。`I-008`/`I-009` 的残余与 verified 状态继续引用 Root，不在此另立状态源。

## 父目标与对齐

父目标 [GOAL-003-prior-art-replanning](../GOAL-003-prior-art-replanning/00-meta.md)，再沿父链服务 [GOAL-001-world-model-method-and-tools](../GOAL-001-world-model-method-and-tools/00-meta.md) → VP-003 v0.1.1 → Charter `method-engineering@0.1.0`。本目标不复写第二套愿景或 Root 状态。

## 台账布局

`01-decision/`、`02-execution/`、`03-audit/`、`attachments/` 平铺；D/E/A 编号在本目标内从 001 起独立递增，信息状态仍只在 Root。