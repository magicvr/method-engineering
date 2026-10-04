---
title: PA2 来源访问与定位台账 v0.1
status: active
created: 2026-10-04
updated: 2026-10-04
parent: GOAL-003-prior-art-replanning
version: 0.1.0
---

# PA2 来源访问与定位台账 v0.1

## 访问核实（2026-10-04）

| ID | 访问路径 | 自动访问结果 | 本地副本标识 | 可抽取性 |
|---|---|---|---|---|
| PA-S01 | Northwestern QRG 公开 PDF | HTTP 200，`application/pdf` | 49 页；大小 3,974,166 bytes；SHA-256 `A679C666C14CF2B6AC20B2F6BDE521F31123AB0EA2AB32A8C247B22B510ECC48` | 全文可读，进入 S2 |
| PA-S02 | Northwestern QRG 公开 PDF | HTTP 200，`application/pdf` | 86 页；大小 5,028,115 bytes；SHA-256 `A0490710236298DDDFA6ADAC83E9D801B738B8080BE5661B634BC125295E6BEA` | 全文可读，进入 S2 |
| PA-S03 | UCSD 大学托管公开 PDF | HTTP 200，`application/pdf` | 26 页；大小 1,586,173 bytes；SHA-256 `ADA7E5613A9E20ECDC6DDEB8ECFF5BF10EC04B44953AB27E5F9B1140D08FB7E3` | 全文可读，进入 S2 |
| PA-S04-C | Wiley 官方 `doi/full/10.1002/sdr.1601` | 页面标注 Free to Read；自动化请求返回 HTTP 403 | 未保存全文；仅官方摘要/书目 | 全文 unresolved；不得冒充已抽取 |
| PA-S04-D | OSTI 公开 PDF `servlets/purl/2477558` | HTTP 200，PDF 可下载 | 16 页；大小 269,559 bytes；SHA-256 `67871024375AC011F5063D45447E4CBA9183DA41F3AD5D0776548D25D11ACD89` | 全文可读，进入 S3 |
| PA-S05 | PMC `PMC128598` HTML | HTTP 200，HTML 可读 | HTML 159,041 bytes；SHA-256 `FAF8AB676D82433FECFFE54E5281820A367D34CC905D60F1055AAF8DF5A47D93`；提取文本 SHA-256 `0D5D0A83B90920BF52C1D64B2948828476ECD5462C10C5B9AECEB8A53F36D190` | 全文可读，进入 S3 |

## S1 结论

- 抽取字段固定为：要素 ID、来源 ID/版次、原文定位、要素/局部主张、前提、输入/输出、适用范围/限制/反例线索、证据等级、冲突/未决。
- 进入抽取的已核实全文为 PA-S01、PA-S02、PA-S03、PA-S04-D、PA-S05；PA-S04-C 保持 unresolved，不使用未核实的第三方副本替代。
- 来源内容只用于内部 PA2/PA3 分析；不提交全文，不复制超出必要摘录的材料。
- 自动访问 403 不等于用户浏览器不可访问；但在获得可核对全文路径前，PA-S04-C 不参与“全文覆盖完成”的结论。