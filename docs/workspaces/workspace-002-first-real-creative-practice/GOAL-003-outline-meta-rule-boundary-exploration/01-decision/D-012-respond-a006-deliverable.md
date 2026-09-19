---
id: D-012-respond-a006-deliverable
doc: decision-entry
status: accepted
parent: GOAL-003-outline-meta-rule-boundary-exploration
created: 2026-09-19
updated: 2026-09-19
version: 0.1.0
---

# D-012 · 响应 A-006：修订可交付响应为 v1.1.0

## 决定

响应 [`A-006-min-background-world-model-deliverable-review.md`](../03-audit/A-006-min-background-world-model-deliverable-review.md)。路径为 `fixed`，不走 residual / overruled。使用文本改为 [`attachments/min-background-world-model-method.md`](../attachments/min-background-world-model-method.md) **v1.1.0**。v1.0.0 不再作为使用文本。D-011 的 P3 退出与「P4 未开始」仍有效；本条只修正交付物语义，不启动 P4。

1. **F-001（required）**：D 定义为「当前工作世界模型明确采用的、相对于 R 的偏离」。区分为已确认 D 与暂定 D。暂定 D 不得称为已成立世界事实；由其推出的 W 随暂定。
2. **F-002（required）**：D 对其声明覆盖的 R 默认进行替换，不构成 C。C 仅用于未覆盖前提不兼容，或 D/D、D/W、W/W 互斥。
3. **F-003（required）**：推论针对每条 D，或产生直接后果所需的最小 D 集合 \(D^*\)。W 依据可为 D-id 集合。有界改为禁止用 W 再推 W，不限制联合前提数量。
4. **F-004（required）**：废除「书面声明暂不决定仍进入」作为 Q2 豁免。若 U 的不同答案使主题选择实质分叉且无法在未知下开始，Q2 必须为 no。仅当主题选择对该 U 不敏感时，才允许 deferred。
5. **F-005～F-008（recommended，一并吸收）**：区分显式记录与模型语义；Q2 收紧为「足以开始主题选择、无需先补新的背景世界事实」；`collecting` 仅为过程状态；重开限于会改变已有默认或主题选择能否开始的新 D；「未写入的维度」改为刻意未展开，不是完整性清单。

A-006 原文与 `conditional` verdict 保留。本拍不向 book_green 交付。

## 理由

四条必改都指向执行一致性：假设洗白、合法覆盖被当成冲突、联合一阶后果推不出、主观豁免绕过停止。不修就进入 P4，不同执行者会对同一输入得到不同世界事实。建议项与必改同向，一并写入 v1.1.0 成本低于留到使用后再改。

无与 A-002 必改项的相反结论。A-005 的 P3 退出是内部产出门禁；A-006 阻断的是向作品仓冻结 1.0.0。本条把使用文本从 1.0.0 换成 1.1.0，不把 P3 打回重做。

## 未选方案

| 方案 | 未选理由 |
|------|----------|
| 驳回 F-001～F-004 或接受残余 | 四处都是文本可改的语义漏洞，没有需要保留的残余收益。 |
| 只改说明、不改步骤与表格 | 漏洞在准入、覆盖、推论范围和 Q2 判定，不改操作句仍会执行错。 |
| 本拍同时开始 P4 交付 | 用户只要求响应 A-006；修正后才具备向作品仓推进的条件。 |
| 改写 A-006 原文或其 verdict | 独立意见只出意见。 |

## 影响

- A-006 F-001～F-004 编排侧记为 `fixed`，待独立 finding-closure 复核。
- F-005～F-008 一并吸收。
- P4 不再被这四条 required finding 阻断；是否立刻交付由下一拍决定。
- G-003 保持 `verified`（内部步骤与走查范围不变）；使用文本版本改为 1.1.0。

## 后续

指定 provider 对 F-001～F-004 做 independent finding-closure；或直接开始 P4，将 v1.1.0 交给 book_green 使用。本条不自动启动 P4。

## 依据

- GOAL-003 A-006。
- 维护者要求响应该独立意见。
- [`D-011-p3-3-deliverable.md`](D-011-p3-3-deliverable.md)。
---
