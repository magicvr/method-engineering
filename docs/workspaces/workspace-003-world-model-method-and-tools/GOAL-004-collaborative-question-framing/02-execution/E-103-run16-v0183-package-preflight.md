---
title: 准备 run-16 v0.18.3 identity-carry-forward package
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-103
doc: execution-entry
---

# E-103 · 准备 run-16 v0.18.3 identity-carry-forward package

## 已完成

- 以已接受的 run-15 historical-anchor trial design/binding 为行为基线，准备 run-16 身份继承封装；Probe 仍为逐字原问「世界有多大？」，没有扩写试跑目标或观察条件。
- 生成 v0.18.3 clean execution projection 与 control-only source→projection map。投影仅承载 v0.18.3 的五项已复核方法改动和此前已接受的 runner projection 内容；映射行号问题经 A-021 前置审查指出后已修正。
- run-16 runner-visible packet 仍恰为五项：v0.18.3 projection、Shared Research Core v0.1.0、Shared Research Record Schema v0.1.0、S1 Research Adapter v0.1.1、只含原问的 raw input card。Control map、trial design、binding、method source、isolation contract、bootstrap capture/manifest 与历史材料均不进入 packet。
- Binding 明确 fresh-context subagent `fork_turns: none`、单一 runner、creator 回复逐字转发、S1 停止点、research/semantic zoom 等仅按条件自然触发，以及不进行真实 S1→S2 handoff/W2/S2。
- Control-side binding 将已审计的 global `~/.codex/AGENTS.md` 捕获内容按 run-16 scope 固定；只允许该精确通用 bootstrap hash。run-13 manifest 仅作为既有内容审计/捕获证据，不继承其 run-13 启动程序；启动前仍须确认当前文件 hash 未变。

## 独立 preflight 与修订

Fresh-context Reviewer 的初次 preflight 指出 source→projection map 的示例行号错误（把第 158 行规范性 scope-diff 规则误作被删例句）。该 finding 已 fixed：map 现标明第 158 行规则完整保留、第 160 行历史案例仅保留首句、Rule D 从第 162 行开始；对应 map 与 binding 身份均已重算。Reviewer closure re-review verdict=`ACCEPT`，没有剩余实质 finding，完整意见见 [A-021](../03-audit/A-021-run16-package-preflight-review.md)。

## 固定身份

| 产物 | Bytes | SHA-256 |
|---|---:|---|
| v0.18.3 method source | 89,607 | `DF462D7607D7F48BCBCCEDA5563D35C3A51339CA4338422343D8A6BCFE1DD5D9` |
| v0.18.3 execution projection | 54,054 | `A3A8F1FBA626391864BE9572119AE5F42F9DE70A0753EC9E0E07556006259CD0` |
| source→projection map（control only） | 4,570 | `C3EB4521B80B02E17532A5FBFF48F007CD8ACF4DD7487520E452284684A79870` |
| run-16 design（control only） | 9,532 | `27D2218D0A8328BB15055A85B8AE774AF40F8EC4249EDC6A04D26DE637017CC4` |
| run-16 binding（control only） | 12,736 | `3CC51E2B85BDA0D768FF75501C50DDD819D46BE0C372B22D2D50F8F680BA13B2` |

Independent Reviewer recomputed all five packet identities and all six control references in the binding; the manifest matched. This is a package preflight only. Run-16 remains `not-run`, and the binding remains `execution_authorization: not-granted`; no runner was spawned, and no S1→S2 handoff or S2 work occurred. The exact binding hash is submitted for creator authorization. The binding's pre-start packet and bootstrap hash check remains required after authorization and before execution.
