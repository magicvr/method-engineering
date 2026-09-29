---
title: 接受 A-014 F-001 并授权形成 v0.18.1 所求守恒修订候选
status: accepted
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-054
doc: decision-entry
---

# D-054 · 接受 A-014 F-001 并授权形成 v0.18.1 所求守恒修订候选

## 决策

接受 [A-014](../03-audit/A-014-v018-scope-preservation-review.md) 的审计结论与 required / MAJOR F-001，采用 `fixed` 路径做最小修订，形成 `stage1-framing-method-integration-candidate-v0.18.1.md`。

修订边界：

1. 研究结果进入 E/F 前，记录当前有效的原问所求、量词范围、答案形态及已确认 scope。
2. 研究回流条件先标明其作用：原问要求求解的维度、必要的 S1 定界项，或答案操作化／适用限定。
3. research-return B3 与 baseline 做 scope diff，检查量词、自由维度、答案形态和信息要求是否扩大；更强问题包含原问答案不构成保持所求。
4. 允许在答案中说明操作化和证据适用边界，但不自动把它们变成完整参数空间求解。
5. 只有原问或已确认意图要求参数域、阈值、函数关系或条件空间时，才承担相应自由参数求解。
6. 条件角色未明且影响阶段二任务定义时，使用现有 B2；不增设 blocker 或要求创作者逐项选参数。
7. 出口检查确认最终问题集不要求比当前有效 demand baseline 严格更多的信息。

**保留边界：** v0.18.0 原文及其 run-13 冻结试跑身份不变；不修改 run-13 记录、Shared Research Core、Schema、S1 Adapter；不重构 E/F/G；不创建新 Probe 或启动新试跑。v0.18.1 保持 `draft / unaccepted`，A-014 F-001 在完成同 scope 独立复审前仍视为未闭合。

## 理由

A-014 指出当前 E/F/G 虽有候选准入、未决项归属和覆盖攻击约束，却没有强制把研究回流条件与研究前所求对照；因此存在把一般存在性或指定对象判断扩大为完整条件空间刻画的路径。上述修订只补充所求守恒的 host-side 检查，并沿用既有 E/F/B2 门禁。

## 未选方案

- **原地改 v0.18.0：**不采用；其身份固定为 run-13 冻结试跑基线。
- **重构 Rule E/F/G 或修改研究组件：**不采用；超出 A-014 F-001 的最小闭合范围。
- **对所有未知值增加创作者确认或变量 blocker：**不采用；会把当前缺口误修成 elicitation／variableization blocker。

## 后续

形成 v0.18.1 后，由独立 Reviewer 对 A-014 F-001 作同 scope 只读复审。只有复审确认修复并有可核对证据，才将 F-001 记录为 `fixed`；本决策不授权新 Probe、试跑、S2 或 handoff。
