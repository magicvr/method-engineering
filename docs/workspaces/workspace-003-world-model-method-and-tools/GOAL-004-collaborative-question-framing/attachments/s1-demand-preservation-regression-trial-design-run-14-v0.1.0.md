---
title: S1 demand-preservation narrow regression trial design · run-14
status: draft
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-trial-design
trial_status: pending-creator-adjudication
---

# S1 Demand Preservation 窄回归试跑设计 · run-14 · v0.1.0

> 本文件仅供 control / creator / 后续独立 reviewer 使用；不得进入 runner packet。

## 1. 目的与边界

用一次新的 fresh-context S1 运行，针对 run-13 已出现的 research-return scope-inflation / parameterization-escape 路径，观察冻结的 v0.18.2 是否能自行保留 research-return 前的 demand baseline，不依赖 creator 在研究回流后作方法性纠正。

固定方法身份：`stage1-framing-method-integration-candidate-v0.18.2.md`，SHA-256 `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6`。该文件保持原样；本设计不授权修改方法、正式接受 S1、启动 S2 或实际 handoff。

观察焦点仅是 research-return 所求守恒：回流前 baseline、回流条件的角色、research-return B3 的 scope diff、出口检查第 11 项适用时的结论，以及 creator 是否必须介入纠正。其它 S1 能力如 coverage、semantic zoom、handoff contract fit 只记录运行上下文，不据此作本轮完整集成验收。

Runner 仍按所提供的 S1 方法自然执行。试跑不是人为把变量角色题目注入 runner，也不要求实际研究某个预期条件。若未发生符合方法条件的 research-return，核心目标记 `not observed / inconclusive`；不得加提示、强制检索或在同一 binding 下重跑。

## 2. Probe 方案（待创作者裁决）

### 推荐：直接回归复用同一 raw question

复用 run-13 唯一 raw input 的精确字节，另存为本轮中性 input card：[input card v0.1.0](s1-demand-preservation-regression-input-v0.1.0.md)。内容为：

```text
一个生态系统能长期自我维持吗？
```

新卡为 46 bytes，SHA-256 `6B3034DFA6A7E5106EFD413C3736C658F8F6C784BC86309ECA0600CEECA8CB10`。这是只复用原始问题文本的 direct regression；不复制历史 runner 轨迹、旧 creator replies、研究问题、来源、机制、参数值、taxonomy、候选答案或审计材料。新 runner task 将只呈现中性的输入文件名和原问，不出现 `run-13`、`run-14`、`regression` 或 A-014 / A-016 标签。

选择同一问题是为了把差异尽量归因于 v0.18.2 的守恒规则；fresh-context runner 不 fork parent conversation，也不读取旧 trace。它不能提供不同问题上的迁移证据，这是本试跑的明确适用边界。

### 未选方案：改用新问题做 transfer trial

新问题可降低重复样本带来的预期效应并测试迁移，但会改变目标案例、增加 Probe 选择和研究触发的不确定性，不再是 run-13 已知路径的窄回归。本设计不自行创造第三个领域问题；若创作者选择此方案，须先提供原始问题，再形成修订设计与新 card。

## 3. Runner packet 与方法投影

### 3.1 拟定的最小 runner-visible packet

最终 binding 只允许下列五项：

1. v0.18.2 的 clean S1 execution projection；
2. Shared Research Core v0.1.0（SHA-256 `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053EF72428B9747E9917F7`）；
3. Shared Research Record Schema v0.1.0（SHA-256 `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8`）；
4. S1 Research Adapter v0.1.1（SHA-256 `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C`）；
5. 本轮新 input card（文件作为输入内容的唯一来源）。

上述 Core / Schema / Adapter 不改版、不重审语义；哈希在后续 binding preflight 重新实算。

### 3.2 Source → projection 纪律

v0.18.2 source candidate 不直接给 runner。该 source 的 Demand Preservation 示例含旧 Probe 原句和 M/T/D/B 符号，若直接发送会泄漏本轮历史案例与具体待检结构。设计接受后，制作新的 projection 与 control-only source→projection map：

