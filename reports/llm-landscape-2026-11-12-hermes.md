# 主流大模型全景对比与 API 定价（Markdown 版）

> 数据截至：**2026-10-30**（联网核实 11:00 刷新）；汇率固定 1 USD = 6.7734 CNY（四舍五入到分）。

## 本期变更摘要（刷新要点）

本期为「OR 双榜刷新 + 事件倒计时重算 + 差异表真实快照对比」刷新——① OpenRouter 周榜：Top3 DeepSeek V4.1 Flash 1017 39.57T / DeepSeek V4.1 Flash 16.58T / GLM 5.3 Flash 15.00T；② OpenRouter 日榜：Top3 DeepSeek V4.1 Flash 1017 7.30T / DeepSeek V4.1 Flash 2.44T / GLM 5.3 Flash 2.43T；③ OpenRouter 挂牌价漂移（A-3b 自动发现）：跨日期检测到 10 处 OR 挂牌价变动（详见差异表「OR 改价」行）；④ 事件日历：倒计时重算（更新 2 行，基准 2026-10-30）；⑤ 汇率：6.7351（当日 CFETS 中间价判定与偏差见变更摘要）；⑥ 价格核实：第一梯队 14 家 WebSearch 全量核实由 LLM 步骤 2 执行，核实结论见差异表「官方定价」行（若为【待 LLM 回填】骨架必须覆写）与家族总览核实卡；⑦ 规则 A：OpenRouter 全量扫描 457 模型完成（vendor/模型数见差异表「市场覆盖」行；A-2 发现见「待补录」行）。

---

## 表 1：两期对比差异表

| 变动类型 | 模型家族 / 厂商 | 上期 · 10-29 00:28 | 本期 · 10-30 00:03 | 变动说明 |
| --- | --- | --- | --- | --- |
| 排行榜 | OpenRouter 周榜Top10 调用量（总 tokens） | 周榜 Top10（2026-10-29）：DeepSeek V4.1 Flash 1017 37.26T / DeepSeek V4.1 Flash 17.00T / GLM 5.3 Flash 14.11T / GPT-6 Luna 9.08T / Hy4 preview 8.97T / MiniMax M3.1 Flash 8.71T / Claude Opus 5.5 8.07T / GLM 5.3 5.15T / Nemotron 3 Ultra 4.99T / MiMo-V2.6-Flash 4.71T / 快照日期 2026-10-29 | ↻周榜 Top10（2026-10-30）：DeepSeek V4.1 Flash 1017 39.57T / DeepSeek V4.1 Flash 16.58T / GLM 5.3 Flash 15.00T / GPT-6 Luna 9.59T / Hy4 preview 8.96T / Claude Opus 5.5 7.86T / Step 5 Preview 5.39T / GLM 5.3 5.15T / Nemotron 3 Ultra 4.44T / MiMo-V2.6-Flash 4.10T / 快照日期 2026-10-30 | MiniMax M3.1 Flash 跌出 Top10；Claude Opus 5.5 7→6 ↑；Step 5 Preview 新入第 7；数据来自 OpenRouter 前端 rankings API（view=week） |
| 排行榜 | OpenRouter 日榜Top10 调用量（总 tokens） | 日榜 Top10（2026-10-29）：DeepSeek V4.1 Flash 1017 6.04T / DeepSeek V4.1 Flash 2.36T / GLM 5.3 Flash 1.87T / Hy4 preview 1.35T / Claude Opus 5.5 1.10T / GPT-6 Luna 1.08T / MiniMax M3.1 Flash 0.84T / Step 5 Preview 0.80T / GLM 5.3 0.71T / DeepSeek V4 Flash 0731 0.66T / 快照日期 2026-10-29 | ↻日榜 Top10（2026-10-30）：DeepSeek V4.1 Flash 1017 7.30T / DeepSeek V4.1 Flash 2.44T / GLM 5.3 Flash 2.43T / Hy4 preview 1.45T / GPT-6 Luna 1.45T / Claude Opus 5.5 1.01T / Step 5 Preview 0.96T / MiniMax M3.1 Flash 0.90T / GLM 5.3 0.64T / jev-1.13-20260917 0.63T / 快照日期 2026-10-30 | Claude Opus 5.5 5→6 ↓；GPT-6 Luna 6→5 ↑；MiniMax M3.1 Flash 7→8 ↓；Step 5 Preview 8→7 ↑；DeepSeek V4 Flash 0731 跌出 Top10；jev-1.13-20260917 新入第 10；数据来自 OpenRouter 前端 rankings API（view=day） |
| 市场覆盖 | 规则 A 全量扫描OpenRouter vendor 枚举 | 2026-10-29 基线（家族总数以家族总览实际行数为准） | —本期扫描 60 vendor / 457 模型；A-2 扫描无未登记的新型号 | 社区微调类（nousresearch 等）不纳入；notable 新厂商/新型号的补录由 LLM 步骤 2 策展完成，主表变动见对应行 |
| 新发布 | openai GPT-6.1 Terra ProA-4 多源扫描 · T1 · 数据源 or | —（2026-10-27 发布） | ＋$1.0/$5.0 每 MTok | OR 已上架；主报告尚未收录 → 当日人工策展补录（家族总览 / 排序总览 / 柱状图）。明细见 data/new_releases_2026-10-30.json，本行不得残留到下期 |
| 新发布 | OpenAI GPT-6.1 TerraA-4 多源扫描 · T1 · 数据源 aa + or | —（2026-10-26 发布） | ＋$1/$5 每 MTok；AA Index 51 | OR 已上架；主报告尚未收录 → 当日人工策展补录（家族总览 / 排序总览 / 柱状图）。明细见 data/new_releases_2026-10-30.json，本行不得残留到下期 |
| 新发布 | Kimi Kimi K3.1 ProA-4 多源扫描 · T1 · 数据源 aa + or | —（2026-10-23 发布） | ＋$2/$10 每 MTok；AA Index 46 | OR 已上架；主报告尚未收录 → 当日人工策展补录（家族总览 / 排序总览 / 柱状图）。明细见 data/new_releases_2026-10-30.json，本行不得残留到下期 |
| 新发布 | MiniMax MiniMax-M3.1-FlashA-4 多源扫描 · T1 · 数据源 aa + or | —（2026-10-19 发布） | ＋$0.15/$0.6 每 MTok；AA Index 28.9 | OR 已上架；主报告尚未收录 → 当日人工策展补录（家族总览 / 排序总览 / 柱状图）。明细见 data/new_releases_2026-10-30.json，本行不得残留到下期 |
| 新发布 | DeepSeek DeepSeek V4.1 Flash 1017A-4 多源扫描 · T1 · 数据源 aa + or | —（2026-10-17 发布） | ＋$0.3/$1.2 每 MTok；AA Index 32.5 | OR 已上架；主报告尚未收录 → 当日人工策展补录（家族总览 / 排序总览 / 柱状图）。明细见 data/new_releases_2026-10-30.json，本行不得残留到下期 |
| 新发布 | meta Muse Spark OpenA-4 多源扫描 · T1 · 数据源 or | —（2026-10-16 发布） | ＋$1.25/$4.25 每 MTok | OR 已上架；主报告尚未收录 → 当日人工策展补录（家族总览 / 排序总览 / 柱状图）。明细见 data/new_releases_2026-10-30.json，本行不得残留到下期 |
| 官方定价 | 规则 B 官网一致性主表价格快照对比 | 主表价格（2026-10-29 基线） | —主表价格机械对比无变动（2026-10-29 → 2026-10-30） | 【待 LLM 回填】2026-10-30 第一梯队 14 家联网核实结论（逐家：一致/已更新/待核实 + 来源）——覆写本单元格后方可交付 |
| OR 改价 | OpenRouter 挂牌价漂移A-3b 自动发现 · 挂牌价 vs 上期基线 | 上期 OR 挂牌价（基线 2026-10-29） | ▲检测到 10 处 OR 挂牌价变动：glm-5.3-flash ↓出 85%、deepseek-v4.1-flash ↓入 68%、Tencent Hunyuan Hy3 ↑出 60%、Z.ai GLM-5.2 ↓入 56% 等 | 脚本自动对比本期 or_models.json 与上期基线（data/or_price_baseline.json），过滤 :free/:batch 变体与 None↔0 噪声后得出；自 2026-08-28 起每次自动运行均自动播报 |
| OR 改价 | glm-5.3-flashOpenRouter 挂牌价 | 输入 ¥1.01 / 输出 ¥3.37 | ▼¥1.01 → ¥0.31 / ▼¥3.37 → ¥0.50 | 输入 -69%；输出 -85% |
| OR 改价 | deepseek-v4.1-flashOpenRouter 挂牌价 | 输入 ¥0.94 / 输出 ¥2.83 | ▼¥0.94 → ¥0.30 / ▲¥2.83 → ¥3.37 | 输入 -68%；输出 +19% |
| OR 改价 | Tencent Hunyuan Hy3OpenRouter 挂牌价 | 输入 ¥0.56 / 输出 ¥2.22 | ▲¥0.56 → ¥0.89 / ▲¥2.22 → ¥3.56 | 输入 +59%；输出 +60% |
| OR 改价 | Z.ai GLM-5.2OpenRouter 挂牌价 | 输入 ¥0.09 / 输出 ¥47.15 | ▼¥0.09 → ¥0.04 / ▼¥47.15 → ¥47.15 | 输入 -56%；输出 +0% |
| OR 改价 | mistral-large-4-0OpenRouter 挂牌价 | 输入 ¥9.16 / 输出 ¥28.15 | ▼¥9.16 → ¥4.71 / ▼¥28.15 → ¥14.14 | 输入 -49%；输出 -50% |
| OR 改价 | kimi-k3OpenRouter 挂牌价 | 输入 ¥1.56 / 输出 ¥134.70 | ▲¥1.56 → ¥1.61 / ▼¥134.70 → ¥72.74 | 输入 +3%；输出 -46% |
| OR 改价 | granite-4.2-8bOpenRouter 挂牌价 | 输入 ¥0.40 / 输出 ¥1.68 | ▼¥0.40 → ¥0.40 / ▼¥1.68 → ¥1.01 | 输入 +0%；输出 -40% |
| OR 改价 | hy4-previewOpenRouter 挂牌价 | 输入 ¥5.06 / 输出 ¥15.16 | ▲¥5.06 → ¥5.62 / ▲¥15.16 → ¥16.84 | 输入 +11%；输出 +11% |

