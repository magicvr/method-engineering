---
title: run-16 research、回问与 semantic zoom 边界的架构审计
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: A-023
doc: audit-entry
source: independent
verdict: conditional
---

# A-023 · run-16 research、回问与 semantic zoom 边界的架构审计

## 审阅元数据

- **source**：independent
- **auditor**：Codex Architect subagent（gpt-6-astra，medium；fresh-context，read-only）
- **scope**：只审查：(1) v0.18.3 是否要求外部知识可能改变 S1 framing 时先做 research discriminability 判断；(2) 按需研究是否允许无论证跳过；(3) semantic zoom 创作者三态与 Rule C“回问末位手段”的关系；(4) 创作者确认前的必要 AI 自主检验；(5) run-16“整体空间尺度”节点及立即确认请求应归为 execution regression 还是 method ambiguity。不审方法修订、不审 run-16 整体产品质量、不作创作者确认或 handoff 判断。
- **inputs**：冻结 S1 v0.18.3；[E-106](../02-execution/E-106-run16-paused-for-architecture-audit.md)；[run-16 paused partial runner trace](../attachments/run-16-paused-partial-runner-trace-v0.1.0.md)；[run-16 control-side pause message addendum](../attachments/run-16-control-side-pause-message-addendum-v0.1.0.md)。Architect 未以 A-020/A-022 作为本次结论依据。
- **本台账 verdict**：`conditional`（编排侧将 Architect 的“仍有 method ambiguity”映射为本项目三值 verdict；Architect 未直接给出 `pass/conditional/fail` 标签）
- **required findings**：0 项被审计者明确列为 required；本意见不把歧义自行升级为修订门禁。

## 独立核查

### 1. 外部知识可能改变 S1 framing 时的可判别性

v0.18.3 Rule B 的 N3 要求“可判别性检查＋按需资料/既有知识检索”，并要求留下能够区分或排除的结论与依据，或说明剩余项为何不可判别（第 132 行）；路由还须记录理由（第 136 行）。因此，**一旦 AI 已识别出影响当前 framing 的事实/知识缺口，不得不经分析就略过该项**。

但外部研究调用是按需动作，不是每个 raw question 或每个 N3 都必须独立搜索（第 142–144 行）。不能从“外部知识也许有帮助”直接推出必搜；也不能仅因原问没有给出 research prompt，就免除 AI 识别与分析当前缺口的责任。

### 2. “按需研究”与跳过理由

方法不允许对已识别未定项任意跳过性质判断与路由；但它也**没有建立一个每轮必做、必须单列“证明不需要 research”的固定仪式**。区分纯推理问题、creator-owned choice、影响 S1 定界的知识缺口与 B3 客观待答，需要按当前节点具体判断。

run-16 的“不调用研究”理由存在于控制侧保存的 runner 状态消息，而非 partial trace 正文。该理由指出尚无具体外部资料问题、当前困难可先作结构分析；它不是完全无理由，但不足以单独证明外部知识不能改变“大小判据/适用条件”的定界。仅凭该不足，不能断言本轮必然应调用 research。

### 3. Semantic zoom 三态与 Rule C

三态本身不构成 Rule C 的豁免：若实际请求创作者确定所求、定义对象/参数，或裁定会改变必要结构的 creator-owned choice，仍须满足 Rule C。另一方面，节点成立/粒度选择不必然等同于 clarification；方法允许创作者保持尚未 handoff-ready 的粗节点。

文本的时序接口尚未完全操作化：Rule C 管理 creator clarification，并要求先判断能否继续分解（第 182–194 行）；出口检查覆盖每项待确认事项并要求套用 Rule C 继续分解判断（第 422–425 行）；semantic zoom 又规定“继续展开”需要创作者授权（第 352–368 行）。文本未明确说明，何种粒度确认只是分析中的局部授权，何种确认已成为必须先满足 Rule C 的回问；也未明确局部三态确认前的最低分析呈示条件是否与最终收束相同。

### 4. 创作者确认前的必要自主检验

AI 必须先完成当前范围内适用的必要分析：从原问生成问题结构（第 79–83 行）、识别节点是否仍可能是问题族，并生成、比较、攻击候选子结构（第 352 行）；若识别到适用的知识缺口，还需按 Rule B/N3 做可判别性分析（第 132 行）。semantic zoom 呈示还要求列出节点成立依据、问题族判断、handoff-ready 四要素、被攻击的候选子结构及准入/排除理由（第 451 行）。

这不等于无限拆解、穷尽外部知识或先求解 B3。歧义在于：方法允许对尚未 handoff-ready 的粗节点发起局部粒度确认，但没有清楚划定这种**中途确认**与最终候选结构**收束确认**各自必须完成哪些自主分析与门禁。

### 5. run-16 当前节点与确认请求的归类

**结论：仍存在 method ambiguity，不能明确归为纯 execution regression，也不能确认执行充分。**

run-16 与 run-15 不同：它生成了 P1–P3、关系，并报告 Rule E/F/G 相关分析；没有仅因 W 未实例化就停止结构生成。但 partial trace 对“整体空间尺度”仍可能是问题族的依据展开不足，未按 semantic zoom 呈示要求逐项报告 handoff-ready 四要素；覆盖攻击记录也不足以核实 Rule G 完整收束。另一方面，若这次请求被解释为对粗节点的局部三态粒度裁决，方法允许保留粗节点并询问粒度，但该确认与 Rule C 的边界并未明确。

因此，若将其解释为最终候选收束，当前可见证据不足；若解释为中途粒度裁决，文本允许但其与 Rule C 的关系仍不清楚。未收到创作者三态答复；控制侧未转发该问题。run-16 仍为 `paused-at-creator-confirmation`，不得据此记为 creator-confirmed、完成、通过/失败或 handoff-ready。

## Findings 与处理边界

- 本次 Architect 意见给出“仍有 method ambiguity”的总体结论，但未指定 finding 级别或要求修订。本条忠实记录该结论，不把它提升为 required finding，不提出方法补丁，也不判 v0.18.3 冻结失效。
- 此条件性结论意味着：现有方法不足以让审阅者仅凭文本与当前 trace 唯一归责该确认请求；它不意味着当前 runner 已被证明违反规则，也不意味着必须调用 research。
- 本审计不改变 v0.18.3 文件/hash、试跑冻结身份、run-16 trace、creator confirmation 状态或 S1→S2 边界。

## 结论

研究可判别性对已识别 N3 有实质要求，但 research 调用不是固定步骤；无须每轮提交“证明不研究”的表单，仍须给当前路由以可核对理由。AI 在 creator confirmation 前须完成当前范围内必要分析，但方法没有清楚区分中途 semantic zoom 粒度授权与最终收束确认。故“整体空间尺度”节点及其即时确认请求目前应归为**method ambiguity**，而非已证实的 execution regression。

run-16 继续暂停。未转发 creator 三态问题，未修改方法正文，未进行实际 S1→S2 handoff 或 S2。
