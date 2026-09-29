---
title: 独立预检 run-19 v0.1.1 binding
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: A-030
doc: audit-entry
source: independent
verdict: pass
---

# A-030 · 独立预检 run-19 v0.1.1 binding（2026-09-29）

- **source / attribution**：independent Reviewer（read-only preflight）；下列核查、verdict 与 findings 归于该 Reviewer。
- **scope**：最终 [run-19 v0.1.1 binding](../attachments/s1-historical-anchor-integrated-trial-binding-run-19-v0.1.1.md) 的身份、manifest、runner-visible packet、控制侧重复条件和隔离边界；Reviewer 未启动 runner，也未审查运行行为。
- **受审身份**：14,416 bytes，raw-byte SHA-256 `684B3B43A6D086AC0BD7FAD37BFA49FF51FC05C647DC77DE01688400A939B1CB`。
- **Reviewer verdict**：`ACCEPT / PASS`；本台账 verdict：`pass`，仅限 binding preflight。
- **findings**：无 material findings；required findings=0。

## 独立核查结果

1. Binding 声明的 14/14 manifest 文件大小与 SHA-256 均匹配。冻结 source v0.18.5 为 96,103 bytes，SHA-256 `6B991D86F5BAB4EC4DF65825EA3759D566377325A22D21FC97CBA393FEF6BBD6`。
2. Runner-visible packet 恰为五项，与 run-18 对应文件逐字节相同；Probe card 恰为 UTF-8 `世界有多大？\n`。
3. Runner task、relay protocol 和 stop instruction 与 run-18 逐字一致。run-19 identity、trace path 及 `proposal / not-run / execution_authorization: not-granted` 状态一致。
4. Packet 与 generic bootstrap 未检出被禁止的历史、findings、预期拆解、L(W)、graph、IR 或 method-issue framing。重复性与历史信息仍只在控制侧，runner 不可见。

## 结论与边界

v0.1.1 binding 的独立 preflight 通过。A-029 对 v0.1.0 的 `REJECT` 保留；其 F-001 已经 D-071/E-117 以 `fixed` 闭合，v0.1.0 仍为 rejected/superseded 身份。本次意见不构成试跑或方法通过，也不授予执行权限。创作者仍须对上列 v0.1.1 精确 SHA 单独授权；run-19 尚未启动。
