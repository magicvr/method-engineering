---
id: E-012-s2-repository-hosting-correction
doc: execution-entry
goal: GOAL-001-method-engineering-runtime
status: recorded
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.1.0
---

# E-012 · 重新核对 S2 仓库级运行记录承载

## 已发生事实

- 用户确认消费仓的实体边界是整个项目仓库，workspace-001 只是建立治理和交互规则的阶段性工作区。
- 已将运行记录从 workspace-001 根移动到项目根 `runtime-records/`，并更新其 README 的归属边界。
- 子目标 D-004 supersede D-003 的工作区级路径决定，但保留两个最小记录对象和单一当前状态来源。
- 子目标 A-004 self review 与本条共同构成 Root I-002 的承载修正证据；没有新的 required finding。
- Root S2 仍已完成，I-002 在路径修正后重新核对为 `verified`；S3 仍未开始。

## 事实边界

本条只修正运行记录的项目级物理承载，不改变 D-002 运行模型、最小对象、状态语义或工作区目标树。

## Checkpoint

- checkpoint commit：`9be9b6f fix(govern): 将运行记录改为仓库级承载`
- 覆盖：项目根 `runtime-records/README.md`、旧路径移除、D-004/A-004/A-012、Root/子目标索引和 `workspace.md` 修正。
