---
title: 独立审计 v0.18.5 与 run-18 当前层结构发现行为
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: A-028
doc: audit-entry
source: independent
verdict: fail
---

# A-028 · 独立审计 v0.18.5 与 run-18 当前层结构发现行为（2026-09-29）

## 审阅元数据

- **source**：independent
- **auditor**：fresh-context Reviewer subagent（gpt-6-sol，medium；`fork_turns:none`，read-only）
- **类型 / scope**：execution-facts；对冻结 v0.18.5 S1 方法语义与 run-18 最终可见 runner 输出做窄 scope 对照，重点审查 P2 是否为足够明确的 B3 求解项、F.2 分支口径、handoff-ready、第二轮 Rule G 与 residual。
- **审阅材料**：v0.18.5 源文、其 S1 execution projection、raw Probe 卡「世界有多大？」、run-18 runner 输出。Reviewer 未收到既有 run/audit、前序解释或预期答案结构。
- **Reviewer verdict**：`REJECT — execution regression`
- **Findings**：1 项 MAJOR；本意见将其登记为 required，因为 run-18 的 S1 结构充分性声明不能据现有材料作为通过证据。
- **本台账 verdict**：fail（限于所审运行行为与 handoff-ready 声明；不等于方法正文 defect，也不表示目标世界事实已知）

## 范围与区间

只审查本轮 runner 对原问的当前层结构生成、B3 转写、coverage attack、residual 与最终候选呈示。Runner 完成输出并停在 S1 creator-confirmation；创作者未答确认问题，按创作者指令未作 relay。没有实际 S1→S2 handoff、S2 求解或目标世界事实核验。

## 成果（有证据）

- Runner 保留抽象对象 W，并提出空间域、答案表达与客观求解三项内容；记录两项 B3、答案形态、无创作者侧精度要求及 residual。
- Runner 对第一轮 coverage attack 报告一组空间差异，并由此加入“依据空间结构选择足以表达尺度的描述”作为 P2。
- Runner 最后请求创作者确认“目标世界整体的空间尺度”口径及三项相互依赖的候选结构；这一确认未发生，故结构仍是候选。
- 上述事实由 [run-18 runner 输出](../attachments/s1-historical-anchor-integrated-trial-run-18-runner-output-v0.1.0.md)支持；该文件保存本次可见的 runner final message。

## 对照方法正文

