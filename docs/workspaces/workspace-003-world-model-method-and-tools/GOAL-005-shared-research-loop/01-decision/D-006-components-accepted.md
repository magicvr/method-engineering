---
title: 接受共享研究记录 schema 与两个 adapter 作为组件设计基线
status: accepted
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-005-shared-research-loop
record_id: D-006
doc: decision-entry
---

# D-006 · 接受共享研究记录 schema 与两个 adapter 作为组件设计基线

创作者接受以下三份 `v0.1.0` 候选作为后续集成与试跑的组件设计基线：

- [S1 Research Adapter](../attachments/s1-research-adapter-v0.1.0.md)
- [S2 Research Adapter](../attachments/s2-research-adapter-v0.1.0.md)
- [Shared Research Record Schema](../attachments/shared-research-record-schema-v0.1.0.md)

接受含义是确认当前职责边界、接口语义与记录结构可作为后续集成和试跑的共同依据；**不表示**已接入 S1/S2 host，也不表示经试跑验证。三份候选文件按创作者要求保持原样，其草案 frontmatter 中的 `acceptance: unaccepted` 未改；本决策台账记录其最新的创作者接受状态，遇到状态投影冲突时以本决策为准。

另记录一项**非阻断观察**：当前 `support`、`limits_and_conditions` 与适用性/迁移记录足以开始验证；如果后续试跑出现类比或间接资料被误当作直接证据，再考虑为 claim 增加显式 `evidence_role`。当前不加字段、不改变 schema，也不影响本次接受。

本决定不授权 host 方法正文修改、调用试跑执行、S2 建模，亦不改变 GOAL-004 Probe 1、run-10 或任何既有案例结论。
