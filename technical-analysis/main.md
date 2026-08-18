# A股技术分析技能库

## 知识库索引

```
technical-analysis/
├── main.md                     # 本文件：导航、路由、组合规则
├── meta.json
├── ref-candlestick.md          # K线理论
├── ref-classic-theories.md     # 经典理论：道氏、波浪、缠论、江恩、周期理论
├── ref-trend-analysis.md       # 趋势与切线
├── ref-price-patterns.md       # 价格形态
├── ref-indicators.md           # 技术指标：趋势类/超买超卖类/波动率类/量价类
├── ref-volume-price.md         # 量价关系
├── ref-chip-distribution.md    # 筹码分布
├── ref-multi-timeframe.md      # 多时间框架
└── ref-a-share-features.md     # A股特色：涨跌停、龙虎榜、情绪周期
```

## 问题路由

### 综合研判（最重要）

当用户要求对某只股票进行全面技术分析时，按以下六步执行：

```
步骤1: 确定时间框架组合 → multi-timeframe.md
步骤2: 判断大趋势方向 → trend-analysis.md
步骤3: 识别价格形态 → price-patterns.md
步骤4: 验证技术指标 → indicators.md
步骤5: 分析量价关系 → volume-price.md
步骤6: 筹码+A股特色验证 → chip-distribution.md + a-share-features.md
```

### 单一维度查询

| 用户意图 | 主文件 | 辅助文件 |
|---------|--------|---------| 
| K线形态怎么看 | candlestick.md | trend-analysis.md |
| MACD/RSI/KDJ怎么用 | indicators.md | multi-timeframe.md |
| 怎么判断趋势 | trend-analysis.md | classic-theories.md |
| 量价背离 | volume-price.md | indicators.md |
| 筹码分布 | chip-distribution.md | volume-price.md |
| 打板/情绪周期 | a-share-features.md | volume-price.md |
| 波浪/缠论 | classic-theories.md | trend-analysis.md, indicators.md |
| 多周期分析 | multi-timeframe.md | — |
| 价格形态 | price-patterns.md | trend-analysis.md |

## 跨文件组合模式

**趋势确认型**: trend-analysis + multi-timeframe + indicators
**反转识别型**: price-patterns + volume-price + indicators + chip-distribution
**突破交易型**: trend-analysis + price-patterns + volume-price + multi-timeframe
**A股短线博弈型**: a-share-features + volume-price + multi-timeframe
**筹码成本分析型**: chip-distribution + volume-price + a-share-features
**经典理论实战型**: classic-theories + trend-analysis + price-patterns + indicators

## 矛盾信号优先级

从高到低：
1. 长周期趋势方向 — 最高优先级
2. 量价关系 — 最重要的反转预警
3. 价格形态 — 需时间确认
4. 技术指标 — 容易钝化
5. 筹码分布 — 辅助验证
6. A股特色指标 — 背景参考

**核心原则**：短期信号与长期趋势矛盾时，永远以长期趋势为准。

## 输出规范

综合研判回答必须包含：
1. **分析前提**：标的、价格、日期、时间框架组合
2. **趋势判断**：各周期方向、支撑阻力、均线排列
3. **形态与信号**：价格形态、指标状态、一致性评估
4. **量价与筹码**：量价形态、背离、筹码分布
5. **A股特色验证**（如适用）
6. **综合评估**：多维度信号汇总 + 信心水平 + 操作建议 + 风险点
7. **局限性声明**

### 信心水平

| 标签 | 条件 |
|------|------|
| 高信心 | ≥4个独立维度同方向信号 |
| 中信心 | 3个一致，1-2个模糊/矛盾 |
| 低信心 | 仅1-2个维度有信号，或主要维度矛盾 |
| 观望 | 无明确信号或完全矛盾 |

## 必须避免的错误

- 单一维度决策（至少3个独立维度确认）
- 忽视时间框架（先执行长周期过滤）
- 忽视量价配合（所有突破/反转需量价验证）
- 迷信资金流向（必须说明计算缺陷）
- 鼓励打板（长期平均收益 -0.93%）
- 精确预测价格（只能给区间和概率）
- 忽略A股制度差异（T+1、涨跌停、筹码分布等）

---

**风险揭示**: 以上内容由 AI 基于公开研究报告及其附属成果总结生成，可能省略完整报告中的重要信息、市场风险、业绩不及预期等风险，请务必阅读完整原始报告。有关数据、观点、评级等具有时效性，请自行核实最新信息。内容依 CC BY-NC-SA 4.0 协议发布，自行承担投资风险。
