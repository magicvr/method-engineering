---
title: 成熟理论来源登记 v0.1
status: draft
created: 2026-10-04
updated: 2026-10-04
parent: null
version: 0.1.1
---

# PA1 首轮来源登记（draft）

主范围按用户指定的五类理论登记，不以相邻理论替换。本轮公开来源核实事实由 Supervisor 提供，访问日期为 2026-10-04，见 [E-002](../02-execution/E-002-first-source-identification-slice.md)。这不是完成的文献综述，也不证明成熟程度、覆盖充分性或适用性。

**书目核实 ≠ 理论内容吸收；摘要读取 ≠ 适用性结论。** 以下四条已核实的是书目与访问状态；没有完成任何来源的系统全文要素抽取。后续调查边界、代表来源和资源安排仍待 I-007/PA1 来源方案确定。

| ID | 理论线索 | 已核实/未核实书目 | 稳定标识 | 核实动作（2026-10-04） | 证据等级 | 访问状态 | 下一动作 |
|---|---|---|---|---|---|---|---|
| PA-S01 | Compositional Modeling | 已核实：Brian Falkenhainer; Kenneth D. Forbus, “Compositional modeling: finding the right model for the job”, Artificial Intelligence, 1991, 51(1-3), 95-143 | DOI: 10.1016/0004-3702(91)90109-W；OpenAlex: W2066814802 | 核对 Crossref/OpenAlex 元数据；Crossref 标题有 “Cmpositional” 拼写异常，以 DOI 书目及 Semantic Scholar 标题交叉核对 | 书目/访问状态元数据；非理论内容证据 | OpenAlex: oa_status: closed、has_fulltext: false，无公开 PDF；本轮未读全文、未抽取理论要素 | 确定授权获取路径或改选公开一手来源，取得原文后按定位抽取 |
| PA-S02 | Qualitative Reasoning | 已核实：Kenneth D. Forbus, “Qualitative process theory”, Artificial Intelligence, 1984, 24(1-3), 85-168 | DOI: 10.1016/0004-3702(84)90038-9 | 核对 Crossref 书目及 OpenAlex 访问状态 | 书目/访问状态元数据；非理论内容证据 | OpenAlex: closed，无全文；本轮未读全文、未抽取理论要素 | 确定授权获取路径或改选公开一手来源，取得原文后按定位抽取 |
| PA-S03 | mechanistic explanation | 已核实：Peter Machamer; Lindley Darden; Carl F. Craver, “Thinking about Mechanisms”, Philosophy of Science, 2000, 67(1), 1-25 | DOI: 10.1086/392759 | 核对 Crossref 书目及 OpenAlex 访问状态；OpenAlex 有 abstract inverted index，但本轮不据此作理论结论 | 书目/访问状态元数据；非理论内容证据 | OpenAlex: closed，无公开全文；本轮未读全文、未抽取理论要素 | 确定授权获取路径或改选公开一手来源，取得原文后按定位抽取 |
| PA-S04 | System Dynamics | unverified：John D. Sterman, “Business Dynamics: Systems Thinking and Modeling for a Complex World”（2000）；或 Jay W. Forrester, “Industrial Dynamics”（1961） | 未核实，不填 DOI/ISBN | 本轮尚未核实精确代表书目、版次与稳定标识 | 候选线索（unverified）；非书目核实或理论内容证据 | 获取路径与权限待核实 | 在 PA1 来源方案中确定代表来源、版次和获取路径，再核实书目 |
| PA-S05 | Agent-Based Modeling | 已核实：Eric Bonabeau, “Agent-based modeling: Methods and techniques for simulating human systems”, PNAS, 2002, 99(Suppl 3), 7280-7287 | DOI: 10.1073/pnas.082080899；PMID: 12011407；PMCID: PMC128598 | 核对 Crossref/OpenAlex/PMC 元数据；实际读取 PubMed BioC 摘要（PMID 12011407，Abstract） | 书目/访问状态元数据 + 已读原始摘要（仅摘要范围）；非全文抽取/适用性证据 | OpenAlex: green OA；公开 PMC 全文页面可访问；本轮只读书目和摘要，未完成系统全文抽取 | 按 PMC128598 全文定位系统抽取要素、前提和限制，之后再作适用性比较 |

## 已读摘要的有限记录

PA-S05 的 PubMed BioC 摘要（PMID 12011407，Abstract）将 ABM 介绍为模拟人类系统的技术，并概述流动、组织、市场与扩散四类应用。这只是对已读摘要的简短转述，不作为理论要素抽取、需求映射或适用性结论。

## 相邻候选（adjacent/unverified，非本阶段主范围）

此前草拟的系统/控制与反馈（W. Ross Ashby / An Introduction to Cybernetics）、因果模型（Judea Pearl / Causality）、需求工程/能力发现（Klaus Pohl / Requirements Engineering）、仿真/模型开发核验（Stewart Robinson / Simulation: The Practice of Model Development and Use）仅保留为 adjacent/unverified 检索线索，书目/版次/原文尚未核实。它们不挤占或替代 PA-S01～PA-S05，是否纳入等待 PA1 来源方案决定。

## 证据边界与后续登记

元数据可核对作者、题名、出版信息、标识和访问状态，不证明理论内容。原始摘要只支持其摘要范围内的陈述；系统全文要素抽取须另有原文定位、前提与限制。二手解释仅作交叉线索；用户需求是必要性依据，不是理论有效性证据；AI/候选书目保持待核实。

后续每项抽取至少登记：原始来源类型、准确作者/题名/版次、获取权限、原文定位、可核对证据、抽取解释、限制、核实人/日期、相关要素 ID。封闭来源需授权获取或改选公开一手来源；查无结果记录调查范围/动作/限制，不推出“理论不存在”。本切片不关闭 I-008、不完成 PA1、不增加 progress；五个阶段检查点仍为 0/5。
