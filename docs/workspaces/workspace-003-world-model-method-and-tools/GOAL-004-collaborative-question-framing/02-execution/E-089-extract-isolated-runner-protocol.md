---
title: 从 run-13 提炼项目级 Isolated Runner Protocol v0.1.0
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-089
doc: execution-entry
---

# E-089 · 从 run-13 提炼项目级 Isolated Runner Protocol v0.1.0

run-13 完成后，按创作者的条件授权，将 fresh-context subagent runner 机制提炼为项目级架构协议草案：[Isolated Runner Protocol v0.1.0](../../../../architecture/isolated-runner-protocol.md)。文档明确其范围是 methodological context isolation，不要求 OS/filesystem security sandbox；固定 binding/hash、`fork_turns: none`、有限 packet、creator 原文 relay、post-run contamination 判据及 trace 可见性限制。

协议保持 `draft`，未宣称方法已被普遍验证或接受。其 run-13 证据引用 fresh-context smoke 与 E2E run；run-13 的 research effort-bound 执行偏差仍单独记录，不被协议吸收为已解决。

同步更新 [架构概览](../../../../architecture/overview.md) 与 [docs README](../../../../README.md) 的协议索引。未修改 S1 v0.18.0、Research Core/Schema/Adapter、Probe、handoff contract 或 S2；未授权实际 handoff 或启动 S2。
