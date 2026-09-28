---
title: 阶段一协作定界方法 v0.18.0 执行投影映射
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.1
artifact_role: control-map-not-runner-input
---

# 阶段一协作定界方法 v0.18.0 执行投影映射 · v0.1.1

> 本文件是独立的控制映射，不属于 runner-visible projection，也不应随方法文本一并提供给试跑执行者。

- **Source**：`stage1-framing-method-integration-candidate-v0.18.0.md`，v0.18.0，SHA-256 `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3`。
- **Projection**：`stage1-framing-method-v0.18.0-execution-projection-v0.1.0.md`，projection v0.1.0，SHA-256 `4C46CB78BC2E13F63CA91FB584D51966642BEFCFD8A8C0613B4C6F9E021CE8E8`（verified from the current file bytes）。

## Section mapping

| Source candidate section | Runner projection section | Treatment |
|---|---|---|
| `## 方法对象与工作表示（工作表示可替换）` | 同名 | Normative method text carried over. |
| `## 规则 A · 产出物规则` | 同名 | Carried over. |
| `## 规则 E · 入结构门槛（候选相关性）` | 同名 | Carried over from v0.18.0, including the three admission conditions, evidence-type table, external-mechanism/anchor relevance limit, and “问题纳入、答案未定” status. |
| `## 规则 B · 按性质路由的主动分析` and `### 外部研究调用与回流（集成自 v0.16.3）` | `## 规则 B · 按性质路由的主动分析` and `### 外部研究调用与回流` | 按需研究调用/回流正文照录；标题去除来源版本说明。 |
| `## 规则 D · 有界诊断性探索与假定边界` | Same heading | Normative rule text carried over verbatim, including the parenthetical examples of undeclared scenario conditions. |
| `## 规则 C · 回问条件（末位手段，三条同时成立）` | Same heading | Carried over. |
| `## 规则 F · 未决项分类与归属（变量化不等于差异已消除）` | Same heading | Carried over. |
| `## 规则 G · 问题集充分性（覆盖攻击）` | Same heading | Carried over. |
| `## 节点粒度与局部递归细化（semantic zoom）` | Same heading | Carried over; the source reference “即使 v0.17.2 后续获接受” is projected as “即使 v0.18.0 后续获接受” to match the projected method identity. The linked contract remains a reference only; its file and case snapshot are control-side and excluded from the runner packet. No handoff rule changes. |
| `## 层级 · L1 世界模型问题 / L2 叙事消费需求` | Same heading | Carried over. |
| `## 认知操作（触发 + 必须产出）` and `### 触发纪律（防止清单退化为流程）` | Same headings | Carried over, except the development/test observation item about the prior global trigger-vs-checklist defect is omitted. |
| `## 出口退回检查（收束前必做）` | Same heading | Carried over from v0.18.0, including its research-related Rule E gate and all existing F/G, semantic zoom, and handoff checks. |
| `## 区分内容及其依据` | Same heading | Carried over. |
| `## 收束与创作者确认` | Same heading | Carried over. |
| `## 阶段二边界与本版状态` | `## 阶段二边界` | Only the operative stage-two boundary paragraph is carried over; candidate state/history is omitted. |
| `## 为什么会有这一版` and all revision/version-history text | Omitted | Development history and prior-run material are not runner input. |
| `## 风险与约束` | Omitted | Summary table omitted in the established projection format; operative rules are present in their primary sections above. |
| `## 本版来源与证据状态` | Omitted | Provenance narrative is kept outside the runner-visible projection. |
| `## 后续检验观察项` | Omitted | The inherited v0.16.3 probe reference and trial observations are control-side provenance, not v0.18.0 runner instructions; run-12 uses its separately bound new probe. |
| Case facts, prior-probe examples, audit/review history | Omitted | No historical case content is included in the projection. |

## Projection controls

- The research adapter, shared core, and schema are referenced from the Rule B interface; this projection does not duplicate or modify those component files.
- The frozen handoff contract is control-side only. The runner stops after S1 structure confirmation; the reviewer evaluates contract-content fit afterward.
- The projection is a clean rendering of the v0.18.0 draft/unaccepted method. It does not declare the method accepted, validated, trial-ready, or authorize S2 start or actual handoff.
- No trial was executed while preparing these files.
