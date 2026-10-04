---
id: GOAL-001-world-model-method-and-tools
doc: decision
status: active
parent: null
created: 2026-09-26
updated: 2026-10-04
version: 1.20.0
---

# 决策记录 · GOAL-001


## 当前摘要（2026-10-04）

现行实现路线以 Root [D-021](01-decision/D-021-prior-art-driven-implementation-reframe.md)/[meta](00-meta.md) 为准：R1、R2-PA、R2-W、R3 已完成，Root progress 80%（4/5）；R4 进入准备，正式用例原始输入已登记；I-002 case/authorization verified，I-004 外部审计模式已定但意见待产出。旧 GOAL-002 cancelled + terminated-by-reframe，历史 0/4；GOAL-003 已 done，GOAL-009 已 done。R1 只证明协议冻结，不证明理论/H 适用；历史 I-005 与 H3-SEM-001 仍 open，旧 H3 不得冻结/运行。本次 self 不替代 I-004 独立审计。以下带旧“当前/路线”的摘要保留为历史语境，不再授权旧 R2。

## 纲领路线图与阶段计划

唯一实时阶段表在 [meta](00-meta.md)；[D-021](01-decision/D-021-prior-art-driven-implementation-reframe.md) 取代旧 R2 实现路线，R1 保留。R2-PA 由 [GOAL-003](../GOAL-003-prior-art-replanning/00-meta.md) 承接；R2-W 工作版形成，R3 条件工具分支，R4 最终检验/交付。旧表/门槛可核对于 [历史基线](attachments/pre-reframe-root-baseline-v1.md) 和历史 D-002/D-019，不再授权旧路线。
## 信息需求与阶段门禁

权威信息表在 [00-meta.md](00-meta.md)。本文件不复制第二份表。

## 决策索引

| D-ID | 日期 | 标题 | 状态 | 文件 |
|------|------|------|------|------|
| D-001 | 2026-09-26 | 受理 `WRK-002` 真实需求并开设 workspace-003 | accepted | `01-decision/D-001-accept-wrk002-and-open-workspace.md` |
| D-002 | 2026-09-30 | 优先验证假设、失败转向的路线选择 | accepted | [D-002](01-decision/D-002-prioritize-hypothesis-validation.md) |
| D-003 | 2026-09-30 | 因回滚授权替换下游 R1 当前绑定 | accepted | [D-003](01-decision/D-003-rebind-r1-after-rollback.md) |
| D-004 | 2026-09-30 | 选择 R1 第一轮方法范围候选 | accepted | [D-004](01-decision/D-004-select-first-r1-scope-candidate.md) |
| D-005 | 2026-09-30 | 选择 H1/H2/H3 判据形成路径 | accepted | [D-005](01-decision/D-005-select-h123-criteria-path.md) |
| D-006 | 2026-09-30 | 选择按声明范围判定证据充分性 | accepted | [D-006](01-decision/D-006-select-claim-scoped-evidence.md) |
| D-007 | 2026-09-30 | 选择共享背景、分立 H 检验单元 | accepted | [D-007](01-decision/D-007-select-shared-test-context.md) |
| D-008 | 2026-09-30 | 将下游问题保留为草案程序黑箱探针 | accepted | [D-008](01-decision/D-008-hold-case-as-blackbox-probe.md) |
| D-009 | 2026-09-30 | 选择独立 Codex 首发 Skill 路径 | accepted | [D-009](01-decision/D-009-select-codex-first-method-skill.md) |
| D-010 | 2026-09-30 | 选择 H1/H2/H3 小型可行性工作量档 | accepted | [D-010](01-decision/D-010-select-small-r1-workload-profile.md) |
| D-011 | 2026-09-30 | 选择证据清单与创作者局部裁决判据形式 | accepted | [D-011](01-decision/D-011-select-checklist-creator-judgment.md) |
| D-012 | 2026-09-30 | 将 v0.6.2 设为 R1 当前两仓澄清引用 | accepted | [D-012](01-decision/D-012-update-current-r1-reference-v0-6-2.md) |
| D-013 | 2026-09-30 | 整理 R1 I-001 / I-003 未决项裁决清单 | accepted | [D-013](01-decision/D-013-prepare-r1-open-items-decision-brief.md) |
| D-014 | 2026-09-30 | 选择创作者主责的方法使用边界候选 | accepted | [D-014](01-decision/D-014-select-creator-primary-method-use.md) |
| D-015 | 2026-09-30 | 响应 A-002 并按阶段修正信息门禁 | accepted | [D-015](01-decision/D-015-respond-a002-stage-gates.md) |
| D-016 | 2026-09-30 | 裁决 R1 协议候选 v0.6.4 的边界与总量计法 | accepted | [D-016](01-decision/D-016-r1-protocol-v0-6-4.md) |
| D-017 | 2026-09-30 | 冻结 R1 方法协议与条件工具策略 v0.6.4 | accepted | [D-017](01-decision/D-017-freeze-r1-protocol-v0-6-4.md) |
| D-018 | 2026-09-30 | 关闭 R1 澄清与冻结阶段 | accepted | [D-018](01-decision/D-018-close-r1-stage.md) |
| D-019 | 2026-10-01 | 建立 R2 子目标并明确父子职责 | accepted | [D-019](01-decision/D-019-create-r2-delivery-goal.md) |
| D-020 | 2026-10-01 | 将“世界有多大”预留为 R2d 完整方法黑箱核对 | accepted | [D-020](01-decision/D-020-reserve-r2d-full-method-blackbox-probe.md) |

| D-021 | 2026-10-04 | 成熟理论驱动实现路线 reframe | accepted | [D-021](01-decision/D-021-prior-art-driven-implementation-reframe.md) |
| D-022 | 2026-10-04 | 完成 R2-W 并启动 R3 | accepted | [D-022](01-decision/D-022-complete-r2w-and-start-r3.md) |
| D-023 | 2026-10-04 | 建立 R3 工具分支评估子目标 | accepted | [D-023](01-decision/D-023-create-r3-tool-branch-evaluation.md) |
| D-024 | 2026-10-04 | 完成 R3 并保持 R4 门禁 | accepted | [D-024](01-decision/D-024-complete-r3-and-hold-r4.md) |
| D-025 | 2026-10-04 | 选择 R4 原始用例并指定外部审计模式 | accepted | [D-025](01-decision/D-025-select-r4-real-case.md) |
| D-026 | 2026-10-04 | ARCHITECT 目标漂移审查结论 | proposed（待用户裁决） | [D-026](01-decision/D-026-architect-goal-drift-review.md) |
| D-027 | 2026-10-04 | R1 能力边界复审结论 | proposed（待用户裁决） | [D-027](01-decision/D-027-r1-capability-boundary-review.md) |
| D-028 | 2026-10-04 | 继任 R1 能力边界承诺 | proposed（待用户确认冻结） | [D-028](01-decision/D-028-r1-successor-capability-commitment.md) |
| D-029 | 2026-10-04 | 授权修订 R1/Root 并澄清 VP-003 | accepted | [D-029](01-decision/D-029-authorize-r1-root-vp-capability-revision.md) |
| D-030 | 2026-10-04 | VP-003 能力范围澄清 | accepted | [D-030](01-decision/D-030-vp003-capability-scope-clarification.md) |