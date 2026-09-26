---
id: GOAL-001-consumer-response-protocol
title: 落地消费方需求—响应协议并完成真实对接链条
status: active
parent: null
plan_refs: VP-002-consumer-demand-response-protocol
primary_plan: VP-002-consumer-demand-response-protocol
serves_summary: 将 VP-002 的双向需求—响应意图落地为消费方可照做的协议说明，并通过双方共同的真实流程链验证交接。
created: 2026-09-25
updated: 2026-09-26
version: 0.3.5
progress: 100%
---

# GOAL-001 · 落地消费方需求—响应协议并完成真实对接链条

## 概述

本 Root 承接 [`VP-002-consumer-demand-response-protocol`](../../../vision/plans/VP-002-consumer-demand-response-protocol.md)，先冻结双向协议与运行记录衔接，再形成可执行指南，最后以跑通链条为真实目的，由双方在实践仓库完成 WRK-001 的有界交接。当前范围依据用户裁决 [D-008](01-decision/D-008-wrk001-real-chain.md)；D-007 保留为先前决定。

本 Root 不建设 API、Web UI、自动化派发、跨仓同步服务或特定平台适配器；不为所有消费仓统一仓库结构；不交付特定领域方法，也不把一次试跑写成协议普遍适用或具体方法有效的证明。试跑只验证协议的可理解性、可执行性与交接连贯性。

## 成功标准

- [x] 消费方协议明确需求发起入口、最低必要信息、参与角色与授权边界，并允许先提交真实问题信号、后由双方澄清方法需求；不把提交者预先证明方法缺口作为受理前提。
- [x] 下游拥有真实需求响应的交付目录、格式与工具最终选择权，可在提交或澄清时确定；形成真实「已接受」承诺及任何真实响应写入前，须确认路径、格式、工具和授权。本次 R3 的 WRK-001 已接受真实流程处理承诺；下游路径、格式、工具与写入授权按 I-008 核对。I-002 范围内的 method-engineering 运行记录依 D-004/D-006 承载，不由未定的响应交付路径阻挡；无需文件交付时约定沟通渠道，不把完整路径作为首次提交强制字段。
- [x] 双方协议明确回执、澄清、受理/不受理、处理边界与限额、状态沟通、范围变化和退出路径，且与 VP-001 的授权语义一致。
- [x] 协议明确响应包及交接责任，区分交付、收件回执、响应验收与异议；消费方能够按约定表达接受或具体异议，双方明确异议是否落在原承诺内及后续责任归属。
- [x] 反馈分类、运行记录引用与新需求重入方式明确；当前运行状态仍由约定的单一主记录维护，事件记录不构成第二状态源。
- [x] 双方沿真实 WRK-001 追踪线完成一次需求提交、回执/澄清与授权、接受承诺、响应形成与验证、交付、实际收件、验收或异议、反馈路由与结束；交接材料使用下游选定的 exchange/WRK-001/，逐次核对双方实际消费的版本与下一责任。只交付本次可使用的交接约定、往返材料及核对结论，不构建或验证领域方法。不得预填对方回执或拼接单侧 walkthrough；同人双角色须记录角色切换。R3 完成后仍须按 I-006 取得共享路径裁决并升格指南，再审计关门。
- [x] 试跑证据能复核协议的实际可读性与交接结果；发现的歧义已修正，或被明确列为有界 residual 且不遮蔽本 Root 声称完成的范围。

- [ ] R3 试跑验收与指南验证完成后、Root 关门前，将协议指南唯一权威全文升格到用户确认的本仓共享运行文档路径，并核对引用；工作区仅保留治理证据与指向，不保留两份可编辑全文。最终路径仍待 R3 后用户裁决（I-006）。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|------|------|------|----------|
| **R1** | 冻结协议语义与运行记录衔接 | 已完成 | 双向协议语义（回执、澄清、受理/不受理、边界与限额、状态沟通、范围变化、退出、交付/收件/验收/异议区分、反馈分类与新需求重入）与 VP-001 的运行记录语义衔接方式冻结并落盘；I-004 经 self + independent 核验为 `verified`；相关 required finding 为 0。 |
| **R2** | 形成消费方可执行的协议说明并完成试跑准备 | 已完成 | 消费方可直接照做的协议说明在 `attachments/consumer-response-protocol.md` 落盘，经 self + independent Reviewer cross 审计且 required finding 全部闭合；由目标消费方确认可读可执行；I-001/I-002 `verified`。证据见 A-009、A-010、A-011 与 E-018。 |
| **R3** | 执行并审视真实对接链条 | 已完成（2026-09-26） | 双方沿真实 WRK-001 追踪线完成一次需求提交、回执/澄清与授权、接受承诺、响应形成与验证、交付、实际收件、验收或异议、反馈路由与结束；交接材料使用下游选定的 exchange/WRK-001/，逐次核对双方实际消费的版本与下一责任。只交付本次可使用的交接约定、往返材料及核对结论，不构建或验证领域方法。不得预填对方回执或拼接单侧 walkthrough；同人双角色须记录角色切换。R3 完成后仍须按 I-006 取得共享路径裁决并升格指南，再审计关门。证据见 E-027/E-028 与 A-020。 |

