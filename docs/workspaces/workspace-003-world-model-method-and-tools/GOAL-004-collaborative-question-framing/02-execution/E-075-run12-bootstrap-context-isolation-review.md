---
title: Run-12 global bootstrap context 来源与隔离范围复核
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.1
id: GOAL-004-collaborative-question-framing
record_id: E-075
doc: execution-entry
---

# E-075 · Run-12 global bootstrap context 来源与隔离范围复核

## 已核实事实

- rollout `world_state` ordinal 6 注入的 `agents_md.text` 为 **7,002 字符 / 13,638 UTF-8 bytes**，SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`，与全局 Codex 文件 `C:\Users\magicvr\.codex\AGENTS.md` 的 13,638 原始字节完全匹配。Ordinal 5 的 user bootstrap block 1 也含同一文本，外围有 `<INSTRUCTIONS>` 包装。完整内容以字节级副本保存于 [run12-global-agents-captured.md](../attachments/run12-global-agents-captured.md)；来源、scope 与内容审查见 [隔离复核报告](../attachments/run12-bootstrap-context-isolation-review-v0.1.0.md)。rollout 没有记录 source-path 字段；路径归属是基于精确内容匹配与本机 Codex home 文件位置，而非运行时显式 provenance。
- 该文件仅含通用 agent 角色路由、执行与用户裁决规则。`方法论`、`历史实现／历史模式调查`、`找案例／查历史` 均为泛化示例；没有 method-engineering 项目名、GOAL、Probe/run 身份、S1/S2 特定内容、城市机制或历史案例事实。Reviewer 子代理 `run12_bootstrap_content_review`（`gpt-6-sol`, `medium`）独立复核此内容与范围，verdict `ACCEPT`；此 verdict 不是 run 有效性判定。
- 项目根 `method-engineering\AGENTS.md` 是另一个文件，28,464 bytes，SHA-256 `4D05EFCF394C18C251BF8594A67A3F9A52316EB4F16335A4ED33136EB360B73A`，与注入内容不同。它位于 runner cwd 的旁系项目根，不是 runner 的 cwd 祖先，且未出现在 rollout ordinal 5 或 6。runner cwd 与唯一 `workspace_roots` 为 `method-engineering-run12-isolated`；运行后清理前的目录清单仅含五项 packet 与 trace 目录，无 `AGENTS.md`。其 cwd 祖先链上没有项目级 `AGENTS.md`。
- 原仓库不在 runner 的 workspace roots 中；managed filesystem scope 是该临时 root 的 read-only。runner 唯一的文件读取尝试为读取全局角色 TOML，ordinal 26 记录 policy rejection。完整 rollout 未记录读取原 workspace 文件的调用，也无 `web_search`。现有记录支持 runner 不能从文件系统读取原 workspace。

## 分类与当前状态

- 将 E-074 最初的 `invalidated / contaminated` 分类更正为 **`unbound bootstrap-context deviation`**；本复核不认定 project-history isolation failure。
- 该降级不自动证明 binding §3 的五项 packet-only 条件通过。隔离复核提交时，样本效力仍待创作者裁决；创作者随后按 [D-047](../01-decision/D-047-run12-limited-sample-and-bootstrap-boundary.md) 接受本轮为**有限的 S1 E2E 行为样本**，可用于评价实际可观察行为，但明确排除“原 binding v0.1.1 packet-only 隔离门禁已通过”这一证据主张；执行记录见 [E-076](E-076-run12-limited-sample-disposition.md)。
- 此项裁决不影响既有 contract-content fit 结果：Reviewer 对 transcript 作 trial-only 判断为“不符合完整 handoff package”；这不构成实际 S1→S2 交接。没有重跑、没有修改任何 raw trace、没有启动 W2/S2。

## 依据

- 完整原始执行轨迹及原 SHA-256：见 [trace manifest](../attachments/run12-invalidated-trace/trace-manifest.md)。原始 rollout 未改写。
- 本次完整隔离复核：见 [review report](../attachments/run12-bootstrap-context-isolation-review-v0.1.0.md)。
