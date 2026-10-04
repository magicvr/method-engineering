---
id: GOAL-003-prior-art-replanning
title: 成熟理论调查、吸收与方法路线重规划
status: active
parent: GOAL-001-world-model-method-and-tools
created: 2026-10-04
updated: 2026-10-04
version: 0.3.1
progress: 20%
---

# GOAL-003 · 成熟理论调查、吸收与方法路线重规划

## 概述与单一 scope

承接 Root R2-PA，围绕已冻结需求调查成熟理论，抽取要素、映射必要需求与旧局部假设，形成可追溯吸收/改造/不适用/未决处置、缺口判断和后续方法路线交接。PA1 已由 [GOAL-004-pa1-baseline-and-source-plan](../GOAL-004-pa1-baseline-and-source-plan/00-meta.md) 完成并经用户确认关门：基线固定、约束迁移、来源/访问方案和资源/停止规则均有证据，A-003 independent verdict pass。I-007 为 `accepted-residual`（非 verified），I-008～I-010 仍 open；PA2 已由 [GOAL-005-pa2-theory-element-extraction](../GOAL-005-pa2-theory-element-extraction/00-meta.md) 承载；S1～S3 完成，S4 因 PA-S04-C 全文 unresolved 待 I-008 核对。无系统全文要素抽取/理论适用结论；PA1～PA5 检查点 1/5=20%。依据为 [Root D-021](../GOAL-001-world-model-method-and-tools/01-decision/D-021-prior-art-driven-implementation-reframe.md)。

## 非目标

不自行构建普遍世界理论，不完成旧预登记、不恢复旧 H 冻结/运行，不把 H 假设当真；不在本目标形成最终 R2-W 工作版、实现工具、运行真实案例、交付验收；不修改 Charter/VP 意图、runtime record、下游或其他工作区；不以来源清单代替研究或适用性验证。

## 成功标准

- [x] 冻结可追溯基线与调查边界/来源方案，继承与新增授权清楚。
- [ ] 来源核实与要素抽取有原文定位、前提、限制和证据等级。
- [ ] §10/§13 与旧 H 局部主张映射完整，四类处置有可核对依据。
- [ ] 必要需求缺口和替代检查、吸收/有限改造方案可追溯，不混淆未知和已证限制。
- [ ] 后续路线/门禁/停止条件/责任冻结并交接，开放必改项和信息项不被假放行。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|---|---|---|---|
| PA1 | 基线与来源方案 | 已完成 | S1～S4 完成；Root I-007 为 accepted-residual；A-003 independent pass；用户 2026-10-04 确认关门。 |
| PA2 | 理论要素抽取 | 进行中 | 原始来源、版本与定位可核对，抽取要素/局部主张、前提/边界与限制；Root I-008 满足。 |
| PA3 | 需求/旧假设映射与四类处置 | 未开始 | 逐项映射 §10/§13 和 H1/H2/H3，明确适用依据、差异与四类处置；Root I-008/I-009 满足。 |
| PA4 | 缺口判定与吸收方案 | 未开始 | 区分尚未查明/适用限制，记录替代检查、必要需求、继承/有限改造不足及吸收方案，关键 unresolved 不冒充缺口。 |
| PA5 | 后续路线冻结与交接 | 未开始 | Root I-010 满足，核对信息/审计/授权门禁，冻结 R2-W 路线、范围/退出/停止/责任，形成可追溯交接。 |

先后 PA1→PA2→PA3→PA4→PA5；同阶段可并行盘点来源，但不得越过前阶段到期 required 门禁。PA1 已由 [GOAL-004](../GOAL-004-pa1-baseline-and-source-plan/00-meta.md) 完成；PA2 由 [GOAL-005](../GOAL-005-pa2-theory-element-extraction/00-meta.md) 承载；PA3 以后暂未建子目标。

## 派生进度展示

PA1～PA5 五个等权检查点中 PA1 已完成，1/5=20%。PA1 关门不放行 PA2、不关闭 I-008～I-010、不覆盖信息状态。

## 信息门禁引用（非第二台账）

唯一状态/证据权威在 [Root 信息表](../GOAL-001-world-model-method-and-tools/00-meta.md)：I-007 约束迁移、调查边界与超出授权的新执行（PA1），当前为 `accepted-residual`（权限未知部分已由用户接受，非 verified）；I-008 来源真实性及抽取充分性（PA2/PA3）；I-009 映射/适用依据（PA3）；I-010 缺口/选路依据（PA5、R2-PA 退出、R2-W/原创启动）。任何真实案例仍引用 I-002，工具/最终交付分别引用 I-006/I-004。旧 I-005 与 H3-SEM-001 仅为旧路线历史开放项，不当作新 PA 必经前置，也不办理闭合；复用旧实验须重检。

## 四类处置操作定义

- **inherit**：来源与适用依据已核对，保留要素语义，无需实质改变而纳入。
- **adapt**：保留可追溯来源，显式记录有限改造、理由、差异风险及验证安排。
- **not-applicable**：有已核实的范围/前提与必要需求不匹配依据；不是声称理论错误或不存在。
- **unresolved**：来源、解释、适用性或比较证据尚不足；不得作吸收已验证或缺口已确证。

分类对象是要素或局部主张，不给整理论贴总标签；同一理论的不同要素可以分别处置。

## 原创许可与停止规则

只有缺口对应必要需求、调查边界和替代检查有记录、区分“尚未查明”与“已发现适用限制”、继承/有限改造不足、原创范围和停止条件明确、相关信息/审计/授权门禁满足时，才可进入原创探索。禁止把“没搜到”写成“理论不存在”。

未核实来源不参与适用性定论；存在关键 unresolved、信息冲突、到期 required、必改 finding 或需新增执行/预算时暂停受影响范围，回流调查/登记/用户裁决；未经授权不扩大范围。

## 父目标与对齐

父目标 [GOAL-001-world-model-method-and-tools](../GOAL-001-world-model-method-and-tools/00-meta.md)。沿父链服务 VP-003 v0.1.1 → Charter method-engineering@0.1.0，只承接既定意图，不复写第二套愿景。旧目标 [GOAL-002-r2-method-validation](../GOAL-002-r2-method-validation/00-meta.md) terminated-by-reframe；历史不是本目标的成功证据。

## 台账布局

按 docs/templates/goal-folder 的 meta/decision/execution/audit 结构建立四个索引文件（五件套角色），并建齐 01-decision/、02-execution/、03-audit/、attachments/；D/E/A 目录平铺，从 D-001/E-001/A-001 起递增，信息状态只在 Root。