## 表 2：OpenRouter 调用量周榜（本周前十大 AI 模型，按总 tokens）新增

| 排名 | 模型 | 调用量（总 tokens） | 涨跌幅 | 输入价¥/MTok · 上行OR/下行官方 | 输出价¥/MTok · 上行OR/下行官方 | 缓存命中价¥/MTok · 上行OR/下行官方 | 上下文 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Deepseek Deepseek V4 Flash | 16.05 万亿调用 8.88 亿次 | 12.39% | ¥0.56官方 ¥0.56 | ¥1.12官方 ¥1.12 | ¥0.11官方 ¥0.11 | 1.0M |
| 2 | Tencent Hy3 | 9.83 万亿调用 1.24 亿次 | 3.62% | ¥0.89官方 ¥0.89 | ¥3.58官方 ¥3.58 | ¥0.22官方 ¥0.22 | 262K |
| 3 | Openai Gpt 5.6 Luna | 5.80 万亿调用 2.50 亿次 | 18.74% | ¥0.68官方 ¥0.68 | ¥4.06官方 ¥4.06 | ¥0.07官方 ¥0.07 | 1.1M |
| 4 | Xiaomi Mimo V2.5 | 5.46 万亿调用 7850.70 万次 | 8.58% | ¥0.95官方 ¥0.95 | ¥1.90官方 ¥1.90 | ¥0.02官方 ¥0.02 | 1.1M |
| 5 | Z Ai Glm 5.2 | 4.34 万亿调用 8059.58 万次 | 17.53% | —待核实 | —待核实 | —无缓存 | 256K |
| 6 | Deepseek Deepseek V4 Pro | 3.52 万亿调用 1.11 亿次 | 0.59% | ¥9.75官方 ¥9.75 | ¥19.51官方 ¥19.51 | ¥0.82官方 ¥0.82 | 1.0M |
| 7 | Google Gemini 3.6 Flash | 2.75 万亿调用 3009.72 万次 | 11.84% | ¥2.54官方 ¥2.54 | ¥12.70官方 ¥12.70 | ¥0.25官方 ¥0.25 | 1.0M |
| 8 | Nvidia Nemotron 3 Ultra 550B A55B | 2.73 万亿调用 3205.27 万次 | 20.06% | —待核实 | —待核实 | —无缓存 | 1.0M |
| 9 | Anthropic Claude Opus 5 | 2.68 万亿调用 3145.84 万次 | 88.56% | ¥16.93官方 ¥16.93 | ¥84.67官方 ¥84.67 | ¥1.69官方 ¥1.69 | 1.0M |
| 10 | Poolside Laguna S 2.1 | 1.72 万亿调用 1854.58 万次 | -5.24% | —待核实 | —待核实 | —无缓存 | 262K |

## 表 3：OpenRouter 调用量日榜（Today 前十大 AI 模型，按总 tokens）新增

| 排名 | 模型 | 调用量（总 tokens） | 涨跌幅 | 输入价¥/MTok · 上行OR/下行官方 | 输出价¥/MTok · 上行OR/下行官方 | 缓存命中价¥/MTok · 上行OR/下行官方 | 上下文 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Deepseek Deepseek V4 Flash | 2.48 万亿调用 1.30 亿次 | 2.93% | ¥0.56官方 ¥0.56 | ¥1.12官方 ¥1.12 | ¥0.11官方 ¥0.11 | 1.0M |
| 2 | Tencent Hy3 | 1.63 万亿调用 1999.31 万次 | 7.70% | ¥0.89官方 ¥0.89 | ¥3.58官方 ¥3.58 | ¥0.22官方 ¥0.22 | 262K |
| 3 | Xiaomi Mimo V2.5 | 1.17 万亿调用 1468.68 万次 | -37.05% | ¥0.95官方 ¥0.95 | ¥1.90官方 ¥1.90 | ¥0.02官方 ¥0.02 | 1.1M |
| 4 | Openai Gpt 5.6 Luna | 1.04 万亿调用 2905.40 万次 | -0.14% | ¥0.68官方 ¥0.68 | ¥4.06官方 ¥4.06 | ¥0.07官方 ¥0.07 | 1.1M |
| 5 | Z Ai Glm 5.2 | 556.68 十亿调用 1066.22 万次 | -12.99% | —待核实 | —待核实 | —无缓存 | 256K |
| 6 | Nvidia Nemotron 3 Ultra 550B A55B | 520.92 十亿调用 561.81 万次 | -0.45% | —待核实 | —待核实 | —无缓存 | 1.0M |
| 7 | Deepseek Deepseek V4 Pro | 466.75 十亿调用 1438.50 万次 | -0.86% | ¥9.75官方 ¥9.75 | ¥19.51官方 ¥19.51 | ¥0.82官方 ¥0.82 | 1.0M |
| 8 | Minimax Minimax M3 | 335.03 十亿调用 569.73 万次 | 32.55% | ¥2.03官方 ¥2.03 | ¥8.13官方 ¥8.13 | ¥0.41官方 ¥0.41 | 524K |
| 9 | Poolside Laguna S 2.1 | 255.72 十亿调用 278.09 万次 | 12.71% | —待核实 | —待核实 | —无缓存 | 262K |
| 10 | Google Gemini 3.7 Flash | 231.33 十亿调用 840.85 万次 | 19.19% | ¥1.27官方 ¥1.27 | ¥6.35官方 ¥6.35 | ¥0.13官方 ¥0.13 | 1.0M |

## 表 4：一、🌍 主流大模型家族总览（产品级 · 各型号独立上下文 / 参数 / 协议）

