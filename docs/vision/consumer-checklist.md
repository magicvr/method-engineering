---
doc_type: vision-consumer-checklist
title: 愿景体系完整安装核对表
status: active
created: 2026-09-14
updated: 2026-09-14
version: 0.1.0
parent: null
---

# 愿景体系完整安装核对表

> 本表只把 [`alignment.md` §0.2 Minimal Complete Install 的 MUST 表](alignment.md#02-完整安装与冷启动)逐项投影为核对项，不新增或放宽规则。
> 当前 Charter、首个 VP、工作区与 Root 已齐。本表不宣称「方向已稳」，也不把 Root 信息项写成已验证。

| # | MUST 项 | 路径 / 条件 | 当前状态 | 说明 |
|---|---------|-------------|----------|------|
| 1 | 规则入口 | 根 `AGENTS.md` | 已具备 | 项目规则入口存在。 |
| 2 | 文档入口 | `docs/README.md` | 已具备 | 核心文档索引存在。 |
| 3 | 方法论 | `docs/architecture/principles.md` | 已具备 | P-001～P-006 存在。 |
| 4 | 方法论 | `docs/architecture/workspace-protocol.md` | 已具备 | 工作区与资料协议存在。 |
| 5 | 目标模板 | `docs/templates/goal-folder/` | 已具备 | 五件套模板存在。 |
| 6 | 工作区模板 | `docs/templates/workspace-context.md` | 已具备 | 工作区上下文模板存在。 |
| 7 | 愿景模板 | `docs/templates/vision/` | 已具备 | Charter、VP、Review 模板存在；revisions 使用实例台账。 |
| 8 | 消费契约（如分发消费适配器） | `docs/contracts/` | 已具备 | canonical `skills-consumer-contract.json` 与 schema 已落回；与 `skills/contracts/` 哈希一致。 |
| 9 | 愿景规则 | `docs/vision/alignment.md` | 已具备 | 对齐契约存在。 |
| 10 | 愿景入口 | `docs/vision/README.md` | 已具备 | 愿景目录说明已更新。 |
| 11 | 现行愿景 | `docs/vision/charter.md` 为 `status: active` | 已具备 | `method-engineering@0.1.0`。 |
| 12 | 愿景树 | `docs/vision/roadmap.md` | 已具备 | 已登记 `VP-001-enter-real-operation` 的组合编排索引。 |
| 13 | 修订台账 | `docs/vision/revisions.md` | 已具备 | Charter 修订台账已建立。 |
| 14 | Review 索引 | `docs/vision/reviews.md` | 已具备 | 已登记 VRev-001、VRev-002；当前 `open required: 0`。 |
| 15 | 工作区索引 | `docs/vision/workspaces.md` | 已具备 | 已登记 `workspace-001-enter-real-operation`。 |
| 16 | 本核对表 | `docs/vision/consumer-checklist.md` | 已具备 | 与 alignment §0.2 对应。 |
| 17 | 首个 VP（开区前） | 至少一个 `plans/VP-*.md`，`vision_ref` 精确匹配 | 已具备 | `VP-001-enter-real-operation`，`vision_ref: method-engineering@0.1.0`，`status: active`。 |
| 18 | 显式工作区（开区后） | `workspaces/workspace-<NNN>-<slug>/workspace.md` | 已具备 | `docs/workspaces/workspace-001-enter-real-operation/workspace.md`。 |
| 19 | 目标树与 Root（开区后） | 工作区 `goal-tree.md` + Root 五件套 | 已具备 | Root `GOAL-001-enter-real-operation`。 |

## 当前结论

冷启动串行链 Charter → VP → 工作区 + Root 已落地。完整安装 MUST 行中本表能核对的项已具备。Root 的 `I-001` / `I-002` 仍开放，S1 尚未开始；不得宣称 D1 已完成或「方向已稳」。
