---
id: GOAL-002-r2-method-validation
doc: decision
status: active
parent: GOAL-001-world-model-method-and-tools
created: 2026-10-01
updated: 2026-10-01
version: 0.1.21
---

# 决策记录 · GOAL-002

## 阶段计划索引

| 阶段 | 计划文件 / 落点 | 说明 |
|------|-----------------|------|
| R2a–R2d | [00-meta.md](00-meta.md)；R2a 准备稿见 [附件](attachments/R2a-operationization-plan-v0.1.md) | 先完成具体预登记，再按适用授权运行；I-005 证据选路及 R2d 放行仍由父目标权威信息项控制。 |
| R2a 预登记基线 | [D-003](01-decision/D-003-select-synthetic-package-preregistration-baseline.md)；[合成候选包](attachments/R2a-H123-synthetic-candidate-pack-v0.1.md) | 用户已接受供水站合成包的基线结构；准确输入、局部判据/严重度、责任、预算/停点、冻结及运行授权仍待逐项完成。 |
| R2a H3 路线 | [D-004](01-decision/D-004-select-h3-form-first-model-set-from-zero.md) | 已选从零形成实际首版模型并在参考揭示前冻结产物；两条初评组合已依 D-013 选择，最低启动/映射规则依 D-015 已定，C-03 两条链适用性候选依 D-016 已选；准确输入、其余矩阵单元、剩余判据及执行安排待补，H3-SEM-001 仍 OPEN。 |
| R2a H3 产物与判定基础 | [D-005](01-decision/D-005-define-h3-text-model-and-checklist-basis.md) | 最低产物类型为可审查纯文本机制模型条目；分析手段按证据需要选择；依 D-007～D-016 已确定核心能力、标签优先级、最低启动能力、C-03 两链候选适用性及映射/遗漏规则。 |
| R2a H3 条目字段 | [D-006](01-decision/D-006-accept-r1-model-entry-fields-for-h3.md) | 接受冻结 R1 §2 的 12 类信息均为可审查纯文本条目的最低内容；能力覆盖与跨链聚合仍待裁定。 |
| R2a H3 核心能力与标签边界 | [D-007](01-decision/D-007-set-h3-core-capability-boundaries.md) | C-02～C-04 为核心能力，C-01 为输入/范围前提；核心缺项 partial、核心矛盾或错述 C-01 refuted、无法可靠评估 insufficient；集合级细则见 D-008～D-011。 |
| R2a H3 跨链汇总单位 | [D-008](01-decision/D-008-aggregate-h3-at-model-set-level.md) | 最终标签针对所选链共同形成的冻结模型集合；逐链映射保留，单链未触及不自动判失败；中间 `explicit-gap` 得到最终集合补足时不自动降级（D-009）。 |
| R2a H3 未触及证据聚合 | [D-009](01-decision/D-009-aggregate-explicit-gaps-at-final-set.md) | 最终集合已覆盖核心能力时，单链的明确缺口不自动阻断 supported；全链未触及且整体不能可靠判断时为 insufficient（D-010）。 |
| R2a H3 全链未触及 | [D-010](01-decision/D-010-label-unassessable-core-as-insufficient.md) | 全部适用链未触及核心能力且集合无可评证据、整体无法可靠判断则为 insufficient；不据无证据推断能力缺失或成功；混合情形见 D-011。 |
| R2a H3 混合证据汇总 | [D-011](01-decision/D-011-prioritize-insufficient-over-partial.md) | 任一核心能力不可评且影响总体判断时优先 insufficient；partial 仅用于核心均可评但最终集合仍缺项；可核对的核心矛盾仍为 refuted。 |
| R2a H3 逐链适用性 | [D-012](01-decision/D-012-preregister-h3-chain-applicability.md) | 运行前按冻结输入分别登记链×能力适用性及理由，运行后另记实际证据状态；不能事后改适用性。C-03 两条初评链均适用的候选单元依 D-016 已选，完整矩阵与准确输入仍待完成。 |
| R2a H3 初评组合 | [D-013](01-decision/D-013-select-h3-two-initial-chains.md) | 选择值班操作员×CTX-017 与检修员×CTX-042 两条初评链，共 2 个 H3 格；未冻结准确输入，也未授权运行。 |
| R2a H3-01 上限输入 | [D-014](01-decision/D-014-add-h3-cap-binding-input.md) | 选择 H3-01 第一步需求 5、实际供水 4；水位候选记录据此保持一致。当时为待审定片段；数值现依 D-018 纳入候选设计基线，未冻结。 |
| R2a H3 最低启动能力 | [D-015](01-decision/D-015-set-h3-minimum-model-startability.md) | 集合至少一个非占位条目、每个模型条目 12 类字段可定位，且至少一条证据可追溯的具体机制关系；不要求全部核心已覆盖。映射规则与关键遗漏规则已确定；逐链矩阵及实际证据链接仍待完成。 |
| R2a H3 可观测输入候选基线 | [D-017](01-decision/D-017-prepare-h3-observable-boundary-input.md)；[D-018](01-decision/D-018-accept-h3-observable-input-candidate-baseline.md) | 全套精确步内读数、连续水量、0.5 单位报告刻度/无误差舍入及评估端均匀时间分布已接受为后续预登记候选；时间扩展版本 H3-BALANCE@0.2 未冻结，旧 @0.1 历史保留。完整可评性/矩阵与运行字段待核对，不授权冻结/运行。 |
| R2d 内部核对 | [D-002](01-decision/D-002-reserve-r2d-full-method-blackbox-probe.md) | “世界有多大”只在 I-005 满足、通用方法版与通用判据冻结后单次输入；不用于前置设计或选路。尚未运行。 |

