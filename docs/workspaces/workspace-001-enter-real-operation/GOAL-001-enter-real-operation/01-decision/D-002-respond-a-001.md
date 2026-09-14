---
id: GOAL-001-enter-real-operation
doc: decision-entry
record_id: D-002
status: accepted
parent: null
created: 2026-09-14
updated: 2026-09-14
version: 0.1.0
---

## D-002 · 响应 A-001：按 fixed 重写成功边界与纲领阶段主语

### 触发

独立审计 [`A-001-root-intent-alignment.md`](../03-audit/A-001-root-intent-alignment.md)（`source: independent`，`verdict: conditional`）提出三条同向 required findings：`F-001`、`F-002`、`F-003`。用户本轮指令：`/govern 响应独立审计A-001`。无冲突意见；用户未要求 residual 或 overruled。

### 决定

对 `F-001`～`F-003` 全部走 **`fixed`**，不接受残余、不驳回降级。

1. **F-001**：Root 成功边界的主语改为「方法工程已进入并能够继续真实运行」。启动条件（`I-001` 基线、`I-002` 首个 Case）保留为必要但不充分；关门不可替代的组成改为：有边界的实际方法工程工作、可评价工作结果、反馈进入后续工作、分层纪律、仅在必要缺口后修正机制。
2. **F-002**：保持三阶段数量，改写阶段主语与退出语义：
   - S1 · 建立运行基线 ↔ VP D1
   - S2 · 真实运行 ↔ VP D2（观察与分层改为工作中的反馈，主语是解题）
   - S3 · 收束与继承 ↔ VP D3
   解题是主过程；不把 Case 写成观察框架的手段。
3. **F-003**：新增 `I-003`（required，最晚 S3 / Root 关门）：对本轮候选运行资产逐项 `Promote` / `Retain as experimental` / `Archive` / `Discard`。不预先承诺任何资产必然 Promote。
4. 本回合**不**冻结 S1 方案、**不**选定 Method Case、**不**把 `I-001`/`I-002` 标为 verified、**不**改 `status`、**不**宣称已进入真实运行。

### 为什么

- 审计结论是定义收缩，不是方向相反；`fixed` 与用户「响应」指令、审计建议的默认路径一致。
- Charter 已冻结「演化服务于解题」；若不改阶段主语，S2/S3 会把真实工作降为机制观察。
- 无继承裁决则下一 Intent / Case 没有权威起点。

### 未选方案

- `accepted-residual`：用户未书面接受过窄成功边界；该残余会在关门时把「跑完一个 Case + 机制看起来够用」当成完成。
- `user-overruled`：用户未驳回这三条 finding。
- 增加阶段数量或拆成新 VP：审计明确不必增加阶段；结构选型仍落在本 Root。
- 把 `I-001`/`I-002` 当作 Root 完成充分条件：正是 F-001 要防止的收缩。
