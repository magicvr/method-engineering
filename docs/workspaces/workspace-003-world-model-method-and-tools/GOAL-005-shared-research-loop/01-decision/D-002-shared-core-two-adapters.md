---
title: 采用共享 core 与 S1/S2 双 adapter 架构并保留版本边界裁决
status: accepted
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-005-shared-research-loop
record_id: D-002
doc: decision-entry
---

# D-002 · 采用共享 core 与 S1/S2 双 adapter 架构并保留版本边界裁决

## 决定

采用一个保持独立语义 owner 的共享 research core，并为 S1、S2 分别定义窄 adapter。Core 负责未知类型/owner、研究问题、来源策略、证据评价、迁移、综合、有界停止与剩余未知；它不拥有 S1 或 S2 的子流程，也无权裁定宿主结果。

S1 adapter 只规定调用条件、如何形成研究候选及如何把结果交回现有 Rule E/F/G；S2 adapter 只规定模型构建/验证中何时调用，以及机制、参数、约束、已有模型、观测资料如何回到 S2 模型验证。两个 adapter 共用同一 core/schema，不复制 core 的证据评价或停止规则。S1 的准入/coverage 由 E/F/G 处理；S2 是否采用证据由其模型构建与验证过程决定。

在接入计划完成后，正式 core/adapter/宿主版本标识、物理落盘位置及每个宿主最小改动范围再交创作者裁决。此决定不选这些值，不等于接受 core 候选或接入计划，也不授权修改方法版本。

未来验证安排为两次分开的调用试跑：先 S1、后 S2；二者使用同一冻结 core/schema，各自验证对应宿主回流接口并独立留存证据。当前只把试跑顺序、验证目标与证据接口写入计划，不选案例、不运行试跑。

## 理由与边界

保留唯一语义 owner，可让来源评价、迁移和停止规则不在两个宿主间分叉；窄 adapter 则把 S1 的结构准入/覆盖与 S2 的模型验证留在各自已有决策链内。核心规则与宿主裁决职责分开，也便于分别核对同一个 core 是否能服务两个 host。

未选在 S1 与 S2 各自复制完整研究闭环，因为那会产生两份证据评价、迁移与停止语义，增加漂移风险；也未让 shared core 决定候选准入或模型采纳，因为这会越过现有宿主裁决权。

当前授权仅限候选与版本化接入方案设计。共享 core 与 integration plan 均保持 `draft / unaccepted`。在后续裁决正式版本、物理位置和最小 diff 前，不修改任何正式或候选方法版本，不改 Probe 1 案例结论，不运行试跑。
