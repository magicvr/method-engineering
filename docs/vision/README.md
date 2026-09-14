---
title: 项目愿景层说明
status: active
created: 2026-09-14
updated: 2026-09-14
parent: null
version: 0.3.0
---

# docs/vision · 项目愿景层

本目录保存本项目唯一的愿景与组合治理资料。规则权威是 [`alignment.md`](alignment.md)，元原则全文是 [`../architecture/principles.md`](../architecture/principles.md) 的 P-006；本目录不是 Goal `goal-tree.md`、progress 或目标审计台账。

## 当前状态

- **现行 Charter**：[`charter.md`](charter.md)，`method-engineering@0.1.0`，`status: active`
- **Vision Review**：[`reviews.md`](reviews.md)；当前 `open required: 0`
- **VP**：[`plans/VP-001-enter-real-operation.md`](plans/VP-001-enter-real-operation.md)，`status: active`，`vision_ref: method-engineering@0.1.0`，`lead_workspace: workspace-001-enter-real-operation`
- **组合编排**：[`roadmap.md`](roadmap.md) 已登记上述单一波次
- **工作区**：[`workspaces.md`](workspaces.md) 绑定 `workspace-001-enter-real-operation`（`vision_role: primary`）

## 文件角色

| 文件 / 目录 | 角色 |
|-------------|------|
| `alignment.md` | 愿景对齐契约与门禁（规则权威） |
| `charter.md` | 项目唯一 active Charter；对齐链源头 |
| `roadmap.md` | 愿景级组合编排索引，不是目标层纲领路线图 |
| `plans/VP-*.md` | 已确认并落盘的愿景意图；现行 `VP-001-enter-real-operation` |
| `revisions.md` | Charter `VR-NNN` 修订台账 |
| `reviews.md` | Vision Review 稳定索引 |
| `reviews/VRev-NNN-*.md` | 单条 self / independent Vision Review 报告 |
| `workspaces.md` | 愿景层工作区贡献/绑定索引，不保存目标状态 |
| `consumer-checklist.md` | 对照 alignment §0.2 的安装核对表 |

## 分层边界

冷启动与后续级联顺序为：

```text
Charter → VP → 工作区 + Root → 纲领路线图 → 阶段计划 → 子目标
```

- `/vision` 负责 Charter、VP、组合编排、Vision Review 与 re-align。
- `/govern` 负责 VP 已存在且对齐后的工作区、Root 与目标执行。
- Vision 层不写 Goal `parent`、Goal status、progress% 或 Goal `03-audit` finding。
- Charter 初建和 `strategic` 修订需要 Vision Review；独立审视必须使用 `/vision-audit`。

## 下一步

冷启动链已接到实现层。继续用 `/govern` 推进 `[workspace-001-enter-real-operation] GOAL-001-enter-real-operation` 的 S1（固定机制基线、选定并开始真实 Method Case）。不得宣称「方向已稳」。
