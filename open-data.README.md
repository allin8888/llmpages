# open-data.json · 开放数据集说明（P1-3 #3/#17）

- 产物：`export_open_data.py` 从主报告解析生成，`publish_site.py` 随刊复制到本目录。
- 口径：与主报告完全一致（s-sort 列示价；混合价 = 0.75×输入 + 0.25×输出；美元价按 meta.fx_rate 折算四舍五入到分）。
- 更新：每日自动化刷新后随站点重新发布；未核实项以 note 文本标「待核实」，严禁另行编造。

## 字段

| 字段 | 类型 | 说明 |
|---|---|---|
| meta.date | string | 数据截至日（YYYY-MM-DD，与主报告「数据截至」一致） |
| meta.fx_rate | number | USD→CNY 汇率（CFETS 中间价口径） |
| meta.source / generator / unit | string | 来源文件 / 生成器 / 计价单位 |
| models[].name | string | 排序总览行名（与主报告一致） |
| models[].prod | string | 产品标识（OR slug 或官方型号名） |
| models[].region | string | 地区（中国/美国/欧洲/…） |
| models[].in / out / mix / cache | number|null | 输入/输出/混合/缓存命中价（¥/MTok；null=待核实） |
| models[].note | string | 备注原文（来源、口径、发布与补录信息） |
| promos[] | object | 价格特惠表（vendor_model / offer / discount / price / status / note） |
| events[] | object | 事件日历（type / event / date / countdown / status） |
| tracks | object | 图像/视频/语音/Embedding 赛道说明（细数据见报告章节与 models.json） |

## 使用约束

- 数据为公开只读；引用请注来源与日期。
- JSON 以 UTF-8 实字写出（无 \\uXXXX 转义）。
