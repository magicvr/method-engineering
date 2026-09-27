---
title: S1 research-loop 独立调用试跑身份与边界绑定包
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-005-shared-research-loop
version: 0.1.0
acceptance: execution-authorization-pending
---

# S1 Research-Loop 独立调用试跑身份与边界绑定包 · v0.1.0

> 本绑定包把已接受的 [试跑设计 v0.1](s1-independent-call-trial-design-v0.1.md) 固定到已接受为 S1 试跑 host 基线的 v0.16.2 及共同组件修订身份。**它不授权执行研究或试跑，也不包含任何研究结果。**实际调用须在创作者另行授权后开始。

本包更新接受设计 §2 与 §7.1 中“host 集成尚待确定”的状态投影：D-010/D-038 已接受 v0.16.2 为本轮 host；原设计的案例、研究问题、预算和验证合同不变，§7.3 所要求的实际调用授权仍未取得。

## 1. 修订身份

| 角色 | 固定文件／版本 | SHA-256 |
|---|---|---|
| S1 host | [GOAL-004 阶段一方法 v0.16.2](../../GOAL-004-collaborative-question-framing/attachments/stage1-framing-method-candidate-v0.16.2.md) | `CBE94EC732E29050D0A3545C415D8D8674EDF1899142C3A62C218861119664AE` |
| 派生及 run-10 参照 | [阶段一方法 v0.16.1](../../GOAL-004-collaborative-question-framing/attachments/stage1-framing-method-candidate-v0.16.1.md) | `E6C1EF612CEAFB64DDB8C26202D84007405723E19D9647025BF17C6BE5994C34` |
| Shared Research Core | [core v0.1.0](shared-research-loop-core-v0.1.0.md) | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema | [schema v0.1.0](shared-research-record-schema-v0.1.0.md) | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |
| S1 Research Adapter | [S1 adapter v0.1.0](s1-research-adapter-v0.1.0.md) | `4A0D683AD6EBD3F4ED22D1E69F0BD2A0F8E71A3090E22F2528318939BE9F0F4E` |
| 试跑设计 | [独立调用试跑设计 v0.1](s1-independent-call-trial-design-v0.1.md) | `A4D402C4E6B6CA49172D5000C010573A08B529D0A72F350922F5A1F25C96D7C2` |

host 候选在创作者接受前的复核对象 SHA-256 为 `A01B5CBDA182D170F03D62F7FED9D68F11B78E5950C9BC41E5BB7A6F7974FB14`；接受时只更新候选接受范围与状态说明，方法规则和接口正文未改。上表记录当前接受版精确身份。运行前如任一文件 hash 不匹配，先停止并重新核对；不得静默替换版本。

## 2. 唯一案例与研究问题

按 [D-008](../01-decision/D-008-s1-trial-design-accepted.md) 接受的合成案例：一个偏远小型聚落从本地水源取水，经处理后由依赖电力驱动的泵向住户供给饮用水；当前不知道停电时哪些系统条件会导致供水中断，哪些会维持供水。它不是 GOAL-004 Probe 1、不是用户创作 canon，也不计作 GOAL-002 W4／`I-402` 的真实案例证据。

唯一 research question：

> 对依赖电力泵送的小型饮用水系统，哪些有资料依据的系统条件会使外部电力中断导致或不导致终端供水中断？

除案例明确给出的条件外，不预设具体系统配置、故障缓解机制或固定子问题清单。资料出现的配置、taxonomy、风险类别先作为有出处的候选，交由 S1 Rule E/F/G 与创作者权责处理；不能把现实资料直接升级为合成聚落事实。

## 3. Owner、来源策略与工作边界

- AI 是本轮研究任务 owner；创作者保留候选是否进入问题结构的最终裁决权。
- 优先查可公开复查的公共机构／供水系统技术资料和同行评审工程研究，仅覆盖与泵送依赖、电力中断和供水连续性直接相关的材料。
- 预算：1 个 research question；最多 5 个定向查询变体；最多查看 6 份来源；查看前三份来源后作一次继续／停止回看；计划总量 45 分钟。墙钟不可可靠计时则记录查询数、来源数、检查点和停止理由。
- 达到预算不等于充分。证据不足、冲突、资料不可得、需要目标对象观测或属于创作者取舍时，使用 schema 对应结局并登记 owner／下一动作；不得把“本轮未找到”推成“不存在”。

## 4. 预定回流和输出

1. 按共享 schema 记录研究问题、来源定位、逐 claim 支持内容、质量判断、限制与适用性／迁移理由，区分来源陈述、AI 推论和目标对象待验证主张。
2. S1 adapter 将候选包回交 v0.16.2 当前局部分析位置；Rule E 判断候选结构准入，Rule F 处理未决归属，Rule G 处理 coverage、收束、残余和范围影响。研究结局本身不能替这些规则作裁决。
3. 局部研究不自动重开顶层 coverage；只有具体证据满足 S1 既有回流条件时，才处理范围扩大。
4. 产出一份完整研究记录和一份调用后 S1 Rule E/F/G 回流记录；由创作者另行判定本轮证据与候选处理。若问题分化为多个独立研究问题，只登记 residual 并停止，不自动开展第二次调用。

## 5. 未授权事项与执行门槛

- 当前只完成 host 与试跑设计身份绑定；没有执行查询、打开来源、形成研究 claim、调用 Core 或生成试跑结果。
- 共享 core、schema、S1 adapter、S2 adapter 与冻结的 v0.16.1 均不得在本次试跑中修改。
- S2 adapter／S2 host 不在本轮调用范围内。
- **执行门槛**：只有创作者对本绑定包的具体试跑任务另行授权后，才可开始一次调用；如输入边界或预算变化，须先修订绑定包并再次确认。
