---
title: S1 end-to-end integration trial binding · run-13
status: draft
created: 2026-09-28
updated: 2026-09-28
parent: GOAL-002-r2-method-working-version
version: 0.1.1
trial_status: prepared-not-run
execution_authorization: not-granted
artifact_role: control-side-trial-binding
---

# S1 end-to-end integration trial binding · run-13 · v0.1.1

本文件是供创作者裁决的 control-side 准备件。当前状态为 `trial_status: prepared-not-run`、`execution_authorization: not-granted`。没有启动 runner，也未创建执行会话。**本 binding 的接受仍不足以启动；启动必须另获创作者明确授权，并在授权中引用本文件完成后的实际 SHA-256。**

## 1. 试跑身份与范围

- **Run ID**：`run-13`。
- **目的**：以单一新 Probe 观察 S1 v0.18.0 integration candidate 与 Shared Research Loop 组件能否在完整 S1 运行中自然组合，重点补充 run-12 未观察到的 host-triggered research-loop 与 evidence return 行为样本。
- **方法身份**：v0.18.0 source candidate 当前精确字节 SHA-256 `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3`，依 D-048 冻结为下一轮试跑基线；仍为 draft/unaccepted，不改写、不接受方法。
- **Probe**：仅 [run-13 raw input card](s1-integration-trial-input-card-run13-v0.1.1.md) 中的单一问题。该输入卡只有问题文本，没有机制、taxonomy、来源、查询方向、候选答案或预期结果。
- **研究原则**：research-loop 按真实 unknown 条件触发，不设固定搜索步骤。未自然触发则记 `not observed`；不得为了覆盖观察表强行调用。搜索工具调用本身不算研究闭环证据。
- **semantic zoom**：仅在真实需要时触发；不得提示或要求 runner 必须递归。
- **结果边界**：单轮行为样本，不证明普遍有效、目标世界事实、全量覆盖、方法接受或实际 handoff。

## 2. 精确 hash manifest

SHA-256 均以仓库当前工作区内对应文件的完整原始字节计算。表内相对路径以本文件所在 `attachments/` 为基准。启动前必须从实际 packet 重算全部 hash；任一不匹配均不得运行。Projection map 链须同时满足 map 中记载的 source candidate hash 与 projection hash 均匹配当前字节。

### 2.1 Runner-visible method packet（仅下列五项）

| Artifact | 精确路径 | 身份／作用 | Bytes | SHA-256 |
|---|---|---|---:|---|
| Clean S1 execution projection | `stage1-framing-method-v0.18.0-execution-projection-v0.1.0.md` | v0.18.0 的 runner-visible method text；投影不是新方法版本 | 44,841 | `4C46CB78BC2E13F63CA91FB584D51966642BEFCFD8A8C0613B4C6F9E021CE8E8` |
| Shared Research Core | `../../GOAL-005-shared-research-loop/attachments/shared-research-loop-core-v0.1.0.md` | v0.1.0 已接受的组件设计基线；不是 host 集成或本轮验证证据 | 8,094 | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema | `../../GOAL-005-shared-research-loop/attachments/shared-research-record-schema-v0.1.0.md` | v0.1.0 已接受的组件设计基线；保留现有记录结构 | 5,922 | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |
| S1 Research Adapter | `../../GOAL-005-shared-research-loop/attachments/s1-research-adapter-v0.1.1.md` | v0.1.1；既有语义照用 | 5,812 | `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C` |
| Raw Probe input card | `s1-integration-trial-input-card-run13-v0.1.1.md` | 单一问题；packet 中唯一案例输入 | 46 | `6B3034DFA6A7E5106EFD413C3736C658F8F6C784BC86309ECA0600CEECA8CB10` |

packet 应由实际字节复制进全新隔离目录。不得把任一 source/control 文件或其父工作区挂载为 runner 可读路径。

### 2.2 Control-side identity 与 projection chain（不得给 runner）

| Artifact | 精确路径 | 控制用途 | Bytes | SHA-256 |
|---|---|---|---:|---|
| v0.18.0 integrated source candidate | `stage1-framing-method-integration-candidate-v0.18.0.md` | D-048 冻结的试跑基线身份；draft/unaccepted；不是 packet 文件 | 75,486 | `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3` |
| Projection map | `stage1-framing-method-v0.18.0-execution-projection-map-v0.1.1.md` | source→projection 映射；map 内 source hash `6A283B…4B4A3`、projection hash `4C46…CE8E8` 均与本 manifest 当前字节一致 | 4,683 | `4CB2664DEADC6EE672B3BE3625361A26B0381176A0A3C68DFFE2B63999C89BAE` |
| Trial design | `s1-e2e-integration-trial-design-run-13-v0.1.1.md` | 控制侧观察矩阵、条件触发纪律和证据边界；绝不展示给 runner | 7,523 | `C786755CC53902D4204FB77ABF1F7C90527EEC15B5C74844A41FBA518303CD30` |
| Isolation context contract | `s1-isolated-trial-context-contract-v0.1.0.md` | 候选通用隔离定义；控制侧 | 6,664 | `C03EDE6BED5098D6235F4A455D06465D3B46157E2220232158334176C628D459` |
| Generic bootstrap manifest | `run13-generic-bootstrap-context-manifest-v0.1.0.md` | control-only allow-list provenance/audit；不展示给 runner | 3,094 | `7EA0A62C2BE59E83932B69E5F89F992F73A59380FA1950799B09B45BD3AA655F` |
| Captured generic bootstrap bytes | `run12-global-agents-captured.md` | allow-listed bootstrap 参考副本；不得作为 packet file；真实注入字节启动前需重核 | 13,638 | `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8` |

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

