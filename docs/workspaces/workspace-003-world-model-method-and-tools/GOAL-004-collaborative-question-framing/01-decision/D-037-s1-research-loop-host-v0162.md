---
title: 授权形成并复核 S1 research-loop 集成方法候选 v0.16.2
status: accepted
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-037
doc: decision-entry
---

# D-037 · 授权形成并复核 S1 research-loop 集成方法候选 v0.16.2

## 创作者裁决

创作者选择「进入正式集成」：在冻结的阶段一 v0.16.1 基线上形成独立版本化的 S1 research-loop 集成候选，并作独立复核。候选以 `v0.16.2` 标识；这项授权允许形成和复核集成修订，**不等于接受 v0.16.2 为集成 host 基线，也不授权实际研究调用或试跑**。候选接受与后续试跑执行仍须按 GOAL-005 已接受的 integration plan 分别裁决。

## 范围与约束

- 唯一方法基线为冻结的 [v0.16.1](../attachments/stage1-framing-method-candidate-v0.16.1.md)，SHA-256：`E6C1EF612CEAFB64DDB8C26202D84007405723E19D9647025BF17C6BE5994C34`。
- 允许新增规则 B 路由说明后、规则 D 前的一处研究调用／回流接口，引用已接受为组件设计基线的 S1 adapter、shared core 与 schema v0.1.0；研究返回后继续由现有规则 E/F/G 处理。
- 不修改 v0.16.1、v0.17.0、run-10、Probe 1、案例结构或共享 core/schema/adapters；不修改规则 D/E/F/G、方法门禁或创作者权责，不合并 semantic zoom。
- 保留非阻断观察：若后续试跑发现类比/间接资料被误当直接证据，再评估 schema 增加 `evidence_role`；当前 `support + limits + applicability` 足以开始验证。

## 结果状态

形成的 v0.16.2 仍为 `draft / unaccepted / not trialled`，须由创作者另行决定是否接受为 S1 集成 host 基线。当前决定不修改 Probe 1 或任何案例结论，也不改变 GOAL status/progress。
