---
title: 接受 A-029 并按 fixed 恢复 run-19 relay parity
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-071
doc: decision-entry
---

# D-071 · 接受 A-029 并按 fixed 恢复 run-19 relay parity

- **日期 / 状态**：2026-09-29；accepted。
- **决策依据**：创作者已授权 run-19 使用相同 v0.18.5 基线、raw Probe、隔离和试跑条件，且明确不做方法纠偏。[A-029](../03-audit/A-029-run19-binding-relay-parity-preflight.md) 对 v0.1.0 的独立 preflight 为 `REJECT`，唯一 required / MAJOR F-001 指出 §5 relay permission 改变；§6 停止点额外措辞仅为 NOTE。
- **处置**：接受 A-029 的 preflight 拒绝，按 `fixed` 关闭 relay parity finding。保留 [v0.1.0](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.0.md) 原字节作被拒身份；新建 [v0.1.1](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.1.md)，将 §5 与 §6.3 恢复为 run-18 原文。run-19 独立 trace 归档路径仅在控制侧单列。没有增加或删减 runner-visible packet、envelope 内容。
- **门禁**：v0.1.1 仍为 `proposal / not-run / execution_authorization: not-granted`。需先对新 binding 精确身份完成 fresh independent preflight，再由创作者对该精确 SHA 单独授权；本决定仅接受修正，不授权启动。v0.18.5、交接合同与共享 packet 未修订；GOAL status/progress 不变。
