---
title: fresh-context subagent smoke test 与 trace 可见性限制
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-085
doc: execution-entry
---

# E-085 · fresh-context subagent smoke test 与 trace 可见性限制

## Smoke 设置与观察

Root 生成并保留一个随机 canary，未将其写入或发送给 subagent task。使用 `collaboration.spawn_agent` 创建 `/root/context_smoke`，参数为 `agent_type: worker`、`fork_turns: none`；task 只含一项无关任务：“Convert 68°F to Celsius. Show the formula and give the answer rounded to one decimal place.” 未测试 filesystem deny、Docker/VM、CLI 或 web search。

Subagent 正常返回 `(68 − 32) × 5/9 = 20.0°C`，正确读取了唯一 task 内容。其回复没有 canary、method-engineering、Probe、旧 run/audit 或其它旧 conversation 内容。collaboration 工具说明明确规定 `fork_turns: none` 不会向新 subagent 传递 surrounding conversation context。

## 证据边界

当前提供的协作接口可查看 subagent 状态与最终回复，但不提供原始 initial context/trace 的读取入口；Codex app thread 列表也没有暴露该 collaboration subagent 的可读会话项。因此，本次 smoke 支持“`fork_turns: none` 的接口契约不传父对话历史，且 subagent 能读取独立 task”这一结论；不能声称完成了原始 trace 逐字节检查。结论不覆盖系统/平台通用上下文，也不证明 OS/filesystem 访问隔离。

本次使用的是 collaboration tool 的 `agent_type: worker` 入口；本地 `$CODEX_HOME/agents/worker.toml` 已只读检查，但没有单独的本地派发适配器证据，不将该 TOML 声称为实际应用的角色配置。该限制不影响 task 内容或 `fork_turns: none` 的上下文测试。

## 状态

Smoke 的接口契约与行为观察均符合预期，但原始 initial trace 级检查受当前工具可见性限制。创作者随后按 D-053 接受“`fork_turns: none` 接口保证 + 行为观察”作为采用 fresh-context subagent runner 架构的充分依据；raw trace 可见性限制仍须保留，不得称已逐字节检查。该裁决授权形成新合同/binding 与 hash manifest，不授权启动 runner。run-13 binding v0.1.3、隔离合同 v0.1.2、五项 packet、Probe 与 v0.18.0 未修改。
