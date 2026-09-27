---
title: 共享研究闭环版本化接入方案
status: draft
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-005-shared-research-loop
version: 0.2.0
acceptance: boundary-sequence-baseline-accepted
---

# 共享研究闭环版本化接入方案 · v0.2

> **状态：draft / boundary-sequence-baseline-accepted。** 创作者已接受本方案作为组件边界与后续顺序基线；它不等于接受每份拆分组件文档，不修改 S1/S2 方法正文，也不授权或报告试跑。S1/S2 宿主正式版本号待可用方法基线明确后再定。

## 1. 架构：一个共享语义 owner，两个窄 adapter

共享研究闭环是独立的语义组件，由唯一 shared core 持有研究过程定义。它不是 S1 或 S2 的子流程所有者，不拥有宿主阶段门禁、结构准入或模型结论的裁决权。S1/S2 adapter 只翻译“何时调用、宿主需要什么输入、研究输出回到哪条既有判断链”，不得重述或复制 core 规则。

```text
S1 宿主未知 ─► S1 adapter ──┐      ┌──► S1 adapter ─► Rule E/F/G
                            ├─► 唯一 Shared Research Core
S2 宿主未知 ─► S2 adapter ──┘      └──► S2 adapter ─► 模型构建与验证
                                     研究记录 / 证据包使用共享 schema
```

同一研究 core/schema 在两个 host 中保持同一语义；adapter 输出进入 host 后，由 host 的现有机制作裁决或验证。单独有来源或得到“足够当前用途”的研究结局，不会自动改变宿主结构/模型。

## 2. 组件职责与裁决权边界

### Shared core：唯一的研究语义 owner

Core 持有并维护以下共享研究语义：未知类型与 owner 区分、研究问题、来源策略与范围上限、逐主张证据评价、来源间独立性/冲突、源对象到目标对象的迁移理由与限制、综合、bounded stop 及剩余未知登记。具体字段与研究闭环规则继续以 core 候选为审阅对象；本接入方案不重写其规则。

Core 输出可复查的来源主张、AI 推论、迁移条件/边界、当前用途结论、反证/冲突、研究结局与剩余未知。Core **不**裁决候选是否进入 S1 问题结构，不裁决某机制/参数是否被 S2 模型采用，也不替创作者作取舍。

### S1 adapter：回到现有 Rule E/F/G

S1 adapter 只定义：何种 S1 未知需要调用研究；S1 的当前原问/待判断内容如何传给 core；哪些研究结果可以作为候选问题/解释、关系/依赖、反例或边界返回；返回记录如何指回当前原问与证据。

回流只进入现有机制：Rule E 处理候选准入，Rule F 处理未知归属与 owner/下一步，Rule G 处理 coverage、收束及残余回流。适用性或证据评价由 shared core 承担，不在 adapter 复制。Core 和 adapter 都不能代替 E/F/G 准入或覆盖裁决。

### S2 adapter：回到模型构建与验证

S2 adapter 只定义：模型构建/验证中何时有明确外部研究问题；如何将研究输出的机制、参数/范围、约束、已有模型或观测资料作为带出处和假设的依据交回；模型如何引用该研究记录。

研究依据回到 S2 既有模型构建与验证，检查目标对象适用性、模型一致性、参数/约束影响与所需观测或推导。Adapter 不复制 core 的来源质量、证据评价、迁移或停止语义；shared core 也不决定证据是否进入目标模型。

## 3. 组件身份与版本边界

按创作者在 [D-003](../01-decision/D-003-central-shared-boundary.md) 的裁决，shared component 集中放在 `GOAL-005-shared-research-loop/attachments/`；以下四份独立候选均从 `v0.1.0` 起：

| 候选文件 | 组件 | 初始候选修订 |
|---|---|---|
| `shared-research-loop-core-v0.1.0.md` | Shared Research Core | `v0.1.0` |
| `shared-research-record-schema-v0.1.0.md` | 共享研究记录 schema | `v0.1.0` |
| `s1-research-adapter-v0.1.0.md` | S1 adapter | `v0.1.0` |
| `s2-research-adapter-v0.1.0.md` | S2 adapter | `v0.1.0` |

此处的 `v0.1.0` 是待形成的候选修订标识，不代表语义已接受、冻结或适合试跑。候选核心 [v0.1](shared-research-loop-candidate-v0.1.md) 保留为来源版本；拆分后的四份文件须逐项说明对它的承接与差异。

