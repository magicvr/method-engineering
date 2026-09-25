---
id: workspace-002-consumer-response-protocol
title: 消费方需求—响应协议工作区
status: active
root_goal: GOAL-001-consumer-response-protocol
canonical_scope: docs/workspaces/workspace-002-consumer-response-protocol/
shared_materials_catalog: none
vision_role: primary
plan_refs: VP-002-consumer-demand-response-protocol
primary_plan: VP-002-consumer-demand-response-protocol
parent: null
created: 2026-09-25
updated: 2026-09-25
version: 0.2.0
---

# 工作区上下文 · 消费方需求—响应协议

## 绑定

| 字段 | 当前值 | 说明 |
|------|--------|------|
| 工作区 ID | `workspace-002-consumer-response-protocol` | 本工作区稳定标识。 |
| Root Goal | `GOAL-001-consumer-response-protocol` | 本区唯一 `parent: null` 的 Root，当前为 `active`。 |
| canonical 范围 | `docs/workspaces/workspace-002-consumer-response-protocol/` | 本区唯一目标状态范围。 |
| 共享资料目录 | `none` | 当前工作区不声明共享资料引用。 |
| 愿景角色 | `primary` | 2026-09-25 按用户确认开设，为 vision 层唯一 `primary`（`VR-004`）。 |
| 规划对齐 | `VP-002-consumer-demand-response-protocol` | 同时作为 `plan_refs` 与 `primary_plan`。 |

## 愿景对齐

本工作区承接 [`VP-002-consumer-demand-response-protocol`](../../vision/plans/VP-002-consumer-demand-response-protocol.md)，该 VP 通过 `vision_ref: method-engineering@0.1.0` 对齐现行 Charter，并于 2026-09-25 进入 `active`。工作区只承载实现层目标状态；VP、Charter 与本区目标分别保持各自权威。

本区职责是把 VP-002 的双向协议意图落地为消费方可照做的协议说明，并用一条真实需求完成端到端试跑。本区不建设 API、Web UI、自动化派发、跨仓同步服务或特定平台适配器，也不为所有消费仓统一仓库结构，不替代 VP-001 的运行记录语义。

## 固定共享资料引用

当前为 `none`。后续若需要共享资料，必须先按工作区协议登记完整的 `material_id`、来源、版本、SHA-256、用途和状态；不能仅因文件可读而将其作为事实、证据或 finding 关闭依据。真实试跑涉及的参与方材料须按约定脱敏并保留可核对依据。

## 纲领阶段

本区的纲领阶段、先后关系与退出条件只记录在 Root 的 [`00-meta.md`](GOAL-001-consumer-response-protocol/00-meta.md) 中：R1 冻结协议语义与运行记录衔接 → R2 形成消费方可执行的协议说明并完成真实消费仓与真实需求的授权和准备 → R3 执行并审视真实端到端试跑。R1–R3 串行；同一阶段内若出现具有独立范围、依赖或交付证据的工作，才创建平铺子目标。

## 备注

2026-09-25 由 `/govern` 按用户确认开设本区并创建 Root（`draft`）。开区只表示实现层目标已建立，**不表示**已具备试跑条件：真实下游实践方、试跑仓库、参与责任人、真实需求与使用/记录授权均尚未指定，相关未知已按 P-005 登记在 Root `00-meta.md`，并在 R2/R3 前构成门禁。本区承载协议文档与方法工程一侧记录引用，项目根 `runtime-records/` 仍是 VP-001 确立的单一运行主记录承载，本区不建立第二套状态源。
