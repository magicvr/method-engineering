---
title: S1 E2E integration trial design · run-13
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-trial-design
---

# S1 E2E integration trial design · run-13 · v0.1.0

## 1. 目的与边界

Run-13 是对已分别获得样本证据的 S1 framing／semantic zoom／Shared Research Loop 组件进行一次完整组合观察。核心增量目标是补充 run-12 未观察到的自然 research-loop 调用及证据回流样本。唯一 runner Probe 是 [raw input card](s1-integration-trial-input-card-run13-v0.1.0.md)，其内容只有一个问题；本设计及其控制侧理由不得提供给 runner。

research 是按真实 unknown 触发的条件分支，**不是每轮固定步骤**。若 S1 没有识别出需要外部资料的未知，或本案例中的缺口可由创作者取舍、目标世界客观求解或纯推理处理，则不应搜索；记为 `not observed`，不是失败。成功也不要求 semantic zoom 必然发生。

本设计不预设任何目标世界事实、机制、taxonomy、来源、查询方向、候选答案或预期结论。没有找到资料只能说明在已记录的有限问题／来源／时间／访问范围内未找到；不能推出目标事物或机制不存在。

## 2. 只供审阅者使用的观察链

观察自然发生的完整链路：

`原问 → 主动定界 → semantic zoom（若真实需要） → unknown 识别与 owner → research-loop（若真实触发） → evidence 回流 → Rule E/F/G → coverage convergence → creator confirmation → runner 停止 → reviewer-only handoff 判断`

完整研究过程证据应能从自然生成的 trace 中追踪：

1. 哪个 unknown 尚不能由当前输入、已授权常识推理或创作者取舍收敛；它的类型与 owner 为什么指向外部研究。
2. S1／研究过程如何定义有界研究问题、选择适当来源并收集资料；边界来自实际研究问题和可用来源，而非本设计预先给出的查询／来源清单。
3. 每条资料的来源、质量／出处、claim、support、limits、applicability 与迁移理由（如适用）如何记录；区分“没找到”与“不存在”。
4. 研究结论如何综合，并分别指出哪些只是一般机制／分析依据、哪些适用于当前候选问题，以及其适用条件；外部证据不自动成为目标世界事实。
5. 研究返回如何重新进入 v0.18.0 的 Rule E/F/G：候选相关性／结构准入与排除、问题和答案未知的区分、owner 与下一阶段状态、coverage 攻击与收束。不得另造第二套结构判断流程。
6. 研究后仍未解决的未知如何留痕、owner 如何归属，以及其对当前问题结构／handoff 判断的影响。

仅出现 `web_search` 或其它搜索工具调用不构成 research-loop 证据。须看到宿主针对真实 unknown 建立的研究问题、来源选择／资料收集、证据评价与适用范围、综合、回流和剩余未知记录。若平台因为产品策略自动要求 browse，此类调用应另记为 platform-mandated browsing；只有 S1 host 自己按方法识别并驱动的闭环才算 host-triggered research。

## 3. 条件触发与过程纪律

- 不向 runner 提供上述观察链、观察项或本设计文本，不为覆盖某一格要求搜索、拆分或回答特定内容。
- 研究触发与否依据原始 trace 中自然出现的 S1 unknown 类型、owner 和研究动作判定。若未触发，research-loop 与 research return 均标 `not observed`，不记 pass/fail。
- 若启动研究，按共享 Core、Schema 与 S1 Adapter 当前绑定版本记录边界与证据；不得为满足研究闭环而强加来源类型、资料数量、查询策略或答案。
- 未找到来源／claim 时，记录实际尝试和访问边界；不得把搜索未果等同于不存在。若适用性不足，明确限制，不强行回流为目标世界事实。
- semantic zoom 只有在 AI 自己识别节点仍可能是问题族并按 v0.18.0 判断需要时才观察；不得提示强制展开。创作者仍只作保持粒度／继续展开／否定节点的支持性裁决。
- creator 负责真实创作取舍与结构确认，不代 AI 识别未知、划定研究任务、列来源或拆子问题。
- runner 在 S1 creator confirmation 后停止。不得实际交给 W2，不启动 S2，不做实际求解。冻结 handoff contract 只由 reviewer 在 runner 停止后按 trial-only content-fit 核对。

## 4. Run-12 证据矩阵与 run-13 补证目标

以下仅为 control-side 设计依据，不是 runner 提示，也不据此要求本轮特定结果。

| 能力／观察项 | run-12 disposition | run-12 证据界限 | run-13 观察目的 |
|---|---|---|---|
| 原问与主动定界 | observed / pass | ordinal 13 分析不同读法；ordinal 20 creator 选择泛化条件 | 观察同一能力在线程中的自然组合 |
| 节点粒度与 semantic zoom | 粒度判断 observed；局部递归 `not observed` | ordinal 41 识别可能的问题族；ordinal 48 creator 选择保持粒度，未授权递归 | 仅在自然触发时观察递归与 E/F/G 复用 |
| Unknown 与 owner | observed / pass（限 S1） | ordinal 41、57 区分 B1/B2/B3 和后续 owner | 观察研究适合性、owner 与求解阶段的区分 |
| Research-loop 调用 | **`not observed`** | 未发生检索或资料收集；未触发不构成失败 | 若真实外部 unknown 出现，追踪有界闭环；否则如实保持 `not observed` |
| 证据评价与 Rule E/F 回流 | 无研究时 E/F observed；研究证据返回 **`not observed`** | 无外部证据可评价或回流 | 观察 support、limits、applicability、综合和回流，而不升格为目标事实 |
| Rule G coverage 与 convergence | observed / bounded pass | ordinal 41、57 有攻击、候选清算与 residual；不证明穷尽 | 观察研究回流后 E/F/G 是否共同收束 |
| Creator confirmation 与停止 | observed / pass | ordinal 48、66；ordinal 69 停止，未实际 handoff/S2 | 再观察确认和停止边界 |
| Handoff contract-content fit | failed / incomplete（运行输出／记录问题，非方法 finding） | A-011 MAJOR：host revision、handoff scope、W2 求解职责／顺序、residual owner／影响／依赖不足 | 仍仅由 reviewer 在停止后判断；缺项原样记录，不补写 runner trace |

## 5. 记录、评判与禁止事项

- 保留完整原始 runner／creator／tool trace；记录调用方、所见上下文、文件访问范围和 hash。不得根据预期矩阵在运行中提示 runner。
- 记录实际 host revision 与 scope，以及方法输出自然提供的 owner、依赖与 residual；只记录 trace 实际出现的内容，不向 runner 询问答案内容来补齐 handoff 包。
- 如使用浏览器／搜索，区分 S1 host-triggered research 与平台强制 browse；逐项标记证据来源和研究边界。只有检索动作不能证明研究闭环成立。
- reviewer 在 runner 停止后，才可查看本设计与 control-side handoff 条款，对 transcript 做 trial-only contract-content fit。必须将“可作为行为样本”与“完整 handoff package 合格”分开判断；不得据此执行交接。
- 无论结果如何，本轮均不接受方法本体、不授权真实 S1→S2 handoff、不启动 W2/S2、不进行目标世界实际求解。run-13 binding 只有在另行接受且用户以该 binding 的精确 SHA-256 作出执行授权后才可执行。
