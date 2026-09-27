---
id: GOAL-005-shared-research-loop
title: S1/S2 共享研究闭环机制设计
status: active
parent: GOAL-002-r2-method-working-version
created: 2026-09-27
updated: 2026-09-28
version: 0.5.7
plan_refs: VP-003-world-model-method-and-tools
primary_plan: VP-003-world-model-method-and-tools
---

# GOAL-005 · S1/S2 共享研究闭环机制设计

## 概述

为阶段一（S1）与未来阶段二（S2）设计一个按需调用、有界收束的共享外部研究子过程，并提出其版本化接入方案：唯一 shared core 保持研究语义 owner；S1/S2 各有窄 adapter 将研究结果交回各自现有裁决/验证过程。本目标位于工作区 `workspace-003-world-model-method-and-tools`，承接 VP-003；父目标是 [GOAL-002-r2-method-working-version](../GOAL-002-r2-method-working-version/00-meta.md)。

本目标是 W2 内当前**顺序处理**的共享研究设计切片。GOAL-004 的 Probe 1 与父层结构确认已按用户要求暂停，本目标不与之并行推进，也不替代或放行 GOAL-004、W2 或 W3。

## 范围与成功标准

- [x] 形成覆盖未知分类与 owner、进入条件、研究问题、来源策略、逐主张证据评价、适用性迁移、综合、停止结局及最小留痕字段的 shared core 候选，并由创作者接受为设计基线（D-004）。
- [x] 候选分别给出 S1 与未来 S2 的窄宿主接口契约；回交到既有判断链，不改写或接入任一方法版本。
- [x] 形成共享 core＋双 adapter 的版本化接入方案 v0.2；创作者接受其组件边界与流程顺序基线（D-005），含未来 S1、S2 两次独立调用试跑的顺序、验证目标与证据接口。
- [x] 完成 core/schema/S1 adapter/S2 adapter 四份独立 v0.1.0 组件候选的复核，并由创作者接受 schema 与两个 adapter 候选为组件设计基线（D-006）。接受不表示 host 集成或试跑验证；三份文件按创作者要求未修改，旧 frontmatter 状态由 D-006 的接受记录更新。
- [x] 选择 S1 可用 host 设计参照并形成一份独立调用试跑设计；v0.16.1 为设计参照（D-007），试跑设计 v0.1 已按案例纯度要求修正并由创作者接受为基线（D-008）。
- [x] 形成、审阅并取得创作者对 S1 集成 host 基线的裁决：窄接口 overlay v0.1.0 经复核（E-010）；完整方法集成候选 v0.16.2 从冻结 v0.16.1 派生并经 Reviewer 复核 ACCEPT（E-011），创作者已接受其作为本轮试跑 host 基线（D-010）。方法仍未试跑；实际研究调用及试跑另需授权。

此工作是单一、已有明确边界的方法候选设计，可直接执行，不另设可执行路线图或 W5。GOAL-002 的 W2→W3→W4 顺序及进度分母保持不变。

## 明确边界

- 只设计共享 research loop 的最小候选、版本化接入方案与 S1/S2 未来试跑设计；本次 S1 试跑设计及身份绑定均已形成并由创作者接受相应基线。实际方法集成和试跑执行仍分别受其既有授权门槛约束。
- 不修改 GOAL-004 的 v0.17.0、GOAL-002 的 W2 v0.4、GOAL-003 结构、共享 core/schema/adapters 或 S2 方法。按 D-009，S1 v0.16.2 已作为从冻结 v0.16.1 派生的集成候选形成、通过复核，并由创作者接受为本轮试跑 host 基线（D-010）；S2 host 版本与插入点留待后续。
- 不运行 S1/S2 调用试跑；当前 S1 合成案例仅用于已接受的试跑设计与待授权绑定包，不计为 W4 / `I-402` 真实案例。S1 实际研究调用与试跑仍未执行，等待单独授权。
- 不启动 Probe 1，不修改任何 Probe 1 运行、呈示或案例结论；不启动 S2 求解或模型构建。
- 不进行开放式、无上限资料搜索；不把搜索未发现资料当成对象不存在。
- 不改变 GOAL-001/002/003/004 的 status 或 progress。GOAL-002 保持 `active / 25%`，W2 为 4 个工作包中的一个、完成分母不变。

