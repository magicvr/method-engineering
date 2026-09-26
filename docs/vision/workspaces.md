---
doc_type: vision-workspaces
title: 愿景工作区贡献图
status: active
created: 2026-09-14
updated: 2026-09-26
version: 0.7.0
parent: null
---

# 愿景工作区贡献图

> 本文件是愿景层的工作区绑定索引，不是工作区本身，也不保存 Goal 状态或 progress。
> VP-001 / VP-002 均已完成有界闭门并保留各自实现工作区的历史绑定。自 2026-09-26 起，vision 层唯一 `primary` 为 `workspace-003-world-model-method-and-tools`（`VR-006`）；`workspace-002-consumer-response-protocol` 改记为 `delivery`，其工作区本身仍为 `active`。Root 状态和进度以工作区内目标记录为准。

## 工作区索引

| workspace_id | root_goal | role | plan_refs | primary_plan | status | notes |
|--------------|-----------|------|-----------|--------------|--------|-------|
| `workspace-001-method-engineering-runtime` | `GOAL-001-method-engineering-runtime` | delivery | `VP-001-demand-driven-method-engineering` | `VP-001-demand-driven-method-engineering` | archived | VP-001 的首个实现工作区；Root 与 VP 均已完成有界结项；按 alignment 保留 VP 的历史绑定，不接收新工作。2026-09-25 起不再声称 vision 层 `primary`，角色改记为 `delivery`（`VR-004`），其历史 primary 事实保留在目标与 VP 证据中。 |
| `workspace-002-consumer-response-protocol` | `GOAL-001-consumer-response-protocol` | delivery | `VP-002-consumer-demand-response-protocol` | `VP-002-consumer-demand-response-protocol` | active | VP-002 的实现工作区；Root 已 `done`，VP-002 已有界 `closed` 并保留历史绑定。2026-09-26 起角色由 `primary` 改为 `delivery`（`VR-006`），vision 层唯一 `primary` 移交 `workspace-003`；工作区自身保持 `active`，本次不归档。 |
| `workspace-003-world-model-method-and-tools` | `GOAL-001-world-model-method-and-tools` | primary | `VP-003-world-model-method-and-tools` | `VP-003-world-model-method-and-tools` | active | VP-003 的实现工作区；2026-09-26 按用户确认开设并绑定，接管 vision 层唯一 `primary`（`VR-006`）。承接真实需求 `WRK-002-world-model-method-and-tools`（下游 `WorldModel.ModernCultivation` 提报）；Root 纲领 **R1 → R2/R3 → R4**，`progress 0%`，`I-001`～`I-004` 均 open。 |

## 约束

- 工作区角色仅允许 `primary` 或 `delivery`。
- 每个工作区必须有 `plan_refs` 与 `primary_plan`，且 `primary_plan` 必须引用已存在的 VP 文件。
- 至多一个工作区为 `primary`，且须与 `workspace.md` 的 `vision_role` 及 Charter 的 `primary_workspace` 保持一致。
- 本索引不替代显式工作区的 `workspace.md`、`goal-tree.md` 或目标五件套。
