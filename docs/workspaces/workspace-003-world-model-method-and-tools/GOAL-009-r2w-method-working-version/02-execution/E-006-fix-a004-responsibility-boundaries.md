---
title: 修复 A-004 责任与排除边界
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-001-world-model-method-and-tools
version: 0.1.0
record_id: E-006
---

# E-006 · 修复 A-004 责任与排除边界

2026-10-04，按 D-003 与用户确认的 `fixed` 裁决，完成 independent A-004 的附件层整改。

## 实际修改

- [方法工作版](../attachments/method-working-version-v0.1.md)：写入 R1 沿用的 AI 协助边界、建议/裁定分栏、无 AI 也可运行，以及需求 §12 十一项排除；世界状态、角色所知、观众所知分开。
- [方法结构](../attachments/method-structure-v0.1.md)：同步 AI 边界、§12 排除、创作者裁定记录和字段名收窄说明。
- [能力缺口判定清单](../attachments/capability-gap-checklist-v0.1.md)：增加 AI 协助、裁定、越界确认、§12 逐项确认和三类认知分开字段。
- [模型条目最小结构](../attachments/model-entry-structure-v0.1.md)：增加同样的 AI/§12/创作者裁定字段，并记录模型条目字段名收窄。
- [需求覆盖与责任](../attachments/requirements-coverage-v0.1.md)：§13-10 指向创作者裁定记录，补记 AI 边界、§12 排除与 GOAL-008 路线冻结落点优先。

## 验证事实

- R1 §12 十一项在方法工作版与两项结构中逐项出现，无缺项。
- AI 协助边界、建议/裁定分栏、创作者裁定记录和字段名收窄已出现。
- §10 五项、§13 十项映射仍齐全；8A/8B、六项 uncertain、PA5 20/14/0/6、H3=0 保留。
- `git diff --check` 通过；未运行真实检查、未新增来源/案例/实验/工具/原创/授权。

A-004-F-001 已形成可核对修正，但须 independent 闭合复审；在复审通过前保持开放 required，S4 不完成。
