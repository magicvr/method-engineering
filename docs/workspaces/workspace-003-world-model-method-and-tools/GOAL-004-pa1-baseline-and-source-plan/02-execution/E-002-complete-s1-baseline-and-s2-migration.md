---
title: 完成 S1 基线与 S2 约束迁移
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.0
record_id: E-002
---

# E-002 · 完成 S1 基线与 S2 约束迁移

## 实际动作

2026-10-04，完成 [PA1 冻结基线](../attachments/pa1-frozen-baseline-v0.1.md) 与 [约束迁移矩阵](../attachments/constraint-migration-matrix-v0.1.md)，决定记录见 [D-002](../01-decision/D-002-constraint-migration-and-authorization-boundary.md)。

- 需求原文固定到下游 `7324bdf`，blob `281582b9...17f3`；本地 SHA-256 `F8B3E49C...4B9`。
- 执行主体澄清第 2 版固定到下游 `e9054c958fa7e0b54e1ba9e272a7f8584dbd9352`，blob `12c55abd...96f6`。
- R1 v0.6.4 固定为本仓 blob `35a617cf...a3d9`，SHA-256 `DCE5C865...B9A81`；旧 H 快照、提取文件和首批来源事实均有版本入口。
- 迁移矩阵覆盖 R1 §1～§5、D-021、D-002 与本目标 D-001，明确通用沿用、内容基线、旧 H 不迁移和待用户裁决四类。

## 事实边界与状态

S1、S2 完成，S3 仅起草来源/访问事实；Root I-007 仍 open，因为来源类型选择、闭源访问权限、调查资源与停止规则尚未由用户裁决。没有读取新的受限全文、没有抽取理论、没有作适用性判断，也没有改变 Root、runtime record、下游或上层愿景。