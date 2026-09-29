---
title: 记录 A-029 拒绝、fixed 闭合及 run-19 v0.1.1 binding
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-117
doc: execution-entry
---

# E-117 · A-029 拒绝与 run-19 v0.1.1 binding 修正

[A-029](../03-audit/A-029-run19-binding-relay-parity-preflight.md) 对 [v0.1.0](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.0.md) 的原始 preflight 为 `REJECT`：§5 relay permission 改变，构成 required / MAJOR F-001；§6 停止点附加措辞是 Reviewer NOTE。受审 v0.1.0 保持原样，14,550 bytes，SHA-256 `E9C322EA96E98D81C5CB89964556321B0E4E714A9F3B6A0AA8A2434D20FC8158`，现仅为 rejected/superseded preflight 身份。

按 [D-071](../01-decision/D-071-a029-relay-parity-fixed-run19-binding.md) 创建新的 [run-19 binding v0.1.1](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.1.md)：14,416 bytes，raw-byte SHA-256 `684B3B43A6D086AC0BD7FAD37BFA49FF51FC05C647DC77DE01688400A939B1CB`。§5 全段与 run-18 binding 对应段逐字一致；§6.3 的 S1-stop/trace 指令逐字一致。run-19 专用 trace 路径移到单独控制侧句子，没有方法 coaching。F-001 的 relay parity 缺陷据此按 `fixed` 闭合；原始拒绝结论不变。

新 binding 表中 14/14 文件当前 raw byte length 与 SHA-256 匹配，包括五项 runner-visible packet、v0.18.5 source、projection/map、design、isolation contract 与 generic bootstrap；五项 packet 清单和 runner envelope 仍与 run-18 一致。未修改 v0.18.5、handoff contract、shared packet 或其他 manifest item。仅完成准备及本地清单核对；v0.1.1 的 fresh independent preflight 和创作者对其精确 SHA 的启动授权均待完成。当前 `proposal / not-run / execution_authorization: not-granted`；未创建或提示 runner，未发生 relay、handoff 或 S2。GOAL status/progress 不变。
