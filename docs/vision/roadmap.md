---
doc_type: vision-roadmap
title: 愿景规划索引
status: active
created: 2026-09-14
updated: 2026-09-18
version: 0.4.0
parent: null
---

# 愿景规划索引（组合编排）

> 本文件作为愿景层组合编排索引使用；当前仅登记已确认的 VP，不包含目标层纲领路线图、子目标编号、Goal status 或 progress%。
> VP 的状态与跟踪权威在各自 `plans/VP-*.md` 文件的 frontmatter，而不在本索引中。

## VP 索引

| id | title | status（派生投影） | vision_ref | lead_workspace | detail |
|----|-------|--------------------|------------|----------------|--------|
| [VP-001-demand-driven-method-engineering](plans/VP-001-demand-driven-method-engineering.md) | 建立需求驱动的方法工程最小运行机制 | closed | method-engineering@0.1.0 | workspace-001-method-engineering-runtime | 首个 VP；8 项退出判据已由 Root/工作区证据满足，VP 已完成有界闭门；工作区保留历史绑定 |

## 波次关系

VP-001 是当前唯一规划，暂无与其他 VP 的先后或并行关系。后续若出现新的 VP，再在本节记录愿景层组合关系；不在此写目标层纲领路线图、子目标编号、Goal status 或 progress%。

## 使用说明

- 新建规划：新增 `plans/VP-NNN-<slug>.md`，再在本表追加一行。
- VP 文件存在后，仍须等用户明确启动实现层，再由 `/govern` 建立工作区并将其作为 `primary_plan`。
- 本索引不是目标树、progress% 或审计意见台账。