| 模型家族 / 厂商 | 地区 | 形态 | 最早版本（首发日期） | 最新产品型号（日期） | 上下文长度 | 参数量（架构） | 多模态 / 协议 | API 价 ¥/MTok（输入 / 输出） | 特惠 / 折扣 | 免费额度 | 核心特点 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GPT / OpenAI（美） | 美国 | 闭源商业 | GPT-1 / 2018-06-11 | GPT-5.6（Sol / Terra / Luna，2026-07-09 GA） / 预览 06-26；前旗舰 GPT-5.5 2026-04-23；GPT-6 未发布 | 1.05M / 输出 128K | 未公开 / MoE 闭源 | 文本+图像 / 闭源商业 | Sol ¥33.87 / ¥203.20 / Terra ¥13.55/¥81.28；Luna ¥1.35/¥8.13（缓存读 Sol ¥3.39 / Terra ¥1.35 / Luna ¥0.14；07-30 OpenAI 降价 20%/80%，缓存价同步下调） | —（标准价；Batch 批量 5 折、缓存命中降 90%） | ChatGPT Free 有限免费消息（约 10 条/5h 降级） | API-first；内置思考（Max/Ultra 多智能体）；三档 Sol/Terra/Luna 同上下文；综合能力第一梯队 |
| Claude / Anthropic（美） | 美国 | 闭源商业 | Claude 1.0 / 2023-03-15 | Claude Opus 5（2026-07-24） / 半价旗舰（性能逼近 Fable 5） | 1M / 输出 128K | 未公开 / 闭源 | 文本+图像 / 闭源商业 | ¥33.87 / ¥169.35 / $5/$25（与 Opus 4.8 同价；缓存读¥3.39） | 无公开特惠 | 无（Opus 无免费层） | “半价旗舰”：性能逼近 Fable 5 顶级推理层，价格仅其一半；长上下文 Agent 与企业首选 |
| Claude / Anthropic（美） | 美国 | 闭源商业 | Claude 1.0 / 2023-03-15 | Claude Opus 4.8（2026-05-28） / 通用旗舰 | 1M / 输出 128K | 未公开 / 闭源 | 文本+图像 / 闭源商业 | ¥33.87 / ¥169.35 / 缓存¥6.77（$5/$25） | 无公开特惠 | 无（Opus 无免费层） | 通用旗舰；编码 / 智能体 / computer use 标杆；企业采用最广 |
| Claude / Anthropic（美） | 美国 | 闭源商业 | Claude 1.0 / 2023-03-15 | Claude Sonnet 5（2026-06-30） / 均衡主力 | 1M / 输出 128K | 未公开 / 闭源 | 文本+图像 / 闭源商业 | ¥13.55 / ¥67.73 / 促销 $2/$10（至 2026-08-31，之后 ¥20.32/¥101.60） | 促销价 $2/$10（至 2026-08-31） | Claude Sonnet 5 每日限量免费消息（基础访问） | 性价比主力档；长上下文智能体常用默认型号 |
| Claude / Anthropic（美） | 美国 | 闭源商业 | Claude 1.0 / 2023-03-15 | Claude Fable 5 / Mythos 5（2026-06-30） / 顶配层（最强推理 / 超大上下文） | 1M / 输出 128K | 未公开 / 闭源 | 文本+图像 / 闭源商业 | ¥67.73 / ¥338.67 / 缓存¥6.77（$10/$50，顶配层；缓存读 $1.00） | 无 | — | 顶配推理层；面向最复杂任务与长程 Agent |
| Claude / Anthropic（美） | 美国 | 闭源商业 | Claude 1.0 / 2023-03-15 | Claude Haiku 4.5 / 轻量快档 | 200K / 输出 64K | 未公开 / 闭源 | 文本+图像 / 闭源商业 | ¥6.77 / ¥33.87 / $1/$5 | 无 | — | 低延迟 / 低成本档；高吞吐简单任务 |
| Gemini / Google（美） | 美国 | 闭源 + 开放分发 | Gemini 1.0 / 2023-12-06 | Gemini 3.6 Flash（2026-07-21） / 同族：3.5 Flash-Lite / Flash Cyber；旗舰 3.5 Pro 已于 2026-07-17 发布（见下行）；Gemini 4 预训练中；3.7 Flash 已于 2026-08-13 发布（$0.75/$3.75 限时五折至 2026 年底） | 1M / 输出 64K | 未公开 / 闭源 | 原生全模态 / 文/图/音/视频 · 闭源 | ¥5.08 / ¥25.40 / $0.75/$3.75 限时五折（至 2026-12-31，2027-01-01 恢复 $1.50/$7.50；3.7 Flash 08-13 同价；3.5 Pro 为 $2/$12） | —（限时五折至 2026-12-31，之后恢复标准价） | Gemini API 免费层（Flash/Flash-Lite 免费；15 RPM/250K TPM） | 原生多模态；1M 上下文；Deep Think；主打效率/成本/延迟；AI Studio 免费开放 |
| Gemini / Google（美） | 美国 | 闭源 + 开放分发 | Gemini 1.0 / 2023-12-06 | Gemini 3.5 Pro（2026-07-17） / 旗舰推理（Deep Think） | 1M / 输出 64K（发布报道称 2M 上下文，待官方确认） | 未公开 / 闭源 | 原生全模态 / 文/图/音/视频 · 闭源 | ¥13.55 / ¥81.28 / $2/$12（≤200k 提示） | —（标准价） | Gemini API 免费层不含 Pro | 旗舰长上下文推理；GA 状态存争议（部分来源称 07-17 发布，亦有称截至 07-31 仍处合作伙伴测试，当前可调用 Pro 实为 3.1 Pro，统一 $2/$12 ≤200K、>200K $4/$18）；2M 上下文待官方确认 |
| Llama / Meta（美） | 美国 | 开放权重 | LLaMA / 2023-02-24 | Llama 5（2026-04-08） | 5M / 研究预览 10M | 600B+ / MoE 开放权重 | 文本+图/音/视频 / Meta 社区许可 | 无官方 API；第三方托管 ¥23.71 / ¥47.41 / Together $3.50/$7；权重免费自托管 | 自托管免费（仅 GPU 算力成本） | Groq / Cerebras 新用户免费调用（Llama/GPT-oss） | 开放权重生态地基；MoE；原生多模态；社区许可（月活>7亿需授权）；System-2 深思 |
| Meta Muse / Meta（美） | 美国 | 闭源商业（智能体编码） | Muse Spark 1.0 / 2026 | Muse Spark 1.2（2026-08-05） | 1M | 未公开 / 闭源 | 文本/图/音/视频/PDF / 工具调用·结构化输出 | ¥8.47 / ¥28.79 / $1.25/$4.25（缓存 $0.15≈¥1.02） | contributor 档 ¥0.10/¥0.20 / 参与训练优化 | contributor 档限流 / 5h 滚动窗口 | Meta 首个智能体编码模型；1M 上下文；与 Muse Code 编码智能体配套；多智能体长程任务（08-05 全球公测，待核实 GA） |
| Grok / xAI（美） | 美国 | 闭源商业 | Grok-1 / 2023-11-05 | Grok 4.6（2026-08-12 深夜发布） | 500K | 1.5T / V9 MoE 底座 | 多模态（文/图/音） / 闭源商业 | ¥13.55 / ¥40.64 / $2/$6；>200K $4/$12（缓存¥3.39） | — | xAI 免费层 / X Premium 含 | 实时 X 数据；“求真”人设；“Opus 级”定位、低价；最大输出口径存疑（部分来源 30K）；Grok 5（6T–10T）在训 |
| Inception Labs / Mercury（美） | 美国 | 闭源商业 | Mercury 1 / 2025 | Mercury 2（2026，扩散 LLM） | 128K | 未公开 / dLLM 扩散式 | 文本（扩散生成） / 闭源商业 | ¥1.69 / ¥5.08 / $0.25/$0.75（首方官方价；缓存读 ¥0.17） | — | 待核实 | 扩散式 LLM（dLLM），并行生成 token、低延迟代码/结构化生成；128K 上下文；本期市场覆盖扫描新增（规则 A） |
| Mistral / Mistral AI（欧） | 欧洲 | 开源 Apache 2.0 | Mistral 7B / 2023-09-27 | Mistral Large 3（2026-04-25） | 256K | 675B 总 / 41B 激活 / MoE（Large 3） | 多模态（40+ 语言） / Apache 2.0 | ¥3.39 / ¥10.16 / $0.50/$1.50 | — | Mistral Free Tier 每月 ~100 credits（限速 ~6 RPM） | 欧洲主权 AI；首个欧洲前沿开放权重；多模态多语言（40+）；256K 上下文 |
| Command / Cohere（加） | 北美 | 开源 Apache 2.0 | Command / 2023 | Command A+（2026-05-20） | 128K 输入 / 64K 输出 | 218B 总 / 25B 激活 / MoE（A+，128 专家 / 8 激活） | 文本+图像+工具 / Apache 2.0 | ¥16.93 / ¥67.73 / $2.50/$10（A+） | — | Cohere 免费试用（有限） | 企业级 / Sovereign AI；RAG 检索与重排强；可私有部署；支持 48 语言 |
| Nova / Amazon（美） | 美国 | 闭源（AWS） | Nova / 2024-12-02 | Nova 2 Pro / 推理旗舰（正式档，本期新增） | 1M / 输出 32.8K | 未公开 | 多模态（文/图/音/视频/文档） / 闭源（AWS） | ¥8.47 / ¥67.73 / $1.25/$10.00 | — | AWS 免费层（有限） | Nova 2 推理旗舰档；1M 上下文；多模态企业云原生 |
| Nova / Amazon（美） | 美国 | 闭源（AWS） | Nova / 2024-12-02 | Nova 2 Lite / 轻量档（2025-12-02） | 1M / 输出 65,536（Lite） | 未公开 | 多模态（文/图/音/视频/文档） / 闭源（AWS） | ¥2.03 / ¥16.93 / $0.30/$2.50 | — | AWS 免费层（有限） | 轻量多模态档；企业云原生；Sonic 支持语音多轮 |
| DeepSeek / 深度求索（中） | 中国 | 开源 MIT | DeepSeek-LLM / 2023-11 | DeepSeek V4 Pro 正式版（2026-08-13 GA） | 1M | 1.6T 总 / 49B 激活 / MoE | 文本为主（+ MCP 工具） / MIT | 峰 ¥9.00 / ¥27.00 / 谷 ¥4.50 / ¥13.50 / 缓存 峰¥0.30 / 谷¥0.15 | 峰谷双档已生效（2026-08-17）：高峰（9–12、14–18 点）×2、空闲基准；峰值时段升价 | 腾讯 TokenHub 新人 100 万（覆盖 V4）；硅基流动 2000 万 | 旗舰款；极致性价比；混合推理；全栈适配国产算力（昇腾 950）；峰谷双档定价（高峰×2、空闲基准） |
| DeepSeek / 深度求索（中） | 中国 | 开源 MIT | DeepSeek-LLM / 2023-11 | DeepSeek V4 Flash（2026-07-15） | 1M | 284B 总 / 13B 激活 / MoE（含视觉原语） | 文本为主（+ MCP 工具） / MIT | 峰 ¥3.00 / ¥9.00 / 谷 ¥1.50 / ¥4.50 / 缓存 峰¥0.10 / 谷¥0.05 | 峰谷双档已生效（2026-08-17）：同 V4 Pro 高峰×2、空闲基准 | 腾讯 TokenHub 新人 100 万（覆盖 V4）；硅基流动 2000 万 | 轻量快档；低成本高吞吐；Flash 含视觉原语多模态技术；峰谷双档定价（高峰×2、空闲基准） |
| Qwen 通义千问 / 阿里巴巴（中） | 中国 | 开源 Apache 2.0 | Qwen / 2023-08 | Qwen3.8-Max 正式版（2026-08-03 发布） / 预览 07-19 → 08-03 GA；下周开源 Qwen3.8-27B；接入「千问办公」 | 1M / 原生视觉 + 长上下文 | 2.4T 总 / 95B 激活 / MoE（Qwen3.8-Max） | 多模态（文/图/音/视频） / Apache 2.0（承诺） | ¥12.00 / ¥36.00（官方人民币价） / 隐式缓存命中 ¥1.5；国际 $2/$6（约为 Opus 5 的 40%/24%）；与在售 qwen3.7-max 标准价持平 | —（正式价；预览限时 1-2 折已结束） | 阿里百炼 新用户 100 万+每模型 100 万；qwen-turbo 永久每月 100 万 | 开源生态全球第一；混合思考（思考预算可调）；原生 Agent 工具调用；单日调用量破 1.4 万亿 token；2.4T 参数最大开源旗舰之一 |
| GLM 智谱 / 智谱华章（中） | 中国 | 开源 MIT | GLM-130B / 2022-08 | GLM-5.2（2026-06） | 1M（无损） / 最大输出 131K | 744B 总 / 40B 激活 / MoE（GLM-5.2） | 文本为主（5V 视觉） / MIT | ¥8.00 / ¥28.00 / 官方人民币价；缓存读¥2.00 / （国际档 $1.40/$4.40） | —（智谱年内三度提价） | 智谱 GLM-4-Flash/4.7-Flash 永久免费无限量；新用户 2000 万 Token | 长程 Agent / 复杂系统工程；兼容 Claude Code 与 OpenClaw；MIT 可商用；港股“大模型第一股” |
| Kimi / 月之暗面（中） | 中国 | 开源 + API | Kimi 助手 / 2023 | Kimi K3（2026-07，开源权重） | 1M | 2.8T 总 / 450B 激活 / MoE（16/896 专家激活） | 原生视觉 + 文本 / 开源 + API | ¥20.00 / ¥100.00 / 官方人民币价；缓存¥2.00 | — | Kimi 新用户约 800 万 Token；常返券（充 100 返 300） | 长程编程 / 知识工作 / 复杂推理；长文本；多智能体集群；国产最贵、定价权提升 |
| Inkling / Thinking Machines（美） | 美国 | 开源 Apache 2.0 | Inkling（2026-07-15） | Inkling（2026-07-15 发布） | 1M | 975B 总 / 41B 激活 / MoE（Apache 2.0） | 文本为主（+ 工具） / Apache 2.0 | ¥6.77 / ¥27.43 / 无第一方 API；OpenRouter 托管挂牌 $1.00/$4.05（缓存读 $0.17）；$1.87/$4.68 系 Tinker 微调采样计费、非 API 价（口径修正） | —（标准价） | 官方免费层（以发布页为准） | 由 Mira Murati 创立的 Thinking Machines 首发开源旗舰；975B/41B 激活 MoE、Apache 2.0，是当前参数规模最大且许可最宽松的开源模型之一 |
| 豆包 / Seed / 字节跳动（中） | 中国 | 闭源 + API | 豆包 / 2023-08 | 豆包 2.1 Pro（2026-06-23） | 256K / 部分来源 262K | 未公开 | 原生全模态（文/图/音/视频） / 闭源 + API | ¥6.00 / ¥30.00 / 缓存¥1.20 | Turbo 版半价 | 火山引擎 每日 200 万 Token（凌晨刷新）；免费版 50 万（Lite） | 多模态最强；C 端月活 3 亿+；MaaS 份额 49.5%；性价比高 |
| 豆包 / Seed / 字节跳动（中） | 中国 | 闭源 + API | 豆包 / 2023-08 | 豆包 4.0（2026-06-10） | 256K | 未公开 | 原生全模态（文/图/音/视频） / 闭源 + API | ¥2.00 / ¥6.00（标准版 1M 上下文） / 专业版（200 万）¥8.00/¥24.00 | 个人用户基础功能免费 | 同火山引擎 每日 200 万 Token | 新一代多模态与 Agent 能力；与 2.1 Pro 并行提供 |
| 文心 ERNIE / 百度（中） | 中国 | 闭源 + 部分开源 | ERNIE 1.0 / 2019-03 | 文心 5.1（2026-05-09） | 128K / 输出 65,536 | 约 0.8T / 较 5.0 的 2.4T 压缩约 1/3（全模态） | 原生全模态 / 闭源 + 部分开源（4.5 系列） | ¥4.00 / ¥18.00（≤32k） / 32k–128k ¥6.00/¥22.00 | — | 百度千帆 ERNIE-Speed/Lite 永久免费；每模型 100 万 | 知识增强；原生全模态；中文 / 合规强；参数较 5.0 大幅压缩、效率提升 |
| 混元 Hunyuan / 腾讯（中） | 中国 | 开源 Apache 2.0 | 混元 / 2023-09-07 | 混元 Hy3 正式版（2026-07）+ 智能体 Hyra-1.0 | 256K | 295B 总 / 21B 激活 / MoE（Hy3，192 专家 / Top-8） | 多模态（图像 3.0 开源） / Apache 2.0 | ¥1.00 / ¥4.00 / 缓存¥0.25 | — | 腾讯混元 lite 永久免费无限量；腾讯云 TokenHub 新人 100 万 | 全栈自研；MoE；256K；性价比；深度微信/腾讯生态；兼容 OpenClaw |
| MiniMax / 稀宇科技（中） | 中国 | 开源（非商业） | MiniMax / 2023 | MiniMax M3（2026-06-01 发布） / 旗舰新架构（开源权重承诺）；前代 M2.7 2026-03-18 | 1M / 前代 M2.7 为 205K | 未公开 / MoE（M3） | 多模态（语音/视频） / 非商业授权（商用需申请） | ¥2.10 / ¥8.40 / 官方人民币价（标准 ¥4.20/¥16.80，≤512k 永久五折）；缓存 ¥0.42；>512k 翻倍 | ≤512k 上下文永久五折（¥4.20/¥16.80 → ¥2.10/¥8.40）；缓存命中再降 80%（¥0.42） | MiniMax 15 元代金券（实名后）；腾讯 TokenHub 覆盖 | “自我进化”机制（Agent Harness 驱动自身训练迭代）；多智能体协作；多模态（语音/视频）；多芯适配 |
| 星火 / 科大讯飞（中） | 中国 | 闭源 + API | 星火 1.0 / 2023-05-06 | 星火 X2-VL 多模态（2026-06） | 待核实 / 前代 X2-Flash 为 256K | 未公开 | 多模态（原生视觉+文本） / 闭源 + API | ¥2.00–¥3.00 / ¥2.00–¥3.00 / X2 系列统一单价（X2-Flash ¥2/¥2，X2 旗舰 ¥3/¥3） | — | 讯飞星火 每模型 20 万永久；V4 50 万（30 天）；注册领 500 万 | 中文 / 语音见长；教育、办公、法律场景；国产化适配；高考 708 分 |
| LongCat / 美团（中） | 中国 | 开源 MIT | LongCat-Flash-Chat / 2025-09-01（龙猫，开源） | LongCat-2.0（2026-06-30 官宣 / 07-06 开源） | 1M / 原生超长上下文 | 1.6T 总 / 48B 激活 / MoE（动态 33B–56B） | 文本（Agentic Coding） / MIT（家族含 Image/Video/Omni） | ¥5.08 / ¥19.98（官方 $0.75/$2.95） / 限时折扣 $0.30/$1.20≈¥2.03/¥8.13（缓存 $0.006≈¥0.04） | 初上线限时折扣 输入¥2/输出¥8（原价¥5/¥20） | 初上线赠送额度；权重 MIT 免费自托管 | 业界首个五万卡国产算力集群全流程训练+推理的万亿模型；专精代码理解/生成/执行；N-gram Embedding + 稀疏注意力；昇腾 910 适配 |
| Agnes / Agnes AI（新加坡） / 母公司 Sapiens AI | 新加坡 | 闭源 + 免费/付费 API | Agnes 平台首发 / 2025-07（Product Hunt） | Agnes-2.5-Pro-Alpha（2026-08-03 发布） | 1M | 未公开 | 文本+图像 URL 输入 / 闭源 + API（OpenAI 兼容） | ¥3.05 / ¥6.10 / $0.45/$0.90；缓存 $0.0038≈¥0.03 | —（收费档） | —（免费层以官方为准） | 新收费推理档（Alpha）；1M 上下文；由「纯免费」转「免费+付费」双轨；2.0-Flash 是否亦有 $0.03/$0.15 收费档待核实 |
| Agnes / Agnes AI（新加坡） / 母公司 Sapiens AI | 新加坡 | 闭源 + 免费/付费 API | Agnes 平台首发 / 2025-07（Product Hunt） | Agnes-2.5-Flash（2026-07-13） | 512K | 未公开 | 文本+图像 URL 输入 / 闭源 + 免费 API（OpenAI 兼容） | 免费（无限期免费 API） / OpenAI 兼容 | 永久免费 | 即免费 API 本身 | 编程/智能体文本模型；SWE-bench Verified 75.6；Thinking 模式；免费开放一周调用超 1 万亿 Token；2.5-Pro 已发布（见上行） |
| Agnes / Agnes AI（新加坡） / 母公司 Sapiens AI | 新加坡 | 闭源 + 免费/付费 API | Agnes 平台首发 / 2025-07（Product Hunt） | Agnes-2.0-Flash（2026-06-01 API 免费） | 256K / 输出 64K（1M 曾灰度后回滚） | 未公开 | 文本+图像 URL 输入 / 闭源 + 免费 API（OpenAI 兼容） | 免费（API 免费） | 免费 | 免费 API | 上一代主力；Clustered 模型路由架构（底层 Gemini Flash）；Claw-Eval 全球前十；面向 Agent 工作流 |
| Xiaomi MiMo / 小米（中国） | 中国 | 开放权重 | 待核实 | mimo-v2.5（待核实） | 1.1M / 输入 | 待核实 | 文本 / 开放权重 | ¥0.95 / ¥1.90 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 小米开源 MoE 推理模型；性价比突出；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| NVIDIA Nemotron / 英伟达（美国） | 美国 | 开放权重 | 待核实 | nemotron-3-ultra-550b-a55b（待核实） | 512K / 输入 | 待核实 | 文本 / 开放权重 | ¥4.06 / ¥24.38 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 英伟达企业级开放权重模型；长上下文 Agent；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| StepFun 阶跃星辰 / 阶跃星辰（中国） | 中国 | 闭源商业 | 待核实 | step-3.7-flash（待核实） | 262K / 输入 | 待核实 | 文本 / 闭源商业 | ¥1.35 / ¥7.79 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 国产多模态大模型厂商；Step 系列；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Poolside / Poolside（美国） | 美国 | 闭源商业 | 待核实 | laguna-s-2.1（待核实） | 1.0M / 输入 | 待核实 | 文本 / 闭源商业 | ¥0.61 / ¥1.22 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 面向软件工程/代码 Agent 的专用模型；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| InclusionAI Ling / 蚂蚁百灵 Ling（中国） | 中国 | 闭源商业 | 待核实 | ling-3.0-flash（2026-07-23 上线） / 付费旗舰仍为 ling-2.6-1t | 262K / 输入 | 待核实 | 文本 / 闭源商业 | 免费 / 免费 / 3.0-Flash 当前 OpenRouter 免费；付费档 ling-2.6-1t ¥0.51 / ¥4.23 | —（3.0-Flash 全免费） | ling-3.0-flash:free（OpenRouter 限速，无额度上限） | 蚂蚁集团百灵（Ling）开源系列（inclusionAI）；长上下文；本期版本升级：新增 3.0-Flash 免费档（周榜第 12，+57.14%）；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Microsoft Phi / 微软（美国） | 美国 | 开放权重 | 待核实 | phi-4（待核实） | 16K / 输入 | 待核实 | 文本 / 开放权重 | ¥0.47 / ¥0.95 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 微软小参数高性能 Phi 系列；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Perplexity Sonar / Perplexity（美国） | 美国 | 闭源商业 | 待核实 | sonar-pro（待核实） | 200K / 输入 | 待核实 | 文本 / 闭源商业 | ¥20.32 / ¥101.60 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 搜索增强（RAG）对话模型；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| IBM Granite / IBM（美国） | 美国 | 开放权重 | 待核实 | granite-4.1-8b（待核实） | 131K / 输入 | 待核实 | 文本 / 开放权重 | ¥0.34 / ¥0.68 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | IBM 企业级开放权重模型；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| ByteDance Seed / 字节 Seed（中国） | 中国 | 开放权重 | 待核实 | seed-2.0-lite（待核实） | 262K / 输入 | 待核实 | 文本 / 开放权重 | ¥1.69 / ¥13.55 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 字节 Seed 团队基础模型（区别于豆包 Doubao）；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Upstage Solar / Upstage（韩国） | 韩国 | 闭源商业 | 待核实 | solar-pro-3（待核实） | 128K / 输入 | 待核实 | 文本 / 闭源商业 | ¥1.02 / ¥4.06 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 韩国领先 LLM；Solar 系列；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| AI21 Jamba / AI21 Labs（以色列） | 以色列 | 闭源商业 | 待核实 | jamba-large-1.7（待核实） | 256K / 输入 | 待核实 | 文本 / 闭源商业 | ¥13.55 / ¥54.19 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | Mamba+Transformer 混合架构 Jamba 系列；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Reka AI / Reka（美国） | 美国 | 闭源商业 | 待核实 | reka-edge（待核实） | 16K / 输入 | 待核实 | 文本 / 闭源商业 | ¥0.68 / ¥0.68 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 多模态基础模型厂商；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| DeepCogito / DeepCogito（美国） | 美国 | 开放权重 | 待核实 | cogito-v2.1-671b（待核实） | 128K / 输入 | 待核实 | 文本 / 开放权重 | ¥8.47 / ¥8.47 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 迭代式推理（iterative reasoning）开放模型；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Sakana AI / Sakana（日本） | 日本 | 闭源商业 | 待核实 | fugu-ultra（待核实） | 1.0M / 输入 | 待核实 | 文本 / 闭源商业 | ¥33.87 / ¥203.20 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 日本 AI 实验室；模型合并（model merging）；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Writer Palmyra / Writer（美国） | 美国 | 闭源商业 | 待核实 | palmyra-x5（待核实） | 1.0M / 输入 | 待核实 | 文本 / 闭源商业 | ¥4.06 / ¥40.64 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 企业级生成式 AI（Palmyra 系列）；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Arcee AI / Arcee（美国） | 美国 | 闭源商业 | 待核实 | trinity-large-thinking（待核实） | 262K / 输入 | 待核实 | 文本 / 闭源商业 | ¥1.49 / ¥5.76 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 领域自适应小模型（SLM）定制；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Kwaipilot KAT / 快手 Kwaipilot（中国） | 中国 | 闭源商业 | 待核实 | kat-coder-pro-v2.5（2026-07-11） / 同期 kat-coder-air-v2.5（07-10） | 256K / 输入 | 待核实 | 文本 / 闭源商业 | ¥5.01 / ¥20.05 / OpenRouter 挂牌价（第三方，待官网核实） | —（标准价；待核实） | —（待核实） | 快手代码智能体专用模型（KAT-Coder）；Pro / Air 双档（Air ¥1.02/¥4.06）；本期市场覆盖扫描新增；数据源自 OpenRouter 挂牌价，官网信息待自动化核校 |
| Nex AGI Nex-N2 / Nex AGI（美国） | 美国 | 开放权重 Apache 2.0 | Nex-N1 / 待核实 | Nex-N2（2026-06-02） / 同期 Nex-N2-mini 轻量档 | 256K / 输入 | 397B 总 / 激活参待核实 / MoE | 文本 / Apache 2.0 | ¥1.69 / ¥6.77 / OpenRouter 挂牌价（第三方，待官网核实）；缓存读 ¥0.17 / mini 档 ¥0.17 / ¥0.68 | —（标准价；待核实） | —（待核实） | 开放权重实验室，397B MoE / Apache 2.0；OpenRouter 综合榜第 29 位；Pro / mini 双档；本期规则 A 市场覆盖扫描新增；官网第一方定价待核实 |