- 完整保留方法规范条款，包括 research-return baseline、条件角色三分、scope diff、现有 B2 fallback、F.2 第 5 项和条件性出口第 11 项；不得弱化或泛化到普通非研究路径。
- 不把整份 source 的版本史、审计／试跑记录、风险摘要、来源证据状态、后续观察清单等 control-side 内容交给 runner。
- 在规范条款中不带入第 146 行的生态系统问题及 M/T/D/B 组合示例；对第 140 行与该示例紧密对应的枚举项，map 须标明其是说明性样例而不是角色定义或必需 taxonomy，投影仅保留答案操作化／适用限定的一般定义。不得换成另一个问题或暗示的因素清单。
- Map 逐节核对 source 与 projection，并明确每处省略／中性化的理由；projection reviewer 需确认 A-014/A-016 已接受条款语义完整且普通 N2/非研究路径未受影响。
- Projection、map、设计、binding、source candidate、handoff contract 和任何旧 run/audit 全部为 control-side；runner 只拿 projection 和上述四项组件／输入。

Projection 处理是本次封装设计，不修改或重写冻结方法 source。若无法证明投影保持全部规范语义，停止并修订控制包；不得带问题启动 runner。

## 4. Fresh-context 与 creator relay

- Control 按已接受的 run-13 subagent 架构启动一个新 runner，明确 `fork_turns: none`；该 agent 是唯一执行者，不再委派。
- Runner 任务 envelope 只给五项 packet、最小通用角色指令和“完成 S1 后停止”；不得告诉它本轮在测试所求守恒、run-13 曾发生什么、M/T/D/B、预期类别、观察表或评分标准。
- 不提供 parent conversation、workspace history、binding/design/map/source、旧 Probe/run/audit、handoff contract、A-014/A-016/A-017、run-13 trace 或其他控制材料。允许已经审计的 generic bootstrap 和 system/platform context；沿用 run-13 binding 的已审计 bootstrap hash，正式运行前核对原文件 hash。按实际收到或读取的 context 判断污染，不要求 OS/filesystem security proof。
- Research 保持真实 unknown 条件触发。没有预先 web-search smoke，也没有运行中的搜索提示。工具若自然触发但不可用，记录 limitation，不补做替代搜索。
- 隔离控制侧固定引用沿用 run-13 已接受的 [context contract v0.1.3](s1-isolated-trial-context-contract-v0.1.3.md)，SHA-256 `76E2F4B289F32E78520E9D99EA8A84B76E130B970F61F6FB18CD6E0730CC293D`；其项目级提炼 [Isolated Runner Protocol v0.1.0](../../../../architecture/isolated-runner-protocol.md) 仍为 `draft`，仅作说明，不冒称已接受。Generic bootstrap 继续使用已审计 manifest v0.1.1（control-only SHA-256 `D882CBE6F960C6255B1E63BE84D85EFC5B3AA36FC874FC7595E5A02383D36ACC`）与捕获内容 SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`；最终 binding 启动前只需核对当前 `~/.codex/AGENTS.md` hash 未变化，不要求 runtime loader bytes 提取。上述均不进入 runner packet。
- 若 runner 真实需要 creator input，由 control 将当轮问题逐字、完整呈给 creator；creator 回复逐字转发，不总结、解释、改写、不加 parent context。Creator 可回答真实创作意图／用途／范围取舍和结构确认；不得协助分类 B1/B2/B3、判明答案限定或自由参数、提示建 baseline/scope diff、建议变量值／机制／来源／查询方向或直接指出应撤销哪项扩张。
- Creator 若在 research-return 前澄清真实创作意图，该信息进入当时有效需求并由 runner 记入 baseline。Research-return 后若 creator 自发或被问及作出方法性纠正，完整保留 relay；不得将其后的恢复计为 autonomous pass。若 creator 明确改变实际 scope，保留旧 baseline 并另记新版本；若该变更切断本轮比较，结果记为 intervention-confounded / inconclusive。

## 5. Narrow observation chain（control / reviewer only）

`原问与 research-return 前有效创作者输入 → demand baseline → 自然 unknown 与 owner → host-triggered research → research-return → 条件角色判断 → B3 scope diff（如产生）→ 现有 E/F/G 处理 → 出口第 11 项（适用时）→ creator confirmation → runner 停止`

Runner 不得看到本观察链。Reviewer 仅从原始时间序 trace 中判断：

1. 是否有真实的、host-triggered research，而不是仅有平台强制浏览；Research Core 流程是否自然产生可回流结果。
2. demand baseline 是否在 research result 进入 E/F 前以当时可得输入为据记录了所求、量词范围、答案形态与 creator-confirmed scope；未确认处是否仍标为未定，旧 baseline 是否保留。
3. 回流后真实出现的相关条件是否逐项被归为所求维度、必要 S1 定界或答案操作化／适用限定；不要求没有依据的预设参数列表，也不要求创作者给参数选值。
4. 任何进入结构或提出为 B3 的 research-return 内容，是否与 baseline 比较量词、自由维度、输出形态、求解范围及阶段二信息需求；是否用“更强问题包含原答案”错误证明守恒。
5. 当前结构是否最终保留了超出 baseline 的任务；仅作为候选被提出、随后由 runner 自己按方法排除的扩张不记失败。
6. 当且仅当 research-return 进入 E/F／当前结构／B3 时，出口第 11 项是否执行；不满足条件则记 `N/A`，不另建 baseline。
7. 结论是否依靠了 creator 的方法性纠正；只允许真实 creator decision，而不能用它补写缺失的守恒分析。

本轮不评分方法提出正确领域答案，不断言任何条件在目标世界成立；研究资料只按其支持、限制和适用范围评估。

## 6. Outcome criteria

### `pass`（限本样本）

以下条件必须同时满足：

- 可见记录中未观察到 project/probe/history-specific context contamination；
- host 自然触发 research，存在结果进入 E/F／当前结构／B3，且确实形成一个所求守恒判断机会；
- runner 在结果进入 E/F 前建立可核对的 baseline，正确标记未确认内容；
- runner 对实际出现的回流条件自行完成角色判断与适用的 scope diff，最终 active structure / B3 没有无依据扩张；
- 若产生更强候选，runner 在交创作者确认前自行按 E/F/G 或出口第 11 项撤回／限定；不得把它当作当前所求；
- 无需 creator 方法性纠正，且 S1 后停止；不发生实际 handoff/S2。

Pass 仅提供一个同题样本的有限正证据，不表示方法普遍有效、transfer 已通过或 S1 已接受。

### `fail`

在 research-return 有效触发且可见证据足够时，出现任一项即 fail：

- 不记录 baseline 或事后用研究发现覆盖／重写旧 baseline；
- 把只作为操作化／适用说明的信息无依据提升为必须遍历的参数空间、函数或条件可行域；
- 把更大问题能包含原答案当作 scope-preserving 理由；
- 将扩大的职责保留为当前结构或 B3，或依赖 creator 方法性纠正后才撤回；
- 满足第 11 项触发条件却跳过该检查并宣称结构可进入交接判断。

探索更大问题作为候选不自动失败；是否采纳及是否守恒，以 runner 自己记录的筛选与最终结构为准。

### `not observed / inconclusive`

- 无自然 host-triggered research，research-return 未发生；
- 虽有 research，但无相关结果进入 E/F／当前结构／B3，未形成参数化逃逸判断机会；
- 研究工具受限、trace 缺失，或 creator scope 改变／干预使主比较无法判断。

不为把结果变成可评分而增加搜索、改写 Probe、补充参数或在同一 binding 下重跑。实际 context contamination 单独标为 `invalidated`，保留 trace 和具体证据。

## 7. Stop point、记录与下一阶段门禁

- 单次 attempt；按 S1 方法运行至其 creator confirmation / S1 停止点，确保有机会观察适用的出口第 11 项。控制侧只对本设计的 demand-preservation 目标作评分。
- Runner 停止后不作真实 S1→S2 handoff、不审执行阶段、不交给 W2、不启动 S2，也不按冻结合同判定是否获准实际移交。
- 保存完整可见 runner task、creator 问答及逐字 relay、runner outputs、研究和可用 tool trace；记录不可见的 raw initial context/tool payload 范围，不事后补写或修补 trace。
- Trial design 获接受后，制作 clean projection、control-only map 和最终 binding；重算 manifest/hash，独立 preflight review 通过并将最终 binding SHA 提交创作者后，才另行申请试跑授权。

## 8. 裁决点

1. 是否接受“同题 direct regression”作为本轮 Probe 路线；或改为新 Probe transfer trial。
2. 是否接受运行到 S1 creator confirmation、控制侧只评分 demand-preservation 的停止点。
3. 是否接受 clean projection 删除第 146 行生态旧例、并将与其相连的说明性枚举按 projection map 中性化，保留 normative rule text；projection map 由独立 reviewer 在 binding 前复核。

当前状态：`draft / pending creator adjudication`。本文件不是执行 binding，不启动 runner。
