---
doc_type: vision-workspaces
title: 愿景工作区贡献图
status: active
created: 2026-09-14
updated: 2026-09-18
version: 0.3.0
parent: null
---

# 愿景工作区贡献图

> 本文件是愿景层的工作区绑定索引，不是工作区本身，也不保存 Goal 状态或 progress。
> VP-001 已激活并绑定首个实现工作区；Root 状态和进度以工作区内目标记录为准。

## 工作区索引

| workspace_id | root_goal | role | plan_refs | primary_plan | status | notes |
|--------------|-----------|------|-----------|--------------|--------|-------|
| `workspace-001-method-engineering-runtime` | `GOAL-001-method-engineering-runtime` | primary | `VP-001-demand-driven-method-engineering` | `VP-001-demand-driven-method-engineering` | active | VP-001 的首个实现工作区；当前按 Root 的 S1–S3 路线图推进。 |

## 约束

- 工作区角色仅允许 `primary` 或 `delivery`。
- 每个工作区必须有 `plan_refs` 与 `primary_plan`，且 `primary_plan` 必须引用已存在的 VP 文件。
- 本索引不替代显式工作区的 `workspace.md`、`goal-tree.md` 或目标五件套。