## 3. Context allow-list、隔离环境与排除项

### Allow-list

1. 第 2.1 节五项精确 runner-visible packet。
2. 经预审计的通用 bootstrap allow-list manifest v0.1.0 中唯一的 `~/.codex/AGENTS.md` 捕获内容，且实际注入 bytes 与 SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8` 完全匹配。启动时必须重新核验实际注入字节；不匹配或无法核对则不得运行。
3. Codex／平台为运行所需生成、但可能无法导出全部字节的系统／工具上下文。必须单独记录其可观察类别、版本／来源和不可导出限制；不得声称其精确全文已绑定或“绝对不存在”。出现可识别的未审计项目、Probe 或历史特定上下文则不得运行。

固定通用 bootstrap 的 provenance 许可与 filesystem access 是两件事：本条不允许 runner 访问 Codex home 文件本身。已授权方法文件写出方法／版本身份或 normative reference 名称不构成额外 project-history context；非 packet 文件仍无读取权限。

### 计划中的运行隔离（本 binding 接受后再设置）

- 新会话必须是未带前序对话的 fresh runner context，独立于本控制会话；runner 不得继承 project chat/workspace history。
- 使用与原仓库平行的临时目录 `C:\Users\magicvr\Documents\Code\method-engineering-run13-isolated\`。该路径目前是计划路径，准备阶段未创建、未挂载。
- 该目录应只包含第 2.1 节五项 packet 和单独保存的 trace 输出位置。runner 的可读／写 root 仅为此目录中必要范围。项目根 `method-engineering`、其上级历史目录、其它 workspace、GOAL-004/GOAL-005 工作区均不得出现在 runner 的可访问 roots。
- 启动前记录真实 cwd、workspace roots、权限范围和文件清单；检查无祖先／项目级 `AGENTS.md` 从隔离目录注入。若沙箱无法保证 runner 不能读取原 workspace，停止，不运行。
- 不挂载、不复制也不展示 source candidate、projection map、design、binding、isolation contract、bootstrap manifest、captured AGENTS、handoff contract、E-064、E-075/E-077/A-011、旧 Probe/run、审计、其它 workspace 文件或 conversation history。

## 4. Run-13 过程约束

- Runner 只接收第 2.1 节五项 packet 与已核验的 allow-listed bootstrap；不接收本 binding 及 control-side 资料。
- research-loop 必须由真实 unknown 条件触发，不得要求检索或为了矩阵打卡而调用搜索。若未触发，research 与 research return 均记 `not observed`。平台强制 browse 与 host-triggered research 分开归因；单次检索调用不算闭环。
- 若自然触发 research，观察 host 如何识别 unknown 类型／owner、形成有界研究问题、选择来源、取证、评价 source/claim 和 applicability、综合、回流 Rule E/F/G 并记录 remaining unknown。无来源找到不等于对象不存在。
- semantic zoom 保持条件触发。Creator 不代 AI 设计子问题或研究来源，只作方法规定的创作取舍与结构确认。
- Runner 在 S1 creator confirmation 后停止。停止前不得查看 §2.3 条目；停止后由 reviewer 用冻结合同做 trial-only content-fit 判断。输出缺项原样记录，不得 patch trace 或要求 runner 回答内容以补齐 handoff package。
- 不发生真实 S1→S2 handoff、节点级独立交接、W2/S2 启动或目标世界实际求解。

## 5. 启动前与运行后门禁

**启动前**：重算第 2 节所有 SHA-256；核对 projection map 中 source→projection 链与当前 bytes；核对 bootstrap manifest 与实际 AGENTS 注入；确认 fresh session／平行目录／文件系统 root；记录不可导出平台 context 限制。任一输入 hash 不符、allow-listed bootstrap hash 不符或无法核验，发现未审计 project-specific context，或 filesystem access 无法隔离，均不得启动。

**运行后**：完整保存 runner／creator／tool trace 和可用访问日志，原样计算 hash；检查实际收到的 context 与文件访问。分开报告固定 generic bootstrap、平台不可导出 context 的限制和 filesystem isolation。未观察到的条件机制记 `not observed`，不得补造。Reviewer 仅在 runner 停止后作 trial-only contract-content fit。若 trace 暴露未授权 project／Probe／history-specific context，按隔离合同分类并明确受影响范围。

## 6. 状态与授权

- `trial_status: prepared-not-run`
- `execution_authorization: not-granted`
- 该 binding、E-078 准备记录或“可以审阅”均不构成执行许可。创作者接受并单独明确授权前不得创建 runner session 或运行本 Probe。
- 用户的实际执行授权必须引用本文件完成后独立计算的精确 SHA-256；任何修改都使先前 hash 失效，须重算完整 manifest 并重新裁决。
- 本 binding 不改 v0.18.0、不接受 S1 方法、不重开 run-12、不启动 W2/S2，也不授权真实 handoff。