## 表 5：一、🌍 主流大模型家族总览（产品级 · 各型号独立上下文 / 参数 / 协议）

| 家族 / 厂商 | 最近动态（2026-08 已核实） | 未纳入原因 |
| --- | --- | --- |
| 零一万物 Yi（中国） | 2026-08 公告全面转企业级（All-in-B）；开放平台即日起停止新注册/充值，2026-09-03 24:00 停止模型体验与 API，退款窗口至 2026-12-03 | 转企业级/停服 不再面向公众通用 API |
| 百川 Baichuan（中国） | 平台在营（Baichuan4-Turbo/Air）；2026 主线转向医疗垂直（M3 Plus 01-22、M4/百小医 05-22），通用前沿无新旗舰 | 转垂直/无前沿旗舰 通用 API 非主线 |
| 商汤 SenseNova（中国） | SenseNova 6.7 Flash-Lite / U1 Fast 公测（2026-06 起，OpenAI+Anthropic 双协议兼容），全部免费（每 5h 1500 次）、无正式定价 | 公测免费/无定价 未达「有价可核」门槛 |
| TII Falcon（阿联酋） | Falcon3（2026-03，1B–10B，Apache-2.0），小型模型主打消费级/主权部署；2026 无前沿旗舰 | 小型非前沿 未达前沿/主流 API 门槛 |
| LG EXAONE（韩国） | EXAONE 4.5（2026-04-09，33B VLM，256K 上下文，开源权重；06-01 入 llama.cpp mainline） | 非商业许可/无 API 定价 NC 许可 + 无公开 API 定价 |

