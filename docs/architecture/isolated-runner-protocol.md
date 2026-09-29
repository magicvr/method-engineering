---
title: Isolated Runner Protocol
status: draft
created: 2026-09-29
updated: 2026-09-29
parent: null
version: 0.1.0
---

# Isolated Runner Protocol v0.1.0

## 1. Purpose and isolation model

本协议规定合作型 runner 的 **methodological context isolation**：runner 只应收到当前任务明确绑定的材料，不应继承或读取 parent conversation、旧 Probe、旧 run/audit 或 control-side history。

本协议不是对抗性安全模型。工作区共享、runner 理论上能读取其他文件、或没有 OS/filesystem sandbox，本身都不构成隔离失败。判定依据是 runner 实际收到的上下文与可见读取记录。

System/platform 通用上下文可以存在。额外 bootstrap 仅在当前 binding 中被版本化、hash 固定并审查为通用内容时允许；任何 project/probe/history-specific 内容不得作为 bootstrap 输入。

## 2. 角色与上下文边界

### Control / creator relay / reviewer

- Control 负责准备试跑 binding、固定 runner packet 和最终 hash、执行启动前核对，并创建唯一 runner。
- 不向 runner 提供 binding、design、frozen contract、历史 run/audit 或其它 control-side 材料，除非它们被明确列入本轮允许 packet；默认不列入。
- 只有 runner 真实需要 creator input 时，才向 creator 提问。转发回复时必须逐字、原样转发该轮 creator 回复，不总结、不解释、不改写、不补充，也不携带任何其它 parent conversation context。
- Runner 按 binding 的停止点结束后，reviewer 才可查看 control-side review materials；reviewer 的材料不得回注 runner。

### Runner

- Runner 是当前唯一执行者；材料要求单 runner 时不得再委派。
- Runner task 只包含当前 binding 明确列出的 packet、完成任务所需的最小角色指令，以及 binding 明确允许的通用 bootstrap。
- Runner 按 packet 执行，不主动访问或读取旧项目、旧 Probe、历史 run/audit、control-side 文件或 parent conversation 内容。
- 试跑的具体 stop condition、是否允许使用某类工具及结果边界由当前 binding 规定；本协议不规定每轮固定搜索或固定拆分步骤。

## 3. Fresh-context 启动与绑定

1. 使用协作接口创建新的 subagent，并明确使用 `fork_turns: none`，不 fork parent conversation。若接口无法提供 fresh context，不得把该次运行标记为 isolated runner。
2. Binding 列出每个 runner-visible 文件的精确路径、版本或用途、字节数与 SHA-256；packet 副本须在启动前逐项核对。Binding 自身也以最终字节的 SHA-256 固定；运行仅在创作者授权该精确 binding 身份后开始。
3. Binding 明确允许的 bootstrap 来源、revision/hash 与审计结论。项目特定或历史特定内容不允许；未经审计或身份变化的额外 bootstrap 不得静默放行。
4. Control 重算 manifest。任一 packet、bootstrap 或 binding 身份不匹配时 fail closed，不启动。
5. 共享 filesystem 不是访问授权。Runner 只使用任务明确提供的文件；对其他位置的潜在可读能力不作 OS 安全保证，也不单独据此判隔离失败。

## 4. Creator relay

当 runner 请求真正需要创作者裁定的信息时，control 将问题呈交创作者。收到答复后，传给 runner 的消息内容必须与创作者当轮原文逐字一致：不得加前缀或后缀、总结、解释、改写、选择性摘录或补入其它 parent context。多个创作者回合分别原样转发。

Creator 只承担 binding 和方法允许的取舍、粒度与结构确认；不要求 creator 代 runner 设计子问题、搜索策略或研究来源。

## 5. Trace 与隔离判定

Control 为每轮使用唯一 trace 文件名，不覆盖旧记录。尽可能保存：

- binding 与 packet 的身份/hash、启动前核验结果；
- 完整 runner task envelope；
- creator 提问、每条 creator 原文回复及实际 relay；
- runner 的完整输出、工具调用/可见结果、工具不可用情况及可获得的访问记录；
- trial stop point、reviewer-only disposition 与未覆盖的 trace 范围。

若平台不暴露 raw initial context、tool payload 或访问记录，明确记录其不可见范围；不得事后要求 runner 重建或补写缺失 trace，也不得宣称已逐字节核验不可见数据。

以下情况构成 methodological context contamination：runner 实际收到或主动读取未授权的 project/probe/history-specific 内容。出现时将该样本标为 contamination/invalidated，并记录具体证据与范围。若可见记录中没有此类注入或读取，则只可在记录 trace 可见性限制后，判为“在可见证据范围内未观察到污染”。System/platform 通用上下文与 binding 已审计允许的 generic bootstrap 不构成污染。

外部研究工具若在真实 unknown 触发时不可用，记录 tool-access limitation；不因此事前要求 smoke search，也不伪记为 research 已完成。无真实 research trigger 时记为 not observed。

## 6. 证据来源与适用边界

本版协议提炼自 run-13 fresh-context runner 试跑。run-13 使用 `fork_turns: none`，runner 只收到 hash 绑定 packet 与最小角色指令；可见 trace 未显示历史上下文注入或读取。协作接口没有向 control 暴露 raw initial subagent context 或完整底层工具 payload，因此该证据支持的是基于 API fresh-context 契约和可见运行记录的 methodological isolation，不证明操作系统级不可访问或隐形上下文绝对不存在。

证据记录：

- D-053：`docs/workspaces/workspace-003-world-model-method-and-tools/GOAL-004-collaborative-question-framing/01-decision/D-053-run13-subagent-context-runner.md`
- E-085：同目标 `02-execution/E-085-subagent-context-isolation-smoke.md`
- E-088：同目标 `02-execution/E-088-run13-e2e-isolated-trial-complete.md`
- 完整可见 trace：同目标 `attachments/run-13-full-visible-trace-2026-09-29.md`

Run-13 的 research runner 另有未在首次搜索前记录 effort cap/checkpoint/stop condition 的执行偏差；该观察不改变本协议的 context-isolation 语义，也不能作为 Shared Research Core 完全符合性的证据。

## 7. 状态

本文件是项目级协议候选 v0.1.0，当前为 `draft`。run-13 提供一次 fresh-context 运行样本，不等于协议已广泛验证或被整体接受。后续试跑应按各自 binding 固定 packet、bootstrap、工具和 stop condition，并用新增 trace 复核本协议的适用边界。