R1 → R2 → R3 串行：协议语义未冻结前不形成对外说明；试跑准备与授权未完成前不启动实际对接。同一阶段内若出现具有独立范围、依赖或交付证据的工作，才创建平铺子目标。

## 派生进度展示

`progress: 100%` 由上方 3 个纲领阶段等权计算（已完成 3 / 3）。该值仅作展示，不放行阶段、不关闭 finding、不覆盖信息门禁，也不自动推导 `status: done`。Root 状态变更依据阶段退出条件与审计证据，不由 progress 单独推导——当前 **Root 仍为 `active`**，因为指南升格（I-006）与 Root 关门审计尚未完成。

## 信息就绪与未知项

| ID | 级别 | 所需信息 / 问题 | 影响门禁 | 最晚需要阶段 | 验证 / 收集动作 | 状态 | 延期 / 复核 | 证据 / 结论 |
|----|------|-----------------|----------|--------------|-----------------|------|-------------|-------------|
| I-001 | required | 真实下游实践方是谁、其真实实践所用的试跑仓库是哪一个、参与责任人如何确认协作与责任边界。 | R2 启动（试跑准备与授权） | R2 | 由用户指定候选方，取得对方对参与、试跑仓库与责任人的明确确认后落盘。 | verified | 用户确认本人作为真实消费方/实践方参与，以 WorldModel.ModernCultivation 为真实实践试跑仓库；维护人与本仓维护人相同。参与方、仓库或责任边界变化时复核。 | [E-008](02-execution/E-008-r2-readiness.md)：用户参与确认与 SCOUT 本地克隆只读检查；此前候选记录见 E-006/E-007。 |
| I-002 | required | 试跑所需的使用/记录授权边界与敏感信息处理约定（可记录哪些内容、如何脱敏、保留何种可核对依据）。 | R2 启动、R3 证据落盘 | R2 | 与方法工程一侧及消费方共同确认授权范围与脱敏规则，并落盘为可引用的约定。 | verified | 用户授权操作试跑仓库所有文件；本仓仅保留去标识化需求摘要、协议过程、响应/验收结果、仓库路径和提交引用，不保留原始个人或敏感材料。收到需要双方跟踪的可追踪真实需求信号时，按该既有范围立即建「待判定」主记录并分配 ID，不新增逐条登记同意、签字或表单。超出该范围前重新确认；具体需求处理授权仍由 I-003 核验。 | [E-008](02-execution/E-008-r2-readiness.md)：用户授权与最小留存约定；[D-006](01-decision/D-006-signal-intake-record-timing.md)：信号登记时点裁决。 |
| I-003 | required | WRK-001 真实流程链的具体边界、限额、角色、授权与最低验证方向。 | R3 接受承诺前 | R3 | 核对用户明确修订及 D-008 逐项接受依据。 | verified | 仅覆盖一条流程链；超出范围或角色/限额变化时复核。原领域需求未完成。 | [D-008](01-decision/D-008-wrk001-real-chain.md)、E-008、EV-003；当前主记录已接受，非验收结果。 |
| I-004 | required | 双向协议语义（回执、澄清、受理/不受理、边界、交付/收件/验收/异议区分、反馈分类与重入）与项目根 `runtime-records` 单一主记录及事件追踪的具体衔接表达。 | R1 方案冻结 | R1 | 将经用户确认的生命周期边界映射到 `runtime-records/README.md`，由 self + independent 复核语义不产生第二状态源，且所有相关 required findings 合法闭合。 | verified | A-004 independent 复核确认 A-002 F-001～F-003 的文档修正；A-005 已逐项以 fixed 合法闭合，I-004 证据与当前摘要一致。 | `01-decision/D-002-runtime-record-boundary.md`；`runtime-records/README.md`；`03-audit/A-001-r1-self-review.md`；`03-audit/A-002-r1-independent-review.md`；`03-audit/A-003-r1-remediation-rereview.md`；`03-audit/A-004-r1-final-independent-review.md`；`03-audit/A-005-r1-finding-closure.md` |
| I-005 | non-blocking | 运行记录的具体字段、模板、work-item ID、引用字段及沟通渠道等尚未确定的物理承载细节。 | 不阻断 R2 协议语义；具体建档与协作时核对适用细节 | 可追踪信号抵达建档与逐案协作时 | 沿用既有 record.md + events.md 模式；按 D-006 在需要双方跟踪的可追踪真实需求信号抵达时，于 I-002 既有最小留存范围内建立「待判定」主记录并分配实际 work-item ID；字段、引用和渠道按需逐案确认，不增加登记手续，不以 I-003 处理授权作为建档前提。 | open | 责任人：运行记录维护者与消费方；复核触发：可追踪真实需求信号抵达及建档准备。尚未定案的细节不得写成已验证。 | D-002 第 5、11 项保留原信息项身份；[D-004](01-decision/D-004-trial-runtime-record-host.md) 仅确定本次试点宿主与目录模式，[D-006](01-decision/D-006-signal-intake-record-timing.md) 确定信号建档和 ID 时点；D-008 确认本次未承诺修订沿用 ID、承载与渠道；其余通用细节仍待逐案确定。 |
| I-006 | required | 协议指南经 R3 验证后的本仓共享运行文档承载路径与单一权威全文迁移方案。 | R3 升格、Root 关门 | R3 试跑验收与指南验证后、Root 关门前 | R2/R3 在 `attachments/consumer-response-protocol.md` 维护唯一草稿；R3 提供证据后提出具体共享路径与迁移方案，请用户确认，再迁移唯一来源并核对引用。 | collecting | 责任人：本仓维护人（用户）裁决路径，编排器准备方案并执行；复核触发：R3 试跑验收与指南验证完成。此前不预选最终路径，未完成升格不得关门。 | [D-003](01-decision/D-003-protocol-guide-lifecycle-and-promotion.md)、[E-009](02-execution/E-009-protocol-guide-promotion-timing.md)：用户已确认归属、临时路径策略与升格时点；最终共享路径及迁移结果未验证。 |
| I-007 | required | 真实方法需求与 Root 非目标的范围冲突。 | R3 范围重新对齐 | R3 范围修订时 | 按用户要求修改 VP 与 Root 退出条件，解除方法构建依赖。 | resolved | D-007 当时将 WRK-001 移出 R3；后经 D-008 用户明确修订为流程链并重新纳入。本次仍排除领域方法构建。本项以范围决定解决，不代表需求处理条件已验证。 | [D-007](01-decision/D-007-protocol-rehearsal-realignment.md)；[D-008](01-decision/D-008-wrk001-real-chain.md) |
| I-008 | required | 真实流程链角色、共享追踪、核对办法及下游路径、格式、工具与写入授权。 | R3 联调与下游材料写入前 | R3 | 核对用户裁决 D-009、下游 D-008 / exchange/README 的材料类型范围及既有目录、格式、核对和授权约定；由 independent rereview 核对 A-016 F-001 的整改证据。 | verified | 用户已选择窄幅扩展；下游契约明确当前 WRK-001 一条流程链的交接约定、实际往返材料与核对结论，并保留非 canon、人工核对、无新工具与单一运行状态来源边界。A-016 F-001 已由 A-018 独立复审通过并经 A-019 以 `fixed` 闭合，写入阻断解除。复核触发：范围超出当前一条链、材料类型变化或双方路径/格式/工具约定变更。`verified` 不代表实际交接已发生。 | [D-009](01-decision/D-009-exchange-process-material-scope.md)、[E-024](02-execution/E-024-exchange-contract-extension.md)、下游 D-008 / exchange/README、[A-016](03-audit/A-016-wrk001-independent-cross-review.md)、[A-018](03-audit/A-018-f001-contract-rereview.md)、[A-019](03-audit/A-019-f001-closure-response.md)。 |

