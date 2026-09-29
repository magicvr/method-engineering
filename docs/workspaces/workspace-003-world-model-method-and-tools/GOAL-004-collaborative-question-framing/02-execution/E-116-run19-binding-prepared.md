---
title: 准备 run-19 同基线隔离试跑 binding
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-116
doc: execution-entry
---

# E-116 · 准备 run-19 同基线隔离试跑 binding

依据 [D-070](../01-decision/D-070-a028-f001-fixed-run18-disposition.md) 的同基线、同 raw Probe 与隔离条件范围授权，在 A-028 F-001 按 `fixed` 闭合后，准备全新 run-19 的 [control-side binding](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.0.md)。Binding 为 14,550 bytes，raw-byte SHA-256 `E9C322EA96E98D81C5CB89964556321B0E4E714A9F3B6A0AA8A2434D20FC8158`。其五项 runner-visible packet 与 run-18 的文件字节及 SHA-256 完全相同：v0.18.5 clean execution projection、Shared Research Core v0.1.0、Shared Research Record Schema v0.1.0、S1 Research Adapter v0.1.1、中性 raw input card「世界有多大？」。冻结 source SHA-256 `6B991D86F5BAB4EC4DF65825EA3759D566377325A22D21FC97CBA393FEF6BBD6` 未变；trial design、isolation contract、projection/map、handoff contract、input card 均未改。

准备阶段对 binding 表内 14 项逐一核对当前 raw byte length 与 SHA-256，14/14 匹配；其中当前 `~/.codex/AGENTS.md` 与捕获件均为 13,638 bytes、SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`。核对仅确认当前内容与 binding 清单一致，不代替启动前复核或独立 Reviewer preflight。Runner envelope 沿用中性文本；历史结果、可重复性目的与评价标准仅留控制侧。新调用须有独立 invocation identity、`fork_turns: none` 与 sole runner；完整 trace 将归档至 run-19 专用路径。

当前 binding 为 `proposal / not-run / execution_authorization: not-granted`。独立 preflight 与创作者对最终精确 SHA 的执行授权均待完成；未创建或提示 runner，未发生 creator relay、实际 handoff 或 S2。v0.18.5 方法仍 `draft / unaccepted`；GOAL status/progress、I-401/I-402 不变。
