---
title: 裁决 shared components 集中落点、候选修订与宿主最小接入范围
status: accepted
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-005-shared-research-loop
record_id: D-003
doc: decision-entry
---

# D-003 · 裁决 shared components 集中落点、候选修订与宿主最小接入范围

## 决定

采用集中共享落点：Shared Research Core、共享记录 schema、S1 adapter、S2 adapter 均置于 `GOAL-005-shared-research-loop/attachments/`，分别以 `v0.1.0` 作为首个**候选修订标识**。后续拆分文件名记于 [接入方案 v0.2](../attachments/shared-research-loop-integration-plan-v0.2.md)。该标识不代表语义接受、冻结或试跑通过；现有综合候选 v0.1 保留为拆分来源。

每个宿主只增加一个窄的调用/回流接口：S1 adapter 规定调用条件与研究结果回到既有 Rule E/F/G 的方式；S2 adapter 规定 S2 模型构建/验证中的调用条件与研究依据回到既有模型验证的方式。共享研究语义不复制进两个宿主，adapter/core 不获得宿主的候选准入、coverage 或模型采纳裁决权。

S1/S2 宿主的下一个正式方法版本号和具体文字插入点暂不指定：S1 v0.17.0 仍为 draft/unaccepted，冻结试跑基线仍为 v0.16.1；S2 W2 v0.4 是历史基线，当前 W2 尚在回流。分别在可用宿主基线确定后再定版本号与精确插入点；后续 host 修改仍须另行授权。

## 理由与边界

集中落点让 core/schema/两种 adapter 有单一可追溯的语义与修订目录；宿主只保留最薄的调用和回流接口，避免重复维护来源评价、迁移与停止规则。宿主版本号暂缓可防止把未接受的 S1 候选或 S2 历史基线误当成正式宿主起点。

本决定只裁决文件边界、shared component 首个候选修订标识和宿主最小接入范围，不接受 core 候选或接入方案的全部语义，不创建拆分后的组件文件，不修改任何 S1/S2 方法版本，也不授权方法集成、案例选择或调用试跑。语义接受和 host 修改授权留待后续独立裁决。
