---
doc_type: vision-roadmap
title: 愿景规划索引
status: active
created: 2026-09-14
updated: 2026-09-26
version: 0.7.0
parent: null
---

# 愿景规划索引（组合编排）

> 本文件作为愿景层组合编排索引使用；当前仅登记已确认的 VP，不包含目标层纲领路线图、子目标编号、Goal status 或 progress%。
> VP 的状态与跟踪权威在各自 `plans/VP-*.md` 文件的 frontmatter，而不在本索引中。

## VP 索引

| id | title | status（派生投影） | vision_ref | lead_workspace | detail |
|----|-------|--------------------|------------|----------------|--------|
| [VP-001-demand-driven-method-engineering](plans/VP-001-demand-driven-method-engineering.md) | 建立需求驱动的方法工程最小运行机制 | closed | method-engineering@0.1.0 | workspace-001-method-engineering-runtime | 首个 VP；8 项退出判据已由 Root/工作区证据满足，VP 已完成有界闭门；工作区保留历史绑定 |
| [VP-002-consumer-demand-response-protocol](plans/VP-002-consumer-demand-response-protocol.md) | 定义消费方与方法工程的双向需求—响应协议 | closed | method-engineering@0.1.0 | workspace-002-consumer-response-protocol | 补足消费方发起、接收与确认交接的协议；2026-09-26 按用户指令完成有界关门。证据为一条真实流程链，不证明领域方法或 Charter 方向级成功；工作区保留历史绑定 |
| [VP-003-world-model-method-and-tools](plans/VP-003-world-model-method-and-tools.md) | 为消费方构建世界模型的方法与工具 | active | method-engineering@0.1.0 | workspace-003-world-model-method-and-tools | 承接 `WRK-002-world-model-method-and-tools` 的真实需求（下游 `WorldModel.ModernCultivation` 提报）；2026-09-26 落盘即 `active` 并绑定唯一 lead 工作区。同轮 self Vision Review 为 VRev-006（`pass`，无 required） |

## 波次关系

VP-002 是 VP-001 的后继补充规划：它沿用 VP-001 已建立的需求处理与运行记录语义，补足消费方与方法工程之间的双向交互协议。该关系不重开或替代已关闭的 VP-001。VP-002 已于 2026-09-26 按用户指令完成有界 `closed`，历史绑定保留在 `workspace-002-consumer-response-protocol`。

VP-003 是与 VP-001 / VP-002 并列的**方法侧**波次：VP-002 定义了供需双方如何发起、受理、交付与确认，但其 Non-goals 明确排除交付特定领域方法；下游经 `WRK-001` 提出的原领域方法需求未获交付，已明写须「另建处理主线」。2026-09-26 下游以 `WRK-002-world-model-method-and-tools` 正式提报《构建按需世界模型方法》，本仓受理后在 VP-003 下构建并交付方法工作版与配套工具。VP-003 不重开、不改写 VP-001 / VP-002 的结项结论。后续若出现其他 VP，再在本节记录愿景层组合关系；不在此写目标层纲领路线图、子目标编号、Goal status 或 progress%。

## 使用说明

- 新建规划：新增 `plans/VP-NNN-<slug>.md`，再在本表追加一行。
- VP 文件存在后，仍须等用户明确启动实现层，再由 `/govern` 建立工作区并将其作为 `primary_plan`。
- 本索引不是目标树、progress% 或审计意见台账。
