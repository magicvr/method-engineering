---
title: 记录 run-13 v0.1.1 修订、独立复核与最终 preflight
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-081
doc: execution-entry
---

# E-081 · 记录 run-13 v0.1.1 修订、独立复核与最终 preflight

## 修订与身份

- 保留 v0.1.0 raw card/design/binding 快照；新增 v0.1.1 版本化修订。raw Probe 精确为“一个生态系统能长期自我维持吗？”。
- Trial design 只替换用户指定的未知项措辞并更新新 card 链接；research trigger/non-trigger 规则未变。
- 最终 binding：[run-13 v0.1.1](../attachments/s1-e2e-integration-trial-binding-run-13-v0.1.1.md)，SHA-256：`9667464D1F0F9C584B5499795AC9F26157F98259021125F4A37645BB997778DC`。
- v0.18.0、Core、Schema、Adapter、isolation context contract v0.1.0、generic bootstrap allow-list 语义均未改。

## Preflight 与独立复核

- 对 binding §§2.1–2.3 的 18 项 manifest 全部重新计算 bytes 与 SHA-256，均匹配；projection map 的 source candidate 与 execution projection hashes 亦匹配当前字节。
- 独立审计 [A-013](../03-audit/A-013-run13-v011-binding-preflight-review.md) verdict `pass`，findings=0；确认变更限于获准范围。
- Binding 状态保持 `prepared-not-run` / `execution_authorization: not-granted`。本次没有创建 runner/session、没有运行 Probe 或搜索，没有 handoff、W2/S2 或实际求解。
- Bootstrap 实际注入与 filesystem isolation 仍须在任何获授权运行启动前按 binding §5 最终核验。

## 待创作者裁决

本 binding 已准备好供创作者作**单独的 run-13 执行授权**。执行授权须明确引用上述最终 SHA-256；本准备记录不构成授权。
