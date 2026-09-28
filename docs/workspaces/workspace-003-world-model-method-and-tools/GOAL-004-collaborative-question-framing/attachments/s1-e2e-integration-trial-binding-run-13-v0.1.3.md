---
title: S1 end-to-end integration trial binding · run-13
status: draft
created: 2026-09-28
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.3
trial_status: not-run
execution_authorization: not-granted
artifact_role: control-side-trial-binding
---

# S1 end-to-end integration trial binding · run-13 · v0.1.3

本文件是供创作者裁决的 control-side 准备件。当前状态为 trial_status: not-run、execution_authorization: not-granted。v0.1.3 将隔离标准限定为 methodological context isolation：通过 fresh Codex conversation、独立 sibling trial directory、精确 packet、已审计 generic bootstrap 与运行后 trace 检查，避免 project／Probe／history-specific 内容实际进入 runner 或被读取；不要求 adversarial OS/filesystem security proof。run-13 Probe 尚未输入。此 binding 的完整 manifest 核对后，仍须创作者对本文件最终 SHA-256 另行明确授权，方可创建正式 runner。

## 1. 试跑身份与范围

- **Run ID**：`run-13`。
- **目的**：以单一新 Probe 观察 S1 v0.18.0 integration candidate 与 Shared Research Loop 组件能否在完整 S1 运行中自然组合，重点补充 run-12 未观察到的 host-triggered research-loop 与 evidence return 行为样本。
- **方法身份**：v0.18.0 source candidate 当前精确字节 SHA-256 `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3`，依 D-048 冻结为下一轮试跑基线；仍为 draft/unaccepted，不改写、不接受方法。
- **Probe**：仅 [run-13 raw input card](s1-integration-trial-input-card-run13-v0.1.1.md) 中的单一问题。该输入卡只有问题文本，没有机制、taxonomy、来源、查询方向、候选答案或预期结果。
- **研究原则**：research-loop 按真实 unknown 条件触发，不设固定搜索步骤。未自然触发则记 `not observed`；不得为了覆盖观察表强行调用。搜索工具调用本身不算研究闭环证据。
- **semantic zoom**：仅在真实需要时触发；不得提示或要求 runner 必须递归。
- **结果边界**：单轮行为样本，不证明普遍有效、目标世界事实、全量覆盖、方法接受或实际 handoff。

## 2. 精确 hash manifest

SHA-256 均以实际完整原始字节计算。相对路径以本文件所在 `attachments/` 为基准；绝对路径按字面固定。正式 Probe 启动前须重算完整 manifest；任一不匹配均不得运行。Projection map 链须同时满足 map 中记载的 source candidate hash 与 projection hash 均匹配当前字节。

### 2.1 Runner-visible method packet（仅下列五项）

| Artifact | 精确路径 | 身份／作用 | Bytes | SHA-256 |
|---|---|---|---:|---|
| Clean S1 execution projection | `stage1-framing-method-v0.18.0-execution-projection-v0.1.0.md` | v0.18.0 的 runner-visible method text；投影不是新方法版本 | 44,841 | `4C46CB78BC2E13F63CA91FB584D51966642BEFCFD8A8C0613B4C6F9E021CE8E8` |
| Shared Research Core | `../../GOAL-005-shared-research-loop/attachments/shared-research-loop-core-v0.1.0.md` | v0.1.0 已接受的组件设计基线；不是 host 集成或本轮验证证据 | 8,094 | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema | `../../GOAL-005-shared-research-loop/attachments/shared-research-record-schema-v0.1.0.md` | v0.1.0 已接受的组件设计基线；保留现有记录结构 | 5,922 | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |
| S1 Research Adapter | `../../GOAL-005-shared-research-loop/attachments/s1-research-adapter-v0.1.1.md` | v0.1.1；既有语义照用 | 5,812 | `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C` |
| Raw Probe input card | `s1-integration-trial-input-card-run13-v0.1.1.md` | 单一问题；packet 中唯一案例输入 | 46 | `6B3034DFA6A7E5106EFD413C3736C658F8F6C784BC86309ECA0600CEECA8CB10` |

packet 应按实际字节复制进原仓库之外的 sibling trial directory。不得主动加载或提供 source/control-side 内容。

### 2.2 Control-side identity 与 projection chain（不得给 runner）

