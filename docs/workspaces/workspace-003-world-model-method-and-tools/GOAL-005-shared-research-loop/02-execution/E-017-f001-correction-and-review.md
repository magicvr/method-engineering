---
title: 记录 A-001/F-001 最小修正候选与独立复核
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-005-shared-research-loop
record_id: E-017
doc: execution-entry
---

# E-017 · 记录 A-001/F-001 最小修正候选与独立复核

按 [D-013](../01-decision/D-013-rule-e-research-relevance-clarification-authorized.md)，形成并保留两份 `draft/unaccepted` 新候选：

- [S1 Research Adapter v0.1.1](../attachments/s1-research-adapter-v0.1.1.md)：§2 只列调用时已知输入；§3–4 将研究返回后的条件问题证据、关联推理、必要结构贡献、目标事实未知与排除/去重检查按 schema 现有字段留痕。
- [S1 host v0.16.3](../../GOAL-004-collaborative-question-framing/attachments/stage1-framing-method-candidate-v0.16.3.md)：对齐调用前/研究返回后时序，并澄清 Rule E 的问题相关性、必要结构/求解依赖与“问题纳入、答案未定”要求。

独立 Reviewer 对两份候选给出 **ACCEPT**，认为此前“研究后才生成的产物被列为调用前输入”的 MAJOR 问题已修复；其意见及范围记录于 [A-002](../03-audit/A-002-f001-closure-review.md)。据 [D-014](../01-decision/D-014-a001-f001-fixed-response.md)，A-001/F-001 已按 `fixed` 路径关闭。

核对范围内，shared Core v0.1.0、Schema v0.1.0、S1/S2 adapter v0.1.0、S2 adapter、S1 host v0.16.2、既有试跑设计/绑定包、run-01 与 GOAL-004 v0.17.0 未修改。没有新增 schema 字段；没有运行 research call 或试跑。新候选仍未获创作者接受为基线，亦未获新试跑授权。
