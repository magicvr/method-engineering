---
title: S1 demand-preservation narrow regression trial binding · run-14
status: draft
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
artifact_role: control-side-draft-trial-binding
trial_status: not-run
execution_authorization: not-granted
---

# S1 demand-preservation trial binding · run-14 · v0.1.0

**DRAFT / PREFLIGHT ONLY.** 本文件当前精确 SHA-256 仅标识供独立 reviewer 复核的准备件；不构成 execution authorization。不得凭此 hash 启动 runner 或输入 Probe。独立 projection/map/binding preflight 完成后，须提交当时最终 binding SHA-256 并取得创作者针对该 hash 的另行明确授权。本设计不接受 v0.18.2 方法，不授权真实 handoff 或 S2。

## 1. 身份与固定范围

- Run ID：`run-14`；单次、同题、fresh-context S1 窄回归。按完整 S1 方法自然运行至 creator confirmation，随即停止。控制侧只评估 research-return 后的 demand preservation；其它 S1 能力只作上下文记录。
- 冻结方法 source：v0.18.2，83,348 bytes，SHA-256 `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6`。该 source 是 draft/unaccepted，保持原字节；runner 使用其 clean projection，不直接读取 source。
- 唯一原问由中性文件名的 input card 提供；它与已选 raw question 完全同字节。此轮不复制先前轨迹、creator 回复、研究问题、来源、机制、参数值、taxonomy、候选答案或审计材料。

## 2. 精确 manifest

SHA-256 对完整原始文件字节计算。下列相对路径以本文件所在 `attachments/` 为基准。启动前须重算所有 binding 身份与 source→projection 链；任何不匹配均停止并重新预检。

### 2.1 Runner-visible packet：仅五项

| Artifact | 相对路径 | 作用 | Bytes | SHA-256 |
|---|---|---|---:|---|
| Clean S1 execution projection v0.1.0 | `stage1-framing-method-v0.18.2-execution-projection-v0.1.0.md` | 完整 S1 运行规则；source 的执行投影，不是新方法版本 | 49,257 | `6F8F5467E25ABEFF55B13B79287BFDCB60931CA2F2CB31AD250FD8A914D40904` |
| Shared Research Core v0.1.0 | `../../GOAL-005-shared-research-loop/attachments/shared-research-loop-core-v0.1.0.md` | 已接受组件设计基线，语义不改 | 8,094 | `F25B35CB508AEE551F3743BABBC7FD1E6DB7B1E053423EF72428B9747E9917F7` |
| Shared Research Record Schema v0.1.0 | `../../GOAL-005-shared-research-loop/attachments/shared-research-record-schema-v0.1.0.md` | 既有记录结构，语义不改 | 5,922 | `5D77C9BABB75CDE12ABB162CFD96BB159F74C4CFB06297620E3A22E38ED852A8` |
| S1 Research Adapter v0.1.1 | `../../GOAL-005-shared-research-loop/attachments/s1-research-adapter-v0.1.1.md` | 按需研究 host 接口，语义不改 | 5,812 | `BBBAE96902E47753AC7844861C1F883F82640DE89AB2EED11E8530CA3807C16C` |
| Raw input card v0.1.0 | `s1-input-card-v0.1.0.md` | 唯一案例输入；中性文件名 | 46 | `6B3034DFA6A7E5106EFD413C3736C658F8F6C784BC86309ECA0600CEECA8CB10` |

正式试跑若获授权，控制侧按上述精确字节准备独立 trial packet。Runner 的 task 仅呈现中性 packet 文件名与原问，不包含 `run-13`、`run-14`、`regression`、审计标签、观察链、评分标准或历史说明。规范文本中的链接和身份名称不授予读取 packet 外文件的权限。

### 2.2 Control-only 身份链与项目资料：全部在 packet 外

