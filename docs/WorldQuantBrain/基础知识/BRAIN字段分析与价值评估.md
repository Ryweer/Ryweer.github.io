# WorldQuant BRAIN 字段分析与价值评估

> 数据来源：WorldQuant BRAIN Platform  |  字段总数：2,627（14个数据集）  |  生成时间：2026年4月

---

## 一、核心发现摘要

基于2,627个字段的统计分析，核心结论如下：

| 结论 | 数据支撑 |
|---|---|
| **pv1是整个平台的原子层** | pv1的23个字段被271.6万个Alpha引用；每个Alpha几乎都会用到close/volume/cap等行情字段 |
| **分析师预期revision是顶级Alpha因子** | analyst4的anl4_adjusted_netincome_ft被3.4万个Alpha引用，排名全球第19 |
| **约20%的字段具有极高覆盖率（90-100%）** | 这部分字段覆盖全市场，可直接用于Universe全局选股 |
| **46%的字段被100~1000个Alpha引用** | 中等热度字段是策略差异化的主要来源 |
| **fundamental6是基本面因子的主战场** | 886个字段，涵盖资产、负债、收入等全科目 |

---

## 二、数据分层架构

BRAIN数据集按信息层级从底向上分为5层：

```
Layer 0  pv1        — 行情数据(OHLCV/市值/ADV)      <- 所有Alpha的原材料
Layer 1  fundamental6  analyst4  fundamental2  — 财务报表 + 分析师预测
Layer 2  model16     — 已排名评分（直接用于排序）
Layer 3  model51     — 系统性风险（BETA/相关性）
Layer 4  news12/18   option8/9  pv13  socialmedia12/8  — 另类数据
Layer 5  univ1       — Universe定义（选股范围边界）
```

**核心原则**：层级越高，数据越加工（已排名/已平滑）；层级越低，数据越原始（需自己做中性化/标准化）。

---

## 三、覆盖率分析（cov = 数据覆盖Universe股票比例）

覆盖率决定了字段在全市场的可用性，是样本选择偏差的关键来源。

| 覆盖率区间 | 字段数 | 占比 | 说明 |
|---|---|---|---|
| 90-100% | 511 | 19.5% | 覆盖全市场，可直接用于Universe全局选股 |
| 70-90% | 426 | 16.2% | 高覆盖率，样本偏差小，适合大部分Alpha |
| 50-70% | 1263 | 48.1% | 中等覆盖率，需注意行业/市值偏差 |
| 30-50% | 322 | 12.3% | 低覆盖率，仅适合特定行业或大中市值选股 |
| 10-30% | 94 | 3.6% | 窄覆盖，需严格限制选股范围 |
| <10% | 11 | 0.4% | 极窄覆盖，慎用，可能产生极端偏差 |

**实战建议**：在做Alpha公式时，优先选择cov>=70%的字段；若必须使用低覆盖率字段，需在universe()层面限制只在大中市值Universe内计算。

---

## 四、Alpha引用热力分析（社区验证度）

alphas字段表示有多少个社区Alpha公式引用了该字段，数值越高代表该字段在实践中被验证越有效。

### 4.1 引用数分布

| 引用数区间 | 字段数 | 占比 | 含义 |
|---|---|---|---|
| >10000 | 53 | 2.0% | 极高热度的平台基础字段，每个Alpha几乎都会用到 |
| 1000-10000 | 468 | 17.8% | 高热度字段，代表某种成熟的Alpha范式 |
| 100-1000 | 1214 | 46.2% | 中等热度，是策略差异化竞争的主战场 |
| 10-100 | 766 | 29.2% | 偏低热度，可能有特定策略用途 |
| 1-10 | 117 | 4.5% | 低热度，慎用，可能存在过拟合风险 |
| 0 | 9 | 0.3% | 无人使用，不建议引入 |

### 4.2 引用数Top30（平台最热字段）

以下字段被最多Alpha引用，代表了社区最主流的Alpha构建范式：

