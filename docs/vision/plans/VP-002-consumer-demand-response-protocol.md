---
doc_type: vision-plan
id: VP-002-consumer-demand-response-protocol
title: 定义消费方与方法工程的双向需求—响应协议
status: closed
vision_ref: method-engineering@0.1.0
lead_workspace: workspace-002-consumer-response-protocol
created: 2026-09-25
updated: 2026-09-26
version: 0.4.1
parent: null
---

# VP-002 · 定义消费方与方法工程的双向需求—响应协议

## Problem

VP-001 建立了方法工程一侧的需求处理状态、授权边界、响应选择、验证、交付、反馈与运行记录承载。其 Non-goals 明确排除了跨仓库请求协议与消费适配器，因此并未定义消费方如何实际发起需求、跟踪处理、接收并确认响应。

现有机制能说明一条需求应如何被记录和处理，却不足以让一个消费仓仅凭协议完成两侧交接。尤其是，需求“被方法工程接受处理”与消费方“确认收到交付”或“验收响应”是不同事件；没有明确区分时，双方可能对承诺、完成与异议处理产生不同理解。

## 术语与适用对象

本 VP 所称**消费方 / 下游需求方**，是直接参与真实下游实践、提出方法需求并接收响应的个人或团队。**试跑仓库**是承载该实践或其请求记录的真实项目仓库；它是否安装了 goal-governance 治理包，不决定其是否属于本 VP 的试跑对象。这里的消费方/试跑仓库，不等同于 `alignment.md` 与消费核对表中“安装并使用 goal-governance 包的消费项目”。本 VP 的退出验证采用真实的对接流程需求：双方在真实实践仓库沿同一处理主线完成实际交接，需求目的本身是跑通链条，不要求领域方法构建。

## Intent

定义并验证一套工具无关的双向协议，使真实下游实践中的消费方能够按清晰约定提出方法需求、参与澄清与授权、了解处理状态、接收响应并表达验收或异议；方法工程一侧能够回执、澄清、接受或不接受处理承诺、交付有边界的响应并接收反馈。协议须与 VP-001 的运行记录语义衔接，不产生第二套运行状态来源。

## Desired Outcome

VP-002 完成时：

- 消费方有一份可直接照做的说明，知道如何发起可追踪的真实需求、提供哪些最低信息、由谁确认边界与授权，以及如何提出澄清和范围变更。
- 方法工程一侧有一致的接收回执、澄清、受理/不受理、边界与限额确认、状态沟通和有界退出约定。
- 双方明确区分“已收到请求”“已接受处理承诺”“已交付响应”“已确认收到交付”和“已验收/提出异议”，并知道每种情况如何记录与继续处理。
- 响应交接能够说明版本、适用条件、验证结论、证据、限制、未决事项与后续责任；反馈可按对象问题、方法问题或运行机制问题回流至既有运行机制。
- 至少一个真实消费仓与方法工程共同完成一条共享追踪线上的真实对接链条；双方实际消费对方交接内容，完成信号、回执/澄清、处理范围与授权、响应交接、收件反馈与结束。
- 流程试跑只验证协议的可理解性、可执行性与交接连贯性，不证明具体方法普遍有效，也不代表协议已适用于所有消费仓。

## Scope

1. 消费方如何识别并提交来自真实实践的方法需求；最低上下文、来源、责任人、边界、授权和追踪信息；信息不足时如何澄清而不要求提交者先证明方法缺口。
2. 方法工程一侧的接收回执、澄清、受理/不受理、处理承诺、工作边界、限额、责任交接与状态沟通。
3. 响应交付的内容与边界，以及消费方的收件确认、验收、异议、补充反馈和责任承接方式；明确交付回执不等同于响应验收，响应验收也不等同于证明普遍有效。
4. 反馈分类、范围变更、退出与新需求重入规则，以及双边协议与 `runtime-records` 主记录和事件追踪之间的引用关系。
5. 与至少一个真实下游需求方在其真实实践仓库中共同开展真实对接链条，以跑通链条为真实目的，使用非敏感的实际交接材料，记录并修正交接歧义；不要求构建领域方法。

