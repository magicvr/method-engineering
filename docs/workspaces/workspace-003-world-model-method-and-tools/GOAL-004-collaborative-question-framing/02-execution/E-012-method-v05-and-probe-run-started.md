---
title: 形成 v0.5 阶段一候选并启动第一例测试
status: recorded
created: 2026-09-27
updated: 2026-09-27
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: E-012
doc: execution-entry
---

# E-012 · 形成 v0.5 阶段一候选并启动第一例测试

### 2026-09-27 · 方法候选形成与阶段一测试启动

- 在 v0.3 的只读复核中，发现情境最小、停止与交接边界未说明，必要性删除测试可能假设创作者已作选择。Architect 建议收束为四组可往返认知操作，并给出未知项归属与定性停止边界；据此形成候选 v0.4。
- v0.4 复核发现输入被预先限定为“客观世界问题”，会排除尚待辨别的混合原问。修订为接受待分类的模糊原问、仅将客观节点交接 W2，形成 [v0.5.0](../attachments/stage1-cognitive-operations-candidate-v0.5.md)。标题版本错字已按复核修正。
- v0.5.0 仍是 `draft / unaccepted`，但已固定为第一例阶段一试跑的测试基线。它不包含“世界有多大”的具体分解、答案或模型。
- 使用平台内置 Worker 创建了隔离的只读任务，仅向其提供 v0.5 方法文件、原问“世界有多大？”和已确认上下文；任务要求不得读取工作区其他资料/旧探针结果，不得写文件，不得进入 W2。该 Worker 未使用仓库自定义 `worker.toml` 派发适配层（当前不可用）；未将此次内置角色调用称为自定义配置派发。
- 下一步：检查返回的阶段一操作证据；案例结果与方法证据分开记录。此轮不改 W2 答案/模型，不改变任何 Goal 状态或进度。
