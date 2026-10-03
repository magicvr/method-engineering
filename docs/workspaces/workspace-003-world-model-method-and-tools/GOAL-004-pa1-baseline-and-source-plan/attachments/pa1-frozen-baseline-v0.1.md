---
title: PA1 冻结基线与来源快照 v0.1
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.1
---

# PA1 冻结基线与来源快照 v0.1

## 目的

固定 PA2～PA5 可引用的需求、执行主体澄清、R1 协议与旧假设原文来源。本文件只固定版本和提取边界，不评价需求、旧假设或理论是否正确，也不把历史文本提升为证据。

## 固定来源

| 基线 | 精确定位 | 固定标识 / 本地证据 | 本阶段用途 |
|---|---|---|---|
| 下游需求原文 | `WorldModel.ModernCultivation@7324bdfcb35676c5fae8a3162b8d5a348a4b37ab:exchange/WRK-002-world-model-method-and-tools/需求-2026-09-26.md` | Git blob `281582b95d8cfcc85ea79b00e9495e305f0d17f3`；本地工作树 SHA-256 `F8B3E49C030AD9E1E1022F78D791D03E24DB66685EC9005F83B7BC96FD5AF4B9`；blob 与工作树一致 | §10/§13 原文提取及后续逐项映射 |
| 执行主体澄清第 2 版 | `WorldModel.ModernCultivation@e9054c958fa7e0b54e1ba9e272a7f8584dbd9352:exchange/WRK-002-world-model-method-and-tools/需求澄清-2026-09-26-构建主体.md` | Git blob `12c55abde59dc0bd70b6271cca61eb39650196f6`；R1 v0.6.2/v0.6.3 已写明该提交定位 | 创作者主责、AI 可协助但不得代劳的边界 |
| R1 冻结协议 | `docs/workspaces/workspace-003-world-model-method-and-tools/GOAL-001-world-model-method-and-tools/attachments/R1-freeze-proposal-v0.6.4.md` | 本仓 Git blob `35a617cfaf3cc5105a6ebcc8267b66045d93a3d9`；SHA-256 `DCE5C865B1BDEA8B98681F89241E9FC53A355987DA409E9667632643FA4B9A81` | 约束迁移矩阵的权威正文 |
| 旧 H1/H2/H3 原文快照 | `docs/workspaces/workspace-003-world-model-method-and-tools/GOAL-001-world-model-method-and-tools/attachments/pre-reframe-root-baseline-v1.md` | 本仓 Git blob `36931f17e7c2b733d39cb6b3d68e12a871d820ae`；SHA-256 `E8093A9D2082F8728CF9E10C1F1F7CB089CFA87C2B71DB58C342B1F699610A85` | 只作旧局部主张的历史基线，不作有效性证据 |
| §10/§13 与 H1/H2/H3 提取 | `GOAL-003-prior-art-replanning/attachments/requirements-and-hypotheses-mapping-v0.1.md` | 本仓 Git blob `f24444648ec782974b47258f8d3c30619b26740b`；SHA-256 `A9A2D015ABE6A8B871AEE8C0781A5945E640F23E17369DB81022B24F7EE49C89` | 供 PA3 逐项映射的原文输入，现有 mapping skeleton 不是结论 |
| 首批来源识别事实 | [GOAL-003 E-002](../../GOAL-003-prior-art-replanning/02-execution/E-002-first-source-identification-slice.md) | PA-S01/02/03/05 书目已核实；PA-S04 未核实；ABM 摘要已读；无理论要素抽取 | S3 来源方案的输入事实 |

## 提取边界

- 需求原文固定用于 §10「模型能力缺口的判定」与 §13「希望的方法交付」；不要从其他章节补造本阶段结论。
- 执行主体澄清固定为第 2 版；第 1 版中“AI 只能做非判断工作”已被撤回，不作为现行边界。
- R1 v0.6.4 是后续通用契约、H 专属额度和条件工具策略的当前协议正文；其历史前置版本只作变更追溯。
- H1/H2/H3 是旧路线局部主张，当前状态为未经本目标验证；H3-SEM-001 仍 required/open，旧 H 冻结/运行禁止。
- 固定来源只保证版本可核对，不自动提供理论内容、适用性或需求有效性结论。

## S1 结论

S1 的需求、澄清、R1 与旧假设基线已可提交级/本地 blob 级复核。后续 PA2/PA3 的原文引用必须回到本表定位；任何替换版本或扩大提取范围须登记并重新核对。