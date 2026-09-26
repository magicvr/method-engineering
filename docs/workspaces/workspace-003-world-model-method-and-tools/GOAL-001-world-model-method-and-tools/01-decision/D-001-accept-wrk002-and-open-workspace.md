---
id: GOAL-001-world-model-method-and-tools
doc: decision-entry
record_id: D-001
status: accepted
parent: null
created: 2026-09-26
updated: 2026-09-26
version: 0.1.0
---

## D-001 · 受理 `WRK-002` 真实需求并开设 workspace-003

### 触发

用户 2026-09-26 明确指令：由下游仓 `WorldModel.ModernCultivation` 正式提报「构建世界模型的方法和工具」需求，本仓正式承接，并以一个新的 VP 和工作区承载该方法和工具的构建，完成后交付给下游；并显式授权双仓操作权限，要求「如有问题，向用户询问，而非自行静默裁决」。用户已就提报材料形态、角色授权、承接边界、命名与结构、VP 状态与 Vision Review、Git checkpoint 逐项裁决。

同时，下游已于同日完成提报并落盘需求原文于其 `exchange/WRK-002-world-model-method-and-tools/需求-2026-09-26.md`（提交 `7324bdf`，分支 `dev/vp-002`，`material_status: 原文`）。

### 决定

1. **受理**：`WRK-002-world-model-method-and-tools` 由「待判定」转为**「已接受」**；运行主记录为 [`runtime-records/WRK-002-world-model-method-and-tools/record.md`](../../../../runtime-records/WRK-002-world-model-method-and-tools/record.md)，事件见其 `events.md` 的 EV-001 / EV-002。
2. **承接边界**：在限额内交付「世界模型构建方法工作版 + 配套工具」，在至少一个真实世界问题上有界检验，并完成交付 / 实际收件 / 验收或异议 / 反馈路由 / 结束回路。工具形态在 R1 澄清阶段按下游需求原文 §9「结构化和工具化只在重复使用确有价值后进行」界定。**不含**：替下游编写 `world/` 设定正文或 canon、替其关闭承载未知 `U-1`～`U-8`、承诺方法普遍有效、承诺工具被下游启用、建设 API / Web UI / 自动化派发或跨仓同步服务。
3. **角色与授权**：需求方、授权人、接收与验收责任人均为用户（两仓维护人）；响应与运行记录为方法工程响应负责人。助手的每项代行须逐次授权并逐条标明，代行不构成独立团队共识，也不替代用户本人的价值判断。
4. **愿景层**：落盘 `VP-003-world-model-method-and-tools`（`v0.1.0`），`status: active`，`vision_ref: method-engineering@0.1.0`，`lead_workspace` 为本区；追加 self Vision Review `VRev-006`（`pass`，`V-001`/`V-F-002` 两条 recommended，无 required）；刷新 `roadmap.md` 与 `reviews.md`。同轮将 `primary_workspace` 由 `workspace-002-consumer-response-protocol` 改为本区，并把 `workspace-002` 的 `vision_role` 改为 `delivery`（editorial，`VR-006`，Charter 版本仍为 `0.1.0`）。
5. **工作区与 Root**：开设 `workspace-003-world-model-method-and-tools`，Root 为 `GOAL-001-world-model-method-and-tools`（`parent: null`，`status: active`），`plan_refs` / `primary_plan` 均为 `VP-003-world-model-method-and-tools`，`shared_materials_catalog: none`。
6. **可执行纲领**：Root 纲领路线图为 **R1 → R2/R3 → R4**（与 VP 方向级阶段同名、不同层）。`progress: 0%` 来自 0/4。本回合只登记路线图与信息表，**不创建子目标**。
7. **信息门禁**：登记 `I-001`（R1 冻结结论）、`I-002`（有界检验用例）、`I-003`（工具是否引入及最小边界）、`I-004`（R4 交付前独立审计模式与 provider），均 `open`，按 P-005 写明影响门禁与最晚需要阶段。`I-001` 阻断 R1 冻结；`I-002` 不阻断开区；`I-004` 到达 R4 前台。
8. **承载与引用**：下游选择 `exchange/WRK-002-world-model-method-and-tools/`、Markdown / UTF-8 无 BOM / LF、人工核对、不新增工具（除非澄清阶段另行确认）、多轮并存不覆盖；跨仓引用一律写「仓库 + 提交 + 路径」，不写本机绝对路径。
9. **审计模式**：本轮（开区、受理、VP 落盘）为 `self`。R4 交付前的高影响门禁按 `I-004` 由用户指定 provider 执行独立审计；provider 不可用、失败或无输出时门禁保持未满足，不得静默降级或由编排器冒充。
10. **Git checkpoint**：两仓在每个阶段落盘后建立 checkpoint，只 `git add -- <显式 owned paths>`，禁止 `git add -A`；commit 仅作恢复点，不作为审计、实现或放行依据。

