---
title: 完成同条件 run-18 binding 准备与独立 preflight
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-113
doc: execution-entry
---

# E-113 · 完成同条件 run-18 binding 准备与独立 preflight

按创作者 [D-068](../01-decision/D-068-run17-inconclusive-and-run18-directive.md)，在不恢复 run-17 的前提下，准备全新的 run-18 control-side binding。使用冻结 v0.18.5 source（SHA-256 `6B991D86F5BAB4EC4DF65825EA3759D566377325A22D21FC97CBA393FEF6BBD6`）、原 run-17 trial 条件及唯一 raw Probe「世界有多大？」；runner packet 和中性任务按对应 binding 固定。Control-only 历史、争议、方法审计意见和运行评价不提供给 runner。

[run-18 binding](../attachments/s1-historical-anchor-integrated-trial-binding-run-18-v0.1.0.md) 最终大小为 14,067 bytes，raw-byte SHA-256 为 `3AE57BAD700AECA7A8EE26939E8BD37F78A0E0FA494FA091CCEAD249C8D7755A`。独立 Reviewer 对全部 14 项 manifest、五项 runner packet、中性输入卡、runner envelope 与试跑/隔离/relay/停止边界给出 `PASS`、findings=0，见 [A-027](../03-audit/A-027-run18-binding-preflight-review.md)。

本记录完成时，binding 仍为 `draft / not-run / execution_authorization: not-granted`。没有创建或提示 runner，没有输入 Probe，没有 creator relay、handoff 或 S2。按隔离合同 v0.1.3，实际启动前还须 creator 对精确 SHA-256 `3AE57BAD700AECA7A8EE26939E8BD37F78A0E0FA494FA091CCEAD249C8D7755A` 明确授权，并按 binding 执行启动前文件与 bootstrap 核验。此准备与授权请求不修改 v0.18.5，不新增方法规则，不改变 GOAL status/progress、I-401/I-402 或 run-17 的 `interrupted / inconclusive` 状态。
