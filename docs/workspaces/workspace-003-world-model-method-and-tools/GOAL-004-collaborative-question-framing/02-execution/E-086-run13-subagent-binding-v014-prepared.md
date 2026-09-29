---
title: 形成 run-13 subagent 隔离合同与 binding v0.1.4 并完成 preflight
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-086
doc: execution-entry
---

# E-086 · 形成 run-13 subagent 隔离合同与 binding v0.1.4 并完成 preflight

按 [D-053](../01-decision/D-053-run13-subagent-context-runner.md)，形成隔离上下文合同 [v0.1.3](../attachments/s1-isolated-trial-context-contract-v0.1.3.md) 与 run-13 binding [v0.1.4](../attachments/s1-e2e-integration-trial-binding-run-13-v0.1.4.md)。v0.1.3/v0.1.2 的旧文件均保留为历史快照。方法、Probe、trial design v0.1.1、Core、Schema、Adapter 与五项 runner-visible packet 身份不变。

## Runner 架构与范围

root 作为 control / creator relay / reviewer；唯一 runner 改为新建的 fresh-context subagent，显式使用 `fork_turns: none`。runner 任务限定为现有五项 runner-visible 文件（其中一项是唯一 raw Probe input card）及“当前 agent 是唯一 runner、按 S1 材料执行、不得再委派”的通用指令。父 conversation、binding/design/contract、旧 run/audit 与其它 control-side 内容不转给 runner。共享 filesystem、cwd 或 runner 理论上的文件访问能力不构成失败；按实际收到或读取的未授权内容判 contamination。Research 与 semantic zoom 均继续按真实条件触发，不强制搜索或递归。

## Preflight 证据

- binding manifest 21 项均已按完整字节重算：21/21 匹配，0 mismatch；source candidate 与 execution projection 的当前 SHA-256 同时匹配 projection map。
- sibling trial directory 顶层仍恰有五项 packet 文件；五份副本各自 SHA-256 均匹配 binding。已有 `trace/` 内容保留，未读取、覆盖或修改；binding 要求后续使用唯一新 trace 文件名。
- 当前已审计 `C:\Users\magicvr\.codex\AGENTS.md` 为 13,638 bytes，SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`，与 allow-list 相同。
- Isolation contract v0.1.3：7,285 bytes，SHA-256 `76E2F4B289F32E78520E9D99EA8A84B76E130B970F61F6FB18CD6E0730CC293D`。
- Binding v0.1.4：SHA-256 `CAE5ED3EFFF1DF60012856D019C7A9359A3FAA9394CAD484F2EFB15CCA1058E4`。

run-13 当前仍为 `not-run`；binding execution authorization 尚未取得。本次只完成准备与 hash preflight，没有创建 runner、输入 Probe、启动 CLI/projectless session、使用 Windows sandbox 或开始 S2。须先由创作者明确接受并授权 binding v0.1.4 的精确 hash。
