---
title: A-014 · 独立审计 v0.18.0 的研究回流所求守恒
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
doc: audit-entry
record_id: A-014
source: independent
scope: v0.18.0 methodology adequacy against research-feedback scope inflation and parameterization escape, informed by run-13 visible trace
verdict: fail
---

# A-014 · 独立审计 v0.18.0 的研究回流所求守恒（2026-09-29）

- **source**：independent
- **auditor**：fresh-context read-only subagent（gpt-6-sol，xhigh；使用通用 agent 派发，未激活仓库 `REVIEWER` role adapter）
- **scope**：审查 v0.18.0 是否足以防止 research-feedback 后的 scope inflation / parameterization escape，聚焦操作化未知的 B1、真实自由参数、答案适用限定、参数化导致的求解任务扩大，以及 E/F/G 是否存在 demand-preservation 检查。未审方法修改、S2 或 handoff。
- **reviewer 原始 verdict**：`REJECT`
- **本台账 verdict**：fail
- **required findings**：1 项 MAJOR（F-001）

## Findings

### F-001 · 缺少研究回流后的所求守恒检查（required / MAJOR）

v0.18.0 已有部分防护：规则 E 要求当前输入锚点、必要结构改变与去重；F.1 区分创作者取舍、定界结构和客观求解；F.2 要求写明 B3 所求和答案形态；G.1.3 将“原问的所求”列为交接相关增量。它们没有要求把**研究前已确认的所求与答案形态**和每个研究回流候选作直接比较，判明回流条件究竟是原问要求求解的维度、必要的 S1 定界项，还是只用于操作化证据／限定答案适用范围的信息。

当前表述允许一条具体逃逸路径：研究来源指出某些条件会影响证据或最终结论；条件因有输入锚点且可被说成改变结构而通过 E；未定值又按 Rule B 变量化进入结构；随后写成一个 B3 条件族，要求阶段二刻画哪些条件组合成立。单纯“需要值”不能区分真正的自由参数与答案限定；F.2 也不检查新 B3 的量词范围或输出是否超过原问。

G.1.3 能检查新差异是否改变当前对原问所求的理解，但覆盖攻击在问题集被扩大后可以围绕这个扩大的结构执行；它没有另设“当前求解任务是否比原问更强/更大”的反向约束。比如“是否至少存在一种长期自我维持的生态系统”可被扩大为“对哪些 M/T/D/B 组合存在正例”的可行域刻画。后者的信息严格多于存在性判断，也能回答它，但并非原问自动要求的求解范围。

## run-13 行为证据

run-13 中，研究支持的 M/T/D/B 操作化口径一度进入 Q0，并被列为 B1；创作者澄清若它们只是自由条件变量，不要求创作者选值。Runner 随后将 B1 口径转成 B3 条件空间，提出描述证据支持哪些 `(M,T,D,B)` 组合。创作者再次纠正：用户确认的是一般存在性，不是整个条件空间；这些口径应说明答案采用的标准与结论适用边界。此后 runner 才把 Q0 收回为一般存在性，并将操作化条件放入答案限定。

可核对记录：[run-13 完整可见 trace](../attachments/run-13-full-visible-trace-2026-09-29.md) §3–§7，尤其 creator relays 与 runner revisions（约第 172–245 行）。该样本同时含有执行偏差与创作者纠正；它不单独证明执行者已遵守所有规则。审计判断方法缺口的依据是：现行 E/F/G 没有要求进行所求守恒与条件角色检查，而该区分需由创作者补充提示后才在本轮固定下来。

## 审计问题答复

1. **未定操作化何时是 B1：** 只有当前输入确实表明不同标准、阈值或边界对应创作者要求回答不同问题或采用不同创作边界，且分析不能收窄时，才是 B1。研究中存在多个口径，不自动构成创作者取舍。
2. **何时是真正自由参数：** 原问或已确认的创作者意图要求对该参数的多值、阈值、范围或条件关系给出函数／范围／条件空间等答案。参数值未指定本身不足以推出其为自由参数。
3. **何时是答案的适用条件：** 原问仍能以原有量词和答案形态作答，条件只说明证据采用何种操作化、结论适用于哪些对象／时间／边界以及口径变化如何限制外推。此时不默认要求全域遍历。
4. **参数化是否可能扩大任务：** 是。把存在性问句改成条件组合的全域可行性刻画，会要求严格更多信息，不能仅因后者包含前者答案就视作 scope-preserving。
5. **E/F/G 是否已有显式 demand-preservation 检查：** 没有。E 的必要结构改变、F.2 的所求字段和 G.1.3 的所求增量检查提供部分依据，但没有要求以研究前需求为基准做差分，也没有禁止无依据扩大量词范围或输出空间。

## 建议的最小修订方向

在研究回流进入 E/F 前或出口检查中，记录研究前已确认的所求与答案形态；给回流条件标记“所求维度／必要定界／操作化或适用限定”；比较 proposed B3 的量词范围和输出是否严格扩大原问。只有原问或已确认意图要求条件空间刻画时，才把完整参数域交给阶段二；若条件角色不明且影响阶段二任务定义，使用现有 B2 机制继续定界。无需重构 E/F/G。

## Verified

- [v0.18.0 integration candidate](../attachments/stage1-framing-method-integration-candidate-v0.18.0.md)：Rule E, Rule B research return, Rule F, Rule G, exit checks.
- [run-13 full visible trace](../attachments/run-13-full-visible-trace-2026-09-29.md)：research-derived M/T/D/B operationalizations, creator corrections, final Q0 and answer limits.
- [Shared Research Core v0.1.0](../../GOAL-005-shared-research-loop/attachments/shared-research-loop-core-v0.1.0.md)：research returns findings to host rules; Core does not rewrite host structure.

## Verdict

**REJECT** — current v0.18.0 is not sufficient to reliably prevent scope inflation or parameterization escape after research feedback. F-001 is required / MAJOR. This opinion does not modify v0.18.0 or run-13 disposition and does not authorize method acceptance, another trial, or S2.
