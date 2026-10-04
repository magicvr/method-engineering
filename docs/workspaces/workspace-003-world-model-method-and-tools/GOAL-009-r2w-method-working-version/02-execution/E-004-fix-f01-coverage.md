---
title: 修复 F-01 覆盖缺口
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-001-world-model-method-and-tools
version: 0.1.0
record_id: E-004
---

# E-004 · 修复 F-01 覆盖缺口

2026-10-04，按 D-002 与用户确认的 `fixed` 裁决，完成 independent A-002 F-01 的文档整改。

## 实际修改

- [方法工作版](../attachments/method-working-version-v0.1.md)：在步骤 8 下定义 8A「反补丁与范围/敏感性检查」和 8B「版本/旧裁决与回接」，保留主步骤 0～8。
- [方法结构](../attachments/method-structure-v0.1.md)：同步流程骨架与字段要求。
- [能力缺口判定清单](../attachments/capability-gap-checklist-v0.1.md)：增加 8A/8B 填写字段。
- [模型条目最小结构](../attachments/model-entry-structure-v0.1.md)：增加反补丁、范围/敏感性和版本/旧裁决回接字段。
- [需求覆盖与责任](../attachments/requirements-coverage-v0.1.md)：§13-6/§13-7 改指实际存在的步骤 8A，§13-9/§13-10 改指步骤 8B，并明确本轮只形成指导、实际检查未执行。

## 验证事实

- §10 五项、§13 十项映射仍齐全，共 15 项；主步骤仍为 0～8。
- 8A/8B 在方法、结构、清单、模型结构和覆盖矩阵中一致出现。
- 六项 uncertain（B03/B05/B08/B13/B17/B20）、PA5 20/14/0/6、H3=0 保留。
- `git diff --check` 通过；未运行真实检查、未新增来源/案例/实验/工具/原创/授权。

F-01 已形成可核对修正，但仍须 independent 闭合复审；在复审通过前保持开放 required。