本 VP 冻结交互意图与退出方向，不预先冻结具体目录位置、文件字段、Issue/PR 模板、消息工具或安装方式；下游交付路径、格式与工具由下游最终选择，方法工程仅协助澄清，任何下游写入前均须明确确认。

## Non-goals

- 建设 API、Web UI、自动化派发、跨仓同步服务或特定平台/工具适配器。
- 为所有消费仓建立统一仓库结构，或声称一次流程试跑证明协议普遍适用。
- 交付某个特定领域方法、保证消费方必须接受响应，或证明响应的普遍有效性。
- 替代 VP-001 的运行记录状态、目标治理状态、信息门禁或审计台账。
- 虚构需求、回执、验收或方法有效性证据；真实流程请求沿既有运行协议形成承诺并追踪，不把过程成功等同领域方法交付。

## 与 Charter 和 VP-001 的关系

本 VP 承接 Charter 的真实问题优先与证据驱动方向，补足 VP-001 明确未覆盖的消费侧交互边界。VP-001 仍作为已完成的需求处理与记录机制保留；VP-002 不追溯改写其原退出判据，也不把任何一次试跑扩写为具体方法有效性或 Charter 方向级成功的证明。

### 与 VP-001 运行语义的衔接

- 是否形成处理承诺，以及承诺对整体 IDLE 的影响，仍以 VP-001 的「已接受需求」与 IDLE 语义为准。收到请求或发出回执本身不等于接受处理承诺；未接受的信号仍按 VP-001 的待判定语义处理。
- 消费方收件回执、响应验收或异议是交接/反馈事件，不新增运行状态，也不另立当前状态来源；它们关联在同一条处理主记录与其事件追踪中。事件历史不能替代主记录的当前状态。
- 本 VP 提到的 `runtime-records`，指 VP-001 已确立的单一运行主记录与追加式事件追踪语义；此处不冻结物理存放路径、字段、目录或通信工具。其具体承载由实现工作区按运行责任决定。

## 方向级退出判据

在同时满足下列方向时，本 VP 可以进入有界关门路径；具体证据应由后续工作区承载：

1. 消费方协议明确需求发起入口、最低必要信息、参与角色与授权边界，并允许先提交真实问题信号、后由双方澄清方法需求；不得把提交者预先证明方法缺口作为受理前提。
2. 双方协议明确回执、澄清、受理/不受理、处理边界与限额、状态沟通、范围变化和退出路径，且与 VP-001 的授权语义一致。
3. 协议明确响应包及交接责任，区分交付、收件回执、响应验收与异议；消费方能够按约定表达接受或具体异议，双方知道异议是否落在原承诺内以及后续责任由谁承担。
4. 反馈分类、运行记录引用和新需求重入方式明确；当前运行状态仍由约定的单一主记录维护，事件记录不构成第二状态源。
5. 至少一个真实下游需求方与方法工程在真实实践仓库中共同完成真实对接链条：承接真实流程需求且不含敏感内容，沿一条共享追踪线实际消费对方交接，覆盖“信号 → 回执/澄清 → 处理范围与授权 → 响应交接 → 消费方收件与反馈 → 结束”。两侧各自 walkthrough 后拼接、只有生产侧内部记录、治理包安装演练均不能替代双边集成证据；不要求交付真实领域方法。若同一人承担消费方与方法工程角色，须记录角色切换；证据只证明本次对接流程实际执行，不声称独立团队达成共识。
6. 试跑证据能复核协议的实际可读性与交接结果；发现的歧义已经修正或被明确列为有界 residual，并且残余不遮蔽本 VP 声称完成的范围。

VP-002 关门须链接双方共同联调的实施与结项证据，明确证据所证明的协议范围。实际参与方、共享追踪、交接消费或处理授权尚未落实时保持未关门。真实方法构建需求不作为本 VP 的退出前提。

