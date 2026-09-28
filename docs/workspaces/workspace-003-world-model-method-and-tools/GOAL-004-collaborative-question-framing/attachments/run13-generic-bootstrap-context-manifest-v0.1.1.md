---
title: Run-13 通用 bootstrap context allow-list manifest
status: draft
created: 2026-09-28
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.1
artifact_role: control-only-bootstrap-allow-list
---

# Run-13 通用 bootstrap context manifest · v0.1.1

本 manifest 仅供试跑控制侧使用，不属于 runner-visible packet。它授权候选 run-13 在启动时使用下列一份、且仅这一份被固定的通用 bootstrap 文件；许可生效仍取决于启动前对实际注入字节的重新核验和 run-13 binding 的独立接受。

## 固定条目

| 字段 | 记录 |
|---|---|
| Artifact | [run12-global-agents-captured.md](run12-global-agents-captured.md) |
| 捕获长度 | 13,638 bytes |
| 捕获件 SHA-256 | `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8` |
| 来源归属 | 内容与 `C:\Users\magicvr\.codex\AGENTS.md` 精确匹配；不是 rollout 记录的运行时 `source_path` provenance |
| 取证限制 | run-12 rollout 未记录物理 loader path；来源归属基于逐字节相同、捕获 hash 和该文件位于 Codex home 的核对，不能声称执行器显式报告了该路径 |
| 审计依据 | [E-075 隔离复核](../02-execution/E-075-run12-bootstrap-context-isolation-review.md)、[D-047 创作者裁决](../01-decision/D-047-run12-limited-sample-and-bootstrap-boundary.md)；capture 内容由独立只读 Reviewer 复核为通用内容，verdict `ACCEPT`（仅针对内容／范围判断） |
| 内容判定 | 通用角色路由、agent 执行纪律、上下文管理和用户裁决指令；不含 method-engineering 项目特定信息、GOAL、Probe/run 身份、S1/S2 结构、城市机制、具体案例事实或历史试跑答案 |
| 捕获完整性 | 保存了 rollout ordinal 6 `agents_md.text` 对应的全部 UTF-8 bytes；精确字节副本 hash 与本表一致。Ordinal 5 中还出现相同文本并由外围 `<INSTRUCTIONS>` 包装 |
| 许可 scope | 仅允许在 run-13 fresh runner session 中作为通用 bootstrap context；不得作为用户 Probe 输入或方法证据，也不得据此访问 Codex home 或原工作区 |
| 生效条件 | Probe 启动前 control side 重新读取当前 `~/.codex/AGENTS.md` 并核对上述 bytes/hash；同启动路径的 disposable smoke session 核对实际模型可见 AGENTS 注入仅为该 allow-list 内容且无 project/history-specific AGENTS；正式运行后以原始 runtime trace 核验实际 AGENTS bytes/hash。任一步骤不匹配或 smoke 无法核对，则不得启动 Probe；正式运行后不匹配则标记 bootstrap contamination / invalidated，不修补 trace |

## 许可效力

该文件是基于 run-12 证据形成的固定通用 bootstrap allow-list 候选，不回写 run-12，也不改变其“有限 S1 E2E 行为样本”与 `unbound bootstrap-context deviation` 裁决。将它加入 run-13 候选 allow-list，意味着精确匹配的通用内容在 run-13 中是**预先绑定的上下文**；不意味着其它 Codex home 文件、祖先目录 `AGENTS.md`、旧工作区资料或对话历史被许可。

即使此条实际被注入，run-13 binding 仍须独立记录平台生成／不可导出 context 的可见性限制，并分别核验文件系统隔离。Probe 前的磁盘 hash 只验证候选 bootstrap 源当前身份；smoke session 验证该启动路径的实际注入；正式 runner 的实际注入须在运行后从原始 trace 核验。这些证据不能相互替代。该 manifest 本身、E-075、D-047、任何 run-12 trace 或其它历史资料均不得交给 runner。
