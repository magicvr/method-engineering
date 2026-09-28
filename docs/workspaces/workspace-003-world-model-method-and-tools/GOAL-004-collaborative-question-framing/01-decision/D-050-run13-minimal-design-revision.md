---
title: 接受 run-13 基线架构并裁决两项最小试跑设计修订
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-050
doc: decision-entry
---

# D-050 · 接受 run-13 基线架构并裁决两项最小试跑设计修订

## 创作者裁决

创作者接受 run-13 基线架构，但暂不授权执行，并指示仅进行以下修订：

1. 将 trial design 中“当前输入、已授权常识推理或创作者取舍”改为“当前输入上的推理或创作者取舍”；研究 trigger／non-trigger 规则不作其它修改。
2. 将 raw Probe 改为“一个生态系统能长期自我维持吗？”，仅删除“这个世界”指称，不加入机制、taxonomy、来源、搜索方向、条件列表或期望答案。

## 处置

- 保留已接受的 v0.1.0 card、design 与 binding 原文，作为历史快照；按版本化方式形成 v0.1.1。
- v0.1.1 仅更新 raw Probe、design 中指定措辞及对应版本／文件引用／bytes／SHA-256。v0.18.0、Core、Schema、Adapter、isolation context contract v0.1.0、generic bootstrap allow-list 语义均未改。
- 独立审计 [A-013](../03-audit/A-013-run13-v011-binding-preflight-review.md) verdict `pass`，未发现阻止提交执行授权请求的问题。完整 18 项 manifest 与 projection map source→projection hash 链均已复核匹配。

## 当前授权边界

最终 binding [run-13 v0.1.1](../attachments/s1-e2e-integration-trial-binding-run-13-v0.1.1.md) 的 SHA-256 为：

`9667464D1F0F9C584B5499795AC9F26157F98259021125F4A37645BB997778DC`

该 binding 仍标记为 `prepared-not-run` / `execution_authorization: not-granted`。本决策不启动 runner、新会话或 Probe，不授权搜索、handoff、W2/S2 或实际求解。实际执行须由创作者另行明确授权，并引用上述最终精确 hash；若 binding 或其所绑定文件更改，须重算 manifest 并重新提交裁决。