| Artifact | 精确路径 | 控制用途 | Bytes | SHA-256 |
|---|---|---|---:|---|
| v0.18.0 integrated source candidate | `stage1-framing-method-integration-candidate-v0.18.0.md` | D-048 冻结的试跑基线身份；draft/unaccepted；不是 packet 文件 | 75,486 | `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3` |
| Projection map | `stage1-framing-method-v0.18.0-execution-projection-map-v0.1.1.md` | source→projection 映射；map 内 source hash `6A283B…4B4A3`、projection hash `4C46…CE8E8` 均与本 manifest 当前字节一致 | 4,683 | `4CB2664DEADC6EE672B3BE3625361A26B0381176A0A3C68DFFE2B63999C89BAE` |
| Trial design | `s1-e2e-integration-trial-design-run-13-v0.1.1.md` | 控制侧观察矩阵、条件触发纪律和证据边界；绝不展示给 runner | 7,523 | `C786755CC53902D4204FB77ABF1F7C90527EEC15B5C74844A41FBA518303CD30` |
| Isolation context contract | s1-isolated-trial-context-contract-v0.1.2.md | methodological context isolation contract; control-only | 6,474 | 05DB754BBFA3F61EE628CEDAE66AEE4E593FC5654CCB6C0DC5A7807EAF813635 |
| Generic bootstrap manifest | `run13-generic-bootstrap-context-manifest-v0.1.1.md` | control-only allow-list provenance/audit；不展示给 runner | 3,574 | `D882CBE6F960C6255B1E63BE84D85EFC5B3AA36FC874FC7595E5A02383D36ACC` |
| Captured generic bootstrap bytes | run12-global-agents-captured.md | Audited generic bootstrap identity reference; pre-run checks current global file hash | 13,638 | 15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8 |

### 2.3 Reviewer-only / control-side evaluator references

仅在 runner 完成 S1 creator confirmation 并停止后，reviewer 可使用以下文件作 trial-only contract-content fit 复核；不得让 runner 查看这些文件，也不得因此实际 handoff。

| Artifact | 精确路径 | Bytes | SHA-256 |
|---|---|---:|---|
| Frozen S1→S2 handoff contract | `s1-to-s2-handoff-contract-v0.1.1.md` | 11,517 | `E14B6E8CF2824DA1423F5F07B347CDBDE32ADB854000791D50DCD69C8F0B53C9` |
| E-064 freeze-time snapshot clarification | `../02-execution/E-064-clarify-frozen-contract-case-snapshot.md` | 1,911 | `DE817BF230C06054B42BD9F16589C1FD20C8918B2A424FFFBA72D81470DE57AB` |
| A-011 run-12 independent behavior review | `../03-audit/A-011-run12-s1-e2e-behavior-review.md` | 4,875 | `8B7846E1D80B9B611D1A061D98C5B8E63C3B7C39FC3784C88393C1A4353D07DC` |
| E-077 run-12 disposition/evidence matrix | `../02-execution/E-077-run12-review-disposition-and-v018-baseline.md` | 3,104 | `79D65DD3CDE7AF2A345C601F87CFE8FCFFE6E71C936E2EBB6C73025AA0B304BC` |
| D-047 bootstrap disposition | `../01-decision/D-047-run12-limited-sample-and-bootstrap-boundary.md` | 2,268 | `8A7D26821A14F397094FDD18A6764845B463B5F5D4BC6EC71B62426F74F03723` |
| D-048 v0.18.0 trial-baseline freeze | `../01-decision/D-048-run12-review-and-freeze-v018-trial-baseline.md` | 2,121 | `832664DA2D6A2D368732B23F614C4C206DF6E21B03AA1D24B16A4ABCD58BC12A` |
| E-075 bootstrap source/scope review | `../02-execution/E-075-run12-bootstrap-context-isolation-review.md` | 3,700 | `C33641C433A52105D8328529C0E22831949FC44FDFA03AA9C8789A54ABDEC786` |

以上 reviewer/control references 的身份并非 runner 权限；链接不允许 runner 自行打开或读取 workspace 文件。

## 3. 方法上下文隔离

### 允许的上下文

1. Runner 的试跑专属方法上下文仅限于 §2.1 所列五项 packet。
2. run-13 唯一额外允许的项目无关 bootstrap 是 generic bootstrap manifest v0.1.1 中已审计的全局 ~/.codex/AGENTS.md：13,638 bytes，SHA-256 为 15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8。启动前由 control side 核对当前文件 hash；hash 未变化时，不要求每轮提取或逐字节核验 runtime loader 的注入内容。
3. 通用 system/platform context 与已审计 generic bootstrap 不构成污染。若实际 trace 显示任何上下文中出现未授权的项目、Probe 或历史特定内容，按 runner 实际收到的内容判定。

### 上下文边界