## 实施前待确认

本节保留 2026-09-26 范围修订当时的确认状态，不作为关门后的当前缺口。参与方与真实实践仓库已经确认；用户明确将既有未承诺请求修订为真实流程目的。实际交接与验收已由工作区证据完成，见下方关门核对；本次不构建领域方法、不自动创建后继 VP。

## 方向级阶段结构

| 阶段 | 方向（非交付承诺） |
|------|--------------------|
| R1 | 冻结消费方—方法工程双向协议语义及与 VP-001 运行记录的衔接。 |
| R2 | 形成消费方可执行的协议说明，确认参与方及基本记录边界。 |
| R3 | 双方共同联调需求—响应对接流程，修正协议并形成有界结项证据。 |

## 工作区绑定

| workspace_id | root_goal | role | joined | notes |
|--------------|-----------|------|--------|-------|
| `workspace-002-consumer-response-protocol` | `GOAL-001-consumer-response-protocol` | `primary` | 2026-09-25 | VP-002 的唯一实现工作区；Root 已于 2026-09-26 `done`。本次关门保留历史绑定，不归档工作区。本行 `role` 记录关门时的绑定事实；该区 `vision_role` 自 2026-09-26 起改记为 `delivery`（`VR-006`），vision 层唯一 `primary` 移交 `workspace-003-world-model-method-and-tools`。 |

## 关门核对（2026-09-26）

本次 `/vision` self closeout 核对结果为 `pass`。6 项方向级退出判据均有可追踪的实现层证据。本核对只证明一条真实流程链上的协议交接，不证明领域方法有效，也不把 Charter 方向级成功边界写成已经满足。

| 退出判据 | 结论 | 工作区 / Root 证据 |
|---------|------|-------------------|
| 1. 消费方协议明确发起入口、最低信息、角色与授权，且不要求先证明方法缺口 | 满足 | [`protocols/consumer-response-protocol.md`](../../../protocols/consumer-response-protocol.md) v1.0.0；Root 成功标准 1；[D-010](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/01-decision/D-010-protocol-guide-promotion-path.md)、[E-029](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/02-execution/E-029-protocol-guide-promotion.md)；R2 [A-011](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/03-audit/A-011-r2-stage-closure.md) |
| 2. 回执、澄清、受理/不受理、边界与限额、状态、范围变化和退出，且与 VP-001 授权语义一致 | 满足 | 协议步骤与 [D-002](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/01-decision/D-002-runtime-record-boundary.md)；I-004 `verified`（A-004 / A-005）；[A-021](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/03-audit/A-021-root-closeout-review.md) 成功标准 3 |
| 3. 区分交付、收件回执、响应验收与异议，并明确后续责任 | 满足 | [E-028](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/02-execution/E-028-r3-chain-closure.md)：第 1 轮两条范围内异议，v1.1 修正后第 2 轮接受；A-021 成功标准 4、6 |
| 4. 反馈分类、运行记录引用与重入明确；单一主记录，事件不是第二状态源 | 满足 | E-028 / EV-009（对象问题 2、运行机制问题 1、方法问题 0）；主记录转「已退出」；A-021 成功标准 5 |
| 5. 至少一个真实下游需求方沿共享追踪完成真实对接链条 | 满足本次有界范围 | [E-027](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/02-execution/E-027-first-exchange-delivery.md)、E-028、[A-020](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/03-audit/A-020-r3-stage-closure.md)；下游 `exchange/WRK-001/`。同人双角色与授权代行已标明，不声称独立团队共识，也不交付领域方法 |
| 6. 试跑证据可复核；歧义已修正或列为不遮蔽完成范围的有界 residual | 满足 | A-020：命名冲突、引用坐标与回执环节、状态滞后均已在范围内闭合；无开放 required finding |

