---
title: PA2 来源覆盖与未决项 v0.1
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.1
---

# PA2 来源覆盖与未决项 v0.1

## 覆盖状态

| 来源 | 访问/版本 | 抽取状态 | 覆盖结论 |
|---|---|---|---|
| PA-S01 | 公开 PDF，HTTP 200，SHA-256 已登记 | S01-01～S01-06 | 全文局部要素已抽取 |
| PA-S02 | 公开 PDF，HTTP 200，SHA-256 已登记 | S02-01～S02-08 | 全文局部要素已抽取 |
| PA-S03 | 公开 PDF，HTTP 200，SHA-256 已登记 | S03-01～S03-06 | 全文局部要素已抽取 |
| PA-S04-C | Wiley 官方页 Free to Read，自动访问 403 | 无全文要素 | unresolved；仅摘要级事实 |
| PA-S04-D | OSTI PDF，HTTP 200，SHA-256 已登记 | S04D-01～S04D-08 | 全文局部要素已抽取 |
| PA-S05 | PMC HTML，HTTP 200，SHA-256 已登记 | S05-01～S05-09 | 全文局部要素已抽取 |
| PA-S04-A/B | 仅书目/历史或细节入口 | 未作核心抽取 | 按 J-01 A，不作为 PA2 核心覆盖 |

## I-008 当前结论

- 对已访问来源：版本/定位、原文位置和抽取记录可核对。
- 对 PA-S04-C：全文未取得，用户 2026-10-04 按 [D-002](../01-decision/D-002-accept-s04c-fulltext-residual.md) 接受有界残余。
- Root I-008 记为 `accepted-residual`，不是 `verified`；PA3/PA4 只以 PA-S04-D 作为 SD 方法定义核心，S04-C 摘要仅作背景。
- 残余不关闭 I-009/I-010，不完成 PA2，不自动进入 PA3；外部交付前或出现冲突时复审。