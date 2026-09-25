---
id: GOAL-001-consumer-response-protocol
doc: decision-entry
record_id: D-003
status: accepted
parent: GOAL-001-consumer-response-protocol
created: 2026-09-25
updated: 2026-09-25
version: 0.1.0
---

## D-003 · 协议指南生命周期与关门前升格

### 用户裁决与依据

用户于 2026-09-25 明确：协议指南属于 method-engineering 仓库，过程可暂存在 workspace-002；在 R3 试跑验收及指南验证后、GOAL-001 关门前升格到本仓共享位置。最终具体路径刻意留待 R3 提供证据后，以具体方案交用户裁决。

真实试跑仓库仍为 WorldModel.ModernCultivation；其 README 将仓库内容定义为世界模型正典，因此不把协议指南写入该仓。操作授权不改变该内容边界。

### 已接受的决定

1. R2/R3 在本目标 `attachments/consumer-response-protocol.md` 维护唯一协议草稿；该路径属于当前工作区 canonical 范围，尚未创建指南。
2. R2 顺序为编写草稿 → self + 上下文独立 Codex Reviewer 的 cross 审计 → 消费方确认可读可执行。跨边界运行协议按 P-003 采用 cross；此处无审计 verdict。R3 审计模式在真实需求 scope 明确后重新判定。
3. R3 试跑验收与指南验证完成后，提出一个具体本仓共享运行文档路径及迁移、引用核对方案，由用户确认，再升格唯一权威全文；此项必须在 Root 关门前完成。当前不选定或创建最终路径。
4. 升格后保留工作区决策、执行、审计作为治理证据，工作区以引用指向共享全文，不保留两份可编辑全文；运行状态继续以既有 `runtime-records` 单一主记录为准。
5. I-005 从 non-blocking/open 调整为 required/collecting，最晚门禁为 R3 升格、Root 关门前。归属与时点已确认不等于共享路径或迁移结果已验证。I-003 仍为 required/open。

### 未采用方案与范围限制

- 不把指南放入真实试跑仓库，避免违反其正典内容边界。
- 不以 `docs/shared-materials/` 充当共享运行文档位置：它提供候选来源库存，不是隐式公共运行区（`docs/architecture/workspace-protocol.md` §1、§5）。
- 当前指南尚未泛化为跨项目治理规则，不据此放入 `docs/architecture/`；也不放入 `skills/core` 并引入安装分发义务。
- 项目根 `runtime-records/README.md` 及仓库承载纠正先例说明运行文档可以属于仓库范围，但不直接决定指南最终路径。先例为 `docs/workspaces/workspace-001-method-engineering-runtime/GOAL-002-s2-minimal-work-mechanism/01-decision/D-004-s2-repository-hosting-correction.md`。

本决定仅调整指南交付生命周期与相应门禁，不增加子目标，不增加纲领阶段；Root 保持 active / 33%，R2 进行中，R3 未开始。
