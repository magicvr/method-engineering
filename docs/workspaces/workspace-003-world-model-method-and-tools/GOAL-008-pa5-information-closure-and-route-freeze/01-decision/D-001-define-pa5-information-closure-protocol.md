---
title: PA5 信息收敛与路线冻结协议
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.0
record_id: D-001
decision_status: accepted
---

# D-001 · PA5 信息收敛与路线冻结协议

## 决定

先对五类未决逐项选择路径：`verify`（补证据后验证）、`accepted-residual`（用户有界接受）或 `blocked`（有界阻塞并说明解除条件）。只有逐项路径明确后，才允许形成 R2-W 路线。

## 规则

- 无证据或用户裁决时不得写 verified。
- 新增来源、真实案例、实验、原创、费用或外部执行必须另行获得用户授权，明确范围、资源、停点和审计门禁。
- 路线冻结必须逐项标注未决/残余/限制、复审触发和责任，不得外推。
- H3-SEM-001、旧 H 门禁和其他信息项不被本目标自动关闭。

## 当前边界

I-010 residual 只允许 PA4 退出；PA5 路线冻结需要新的证据或用户明确扩展残余。S1 先产出信息收敛计划和用户裁决点。
