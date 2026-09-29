---
title: A-014 F-001 响应记录 · v0.18.1 所求守恒修订
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
doc: audit-response
---

# A-014 F-001 响应记录 · v0.18.1 所求守恒修订

## disposition

- **来源 finding**：[A-014 F-001](A-014-v018-scope-preservation-review.md)，required / MAJOR。
- **创作者裁决**：[D-054](../01-decision/D-054-a014-f001-v0181-scope-preservation.md)：按 required / MAJOR 处理；保留 v0.18.0 为 run-13 冻结试跑基线；建立最小后继候选 v0.18.1。
- **修订产物**：[v0.18.1 integration candidate](../attachments/stage1-framing-method-integration-candidate-v0.18.1.md)，SHA-256 `A894CF5BF95F877D8DD904B4E276232E1444C4CFBA575D7D7B7BA98585EF499A`。
- **独立复审**：[A-015](A-015-a014-f001-v0181-closure-review.md) 对七项文本响应给出 `pass`；更完整的 A-014 原 scope 复核见 [A-016](A-016-v0181-a014-scope-closure-review.md)，确认研究回流路径上的 F-001 修复，同时提出一项新的 required / BLOCKER 范围回归。
- **A-014 F-001 处置**：研究回流路径上的所求守恒修复经独立复核可核对；A-014 原始 `fail` verdict 保留为对 v0.18.0 的历史审计结论。由于 A-016 的新 finding 尚待创作者裁决，v0.18.1 不冻结。

## 逐项响应

| A-014 F-001 要求 | v0.18.1 修复位置 | 响应说明 |
|---|---|---|
| 1. 建立回流前 demand baseline：原问所求、量词范围、答案形态、creator 已确认 scope | §“研究回流所求守恒检查”，段落 1（约第 132 行） | 研究结果进入 E/F 前记录当前有效 baseline；未确认部分保持未定，研究材料不得替代 creator 意图；creator 后续改 scope 时另建 baseline。 |
| 2. 先区分条件角色：原问所求维度、必要 S1 定界项、操作化／适用限定 | 同节条目（约第 134–140 行） | 明确三种当前需求角色，且声明这是回流候选的作用标记，不是 B1/B2/B3 外的新 taxonomy。 |
| 3. 形成 B3 时对 demand baseline 做 scope diff | 同节 scope diff 段（约第 142 行）；F.2（约第 196–204 行） | 检查量词、未要求遍历的自由维度、答案形态升级和额外信息量；“更强问题包含原答案”不构成所求守恒；研究回流 B3 留存第 5 项对照。 |
| 4. 允许答案说明操作化与适用限定，不自动变成求解维度 | 例示段（约第 144 行）；F.2（约第 198–204 行） | 存在性问题可要求说明标准、时间尺度、扰动范围、系统边界及其如何限定结论；无需因此刻画整个条件组合空间。 |
| 5. 仅原问或 creator 已确认意图要求参数域等时，才产生自由参数职责 | 角色条目（约第 136、138 行）；F.2（约第 198 行） | “值未知”或“会影响结果”不足以要求参数空间求解；不得无依据增设自由维度。 |
| 6. 角色不明且改变 S2 任务定义时，走现有 B2 | 角色条目与 scope diff 段（约第 137、142 行） | 复用既有 F.1/B2 定界，不新增 blocker 类型；不要求 creator 逐项指定变量值。 |
| 7. 出口检查增加 demand-preservation | 出口检查第 11 项（约第 410 行） | 对最终问题集、baseline、量词、自由维度、答案升级、research-return B3 scope diff 和限定误升格作检查；无明确需求依据的扩大退回重写。 |
| 8. 风险表反映 scope inflation / parameterization escape 风险及对应防护 | 风险表（约第 453 行） | 明确把答案操作化／适用条件被扩大成无依据参数空间求解列为风险，并指向回流前 baseline、角色区分、B3 scope diff 与出口检查作为防护。 |
| 9. 后续检验项能检查所求守恒是否实际发生 | 后续检验观察项（约第 499 行） | 将 baseline 记录、条件角色判定、scope diff、避免把存在性／指定对象判断升级为全域刻画，以及不要求 creator 逐项选值列为观察项。 |

## 边界与不变项

- v0.18.0 文件未修改，仍保留为 run-13 的冻结试跑基线；原 SHA-256：`6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3`。
- run-13 完整 trace 未修改；SHA-256：`3D12AC8D6C1866CA453798CD7E3186D45A671EAFDABFAA331243B35537D50546`。
- Shared Research Core v0.1.0（`F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7`）、Record Schema v0.1.0（`5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8`）及 S1 Research Adapter v0.1.1（`BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C`）均未修改。
- 未重构 E/F/G；未修改 Probe、案例裁决或 run-13 记录；未启动新 Probe、S1→S2 handoff、W2/S2 或实际求解。
- v0.18.1 仍为 `draft / unaccepted`，尚未冻结、试跑或验证。A-015 的 pass 仅闭合 A-014 F-001 的文本修正审查，不代表方法行为验证。
- A-016 指出研究回流以外的 N2 路由和出口检查可能被意外扩展；该 finding 当前开放，见 [A-016](A-016-v0181-a014-scope-closure-review.md)。
