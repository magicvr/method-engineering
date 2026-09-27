---
id: GOAL-002-r2-method-working-version
doc: decision
status: active
parent: GOAL-001-world-model-method-and-tools
created: 2026-09-26
updated: 2026-09-28
version: 0.9.10
---

# 决策记录 · GOAL-002

## 纲领路线图与阶段计划

纲领路线图（工作包 W1～W4）只写在 [00-meta.md](00-meta.md)。本文件不复制第二份阶段表。

| 工作包 | 计划文件 / 落点 | 说明 |
|--------|-----------------|------|
| W1 | **已完成**（2026-09-26） | 条款映射与差异登记；产出 [`01-decision/D-004-w1-clause-mapping.md`](01-decision/D-004-w1-clause-mapping.md) |
| W2 | **有界修订中**，GOAL-004 承载阶段一方法；当前顺序处理 [GOAL-005](../GOAL-005-shared-research-loop/00-meta.md) 的共享研究闭环 | 当前状态见 [D-015](01-decision/D-015-w2-bounded-reflow.md)～[D-024](01-decision/D-024-s1-host-baseline-accepted.md)；[v0.4](attachments/world-model-method-working-version-v0.4.md) / [A-008](03-audit/A-008-a007-closure-check.md) 保留为历史版本与闭审事实；GOAL-005 core、接入方案边界/顺序、schema 与两个 adapter 设计基线均已接受（GOAL-005 D-004～D-006）；S1 试跑设计 v0.1 经案例纯度修正后已接受，完整 S1 host v0.16.2 已经 Reviewer 复核并由创作者接受为本轮试跑基线（GOAL-005 D-010／GOAL-004 D-038）。试跑绑定包已固定版本与范围；实际研究/试跑未执行，仍需单独授权；不与 GOAL-004 的 Probe 1 并行，不增设 W5 或进度分母；升格路径仍待 I-203 裁决 |
| W3 | [GOAL-003](../GOAL-003-w3-minimal-structures/00-meta.md) 承载；建立依据 [D-014](01-decision/D-014-w3-subgoal-setup.md) 保留 | S1 两结构及字段映射草案已完成；S2 暂停，等待 GOAL-004 形成 W2 新版基线与影响交接；创作者逐字段可填性仍待核 |
| W4 | 未写 | 适用性核对；走查记录是否并入交付包待 `I-202` 裁决 |

## 信息需求与阶段门禁

权威信息表在 [00-meta.md](00-meta.md)。本文件不复制第二份表。

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-09-26 | 建立 R2 子目标并以真实问题为适用性判据 | accepted | `01-decision/D-001-r2-subgoal-setup.md` |
| D-002 | 2026-09-26 | 方法执行主体约束：构建人是创作者，不是 AI 助手 | accepted（部分被 `D-003` 取代，原文保留） | `01-decision/D-002-executor-boundary.md` |
| D-003 | 2026-09-26 | 修正执行主体约束：助手应尽可能协助，但不得代劳 | accepted | `01-decision/D-003-executor-boundary-revision.md` |
| D-004 | 2026-09-26 | W1 条款映射与差异登记 | accepted（由 `D-005` 修订，原文保留） | `01-decision/D-004-w1-clause-mapping.md` |
| D-005 | 2026-09-26 | 响应独立审计 A-001：修订 D-004（三层分离、C3/C4 改写、候选分级） | accepted | `01-decision/D-005-w1-mapping-revision.md` |
| D-006 | 2026-09-26 | 响应独立复审 A-002：修正 §6 / §7.2 / §13 的 ②③ 边界 | accepted | `01-decision/D-006-response-a002.md` |
| D-007 | 2026-09-26 | closure check 通过：冻结 W1 产物为 W2 输入 | accepted | `01-decision/D-007-w1-freeze.md` |
| D-008 | 2026-09-26 | `I-205` 三项裁定落盘并开始 W2（含默认章节顺序） | accepted（**其第 2 节关键项绝对句经 `D-012` 修订为依赖式**，原文保留） | `01-decision/D-008-i205-adjudication.md` |
| D-009 | 2026-09-26 | 响应 A-004：整改为草稿 v0.2 并完成 W2 | accepted | `01-decision/D-009-a004-response.md` |
| D-010 | 2026-09-26 | 响应独立审 A-005：出草稿 v0.3、收回 W2 完成标记、处理 F-004 | accepted | `01-decision/D-010-a005-response.md` |
| D-011 | 2026-09-26 | 接受 A-006 的闭合确认：重新记 W2 完成 | accepted | `01-decision/D-011-a006-closure.md` |
| D-012 | 2026-09-26 | 响应独立审 A-007：修订 D-008 关键项绝对句、出草稿 v0.4 | accepted | `01-decision/D-012-a007-response.md` |
| D-013 | 2026-09-26 | 接受 A-008 闭审：冻结 W2（v0.4）并进入 W3 | accepted | `01-decision/D-013-a008-closure.md` |
| D-014 | 2026-09-26 | 为 W3 建立统一承载子目标 | accepted | [D-014](01-decision/D-014-w3-subgoal-setup.md) |
| D-015 | 2026-09-27 | 按真实方法探针有界回流 W2 | accepted | [D-015](01-decision/D-015-w2-bounded-reflow.md) |
| D-016 | 2026-09-27 | 建立 W2 内共享研究闭环设计切片 GOAL-005 | accepted | [D-016](01-decision/D-016-shared-research-loop-slice.md) |
| D-017 | 2026-09-27 | 登记共享研究闭环版本化接入方案范围与顺序 | accepted | [D-017](01-decision/D-017-versioned-integration-plan-scope.md) |
| D-018 | 2026-09-27 | 裁决共享研究组件集中落点与宿主最小接入范围 | accepted | [D-018](01-decision/D-018-shared-component-boundary.md) |
| D-019 | 2026-09-27 | 接受共享研究 core 设计与接入方案基线 | accepted | [D-019](01-decision/D-019-research-design-baselines.md) |
| D-020 | 2026-09-27 | 记录共享研究组件设计基线接受并继续 W2 有界切片 | accepted | [D-020](01-decision/D-020-research-components-accepted.md) |
| D-021 | 2026-09-27 | 登记 S1 独立研究调用试跑设计范围 | accepted | [D-021](01-decision/D-021-s1-trial-design-scope.md) |
| D-022 | 2026-09-27 | 接受 S1 research-loop 试跑设计并授权形成窄 host 集成候选 | accepted | [D-022](01-decision/D-022-s1-trial-and-host-candidate.md) |
| D-023 | 2026-09-27 | 授权形成并复核 S1 research-loop 集成方法候选 v0.16.2 | accepted | [D-023](01-decision/D-023-s1-host-v0162-integration.md) |
| D-024 | 2026-09-28 | 接受 S1 research-loop 集成版 v0.16.2 为试跑 host 基线 | accepted | [D-024](01-decision/D-024-accept-s1-host-baseline-v0162.md) |