## 当前状态

创作者已接受原 core 候选 v0.1 为设计基线（D-004）、接入方案 v0.2 为组件边界与顺序基线（D-005），并裁决集中落点及宿主最小接口范围（D-003）。四份 v0.1.0 候选均已形成并通过独立复核；schema 与两个 adapter 已由创作者接受为组件设计基线（D-006），三份组件附件按要求保持原样，旧 frontmatter 状态由 D-006 的接受记录更新。v0.16.1 已选作 S1 试跑**设计参照**（D-007），独立调用试跑设计 v0.1 已按创作者指定完成唯一的案例纯度修正并获接受（D-008）；45 分钟为计划工作量边界，墙钟不可可靠计时时按查询、来源、检查点和停止理由留痕。窄接口 overlay candidate v0.1.0 已复核 ACCEPT（E-010）；从冻结 v0.16.1 派生的完整 S1 方法候选 v0.16.2 经独立 Reviewer ACCEPT（E-011），并由创作者接受为本轮试跑 host 基线（D-010）。v0.16.2 仍是 draft、未验证且未试跑；独立调用试跑绑定包已固定 host/core/schema/adapter/设计版本及边界，Reviewer 复核为 ACCEPT WITH NOTES（E-013）：执行时须明确应用已接受试跑设计的用途标准，并在首次查询前补齐 schema 要求的本地问题位置、触发与影响、搜索域及时间等调用上下文。执行授权仍待创作者单独裁决。没有修改 v0.16.1、v0.17.0 或已接受组件，未运行研究或试跑。本目标保持 `active`，不声明完成。

## 愿景对齐

- `plan_refs` / `primary_plan`：`VP-003-world-model-method-and-tools`，继承工作区绑定。
- 本目标只提供共享研究子过程设计，不重写 Charter、VP、GOAL-002 的交付范围或下游世界观 canon。

## 信息就绪与未知项

当前未新增 P-005 独立信息项。D-006 记录的 `evidence_role` 是非阻断观察：只有实际试跑出现类比/间接资料被误认作直接证据，才考虑扩展 schema；当前 `support + limits + applicability` 足以开始验证。组件接受不替代 host 集成授权或试跑证据。

## 父目标与台账

- 父目标：[GOAL-002-r2-method-working-version](../GOAL-002-r2-method-working-version/00-meta.md)。
- 决策、执行、审计分别记入本目标 `01-decision/`、`02-execution/`、`03-audit/`；新条目使用平铺 ledger 文件。
- 原始 core 候选：[shared-research-loop-candidate-v0.1.md](attachments/shared-research-loop-candidate-v0.1.md)（文件保留 `draft` 状态；其研究语义已由 D-004 接受为设计基线，并映射至下列拆分 Core 候选）。
- 当前接入方案：[shared-research-loop-integration-plan-v0.2.md](attachments/shared-research-loop-integration-plan-v0.2.md)（boundary/sequence baseline accepted；不授权宿主方法编辑）；[v0.1 初稿](attachments/shared-research-loop-integration-plan-v0.1.md)保留为历史。
- Shared Research Core：[shared-research-loop-core-v0.1.0.md](attachments/shared-research-loop-core-v0.1.0.md)（design baseline accepted）。
- 其余组件基线：[shared-research-record-schema-v0.1.0.md](attachments/shared-research-record-schema-v0.1.0.md)、[S1 adapter](attachments/s1-research-adapter-v0.1.0.md)、[S2 adapter](attachments/s2-research-adapter-v0.1.0.md)（由 D-006 接受为设计基线；附件 frontmatter 按要求保留原样，不代表 host 集成或试跑验证）。
