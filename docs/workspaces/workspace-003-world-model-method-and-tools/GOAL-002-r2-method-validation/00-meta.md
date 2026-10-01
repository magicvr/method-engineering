---
id: GOAL-002-r2-method-validation
title: R2 · 方法假设验证与工作版形成
status: active
parent: GOAL-001-world-model-method-and-tools
created: 2026-10-01
updated: 2026-10-01
version: 0.1.24
progress: 0%
---

# GOAL-002 · R2 方法假设验证与工作版形成

## 概述

承接 Root `GOAL-001-world-model-method-and-tools` 的 R2 纲领阶段，按 R2a → R2b → R2c → R2d 推进 H1/H2/H3 操作化、有界检验、证据选路及暂定方法工作版形成。本目标只承载 R2；Root 继续维护整体纲领路线、全局信息门禁与最终交付目标。

本目标于 2026-10-01 按用户选择建立。当前处于 R2a 的操作化准备；用户已选择 [H1/H2/H3 合成候选包](attachments/R2a-H123-synthetic-candidate-pack-v0.1.md) 的共享供水站背景、分立 H 单元结构，作为补齐正式预登记的基线（[D-003](01-decision/D-003-select-synthetic-package-preregistration-baseline.md)）。H1 问题、两模型、唯一初始存量变化和四格预测已按 D-022 接受为候选但未冻结；其他准确输入、局部判据/严重度、责任、预算/停点、最终冻结及运行授权仍待逐项完成。基线选择不等于逐字段接受。尚无已冻结的运行预登记、已尝试 H 结果格、方法有效性结论或 R2d 工作版。未记录可核对的人工活动分钟，AI 时间未折算为人时。

2026-10-01，用户按 [D-019](01-decision/D-019-bound-h3-c03-assessability-scope.md) 将 C-03 本轮可评范围限定为两条已选封闭合成链中可观测的供水外减量、窗内变化与零存量边界，不外推一般因果损失公式。该范围决定不关闭 H3-SEM-001；完整矩阵、准确快照及其余运行字段仍待完成，未冻结或运行。

2026-10-01，用户依 [D-020](01-decision/D-020-add-h3-inventory-binding-step.md) 在 H3-01 的 D-014 两步候选后增加一步：步初存量 2、需求 3、供水 2、步末 0，以触及 C-02 库存绑定。保留两条链与 2 个 H3 初评格；H3-01 三步、H3-02 两步。此为未冻结候选，不扩张 D-019 的 C-03 范围、不授权运行；H3-SEM-001 仍 OPEN。

2026-10-01，用户按 [D-021](01-decision/D-021-accept-h3-candidate-applicability-matrix.md) 接受 H3 C-01～C-04 的候选逐链适用性分类与理由：C-01 两链适用；C-02 两链适用但库存绑定机会仅在 H3-01；C-03 两链均限 D-019；C-04 两链适用，保留三步/两步差异且不默默按步数加权。该候选矩阵须与准确输入在生成前复核并冻结，仍不是冻结登记或运行授权；H3-SEM-001 继续 OPEN。

2026-10-01，用户依 [D-022](01-decision/D-022-accept-h1-candidate-inputs-and-predictions.md) 接受 H1 问题、M1/M2 规则、初始存量 8→4 的唯一变化及四格预测 `4 / 0 / 2 / 2` 为候选输入。预测不是观察；局部主张/判据和逐格定性严重度口径随后依 D-023 接受为候选，证据/责任/停止字段与正式冻结仍待完成，不授权运行。

2026-10-01，用户依 [D-023](01-decision/D-023-accept-h1-local-claim-and-judgment-rules.md) 接受 H1 四格局部主张、四标签判据及逐格定性严重度记录为预登记候选。它们仍待与证据字段、停止/偏离流程一并核对冻结；R2a 未完成，不放行运行。

## 成功标准

依 [D-015](01-decision/D-015-set-h3-minimum-model-startability.md)，首版模型集合的最低启动条件是：参考揭示前形成并冻结至少一个实际非占位纯文本模型条目；集合中的每个实际模型条目均可定位 12 类字段，且集合至少含一条可追溯的状态/输入—规则/约束—输出/状态变化机制关系；不要求三个核心均已覆盖。链→能力/模型证据映射与关键遗漏判定按 D-015 执行。该门槛不等同于 H3 支持结论；矩阵、准确输入及执行字段未齐前 H3-SEM-001 仍 OPEN，不授权运行。

