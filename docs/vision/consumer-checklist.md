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
> 当前仍处于 Charter 冷启动阶段；本表不宣称完整独立启用已通过。

| # | MUST 项 | 路径 / 条件 | 当前状态 | 说明 |
|---|---------|-------------|----------|------|
| 1 | 规则入口 | 根 `AGENTS.md` | 已具备 | 项目规则入口存在。 |
| 2 | 文档入口 | `docs/README.md` | 已具备 | 核心文档索引存在。 |
| 3 | 方法论 | `docs/architecture/principles.md` | 已具备 | P-001～P-006 存在。 |
| 4 | 方法论 | `docs/architecture/workspace-protocol.md` | 已具备 | 工作区与资料协议存在。 |
| 5 | 目标模板 | `docs/templates/goal-folder/` | 已具备 | 五件套模板存在。 |
| 6 | 工作区模板 | `docs/templates/workspace-context.md` | 已具备 | 工作区上下文模板存在。 |
| 7 | 愿景模板 | `docs/templates/vision/` | 已具备 | Charter、VP、Review 模板存在；revisions 使用实例台账。 |
| 8 | 消费契约（如分发消费适配器） | `docs/contracts/` | 待补齐 | 当前未发现 canonical `docs/contracts/`；本轮不处理该安装问题。 |
| 9 | 愿景规则 | `docs/vision/alignment.md` | 已具备 | 对齐契约存在。 |
| 10 | 愿景入口 | `docs/vision/README.md` | 已具备 | 愿景目录说明已更新。 |
| 11 | 现行愿景 | `docs/vision/charter.md` 为 `status: active` | 已具备 | `method-engineering@0.1.0`。 |
| 12 | 愿景树 | `docs/vision/roadmap.md` | 已具备 | 仅保留空组合编排索引，未开始路线图设计。 |
| 13 | 修订台账 | `docs/vision/revisions.md` | 已具备 | Charter 修订台账已建立。 |
| 14 | Review 索引 | `docs/vision/reviews.md` | 已具备 | 已登记 `VRev-001-charter-init`。 |
| 15 | 工作区索引 | `docs/vision/workspaces.md` | 已具备 | 当前为空索引。 |
| 16 | 本核对表 | `docs/vision/consumer-checklist.md` | 已具备 | 与 alignment §0.2 对应。 |
| 17 | 首个 VP（开区前） | 至少一个 `plans/VP-*.md`，`vision_ref` 精确匹配 | 按阶段待具备 | 本轮按用户指令不创建 VP。 |
| 18 | 显式工作区（开区后） | `workspaces/workspace-<NNN>-<slug>/workspace.md` | 按阶段待具备 | 本轮按用户指令不建立工作区。 |
| 19 | 目标树与 Root（开区后） | 工作区 `goal-tree.md` + Root 五件套 | 按阶段待具备 | 本轮不进入实现层。 |

## 当前结论

当前已完成 Charter 层的冷启动写入与自审，但由于用户明确要求暂不创建 VP、路线图设计或工作区，项目仍处于冷启动中间态；后续不得把本状态表述为完整治理安装或已进入交付推进。
