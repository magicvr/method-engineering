---
id: GOAL-001-enter-real-operation
title: 让方法工程进入真实运行
status: active
parent: null
created: 2026-09-14
updated: 2026-09-14
version: 0.1.0
progress: 0%
plan_refs: VP-001-enter-real-operation
primary_plan: VP-001-enter-real-operation
---

# GOAL-001 · 让方法工程进入真实运行

## 概述

本 Root 服务 [`VP-001-enter-real-operation`](../../../vision/plans/VP-001-enter-real-operation.md)：将当前最小方法工程启动机制投入真实实践，围绕真实、具体且有边界的问题开展 Method Case，并在运行中获得对结构、规则与适用边界的反馈。

具体 Method Case 是证据来源，不是本目标要完成的「某一个方法」。本目标也不以证明状态机、Frame、Challenge Gate 或治理结构「正确」为成功条件。

## 愿景对齐

- `serves_summary`：把当前最小启动机制投入真实 Method Case，并建立通过实践证据识别、定位和修正必要问题的基本闭环。
- `plan_refs` / `primary_plan`：`VP-001-enter-real-operation`
- Charter：`method-engineering@0.1.0`

## 成功标准

- [ ] 已固定当前最小启动机制的可核对基线（仓内路径或固定引用），作为后续使用与比对的起点（`I-001`）
- [ ] 至少一个真实、具体且有边界的 Method Case 已实际使用该机制开展工作，而不是继续预先扩展机制（`I-002`）
- [ ] 实践记录能说明该机制是否足以支持问题界定、研究、工程、评价与重构；必要缺口已被识别并定位
- [ ] 实践记录能区分 Case 本身的问题、所构造方法的问题、方法工程框架自身的问题
- [ ] 对启动机制的修正只发生在真实实践暴露必要缺口之后，并形成「真实工作 → 反馈 → 必要时修正」的基本闭环

## 纲领路线图（P-001）

> 本表属于本 Root，是可执行纲领阶段。愿景层 VP-001 的 D1–D3 只给方向，不替代本表。
> 不在此写细任务流水或愿景边界复写。

| 阶段 | 名称 | 状态 | 退出条件 |
|------|------|------|----------|
| **S1** | 投入使用 | 未开始 | `I-001` 已给出可核对基线；`I-002` 已选定至少一个真实、有边界的 Method Case；该 Case 已开始实际使用当前机制，而非继续预先扩展。 |
| **S2** | 观察与分层 | 未开始 | 已有实践记录，能说明机制是否足以支持问题界定、研究、工程、评价与重构；记录能区分 Case / 方法 / 框架三类问题。 |
| **S3** | 必要修正与闭环 | 未开始 | 对机制的修正仅发生在实践暴露必要缺口之后；已形成真实工作 → 反馈 → 识别定位并在必要时修正的基本闭环。 |

阶段先后：S1 → S2 → S3 串行。S2 与 S3 可在同一 Case 内交替取证，但不得在 S1 的基线与 Case 选定完成前假装进入观察或修正。同一纲领阶段内允许并行子目标。

`progress: 0%` 由本表 3 个阶段检查点等权派生（已完成 0 / 总 3）。progress 仅为展示，不放行阶段、不关闭 finding、不覆盖信息门禁，也不推导 `done`。

## 信息就绪与未知项

权威台账在 `01-decision.md`。当前开放 required：`I-001`（机制基线）、`I-002`（首个 Method Case）。二者均阻断 S1 方案冻结与开始实际使用。

## 父目标

`null`（本工作区 Root）

## 台账布局

`01-decision/`、`02-execution/`、`03-audit/` 平铺 ledger；`attachments/` 可空。
