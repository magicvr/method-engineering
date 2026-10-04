---
id: GOAL-001-world-model-method-and-tools
title: 为消费方构建并交付世界模型的方法与工具
status: active
parent: null
created: 2026-09-26
updated: 2026-10-04
version: 0.39.7
progress: 60%
plan_refs: VP-003-world-model-method-and-tools
primary_plan: VP-003-world-model-method-and-tools
---

# GOAL-001 · 为消费方构建并交付世界模型的方法与工具

## 概述

承接真实消费需求 `WRK-002-world-model-method-and-tools`：为下游 `WorldModel.ModernCultivation` 构建并交付「世界模型构建方法工作版 + 配套工具」，在至少一个真实世界问题上有界检验，并按 [`protocols/consumer-response-protocol.md`](../../../../protocols/consumer-response-protocol.md) v1.0.0 完成交付、实际收件、验收或异议迭代与结束回路。本目标是 VP-003 的实现承载：VP 给方向级意图与退出判据，本目标给可执行纲领阶段、信息门禁与证据。

## 成功标准

对齐 VP-003 v0.1.1（意图/方向判据未改）。本轮未完成后续交付。

- [x] R1：冻结需求与治理基线，历史成果沿用；仅证明协议冻结，不证明旧 H 或理论适用。
- [x] R2-PA：成熟理论调查、要素抽取、需求/旧假设映射、缺口判定与吸收选路可追溯；PA1～PA5 完成，受限 R2-W 路线已冻结。
- [x] R2-W：按选路形成版本化方法工作版，覆盖 §10/§13、两项可手填结构与内部核对；适用条件、证据范围、限制、未决与后续责任可核对。
- [ ] R3：根据人工过程/既有实践落实工具或本轮 no-tool 分支。
- [ ] R4：最终有界检验、交付、实际收件、验收/异议迭代、反馈路由与结束各有证据。
- [ ] 各阶段到期 required 信息项与必改 finding 合法满足；交付独立审计满足。不以 progress 放行。

修改前成功标准、路线、假设与门禁全文见 [历史基线](attachments/pre-reframe-root-baseline-v1.md)，本次决定见 [D-021](01-decision/D-021-prior-art-driven-implementation-reframe.md)。
## 愿景对齐

- `plan_refs` / `primary_plan`：`VP-003-world-model-method-and-tools`（[docs/vision/plans/VP-003-world-model-method-and-tools.md](../../../vision/plans/VP-003-world-model-method-and-tools.md)），其 `vision_ref: method-engineering@0.1.0` 与现行 Charter 精确一致。
- `serves_summary`：服务于 Charter 方向级成功边界 1（从真实、具体、有边界的问题出发形成可被使用、检验和改进的方法）与 3（区分对象问题、方法问题与框架问题）。本目标不替下游编写设定正文或 canon，不承诺方法普遍有效，也不承诺工具被下游启用。

## 纲领路线图（P-001）

这是 Root 的实现路线；R2-PA/R2-W 是 VP R2 方法形成方向的细化，不改 VP 方向结构。

| 阶段 | 名称 | 状态 | 退出条件 |
|---|---|---|---|
| R1 | 已冻结需求与治理基线 | 已完成 | D-017/E-032/A-004 及 D-018/E-033/E-034/A-005 证明协议冻结与同步；历史成果沿用，不证明 H 假设或理论适用。 |
| R2-PA | 成熟理论吸收与选路 | 已完成 | [后继目标](../GOAL-003-prior-art-replanning/00-meta.md) 的 PA1～PA5 已完成并经用户确认关门；受限 R2-W 路线与交接包已冻结。I-007/I-008/I-010 为 accepted-residual（非 verified），I-009 verified（限定映射覆盖与处置依据）。 |
| R2-W | 方法工作版形成与内部核对 | 已完成 | GOAL-009 已形成版本化方法并覆盖 §10/§13；A-002 F-01 与 A-004-F-001 均已 fixed，A-003/A-005 independent pass，无开放 required；用户确认关门。 |
| R3 | 工具分支评估与落实 | 进行中（S1～S4 已完成，待用户确认 Root checkpoint） | GOAL-010 no-tool 分支与 no-tool 记录已完成；A-001 F-001 经 A-002/A-003 fixed 闭合，无开放 required；I-006 保持 accepted-residual（非 verified）。 |
| R4 | 最终有界检验、交付与验收 | 未开始 | I-002 最终用例及授权就绪，I-004 独立审计模式/provider 及所需意见满足；最终版端到端有界检验、交付、实际收件、验收/异议迭代、反馈路由与运行主记录终态分别留证。 |

