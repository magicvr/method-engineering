---
title: protocols · 运行协议
status: active
parent: null
created: 2026-09-26
updated: 2026-09-26
version: 0.1.0
---

# protocols/ · 运行协议

本目录承载 **method-engineering 对外运行协议的唯一权威全文**——即“消费方如何提需求、双方如何协作、如何交接与验收”的可照做说明。

与相邻目录的分工：

| 目录 | 职责 |
|------|------|
| `docs/` | 目标治理框架（Charter / VP / 工作区 / 目标五件套 / 审计台账）；**不放**运行协议全文 |
| `runtime-records/` | 每条真实需求的运行主记录与事件历史（当前状态的唯一来源） |
| `protocols/`（本目录） | 与消费方协作的运行协议全文；协议约束的**状态**仍只在 `runtime-records/` |

## 现行协议

| 协议 | 状态 | 说明 |
|------|------|------|
| [`consumer-response-protocol.md`](consumer-response-protocol.md) | active（v1.0.0） | 消费方需求—响应协议。2026-09-25 起在工作区 `workspace-002-consumer-response-protocol` 内起草，2026-09-26 经一轮真实链条验证后按 I-006 升格至此，成为唯一权威全文。 |

## 边界

- 本目录**不承载**目标状态、进度、审计意见或运行记录；这些分别归 `docs/workspaces/` 与 `runtime-records/`。
- 协议升格/改写属于实现层决策：改写前须按相应目标的决策与审计流程留痕，并保持与 `runtime-records/README.md` 的语义一致。
- 工作区在升格后只保留治理证据与指向，不保留第二份可编辑全文。
