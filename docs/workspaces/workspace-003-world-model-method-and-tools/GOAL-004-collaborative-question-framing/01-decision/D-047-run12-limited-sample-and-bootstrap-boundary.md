---
title: 接受 run-12 为有限 S1 E2E 行为样本并明确 bootstrap 隔离边界
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-047
doc: decision-entry
---

# D-047 · 接受 run-12 为有限 S1 E2E 行为样本并明确 bootstrap 隔离边界

## 创作者裁决

创作者于 2026-09-28 书面接受 run-12 为**有限的 S1 E2E 行为样本**。隔离复核见 [E-075](../02-execution/E-075-run12-bootstrap-context-isolation-review.md)，执行与证据范围记录见 [E-076](../02-execution/E-076-run12-limited-sample-disposition.md)。

## 样本效力与证据边界

- 唯一已确认的未绑定上下文是固定的用户级 `~/.codex/AGENTS.md`。其内容经复核不含 method-engineering 项目信息、旧 Probe/run、S1/S2 结构、城市机制、候选答案或其他试验特定提示；分类为 **`unbound bootstrap-context deviation`**，不分类为 `project-history isolation failure`。
- 本轮可用于评价实际 transcript 中可观察到的 S1 framing、B1/B2/B3 路由、semantic zoom / coverage / convergence、creator interaction，以及真实发生或未发生的条件分支。未触发的机制只能记为 `not observed`，不能推断为通过或失败。
- 本轮**不能**作为原 binding v0.1.1 的“五项 runner-visible packet-only 隔离门禁已通过”的证据，因为实际存在一个未预登记、未被 binding 绑定的 global bootstrap context。
- “有限行为样本”不等于 v0.18.0 方法被接受或普遍验证，也不改变 run-11 / run-10 既有证据地位。

## 后续隔离合同设计方向

后续试跑的隔离合同应明确允许一组固定、预审计、版本化并由 SHA-256 固定的通用 bootstrap context（例如系统运行指令与用户级通用 `AGENTS.md`），同时将禁止范围定义为 project-specific、probe-specific 或 history-specific context。不要继续采用“除 packet 外任何上下文都不存在”的不可现实满足定义。

此方向仅作为后续合同修订要求记录；本决策不修改 run-12 binding、projection、packet 或任何原始 trace，不授权重跑、实际 S1→S2 handoff 或 W2/S2。
