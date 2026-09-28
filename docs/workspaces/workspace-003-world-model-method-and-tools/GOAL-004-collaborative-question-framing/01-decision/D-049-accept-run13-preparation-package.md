---
title: 接受 run-13 隔离合同与试跑包作为准备基线，不授权执行
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-049
doc: decision-entry
---

# D-049 · 接受 run-13 隔离合同与试跑包作为准备基线，不授权执行

## 创作者裁决

创作者选择“接受准备包”：接受 run-13 隔离合同、generic bootstrap manifest、raw Probe input、trial design 与 binding 作为准备基线；**不授权执行 run-13**。

裁决对象包括 [run-13 binding v0.1.0](../attachments/s1-e2e-integration-trial-binding-run-13-v0.1.0.md)，其接受时精确 SHA-256 为：

`447A250197EB85973FDF75A3B3B7F2262B86A7751B1DF3577544D1E8B11E8E1F`

独立审计 A-012 对该 package 给出 `ACCEPT WITH NOTES`，本台账 verdict `pass`，required finding=0；唯一 NOTE 是 Probe 较宽泛，research 可能自然为 `not observed`。该路径仍有效且不允许为了验证而强制搜索。

## 决策边界

- run-13 仍为 `prepared-not-run`；binding 中 `execution_authorization` 保持 `not-granted`。实际运行必须另获创作者明确授权，并引用届时完整复算的 binding SHA-256。
- 本裁决不创建 runner/session，不运行 Probe，不授权搜索、真实 S1→S2 handoff、节点级独立交接、W2/S2 或目标世界求解。
- 任一绑定文件或 binding 本身发生变化，旧 hash 接受不覆盖新字节；须重算 manifest 并重新提交裁决。
- S1 v0.18.0 仅保持 D-048 已定的下一轮集成试跑基线，仍为 draft/unaccepted；本裁决不接受方法或宣称验证成功。
