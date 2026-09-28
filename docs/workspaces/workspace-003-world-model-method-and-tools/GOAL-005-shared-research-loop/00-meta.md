---
id: GOAL-005-shared-research-loop
title: S1/S2 共享研究闭环机制设计
status: done
parent: GOAL-002-r2-method-working-version
created: 2026-09-27
updated: 2026-09-28
version: 0.5.18
plan_refs: VP-003-world-model-method-and-tools
primary_plan: VP-003-world-model-method-and-tools
---

# GOAL-005 · S1/S2 共享研究闭环机制设计

## 概述

为阶段一（S1）与未来阶段二（S2）设计一个按需调用、有界收束的共享外部研究子过程，并提出其版本化接入方案：唯一 shared core 保持研究语义 owner；S1/S2 各有窄 adapter 将研究结果交回各自现有裁决/验证过程。本目标位于工作区 `workspace-003-world-model-method-and-tools`，承接 VP-003；父目标是 [GOAL-002-r2-method-working-version](../GOAL-002-r2-method-working-version/00-meta.md)。

本目标是 W2 内按顺序处理的共享研究设计切片。设立时，GOAL-004 的 Probe 1 与父层结构确认按用户要求暂停；其后父层结构与①-a粒度已按 GOAL-004 D-042／E-061 获创作者确认，所确认范围的 S1 handoff package 已按 E-063 完成合同预检。GOAL-004 的 Probe 1 仍暂停，实际 S2 求解未启动且须另行授权。本目标不替代或放行 GOAL-004、W2 或 W3。

## 范围与成功标准

- [x] 形成覆盖未知分类与 owner、进入条件、研究问题、来源策略、逐主张证据评价、适用性迁移、综合、停止结局及最小留痕字段的 shared core 候选，并由创作者接受为设计基线（D-004）。
- [x] 候选分别给出 S1 与未来 S2 的窄宿主接口契约；回交到既有判断链，不改写或接入任一方法版本。
- [x] 形成共享 core＋双 adapter 的版本化接入方案 v0.2；创作者接受其组件边界与流程顺序基线（D-005），含未来 S1、S2 两次独立调用试跑的顺序、验证目标与证据接口。
- [x] 完成 core/schema/S1 adapter/S2 adapter 四份独立 v0.1.0 组件候选的复核，并由创作者接受 schema 与两个 adapter 候选为组件设计基线（D-006）。接受不表示 host 集成或试跑验证；三份文件按创作者要求未修改，旧 frontmatter 状态由 D-006 的接受记录更新。
- [x] 选择 S1 可用 host 设计参照并形成一份独立调用试跑设计；v0.16.1 为设计参照（D-007），试跑设计 v0.1 已按案例纯度要求修正并由创作者接受为基线（D-008）。
- [x] 形成、审阅并取得创作者对 S1 集成 host 基线的裁决：窄接口 overlay v0.1.0 经复核（E-010）；完整方法集成候选 v0.16.2 从冻结 v0.16.1 派生并经 Reviewer 复核 ACCEPT（E-011），创作者已接受其作为原试跑 host 基线（D-010）。一次有界试跑按 D-011 执行，创作者按 D-012 接受其为有效调用/取证样本；其 E/F/G 回流未整体接受。Rule E 边界审查见 A-001（conditional，F-001 required）；D-013 授权形成 v0.1.1 S1 adapter 与 v0.16.3 host 的澄清候选，独立复核已 ACCEPT 并按 D-014 以 fixed 路径关闭 F-001；二者仍保留一般候选身份。按 D-015，创作者接受 run-02 设计 v0.2 与 v0.16.3/v0.1.1 作为一次调用的特定绑定，并授权一轮隔离 S1 research-loop 试跑；不构成方法验证或一般基线更新。

此工作是单一、已有明确边界的方法候选设计，可直接执行，不另设可执行路线图或 W5。GOAL-002 的 W2→W3→W4 顺序及进度分母保持不变。

## 明确边界

