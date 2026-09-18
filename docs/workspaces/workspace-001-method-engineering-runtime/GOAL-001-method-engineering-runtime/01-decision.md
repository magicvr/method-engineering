---
id: GOAL-001-method-engineering-runtime
doc: decision
status: active
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.2.0
---

# 决策记录 · GOAL-001

## 纲领路线图与阶段计划

Root 采用 `S1 冻结运行模型 → S2 落盘最小工作机制 → S3 机制 walkthrough 与交接` 的串行路线图。纲领路线图的权威在 `00-meta.md`；本文件只登记阶段计划和影响范围的决定。

## 信息需求与阶段门禁

| ID | 级别 | 所需信息 / 假设 | 影响门禁 | 最晚需要阶段 | 验证 / 收集动作 | 状态 | 延期 / 复核 | 证据 / 决策 |
|----|------|-----------------|----------|--------------|-----------------|------|-------------|-------------|
| I-001 | required | 最小运行状态、转换、责任边界和追踪语义。 | 方案冻结、S1 退出 | S1 | 形成运行模型并做机制内部一致性检查。 | verified | 不延期；已在 S1 关门时处理。 | D-002 v0.4.0、E-003 v0.4.0、A-008 self `pass`、A-009 Grok independent `pass`、A-010 closeout；无新的 required finding。 |
| I-002 | required | 最小工作对象、记录边界、目录承载和流程文档。 | 实施、S2 退出 | S2 | 已从运行责任逐项反推，完成对象/承载方案、流程说明落盘和关门核对。 | verified | 不延期；已由 A-011 关闭。 | `GOAL-002-s2-minimal-work-mechanism` 的 I-201、D-002、D-003、A-001～A-003；`runtime-records/README.md`；`03-audit/A-011-s2-closeout.md`。 |

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-09-18 | 工作区启动边界与 Root 路线图 | accepted | `01-decision/D-001-bootstrap-scope.md` |
| D-002 | 2026-09-18 | S1 需求—响应运行模型与交叉审计路径 | accepted | `01-decision/D-002-runtime-model.md` |
| D-003 | 2026-09-18 | S2 启动与最小工作机制反推边界 | accepted | `01-decision/D-003-s2-minimal-work-mechanism.md` |
