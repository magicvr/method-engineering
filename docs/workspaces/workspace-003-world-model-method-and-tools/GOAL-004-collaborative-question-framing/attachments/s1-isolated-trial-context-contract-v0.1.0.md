---
title: S1 隔离试跑上下文合同
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-future-trial-isolation-contract
---

# S1 隔离试跑上下文合同 · v0.1.0

本合同用于后续 S1 隔离试跑的准备、启动前核验与运行后复核。它区分 runner 可见的精确试跑材料、经审计并固定身份的通用 bootstrap，以及平台生成或不可导出的上下文。它不授权任何一次具体运行；每轮仍须另行绑定文件并取得执行授权。

## 1. 三类上下文

### A. 精确绑定的试跑 packet

每个 binding 必须逐项列出 runner 可见的全部 method packet，给出相对路径、职责、版本／修订和 SHA-256。没有列入 packet 的项目文件、案例、审计、历史试跑、旧 Probe 与对话内容，不得作为 runner 输入。

被授权的 method、adapter、Core、Schema 及规范性投影可以写明项目／方法身份、版本、规则名和允许引用的规范文件。仅仅出现 `S1`、方法版本或已授权规范引用的名称，不构成泄漏；只有内容超出精确绑定范围、向 runner 暴露未授权项目资料，或由链接／引用实际授予读取权限时才违反隔离。**文档中的链接只标识引用，不授予访问不存在于 packet 中的文件的权限。**

### B. 版本化、hash 固定并预审计的通用 bootstrap allow-list

通用 bootstrap 是不携带当前项目、Probe 或历史试跑特定信息的运行／角色／工具通用指令。它不并入 method packet，而须由独立 control-side manifest 逐项绑定来源归属、可取得的精确字节、长度、SHA-256、适用 scope、内容审计结论与许可作用。

run-13 候选 allow-list 只包括 [bootstrap manifest v0.1.0](run13-generic-bootstrap-context-manifest-v0.1.0.md) 固定的 `~/.codex/AGENTS.md` 捕获件：13,638 bytes，SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`。此许可只适用于实际注入字节与捕获件逐字节相同的情况；启动前必须重新核验。其它全局文件、不同版本或不同 hash 不因其“看起来通用”而自动获准，须先另行审计并加入 binding。

### C. 平台生成或不可导出的上下文

Codex／运行平台可能附加其自身生成、且无法从 runner transcript 导出完整原始字节的系统指令、工具说明或运行元数据。若字节不可取得，不得声称其完整内容已被保存、hash 固定或完全不存在。binding 与运行后记录须说明可观察的类别、来源／版本或范围、可见性限制，以及无法进行的逐字节核验。

平台上下文的存在本身不等于 project-history contamination；也不能用它推断污染不存在。发现未绑定的项目／Probe／历史特定上下文时，不得运行。对不可导出部分只能报告平台信息所能支持的范围，不能作超出证据的纯净性保证。

## 2. 内容边界与判定

- **允许的项目身份信息**：精确绑定的方法或 adapter 自身包含的版本、规则与规范引用身份；其规范内容须属于授权 packet。
- **允许的通用 bootstrap**：只限 binding 指向的已审计版本／hash，作用仅为一般 agent 行为、工具使用或平台运行。
- **禁止的未绑定特定上下文**：任何未列入精确 packet、也未列入通用 allow-list 的项目目标／私有文件内容、具体 Probe／期望答案／查询方向、旧 run／audit／conversation 历史、案例结构或目标世界事实。
- **隔离偏差（deviation）**：出现未绑定上下文，但可核对证据表明它只是通用 bootstrap，且不含项目、Probe 或历史特定信息。应如实记录来源和范围；它不自动等于 project-history contamination，也不自动证明 binding 已满足。
- **Project-history contamination**：存在证据表明 runner 接收、读取或实际使用了未授权的项目／Probe／历史特定内容。记录其具体来源、内容和受影响范围；不得把它降格为一般环境偏差。
- **来源／内容未能判清**：不能据此宣称隔离通过或 contamination 已证实；若该未知会遮蔽是否出现未授权特定上下文，启动前暂停，先查明可查证部分。

上下文 provenance 与 filesystem isolation 是两项独立核验。内容来源已绑定，不表示 runner 可读取其所在工作区；文件不可访问，也不证明 prompt 中没有注入该内容。二者都须分别检查。

## 3. 启动前检查

1. 对本轮精确 packet、所有投影及 projection map 链、allow-list manifest 和捕获字节重新计算 SHA-256；逐项与本轮 binding 对比。
2. 在全新 runner 会话和单独的平行临时目录中启动。记录实际 cwd、workspace roots、可写／可读根、packet 目录清单和执行器可观察的上下文来源。
3. 确认原项目工作区、其历史资料及其他工作区不在 runner 可访问根中。若沙箱不能阻止读取这些位置，不启动。引用链接不改变此门禁。
4. 重新取得实际注入的、可导出的 generic AGENTS 字节并逐字节核对 allow-list hash。若不匹配、无法取得以核对，或发现未审计的项目特定上下文，不启动。
5. 对不可导出的平台上下文记录其可知类别和限制；不把它写成已知不存在，也不把未知字节伪称为已审计内容。

## 4. 运行后检查

1. 原样保存 runner／creator／工具调用 trace 和环境可提供的访问记录，计算 hash；不得为补足观察项而编辑 trace 或要求 runner 重写答案。
2. 检查实际 runner 输入中的 method packet、allow-listed bootstrap、platform context 标注、工具调用和文件访问；分别报告 provenance 与 filesystem 证据。
3. 若 trace 中实际 AGENTS 字节与固定 hash 不符，或出现未授权项目／Probe／历史特定内容，标记隔离失败／project-history contamination 的具体依据；若只有一般上下文超出已绑定范围且已核实无特定资料，记作 bootstrap-context deviation。
4. 对不可导出上下文只陈述核验限制。不得把“未在 trace 中看到”写成“绝对没有发生”，也不得把一次 `search` 调用本身当作 research-loop 闭环证据。

## 5. 运行有效性边界

候选隔离合同的审计或通过，只固定未来试跑的上下文边界；不接受方法、不验证方法、不授权 S1→S2 handoff、节点级交接、W2/S2 或实际求解。每轮试跑须另有用户对该轮 binding 精确 hash 的执行授权。
