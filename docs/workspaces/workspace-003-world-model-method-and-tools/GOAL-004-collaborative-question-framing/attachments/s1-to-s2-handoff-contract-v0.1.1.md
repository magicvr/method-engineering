---
title: S1→S2 交接合同
status: frozen
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-004-collaborative-question-framing
version: 0.1.1
acceptance: frozen-by-creator-after-a003-pass
cross_gate_disposition: a003-independent-pass-responded
frozen: true
---

# S1→S2 交接合同 v0.1.1

> 本文是 S1→S2 交接合同 v0.1.1，已由 A-003 完成同 scope independent review（verdict: pass），并由创作者按 D-041 接受后冻结。冻结仅稳定接口合同；不确认案例结构或 S1/S2 方法，不授权实际 S2 integration、trial 或 solving。具体范围只有满足本合同门禁且另获授权，才能实际进入 S2。本文只说明交接接口并链接既有记录；不另建拆解方法或 machine schema，不改写规则 E/F/G、共享 schema 或方法版本。

## 1. 交接层级与范围

- **整体交接**：创作者已确认所声明范围内的完整阶段一结构，且该范围的交接材料满足下节要求后，才可将该已确认范围整体交给 S2。整体确认只开启这一整体交接范围。
- **节点级交接**是独立能力，只能在以下三项同时成立时使用：
  1. 当前已接受的 S1 method／host 明文允许拆分该范围；
  2. 已提供该方法要求的局部 coverage／closure evidence；
  3. 独立交接不会破坏父级或兄弟节点的已确认结构。

  父层确认本身不能替代上述任何局部门禁。S1 v0.16.1 与 v0.16.2 均无已接受的局部递归／节点拆分门禁，因此当前节点级交接路径关闭；不得以父层整体确认作为缺少这些门禁时的替代出口。
- 当前案例中，①-b 已获局部粒度确认，但父层与①-a仍待确认；因此目前不得实际移交整体，也不得单独移交 B3-b-01。[D-036](../01-decision/D-036-accept-local-b-granularity.md) [E-051](../02-execution/E-051-local-b-granularity-confirmed.md) [阶段一呈示 03](case-structure-presentation-03.md)。即便将来父层整体确认，①-b／B3-b-01 也须随整体结构交给 W2；本合同不授权将其单独交给 S2。
- [D-017](../../GOAL-005-shared-research-loop/01-decision/D-017-run02-local-candidates-accepted.md) 只接受 run-02 的两个局部 B3 候选及其 F.2/F.3 完整性；它不确认全局 coverage／closure，也未授权 S2 调用。

## 2. 范围内的最低交接内容

交接采用自然语言说明并链接既有记录。所声明范围内须能核对：

- 哪些问题节点已确认、由谁／哪条记录确认、确认覆盖到哪一层；实际采用的 S1 方法与 host 修订，以及整体交接范围。
- 每个未决项的类别、owner 和下一状态：**B1 已裁定，B2 已收敛，B3 已转写为 F.2 求解项**。每个 B3 求解项须包含 F.2 的四项：所求；答案形态；有依据的分支影响（未知时写“分支待阶段二发现”）；来源及 S1 不能回答的原因。只有创作者当前输入明确提出精度、容差或答案边界要求时，才将该项记录为 B1 约束；不得仅因需要说明答案形态而制造 B1。不得遗留归属或状态悬空项。
- S2 接收这些已明确的客观问题并承担其模型任务；**B1 不交给 S2 补定界或替代裁决，未完成的 B2 不得改称模型缺口或转交 S2**。问题定界责任仍属 S1。
- B3 只授权 S2 按 W2 v0.4 的顺序检查**已有裁决能力、状态、模型组合、客观可实现精度与机制缺口**，再依 W2 处理当前实际存在的缺口；交接本身不预先判定必须新建机制模型。S1 无须交付目标状态值、完整参数表、既有机制、已证明的机制缺口或客观可实现精度的结论；这些不是启动 W2 对明确客观问题进行检查的通用输入门槛。客观可实现精度由 B3／S2 求解。仅当创作者当前输入明确提出精度、容差或答案边界要求时才记录相应 B1 约束；没有明确要求时不制造 B1。
- 对范围外仍开放的事项，注明 owner、依赖／对本交付范围的影响、为何当前不阻断及回流 trigger。trigger 应说明出现何种未来证据后回流，不把未来 trigger 可能发生本身写成当前阻断理由。有证据表明某事项已改变当前交接范围的所求、必要问题结构、未决项归属或下一阶段状态时，hold 受影响范围；是否存在这些影响判不清时先 hold 受影响范围。
- 按规范性基线中所引 S1 修订的规则 G 判断整体交接范围是否足以启动该范围的 S2 工作；最新结构变化后完成相应收束攻击，并登记 residual 的范围、当前为何不阻断及回流 trigger。此处不要求证明全局穷尽；局部展开不会自动重开全局 coverage。

