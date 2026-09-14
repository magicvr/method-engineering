---
doc_type: vision-review
id: VRev-002-vp-001-enter-real-operation
status: active
source: independent
created: 2026-09-14
updated: 2026-09-14
version: 0.1.0
parent: null
---

# VRev-002 · VP-001 独立审视（2026-09-14）

| 字段 | 值 |
|------|-----|
| source | independent |
| auditor | DeepSeek Harness（deepseek-flash）· `/vision-audit` 独立入口 |
| scope | vision-plan：`VP-001-enter-real-operation`，含其 D1 与关门所依赖的对齐链、安装门禁 |
| verdict | conditional |
| 建议 class | editorial |

## 范围与结论

本次审视对象是已落盘的 `docs/vision/plans/VP-001-enter-real-operation.md`（`status: planned`）及其直接对齐面：`vision/charter.md`、`vision/alignment.md`、`vision/roadmap.md`、`vision/workspaces.md`、`vision/plans/README.md`、`vision/consumer-checklist.md`、`vision/reviews.md`、`reviews/VRev-001-charter-init.md`、`architecture/principles.md` P-006。本意见为 `source: independent`；本报告是台账中第一条覆盖该 VP 的正式意见（VRev-001 的 scope 为 `charter-init`，且明确记载当时尚无 VP）。

**核对通过的部分（可核对证据）**

- **单愿景**：`vision/charter.md` 为唯一 `status: active` Charter，`vision_id: method-engineering`，`version: 0.1.0`；无第二 Charter、无争用 id。
- **机读对齐链**：VP `vision_ref: method-engineering@0.1.0` 与 Charter 的 `vision_id@version` 精确一致（不做 semver 范围）；VP `status: planned` 属 alignment §1 允许集合；`lead_workspace` 为空与「0 工作区」相容（alignment §5 要求 `planned` 允许 0 区、多区时才必填 lead）。
- **投影一致性**：`roadmap.md` 索引行、`plans/README.md`、`vision/README.md`、`consumer-checklist.md` 第 17 行的 `planned` / `vision_ref` 与 VP frontmatter 一致；未出现以索引反改 VP 状态的痕迹（权威仍在 VP 文件）。
- **VP 最小完备（P-006 §6.5）**：意图说明、方向级退出判据（5 条）、`vision_ref`、工作区绑定表、关门记录位、前提表齐备。
- **无层级错位**：D1–D3 为方向级（先后与退出方向），并显式声明「可执行纲领阶段、子目标编号、Goal status、progress% 属于后续工作区 Root」；文件内无子目标编号、无 Goal status、无 progress%。
- **语义对齐谓词 1–4 均未触发**：VP 未肯定 Charter 的非目标（VP「本波次不追求」4 条为 Charter 非目标的更窄子集），未否定或收缩 Charter 方向级成功边界 1–5，`serves_summary` 与上级意图不相反，机读链未断裂。
- **前序意见闭合**：VRev-001（self, charter-init）verdict `pass`、0 findings，无待闭合 required。

**结论**：VP-001 的方向、边界与对齐链在 vision 层成立且可核对，未发现需要改写目的/边界/非目标的理由（建议 class = `editorial`）。但**进入 D1 的条件尚不完整**：其起点基线在仓内不可核对（V-F-001），安装 MUST 行存在未闭合缺口（V-F-002）。二者均为中等严重度的 required 缺口，故 verdict 为 `conditional`，当前不宜宣称该 VP 已可推进 D1 或「方向已稳」。

**证据边界（本次未覆盖）**：无工作区（`docs/workspaces/` 不存在），故不存在可核对的区内证据、Root `plan_refs` / `primary_plan` 或目标五件套；无 Charter `strategic` 修订，故无 re-align 宽阻断可判；仓外材料（若 A-001 所述机制位于其他项目）本次未读取，也不得跨项目读取，仅按「引用缺失」处理。生产者工具链其余残留引用（`mcp/`、`docs/releases/`、dogfood 目标树等）不属本 scope，仅在构成 D1 门禁时记入 V-F-002/V-F-003/V-F-007。

## Findings

- `V-F-001`：**required**；严重度 中。
  **问题**：VP 前提 `A-001`（第 67 行）断言「当前已形成可开始工作的最小启动机制（含状态机、Frame、Challenge Gate 及相关纪律）」，但该机制的**存在性**在本治理实例内无任何可核对基线。
  **证据**：仓库全域检索 `Challenge Gate|状态机|Frame|最小启动机制` 仅命中 `docs/vision/plans/VP-001-enter-real-operation.md`（第 22、30、40、51、67 行）与 `docs/architecture/principles.md` 第 146 行一处与本波次无关的「完整自动状态机」提法；`docs/workspaces/` 不存在，无区内证据可指；VP 前提表仅 4 列（id / 假设未知 / 影响 / 状态），无「最晚需要阶段」与「验证收集动作」。
  **影响门禁**：D1（第 51 行）「以当前最小启动机制为起点」的可核对性；方向级退出判据 1（第 30 行「已经实际使用当前最小启动机制」）与判据 2（第 31 行「该机制是否足以支持…」）的比对基线；alignment §7.1「证据链接指向工作区目标」的关门核对；P-006 §6.5「影响方向已稳的假设未关闭或未 residual 前不得宣称方向已稳」。
  **关闭要求**（编辑级，二选一）：① 在前提表补基线引用——仓内路径/版本，或仓外来源的固定引用（来源 + 版本/提交 + 获取方式）；② 改写为「基线由首个工作区建立并在其 Root 信息登记中固定」，并给 A-001 补 `最晚需要阶段`，使该前提在开区后必然进入目标层 P-005 信息登记，而不静默滑过关门。