先后为 R1→R2-PA→R2-W→R4；R3 可并行评估，工具实现等接口稳定，R2-W/R3 同时就绪才进入 R4。

沿用 R1 v0.6.4 的需求边界、创作者主责与 AI 可选协助、输入来源/版本/用途/权限核对、观察/推断/假设/建议/裁定分离、可手填结构与逐项映射退出契约、条件工具策略及停止/变更机制。R1 完成只证明协议冻结，不证明 H1/H2/H3 或任何理论适用。原 9 格/180 人分钟仅约束旧 H 可行性工作，不自动挪作 prior-art 调查额度；新增执行授权/预算由 I-007 核对，不自动扩容。

只有缺口对应必要需求、调查边界和替代检查有记录、区分“尚未查明”与“已发现适用限制”、继承/有限改造不足、原创范围和停止条件明确、相关信息/审计/授权门禁满足时，才可进入原创探索。禁止把“没搜到”写成“理论不存在”。

### 旧 R2 路线历史入口

[旧基线](attachments/pre-reframe-root-baseline-v1.md) 保留 H1/H2/H3 原文、R2a～R2d、成功标准及旧门禁；[旧目标](../GOAL-002-r2-method-validation/00-meta.md) cancelled + terminated-by-reframe，0/4，承接 [新目标](../GOAL-003-prior-art-replanning/00-meta.md)。I-005 的最后事实状态保持 open，旧 R2c/R2d 门禁撤回当前执行范围、编号不复用；H3-SEM-001 仍 required/open，H3 冻结/运行继续禁止。这不是 finding fixed/residual/overruled；只退出旧路线。新路线不要求先补完旧预登记；未来复用任何旧实验须重新检查旧门禁、剩余额度、角色隔离及授权。

以下 R1 沿革保留历史语境，出现旧 R2 阶段时不作为现行路线授权。

### R1 草案准备与关门沿革（2026-09-30）

历史准备：v0.6.1 草案与首次范围选择见 E-004 / D-004 / E-009；H1/H2/H3 的观察项、声明范围判充分、共享背景分立单元、小型上限及证据清单 + 创作者局部裁决路径见 D-005～D-007 / D-010 / D-011。D-009 选独立 Codex 首发 Skill；D-014 选创作者主责、AI 可选协助。黑箱探针见 D-008 / E-016，排除在方法规划与领域证据之外，不选定 R2b/R4 案例。上述用户选择按授权继承，不重复询问同一方向。

先前 v0.6.2 的选择/首次绑定见 D-012 / E-025；该版本最后的下游指针为 WorldModel.ModernCultivation@f24f83c7150499bef1a103bc99ccdbf712fbde53，引用上游 magicvr/method-engineering@0340ee94cd07c4da2ce0f3164ddb56bb9e5fc082（E-028），均保留为历史。当时 v0.6.3 精确引用为 magicvr/method-engineering@90e8a2114f9d3ddfbb916d5bd02e3dd66b49b160:docs/workspaces/workspace-003-world-model-method-and-tools/GOAL-001-world-model-method-and-tools/attachments/R1-freeze-proposal-v0.6.3.md，由下游 WorldModel.ModernCultivation@250a632cb666540a25931034a0274b10f51b1136（下游 E-012）同步，本仓以 E-030 记录。当前 v0.6.4 来源和下游同步见 D-018 / E-033。

