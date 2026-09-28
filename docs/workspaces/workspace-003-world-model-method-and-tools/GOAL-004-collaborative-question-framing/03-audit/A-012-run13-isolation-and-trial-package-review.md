---
title: A-012 · 独立复核 run-13 隔离合同与试跑包
status: recorded
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: A-012
doc: audit-entry
source: independent
scope: run-12 disposition, generic-bootstrap classification, and run-13 isolation contract/design/binding; no trial execution
verdict: pass
---

# A-012 · 独立复核 run-13 隔离合同与试跑包（2026-09-28）

- **source**：independent
- **auditor**：Codex Reviewer subagent（gpt-6-sol，medium；按只读任务执行）
- **scope**：复核 run-12 disposition、通用 bootstrap deviation 分类、run-13 隔离合同、Probe、trial design 与 binding；不启动试跑、不修改方法、不执行 S1→S2 或 S2。
- **reviewed binding SHA-256**：`447A250197EB85973FDF75A3B3B7F2262B86A7751B1DF3577544D1E8B11E8E1F`
- **reviewer 原始 verdict**：`ACCEPT WITH NOTES`
- **本台账 verdict**：`pass`
- **required 级方法 findings**：0
- **阻止提交创作者裁决的 findings**：0

## Findings

### NOTE · Probe 保持宽泛

生态系统 Probe 仍可能自然不触发 research；试跑设计正确地允许该结果记为 `not observed`，不以搜索打卡代替真实 unknown。此项为非阻断观察，不要求修改 Probe 或强制研究。

## Verified

- Run-12 evidence matrix 将 host-triggered research-loop 与 evidence return 标为 `not observed`，确认 required 级方法 finding 为 0；A-011 的 handoff-package MAJOR 保留为运行输出／记录缺口。
- v0.18.0 仅按 D-048 冻结为下一轮试跑基线，SHA-256 为 `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3`；仍为 draft/unaccepted，方法文件未变。
- global `~/.codex/AGENTS.md` 捕获件为 13,638 UTF-8 bytes，SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`，与 run-12 注入记录及本机全局文件精确匹配。内容仅含通用 agent 执行指令；文件明确未把未记录的 runtime loader path 声称为已知，也未把该内容认定为 project-history contamination。
- 隔离合同把精确 packet、经 hash 固定与审计的通用 bootstrap、平台生成／不可导出的 context 分开；诚实记录不可导出限制，并将 context provenance 与 filesystem access 分别核验。
- run-13 raw input card 仅含单一新 Probe：“这个世界的生态系统能长期自我维持吗？”。其中无机制、taxonomy、来源、查询方向、候选答案或预期结果。research 与 semantic zoom 均为条件触发；设计要求完整研究闭环证据，不把一次搜索调用视为 research-loop。
- run-13 binding §§2.1–2.3 所列 18 项文件的当前长度与 SHA-256 全部匹配；projection map 中 source candidate 与 projection 两个 hash 均匹配当前文件字节。Binding 自身 hash 为 `447A250197EB85973FDF75A3B3B7F2262B86A7751B1DF3577544D1E8B11E8E1F`。
- 复核期间没有启动 runner 或新会话；未来实际 context injection 与 filesystem isolation 仍必须按合同在启动前核验，不能由本次 package review 预先宣称已验证。

## Verdict 与边界

`ACCEPT WITH NOTES`；唯一意见为上述非阻断 NOTE。隔离合同、design 与 binding 可提交创作者裁决。此审计不授权 run-13，不冻结或接受隔离合同，不接受 S1 方法，不授权 handoff、W2/S2 或实际求解。