## 3. 局部展开、未完成节点与回流

- 仍由 S1 持有的未完成节点是 **`S1-held context`**，可以作为说明性上下文随材料注明；该未完成节点自身不得作为可执行 S2 求解项。它与已按 Rule G 完整登记范围、当前为何不阻断及回流 trigger 的 **`non-blocking residual`** 分开记录，不能相互替代。标记 `S1-held context` 本身也不给其兄弟节点额外授权；兄弟节点如单独交接，只能依据§1的三项条件独立判定。
- 仅对未来经接受、且明文允许局部拆分范围的 S1 method／host，节点级交接才可能适用；并且必须同时满足：该 method／host 明文允许拆分该范围、已提供该方法要求的局部 coverage／closure evidence、独立交接不会破坏父级或兄弟节点的已确认结构。当前已接受的 S1 v0.16.1 与 v0.16.2 均无此类门禁，因此当前节点级路径关闭。父层整体确认不替代任何局部门禁，也不构成替代出口。
- v0.17.0 的 semantic zoom 尚未接受；本合同对未完成节点的 hold/context 约定，不将其局部 Rule G 收束自动写入冻结的 v0.16.1 或已接受的 v0.16.2 host。局部展开本身不重开全局 coverage；若产生父级结构变化，按**当前适用且已接受**的 S1 规则检查受影响父级，不把局部结论自动推广到父级。以上仅定义输入、范围与回流接口；不授权改变现行 S1 门禁。以后如需改变门禁，须另行按授权更新并接受 S1 方法／host。
- 若有证据表明当前所求、必要问题结构、未决项归属或下一阶段状态已经改变，hold 受影响范围并按所引用 S1 规则回流。若是否存在这些影响判不清，先 hold 受影响范围；不由 S2 代作 S1 定界。已完整登记 Rule G residual（范围、当前为何不阻断、回流 trigger）不得仅因未来 trigger 可能发生而阻断。trigger 描述的是出现何种未来证据后回流；当该证据出现时，再按其实际影响处理受影响范围。其余不受影响且已确认的范围可保持原状态。

## 4. 规范性基线与研究依据

本合同 v0.1.1 固定以下规范性基线身份：

- **S1**：run-10 冻结试跑基线 v0.16.1，[文件](stage1-framing-method-candidate-v0.16.1.md)，SHA-256：`e6c1ef612ceafb64ddb8c26202d84007405723e19d9647025bf17c6be5994c34`。
- **W2**：方法工作版 v0.4，[文件](../../GOAL-002-r2-method-working-version/attachments/world-model-method-working-version-v0.4.md)，SHA-256：`8170a8f5cadb8db58a3282b01d6781efe42a7e835a37ea32bf0f8eaa660a98f6`。

未来更换任一基线版本、所引文件内容变化或发现同名文件漂移时，须进行兼容性复审；不得以相同名称静默改变已固定基线的内容或含义。

以下只作上下文身份记录，不构成本合同的规范性基线或新增一般门槛：已接受的 research-loop host S1 v0.16.2，[文件](stage1-framing-method-candidate-v0.16.2.md)，SHA-256：`cbe94ec732e29050d0a3545c415d8d8674edf1899142c3a62c218861119664ae`。该 host 身份本身不授予 split gate；v0.16.1 与 v0.16.2 均没有已接受的局部递归／节点拆分门禁。