**阶段修正沿革**：用户选择方案 A 响应 A-002，决定见 [D-015](01-decision/D-015-respond-a002-stage-gates.md)，实施见 [E-029](02-execution/E-029-respond-a002-stage-gates.md)。v0.6.3 [历史提案](attachments/R1-freeze-proposal-v0.6.3.md)及[未决清单](attachments/R1-open-items-decision-brief-v0.6.3.md)按 R1/R2a/R3 分配门禁。I-001 只卡 R1 协议级边界，逐次字段在 R2a；I-003 只卡 R1 条件策略，R3 的 I-006 评估价值并落实分支。两仓是同一维护人，上游一次实质裁决、下游同步引用，取消共同维护组再次确认/签字门禁。

此后 v0.6.4 由 D-017/E-032 冻结、A-004 独立审阅通过，下游 E-013 于 `WorldModel.ModernCultivation@2985080414ca57acda3ee19f3a592efef9676fa3` 精确同步（本仓 E-033）。D-018/E-034/A-005 完成 R1 关门；I-001/I-003 verified，R1 检查点完成。A-002 的四项 required findings 已由 A-003 以 `fixed` 闭合。v0.6.3 与历史意见不改写。R2/R3/R4 未开始，无真实 H 试验、工作版、工具实现或交付；无需新建子目标。


## 派生进度展示

五个等权纲领检查点中 R1/R2-PA/R2-W 完成，progress: 60%（3/5）。分母从旧 1/4 调整为 1/5，不代表撤销 R1 或新增失败；PA1～PA5 不额外计入 Root 分母。progress 不放行、不闭合 finding、不覆盖门禁、不推导 done。
## 信息就绪与未知项

本表为唯一权威；后继目标只引用编号与证据，不复制状态。I-001/I-003 的 verified 仅是协议结论；已授权文档盘点可先启动，后续调查/选路/原创仍按最晚阶段核对。不得自动把新路线授权扩大为试验或付费授权。