### 为什么

- 用户明确指令要求「正式承接」并「开始对应的 vp 和工作区」，因此受理承诺与结构落盘在同一轮内完成，而不是先只登记「待判定」。
- 下游 `VP-002-world-model-method-acquisition` 判据 2 要求方法工作版与配套工具**都可验收**，其判据 3 才是 `U-1`～`U-8` 关闭；本 VP 的判据 2/3 与之一致，但两边保持各自的状态权威与门禁，不在本仓替下游放行。
- `WRK-001` 已「已退出」，其原领域方法需求未获交付且明写须另建主线；本条正是该主线，故**不复用**旧记录、不恢复旧授权，只引用其历史。
- `active` VP 若零绑定会触发空转规则，因此在同一轮内完成 VP 落盘与工作区绑定，不申请空转宽限。
- 把「工具形态」放在 R1 澄清而不是本决定，是因为下游需求原文 §9 与 VP-002 判据 2 的口径需在双边澄清中一次对齐，不在本仓单方面冻结。

### 未选方案

- **先只登记「待判定」、另轮再受理**：未选。用户明确要求本轮「正式承接」。
- **复用或重开 `WRK-001` 主线**：未选。其已为终态「已退出」，按运行协议不得复用或重置，也不得自动恢复旧授权。
- **把新工作区设为 `delivery`、`workspace-002` 保持 `primary`**：未选。用户选择切换 primary，与本仓 `VR-004` 先例一致，使 vision 层唯一 `primary` 指向承载现行 `active` VP 的区。
- **本轮不加 Vision Review**：未选。用户选择落盘即 `active` 并追加 self `VRev-006`。
- **本轮创建 R1/R2 子目标**：未选。`I-001` 尚未冻结，先写纲领路线图与信息表；子目标待 R1 结论明确后再按阶段创建。
- **把工具形态在本决定中直接冻结为「完整配套工具」**：未选。与下游需求原文 §9 的时序保留冲突，须先澄清。

### 影响

- 新增：`docs/vision/plans/VP-003-world-model-method-and-tools.md`、`docs/vision/reviews/VRev-006-*.md`、本工作区（`workspace.md`、`goal-tree.md`、Root 五件套）、`runtime-records/WRK-002-world-model-method-and-tools/`。
- 修改：`docs/vision/roadmap.md`、`docs/vision/reviews.md`、`docs/vision/charter.md`（`primary_workspace`）、`docs/vision/revisions.md`（`VR-006`）、`docs/vision/workspaces.md`、`docs/workspaces/workspace-002-consumer-response-protocol/workspace.md`（`vision_role` → `delivery`）。
- 跨仓：本仓向下游 `exchange/WRK-002-world-model-method-and-tools/` 投放「澄清与授权」材料；下游据此在 `E-003` 记录收件与受理承诺，并把其 `I-002` 置 `verified`。
- 未发生：方法响应、验证、交付、实际收件、验收或退出**均未发生**；本决定不推导其中任何一项。

### 后续

- 事实见 `02-execution/E-001-workspace-open.md` 与 `02-execution/E-002-wrk002-acceptance.md`。
- 下一责任：R1 与下游澄清并冻结 `I-001` / `I-003`，随后按阶段创建子目标并进入 R2。