> `resolved` 仅表示 I-007 的范围问题由用户裁决解决，不代替 I-003/I-008 的授权核对或实际交接证据。本表只登记已识别的未知与门禁；未获 `verified` 或用户书面接受的 `accepted-residual` 前，不得把上述项目写成已确认事实。到达最晚需要阶段仍为 `open` 的 required 项按 P-005 阻断对应门禁。

## R1 实施前审计模式

R1 涉及协议边界和运行记录语义，按 P-003 风险表采用 **`cross`**：本编排器 self 审 + 用户指定的上下文独立 Codex Reviewer 子代理审计。用户已在本轮指定该 provider。当前派发接口不能传入仓库 `reviewer.toml` 的 `sandbox_mode` 与完整 developer instructions；任务将明确要求只读，审计意见以该独立会话实际产出为准，不宣称项目角色 TOML 已完整生效，也不将其描述为第三方鉴证。R2/R3 的模式按各自 scope 判定，见下文。

## R2 实施计划与审计模式

按 [D-003](01-decision/D-003-protocol-guide-lifecycle-and-promotion.md)，先在本目标 `attachments/consumer-response-protocol.md` 编写唯一协议草稿，再完成 self + 上下文独立 Codex Reviewer 的 **cross** 审计，最后取得消费方可读可执行确认。R2 涉及跨边界运行协议，依 P-003 采用 cross；草稿 v0.1.3 已完成复审：A-009 independent verdict 为 pass，A-010 已按 `fixed` 闭合 A-006/A-007/A-008 共 6 条 required findings，当前开放 required 为 0。用户已在 E-018 确认指南可执行，A-011 自审通过并关闭 R2。独立 provider 沿用本会话指定的 Codex Reviewer；派发限制同上。R1、R2 已完成，Root 保持 active；`progress` 现为 100%（3/3 阶段），但状态仍为 `active`。按 D-008，R3 承接 WRK-001 的真实流程链请求；WRK-001 运行主线已由「已接受」经「已交付」转**已退出**（E-028、EV-008/EV-009）。I-003 required/verified 证明本次边界与授权；I-008 required/verified，契约修订已经 A-018 独立复审通过并由 A-019 合法闭合 F-001，下游实际写入阻断解除。真实双边交接已完成一轮并获消费方接受（消费方动作经用户授权代行并标明）。I-006 required/collecting 继续阻断升格与关门。原领域方法需求保留为历史且未完成；未创建后继 VP，也未满足下游 Root 的方法构建成功标准。本次规则与范围修订已完成 cross 审视闭环：A-015 self pass 与 A-016 independent fail 的历史 verdict 保留；用户按 D-009 选择窄幅修复路径，A-017 以 `fixed` 关闭 F-002，A-018（independent，grok build / grok-4.6 / effort high）复审 pass 且无 required finding，A-019 以 `fixed` 关闭 F-001，当前开放 required 为 0。R3 下游写入已解除阻断；2026-09-26 完成一轮真实往返：交付 v1 → 消费方第 1 轮收件与两条范围内异议 → 交付 v1.1（补引用坐标与环节—材料对照） → 消费方第 2 轮验收**接受** → 反馈路由与结束（对象问题 2、运行机制问题 1、方法问题 0）。R3 阶段由 A-020 self 复核判为**完成**，`progress` 派生为 100%；WRK-001 运行主线状态为「已退出」。**Root 仍为 `active`**：I-006 指南升格与 Root 关门审计尚未完成。原领域方法需求保留为历史且未完成；未创建后继 VP，也未满足下游 Root 的方法构建成功标准。D-007 的历史范围重新对齐按 cross 审视：A-012 self pass，A-013 上下文独立 Reviewer 为 conditional / ACCEPT WITH NOTES，A-014 已 `fixed` 响应两条 minor；无开放 required findings。D-005 于 2026-09-26 再确认下游拥有交付目录、格式与工具最终选择权；可在提交或澄清时确定，向下游仓库写入响应材料前须按对应信息门禁确认承载与授权。

