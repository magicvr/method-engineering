---
id: GOAL-001-consumer-response-protocol
doc: decision-entry
record_id: D-010
status: accepted
parent: GOAL-001-consumer-response-protocol
created: 2026-09-26
updated: 2026-09-26
version: 0.1.0
---

## D-010 · 协议指南共享承载路径：`protocols/`

用户于 2026-09-26 就 I-006 指示：**`docs/` 保留给目标治理框架，另规划合理路径；并评估是否与 VP-001 的结果放在一起**。据此裁决如下。

### 决定

协议唯一权威全文升格至仓库根的 **`protocols/consumer-response-protocol.md`**（v1.0.0），并在 `protocols/README.md` 登记其职责与目录分工；`README.md` 与 `runtime-records/README.md` 各加一处指向。工作区 `attachments/consumer-response-protocol.md` 改为指向存根。

### 为什么不与 VP-001 的结果（`runtime-records/`）放在一起

- `runtime-records/` 是**运行记录容器**，其 [`README.md`](../../../../../runtime-records/README.md) 明确约定目录形态为 `README.md` + `<work-item-id>/`，并规定「每条处理主线使用一个稳定的 `<work-item-id>` 目录」。协议全文不是处理主线，放入其中要么破坏该约定，要么迫使改写 VP-001 已关闭的结果文档。
- 该目录的语义是「承载某条需求从待判定到接受/终结的运行主线」；协议是**跨主线**的协作规则，层级不同。
- `protocols/` 与 `runtime-records/` **并列**于仓库根，且两者互相指向（协议 §去哪里看当前状态 ↔ 记录说明）。因此仍满足用户「与 VP-001 结果就近」的意图，只把「记录」与「协议」两类对象分开。

### 未选方案

- **`runtime-records/consumer-response-protocol.md`**：与目录既有约定冲突（见上）。
- **`docs/` 内任意位置**：用户已明确 `docs/` 留给目标治理框架。
- **仓库根单文件 `PROTOCOL.md`**：单文件省事，但缺少同类协议继续增加的落点；`protocols/README.md` 可承载目录职责，避免日后各自为政。

### 影响

- I-006 由 `collecting` 转 `verified`（升格与引用核对见 [E-029](../02-execution/E-029-protocol-guide-promotion.md)）。
- 不改变协议语义：v1.0.0 与升格前的 v0.2.2 内容一致，仅更新文首/文末的升格说明与相对链接。
- 本决定不涉及 Root `status`；关门仍须独立的关门审计。