| Artifact | 相对路径 | Bytes | SHA-256 | 控制用途 |
|---|---|---:|---|---|
| Frozen source v0.18.2 | `stage1-framing-method-integration-candidate-v0.18.2.md` | 83,348 | `8C859E13DDCDEDBDB820129DAD4B7CAFA8DA7E9C4E0D4BD92F3C05E7F51CF8E6` | 方法身份与冻结链 |
| Source→projection map v0.1.0 | `stage1-framing-method-v0.18.2-execution-projection-map-v0.1.0.md` | 5,456 | `D89C84D5B4A060F8FBB71F3662C3D32A44B71DF1BF04AE0A338C157E910D71F2` | 逐节保真与例句省略审查 |
| Accepted trial design v0.1.2 | `s1-demand-preservation-regression-trial-design-run-14-v0.1.2.md` | 13,885 | `BFEE36E91A33E7CD063FB9F0AF82E6E78BBA29FEBF67D79A362672095AC61A55` | 观察链和判据 |
| Accepted isolation context contract v0.1.3 | `s1-isolated-trial-context-contract-v0.1.3.md` | 7,285 | `76E2F4B289F32E78520E9D99EA8A84B76E130B970F61F6FB18CD6E0730CC293D` | fresh-context / relay / contamination 规则 |
| Audited generic bootstrap manifest v0.1.1 | `run13-generic-bootstrap-context-manifest-v0.1.1.md` | 3,574 | `D882CBE6F960C6255B1E63BE84D85EFC5B3AA36FC874FC7595E5A02383D36ACC` | 唯一项目无关 bootstrap allow-list |
| Captured global AGENTS bytes | `run12-global-agents-captured.md` | 13,638 | `15BC64EF0E9A33AAEBD780F708BEEFB44536D7722C8A55EB9CF5D0C20F053DB8` | 启动前核对 `~/.codex/AGENTS.md` 当前 hash |
| Creator scope choice D-057 | `../01-decision/D-057-select-run14-same-probe-full-s1.md` | 1,316 | `61A5446875F962EAF4F52248868C3CA061C737093F2161D061A2F4DC1D9B5EC0` | 同题、完整 S1 与停止点裁决 |
| Creator design acceptance D-058 | `../01-decision/D-058-accept-run14-design-binding-preparation.md` | 1,376 | `1F2DE2CFB7F9C4FC5804B14A6C4A66A33622805F497C5BA9E8E53A059C27BB17` | 接受设计并授权 binding 准备，不授权执行 |
| v0.18.2 baseline decision D-056 | `../01-decision/D-056-accept-v0182-and-authorize-regression-design.md` | 1,774 | `5F3C924E063AB9B5D96F4BFDBBDACE8C65B3CC03EFA63607555C4C38D63DF279` | 冻结身份与设计范围 |
| Prior subagent binding v0.1.4 | `s1-e2e-integration-trial-binding-run-13-v0.1.4.md` | 15,648 | `B9692F1034F00085509E4456C810F1909A45C32196E82672EB8CB0815F66D7A4` | 已接受的控制架构先例；历史文件，不授权本轮 |

上述文件及 frozen handoff contract、旧 run/audit/trace、parent conversation、旧 Probe 和其它 workspace 内容均不得交给 runner。Control/reviewer 可以为本轮预检与评分读取；其内容不得作为 runner 输入。

## 3. Fresh-context envelope 与 relay

在取得最终 hash 执行授权后，control 使用 `collaboration.spawn_agent` 创建唯一 runner，**显式 `fork_turns: none`**，不 fork parent conversation；该 runner 不再委派。Task 只给 §2.1 五项精确内容及通用角色指令：“当前 agent 本身就是唯一 runner；按提供的 S1 材料执行；不得再委派；在 S1 creator confirmation 后停止。”不向 runner 说明本轮的所求守恒目标、以往错误、预期分类或评分判据。

唯一额外允许的项目无关 bootstrap 为 §2.2 manifest 已审计的 `~/.codex/AGENTS.md` 当前同 hash 内容。系统/平台通用上下文允许；如实际可见内容含未授权项目、Probe 或历史特定信息，仍按实际收到或读取内容判断污染。启动前核对当前 global 文件 hash 即可，不要求 runtime loader 注入字节提取。Trial directory 只作 packet/trace 存储；共享文件系统或理论可读能力本身不构成污染，实际读取 packet 外特定资料则构成污染。不要求 OS 文件系统隔离证明、CLI/shell/web smoke 或其它未约定安全测试。

