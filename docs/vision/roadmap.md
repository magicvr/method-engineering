---
doc_type: vision-roadmap
title: 愿景规划索引
status: active
created: 2026-09-14
updated: 2026-09-26
version: 0.6.1
parent: null
---

# 愿景规划索引（组合编排）

> 本文件作为愿景层组合编排索引使用；当前仅登记已确认的 VP，不包含目标层纲领路线图、子目标编号、Goal status 或 progress%。
> VP 的状态与跟踪权威在各自 `plans/VP-*.md` 文件的 frontmatter，而不在本索引中。

## VP 索引

| id | title | status（派生投影） | vision_ref | lead_workspace | detail |
|----|-------|--------------------|------------|----------------|--------|
| [VP-001-demand-driven-method-engineering](plans/VP-001-demand-driven-method-engineering.md) | 建立需求驱动的方法工程最小运行机制 | closed | method-engineering@0.1.0 | workspace-001-method-engineering-runtime | 首个 VP；8 项退出判据已由 Root/工作区证据满足，VP 已完成有界闭门；工作区保留历史绑定 |
| [VP-002-consumer-demand-response-protocol](plans/VP-002-consumer-demand-response-protocol.md) | 定义消费方与方法工程的双向需求—响应协议 | active | method-engineering@0.1.0 | workspace-002-consumer-response-protocol | 补足消费方发起、接收与确认交接的协议；2026-09-25 按用户指令激活并挂接首个 `primary` 工作区；2026-09-26 按用户要求进一步修订为真实消费仓参与的实际对接链条，链条本身为真实需求；不要求完成真实领域方法构建 |

## 波次关系

VP-002 是 VP-001 的后继补充规划：它沿用 VP-001 已建立的需求处理与运行记录语义，补足消费方与方法工程之间的双向交互协议。该关系不重开或替代已关闭的 VP-001。VP-002 已于 2026-09-25 按用户指令进入 `active`，并挂接首个实现工作区 `workspace-002-consumer-response-protocol`（`primary`）。后续若出现其他 VP，再在本节记录愿景层组合关系；不在此写目标层纲领路线图、子目标编号、Goal status 或 progress%。

## 使用说明

- 新建规划：新增 `plans/VP-NNN-<slug>.md`，再在本表追加一行。
- VP 文件存在后，仍须等用户明确启动实现层，再由 `/govern` 建立工作区并将其作为 `primary_plan`。
- 本索引不是目标树、progress% 或审计意见台账。