- `V-F-002`：**required**；严重度 中。
  **问题**：alignment §0.2 MUST 行「契约（若分发消费适配器）→ `{governance_root}/contracts/`」（第 49 行）当前不满足，且无用户书面 residual。
  **证据**：`docs/contracts/` 不存在；本仓确实分发消费适配器（`skills/install/{claude,codex,copilot,grok}/`、`.claude/`、`.agents/`、`.grok/`、`.github/prompts/`），故该行条件成立；`skills/contracts/skills-consumer-contract.json` 自述 `canonical.owner = docs/contracts`、`manifestPath = docs/contracts/skills-consumer-contract.json`、`schemaPath = docs/contracts/skills-consumer-contract.schema.json`，即**镜像在而 canonical 缺**；`docs/architecture/directory-layout.md` 第 74 行规定 `{governance_root}/contracts/` 为 canonical、`skills/contracts/` 为 stage 生成的逐字节镜像；`docs/vision/consumer-checklist.md` 第 8 行自记「待补齐 … 本轮不处理该安装问题」——属**已披露的开放项**，但未按 P-004 取得用户书面接受（范围 + 复审触发）。
  **影响门禁**：alignment §0.2「缺任一 MUST 行 = 不完整安装」、§6 门禁时机 1–2（完整安装判定、新建工作区/Root），即 VP-001 D1 的开区动作。
  **关闭要求**：① 将 canonical 契约落回 `docs/contracts/`，并按 directory-layout §76 stage 门禁同步 `skills/contracts/`；或 ② 由用户书面接受有界 residual（点名范围：本实例的安装判定；复审触发：下次契约/兼容声明变更或开区前复核）。本项属 P-004 用户裁决点，本意见不代为选择。

- `V-F-003`：**recommended**；严重度 低-中。
  **问题**：alignment §0.2.1（第 30 行）声明 `consumer-checklist.md`、`standalone-bootstrap.md`、principles P-006 §6.2「必须同表，禁止三处各写分裂定义」，但 `{governance_root}/standalone-bootstrap.md` 在本仓不存在，该「同表」要求无法核对。
  **证据**：链接检查显示 `docs/vision/alignment.md` 第 30、93 行 → `../standalone-bootstrap.md` 均指向缺失文件；`skills/README.md` 第 113 行同样引用 `../docs/standalone-bootstrap.md`；全仓检索无任何 `standalone-bootstrap*` 文件，git 历史中亦从未存在；`skills/core/docs/` 镜像同样缺该文件（同源缺陷）。
  **影响门禁**：同 V-F-002（完整安装判定 / 开区）。
  **关闭要求**：补齐该文件，或把 §0.2.1 / §0.4.4 的引用改为指向现存权威并说明取舍；`alignment.md` 属 stage 门禁范围，改动须同步 `skills/core/docs/vision/alignment.md`。

- `V-F-004`：**recommended**；严重度 低。
  **问题**：愿景权威面当前不在版本历史中：`git status` 显示 `docs/vision/README.md`、`charter.md`、`consumer-checklist.md`、`plans/README.md`、`roadmap.md`、`workspaces.md` 为已修改，`docs/vision/plans/VP-001-enter-real-operation.md` 为**未跟踪**；最近提交 `4a090f7` 只含 Charter 与骨架。
  **影响门禁**：不阻断对齐链；但 VP 是后续开区挂接与关门的绑定对象，未跟踪文件丢失即失去权威面。
  **关闭要求**：进入 D1 前按显式 owned paths 提交一次 checkpoint（禁止 `git add -A`；P-002 checkpoint 纪律），把 VP 与索引投影纳入历史。

- `V-F-005`：**recommended**；严重度 低。
  **问题**：P-006 §6.7（principles 第 499 行）把「新 VP 立项 → 用户确认意图」列为**强制**门（落点为 VP 文件 + 组合编排索引），但 VP-001 的「规划修订短史」只记「初创：落盘首个意图，进入真实运行」，`roadmap.md` 亦无确认留痕，独立审计无法从仓内证据核对确认是否发生。
  **证据边界**：本条只主张「缺留痕」，**不主张**用户未确认。
  **影响门禁**：VP 立项门的可核对性；VP 关门提案时的用户确认链（alignment §7.4）。
  **关闭要求**：在 VP「规划修订短史」或 `roadmap.md` 备注补一行确认记录（日期 + 确认范围），或由 `/vision` 在本报告响应区留痕。

