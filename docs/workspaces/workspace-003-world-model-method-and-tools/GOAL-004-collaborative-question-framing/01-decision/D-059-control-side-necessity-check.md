---
title: 采用控制侧 necessity check 并修正 run-14 后续判断边界
status: accepted
created: 2026-09-29
updated: 2026-09-29
parent: GOAL-002-r2-method-working-version
version: 0.1.0
id: GOAL-004-collaborative-question-framing
record_id: D-059
doc: decision-entry
decision_status: accepted
---

# D-059 · 采用控制侧 necessity check 并修正 run-14 后续判断边界

## 决定

后续控制侧准备作出“必须 X，所以……”判断时，先按本记录检查 X 是否确为当前目标的必要条件。此约束用于控制侧的目标、运行和证据判断；不修改 S1 方法、Shared Research Core/Schema/Adapter、run-14 binding 或运行结果。

### Necessity check

1. **回到目标与已接受契约**：明确本轮真正需要证明/观察的结果，并列出方法、binding、contract 或 creator 明文定义的 required 条件；不得从历史运行轨迹反推新的 required 条件。
2. **分开目标、路径、证据**：目标是本轮要达到或观察什么；路径是某次运行曾如何完成；证据是本轮实际观察到什么。一次成功路径不是唯一合法路径，历史行为也不是方法必经步骤。
3. **验证必要性**：“有帮助”“可能有风险”“无法排除”不足以推出 necessary。只有能指出没有 X 时，按当前目标定义的 Y 无法成立，才把 X 记为 required。
4. **不从 possibility 推出 absolute requirement**：理论可访问不等于实际污染；答案可能需要领域知识不等于 S1 framing 需要 research。只有未经授权的特定内容实际进入/被读取才是 contamination；只有 framing 本身不能在不依赖该知识时确定，才构成 S1-level research dependency。
5. **保留多条合法路径**：除非已接受方法或契约明文要求，不从多条合法路径中选一条作为规范路径。记录每条合法路径及本次实际走过的路径；若实验只观察其中一种，按实际观察记 outcome，不倒逼 runner 改走另一条。
6. **进行需求增量审计**：从观察提出新 requirement 前，检查其来源、是否由当前目标直接蕴含，以及是否只为方便评分、排除所有可能风险或沿袭历史路径而加入。后一类默认只登记为 observation、risk 或 candidate hypothesis，等待独立证据，不加入 requirement。

### 何时属于 S1-level research dependency

这项判断用于控制侧区分 framing 未知与阶段二领域求解，不是给 runner 新增 research gate，也不把 research 变成固定步骤。依据现有 S1 Research Adapter：

- 先指出一个具体且尚未解决的未知；单纯“最终答案需要领域知识”不够。
- 说明如果该未知不同，S1 的候选问题、关系/依赖、反例、边界或局部/全局影响中的哪一项会改变。仅改变 B3 的答案或答案细节，不构成 S1 framing dependency。
- 判断外部资料是否可能为这个 framing 判断提供有用依据；仅可用于目标世界内部求解的事实，仍归 S2/B3，外部资料只能作为有迁移限制的一般机制/模型参考。
- 只有当没有该知识就无法负责任地确定所需的问题结构或对象边界时，才称其为 S1-level dependency。若当前输入、推理或 creator 的真实取舍已足以确定 framing，research 不是必要路径；Adapter 条件满足时它仍可能是一个可选、有用路径。

若有明确 S1-level dependency，外部研究是否实际调用仍按现有 Adapter 条件决定；若未调用，不因“可研究”本身判失败。实际 research-return 进入 E/F/结构/B3 后，才按适用规则检查 Demand Preservation。

## 对 run-14 的具体修正

- run-13 曾自然触发 research，只证明 research 是一种合法执行路径；不证明它是同一 Probe 或 S1 的必要路径。
- run-14 未触发 research，依预先接受的 binding 记为 `not observed / inconclusive`：目标现象未被观察，不表示被测方法错误，也不构成漏做 required 步骤。
- 不以“更容易触发 research”作为新 Probe 的必要设计目标，不为获取回归证据而诱导 runner 搜索。
- 若将来仍要评价 research-return Demand Preservation，先明确某项真实未知为何属于 S1-level dependency、如何依现有 Adapter 的调用条件影响必要问题结构/边界；只有这一依赖获得依据后，才决定是否需要相应 Probe。即使设计 Probe，research 仍是条件触发路径；未发生时按预先判据记录，不算失败。
- 本项后续指引修正 D-058 中“再判断是否需要更适合自然触发 research-return 的独立回归 Probe”的表述：该句不构成必须继续设计 Probe 的要求，也不把更高 research 触发可能性设为选题目标。D-058 原文作为历史裁决保留。

## 未改变的事项

run-14 outcome、run-14 binding、v0.18.2 冻结身份与 A-019 disposition 保持不变。此决定不创建新 Probe、不授权 trial/binding/handoff/S2，不修改方法正文，也不把 run-14 评为正向或负向方法证据。
