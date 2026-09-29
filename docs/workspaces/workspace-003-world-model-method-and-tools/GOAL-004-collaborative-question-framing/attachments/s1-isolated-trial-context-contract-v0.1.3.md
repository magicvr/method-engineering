---
title: S1 隔离试跑上下文合同
status: draft
created: 2026-09-28
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.3
artifact_role: control-side-future-trial-isolation-contract
---

# S1 隔离试跑上下文合同 · v0.1.3

本合同定义方法上下文隔离，用于避免旧项目、旧 Probe、历史 run/audit 或 conversation 内容实际进入 runner 上下文或被运行读取。它不是对抗性安全边界，不要求证明 runner 在 OS 层面无法访问其它文件。每轮仍须另行绑定文件并取得执行授权。

## 1. 三类上下文

### A. 精确绑定的试跑 packet

每个 binding 必须逐项列出 runner 可见的全部 method packet，给出相对路径、职责、版本／修订和 SHA-256。没有列入 packet 的项目文件、案例、审计、历史试跑、旧 Probe 与对话内容，不得作为 runner 输入或由 runner 主动加载。

被授权的 method、adapter、Core、Schema 及规范性投影可以写明项目／方法身份、版本、规则名和允许引用的规范文件。仅仅出现 S1、方法版本或已授权规范引用的名称，不构成泄漏；只有实际内容超出精确绑定范围、向 runner 提供未授权项目资料，或在运行中读取此类资料时才违反隔离。文档中的链接只标识引用，不授予访问 packet 之外文件的授权。

### B. 已审计的通用 bootstrap

通用 bootstrap 是不携带当前项目、Probe 或历史试跑特定信息的运行／角色／工具通用指令。每轮 binding 固定允许文件的来源、适用 scope、内容审计结论与 SHA-256。

run-13 候选 allow-list 只包括 bootstrap manifest v0.1.1 固定的 `~/.codex/AGENTS.md` 捕获件：13,638 bytes，SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`。启动前 control side 重新读取该文件并确认 hash 未变化；hash 未变化时无需每轮另外证明 runtime loader 注入字节。其它全局文件或不同 hash 不因其看起来通用而自动获准，须先另行审计并加入 binding。

### C. 系统与平台上下文

Codex／运行平台可能附加系统指令、工具说明或运行元数据。系统／平台通用上下文本身，以及上述已审计通用 bootstrap，本身不构成污染。若实际可见 trace 显示其中包含未授权的项目、Probe 或历史特定内容，则按实际收到的具体内容判定，不按其系统或平台来源豁免。

## 2. 内容边界与判定

- 允许的项目身份信息：精确绑定的方法或 adapter 自身包含的版本、规则与规范引用身份；其规范内容属于授权 packet。
- 允许的通用 bootstrap：只限 binding 指向的已审计文件及 hash，作用仅为一般 agent 行为、工具使用或平台运行。
- 禁止的未绑定特定上下文：任何未列入精确 packet、也未列入通用 bootstrap allow-list 的项目目标／私有文件内容、具体 Probe／期望答案／查询方向、旧 run／audit／conversation 历史、案例结构或目标世界事实。
- Methodological context isolation 以 runner 实际收到或主动读取的内容为准。runner 具有共享 filesystem 或理论上能够读取其它文件的能力，本身不构成失败。
- Contamination：实际可见 trace、输入记录或可用访问记录表明 runner 收到或读取了未授权的项目／Probe／历史特定内容。记录具体来源、内容与影响范围；该样本无效。
- 满足隔离：使用 `fork_turns: none` 创建 fresh-context subagent；结合 task envelope、可见 runner 消息、最终输出与可用工具记录，没有证据表明 runner 收到或读取未授权内容。系统／平台通用上下文及已审计通用 bootstrap 不计为污染。

## 3. 启动前检查

1. 通过当前 Codex collaboration API 创建 fresh-context subagent，明确设置 `fork_turns: none`，不得 fork 父对话。API 的该参数语义是不向 subagent 传递 surrounding conversation context。
2. root agent 只作 control、creator relay 与 reviewer；不将自身 conversation history、旧项目／Probe/run/audit、binding/design/contract 或其它 control-side 内容转发给 runner。
3. runner 是本轮唯一执行者。task 只提供 binding 指定的五项 packet（其中唯一 raw Probe input card 是本轮 Probe）及通用角色指令：“当前 agent 本身就是唯一 runner；按提供的 S1 材料执行；不得再委派。”不得提供观察矩阵、预期结果或额外案例信息。
4. 如执行中需要真实创作者裁决，root 只把创作者当轮的答复作为当前决策输入转给 runner，不附带其它父对话上下文。
5. trial directory 继续作为 packet 与输出 trace 的存储位置，但不要求 subagent cwd/workspace 指向该目录。文件系统可共享；目录位置、root agent 的工作目录及 runner 理论访问能力不单独作为隔离门禁。runner 实际读取未授权内容仍按 §2 判定。
6. 启动前 control side 核对 `~/.codex/AGENTS.md` 的 hash 与本轮 allow-list 一致，并重算绑定 packet 与方法 source/projection chain 的 SHA-256。
7. 不主动向 runner 提供项目特定 AGENTS、历史 conversation 或其它 bootstrap。若实际初始上下文或后续 trace 显示它们被注入／读取，按 §2 处理。

本合同不要求 OS 级 root-deny 或 filesystem-deny 证明，不要求 elevated sandbox、生效路径白名单、repo canary、shell smoke、web-search smoke、VM 或 Docker。研究工具仅在方法自然触发时使用；实际触发但不可用时记录 tool-access limitation，不作为启动前阻断。

## 4. 运行后检查

1. 保存可取得的原始 runner task envelope、creator relay、runner 输出、工具使用记录与访问记录，并计算可保存文件的 hash；不得重写原始输出或为补足观察项要求 runner 改写答案。
2. 按实际可见 trace、上下文输入与可用访问记录检查 runner 是否收到或读取未授权的项目／Probe／历史特定内容。若出现，标记 methodological context contamination / invalidated 并记录具体来源与影响范围。
3. 当前 collaboration API 可能不暴露 subagent 的原始 initial trace。若不可取得，记录该可见性限制；使用实际设置的 `fork_turns: none` API 契约及其余可见记录作判断，不得声称已逐字节检查不可见 trace。
4. 如果没有实际注入或读取未授权内容的证据，结合 §2 所述 API 契约与可用 trace，视为 methodological context isolation 满足，并明确说明未覆盖的 trace 范围。runner 理论上的文件访问能力本身不是 failure。
5. 系统／平台通用上下文与已审计通用 bootstrap 不构成污染。不得因其来源于系统而豁免其中实际出现的项目特定内容。
6. Research 工具若被真实触发且不可用，记录 tool-access limitation；未触发则按试跑设计记录 `not observed`。

## 5. 运行有效性边界

合同的审计或通过只固定未来试跑的方法上下文边界；不接受方法、不验证方法、不授权 S1→S2 handoff、节点级交接、W2/S2 或实际求解。每轮试跑须另有用户对该轮 binding 精确 hash 的执行授权。
