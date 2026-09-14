---
doc_type: vision-roadmap
title: 愿景规划索引
status: active
created: 2026-09-14
updated: 2026-09-14
version: 0.1.0
parent: null
---

# 愿景规划索引（组合编排）

> 本文件是愿景层组合编排索引，**不是**目标层纲领路线图，也**不是** progress%。
> VP 的状态与跟踪权威在各自 `plans/VP-*.md` 文件的 frontmatter，而不在本索引中。

## VP 索引

| id | title | status（派生投影） | vision_ref | lead_workspace | detail |
|----|-------|--------------------|------------|----------------|--------|
| VP-001-enter-real-operation | 让方法工程进入真实运行 | active | method-engineering@0.1.0 | workspace-001-enter-real-operation | [plans/VP-001-enter-real-operation.md](plans/VP-001-enter-real-operation.md) |

> **`status` 列只是派生投影**：其权威是 `plans/VP-*.md` 的 frontmatter；本列不得用于任何门禁判定，也不构成第二权威。发现不一致时以 VP 文件为准并刷新本列。

## 波次关系

```text
Charter · 可靠的方法工程能力（method-engineering@0.1.0）
  → 意图 1 · 让方法工程进入真实运行
      → VP-001-enter-real-operation（当前波次）
          → lead：workspace-001-enter-real-operation
```

当前只有一个已落盘意图、一个绑定工作区。本索引只记录愿景层的先后、并行与 lead 区关系；不写目标层纲领路线图、子目标编号、Goal status 或 progress%。

## 使用说明

- 新建规划：新增 `plans/VP-NNN-<slug>.md`，再在本表追加一行。
- 未开工：VP `status: planned`，绑定工作区可为 0。
- `active` 且 0 区：遵守 [`alignment.md`](alignment.md) 的空转规则并告警，不静默当健康推进。
- 关门：先在 VP 文件写关门摘要与区证据链接，再刷新本表的投影列（不得反向：不以本表为准改 VP 状态）。
- 在 VP 文件存在且 `vision_ref` 精确匹配前，不得将草案用作 `primary_plan`。
- 本索引不是目标树、progress% 或审计意见台账。
