---
title: A-016 · 独立复核 v0.18.1 的 A-014 原 scope 修复与非研究范围边界
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
doc: audit-entry
record_id: A-016
source: independent
scope: same-scope closure review of A-014 F-001 against v0.18.1, including regression check against unintended non-research applicability
verdict: fail
---

# A-016 · 独立复核 v0.18.1 的 A-014 原 scope 修复与非研究范围边界（2026-09-29）

- **auditor**：Codex Reviewer subagent（gpt-6-sol，medium；fresh-context、read-only；仓库自定义 `REVIEWER` role adapter 未激活）。
- **审计类型**：finding-closure / methodology scope review。
- **审计范围**：以 A-014 原 scope 复核 research-return 后 scope inflation / parameterization escape 的修复，并检查整改是否将 Demand Preservation Check 扩至无 research-return 的场景；逐项核验 response record 所列 baseline、条件角色、B3 scope diff、F.2 第 5 项、出口第 11 项、风险表与后续检验项。不审查新 Probe、runtime 行为、方法普遍有效性、实际 handoff 或 S2。
- **verdict**：`fail`（Reviewer verdict：`REJECT`）。
- **required findings**：1 项 BLOCKER。
- **已确认内容**：[A-014 response record](A-014-response-v0181-scope-preservation.md) 所列九项修复位置均能对应到 v0.18.1；A-014 F-001 的研究回流路径文本缺口已得到修复。发现的新 finding 是修订越出研究回流范围。

## Finding

### F-001 · Demand Preservation Check 被扩展至非研究路径（required / BLOCKER）

**位置：** [v0.18.1 规则 B N2](../attachments/stage1-framing-method-integration-candidate-v0.18.1.md#L115)；[研究回流 baseline 定义](../attachments/stage1-framing-method-integration-candidate-v0.18.1.md#L132)；[出口检查第 11 项](../attachments/stage1-framing-method-integration-candidate-v0.18.1.md#L410)。

**Finding：** N2 通用路由要求“确认该项确为原问所求参数后变量化继续”，未限定这是 research-return 条件。出口检查第 11 项作为通用 handoff 检查，无条件要求最终问题集与当前有效 demand baseline 对照；但 §“研究回流所求守恒检查”只在研究结果进入 E/F 前建立该 baseline。无 research-return 的运行可能因此缺少一个通用出口所需的 baseline；既有 N2 变量化路径也可能被新条件意外限制。

**为何重要：** 创作者接受的修订边界只补充 research-return → E/F 与 F.2／出口检查间的窄约束，并明确不得泛化到所有非研究场景。当前措辞会改变没有发生 research-return 时的 S1 路由与交接条件，属于范围回归；它也使「条件性的研究回流检查」与通用出口条款不一致。

**建议修正：** 将 N2 的新增需求确认明确限定为 research-return 条件；无 research-return 时保留此前适用的 N2 路由。将出口第 11 项明确限定为本轮存在 research-return 的情况；没有研究结果回流时将该项标为不适用，不要求另建研究 baseline 或运行通用 Demand Preservation Check。若要对所有场景设同一 baseline 门禁，应另行获得创作者授权，本 finding 不作此建议。

## Verified

- v0.18.1 第 132–144 行建立 research-return 前 baseline、区分条件角色并做 scope diff；F.2 第 5 项、第 11 项、风险表和后续检验观察均与 response record 映射相符。
- run-13 trace 中确有一般存在性问题被扩为条件空间后由 creator 纠正的过程；这支持原 A-014 所指研究回流风险。
- 实际 SHA-256 与 response record 一致：v0.18.0 `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3`；v0.18.1 `A894CF5BF95F877D8DD904B4E276232E1444C4CFBA575D7D7B7BA98585EF499A`；run-13 trace `3D12AC8D6C1866CA453798CD7E3186D45A671EAFDABFAA331243B35537D50546`；Shared Research Core `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7`；Schema `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8`；S1 Adapter `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C`。

## Unable to verify

- v0.18.1 没有新运行，无法验证执行者会否在无 research-return 时把第 11 项标为不适用，或按 N2 处理非研究参数。
- 本意见不评价新 Probe，不证明该修订已运行验证，也不授权试跑或 S2。

## Verdict and next step

**REJECT。** A-014 F-001 在研究回流路径上的修复可确认，但新增 required / BLOCKER F-001 未闭合，因此 v0.18.1 不应冻结为下一轮 regression baseline。建议由 `/govern` 响应此意见并裁决最小范围修正、接受 residual 或 overrule 路径。A-014 与 A-016 原 verdict 均保留；本意见不改目标 status/progress，不授权新 Probe、handoff 或 S2。
