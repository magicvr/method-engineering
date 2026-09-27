---
title: 登记共享研究闭环版本化接入方案范围与顺序
status: accepted
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-001-world-model-method-and-tools
version: 0.1.0
id: GOAL-002-r2-method-working-version
record_id: D-017
doc: decision-entry
---

# D-017 · 登记共享研究闭环版本化接入方案范围与顺序

用户裁决由 [GOAL-005](../../GOAL-005-shared-research-loop/00-meta.md) 在 W2 当前顺序切片中记录并规划“一个共享研究 core＋S1/S2 双 adapter”的版本化接入方案，方案见 [shared-research-loop-integration-plan-v0.1](../../GOAL-005-shared-research-loop/attachments/shared-research-loop-integration-plan-v0.1.md)。Core 是唯一研究语义 owner；S1 adapter 只把研究调用与输出接回 Rule E/F/G，S2 adapter 只把模型构建/验证所需研究依据接回其模型验证。Core 不拥有两阶段子流程或宿主裁决权，两个 adapter 不复制 core 规则。

本轮只形成方案，不修改任何正式/候选方法版本，不运行 S1/S2 试跑，也不改 Probe 1 或其案例结论。正式组件/宿主版本号、物理位置与各 host 最小 diff，待方案完成后另由创作者裁决。之后分别设计 S1 与 S2 两次调用试跑；两轮使用同一冻结 core/schema，各自验证研究结果是否回到对应既有宿主机制，并独立记录证据。

GOAL-005 的 core 候选与接入方案均保持 `draft / unaccepted`。该切片不增加 W5、不改变 W1→W2→W3→W4 串行关系，不改变 GOAL-002 `active / 25%`，也不放行 GOAL-004、W2 或 W3。