不得主动加载或提供 method-engineering 仓库、旧 run/audit、此前的 Probe、binding/design/contract 等控制资料或 conversation history。不得向 runner 展示本 binding 或其它 control-side 文件。授权 packet 中的链接或规范名称本身不授予访问其它文件的权限。

Runner 理论上能够访问 trial directory 之外的文件，不构成隔离失败。隔离判断依据是 runner 实际收到或读取了什么，由 runtime trace 与可用访问记录判定。本 binding 不要求 OS 级 root-deny 或 filesystem-deny 证明、elevated sandbox、readable-root 独占证明、仓库 canary 被拒绝、shell 能力 smoke、hosted web-search smoke、VM 或 Docker。

## 4. Run-13 过程约束

- Runner 的试跑专属内容只包括第 2.1 节五项 packet。另允许已审计 generic bootstrap 和系统／平台通用上下文；不向 runner 提供本 binding 及其它 control-side 资料。
- research-loop 必须由真实 unknown 条件触发，不得要求检索或为了矩阵打卡而调用搜索。若未触发，research 与 research return 均记 `not observed`。平台强制 browse 与 host-triggered research 分开归因；单次检索调用不算闭环。
- 若自然触发 research，观察 host 如何识别 unknown 类型／owner、形成有界研究问题、选择来源、取证、评价 source/claim 和 applicability、综合、回流 Rule E/F/G 并记录 remaining unknown。无来源找到不等于对象不存在。
- semantic zoom 保持条件触发。Creator 不代 AI 设计子问题或研究来源，只作方法规定的创作取舍与结构确认。
- Runner 在 S1 creator confirmation 后停止。停止前不得查看 §2.3 条目；停止后由 reviewer 用冻结合同做 trial-only content-fit 判断。输出缺项原样记录，不得 patch trace 或要求 runner 回答内容以补齐 handoff package。
- 不发生真实 S1→S2 handoff、节点级独立交接、W2/S2 启动或目标世界实际求解。

## 5. 启动、运行后与有效性门禁

**启动前**：重算本 binding 所列 packet 与 source/projection chain 的 SHA-256，并逐项匹配 manifest。重新读取 `C:\Users\magicvr\.codex\AGENTS.md`，确认其 hash 与已审计 allow-list 相同。创建 fresh Codex conversation/session；cwd/workspace 指向原仓库之外的独立 sibling trial directory：`C:\Users\magicvr\Documents\Code\method-engineering-run13-isolated`。该目录初始只含 §2.1 五项 packet 与必要输出目录 trace/。确认 trial directory 及其 ancestor 不存在 project-specific AGENTS.md。不得主动加载或提供原仓库、旧 Probe/run/audit、binding/design/contract 或历史 conversation。满足以上条件并取得授权后即可启动；不要求 shell、filesystem-security 或 research-tool smoke。

**执行授权**：完整 manifest 与启动前条件就绪后，仍须先取得对本 binding 最终 SHA-256 的明确执行授权。授权前不创建正式 runner、不输入 Probe。授权只覆盖本轮 S1 runner；不授权实际 handoff、节点级独立交接或启动 W2/S2。

**正式运行后**：原样保存 runner／creator／tool runtime trace 和可用访问记录，计算 hash，不补写或修补 trace。检查实际收到的上下文和读取记录：若 runner 实际收到或读取未授权 project／Probe／history-specific 内容，标记 methodological context contamination / invalidated，并记录具体内容和影响范围；若未发现此类注入或读取，methodological context isolation 视为满足。runner 理论上能访问其它文件本身不构成失败。系统／平台通用上下文及已审计 generic bootstrap 不构成污染。无需从 runtime loader 提取其注入副本；但不得忽略 trace 中实际出现的未授权特定内容。

**研究工具**：research 仍按真实 unknown 条件触发，不为测试强制调用。若实际触发时所需工具不可用，只记录 tool-access limitation；不因此预先阻断本轮。未触发记录为 not observed。Runner 在 creator confirmation 后停止；停止后 reviewer 才使用 §2.3 frozen contract 做 trial-only contract-content fit，不发生真实交接。

## 6. 状态与授权

- trial_status: not-run
- `execution_authorization: not-granted`
- 当前状态为 not-run，execution authorization 尚未授予。此文件及其最终 hash 提交创作者裁决；只有收到引用该 hash 的明确授权后，才可输入 Probe 并启动正式 runner。
- 用户的实际执行授权必须引用本文件最终字节的精确 SHA-256；任何修改都使先前 hash 失效，须重算完整 manifest 并重新裁决。
- 本 binding 不改 v0.18.0、不接受 S1 方法、不重开 run-12、不启动 W2/S2，也不授权真实 handoff。
