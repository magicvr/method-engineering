---
title: R4 多轮运行记录与程序性非读取协议 v0.1
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-011-r4-bounded-real-case-validation
version: 0.1.0
---

# R4 多轮运行记录与程序性非读取协议 v0.1

## 1. 目的与边界

本协议服务于 GOAL-011 多轮 R4 真实运行：所有记录集中在 `attachments/runs/`，每轮独立、可回顾、互不污染。它不是硬沙盒，也不建设通用隔离基础设施；它规定 worker 的读取纪律、运行包边界和核验规则。

**核心接受规则**：worker 被要求只读本次 run 的允许输入。若核验显示其确实未读取禁止内容，该轮可接受；若发现读取，该轮不承认（`excluded`），完整保留供诊断并另起新 run；若无法核验，不得写成 clean。

## 2. 目录 schema

```text
attachments/runs/
├── index.md                         # controller 维护的派生索引
└── RUN-NNN-slug/
    ├── input/                       # worker 可读；发布后冻结
    │   ├── packet.md                # 本轮运行说明、权限、限额、停止规则
    │   ├── raw-input.txt            # 原问正文，仅原文
    │   ├── manifest.json            # 输入清单与 SHA-256
    │   ├── runtime-authorization.md # 本轮授权与边界
    │   ├── method/                  # 冻结方法快照（工作版/两项结构/必要依赖）
    │   └── interactions/            # 方法追问后的真实用户回应 U-NNN.txt
    ├── work/                        # worker 可读写；非正式交付
    ├── output/                      # worker 可读写；结果与结构
    ├── events/                      # worker 追加事件
    └── controller/                  # worker 禁止读写
        ├── run.yaml                 # 本轮状态/评价唯一权威
        ├── provenance.yaml          # 来源、版本、哈希、包装差异
        ├── packaging-diff.md
        ├── originals/               # 被测源资产原字节快照
        ├── acceptance-criteria.md
        ├── trace/                   # 可导出的消息/工具轨迹
        ├── access-check.md
        ├── acceptance.md
        └── feedback.md
```

`index.md` 只是 `controller/run.yaml` 的投影。run 不是新 Goal，不创建五件套。不同 run 不共享 worker 可读方法目录。

## 3. worker 读写白名单

```text
READ  = input/**（manifest 允许的冻结文件）
      + input/interactions/U-*.txt（本轮已发布真实用户回应）
      + 本 worker 本轮生成的 work/**、output/**、events/**

WRITE = work/**
      + output/**
      + events/**（追加，不覆盖）
```

禁止：

- `controller/**`、其他 `RUN-*/**`、`runs/index.md`；
- Root/GOAL meta/decision/audit/goal-tree/workspace 等治理上下文；
- `.git`、Git 历史、仓库递归搜索；
- 其他线程、共享记忆、外部搜索/连接器；
- 通过绝对路径、`../`、链接或子进程绕过白名单；
- 自行追链补缺失依赖；缺材料时记录缺口并停止/等待真实用户。

## 4. run packet 最小内容

`input/packet.md` 只含执行所需内容：

- run id、协议版本、run root；
- 原始输入路径与哈希；原问不得改写；
- 被测方法快照文件清单与哈希；
- 角色：AI 为协助执行者，创作者/维护者保留设定、采用与最终裁定；
- 本轮授权与禁止范围；
- 可读文件与可写目录白名单；
- 运行限额、停止/等待规则、下一责任；
- 输出格式、事件格式、证据定位；
- 明确 worker 不得自标 accepted 或关闭 Goal。

原始输入使用 UTF-8、无 BOM、无附加换行的固定字节表示；SHA-256 按该文件字节计算。后续澄清另存 `input/interactions/U-NNN.txt`，不覆盖原问。

## 5. 方法快照与包装

- controller 保存源方法原字节快照；运行版仅保留执行所需流程、结构、角色、排除、停止和证据规则，移除治理导航/历史门禁状态/审计导航。
- 不静默删除原阶段限制；用 `packaging-diff.md` 说明“原阶段未授权真实案例，本次通过已记录授权进入 R4 有界运行，其他禁止仍有效”。
- 若包装改变方法判断或步骤，须形成新被测版本并重新核对 G-I-003；纯包装变化也要记录哈希与差异。

## 6. 运行核验与有效性

controller 在运行后核对：

- 输入与方法快照哈希是否变化；
- 启动上下文是否为新上下文，是否有自动注入的治理内容；
- 可导出的工具轨迹、命令、解析路径、子进程；
- 是否读取/修改 `controller/`、其他 run 或治理文件；
- 输出是否来自本轮 run，是否有前轮答案/外部答案/虚构用户裁定。

有效性：

- 未发现越界读取：可接受本轮运行；
- 发现越界读取：`excluded`，保留诊断，另起新 run；
- 轨迹/声明/路径核验不足：不得写成 clean，按 `indeterminate` 处理并另起新 run。

worker 的“未越界”声明只是自报，不能替代核验。

## 7. 状态、结果与本仓验收

`controller/run.yaml` 至少区分：run id、类型、协议版本、baseline、输入哈希、方法源/运行版哈希、执行者与上下文、时间、生命周期状态、方法结果、停止、证据、访问核验、有效性、本仓验收、反馈/复评。

- `completed` 只表示执行结束；正确停止/拒答可以是有效结果。
- `accepted` 须写明接受的是答案、条件结果还是合理未决边界；不等于原问题解决。
- 本仓验收人：维护者；记录在 `controller/acceptance.md`。
- 正式 independent/cross 审计由维护者在工作流外调用外部工具，AI 不代调用。

## 8. 多轮、失败、重跑与保留

- `RUN-NNN-slug`，编号三位递增不复用；reserved/failed/aborted 均占号。
- 正式验证、复跑、整改复验在开始前登记类型，不能事后把失败改称试跑。
- 新 worker 不读取旧轮输出/验收/反馈；关联原因只放 controller。
- 基础设施失败记 failed；人为终止记 aborted；隔离异常单独记 validity，部分输出标 partial。
- 终止后冻结输入、输出、事件与轨迹；后续验收/反馈追加不覆盖。
- 默认长期保留；删除/迁移/脱敏须用户另行授权。
- 全部轮次纳入回顾，说明采用/排除原因，不只展示最佳结果。
