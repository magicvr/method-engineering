---
title: A-008 响应闭合核验
status: active
created: 2026-10-04
updated: 2026-10-04
parent: null
version: 0.1.0
record_id: A-010
source: independent
date: 2026-10-04
scope: A-008 F-001～F-007 响应与 D-028 冻结条件
verdict: reject（REJECT；F-003 部分、F-004 矛盾、VP 版本展示 minor）
---

# A-010 · A-008 响应闭合核验

## Findings

### MAJOR

1. F-003 仅部分修正：草案只写“十一项排除继续有效”“缺口次序保留”，没有把排除和缺口检查写成可核对条目；正向链路直接进入模型构建。
2. F-004 矛盾：投入上限已记录为 user-overruled，但 §14 仍要求用户确认首轮投入上限；§1/§9/§14 仍把 VP 澄清写成候选或待裁决，而 D-030 已 accepted、VP 已 v0.1.2。

### MINOR

3. VP 版本展示未完全同步：workspace.md 规划对齐行与 goal-tree.md primary_plan 摘要仍写 v0.1.1。

## Verified

- F-001 fixed：回答成立判定已写入。
- F-002 fixed：初始验收与长期观察标准已分开。
- F-005 fixed：运行时交互移出失败清单。
- F-006 fixed：适用层级已写入。
- F-007 fixed：附件 draft 与 D-028 proposed 对齐。
- VP-003 v0.1.2 能力表述与 D-030 一致；非 strategic，方向结构未改。
- RUN-001 仍为 failed；R4 未放行。

## Verdict

REJECT。F-003 未完整 fixed；F-004 留痕存在但文本仍自相矛盾。修正后可支持提交用户确认冻结 D-028。
