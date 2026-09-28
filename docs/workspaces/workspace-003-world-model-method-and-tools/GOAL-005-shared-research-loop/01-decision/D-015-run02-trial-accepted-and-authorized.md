---
title: 接受 run-02 设计并授权一次 S1 research-loop 调用
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-005-shared-research-loop
record_id: D-015
doc: decision-entry
---

# D-015 · 接受 run-02 设计并授权一次 S1 research-loop 调用

## 创作者裁决

创作者书面授权“开始试跑”，据此接受 [后续试跑设计 v0.2](../attachments/s1-independent-call-trial-design-v0.2.md) 的职责边界、接口语义、合成案例、来源策略、执行隔离、预算和评估标准，并授权**仅执行一次** run-02 S1 research-loop 调用。

本次接受的执行修订为：

| 角色 | 修订 | 本次范围 |
|---|---|---|
| S1 host | GOAL-004 v0.16.3 | 仅作为本次 run-02 host；不取代已接受的通用试跑基线 v0.16.2，也不代表该方法已验证 |
| S1 adapter | v0.1.1 | 仅作为本次 run-02 adapter；不取代组件设计基线 v0.1.0 |
| Shared Research Core | v0.1.0 | 沿用已接受设计基线，保持文件不变 |
| Shared Research Record Schema | v0.1.0 | 沿用已接受设计基线，保持文件不变 |

S1 adapter v0.1.0 与 S2 adapter v0.1.0 继续保留为已接受的组件设计基线；二者文件均不修改。本次不调用 S2 adapter。

## 案例、预算与盲测边界

唯一案例是：

> 一个偏远小型社区有饮用水送达住户。一次服务中断期间，记录显示住户端情况不一致：部分住户仍能取水，部分住户不能。当地供水系统的具体结构、依赖与中断原因均未提供。请进行一次有界外部研究，识别可能导致同一服务中断期间住户端结果不同的一般机制候选，并说明哪些目标侧事实可用于区分或验证这些候选；资料只能支持一般机制候选及其适用边界，不能证明该社区的真实系统情况。

执行前须在隔离会话中根据案例和 S1 当前未知确定并记录唯一 research question、用途充分标准与查询计划。边界为：最多 5 个定向查询变体、最多查看 6 份来源、查看 3 份来源后复核是否继续，计划总量 45 分钟。逐主张记录出处、来源支持、评价、迁移依据及限制，并区分来源陈述、AI 推论与目标侧待验证事实。

执行会话不读取 run-01、A-001/A-002、旧查询/来源、旧候选结构或既有机制提示。若隔离条件不能满足，结果须降格标为“去提示试跑”并说明原因。AI 执行研究、生成/比较/攻击候选并给出 Rule E/F/G 回流建议；创作者仍保留对候选结构和结果的最终裁决权。

## 不在授权范围内

- 不授权第二次调用、S2 试跑、Probe 1、父层结构确认或开放式全局 coverage search。
- 不授权修改 Core、Schema、S1/S2 adapter v0.1.0，或 S1 host v0.16.2 与 run-01 记录。
- 单次样本不构成方法普遍有效、目标社区真实系统事实、问题覆盖穷尽或 handoff-ready 的证明。
- 试跑的候选准入、归属、coverage 与收束回流须留痕；创作者裁决待本次结果呈示后另行记录。

## 执行记录

固定身份与工作边界见 [run-02 binding](../attachments/s1-independent-call-trial-binding-run-02-v0.1.0.md)。本 D-015 授权不表示执行已完成；执行事实与原始研究记录见后续 E-019 及其附件。
