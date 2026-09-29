---
title: 接受 fresh-context subagent 作为 run-13 runner 架构并授权 binding 修订
status: accepted
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-053
doc: decision-entry
---

# D-053 · 接受 fresh-context subagent 作为 run-13 runner 架构并授权 binding 修订

## 裁决依据

Fresh-context smoke 使用 `collaboration.spawn_agent` 的 `fork_turns: none` 创建 worker subagent；task 只含一项无关换算任务，root-only random canary 未写入 task。Subagent 正确读取并回答。当前接口不提供原始 initial trace，但工具契约明确 `fork_turns: none` 不传递 surrounding conversation context。创作者通过同步裁决接受“接口保证 + 行为观察”作为该隔离决策的充分依据；保留 E-085 所述 raw trace 可见性限制，不把它描述成逐字节 trace 检查。

## 决策

run-13 采用以下 runner 架构：

- root agent 只负责 control / creator relay / reviewer 工作；
- 唯一 runner 是一个通过 `collaboration.spawn_agent` 新建的 fresh-context subagent，必须使用 `fork_turns: none`，不得 fork 父对话；
- runner task 仅含 binding §2.1 的五项 runner-visible packet（其中 raw Probe input card 是本轮唯一案例输入）与最小通用指令：“当前 agent 本身就是唯一 runner；按提供的 S1 材料执行；不要再委派”；不得包含 binding、design、contract、历史 run/audit 或原对话内容；
- 共享 filesystem 不构成隔离失败；runner 实际收到或读取未授权项目／Probe／历史特定内容才构成 contamination；
- root 只在需要真实 creator input 时转交该次创作者答复，不转发其它父对话内容；runner 在 S1 creator confirmation 后停止。

据此授权形成后继隔离合同与 run-13 binding 版本，并做完整 hash / manifest 核验。**本决策不授权启动新 runner。** 新 binding 必须以最终精确 SHA-256 再获单独执行授权。v0.1.3 原 binding 与 v0.1.2 原合同保留为历史快照；不改 Probe、v0.18.0、Core/Schema/Adapter，不运行 CLI、projectless session、Windows sandbox 或 filesystem-root 隔离，不启动 W2/S2，不创建 run-14。
