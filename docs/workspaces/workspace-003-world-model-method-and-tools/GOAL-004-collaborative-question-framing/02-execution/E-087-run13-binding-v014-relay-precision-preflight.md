---
title: 修正 run-13 binding creator relay 精度并完成最终 preflight
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-087
doc: execution-entry
---

# E-087 · 修正 run-13 binding creator relay 精度并完成最终 preflight

按创作者裁决，只对 [run-13 binding v0.1.4](../attachments/s1-e2e-integration-trial-binding-run-13-v0.1.4.md) 做一处非结构性精确化：当需要 creator input 时，root 必须将当轮 creator 回复原样、逐字转发给 runner，不得总结、解释、改写、补充，也不得携带其它 parent conversation context。其余隔离模型、runner architecture、Probe、v0.18.0、Core/Schema/Adapter 与 trial design 均未改动。

## 最终身份与 preflight

- Isolation contract v0.1.3 保持不变，SHA-256：`76E2F4B289F32E78520E9D99EA8A84B76E130B970F61F6FB18CD6E0730CC293D`。
- 按 binding manifest 全量重算 21 项：21/21 匹配，0 mismatch；projection map 所载 source candidate 与 execution projection hashes 均匹配。
- 最终 binding v0.1.4：15,648 bytes，SHA-256：`B9692F1034F00085509E4456C810F1909A45C32196E82672EB8CB0815F66D7A4`。
- E-086 保留为前一次 v0.1.4 preflight 的历史记录；其当时 hash `CAE5ED3E…1058E4` 已被本次精确化替代，不再作为执行身份。

本记录完成时，binding 中 `trial_status` 仍为 `not-run`，`execution_authorization` 仍为 `not-granted`。未创建正式 runner、未输入 Probe、未运行试跑。执行前须获得明确引用最终 binding SHA 的授权。
