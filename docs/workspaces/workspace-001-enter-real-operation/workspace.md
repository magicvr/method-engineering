---
id: workspace-001-enter-real-operation
title: 进入真实运行
status: active
root_goal: GOAL-001-enter-real-operation
canonical_scope: docs/workspaces/workspace-001-enter-real-operation/
shared_materials_catalog: none
vision_role: primary
plan_refs: VP-001-enter-real-operation
primary_plan: VP-001-enter-real-operation
created: 2026-09-14
updated: 2026-09-14
version: 0.1.0
parent: null
---

# 工作区上下文 · 进入真实运行

## 绑定

| 字段 | 当前值 | 说明 |
|------|--------|------|
| 工作区 ID | `workspace-001-enter-real-operation` | 与所有共享资料引用的 `workspace_id` 一致。 |
| Root Goal | `GOAL-001-enter-real-operation` | 必须存在，且其 `parent: null`。 |
| canonical 范围 | `docs/workspaces/workspace-001-enter-real-operation/` | 当前工作区唯一的目标状态范围。 |
| 共享资料目录 | `none` | 本区不声明共享资料引用。 |
| 愿景角色 | `primary` | 本仓库唯一 primary 工作区。 |
| 规划对齐 | `VP-001-enter-real-operation` | `plan_refs` / `primary_plan` 均指向该 VP。 |

## 愿景对齐

完整治理下仓库必有唯一 [docs/vision/](../../vision/) Charter。本工作区通过必填的 `plan_refs` 与 `primary_plan` 对齐 [`VP-001-enter-real-operation`](../../vision/plans/VP-001-enter-real-operation.md)；VP 再对齐 Charter `method-engineering@0.1.0`。

`serves_summary`：把当前最小方法工程启动机制投入真实、有边界的 Method Case，并建立通过实践证据识别、定位和修正必要问题的基本闭环。

不要在本文件维护 progress% 或把愿景目录当作第二套目标树。

## 固定共享资料引用

`shared_materials_catalog: none`，本工作区不声明共享资料引用。

## 串行阶段说明

本工作区的纲领阶段写在 Root Goal `GOAL-001-enter-real-operation` 的路线图中（S1–S3）。它们承接 VP-001 的方向级阶段 D1–D3：VP 只给方向，Root 给可执行纲领阶段。纲领阶段通常串行，同一阶段内可由多个子目标并行承接。

## 备注

工作区与 Root slug 由已确认的 VP id `enter-real-operation` 派生，见 Root `D-001`。本区不预先扩展启动机制，也不把具体 Method Case 写成愿景意图。
