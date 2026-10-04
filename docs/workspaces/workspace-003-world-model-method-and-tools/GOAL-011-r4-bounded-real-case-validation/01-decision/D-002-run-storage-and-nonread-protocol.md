---
title: 多轮运行记录与程序性非读取协议
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-001-world-model-method-and-tools
version: 0.1.0
record_id: D-002
decision_status: accepted
---

# D-002 · 多轮运行记录与程序性非读取协议

## 用户裁决

2026-10-04，用户确认：

- R4 试运行的真实需求结果在本仓验收；方法工作版与 no-tool 记录仍须交付下游，完成实际收件/验收/异议迭代；分层规则见 [D-003](D-003-dual-acceptance-layers.md)。
- 预计多轮运行；所有运行记录位于 GOAL-011 `attachments/runs/` 下，不放到其他位置。
- 不建设硬沙盒；要求 worker 不读取治理上下文或其他 run 记录。只要核验确认本轮确实未读取禁止内容，该轮可接受；若发现读取，则该轮不承认，另起新 run。
- 不把目标扩大为“构建子代理隔绝环境”。

## 规则摘要

采用 [run-protocol-v0.1](../attachments/run-protocol-v0.1.md)：

- 每轮 `RUN-NNN-slug/` 自包含：`input/`（含 raw-input、冻结方法快照、packet）、`work/`、`output/`、`events/`、`controller/`。
- worker 只读 `input/` 与本轮已发布的用户回应，读写 `work/`、`output/`、`events/`；禁止读取 `controller/`、其他 run、治理文件、Git 历史、其他线程/记忆/外部搜索。
- controller 保存来源、哈希、包装差异、轨迹、核验、验收与反馈；worker 不得读写。
- 运行有效性：若轨迹/声明/路径核验未发现越界读取，可接受；发现越界则 `excluded`，保留该轮供诊断并另起新 run；无法核验则不得写成 clean。
- 本仓试运行验收：维护者为验收人；记录在该轮 `controller/acceptance.md`；下游交付验收在 S5 另行记录。

## 边界

本协议不实现硬沙盒、不创建通用隔离基础设施、不改变 no-tool 分支。R4 仍须 S2 最终版适配、S3 运行、S4 本仓验收、S5 维护者外部审计。