- 设计共享 research loop 的最小候选、版本化接入方案与 S1/S2 试跑设计，并记录两次分别授权的 S1 调用：run-01 按 D-011 执行并按 D-012 接受为调用/取证样本，E/F/G 回流未整体接受；run-02 按 D-015 绑定 v0.16.3/v0.1.1 与新合成案例，仅授权一次调用。Rule E 边界审查见 A-001；F-001 已按 D-014 以 fixed 路径闭合（独立复核 A-002）。run-02 单次授权不构成一般新基线接受、方法验证或额外调用授权。
- 不覆写 GOAL-004 的 v0.17.0、GOAL-002 的 W2 v0.4、GOAL-003 结构、既有 shared Core/Schema/S1 adapter v0.1.0/S2 adapter v0.1.0、S1 host v0.16.2 或 S2 方法。按 D-013 可形成新版本 S1 adapter v0.1.1 与 host v0.16.3 草案；须经独立复核与后续创作者接受才成为新基线。S2 host 版本与插入点留待后续。
- run-01 合成案例仅用于一次已授权并完成、且被接受为有效样本的独立调用试跑（D-011/D-012/E-014），不计为 W4 / `I-402` 真实案例；Rule E/F/G 回流未整体接受。D-015 另授权一次 run-02，限本次绑定的合成案例和修订栈；不包含第二次调用或 S2 试跑。
- 不启动 Probe 1，不修改任何 Probe 1 运行、呈示或案例结论；不启动 S2 求解或模型构建。
- 不进行开放式、无上限资料搜索；不把搜索未发现资料当成对象不存在。
- 不改变 GOAL-001/002/003/004 的 status 或 progress。GOAL-002 保持 `active / 25%`，W2 为 4 个工作包中的一个、完成分母不变。

## 当前状态

创作者已接受原 core 候选 v0.1 为设计基线（D-004）、接入方案 v0.2 为组件边界与顺序基线（D-005），并裁决集中落点及宿主最小接口范围（D-003）。四份 v0.1.0 候选均已形成并通过独立复核；schema 与两个 adapter 已由创作者接受为组件设计基线（D-006），其原版本保持不变。S1 host v0.16.2 仍为原通用试跑基线且未获方法普遍验证；run-01 按 D-011 完成（E-014），创作者按 D-012 接受其为有效调用/取证样本及 Core outcome `sufficient-for-next-step`，但未整体接受 Rule E/F/G 回流；机制自主发现能力未由本轮证明，R-03 保留。A-001 对 Rule E 准入/目标事实边界给出 conditional 意见，D-013 授权形成 S1 adapter v0.1.1 与 host v0.16.3 的澄清候选；F-001 已按 D-014 以 fixed 路径闭合（独立复核 A-002）。后续试跑设计 v0.2 已于 D-015 接受；v0.16.3/v0.1.1 仅作为 run-02 单次调用的 host/adapter 修订，并已绑定身份 hash、合成案例、隔离条件和预算（见 run-02 binding）。一次有界调用已按 D-015 完成（E-019）；A-003 独立复核为 ACCEPT WITH NOTES，可保存为行为样本；其隔离/访问过程无法由现有原始轨迹独立复放。样本接受、两项局部候选协调及 D-017 创作者裁决见下方补记。独立目标级关门审计 [A-004](03-audit/A-004-goal-closeout.md) verdict=`pass`、开放 required=0；创作者按 [D-018](01-decision/D-018-goal-closeout.md) 结项，边界与执行记录见 [E-022](02-execution/E-022-goal-closed.md)。

## 当前状态补记（2026-09-28）

创作者按 [D-016](01-decision/D-016-run02-sample-accepted-and-reconciliation-authorized.md) 接受 run-02 为有效、相对干净的有界 S1 行为样本，并保留 A-003 两项 MINOR 注意项；注意项不是 required findings。按 D-016 授权的一次既有候选协调与 Rule F.2 四字段转写已于 [E-020](02-execution/E-020-run02-candidate-reconciliation.md) 完成。创作者按 [D-017](01-decision/D-017-run02-local-candidates-accepted.md) 接受合并后的 B3-1 与条件性 B3-2，并保留当前粒度；B3-2 的适用性仍待求解项核实，household storage 仍未准入且保持未知。两项是局部内容完整的 S2 求解项，但没有执行全局 Rule G 收束，因此总体 S1→S2 handoff-ready 未建立。本目标 status=`done`；结项仅限本目标有界范围，不建立整体 S1→S2 handoff-ready。

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