| 排名 | 字段名 | 数据集 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|---|---|
| 1 | **close** | `pv1` | 100% | 506,708 | close是Alpha公式中引用最多的字段（50.6万次），几乎所有基于价格数据的策略都以此为基础。 |
| 2 | **cap** | `pv1` | 100% | 391,861 | cap（市值）是规模和价值因子的核心构成，rank(-log(cap))是经典市值因子。 |
| 3 | **sector** | `pv1` | 100% | 313,023 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |
| 4 | **returns** | `pv1` | 100% | 306,753 | returns（收益率）是动量/反转策略的原材料，配合delay()构建各种周期动量。 |
| 5 | **volume** | `pv1` | 100% | 281,702 | volume（成交量）反映资金流向，rank(volume/adv20)是标准化成交量异象的经典公式。 |
| 6 | **subindustry** | `pv1` | 100% | 251,541 | subindustry（子行业）比GICS二级行业更细分，是精细化行业轮动的基础。 |
| 7 | **industry** | `pv1` | 100% | 207,718 | Industry grouping |
| 8 | **assets** | `fundamental6` | 50% | 133,897 | assets（总资产）是价值因子的核心财务科目。 |
| 9 | **market** | `pv1` | 100% | 114,455 | Market grouping |
| 10 | **adv20** | `pv1` | 100% | 96,100 | adv20（20日日均成交量）是流动性因子的基础，rank(adv20)是标准流动性代理变量。 |
| 11 | **vwap** | `pv1` | 100% | 62,753 | vwap（成交量加权均价）是执行基准，close/vwap-1衡量收盘相对均价的偏离度。 |
| 12 | **liabilities** | `fundamental6` | 50% | 54,826 | liabilities（总负债）与assets组合构建杠杆率因子。 |
| 13 | **high** | `pv1` | 100% | 53,301 | Daily high price |
| 14 | **open** | `pv1` | 100% | 50,627 | Daily open price |
| 15 | **exchange** | `pv1` | 100% | 48,609 | Exchange grouping |
| 16 | **low** | `pv1` | 100% | 46,173 | Daily low price |
| 17 | **operating_income** | `fundamental6` | 50% | 42,627 | Operating Income After Depreciation - Quarterly |
| 18 | **enterprise_value** | `fundamental6` | 50% | 37,001 | enterprise_value（企业价值=市值+净负债）是比市值更全面的公司价值度量。 |
| 19 | **anl4_adjusted_netincome_ft** | `analyst4` | 87% | 34,140 | adjusted_netincome_ft（调整后净利润预测）是分析师共识预测，revision版本是修正方向因子。 |
| 20 | **sales** | `fundamental6` | 50% | 33,902 | Sales/Turnover (Net) |
| 21 | **sharesout** | `pv1` | 100% | 28,518 | Daily outstanding shares (in millions) |
| 22 | **capex** | `fundamental6` | 50% | 26,029 | cap（市值）是规模和价值因子的核心构成，rank(-log(cap))是经典市值因子。 |
| 23 | **debt** | `fundamental6` | 50% | 26,022 | Debt |
| 24 | **equity** | `fundamental6` | 50% | 20,855 | Common/Ordinary Equity - Total |
| 25 | **country** | `pv1` | 100% | 19,343 | Country grouping |
| 26 | **ebit** | `fundamental6` | 50% | 18,992 | Earnings Before Interest and Taxes |
| 27 | **ebitda** | `fundamental6` | 50% | 18,975 | Earnings Before Interest |
| 28 | **scl12_buzz** | `socialmedia12` | 100% | 18,898 | relative sentiment volume |
| 29 | **anl4_ptp_flag** | `analyst4` | 83% | 18,154 | Pretax income - forecast type (revision/new/...) |
| 30 | **pv13_r2_min2_3000_sector** | `pv13` | 100% | 17,966 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |

### 4.3 Top字段的规律

Top50最热字段中，各数据集贡献：

- **pv1**（行情数据）：18个字段
- **fundamental6**（公司基本面）：18个字段
- **analyst4**（分析师预期）：6个字段
- **pv13**（关系数据）：3个字段
- **socialmedia12**（社交媒体情绪）：1个字段
- **news12**（新闻数据）：1个字段
- **fundamental2**（报表附注）：1个字段
- **option9**（期权希腊值）：1个字段
- **option8**（波动率数据）：1个字段

**规律**：pv1（行情数据）在Top50中占据绝对多数，说明价格/市值/成交量类字段是几乎所有Alpha的共同基础。fundamental6和analyst4的核心财务字段紧随其后，构成了价值/盈利因子的主力。

---

## 五、各数据集价值详解

### 5.1 pv1 -- 行情数据

**层级**：L0 基础层  |  **字段总数**：23  |  **Matrix**：12  **Vector**：0  **Universe**：0  |  **平均覆盖率**：100%

