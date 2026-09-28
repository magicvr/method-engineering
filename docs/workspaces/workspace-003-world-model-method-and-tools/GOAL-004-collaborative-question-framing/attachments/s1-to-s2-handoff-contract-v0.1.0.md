---
title: S1→S2 交接合同候选
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-004-collaborative-question-framing
version: 0.1.0
acceptance: bilateral-interface-review-passed
cross_gate_disposition: pending-external-cross-review
---

# S1→S2 交接合同候选 v0.1.0

> 本文是供 S1 与现有 S2 接口复审的最小自然语言合同候选，尚未冻结。它用文字说明交接范围并链接既有记录；不另建拆解方法或 machine schema，不改写规则 E/F/G、共享 schema 或方法版本。

## 1. 交接层级与范围

- **整体交接**：创作者已确认所声明范围内的完整阶段一结构，且该范围的交接材料满足下节要求后，才可将该范围交给 S2。节点就绪不能替代父层或整体现阶段一确认。
- **节点级交接**：只交付明确列出的节点及其局部范围；S1 必须引用当前已接受且明确允许该范围的 S1 方法／host 规则，并附该范围的覆盖收束证据。它只表示局部范围就绪，不推导整体确认、全局 coverage 完成或其他节点就绪。自然语言交接包须附范围、父子关系、确认记录和实际 S1 修订链接。若当前 S1 版本没有局部覆盖／递归门禁依据，不得仅凭本合同启动节点级 S2；须等父层整体确认，或以后按授权更新 S1 方法。
- 当前案例中，①-b 已获局部粒度确认，但父层与①-a仍待确认；因此目前不得实际移交整体，也不得单独移交 B3-b-01。[D-036](../01-decision/D-036-accept-local-b-granularity.md) [E-051](../02-execution/E-051-local-b-granularity-confirmed.md) [阶段一呈示 03](case-structure-presentation-03.md)
- [D-017](../../GOAL-005-shared-research-loop/01-decision/D-017-run02-local-candidates-accepted.md) 只接受 run-02 的两个局部 B3 候选及其 F.2/F.3 完整性；它不确认全局 coverage / closure，也未授权 S2 调用。

## 2. 范围内的最低交接内容

交接采用自然语言说明并链接既有记录。所声明范围内须能核对：

- 哪些问题节点已确认、由谁／哪条记录确认、确认覆盖到哪一层；实际采用的 S1 方法与 host 修订，以及整体或节点级范围。
- 每个未决项的类别、owner 和下一状态：**B1 已裁定，B2 已收敛，B3 已转写为 F.2 求解项**。每个 B3 求解项须包含 F.2 的四项：所求；答案形式与精度；有依据的分支影响（未知时写“分支待阶段二发现”）；来源及 S1 不能回答的原因。不得遗留归属或状态悬空项。
- S2 接收这些已明确的客观问题并承担其模型任务；**B1 不交给 S2 补定界或替代裁决，未完成的 B2 不得改称模型缺口或转交 S2**。问题定界责任仍属 S1。
- B3 只授权 S2 按冻结的 W2 v0.4 顺序检查**已有裁决能力、状态、模型组合、精度与机制缺口**，再依 W2 处理当前实际存在的缺口；交接本身不预先判定必须新建机制模型。F.2 仍要求说明答案形式与所求精度，但 S1 无须交付目标状态值、完整参数表、既有机制、已证明的机制缺口或客观可实现精度的结论；这些不是启动 W2 对明确客观问题进行检查的通用输入门槛。**客观可实现精度属于 B3／S2 求解范围**；只有创作者在当前输入中实际提出精度、容差或答案边界要求时才另立 B1，S1／S2 不得自行制造此类要求。
- 对范围外仍开放的事项，注明 owner、依赖／对本交付范围的影响、为何当前不阻断及回流 trigger；若可能改变本范围的问题边界或求解职责，则受影响范围一并 hold。
- 按所引用 S1 修订的规则 G 判断交接范围是否足以启动该范围的 S2 工作；最新结构变化后完成相应收束攻击，并登记 residual 的范围、为何不阻断及回流 trigger。此处不要求证明全局穷尽；局部展开不会自动重开全局 coverage。

## 3. 局部展开、未完成节点与回流

