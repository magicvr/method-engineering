---
id: GOAL-001-method-engineering-runtime
doc: decision
status: done
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.6.0
---

# 决策记录 · GOAL-001

## 纲领路线图与阶段计划

Root 采用 `S1 冻结运行模型 → S2 落盘最小工作机制 → S3 机制 walkthrough 与交接` 的串行路线图。纲领路线图的权威在 `00-meta.md`；本文件只登记阶段计划和影响范围的决定。

## 阶段计划

| 阶段 | 计划 / 承接目标 | 说明 |
|------|-----------------|------|
| S1 | `01-decision/D-002-runtime-model.md` | 已冻结需求—响应运行模型、有限纸面 walkthrough 与 cross 审计路径。 |
| S2 | `01-decision/D-003-s2-minimal-work-mechanism.md`；`GOAL-002-s2-minimal-work-mechanism` | 已根据 S1 运行责任反推最小对象、记录边界、项目级承载和流程文档。 |
| S3 | `GOAL-003-s3-mechanism-walkthrough-handoff`；其 `01-decision/D-001-s3-walkthrough-boundary.md` | 用虚构 trace 验证机制自身的完整路径与交接，不创建真实运行记录；I-003 在 S3 退出前关闭。 |

## Root 整体闭门

Root 已按 `D-004-root-closeout.md` 完成整体闭门；关闭范围是当前实现层目标，不延伸为 VP-001 或 Charter 关闭。

## 信息需求与阶段门禁

| ID | 级别 | 所需信息 / 假设 | 影响门禁 | 最晚需要阶段 | 验证 / 收集动作 | 状态 | 延期 / 复核 | 证据 / 决策 |
|----|------|-----------------|----------|--------------|-----------------|------|-------------|-------------|
| I-001 | required | 最小运行状态、转换、责任边界和追踪语义。 | 方案冻结、S1 退出 | S1 | 形成运行模型并做机制内部一致性检查。 | verified | 不延期；已在 S1 关门时处理。 | D-002 v0.4.0、E-003 v0.4.0、A-008 self `pass`、A-009 Grok independent `pass`、A-010 closeout；无新的 required finding。 |
| I-002 | required | 最小工作对象、记录边界、目录承载和流程文档。 | 实施、S2 退出 | S2 | 已从运行责任逐项反推，完成对象/承载方案、流程说明落盘，并按 D-004 重新核对项目级承载。 | verified | 不延期；已由 A-011 后的 A-012 修正核对。 | `GOAL-002-s2-minimal-work-mechanism` 的 I-201、D-002、D-004、A-001～A-004；项目根 `runtime-records/README.md`；`03-audit/A-012-s2-repository-hosting-correction.md`。 |
| I-003 | required | S3 bounded walkthrough 能否把 D-002、S2 项目级承载和 VP-001 退出判据 7/8 连接成可核对的机制证据。 | S3 walkthrough、Root/VP 后续结项 | S3 | 由 `GOAL-003-s3-mechanism-walkthrough-handoff` 执行虚构 trace、覆盖矩阵、交接核对，并完成 self + 指定 Grok independent 审视。 | verified | 不延期；已由 E-002/E-003、A-001～A-005、E-014/A-013 核对。 | `GOAL-003-s3-mechanism-walkthrough-handoff/02-execution/E-002-s3-bounded-walkthrough.md`；`E-003-s3-branch-paper-snapshots.md`；`03-audit/A-004-s3-finding-closure-a002.md`；`GOAL-001/02-execution/E-014-s3-root-handoff.md`；`GOAL-001/03-audit/A-013-s3-root-closeout-self.md`。 |

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-09-18 | 工作区启动边界与 Root 路线图 | accepted | `01-decision/D-001-bootstrap-scope.md` |
| D-002 | 2026-09-18 | S1 需求—响应运行模型与交叉审计路径 | accepted | `01-decision/D-002-runtime-model.md` |
| D-003 | 2026-09-18 | S2 启动与最小工作机制反推边界 | accepted | `01-decision/D-003-s2-minimal-work-mechanism.md` |
| D-004 | 2026-09-18 | Root 整体闭门 | accepted | `01-decision/D-004-root-closeout.md` |
