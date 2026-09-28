---
title: 对 v0.17.1 做最小一致性修订并冻结 v0.17.2 为试跑基线
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-044
doc: decision-entry
---

# D-044 · 对 v0.17.1 做最小一致性修订并冻结 v0.17.2 为试跑基线

## 创作者裁决

接受 v0.17.1 的主体设计，先按以下范围做最小一致性修订形成 v0.17.2，再经文本一致性复核；没有新的 required finding 时，将 v0.17.2 冻结为新的 trial baseline：

1. 把出口总结统一为 Rule F/F.3：B1 已裁定、B2 已收敛、B3 已按 F.2 转写；变量化本身不构成交接充分条件。
2. 创作者确认只使当前结构进入 handoff 判断；实际 S1→S2 交接须满足冻结合同 v0.1.1 并另获实际交接授权；结构确认不自动启动 S2。
3. 允许局部递归细化与标记粒度已就绪的候选求解节点；本版获接受本身不自动开放节点级独立交接。节点级交接须由之后已接受、且明文允许相应范围拆分的 method/host 满足冻结合同 §1 的三项门禁。
4. 可将 F.2 标题“答案形式与精度”改为“答案形态与精度归属”，正文语义不变。

不改 Rule E/F/G、semantic zoom 操作、局部 G.1.3、向上冒泡或全局 coverage 规则。

## 执行结果

修订候选 v0.17.2 经独立复核 [A-006](../03-audit/A-006-v0172-text-consistency-review.md)：verdict=`pass`，required=0。依据本裁决将 v0.17.2 冻结为新的试跑基线，记录见 [E-067](../02-execution/E-067-v0172-consistency-freeze.md)。

冻结只固定实验版本，不表示方法已验证，不取代 v0.16.1 的 run-10 既有证据，也不授权 S2 或实际交接。方法 acceptance 仍为 `unaccepted`；GOAL-004 status/progress、I-401 与 I-402 状态不变。