H3 已按 [D-004](01-decision/D-004-select-h3-form-first-model-set-from-zero.md) 选择从零形成首版模型：由采样链输出形成实际机制模型集合，在揭示隐藏评估参考前冻结该产物。按 [D-005](01-decision/D-005-define-h3-text-model-and-checklist-basis.md) 与 [D-006](01-decision/D-006-accept-r1-model-entry-fields-for-h3.md)，首版为可审查纯文本机制模型条目，R1 v0.6.4 §2 的 12 类字段信息均须可定位；分析方式按证据需要选择。按 [D-007](01-decision/D-007-set-h3-core-capability-boundaries.md)，C-02～C-04 是核心机制能力，C-01 是须正确遵守的输入/范围前提；核心缺项为 partial，核心矛盾或错述 C-01 为 refuted，无可审查冻结模型或证据不足为 insufficient。按 [D-008](01-decision/D-008-aggregate-h3-at-model-set-level.md)，H3 最终标签针对最终预登记所选链共同形成的模型集合，逐链证据映射保留；单条链未触及能力不自动算失败。按 [D-009](01-decision/D-009-aggregate-explicit-gaps-at-final-set.md)，单链显露的 `explicit-gap` 若由最终冻结集合中的其他模型补足，不自动导致 partial；依 [D-010](01-decision/D-010-label-unassessable-core-as-insufficient.md) 与 [D-011](01-decision/D-011-prioritize-insufficient-over-partial.md)，任一核心能力不可评且影响总体判断时优先标 `insufficient`，`partial` 仅用于核心均可评但最终集合仍缺项；可核对的核心矛盾仍标 `refuted`。依 [D-012](01-decision/D-012-preregister-h3-chain-applicability.md)，运行前按冻结链输入/任务范围预登记逐链适用性及理由，运行后另记实际证据状态；依 [D-016](01-decision/D-016-set-h3-c03-chain-applicability.md)，当前可见日志候选下 C-03 在两条初评链均列为适用，仅表示可核对供水之外的减量，不等于完整 C-03 均可评，仍待并入准确输入与完整矩阵后正式冻结。用户按 [D-013](01-decision/D-013-select-h3-two-initial-chains.md) 选定 `H3-01` 值班操作员×`CTX-017` 与 `H3-02` 检修员×`CTX-042` 为两条初评组合（2 个 H3 格）；依 [D-014](01-decision/D-014-add-h3-cap-binding-input.md)，H3-01 第一阶段需求 5、实际供水 4，并据候选规则相应更新两步水位轨迹。该输入仍是待补齐/审定的草稿，不构成运行授权。H3-SEM-001 保持 OPEN，阻断 H3 正式预登记最终冻结。尚无已形成或冻结的实际首版模型。

- [ ] **R2a · 操作化假设**：为 H1/H2/H3 分别形成具体、可核对且运行前冻结的预登记，包含问题/主张、模型或样本、逐格预测、局部判据、正反例、对照/抽样、证据位置、责任、预算、停止与偏离规则。创作者给出最终局部裁决规则；空白字段不作默认值。
- [ ] **R2b · 有界试验**：仅在相应预登记完整且执行授权适用后，按登记运行并记录观察、反例、偏离、各 H 局部标签、证据与实际人时；试验不超出 R1 冻结额度。真实案例使用前，须按 Root `I-002` 留下案例、用途范围和授权，并关闭该范围门禁。
- [ ] **R2c · 证据选路与必要转向**：分别为 H1/H2/H3 记录 `supported` / `partial` / `refuted` / `insufficient` 及证据，形成有边界的路线选择并按证据处理局部或整体失败。Root `I-005` 仍为权威登记；`insufficient` 保持 open/collecting 并阻断 R2d。
- [ ] **R2d · 暂定方法工作版**：依选路证据形成版本化工作版，覆盖 Root `00-meta.md` 所列需求 §10 / §13 指导范围与两项可手填结构，附逐项映射、证据支持范围、适用条件、限制、未决事项及后续责任；不把流程描述或局部证据外推成普遍有效。

## 本目标路线图（P-001）

用户先按 [D-017](01-decision/D-017-prepare-h3-observable-boundary-input.md) 选择准备非零存量边界输入，后按 [D-018](01-decision/D-018-accept-h3-observable-input-candidate-baseline.md) 接受全套草案为后续预登记候选基线：H3-02 需求/供水 `4 / 2.5`、步界 `8 → 3 → 0`；与 H3-01 同字段、同窗的步内精确读数以 0.5 单位刻度报告，无误差/舍入，零恰为零，窗内水量可连续变化。H3-01/D-014 数值保持不变；新增评估端均匀时间分布/零存量下限另定为未冻结 `H3-BALANCE@0.2`，保留旧离散 `@0.1` 与 D-007 历史。W 的确切时长/单位及完整输入快照等仍待登记；完整 C-03 可评性/矩阵仍须复核，C-02 的步初存量绑定供水案例仍缺。候选基线接受不等于正式冻结或运行授权；H3-SEM-001 继续 `required / OPEN`。

