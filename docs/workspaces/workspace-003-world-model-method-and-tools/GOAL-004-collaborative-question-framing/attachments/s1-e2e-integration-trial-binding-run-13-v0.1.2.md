---
title: S1 end-to-end integration trial binding · run-13
status: draft
created: 2026-09-28
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.2
trial_status: prepared-not-run
execution_authorization: not-granted
artifact_role: control-side-trial-binding
---

# S1 end-to-end integration trial binding · run-13 · v0.1.2

本文件是供创作者裁决的 control-side 准备件。当前状态为 `trial_status: prepared-not-run`、`execution_authorization: not-granted`。v0.1.2 只封装 run-13 专用 Codex CLI 隔离 profile、bootstrap 时序和 smoke 门禁；创作者已授权 smoke preparation/verification，但**未授权输入 Probe 或创建正式 runner**。smoke 只能使用独立 disposable session 与无关安全查询。本 binding 后续通过 smoke 仍不足以启动正式试跑；正式 run-13 必须另获创作者明确授权，并在授权中引用本文件完成后的实际 SHA-256。

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

packet 应由实际字节复制进全新隔离目录。不得把任一 source/control 文件或其父工作区挂载为 runner 可读路径。

### 2.2 Control-side identity 与 projection chain（不得给 runner）

| Artifact | 精确路径 | 控制用途 | Bytes | SHA-256 |
|---|---|---|---:|---|
| v0.18.0 integrated source candidate | `stage1-framing-method-integration-candidate-v0.18.0.md` | D-048 冻结的试跑基线身份；draft/unaccepted；不是 packet 文件 | 75,486 | `6A283B02614FE23454E27773ACE29A84705763A7958454A3CD88FD132F46B4A3` |
| Projection map | `stage1-framing-method-v0.18.0-execution-projection-map-v0.1.1.md` | source→projection 映射；map 内 source hash `6A283B…4B4A3`、projection hash `4C46…CE8E8` 均与本 manifest 当前字节一致 | 4,683 | `4CB2664DEADC6EE672B3BE3625361A26B0381176A0A3C68DFFE2B63999C89BAE` |
| Trial design | `s1-e2e-integration-trial-design-run-13-v0.1.1.md` | 控制侧观察矩阵、条件触发纪律和证据边界；绝不展示给 runner | 7,523 | `C786755CC53902D4204FB77ABF1F7C90527EEC15B5C74844A41FBA518303CD30` |
| Isolation context contract | `s1-isolated-trial-context-contract-v0.1.1.md` | 候选通用隔离定义；control-only | 7,376 | `DF8DF6D34B994163E01E1A414A9EE0D8E13141B3D52CC9BF8558CA03635C308A` |
| Generic bootstrap manifest | `run13-generic-bootstrap-context-manifest-v0.1.1.md` | control-only allow-list provenance/audit；不展示给 runner | 3,574 | `D882CBE6F960C6255B1E63BE84D85EFC5B3AA36FC874FC7595E5A02383D36ACC` |
| CLI permission-profile specification | `run13-cli-permission-profile-v0.1.0.md` | control-only exact CLI profile and smoke invocation definition | 4,822 | `8C293E8F65D8ADFCF8263093CA50055710E4D4B88E0A2D759546140236E85E98` |
| Installed run-13 permission profile | `C:\Users\magicvr\.codex\run13-isolated.config.toml` | Codex CLI named profile file selected with `--profile run13-isolated`; never runner-readable | 968 | `3D8F88C02F9F79FFF41454B1BD79B1F7495883747A4EB71D01620973B421B952` |
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
2. 经预审计的通用 bootstrap allow-list manifest v0.1.1 中唯一的 `~/.codex/AGENTS.md` 捕获内容，13,638 bytes，SHA-256 `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8`。Probe 前 control side 重新读取磁盘源并核对；同启动路径的 smoke 验证实际模型可见 AGENTS 注入；正式 runner 的注入字节在运行后从 runtime trace 核验。不匹配或无法核对均不得启动／定性为有效运行。
3. Codex／平台为运行所需生成、但可能无法导出全部字节的系统／工具上下文。必须单独记录其可观察类别、版本／来源和不可导出限制；不得声称其精确全文已绑定或“绝对不存在”。出现可识别的未审计项目、Probe 或历史特定上下文则不得运行。

固定通用 bootstrap 的 provenance 许可与 filesystem access 是两件事：本条不允许 runner 访问 Codex home 文件本身。已授权方法文件写出方法／版本身份或 normative reference 名称不构成额外 project-history context；非 packet 文件仍无读取权限。

### 运行隔离与专用 CLI profile