| ID | 级别 | 所需信息 / 问题 | 影响门禁 | 最晚需要阶段 | 验证 / 收集动作 | 状态 | 延期 / 复核 | 证据 / 结论 |
|---|---|---|---|---|---|---|---|---|
| I-001 | required | 已冻结需求、用途/退出契约、输入授权规则、证据类型、总体限额、停止/变更与责任 | R1 退出；现行路线约束迁移 | R1 已完成；新增执行前由 I-007 复核适用性 | 沿用冻结协议；区分通用约束与旧 H 专属额度 | verified | 非延期；责任人：方法工程响应负责人；超出旧授权触发 I-007，不撤销 R1 | [v0.6.4](attachments/R1-freeze-proposal-v0.6.4.md)、D-017/E-032/A-004、D-018/E-033/E-034/A-005；仅证明协议冻结与同步 |
| I-002 | required | 最终真实世界问题、用途范围、授权及最终版适配；任何现行路线真实案例使用也需核对 | 任何真实案例使用；R4 检验 | 使用真实案例前；R4 前复核 | 同一维护人书面选定案例/用途/授权；核对最终版适配并留痕 | open | 非延期；责任人：同一维护人；尚未授权不得使用 | [D-020](01-decision/D-020-reserve-r2d-full-method-blackbox-probe.md)/[E-036](02-execution/E-036-record-r2d-full-method-probe-decision.md) 的“世界有多大”仍只是预留，未运行；旧 R2c/R2d 前置属历史，现行须待 PA5/R2-W 通用工作版与通用判据就绪并复核授权；不得围绕本题定制；未选为 R4 用例 |
| I-003 | required | 条件工具策略：最小职责/权限、触发时点、责任与支持/不足两分支 | R1 退出；R3 策略依据 | R1 已完成 | 沿用 D-009、v0.6.4 §5；现行人工过程价值由 I-006 核对 | verified | 非延期；策略沿用，不要求先实现或安装 Skill | D-009/E-018、D-017/E-032/A-004、D-018/E-033/E-034/A-005；不证明工具化价值 |
| I-004 | required | R4 高影响交付门禁的独立审计模式与 provider | R4 交付放行 | R4 交付前 | 用户指定 provider，取得覆盖交付范围的可核对独立意见并处理必改项 | open | 非延期；责任人：用户；无 provider/输出不得静默降级 | 待确定；本轮 self 不替代 |
| I-006 | required | 依据现行方法路线人工过程/既有实践，是否值得工具化及如何落实：重复步骤、人工成本、收益、维护负担 | R3 分支决定与退出 | R3 退出前 | 收集现行人工过程或既有实践证据，作支持/不足或不成立分支决定；稳定接口后落实 Skill，或 no-tool 理由、责任与复评触发 | accepted-residual（非 verified） | 责任人：同一维护人；用户 2026-10-04 按 GOAL-010 D-001 接受：仅允许 GOAL-010 S2～S4 分支冻结/R3 退出，不解除 I-002/I-004、真实案例、工具实现/安装、下游写入、外部模型、自动验证或 R4 交付；复评触发：获得任务级成本/重复/遗漏证据、需求或步骤实质变化、有依据的工具候选、R4 方案冻结前 | [D-001](../GOAL-010-r3-tool-branch-evaluation/01-decision/D-001-r3-branch-decision-proposal.md)、[E-003](../GOAL-010-r3-tool-branch-evaluation/02-execution/E-003-accept-i006-residual.md)：证据不足下 no-tool；未知仍为非 verified |
| I-007 | required | R1 通用约束、旧 H 专属额度及现行调查边界/来源方法/资源/执行授权如何迁移 | PA1 基线与来源方案；超出既有授权的新执行 | PA1 退出；任何超出已授权有界公开来源识别的新执行前 | 逐条盘点 R1、固定需求来源与调查边界，列可沿用/专属/需新裁决；新增费用/执行/预算须用户书面裁决 | accepted-residual（非 verified） | 责任人：方法工程响应负责人；残余范围仅限 GOAL-003 的 PA2/PA3 内部阅读/引用；外部交付前、出版方异议、获得正式许可或改用开放来源时复审；超出 6 人时、0 费用上限、来源/范围/策略变化时重新裁决 | [约束迁移矩阵](../GOAL-004-pa1-baseline-and-source-plan/attachments/constraint-migration-matrix-v0.1.md)、[来源/访问方案](../GOAL-004-pa1-baseline-and-source-plan/attachments/source-and-access-plan-v0.1.md)、[D-003](../GOAL-004-pa1-baseline-and-source-plan/01-decision/D-003-record-user-source-access-and-resource-decisions.md)：用户 2026-10-04 接受 J-01 A、J-02 A 残余、J-03 A（1 核心+至多 2 支撑/类；6 人时；费用 0）；公开托管副本权限未核实但按明确范围/复审接受，不写成 verified |
| I-008 | required | 理论来源真实性/版本/原文定位及要素抽取对已界定调查范围是否充分 | PA2 抽取；PA3 比较输入 | PA2 退出；PA3 比较前 | 核实候选原始来源、版次与定位，保留可核对原文/解释边界，记录覆盖、反向/替代来源检查与不足 | accepted-residual（非 verified） | 责任人：方法工程响应负责人；S04-C 全文未取得，用户 2026-10-04 按 GOAL-005 D-002 接受有界残余；PA3/PA4 只以 S04-D 为 SD 方法定义核心，S04-C 摘要仅背景；冲突、需要 SD 历史/领域回顾、获得合法全文或外部交付前复审 | [访问台账](../GOAL-005-pa2-theory-element-extraction/attachments/source-access-ledger-v0.1.md)、[理论要素](../GOAL-005-pa2-theory-element-extraction/attachments/theory-elements-v0.1.md)、[覆盖/未决](../GOAL-005-pa2-theory-element-extraction/attachments/coverage-and-unresolved-v0.1.md)、[D-002](../GOAL-005-pa2-theory-element-extraction/01-decision/D-002-accept-s04c-fulltext-residual.md)：S01/S02/S03/S04-D/S05 已系统抽取 37 项；S04-C 保持 unresolved，不以摘要冒充全文 |
| I-009 | required | 理论要素/局部主张与需求 §10/§13、旧 H 假设的映射及适用性依据 | PA3 四类处置；PA4 吸收输入 | PA3 退出 | 逐项核对条件、目标/输入/输出、差异、证据等级、反例与适用限制，记录 inherit/adapt/not-applicable/unresolved | verified | 验证对象仅限“映射覆盖与处置依据已核对”；关键 unresolved 仍是 PA4 输入，未解决/未接受为残余；证据冲突暂停受影响选路并请用户裁决 | [PA3 映射矩阵](../GOAL-006-pa3-requirement-mapping/attachments/mapping-matrix-v0.1.md)、[关键未决](../GOAL-006-pa3-requirement-mapping/attachments/unresolved-and-decision-points-v0.1.md)、[A-002](../GOAL-006-pa3-requirement-mapping/03-audit/A-002-independent-pa3-exit-audit.md)：15 需求项与 H1/H2/H3 局部主张已映射；未用 inherit |
| I-010 | required | 缺口是否对应必要需求，调查边界/替代检查、继承/有限改造不足及后续选路依据是否充分 | PA5 路线冻结；R2-PA 退出；R2-W 进入；任何原创启动 | PA5 退出前；进入 R2-W/原创前 | 分清尚未查明与已发现适用限制，建立缺口/处置证据链、吸收方案、有限原创范围/停止条件及授权/审计核对 | accepted-residual（非 verified） | 责任人：方法工程响应负责人；五类未决仍未解决，用户按 GOAL-007 D-002 接受为 PA5 必带输入；按 GOAL-008 D-003 允许受限 PA5 路线冻结；不承诺六项 uncertain 已解决；新增来源/实验/费用、真实案例、外部交付或扩大承诺前复核 | [PA4 缺口/吸收](../GOAL-007-pa4-gap-and-absorption/attachments/gap-and-absorption-register-v0.1.md)、[用户裁决点/原创闸门](../GOAL-007-pa4-gap-and-absorption/attachments/user-decisions-and-original-gates-v0.1.md)、[D-002](../GOAL-007-pa4-gap-and-absorption/01-decision/D-002-accept-i010-residual.md)：五类未决未被升级为缺口；无原创授权 |

