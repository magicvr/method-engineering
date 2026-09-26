---
doc_type: vision-consumer-checklist
title: 愿景体系完整安装核对表
status: active
created: 2026-09-14
updated: 2026-09-26
version: 0.4.3
parent: null
---

# 愿景体系完整安装核对表

> 本表只把 [`alignment.md` §0.2 Minimal Complete Install 的 MUST 表](alignment.md#02-完整安装与冷启动)逐项投影为核对项，不新增或放宽规则。
> Charter、首个 VP、显式工作区和 Root 已按冷启动顺序落盘；本表不把实现层开区误写成 VP-001 已完成。若未来分发消费适配器，`docs/contracts/` 仍需按条件项单独补齐。

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
| 12 | 愿景树 | `docs/vision/roadmap.md` | 已具备 | 已登记 VP-001 与 VP-002，二者均为 `closed`；VP-002 保留对 `workspace-002-consumer-response-protocol` 的历史绑定。实现层 Root 路线图位于工作区目标，不在愿景层复制。 |
| 13 | 修订台账 | `docs/vision/revisions.md` | 已具备 | Charter 修订台账已建立。 |
| 14 | Review 索引 | `docs/vision/reviews.md` | 已具备 | 已登记 `VRev-001`～`VRev-005`；当前 `open required: 0`。 |
| 15 | 工作区索引 | `docs/vision/workspaces.md` | 已具备 | 已登记 `workspace-001-method-engineering-runtime`（archived / `delivery`）与 `workspace-002-consumer-response-protocol`（active / 唯一 `primary`）及其 Root。 |
| 16 | 本核对表 | `docs/vision/consumer-checklist.md` | 已具备 | 与 alignment §0.2 对应。 |
| 17 | 首个 VP（开区前） | 至少一个 `plans/VP-*.md`，`vision_ref` 精确匹配 | 已具备 | `VP-001-demand-driven-method-engineering`，`method-engineering@0.1.0`，已完成有界 `closed`。 |
| 18 | 显式工作区（开区后） | `workspaces/workspace-<NNN>-<slug>/workspace.md` | 已具备 | `workspace-001-method-engineering-runtime`（archived）与 `workspace-002-consumer-response-protocol`（active），均含必填 `plan_refs` / `primary_plan`。 |
| 19 | 目标树与 Root（开区后） | 工作区 `goal-tree.md` + Root 五件套 | 已具备 | Root 为 `GOAL-001-method-engineering-runtime` 与 `GOAL-001-consumer-response-protocol`，二者均为 `done` 且 `parent: null`；各自已建三类 ledger 目录与 `attachments/`。 |

## 当前结论

当前已完成 Charter → VP → 工作区 + Root 的冷启动与实现链。VP-001 与 VP-002 均已有界 `closed`；两个 Root 均为 `done`。workspace-001 已归档并记为 `delivery`；workspace-002 仍为 `active` / 唯一 `primary`，本次 VP 关门不归档该区。以上不表示 Charter 方向级成功边界、具体方法有效性或领域效果已经证明。条件性消费契约项仍按其适用条件处理。
