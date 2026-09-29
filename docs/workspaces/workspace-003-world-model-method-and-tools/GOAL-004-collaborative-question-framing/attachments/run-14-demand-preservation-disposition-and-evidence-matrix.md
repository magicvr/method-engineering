---
title: run-14 Demand Preservation disposition 与证据矩阵
status: recorded
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: trial-disposition
run_id: run-14
---

# run-14 Demand Preservation disposition 与证据矩阵

## 范围与判定

- Binding：run-14 v0.1.0，SHA-256 `FA71DF2215978145105F3BA600F3B827F7A0FC69E4E8932A26161D3A4AA09E9C`。
- 方法基线：v0.18.2，SHA-256 `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6`。
- 唯一评分目标：自然 research-return 路径上的 Demand Preservation。
- Trial outcome：**`not observed / inconclusive`**。
- Independent disposition review：Reviewer verdict `ACCEPT WITH NOTES`；本台账接受该有限裁决。

可见 trace 中没有 research-return 进入 E/F、当前结构或 B3。Runner 报告未调用外部研究，但没有独立工具调用日志。依 binding §5 与 design §§5–6，未发生研究回流即没有可评分的 scope-preservation 机会；因此本轮既不是 `pass` 也不是 `fail`。

## 证据矩阵

| 检查项 | 可见证据 | 判定 |
|---|---|---|
| Research-loop 是否自然触发 | Runner 最终输出报告“未调用外部研究”；可见问答与结构输出无 research-return。无独立工具日志。 | `not observed`；报告为未触发，无法从独立调用日志确认。 |
| Demand baseline 是否在 research-return 前建立 | 没有 research-return，也无触发适用条件。 | `N/A`；不得因缺少 research-specific baseline 判 fail。 |
| 回流条件的角色判断 | 没有 research-return 条件进入 E/F、结构或 B3。Runner 把操作化标准与适用范围写作未来答案说明。 | 非研究路径的相关行为只作上下文描述，不是本轮回归评分证据。 |
| B3 scope diff / 参数化逃逸 | 未出现由 research-return 带入并进入结构或 B3 的新变量，也未形成参数空间候选。 | 无可评分机会；既不 pass 也不 fail。 |
| 出口检查第 11 项 | Demand Preservation 的条件触发条件未满足。 | `N/A`。 |
| Creator 是否提供方法性纠正 | Creator 回复为“至少存在一个”“现实世界”“1. 接受并保持”，均为真实范围/结构裁决；未见方法性纠正。 | 未见 creator intervention confound。 |
| 最终 demand 是否保持 | 最终节点仍是现实世界中至少存在一个生态系统的存在性问题；Runner 将操作化标准/适用范围留作答案说明。 | 与创作者确认范围一致，但没有 research-return，故不计为 regression pass。 |
| Context contamination | 可见问答和 final output 未出现旧 Probe/run/audit 或其它项目特定信息。Runner 自报未读其它本地项目文件。初始任务文本、initial context byte dump 与独立文件/工具访问日志不可用。 | `未见可见污染`；不能声称完整 context isolation 已逐字节验证。 |
| 停止与越权边界 | Runner 在 creator confirmation 后停止；final output 称未实际 handoff、未启动 S2。 | 与 binding 停止边界一致；以可见输出为证。 |

## Independent reviewer disposition

Fresh-context independent Reviewer（`agent_type=reviewer`，gpt-6-sol，medium，read-only）认为该 `not observed / inconclusive` 处置符合 accepted binding 与 design；无 material finding。其指出的非阻断证据限制是：精确 initial spawn task、raw initial context 和独立工具日志未能在所供 trace 中验证。完整审计意见见 [A-019](../03-audit/A-019-run14-demand-preservation-disposition-review.md)。

## 后续含义

- 本轮不构成 v0.18.2 对 run-13 已知失败路径的 positive regression evidence。
- 不构成方法修改依据，也不改变 v0.18.2 冻结身份。
- 不在同一 binding 下强制重跑。
- 若仍需直接验证研究回流后的所求守恒，应另行决定是否设计一个更可能自然触发相关 research-return 的独立 Probe；本记录不创建 Probe、不授权 transfer trial。
- 不启动 S2、不执行 handoff、不表示方法正式接受。
