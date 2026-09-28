---
title: Run-12 首次隔离判断与执行轨迹保全（分类由 E-075 复核）
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.1
id: GOAL-004-collaborative-question-framing
record_id: E-074
doc: execution-entry
---

# E-074 · Run-12 首次隔离判断与执行轨迹保全

> 本条记录最初将全局 bootstrap 指令误判为 project-history isolation failure。依据后续 [E-075](E-075-run12-bootstrap-context-isolation-review.md)，现将问题分类更正为 `unbound bootstrap-context deviation`；不认定发生项目历史泄漏。样本效力随后由创作者按 [D-047](../01-decision/D-047-run12-limited-sample-and-bootstrap-boundary.md) 裁定为有限 S1 E2E 行为样本，详细范围见 [E-076](E-076-run12-limited-sample-disposition.md)。

## 已发生事实

- 按 run-12 binding v0.1.1 的绑定身份启动一次 Codex CLI runner 会话。启动前再次核对 manifest 所列 14 项 SHA-256；均与 binding 一致，授权 binding SHA-256 为 `370D73B081B3917E9CFACE00FF75BFE738511E0193C8842000CF8E204E5BF50F`。会话 id 为 `01a0e825-c2bb-7bc0-95c0-8536d99b7236`，声明的 cwd 为临时平行目录 `method-engineering-run12-isolated`。
- runner context 的 rollout `world_state` ordinal 6 含主环境完整 `AGENTS.md`；后续核对确认该内容与全局 `C:\Users\magicvr\.codex\AGENTS.md` 字节级一致，且只是通用角色／执行治理指令。它不包含项目方法、Probe/run 历史、S1/S2 或城市机制信息。该内容仍未绑定到五项 packet，故保留为 packet-boundary deviation；按 E-075 不再称为 project-history leakage。
- runner 随后尝试经 `functions.exec` 读取 `$CODEX_HOME/agents/scout.toml` 与 `reviewer.toml`；rollout ordinal 26 记录命令被策略阻止，未返回这些文件的内容。未发现 `web_search` 调用。Codex `turn_context` 记录 active permission profile 为 `:read-only`；该运行配置未实现 binding 要求的纯五项上下文隔离。
- transcript 中确实记录了创作者的三项真实输入：Probe 不绑定具体世界观；接受 Q1/Q2 并保持当前粒度；确认并收束 S1。runner 随后停止，并明确没有交接或启动 S2。按 D-047，这些行为可作为有限样本的可观察证据；但不能证明原 binding v0.1.1 的 packet-only 隔离门禁已通过，也不构成方法接受依据。
- 本轮没有触发 external research；semantic zoom 的行为能力也不能据此判为通过或失败。runner 停止后，Reviewer 子代理 `run12_contract_fit_review`（`gpt-6-sol`, `medium`）依 binding 做了 trial-only contract-content fit 检查：transcript **不符合完整 S1→S2 handoff package**。具体缺口为：未标明实际使用的 S1 method／host 修订及整体 handoff scope；B3 owner 仅写“后续求解者”，没有说明 W2 v0.4 的求解职责／检查顺序；residual 表未给 owner 及其对所声明交付范围的影响／依赖。Reviewer 排除了冻结合同 §1 的 freeze-time case sentence，依 E-064 将其视为历史快照。此 fit 结论只评估记录内容，不是行为 finding；没有执行实际 S1→S2 handoff、节点级交接或 W2/S2。
- 完整 73-event Codex rollout、补充分轮 JSONL、stderr 与最后消息均已从临时沙箱复制至 [run-12 原始轨迹清单](../attachments/run12-invalidated-trace/trace-manifest.md)，并记录逐文件 SHA-256。源侧完整 rollout SHA-256：`CCC2EE5548DF3489884C12750E49BF90915BDA452B16CE824B589BB81FC9D2CF`。

## 状态边界

- Run-12 的当前分类与样本效力边界以 E-075、D-047 和 E-076 为准：它已被接受为有限行为样本，但不得外推为无偏／完整样本或原 binding packet-only 门禁通过；不得继续把全局 bootstrap 指令称作项目历史泄漏。
- 不据此修改或接受 v0.18.0，不改 run-11 或此前证据，不改变 I-401 / I-402、GOAL-004 status/progress 或 goal-tree。
- 后续若考虑另行试跑，须重新评估隔离方案并取得针对新 run/binding 的授权；本次单次 run-12 授权不延伸为重跑授权。