宿主最小接入范围也已由 D-003 裁决为**每个宿主各自增加一个窄的调用/回流接口**，不复制共享研究闭环的评价、迁移或停止规则：

- **S1**：只补充何时调用 S1 adapter、传入当前 S1 未知的引用、以及怎样把带来源的研究结果交回既有 Rule E/F/G。不得改写或绕开 E/F/G 的候选准入、未知归属、coverage 与收束职责。S1 当前冻结试跑基线为 v0.16.1，v0.17.0 仍是 `draft / unaccepted`；宿主版本号与具体插入点待后续选择可用基线时确定。
- **S2**：在当前 W2 回流形成可用的新方法基线后，只补充何时调用 S2 adapter、传入模型构建/验证中的研究问题、以及怎样把机制/参数/约束/已有模型/观测依据交回 S2 既有模型构建与验证。不得改写其采纳判断，也不改 GOAL-003 的暂停中结构。W2 v0.4 为历史基线，S2 宿主新版本号待可用基线形成后确定。

接入时仍应能分别识别以下组件身份及其实际修订：

| 组件 | 独立语义职责 | 版本关系 |
|---|---|---|
| Shared Research Core | 研究问题至证据综合、停止与剩余未知 | `GOAL-005/attachments/shared-research-loop-core-v0.1.0.md`；单一共享语义版本，不得由 host 文件中的隐式副本替代 |
| 共享记录 schema | 研究任务、证据主张、迁移、综合与回流记录结构 | `GOAL-005/attachments/shared-research-record-schema-v0.1.0.md`；与实际 core/adapter/host revision 一并留痕，结构变更需显式兼容说明 |
| S1 adapter | S1 调用契约及 core 输出到 E/F/G 的接口 | `GOAL-005/attachments/s1-research-adapter-v0.1.0.md`；可独立演进，不得改变 core 语义或 Rule E/F/G |
| S2 adapter | S2 调用契约及 core 输出到模型构建/验证的接口 | `GOAL-005/attachments/s2-research-adapter-v0.1.0.md`；可独立演进，不得改变 core 语义或模型裁决规则 |
| S1/S2 host 方法 | 各自宿主的现有方法正文、规则和门禁 | 宿主的下一个方法修订标识待选定可用基线后决定；adapter/core 变更不能隐式回写 host |

本方案已指定 shared component 的候选落点与初始修订标识，但**没有替 S1/S2 宿主指定下一正式版本号**。不得从 core/schema/adapter 的 `v0.1.0` 自动推导 host 版本号；宿主须先选定可用基线，再按各自方法版本规则确定。

### 不可追溯修改规则

- 不得把 core 的定义复制到两个 adapter 后分别维护；core 语义调整应作为 shared core 的显式新修订，说明变化、理由、兼容影响与采用该修订的试跑记录。
- Adapter 契约调整应单独标出对应 host、接口变化及影响范围；不得以 adapter 文案改变 core 的来源评价、迁移、停止等语义。
- Host 方法正文、Rule E/F/G、S2 模型验证机制只有经该 host 的版本审阅/授权才修改；不能因接入 core 而静默修改。
- 每份研究/试跑记录须标识实际使用的 core、共享 schema、对应 adapter 与 host 方法修订。正式身份标识待裁决后确定；不得事后覆写旧记录来掩盖当时使用的语义。
- 两个 host 试跑之间若 core/schema 有变化，则不再视为“同一 core/schema”验证：先显式冻结共同基线；如 S1 已按旧基线完成，应决定是否重跑 S1，确保 S1/S2 比较具有共同依据。Adapter/host 单独变化时标明变更并重跑受影响的 host 试跑。

## 4. 后续接入与裁决顺序

