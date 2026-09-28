---
title: S1 隔离试跑上下文合同
status: draft
created: 2026-09-28
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.2
artifact_role: control-side-future-trial-isolation-contract
---

# S1 隔离试跑上下文合同 · v0.1.2

本合同定义方法上下文隔离，用于避免旧项目、旧 Probe、历史 run/audit 或 conversation 内容实际进入 runner 上下文或被运行读取。它不是对抗性安全边界，不要求证明 runner 在 OS 层面无法访问其它文件。每轮仍须另行绑定文件并取得执行授权。

## 1. 三类上下文

### A. 精确绑定的试跑 packet

每个 binding 必须逐项列出 runner 可见的全部 method packet，给出相对路径、职责、版本／修订和 SHA-256。没有列入 packet 的项目文件、案例、审计、历史试跑、旧 Probe 与对话内容，不得作为 runner 输入或由 runner 主动加载。

被授权的 method、adapter、Core、Schema 及规范性投影可以写明项目／方法身份、版本、规则名和允许引用的规范文件。仅仅出现 S1、方法版本或已授权规范引用的名称，不构成泄漏；只有实际内容超出精确绑定范围、向 runner 提供未授权项目资料，或在运行中读取此类资料时才违反隔离。文档中的链接只标识引用，不授予访问不存在于 packet 中文件的授权。

### B. 已审计的通用 bootstrap

通用 bootstrap 是不携带当前项目、Probe 或历史试跑特定信息的运行／角色／工具通用指令。每轮 binding 固定允许文件的来源、适用 scope、内容审计结论与 SHA-256。

run-13 候选 allow-list 只包括 bootstrap manifest v0.1.1 固定的 ~/.codex/AGENTS.md 捕获件：13,638 bytes，SHA-256 15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8。启动前 control side 重新读取该文件并确认 hash 未变化；hash 未变化时无需每轮另外证明 runtime loader 注入字节。其它全局文件或不同 hash 不因其看起来通用而自动获准，须先另行审计并加入 binding。

### C. 系统与平台上下文

Codex／运行平台可能附加系统指令、工具说明或运行元数据。系统／平台通用上下文本身，以及上述已审计通用 bootstrap，本身不构成污染。若实际 trace 显示其中包含未授权的项目、Probe 或历史特定内容，则按实际收到的具体内容判定，不按其系统或平台来源豁免。

## 2. 内容边界与判定

- 允许的项目身份信息：精确绑定的方法或 adapter 自身包含的版本、规则与规范引用身份；其规范内容属于授权 packet。
- 允许的通用 bootstrap：只限 binding 指向的已审计文件及 hash，作用仅为一般 agent 行为、工具使用或平台运行。
- 禁止的未绑定特定上下文：任何未列入精确 packet、也未列入通用 bootstrap allow-list 的项目目标／私有文件内容、具体 Probe／期望答案／查询方向、旧 run／audit／conversation 历史、案例结构或目标世界事实。
- Methodological context isolation 以实际上下文和运行行为为准。runner 理论上能够读取其它文件，或平台未提供 OS 级隔离证明，本身不构成失败。
- Contamination：实际 trace、输入记录或可用访问记录表明 runner 收到或读取了未授权的项目／Probe／历史特定内容。记录具体来源、内容与影响范围；该样本无效。
- 满足隔离：复核实际可用 trace 与访问记录后，没有证据表明 runner 收到或读取未授权的项目／Probe／历史特定内容。系统／平台通用上下文及已审计通用 bootstrap不计为污染。

## 3. 启动前检查

1. 创建 fresh Codex conversation/session，不携带前序试跑对话历史。
2. cwd/workspace 是原仓库之外的独立 sibling trial directory。
3. trial directory 初始只包含本轮 binding 指定的五项 runner packet 与必要输出目录。
4. 不主动加载或提供 method-engineering repo、旧 run/audit、binding、design、contract 等控制材料。
5. trial directory 及其 ancestor 不存在 project-specific AGENTS.md。已审计的全局 ~/.codex/AGENTS.md 可作为 generic bootstrap 存在。
6. 启动前重新计算已审计 global AGENTS 文件 hash；只有 hash 与本轮 allow-list 不一致时才停止并复核。
7. 重新计算五项 packet 及 binding 所列方法身份与 projection chain 的 SHA-256，必须与 binding 一致。

本合同不要求 OS 级 root-deny 或 filesystem-deny 证明，不要求 elevated sandbox 生效或 readable roots 仅包含 trial directory，不要求 repo canary 被拒绝，不要求 PowerShell/shell smoke、web-search smoke、VM 或 Docker。不得把 runner 理论上具有访问其它文件的能力当作隔离失败。研究工具在运行中被真实需要时若不可用，记录 tool-access limitation；不得以此作为启动前阻断条件。

## 4. 运行后检查

1. 原样保存 runner／creator／tool trace 和可用访问记录，并计算 hash；不得为补足观察项而编辑 trace 或要求 runner 重写答案。
2. 根据实际 trace、上下文输入与可用访问记录检查 runner 是否收到或读取未授权的项目／Probe／历史特定内容。
3. 若发现上述实际注入或读取，标记 methodological context contamination / invalidated，并记录具体来源与影响范围。若没有发现此类注入或访问，methodological context isolation 视为满足。runner 理论上的外部文件访问能力不是 failure。
4. 不要求从 runtime loader 提取或逐字节复核已审计 global AGENTS 的注入副本；启动前磁盘文件 hash 未变化即可沿用 allow-list。不得因此忽略 trace 中实际可见的未授权项目特定内容。
5. 系统／平台通用上下文和已审计通用 bootstrap 不构成污染。对 trace 未覆盖的部分只说明证据边界，不作超出证据的安全保证。
6. Research 工具若被实际触发且不可用，记录 tool-access limitation；不将该限制改写为 context contamination。未触发研究的分支按试跑设计记录为 not observed。

## 5. 运行有效性边界

合同的审计或通过只固定未来试跑的方法上下文边界；不接受方法、不验证方法、不授权 S1→S2 handoff、节点级交接、W2/S2 或实际求解。每轮试跑须另有用户对该轮 binding 精确 hash 的执行授权。
