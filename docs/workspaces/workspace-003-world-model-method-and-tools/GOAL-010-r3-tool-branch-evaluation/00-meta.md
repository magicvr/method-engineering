---
id: GOAL-010-r3-tool-branch-evaluation
title: R3 · 工具分支评估与落实
status: active
parent: GOAL-001-world-model-method-and-tools
created: 2026-10-04
updated: 2026-10-04
version: 0.1.3
progress: 75%
---

# GOAL-010 · R3 工具分支评估与落实

## 概述

承接 Root R3：依据现行人工方法过程/既有实践证据关闭 I-006，判断是否值得工具化，并在分支决定后形成最小 Skill 规格或本轮 no-tool 记录。工具不得代替方法有效性，也不得绕过真实案例与 R4 交付门禁。

## 非目标

- 不在 S2 分支决定前实现或安装工具/Skill。
- 不运行真实案例、不新增来源/实验/原创、不交付 R4、不修改下游。
- 不关闭 I-002/I-004/I-010，不恢复旧 H/H3，不把方法工作版写成已验证。
- 不把字段完整、纸面检查或 no-tool 结论写成工具价值/方法有效性的证明。

## 成功标准

- [x] S1：盘点现行人工过程与既有实践证据，覆盖重复步骤、人工成本、收益、维护负担和失败/停止路径。
- [x] S2：形成支持工具化 / no-tool / 证据不足的明确分支决定；关闭 I-006 或登记用户裁决的残余/延期。
- [x] S3：按分支形成最小 Skill 接口规格，或形成 no-tool 理由、证据范围、责任与复评触发。
- [ ] S4：内部核对与独立退出审计完成，无开放 required；用户确认后才置 done。

## 纲领路线图（P-001）

| 阶段 | 名称 | 状态 | 退出条件 |
|---|---|---|---|
| S1 | I-006 证据盘点 | 已完成 | E-001 已形成证据清单并区分事实/边界：流程已文档化，但真实重复、成本、收益、维护与实际失败路径未观察。 |
| S2 | 工具分支决定 | 已完成 | 用户接受 D-001：证据不足下的本轮 no-tool；I-006 记为限定 accepted-residual（非 verified），仅解除 GOAL-010 S2～S4/R3 退出门禁。 |
| S3 | 分支落实 | 已完成 | E-004 已形成 no-tool 记录：证据不足、未验证项、人工继续路径、未授权边界、责任与复评触发均可核对。 |
| S4 | 内部核对与独立审计 | 未开始 | 分支成果可核对、门禁未误放行、无开放 required；独立审计通过后待用户确认 done。 |

S1→S2→S3→S4 串行；工具实现必须等 S2 支持分支与接口稳定，真实案例/R4 不放行。

## 派生进度展示

S1～S4 四个等权检查点，当前 3/4=75%。S1 证据盘点、S2 分支决定、S3 no-tool 记录完成；S4 内部核对与 independent 退出审计待完成。progress 只作展示，不放行工具实现、真实案例、原创或 R4。

## 信息门禁引用（非第二台账）

唯一状态权威在 [Root 信息表](../GOAL-001-world-model-method-and-tools/00-meta.md)：I-006 为 R3 分支决定门禁；I-002/I-004 控制真实案例/R4；I-010 保持 accepted-residual（非 verified）；I-007/I-008 不扩容；旧 H/H3-SEM-001 不恢复。

## 审计模式

S1～S3 至少 self；若 S2 选择工具化并进入接口规格/实现评估，需对接口和门禁作 independent 审查。S4 采用 independent 退出审计；provider 与范围在 S2/S4 前确认。无 provider 时不得静默降级。

## 父目标与对齐

父目标 [GOAL-001-world-model-method-and-tools](../GOAL-001-world-model-method-and-tools/00-meta.md)，服务 VP-003 v0.1.1 → Charter method-engineering@0.1.0。

## 台账布局

01-decision/、02-execution/、03-audit/、attachments/ 平铺；D/E/A 编号从 001 起独立递增。