1. **审阅并接受组件候选**：core 的研究语义已按 D-004 接受为设计基线，本方案的边界与顺序已按 D-005 接受为基线；四份组件候选的独立复核已通过，schema 与两个 adapter 已按 D-006 接受为组件设计基线。D-003 的文件边界决定本身不等于接受组件语义。
2. **形成可审阅组件候选**：已按 D-003 路径和 `v0.1.0` 候选修订标识形成 core/schema/两个 adapter 文件，记录其相对原 core 候选的承接与差异。后续只在审阅提出修订时更新相应候选；此步不改 S1/S2 host 方法。
3. **另行授权宿主方法集成**：在选择可用 S1/S2 host 基线后，按本节所列最小范围编辑各自方法版本。候选与计划不自动授权 host 方法修改；Rule E/F/G 与 S2 模型验证的既有裁决权保持不变。
4. **冻结共同试跑基线**：在两次试跑前固定同一 core/schema 修订，并记录两个 adapter 与 host 方法的各自修订身份；若基线变动，先裁定是否需重跑已完成试跑。
5. **分别设计并执行 S1、S2 两次独立调用试跑**：先设计/运行 S1，再单独设计/运行 S2；各自案例由后续另行裁决，本方案不预设两案例是否相同，也不指定具体案例或启动运行。
6. **分别审阅证据和 host 回流结果**：验证 core 对两个 host 的共同服务能力，同时确认每个结果由各自既有宿主规则裁决。两轮结果不得合并成一次演示，也不得用一侧试跑替代另一侧。

## 5. 两次未来试跑的设计合同

| 项目 | S1 独立调用试跑 | S2 独立调用试跑 |
|---|---|---|
| 顺序 | 第一轮 | 第二轮；在 S1 结果留痕并冻结共同 core/schema 后单独进行 |
| 验证目标 | 同一 core 能处理 S1 的有界研究任务；证据包能产出可追溯候选并回到 Rule E/F/G，而不替 E/F/G 作结构准入或 coverage 裁决 | 同一 core 能处理模型构建/验证中的研究任务；机制/参数/约束/模型/观测依据能回到模型验证，由 S2 宿主判断适用与采用 |
| 不验证什么 | 不证明 S1 覆盖穷尽，不证明创作者已接受案例结构，不验证目标世界事实 | 不证明来源模型普遍有效，不证明目标世界结论，不让 research core 决定模型取舍 |
| 最小证据接口 | core/schema/adapter/host 修订身份；调用触发与研究问题；证据 claim＋locator/评价/迁移；返回的候选及其与原问关系；E/F/G 对候选的准入、归属、coverage/收束处理；剩余未知与失败/限制 | core/schema/adapter/host 修订身份；模型任务与研究问题；机制/参数/约束/模型/观测主张及出处、评价、单位/范围/迁移条件；回到模型构建/验证后的采纳/拒绝/调整理由；剩余未知、验证缺口与失败/限制 |
| 共同性要求 | 与 S2 使用完全相同冻结的 core/schema 语义；不要求 adapter 或 host 方法文本相同 | 与 S1 使用完全相同冻结的 core/schema 语义；S2 adapter 与模型验证证据单独记录 |

两个试跑各用自己的研究任务、host 记录与结论。Core/schema 不因某次结果而在两轮间静默变化；如需修改，按第 3 节先变更并决定对先行轮的重跑需求。

## 6. 本方案暂不决定与不授权事项

- shared components 的落点及 `v0.1.0` 候选修订标识已按 D-003 决定；四份拆分组件候选已形成并通过独立复核，core/schema/两个 adapter 的设计基线均已接受（D-004、D-006）。三份新接受附件仍保留原有 draft frontmatter；最新接受状态以 D-006 为准。
- 不选择 S1/S2 host 的下一个正式版本号或具体文本插入点；不修改任何 host 方法正文。各 host 后续只增加本方案 §3 定义的一处窄调用/回流接口，不修改现有裁决规则。
- core/schema/adapter 组件设计基线与本 integration plan 的边界/顺序基线已分别按 D-004、D-006、D-005 接受；这不代表已集成或验证。
- 不选 S1/S2 试跑案例、不运行试跑，不把计划或模拟当作验证证据。
- 不修改 GOAL-004、Probe 1、presentation-03、b-refinement 或其案例结论；不启动 GOAL-004 父层确认、W2 求解或 W3 放行。

因此，本方案把创作者已选的 shared component 版本与物理边界写实，并建立“**接受组件基线 → 另行授权 host 方法集成 → 分别规划与执行 S1、S2 试跑 → 用同一 core/schema 检查各自宿主回流**”的顺序与证据接口。core/schema/adapters 与本方案边界/顺序基线已接受；S1 试跑设计参照 v0.16.1 已按 D-007 选定，集成 host 版本号仍待单独授权 host 集成后确定。组件接受、候选形成及后续状态见 D-004～D-007 与 E-006～E-008。