## 信息需求与阶段门禁

父目标 [GOAL-001](../GOAL-001-world-model-method-and-tools/00-meta.md) 的 I-002、I-005、I-006 是本目标对应门禁的唯一状态来源。本目标不复制其状态：I-002 适用于真实案例运行前；I-005 适用于 R2c 选路与 R2d；I-006 仅适用于 R3。R2a 具体测试问题、模型/样本和局部裁决规则仍待逐项操作化，不代表试验已获准。

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-10-01 | 建立 R2 子目标并界定职责与门禁 | accepted | [D-001](01-decision/D-001-r2-scope-and-gate-authority.md) |
| D-002 | 2026-10-01 | 预留“世界有多大”为完整方法冻结后的黑箱核对 | accepted | [D-002](01-decision/D-002-reserve-r2d-full-method-blackbox-probe.md) |
| D-003 | 2026-10-01 | 选择供水站合成候选包作为正式预登记基线 | accepted | [D-003](01-decision/D-003-select-synthetic-package-preregistration-baseline.md) |
| D-004 | 2026-10-01 | 选择 H3 从零形成首版机制模型集合 | accepted | [D-004](01-decision/D-004-select-h3-form-first-model-set-from-zero.md) |
| D-005 | 2026-10-01 | 确定 H3 文本模型产物与能力清单判定基础 | accepted | [D-005](01-decision/D-005-define-h3-text-model-and-checklist-basis.md) |
| D-006 | 2026-10-01 | 接受 H3 首版模型采用 R1 完整条目字段 | accepted | [D-006](01-decision/D-006-accept-r1-model-entry-fields-for-h3.md) |
| D-007 | 2026-10-01 | 确定 H3 核心能力范围与局部标签边界 | accepted | [D-007](01-decision/D-007-set-h3-core-capability-boundaries.md) |
| D-008 | 2026-10-01 | 确定 H3 按冻结模型集合汇总结果 | accepted | [D-008](01-decision/D-008-aggregate-h3-at-model-set-level.md) |
| D-009 | 2026-10-01 | 确定明确能力缺口以最终冻结集合判定 | accepted | [D-009](01-decision/D-009-aggregate-explicit-gaps-at-final-set.md) |
| D-010 | 2026-10-01 | 将全链未触及且不可评的核心能力判为不足 | accepted | [D-010](01-decision/D-010-label-unassessable-core-as-insufficient.md) |
| D-011 | 2026-10-01 | 确定不可评证据优先于部分缺项 | accepted | [D-011](01-decision/D-011-prioritize-insufficient-over-partial.md) |
| D-012 | 2026-10-01 | 预登记 H3 逐链能力适用性 | accepted | [D-012](01-decision/D-012-preregister-h3-chain-applicability.md) |
| D-013 | 2026-10-01 | 选择 H3 两条初评采样链 | accepted | [D-013](01-decision/D-013-select-h3-two-initial-chains.md) |
| D-014 | 2026-10-01 | 为 H3-01 加入触发供水上限的输入 | accepted | [D-014](01-decision/D-014-add-h3-cap-binding-input.md) |
| D-015 | 2026-10-01 | 设定 H3 最低模型启动能力与遗漏规则 | accepted | [D-015](01-decision/D-015-set-h3-minimum-model-startability.md) |
| D-016 | 2026-10-01 | 设定 H3 两条初评链的 C-03 适用性 | accepted | [D-016](01-decision/D-016-set-h3-c03-chain-applicability.md) |
| D-017 | 2026-10-01 | 选择补足 H3 可观测输入并准备非零存量边界草稿 | accepted（仅准备方向） | [D-017](01-decision/D-017-prepare-h3-observable-boundary-input.md) |
| D-018 | 2026-10-01 | 接受 H3 完整可观测输入草案为后续预登记基线 | accepted（候选设计，未冻结） | [D-018](01-decision/D-018-accept-h3-observable-input-candidate-baseline.md) |
