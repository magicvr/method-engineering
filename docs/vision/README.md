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
- **VP**：尚未创建（按本轮指令暂不启动）
- **组合编排 / 路线图设计**：尚未开始；[`roadmap.md`](roadmap.md) 仅为空索引骨架
- **工作区**：尚未建立；[`workspaces.md`](workspaces.md) 仅为空绑定索引

## 文件角色

| 文件 / 目录 | 角色 |
|-------------|------|
| `alignment.md` | 愿景对齐契约与门禁（规则权威） |
| `charter.md` | 项目唯一 active Charter；对齐链源头 |
| `roadmap.md` | 愿景级组合编排索引，不是目标层纲领路线图 |
| `plans/VP-*.md` | 已确认并落盘的愿景意图；本轮尚无 VP |
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

本轮停止在 Charter 层。准备继续时，先使用 `/vision` 确认并创建首个 VP；只有 VP 文件存在且 `vision_ref` 精确匹配后，再使用 `/govern` 建立明确命名的工作区并绑定 `primary_plan`。
