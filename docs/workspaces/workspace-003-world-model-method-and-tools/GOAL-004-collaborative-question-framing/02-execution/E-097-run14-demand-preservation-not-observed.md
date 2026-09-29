---
title: 记录 run-14 Demand Preservation 窄回归试跑结果
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-097
doc: execution-entry
---

# E-097 · 记录 run-14 Demand Preservation 窄回归试跑结果

## 执行事实

创作者针对 binding SHA-256 `FA71DF2215978145105F3BA600F3B827F7A0FC69E4E8932A26161D3A4AA09E9C` 明确授权执行 run-14。试跑沿用 v0.18.2（SHA-256 `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6`），使用已接受的 run-14 design v0.1.2，按完整 S1 路径运行到 creator confirmation 后停止。

Runner 通过 fresh-context subagent 建立，`fork_turns:none`。Creator 依次确认：

1. 原问范围为“至少存在一个”；
2. 对象域为“现实世界”；
3. 接受 N1 并保持当前粒度。

Control 对三次回复逐字转回 runner。随后 runner 输出了候选结构、E/F 处理、覆盖攻击、残余遗漏与出口状态，并在 creator confirmation 后停止。可见交互、runner final 与证据限制保存在 [run-14 visible trace](../attachments/run-14-visible-runner-creator-trace.md)。

证据文件身份：

- Visible runner/creator trace：7,891 bytes，SHA-256 `801B6D19E3723E008B79B452D131CDA6C3805C0EAE9F78468CC20E6257A57A4C`。
- Disposition / evidence matrix：4,101 bytes，SHA-256 `9FB53A3905B78240D1711EDA21BEF4975A9AE64AD41C94B1E132E04D42B114F5`。
- A-019 independent review entry：3,296 bytes，SHA-256 `CF95F96AA0B0C2FA94DE1A0AA94469E07767A906303F16BB8215746ACC62C31C`。

## 试跑结果与审查

Runner 最终输出报告未调用外部研究，未产生 research-return。可见 trace 中也没有 research-return 进入 E/F、当前结构或 B3。按 binding §5 / design §§5–6，Demand Preservation 核心评分机会未出现，故 run-14 outcome 为 **`not observed / inconclusive`**；baseline、scope diff 与出口第 11 项均不适用，不能以未出现的检查步骤判 fail，也不能把非研究路径上的范围保持记作 regression pass。

Independent Reviewer 对该处置给出 `ACCEPT WITH NOTES`，本次处置无 required finding。意见指出，精确 spawn task、raw initial context 与独立工具日志未保存在所给证据中；隔离状态因此记为“可见交互中未见污染”，runner 自报没有被误写为独立工具日志。完整矩阵见 [run-14 disposition](../attachments/run-14-demand-preservation-disposition-and-evidence-matrix.md) 与 [A-019](../03-audit/A-019-run14-demand-preservation-disposition-review.md)。

## 结果边界与后续

- 该样本没有提供 v0.18.2 对 run-13 已知 failure path 的 positive regression evidence。
- 依创作者先前设定的 outcome 处理规则，不在同一 binding 下强制重跑。
- 后续是否需要另设一个更适合自然触发 research-return 的独立 Probe，留待单独决定；本条不创建 Probe 或启动 transfer trial。
- 没有修改 v0.18.2、Shared Research Core/Schema/Adapter；没有真实 S1→S2 handoff、S2、W2 或方法接受。
- GOAL status/progress 未变化。
