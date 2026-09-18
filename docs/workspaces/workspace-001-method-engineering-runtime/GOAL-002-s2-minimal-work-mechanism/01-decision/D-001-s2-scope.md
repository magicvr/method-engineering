---
id: D-001-s2-scope
doc: decision-entry
goal: GOAL-002-s2-minimal-work-mechanism
status: accepted
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.1.0
---

# D-001 · S2 子目标范围与责任反推边界

## 触发

用户要求创建新的子目标承接 Root S2。Root 已完成 S1，I-001 为 `verified`，D-003 已规定 S2 先从运行责任反推最小工作机制；Root I-002 仍为 `open`。

## 决定

创建并激活 `GOAL-002-s2-minimal-work-mechanism`，父目标为 `GOAL-001-method-engineering-runtime`。本子目标只处理 S2 的最小工作机制反推与落盘，第一阶段建立“运行责任→记录需求”映射。

## 继承的治理上下文

- 愿景：`VP-001-demand-driven-method-engineering`，沿用当前 Charter 对齐链。
- 输入决策：Root `D-002-runtime-model.md` v0.4.0；Root `D-003-s2-minimal-work-mechanism.md`。
- 当前审计事实：Root A-009 Grok independent `pass`；无新的 required finding；S1 已关闭。
- 当前信息门禁：Root I-002 `open`；本子目标 I-201 `open`，作为其 S2 证据切片。

## 范围边界

本子目标不重新审视 S1，不新增运行状态或角色，不设计完整 Artifact/Evidence Schema，不构建自动化或并行调度，也不要求真实 Method Case。任何保留对象必须能指回 D-002 的具体运行责任。

## 退出方向

完成 P1 责任→记录需求映射、P2 最小对象与承载方案、P3 落盘与核对后，以可追踪证据关闭 I-201，并向 Root I-002 回传 S2 退出证据。
