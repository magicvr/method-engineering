---
title: 独立预检 run-19 v0.1.0 binding 的 relay parity
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: A-029
doc: audit-entry
source: independent
verdict: fail
---

# A-029 · 独立预检 run-19 v0.1.0 binding 的 relay parity

- **source / attribution**：independent Reviewer（read-only preflight）。以下 verdict、finding 与 NOTE 归于该 Reviewer；末节单列后续 `/govern` 响应。
- **scope**：read-only independent preflight of run-19 v0.1.0 binding；只允许与控制侧 run-18 binding 对比未变的试跑条件和五项 packet。Reviewer 未读 run-18 output、A-028、D-070、E-115 或后运行分析；未执行 runner。
- **受审身份**：[run-19 v0.1.0 binding](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.0.md)，14,550 bytes，SHA-256 `E9C322EA96E98D81C5CB89964556321B0E4E714A9F3B6A0AA8A2434D20FC8158`。
- **Reviewer verdict**：`REJECT`；本台账 verdict：`fail`，仅限 v0.1.0 preflight。

## F-001 · Relay permission mismatch（required / MAJOR）

- **原始 Reviewer finding**：`FAIL — relay protocol differs from run-18. Run-19 §5 changes which creator questions the runner may relay, adding “only genuine creator-owned decisions” and “granularity.” That changes a trial condition beyond run identity and trace paths. Restore the run-18 relay rule if strict repeatability is required. Route to WORKER.`
- **classification**：required；**severity**：MAJOR。受影响门禁是 run-19 同条件 binding preflight 与后续精确 SHA 启动授权；不能将 v0.1.0 判为通过。
- **独立 Reviewer NOTE（非 required finding）**：`Run-19 §6 adds “pause without method coaching” at the S1 stop point. This clarifies conduct, but is another textual change to the control protocol.`
- Reviewer 已核对五项 runner-visible item 的字节数与哈希、source 身份、projection map、design、isolation contract、bootstrap、run-19 身份与 trace 路径、proposal/not-run/not-authorized 状态，以及中性 runner envelope。

## `/govern` 响应与 F-001 闭合（2026-09-29）

本节是后续控制侧响应，不更改上方独立 Reviewer 对 v0.1.0 的 `REJECT`、finding 范围、归因或 NOTE。创作者此前已明确授权同条件且不做方法纠偏；[D-071](../01-decision/D-071-a029-relay-parity-fixed-run19-binding.md) 将本项按 `fixed` 处置。[v0.1.1 binding](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.1.md) 恢复 run-18 §5 relay protocol 和 §6.3 S1-stop/trace 指令原文；run-19 trace 路径仍以控制侧独立句子保留。核对事实见 [E-117](../02-execution/E-117-a029-fixed-run19-binding-v011.md)。

F-001 的具体 relay parity 缺陷已 `fixed`。v0.1.0 原字节保留为 rejected/superseded preflight 身份；该闭合不将它改判通过，也不构成 v0.1.1 的独立 preflight、runner 启动或精确 SHA 授权。
