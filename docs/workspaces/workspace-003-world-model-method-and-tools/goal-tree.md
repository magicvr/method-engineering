---
title: 目标树 · workspace-003-world-model-method-and-tools
status: active
created: 2026-09-26
updated: 2026-09-30
parent: null
version: 0.47.28
---

# 目标树 · 世界模型方法与工具

- 工作区：`workspace-003-world-model-method-and-tools`
- canonical：`docs/workspaces/workspace-003-world-model-method-and-tools/`
- vision_role：`primary`
- primary_plan：`VP-003-world-model-method-and-tools`（`active`，`v0.1.1`，`vision_ref` = `method-engineering@0.1.0`）

## 树

```text
GOAL-001-world-model-method-and-tools [active] 为消费方构建并交付世界模型的方法与工具 · progress 25%
└── GOAL-002-r2-method-working-version [active] 形成《世界模型构建方法（工作版）》与两个最小结构 · progress 25%
    ├── GOAL-003-w3-minimal-structures [blocked] W3 · 两个最小结构形成 · progress 33%（S2 暂停）
    ├── GOAL-004-collaborative-question-framing [active] 阶段一协作定界认知方法与 W2 交接 · progress 33%（接口合同 v0.1.1 已冻结，presentation-03 父层结构及①-a当前粒度已获创作者确认；该范围 S1 handoff package 已按合同完成预检（E-063）；R-1／R-2／R-3 保持 residual；run-17 interrupted/inconclusive；run-18 runner 已完成 S1 输出并停在 creator-confirmation；A-028 原始 fail、F-001 已按 fixed 闭合；run-18 候选／coverage／handoff-ready 不作通过证据；run-19 v0.1.0 preflight 被 A-029 拒绝，v0.1.1 已由 A-030 独立 preflight 判为 ACCEPT/PASS，创作者已授权精确 SHA；run-19 于 Rule C 提出澄清但控制侧未 relay，创作者暂停当前 S1 v0.18.5 路线并转入单独的产品层架构重审；run-19 为 interrupted/inconclusive，未到 G／最终候选／确认／handoff-ready；creator confirmation 未 relay；实际进入 S2 尚未执行，待单独授权；旧 S1 v0.18.5 路线暂停；架构 spike 由 GOAL-006 承载且尚未形成正式产品路线）
    │   └── GOAL-006-query-contract-architecture-spike [active] 验证 QueryContract → capability/gap 架构假设（S1 run-001 已完成；D-003 契约就绪获局部支持；无可评估 baseline，能力/gap 结论未观察；S2 未开始或获授权）
    └── GOAL-005-shared-research-loop [done] S1/S2 共享研究闭环机制设计（A-004 独立关门审计 pass；六项成功标准有证据；局限及总体 handoff/S2 边界见 GOAL-005 E-022）
```

Root 的 P-001 纲领路线图为 **R1 → R2/R3 → R4**。R1 已完成（2026-09-26）：适用对象、退出形态、限额与责任、工具边界均已冻结（`D-002` / `E-003`）。**R2 进行中**，由子目标 `GOAL-002` 承载（工作包 W1～W4，**1/4**：仅 W1 完成；W2 有界回流；当前顺序由 GOAL-005 承载共享研究闭环组件与版本化接入计划设计；core、接入方案边界/顺序及三个共享组件设计基线已由创作者接受，S1 设计参照 v0.16.1 与试跑设计 v0.1 已接受；run-01 调用已被接受为有效试跑样本及 Core outcome，但 E/F/G 回流未整体接受。A-001/F-001 已按 D-014 以 `fixed` 路径关闭，独立复核 A-002 通过。run-02 按 D-015 完成一次绑定调用并经 A-003 独立复核为 ACCEPT WITH NOTES；创作者按 D-016 接受其为有效、相对干净的有界行为样本并保留两项 MINOR。E-020 合并候选 1/2、保留由 F.2 求解项核实适用性的条件性候选 3，并完成拟议 B3 的 F.2 四字段；D-017接受两项局部候选当前粒度；总体S1→S2 handoff未建立，不构成方法普遍验证或一般基线更新。run-17 于 creator 局部三态处暂停并记为 `interrupted / inconclusive`；run-18 已按精确 binding SHA 获授权并完成 S1 runner 输出；A-028 独立审计判为 execution regression，原始 fail 保留；F-001 经 D-070/E-115 修正 run-18 证据处置并按 fixed 闭合，run-18 候选／coverage／handoff-ready 不作通过证据；creator confirmation 未 relay，实际 handoff/S2 未发生；run-19 v0.1.0 preflight 被 A-029 拒绝，v0.1.1 已由 A-030 独立 preflight 判为 ACCEPT/PASS，创作者已授权精确 SHA；run-19 于 Rule C 提出澄清但控制侧未 relay，创作者暂停当前 S1 v0.18.5 路线并转入单独的产品层架构重审；run-19 为 interrupted/inconclusive，未到 G／最终候选／确认／handoff-ready；可重复性未获结论；presentation-03 父层结构及①-a当前粒度已获创作者确认，其范围 S1 handoff package 已通过冻结合同预检（E-063），实际进入 S2 待单独授权；不增设 W5，W3 S2 暂停）；R3 经复核无独立形成工作，待交付材料落定后确认；R4 未开始。Root 派生 `progress: 25%`（1/4）——R2 未完成，故不计完成。progress 不推导 `done`。

