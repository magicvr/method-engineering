---
doc_type: vision-revisions
title: Charter 修订台账
status: active
created: 2026-09-14
updated: 2026-09-25
version: 0.4.0
parent: null
---

# Charter 修订台账

> 本文件只记录现行 Charter 的后续修订，编号使用 `VR-NNN`；它与 Vision Review 的 `VRev-NNN` 分开编号。
> Charter 初建事实记录在下方，不将初建伪装成一次修订。

## 初建记录

| date | vision_id | version | summary |
|------|-----------|---------|---------|
| 2026-09-14 | `method-engineering` | `0.1.0` | 根据用户提供的愿景建立唯一 active Charter。 |

## 修订条目

| id | date | class | summary | impact | status |
|----|------|-------|---------|--------|--------|
| VR-001 | 2026-09-18 | editorial | 更新 Charter 中 VP/工作区当前状态，并登记已落盘的 VP-001；未改变目的、边界或非目标。 | Charter 状态说明 | applied |
| VR-002 | 2026-09-18 | editorial | 登记 VP-001 的首个 `primary` 工作区与 Root 已建立并绑定；未改变 Charter 目的、边界或非目标。 | 工作区绑定元数据 | applied |
| VR-003 | 2026-09-25 | editorial | 更新愿景关系说明，反映 VP-001 已 `closed`、其工作区已归档，以及后继 VP-002 为 `planned` 且尚未绑定工作区；未改变 Charter 目的、边界、非目标或 `vision_ref`。 | Charter 与 VP / 工作区当前状态说明 | applied |
| VR-004 | 2026-09-25 | editorial | 按用户确认登记 VP-002 已由 `planned` 激活为 `active` 并绑定新工作区；将 `primary_workspace` 由已归档的 `workspace-001-method-engineering-runtime` 改为 `workspace-002-consumer-response-protocol`，同步 `workspaces.md` 与 workspace-001 的 `vision_role`（`primary`→`delivery`），使 vision 层唯一 `primary` 指向实际承载现行 active VP 的工作区；未改变 Charter 目的、边界、非目标或 `vision_ref`。 | Charter `primary_workspace` 字段；VP-002 状态说明；工作区角色元数据 | applied |

## 使用说明

- `editorial` 修订用于不改变目的、边界或非目标的措辞、链接等维护。
- `strategic` 修订至少提升 minor 版本，并须记录影响范围、Vision Review 与 re-align 安排。
