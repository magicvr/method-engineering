---
title: R4 双验收层：本仓试运行与下游交付
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-001-world-model-method-and-tools
version: 0.1.0
record_id: D-003
decision_status: accepted
---

# D-003 · R4 双验收层：本仓试运行与下游交付

## 用户澄清

2026-10-04，用户澄清“在本仓直接验收”的含义：指**试运行的真实需求结果**在本仓验收；**方法工作版与可能存在的工具/ no-tool 记录仍须交付下游仓**，并完成实际收件、验收/异议迭代与结束回路。

## 决定

- 本仓验收层：R4 试运行结果由维护者在本仓验收，记录在该轮 `controller/acceptance.md`。
- 下游交付层：方法工作版与 no-tool 记录（未来工具另行授权）按 VP-003 与 consumer-response-protocol 交付下游 `WorldModel.ModernCultivation` 的 exchange 路径，并取得实际收件、验收/异议与反馈路由。
- VP-003 的方向级退出判据 4 不变，无需 strategic re-align；此前“本仓直接验收，不做下游交付验收”的草稿表述作废。
- 两层验收均留证；任一层未完成不得把 R4 标为 done。

## 影响

GOAL-011 S4 改为本仓试运行验收，新增 S5 下游交付/收件/验收回路，S6 维护者外部审计与关门。G-I-001 只表示本仓试运行验收目标；下游交付目标另登记为 G-I-005。
