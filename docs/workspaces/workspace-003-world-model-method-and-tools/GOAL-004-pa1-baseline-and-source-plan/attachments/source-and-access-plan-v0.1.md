---
title: PA1 来源与访问方案 v0.2（已裁决）
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.2.0
---

# PA1 来源与访问方案 v0.2（已裁决）

## 状态与边界

用户已于 2026-10-04 接受 J-01 A、J-02 A（含明确权限残余）和 J-03 A，见 [D-003](../01-decision/D-003-record-user-source-access-and-resource-decisions.md)。本文件冻结 S3 来源/访问策略并给出 S4 资源与停止规则；来源权限未知部分保持 `accepted-residual`，不写成 `verified`。I-007 的 Root 证据更新和 PA1 退出审计完成前，PA2 不开始。

## 已核实的来源事实

| ID | 主范围 | 可引用来源 | 稳定标识 | 公开访问状态 | 合法/稳定路径 |
|---|---|---|---|---|---|
| PA-S01 | Compositional Modeling | Falkenhainer, B.; Forbus, K. D. “Compositional modeling: finding the right model for the job”, *Artificial Intelligence* 51(1–3), 95–143 (1991) | DOI 10.1016/0004-3702(91)90109-W；OpenAlex W2066814802 | 出版方记录可查；正式全文受限。Northwestern QRG 有公开作者 PDF，页面可访问，但未确认出版社开放授权或再利用许可 | Elsevier 记录；`https://www.qrg.northwestern.edu/papers/Files/QRG_Dist_Files/QRG_1991/FalkenhainerForbus_1991_CompModeling.pdf` |
| PA-S02 | Qualitative Reasoning | Forbus, K. D. “Qualitative process theory”, *Artificial Intelligence* 24(1–3), 85–168 (1984) | DOI 10.1016/0004-3702(84)90038-9 | 出版方记录可查；正式全文受限。Northwestern QRG 有公开作者 PDF，页面可访问，但未确认出版社开放授权或再利用许可 | Elsevier 记录；`https://www.qrg.northwestern.edu/papers/Files/QPT-PHD%28searchable%29.pdf` |
| PA-S03 | mechanistic explanation | Machamer, P.; Darden, L.; Craver, C. F. “Thinking about Mechanisms”, *Philosophy of Science* 67(1), 1–25 (2000) | DOI 10.1086/392759 | Cambridge Core 有摘要/书目；正式全文受限。UCSD 有大学托管 PDF，页面可访问，但未确认出版社开放授权或再利用许可 | Cambridge Core 记录；`https://mechanism.ucsd.edu/bill/teaching/w10/machamer.darden.craver.pdf` |
| PA-S04-A | System Dynamics（历史专著） | Forrester, J. W. *Industrial Dynamics*, MIT Press (1961) | ISBN 0-262-06003-5 / 978-0-262-06003-5（以实际版次版权页为准） | 公开书目可查；未确认合法开放全文 | MIT/书目页；System Dynamics Society 历史书目页 |
| PA-S04-B | System Dynamics（现代教科书） | Sterman, J. D. *Business Dynamics: Systems Thinking and Modeling for a Complex World*, 1st ed., McGraw Hill (2000) | ISBN 0-07-231135-5 / 978-0-07-231135-8 | 出版方书目/销售页；无确认开放全文 | McGraw Hill 出版方页 |
| PA-S04-C | System Dynamics（领域回顾） | Sterman, J. D. “System dynamics at sixty: the path forward”, *System Dynamics Review* 34(1–2), 5–47 (2018) | DOI 10.1002/sdr.1601 | Wiley 标为 Free to Read；可确认的是出版方阅读访问，不推断再利用许可 | `https://onlinelibrary.wiley.com/doi/abs/10.1002/sdr.1601` |
| PA-S04-D | System Dynamics（近期定义） | Naugle, A.; Langarudi, S.; Clancy, T. “What is (quantitative) system dynamics modeling? Defining characteristics and the opportunities they create”, *System Dynamics Review* 40(2), e1762 (2024) | DOI 10.1002/sdr.1762 | Wiley 标为 Open Access | `https://doi.org/10.1002/sdr.1762` |
| PA-S05 | Agent-Based Modeling | Bonabeau, E. “Agent-based modeling: methods and techniques for simulating human systems”, *PNAS* 99(Suppl. 3), 7280–7287 (2002) | DOI 10.1073/pnas.082080899；PMID 12011407；PMCID PMC128598 | PMC 收录全文，公开访问 | `https://pmc.ncbi.nlm.nih.gov/articles/PMC128598/` |

访问核实日期均为 2026-10-04。以上事实只证明书目、版本线索和访问状态；不证明理论成熟度、内容充分性或对本需求的适用性。

## 已裁决的 S3/S4 选择

### J-01 A · System Dynamics 现代方法核心

PA-S04-C（Sterman 2018 领域回顾）与 PA-S04-D（Naugle 等 2024 近期定义）作为核验来源；PA-S04-B（Sterman 2000）仅作教科书细节入口；PA-S04-A（Forrester 1961）仅作历史起源引用。后续若需把 B/A 提升为主来源，须新增用户裁决。

### J-02 A · 公开托管副本与有界残余

授权为本次内部研究读取 PA-S01～PA-S03 的公开托管 PDF；以出版方版本引用，不提交/复制全文、不再分发、不推定再利用授权。来源权限未知部分按以下残余记录：

| 残余字段 | 内容 |
|---|---|
| 未知 | 出版方对公开托管副本在拟议研究用途下的授权未核实 |
| 范围/影响 | 仅限 GOAL-003 的 PA2/PA3 内部阅读与引用；不影响对外发布、再分发或再利用许可 |
| 理由/缓解 | 核心原始来源且公开托管路径可访问；用官方书目定位、只保留必要摘录；发现异议或更可靠许可路径时停止 |
| 期限/复审触发 | 外部交付前、出版方异议、获得正式许可或改用开放替代来源时复核 |
| 责任人 | 方法工程响应负责人 |
| 状态语义 | `accepted-residual`，不是 `verified`；不自行关闭 I-007 |

### J-03 A · 有界首轮

每类 1 个核心来源、最多 2 个支撑来源；新增费用上限 0；人类复核与决策上限 6 人时；AI 执行时间另记，不折算为人时。覆盖五类后先作要素抽取；只有冲突、缺口或映射失败才新增来源。禁止声称穷尽或“理论不存在”。超出任一上限须暂停并重新请求用户裁决。
## S4 冻结内容

1. PA-S01～PA-S05 主来源、版次/稳定标识与访问路径按本文件执行。
2. PA-S01～PA-S03 权限未知部分按 J-02-A 的 `accepted-residual` 执行，不写成 `verified`。
3. 调查执行遵守 J-03-A：来源数量、0 新增费用、6 人时人类上限；AI 执行时间另记。
4. 新增来源、范围、费用或改变来源策略必须重新触发 P-005/P-004。
5. 下一步是更新 Root I-007 证据并完成独立 PA1 退出审计；该审计不代替用户对 `status: done` 的确认。