## 表 6：二、主要特点与区别对比（跨维度）

| 维度 | 闭源前沿（美） | 开放权重 / 开源 | 国产主力 |
| --- | --- | --- | --- |
| 代表 | GPT-5.6 / Claude Fable 5·Opus 4.8 / Gemini 3.6 Flash / Grok 4.5 | Llama 5、Mistral Large 3、Command A+、DeepSeek V4、Qwen3.8-Max、GLM-5.2、Thinking Machines Inkling | 豆包 2.1 Pro、文心 5.1、混元 Hy3、Kimi K3、MiniMax M3、星火 X2-VL、LongCat-2.0 |
| 授权 | 闭源、API 收费、不可自托管 | Apache 2.0 / MIT，可下载权重自部署 | 多数闭源 API + 部分开源（混元/DeepSeek/智谱/Qwen 开源） |
| 多模态 | 原生全模态（文本/图/音/视频） | Mistral/Command/Llama 多模态；DeepSeek/Qwen 偏文本+MCP 工具 | 文心/豆包/混元原生全模态；Kimi 视觉；星火语音强 |
| 上下文 | GPT/Claude/Gemini 1M；Grok Fast 2M | Llama 4 Scout 10M；其余 128K–1M | 普遍 128K–256K（混元/DeepSeek/Kimi 256K–1M） |
| 自主 Agent | 强（Codex/Claude Code/计算机使用） | 中–强（GLM/Kimi/DeepSeek 原生工具调用） | 强（Kimi Agent Swarm、MiniMax 自我进化、豆包/混元办公智能体） |
| 价格策略 | 高端（按 token，含缓存折扣） | 低–中（DeepSeek/Qwen 极致性价比） | 低价（人民币计价，普遍 ¥1–8 / 百万 token） |
| 中文 / 合规 | 英文优先，中文良好 | 多语言；中文良好 | 中文最优、本土合规、数据驻留可控 |
| 典型用户 | 全球开发者 / 企业 / 专业团队 | 自托管企业、研究者、成本敏感部署 | 国内 C 端用户、政企、合规刚需行业 |

## 表 7：三、关键区别一句话总结

| 家族 | 差异化定位（一句话） |
| --- | --- |
| GPT（OpenAI） | 综合能力最均衡、生态最成熟的闭源标杆，API 与 ChatGPT 双线驱动 |
| Claude（Anthropic） | 编码 / 长程智能体 / 计算机使用的“事实标准”，安全分级最严 |
| Gemini（Google） | 原生多模态 + 1M 上下文 + 免费开放分发，绑定谷歌云与安卓生态 |
| Llama（Meta） | 开放权重生态地基；但 2026 前沿已转闭源 Muse Spark |
| Grok（xAI） | 实时联网（X）+ 多智能体 + “求真”人设，迭代极快 |
| Mistral / Cohere | 欧洲 / 北美主权 AI 代表，强调可私有部署与 RAG 企业工作流 |
| DeepSeek / Qwen / GLM | 开源性价比与生态三强；DeepSeek 拼成本、Qwen 拼生态、GLM 拼长程 Agent |
| Kimi / MiniMax | Agent 范式先锋：Kimi 多智能体集群、MiniMax 模型自我进化 |
| 豆包 / 文心 / 混元 / 星火 | 大厂 C 端 + 全模态路线；豆包拼多模态与规模、文心拼知识增强、混元拼性价比与生态、星火拼语音 |

## 表 8：📜 四、最早版本发布时间线（按首发日期）

