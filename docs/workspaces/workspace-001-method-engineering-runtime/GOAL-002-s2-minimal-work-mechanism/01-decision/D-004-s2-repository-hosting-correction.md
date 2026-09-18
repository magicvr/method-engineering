---
id: D-004-s2-repository-hosting-correction
doc: decision-entry
goal: GOAL-002-s2-minimal-work-mechanism
status: accepted
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.2.0
---

# D-004 · S2 运行记录改为仓库级承载

## 触发

用户确认：消费仓对接的实体边界是整个项目仓库，而不是 `workspace-001`；工作区只负责建立治理与交互规则，完成后可以关闭。由此，运行记录不能依附于某一工作区的生命周期。

## 决定

将 `runtime-records/` 的 canonical 承载位置修正为仓库项目根：

```text
<repository-root>/runtime-records/
```

该目录是整个消费仓的仓库级运行记录承载。`workspace-001` 及其后续工作区可以引用、治理或审视其中的运行记录，但不拥有该目录，也不能用工作区关闭来结束或隐藏其中的记录。

## 保留与修正范围

- 保留 D-003 已冻结的两个最小记录对象：每条处理主线的 `record.md` 与追加式 `events.md`。
- 保留 `record.md` 作为唯一当前运行状态来源，`events.md` 只作为历史追踪；不新增状态、角色或 Schema。
- 仅修正物理承载边界、路径说明和对应的治理证据；D-003 原方案的工作区级路径被本决定 supersede。
- 运行记录仍不替代任何 workspace `goal-tree.md`、Goal status、progress、信息门禁或 Audit verdict。
- 如需追踪治理来源，可在运行记录中引用 workspace/Goal；这只是来源引用，不把运行记录重新归属到该工作区。

## 理由

仓库级承载与消费方实体边界一致，保证 workspace-001 关闭后，后续工作区和消费流程仍能发现同一套运行记录。它也避免把可持续的运行资产误放入一次性治理上下文，同时不改变工作区内目标台账的 canonical 范围。

## 证据修正

原 P3 记录和 A-003 仍保留当时“工作区根承载”的历史事实，但不再作为当前路径依据。E-005/A-004 记录子目标修正，E-012/A-012 重新验证 Root I-002 的当前承载证据。
