---
title: 准备 run-17 隔离试跑包并完成最终 binding preflight
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-111
doc: execution-entry
---

# E-111 · 准备 run-17 隔离试跑包并完成最终 binding preflight

按创作者 [D-067](../01-decision/D-067-freeze-v0185-run17-baseline-and-prepare.md)，创建并固定 run-17 的 execution projection、source map、中性 raw input card、trial design 与 draft binding。Projection 以冻结的 v0.18.5 为 source，map 逐段记录删节／转换及规范保真；保留 current-layer readiness 等全部当前 S1 规范。Runner-visible packet 恰为五项：clean projection、Shared Research Core v0.1.0、Record Schema v0.1.0、S1 Research Adapter v0.1.1、中性输入卡。初检发现输入卡文件名会泄露 historical-anchor/run ID 标签，已在提交最终 preflight 前改为 `s1-raw-question-input-v0.1.0.md`；卡片原文仍仅为「世界有多大？」及换行。

沿用隔离合同 v0.1.3 与逐字 creator relay；control-only 历史比较只可在 runner 停止且 creator 先作产品判断之后使用。run-15/run-16 与方法修订原因不进入 runner packet；未设预期答案、维度或内部机制触发门槛。

Fresh-context independent Reviewer 对最终 binding 做 preflight，verdict=`ACCEPT`、无 finding。12 项 manifest 的文件路径、raw byte length 与 SHA-256 全部匹配；当前 `~/.codex/AGENTS.md` 与已审计捕获件均为 13,638 bytes，SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`。具体身份见下表及 [A-026](../03-audit/A-026-run17-binding-preflight-review.md)。

| 产物 | Bytes | SHA-256 |
|---|---:|---|
| [v0.18.5 execution projection](../attachments/stage1-framing-method-v0.18.5-execution-projection-v0.1.0.md) | 58,415 | `CB71BA8A949E775CBD9C8E8FEB4F99CE1EC8E77E4D83A71E3890409D0BC0F13F` |
| [Source map](../attachments/stage1-framing-method-v0.18.5-execution-projection-map-v0.1.0.md) | 4,504 | `5525C346A295DC7AA0B21EC1868E2B03B42CEB584D8232B4DFDDD03C90428140` |
| [Raw input card](../attachments/s1-raw-question-input-v0.1.0.md) | 19 | `0F055FB9C915E116272BC676EF9BBF5768A752C02C9D6483D9CCF7049FC3ECCE` |
| [Trial design](../attachments/s1-historical-anchor-integrated-trial-design-run-17-v0.1.0.md) | 10,306 | `73A8752FEC73B8DE6E1F943E29EC059B137B6405B38DF622746799BE5C5E5A21` |
| [Binding](../attachments/s1-historical-anchor-integrated-trial-binding-run-17-v0.1.0.md) | 13,342 | `89219D7539CDF37B4B797C777AB9AC5165E1FE73EFF363BF2BC7698C5B9C258E` |

run-17 remains `not-run / execution_authorization: not-granted`. No runner was created or prompted, no creator relay occurred, and no S1→S2 handoff or S2 start occurred. The exact final binding SHA is submitted separately for creator execution authorization.