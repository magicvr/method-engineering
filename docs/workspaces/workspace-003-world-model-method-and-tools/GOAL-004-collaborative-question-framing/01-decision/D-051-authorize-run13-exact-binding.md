---
title: 授权按精确 binding 执行 run-13
status: accepted
created: 2026-09-28
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-051
doc: decision-entry
---

# D-051 · 授权按精确 binding 执行 run-13

## 创作者裁决

创作者接受 run-13 v0.1.1 准备包，并授权执行一次 run-13 S1 end-to-end isolated trial。授权身份为 [run-13 binding v0.1.1](../attachments/s1-e2e-integration-trial-binding-run-13-v0.1.1.md)，SHA-256：

`9667464D1F0F9C584B5499795AC9F26157F98259021125F4A37645BB997778DC`

启动前须重新核对 binding §§2.1–2.3 的完整 manifest、projection map source→projection 链、五项 runner-visible packet、经审计的 generic bootstrap 与实际运行隔离。任何 required identity 不匹配，或 fresh context／filesystem isolation 无法证实时，不得启动。

授权只覆盖该 binding 规定的一次 run-13。条件触发的 research-loop 与 semantic zoom 不得被强制；runner 应在 S1 creator confirmation 后停止。授权不包含 S1→S2 handoff、节点级独立交接、W2/S2 或实际求解。

## 身份与范围边界

- Binding 文件保持获授权时的原始字节与 SHA-256；本决策记录单独保存授权事实，不回写 binding frontmatter，以免改变授权身份。
- 本裁决不修改 v0.18.0、Core、Schema、Adapter、isolation context contract、design 或 raw Probe。
- 启动门禁结果另记于 [E-082](../02-execution/E-082-run13-startup-isolation-gate-failed.md)；不得将未启动记成已执行试跑。