相关愿景门禁同时满足：唯一 active Charter 为 `method-engineering@0.1.0`；`vision_ref` 精确匹配；单一 lead 工作区 `workspace-002-consumer-response-protocol` 的 Root 已 `done`；VRev-003～VRev-005 均为 `pass`，开放 Vision Review required 为 0；无 strategic re-align 债务。用户本轮明确指令即本次关门确认。

## 关门记录

（仅 `closed` / `abandoned` 时填写。）

| date | outcome | summary | evidence_links | residuals |
|------|---------|---------|----------------|-----------|
| 2026-09-26 | closed | 6 项方向级退出判据均满足本次有界协议交接；Root `GOAL-001-consumer-response-protocol` 已 `done`。不证明领域方法或 Charter 方向级成功。 | Root [`00-meta.md`](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/00-meta.md)、[A-021](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/03-audit/A-021-root-closeout-review.md)、[A-022](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/03-audit/A-022-root-closeout-response.md)、[E-028](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/02-execution/E-028-r3-chain-closure.md)、[E-029](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/02-execution/E-029-protocol-guide-promotion.md)、[`protocols/consumer-response-protocol.md`](../../../protocols/consumer-response-protocol.md)、workspace [`goal-tree.md`](../../workspaces/workspace-002-consumer-response-protocol/goal-tree.md) | 无遮蔽本 VP 声称范围的 VP 级 residual。同人双角色与授权代行只证明 [`workspace-002-consumer-response-protocol`](../../workspaces/workspace-002-consumer-response-protocol/workspace.md) / `GOAL-001-consumer-response-protocol` 上的本次流程执行，不构成独立团队共识。领域方法未构建属于 Non-goal。工作区保持 `active`；关门时其 vision 层角色为 `primary`，该角色自 2026-09-26 起改记为 `delivery`（`VR-006`），本次不归档。 |

## 规划修订短史

| date | change |
|--------|--------|
| 2026-09-25 | 根据用户确认，新增消费方与方法工程之间的双向交互协议；关门要求至少一个真实消费仓完成一条真实需求的端到端试跑。 |
| 2026-09-25 | 响应 VRev-003 V-F-001 / V-F-002：区分下游需求方与治理包消费安装；明确 VP-001 的接受需求 / IDLE 权威、同一主记录与事件追踪，以及 `runtime-records` 名称在本 VP 中的语义范围。 |
| 2026-09-25 | 按用户指令将 VP-002 由 `planned` 激活为 `active`。激活瞬间区绑定数为 0，按 alignment §5.1 告警；同一轮内由用户确认的 `primary` 工作区挂接消除空转，不申请空转宽限，也不把该 VP 当作已有交付证据。 |
| 2026-09-25 | 按用户确认开设并绑定 `workspace-002-consumer-response-protocol`（`primary`）与 Root `GOAL-001-consumer-response-protocol`；`lead_workspace` 随绑定写入。 |
| 2026-09-26 | 按用户要求将退出范围修订为双边协议联调演练，解除真实领域方法构建依赖；双方须沿共享追踪实际消费交接，合成材料不得冒充真实需求或建立虚假运行记录。实现层裁决见 [D-007](../../workspaces/workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/01-decision/D-007-protocol-rehearsal-realignment.md)。 |
| 2026-09-26 | 用户进一步明确把既有请求修订为跑通真实对接链条；取代合成演练安排，保留请求历史，仅接受有界流程工作。领域方法构建仍非退出前提；实现依据见 D-008。 |
| 2026-09-26 | 按用户指令完成有界关门：6 项退出判据均有工作区证据，`status` 改为 `closed`；不归档工作区，不创建后继 VP，不改 Charter 目的、边界或非目标。 |
| 2026-09-26 | 投影修正（`v0.4.0`→`v0.4.1`，editorial）：按 `VR-006` 修正工作区绑定行与关门 residual 的措辞——`workspace-002` 的 `vision_role` 已改记为 `delivery`，vision 层唯一 `primary` 移交 `workspace-003-world-model-method-and-tools`（承担新受理的 `WRK-002-world-model-method-and-tools`）。`status`、意图、判据与关门结论均不变。 |
