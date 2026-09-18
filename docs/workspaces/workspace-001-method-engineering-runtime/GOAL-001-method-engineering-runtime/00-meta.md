---
id: GOAL-001-method-engineering-runtime
title: 落地需求驱动的方法工程最小运行机制
status: done
parent: null
plan_refs: VP-001-demand-driven-method-engineering
primary_plan: VP-001-demand-driven-method-engineering
serves_summary: 将 VP-001 的意图落地为可正式运行、需求驱动且保持 IDLE 语义的最小方法工程机制。
created: 2026-09-18
updated: 2026-09-18
version: 0.7.0
progress: 100%
---

# GOAL-001 · 落地需求驱动的方法工程最小运行机制

## 概述

本 Root 承接 [`VP-001-demand-driven-method-engineering`](../../../vision/plans/VP-001-demand-driven-method-engineering.md)，负责在当前工作区内把已冻结的愿景意图转化为可正式运行的最小机制。它首先建立运行模型，再由运行责任反推出必要的工作对象、状态、流程文档和仓库承载方式。

本目标不构建具体领域方法，不预先枚举未来方法，也不把 bounded walkthrough 当作真实 Method Case 或具体方法有效性证明。没有已接受的真实需求时，机制应保持 IDLE。

## 成功标准

- [x] 运行模型明确需求信号、澄清与接受、响应选择、验证、交付、反馈、退出及 IDLE 之间的语义、状态转换、责任交接和追踪关系。
- [x] 运行模型能够记录选择、复用、裁剪、组合、修改、新建或确认无需方法变更等最小响应路径，并区分对象问题、方法问题和运行机制问题。
- [x] 由运行责任反推出的最小工作对象、状态、目录和流程文档已落盘；每个保留对象都有明确运行责任，不产生第二套状态源。
- [x] bounded walkthrough 完整走通机制自身的需求进入、状态转换、责任交接、响应选择、验证、交付、反馈和退出，并明确标注其不是真实 Case、不证明领域方法有效性。
- [x] 工作区和 Root 的实施、验证、审计与结项证据可追踪到 VP-001 的方向级退出判据。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|------|------|------|----------|
| **S1** | 冻结运行模型 | 已完成 | D-002 v0.4.0、E-003 v0.4.0、A-008 self 与 A-009 Grok independent 完成；无新的 required finding；I-001 已 verified。 |
| **S2** | 落盘最小工作机制 | 已完成 | 根据 S1 的运行责任确定最小工作对象、状态承载、记录边界、仓库结构和必要流程文档；I-002 关闭；未引入无法由运行责任推出的机制。 |
| **S3** | 机制 walkthrough 与交接 | 已完成 | 完成一次明确标注为机制验证的 bounded walkthrough，记录其内部连贯性、剩余问题和修正；不把 walkthrough 写成真实 Case 或方法有效性证据，并形成 Root/VP 后续结项所需证据。 |

阶段按 S1→S2→S3 串行；同一阶段内若出现具有独立范围、依赖或交付证据的工作，才创建平铺子目标。

## 派生进度展示

`progress: 100%` 由上方 3 个纲领阶段等权计算（已完成 3 / 3）。该值仅作展示，不放行阶段、不关闭 finding、不覆盖信息门禁。Root 整体闭门已按 D-004 / E-015 / A-014 完成，`status` 现为 `done`；状态变更依据闭门条件与证据，不由 progress 单独推导。

## Root 整体闭门

2026-09-18，Root 完成整体闭门核对：5 项成功标准均满足，I-001/I-002/I-003 均为 `verified`，相关 required finding 为 0，且阶段与闭门审计证据齐备。Root 关闭本身不自动关闭 VP；随后 VP-001 已按愿景层规则完成有界 `closed`，workspace-001 已归档，Charter 仍保持 `active`。详见 `01-decision/D-004-root-closeout.md`、`02-execution/E-015-root-closeout.md` 与 `03-audit/A-014-root-closeout-self.md`。

## 信息就绪与未知项

| ID | 级别 | 所需信息 / 假设 | 影响门禁 | 最晚需要阶段 | 验证 / 收集动作 | 状态 | 延期 / 复核 | 证据 / 结论 |
|----|------|-----------------|----------|--------------|-----------------|------|-------------|-------------|
| I-001 | required | VP-001 所要求的最小运行状态、转换、责任边界和追踪语义的具体表达方式。 | 方案冻结、S1 退出 | S1 | 基于 VP-001 退出判据形成运行模型，并用有限 walkthrough 检查内部连贯性。 | verified | 不延期；已在 S1 关门时处理。 | D-002 v0.4.0、E-003 v0.4.0、A-008 self `pass`、A-009 Grok independent `pass`、A-010 closeout；无新的 required finding。 |
| I-002 | required | 支撑运行模型所必需的最小工作对象、记录边界、目录承载和流程文档集合。 | 实施、S2 退出 | S2 | 已由 S2 子目标完成责任→记录→对象/承载→流程说明反推，并在用户确认仓库边界后重新完成落盘核对。 | verified | 不延期；已由 A-011 后的 A-012 修正核对。 | `GOAL-002-s2-minimal-work-mechanism` 的 I-201、D-002、D-004、A-001～A-004；项目根 `runtime-records/README.md`；A-012。 |
| I-003 | required | 已冻结的运行模型与项目级运行记录说明能否通过一次不依赖真实业务事实的机制验证 walkthrough，并形成可交接的 Root/VP 证据。 | S3 walkthrough、Root/VP 后续结项 | S3 | 由 S3 子目标以虚构 trace 核对需求进入、授权、响应、验证、交付、反馈、退出、交接和不产生真实运行记录的边界；完成 self + 指定 independent 后核对。 | verified | 不延期；已由 E-002/E-003、A-001～A-005 和 Root E-014/A-013 完成核对。 | `GOAL-003-s3-mechanism-walkthrough-handoff/02-execution/E-002-s3-bounded-walkthrough.md`；`E-003-s3-branch-paper-snapshots.md`；`03-audit/A-004-s3-finding-closure-a002.md`；Root `E-014-s3-root-handoff.md`；`A-013-s3-root-closeout-self.md`。 |

## 愿景对齐

- `plan_refs`: `VP-001-demand-driven-method-engineering`
- `primary_plan`: `VP-001-demand-driven-method-engineering`
- 服务摘要：本目标只实现 VP-001 的最小运行机制，不扩大 Charter 或 VP 的方向边界。
- 现行 Charter：[`method-engineering@0.1.0`](../../../vision/charter.md)。

## 父目标

本目标为当前工作区唯一 Root，`parent: null`。VP-001 是愿景层规划，不是本目标的 `parent`。

## 台账布局

本目标使用平铺的 `01-decision/`、`02-execution/`、`03-audit/` 和 `attachments/`。索引文件保留稳定入口；新增决定、事实和正式审计意见分别写入对应 ledger 目录。
