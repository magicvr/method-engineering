---
id: D-001-bootstrap-scope
doc: decision-entry
goal: GOAL-001-method-engineering-runtime
status: accepted
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.1.0
---

# D-001 · 工作区启动边界与 Root 路线图

## 决定

1. 使用已确认的显式工作区 `workspace-001-method-engineering-runtime`，Root 为 `GOAL-001-method-engineering-runtime`，标题为“落地需求驱动的方法工程最小运行机制”。
2. 该工作区声明为当前 VP-001 的 `primary` 工作区，并以 `VP-001-demand-driven-method-engineering` 同时作为 `plan_refs` 与 `primary_plan`。
3. Root 保持 `active`，但暂不创建子目标；先用 Root 内的三阶段路线图承载 S1–S3，只有阶段范围、依赖和独立交付证据明确后才拆分子目标。
4. 当前工作区不声明共享资料。运行机制设计从 VP-001 已冻结的意图和治理规则出发，不额外引入未来 Case、具体方法或自动化平台协议。

## 理由

这是 VP-001 的首个实现工作区。当前最小必要动作是建立可正式运行的实现承载和高层执行边界，而不是提前创建具体方法工作或复杂工作对象。Root 路线图保持与 VP-001 的方向级退出判据对齐，并把未知项留在 P-005 信息台账中。

## 未选择的方向

- 不把 VP 直接写成 Goal 或把 VP 作为 Root 的 `parent`。
- 不把 bounded walkthrough、示例方法或假设的下游需求当作真实 Method Case。
- 不在 S0 阶段创建方法资产、复杂 schema、跨仓库协议或未由运行责任推出的目录层级。
