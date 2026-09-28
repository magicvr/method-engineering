---
title: A-004 · 独立复核 S1 v0.17.0 semantic zoom 候选
status: active
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: A-004
doc: audit-entry
source: independent
---

# A-004 · 独立复核 S1 v0.17.0 semantic zoom 候选

- **日期**：2026-09-28
- **auditor**：Codex Reviewer subagent（gpt-6-sol，medium）
- **审查类型**：独立只读 methodology review
- **scope**：`attachments/stage1-framing-method-candidate-v0.17.0.md` 中的 semantic zoom 设计；核对 handoff-ready、细化触发判据、AI／创作者职责、三态确认、复用同一 S1 方法、OR／AND、规则 E/F/G、局部深度、向上冒泡、不自动重开全局 coverage，以及 handoff 边界。参考 D-034、b-refinement-03、presentation-03、冻结合同 v0.1.1 与 E-064。
- **verdict**：**fail**（Reviewer verdict：REJECT）

## Findings

### F-001 · MAJOR · 粒度就绪与节点级独立交接边界不清

- **位置**：`stage1-framing-method-candidate-v0.17.0.md` 第 302 行，特别是“只将已达到 handoff-ready 的节点标作可交给阶段二的节点”。
- **发现**：该句把节点的答案粒度已经明确到足以支持 S2 启动，直接表述成节点“可交给”阶段二，没有同时要求冻结合同 §1 明确规定的节点级独立交接三条件：① 当前已接受的 S1 method／host 明文允许该范围拆分；② 已提供该方法要求的局部 coverage／closure 证据；③ 独立交接不会破坏父级或兄弟节点的已确认结构。
- **依据**：冻结合同 v0.1.1 §1 将节点级交接设为独立能力，并明确父层确认不能替代局部门禁；当前已接受的 S1 v0.16.1／v0.16.2 没有局部递归／节点拆分门禁。候选 v0.17.0 仍为 draft/unaccepted，不能启用此路径。
- **后果**：读者可能再次把“节点本身达到 handoff-ready”误解为“可单独交给 S2”，形成 A-002 F-001 已修复风险的替代出口。
- **建议**：改为将其称为“粒度已就绪的候选求解节点”或同等不授权措辞；明确实际节点级独立交接另须逐项满足冻结合同 §1 的三条件，且未接受的 v0.17.0 不打开该路径。
- **状态**：待创作者处置；当前未修订候选。

## 已核对项

- v0.17.0 不以“原子问题”为粒度完成标准，明示 handoff-ready 四要素。
- AI 负责判断问题族可能性、举证并生成／比较／攻击候选子结构；创作者只作保持、继续展开或否定节点的三态选择。
- 继续展开时以节点作为局部原问复用阶段一方法，保留 OR／AND、规则 E/F/G；允许局部深度不一致。
- 局部 G.1.3 沿用原判据，按影响向上冒泡；局部递归不自动重开全局 coverage，保留 R-1 并要求具体证据触发更高层回流。
- E-064 正确区分 v0.1.1 冻结时点的案例状态与后续 D-042／E-061／E-063 状态；本次案例确认未被写作 v0.17.0 方法接受。

## Unable to verify

- v0.17.0 仍为 draft/unaccepted；只读设计审阅不能证明运行表现或方法有效性。本审阅不启动试跑、不改变 v0.16.1／v0.16.2 基线，也不授权任何 S2 操作。
