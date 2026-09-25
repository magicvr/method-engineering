---
id: GOAL-001-consumer-response-protocol
doc: decision-entry
record_id: D-001
status: accepted
parent: GOAL-001-consumer-response-protocol
created: 2026-09-25
updated: 2026-09-25
version: 0.1.0
---

## D-001 · 工作区开设边界、Root 纲领路线图与 vision primary 转移

### 触发

- 用户本轮指令：先以 `/vision` 激活 `VP-002-consumer-demand-response-protocol`，再交 `/govern` 开设工作区，最后做一次 git 提交。
- 愿景扫描：唯一 active Charter `method-engineering@0.1.0`；VP-002 `vision_ref` 精确匹配；`reviews.md` 开放 VRev required = 0（VRev-003 三条 recommended 已 `fixed`），激活与开区门禁不阻断。
- 前置状态：VP-001 已 `closed`，`workspace-001-method-engineering-runtime` 已 `archived` 且仍声称 vision 层 `primary`；Charter `primary_workspace` 亦指向该归档区。
- 用户裁决（本轮确认）：工作区 slug 取 `workspace-002-consumer-response-protocol`、Root slug 取 `GOAL-001-consumer-response-protocol`；`vision_role` 取 `primary`，并把归档的 workspace-001 降为 `delivery`；收尾提交合并已暂存的 VP-002 文件与本轮改动为一次提交。

### 决定

1. VP-002 由 `planned` 激活为 `active`（`version: 0.2.0`），写入 `lead_workspace`，登记绑定表与修订短史。
2. 开设 `docs/workspaces/workspace-002-consumer-response-protocol/`，创建 Root `GOAL-001-consumer-response-protocol`（`parent: null`，初始 `status: draft`），`plan_refs` / `primary_plan` 均为 `VP-002-consumer-demand-response-protocol`。
3. Root 采用 R1 → R2 → R3 串行纲领路线图，登记 I-001～I-005 信息项（I-001/I-002 卡 R2、I-003 卡 R3、I-004 卡 R1 方案冻结、I-005 非阻断）。
4. vision 层唯一 `primary` 转移：`workspace-002` 记 `primary`；`workspace-001` 的 `vision_role` 改为 `delivery`；Charter `primary_workspace` 改为 `workspace-002-consumer-response-protocol`；`workspaces.md` 同步；该 Charter 元数据变更记为 `VR-004`（editorial）。
5. 开区不启动 R1 实施：进入 R1 实施前须先由用户确认实施前审计模式（初步建议 `cross`）并落盘。

### 为什么

- VP-002 是本轮唯一 active VP，其工作区应是 vision 层声明的主承载；alignment §3 要求至多一个工作区为 `primary`，因此必须同时改正 workspace-001 的角色，而不能出现两个 `primary` 声明（否则按 §3.1 fail closed）。
- 冷启动/开区顺序要求「已落盘 VP → 工作区 + Root」，且工作区必须挂 `plan_refs` / `primary_plan`；VP-002 已在 VRev-003 后落盘且无开放 required，满足开区门禁。
- VP-002 的方向级退出判据 5 要求真实试跑，而真实实践方、试跑仓库、真实需求与授权均未指定；按 P-005 必须把未知登记为信息项并设定门禁，而不是在开区时假装条件已具备。
- 激活瞬间 VP 绑定区数为 0，按 alignment §5.1 需告警；本轮由用户确认的工作区挂接在同一轮内消除空转，故不申请空转宽限。

### 未选方案

- **workspace-002 取 `delivery`、workspace-001 与 Charter 不动**：改动最小，但会使 vision 层 `primary` 长期指向已归档、不接收新工作的区，与实际承载现行 active VP 的区不符；用户已选择转移 primary。
- **新建 `primary` 而不改 workspace-001**：会形成两处 `primary` 声明（不同 `workspace_id`），按 alignment §3.1 属 fail closed 的冲突，不能采用。
- **开区同时启动 R1 实施**：R1 实施前需先定审计模式（P-004 3.1），且 I-004 仍是 open required；本轮只开设并登记，不越门禁推进。
- **Root 直接取 `active`**：本轮只完成开设与登记，尚无实施事实；按原语默认取 `draft`，待 R1 启动时再变更并同步 `goal-tree.md`。
