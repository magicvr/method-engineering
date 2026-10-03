---
title: PA1 来源与访问方案 v0.1（待裁决）
status: draft
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.1
---

# PA1 来源与访问方案 v0.1（待裁决）

## 状态与边界

本文件汇总 2026-10-04 的公开书目与访问状态核实，并列出 S3/S4 尚需用户裁决的选择。它**尚不能关闭 I-007**：System Dynamics 的代表来源类型、闭源来源的读取路径/权限残余、调查资源上限与停止规则仍未冻结。未获用户书面选择前，不读取授权状态不明的全文、不购买或借阅受限材料、不扩大主范围。

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

## 需要用户裁决的选择

### J-01 · System Dynamics 代表来源策略

- **A（建议）· 现代方法核心**：以 PA-S04-C 领域回顾 + PA-S04-D 近期定义为核验来源，PA-S04-B 作为教科书细节入口，PA-S04-A 仅作历史起源引用。优点是方法概念与当代实践边界较清楚，范围可控。
- **B · 起源 + 现代综合**：同时把 PA-S04-A、B、C、D 当主来源。优点是历史与当代完整；缺点是显著增加 PA2 抽取量和版本协调成本。
- **C · 历史起源主导**：以 PA-S04-A 为主，辅以 PA-S04-C。优点是直接追溯奠基；缺点是 1961 版本边界与现代 SD 方法差异大，可能不适合直接映射当前需求。

### J-02 · 受限来源读取路径

J-02 必须同时回答两个不同问题：①用户是否授权本次研究读取某路径；②该来源在拟议用途下是否有已核实权限依据。选择 A 只解决前者，**不把公开可访问或作者托管副本证明为已授权来源**。

- **A（建议）· 公开托管作者/大学副本 + 明确残余接受**：授权为本次内部研究读取 PA-S01～PA-S03 的公开托管 PDF；引用以出版方版本为准，不提交/复制全文、不再分发、不推定再利用授权。用户须同时接受以下 P-005 残余字段，未确认则保持停止：
  - **未知**：出版方对公开托管副本在拟议研究用途下的授权未核实。
  - **范围/影响**：仅限本目标 PA2/PA3 内部阅读与引用；不影响对外发布、再分发或再利用许可。
  - **理由/缓解**：这些是核心原始来源，公开托管路径可访问；用官方书目定位、只保留必要摘录、发现异议或更可靠许可路径即停止使用。
  - **期限/复审触发**：在外部交付前、出版方异议、获得正式许可或改用开放替代来源时复核。
  - **责任人**：方法工程响应负责人。
  - **状态语义**：来源权限项保持 `accepted-residual`，不是 `verified`；选择 A 本身不等于 I-007 已关闭。
- **B · 授权/购买访问**：由用户提供或授权机构访问、购买、馆际互借等正式路径，并明确可访问范围与费用上限。该路径可形成更清楚的权限证据，但触发新增费用/执行授权，须先完成用户裁决。
- **C · 仅开放/摘要**：只使用出版方摘要或明确开放全文；PA-S01～PA-S03 无开放全文时保持 unresolved，不进入全文抽取，可能阻断这些主范围的 PA2 工作。

### J-03 · 调查资源与停止规则

- **A（建议）· 有界首轮**：每类 1 个核心来源，最多 2 个支撑来源；覆盖五类后先作要素抽取，只有冲突、缺口或映射失败才新增来源。禁止声称穷尽或“理论不存在”。
- **B · 深入检索**：每类允许更宽来源扫描，并要求同领域综述/反向来源交叉检查后再进入 PA2。资源消耗更高。
- **C · 最小检查**：每类只读 1 个核心来源，记录限制后直接进入抽取；快但可能遗漏跨来源冲突或替代解释。

## 建议进入 S4 的冻结内容（待用户选择后生效）

1. PA-S01～PA-S05 各有明确主来源、版次/稳定标识和访问路径。
2. 受限来源的权限项必须有可核对依据，或由用户明确接受有范围/期限/复审触发/责任人的残余风险；`accepted-residual` 不写成 `verified`。
3. 明确调查的人工时间、费用上限、拒绝条件、停止规则和责任人；用户只选择 J-03 深度仍不足以关闭 I-007。
4. 每次新增来源/范围/费用必须重新触发 P-005/P-004；AI 不得自行扩容。
5. 用户选择写入 GOAL-004 D-003，来源方案据此冻结；I-007 候选证据更新后还须独立闭合核验，用户选择本身不直接放行 PA2。