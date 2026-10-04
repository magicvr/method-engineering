---
title: RUN-001 访问核验
status: active
created: 2026-10-04
updated: 2026-10-04
parent: null
version: 0.1.0
---

# RUN-001 访问核验

核验对象：RUN-001 actual worker 的事件与产物；本轮仍 waiting，validity 最终结论待 S4 验收。

## 事实

- 成功读取的路径均在本 run 的 `input/**` 或本 worker 已写出的 `output/**`、`events/**`；未发现成功读取 `controller/**`、其他 run、治理文件、Git 历史或其他线程内容。
- worker 自报两次按相对路径尝试读取 run 根 `manifest.json`，文件不存在，未取得内容；正确文件为 `input/manifest.json`。这是白名单外读取尝试，但不是成功读取禁止内容。
- worker 自报一次工具调用传入绝对 `workdir` 用于绑定 run root；文件参数仍为相对路径。该参数使用与“绝对路径禁令”的关系已记录为异常，未观察到读取 run 外内容。
- 输出仅写入 `output/result.md`、`output/structures/*`、`events/events.jsonl`；未写 `controller/**` 或 run 外路径。
- 原始输入与方法快照哈希在运行记录中一致；未发现前轮答案、外部答案或虚构用户裁定。

## 当前判定

`pending`：未发现成功的越界读取，但本轮仍在等待真实用户澄清，尚未完成 S3；access check 不替代最终验收。上述两次失败读取尝试与一次绝对 workdir 参数使用保留为异常记录，供 S4 维护者复核。

若后续发现成功读取禁止内容，本轮应改为 `excluded`，另起新 run。