**核心价值**：所有Alpha的原材料，建议全量使用。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **close** | 100% | 506,708 | Daily close price |
| **cap** | 100% | 391,861 | Daily market capitalization (in millions) |
| **sector** | 100% | 313,023 | Sector grouping |
| **returns** | 100% | 306,753 | Daily returns |
| **volume** | 100% | 281,702 | Daily volume |
| **subindustry** | 100% | 251,541 | Subindustry grouping |
| **industry** | 100% | 207,718 | Industry grouping |
| **market** | 100% | 114,455 | Market grouping |

### 5.2 analyst4 -- 分析师预期

**层级**：L1 财务层  |  **字段总数**：653  |  **Matrix**：469  **Vector**：184  **Universe**：0  |  **平均覆盖率**：72%

**核心价值**：分析师预测revision是核心Alpha因子。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **anl4_adjusted_netincome_ft** | 87% | 34,140 | Adjusted net income - forecast type (revision/new/...) |
| **anl4_ptp_flag** | 83% | 18,154 | Pretax income - forecast type (revision/new/...) |
| **anl4_ebit_value** | 95% | 14,443 | Earnings before interest and taxes - announced financia |
| **anl4_ebitda_value** | 81% | 14,056 | Earnings before interest, taxes, depreciation and amort |
| **anl4_bvps_flag** | 82% | 12,242 | Book value per share - forecast type (revision/new/...) |
| **anl4_netdebt_flag** | 86% | 10,603 | Net debt - forecast type (revision/new/...) |
| **anl4_epsr_flag** | 87% | 10,471 | GAAP Earnings - estimation type (revision/new/...), per |
| **anl4_flag_erbfintax** | 82% | 9,196 | Earnings before interest and taxes - forecast type (rev |

### 5.3 fundamental6 -- 公司基本面

**层级**：L1 财务层  |  **字段总数**：886  |  **Matrix**：574  **Vector**：312  **Universe**：0  |  **平均覆盖率**：50%

**核心价值**：最常用的价值因子来源，注意财务数据滞后1~2个月。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **assets** | 50% | 133,897 | Assets - Total |
| **liabilities** | 50% | 54,826 | Liabilities - Total |
| **operating_income** | 50% | 42,627 | Operating Income After Depreciation - Quarterly |
| **enterprise_value** | 50% | 37,001 | Enterprise Value |
| **sales** | 50% | 33,902 | Sales/Turnover (Net) |
| **capex** | 50% | 26,029 | Capital Expenditures |
| **debt** | 50% | 26,022 | Debt |
| **equity** | 50% | 20,855 | Common/Ordinary Equity - Total |

### 5.4 fundamental2 -- 报表附注

**层级**：L1 财务层  |  **字段总数**：300  |  **Matrix**：300  **Vector**：0  **Universe**：0  |  **平均覆盖率**：41%

**核心价值**：附注数据覆盖率偏低，使用前务必检查cov指标。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **fn_liab_fair_val_l1_a** | 36% | 16,534 | Liabilities Fair Value, Recurring, Level 1 |
| **fn_accrued_liab_a** | 39% | 5,803 | Carrying value as of the balance sheet date of obligati |
| **fn_op_lease_rent_exp_a** | 64% | 2,335 | Rental expense for the reporting period incurred under  |
| **fn_business_acq_ppne_a** | 23% | 1,894 | Business Combination, Assumed Property, Plant and Equip |
| **fn_accum_oth_income_loss_net_of_tax_a** | 69% | 1,540 | Accumulated change in equity from transactions and othe |
| **fn_op_lease_min_pay_due_a** | 60% | 1,428 | Amount of required minimum rental payments for leases h |
| **fn_new_shares_issued_a** | 37% | 1,410 | Number of new stock issued during the period. |
| **fn_comp_options_grants_a** | 64% | 1,283 | Net number of share options (or share units) granted du |

### 5.5 model16 -- 基本面评分

**层级**：L2 评分层  |  **字段总数**：24  |  **Matrix**：24  **Vector**：0  **Universe**：0  |  **平均覆盖率**：56%

**核心价值**：已排名化，可直接用于排序，无需中性化处理。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **fscore_quality** | 30% | 1,467 | The purpose of this metric is to measure both the susta |
| **fscore_momentum** | 30% | 429 | The purpose of this metric is to identify stocks which  |
| **fscore_surface** | 30% | 427 | The static score. An index between 0 & 100 is applied f |
| **fscore_value** | 30% | 379 | The purpose of this metric is to see if the stock is un |
| **fscore_total** | 29% | 325 | The final score M-Score is a weighted average of both t |
| **fscore_profitability** | 30% | 315 | The purpose of this metric is to rank stock based on th |
| **fscore_growth** | 30% | 267 | The purpose of this metric is to qualify the expected M |
| **fscore_surface_accel** | 29% | 212 | The derivative score. In a second step, we calculate th |

### 5.6 model51 -- 风险指标

**层级**：L3 风险层  |  **字段总数**：16  |  **Matrix**：16  **Vector**：0  **Universe**：0  |  **平均覆盖率**：77%

**核心价值**：Beta用于风险归因和对冲，是组合风控的核心输入。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **unsystematic_risk_last_360_days** | 76% | 8,461 | Unsystematic Risk Last 360 Days - Relative to SPY |
| **unsystematic_risk_last_90_days** | 77% | 3,016 | Unsystematic Risk Last 90 Days - Relative to SPY |
| **unsystematic_risk_last_60_days** | 78% | 1,712 | Unsystematic Risk Last 60 Days - Relative to SPY |
| **beta_last_60_days_spy** | 78% | 1,500 | Beta to SPY in 60 Days |
| **correlation_last_60_days_spy** | 78% | 1,499 | Correlation to SPY in 60 Days |
| **systematic_risk_last_90_days** | 77% | 1,414 | Systematic Risk Last 90 Days |
| **beta_last_30_days_spy** | 78% | 1,281 | Beta to SPY in 30 Days |
| **beta_last_90_days_spy** | 78% | 1,247 | Beta to SPY in 90 Days |

### 5.7 news12 -- 新闻数据

**层级**：L4 另类层  |  **字段总数**：322  |  **Matrix**：75  **Vector**：247  **Universe**：0  |  **平均覆盖率**：80%

**核心价值**：Buzz是信息扩散代理，事件驱动Alpha的重要信号源。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **nws12_afterhsz_sl** | 71% | 16,967 | Whether a long or short position would have been more a |
| **news_mins_10_pct_dn** | 4% | 7,432 | Number of minutes that elapsed before price went down 1 |
| **news_cap** | 83% | 6,470 | Reported market capitalization for the calendar day of  |
| **news_atr14** | 89% | 3,600 | 14-day Average True Range |
| **news_eod_close** | 88% | 2,843 | Close price of the session |
| **news_pe_ratio** | 97% | 2,760 | Reported price-to-earnings ratio for the calendar day o |
| **news_atr_ratio** | 80% | 2,220 | Ratio of today's range to 20-day average true range |
| **news_mins_20_chg** | 91% | 2,141 | The minimum of L or S above for 20-minute bucket |

### 5.8 news18 -- Ravenpack情绪

**层级**：L4 另类层  |  **字段总数**：75  |  **Matrix**：61  **Vector**：14  **Universe**：0  |  **平均覆盖率**：50%

**核心价值**：NLP结构化情绪，可针对事件类型做定向分析。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **rp_css_business** | 50% | 2,984 | Composite sentiment score of business-related news |
| **rp_nip_inverstor** | 50% | 2,138 | News impact projection of investor relations news |
| **rp_ess_ratings** | 50% | 1,768 | Event sentiment score of analyst ratings-related news |
| **rp_nip_ratings** | 50% | 1,705 | News impact projection of analyst ratings-related news |
| **rp_css_ratings** | 50% | 1,692 | Composite sentiment score of analyst ratings-related ne |
| **rp_css_inverstor** | 50% | 1,655 | Composite sentiment score of investor relations news |
| **rp_css_earnings** | 50% | 1,502 | Composite sentiment score of earnings news |
| **rp_ess_partner** | 50% | 1,417 | Event sentiment score of partnership news |

### 5.9 option8 -- 波动率数据

**层级**：L4 另类层  |  **字段总数**：64  |  **Matrix**：64  **Vector**：0  **Universe**：0  |  **平均覆盖率**：70%

**核心价值**：IV-HV溢价反映市场情绪，是期权相对价值策略的核心。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **implied_volatility_call_270** | 70% | 10,534 | At-the-money option-implied volatility for call Option  |
| **implied_volatility_put_270** | 70% | 10,078 | At-the-money option-implied volatility for Put Option f |
| **implied_volatility_call_120** | 70% | 9,481 | At-the-money option-implied volatility for call Option  |
| **implied_volatility_call_1080** | 70% | 8,002 | At-the-money option-implied volatility for call option  |
| **implied_volatility_mean_10** | 69% | 6,552 | At-the-money option-implied volatility mean for 10 days |
| **implied_volatility_call_60** | 70% | 5,754 | At-the-money option-implied volatility for call Option  |
| **implied_volatility_call_180** | 70% | 5,549 | At-the-money option-implied volatility for call Option  |
| **implied_volatility_put_120** | 70% | 5,017 | At-the-money option-implied volatility for Put Option f |

### 5.10 option9 -- 期权希腊值

**层级**：L4 另类层  |  **字段总数**：74  |  **Matrix**：74  **Vector**：0  **Universe**：0  |  **平均覆盖率**：70%

**核心价值**：Greeks是期权做市和对冲策略的基础。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **pcr_oi_270** | 71% | 10,598 | Ratio of put open interest to call open interest on a s |
| **pcr_oi_180** | 71% | 2,367 | Ratio of put open interest to call open interest on a s |
| **call_breakeven_10** | 70% | 2,337 | Price at which a stock's call options with expiration 1 |
| **call_breakeven_20** | 70% | 1,627 | Price at which a stock's call options with expiration 2 |
| **pcr_oi_120** | 71% | 1,340 | Ratio of put open interest to call open interest on a s |
| **pcr_oi_10** | 71% | 1,307 | Ratio of put open interest to call open interest on a s |
| **pcr_oi_150** | 71% | 1,242 | Ratio of put open interest to call open interest on a s |
| **pcr_oi_1080** | 71% | 1,144 | Ratio of put open interest to call open interest on a s |

### 5.11 pv13 -- 关系数据

**层级**：L4 另类层  |  **字段总数**：164  |  **Matrix**：30  **Vector**：0  **Universe**：0  |  **平均覆盖率**：80%

**核心价值**：供应链数据用于传导效应和行业联动分析。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **pv13_r2_min2_3000_sector** | 100% | 17,966 | grouping fields |
| **pv13_h_min2_3000_sector** | 100% | 17,818 | grouping fields |
| **pv13_r2_min20_3000_sector** | 100% | 10,864 | grouping fields |
| **pv13_h_min2_focused_pureplay_3000_sector** | 100% | 10,461 | grouping fields |
| **rel_num_part** | 78% | 5,991 | number of the instrument's partners |
| **pv13_h_f1_sector** | 100% | 5,026 | grouping fields |
| **rel_num_all** | 99% | 3,845 | number of the companies whose product overlapped with t |
| **pv13_revere_key_sector_total** | 100% | 3,200 | Number of key focus sectors for the company |

### 5.12 socialmedia12 -- 社交媒体情绪

**层级**：L4 另类层  |  **字段总数**：18  |  **Matrix**：12  **Vector**：6  **Universe**：0  |  **平均覆盖率**：99%

**核心价值**：散户情绪指标，异常Buzz常领先价格反转。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **scl12_buzz** | 100% | 18,898 | relative sentiment volume |
| **snt_buzz** | 100% | 8,551 | negative relative sentiment volume, fill nan with 0 |
| **snt_buzz_bfl** | 100% | 5,537 | negative relative sentiment volume, fill nan with 1 |
| **scl12_buzzvec** | 100% | 4,066 | sentiment volume |
| **snt_buzz_ret** | 100% | 3,759 | negative return of relative sentiment volume |
| **scl12_sentiment** | 100% | 3,070 | sentiment |
| **snt_value** | 100% | 2,278 | negative sentiment, fill nan with 0 |
| **scl12_sentvec** | 100% | 577 | sentiment |

### 5.13 socialmedia8 -- 社媒综合得分

**层级**：L4 另类层  |  **字段总数**：2  |  **Matrix**：2  **Vector**：0  **Universe**：0  |  **平均覆盖率**：86%

**核心价值**：Z-score标准化后可直接与其他因子相加。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **snt_social_value** | 86% | 4,657 | Z score of sentiment |
| **snt_social_volume** | 86% | 4,635 | Normalized tweet volume |

### 5.14 univ1 -- Universe

**层级**：L5 定义层  |  **字段总数**：6  |  **Matrix**：0  **Vector**：0  **Universe**：6  |  **平均覆盖率**：30%

**核心价值**：只用于universe()选股范围，不参与数值计算。

| 字段名 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|
| **top3000** | 100% | 55 | No field description |
| **top500** | 17% | 30 | No field description |
| **top1000** | 33% | 8 | No field description |
| **top200** | 7% | 7 | No field description |
| **topsp500** | 22% | 3 | No field description |

---

## 六、字段命名规律与构建思路

BRAIN字段名遵循统一的前缀/后缀规范，理解这些规范可以快速推断字段含义。

| 类别 | 命名模式 | 英文名 | 含义 | 构建示例 |
|---|---|---|---|---|
| 实际值 | `actual_` | Actual | 已披露的实际财务数据 | actual_eps_value_quarterly -> 最新季度EPS实际披露值 |
| 预测值 | `_ft` / `forecast_` | Forecast | 分析师对未来财务的预测 | anl4_af_eps_value -> 分析师预测EPS实际值 |
| 修正信号 | `_revision` | Revision | 分析师预测的修正方向 | _revision_rank -> 预测上调/下调的排名，动量Alpha之核心 |
| 均值/中位数 | `_mean` / `_median` | Central Tendency | 多个估计值的集中趋势 | anl4_afv4_eps_mean -> 分析师EPS预测均值，最常用的共识预期 |
| 最高/最低 | `_high` / `_low` | Range | 估计值的乐观/悲观边界 | _high - _low -> 分析师分歧度，值越大分歧越大 |
| 标准差 | `_std` | Dispersion | 分析师预测的分歧程度 | eps_std -> 预测EPS的标准差，高std代表分析师分歧大 |
| 数量 | `_number` | Sample Size | 样本数量（分析师覆盖数等） | _number -> 覆盖该股票的分析师数量，衡量数据可靠性 |
| 同比/环比 | `_yoy` / `_mom` | Period Change | 时间维度的变化率 | sales_yoy -> 销售额同比变化率，消除季节性 |
| 动量 | `_momentum` | Momentum | 一段时间内的变化趋势 | earnings_momentum -> 盈利动量，趋势持续性优于单期变化 |
| 排名 | `_rank` | Cross-sectional Rank | Universe内百分位排名（0~1） | rank(pe_ratio) -> 市盈率排名（0~1），直接排序选股的最简方法 |
| 日均成交量 | `adv{N}` | Average Daily Volume | N日平均日成交量 | adv20 -> 20日日均成交量，最常用的流动性度量 |
| 历史波动率 | `historical_volatility_{N}` | Historical Vol | N日历史波动率 | historical_volatility_10 -> 近10天HV，期权定价基础输入 |
| 隐含波动率 | `implied_volatility_*` | Implied Vol | 由期权价格反推的未来波动率预期 | implied_volatility_call_10 -> 10天到期Call的隐含波动率 |
| 希腊值 | `_delta_` / `_gamma_` / `_vega_` | Greeks | 期权敏感性指标 | call_delta_10 -> 10天到期Call的Delta，对冲策略核心参数 |
| 社媒情绪 | `scl12_*` | Social Sentiment | 社交媒体情绪量化 | scl12_buzz -> 社媒关注度，scl12_sentiment -> 情绪方向 |
| 新闻情绪 | `nws18_*` | News Sentiment | Ravenpack NLP新闻情绪 | nws18_acb -> 公司公告类新闻情绪，NLP标准化后可直接用 |
| 市值 | `cap` | Market Cap | 总市值 = 股价 x 流通股数 | cap是规模因子的基础，rank(-log(cap))是经典市值因子 |
| 拆股标记 | `split` | Corporate Action | 拆股/并股事件标记 | split常用于过滤价格异动，拆股前后价格不连续会严重影响动量信号 |
| 行业分类 | `sector` / `subindustry` | Classification | GICS行业/子行业分类 | subindustry是最细粒度行业分组，group_neutralize(..., group=subindustry)做子行业中性化 |

---

## 七、高价值字段速查（覆盖率>=80% 且 Alpha引用>=100）

共筛选出230个高价值字段，这些字段覆盖全市场且被大量Alpha验证，是因子构建的首选原材料。

| 字段名 | 数据集 | 覆盖率 | Alpha引用 | 描述 |
|---|---|---|---|---|
| **close** | `pv1` | 100% | 506,708 | close是Alpha公式中引用最多的字段（50.6万次），几乎所有基于价格数据的策略都以此为基础。 |
| **cap** | `pv1` | 100% | 391,861 | cap（市值）是规模和价值因子的核心构成，rank(-log(cap))是经典市值因子。 |
| **sector** | `pv1` | 100% | 313,023 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |
| **returns** | `pv1` | 100% | 306,753 | returns（收益率）是动量/反转策略的原材料，配合delay()构建各种周期动量。 |
| **volume** | `pv1` | 100% | 281,702 | volume（成交量）反映资金流向，rank(volume/adv20)是标准化成交量异象的经典公式。 |
| **subindustry** | `pv1` | 100% | 251,541 | subindustry（子行业）比GICS二级行业更细分，是精细化行业轮动的基础。 |
| **industry** | `pv1` | 100% | 207,718 | Industry grouping |
| **market** | `pv1` | 100% | 114,455 | Market grouping |
| **adv20** | `pv1` | 100% | 96,100 | adv20（20日日均成交量）是流动性因子的基础，rank(adv20)是标准流动性代理变量。 |
| **vwap** | `pv1` | 100% | 62,753 | vwap（成交量加权均价）是执行基准，close/vwap-1衡量收盘相对均价的偏离度。 |
| **high** | `pv1` | 100% | 53,301 | Daily high price |
| **open** | `pv1` | 100% | 50,627 | Daily open price |
| **exchange** | `pv1` | 100% | 48,609 | Exchange grouping |
| **low** | `pv1` | 100% | 46,173 | Daily low price |
| **anl4_adjusted_netincome_ft** | `analyst4` | 87% | 34,140 | adjusted_netincome_ft（调整后净利润预测）是分析师共识预测，revision版本是修正方向因子。 |
| **sharesout** | `pv1` | 100% | 28,518 | Daily outstanding shares (in millions) |
| **country** | `pv1` | 100% | 19,343 | Country grouping |
| **scl12_buzz** | `socialmedia12` | 100% | 18,898 | relative sentiment volume |
| **anl4_ptp_flag** | `analyst4` | 83% | 18,154 | Pretax income - forecast type (revision/new/...) |
| **pv13_r2_min2_3000_sector** | `pv13` | 100% | 17,966 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |
| **pv13_h_min2_3000_sector** | `pv13` | 100% | 17,818 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |
| **split** | `pv1` | 100% | 17,343 | split（拆股标记）用于过滤价格异动，拆股前后价格不连续会产生错误的动量信号。 |
| **anl4_ebit_value** | `analyst4` | 95% | 14,443 | Earnings before interest and taxes - announced fin |
| **anl4_ebitda_value** | `analyst4` | 81% | 14,056 | Earnings before interest, taxes, depreciation and  |
| **anl4_bvps_flag** | `analyst4` | 82% | 12,242 | Book value per share - forecast type (revision/new |
| **dividend** | `pv1` | 100% | 11,137 | Dividend |
| **pv13_r2_min20_3000_sector** | `pv13` | 100% | 10,864 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |
| **anl4_netdebt_flag** | `analyst4` | 86% | 10,603 | Net debt - forecast type (revision/new/...) |
| **anl4_epsr_flag** | `analyst4` | 87% | 10,471 | GAAP Earnings - estimation type (revision/new/...) |
| **pv13_h_min2_focused_pureplay_3000_sector** | `pv13` | 100% | 10,461 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |
| **anl4_flag_erbfintax** | `analyst4` | 82% | 9,196 | Earnings before interest and taxes - forecast type |
| **anl4_totassets_flag** | `analyst4` | 81% | 9,146 | assets（总资产）是价值因子的核心财务科目。 |
| **anl4_netprofit_flag** | `analyst4` | 88% | 9,087 | Net profit - forecast type (revision/new/...) |
| **snt_buzz** | `socialmedia12` | 100% | 8,551 | negative relative sentiment volume, fill nan with  |
| **anl4_gric_flag** | `analyst4` | 90% | 7,607 | Gross income - forecast type (revision/new/...) |
| **anl4_tbve_ft** | `analyst4` | 93% | 7,133 | Tangible Book Value per Share - forecast type (rev |
| **news_cap** | `news12` | 83% | 6,470 | cap（市值）是规模和价值因子的核心构成，rank(-log(cap))是经典市值因子。 |
| **anl4_ptpr_flag** | `analyst4` | 90% | 5,716 | Reported Pretax income - forecast type (revision/n |
| **anl4_capex_flag** | `analyst4` | 85% | 5,695 | cap（市值）是规模和价值因子的核心构成，rank(-log(cap))是经典市值因子。 |
| **snt_buzz_bfl** | `socialmedia12` | 100% | 5,537 | negative relative sentiment volume, fill nan with  |
| **anl4_tot_gw_ft** | `analyst4` | 85% | 5,361 | Total Goodwill - forecast type (revision/new/...) |
| **anl4_ffo_flag** | `analyst4` | 100% | 5,163 | Funds from Operation - forecast type (revision/new |
| **anl4_fsdetailrecv4v104_item** | `analyst4` | 80% | 5,095 | Financial item |
| **pv13_h_f1_sector** | `pv13` | 100% | 5,026 | sector（行业分类）是最重要的分组变量，group_neutralize(rank(...), group=sect |
| **snt_social_value** | `socialmedia8` | 86% | 4,657 | Z score of sentiment |
| **snt_social_volume** | `socialmedia8` | 86% | 4,635 | volume（成交量）反映资金流向，rank(volume/adv20)是标准化成交量异象的经典公式。 |
| **scl12_buzzvec** | `socialmedia12` | 100% | 4,066 | sentiment volume |
| **rel_num_all** | `pv13` | 99% | 3,845 | number of the companies whose product overlapped w |
| **snt_buzz_ret** | `socialmedia12` | 100% | 3,759 | negative return of relative sentiment volume |
| **anl4_rd_exp_flag** | `analyst4` | 98% | 3,736 | Research and Development Expense - forecast type ( |

（共230个高价值字段，详见完整数据文件）
---

## 八、实战策略构建参考

基于字段分析，总结以下经过社区大量验证的Alpha构建范式：

| 策略类型 | 子类 | 参考公式 | 逻辑说明 |
|---|---|---|---|
| 规模因子 | 市值因子 | `rank(-log(cap))` | 做多小市值、做空大市值，是最经典的基本面因子之一。 |
| 价值因子 | 账面市值比 | `rank(book/cap) 或 rank(assets/cap)` | 做多低估值、做空高估值；注意用group_neutralize做行业中性化。 |
| 盈利因子 | 盈利质量 | `rank(operating_income/assets)` | 做多高盈利质量、做空低盈利质量；可与rank(equity/assets)组合。 |
| 分析师预期修正 | Revision Momentum | `anl4_adjusted_netincome_ft_revision 配合 rank()` | 分析师上调 -> 正Alpha；下调 -> 负Alpha；Revision是AQR等顶级量化基金的招牌因子。 |
| 分析师分歧度 | 预测离散度 | `anl4_*_eps_std` | 高std代表分析师分歧大，往往意味着更高的风险/机会。 |
| 流动性因子 | 成交量异常 | `rank(volume/adv20)` | 成交量异常放大往往预示短期价格动能，但反转也快，需设置止损。 |
| 波动率因子 | 低波动异象 | `rank(-historical_volatility_20)` | 低波动股票长期跑赢高波动股票（波动率诅咒），是做空波动率尾部对冲的候选。 |
| 市场Beta因子 | 系统性风险 | `rank(beta_last_30_days_spy)` | 高Beta在牛市中上行弹性大，低Beta更抗跌；可用于风险归因。 |
| 行业轮动 | 子行业动量 | `group_rank(returns, group=subindustry) - ts_rank(returns, 20)` | 行业内部做相对强弱轮动，减少市场Beta暴露。 |
| 新闻事件驱动 | Buzz异象 | `scl12_buzz - ts_mean(scl12_buzz, 20)` | 异常Buzz出现后价格往往有惯性，需快进快出；配合news_all_vwap做事件研究。 |
| 分析师覆盖数 | 信息代理 | `rank(anl4_afv4_eps_number)` | 覆盖分析师越多，信息越充分，定价效率越高；低覆盖股票往往存在更多定价偏差。 |
| 开盘跳空 | 隔夜风险 | `open/delay(close,1)-1` | 美股开盘跳空常见于财报/宏观事件后，开盘动量因子可捕捉这种规律。 |

---

## 九、使用建议总结

| 优先级 | 建议 | 代表字段 |
|---|---|---|
| 必须掌握 | pv1行情字段是所有Alpha的基础 | close, volume, cap, returns, adv20, sector |
| 高频使用 | fundamental6财务报表是价值因子的核心来源 | assets, liabilities, equity, operating_income |
| 高频使用 | analyst4分析师预期revision是顶级Alpha信号 | anl4_adjusted_netincome_ft, revision_rank |
| 重要补充 | pv13关系数据用于供应链传导策略 | primary_sector_focused_company_count |
| 重要补充 | socialmedia12情绪数据用于另类Alpha | scl12_buzz, sentiment |
| 需注意 | 使用前务必检查cov（覆盖率）；覆盖率低于50%的字段需做universe()限制 | fundamental2附注数据 |
| 需注意 | 财务数据有1~2个月披露滞后；短期Alpha建议用分析师预测数据代替 | analyst4 > fundamental6 |

---
*本分析报告由AI自动生成，基于WorldQuant BRAIN Platform抓取的2,627个字段数据。*