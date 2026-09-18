---
title: 项目愿景层说明
status: active
created: 2026-09-14
updated: 2026-09-18
parent: null
version: 0.7.0
---

# docs/vision · 项目愿景层

本目录保存本项目唯一的愿景与组合治理资料。规则权威是 [`alignment.md`](alignment.md)，元原则全文是 [`../architecture/principles.md`](../architecture/principles.md) 的 P-006；本目录不是 Goal `goal-tree.md`、progress 或目标审计台账。

## 当前状态

- **现行 Charter**：[`charter.md`](charter.md)，`method-engineering@0.1.0`，`status: active`
- **Vision Review**：[`reviews.md`](reviews.md)；当前 `open required: 0`
- **VP**：[`VP-001-demand-driven-method-engineering`](plans/VP-001-demand-driven-method-engineering.md)，`status: closed`（有界闭门）；[`VP-002-first-real-creative-practice`](plans/VP-002-first-real-creative-practice.md)，`status: active`（已激活，已绑定 delivery 工作区）
- **组合编排 / 路线图设计**：已登记 VP-001 与 VP-002；VP-001 的实现层 Root 已完成三阶段纲领路线图
- **工作区**：[`workspace-001-method-engineering-runtime`](../workspaces/workspace-001-method-engineering-runtime/workspace.md) 已归档；[`workspace-002-first-real-creative-practice`](../workspaces/workspace-002-first-real-creative-practice/workspace.md) 已作为 VP-002 的 `delivery` 工作区建立

## 文件角色

| 文件 / 目录 | 角色 |
|-------------|------|
| `alignment.md` | 愿景对齐契约与门禁（规则权威） |
| `charter.md` | 项目唯一 active Charter；对齐链源头 |
| `roadmap.md` | 愿景级组合编排索引，不是目标层纲领路线图 |
| `plans/VP-*.md` | 已确认并落盘的愿景意图；当前为 VP-001 与 VP-002 |
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

VP-001 已落盘并完成有界闭门；VP-002 已激活且 `vision_ref` 精确匹配现行 Charter。VP-002 的 `delivery` 工作区与 Root 已建立；下一步由 `/govern` 处理 Root 的 I-001～I-005 信息就绪门禁，真实作品仓确认后再推进 D1。
