---
title: 独立预检 run-16 v0.18.3 projection 与精确 binding
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: A-021
doc: audit-entry
source: independent
verdict: pass
---

# A-021 · 独立预检 run-16 v0.18.3 projection 与精确 binding

## 审阅元数据

- **source**：independent
- **auditor**：Codex Reviewer subagent（gpt-6-sol，medium；fresh-context，`fork_turns:none`，read-only）
- **scope**：只读预检 v0.18.3 clean execution projection 与 source map、run-16 trial identity carry-forward、五项 runner packet、control-only references、隔离与停止边界，以及完整 SHA-256/bytes manifest。未执行 runner，不评价运行行为或 S1 方法整体接受。
- **初次 verdict**：`REJECT`；1 项 MAJOR，另有 1 项 NOTE。
- **closure verdict**：`ACCEPT`；剩余 material findings=0。

## Findings 与响应

### MAJOR · Source→projection map 行号与删节说明不准确

初审指出 map 把 source line 158 误写成只保留首句、并把 Rule D 起点列为 159；实际 line 158 是完整保留的 research-return B3 scope-diff 规范，历史例句位于 line 160，Rule D 从 line 162 开始。此错误使投影保真依据无法精确核对。

**处置：fixed。** 修订 map 后明确 line 158 规范完整保留，line 160 的历史案例仅省略例句后半，line 161 是空行，Rule D 自 line 162 开始；更新 binding 中 map 的 bytes/SHA。Closure reviewer 确认修正准确。

### NOTE · run-13 bootstrap manifest 的既有 scope

初审注意到 run13 generic-bootstrap manifest 描述的是 run-13-only许可及较早的 smoke 流程，而 run-16 采用已接受的隔离合同 v0.1.3 与 run-15 carry-forward 程序。

**处置：澄清控制侧权威。** Binding 逐项固定 run-16 使用的 `~/.codex/AGENTS.md` 来源、run-16 scope、通用内容审计结论与 hash，并明确旧 run-13 manifest 仅作审计/捕获证据，run-13 专属启动流程不继承。不修改 isolation contract，不增加 runner packet 项，也不扩大允许内容。

## Closure reviewer 验证

- v0.18.3 execution projection 包含五项已复核方法修订；投影中未发现 run-15 历史或案例提示。
- run-16 design 与 binding 仅更新 run ID、v0.18.3 source/projection identity 及相应执行身份；原问、自然条件触发路径、creator relay、停止点、评价范围与执行后流程沿用 run-15 接受的范围。
- Runner-visible packet 仍严格为五项；source、map、design、binding、contract、bootstrap references、历史 trace/audits 不进入 packet。
- Binding 使用 `fork_turns: none`，creator relay 逐字，状态保持 `not-run` 与 `execution_authorization: not-granted`，且不授权实际 S1→S2 handoff 或 S2。
- Reviewer 独立核对五项 packet 与六项 control reference 的 bytes/SHA 全部匹配。

## 最终封装身份

- Corrected source→projection map：4,570 bytes，SHA-256 `C3EB4521B80B02E17532A5FBFF48F007CD8ACF4DD7487520E452284684A79870`。
- Run-16 binding：12,736 bytes，SHA-256 `3CC51E2B85BDA0D768FF75501C50DDD819D46BE0C372B22D2D50F8F680BA13B2`。
- Final reviewer verdict：`ACCEPT`，no remaining material finding.

## 审计边界

A-021 只确认最终控制封装与 manifest 可提交精确身份请求创作者授权。它本身不授权或启动 run-16，不证明 v0.18.3 的实际行为，不接受 S1 方法整体，不授权真实 S1→S2 handoff 或 S2。
