---
id: GOAL-001-enter-real-operation
doc: decision-entry
record_id: D-001
status: accepted
parent: null
created: 2026-09-14
updated: 2026-09-14
version: 0.1.0
---

## D-001 · 开设工作区并登记 S1 信息门禁

### 触发

用户在 `/vision` 响应 VRev-002 并激活 VP 之后，明确指令交 `/govern` 开设工作区。VRev-002 `V-F-001` / `V-F-002` 已按 `fixed` 闭合，开区门禁解除。

### 决定

1. 建立本仓库首个显式工作区 `workspace-001-enter-real-operation`，`vision_role: primary`，`shared_materials_catalog: none`。
2. Root 为 `GOAL-001-enter-real-operation`，`parent: null`，标题与 VP 意图一致：「让方法工程进入真实运行」。
3. `plan_refs` / `primary_plan` 均挂 `VP-001-enter-real-operation`。
4. 工作区与 Root slug 由**已确认**的 VP id `enter-real-operation` 派生，不是 `main-vision` 一类静默占位。
5. 本回合只 scaffold 工作区 + Root 五件套 + 纲领路线图 S1–S3 + 信息登记；**不**创建 Method Case 子目标，**不**预先扩展启动机制。
6. 将 VP 前提 A-001 登记为 Root `I-001`（required，最晚 S1 方案冻结 / 开始使用前）。另登记 `I-002`：首个 Method Case 选题与边界（required，最晚 S1 开始使用前）。

### 为什么

- 冷启动串行要求 Charter → VP → 工作区 + Root。VP 已 `active`，实现层必须有唯一 canonical 区承接证据。
- slug 必须可追踪且经用户意图确认；本轮用户未另给新 slug，采用与已确认 VP 相同的 `enter-real-operation`，避免发明第二套名称。
- P-001：Root 尚不可直接执行，先写纲领路线图再按阶段立项。
- P-005 / V-F-001：机制基线不可在愿景层假装已可核对，必须进入本区信息门禁。

### 未选方案

- 使用 `main-vision` 或其他示例占位 slug：违反 S0 禁止静默占位。
- 另起与 VP 无关的工作区名：本轮用户未提供新名，且会切断与 VP-001 的对应。
- 先建 Case 子目标再写路线图：违反 P-001。
- 把 A-001 写成已验证，或接受 V-F-002 residual 而不落回 `docs/contracts/`：与本轮「响应并开区」的 `fixed` 路径相反。
- 将 VP 标 `active` 却不开区：触发空转规则，且无法收集 D1 证据。
