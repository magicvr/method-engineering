---
id: D-003-s2-minimal-work-mechanism
doc: decision-entry
goal: GOAL-001-method-engineering-runtime
status: accepted
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.1.0
---

# D-003 · S2 启动与最小工作机制反推边界

## 触发与前置条件

- A-008 `source: self` 与 A-009 指定 Grok independent 均为 `pass`；A-009 无新的 required finding。
- `/govern` 按用户明确规则将 I-001 标为 `verified`，完成 S1，并进入 S2。
- I-002 是当前 S2 的 required 信息项，仍为 `open`；本决定不把它预先写成已知。

## 决定

S2 只根据 D-002 已冻结的运行责任反推出最小工作对象、记录边界、状态承载、仓库目录和必要流程文档。第一步是建立“运行责任 → 必要记录/承载”的可核对映射，再据此形成最小机制方案。

## 范围边界

- 必须覆盖：需求进入与接受、响应开始与候选响应、验证、交付、三类反馈、退出、责任交接和追踪问句。
- 不预先建立无法由运行责任推出的完整 Schema、方法知识库、自动化平台、并行调度协议或未来 Case 特殊对象。
- A-009 的两条 recommended 不作为 S1 关门阻断；只有 S2 责任反推实际需要时，才在 S2 的方案记录中处理。
- I-002 只有在最小对象、记录边界、目录承载和流程文档均有证据后才能关闭。

## 下一步

在 S2 内先记录运行责任清单及其最小记录需求，随后提出最小工作对象与仓库承载方案；方案冻结和实施前按风险确定相应审视路径。
