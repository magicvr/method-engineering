---
title: 建立候选 QueryContract 架构验证范围
status: recorded
created: 2026-09-30
updated: 2026-09-30
parent: GOAL-004-collaborative-question-framing
version: 0.1.2
id: GOAL-006-query-contract-architecture-spike
record_id: D-001
doc: decision-entry
---

# D-001 · 建立候选 QueryContract 架构验证范围

> **门槛后续修订**：案例准入、I-001 状态与能力不足类别的处理以 [D-002](D-002-correct-case-entry-gate.md) 为准；D-001 其余候选假设、观察范围、S2 条件和非目标继续有效。D-001 的「先关闭 I-001～I-003」已更新为 I-001 verified、S1 前关闭 I-002～I-003。

- **日期 / 状态**：2026-09-30；accepted（creator 明确授权，并选择由 GOAL-004 下独立子目标承载）。
- **决定**：建立本短周期架构 spike，检验“有界、版本化 QueryContract 足以进入 capability assessment，并允许能力检查/执行反馈触发局部重新定界”这一候选假设。先以真实需求执行 S1；只有 S1 通过才执行一次最小 S2 feedback loop。Role / Situation / Purpose 仅作为 optional grounding 变量观察其增量效果。
- **依据**：Architect A clean-room 独立提出 QueryContract 与迭代控制环；Architect B reconciliation 认为角色情境信息有帮助但不应成为必经入口。Creator 接受二者作为候选比较结论，但明确不接受产品分支为正式路线。试验比直接改方法或单凭旧 S1 证据选路线，更贴合当前决策状态。
- **未选方案**：继续在 GOAL-004 既有 S1/run 线内混合记录，会把新假设验证与历史执行证据混在一起；回迁 GOAL-003 会偏离其 W3 两个最小结构与 I-301 对 GOAL-004 证据的既有依赖。两者均未采用。
- **试验范围**：S1 至少四项真实需求，各至少覆盖明确直接查询、实质模糊查询、已有明确使用情境查询、现有 capability 不足查询；**该类别覆盖条件已由 D-002 修订**：四项可来自同一真实用途，能力不足改为评估结果，未观察到时限制结论。逐例记录原始所求、QueryContract 版本和当前 query commitment、答案形态/范围/假设、会影响 capability 判断的未决歧义、capability / gap 分类及变更。该记录格式只服务本次试验，不建立通用 schema。
- **观察问题**：query commitment 是否明确；是否发生无必要 creator elicitation；能否区分 semantic ambiguity、world-state gap、mechanism gap、mapping/composition gap；是否守住原始所求；optional Role / Situation / Purpose 是否实际减少会影响答案或 capability 判断的未决歧义。若存在真实来源情境，对模糊需求记录加入情境前后的 QueryContract 版本差异；取不到真实情境时记 `not observed`，不得合成 persona 代替。
- **判读与升级触发**：在开始试验前，按 I-003 冻结 S1 的 pass / refute / inconclusive 判读及 S2 入口条件，并将 creator 给出的“多个真实模糊需求反复出现字面解释枚举或要求 creator 代替建模，而可选 Role / Situation / Purpose 能显著且稳定解除”的条件转成可逐例核对标准。若证据满足，提交 creator 重新审视强制 Role→Situation→Purpose grounding；不得由本目标自动升格为路线或规则。
- **范围控制**：S1 不以完整问题分解为成功标准。S2 只有 S1 通过后做一次；只评价实际发生的 replan / refine / change-question 对受影响决定的局部重开，未触发的操作记 `not observed`。不得用模拟结果替代真实 capability/execution 证据；无可执行 capability 时停止并报告。
- **影响**：GOAL-004 继续 `active`，progress 与 I-401/I-402 不变；旧 v0.18.5/run-19/run-20 路线暂停。GOAL-002 的 W1～W4、GOAL-003 的 W3、方法文件、handoff contract、历史 audit 与 canon 均不改。
- **后续**：先关闭 I-001～I-003，再冻结本次案例材料与判读记录；完成 S1 后按其结果决定是否进入一次 S2；向 creator 提交证据供其另行裁定产品路线。
