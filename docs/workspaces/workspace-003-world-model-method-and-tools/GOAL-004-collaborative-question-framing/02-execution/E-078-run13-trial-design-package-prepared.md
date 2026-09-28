---
title: 准备 run-13 S1 research-loop 集成试跑 binding 供创作者裁决
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-078
doc: execution-entry
---

# E-078 · 准备 run-13 S1 research-loop 集成试跑 binding 供创作者裁决

## 已完成的准备

- 在 A-011 的 run-12 reviewer disposition 与 E-077 evidence matrix 基础上，形成 run-13 候选隔离定义 [v0.1.0](../attachments/s1-isolated-trial-context-contract-v0.1.0.md) 和通用 bootstrap allow-list manifest [v0.1.0](../attachments/run13-generic-bootstrap-context-manifest-v0.1.0.md)。前者区分精确试跑 packet、hash 固定的通用 bootstrap 与平台生成／不可导出的 context，并要求分别核验 provenance 和 filesystem access。
- 新建 raw input card [run-13 v0.1.0](../attachments/s1-integration-trial-input-card-run13-v0.1.0.md)，其内容仅为一个问题。新建 control-side [run-13 E2E design v0.1.0](../attachments/s1-e2e-integration-trial-design-run-13-v0.1.0.md)，将 research 保持为由真实 unknown 条件触发；检索调用本身不算研究闭环证据。
- 新建 [run-13 binding v0.1.0](../attachments/s1-e2e-integration-trial-binding-run-13-v0.1.0.md)，逐项固定 candidate、projection／map、Shared Research Core／Schema、S1 Adapter、Probe、design、isolation contract、bootstrap manifest 与 capture 的 SHA-256，并包含 handoff contract 和 E-064 的 reviewer-only 身份。binding 状态为 `prepared-not-run` / `not-granted`，待创作者裁决。
- 保留 run-12 的 `research-loop` 与 research return 为 **`not observed`**；局部递归也未观察到。run-12 handoff contract-content fit 的 MAJOR 继续视为运行输出／记录问题，不升级为方法 finding。

## 验证与限制

- 对绑定文件计算完整 SHA-256 manifest，并复核 v0.18.0 源候选保持 D-048 冻结值 `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3`；projection map 的 source→projection hash 链须与当前实际字节相符。
- 内容／链接／hash 的准备核验不等同独立审计或运行证据。尚未创建 runner、启动会话、运行搜索、生成 trace 或执行任何 S1→S2 handoff。
- 方法 v0.18.0 仍为 draft/unaccepted 的试跑基线；本记录不改变目标 status/progress、I-401/I-402，不启动 W2/S2，也不执行实际求解。

## 待裁决

创作者可先审查 run-13 disposition、隔离合同、bootstrap manifest、单题 Probe、design 和完整 hash binding。只有创作者接受该 binding 并另行明确授权其当前精确 SHA-256 后，才可启动 run-13；沉默或本次准备不构成执行授权。