| 年份 | 月份 | 家族（首个版本） |
| --- | --- | --- |
| 2018 | 06 月 | 美国 GPT（GPT-1） |
| 2019 | 03 月 | 中国 文心 ERNIE（ERNIE 1.0） |
| 2022 | 08 月 | 中国 智谱 GLM（GLM-130B） |
| 2023 | 02 月 | 美国 Llama（LLaMA） |
| 2023 | 03 月 | 美国 Claude（Claude 1.0，03-15） |
| 2023 | 05 月 | 中国 讯飞星火（星火 1.0，05-06） |
| 2023 | 08 月 | 中国 Qwen 通义千问 / 豆包 Seed（均为 2023-08） |
| 2023 | 09 月 | 中国 腾讯混元（09-07）｜欧洲 Mistral（Mistral 7B，09-27） |
| 2023 | 11 月 | 美国 Grok（Grok-1，11-05）｜中国 DeepSeek（DeepSeek-LLM） |
| 2023 | 12 月 | 美国 Gemini（Gemini 1.0，12-06） |
| 2023 | 全年 | 中国 Kimi（月之暗面助手）｜北美 Cohere Command｜中国 MiniMax（首代模型） |
| 2024 | 12 月 | 美国 Amazon Nova（Nova，12-02，re:Invent） |
| 2025 | 07 月 / 09 月 | 新加坡 Agnes（Agnes AI / Sapiens AI，2025-07 平台首发）｜中国 LongCat（LongCat-Flash-Chat / 龙猫，2025-09-01 开源） |
| 2025– / 2026 | 最新版本密集发布期（截至 2026-08-06）：GPT-5.6（07-09）、Claude Fable 5/Mythos 5（06-30）+ Opus 4.8（05-28）+ Opus 5（07-24）、Gemini 3.6 Flash 家族（07-21）+ 3.5 Pro（07-17）、Grok 4.5（07-09）、Llama 5（04-08）、Mistral Large 3、Command A+、Nova 2（Lite / Pro）；国产 DeepSeek V4 正式版（07-15）、Qwen3.8-Max（07-19 预览 → 08-03 正式）、GLM-5.2（06）、Kimi K3（07，07-27 开源权重）、豆包 2.1 Pro、文心 5.1、混元 Hy3 正式版（07）、MiniMax M3（06-01）、星火 X2-VL（06）；LongCat-2.0（07-06 开源）、Agnes 2.5-Flash（07-13）+ 2.5-Pro-Alpha（08-03）等；Thinking Machines Inkling（07-15）等（详见第一节） |  |

## 表 9：📅 事件日历（前瞻 · 待生效复核）

| 类别 | 事件 | 生效日 | 距今日 | 状态 | 复核机制 / 备注 |
| --- | --- | --- | --- | --- | --- |
| 促销到期 | Claude Sonnet 5 促销 $2/$10 到期恢复 ¥20.32/¥101.60（$3/$15） | 2026-08-31 | 已生效 | pending | T-7 已触发；到期日复核官网价是否恢复 |
| 平台停服 | 零一万物开放平台停止 API / 在线体验转企业级（All-in-B）；退款窗口至 2026-12-03 | 2026-09-03 | 已生效 | pending | 生产用户迁移风险；停服日复核链接是否失效 |
| 发布 | Qwen3.8-27B 开源发布08-03 GA 时官方承诺「下周」开源 | 待确认 | — | 待核实 | 承诺已过期；复核 HuggingFace 是否已发布 |
| 促销到期 | 腾讯云 TokenHub 新人 100 万到期覆盖 Hy3 preview / DeepSeek-V4 / GLM-5 / MiniMax-M3 | 2026-12-31 | 62 天 | pending | T-7 再提醒（2026-12-24 起） |
| 促销到期 | Gemini 3.6/3.7 Flash 限时五折到期双双恢复 $1.50/$7.50（¥10.16/¥50.80）；3.6 Flash 已同步降价 | 2027-01-01 | 63 天 | pending | T-7 再提醒（2026-12-25 起） |
| 促销到期 | 阿里 Qwen3.7-Max 错峰 2 折22:00–08:00 低至 2 折；Token Plan 夜间 5 折 | 待定 | 持续监控 | pending | 结束日待定 → 每周轮询官方活动页 |
| 调价生效 | DeepSeek V4 全系峰谷调价生效高峰×2 / 空闲基准；V4 Pro 峰 ¥9.00/¥27.00（官方人民币价） | 2026-08-17 | 已生效 | confirmed | 6 源交叉确认（08-17 00:00）；状态机闭环示例 |

## 表 10：📈 排序总览（按输入价从低到高）

| # | 模型（厂商） | 最新产品 | 地区 | 输入价 / ¥/MTok | 输出价 / ¥/MTok | 缓存命中 / 输入价 | 备注 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | IBM Granite granite-4.1-8b | ibm-granite/granite-4.1-8b | 美国 | ¥0.34 | ¥0.68 | ¥0.34 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.34；上下文 131K；来源 openrouter.ai/api/v1/models |
| 2 | Microsoft Phi phi-4 | microsoft/phi-4 | 美国 | ¥0.47 | ¥0.95 | ¥0.00 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.00；上下文 16K；来源 openrouter.ai/api/v1/models |
| 3 | InclusionAI Ling ling-2.6-1t | inclusionai/ling-2.6-1t | 中国 | ¥0.51 | ¥4.23 | ¥0.10 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.10；上下文 262K；来源 openrouter.ai/api/v1/models |
| 4 | Poolside laguna-s-2.1 | poolside/laguna-s-2.1 | 美国 | ¥0.61 | ¥1.22 | ¥0.06 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.06；上下文 1.0M；来源 openrouter.ai/api/v1/models |
| 5 | Reka AI reka-edge | rekaai/reka-edge | 美国 | ¥0.68 | ¥0.68 | ¥0.00 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.00；上下文 16K；来源 openrouter.ai/api/v1/models |
| 6 | Xiaomi MiMo mimo-v2.5 | xiaomi/mimo-v2.5 | 中国 | ¥0.95 | ¥1.90 | ¥0.02 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.02；上下文 1.1M；来源 openrouter.ai/api/v1/models |
| 7 | 腾讯混元 Hy3 | Tencent Hunyuan Hy3 | 中国 | ¥1.00 | ¥4.00 | ¥0.25 | Apache 2.0 开源；性价比标杆 |
| 8 | Upstage Solar solar-pro-3 | upstage/solar-pro-3 | 韩国 | ¥1.02 | ¥4.06 | ¥0.10 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.10；上下文 128K；来源 openrouter.ai/api/v1/models |
| 9 | StepFun 阶跃星辰 step-3.7-flash | stepfun/step-3.7-flash | 中国 | ¥1.35 | ¥7.79 | ¥0.27 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.27；上下文 262K；来源 openrouter.ai/api/v1/models |
| 10 | Arcee AI trinity-large-thinking | arcee-ai/trinity-large-thinking | 美国 | ¥1.49 | ¥5.76 | ¥0.41 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.41；上下文 262K；来源 openrouter.ai/api/v1/models |
| 11 | Inception Labs Mercury 2 | inception/mercury-2 | 美国 | ¥1.69 | ¥5.08 | ¥0.17 | $0.25 / $0.75（首方官方价，本期市场覆盖扫描新增）；缓存读 ¥0.17；上下文 128K；来源 官方定价页 |
| 12 | Nex AGI Nex-N2-Pro | nex-agi/nex-n2-pro | 美国 | ¥1.69 | ¥6.77 | ¥0.17 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.17；上下文 256K；397B MoE / Apache 2.0；mini 档 ¥0.17/¥0.68；本期市场覆盖扫描新增；来源 openrouter.ai/api/v1/models |
| 13 | ByteDance Seed seed-2.0-lite | bytedance-seed/seed-2.0-lite | 中国 | ¥1.69 | ¥13.55 | ¥0.00 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.00；上下文 262K；来源 openrouter.ai/api/v1/models |
| 14 | 讯飞星火 Spark X2 | iFlytek Spark X2 | 中国 | ¥2.00 | ¥2.00 | — | 官方统一单价（输入=输出） |
| 15 | Amazon Nova 2 Lite | Nova 2 Lite | 美国 | ¥2.03 | ¥16.93 | — | $0.30 / $2.50；1M 上下文 |
| 16 | MiniMax M3 | MiniMax-M3 | 中国 | ¥2.10 | ¥8.40 | ¥0.42 | 官方人民币价：标准 ¥4.20/¥16.80，≤512k 上下文永久五折后 ¥2.10/¥8.40；>512k 翻倍；1M 上下文；本期完整性修正补入 |
| 17 | Agnes 2.5 Pro Alpha | Agnes-2.5-Pro-Alpha | 新加坡 | ¥3.05 | ¥6.10 | ¥0.03 | $0.45 / $0.90（08-03 Alpha 收费档）；缓存 $0.0038；1M 上下文（本期新增） |
| 18 | Mistral Large 3 | Mistral Large 3 | 欧洲 | ¥3.39 | ¥10.16 | — | $0.50 / $1.50；开放权重 |
| 19 | 百度文心 ERNIE 5.1 | ERNIE 5.1 | 中国 | ¥4.00 | ¥18.00 | — | ≤32k 档（¥0.004/千tok 入、¥0.018/千tok 出）；32k–128k 升 ¥6/¥22 |
| 20 | NVIDIA Nemotron nemotron-3-ultra-550b-a55b | nvidia/nemotron-3-ultra-550b-a55b | 美国 | ¥4.06 | ¥24.38 | ¥1.35 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥1.35；上下文 512K；来源 openrouter.ai/api/v1/models |
| 21 | Writer Palmyra palmyra-x5 | writer/palmyra-x5 | 美国 | ¥4.06 | ¥40.64 | ¥0.00 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.00；上下文 1.0M；来源 openrouter.ai/api/v1/models |
| 22 | DeepSeek V4 Pro | DeepSeek-V4-Pro | 中国 | ¥4.50 | ¥13.50 | ¥0.15 | 峰谷双档已生效（2026-08-17）：高峰（9–12、14–18 点）×2 → 峰 入¥9.00/出¥27.00/缓存¥0.30；谷（空闲基准）入¥4.50/出¥13.50/缓存¥0.15（官方人民币价）；08-13 正式版（-0813）GA |
| 23 | Kwaipilot KAT-Coder-Pro V2.5 | kwaipilot/kat-coder-pro-v2.5 | 中国 | ¥5.01 | ¥20.05 | ¥1.02 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥1.02；上下文 256K；Air V2.5 档 ¥1.02/¥4.06；本期市场覆盖扫描新增；来源 openrouter.ai/api/v1/models |
| 24 | 美团 LongCat-2.0 | LongCat-2.0 | 中国 | ¥5.08 | ¥19.98 | ¥0.04 | 官方 $0.75/$2.95；初上线限时折扣 ¥2.03/¥8.13（缓存 ¥0.04）；1M 上下文；MIT 开源可自托管；本期完整性修正补入 |
| 25 | Google Gemini 3.6 Flash | Gemini 3.6 Flash | 美国 | ¥5.08 | ¥25.40 | — | $0.75/$3.75 限时五折（08-13 起，至 2026-12-31，之后恢复 $1.50/$7.50）；3.5 Pro 已发（$2/$12） |
| 26 | 字节豆包 2.1 Pro | Doubao-Seed-2.1-pro | 中国 | ¥6.00 | ¥30.00 | ¥1.20 | 缓存命中 ¥1.2；Turbo 版半价 |
| 27 | Thinking Machines Inkling | Inkling | 美国 | ¥6.77 | ¥27.43 | ¥1.15 | 无第一方 API，OpenRouter 托管 $1.00/$4.05（缓存读 $0.17≈¥1.15）；975B/41B MoE、Apache 2.0（07-15） |
| 28 | 智谱 GLM-5.2 | GLM-5.2 | 中国 | ¥8.00 | ¥28.00 | ¥2.00 | 官方人民币价（输入¥8 / 输出¥28 / 缓存¥2）；1M 上下文；国际档 $1.40/$4.40 |
| 29 | DeepCogito cogito-v2.1-671b | deepcogito/cogito-v2.1-671b | 美国 | ¥8.47 | ¥8.47 | ¥0.00 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.00；上下文 128K；来源 openrouter.ai/api/v1/models |
| 30 | Amazon Nova 2 Pro | Nova 2 Pro | 美国 | ¥8.47 | ¥67.73 | — | $1.25 / $10.00；1M 上下文；Nova 2 推理旗舰 |
| 31 | Meta Muse Spark 1.2 | muse-spark-1.2 | 美国 | ¥8.47 | ¥28.79 | ¥1.02 | Meta 首个智能体编码模型（08-05 公测）；1M 上下文；缓存读 ¥1.02；来源 官方/OpenRouter meta/muse-spark-1.2 |
| 32 | 阿里通义千问 qwen3.8-max | qwen3.8-max | 中国 | ¥12.00 | ¥36.00 | ¥1.50 | 官方人民币价（08-03 正式发布）；隐式缓存命中 ¥1.5；国际 $2/$6；qwen3.7-max 同价在售 |
| 33 | xAI Grok 4.6 | Grok 4.6 | 美国 | ¥13.55 | ¥40.64 | ¥3.39 | $2 / $6；>200K 长上下文 $4/$12；08-12 深夜发布 |
| 34 | AI21 Jamba jamba-large-1.7 | ai21/jamba-large-1.7 | 以色列 | ¥13.55 | ¥54.19 | ¥0.00 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.00；上下文 256K；来源 openrouter.ai/api/v1/models |
| 35 | Google Gemini 3.5 Pro | Gemini 3.5 Pro | 美国 | ¥13.55 | ¥81.28 | — | $2/$12（≤200k 提示）；2M 上下文（发布报道，待官方确认） |
| 36 | Cohere Command A | Command A | 加拿大 | ¥16.93 | ¥67.73 | — | $2.50 / $10；企业 RAG / Agents |
| 37 | 月之暗面 Kimi K3 | Kimi K3 | 中国 | ¥20.00 | ¥100.00 | ¥2.00 | 官方人民币价；缓存¥2.00；1M 上下文；2.8T/450B 激活（07-27 开源权重） |
| 38 | Perplexity Sonar sonar-pro | perplexity/sonar-pro | 美国 | ¥20.32 | ¥101.60 | ¥0.00 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥0.00；上下文 200K；来源 openrouter.ai/api/v1/models |
| 39 | Meta Llama 5 (600B) | Llama 5 600B MoE | 美国 | ¥23.71 | ¥47.41 | — | 第三方托管价 $3.50/$7（如 Together）；权重免费自托管（仅算力成本）；第三方来源价格存分歧（待核实） |
| 40 | Anthropic Claude Opus 5 | Claude Opus 5 | 美国 | ¥33.87 | ¥169.35 | ¥3.39 | $5 / $25（半价旗舰，性能逼近 Fable 5；07-24 发布） |
| 41 | Sakana AI fugu-ultra | sakana/fugu-ultra | 日本 | ¥33.87 | ¥203.20 | ¥3.39 | OpenRouter 挂牌价（第三方，非官方，待官网核实）；缓存读 ¥3.39；上下文 1.0M；来源 openrouter.ai/api/v1/models |
| 42 | OpenAI GPT-5.6 (Sol) | gpt-5.6-sol | 美国 | ¥33.87 | ¥203.20 | ¥3.39 | $5 / $30；Terra $2/$12（07-30 降 20%）、Luna $0.20/$1.20（降 80%）；Sol 新增 Fast 模式（2.5× 速、2× 价） |
| 43 | Anthropic Claude Fable 5 | Claude Fable 5 | 美国 | ¥67.73 | ¥338.67 | ¥6.77 | $10 / $50（Mythos 级）；缓存读 $1.00（口径修正）；Opus 4.8 $5/$25、Sonnet 5 $2-3/$10-15 |

