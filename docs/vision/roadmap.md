---
doc_type: vision-roadmap
title: 愿景规划索引
status: active
created: 2026-09-14
updated: 2026-09-19
version: 0.9.0
parent: null
---

# 愿景规划索引（组合编排）

> 本文件作为愿景层组合编排索引使用；当前仅登记已确认的 VP，不包含目标层纲领路线图、子目标编号、Goal status 或 progress%。
> VP 的状态与跟踪权威在各自 `plans/VP-*.md` 文件的 frontmatter，而不在本索引中。

## VP 索引

| id | title | status（派生投影） | vision_ref | lead_workspace | detail |
|----|-------|--------------------|------------|----------------|--------|
| [VP-001-demand-driven-method-engineering](plans/VP-001-demand-driven-method-engineering.md) | 建立需求驱动的方法工程最小运行机制 | closed | method-engineering@0.1.0 | workspace-001-method-engineering-runtime | 首个 VP；8 项退出判据已由 Root/工作区证据满足，VP 已完成有界闭门；工作区保留历史绑定 |
| [VP-002-first-real-creative-practice](plans/VP-002-first-real-creative-practice.md) | 支持首个真实作品完成故事线规划大纲 | active | method-engineering@0.1.0 | — | 第二个 VP；以作品方接受包含故事线规划的大纲为有界终点；若接受条件/下一阶段未知，D1 可在四周总上限内探索作品自身的创作边界；局部方法需求由 Method Engineering 主导澄清、构建、交付和迭代，不受 D1 作为统一门禁的阻挡；D1/D2 可并行或局部交错，Goal 由具体需求动态生成，已绑定 `workspace-002-first-real-creative-practice`（delivery） |

## 波次关系

VP-001 建立并关闭了需求驱动的方法工程最小运行机制；VP-002 在其机制基础上进入首个真实作品支持波次。VP-002 只覆盖该作品到包含故事线规划的大纲接受点，后续详细创作如仍需支持，应另设有界意图；本节不写目标层纲领路线图、子目标编号、Goal status 或 progress%。

## 使用说明

- 新建规划：新增 `plans/VP-NNN-<slug>.md`，再在本表追加一行。
- VP 文件存在后，仍须等用户明确启动实现层，再由 `/govern` 建立工作区并将其作为 `primary_plan`。
- 本索引不是目标树、progress% 或审计意见台账。