- 若创作者选择继续展开某节点，该节点仍由 S1 持有，**不得作为可执行 S2 求解项移交**；可随包作为明确标注的 `S1-held context`。此类未完成节点不等同于 Rule G 中已判断为当前交接范围不阻断、并登记范围／理由／触发条件的 `non-blocking residual`；两者须分开登记，不能相互替代。只有当前已接受的 S1 方法／host 规则明确允许拆分该范围，且该节点不影响其他已 ready 节点时，其他节点才可单独作节点级交接；否则 hold 受影响范围。节点深度可以不同。
- v0.17.0 的 semantic zoom 尚未接受；本合同对未完成节点的 hold/context 约定，不将其局部 Rule G 收束自动写入冻结的 v0.16.1 或已接受的 v0.16.2 host。局部展开本身不重开全局 coverage；若产生父级结构变化，按**当前适用且已接受**的 S1 规则检查受影响父级，不把局部结论自动推广到父级。若该版本没有相应的局部覆盖／递归门禁依据，依上一节停止节点级交接，不能以本合同替代该依据。
- 以上仅定义输入、范围与回流接口；不授权改变现行 S1 门禁。以后如需改变门禁，须另行按授权更新并接受 S1 方法／host。
- 若交接后出现会改变已交范围的问题边界、B1/B2 归属或 S2 职责的证据，暂停受影响范围并按所引用 S1 规则回流；其余不受影响且已确认的范围可保持原状态。范围或依赖影响不能判清时，先 hold，不由 S2 代作 S1 定界。

## 4. 研究依据与目标事实

外部研究材料可支持候选相关性、一般机制或调查办法。它们的引用本身不证明目标对象事实；目标事实须有针对该目标对象的证据，并由 S2 核对适用性后才能作为模型／状态依据。S2 仍按现有 W2 方法判断机制、状态参数、精度、范围与边界。

只有 S2 **另行发起外部研究调用**时，才补齐 [S2 research adapter v0.1.0 §2](../../GOAL-005-shared-research-loop/attachments/s2-research-adapter-v0.1.0.md) 的研究问题、模型候选与缺口、目标边界、未知归属、用途标准及单位／定义／范围／观测条件等调用上下文。这些字段不是一般 S1→S2 handoff 或所有 S2 建模任务的额外先决条件。本合同不改共享 schema，也不引入 `evidence_role` 字段。

## 5. 双边复审结果与停止路径

当前状态为 **draft / bilateral-interface-review-passed / pending-external-cross-review**。S1-side Codex Reviewer side review 为 **PASS**（原 MINOR 已闭合），S2-side Codex Reviewer side review 为 **PASS**；两者 scope 仅为交接接口候选兼容性，不能替代 formal cross review。创作者按 [D-040](../01-decision/D-040-handoff-contract-wait-external-cross-review.md) 选择等待外部 independent provider 对同一合同版本复审；[E-059](../02-execution/E-059-record-cross-gate-disposition.md) 记录执行状态。正式审查意见尚未产生；外部审查完成并按意见响应前，本候选不冻结。双边复审不接受 S1/S2 方法版本、不确认案例结构，也不授权启动试跑或 S2 求解。

- **双边接口复审通过**：S1 与 S2 接口责任方均同意同一修订及其范围；记录双方、版本与适用范围。该结果只确认接口候选兼容性；依 [D-040](../01-decision/D-040-handoff-contract-wait-external-cross-review.md)，外部 formal cross review 完成并响应前，合同保持 draft、不冻结。具体交接仍须逐项满足其范围门禁。
- **拒绝**：任一方指出责任错置、输入不足或边界不兼容；记录问题及受影响范围，停止该范围交接，修订本候选后重新双边复审。不得藉此改写源方法或案例裁决。
- **暂缓**：确认范围、必要确认、依赖影响或接口事实尚未确定；记录待决事项、owner 与复核 trigger，停止受影响范围的实际交接，待明确后再审。
- 任一门禁未满足、范围间的影响不清或双方结果不一致时，停止受影响范围；不将沉默、局部 ready 或引用研究材料解释为通过。

## 依据

- S1：[run-10 冻结试跑基线 v0.16.1](stage1-framing-method-candidate-v0.16.1.md)；[已接受的 research-loop host v0.16.2](stage1-framing-method-candidate-v0.16.2.md) 仅确认 host 身份；[v0.16.3](stage1-framing-method-candidate-v0.16.3.md) 是 run-02 配套候选，不是一般已接受版本；[v0.17.0](stage1-framing-method-candidate-v0.17.0.md) semantic zoom 仍为 draft / unaccepted。
- S2：[W2 方法 v0.4](../../GOAL-002-r2-method-working-version/attachments/world-model-method-working-version-v0.4.md) 描述从明确的客观问题进入现有模型构建与验证。
- S2 外部研究补充：[S2 research adapter v0.1.0](../../GOAL-005-shared-research-loop/attachments/s2-research-adapter-v0.1.0.md)；其字段仅适用于外部研究调用。
