# 美联储货币政策与利率传导

---

## 触发场景

以下任一场景出现时，必须调用本skill的对应参考文档：

| 触发场景 | 核心问题 | 优先参考 |
|---------|---------|----------|
| **FOMC会议前后** | 加息/降息概率？点阵图变化？声明措辞？ | ref-01(Fed决策) + ref-04(市场预期框架) |
| **非农/CPI/PCE等关键数据发布** | 数据如何影响降息预期？基本面-政策-市场三方偏差？ | ref-04(市场预期) + ref-06(利率传导) |
| **SOFR/回购利率异常跳升** | 流动性出了什么问题？SLR季末？ | ref-03(利率走廊) + ref-05(回购市场) |
| **Fed资产负债表变动（QT/RMP）** | 准备金够不够？ON RRP还剩多少？ | ref-02(资产负债表) + ref-03(利率走廊) |
| **期限利差倒挂/异常走阔** | 衰退信号？传导链断在哪？ | ref-06(利率传导) + ref-04(市场预期) |
| **债务上限僵局** | TGA冲击？解决后补发效应？ | ref-03(利率走廊) + ref-07(Fed-Treasury) |
| **市场降息/加息预期与Fed分歧** | 市场定价是否过度？预期差交易？ | ref-04(市场预期框架) + ref-10(周期资产) |
| **基差交易/CFTC头寸极端** | 系统性风险？杠杆基金平仓冲击？ | ref-05(回购市场) |
| **加息/降息周期开启** | 哪种类型？大类资产怎么走？类比哪个历史周期？ | ref-10(周期资产) |
| **Fed官员密集发声** | 做比说重要？操作与表态一致吗？ | ref-01(Fed决策) + ref-04(市场预期框架) |
| **财政支配担忧升温** | 期限溢价无增长支撑上行？Fed独立性受压？ | ref-07(Fed-Treasury) |
| **SRF被使用** | 流动性结构性紧张？还是季节性？ | ref-03(利率走廊) |

**快速判断**：如果问题涉及"Fed会怎么动""流动性紧不紧""市场定价了什么""利率为什么动"——就用本skill。

---

## 核心理念

1. **基本面-美联储-市场：基本面定方向，Fed定节奏，市场定定价**
2. **重价不重量**：货币市场看利率定价，不看操作量
3. **准备金是血液，利率是脉搏**
4. **政策利率与准备金数量"脱嵌"**
5. **做比说重要**
6. **先看ON RRP，再看准备金**
7. **影响波动而非方向**
8. **财政支配是长端最大尾部风险**

---

## 参考文档索引

| 编号 | 文件 | 功能定位 |
|---|---|---|
| 1 | [ref-01-fed-decision-and-communication.md](ref-01-fed-decision-and-communication.md) | FOMC架构、双重使命、政策工具箱、沟通解读、**关键人物档案** |
| 2 | [ref-02-fed-balance-sheet-and-reserves.md](ref-02-fed-balance-sheet-and-reserves.md) | Fed资产负债表、QT/RMP机制、准备金充足标准 |
| 3 | [ref-03-rate-corridor-and-money-rates.md](ref-03-rate-corridor-and-money-rates.md) | 地板系统、三种准备金状态、SRF、债务上限 |
| 4 | [ref-04-market-expectations.md](ref-04-market-expectations.md) | 基本面-美联储-市场三方框架、市场预期度量、三方偏差对比 |
| 5 | [ref-05-repo-and-basis-trade.md](ref-05-repo-and-basis-trade.md) | 回购市场结构、Specials、SLR约束、基差交易 |
| 6 | [ref-06-rate-transmission-and-curve.md](ref-06-rate-transmission-and-curve.md) | 短端/长端传导、曲线形态、传导链断点 |
| 7 | [ref-07-fed-treasury-and-fiscal-dominance.md](ref-07-fed-treasury-and-fiscal-dominance.md) | Fed-Treasury协调、RMP争议、财政支配风险 |
| 8 | [ref-08-data-sources-and-workflow.md](ref-08-data-sources-and-workflow.md) | 数据源汇总、日常跟踪、事件驱动流程 |
| 9 | [ref-09-common-misconceptions.md](ref-09-common-misconceptions.md) | 17条常见误读及正确理解 |
| 10 | [ref-10-rate-cycles-and-assets.md](ref-10-rate-cycles-and-assets.md) | 历次加息/降息周期、大类资产影响、历史类比 |

---

**风险揭示**: 以上内容由 AI 基于公开研究报告及其附属成果总结生成，可能省略完整报告中的重要信息、市场风险、业绩不及预期等风险，请务必阅读完整原始报告。有关数据、观点、评级等具有时效性，请自行核实最新信息。以上内容仅供研究学习使用，不构成任何投资建议。内容依 CC BY-NC-SA 4.0 协议发布，自行承担投资风险。
