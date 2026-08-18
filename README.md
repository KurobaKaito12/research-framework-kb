# research-framework-kb · 研究框架知识库

## 框架清单

| # | 框架标识 | 中文名 |
|---|---------|--------|
| 1 | a-share-rotation-allocation | 风格/行业/主线轮动方法论 |
| 2 | a-share-stock-deep-analysis | A股个股深度分析框架 |
| 3 | a-share-strategy | A股权益投资策略研判框架 |
| 4 | asset-allocation | 大类资产配置分析技能 |
| 5 | china-macro-tracker | 中国宏观经济追踪 |
| 6 | convertible-bond-skill | 中国可转债深度分析 |
| 7 | credit-analysis-skill | 信用债主体深度信用分析 |
| 8 | fed-monetary-policy | 美联储货币政策与利率传导 |
| 9 | fiscal-policy-analysis | 财政政策分析 |
| 10 | fixed-income-analysis | 固收研究框架 |
| 11 | gold-trader | 黄金交易员实战手册 |
| 12 | industry-analysis | 行业研究分析 |
| 13 | interest-rate-derivatives | 利率衍生品研究 |
| 14 | monetary-policy-liquidity | 货币政策与流动性分析框架 |
| 15 | overseas-strategy | 港股与海外权益策略研判框架 |
| 16 | pboc-balance-sheet | 中国央行资产负债表深度分析 |
| 17 | technical-analysis | A股技术分析技能库 |
| 18 | cross-asset-radar | 大类资产隐含预期雷达 |
| 19 | quant-industry-rotation | A股量化行业轮动 |
| 20 | quant-market-timing | A股多维量化择时 |
| 21 | quant-style-rotation | A股风格因子择时与轮动 |
| 22 | quant-asset-allocation | 量化大类资产配置 |
| 23 | quant-fund-evaluation | 公募基金评价归因筛选 |
| 24 | quant-fundamental-factors | 基本面量化选股因子 |
| 25 | consumer-discretionary-research | 可选消费研究框架 |
| 26 | us-equity-analysis | 美股市场综合分析 |
| 27 | us-macro-handbook | 美国基本面研究手册 |
| 28 | ust-framework | 美债利率走势研判框架 |

## 使用方式

三层调用，按需读取：

1. **list** — 读 `index.json`，浏览所有框架的名称、描述和触发场景
2. **get** — 读 `{framework-name}/main.md`，获取框架主文档（核心方法论、分析步骤）
3. **reference** — 读 `{framework-name}/ref-*.md`，获取子模块深度内容

人类读者从清单找到感兴趣的框架 → 打开 `main.md` → 需要深化时读同目录 `ref-*.md`。AI Agent 把本仓库挂为知识库（skill / RAG / 上下文均可），按上述三层调用，按需读取。

## 目录结构

```
./
├── SKILL.md                 调用说明（三层调用体系）
├── index.json               框架总索引
├── LICENSE                  许可协议
└── {framework-name}/
    ├── meta.json            框架元信息
    ├── main.md              主文档（核心方法论）
    └── ref-*.md             参考资料（子模块/指标清单/案例库）
```

## 环境依赖与已知限制

本库为**方法论知识库**，28 个框架的文档均完整可读；部分框架的**执行环节**依赖以下外部环境：

**1. 外部数据源与工具依赖（影响取数流程，不影响方法论阅读）**

- **数据终端**：框架的取数步骤以"数据需求：指标名（频率，日期区间）"的通用形式标注，任何数据源（iFinD / Wind / jin10 / tushare / 同花顺，或免费源如中国货币网、统计局官网、FRED）均可满足。文档不绑定任何特定工具。
- **联网搜索**：政策解读、央行沟通措辞等场景需要联网检索能力（任意搜索工具均可）。
- **浏览器抓取**：AAII、CME FedWatch、FINRA 等官网数据需要浏览器访问（us-equity-analysis 场景）。


**按数据门槛的框架分档（执行视角）**：

| 档位 | 框架 | 说明 |
|---|---|---|
| 免费公开源可跑 | ust-framework、us-macro-handbook、fed-monetary-policy、fiscal-policy-analysis、pboc-balance-sheet、monetary-policy-liquidity、china-macro-tracker、us-equity-analysis、cross-asset-radar、asset-allocation | FRED / 央行·财政部·CFTC 官网 / CME FedWatch / GDPNow，零成本可执行 |
| 低门槛商业源 | a-share-strategy、a-share-rotation-allocation、technical-analysis、quant-market-timing、quant-style-rotation、quant-industry-rotation（部分）、gold-trader、overseas-strategy | tushare（免费额度）/ jin10 / 同花顺，个人可负担 |
| 机构级订阅才能完整复现 | quant-fundamental-factors（朝阳永续分析师预期）、quant-fund-evaluation（基金持仓/Brinson 需 Wind）、quant-industry-rotation（分析师预期部分）、consumer-discretionary-research（电商 GMV 等行业高频数据） | 方法论与因子构造思路完全可学，可用公开数据近似复现；但原机构数据口径下的回测数字不可复现 |

以上环境仅为取数环节的可选项——本库全部 28 个框架的方法论自洽完整，无外部 skill 或脚本的前置依赖。

## 许可与免责

- 本库以 **CC BY-NC-SA 4.0**（署名-非商业性-相同方式共享）协议发布，见 [LICENSE](LICENSE)。
- 方法论内容整理自公开投研资料，仅供学习研究使用，不构成任何投资建议。有关数据、观点、评级等具有时效性，请自行核实最新信息，自行承担投资风险。
- 若内容涉及您的版权且您不希望其以当前方式呈现，请提 Issue，将在核实后第一时间处理。

