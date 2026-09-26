---
work_item_id: WRK-002-world-model-method-and-tools
status: 已接受
created: 2026-09-26
updated: 2026-09-26
---

# WRK-002 · 为 WorldModel.ModernCultivation 构建世界模型的方法与工具

## 当前状态

- **状态**：已接受
- **最近状态依据**：[events.md](events.md) 的 EV-002（2026-09-26 形成处理承诺）
- **处理承诺**：在已确认的边界与限额内，为下游交付「世界模型构建方法工作版 + 配套工具」（工具形态在澄清阶段按需求原文 §9 界定），并在至少一个真实世界问题上有界检验后完成交付、收件、验收/异议与结束回路。**尚未开始具体响应**。
- **具体授权依据**：[D-001](../../docs/workspaces/workspace-003-world-model-method-and-tools/GOAL-001-world-model-method-and-tools/01-decision/D-001-accept-wrk002-and-open-workspace.md)；用户 2026-09-26 的显式指令（提报 → 正式承接 → 新开 VP 与工作区）。

## 当前需求与限额

下游 `WorldModel.ModernCultivation` 在真实创作实践中需要一套**按需世界模型方法**：创作中遇到关于世界客观规律、客观状态或交互结果的问题时，判断现有世界模型能否裁决；不能时识别所缺是状态、组合、精度还是机制，并以最低必要成本补足可复用的机制模型。需求原文（原文，非摘要）见下游仓 `exchange/WRK-002-world-model-method-and-tools/需求-2026-09-26.md`。

限额：一条处理主线（`WRK-002`）；交付「方法工作版 + 配套工具」并在至少一个真实世界问题上有界检验。**不包含**：替下游编写 `world/` 设定正文或 canon；替下游裁决其承载未知（`U-1`～`U-8`）；承诺方法普遍有效；承诺工具被下游启用；建设 API / Web UI / 自动化派发或跨仓同步服务；领域有效性的大规模实验。超出此范围须重新澄清并取得新的授权。

## 责任、承载与验证

- 需求方、授权人、接收与验收责任：用户（真实实践方，亦为两仓维护人）；响应与运行记录：方法工程响应负责人。每次执行标明角色切换。消费方动作经用户当次授权由执行助手代行并逐条标明；代行不构成独立团队共识，也不替代用户本人的价值判断。
- 下游选择：`exchange/WRK-002-world-model-method-and-tools/`；Markdown / UTF-8 无 BOM / LF；人工阅读核对、不新增工具（除非澄清阶段另行确认）；多轮材料并存不覆盖。下游约定见其 `exchange/README.md` 与 `D-006` / `D-007` / `D-009`。
- 最低核对：同一追踪线上的需求、澄清与授权、接受承诺、响应版本与验证、交付、实际收件、验收或异议、反馈路由与结束；响应包须明确版本、适用条件、验证结论与证据、限制、未决事项与后续责任。
- 沟通：当前协作与 exchange 材料；重要转换或需要对方行动时更新，下一更新触发为下一交接动作或用户回复。
- 留存：本仓只留去标识化摘要、协议过程、结果与路径/版本引用；不复制原始个人或敏感材料。下游需求原文由下游仓留存，本记录不复制全文。

## 来源与追溯

- 提报：下游于 2026-09-26 提报，work-item id `WRK-002-world-model-method-and-tools`（由方法工程在受理登记时分配，用户本轮确认）。下游提交事实见其 `D-002` / `E-002`，提交 `7324bdf`（分支 `dev/vp-002`），材料路径 `exchange/WRK-002-world-model-method-and-tools/需求-2026-09-26.md`（`material_status: 原文`）。
- 下游治理：`WorldModel.ModernCultivation` 的 `docs/workspaces/workspace-002-world-model-method-acquisition/GOAL-001-world-model-method-acquisition/`，挂 `VP-002-world-model-method-acquisition`（`active`，`vision_ref: vision-modern-cultivation@0.2.0`），纲领 M1 → M2。
- 下游澄清：其 `I-001`（首个真实世界问题）属其与其**自身作品侧下游**之间的消费链问题，不是本次跨仓提报的前提；具体首个裁决案例登记为其 `I-011`，最晚 M2 检验前选定。
- 本仓治理：`workspace-003-world-model-method-and-tools` / `GOAL-001-world-model-method-and-tools`（挂 `VP-003-world-model-method-and-tools`）；唯一当前运行状态在本文件，`events.md` 仅历史。
- 前驱：`WRK-001-world-model-demand-method` 已于 2026-09-26「已退出」，其原领域方法需求未获接受或交付；本记录即该需求另建的处理主线，不复用、不重置旧记录。

## 当前结果与下一责任

2026-09-26 受理并形成处理承诺（EV-002）；**尚无**响应、验证、交付、实际收件、验收或退出事实。下一责任：在 `workspace-003` Root 的 R1 阶段与下游澄清并冻结需求边界、交付形态、工具形态与检验用例（`I-001`～`I-003`），随后进入响应。本记录的状态转换须与触发动作同批落盘。
