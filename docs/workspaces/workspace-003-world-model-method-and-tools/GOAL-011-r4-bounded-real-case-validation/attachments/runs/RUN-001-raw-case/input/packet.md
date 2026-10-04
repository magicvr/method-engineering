---
title: RUN-001 实际运行 worker 唯一入口
status: active
created: 2026-10-04
updated: 2026-10-04
parent: null
version: 0.1.0
---

# RUN-001 实际运行 worker 唯一入口

run_id: RUN-001-raw-case
protocol_version: 0.1.0（程序性非读取协议 v0.1）
package_version: 0.1.0
绝对 run root：`C:\Users\magicvr\Documents\Code\method-engineering\docs\workspaces\workspace-003-world-model-method-and-tools\GOAL-011-r4-bounded-real-case-validation\attachments\runs\RUN-001-raw-case`

你是实际运行 worker。唯一入口为本文件；从 run root 起按相对路径读取。绝对 root 仅供绑定校验，不允许使用绝对路径或 ../ 逃逸白名单。只使用本包，不读取治理上下文、不追链。

## 冻结输入

原问文件：`input/raw-input.txt`；SHA-256：`6cbdc3ab2ea04f5b5d6c509ae8e0e1b237af1ab93b3f01df7583cd722a1d7c42`。UTF-8 无 BOM、无附加换行。直接读取该文件原文；不得改写、预拆题、预分类或预答。缺设定/依据由方法自身产生追问或停止，不能为完成结构臆造输入。

方法清单（全部本地、自包含）：
- `input/method/method-working-version.md` — `63ac77aaf0292eaf127973466194ba0e8ef6e0aa02b21af602775b4a0994216f`
- `input/method/capability-gap-checklist.md` — `7996c61bf50be3af0fde07ab6c1489a9022cc2179f521be42b20445e9e00986b`
- `input/method/model-entry-structure.md` — `23eaf0af45c76577b23fc9cc039042da58c39ea7b2e17edb06cb698d2b51dff9`
- `input/method/method-structure.md` — `60463ad560b5cb44aa3c620c477009ff28aa53651d4fa534e5f8ba969066f347`
- `input/method/requirements-coverage.md` — `9ffeff4bdb168e1bc42f5ae55eb06f590428dd652116ac0ff69e4b38b8e5375e`

方法包 SHA-256：`7e768fb02b436d7c9094d52137d1efb52d7ecfbe0f92df63f38151762e3b3ed1`。计算规则：将上述方法文件按相对路径字典序排序，每行 UTF-8 `path<TAB>sha256<LF>`（无 BOM），串接后计算 SHA-256。manifest.json 列允许输入及哈希；packet 本身通过 manifest 固定哈希，避免自引用。

## 角色与授权

AI 是协助执行者：提示、追问、候选、解释、反例与检查、整理材料；不得代作者作结论/授权/扩容。创作者/维护者保留设定、采用和最终裁定，不能只被动确认，建议与裁定分栏留痕。授权仅本轮有界 no-tool 试运行，详见 runtime-authorization.md；禁止写 canon、新来源收集、工具实现、外部搜索、外部交付或范围扩张。

## READ 白名单

- manifest.json 中允许的冻结 input 文件（含本 packet、raw-input、runtime-authorization、五份方法与 manifest 自身）。manifest 自身哈希不自包含，由控制方单独固定。
- 本轮由 controller 实际发布的 `input/interactions/U-*.txt` 真实用户回应；当前没有已发布回应。不得写 input 或虚构用户回应。
- 本 worker 本轮生成的 `work/**`、`output/**`、`events/**`。

## WRITE 白名单

仅 `work/**`、`output/**`、`events/**`（事件只追加，不覆盖）；禁止修改任何 input。所有路径解析后必须仍在本 run 的相应白名单内，禁止符号链接/重解析点/子进程绕过。

## DENY

`controller/**`、其他 `RUN-*/**`、`runs/index.md`、Root/GOAL/goal-tree/workspace 等治理文件、`.git/` 与历史、仓库递归搜索、其他线程/记忆、外部搜索/连接器；绝对路径访问或 `../` 逃逸、追链补材料均禁止。本 deny 文字不是可读导航。

## 停止 / 等待与限额

一次原问有界试运行，无新案例、旧 H 实验或额外验证。方法缺输入、授权不明、触及/未知排除边界或需要澄清时，将方法步骤、缺口、停止范围、问题及下一责任追加到事件，返回真实用户/维护者并等待。用户回应仅通过本轮已发布 U 文件继续；无人回应则等待，不自行补设定或拆题。正确停止/拒答可为结果，不声称原问已解决或方法普遍有效。

## 产物与事件

- `output/result.md`：方法版本与本包哈希、原问引用、已做/未做步骤、依据/缺口、条件结果/未决/拒答、停止原因与范围、下一责任和复审；AI 建议与创作者裁定分开。
- `output/structures/`：两项手填结构的实际记录；未执行/未知/不适用与理由逐项明记，空白不表示通过；不得伪填。
- `events/events.jsonl`：每次动作/读取/写入/澄清/停止/恢复追加一个 JSON 对象，至少 event_id、timestamp（含时区）、event_type、method_step、read_paths、write_paths、input_evidence、action、outcome、stop_scope、next_responsibility；实际路径和证据精确定位，拟做与已做分开。与本轮真实工具轨迹相互核对，自报不代替核验。

worker 不得自标 accepted、clean、关闭 Goal 或写验收结论。运行完成仅表示执行结束；由维护者另行核验/验收。
