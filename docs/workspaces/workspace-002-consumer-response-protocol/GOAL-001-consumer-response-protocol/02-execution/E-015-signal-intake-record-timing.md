---
id: GOAL-001-consumer-response-protocol
doc: execution-entry
record_id: E-015
status: recorded
parent: GOAL-001-consumer-response-protocol
created: 2026-09-26
updated: 2026-09-26
version: 0.2.0
---

## E-015 · 信号登记时点裁决与文档修正（2026-09-26）

用户再次确认 D-005 的下游交付选择权与承诺/写入前确认规则，并选择「按 I-002 直接登记」。已将新决定落盘为 [D-006](../01-decision/D-006-signal-intake-record-timing.md)：需要双方跟踪的可追踪真实需求信号抵达时，在既有最小留存授权范围内立即创建「待判定」主记录并分配 ID，不新增逐条登记同意、签字或表单；实质处理仍须 I-003 的具体授权与「已接受」承诺。

已同步 Root 的 I-002/I-003/I-005、决策阶段计划与门禁摘要、执行索引及 goal-tree；D-004 保留历史决定并追加后续勘误。协议草稿更新至 v0.1.2，明确建档、回执和澄清不构成承诺，保留 D-004 宿主与全仓最小留存边界，克隆中不写运行记录。

独立复审指出「涉及仓库写入」可能与试点内部运行记录相混淆。依 D-005 已接受的下游交付选择权，明确其路径、格式、工具与授权门槛针对向下游仓库写入响应交付材料；method-engineering 内部试点记录由 I-002、D-004/D-006 承载。协议草稿相应更新至 v0.1.3。

本次仅为文档修正，未获得真实需求、未分配实际 ID、未创建运行记录、未开展试跑，未访问或修改实践仓库克隆。未运行测试，未自行提交。A-006/A-007 的 5 条 findings 与 A-008 F-001 合计 6 条 required 仍开放；A-008 原意见未改写，F-001 待后续 independent 复审。本记录不是审计通过或 finding 闭合证据。I-003 open、I-005 non-blocking/open、I-006 collecting 及最终共享路径待裁决保持不变；Root active / 33%，R2 进行中且不放行，R3 未开始。
