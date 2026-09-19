---
doc_type: vision-workspaces
title: 愿景工作区贡献图
status: active
created: 2026-09-14
updated: 2026-09-19
version: 0.8.0
parent: null
---

# 愿景工作区贡献图

> 本文件是愿景层的工作区绑定索引，不是工作区本身，也不保存 Goal 状态或 progress。
> VP-001 已完成有界闭门并保留首个实现工作区的历史绑定；Root 状态和进度以工作区内目标记录为准。

## 工作区索引

| workspace_id | root_goal | role | plan_refs | primary_plan | status | notes |
|--------------|-----------|------|-----------|--------------|--------|-------|
| `workspace-001-method-engineering-runtime` | `GOAL-001-method-engineering-runtime` | primary | `VP-001-demand-driven-method-engineering` | `VP-001-demand-driven-method-engineering` | archived | VP-001 的首个实现工作区；Root 与 VP 均已完成有界结项；按 alignment 保留 VP 的历史绑定，不接收新工作。 |
| `workspace-002-first-real-creative-practice` | `GOAL-001-first-real-creative-practice` | delivery | `VP-002-first-real-creative-practice` | `VP-002-first-real-creative-practice` | active | VP-002 的新实现工作区；book_green 已提交首轮信息，I-003 进入 D1 有界接受条件定义探索，Root 已 `active` 但 S1 尚未退出；VP-002 v0.3.0 允许 D1 有限前置方法分析。 |

## 约束

- 工作区角色仅允许 `primary` 或 `delivery`。
- 每个工作区必须有 `plan_refs` 与 `primary_plan`，且 `primary_plan` 必须引用已存在的 VP 文件。
- 本索引不替代显式工作区的 `workspace.md`、`goal-tree.md` 或目标五件套。
