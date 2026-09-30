---
title: QueryContract 与能力分类架构验证
status: active
created: 2026-09-30
updated: 2026-09-30
parent: GOAL-004-collaborative-question-framing
version: 0.1.4
id: GOAL-006-query-contract-architecture-spike
---

# GOAL-006 · QueryContract 与能力分类架构验证

## 概述

用独立、短周期的真实需求试验检验一个候选架构假设：模糊需求不必在求解前完成全局问题分解；系统可以先形成有版本、语义承诺明确到足以评估现有 capability 的 QueryContract，并在能力检查或一次执行反馈后，只重新打开受影响的定界决定。

Architect A 独立提出 QueryContract 与迭代控制环；Architect B 认为 operational context 有用但不应成为必经步骤。二者只作为本目标的候选比较依据。**本目标不接受任何产品分支为正式路线**；Role / Situation / Purpose 暂作为可选 grounding 机制，其是否能降低实质未决歧义由案例证据判断。

## 成功标准

- [ ] 第一阶段使用至少四项有来源的真实问题；它们可来自同一项真实用途，不要求额外项目、用户或 persona。四项原问与来源见 E-002，creator 已确认其实际用途情境为 VP-003 下游的“构建星际时代的修真世界观”需求，见 E-003。S1 逐例观察查询特征与能力结果；“现有 capability 不足”是评估结果，不是试验前准入条件。若没有观察到该结果，明确记为未观察/未决并限制相应结论，不补造案例。
- [ ] 每项需求都有版本化 QueryContract，明确当前查询承诺、答案形态、适用范围、重要假设及仍未解决且会影响 capability 判断的歧义；仅达到当前能力评估所需的语义清晰度，不要求穷尽拆解。
- [ ] 每项需求都有可追溯的 capability / gap classification，并区分 semantic ambiguity、world-state gap、mechanism gap、mapping/composition gap；creator 确认当前无可评估 baseline，不能自动推导为 capability insufficiency；无法与当前能力比较时记 `not observed` / `inconclusive`，不得强行归类或声称能力不足。
- [ ] 对 query commitment、creator elicitation 必要性、gap 区分、原始所求守恒、可选 Role / Situation / Purpose 的实际影响逐项留下案例证据；对有真实来源情境的模糊需求比较加入情境前后的 QueryContract 版本，若取不到真实情境则记为 `not observed`，不得自造 persona 补足。
- [ ] 仅当第一阶段达到其局部通过条件时，执行一次最小 execution-feedback cycle；准确记录 replan / refine / change-question 中实际发生的操作及其影响范围。未触发的操作记为未观察，不推断已验证。
- [ ] 向 creator 提交支持、反证或证据不足的结论及范围；无论结果如何，本目标都不自动接受方法规则、通用 schema、数据库或产品路线。

第一阶段的评价对象是 QueryContract 是否足以启动 capability assessment 及其代价、失效模式；**“是否完成完整问题分解”不是成功标准**。本目标的成功是产出可裁定证据，不要求候选假设得到支持。

## 有界路线图

| 阶段 | 名称 | 状态 | 退出条件 |
|------|------|------|----------|
| S1 | real need → QueryContract → capability / gap classification | run-001 已执行并经 A-002 独立审视；D-003 的 QueryContract 就绪阈值获局部支持 | 四题契约足以开始定位/检查可比能力；当前没有可评估 baseline 或材料，能力覆盖、质量、充分性及具体 gap 分类仍为 `not observed` / `inconclusive`。强制 grounding 重审触发条件未满足；没有可执行的既有 capability 路径，S2 入口条件未满足 |
| S2 | 一次最小 execution-feedback 试验 | 条件阶段；仅 S1 通过后进入 | 对一项已有可执行 capability 路径的需求执行一次反馈循环，记录被重新打开和保持不变的决定；不得据此推断未触发的操作 |
| S3 | 证据综合并提交 creator 裁定 | 未开始 | 提交本目标证据、局限与候选架构含义；正式产品路线仍由 creator 另行裁定 |

阶段关系为 S1 →（仅 S1 通过时）S2 → S3。若 S1 未通过或结论不充分，停止 S2，记录原因并提交 creator；不得为满足阶段计划而补造需求或执行反馈。

## 边界与非目标

- 不修改 v0.18.5，不续跑 run-19，不启动 run-20，不恢复旧 S1 线路。
- 不改写 W2，不改变既有 audit 身份，不重排 GOAL-003 的 W3 状态或 GOAL-002 的 W1～W4 计数。
- 不把 QueryContract 写成通用 ontology / schema，不建立 Graph IR、数据库或产品实现。
- 不把 Role → Situation → Purpose 设为强制入口；不将现实角色、习惯或价值观自动投射为虚构世界事实或 canon。
- QueryContract、分类词汇与本次阈值若有，仅是本 spike 的试验材料，不构成方法不变量。
- 当前无可评估 capability baseline 是已知试验限制，不等于证明所有 capability 均不足；不得从空缺/未登记状态推出世界模型能力结论。
- 推导、求解或试验完成不使任何结果自动成为世界 canon；creator 继续保留意图、边界和主动设定的决定权。

## 父目标与门禁

- 父目标：[GOAL-004-collaborative-question-framing](../GOAL-004-collaborative-question-framing/00-meta.md)。
- 本目标可为 GOAL-004 的 I-401 / I-402 提供局部证据，但不会自动关闭它们，也不构成 GOAL-004 的整体方法验证或交接。
- I-001 已由 D-002 / E-003 核实；I-002 已按 D-003 核实为“当前无可评估 baseline”，I-003 的本次判读阈值也已确认。Creator 后续仅授权按冻结包执行 S1 run-001；执行及独立审视见 E-006 / A-002。其局部结果支持四题 QueryContract 足以启动基线评估，但无可比较证据，能力充分性与具体 gap 主张仍为 `not observed` / `inconclusive`。S2 还须有可执行的既有 capability 路径；该条件未获证据支持，且 creator 未授权 S2。
- 本目标不改变工作区的 VP-003 / Charter 对齐。
