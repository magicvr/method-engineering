---
title: 授权澄清研究证据与 S1 条件问题准入边界
status: accepted
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-005-shared-research-loop
record_id: D-013
doc: decision-entry
---

# D-013 · 授权澄清研究证据与 S1 条件问题准入边界

## 创作者裁决

创作者选择以实施修正的方式响应 A-001 required finding F-001（目标按 `fixed` 路径闭合；在修正与复核证据到位前，finding 保持开放），授权形成并复核一组最小、版本化的 S1 合同候选：从已接受且保持不变的 S1 adapter v0.1.0 派生 S1 adapter v0.1.1；从已接受且保持不变的 S1 host v0.16.2 派生 host v0.16.3。修订仅澄清：外部研究可与当前输入锚点及显式推理共同支持“某条件是否成立/其值为何”作为待答问题的相关性依据；该准入不证明目标对象具备该条件。

准入说明须要求具体结构贡献落在**必要问题结构或求解依赖**上；“不同参数会改变最终结果”本身不足以准入。还须检查输入排除、既有节点承载及冗余。宿主需把“问题纳入、答案未定”与“目标条件为真”分开记录，答案 owner 再按现有 Rule F 分类。此项澄清不预先接受 run-01 的任一候选。

## 范围与保护

- 不修改或覆写 shared Core v0.1.0、共享 Schema v0.1.0、S1 adapter v0.1.0、S2 adapter v0.1.0、S1 host v0.16.2、run-01 或 GOAL-004 v0.17.0。
- 不新增 schema 字段，不改 Core/S2 研究职责，不改变 Rule F/G 或研究停止规则。
- 只授权产生 S1 adapter v0.1.1 与 S1 host v0.16.3 草案并进行独立复核；两者在创作者另行接受前均不是新基线。
- 本决定不授权新的 research call、清洁盲试、S2 试跑、Probe 1、父层结构确认或全局 coverage search。

## Finding 状态

A-001/F-001 仍开放，直至新候选形成、经 Reviewer 独立复核并有可核对修正证据。完成修正本身不等于接受新版本或授权执行盲试；试跑需另行裁决。
