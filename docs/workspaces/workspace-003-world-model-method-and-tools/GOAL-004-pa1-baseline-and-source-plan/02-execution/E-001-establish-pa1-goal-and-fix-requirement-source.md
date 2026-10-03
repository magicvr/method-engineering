---
title: 建立 PA1 阶段子目标并固定需求快照
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.2
record_id: E-001
---

# E-001 · 建立 PA1 阶段子目标并固定需求快照

2026-10-04，依据用户要求渐进开设子目标，建立 GOAL-004-pa1-baseline-and-source-plan 五件套及四个 ledger 目录，承接 GOAL-003 的 PA1。

## S1 需求固定事实

下游仓 `C:\Users\magicvr\Documents\Code\WorldModel.ModernCultivation` 中：

- 分支：`dev/vp-002`，当前 HEAD `2985080`；目标提交 `7324bdfcb35676c5fae8a3162b8d5a348a4b37ab` 可读取。
- 材料路径：`exchange/WRK-002-world-model-method-and-tools/需求-2026-09-26.md`。
- `7324bdf` 中该路径 blob：`281582b95d8cfcc85ea79b00e9495e305f0d17f3`。
- 当前工作树文件 blob：同一值；`git diff --quiet 7324bdf -- <path>` 退出码 0。
- 当前工作树文件 SHA-256：`F8B3E49C030AD9E1E1022F78D791D03E24DB66685EC9005F83B7BC96FD5AF4B9`。
- 固定结论：提交级 blob 与本地提取所用的当前文件一致；后续 §10/§13 原文可追溯到 `7324bdf`。该事实只固定来源版本，不评价需求或理论。

checkpoint commit：`a6ddcc8273d5ea6e49a843b350f7c4575f35111c`。该提交包含 GOAL-004 建目标时的五件套与需求固定事实；后续 S1/S2 记录另以后续提交追踪。

## 当前边界

S1 的需求 blob 固定已完成；S1 仍待将 H1/H2/H3 原文来源与 GOAL-003 基线引用整理成统一 S1 记录并审计。S2～S4 未开始；Root I-007 仍 open；未抽取理论、未作适用性判断。