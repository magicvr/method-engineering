---
title: A-017 独立复核 v0.18.2 对 A-016 F-001 的闭合
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
doc: audit-opinion
---

# A-017 · 独立复核 v0.18.2 对 A-016 F-001 的闭合

- **source**：independent
- **auditor**：Codex Reviewer subagent（gpt-6-sol，medium；fresh-context、read-only；仓库自定义 `REVIEWER` role adapter 未激活）
- **scope**：复核 A-016 原 scope，判断 v0.18.2 是否只修复 research-return 路径的 Demand Preservation Check 适用范围，并保留 A-014 F-001 修复；不审查或启动新 Probe、S2 或实际运行验证。
- **verdict**：pass（Reviewer 原始意见：`ACCEPT`）
- **required findings**：0

## 复核结论

未发现 finding。A-016 F-001 已在指定范围内闭合。

## 已核对

1. v0.18.2 规则 B 的 N2 路由恢复普通非研究路径既有变量化和 Rule F 归属语义；仅当未定项／候选源自 research-return 时，才在变量化或转写前执行 Demand Preservation Check（第 117 行）。
2. 出口检查第 11 项仅在本轮 research-return 结果进入 E/F、当前结构或 B3 时适用；否则明确记 `N/A`，不要求另建 demand baseline（第 412 行）。
3. 风险表、后续检验观察项和版本说明均限定在 research-return 结果进入 E/F／当前结构／B3 的场景（第 455、501 行及相应版本说明）。
4. A-014 F-001 的 research-return baseline、条件角色三分、scope diff、F.2 第 5 项和现有 B2 fallback 保持不变；未泛化至普通非研究 S1，也未增加固定 taxonomy、逐项创作者选值或新 blocker。
5. v0.18.1 原文及 SHA-256 `A894CF5BF95F877D8DD904B4E276232E1444C4CFBA575D7D7B7BA98585EF499A` 保留为 A-016 的审计对象；v0.18.2 SHA-256 为 `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6`。Reviewer 核对 v0.18.0、run-13 trace、Shared Research Core、Record Schema 与 S1 Research Adapter 的文件身份／hash 仍与既有记录一致。

## 未验证范围

本意见只确认文本修订闭合 A-016 原 scope；没有新运行证据，不判断 v0.18.2 的实际行为有效性、方法接受、Probe 结果、handoff 或 S2。
