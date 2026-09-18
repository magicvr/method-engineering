---
id: GOAL-002-s2-minimal-work-mechanism
title: S2 最小工作机制反推与落盘
status: done
parent: GOAL-001-method-engineering-runtime
plan_refs: VP-001-demand-driven-method-engineering
primary_plan: VP-001-demand-driven-method-engineering
serves_summary: 承接 Root S2，根据已冻结的运行责任反推出最小工作对象、记录承载、目录结构和流程文档。
created: 2026-09-18
updated: 2026-09-18
version: 0.5.0
progress: 100%
---

# GOAL-002 · S2 最小工作机制反推与落盘

## 概述

本子目标承接 Root `GOAL-001-method-engineering-runtime` 的 S2 阶段。输入是已通过 S1 cross audit 的 D-002 需求—响应运行模型；输出是由运行责任推出的最小工作对象、记录边界、状态承载、仓库目录和必要流程文档。

本目标不重新设计 D-002，不构建具体领域方法，不把 S1 纸面 walkthrough 当作真实 Method Case，也不预先建立无法由运行责任推出的完整 Schema、自动化平台或并行调度协议。

## 成功标准

- [x] D-002 的运行责任、状态转换、授权边界、反馈和追踪问句均有对应的最小记录/承载需求说明。
- [x] 最小工作对象集合及其边界已确定；每个对象都能指回运行责任，不产生第二套状态源。
- [x] 记录承载、目录结构和必要流程文档已落盘，能够支持 S1 的授权、响应、验证、交付、反馈和退出语义。
- [x] I-201 以可核对证据关闭，并向 Root I-002 提供 S2 退出所需证据。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|------|------|------|----------|
| **P1** | 运行责任→记录需求映射 | 已完成 | D-002 的责任位置、状态转换、追踪问句和反馈路由均完成最小记录需求核对；I-201 仍可追踪。 |
| **P2** | 最小对象与承载方案 | 已完成 | 对象、记录边界、状态承载、目录和流程文档方案形成并通过方案审视；不引入无法由责任推出的机制。 |
| **P3** | 落盘与 S2 验收 | 已完成 | 必要文档/承载落盘，事实可核对，I-201 关闭并向 Root I-002 回传证据。 |

阶段按 P1→P2→P3 串行；只有在阶段内出现独立范围、依赖或交付证据时才创建进一步子目标。

## 信息就绪与未知项

| ID | 级别 | 所需信息 / 问题 | 影响门禁 | 最晚需要阶段 | 验证 / 收集动作 | 状态 | 延期 / 复核 | 证据 / 结论 |
|----|------|-----------------|----------|--------------|-----------------|------|-------------|-------------|
| I-201 | required | 从 D-002 已冻结的运行责任反推出哪些最小工作对象、记录边界和承载位置。 | P2 方案冻结、P3/S2 退出 | P2 | 已完成 P1 映射、P2 对象/承载方案、P3 落盘和仓库级路径修正核对。 | verified | 不延期；已由 A-003/A-004 self review 关闭并修正路径。 | `01-decision/D-002-s2-responsibility-record-map.md`；`01-decision/D-004-s2-repository-hosting-correction.md`；`../../../../runtime-records/README.md`；`03-audit/A-004-repository-hosting-correction-self-review.md`。 |

## 父目标与 S2 上下文

- 父目标：`GOAL-001-method-engineering-runtime`。
- Root S2 决策：`D-003-s2-minimal-work-mechanism.md`。
- 输入运行模型：`GOAL-001-method-engineering-runtime/01-decision/D-002-runtime-model.md` v0.4.0。
- Root I-002 已由 Root A-011 标记为 `verified`；本子目标的 I-201 是其 S2 证据切片，不取代 Root 信息台账。

## 台账布局

本目标使用平铺的 `01-decision/`、`02-execution/`、`03-audit/` 和 `attachments/`。新增决定、事实和正式审计意见分别写入对应 ledger 目录。
