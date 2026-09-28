---
title: 准备 S1 end-to-end integration candidate 与 run-12 binding
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-072
doc: execution-entry
---

# E-072 · 准备 S1 end-to-end integration candidate 与 run-12 binding

## 已发生事实

- A-010 窄范围独立审计 verdict=`pass`、required findings=0：run-11 Q1 起初 B2/B3 错分属于执行错误；v0.17.2 Rule F 足够明确。该错分保留为 runner regression observation，未修改 v0.17.2、Rule F 或 semantic zoom。
- 以 v0.17.2 为主干，形成 S1 integration candidate v0.18.0；纳入此前 run-02 已出现并经复核的 v0.16.3 Rule E 条件问题准入、Rule B 按需 research 调用/回流语义。Shared Research Core / Schema v0.1.0 与 S1 Research Adapter v0.1.1 文件均未修改。候选中的旧“世界有多大”检验计划已明确标为来源历史，不再充当 run-12 Probe。集成候选未接受、未试跑。
- 为候选制作 runner-visible clean execution projection 与 control-only projection map。映射复核发现 Rule D 的示例是方法文本中的操作性例示，投影已补回并在映射中如实说明；另将候选继承的旧 Probe 计划标明为历史来源说明，方法规则未改。
- 形成 control-side end-to-end trial design 和独立 raw input card，Probe 为“为什么这个世界仍然需要城市？”。输入卡不包含城市机制、taxonomy、答案、来源或搜索方向。
- 形成 run-12 binding，固定候选、投影、映射、试跑设计、原问、Core、Schema、Adapter 与冻结 handoff contract 的文件身份及 SHA-256，并区分 runner-visible 与 control-only 材料。冻结合同仅按其规范规则使用；§1 案例状态句按 E-064 作为冻结时点快照处理。
- 已按 binding manifest 逐项复核 runner packet 与 control-side provenance 文件的 SHA-256，均与登记值匹配；binding 本身 SHA-256 为 `1A7548CECE0832A208150EECE6007522F6479CD3723DAA41219575E7D195A6EC`。

## 当前状态与边界

- run-12 仅完成准备，状态为 `prepared-not-run`；本轮未启动 runner，也未执行新的 E2E 试跑。
- Research 与 semantic zoom 均是按真实需要触发的条件分支；不为覆盖观察项强制搜索或拆分。未触发分支只记 `not observed`。
- 试跑设计止于 S1 handoff-criteria judgment；不授权实际 S1→S2 handoff、节点独立交接、W2/S2、S2 research-loop、方法接受或一般有效性主张。
- GOAL-004 状态、progress、goal-tree 与 I-401 / I-402 未变。运行须等用户接受所请求的三项产物并另给明确 run-12 执行授权。

## 固定身份

| 产物 | SHA-256 |
|---|---|
| S1 integration candidate v0.18.0 | `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3` |
| Execution projection v0.1.0 | `4C46CB78BC2E13F63CA91FB584D51966642BEFCFD8A8C0613B4C6F9E021CE8E8` |
| Projection map v0.1.0 | `7DBB4A07D3CD4A74C15BC0C91355E18F834AF2A481E931577C6C038BCE4C909C` |
| Raw input card v0.1.0 | `28E676D6D59459304DD2CF48B31C91B10B71B5DB3106A39DD429A4F7A88CA028` |
| Trial design v0.1.0 | `A9BC20F1C074BB907D6F4A7339BFA84A2E0374DD0F82C382F2B39A0D1ADDD50F` |
| Run-12 binding v0.1.0 | `1A7548CECE0832A208150EECE6007522F6479CD3723DAA41219575E7D195A6EC` |

完整 manifest 与执行边界见 [run-12 binding](../attachments/s1-e2e-integration-trial-binding-run-12-v0.1.0.md)；设计见 [S1 E2E trial design](../attachments/s1-e2e-integration-trial-design-v0.1.0.md)。
