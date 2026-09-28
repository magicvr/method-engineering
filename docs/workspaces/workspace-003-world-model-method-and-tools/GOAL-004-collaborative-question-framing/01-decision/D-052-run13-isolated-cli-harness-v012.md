---
title: 接受 run-13 isolated CLI harness 修订；只授权 disposable smoke
status: accepted
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-052
doc: decision-entry
---

# D-052 · 接受 run-13 isolated CLI harness 修订；只授权 disposable smoke

## 裁决

接受将 run-13 启动改为普通 PowerShell 调用 Codex CLI，并用 C:/Users/magicvr/Documents/Code/method-engineering-run13-isolated 固定 cwd/workspace root；新增按当前 CLI permission-profile schema 配置的 run13-isolated profile，使用 Windows elevated sandbox、最小 runtime read、五项 packet read-only、仅 trace write，以及原 repo／旧 trial 位置显式 deny。正式与 smoke 使用完全相同的 binary/profile/cwd/启动路径。

接受 bootstrap 门禁分成三个时点：Probe 前 control side 重读并 hash 当前 ~/.codex/AGENTS.md；同路径 disposable smoke 核验 runtime 注入及 filesystem 权限；正式运行后从 runtime trace 核对正式 session 实际注入 bytes/hash。若正式注入不匹配，标记 bootstrap contamination / invalidated，保留原 trace，不补写。

## 授权边界

- 本裁决接受 binding v0.1.2 准备和 disposable smoke；smoke 不输入 run-13 Probe，不能发展成正式 runner，也不得读 Probe input card。
- smoke 通过后必须重新申请一次 run-13 正式执行授权，并绑定 v0.1.2 最终 SHA-256。D-051 对 v0.1.1 的旧 hash 授权不延续到 v0.1.2。
- 任一 profile parse、elevated sandbox、cwd/root、packet access、repo canary denial、AGENTS injection、history isolation 或 hosted web-search smoke 失败，均停止并记录；不得为了通过而扩大 profile。
- run-13 仍是 prepared-not-run；不创建 run-14，不修改 v0.18.0、Research Core、Schema、Adapter、Probe 或试跑设计，不启动 W2/S2，不实际 handoff/求解。
