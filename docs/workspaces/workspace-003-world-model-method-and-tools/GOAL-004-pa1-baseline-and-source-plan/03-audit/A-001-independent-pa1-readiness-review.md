---
title: PA1 S1/S2 与来源裁决包独立审查
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.0
record_id: A-001
source: independent
date: 2026-10-04
scope: GOAL-004 S1/S2 中间产物、S3 来源方案与 S4 待裁决包
verdict: fail
---

# A-001 · 独立审查

## 原始意见（REJECT，保留）

独立 REVIEWER 判断：现有裁决包不能直接作为“用户选择 J-01～J-03 后即冻结 S3、进入 S4 放行”的充分依据。基线与迁移矩阵主体可保留，但必须修正一条 required 与两条登记错误。

### F-001 · MAJOR / required

**问题**：J-02-A 把“用户授权本次研究读取”与“来源权限已核实”混为一体，且拟将权限不确定性留到 PA2，不能支撑 S3 冻结或 I-007 关闭。

**证据**：[source-and-access-plan-v0.1.md](../attachments/source-and-access-plan-v0.1.md) J-02 与 [s3-s4-user-decision-request-v0.1.md](../attachments/s3-s4-user-decision-request-v0.1.md)；对照约束迁移矩阵 C-07/C-14/C-22 与 GOAL-004 S4 退出条件。

**最小修正**：明确两条分支：①补齐权限依据；②用户明确接受有范围、期限、复审触发、责任人和缓解措施的残余风险。残余不等于 verified，也不自动关闭 I-007。

### F-002 · MINOR

**问题**：[pa1-frozen-baseline-v0.1.md](../attachments/pa1-frozen-baseline-v0.1.md) 登记的提取文件 SHA-256 末段错误。

**最小修正**：改为实际值 `A9A2D015ABE6A8B871AEE8C0781A5945E640F23E17369DB81022B24F7EE49C89`。

### F-003 · MINOR

**问题**：[E-002](../02-execution/E-002-complete-s1-baseline-and-s2-migration.md) 登记的 checkpoint commit 全哈希不存在；[E-001](../02-execution/E-001-establish-pa1-goal-and-fix-requirement-source.md) 的 checkpoint 前存在控制字符。

**最小修正**：E-002 改为实际对象 `cd24d518a6ba7e58384a0675d68d012ccd611859`；E-001 恢复为正常哈希文本。

## Verified

- 需求 `7324bdf` 与澄清 `e9054c9` 的 blob、本地文件一致。
- R1、旧 H 快照的 blob/SHA-256 与冻结基线一致。
- §10/§13 与 H1/H2/H3 提取未发现篡改或遗漏。
- 旧 H 9 格、180 分钟、预登记和 D-011 标签未被错误迁移到 prior-art。
- Root I-007、GOAL-003 PA1、PA2 的状态未被越阶放行。

## Unable to verify

- 未独立重现全部外部来源访问状态。
- 未独立重验历史用户授权对话原文。

## 编排响应（独立闭合核验通过）

2026-10-04 已实施局部修正：

- F-001：来源方案已拆分“研究读取授权”和“权限核实”；J-02-A 改为有范围、期限、复审触发、责任人和缓解措施的 `accepted-residual` 路径，并明确不写成 `verified`；S4 退出条件同步区分 verified/residual；裁决请求声明用户选择本身不关闭 I-007。
- F-002：已更正提取文件 SHA-256。
- F-003：已更正 checkpoint commit，并清除控制字符。

[A-002](A-002-independent-closure-verification.md) 为独立 REVIEWER 的第二次只读核验，确认 F-001/F-002/F-003 均已合法 `fixed`。本条原始 `fail` / REJECT 保留；本响应只登记闭合状态，不构成 S3 冻结、I-007 关闭、PA1 退出或 PA2 放行。