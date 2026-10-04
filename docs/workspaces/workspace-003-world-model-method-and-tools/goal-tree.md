---
title: 目标树 · workspace-003-world-model-method-and-tools
status: active
created: 2026-09-26
updated: 2026-10-04
parent: null
version: 0.48.5
---

# 目标树 · 世界模型方法与工具

- 工作区：`workspace-003-world-model-method-and-tools`
- canonical：`docs/workspaces/workspace-003-world-model-method-and-tools/`
- vision_role：`primary`
- primary_plan：`VP-003-world-model-method-and-tools`（`active`，`v0.1.1`，`vision_ref` = `method-engineering@0.1.0`）

## 树

```text
GOAL-001-world-model-method-and-tools [active] 为消费方构建并交付世界模型的方法与工具 · R1/R2-PA/R2-W/R3 完成，R4 准备 · progress 80%
|-- GOAL-002-r2-method-validation [cancelled] 旧 R2 路线 · terminated-by-reframe · 历史 progress 0%（0/4）
|-- GOAL-003-prior-art-replanning [done] 成熟理论调查、吸收与方法路线重规划 · PA1～PA5 完成，用户确认关门 · progress 100%（5/5）
|   |-- GOAL-004-pa1-baseline-and-source-plan [done] PA1 · 基线与来源方案 · 用户确认关门 · progress 100%（4/4）
|   |-- GOAL-005-pa2-theory-element-extraction [done] PA2 · 理论来源核实与要素抽取 · 用户确认关门 · progress 100%（4/4）
|   |-- GOAL-006-pa3-requirement-mapping [done] PA3 · 需求/旧假设映射与四类处置 · 用户确认关门 · progress 100%（4/4）
|   |-- GOAL-007-pa4-gap-and-absorption [done] PA4 · 缺口判定与吸收方案 · 用户接受残余并关门 · progress 100%（4/4）
|   `-- GOAL-008-pa5-information-closure-and-route-freeze [done] PA5 · 未决收敛、路线冻结与交接 · S1～S4 完成，A-003 pass，用户确认关门 · progress 100%（4/4）
|-- GOAL-009-r2w-method-working-version [done] R2-W · 方法工作版与内部核对 · S1～S4 完成，A-005 pass，用户确认关门 · progress 100%（4/4）
|-- GOAL-010-r3-tool-branch-evaluation [done] R3 · 工具分支评估与落实 · S1～S4 完成，A-003 pass，用户确认关门 · progress 100%（4/4）
`-- GOAL-011-r4-bounded-real-case-validation [active] R4 · 真实用例 black-box 检验与交付验收 · S3 waiting 真实用户澄清，RUN-001 未完成 · progress 33%（2/6）
```

现行实现路线为 R1→R2-PA→R2-W→R4，R3 在冻结边界内可并行评估，工具实现等接口稳定，R2-W/R3 均就绪后才进入 R4。VP-003 v0.1.1 意图、方向级退出判据和 R1→R2/R3→R4 不改；此次非 strategic。Root 五个等权检查点中 R1/R2-PA/R2-W/R3 完成，4/5=80%；PA 内阶段不计入 Root 分母，progress 不放行。

R1 v0.6.4 历史冻结/同步/关门成果沿用，只证明协议冻结，不证明旧 H1/H2/H3 或理论适用。Root [D-021](GOAL-001-world-model-method-and-tools/01-decision/D-021-prior-art-driven-implementation-reframe.md) 记录新路线；旧路线与成功标准/门禁原文见 [历史基线](GOAL-001-world-model-method-and-tools/attachments/pre-reframe-root-baseline-v1.md)。旧目标终止不是 done/100%，历史 D/E/A 与附件原位保全，见 [清单](GOAL-002-r2-method-validation/attachments/reframe-history-manifest-v1.md)。

门禁唯一权威在 [Root meta](GOAL-001-world-model-method-and-tools/00-meta.md)：I-001/I-003 verified；I-007 为 accepted-residual（权限未知部分经用户明确接受，非 verified）；I-008 为 accepted-residual（S04-C 全文未决经用户接受，非 verified）；I-009 verified（限定映射覆盖与处置依据）；I-010 accepted-residual（非 verified）；I-002 verified（case/authorization；final-version 适配在 R4 S2 核对）；I-004 open（provider/mode selected；external audit output pending）；I-006 accepted-residual（非 verified，仅限 GOAL-010 S2～S4/R3 退出）；历史 I-005 最后事实状态仍 open、旧 R2c/R2d 撤回。H3-SEM-001 required/open 不作闭合，旧 H3 冻结/运行禁止；新 PA 不要求补完旧预登记，复用旧实验前须重检全部适用门禁。I-007 约束迁移/PA1/新增执行，I-008 来源/抽取 PA2-PA3，I-009 映射 PA3，I-010 缺口/PA5/R2-PA 退出/R2-W/原创启动；I-006 按现行人工过程/既有实践支持 R3 分支，I-002 控制真实案例，I-004 控制 R4 独立审计。

