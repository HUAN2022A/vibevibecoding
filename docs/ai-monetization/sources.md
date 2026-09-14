# 来源清单、可信度与待核实项

## 主要来源

| 来源 | 类型 | 可信度 | 说明 |
| --- | --- | --- | --- |
| [Sacra](https://sacra.com/) | 研究机构（公司档案 + 收入估算） | B | 提供 ARR/估值/融资/业务模式拆解。**收入为估算**，部分页面内部存在数字混用问题 |
| [Business of Apps](https://www.businessofapps.com/data/) | 行业数据聚合 | B | `ai-app-market`、`chatgpt-statistics`、`claude-statistics`、`suno-statistics`、`grok-statistics`、`character-ai-statistics`、`deepseek-statistics`、`google-gemini-statistics`、`microsoft-copilot-statistics`、`faceapp-statistics` |
| [levels.io](https://levels.io/) | 创始人本人公开数据 | A（自述） | Pieter Levels 长期公开自己的收入与成本，属**本人自述**，非审计 |
| AppMagic / Appfigures / Sensor Tower / SimilarWeb | 第三方 App 数据 | B | BoA 页面中大量收入与下载数据来源于此，均为估算 |
| Crunchbase | 融资数据 | B | 部分条目存在脏数据（如 Character.AI 融资额） |

## 按来源可信度对照

### 相对可靠（公司披露或以公司披露为准）

- OpenAI：$852B 估值、$122B 融资轮、$40B 年化收入、33% 毛利率、50M 消费者订阅、>9M 企业付费用户、$1B 广告年化、Stargate 相关承诺
- Suno：2M 付费订阅者、$5.4B Series D、WMG 合作条款
- ElevenLabs：41% Fortune 500、$11B Series D、$22/月起定价
- Midjourney：从未融资、约 40-45 人
- Pieter Levels 全部数字（本人自述）

### 机构估算（B 级，引用需注明「估算」）

- 所有 Sacra 的 ARR 数字（含 OpenAI $40B、Anthropic $65B、ElevenLabs $600M、Perplexity $750M、Sierra $200M、Glean $300M、Clay $150M、Harvey $350M、Abridge $100M、OpenEvidence $300M、HeyGen $205M、Synthesia $146M、Cursor $4B、Midjourney $200M、Runway $90M、Suno $300M）
- 所有 AppMagic / Appfigures / Sensor Tower 的 App 收入估算（FaceApp、Character.AI、Grok、Suno、CHATGPT 下载等）

### 需要谨慎（C 级）

- GitHub Copilot 订阅者 >1M（单一来源）
- Photopea 约 $1M/年（2021 年数据，已过期）
- 所有「某季度某 App 收入」的细分数据

### 不可用（D 级）

- Character.AI 的 Crunchbase 融资数据（$150K / $80K，明显错误）

---

## ⚠️ 待核实清单

以下是本次建立知识库时发现的**明确冲突或存疑项**，正式引用前必须回源核实。

### 1. Anthropic 收入：$6B vs $65B（冲突严重）

| 来源 | 数字 | 口径 |
| --- | --- | --- |
| Business of Apps | $6B | Anthropic 2025 自然年收入 |
| Business of Apps | $1.25B | Claude 产品线 2025 年收入 |
| Sacra | $65B | 2026-07 年化收入 |
| Sacra | $47B | 2026-05 年化收入 |

**问题**：从 2025 年底到 2026-07 的 7 个月内，年化收入从约 $6B 涨到 $65B（约 10 倍），需要极强的外部验证。

**更严重的疑点**：Sacra 页面同时出现 "`$65B` Series H funding round" 与 "`$65B` ARR"，两者的数字完全相同。**存在把融资轮金额与 ARR 混淆的可能性。**

**还需注意**：Sacra 明确指出 Anthropic 对云转售（AWS/Google/Microsoft）按 **gross 口径**记账，把终端客户总支出记为收入、把伙伴分成记为费用。这会系统性抬高收入，与 net 口径公司不可比。

**处理方式**：本知识库在两个数字间不加取舍，全部并列展示。**不要在任何对外材料中使用 Anthropic 的具体收入数字而不加说明。**

### 2. AI App 市场规模：$16.5B vs $18.5B（同一页面内部冲突）

Business of Apps 的 `ai-app-market` 页面中：

- 「Key AI Statistics」段落：AI app 行业 2025 年产生 **$18.5B**，其中 43% 来自 ChatGPT
- 「AI App Revenue」段落：AI app 行业 2025 年收入达 **$16.5B**，同比增长 180%

差 $2B。**以 $16.5B 为准更可能**（其明确写了同比 +180%），但需核实。

### 3. Suno 定价：$8/$24 vs $10/$30（冲突）

| 来源 | Pro | Premier |
| --- | --- | --- |
| Sacra | $8/月（~500 首） | $24/月（~2,000 首） |
| Business of Apps | $10/月（2,500 credits） | $30/月（10,000 credits） |

可能是定价调整前后、或年付 vs 月付的差异。**未解决。**

### 4. Suno 收入：$150M vs $300M（口径不同）

- Business of Apps：2025 Q3 单季 $34M，年化约 $150M
- Sacra：2026-02 ARR $300M

时点不同（2025 Q3 vs 2026 Q2），**不是直接冲突**，但引用时容易混淆。

### 5. WordPress 之外：估值与收入口径混用

Sacra 页面头部标签的语义不完全一致。例如：

- Anthropic 页面：REVENUE $65.00B / VALUATION $965.00B / FUNDING $125.00B / GROWTH RATE 800%（2025）
- Runway 页面：REVENUE $90.00M（2025）/ VALUATION $1.50B（2024）/ FUNDING $591.45M（2024）

**这些标签对应的时点不同**，不能当成同一时点的数据一起用。引用时必须逐个确认时点。

### 6. 需要补充的案例（下一步）

- [ ] 中国与亚太：Kimi、豆包、可灵、即梦、钉钉 AI、美图（Meitu）AI 收入
- [ ] AI 硬件与端侧：AI 眼镜、AI 玩具、AI 录音笔（Plaud 等）
- [ ] 移动端订阅榜：App Store / Google Play AI 类目高收入产品
- [ ] 失败案例：有融资但收入未跑出来的 AI 产品
- [ ] 基础设施层：CoreWeave、Together、Fireworks 等「卖铲子」的盈利能力
- [ ] AI 应用的真实定价与毛利率追踪表（需要持续更新）

---

## 数据维护约定

1. 新增案例必须在卡片末尾标注「可信度」等级。
2. 同一指标出现多个来源时，**全部并列写出**，不要只保留一个。
3. 所有数字必须带时点（YYYY-MM 或 YYYY Qn）。
4. 发现冲突时，同步写入本文件的「待核实清单」。
5. 定期复核：本知识库的基准日为 **2026-09-14**，AI 行业数据半衰期很短，建议每季度整体复核一次。
