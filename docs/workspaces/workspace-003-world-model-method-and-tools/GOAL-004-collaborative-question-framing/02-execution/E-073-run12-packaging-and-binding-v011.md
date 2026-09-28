---
title: 修正 run-12 封装边界与最终 binding v0.1.1
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-073
doc: execution-entry
---

# E-073 · 修正 run-12 封装边界与最终 binding v0.1.1

## 已发生事实

- 按用户要求重新读取当前 runner-visible execution projection v0.1.0 的实际文件字节并核对：SHA-256 为 `4C46CB78BC2E13F63CA91FB584D51966642BEFCFD8A8C0613B4C6F9E021CE8E8`。建立 projection map v0.1.1，将该实际 hash 写入映射，并同步重算 map hash。
- 将冻结 S1→S2 handoff contract v0.1.1 从 runner-visible packet 移至 control-side。Runner 在 S1 candidate 与创作者确认结束后停止；Reviewer 随后使用合同规范条款作 trial-only `contract-content fit` 判断。合同旧案例快照及 E-064 均不进入 runner context。
- 更新 trial design 至 v0.1.1，并形成 run-12 binding v0.1.1。旧 binding v0.1.0 SHA-256 `1A7548CECE0832A208150EECE6007522F6479CD3723DAA41219575E7D195A6EC` 已废止，不能作为执行授权身份。
- 新 binding manifest 所列 runner packet 与 control-side 文件的路径、身份及 14 项 SHA-256 均已逐项核对匹配。
- v0.18.0 method candidate 与 Probe 原问保持原样；Core、Schema、S1 Adapter 文件保持原样。没有修改 Rule E/F/G、semantic zoom 或 research-loop 语义；没有执行 run-12，也没有进入 S2。

## 最终固定身份

| 产物 | SHA-256 |
|---|---|
| S1 integration candidate v0.18.0 | `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3` |
| Execution projection v0.1.0（actual current bytes） | `4C46CB78BC2E13F63CA91FB584D51966642BEFCFD8A8C0613B4C6F9E021CE8E8` |
| Projection map v0.1.1 | `4CB2664DEADC6EE672B3BE3625361A26B0381176A0A3C68DFFE2B63999C89BAE` |
| Trial design v0.1.1 | `35011BA1451137AB9BBFCD3CE5FC464A5676ED2830EE8D457F3B828CF61212EC` |
| Raw input card v0.1.0 | `28E676D6D59459304DD2CF48B31C91B10B71B5DB3106A39DD429A4F7A88CA028` |
| Run-12 binding v0.1.1 | `370D73B081B3917E9CFACE00FF75BFE738511E0193C8842000CF8E204E5BF50F` |

Full component and control-reference manifest: [run-12 binding v0.1.1](../attachments/s1-e2e-integration-trial-binding-run-12-v0.1.1.md). Updated observation design: [S1 E2E trial design v0.1.1](../attachments/s1-e2e-integration-trial-design-v0.1.1.md).

## 状态与边界

Run-12 remains `prepared-not-run`, `execution_authorization: not-granted`. This entry records package repair only; it is not authorization to execute, a method acceptance, a handoff, or an S2 start. GOAL-004 status, progress, goal-tree, and I-401 / I-402 are unchanged.
