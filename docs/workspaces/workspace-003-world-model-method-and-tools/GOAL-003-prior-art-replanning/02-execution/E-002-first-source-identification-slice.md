---
title: 首批公开来源书目识别切片
status: active
created: 2026-10-04
updated: 2026-10-04
parent: null
version: 0.1.1
record_id: E-002
---

# E-002 · PA1 首批来源识别与范围纠正

## 授权依据（2026-10-04 补齐记录）

用户 2026-10-04 原始指令：“新的子目标应聚焦于：系统调查、比较并吸收与我们问题相关的成熟理论……并据此重新规划 VP-003 后续路线图。……然后开始新的子目标继续推进。”明确授权开始系统调查。本轮为五类主范围内未付费、公开元数据与公开摘要的有界来源识别切片，授权解释与边界见 [D-002](../01-decision/D-002-authorize-initial-public-source-slice.md)。此前正式记录遗漏该依据且错误收窄为本地盘点；本次补齐引用，不声称 D-002 在执行时已存在，也不新增检索或改写已发生事实。

不含付费、模型/实验运行、外部模型执行、无限扩展；不授权把 metadata/abstract 当理论内容或适用性证据。I-007 仍 open，完整迁移矩阵/来源方案/资源与停止规则待核对；不关闭 PA1/PA2 或 I-008。

## 实际动作与来源

2026-10-04，登记 Supervisor 已完成的公开元数据核实与摘要读取事实，并将 [来源登记](../attachments/prior-art-source-register-v0.1.md) 的主表纠正为用户指定的 Compositional Modeling、Qualitative Reasoning、mechanistic explanation、System Dynamics、Agent-Based Modeling 五项（PA-S01～PA-S05）。此前相邻候选降为 adjacent/unverified，不替代主范围。E-001 保留为历史记录，不重写其当时事实。

实际使用的公开来源与访问日期：Crossref（2026-10-04）、OpenAlex（2026-10-04）、Semantic Scholar（2026-10-04）、PMC/PubMed（2026-10-04）。本记录不粘贴原始长响应；可核对书目与稳定标识见来源登记。

## 已核实事实

- PA-S01 Compositional Modeling：Falkenhainer/Forbus（1991）的书目与访问状态已核实；DOI 10.1016/0004-3702(91)90109-W，OpenAlex W2066814802。未读全文、未抽取理论要素。
- PA-S02 Qualitative Reasoning：Forbus（1984）“Qualitative process theory”的书目与访问状态已核实；DOI 10.1016/0004-3702(84)90038-9。未读全文、未抽取理论要素。
- PA-S03 mechanistic explanation：Machamer/Darden/Craver（2000）“Thinking about Mechanisms”的书目与访问状态已核实；DOI 10.1086/392759。未读全文，未据 OpenAlex 摘要索引或二手解释作理论结论。
- PA-S04 System Dynamics：代表书目、版次、稳定标识和获取路径仍 unverified；Sterman/Forrester 仅是候选，待 PA1 来源方案确定。
- PA-S05 Agent-Based Modeling：Bonabeau（2002）的书目已核实；DOI 10.1073/pnas.082080899、PMID 12011407、PMCID PMC128598。实际读取 PubMed BioC 摘要（Abstract），简短摘要及定位见来源登记；公开 PMC 全文页面可访问，但未完成系统全文要素抽取。

首批完成 4/5 条书目识别；这是来源识别计数，不是阶段 progress。无全文系统抽取、无理论适用性判断，无需求映射、缺口或路线结论。

## 偏差与限制

- Crossref 的 Compositional 标题字段有 “Cmpositional” 拼写异常；以 DOI 书目和 Semantic Scholar 标题交叉核对，不静默当作原论文题名。
- Crossref、OpenAlex、Semantic Scholar 的三方元数据核对只证明对应书目/访问状态，不证明理论内容；不是每项都已获得三方核对。
- PA-S01～PA-S03 在本轮 OpenAlex 显示 closed、无可读全文（PA-S01 另显示 has_fulltext: false、无公开 PDF）。封闭来源需授权获取或改选公开一手来源，不能据未读全文推断内容。
- ABM 已读公开摘要不等于全文抽取完成，更不等于适用性成立；System Dynamics 尚未核实，不能补造 DOI/ISBN 或结论。

## 门禁与下一动作

该切片只推进 PA1 来源识别，不关闭 I-008、不完成 PA1、不增加 progress。PA1/PA2 门禁仍开放，五个阶段检查点维持 0/5；信息状态权威仍在 Root。本记录不修改 Root、旧目标、VP 或 goal-tree。

下一步在 PA1 来源方案中确定 System Dynamics 代表来源/版次/获取路径，安排封闭文献的授权获取或公开一手替代来源；按 PA1/PA2 门禁取得原文后再开展系统要素抽取。书目核实 ≠ 理论内容吸收；摘要读取 ≠ 适用性结论。