- `V-F-006`：**recommended**；严重度 低。
  **问题**：`docs/README.md`（MUST 文件）「最小目录」树第 35 行把工作区画作 `docs/workspace-<NNN>-<slug>/` 直属子目录，与同文件第 13 行、alignment §0.1、`directory-layout.md` 第 70 行的 `{governance_root}/workspaces/workspace-<NNN>-<slug>/` 不一致；按 alignment §0.1，直属 `workspace-*/` 只触发迁移阻断。
  **影响门禁**：D1 首区 scaffold 的路径形状（误操作风险，非规则冲突；规范面本身正确）。
  **关闭要求**：该行改为 `workspaces/workspace-<NNN>-<slug>/`（editorial）。

- `V-F-007`：**recommended**；严重度 低。
  **问题**：生产者工具链与镜像一致性在本实例不可核对：① `scripts/` 目录不存在，`directory-layout.md` 第 68、74、76 行的 stage 门禁（`python scripts/stage_skills_mirrors.py`）不可执行；② 根 `AGENTS.md` 无 §8c，而 directory-layout §76 将其作为该门禁的 AI 操作入口；③ `docs/vision/README.md` 与其镜像 `skills/core/docs/vision/README.md` 的 SHA256 **不同**（前者已更新为提及 VP-001），即镜像已漂移。
  **影响门禁**：镜像一致性门禁当前不可执行、不可核对；不影响 VP-001 的对齐链，但削弱「完整安装」证据强度，并使 docs 侧后续改动无强制同步路径。
  **关闭要求**：恢复 stage 脚本路径，或记录本实例的镜像冻结/手工同步规则（含用户留痕），并同步已漂移的 `vision/README.md` 镜像。

## 声明

本意见不修改 Charter / VP / Goal status；required finding 的响应由 `/vision` 协调，实施工作交 `/govern`。原 verdict 与 finding 原文不得改写；`/vision` 的响应追加在本报告中，并按 `fixed` / `accepted-residual` / `user-overruled` 留痕。本入口不自行闭合 finding。

## 响应（`/vision` · 2026-09-14）

响应人：`/vision` 编排器。用户本轮指令：「响应 VRev-002，然后激活 VP，交 `/govern` 开设工作区」。

原 `verdict: conditional` 与 Findings 原文不改写。本响应只记录闭合路径与证据。本轮**不**宣称「方向已稳」，也不把 A-001 的充分性写成已验证。

| Finding | 闭合路径 | 说明与证据 |
|---------|----------|------------|
| `V-F-001` | **fixed** | 按关闭要求②改写 VP 前提 `A-001`：不把仓内可核对基线写成已落盘事实；基线由首个工作区建立，并在 Root P-005 信息登记中固定；补「最晚需要阶段」= 开区后、Root `S1` 方案冻结 / 开始实际使用前。实现层对应 `I-001`。证据：[`../plans/VP-001-enter-real-operation.md`](../plans/VP-001-enter-real-operation.md) 前提表；[`../../workspaces/workspace-001-enter-real-operation/GOAL-001-enter-real-operation/01-decision.md`](../../workspaces/workspace-001-enter-real-operation/GOAL-001-enter-real-operation/01-decision.md) `I-001`。 |
| `V-F-002` | **fixed** | 走关闭要求①，而非 residual。将已存在的 `skills/contracts/` 消费契约落回 canonical `{governance_root}/contracts/`。`skills-consumer-contract.json` 与 `.schema.json` 的 SHA-256 与镜像一致（json `E33AF442…5C6B`，schema `1C0BBD2E…9D98`）。本实例无 `scripts/stage_skills_mirrors.py`，无法再跑 stage；当前 docs 与 skills 侧上述两文件哈希一致，MUST 行「契约（若分发消费适配器）」已满足。未接受残余、未宣称 producer compatibility matrix 已具备。证据：`docs/contracts/`。 |
| `V-F-003` | 仍开放（recommended） | 本轮不补 `standalone-bootstrap.md`，也不改 alignment 同表条款。不阻断开区。 |
| `V-F-004` | 仍开放（recommended） | 本轮不代为 git commit。权威面仍待用户按显式 owned paths 做 checkpoint。不阻断开区。 |
| `V-F-005` | **fixed** | 在 VP「规划修订短史」补 2026-09-14 用户确认留痕：用户以 `/vision` 明确指令「没问题的话，落盘vp」确认意图与退出方向。本响应为第二处可核对确认记录。 |
| `V-F-006` | **fixed** | `docs/README.md`「最小目录」将工作区从直属 `workspace-<NNN>-<slug>/` 改为 `workspaces/workspace-<NNN>-<slug>/`。 |
| `V-F-007` | 仍开放（recommended） | 本实例无 producer `scripts/` 与 AGENTS §8c；不在本轮恢复 stage 工具链。镜像漂移不阻断 VP 对齐链与开区。 |

**开放 required**：0（`V-F-001`、`V-F-002` 均 `fixed`）。

**随后动作（本轮用户已确认）**：将 `VP-001-enter-real-operation` 标为 `active`，并由 `/govern` 开设 `workspace-001-enter-real-operation`（slug 由已确认 VP id 派生，非 `main-vision` 占位），`primary_plan` 挂本 VP。
