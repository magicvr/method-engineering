---
id: D-001-vp-002-root-scope
doc: decision-entry
status: accepted
parent: null
created: 2026-09-18
updated: 2026-09-18
version: 0.1.0
---

# D-001 · VP-002 工作区与 Root 开区边界

- **日期**：2026-09-18
- **状态**：accepted
- **决策来源**：用户确认采用推荐方案

## 决定

1. 为 VP-002 新建显式 `delivery` 工作区 `workspace-002-first-real-creative-practice`。
2. 在该区建立 Root `GOAL-001-first-real-creative-practice`，初始状态为 `draft`。
3. 将真实作品仓、当前状态、范围、接受条件、协作责任和投入限额登记为 Root 的 P-005 required 信息项；真实作品仓未定不阻止先建立工作区，但阻止将 D1 写成已完成或进入受其影响的实施门禁。
4. 具体需求 Goal 不在本次开区时预先创建，待真实、已接受且具有独立方法工程边界的需求出现后再按 P-001 立项。

## 理由

VP-002 已完成愿景层激活且 `open required: 0`。新建 delivery 区可以保留已归档 `workspace-001-method-engineering-runtime` 的历史 `primary` 声明，避免把 VP-001 的历史实现区重新塞入 VP-002，也不把未确认的作品事实伪装成当前运行事实。

## 未选方案

- **将新区声明为 `primary`**：需要迁移 Charter、愿景工作区索引和主声明，改变范围较大；本轮不采用。
- **复用已归档的 `workspace-001`**：该区已声明不接收新工作，且其 `plan_refs` 绑定 VP-001；本轮不采用。

## 影响与后续

- 工作区与 Root 已建立后，下一步先完成 I-001～I-005 的信息确认；未确认前不创建具体需求子目标。
- 若真实作品下一阶段不符合 VP-002 已冻结的终点，回流 `/vision` 修订 VP-002，不扩张「大纲」语义或要求作品适配预设流程。