## 愿景对齐

- `plan_refs`: `VP-002-consumer-demand-response-protocol`
- `primary_plan`: `VP-002-consumer-demand-response-protocol`
- 服务摘要：本目标只实现 VP-002 的双向协议与一次真实对接链条，不扩大 Charter 或 VP 的方向边界，不证明具体方法普遍有效。
- 现行 Charter：[`method-engineering@0.1.0`](../../../vision/charter.md)。
- 与 VP-001 的关系：沿用其「已接受需求」/IDLE 权威与单一运行主记录语义，一般消费仓根目录所有权规则保持不变；真实需求仍依 D-004 在 method-engineering 根 `runtime-records/<work-item-id>/` 承载；R3 复用用户明确修订的真实 WRK-001，并保留全部历史事件。

## 父目标

本目标为当前工作区唯一 Root，`parent: null`。VP-002 是愿景层规划，不是本目标的 `parent`。

## 台账布局

本目标使用平铺的 `01-decision/`、`02-execution/`、`03-audit/` 和 `attachments/`。索引文件保留稳定入口；新增决定、事实和正式审计意见分别写入对应 ledger 目录。本仓全域（含 attachments、运行主记录与事件）仅保留去标识化需求摘要、协议过程、响应/验收结果、实践仓库路径和提交引用；使用角色标签或责任引用，不留存原始个人或敏感材料。超出范围须暂停并取得用户明确追加授权。
