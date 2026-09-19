---
id: D-009-respond-a002-p3-1-procedure
doc: decision-entry
status: accepted
parent: GOAL-003-outline-meta-rule-boundary-exploration
created: 2026-09-19
updated: 2026-09-19
version: 0.1.0
---

# D-009 · 响应 A-002：修订 P3.1 第 5 步与第 7 步

## 决定

响应 [`A-002-p3-1-procedure-review.md`](../03-audit/A-002-p3-1-procedure-review.md)。路径为 `fixed`，不走 residual / overruled。D-008 仍有效；本条只修订其第 5 步准入和第 7 步 Q1 范围，并吸收 F-003、F-004。修订写入 [`attachments/p3-1-min-background-world-model-procedure.md`](../attachments/p3-1-min-background-world-model-procedure.md) v0.2.0。

1. **F-001（required）**：W 准入改为两道门同时成立。推论条件：$R+D \models x$。物化条件：若不显式记录，本遍已暴露且足以改变主题选择判断的共享默认会不稳定。无法由 $R+D$ 推出、但对主题选择重要的事项一律入 U，禁止因「下游需要知道」写入 W。
2. **F-002（required）**：Q1 改为只评估截至本遍已经暴露、且其不同解释足以改变主题选择判断的背景问题。删除「作品将会涉及、但未逐条声明的事实」这一未知全集量词。
3. **F-003（recommended，一并吸收）**：写明 W 不是全部世界事实；当前工作世界模型为 $R + D + W$；D 本身是已成立事实，不重复登记于 W。
4. **F-004（recommended，一并吸收）**：W 的确定性不得高于所依据的 D；依据含暂定 D 时，该 W 标「随暂定 D-n」，不得当作作者已确认事实。

本拍不启动 P3.2，不把操作稿写成已验证方法。A-002 原文与 `conditional` verdict 保留。

## 理由

F-001 指出的漏洞成立：把「主题选择需要共享默认」当成世界内必然性，会让方法替作者编造事实。F-002 指出的量词也成立：主题选择前不存在「作品将会涉及」的闭集，按该量词执行会把 Q1 做成无界世界构建。

F-003、F-004 与必改项同向，成本低，进入 P3.2 前吸收可减少走查时把 D/W 或暂定推论读错。不存在与 A-001 或其他意见的 verdict/必改冲突。

未选「驳回 F-001/F-002」或「接受残余」：两处都是操作稿自身语义缺陷，可在进入内部验证前直接改文，没有需要保留的残余收益。

## 未选方案

| 方案 | 未选理由 |
|------|----------|
| 只改说明、不改第 5 步判定表 | 漏洞在准入规则，不改判定仍会在走查中把未推出事项写入 W。 |
| 把「主题选择需要」单独做成第三类写入 W | 仍是用工作流需要创造世界事实，与 F-001 闭合要求相反。 |
| 本拍同时开始 P3.2 | 用户本拍只要求响应 A-002；必改项闭合后即可建议启动 P3.2，但不在本条自动开跑。 |
| 改写 A-002 原文或改其 verdict | 独立意见只出意见；响应走本条与 A-003。 |

## 影响

- A-002 F-001、F-002 在编排响应中记为 `fixed`，待独立 finding-closure 复核；未复核不改变 A-002 原文。
- A-002 F-003、F-004 一并吸收，记为 `fixed`。
- P3.2 不再被这两条 required finding 阻断；是否立刻开跑由下一拍决定。
- G-003 仍为 `collecting`。操作稿修订不等于内部验证完成。

## 后续

建议指定 provider 对 F-001/F-002 的修正做 independent finding-closure；也可按 A-002 建议，在修正后直接做 P3.2 有界走查（极小现实基准 + 带明显差异的例子）。本条不自动启动 P3.2。

## 依据

- GOAL-003 [`A-002-p3-1-procedure-review.md`](../03-audit/A-002-p3-1-procedure-review.md)。
- 维护者要求响应该独立意见。
- [`D-008-p3-1-operationalize-procedure.md`](D-008-p3-1-operationalize-procedure.md)。
---