外部研究材料可支持候选相关性、一般机制或调查办法。它们的引用本身不证明目标对象事实；目标事实须有针对该目标对象的证据，并由 S2 核对适用性后才能作为模型／状态依据。S2 仍按 W2 方法判断机制、状态参数、客观可实现精度、范围与边界。

只有 S2 **另行发起外部研究调用**时，才补齐 [S2 research adapter v0.1.0 §2](../../GOAL-005-shared-research-loop/attachments/s2-research-adapter-v0.1.0.md) 的研究问题、模型候选与缺口、目标边界、未知归属、用途标准及单位／定义／范围／观测条件等调用上下文。该 adapter 是外部研究调用的条件性规范来源，SHA-256：`9885685990e54c47d6ee81908a5595bc94de5ccb1ef0342165acd24cead74c69`；这些字段不是一般 S1→S2 handoff 或所有 S2 建模任务的额外先决条件。本合同不改共享 schema，也不引入 `evidence_role` 字段。

## 5. 审查响应、finding 闭合与冻结范围

本合同 v0.1.1 于 2026-09-28 完成同 scope independent review：[A-003](../03-audit/A-003-handoff-contract-v011-closure-review.md) 的 verdict 为 **pass**（auditor：grok-4.7）。创作者按 [D-041](../01-decision/D-041-accept-a003-and-freeze-handoff-contract.md) 接受该意见，并将 v0.1.1 冻结为 S1→S2 接口合同。

[A-002](../03-audit/A-002-s1-s2-handoff-contract-freeze-readiness.md) 对 v0.1.0 的原始 verdict **conditional** 保留为历史审查结论，不予改写。依据 A-003 对修订版的核对，A-002 finding 响应如下：

| Finding | 响应 | 状态 |
|---------|------|------|
| A-002 F-001（required/high） | v0.1.1 §§1/3 明确整体交接与节点级门禁分离，父层确认不替代局部门禁。 | fixed |
| A-002 F-002（required/high） | v0.1.1 §§2/3 将 hold 限于实际影响或影响不明，已登记 residual 不因未来 trigger 可能发生而阻断。 | fixed |
| A-002 F-003（recommended） | v0.1.1 §2 使用“答案形态”，并区分创作者侧 B1 要求与客观可实现精度的 B3/S2 求解。 | absorbed |
| A-002 F-004（recommended） | v0.1.1 §4 固定所引 S1/W2 基线文件与 SHA-256，并规定兼容性复审条件。 | absorbed |
| A-003 F-001（recommended/low） | 删除旧的“复审尚未完成”状态句，以本节和 frontmatter 记录 pass、创作者响应及冻结状态。 | addressed |

冻结只稳定 S1→S2 接口合同，不表示 S1 已完成，不表示案例结构或 S1/S2 方法已接受，也不授权实际 S2 integration、trial 或 solving。具体范围须满足本合同门禁，并另获创作者授权后才能实际进入 S2。

I-401 保持 open，I-402 保持 collecting；本次冻结不改变两项状态，也不解除其门禁。

## 依据

- S1：[run-10 冻结试跑基线 v0.16.1](stage1-framing-method-candidate-v0.16.1.md)；[已接受的 research-loop host v0.16.2](stage1-framing-method-candidate-v0.16.2.md) 仅作 host 身份上下文，不提供 split gate；[v0.16.3](stage1-framing-method-candidate-v0.16.3.md) 是 run-02 配套候选，不是一般已接受版本；[v0.17.0](stage1-framing-method-candidate-v0.17.0.md) semantic zoom 仍为 draft／unaccepted。
- S2：[W2 方法 v0.4](../../GOAL-002-r2-method-working-version/attachments/world-model-method-working-version-v0.4.md) 描述从明确的客观问题进入现有模型构建与验证。
- S2 外部研究补充：[S2 research adapter v0.1.0](../../GOAL-005-shared-research-loop/attachments/s2-research-adapter-v0.1.0.md)；仅在单独外部研究调用时适用。