1. **S1 的初始结构生成责任。** Execution projection §“从原问主动生成结构”要求推导“为基本回答 Q，还必须回答什么？”，要求提出必要问题及关系、说明各答案如何支持 Q，并明示对 Q 的释义、变量命名或未定项登记本身不等同于必要问题结构（[方法投影第 20 行](../attachments/stage1-framing-method-v0.18.5-execution-projection-v0.1.0.md#L20)）。Rule B 允许保留抽象对象继续分析（第 22 行），并不取消该结构生成责任。

2. **B3 与 F.2 的最低边界。** F.1 把 B2 定义为“阶段一对问题本身的理解或结构”，并要求继续分析到能明确阶段二要回答什么；B3 的前提则是“问题已经明确”（第 150–151 行）。F.2 要求所求是可检验表述、记录答案形态，并记录有依据可知的后续模型分支（第 165–168 行）。其中“若答案空间本身需要阶段二才能发现，就标记‘分支待阶段二发现’”紧接着“不同答案会如何路由后续模型分支”，本 Reviewer 将其解作允许把**分支影响**留给 S2，而非明确允许把原问的语义答案组成留给 S2。若后者被允许，将与 S1 明文的主动结构发现责任不相容。

3. **handoff-ready 与粗粒度节点。** 方法允许节点不是原子问题，但 handoff-ready 仍须让阶段二明确“要回答什么、求解任务／建模职责、答案类型、未决项 owner 与阶段状态”（第 291 行）。本轮 P2 的“依据目标空间结构选择足以表达尺度的描述”没有界定何种回答内容构成对原问的回答；“足以表达”把 answer composition 的确定留到求解期。Runner 给出的“尺度值／范围／无有限值”描述了部分答案形态，却未消除 P2 对问题所求内容的开放性。因此 Reviewer 认为 P2 不足以证明已 handoff-ready，而是一个由充分性标准定义的 catch-all 求解项。

4. **Rule G coverage attack。** G.1.1 要求在保持当前问题集全部答案不变的条件下，最大化两个世界在原问整体判断上的差异；G.1.2 第 1 项要求写出构造的两个世界及其整体判断差异，第 6 项要求逐轮留痕；G.1.3 明确把“问题集、依赖关系或答案形态”的改变列作必要结构增量（第 201、213、218、224–225 行）。本轮第二轮以“若空间差异影响尺度，应已反映在 P2”作为排除理由，预设了 P2 已能承载全部相关结构，因而用待检验的充分性声明关闭对该声明的攻击，构成 self-sealing coverage。该轮也未给出具体两个世界及其原问整体判断差异，不满足 G.1.2 的留痕要求。

5. **Residual 不能补足缺失的发现。** Runner 明确登记“可能仍有目标空间的特殊结构，使现有尺度表达不够用”，随后以“当前第二项承载按实际结构确定答案表达”作为暂不阻断理由（运行输出第 33 行）。这承认一种可能需要额外答案表达的未发现结构；P2 对其开放承载的承诺本身不能证明该结构不会改变必要问题结构，故不能据此把它判为非增量。

## Findings

### F-001 · P2 的开放承载与第二轮 Rule G 未证明当前层结构发现充分

- **status**：open
- **classification**：required
- **severity**：MAJOR
- **evidence**：运行输出第 24 行把 P2 写为阶段二“需依据目标空间结构确定”的适用尺度描述；第 31 行以“影响尺度的差异应已反映在 P2”排除差异；第 33 行仍保留“特殊结构使现有尺度表达不够用”的 residual，但称由 P2 承载；第 35 行据此声称覆盖轮后当前粒度足以呈示最终候选。与方法第 20、150–168、291、201、213、218、224–225 行对照。
- **审计意见**：这些运行结论不足以证明当前 S1 已发现“为基本回答原问还必须回答什么”的必要结构。P2 不是一个边界清楚、已能交由 S2 求解的 B3，而是以“足以表达”为判据、可吸收潜在 answer dependencies 的 adequacy-defined catch-all；第二轮 coverage 以 P2 的开放性作为排除条件，构成循环／自封闭论证。独立 Reviewer 将本轮行为归为 **execution regression**，不是 method ambiguity、method defect 或合法 S1→S2 边界。
- **要求闭合的范围**：在 run-18 可被接受为 S1 充分性通过证据之前，须按治理流程响应此 finding；此意见本身不指定固定拆分维度，不要求改方法文本。

## 必改项汇总

- 1 项 open required / MAJOR：F-001。按 P-003，只能经 `fixed`、`accepted-residual` 或 `user-overruled` 路径闭合，并由 `/govern` 留痕。当前未作任何闭合。

## 反证、限制与不能推出的结论

- 方法允许非原子粗粒度节点，且 handoff-ready 不要求问题集穷尽；这些条文不等于可以把尚未明确的回答组成整体留给一个未定边界的元问题。
- 现有材料没有证明目标世界实际上需要哪些额外尺度维度，也不能推出某个固定的空间描述清单。
- 该 verdict 只评价 run-18 声称结构已充分并可呈示的行为证据；创作者确认未发生，真实 S1→S2 handoff 与 S2 行为未被检验。不得据此改写 v0.18.5、run-17 trace 或历史结果。

## 结论 + 建议给编排器 / 用户的下一步

**Verdict：fail；分类：execution regression。** Runner 已形成候选并停在 creator-confirmation，但当前输出不足以支持该候选满足 S1 必要结构发现与 handoff-ready 门槛。由 creator 经 `/govern` 响应 F-001；本审计不改方法、不 relay 未裁定的最终确认、不推进 S2。

## 声明

本意见为独立 audit，不修改 GOAL status/progress、方法正文、creator 裁决或 run-18 authorization。该 finding 的响应与任何后续运行安排由 `/govern` 处理。

## `/govern` 响应与 F-001 闭合（2026-09-29）

本节是后续治理响应，不改动上方独立 Reviewer 的原始 `fail` verdict、F-001 发现、证据或审阅范围。创作者在 [D-070](../01-decision/D-070-a028-f001-fixed-run18-disposition.md) 接受 A-028，并对唯一 required / MAJOR F-001 选择 `fixed`。

- **闭合状态**：F-001 `fixed`。可核对修正是 run-18 的结果处置与证据状态：最终候选结构、coverage 充分性及 handoff-ready 声称均不再采纳为 pass／成功证据；[E-115](../02-execution/E-115-a028-f001-fixed-run18-disposition-recorded.md) 已记录该处置。
- **历史证据**：[runner 原始输出](../attachments/s1-historical-anchor-integrated-trial-run-18-runner-output-v0.1.0.md) 原样保留；原始 `fail` 仍是对 run-18 行为的历史结论。此 `fixed` 仅关闭 F-001 所要求的治理响应，不追溯修复运行行为或把 run-18 改判为 pass。
- **未获通过的门禁**：创作者确认未 relay，候选未获接受；没有实际 S1→S2 handoff 或 S2。v0.18.5 方法正文、交接合同和 binding 均未修订；未新增方法规则或推定固定拆分。可重复性仍待全新 run-19；run-17 保持 `interrupted / inconclusive` 且不恢复。
- **后续授权边界**：D-070 仅授权在同一精确 v0.18.5 基线、raw Probe「世界有多大？」及相同隔离条件下开展 run-19 范围。实际启动仍须先完成最终 binding 身份及 SHA-256 的独立 preflight，再取得创作者对该精确 hash 的单独授权；此处没有授予启动权限。