### 历史信息项（编号不复用）

| ID | 级别 | 所需信息 / 问题 | 原门禁 / 最晚阶段 | 收集动作 | 最后事实状态 | 当前处理 / 复核 | 证据 / 结论 |
|---|---|---|---|---|---|---|---|
| I-005 | required | H1/H2/H3 在旧冻结范围内是否足以支持方法选路，哪些有证据/需替代/不足 | 旧 R2c 选路前、旧 R2d 形成前 | 旧预登记下有界试验与四标签证据选路 | open | 旧 R2c/R2d 撤回当前执行范围，不是 verified 或 finding 闭合；未来复用旧路线前由响应负责人复核旧门禁 | [旧基线](attachments/pre-reframe-root-baseline-v1.md)、[D-021](01-decision/D-021-prior-art-driven-implementation-reframe.md)；无试验/有效性证据，H3-SEM-001 required/open 仍阻断 H3 冻结/运行 |

**门禁现状（2026-10-04）**：I-001/I-003 verified；I-007/I-008 为 `accepted-residual`（权限/全文未知部分经用户明确接受，非 verified）；I-009 verified（限定映射覆盖与处置依据）；I-010 accepted-residual（非 verified；按 GOAL-008 D-003 允许受限 PA5 路线冻结）；I-002/I-004 open；I-006 accepted-residual（非 verified，仅限 GOAL-010 S2～S4/R3 退出）；历史 I-005 最后状态 open。旧 H3 门禁隔离且不闭合；PA1～PA5 已完成并经用户确认关门，R2-PA/R2-W 完成。R3 进入下一阶段，R4 未启动。本轮不改变运行记录或下游状态。

## 父目标

`null`

## 台账布局

`01-decision/`、`02-execution/`、`03-audit/` 为可追加台账。索引文件只保留 frontmatter、摘要和条目索引；独立记录使用 `D-NNN-*`、`E-NNN-*`、`A-NNN-*` 文件。

## 备注

本轮 self 仅审历史保全、合法状态、门禁隔离与愿景对齐，见 [A-006](03-audit/A-006-review-implementation-reframe.md)。R1 A-002 的四项 required 已由 A-003 fixed，A-004/A-005 历史结论不替代 R4 I-004；旧 H3-SEM-001 保持 required/open。运行状态唯一来源仍是 [runtime record](../../../../runtime-records/WRK-002-world-model-method-and-tools/record.md)，本轮未修改。修改前备注亦保存在历史基线。
