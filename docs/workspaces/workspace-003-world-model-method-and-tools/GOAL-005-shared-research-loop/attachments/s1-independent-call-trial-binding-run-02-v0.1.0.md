---
title: S1 research-loop run-02 身份与边界绑定
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-005-shared-research-loop
version: 0.1.0
acceptance: authorized-by-D-015
---

# S1 Research-Loop 独立调用身份与边界绑定 · run-02

> 本绑定固定 D-015 授权的一次 S1 research-loop 调用。它只标识本次试跑的执行栈、研究任务与停止边界；不含研究结果，不构成方法普遍验证。

## 1. 组件身份四元组

| 角色 | 精确文件／修订 | 本次状态 | SHA-256 |
|---|---|---|---|
| S1 host | [GOAL-004 v0.16.3](../../GOAL-004-collaborative-question-framing/attachments/stage1-framing-method-candidate-v0.16.3.md) | draft；由 D-015 接受为本次运行 host | `E55C50722A909293B0BA483F0F67D35CE027B8ECBF6518DE1C0190DD83D52D96` |
| S1 adapter | [v0.1.1](s1-research-adapter-v0.1.1.md) | draft；由 D-015 接受为本次运行 adapter | `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C` |
| Shared Research Core | [v0.1.0](shared-research-loop-core-v0.1.0.md) | 已接受设计基线；本次沿用 | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema | [v0.1.0](shared-research-record-schema-v0.1.0.md) | 已接受设计基线；本次沿用 | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |

固定设计与未使用组件：

| 文件 | 本次处理 | SHA-256 |
|---|---|---|
| [run-02 设计 v0.2](s1-independent-call-trial-design-v0.2.md) | 创作者按 D-015 接受；本次执行合同 | `C28D58ED5BBAA8DE2BFB1F43E0D4925D1D233E80EA6416455E7F5DDD52EF8F5E` |
| S1 adapter v0.1.0 | 已接受的组件基线；本轮不调用、不修改 | `4A0D683AD6EBD3F4ED22D1E69F0BD2A0F8E71A3090E22F2528318939BE9F0F4E` |
| S2 adapter v0.1.0 | 已接受的组件基线；本轮不调用、不修改 | `9885685990E54C47D6EE81908A5595BC94DE5CCB1EF0342165ACD24CEAD74C69` |
| S1 host v0.16.2 | 已接受的通用 S1 试跑 host 基线；本轮不调用、不修改 | `CBE94EC732E29050D0A3545C415D8D8674EDF1899142C3A62C218861119664AE` |

运行前须再次核对四元组和设计文件哈希；任一不符则停止，不得静默换版。v0.16.3 / v0.1.1 的接受只适用于本次调用，既有 v0.16.2 / v0.1.0 身份不变。

## 2. 唯一问题、未知、owner 与用途标准

- **研究对象**：合成案例中的偏远小型社区与住户端饮用水供给。
- **调用时已知**：发生一次服务中断；记录显示部分住户仍能取水、部分住户不能。
- **调用时未知**：当地供水系统结构、依赖与中断原因；不得补造为案例事实。
- **唯一 research question**：在一次服务中断期间，哪些一般系统机制可能解释同一小型社区内住户仍可或不可取水的差异？各候选机制需要哪些可观察的供水系统事实来区分或验证？
- **研究用途**：发现有来源支持、但明确受适用边界约束的一般机制候选，并指出区分/验证每项候选所需的目标侧事实；不判断合成社区真实配置。
- **owner / 权限**：AI 负责本次研究、机制候选生成/比较/攻击、证据评价与 S1 E/F/G 回流建议；目标侧条件真值仍未知。创作者保留问题结构及方法回流的最终裁决权。
- **用途充分标准**：来源和定位可复查；可区分来源直接主张与 AI 推论；每个拟回流机制带有来源对象、目标对象差异、迁移理由和限制；给出可区分/验证它的目标侧事实；结局不把未找到写成不存在；按现有 Rule E/F/G 回交而不自动准入。

## 3. 来源策略和有界工作量

- 仅由隔离执行者从唯一研究问题导出查询；本绑定不预设机制名称、taxonomy、检索词、来源标题或预期结果。
- 优先选择与主张直接相关、可复核的权威技术资料、原始研究或同行评审研究；二手来源只可按其实际用途用于线索/综述，并记录其转引链、质量和适用范围。
- 上限：一个 research question；最多 5 个定向查询变体；最多查看 6 份来源；查看第 3 份来源后明确记录继续/停止理由；计划总量 45 分钟。墙钟不可可靠计时则记录查询数、来源数、检查点和停止理由。
- 达用途标准且没有可能改变下一步的必要研究未知时收束；到上限仍不足则记录 `partial-or-insufficient`、`conflicting-evidence`、`not-found-or-inaccessible` 或适用结局并登记 residual。不得因没有找到预期候选而超限扩搜。

## 4. 隔离、回流及禁止范围

- 执行使用新建、无历史上下文的 SCOUT 会话。会话只接收本绑定的案例卡/问题、调用预算和本次所需方法组件；不得读取 run-01、A-001/A-002、旧查询/来源、旧候选结构或审计材料。
- 执行者回交 research record 与 S1 `host_disposition`：Rule E 候选结构贡献、输入否定/冗余/既有节点检查；Rule F 的未知 owner/状态；Rule G 的 coverage、收束、残余与范围影响。候选结构作为建议，创作者裁决另记。
- 一次调用到此停止。不授权第二次调用、S2 试跑、GOAL-004 Probe 1、父层确认或开放式全局 coverage search；不修改 Core、Schema、已接受的 v0.1.0 adapter 文件、v0.16.2 host、run-01 或其结论。

授权来源：[D-015](../01-decision/D-015-run02-trial-accepted-and-authorized.md)。本包表示授权且身份已固定；执行事实须记在 E-019 和独立运行附件中。