- 新会话必须是未带前序对话的 fresh runner context，独立于本控制会话；runner 不得继承 project chat/workspace history。
- 使用与原仓库平行的临时目录 C:\Users\magicvr\Documents\Code\method-engineering-run13-isolated\。该目录当前已创建，恰有第 2.1 节五项 runner-visible packet 与 trace/ 目录。
- 普通 PowerShell 从绑定的 Codex CLI binary 启动，明确设置 -C 为该隔离目录；使用 --search exec --ignore-user-config --ignore-rules --strict-config --profile run13-isolated --skip-git-repo-check --ephemeral --json。不得 resume/fork 桌面或历史 session，不继承 project chat/workspace history；--ignore-rules 排除 user/project execpolicy 文件。
- C:\Users\magicvr\.codex\run13-isolated.config.toml 是该 CLI 唯一专用 profile 文件。它须设置 default_permissions=run13-isolated；仅将隔离目录登记为 workspace root；授予 :minimal runtime read；对 :root、原 method-engineering 仓库、旧 Codex trial area、run-11/run-12 临时目录显式 deny；隔离 root 内的 . 为 deny，五项 packet 各自只读，只有 trace/ 可写；Windows sandbox 必须为 elevated。不得继承 :workspace 或加载普通用户 config 中的 legacy sandbox_mode，不得回退到广泛 default permissions。确切 TOML 与 CLI flags 见 control-side profile spec，并纳入 hash manifest。
- smoke 与正式 runner 使用同一 binary、profile、当前工作目录、-C 与 CLI 启动方式。启动前记录 cwd、有效 workspace/read/write roots、packet 目录和执行器可观察上下文来源；若源仓库进入任何 effective readable roots，或 canary 读取未被拒绝，立即停止。目标目录及其祖先不得有 project/ancestor AGENTS.md；base user config 由 --ignore-user-config 跳过；仅 allow-list 中的 global ~/.codex/AGENTS.md 获准作为通用 bootstrap。

## 4. Run-13 过程约束

- Runner 只接收第 2.1 节五项 packet 与已核验的 allow-listed bootstrap；不接收本 binding 及 control-side 资料。
- research-loop 必须由真实 unknown 条件触发，不得要求检索或为了矩阵打卡而调用搜索。若未触发，research 与 research return 均记 `not observed`。平台强制 browse 与 host-triggered research 分开归因；单次检索调用不算闭环。
- 若自然触发 research，观察 host 如何识别 unknown 类型／owner、形成有界研究问题、选择来源、取证、评价 source/claim 和 applicability、综合、回流 Rule E/F/G 并记录 remaining unknown。无来源找到不等于对象不存在。
- semantic zoom 保持条件触发。Creator 不代 AI 设计子问题或研究来源，只作方法规定的创作取舍与结构确认。
- Runner 在 S1 creator confirmation 后停止。停止前不得查看 §2.3 条目；停止后由 reviewer 用冻结合同做 trial-only content-fit 判断。输出缺项原样记录，不得 patch trace 或要求 runner 回答内容以补齐 handoff package。
- 不发生真实 S1→S2 handoff、节点级独立交接、W2/S2 启动或目标世界实际求解。

## 5. Smoke、正式启动前与运行后门禁

**Probe 前 control-side preflight**：重算第 2 节所有 SHA-256；核对 projection map 中 source→projection 链与当前 bytes；重新读取当前 global AGENTS 原始 bytes/hash，必须等于 allow-list；核对 CLI profile config hash 与 binding；隔离目录必须只有五项 packet 和空 trace/，无 .git、无目录级／祖先级 AGENTS.md。任何不匹配均停止。

**Disposable smoke（已单独授权；不含 Probe）**：使用与正式 runner 相同的 Codex CLI binary、permission profile、-C、PowerShell 启动路径与 flags。smoke 必须证明：(1) 实际 cwd 与唯一 workspace root 是隔离目录；(2) 可只读打开非 Probe 的方法 packet canary；(3) 对原仓库 canary 的只读 open 被 sandbox 拒绝；(4) 有效 readable roots 不含 source repo、历史 trial/workspace；(5) model-visible AGENTS inputs 仅含已审计 global 文件且 hash/content 匹配，不含项目／Probe／历史 AGENTS 或历史会话；(6) Codex 原生 hosted web_search 对无害且与 Probe 无关的 query 有实际工具调用及结果。shell HTTPS/TLS 成败单独记，不代替 hosted search 验证。若 run-13 的可用研究工具不止 hosted web_search，则每个实际依赖工具另做 disposable availability smoke。任一失败即停；不输入 Probe、不创建正式 runner、不放宽 profile。

**正式运行启动前**：smoke 全通过后仍需等候创作者对 v0.1.2 最终 SHA-256 的单独执行授权。授权后重算完整 manifest，并按同一 profile/cwd/启动路径创建全新 ephemeral runner；记录不可导出平台 context 限制。任一输入 hash 不符、发现未审计 project-specific context，或 filesystem access 无法隔离，均不得输入 Probe。

**正式运行后**：完整保存 runner／creator／tool runtime trace 和可用访问日志，原样计算 hash；从正式 run 的 runtime prompt/input trace 核对实际注入 AGENTS bytes/hash。若不能取得正式 run 实际可见 AGENTS bytes/hash，则 run 不能评为有效隔离样本；若不匹配 allow-list，标记 bootstrap contamination / invalidated，发现未授权 project／Probe/history-specific context 则依隔离合同标记并说明范围。不得补写或修补 trace。检查实际文件访问。未观察到的条件机制记 `not observed`，不得补造。Reviewer 仅在 runner 停止后作 trial-only contract-content fit。

## 6. 状态与授权

- `trial_status: prepared-not-run`
- `execution_authorization: not-granted`
- 当前创作者授权仅覆盖本 binding 定义的 disposable harness smoke 与必要的准备记录，不覆盖 Probe。smoke 通过后必须再次申请正式 run-13 授权；不得创建正式 runner session 或运行本 Probe，直至收到新的明确授权。
- 用户的实际执行授权必须引用本文件完成后独立计算的精确 SHA-256；任何修改都使先前 hash 失效，须重算完整 manifest 并重新裁决。
- 本 binding 不改 v0.18.0、不接受 S1 方法、不重开 run-12、不启动 W2/S2，也不授权真实 handoff。
