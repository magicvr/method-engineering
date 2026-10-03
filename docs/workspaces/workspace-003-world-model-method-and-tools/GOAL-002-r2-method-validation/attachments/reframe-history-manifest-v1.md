---
title: 旧 R2 路线历史保全清单
status: active
created: 2026-10-04
updated: 2026-10-04
parent: null
version: 1.0.0
---

# 旧路线历史保全清单

保存日期：2026-10-04。来源为 reframe 前本工作区文件；附件摘要已用 PowerShell `Get-FileHash -Algorithm SHA256` 取得，并在后续验证复核。此清单记录保全，不证明方法或理论适用。

## 历史范围

- 路线：旧 [meta](../00-meta.md) 中 R2a→R2b→R2c→R2d，检查点 0/4；Root 旧实时基线见 [历史快照](../../GOAL-001-world-model-method-and-tools/attachments/pre-reframe-root-baseline-v1.md)。
- 决策：D-001～D-029；执行：E-001～E-034；审计：A-001～A-019。全部历史条目保持原位、原字节；本次仅追加 D-030/E-035/A-020，补齐索引。
- 预登记准备、共享供水站合成候选包、H1/H2/H3 预登记草稿、H3 能力候选清单如下。候选接受不是冻结、运行或有效性证据。
- H3-SEM-001 仍为 required/open；[A-019](../03-audit/A-019-review-h3-preregistration-draft.md) 原文不改。准确输入/责任/隔离/预算与冻结门禁仍未满足，H3 冻结和运行继续禁止。
- 启动时已有 Git 暂存改动：旧 meta、decision 索引、E-034、A-019、H3 草稿。H2/H3 等未提交或可能未跟踪材料原位保留，不迁移、不回滚、不重新暂存；清单的 hash 只代表本次文件快照，不表示已提交或来源已验证。

## 附件 SHA-256

| 历史附件 | 保存状态 | SHA-256 |
|---|---|---|
| [H3-capability-checklist-candidate-v0.1.md](H3-capability-checklist-candidate-v0.1.md) | 原位保留；候选/草稿不升级 | `0aa3319faf4e3da7d7007ac02cd42eba436f9f616e49af7ba93456ee119d5260` |
| [R2a-H1-preregistration-draft-v0.1.md](R2a-H1-preregistration-draft-v0.1.md) | 原位保留；候选/草稿不升级 | `fe434c1c370b4c0672d094ce2b50aced7026aa8c9a4c38cb9bfb2163587577c9` |
| [R2a-H123-synthetic-candidate-pack-v0.1.md](R2a-H123-synthetic-candidate-pack-v0.1.md) | 原位保留；候选/草稿不升级 | `019860dfe8bcbcc63eee5679c69e8aa648c766480d15c1080ce702a28bccc79b` |
| [R2a-H2-preregistration-draft-v0.1.md](R2a-H2-preregistration-draft-v0.1.md) | 原位保留；候选/草稿不升级 | `a78d475cfbf1c008d33fd036735b78986e2b0b75aabdfe71ffc148dff3fc0582` |
| [R2a-H3-preregistration-draft-v0.1.md](R2a-H3-preregistration-draft-v0.1.md) | 原位保留；候选/草稿不升级 | `aa4611d1f4c0b2213a76e1b89fb4d04fdc3034fb3a403817468a73e2e7cde5b2` |
| [R2a-operationization-plan-v0.1.md](R2a-operationization-plan-v0.1.md) | 原位保留；候选/草稿不升级 | `9abc6214bbe4c92d9520cd92279b9f26a828e07362b34063000ed88ace634e0a` |

## 恢复规则

`cancelled + terminated-by-reframe` 终止的是当前执行路线，不删除证据，也不是必改项闭合。新路线无需补完旧预登记；将来复用旧实验必须先记录新的范围与授权裁决，复核 R1 原额度、逐次预登记、人员/参考隔离、Root 真实案例授权与 H3-SEM-001 等全部适用旧门禁；不得因历史保存或后继目标建立直接恢复冻结/运行。