Runner 若真实需要 creator input，control 把当轮问题逐字、完整交给 creator，并把回复逐字转发，不总结、解释、改写或附带 parent context。Creator 只回答真实创作意图、用途、scope 取舍及结构确认，不替 runner 判 B1/B2/B3、答案限定／自由参数、baseline/scope diff 或提供参数值、机制、来源、查询方向。回流前的真实 creator 澄清进入当时有效需求；回流后的方法性纠正须原样记录，不能算 autonomous pass。若 creator 确实改变 scope，保留旧 baseline 并记新版本；切断比较时标为 intervention-confounded / inconclusive。

## 4. 自然触发、停止与 trace

按方法内真实 unknown 条件决定是否研究；不预先提示或强制检索。平台强制 browse 与 host-triggered research 分开记；单次工具调用不等于研究闭环。未自然触发记 `not observed`；工具真实触发但不可用，记 tool-access limitation，不做替代搜索。Semantic zoom 同样按真实条件触发。

完整保存可见 runner task、creator 问答与逐字 relay、runner 输出、研究/工具 trace 与可用访问记录，计算可保存文件的 hash；原样保留，不能事后补写、修补或为打分而要求 runner 重写。若 raw initial context 或工具 payload 不可见，明确记录范围；不得声称逐字节检查不可见 trace。若实际收到或读取未授权项目、Probe 或历史特定内容，标 `invalidated` 并记录来源、内容与影响。只有 S1 creator confirmation 后停止；不作实际 S1→S2 handoff、节点级交接、W2/S2、目标世界求解或 handoff contract fit 验收。

## 5. Control-only 观察与 outcome

从原始时间序 trace 检查：回流前有效原问/creator 输入及 demand baseline；自然 unknown/owner 与 host-triggered research；research return；实际条件角色；必要时 B3 scope diff；E/F/G 处理；适用时出口 #11 结论；creator confirmation 与 runner 停止。Baseline 须在结果进入 E/F 前记录所求、量词、答案形态、已确认 scope，未确认处标未定并保留旧版。角色按实际出现条件判断，不预设因素列表；scope diff 比较量词、自由维度、输出形态、求解范围和阶段二信息需求。“更强问题包含原答案”不证明守恒。只有 research-return 结果进入 E/F、当前结构或 B3 时执行 #11，否则记 `N/A`、不另建 baseline；普通非研究 N2 不变。

- `pass`（仅本样本）：无可见特定上下文污染；自然研究结果形成真实守恒判断机会；runner 先立可核对 baseline，自行完成角色判断与适用 scope diff，最终 active structure/B3 无无依据扩张；适用时执行出口 #11 并记结论，不适用时记 `N/A`；较强候选若曾提出，在 creator confirmation 前由 runner 自行撤回或限定；不依赖 creator 方法性纠正，S1 后停止且无 S2/handoff。
- `fail`：有效 research-return 且证据足够时，缺 baseline、用研究发现覆盖旧 baseline、将操作化／适用限定无依据升为参数空间等自由职责、以更强问题包含原答案作守恒理由、扩大职责保留在当前结构/B3 或靠 creator 方法性纠正撤回；已到 S1 停止点且 #11 条件成立，却漏检或未记结论。仅提出后自行排除的扩张候选不算失败。
- `not observed / inconclusive`：无自然 host-triggered research、无相关结果进入 E/F／结构／B3、工具或 trace 限制、或 creator scope 变更/干预使主比较无法判断。不得为得到可评分结果补搜、改 Probe、补参数或在同一 binding 下重跑。实际特定上下文污染另标 `invalidated`。

本轮不评分领域答案或断言条件在目标世界成立。Pass 只是一例同题有限正证据，不代表迁移验证、方法接受或实际交接许可。

## 6. 预检与授权状态

当前 `trial_status: not-run`、`execution_authorization: not-granted`。须由独立 reviewer 核查 map、投影的 A-014/A-016 条款、普通 N2/非研究路径和完整 manifest；控制侧提交经该 preflight 后的**最终 binding SHA-256**，再单独取得创作者引用该 hash 的执行授权。修改任一绑定文件或本文件都会使旧 hash 失效，须重算并重新裁决。本 v0.1.0 当前 hash 仅为 draft/preflight identity，不是运行许可。