## 表 11：🧪 能力评测AA 免费 API

| 模型 | 厂商 | AA Index | 编码 Index | 混合价 ¥/1M | 性价比 value | 吞吐 tok/s | TTFT s |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1. Claude Opus 5.5 (Max, Default Fallback) | Anthropic | 58.4 | — | 53.88 | 1.08 | 96.571 | 393.022 |
| 2. Claude Opus 5.5 (Xhigh, Default Fallback) | Anthropic | 57.0 | — | 53.88 | 1.06 | 82.442 | 49.036 |
| 3. GPT-6 Astra (Max) | OpenAI | 56.9 | 76.9 | 134.70 | 0.42 | 68.937 | 191.76 |
| 4. GPT-6 Astra (Xhigh) | OpenAI | 55.3 | 75.9 | 134.70 | 0.41 | 71.036 | 69.053 |
| 5. GPT-6 Astra (High) | OpenAI | 54.8 | 77.1 | 134.70 | 0.41 | 56.158 | 27.526 |
| 6. GPT-6.1 Sol (Max) | OpenAI | 54.5 | — | 26.94 | 2.02 | 79.663 | 157.321 |
| 7. Claude Sonnet 5.5 (Max, Default Fallback) | Anthropic | 54.2 | — | 26.94 | 2.01 | 136.207 | 283.739 |
| 8. GPT-6.1 Sol (Xhigh) | OpenAI | 52.3 | — | 26.94 | 1.94 | 66.145 | 67.969 |
| 9. Claude Opus 5.5 (High, Default Fallback) | Anthropic | 51.7 | — | 53.88 | 0.96 | 80.392 | 13.963 |
| 10. GPT-6 Astra (Medium) | OpenAI | 51.5 | 76.7 | 134.70 | 0.38 | 51.179 | 3.899 |
| 11. GPT-6.1 Terra (Max) | OpenAI | 51.0 | — | 13.47 | 3.79 | 90.933 | 169.206 |
| 12. Gemini 4 Argon (High) | Google | 50.4 | — | 26.94 | 1.87 | 82.47 | 28.227 |
| 13. GPT-6.1 Sol (High) | OpenAI | 50.2 | — | 26.94 | 1.86 | 63.419 | 19.758 |
| 14. Muse Wonder Full (Max) | Meta | 49.7 | — | — | — | 0 | 0 |
| 15. Claude Fable 5.1 (Xhigh, Default Fallback) | Anthropic | 49.7 | 80.7 | 134.70 | 0.37 | 61.038 | 30.378 |
| 16. Claude Sonnet 5.5 (Xhigh, Default Fallback) | Anthropic | 49.6 | — | 26.94 | 1.84 | 106.054 | 12.061 |
| 17. Claude Fable 5.1 (Max, Default Fallback) | Anthropic | 49.0 | 81.6 | 134.70 | 0.36 | 67.845 | 155.724 |
| 18. Claude Opus 5.5 (Medium, Default Fallback) | Anthropic | 48.1 | — | 53.88 | 0.89 | 79.344 | 10.698 |
| 19. Claude Fable 5.1 (High, Default Fallback) | Anthropic | 47.0 | 79.1 | 134.70 | 0.35 | 56.434 | 1.765 |
| 20. GPT-6.1 Sol (Medium) | OpenAI | 46.1 | — | 26.94 | 1.71 | 56.406 | 3.722 |

## 表 12：🌐 开源生态数据HF 镜像 + GitHub