子目标 `GOAL-002` 的 W4 判据是用户 2026-09-26 提供的真实世界问题（星际时代修真个体伟力及其社会影响），该问题同时作为 `WRK-002` 的有界检验用例（Root `I-002`，已 `verified`）与 R4 的检验输入。其「星际时代」与「为什么可以实现」按该用例的假定切片处理，不裁决下游 `H-003` / `H-004`。

运行状态唯一来源为 [`runtime-records/WRK-002-world-model-method-and-tools/record.md`](../../../runtime-records/WRK-002-world-model-method-and-tools/record.md)（2026-09-26 转为**「响应中」**），本目标不镜像。

跨区引用用限定形式：[workspace-002-consumer-response-protocol](../workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/00-meta.md) 的 Root 已 `done`，其 VP-002 已有界 `closed`；那次关门只验证供需对接流程，不验证任何领域方法。

## 状态表

| id | title | parent | status | progress | notes |
|----|-------|--------|--------|----------|-------|
| `GOAL-001-world-model-method-and-tools` | 为消费方构建并交付世界模型的方法与工具 | `null` | active | 25% | R1 完成；R2 进行中；R3 待交付材料确认；R4 未开始。Root 进度独立计算为 1/4。I-004 仍 open。 |
| `GOAL-002-r2-method-working-version` | 形成《世界模型构建方法（工作版）》与两个最小结构 | `GOAL-001-world-model-method-and-tools` | active | 25% | W1 完成；W2 有界修订中，GOAL-005 按顺序承载共享研究闭环。Core、接入方案边界/顺序及 schema/adapter 组件设计基线已接受；S1 试跑设计 v0.1 已接受，host v0.16.2 为原试跑基线；run-01 获接受为有效样本及 Core outcome，E/F/G 回流未整体接受。A-001/F-001 已按 D-014 关闭，A-002 独立复核通过。run-02 按 D-015 完成一次绑定调用并经 A-003 独立复核为 ACCEPT WITH NOTES；D-016 接受样本并保留两项 MINOR；E-020 仅准备候选 1/2 合并、候选 3 条件性拟议 B3 和其 F.2 四字段，D-017已接受两项局部候选当前粒度，但总体S1→S2 handoff未建立，不构成方法普遍验证或一般基线更新。见 [E-032](GOAL-002-r2-method-working-version/02-execution/E-032-goal005-run02-disposition-and-reconciliation.md) / [E-033](GOAL-002-r2-method-working-version/02-execution/E-033-goal005-run02-local-candidates-accepted.md)。run-17 于 creator 局部三态处暂停并记为 `interrupted / inconclusive`；run-18 已按精确 binding SHA 获授权并完成 S1 runner 输出；A-028 独立审计判为 execution regression，原始 fail 保留；F-001 经 D-070/E-115 修正 run-18 证据处置并按 fixed 闭合，run-18 候选／coverage／handoff-ready 不作通过证据；creator confirmation 未 relay，实际 handoff/S2 未发生；run-19 v0.1.0 preflight 被 A-029 拒绝，v0.1.1 已由 A-030 独立 preflight 判为 ACCEPT/PASS，创作者已授权精确 SHA；run-19 于 Rule C 提出澄清但控制侧未 relay，创作者暂停当前 S1 v0.18.5 路线并转入单独的产品层架构重审；run-19 为 interrupted/inconclusive，未到 G／最终候选／确认／handoff-ready；可重复性未获结论；presentation-03 父层结构已获创作者确认，其范围 S1 handoff package 已通过冻结合同预检（E-063），实际进入 S2 待单独授权。W3 S2 暂停，W4 未开始；仍按 W1→W2→W3→W4 四个工作包计算，不增设 W5；GOAL-002 progress 25%。见 [D-026](GOAL-002-r2-method-working-version/01-decision/D-026-run01-sample-accepted-e-f-review.md) / [E-029](GOAL-002-r2-method-working-version/02-execution/E-029-run01-disposition-recorded.md) / [E-030](GOAL-002-r2-method-working-version/02-execution/E-030-a001-f001-closure-recorded.md) / [E-031](GOAL-002-r2-method-working-version/02-execution/E-031-goal005-run02-research-trial-recorded.md)。 |
| `GOAL-003-w3-minimal-structures` | W3 · 两个最小结构形成 | `GOAL-002-r2-method-working-version` | blocked | 33% | S1 草案保留；S2 暂停，等待 GOAL-004 形成 W2 新版及影响交接；S3 未开始。I-301 open，真实问题“世界有多大”为方法探针；创作者逐字段可填性和填写负担仍待核。见 [D-004](GOAL-003-w3-minimal-structures/01-decision/D-004-real-method-probe-and-pause.md)。 |
| `GOAL-004-collaborative-question-framing` | 阶段一协作定界认知方法与 W2 交接 | `GOAL-002-r2-method-working-version` | active | 33% | 接口合同 v0.1.1 已冻结，presentation-03 父层结构及①-a当前粒度已获创作者确认（D-042/E-061）；该范围 S1 handoff package 已完成合同预检（E-063），R-1／R-2／R-3 保持 residual，B3 包仍未实际移交。run-17 interrupted/inconclusive；run-18 A-028 原始 fail 保留、F-001 按 fixed 闭合；run-18 候选／coverage／handoff-ready 不作通过证据，run-19 v0.1.0 preflight 被 A-029 拒绝，v0.1.1 已由 A-030 独立 preflight 判为 ACCEPT/PASS，创作者已授权精确 SHA；run-19 于 Rule C 提出澄清但控制侧未 relay，创作者暂停当前 S1 v0.18.5 路线并转入单独的产品层架构重审；run-19 为 interrupted/inconclusive，未到 G／最终候选／确认／handoff-ready；可重复性未获结论。实际进入 S2 尚未执行，待单独授权；GOAL-004 status/progress 未变。 |
| GOAL-006-query-contract-architecture-spike | 验证 QueryContract 与能力分类架构 | GOAL-004-collaborative-question-framing | active | — | 四项真实问题处于同一已确认的 VP-003 下游用途；I-001～I-003 verified。S1 run-001 已执行并经 A-002 独立审视；D-003 的四题 QueryContract 就绪阈值获局部支持。无可评估 baseline/材料，能力覆盖、质量、充分性/不足及具体 gap 分类均为 `not observed` / `inconclusive`；无可执行既有 capability 路径证据，S2 未开始、未获授权；不接受正式方法/产品路线。 |
| `GOAL-005-shared-research-loop` | S1/S2 共享研究闭环机制设计 | `GOAL-002-r2-method-working-version` | done | — | 按 D-018 结项；独立关门审计 A-004 verdict=`pass`、开放 required=0，六项成功标准均有证据。A-003 两项 MINOR 与 run-02 轨迹限制保留；不代表 S2 集成/试跑/求解、方法普遍有效或总体 S1→S2 handoff-ready。详见 [A-004](GOAL-005-shared-research-loop/03-audit/A-004-goal-closeout.md) / [E-022](GOAL-005-shared-research-loop/02-execution/E-022-goal-closed.md)。 |
