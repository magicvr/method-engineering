---
title: 冻结 v0.18.5 为 run-17 基线并准备新历史锚点试跑
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-067
doc: decision-entry
---

# D-067 · 冻结 v0.18.5 为 run-17 基线并准备新历史锚点试跑

- **日期**：2026-09-29
- **状态**：accepted
- **决定**：接受 A-025 closure；冻结 `stage1-framing-method-integration-candidate-v0.18.5.md`（SHA-256 `6B991D86F5BAB4EC4DF65825EA3759D566377325A22D21FC97CBA393FEF6BBD6`）为下一轮 S1 试跑固定 baseline。冻结只固定 run-17 实验版本身份；方法总体状态仍为 `draft / unaccepted`。准备新的 run-17 historical-anchor integrated operational trial，raw Probe 为「世界有多大？」；沿用 fresh-context subagent、隔离合同 v0.1.3 与 creator relay 逐字转发规则。完成 execution projection、source map、binding 与完整 preflight 后，将精确 binding SHA 提交创作者单独授权；在授权前不启动 runner。
- **理由**：A-025 已对局部请求就绪修订给出文本 closure `ACCEPT`，无 required finding。新的完整历史锚点运行用于评价整合后的 S1 产品行为；不能让旧运行、修订原因或预期维度影响 runner。
- **未选方案**：不恢复 run-16；其 trace 继续作为 v0.18.3 下的暂停证据，不判 pass/fail。不中断旧 trace、不给 runner 旧 Probe/run/audit 或修订说明，不把已知回归点设为运行时提示或必经步骤；冻结不等于方法正式接受，也不授权 S1→S2 handoff 或 S2。
- **影响**：v0.18.5 成为 run-17 的固定 trial baseline；历史锚点范围仍不构成 blind transfer 证据。run-16、v0.18.3 冻结基线、I-401/I-402 与 GOAL 状态保持不变。
- **后续**：完成 run-17 clean execution projection、source map、design/binding 与 hash preflight，提交确切 binding 身份等待执行授权。