| 家族/厂商 | HF 代表模型 | 下载量 | 周增量 | 点赞 | 衍生 | License | GitHub 主仓 | Star | 周增量 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Qwen 通义千问 | Qwen/Qwen3-0.6B | 24,162,298 | +433,241 | 1,856 | 100+ | apache-2.0 | QwenLM/Qwen3 | 27,688 | +5 |
| GLM 智谱 | zai-org/GLM-5.3-Flash | 6,417,099 | +66,433 | 2,973 | 100+ | mit | zai-org/GLM-4.5 | 4,425 | +1 |
| IBM Granite | ibm-granite/granite-embedding-small-english-r2 | 6,387,902 | +141,830 | 112 | 16 | apache-2.0 | ibm-granite/granite-code-models | 1,249 | +0 |
| DeepSeek | deepseek-ai/DeepSeek-V3.2 | 6,019,167 | +324,553 | 1,591 | 62 | mit | deepseek-ai/DeepSeek-V3 | 104,656 | +42 |
| Microsoft Phi | microsoft/mdeberta-v3-base | 5,527,817 | +129,194 | 261 | 100+ | mit | microsoft/PhiCookBook | 3,902 | -1 |
| MiniMax | MiniMaxAI/MiniMax-H3 | 5,441,738 | +156,419 | 6,417 | 100+ | other | MiniMax-AI/MiniMax-M1 | 3,186 | +1 |
| Llama | meta-llama/Llama-3.1-8B-Instruct | 4,899,647 | +54,562 | 8,649 | 100+ | llama3.1 | meta-llama/llama | 59,628 | -1 |
| Mistral | mistralai/Voxtral-Mini-4B-Realtime-2602 | 1,994,449 | -37,264 | 1,052 | 68 | apache-2.0 | mistralai/mistral-inference | 10,823 | +2 |
| Kimi 月之暗面 | moonshotai/Kimi-K3 | 854,823 | -1,409 | 11,863 | 100+ | other | MoonshotAI/Kimi-K3 | 9,002 | +11 |
| MiMo 小米 | XiaomiMiMo/MiMo-V2.5 | 117,800 | -10,244 | 431 | 30 | mit | XiaomiMiMo/MiMo-Code | 13,734 | +7 |
| InclusionAI | inclusionAI/LLaDA2.0-mini | 98,555 | -10,049 | 71 | 10 | apache-2.0 | inclusionAI/Ling | 273 | +1 |
| ByteDance Seed | ByteDance-Seed/UI-TARS-1.5-7B | 57,754 | -29,641 | 616 | 28 | apache-2.0 | — | — | 首日快照 |
| LongCat 美团 | meituan-longcat/LongCat-Image-Edit-Turbo | 23,138 | +362 | 72 | 4 | apache-2.0 | — | — | 首日快照 |
| Nex AGI | nex-agi/Nex-N2.5-mini | 3,205 | +37 | 879 | 46 | apache-2.0 | — | — | 首日快照 |
| Agnes Sapiens | Agnes-AI/Agnes-3.0-Flash | 689 | -23 | 252 | 21 | apache-2.0 | — | — | 首日快照 |

## 表 13：🌐 开源生态数据HF 镜像 + GitHub

| 家族 | 模型 | 现 License |
| --- | --- | --- |
| 本周无许可证变更 |  |  |

## 表 14：🎯 价格特惠 / 折扣活动（2～5 折及更多）新增

| 厂商 / 模型 | 特惠内容 | 折扣力度 | 折扣后实际价 / ¥/MTok（输入/输出） | 状态 / 有效期 | 备注 |
| --- | --- | --- | --- | --- | --- |
| 阿里 Qwen3.7-Max（百炼 / Qoder） | 常规时段 5 折；错峰 22:00–08:00 低至 2 折（0.1x，省 80%） | 5 折 / 2 折 | 5折 ¥6.00/¥18.00 / 2折 ¥2.40/¥7.20 | 进行中 结束日待定 | 基准：标准价 ¥12/¥36；覆盖输入/输出/缓存 |
| 阿里百炼 Token Plan | 新客直省 50%；包季综合低至 4.5 折 | 5 折 / 4.5 折 | 套餐充值 / ×0.5 / ×0.45 | 进行中 订阅制 | 150+ 款通用 Credits，无单一模型价 |
| 阿里 Qwen3.8-Max（千问 AI 平台 Token Plan） | 夜间时段调用 Qwen3.8-Max 享 5 折 Credits 消耗（2026-08-03 官宣，随新模型首发） | 5 折（夜间） | 按 Credits 折算 / 等效 ¥6.00/¥18.00 | 进行中 结束日待定 | 基准：标准价 ¥12/¥36（缓存 ¥1.5）；限 Token Plan 订阅用户，按量计费用户不适用 |
| DeepSeek V4-Pro | 2026-05-31 起永久降价至原价 1/4（2.5 折）；2026-08-17 演进为峰谷双档官方价（见下条） | 2.5 折 → 峰谷 | 历史 2.5折 ¥3.00/¥6.00 / 现峰谷 峰¥8.94/谷¥4.47 | 已永久化 峰谷 2026-08-17 生效 | 原价 ¥12/¥24；2.5 折仍为峰谷历史基准 |
| DeepSeek V4 峰谷 | 峰谷计费：高峰（工作日 9–12、14–18 点）价格 ×2；空闲时段（谷）为基准价；V4 Flash 同结构 | 高峰 ×2 / 空闲基准 | Pro 峰 ¥8.94/¥26.82（缓存¥0.30） / Pro 谷 ¥4.47/¥13.41（缓存¥0.15） / Flash 峰 ¥2.98/¥8.94（缓存¥0.09） / Flash 谷 ¥1.49/¥4.47（缓存¥0.05） | 已生效 2026-08-17 00:00 | 官方峰谷双档（api-docs.deepseek.com）；资源调度式「电价化」 |
| 腾讯云 DeepSeek-V4（转售） | 缓存命中降幅最高 97.5% | 缓存命中 -97.5% | 低至 ¥0.30/¥0.60 | 进行中 渠道价 | 基准：转售标准价 ¥12/¥24 |
| 阿里 Qwen3 系列（6/13） | 全系 40% 降价 | 6 折 | ¥2.03/¥8.13 | 已并入 标准价 | Qwen3 Max → $0.30/$1.20，已永久化 |
| 小米 MiMo V2.5 | 永久降价最高 99% | 1 折 | —（补充参考） | 已永久化 | 不在主表 16 款，无标准基准价 |
| MiniMax M3 | ≤512k 上下文永久五折（标准价 ¥4.20/¥16.80 折后 ¥2.10/¥8.40） | 5 折 | ¥2.10/¥8.40 | 已永久化 标准价 | 基准：标准价 ¥4.20/¥16.80；开放平台文档标注（08-02 官宣） |
| Qoder 全系列工具 | 夜间 22:00–08:00 调用低至 2 折 | 2 折（夜间） | 以 Qwen3.7-Max 计 / ¥2.40/¥7.20 | 进行中 会员 | 各模型同 ×0.2；QoderWork CN 等工具 |

## 表 15：🎁 免费试用 / 送 Token 活动新增

| 厂商 / 平台 | 免费额度 | 有效期 | 备注 |
| --- | --- | --- | --- |
| 阿里百炼 | 新用户 100 万 + 每模型 100 万；qwen-turbo 永久每月 100 万 | 90 天 / 永久 | 覆盖 Qwen3.7 全系 |
| 智谱 GLM | GLM-4-Flash / 4.7-Flash 永久免费无限量；新用户 2000 万 Token | 永久 / 3 个月 | 128K 上下文，无需注册即用 |
| 腾讯云 TokenHub | 新人 100 万 Tokens（语言模型共享） | 至 2026-12-31 | 覆盖 Hy3 preview、DeepSeek-V4、GLM-5、MiniMax-M3 |
| 腾讯混元 lite | 永久免费无限量 | 永久 | 128K 上下文基础对话 |
| 火山引擎（豆包） | 每日 200 万 Token（凌晨刷新，不累积） | 持续 | 需实名，QPS=2 |
| 月之暗面 Kimi | 新用户约 800 万 Token；每日限量消息 | 活动期 | 长上下文之王，常返券（充 100 返 300） |
| MiniMax | 15 元代金券（实名后） | 约 2 个月 | — |
| 百度千帆 | ERNIE-Speed / Lite 永久免费；每模型 100 万 | 永久 / 3 个月 | — |
| 讯飞星火 | 每模型 20 万永久；V4 50 万（30 天试用） | 永久 / 30 天 | 注册可领 500 万 |
| 硅基流动（SiliconCloud） | 新用户 2000 万（永久，活动期累计 3000 万） | 永久 | 多模型聚合，最快推理 |
| 超算互联网 | 1000 万 Tokens | 1 个月 | MiniMax/DeepSeek/Qwen 等 |
| OpenRouter | ~30 个永久免费模型，每日 50 次请求 | 永久 | 无需信用卡，router 自动路由 |
| Google Gemini API | Flash / Flash-Lite 免费额度 | 持续 | Pro 已于 4/1 移出免费层；15 RPM / 250K TPM |
| ChatGPT Free / Go | 有限免费消息（约 10 条 / 5 小时降级） | 持续 | — |
| Claude Sonnet 5 | 每日限量免费消息（基础访问） | 持续 | — |
| Mistral | Free Tier 每月 ~100 credits | 每月 | 限速 ~6 RPM |
| NVIDIA NIM | 新用户 1000 Credits | 12 个月 | 企业级 GPU |
| Cloudflare Workers AI | 每日 1 万次免费请求（无 token 限制） | 持续 | 边缘低延迟 |
| GitHub Models | GitHub token 免费调用 GPT-5 / 4o 等 | 持续 | 无需绑卡 |
| Groq / Cerebras | 新用户注册免费调用 | 持续 | 无需绑卡；Llama / GPT-oss 等 |

## 表 16：预算档 / 轻量档参考（更便宜的同家族选项）

| 模型 | 轻量档产品 | 输入价 ¥/MTok | 输出价 ¥/MTok | 说明 |
| --- | --- | --- | --- | --- |
| OpenAI | gpt-5.6-luna | ¥1.35 | ¥8.13 | $0.20 / $1.20（07-30 降价 80%） |
| Google | Gemini 3.5 Flash-Lite | ¥2.03 | ¥16.93 | $0.30 / $2.50（全系最低之一） |
| DeepSeek | V4 Flash | ¥1.50 | ¥4.50 | 峰谷双档（2026-08-17 生效）：谷（空闲基准）¥1.50/¥4.50（缓存¥0.05）、峰（9–12、14–18 点）×2 → ¥3.00/¥9.00（缓存¥0.10）；权重开源 HuggingFace MIT |
| Kwaipilot 快手 | KAT-Coder-Air V2.5 | ¥1.02 | ¥4.06 | $0.15 / $0.60（OpenRouter 挂牌价，待官网核实）；缓存读 ¥0.20；256K 上下文（本期新增） |
| 字节豆包 | Seed-2.1-mini | ¥0.20 | ¥2.00 | 超低本档，规模化首选 |
| Anthropic | Haiku 4.5 | ¥6.77 | ¥33.87 | $1 / $5，最便宜 Claude 档 |
| Meta Llama 5 | 70B / 8B 自托管 | 免费 | 免费 | 权重免费（仅 GPU 算力），商业 700M MAU 内免授权费 |
