---
id: E-005-repository-hosting-correction
doc: execution-entry
goal: GOAL-002-s2-minimal-work-mechanism
status: recorded
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.1.0
---

# E-005 · 修正运行记录为仓库级承载

## 已发生事实

- 用户确认消费仓的实体边界是整个仓库，workspace-001 只是建立治理与交互规则的阶段性上下文。
- 已将 `docs/workspaces/workspace-001-method-engineering-runtime/runtime-records/` 移动到项目根 `runtime-records/`；源目录已不存在，目标目录已存在。
- 已更新 `runtime-records/README.md`，明确仓库级归属、工作区关闭后的可持续使用和治理来源引用边界。
- 已创建 D-004，保留 D-003 的对象模型和单一状态源，只 supersede 工作区级物理路径。
- 未创建真实需求记录、示例 Method Case、完整 Schema 或自动化。

## 阶段判断

这是对已完成 S2 承载方案的边界修正，不是重新设计运行对象。待 A-004 self review 和 Root A-012 重新核对后，I-201/I-002 继续保持 `verified`。

## Checkpoint

- checkpoint commit：`9be9b6f fix(govern): 将运行记录改为仓库级承载`
- 覆盖：仓库根 `runtime-records/README.md`、D-004、A-004、Root E-012/A-012、workspace 上下文和路径引用修正。
