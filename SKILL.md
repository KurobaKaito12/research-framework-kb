---
name: research-framework-kb
description: 研究框架知识库——覆盖28个投研方法论框架的三层调用体系（list/get/reference），支持A股策略、行业分析、固收、宏观、可转债、信用债、海外策略、量化金工、技术分析等全品类投研框架的程序化读取。
trigger: 用户询问投研方法论、研究框架、分析体系、策略框架、行业分析框架、固收框架、宏观框架、可转债框架、估值方法、技术分析框架，或需要系统化的分析指引时触发。也适用于"XX该怎么分析"、"用什么框架看XX"、"帮我梳理XX的研究方法"等提问。
---

# 研究框架知识库 Skill

## 概述

本 Skill 封装了 28 个投研方法论框架的知识库，支持三层调用体系：

1. **list** — 浏览所有可用框架的名称、描述和触发条件
2. **get** — 获取指定框架的主文档（核心方法论、分析步骤、关注要点）
3. **reference** — 获取框架下指定参考资料的深度内容（子模块方法论、指标清单、案例库）

采用 `list` / `get` / `reference` 三层调用，方法论文档源自公开投研方法论整理。

## 28 个框架一览

| # | 框架标识 | 中文名 | 触发场景 |
|---|---------|--------|---------|
| 1 | a-share-strategy | A股权益投资策略 | A股市场判断、大势/风格/行业三层研判 |
| 2 | a-share-rotation-allocation | A股风格轮动与行业轮动 | 大小盘切换、成长价值轮动、主题投资 |
| 3 | a-share-stock-deep-analysis | A股个股深度分析 | 商业模式、财务质量、护城河、估值、催化剂 |
| 4 | industry-analysis | 行业研究分析 | 行业分析、产业研究、竞争格局、生命周期 |
| 5 | asset-allocation | 大类资产配置 | MVO/BL/美林时钟/全天候/风险平价 |
| 6 | china-macro-tracker | 中国宏观经济跟踪 | GDP/PMI/社融/CPI/PPI/货币/财政 |
| 7 | overseas-strategy | 海外权益策略 | 港股/美股/南向资金/AH溢价 |
| 8 | fixed-income-analysis | 固收研究（五碗面） | 基本面/政策面/资金面/供求面/情绪面 |
| 9 | monetary-policy-liquidity | 货币政策与流动性 | 降息/降准/DR007/M1-M2/超储率 |
| 10 | fiscal-policy-analysis | 财政分析 | 赤字率/专项债/化债/土地财政 |
| 11 | convertible-bond-skill | 可转债分析 | 转股价值/溢价率/下修/赎回/双低策略 |
| 12 | credit-analysis-skill | 信用债分析 | 主体信用分析/偿债能力/评级 |
| 13 | interest-rate-derivatives | 利率衍生品 | 国债期货/IRS/基差/套保 |
| 14 | fed-monetary-policy | 美联储货币政策 | FOMC/QT/点阵图/SOFR |
| 15 | pboc-balance-sheet | 央行资产负债表 | 基础货币/货币乘数/科目分析 |
| 16 | gold-trader | 黄金交易 | 核心因子/价格行为/情景决策 |
| 17 | technical-analysis | 技术分析 | K线/形态/指标/量价/筹码 |
| 18 | cross-asset-radar | 大类资产隐含预期雷达 | 跨资产预期解码、背离扫描、risk-on/off |
| 19 | quant-industry-rotation | A股量化行业轮动 | 景气投资/残差动量/拥挤度/NDCG |
| 20 | quant-market-timing | A股多维量化择时 | ERP/期权PCR/融资买入/多路径打分 |
| 21 | quant-style-rotation | A股风格因子择时 | 市值/红利因子、趋势+拐点模型 |
| 22 | quant-asset-allocation | 量化大类资产配置 | 三层次逻辑（经济周期/宏观因子/趋势追踪） |
| 23 | quant-fund-evaluation | 公募基金评价归因 | Brinson/T-M/C-L/风格漂移 |
| 24 | quant-fundamental-factors | 基本面量化选股因子 | 价值/成长/分析师预期因子改造 |
| 25 | consumer-discretionary-research | 可选消费研究框架 | 酒店/餐饮/纺服/美护/家电五子行业 |
| 26 | us-equity-analysis | 美股市场综合分析 | 盈利×估值定价/AI周期/资金流情绪 |
| 27 | us-macro-handbook | 美国基本面研究手册 | GDP/非农/CPI/PCE/贸易政策 |
| 28 | ust-framework | 美债利率走势研判 | 五碗面+Clarida四因素/期限溢价 |