2026-10-01，D-020 后续补入 H3-01 的 C-02 库存绑定候选；此前 D-018 摘要中的“案例仍缺”应读作当时尚无候选步。当前已有候选输入但没有冻结快照或运行证据。H3-01 三步、H3-02 两步，仍保留两条初评链与 2 个结果格，R2a 门禁未关闭。

| 阶段 | 名称 | 状态 | 退出条件 |
|------|------|------|----------|
| **R2a** | 操作化假设 | 进行中 | H1/H2/H3 的具体主张、问题/输入、逐格预测、创作者局部判据、证据与责任、限额、人时及停止/偏离规则均写入相应预登记；每份登记在对应运行前冻结。当前准备方案见 [R2a-operationization-plan-v0.1.md](attachments/R2a-operationization-plan-v0.1.md)，本阶段尚未完成。 |
| **R2b** | 有界试验 | 未开始 | 只执行预登记完整且获得适用授权的单元；遵守各 H 与累计结果格、人时限额，逐项留证。适用真实案例时先关闭 Root `I-002`。 |
| **R2c** | 证据选路与必要转向 | 未开始 | 对各 H 的证据及局部标签形成可核对选路；更新 Root 权威 `I-005` 所需证据。若不足以选路，保持 `I-005` open/collecting，不进入 R2d。 |
| **R2d** | 暂定方法工作版 | 未开始 | 形成有版本、边界、适用条件、证据范围、限制和未决项的工作版，覆盖需求 §10 / §13；完成本目标范围内的内部核对。 |

阶段按 **R2a → R2b → R2c → R2d** 串行；只有已有登记与授权允许时才运行。R2a–R2d 的完成数是本目标 `progress` 唯一来源。

## 派生进度展示

`progress: 0%` 由上方 4 个阶段检查点中 0 个完成项等权计算（0/4）。R2a 正在准备但尚未完成，因此当前仍为 0%。进度不放行试验、选路或工作版形成，不关闭信息项或 finding，也不推导 `done`。

## 信息门禁与父级权威

本目标不复制父目标的同号信息项状态，避免形成第二权威：

- [Root I-002](../GOAL-001-world-model-method-and-tools/00-meta.md) 控制 R2b 真实案例的选择、用途范围和授权；Root [D-008](../GOAL-001-world-model-method-and-tools/01-decision/D-008-hold-case-as-blackbox-probe.md) / [E-016](../GOAL-001-world-model-method-and-tools/02-execution/E-016-r1-procedure-blackbox-probe.md) 只覆盖 R1 草案程序探针，不能推定为 R2b/R4 授权。
- [Root I-005](../GOAL-001-world-model-method-and-tools/00-meta.md) 控制 R2c 证据选路及 R2d 放行；`insufficient` 阻断 R2d。
- Root I-006 只控制 R3 的工具化分支，不阻断 R2。

R2a 的具体测试单元与逐次预登记字段由本目标的决策/附件承载。任何需要改变冻结范围、授权、证据规则或预算的情况，暂停受影响部分并回到 Root 用户裁决流程。

## R2d 完整方法黑箱探针边界

用户于 2026-10-01 提供准确问题“世界有多大”，选择完整方法黑箱路径，要求不围绕该题设计或定制方法、工具（[D-002](01-decision/D-002-reserve-r2d-full-method-blackbox-probe.md)，Root D-020）。本题预留为 R2d 内部的单次完整流程核对：先以先行 H 证据完成 R2c 选路并满足 Root I-005，再形成并冻结通用方法工作版及通用判据，之后才输入本题。

本题不用于 R2a–R2c 的方法设计、操作化或选路，不自动作为 H1/H2/H3 证据、I-005 替代或 R4 最终版案例。流程允许澄清或信息不足；运行前须另行登记有限的人工作业预算/截止点及通用终止条件，当前具体预算和截止点未定，达到任一停点即记录并停止。不预设必须给出数值，不为通过本题临时补造或调参。若实际承担 H 可行性评价，计入 R1 对应 H 额度及累计 9 格 / 180 人分钟上限，不借 R2d/R4 绕限额。

Root I-002 仍 open，本次选择未证明 R2b/R4 用例门禁或下游 I-001/I-011 对应关系；R4 复用须另行复核最终版适配性与授权。Root D-008 的旧修真问题来源与授权不沿用。当前通用方法版、通用判据及探针运行均未完成，本段不推进阶段或增加已完成检查点。

## 父目标与愿景对齐

父目标：[GOAL-001-world-model-method-and-tools](../GOAL-001-world-model-method-and-tools/00-meta.md)。本目标通过父目标挂接 `VP-003-world-model-method-and-tools`，再对齐现行 Charter `method-engineering@0.1.0`；不修改愿景边界或 VP 判据。

## 台账布局

本目标包含 `01-decision/`、`02-execution/`、`03-audit/`、`attachments/`。信息门禁主表与项目整体路线仍由父目标维护；本目标记录 R2 执行决策、事实及审计意见。
