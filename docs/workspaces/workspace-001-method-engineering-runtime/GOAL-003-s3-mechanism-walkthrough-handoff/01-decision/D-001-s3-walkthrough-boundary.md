---
id: D-001-s3-walkthrough-boundary
doc: decision-entry
goal: GOAL-003-s3-mechanism-walkthrough-handoff
status: accepted
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.1.0
---

# D-001 · S3 walkthrough 边界、覆盖与交接范围

## 触发

Root S1/S2 已完成，I-001/I-002 已 verified，当前进入 Root 路线图的 S3。VP-001 的退出判据要求一次明确标注为机制验证的 bounded walkthrough，以及由运行责任反推出的最小仓库结构和流程文档的可追踪证据。

## 决定

S3 只做一条机制验证用的纸面 trace，并用覆盖矩阵补足同一运行模型的分支检查。trace 使用虚构但可追踪的 `REQ-PAPER-002`，其记录形状模拟项目根 `runtime-records/<work-item-id>/record.md` 与 `events.md`，但不创建该目录、不把虚构内容写入消费仓运行记录，也不把它当作真实 Method Case。

主 trace 至少经过：

`待判定 → 已接受 → 响应中 → 验证中 → 已交付 → 已退出`

主 trace 采用“确认无需方法变更”响应，以记录判断依据和对该判断本身的验证；覆盖矩阵另行明确它与“复用成熟方法”的区别。矩阵同时核对：

1. 需求进入、IDLE、接受授权、已接受与响应中接缝、响应版本和责任交接；
2. 方法声明、假设、适用条件、已验证结论及证据范围的区分；
3. 验证失败但原边界/限额不变、需要改变边界/限额并重新确认、关键未知尚不能形成失败结论而等待；
4. 对象问题、方法问题、运行机制问题三类反馈，以及反馈不自动授权新的方法工作；
5. 已交付、已退出、退出不等于成功，以及后续信号重新进入待判定；
6. 从 Root D-002、S2 D-004 和项目根 `runtime-records/README.md` 到 Root/VP 退出判据的证据交接。

## 审视路径

S3 采用 `cross`：当前治理会话完成 `source: self`，再由用户已指定的本地 Grok Build CLI 完成 `source: independent`，使用 `grok-4.6` / `xhigh`。provider 不可用或没有可核对输出时，cross 门禁保持未满足，不以其他模型代替。

## 明确不做

- 不接入真实下游需求，不创建真实 `record.md` / `events.md`。
- 不把 `REQ-PAPER-002` 或 walkthrough 结论写成领域方法有效性证据。
- 不新增状态、角色、对象、Schema、自动化、并行调度或未来 Case 特殊协议。
- 不因为 walkthrough 发现理论上可扩展的情形而扩大 S3；只有实际 required finding 才触发最小修正。

## 交接边界

S3 交接的对象是可核对的机制证据：walkthrough、覆盖矩阵、Root I-003 证据引用、项目根运行记录说明和审计意见。交接不改变 `runtime-records/` 的仓库级归属，也不改变 Goal、VP 或 Charter 的状态权威。
