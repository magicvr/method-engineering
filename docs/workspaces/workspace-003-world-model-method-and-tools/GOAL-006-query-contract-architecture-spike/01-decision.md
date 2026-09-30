---
title: 决策记录 · GOAL-006
status: active
created: 2026-09-30
updated: 2026-09-30
parent: GOAL-004-collaborative-question-framing
version: 0.1.2
id: GOAL-006-query-contract-architecture-spike
doc: decision
---

# 决策记录 · GOAL-006

## 信息需求与阶段门禁

| ID | 级别 | 所需信息 / 假设 | 影响门禁 | 最晚需要阶段 | 验证 / 收集动作 | 状态 | 延期 / 复核 | 证据 / 决策 |
|----|------|-----------------|----------|--------------|-----------------|------|-------------|-------------|
| I-001 | required | 至少四项真实世界模型问题的原始表述与来源，以及其真实用途情境；可来自同一真实需求，不要求独立项目、用户或 persona；不要求试验前预判 capability insufficiency | S1 试验准备 | S1 开始试验前 | Creator 提供或确认真实问题和用途情境；QueryContract 特征及 capability / gap 分类在 S1 中观察；如使用其他工作区材料，先按 workspace protocol 固定合规引用 | verified | 已由 D-002 / E-003 核实；S1 逐例分析类别与能力结果 | 四项问题原文、来源见 E-002；creator 确认其真实用途为 VP-003 下游需求，见 E-003；不要求另找案例或预先证明能力不足 |
| I-002 | required | 对每项需求可供检查的现有 capability、数据/状态输入及机制组合基线；若无可评估基线，须明确记录此状态且不得推断能力不足 | S1 capability / gap classification；S2 执行可行性 | S1 capability assessment 前；S2 执行前再次核对 | 由 creator 提供可核对的当前模型/能力描述，或确认当前无可评估基线；不得假定能读取未固定的跨工作区材料 | verified | 已核实当前无可评估基线；不代表能力不足已成立 | Creator 于本轮确认尚无 baseline；S1 中如无法比较，能力结论记为 not observed / inconclusive，见 D-003 / E-004 |
| I-003 | required | 预先操作化“实质模糊”“不必要 creator elicitation”“稳定/显著解除”及升级触发的判定方式；定义 S1 的 pass / refute / inconclusive 标准和 S2 入口门 | S1 试验判读、是否进入 S2、是否重新审视强制 Role / Situation / Purpose grounding | S1 试验前 | 提出本次局部观察判据并由 creator 确认；不把判据写成通用方法规则 | verified | 已由 creator 书面确认，仅适用于本 spike | D-003 记录实质歧义、elicitation、S1 结果、未观察能力不足及 S2 / grounding escalation 判据 |

I-001～I-003 已完成信息核实；当前无可评估的 capability baseline，不得据此自动判定 capability insufficiency。试验包及执行授权仍须另行准备与留痕。没有来源或授权的材料不得作为真实需求、capability 事实或试验结论。

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-09-30 | 建立候选 QueryContract 架构验证范围 | accepted | `01-decision/D-001-bounded-query-contract-spike.md` |
| D-002 | 2026-09-30 | 修正真实用途情境与案例准入门槛 | accepted | `01-decision/D-002-correct-case-entry-gate.md` |
| D-003 | 2026-09-30 | 确认能力基线现状与本次试验判读阈值 | accepted | `01-decision/D-003-baseline-and-trial-thresholds.md` |

> 之后的新决策从 `D-004` 顺延；本目标编号不与其他目标共用。