## 数据源

框架文档存储在仓库根目录下，结构如下：

```
./
├── SKILL.md                        # 本文件（调用说明）
├── index.json                      # 全局索引
├── {framework-name}/
│   ├── meta.json                   # 框架元信息
│   ├── main.md                     # 主文档
│   └── ref-{reference-name}.md     # 参考资料文档
```

## 调用流程

### Step 1: list — 浏览框架

```bash
# 读取全局索引
cat ./index.json
```

返回所有框架的 name、title、description、trigger、references 列表。

### Step 2: get — 获取主文档

```bash
# 读取指定框架的主文档
cat ./{framework-name}/main.md
```

主文档包含：核心方法论、分析步骤、关注要点、available_references 列表。

### Step 3: reference — 获取参考资料

```bash
# 读取指定参考资料的深度内容
cat ./{framework-name}/ref-{reference-name}.md
```

参考资料是主文档的细化补充：子模块方法论、指标清单、案例库等。

## 使用指引

### 何时调用本 Skill

| 用户问题类型 | 应读取的框架 | 应读取的层级 |
|-------------|-------------|-------------|
| "A股怎么看 / 大盘走势" | a-share-strategy | main + ref按需 |
| "大小盘怎么选 / 主题投资" | a-share-rotation-allocation | main + refs |
| "这家公司怎么样 / 护城河" | a-share-stock-deep-analysis | main + refs |
| "XX行业怎么分析" | industry-analysis | main + refs |
| "资产怎么配置" | asset-allocation | main + refs |
| "中国经济怎么看" | china-macro-tracker | main + refs |
| "港股/美股怎么看" | overseas-strategy | main + refs |
| "债市怎么看" | fixed-income-analysis | main + refs |
| "流动性怎么看" | monetary-policy-liquidity | main + refs |
| "财政怎么看" | fiscal-policy-analysis | main + refs |
| "这个转债怎么样" | convertible-bond-skill | main + refs |
| "信用风险怎么看" | credit-analysis-skill | main + refs |
| "国债期货/IRS" | interest-rate-derivatives | main + refs |
| "美联储怎么看" | fed-monetary-policy | main + refs |
| "央行资产负债表" | pboc-balance-sheet | main + refs |
| "黄金怎么看" | gold-trader | main |
| "技术面怎么看" | technical-analysis | main + refs |
| "市场在price in什么 / 跨资产背离" | cross-asset-radar | main |
| "行业轮动 / 景气投资" | quant-industry-rotation | main |
| "A股择时 / 该不该买" | quant-market-timing | main |
| "大小盘 / 红利择时" | quant-style-rotation | main |
| "量化资产配置 / 股债商汇" | quant-asset-allocation | main |
| "基金评价 / 怎么挑基金" | quant-fund-evaluation | main |
| "价值/成长因子 / 多因子选股" | quant-fundamental-factors | main |
| "酒店/餐饮/纺服/美护/家电" | consumer-discretionary-research | main + 子行业ref |
| "美股怎么看 / 科技股" | us-equity-analysis | main + refs |
| "美国GDP/非农/CPI" | us-macro-handbook | main + refs |
| "美债利率 / 十年期美债" | ust-framework | main + refs |

### 按需读取原则

- **不要一次读取全部文档**。先根据用户问题定位框架，读取 main.md，然后按需读取 reference
- main.md 末尾通常会列出 available_references，指引用户需要深入哪个子模块
- 一次最多读取 2-3 个 reference，避免上下文溢出

## 数据来源与风险揭示

**数据来源**：研究框架知识库（原始方法论源自公开投研方法论整理）

**风险揭示**：以上内容由 AI 基于研究报告及公开投研方法论总结生成，可能省略完整报告中的重要信息、市场风险、业绩不及预期等风险，请务必阅读完整原始报告。有关数据、观点、评级等具有时效性，请自行核实最新信息。以上内容仅供研究学习使用，不构成任何投资建议。内容依 CC BY-NC-SA 4.0 协议发布，自行承担投资风险。
