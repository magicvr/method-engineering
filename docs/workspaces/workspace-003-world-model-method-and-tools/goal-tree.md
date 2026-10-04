---
title: 目标树 · workspace-003-world-model-method-and-tools
status: active
created: 2026-09-26
updated: 2026-10-04
parent: null
version: 0.36.0
---

# 目标树 · 世界模型方法与工具

- 工作区：`workspace-003-world-model-method-and-tools`
- canonical：`docs/workspaces/workspace-003-world-model-method-and-tools/`
- vision_role：`primary`
- primary_plan：`VP-003-world-model-method-and-tools`（`active`，`v0.1.1`，`vision_ref` = `method-engineering@0.1.0`）

## 树

```text
GOAL-001-world-model-method-and-tools [active] 为消费方构建并交付世界模型的方法与工具 · R1 完成，PA1 完成 · progress 20%
|-- GOAL-002-r2-method-validation [cancelled] 旧 R2 路线 · terminated-by-reframe · 历史 progress 0%（0/4）
`-- GOAL-003-prior-art-replanning [active] 成熟理论调查、吸收与方法路线重规划 · PA1 完成 · progress 20%（1/5）
    `-- GOAL-004-pa1-baseline-and-source-plan [done] PA1 · 基线与来源方案 · 用户确认关门 · progress 100%（4/4）
```

现行实现路线为 R1→R2-PA→R2-W→R4，R3 在冻结边界内可并行评估，工具实现等接口稳定，R2-W/R3 均就绪后才进入 R4。VP-003 v0.1.1 意图、方向级退出判据和 R1→R2/R3→R4 不改；此次非 strategic。Root 五个等权检查点仅 R1 完成，1/5=20%；分母由旧 1/4 改为 1/5，不撤销 R1、不新增失败，PA 内阶段不计入 Root 分母，progress 不放行。

R1 v0.6.4 历史冻结/同步/关门成果沿用，只证明协议冻结，不证明旧 H1/H2/H3 或理论适用。Root [D-021](GOAL-001-world-model-method-and-tools/01-decision/D-021-prior-art-driven-implementation-reframe.md) 记录新路线；旧路线与成功标准/门禁原文见 [历史基线](GOAL-001-world-model-method-and-tools/attachments/pre-reframe-root-baseline-v1.md)。旧目标终止不是 done/100%，历史 D/E/A 与附件原位保全，见 [清单](GOAL-002-r2-method-validation/attachments/reframe-history-manifest-v1.md)。

门禁唯一权威在 [Root meta](GOAL-001-world-model-method-and-tools/00-meta.md)：I-001/I-003 verified；I-007 为 accepted-residual（权限未知部分经用户明确接受，非 verified）；I-002/I-004/I-006/I-008～I-010 open；历史 I-005 最后事实状态仍 open、旧 R2c/R2d 撤回。H3-SEM-001 required/open 不作闭合，旧 H3 冻结/运行禁止；新 PA 不要求补完旧预登记，复用旧实验前须重检全部适用门禁。I-007 约束迁移/PA1/新增执行，I-008 来源/抽取 PA2-PA3，I-009 映射 PA3，I-010 缺口/PA5/R2-PA 退出/R2-W/原创启动；I-006 按现行人工过程/既有实践支持 R3 分支，I-002 控制真实案例，I-004 控制 R4 独立审计。

PA1 S1～S4 已完成并经用户确认关门：需求/澄清/R1/旧 H 基线固定，约束迁移矩阵完成，五类来源与访问策略按 J-01 A、J-02 A 残余、J-03 A 冻结，A-003 independent pass。I-007 为 `accepted-residual`（非 verified）；I-008～I-010 仍 open；PA2 未开始。无系统全文抽取/理论适用结论，无新 H 运行/方法工作版/工具/交付事实。运行主记录及下游材料未改。

跨区历史入口：[workspace-002 的 Root](../workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/00-meta.md) 关门仅验证供需流程，不证明领域方法。
## 状态表

| id | title | parent | status | progress | notes |
|---|---|---|---|---|---|
| `GOAL-001-world-model-method-and-tools` | 为消费方构建并交付世界模型的方法与工具 | `null` | active | 20% | R1/R2-PA/R2-W/R3/R4 五等权检查点，1/5；仅 R1 完成。I-007 accepted-residual（非 verified）。VP-003 v0.1.1。 |
| `GOAL-002-r2-method-validation` | R2 · 方法假设验证与工作版形成 | `GOAL-001-world-model-method-and-tools` | cancelled | 0% | terminated-by-reframe，历史 0/4；superseded_by: GOAL-003-prior-art-replanning；H3-SEM-001 required/open，旧 H3 禁止冻结/运行。 |
| `GOAL-003-prior-art-replanning` | 成熟理论调查、吸收与方法路线重规划 | `GOAL-001-world-model-method-and-tools` | active | 20% | PA1 已完成并经用户确认关门；PA2 未开始。I-007 accepted-residual，I-008～I-010 open；无系统全文抽取/理论适用结论。 |
| `GOAL-004-pa1-baseline-and-source-plan` | PA1 · 基线与来源方案 | `GOAL-003-prior-art-replanning` | done | 100% | S1～S4 完成，4/4；J-01/J-02/J-03 已裁决并冻结；A-001 findings 经 A-002 fixed；A-003 independent pass；用户确认关门。 |