PA1～PA5 已完成并经用户确认关门，R2-PA/R2-W/R3 完成；GOAL-009 已 done，Root R2-W checkpoint 完成。GOAL-010 已完成 S1～S4：用户接受证据不足下的 no-tool，I-006 为限定 accepted-residual（非 verified）；no-tool 记录与独立闭合复审已完成，无开放 required；用户确认 GOAL-010 done，Root R3 checkpoint 完成。GOAL-011 S1/S2 完成：正式 R4 原始输入“修真具体怎么修”直接输入方法；RUN-001 冻结包与最终版适配已就绪；本仓验收仅指试运行结果，方法/no-tool 仍须交付下游；S3 待运行。I-007/I-008/I-010 为 `accepted-residual`（非 verified）；I-009 verified（限定）。无理论适用性结论，无新 H 运行/工具/真实案例/交付事实。运行主记录及下游材料未改。

跨区历史入口：[workspace-002 的 Root](../workspace-002-consumer-response-protocol/GOAL-001-consumer-response-protocol/00-meta.md) 关门仅验证供需流程，不证明领域方法。
## 状态表

| id | title | parent | status | progress | notes |
|---|---|---|---|---|---|
| `GOAL-001-world-model-method-and-tools` | 为消费方构建并交付世界模型的方法与工具 | `null` | active | 80% | R1/R2-PA/R2-W/R3/R4 五等权检查点，4/5；R1/R2-PA/R2-W/R3 完成，R4 准备：正式用例原始输入已登记，I-002 case/authorization verified，I-004 外部审计意见待产出。I-007/I-008/I-010 accepted-residual（非 verified）；I-009 verified（限定）；I-006 accepted-residual（非 verified，限定 R3）。 |
| `GOAL-002-r2-method-validation` | R2 · 方法假设验证与工作版形成 | `GOAL-001-world-model-method-and-tools` | cancelled | 0% | terminated-by-reframe，历史 0/4；superseded_by: GOAL-003-prior-art-replanning；H3-SEM-001 required/open，旧 H3 禁止冻结/运行。 |
| `GOAL-003-prior-art-replanning` | 成熟理论调查、吸收与方法路线重规划 | `GOAL-001-world-model-method-and-tools` | done | 100% | PA1～PA5 完成，受限 R2-W 路线与交接包冻结；用户确认 GOAL-003 关门。 |
| `GOAL-004-pa1-baseline-and-source-plan` | PA1 · 基线与来源方案 | `GOAL-003-prior-art-replanning` | done | 100% | S1～S4 完成，4/4；J-01/J-02/J-03 已裁决并冻结；A-001 findings 经 A-002 fixed；A-003 independent pass；用户确认关门。 |
| `GOAL-005-pa2-theory-element-extraction` | PA2 · 理论来源核实与要素抽取 | `GOAL-003-prior-art-replanning` | done | 100% | S1～S4 完成，4/4；37 项来源要素已抽取；A-002 pass；S04-C 为 accepted-residual；用户确认关门。 |
| `GOAL-006-pa3-requirement-mapping` | PA3 · 需求/旧假设映射与四类处置 | `GOAL-003-prior-art-replanning` | done | 100% | S1～S4 完成，4/4；15 个需求项和 H1/H2/H3 已映射；A-002 pass；用户确认关门。 |
| `GOAL-007-pa4-gap-and-absorption` | PA4 · 缺口判定与吸收方案 | `GOAL-003-prior-art-replanning` | done | 100% | S1～S4 完成，4/4；A-002 pass；I-010 为 accepted-residual；用户确认关门。 |
| `GOAL-008-pa5-information-closure-and-route-freeze` | PA5 · 未决收敛、路线冻结与交接 | `GOAL-003-prior-art-replanning` | done | 100% | S1～S4 完成，4/4；受限 R2-W 路线与交接包冻结；A-003 pass；用户确认关门。 |
| `GOAL-009-r2w-method-working-version` | R2-W · 方法工作版与内部核对 | `GOAL-001-world-model-method-and-tools` | done | 100% | S1～S4 完成，4/4；A-002 F-01 与 A-004-F-001 均已 fixed，A-003/A-005 independent pass，无开放 required；用户确认关门。 |
| `GOAL-010-r3-tool-branch-evaluation` | R3 · 工具分支评估与落实 | `GOAL-001-world-model-method-and-tools` | done | 100% | S1～S4 完成，4/4；A-001 F-001 经 A-002/A-003 fixed 闭合，无开放 required；用户确认关门。 |
| `GOAL-011-r4-bounded-real-case-validation` | R4 · 真实用例 black-box 检验与交付验收 | `GOAL-001-world-model-method-and-tools` | active | 33% | S1/S2 完成，S3 进行中：RUN-001 原文直接输入，方法在步骤0提出澄清并 waiting；须真实用户回应后继续。 |
