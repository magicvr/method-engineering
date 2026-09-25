---
id: GOAL-001-consumer-response-protocol
doc: decision
status: active
parent: null
created: 2026-09-25
updated: 2026-09-26
version: 0.2.6
---

# 决策记录 · GOAL-001

## 纲领路线图与阶段计划

Root 采用 `R1 冻结协议语义与运行记录衔接 → R2 形成消费方可执行的协议说明并完成试跑准备 → R3 执行并审视真实端到端试跑` 的串行路线图。纲领路线图与阶段退出条件的权威在 `00-meta.md`；本文件只登记阶段计划与影响范围的决定。

## 阶段计划

| 阶段 | 计划 / 承接目标 | 说明 |
|------|-----------------|------|
| R1 | `01-decision/D-001-bootstrap-scope.md`、`01-decision/D-002-runtime-record-boundary.md`；I-004 | 冻结双向协议语义与项目根 `runtime-records` 单一主记录的衔接方式；按 P-003 对协议语义采用 `cross` 审计。 |
| R2 | 进行中；[E-008](02-execution/E-008-r2-readiness.md)；I-001/I-002 verified | 参与、仓库、责任人、授权与最小留存边界已确认；按 [D-003](01-decision/D-003-protocol-guide-lifecycle-and-promotion.md) 在 `attachments/consumer-response-protocol.md` 编写唯一草稿并完成 self + independent Reviewer cross 复审。A-009 为 independent pass，A-010 已按 `fixed` 关闭 A-006/A-007/A-008 的 6 条 required findings；v0.1.3 仍待消费方可读可执行确认。D-005 于 2026-09-26 再确认：下游保有目录、格式与工具的最终选择权，可在提交或澄清时决定；若需向下游仓库写入响应材料，须在接受承诺和写入前确认，本次具体目录待真实需求澄清。 |
| R3 | 待 R2 退出后登记 | 对一条真实且获授权处理的需求执行端到端试跑（I-003）；按 D-004 在 method-engineering 根 `runtime-records/<work-item-id>/` 承载 record.md 与追加式 events.md，按 D-006 在可追踪真实需求信号抵达时，于 I-002 既有范围内建立「待判定」主记录并分配实际 work-item ID；登记、回执与澄清不构成接受或处理承诺，实质处理仍须 I-003 具体授权和「已接受」承诺，不在 WorldModel 克隆创建记录；修正歧义或登记有界 residual，试跑验收与指南验证后提出具体共享路径迁移方案，取得用户裁决并完成唯一全文升格和引用核对（I-006），在 Root 关门前形成 VP-002 关门证据；审计模式待真实需求范围明确后重新判定。 |

## 信息需求与阶段门禁

信息项全文与证据列以 `00-meta.md` 的「信息就绪与未知项」表为准；此处只登记门禁摘要：

| 门禁 | 相关信息项 | 当前状态 |
|------|----------------------|----------|
| R1 方案冻结前 | I-004（协议语义与运行记录衔接） | verified |
| R2 启动前 | I-001（实践方/试跑仓库/责任人）、I-002（授权与敏感信息边界） | verified；证据见 E-008 |
| R3 试跑与 VP-002 关门证据前 | I-003（一条真实且获授权的需求） | open；约束具体需求处理，不阻断 I-002 范围内的信号登记 |
| 可追踪信号抵达建档与逐案协作时（非阶段门禁） | I-005（字段、模板、work-item ID、引用、渠道） | non-blocking / open；D-004 确定试点宿主，D-006 确定 I-002 范围内信号抵达即建档并分配 ID；不新增逐条登记同意、签字或表单，其余逐案确认 |
| R3 试跑验收与指南验证后、Root 关门前 | I-006（指南共享路径与单一来源升格） | required / collecting；最终路径待用户裁决，升格尚未执行 |

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-09-25 | 工作区开设边界、Root 纲领路线图与 vision primary 转移 | accepted | `01-decision/D-001-bootstrap-scope.md` |
| D-002 | 2026-09-25 | 运行主记录生命周期边界与不受理终态 | accepted | `01-decision/D-002-runtime-record-boundary.md` |
| D-003 | 2026-09-25 | 协议指南生命周期与关门前升格 | accepted | [D-003](01-decision/D-003-protocol-guide-lifecycle-and-promotion.md) |
| D-004 | 2026-09-25 | 本次试点运行记录宿主与信息项勘误 | accepted | [D-004](01-decision/D-004-trial-runtime-record-host.md) |
| D-005 | 2026-09-25 | 下游交付选择权与写入前确认 | accepted | [D-005](01-decision/D-005-consumer-delivery-choice.md) |
| D-006 | 2026-09-26 | 信号登记时点与既有记录授权边界 | accepted | [D-006](01-decision/D-006-signal-intake-record-timing.md) |
