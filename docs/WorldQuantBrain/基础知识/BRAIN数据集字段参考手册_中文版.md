# WorldQuant BRAIN 数据集字段参考手册（中文版）

> 本手册涵盖 BRAIN 平台全部 14 个数据集、2,627 个字段的完整中文描述。
> 所有字段描述均由 Microsoft Translator 翻译，覆盖率和 Alpha 引用数来自 BRAIN 平台实时数据。
>
> 生成时间：2026-04-11 17:56

---

## 一、数据集总览

| 数据集 | 中文名 | 字段数 | 简介 |
|--------|--------|--------|------|
| analyst4 | 分析师预期 (analyst4) | 653 | 分析师对每股收益、股息、销售额等的预测与实际值 |
| fundamental2 | 财务基本面-季度 (fundamental2) | 300 | 季度财务报表数据，含资产负债表、损益表、现金流量表 |
| fundamental6 | 财务基本面-年度 (fundamental6) | 886 | 年度财务报表数据，覆盖最广的基本面指标 |
| model16 | 因子模型-排名 (model16) | 24 | 多因子排名及排名变化，含复合因子评分 |
| model51 | 因子模型-Beta (model51) | 16 | Beta 与相关性指标（相对 SPY 的 30/60/90/360 天） |
| news12 | 新闻行情 (news12) | 322 | 新闻关联的价格、成交量、波动率等行情数据 |
| news18 | 新闻情绪 (news18) | 75 | 新闻情感分析，涵盖并购、盈利、分析师等专题 |
| option8 | 期权-波动率 (option8) | 64 | 历史波动率（收盘-收盘/日内/ Parkinson等） |
| option9 | 期权-定价 (option9) | 74 | 期权盈亏平衡价、隐含波动率、Greeks等 |
| pv1 | 价格成交量 (pv1) | 23 | 核心量价数据：收盘价、市值、成交量、收益率等 |
| pv13 | 行业分组 (pv13) | 164 | 按行业/板块分组的统计指标 |
| socialmedia12 | 社交媒体-情感 (socialmedia12) | 18 | 社交媒体情感向量与成交量指标 |
| socialmedia8 | 社交媒体-情绪 (socialmedia8) | 2 | Twitter 情绪 Z 分数与标准化成交量 |
| univ1 | 股票池 (univ1) | 6 | 市值排名选股池定义（top200-top3000） |

## 二、各数据集字段详情

### 分析师预期 (analyst4)（653 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| actual_cashflow_per_share_value_quarterly | 每股现金流——季度实际价值 | Matrix | 47% | 145 |
| actual_dividend_value_quarterly | 股息——季度的实际价值 | Matrix | 61% | 37 |
| actual_eps_value_quarterly | 每股盈余（损益表/每股）（实际） | Matrix | 100% | 229 |
| actual_sales_value_annual | 销售——实际价值 | Matrix | 99% | 120 |
| actual_sales_value_quarterly | 销售额——金融服务损益表中的价值（以百万计） | Matrix | 100% | 120 |
| actuals_reporting_currency | 本国货币 | Vector | 99% | 138 |
| actuals_value_currency_code | 证券交易的货币定价 | Matrix | 100% | 332 |
| anl4_adjusted_netincome_ft | 调整后净收益 - 预测类型（修订/新/...） | Matrix | 87% | 34140 |
| anl4_ads1detailafv110_bk | 经纪人名称（int） | Vector | 69% | 169 |
| anl4_ads1detailafv110_estvalue | 估计值 | Vector | 69% | 134 |
| anl4_ads1detailafv110_person | 经纪人标识 | Vector | 69% | 753 |
| anl4_ads1detailafv110_prevval | 之前对财务项目的估算 | Vector | 69% | 117 |
| anl4_ads1detailqfv110_bk | 经纪人名称（int） | Vector | 63% | 324 |
| anl4_ads1detailqfv110_estvalue | 估计值 | Vector | 63% | 109 |
| anl4_ads1detailqfv110_person | 经纪人标识 | Vector | 63% | 269 |
| anl4_ads1detailqfv110_prevval | 之前对财务项目的估计 | Vector | 63% | 348 |
| anl4_adxqfv110_down | 较低估计的数量 | Vector | 70% | 935 |
| anl4_adxqfv110_high | 最高估计 | Vector | 70% | 49 |
| anl4_adxqfv110_low | 最低估计 | Vector | 70% | 531 |
| anl4_adxqfv110_mean | 估计的平均值 | Vector | 70% | 73 |
| anl4_adxqfv110_median | 估计的中位数 | Vector | 70% | 70 |
| anl4_adxqfv110_numest | 汇总中计入的预报数量 | Vector | 70% | 1347 |
| anl4_adxqfv110_pu | 上估数 | Vector | 70% | 4428 |
| anl4_ady_down | 较低估计的数量 | Vector | 72% | 106 |
| anl4_ady_high | 最高估计 | Vector | 72% | 68 |
| anl4_ady_low | 最低估计 | Vector | 72% | 79 |
| anl4_ady_mean | 估计的平均值 | Vector | 72% | 35 |
| anl4_ady_median | 估计的中位数 | Vector | 72% | 28 |
| anl4_ady_numest | 汇总中计入的预报数量 | Vector | 72% | 876 |
| anl4_ady_pu | 上估数 | Vector | 72% | 5374 |
| anl4_af_cfps_value | 每股现金流 - 实际价值 | Matrix | 62% | 51 |
| anl4_af_div_value | 股息——实际价值 | Matrix | 76% | 65 |
| anl4_af_eps_value | 每股收益 - 实际价值 | Matrix | 100% | 163 |
| anl4_afv4_actual | 公布的财务数据 | Vector | 92% | 59 |
| anl4_afv4_cfps_high | 每股现金流——年度预测的最高估计值 | Matrix | 68% | 35 |
| anl4_afv4_cfps_low | 每股现金流——即将到来的财年最低估计 | Matrix | 68% | 39 |
| anl4_afv4_cfps_mean | 每股现金流——年度频率估计的平均值 | Matrix | 68% | 50 |
| anl4_afv4_cfps_median | 每股现金流——年度频率预测中的中位数 | Matrix | 68% | 47 |
| anl4_afv4_cfps_number | 每股现金流——年度频率的估算次数 | Matrix | 68% | 90 |
| anl4_afv4_div_high | 每股股息——年度预测的最高估计。 | Matrix | 82% | 21 |
| anl4_afv4_div_low | 股息——年度预测的最低估计 | Matrix | 82% | 27 |
| anl4_afv4_div_mean | 每股股息——年度频率估计的平均值 | Matrix | 82% | 31 |
| anl4_afv4_div_median | 每股股息——各预测中的中位数 | Matrix | 82% | 35 |
| anl4_afv4_div_number | 每股股息估算次数 - 每年 | Matrix | 82% | 52 |
| anl4_afv4_div_std | 每股股息——估算的标准差 | Matrix | 39% | 7 |
| anl4_afv4_dts_spe | 每股收益——估计的标准差 | Matrix | 69% | 68 |
| anl4_afv4_eps_high | 每股收益——最高估计 | Matrix | 100% | 149 |
| anl4_afv4_eps_low | 每股收益——年度频率的最低估计 | Matrix | 100% | 112 |
| anl4_afv4_eps_mean | 每股收益——年度频率估计的平均值 | Matrix | 100% | 332 |
| anl4_afv4_eps_number | 每股收益——每年频率的估算次数 | Matrix | 100% | 155 |
| anl4_afv4_maxguidance | 最大导引值 | Vector | 70% | 230 |
| anl4_afv4_median_eps | 每股收益——估算的中位数 | Matrix | 100% | 109 |
| anl4_afv4_minguidance | 最小指导值 | Vector | 70% | 132 |
| anl4_bac1actualqfv110_actual | 公布的财务数据 | Vector | 65% | 91 |
| anl4_bac1actualqfv110_item | 财务项目 | Vector | 66% | 136 |
| anl4_bac1conafv110_item | 财务项目 | Vector | 73% | 149 |
| anl4_bac1conltv110_item | 财务项目 | Vector | 70% | 31 |
| anl4_bac1conqfv110_item | 财务项目 | Vector | 73% | 74 |
| anl4_bac1conrecv110_item | 财务项目 | Vector | 62% | 136 |
| anl4_bac1detailafv110_item | 财务项目 | Vector | 72% | 638 |
| anl4_bac1detaillt_item | 财务项目 | Vector | 68% | 4009 |
| anl4_bac1detailqfv110_item | 财务项目 | Vector | 69% | 168 |
| anl4_bac1detailrec_item | 财务项目 | Vector | 71% | 2810 |
| anl4_basicafv4_actual | 公布了年度财务数据。 | Vector | 92% | 17 |
| anl4_basicconafv110_down | 较低估计的数量 | Vector | 73% | 142 |
| anl4_basicconafv110_high | 最高估计 | Vector | 73% | 32 |
| anl4_basicconafv110_low | 最低估计 | Vector | 73% | 38 |
| anl4_basicconafv110_mean | 估计的平均值 | Vector | 73% | 50 |
| anl4_basicconafv110_median | 估计的中位数 | Vector | 73% | 33 |
| anl4_basicconafv110_numest | 汇总中计入的预报数量 | Vector | 73% | 650 |
| anl4_basicconafv110_pu | 上估数 | Vector | 73% | 1683 |
| anl4_basicconltv110_down | 较低估计的数量 | Vector | 70% | 90 |
| anl4_basicconltv110_high | 最高估计 | Vector | 70% | 124 |
| anl4_basicconltv110_low | 最低估计 | Vector | 70% | 48 |
| anl4_basicconltv110_mean | 估计的平均值 | Vector | 70% | 79 |
| anl4_basicconltv110_median | 估计的中位数 | Vector | 70% | 119 |
| anl4_basicconltv110_numest | 汇总中计入的预报数量 | Vector | 70% | 1609 |
| anl4_basicconltv110_pu | 上估数 | Vector | 70% | 1104 |
| anl4_basicconqfv110_down | 较低估计的数量 | Vector | 73% | 1219 |
| anl4_basicconqfv110_high | 最高估计 | Vector | 73% | 60 |
| anl4_basicconqfv110_low | 最低估计 | Vector | 73% | 50 |
| anl4_basicconqfv110_mean | 估计的平均值 | Vector | 73% | 1257 |
| anl4_basicconqfv110_median | 估计的中位数 | Vector | 73% | 87 |
| anl4_basicconqfv110_numest | 汇总中计入的预报数量 | Vector | 73% | 1335 |
| anl4_basicconqfv110_pu | 上估数 | Vector | 73% | 3458 |
| anl4_basicdetaillt_bk | 经纪人名称（int） | Vector | 68% | 59 |
| anl4_basicdetaillt_estvalue | 估计值 | Vector | 68% | 82 |
| anl4_basicdetaillt_person | 经纪人标识 | Vector | 68% | 99 |
| anl4_basicdetaillt_prevval | 之前对财务项目的估算 | Vector | 68% | 100 |
| anl4_basicdetailqfv110_bk | 经纪人名称（int） | Vector | 69% | 34 |
| anl4_basicdetailqfv110_estvalue | 估计值 | Vector | 69% | 40 |
| anl4_basicdetailqfv110_person | 经纪人标识 | Vector | 69% | 38 |
| anl4_basicdetailqfv110_prevval | 之前对财务项目的估计 | Vector | 68% | 57 |
| anl4_basicdetailrec_bk | 经纪人名称（int） | Vector | 71% | 83 |
| anl4_basicdetailrec_person | 经纪人标识 | Vector | 71% | 68 |
| anl4_basicdetailrec_ratingvalue | 给定乐器的配乐 | Vector | 71% | 476 |
| anl4_basicqfv4_actual | 公布的财务数据 | Vector | 100% | 9 |
| anl4_basicqfv4_maxguidance | 最大导引值 | Vector | 48% | 764 |
| anl4_basicqfv4_minguidance | 最小指导值 | Vector | 48% | 709 |
| anl4_baz1v110_bk | 经纪人名称（int） | Vector | 72% | 73 |
| anl4_baz1v110_estvalue | 估计值 | Vector | 72% | 64 |
| anl4_baz1v110_person | 经纪人标识 | Vector | 72% | 618 |
| anl4_baz1v110_prevval | 之前对财务项目的估计 | Vector | 71% | 33 |
| anl4_buy | 延长该乐器的建议数量 | Vector | 62% | 504 |
| anl4_bvps_flag | 每股账面价值 - 预测类型（修订/新值/...） | Matrix | 82% | 12242 |
| anl4_bvps_high | 账面价值——每股最高的估算 | Matrix | 65% | 1029 |
| anl4_bvps_low | 账面价值——每股最低估算 | Matrix | 65% | 1506 |
| anl4_bvps_mean | 每股账面价值——估算的平均值 | Matrix | 65% | 952 |
| anl4_bvps_median | 每股账面价值——预测中的中位数 | Matrix | 65% | 890 |
| anl4_bvps_number | 每股账面价值——估算次数 | Matrix | 65% | 1183 |
| anl4_bvps_value | 每股账面价值——公布的财务价值 | Matrix | 52% | 473 |
| anl4_capex_flag | 资本支出 - 预测类型（修订/新/...） | Matrix | 85% | 5695 |
| anl4_capex_high | 资本支出——最高估计 | Matrix | 62% | 8073 |
| anl4_capex_low | 资本支出——最低估计 | Matrix | 62% | 7095 |
| anl4_capex_mean | 资本支出——估算均值 | Matrix | 62% | 699 |
| anl4_capex_number | 资本支出——估算次数 | Matrix | 62% | 387 |
| anl4_capex_std | 资本支出——估算的标准差 | Matrix | 26% | 3002 |
| anl4_capex_value | 资本支出——公布的财务价值 | Matrix | 66% | 5959 |
| anl4_cff_flag | 融资活动现金流 - 预测类型（修订/新/等） | Matrix | 82% | 2449 |
| anl4_cff_high | 融资现金流——预测值中最高的 | Matrix | 59% | 2048 |
| anl4_cff_low | 融资现金流——最低估算 | Matrix | 59% | 4903 |
| anl4_cff_mean | 融资现金流——估算均值 | Matrix | 59% | 234 |
| anl4_cff_median | 融资活动现金流——预测中的中位数 | Matrix | 59% | 313 |
| anl4_cff_number | 融资现金流——估算次数 | Matrix | 59% | 476 |
| anl4_cff_value | 融资现金流——公布的财务价值 | Matrix | 48% | 550 |
| anl4_cfi_flag | 投资现金流 - 预测类型（修订/新/...） | Matrix | 83% | 1696 |
| anl4_cfi_high | 投资现金流——最高估计 | Matrix | 58% | 1421 |
| anl4_cfi_low | 投资现金流——最低估算 | Matrix | 58% | 2985 |
| anl4_cfi_mean | 投资现金流——估算平均值 | Matrix | 58% | 207 |
| anl4_cfi_median | 投资现金流——估算的中位数 | Matrix | 58% | 394 |
| anl4_cfi_number | 投资现金流——估算次数 | Matrix | 58% | 290 |
| anl4_cfi_value | 投资现金流——公布的财务价值 | Matrix | 49% | 2051 |
| anl4_cfo_flag | 运营现金流 - 预测类型（修订/新/...） | Matrix | 83% | 1997 |
| anl4_cfo_high | 运营现金流——预测中最高的价值 | Matrix | 62% | 2209 |
| anl4_cfo_low | 运营现金流——最低估计 | Matrix | 62% | 6677 |
| anl4_cfo_mean | 运营现金流——估算均值 | Matrix | 62% | 290 |
| anl4_cfo_median | 运营现金流——估计的中位数 | Matrix | 62% | 2391 |
| anl4_cfo_number | 运营现金流——估算次数 | Matrix | 62% | 926 |
| anl4_cfo_value | 运营现金流——公布的财务价值 | Matrix | 58% | 6339 |
| anl4_cuo1actualqfv110_actual | 公布的财务数据 | Vector | 63% | 527 |
| anl4_cuo1actualqfv110_item | 财务项目 | Vector | 65% | 222 |
| anl4_cuo1conafv110_item | 财务项目 | Vector | 72% | 160 |
| anl4_cuo1conqfv110_item | 财务项目 | Vector | 70% | 1049 |
| anl4_cuo1detailafv110_item | 财务项目 | Vector | 69% | 3895 |
| anl4_cuo1detailqfv110_item | 财务项目 | Vector | 63% | 2832 |
| anl4_cuo1guidaf_item | 财务项目 | Vector | 30% | 25 |
| anl4_cuo1guidaf_maxguidance | 最大导引值 | Vector | 29% | 41 |
| anl4_cuo1guidaf_minguidance | 最低指导值 | Vector | 30% | 71 |
| anl4_dei2laf_item | 财务项目 | Vector | 49% | 1169 |
| anl4_dei2lqfv110_item | 财务项目 | Vector | 43% | 2763 |
| anl4_dei3lafv110_item | 财务项目 | Vector | 54% | 731 |
| anl4_dei3lltv110_item | 财务项目 | Vector | 47% | 3931 |
| anl4_dei3lqfv110_item | 财务项目 | Vector | 51% | 403 |
| anl4_dei3lrec_item | 财务项目 | Vector | 55% | 426 |
| anl4_detailltv4_est | 长期估计值 | Vector | 100% | 6 |
| anl4_detailltv4_preest | 之前对财务项目的估计 | Vector | 100% | 5 |
| anl4_detailltv4v104_est | 估计值 | Vector | 79% | 75 |
| anl4_detailltv4v104_preest | 之前对财务项目的估计 | Vector | 79% | 71 |
| anl4_detailrecv4_est | 推荐细节的估计值 | Vector | 100% | 35 |
| anl4_detailrecv4v104_est | 估计值 | Vector | 79% | 955 |
| anl4_dez1afv4_est | 估计值 | Vector | 97% | 204 |
| anl4_dez1afv4_preest | 之前对金融项的估计 | Vector | 97% | 66 |
| anl4_dez1basicafv4_est | 估计值 | Vector | 100% | 6 |
| anl4_dez1basicafv4_preest | 之前对金融项的估计 | Vector | 100% | 3 |
| anl4_dez1basicafv4v104_est | 估计值 | Vector | 81% | 102 |
| anl4_dez1basicafv4v104_preest | 之前对财务项目的估计 | Vector | 81% | 48 |
| anl4_dez1basicqfv4_est | 估计值 | Vector | 100% | 22 |
| anl4_dez1basicqfv4_preest | 之前对金融项的估计 | Vector | 100% | 2 |
| anl4_dez1basicqfv4v104_est | 估计值 | Vector | 79% | 667 |
| anl4_dez1basicqfv4v104_preest | 之前对财务项目的估计 | Vector | 79% | 295 |
| anl4_dez1qfv4_est | 估计值 | Vector | 96% | 968 |
| anl4_dez1qfv4_preest | 之前对金融项的估计 | Vector | 96% | 512 |
| anl4_dez1safv4_est | 估计值 | Vector | 43% | 43 |
| anl4_dez1safv4_preest | 之前对金融项的估计 | Vector | 41% | 35 |
| anl4_dts_ptp | 税前收入 - 估算标准 | Matrix | 51% | 765 |
| anl4_dts_rspe | 报告每股收益——估计标准差 | Matrix | 48% | 2429 |
| anl4_eaz1laf_bk | 经纪人名称（int） | Vector | 49% | 680 |
| anl4_eaz1laf_estvalue | 估计值 | Vector | 48% | 19 |
| anl4_eaz1laf_person | 经纪人标识 | Vector | 49% | 547 |
| anl4_eaz1laf_prevval | 之前对财务项目的估计 | Vector | 48% | 35 |
| anl4_eaz1lqfv110_bk | 经纪人名称（int） | Vector | 43% | 182 |
| anl4_eaz1lqfv110_estvalue | 估计值 | Vector | 42% | 30 |
| anl4_eaz1lqfv110_person | 经纪人标识 | Vector | 43% | 235 |
| anl4_eaz1lqfv110_prevval | 之前对财务项目的估计 | Vector | 41% | 17 |
| anl4_eaz2lafv110_bk | 经纪人名称（int） | Vector | 54% | 733 |
| anl4_eaz2lafv110_estvalue | 估计值 | Vector | 53% | 41 |
| anl4_eaz2lafv110_person | 经纪人标识 | Vector | 54% | 37 |
| anl4_eaz2lafv110_prevval | 之前对财务项目的估计 | Vector | 52% | 21 |
| anl4_eaz2lltv110_bk | 经纪人名称（int） | Vector | 47% | 725 |
| anl4_eaz2lltv110_estvalue | 估计值 | Vector | 46% | 33 |
| anl4_eaz2lltv110_person | 经纪人标识 | Vector | 47% | 898 |
| anl4_eaz2lltv110_prevval | 之前对财务项目的估计 | Vector | 45% | 76 |
| anl4_eaz2lqfv110_bk | 经纪人名称（int） | Vector | 51% | 154 |
| anl4_eaz2lqfv110_estvalue | 估计值 | Vector | 50% | 136 |
| anl4_eaz2lqfv110_person | 经纪人标识 | Vector | 51% | 145 |
| anl4_eaz2lqfv110_prevval | 之前对财务项目的估计 | Vector | 49% | 151 |
| anl4_eaz2lrec_bk | 经纪人名称（int） | Vector | 55% | 426 |
| anl4_eaz2lrec_person | 经纪人标识 | Vector | 55% | 1447 |
| anl4_eaz2lrec_ratingvalue | 给定乐器的配乐 | Vector | 53% | 5396 |
| anl4_ebit_high | 息税前利润——最高估计 | Matrix | 71% | 3230 |
| anl4_ebit_low | 息税前利润——最低估算 | Matrix | 71% | 3704 |
| anl4_ebit_mean | 息税前收益——估算均值 | Matrix | 71% | 624 |
| anl4_ebit_median | 息税前收益——估算的中位数 | Matrix | 71% | 1828 |
| anl4_ebit_number | 息税前利润——估算次数 | Matrix | 71% | 2254 |
| anl4_ebit_std | 息税前利润——估计标准差 | Matrix | 47% | 1411 |
| anl4_ebit_value | 息税前利润——公布的财务价值 | Matrix | 95% | 14443 |
| anl4_ebitda_flag | 息税折旧摊销前利润 - 预测类型（修订/新/...） | Matrix | 86% | 3569 |
| anl4_ebitda_high | 扣除利息、税收、折旧和摊销前利润——最高估计 | Matrix | 58% | 4905 |
| anl4_ebitda_low | 息税折旧摊销前利润——最低估算 | Matrix | 58% | 6195 |
| anl4_ebitda_mean | 扣除利息、税收、折旧和摊销前利润——估算平均值 | Matrix | 58% | 290 |
| anl4_ebitda_number | 息税折旧摊销前利润——估算次数 | Matrix | 58% | 431 |
| anl4_ebitda_std | 扣除利息、税收、折旧和摊销前利润——估算的标准差 | Matrix | 36% | 531 |
| anl4_ebitda_value | 息税折旧摊销前利润——已公布财务价值 | Matrix | 81% | 14056 |
| anl4_epsa_flag | 每股收益调整后，剔除非常项和股票期权费用——预测类型（修订/新/等） | Matrix | 100% | 787 |
| anl4_epsr_flag | GAAP盈利——估算类型（修订/新/等），每股 | Matrix | 87% | 10471 |
| anl4_epsr_high | GAAP每股收益——最高估计 | Matrix | 72% | 2427 |
| anl4_epsr_low | GAAP每股收益——最低估计 | Matrix | 72% | 4803 |
| anl4_epsr_mean | GAAP每股收益——估算平均值 | Matrix | 72% | 991 |
| anl4_epsr_number | GAAP每股收益——估算次数 | Matrix | 72% | 3596 |
| anl4_epsr_value | GAAP每股收益——公布的财务价值 | Matrix | 99% | 1716 |
| anl4_fcf_flag | 自由现金流——预测类型（修订/新/...） | Matrix | 86% | 3355 |
| anl4_fcf_high | 自由现金流——根据估算进行汇总，最大值 | Matrix | 55% | 1050 |
| anl4_fcf_low | 自由现金流——最低估算 | Matrix | 55% | 3335 |
| anl4_fcf_mean | 自由现金流——估算的平均值 | Matrix | 55% | 243 |
| anl4_fcf_median | 自由现金流——估算汇总，第50百分位 | Matrix | 55% | 1261 |
| anl4_fcf_number | 自由现金流——估算次数 | Matrix | 55% | 394 |
| anl4_fcf_value | 自由现金流——已公布的财务价值 | Matrix | 53% | 1546 |
| anl4_fcfps_flag | 每股自由现金流——预测类型（修订/新/...） | Matrix | 89% | 1280 |
| anl4_fcfps_high | 每股自由现金流——最高估计 | Matrix | 44% | 224 |
| anl4_fcfps_low | 每股自由现金流——最低估计 | Matrix | 44% | 264 |
| anl4_fcfps_mean | 每股自由现金流——估算平均值 | Matrix | 44% | 141 |
| anl4_fcfps_median | 自由现金流——每股第50百分位估算摘要 | Matrix | 44% | 176 |
| anl4_fcfps_number | 每股自由现金流——估算次数 | Matrix | 44% | 4483 |
| anl4_ffo_flag | 运营资金 - 预测类型（修订/新/...） | Matrix | 100% | 5163 |
| anl4_flag_erbfintax | 息税前利润 - 预测类型（修订/新/...） | Matrix | 82% | 9196 |
| anl4_fsactualafv4_actual | 公布的财务数据 | Vector | 76% | 1 |
| anl4_fsactualafv4_item | 财务项目 | Vector | 79% | 2588 |
| anl4_fsactualqfv4_actual | 公布的财务数据 | Vector | 77% | 461 |
| anl4_fsactualqfv4_item | 财务项目 | Vector | 78% | 125 |
| anl4_fsdetailltv4v104_item | 财务项目 | Vector | 80% | 3385 |
| anl4_fsdetailrecv4v104_item | 财务项目 | Vector | 80% | 5095 |
| anl4_fsdtlestmtafv4_item | 财务项目 | Vector | 79% | 4097 |
| anl4_fsdtlestmtbscqv104_item | 财务项目 | Vector | 79% | 1067 |
| anl4_fsdtlestmtbscv104_item | 财务项目 | Vector | 81% | 880 |
| anl4_fsdtlestmtqfv4_item | 财务项目 | Vector | 73% | 450 |
| anl4_fsdtlestmtsafv4_item | 财务项目 | Vector | 31% | 30 |
| anl4_fsgdncbscv4_maxguidance | 最大导引值 | Vector | 32% | 1 |
| anl4_fsgdncbscv4_minguidance | 最低指导值 | Vector | 32% | 2 |
| anl4_fsguidanceafv4_item | 财务项目 | Vector | 45% | 42 |
| anl4_fsguidanceafv4_maxguidance | 最大导引值 | Vector | 45% | 2 |
| anl4_fsguidanceafv4_minguidance | 最小指导值 | Vector | 45% | 108 |
| anl4_fsguidancebasicqfv4_item | 财务项目 | Vector | 32% | 3704 |
| anl4_fsguidanceqfv4_item | 财务项目 | Vector | 31% | 2089 |
| anl4_fsguidanceqfv4_maxguidance | 最大导引值 | Vector | 31% | 4 |
| anl4_fsguidanceqfv4_minguidance | 最小指导值 | Vector | 31% | 6 |
| anl4_gric_flag | 毛收入 - 预测类型（修订/新/...） | Matrix | 90% | 7607 |
| anl4_gric_high | 毛收入——最高估计 | Matrix | 60% | 798 |
| anl4_gric_low | 毛收入——最低估计 | Matrix | 60% | 1962 |
| anl4_gric_mean | 毛收入——估算平均值 | Matrix | 60% | 620 |
| anl4_gric_median | 毛收入——估计的中位数 | Matrix | 60% | 1109 |
| anl4_gric_number | 毛收入——估算次数 | Matrix | 60% | 1274 |
| anl4_gric_std | 毛收入——估算标准 | Matrix | 41% | 2735 |
| anl4_gric_value | 总收入——已公布的财务价值 | Matrix | 70% | 2047 |
| anl4_guiafv4_est | 估计值 | Vector | 70% | 45 |
| anl4_guibasicqfv4_est | 估计值 | Vector | 48% | 2693 |
| anl4_guiqfv4_est | 估计值 | Vector | 48% | 1787 |
| anl4_hold | 关于做空或做空的建议数量不明确 | Vector | 62% | 907 |
| anl4_mark | 推荐共识评分 | Vector | 62% | 748 |
| anl4_median_capexp | 资本支出——估算的中位数 | Matrix | 62% | 441 |
| anl4_median_epsreported | 公认会计准则每股收益——估算的中位数 | Matrix | 72% | 3622 |
| anl4_medianepsbfam | 息税折旧摊销前利润——估算的中位数 | Matrix | 58% | 1000 |
| anl4_netdebt_flag | 净债务 - 预测类型（修订/新/...） | Matrix | 86% | 10603 |
| anl4_netdebt_high | 净债务——最高估计 | Matrix | 52% | 99 |
| anl4_netdebt_low | 净债务——最低估算 | Matrix | 52% | 254 |
| anl4_netdebt_mean | 净债务——估算均值 | Matrix | 52% | 415 |
| anl4_netdebt_median | 净债务——估算的中位数 | Matrix | 52% | 103 |
| anl4_netdebt_number | 净债务——估算次数 | Matrix | 52% | 222 |
| anl4_netprofit_flag | 净利润 - 预测类型（修订/新/...） | Matrix | 88% | 9087 |
| anl4_netprofit_high | 净利润——最高估计 | Matrix | 77% | 542 |
| anl4_netprofit_low | 净利润——最低估计 | Matrix | 77% | 1387 |
| anl4_netprofit_mean | 净利润——估算的平均值 | Matrix | 77% | 685 |
| anl4_netprofit_median | 净利润——估算的中位数 | Matrix | 77% | 1079 |
| anl4_netprofit_number | 净利润——估算次数 | Matrix | 77% | 6106 |
| anl4_netprofit_std | 净利润——估算的标准差 | Matrix | 60% | 216 |
| anl4_netprofit_value | 净利润——公布的财务价值 | Matrix | 100% | 1408 |
| anl4_netprofita_high | 调整后净收入——最高估计值 | Matrix | 75% | 787 |
| anl4_netprofita_low | 调整后净收入——最低估计 | Matrix | 75% | 3902 |
| anl4_netprofita_mean | 调整后净收入——均值估计 | Matrix | 75% | 911 |
| anl4_netprofita_median | 调整后净收入——估计的中位数 | Matrix | 75% | 579 |
| anl4_netprofita_number | 调整后净收益——估计次数 | Matrix | 75% | 2238 |
| anl4_netprofita_std | 调整后净收益——估计标准 | Matrix | 50% | 230 |
| anl4_netprofita_value | 调整后净收益——公布财务价值 | Matrix | 93% | 643 |
| anl4_norec | 没有推荐的经纪人数量 | Vector | 62% | 48 |
| anl4_ptp_flag | 税前收入——预测类型（修订/新/...） | Matrix | 83% | 18154 |
| anl4_ptp_high | 税前收入——最高估算 | Matrix | 73% | 2730 |
| anl4_ptp_low | 税前收入——最低估算 | Matrix | 73% | 4450 |
| anl4_ptp_mean | 税前收入——估算均值 | Matrix | 73% | 555 |
| anl4_ptp_median | 税前收入——估算的中位数 | Matrix | 73% | 541 |
| anl4_ptp_number | 税前收入——估算次数 | Matrix | 73% | 5488 |
| anl4_ptp_value | 税前收入公布的财务价值 | Matrix | 94% | 1172 |
| anl4_ptpr_flag | 报告的税前收入——预测类型（修订/新/...） | Matrix | 90% | 5716 |
| anl4_ptpr_high | 报告的税前收入——最高估算 | Matrix | 41% | 298 |
| anl4_ptpr_low | 报告的税前收入——最低估计 | Matrix | 41% | 2796 |
| anl4_ptpr_mean | 报告的税前收入——估算平均值 | Matrix | 41% | 247 |
| anl4_ptpr_median | 报告的税前收入——估算的中位数 | Matrix | 41% | 353 |
| anl4_ptpr_number | 报告的税前收入——估算次数 | Matrix | 41% | 8824 |
| anl4_qf_az_cfps_mean | 每股现金流——估算的平均值 | Matrix | 33% | 239 |
| anl4_qf_az_cfps_median | 每股现金流——各预测中的中位数 | Matrix | 33% | 100 |
| anl4_qf_az_cfps_number | 每股现金流——估算次数 | Matrix | 33% | 63 |
| anl4_qf_az_div_mean | 每股股息——估算平均值 | Matrix | 49% | 60 |
| anl4_qf_az_div_median | 每股股息——估算的中位数 | Matrix | 49% | 42 |
| anl4_qf_az_div_number | 每股股息——估算次数 | Matrix | 49% | 43 |
| anl4_qf_az_dts_spe | 每股收益——估算标准 | Matrix | 57% | 418 |
| anl4_qf_az_eps | 每股收益（EPS）——估算汇总，第50百分位 | Matrix | 78% | 467 |
| anl4_qf_az_eps_mean | 每股收益——估算平均值 | Matrix | 78% | 996 |
| anl4_qf_az_eps_number | 每股收益——估算次数 | Matrix | 78% | 8908 |
| anl4_qf_az_hgih_spe | 每股收益——最高估计 | Matrix | 78% | 541 |
| anl4_qf_az_hgih_spfc | 现金流——每股最高的估计 | Matrix | 33% | 252 |
| anl4_qf_az_hgih_vid | 每股股息——最高估算 | Matrix | 49% | 80 |
| anl4_qf_az_wol_spe | 每股收益——最低估计 | Matrix | 78% | 490 |
| anl4_qf_az_wol_spfc | 每股现金流——最低估计 | Matrix | 33% | 97 |
| anl4_qf_az_wol_vid | 每股股息——预测中最低的数值 | Matrix | 49% | 87 |
| anl4_qfd1_az_cfps_median | 每股现金流——各预测中的中位数 | Matrix | 33% | 157 |
| anl4_qfd1_az_cfps_number | 每股现金流——估算次数 | Matrix | 33% | 55 |
| anl4_qfd1_az_div_median | 每股股息——估算的中位数 | Matrix | 49% | 80 |
| anl4_qfd1_az_div_number | 每股股息——估算次数 | Matrix | 49% | 68 |
| anl4_qfd1_az_dts_spe | 每股收益——估算标准 | Matrix | 57% | 375 |
| anl4_qfd1_az_eps_number | 每股收益——估算次数 | Matrix | 78% | 5371 |
| anl4_qfd1_az_hgih_spe | 每股收益——最高估计 | Matrix | 78% | 695 |
| anl4_qfd1_az_hgih_spfc | 现金流——每股最高的估计 | Matrix | 33% | 112 |
| anl4_qfd1_az_hgih_vid | 每股股息——最高估算 | Matrix | 49% | 64 |
| anl4_qfd1_az_wol_spe | 每股收益——最低估计 | Matrix | 78% | 412 |
| anl4_qfd1_az_wol_spfc | 每股现金流——最低估计 | Matrix | 33% | 75 |
| anl4_qfd1_az_wol_vid | 每股股息——预测中最低的数值 | Matrix | 49% | 72 |
| anl4_qfd1_azeps | 每股收益（EPS）——估算汇总，第50百分位 | Matrix | 78% | 451 |
| anl4_qfv4_actual | 公布的财务数据 | Vector | 99% | 470 |
| anl4_qfv4_cfps_high | 每股现金流——季度最高估计值 | Matrix | 40% | 3 |
| anl4_qfv4_cfps_low | 每股现金流——最低估计 | Matrix | 40% | 1 |
| anl4_qfv4_cfps_mean | 每股现金流——估算的平均值 | Matrix | 40% | 4 |
| anl4_qfv4_cfps_median | 每股现金流——各预测中的中位数 | Matrix | 40% | 3 |
| anl4_qfv4_cfps_number | 每股现金流——估算次数 | Matrix | 40% | 10 |
| anl4_qfv4_div_high | 每股股息——最高估算 | Matrix | 62% | 7 |
| anl4_qfv4_div_low | 每股股息——最低估算 | Matrix | 62% | 19 |
| anl4_qfv4_div_mean | 每股股息——估算平均值 | Matrix | 62% | 10 |
| anl4_qfv4_div_median | 每股股息——估算的中位数 | Matrix | 62% | 8 |
| anl4_qfv4_div_number | 股息——估计次数 | Matrix | 62% | 19 |
| anl4_qfv4_dts_spe | 每股收益——估计的标准差 | Matrix | 72% | 84 |
| anl4_qfv4_eps_high | 每股收益——最高估计 | Matrix | 100% | 27 |
| anl4_qfv4_eps_low | 每股收益——最低估计 | Matrix | 100% | 20 |
| anl4_qfv4_eps_mean | 每股收益——估算平均值 | Matrix | 100% | 27 |
| anl4_qfv4_eps_number | 每股收益——估算次数 | Matrix | 100% | 174 |
| anl4_qfv4_maxguidance | 最大导引值 | Vector | 48% | 2954 |
| anl4_qfv4_median_eps | 每股收益——估算的中位数 | Matrix | 100% | 35 |
| anl4_qfv4_minguidance | 最小指导值 | Vector | 48% | 2461 |
| anl4_rd_exp_flag | 研发费用 - 预测类型（修订/新/...） | Matrix | 98% | 3736 |
| anl4_rd_exp_high | 研发费用——最高估算 | Matrix | 29% | 176 |
| anl4_rd_exp_low | 研发费用——最低估算 | Matrix | 29% | 3023 |
| anl4_rd_exp_mean | 研发费用——估算的平均值 | Matrix | 29% | 3121 |
| anl4_rd_exp_median | 研发费用——估算的中位数 | Matrix | 29% | 160 |
| anl4_rd_exp_number | 研发费用——估算次数 | Matrix | 29% | 203 |
| anl4_tbve_ft | 每股有形账面价值 - 预测类型（修订/新/等） | Matrix | 93% | 7133 |
| anl4_tbvps_high | 每股有形账面价值——最高估计 | Matrix | 33% | 146 |
| anl4_tbvps_low | 每股有形账面价值——最低估算 | Matrix | 33% | 294 |
| anl4_tbvps_mean | 每股有形账面价值——估算平均值 | Matrix | 33% | 256 |
| anl4_tbvps_median | 每股有形账面价值——估算的中位数 | Matrix | 33% | 130 |
| anl4_tbvps_number | 每股有形账面价值——估算次数 | Matrix | 33% | 1419 |
| anl4_tot_gw_ft | 总商誉 - 预测类型（修订/新/...） | Matrix | 85% | 5361 |
| anl4_total_rec | 推荐总数 | Vector | 62% | 2462 |
| anl4_totassets_flag | 总资产 - 预测类型（修订/新/...） | Matrix | 81% | 9146 |
| anl4_totassets_high | 总资产——最高估计 | Matrix | 72% | 688 |
| anl4_totassets_low | 总资产——最低估算 | Matrix | 72% | 2247 |
| anl4_totassets_mean | 总资产——估算均值 | Matrix | 72% | 465 |
| anl4_totassets_median | 总资产——估算的中位数 | Matrix | 72% | 430 |
| anl4_totassets_number | 总资产——估算次数 | Matrix | 72% | 5227 |
| anl4_totassets_std | 总资产——估算的标准差 | Matrix | 32% | 1030 |
| anl4_totassets_value | 总资产——实际价值 | Matrix | 65% | 1225 |
| anl4_totgw_high | 总商誉——最高估计 | Matrix | 54% | 140 |
| anl4_totgw_low | 总好感度——最低估计 | Matrix | 54% | 165 |
| anl4_totgw_mean | 总商誉——估算均值 | Matrix | 54% | 217 |
| anl4_totgw_median | 总善意度——估算的中位数 | Matrix | 54% | 135 |
| anl4_totgw_number | 总商誉——估算次数 | Matrix | 54% | 223 |
| anl4_under | 体重过轻推荐数量 | Vector | 62% | 102 |
| basic_shares_max_guidance_qtr | 基础股的最高指导值。 | Matrix | 100% | 36 |
| book_value_per_share_2 | 每股账面价值 - 实际价值 | Matrix | 75% | 36 |
| book_value_per_share_min_guidance_qtr | 每股账面价值——最低指导价值 | Matrix | 100% | 19 |
| book_value_per_share_reported_value | 每股账面价值 - 实际价值 | Matrix | 52% | 80 |
| capital_expenditure_amount | 资本支出——总价值 | Matrix | 75% | 16 |
| capital_expenditure_guidance_value | 资本支出——年度指导的总价值 | Matrix | 36% | 7 |
| capital_expenditure_max_guidance_qtr | 资本支出的最高指导值 | Matrix | 100% | 15 |
| capital_expenditure_reported_value | 资本支出 - 总额（现金流/投资）（数百万） | Matrix | 66% | 25 |
| cash_flow_financing_max_guidance | 融资现金流——每年提供的最高指导价值 | Matrix | 100% | 37 |
| cash_flow_from_financing | 融资现金流——价值 | Matrix | 64% | 35 |
| cash_flow_from_investing | 投资现金流——价值 | Matrix | 65% | 55 |
| cash_flow_from_operations | 运营现金流——年度价值 | Matrix | 71% | 138 |
| cash_flow_operations_min_guidance | 年度运营现金流的最低指导值。 | Matrix | 100% | 6 |
| cashflow_per_share_average | 每股现金流——估计平均值，延迟1季度 | Matrix | 40% | 19 |
| cashflow_per_share_estimate_count | 每股现金流 - 估算次数 - delay1 | Matrix | 40% | 17 |
| cashflow_per_share_max_guidance | 每股现金流的年度最高指导值。 | Matrix | 100% | 5 |
| cashflow_per_share_max_guidance_quarterly | 每股现金流的最大指引值。 | Matrix | 100% | 20 |
| cashflow_per_share_maximum | 现金流——每股最高的估算，延迟1季度 | Matrix | 40% | 6 |
| cashflow_per_share_median_value | 每股现金流——各预测中的中位数 | Matrix | 40% | 5 |
| cashflow_per_share_min_guidance | 每股现金流——年度最低指导值 | Matrix | 100% | 15 |
| cashflow_per_share_min_guidance_quarterly | 每股现金流的最低指导值 | Matrix | 100% | 23 |
| cashflow_per_share_minimum | 每股现金流——最低估计，延迟1季度 | Matrix | 40% | 4 |
| dividend_estimate_average | 每股股息——估算平均值——延迟1 | Matrix | 62% | 5 |
| dividend_estimate_count | 每股股息——预计预估次数，延迟1季度 | Matrix | 62% | 15 |
| dividend_estimate_maximum | 每股股息——预测中延迟1个季度的最高值 | Matrix | 62% | 6 |
| dividend_estimate_median_value | 每股股息——估算的中位数 | Matrix | 62% | 8 |
| dividend_estimate_minimum | 每股股息——预测中最低的值——D1 | Matrix | 62% | 11 |
| dividend_estimate_standard_deviation | 每股股息——估算的标准差 | Matrix | 27% | 4 |
| dividend_estimate_stddev_quarterly | 每股股息——估算的标准差 | Matrix | 27% | 1 |
| dividend_estimate_value | 每股股息——估算价值 | Vector | 47% | 0 |
| dividend_max_guidance_quarterly | 每股股息的最高指导值 | Matrix | 100% | 55 |
| dividend_max_guidance_value | 每股股息的年度最高指导值。 | Matrix | 100% | 73 |
| dividend_min_guidance_quarterly | 每股股息的最低指导值 | Matrix | 100% | 51 |
| dividend_min_guidance_value | 每股年度股息的最低指导值 | Matrix | 100% | 40 |
| dividend_previous_estimate_value | 之前对股息的估计 | Vector | 46% | 0 |
| earnings_per_share_average | 每股收益——估算平均值 | Matrix | 100% | 93 |
| earnings_per_share_estimate_count | 每股收益——估算次数 | Matrix | 100% | 183 |
| earnings_per_share_guidance_value | 每股收益——年度频率的指导值 | Matrix | 36% | 41 |
| earnings_per_share_max_guidance | 每股收益的年度最高指导值。 | Matrix | 100% | 27 |
| earnings_per_share_maximum | 每股收益——最高估计 | Matrix | 100% | 28 |
| earnings_per_share_median_value | 每股收益——估算的中位数 | Matrix | 100% | 38 |
| earnings_per_share_min_guidance | 每股收益的年度最低指导值。 | Matrix | 100% | 19 |
| earnings_per_share_minimum | 每股收益——最低估计 | Matrix | 100% | 17 |
| earnings_per_share_nongaap_value | 非GAAP每股收益 - 实际价值 | Matrix | 80% | 31 |
| earnings_per_share_reported | 每股报告收益 - 实际价值 | Matrix | 96% | 66 |
| earnings_per_share_reported_value | 每股报告收益 - 实际价值 | Matrix | 99% | 88 |
| earnings_per_share_standard_deviation | 每股收益——估计的标准差 | Matrix | 72% | 114 |
| ebit_reported_value | 息税前利润——季度实际价值 | Matrix | 95% | 80 |
| ebitda_reported_value | 季度的EBITDA值。 | Matrix | 81% | 95 |
| eps_adjusted_min_guidance_qtr | 调整后每股收益的最低指导值，不包括非常规项目和股票期权费用。 | Matrix | 100% | 22 |
| eps_adjusted_min_guidance_value | 调整后每股收益（不含非常规项目和股票期权费用）的最低指导值。 | Matrix | 100% | 14 |
| eps_estimate_value | 每股收益 - 估算价值 | Vector | 99% | 28 |
| eps_guidance_value_quarterly | 每股收益 - 基本价值 | Matrix | 30% | 17 |
| eps_max_guidance_quarterly | 每股收益的最高指导值。 | Matrix | 100% | 52 |
| eps_min_guidance_quarterly | 每股收益的最低指导值 | Matrix | 100% | 27 |
| eps_previous_estimate_value | 此前对每股收益的估计 | Vector | 99% | 15 |
| eps_reported_min_guidance_qtr | 报告每股收益 - 最低指导值 | Matrix | 100% | 11 |
| est_bookvalue_ps | 每股账面价值——估算的平均值 | Matrix | 68% | 1294 |
| est_capex | 资本支出——估算均值 | Matrix | 64% | 4760 |
| est_cashflow_fin | 融资现金流——估算均值 | Matrix | 62% | 795 |
| est_cashflow_invst | 投资现金流——估算平均值 | Matrix | 62% | 605 |
| est_cashflow_op | 运营现金流——估算均值 | Matrix | 65% | 1649 |
| est_cashflow_ps | 每股现金流——估算的平均值 | Matrix | 33% | 268 |
| est_dividend_ps | 每股股息——估算平均值 | Matrix | 49% | 346 |
| est_ebit | 息税前收益——估算均值 | Matrix | 73% | 1772 |
| est_ebitda | 息税折旧摊销前利润——估算平均值 | Matrix | 60% | 1759 |
| est_eps | 每股收益——估算平均值 | Matrix | 78% | 4559 |
| est_epsa | 每股收益调整后，剔除非常规项目和股票期权费用——估算平均值 | Matrix | 16% | 1297 |
| est_epsr | GAAP每股收益——估算平均值 | Matrix | 74% | 2571 |
| est_fcf | 自由现金流——估算均值 | Matrix | 58% | 689 |
| est_fcf_ps | 每股自由现金流——估算平均值 | Matrix | 46% | 227 |
| est_ffo | 运营资金——估算摘要，均值 | Matrix | 4% | 41 |
| est_grossincome | 毛收入——估算均值 | Matrix | 62% | 1165 |
| est_netdebt | 净债务——估算均值 | Matrix | 54% | 278 |
| est_netprofit | 净利润——估算的平均值 | Matrix | 79% | 2095 |
| est_netprofit_adj | 调整后净收入——估计均值 | Matrix | 77% | 1228 |
| est_ptp | 税前收入——估算均值 | Matrix | 75% | 1285 |
| est_ptpr | 报告的税前收入——估算均值 | Matrix | 44% | 509 |
| est_rd_expense | 研发费用——估算的平均值 | Matrix | 31% | 4571 |
| est_sales | 销售——估算的平均值 | Matrix | 75% | 2529 |
| est_sga | SGA - 估计均值 | Matrix | 51% | 447 |
| est_shequity | SH股权部分均值——估算均值 | Matrix | 76% | 1120 |
| est_tbv_ps | 每股有形账面价值——估算平均值 | Matrix | 35% | 191 |
| est_tot_assets | 总资产——估算均值 | Matrix | 75% | 1167 |
| est_tot_goodwill | 总商誉——估算均值 | Matrix | 57% | 446 |
| estimate_value_currency_code | 本国货币 | Vector | 100% | 17 |
| estimate_value_currency_code_detail_qtr | 本国货币 | Vector | 96% | 67 |
| estimate_value_currency_code_qtr | 本国货币 | Vector | 100% | 50 |
| financing_cashflow_reported_value | 融资现金流——价值 | Matrix | 48% | 76 |
| free_cash_flow_per_share | 每股自由现金流——年度期的实际财务价值 | Matrix | 49% | 53 |
| free_cash_flow_per_share_actual_value | 每股自由现金流——公布的财务价值 | Matrix | 35% | 13 |
| free_cash_flow_per_share_max_guidance | 每股自由现金流的年度最高指导值。 | Matrix | 100% | 48 |
| free_cash_flow_per_share_reported_value | 每股自由现金流——公布的财务价值 | Matrix | 35% | 15 |
| free_cash_flow_reported_value | 季度自由现金流价值。 | Matrix | 53% | 46 |
| free_cash_flow_total | 自由现金流价值 - 年度 | Matrix | 68% | 83 |
| funds_from_operations_max_guidance | 运营基金的最高指导值——年度 | Matrix | 100% | 37 |
| goodwill_min_guidance_qtr | 总商誉的最低指导值 | Matrix | 100% | 16 |
| gross_income_reported_value | 季度总收入值 | Matrix | 70% | 85 |
| gross_income_total | 按年计算的总收入价值 | Matrix | 70% | 21 |
| guidance_estimate_value | 基本年度财务指导的估算价值 | Vector | 58% | 153 |
| guidance_previous_estimate_value_qtr | 之前对金融项的估计 | Vector | — | 0 |
| guidance_reporting_currency | 证券交易的货币定价 - 年度 | Matrix | 100% | 51 |
| guidance_value_currency_code_qtr | 本国货币 | Vector | 48% | 14 |
| highest_sales_estimate | 销售额——年度期间的最高估计 | Matrix | 100% | 23 |
| investing_cashflow_reported_value | 投资现金流——价值 | Matrix | 49% | 27 |
| lowest_sales_estimate | 销售额——年度最低估算 | Matrix | 100% | 32 |
| max_adjusted_eps_guidance | 调整后每股收益的最大指导值。 | Matrix | 100% | 39 |
| max_adjusted_eps_guidance_2 | 调整后每股收益的年度最高指导值。 | Matrix | 100% | 14 |
| max_adjusted_funds_from_operations_adj_guidance | 运营调整后的资金——最大指导值 | Matrix | 100% | 27 |
| max_adjusted_funds_from_operations_guidance | 运营起资金的最大指导值 | Matrix | 100% | 10 |
| max_adjusted_funds_from_operations_guidance_2 | 经运营调整后的资金——年度期内最大指导值 | Matrix | 100% | 8 |
| max_adjusted_net_income_guidance | 调整后净收入的最大指导值。 | Matrix | 100% | 466 |
| max_adjusted_net_profit_guidance | 调整后净利润的年度最高指导值。 | Matrix | 100% | 12 |
| max_book_value_per_share_guidance | 每股账面价值——预测中的最大值 | Matrix | 100% | 16 |
| max_book_value_per_share_guidance_2 | 每股账面价值——年度期内最大指导值 | Matrix | 100% | 26 |
| max_capital_expenditure_guidance | 资本支出的年度最高指导值。 | Matrix | 100% | 21 |
| max_custom_eps_guidance | 定制每股收益——最高指导值 | Matrix | 100% | 34 |
| max_customized_eps_guidance | 每年定制每股收益的最高指导值。 | Matrix | 100% | 16 |
| max_ebit_guidance | 利息和税前利润（EBIT）的年度最高指导值。 | Matrix | 100% | 25 |
| max_ebitda_guidance | 利息、税扣折旧和摊销前利润（EBITDA）的年度最高指导值。 | Matrix | 100% | 8 |
| max_financing_cashflow_guidance | 融资现金流——最大指导值 | Matrix | 100% | 23 |
| max_free_cash_flow_guidance | 自由现金流的年度最大指导值。 | Matrix | 100% | 26 |
| max_free_cashflow_guidance | 自由现金流的最高指导值。 | Matrix | 100% | 46 |
| max_free_cashflow_per_share_guidance | 每股自由现金流的最大指导值。 | Matrix | 100% | 35 |
| max_gross_income_guidance | 毛收入的最高指导值。 | Matrix | 100% | 26 |
| max_gross_income_guidance_2 | 年度总收入的最高指导值。 | Matrix | 100% | 15 |
| max_investing_cashflow_guidance | 投资现金流的最大指导值。 | Matrix | 100% | 32 |
| max_investing_cashflow_guidance_2 | 投资活动现金流的年度最高指导值。 | Matrix | 100% | 29 |
| max_net_debt_guidance | 年度净债务的最高指导值。 | Matrix | 100% | 42 |
| max_net_income_guidance | 净利润的最大指导值。 | Matrix | 100% | 29 |
| max_net_profit_guidance | 每年净利润的最高指导值。 | Matrix | 100% | 27 |
| max_operating_cashflow_guidance | 运营现金流的最大指导值。 | Matrix | 100% | 28 |
| max_operating_cashflow_guidance_2 | 年度运营现金流的最高指导值。 | Matrix | 100% | 18 |
| max_pretax_profit_guidance | 税前收入的年度最高指导值。 | Matrix | 100% | 10 |
| max_reported_eps_guidance | 报告每股收益——最大指引值 | Matrix | 100% | 18 |
| max_reported_eps_guidance_2 | 报告每股收益——年度期内最高指引值 | Matrix | 100% | 13 |
| max_reported_pretax_income_guidance | 报告的税前收入——最大指导值 | Matrix | 100% | 21 |
| max_reported_pretax_income_guidance_2 | 报告的税前收入——最大指导值 | Matrix | 100% | 75 |
| max_research_development_expense_guidance | 研发费用的最高指导值。 | Matrix | 100% | 34 |
| max_selling_general_admin_guidance | 销售、一般及行政费用的最高指导值 | Matrix | 100% | 33 |
| max_share_buyback_guidance | 股票最高指引值 基本 - 年度 | Matrix | 100% | 16 |
| max_shareholders_equity_guidance | 股东权益总额的最高指导值。 | Matrix | 100% | 66 |
| max_shares_outstanding_guidance | 股份的最高指导标准 | Matrix | 100% | 29 |
| max_stock_option_expense_guidance | 股票期权费用——年度期内最大指导值 | Matrix | 100% | 31 |
| max_tangible_book_value_per_share_guidance | 每股有形账面价值——最大指导价值 | Matrix | 100% | 15 |
| max_total_assets_guidance | 总资产的最高指导值。 | Matrix | 100% | 59 |
| max_total_assets_guidance_2 | 总资产的最大指导值 | Matrix | 100% | 62 |
| max_total_goodwill_guidance | 《全面商誉》的最大指导值。 | Matrix | 100% | 31 |
| max_total_goodwill_guidance_2 | 年度总商誉的最高指导值。 | Matrix | 100% | 24 |
| maximum_guidance_value | 基本年度财务报表的最高指导值 | Vector | 58% | 71 |
| median_sales_estimate | 销售额——估算的中位数 | Matrix | 100% | 34 |
| min_adjusted_funds_from_operations_adj_guidance | 调整后基金运营起的最低指导值 | Matrix | 100% | 20 |
| min_adjusted_funds_from_operations_guidance | 运营资金 - 最低指导值 | Matrix | 100% | 21 |
| min_adjusted_funds_from_operations_guidance_2 | 运营调整后的资金——年度最低指导 | Matrix | 100% | 19 |
| min_adjusted_net_income_guidance | 调整后净收益——最低指导值 | Matrix | 100% | 892 |
| min_basic_shares_guidance | 股票基础——最低指导值 | Matrix | 100% | 32 |
| min_book_value_per_share_guidance | 每股账面价值——年度期的最低指导值 | Matrix | 100% | 27 |
| min_capex_guidance | 资本支出的最低指导值 | Matrix | 100% | 8 |
| min_capital_expenditure_guidance | 资本支出的最低指导值 | Matrix | 100% | 5 |
| min_custom_eps_guidance | 定制每股收益 - 最低指导值 | Matrix | 100% | 15 |
| min_customized_eps_guidance | 定制每股收益——年度最低指导值 | Matrix | 100% | 16 |
| min_ebit_guidance | 息税前利润（EBIT）的最低指导值 | Matrix | 100% | 34 |
| min_ebit_guidance_2 | 利息税前利润（EBIT）的年度最低指导值。 | Matrix | 100% | 16 |
| min_ebitda_guidance | 息税折旧摊销前利润（EBITDA）的最低指导值 - 年度 | Matrix | 100% | 23 |
| min_financing_cashflow_guidance | 融资现金流的最低指导值 | Matrix | 100% | 13 |
| min_financing_cashflow_guidance_2 | 年度融资现金流的最低指导值 | Matrix | 100% | 18 |
| min_free_cash_flow_guidance | 自由现金流的年度最低指导值。 | Matrix | 100% | 15 |
| min_free_cash_flow_per_share_guidance | 每股自由现金流——年度期的最低指导值 | Matrix | 100% | 28 |
| min_free_cashflow_guidance | 自由现金流的最低指导值 | Matrix | 100% | 24 |
| min_free_cashflow_per_share_guidance | 每股自由现金流——最低指导值 | Matrix | 100% | 27 |
| min_funds_from_operations_guidance | 运营资金——年度最低指导值 | Matrix | 100% | 18 |
| min_gross_income_guidance | 毛收入的最低指导值。 | Matrix | 100% | 16 |
| min_gross_income_guidance_2 | 年度毛收入的最低指导标准。 | Matrix | 100% | 18 |
| min_investing_cashflow_guidance | 投资现金流——最低指导值 | Matrix | 100% | 33 |
| min_investing_cashflow_guidance_2 | 投资现金流——年度最低指导值 | Matrix | 100% | 32 |
| min_net_debt_guidance | 净债务的最低指导值为年度。 | Matrix | 100% | 43 |
| min_net_income_guidance | 净利润——最低指导值 | Matrix | 100% | 42 |
| min_net_profit_guidance | 年度净利润的最低指导值 | Matrix | 100% | 28 |
| min_operating_cashflow_guidance | 运营现金流的最低指导值 | Matrix | 100% | 25 |
| min_pretax_profit_guidance | 税前收入的最低指导值 | Matrix | 100% | 22 |
| min_pretax_profit_guidance_2 | 税前收入的年度最低指导值。 | Matrix | 100% | 42 |
| min_reported_eps_guidance | 报告每股收益——年度期的最低指导值 | Matrix | 100% | 10 |
| min_research_development_expense_guidance | 研发费用的最低指导值 | Matrix | 100% | 15 |
| min_research_development_expense_guidance_2 | 年度研发费用的最低指导值 | Matrix | 100% | 17 |
| min_sg_and_a_expense_guidance | 销售、一般及行政费用——最低指导值 | Matrix | 100% | 17 |
| min_share_buyback_guidance | 股票基础——年度最低指导值 | Matrix | 100% | 34 |
| min_share_count_guidance | 年度股票的最低指导标准 | Matrix | 100% | 17 |
| min_shareholders_equity_guidance | 股东权益的最低指导值 | Matrix | 100% | 25 |
| min_shares_outstanding_guidance | 股份的最低指导值 | Matrix | 100% | 19 |
| min_stock_option_expense_guidance | 股票期权费用——最低指导值 | Matrix | 100% | 47 |
| min_stock_option_expense_guidance_2 | 股票期权费用的年度最低指导值 | Matrix | 100% | 18 |
| min_tangible_book_value_per_share_guidance | 每股有形账面价值——最低指导价值 | Matrix | 100% | 24 |
| min_tangible_book_value_per_share_guidance_2 | 每股有形账面价值——最低指导价值 | Matrix | 100% | 28 |
| min_total_assets_guidance | 总资产的最低指导值 | Matrix | 100% | 15 |
| min_total_assets_guidance_2 | 总资产的年度最低指导值 | Matrix | 100% | 19 |
| min_total_goodwill_guidance | 总商誉——最低的指导值 | Matrix | 100% | 22 |
| minimum_guidance_value | 基本年度财务报表的最低指导值 | Vector | 58% | 27 |
| net_debt_actual_value | 净债务——公布的财务价值 | Matrix | 39% | 18 |
| net_debt_amount | 净负债——年度实际价值 | Matrix | 68% | 51 |
| net_debt_max_guidance_qtr | 净债务的最高指导值 | Matrix | 100% | 32 |
| net_debt_min_guidance_qtr | 净债务的最低指导值 | Matrix | 100% | 36 |
| net_debt_reported_value | 季度净债务值 | Matrix | 39% | 24 |
| net_income_adjusted | 调整后的净收益——年度频率的已公布财务价值 | Matrix | 91% | 189 |
| net_income_total_2 | 年度数据的净利润——公布财务价值 | Matrix | 97% | 42 |
| net_profit_adjusted_min_guidance | 调整后净利润的最低指导值。 | Matrix | 100% | 10 |
| net_profit_adjusted_value | 调整后净收益——公布财务价值 | Matrix | 93% | 52 |
| net_profit_reported_value | 净利润——公布的财务价值 | Matrix | 100% | 27 |
| operating_cashflow_reported_value | 运营现金流 - 价值 | Matrix | 58% | 101 |
| operating_profit_before_depr_amort | EBITDA值 - 年度 | Matrix | 83% | 9 |
| operating_profit_before_depr_amort_max_guidance_qtr | 息税折旧摊销前利润的最高指导值 | Matrix | 100% | 128 |
| operating_profit_before_depr_amort_min_guidance_qtr | 息税折旧摊销前利润的最低指导值 | Matrix | 100% | 102 |
| operating_profit_before_interest_tax | 息税前利润（EBIT）- 实际价值 | Matrix | 93% | 22 |
| operating_profit_max_guidance_qtr | 利息和税前收益的最高指导值。 | Matrix | 100% | 77 |
| pretax_income_actual_reported_value | 税前收入报告的已公布财务价值 | Matrix | 42% | 7 |
| pretax_income_max_guidance_qtr | 税前收入的最高指导值。 | Matrix | 100% | 30 |
| pretax_income_reported | 报告的税前收入——年度财政期的实际价值 | Matrix | 56% | 12 |
| pretax_income_reported_min_guidance | 报告的税前收入——最低指导值 | Matrix | 100% | 34 |
| pretax_income_reported_min_guidance_qtr | 报告的税前收入——最低指导值 | Matrix | 100% | 12 |
| pretax_income_reported_value | 报告的税前收入——季度的实际价值 | Matrix | 42% | 12 |
| pretax_income_standalone_value | 税前利润——季度的实际价值 | Matrix | 94% | 83 |
| pretax_income_total | 税前利润——年度期间的价值 | Matrix | 94% | 23 |
| previous_guidance_estimate | 之前对财务项目的估计——年度频率 | Vector | — | 0 |
| previous_guidance_value_annual | 之前对金融项的估计 | Vector | — | 0 |
| previous_quarterly_guidance_estimate | 之前对金融项的估计 | Vector | — | 0 |
| previous_recommendation_value | 之前对财务项目的估算 | Vector | — | 0 |
| reporting_currency_code_9 | 本国货币 | Matrix | 100% | 341 |
| research_development_expense | 研发费用 - 实际价值（年度） | Matrix | 38% | 34 |
| research_development_expense_actual_value | 研发费用——公布的财务价值 | Matrix | 38% | 13 |
| research_development_expense_reported_value | 研发（损益表）价值（以百万计） | Matrix | 38% | 22 |
| research_development_max_guidance | 每年研发费用的最高指导值。 | Matrix | 100% | 21 |
| sales_estimate_average | 销售——估算平均值，延迟1季度 | Matrix | 100% | 40 |
| sales_estimate_average_annual | 销售——估算的平均值 | Matrix | 100% | 35 |
| sales_estimate_average_quarterly | 销售——估算的平均值 | Matrix | 100% | 28 |
| sales_estimate_count | 销售——估算次数 | Matrix | 100% | 587 |
| sales_estimate_count_2 | 销售估算数量 | Matrix | 100% | 73 |
| sales_estimate_count_quarterly | 销售——估算次数 | Matrix | 100% | 567 |
| sales_estimate_dispersion | 年度销售估算的标准差。 | Matrix | 68% | 20 |
| sales_estimate_maximum | 销售——最高估算 | Matrix | 100% | 36 |
| sales_estimate_maximum_quarterly | 销售——最高估算 | Matrix | 100% | 21 |
| sales_estimate_median_quarterly | 销售额——估算的中位数 | Matrix | 100% | 23 |
| sales_estimate_median_value | 销售——预测中的中位数 | Matrix | 100% | 33 |
| sales_estimate_minimum | 销售——最低估算 | Matrix | 100% | 24 |
| sales_estimate_minimum_quarterly | 销售——最低估算 | Matrix | 100% | 24 |
| sales_estimate_standard_deviation | 销售——估计的标准差 | Matrix | 73% | 243 |
| sales_estimate_stddev_quarterly | 销售估算的标准差 | Matrix | 73% | 323 |
| sales_estimate_value | 销售额 - 估算价值 | Vector | 99% | 17 |
| sales_guidance_value | 销售——年度期的指导值 | Matrix | 43% | 63 |
| sales_guidance_value_quarterly | 销售——指导价值 | Matrix | 33% | 34 |
| sales_max_guidance_quarterly | 销售的最高指导值。 | Matrix | 100% | 189 |
| sales_max_guidance_value | 年度销售额的最高指导值 | Matrix | 100% | 27 |
| sales_min_guidance_quarterly | 销售的最低指导值 | Matrix | 100% | 201 |
| sales_min_guidance_value | 年度最低销售指导。 | Matrix | 100% | 11 |
| sales_previous_estimate_value | 之前对销售额的估计 | Vector | 99% | 2 |
| selling_general_admin_expense | 销售、一般及行政费用价值 | Matrix | 63% | 20 |
| selling_general_admin_expense_actual_value | 销售、一般及行政费用——实际价值 | Matrix | 62% | 29 |
| selling_general_admin_expense_max_guidance_qtr | 销售、一般及行政费用——最高指导价值 | Matrix | 100% | 30 |
| selling_general_admin_expense_reported_value | 销售、一般及行政费用价值 | Matrix | 62% | 43 |
| sg_and_admin_min_guidance_value | 销售、一般及行政费用的年度最低指导值。 | Matrix | 100% | 36 |
| shareholders_equity_actual_value | 股东权益——总价值 | Matrix | 70% | 48 |
| shareholders_equity_max_guidance | 股东权益的年度最高指导值。 | Matrix | 100% | 16 |
| shareholders_equity_min_guidance | 股权的最低指导值 | Matrix | 100% | 31 |
| shareholders_equity_reported_value | 股东权益——总价值 | Matrix | 70% | 44 |
| shareholders_equity_total_2 | 股东权益——总价值 | Matrix | 85% | 19 |
| shares_outstanding_max_guidance | 股份的最高指导值 | Matrix | 100% | 65 |
| stock_option_expense_max_guidance_qtr | 股票期权费用——最大指导值 | Matrix | 100% | 26 |
| tangible_book_value_per_share_max_guidance | 每股有形账面价值——最大指导价值 | Matrix | 100% | 42 |
| total_assets_amount | 总资产——实际价值 | Matrix | 80% | 63 |
| total_assets_reported_value | 总资产——实际价值 | Matrix | 65% | 112 |
| total_goodwill_actual_value | 总商誉——公布的财务价值 | Matrix | 38% | 53 |
| total_goodwill_amount | 总商誉 - 价值 | Matrix | 53% | 18 |
| total_goodwill_reported_value | 总商誉——以数百万计的实际价值 | Matrix | 38% | 27 |

### 财务基本面-季度 (fundamental2)（300 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| fn_accrued_liab_a | 截至资产负债表日期的已发生和应付债务的账面价值，涉及法定性质、合同义务产生的费用，或随着时间累积且尚未收到发票或将不会开具的费用。 | Matrix | 39% | 5803 |
| fn_accrued_liab_curr_a | 截至资产负债表日期的已发生和应付债务的账面价值，涉及法定性质、合同义务产生的费用，或随着时间累积且尚未收到发票或将不会开具的费用。 | Matrix | 36% | 1120 |
| fn_accrued_liab_curr_q | 截至资产负债表日期的已发生和应付债务的账面价值，涉及法定性质、合同义务产生的费用，或随着时间累积且尚未收到发票或将不会开具的费用。 | Matrix | 34% | 958 |
| fn_accrued_liab_q | 截至资产负债表日期的已发生和应付债务的账面价值，涉及法定性质、合同义务产生的费用，或随着时间累积且尚未收到发票或将不会开具的费用。 | Matrix | 37% | 876 |
| fn_accum_depr_depletion_and_amortization_ppne_a | 用于正常营业以生产商品和服务的实物资产的累计折旧、耗尽和摊销金额。 | Matrix | 63% | 623 |
| fn_accum_depr_depletion_and_amortization_ppne_q | 用于正常营业以生产商品和服务的实物资产的累计折旧、耗尽和摊销金额。 | Matrix | 38% | 277 |
| fn_accum_oth_income_loss_fx_adj_net_of_tax_a | 累计调整，扣除子公司财务报表和外国股权投资从报告实体功能货币转换为报告货币的过程所得，扣除已实现外币换算收益或亏损的重新分类。 | Matrix | 32% | 525 |
| fn_accum_oth_income_loss_fx_adj_net_of_tax_q | 累计调整，扣除子公司财务报表和外国股权投资从报告实体功能货币转换为报告货币的过程所得，扣除已实现外币换算收益或亏损的重新分类。 | Matrix | 26% | 234 |
| fn_accum_oth_income_loss_net_of_tax_a | 期末时，因交易及其他非所有者来源事件和情况产生的累计股权变动，扣除税务影响。不包括净收益（亏损）以及因所有者投资和分配而产生的累积股权变动。包括外币换算项目、某些养老金调整、某些债务和股权证券投资的未实现收益和亏损，以及因非信用损失而导致的临时减值（OTTI）损失，这些损失是实体无意出售且很可能在摊销成本基础回收前被要求出售的。 以及与指定现金流对冲有效部分相关的衍生品公允价值变化。 | Matrix | 69% | 1540 |
| fn_accum_oth_income_loss_net_of_tax_q | 期末时，因交易及其他非所有者来源事件和情况产生的累计股权变动，扣除税务影响。不包括净收益（亏损）以及因所有者投资和分配而产生的累积股权变动。包括外币换算项目、某些养老金调整、某些债务和股权证券投资的未实现收益和亏损，以及因非信用损失而导致的临时减值（OTTI）损失，这些损失是实体无意出售且很可能在摊销成本基础回收前被要求出售的。 以及与指定现金流对冲有效部分相关的衍生品公允价值变化。 | Matrix | 66% | 764 |
| fn_allocated_share_based_compensation_expense_a | 代表因股权薪酬安排（例如股票、单位、股票期权或其他股权工具）而产生的费用，员工、董事及某些顾问符合员工视为员工的资格。 | Matrix | 67% | 809 |
| fn_allocated_share_based_compensation_expense_q | 代表因股权薪酬安排（例如股票、单位、股票期权或其他股权工具）而产生的费用，员工、董事及某些顾问符合员工视为员工的资格。 | Matrix | 65% | 1120 |
| fn_allowance_for_doubtful_accounts_receivable_a | 对于未分类资产负债表，公司应收的应收账款估值准备金，这些应收款预计无法被催收。 | Matrix | 52% | 496 |
| fn_allowance_for_doubtful_accounts_receivable_q | 对于未分类资产负债表，公司应收的应收账款估值准备金，这些应收款预计无法被催收。 | Matrix | 38% | 261 |
| fn_amortization_of_intangible_assets_a | 将无形资产（未用于生产的非物质资产）成本系统性合理分配到预期受益期间的收益总费用。作为非现金费用，该要素在计算由运营提供或用于运营的现金时，采用间接方法加回净收入。 | Matrix | 49% | 361 |
| fn_amortization_of_intangible_assets_q | 将无形资产（未用于生产的非物质资产）成本系统性合理分配到预期受益期间的收益总费用。作为非现金费用，该要素在计算由运营提供或用于运营的现金时，采用间接方法加回净收入。 | Matrix | 38% | 400 |
| fn_antidilutive_securities_excl_from_eps_a | 未来可能稀释基本每股盈余（EPS）或每股收益（EPU）的证券（包括根据有条件股票协议发行的证券），但未计入稀释EPS或EPU的计算，因为这样做会增加每股收益或EPU金额，或减少当前期间每股或单位的亏损。 | Matrix | 60% | 860 |
| fn_antidilutive_securities_excl_from_eps_q | 未来可能稀释基本每股盈余（EPS）或每股收益（EPU）的证券（包括根据有条件股票协议发行的证券），但未计入稀释EPS或EPU的计算，因为这样做会增加每股收益或EPU金额，或减少当前期间每股或单位的亏损。 | Matrix | 58% | 598 |
| fn_assets_fair_val_a | 资产公允价值、经常性、总额 | Matrix | 33% | 913 |
| fn_assets_fair_val_l1_a | 资产公允价值，经常性，1级 | Matrix | 40% | 296 |
| fn_assets_fair_val_l1_q | 资产公允价值，经常性，1级 | Matrix | 38% | 269 |
| fn_assets_fair_val_l2_a | 资产公允价值，经常性，2级 | Matrix | 39% | 410 |
| fn_assets_fair_val_l2_q | 资产公允价值，经常性，2级 | Matrix | 38% | 212 |
| fn_assets_fair_val_l3_a | 资产公允价值，经常性，3级 | Matrix | 39% | 360 |
| fn_assets_fair_val_l3_q | 资产公允价值，经常性，3级 | Matrix | 38% | 206 |
| fn_assets_fair_val_q | 资产公允价值、经常性、总额 | Matrix | 33% | 183 |
| fn_avg_diluted_sharesout_adj_a | 计算稀释后的每股或单位计算时所用的稀释潜在普通股或单位的总和。 | Matrix | 58% | 203 |
| fn_avg_diluted_sharesout_adj_q | 计算稀释后的每股或单位计算时所用的稀释潜在普通股或单位的总和。 | Matrix | 57% | 227 |
| fn_business_acq_ppne_a | 商业合并，推定财产、工厂和设备 | Matrix | 23% | 1894 |
| fn_business_acq_ppne_q | 业务合并，承接物业、厂房及设备 | Matrix | 28% | 170 |
| fn_business_combination_assets_aquired_goodwill_a | 商业合并，部分用于商誉的购价 | Matrix | 31% | 218 |
| fn_business_combination_assets_aquired_goodwill_q | 商业合并，部分用于商誉的购价 | Matrix | 36% | 221 |
| fn_business_combination_purchase_price_a | 商业合并，购买价格 | Matrix | 48% | 400 |
| fn_business_combination_purchase_price_q | 商业合并，购买价格 | Matrix | 43% | 227 |
| fn_comp_non_opt_forfeited_a | 报告期内被没收的股票（或单位）支付工具数量（不包括股票（或单位）期权。 | Matrix | 58% | 799 |
| fn_comp_non_opt_forfeited_q | 报告期内被没收的股票（或单位）支付工具数量（不包括股票（或单位）期权。 | Matrix | 28% | 110 |
| fn_comp_non_opt_grants_a | 在股票（或单位）期权计划之外（例如，幻影股票或单位计划、股票或单位增值权利计划、绩效目标计划）期间内所授予的拨款数量。 | Matrix | 61% | 826 |
| fn_comp_non_opt_grants_q | 在股票（或单位）期权计划之外（例如，幻影股票或单位计划、股票或单位增值权利计划、绩效目标计划）期间内所授予的拨款数量。 | Matrix | 40% | 160 |
| fn_comp_non_opt_nonvested_number_a | 在资产负债表日期时，有效存在且未偿还的非归属股权支付工具数量（不包括股票（或单位）期权。 | Matrix | 62% | 694 |
| fn_comp_non_opt_nonvested_number_q | 在资产负债表日期时，有效存在且未偿还的非归属股权支付工具数量（不包括股票（或单位）期权。 | Matrix | 36% | 245 |
| fn_comp_non_opt_vested_a | 报告期内归属的股票（或单位）支付工具数量，不包括股票（或单位）期权。 | Matrix | 61% | 540 |
| fn_comp_non_opt_vested_q | 报告期内归属的股票（或单位）支付工具数量，不包括股票（或单位）期权。 | Matrix | 30% | 401 |
| fn_comp_not_rec_a | 未归属的基于股份的赔偿裁决未确认成本。 | Matrix | 65% | 1156 |
| fn_comp_not_rec_q | 未归属的基于股份的赔偿裁决未确认成本。 | Matrix | 38% | 330 |
| fn_comp_not_rec_stock_options_a | 未归属股票期权奖励的未确认成本。 | Matrix | 52% | 210 |
| fn_comp_not_rec_stock_options_q | 未归属股票期权奖励的未确认成本。 | Matrix | 30% | 316 |
| fn_comp_number_of_shares_authorized_a | 行业参与者的唯一身份证数量。Industry 代表对相关日期、代码和交易类型的所有股票清算活动的综合视图。 | Matrix | 43% | 162 |
| fn_comp_number_of_shares_authorized_q | 股权基础薪酬计划下，最初批准（通常由股东和董事会批准）的最高股份（或其他类型的股权）相去后续任何修订和调整。由于股票或单位期权及非期权以外的股权工具被授予参与者，这些股票或单位仍具授权性，并根据未结决奖励（不一定已归属）保留发行。 | Matrix | 26% | 147 |
| fn_comp_options_exercisable_number_a | 截至资产负债表日期，目前可根据期权计划转换为已全部或部分归属股票期权的股份数量。 | Matrix | 59% | 749 |
| fn_comp_options_exercisable_number_q | 截至资产负债表日期，目前可根据期权计划转换为已全部或部分归属股票期权的股份数量。 | Matrix | 27% | 198 |
| fn_comp_options_exercisable_weighted_avg_a | 资产负债表日期的加权平均价，受让人可获得已归属部分期权的预留发行股份，这些期权目前可根据期权计划行使。 | Matrix | 58% | 224 |
| fn_comp_options_exercisable_weighted_avg_q | 资产负债表日期的加权平均价，受让人可获得已归属部分期权的预留发行股份，这些期权目前可根据期权计划行使。 | Matrix | 27% | 318 |
| fn_comp_options_exercises_weighted_avg_a | 基于股份的报酬、假设期权、加权平均行权价 | Matrix | 62% | 890 |
| fn_comp_options_exercises_weighted_avg_q | 基于股份的报酬、假设期权、加权平均行权价 | Matrix | 28% | 242 |
| fn_comp_options_forfeitures_and_expirations_a | 对于合并终止的陈述，指在报告期内因与股票期权计划相关的合同协议中规定的终止事件而被取消的期权股票数量。 | Matrix | 59% | 653 |
| fn_comp_options_forfeitures_and_expirations_q | 对于合并终止的陈述，指在报告期内因与股票期权计划相关的合同协议中规定的终止事件而被取消的期权股票数量。 | Matrix | 28% | 230 |
| fn_comp_options_grants_a | 该期间授予的股份期权（或股份单位）净数量。 | Matrix | 64% | 1283 |
| fn_comp_options_grants_fair_value_a | 按年份薪酬安排 按股份支付 奖励期权 授予 期间加权 平均 授予日期 公允价值 | Matrix | 52% | 571 |
| fn_comp_options_grants_fair_value_q | 按年份薪酬安排 按股份支付 奖励期权 授予 期间加权 平均 授予日期 公允价值 | Matrix | 24% | 315 |
| fn_comp_options_grants_q | 该期间授予的股份期权（或股份单位）净数量。 | Matrix | 45% | 255 |
| fn_comp_options_grants_weighted_avg_a | 加权平均价格，受让人本可获得标的股票，相对于已终止的股票期权。 | Matrix | 57% | 404 |
| fn_comp_options_grants_weighted_avg_q | 加权平均价格，受让人本可获得标的股票，相对于已终止的股票期权。 | Matrix | 29% | 1197 |
| fn_comp_options_out_intrinsic_value_a | 股票期权的内在价值是指标的股票市场价值超过期权行权价的幅度。 | Matrix | 53% | 452 |
| fn_comp_options_out_intrinsic_value_q | 股票期权的内在价值是指标的股票市场价值超过期权行权价的幅度。 | Matrix | 22% | 172 |
| fn_comp_options_out_number_a | 未确定的期权数量，包括既得和非既得期权。 | Matrix | 62% | 474 |
| fn_comp_options_out_number_q | 未确定的期权数量，包括既得和非既得期权。 | Matrix | 34% | 250 |
| fn_comp_options_out_weighted_avg_a | 加权平均价格，受让人可以以这些价格购买股票保留发行的股票。 | Matrix | 65% | 600 |
| fn_comp_options_out_weighted_avg_q | 加权平均价格，受让人可以以这些价格购买股票保留发行的股票。 | Matrix | 34% | 236 |
| fn_comprehensive_income_net_of_tax_a | 税后因交易及其他事件和情况而产生的股权增加（减少）金额，来自净收入及其他综合收入，归属于母公司。不包括因所有者投资及分配给所有者而产生的股权变动。 | Matrix | 61% | 556 |
| fn_comprehensive_income_net_of_tax_q | 税后因交易及其他事件和情况而产生的股权增加（减少）金额，来自净收入及其他综合收入，归属于母公司。不包括因所有者投资及分配给所有者而产生的股权变动。 | Matrix | 60% | 280 |
| fn_debt_instrument_carrying_amount_a | 负债金额 | Matrix | 57% | 610 |
| fn_debt_instrument_carrying_amount_q | 负债金额 | Matrix | 53% | 491 |
| fn_debt_instrument_face_amount_a | 债务面额 | Matrix | 35% | 218 |
| fn_debt_instrument_face_amount_q | 债务面额 | Matrix | 37% | 184 |
| fn_debt_issuance_costs_a | 债务发行成本（例如但不限于法律、会计、经纪和监管费用）。 | Matrix | 36% | 216 |
| fn_debt_issuance_costs_q | 债务发行成本（例如但不限于法律、会计、经纪和监管费用）。 | Matrix | 32% | 231 |
| fn_def_income_tax_expense_a | 所得税费用，递延 | Matrix | 64% | 399 |
| fn_def_income_tax_expense_q | 所得税费用，递延 | Matrix | 47% | 163 |
| fn_def_tax_assets_liab_net_a | 扣除估价扣除额和递延税负后，因可扣除差额和结转而产生的递延税款资产金额，不含管辖权净额。 | Matrix | 71% | 1087 |
| fn_def_tax_assets_liab_net_q | 扣除估价扣除额和递延税负后，因可扣除差额和结转而产生的递延税款资产金额，不含管辖权净额。 | Matrix | 57% | 305 |
| fn_def_tax_assets_net_a | 递延税资产扣除估值扣除额 | Matrix | 68% | 611 |
| fn_def_tax_assets_net_q | 递延税资产扣除估值扣除额 | Matrix | 44% | 121 |
| fn_def_tax_liab_a | 扣除递延税款资产后，因应税差异而产生的递延税负金额，且无管辖权净额。 | Matrix | 65% | 460 |
| fn_def_tax_liab_q | 扣除递延税款资产后，因应税差异而产生的递延税负金额，且无管辖权净额。 | Matrix | 45% | 214 |
| fn_derivative_fair_value_of_derivative_asset_a | 在主净额安排生效之前，金融资产或其他合同与一个或多个标的资产、名义金额或支付条款或两者兼有的公允价值，合同可通过合同或资产交付之外的方式净结算。包括选择不被抵消的资产。排除不受主净额净额安排约束的资产。 | Matrix | 36% | 91 |
| fn_derivative_fair_value_of_derivative_asset_q | 在主净额安排生效之前，金融资产或其他合同与一个或多个标的资产、名义金额或支付条款或两者兼有的公允价值，合同可通过合同或资产交付之外的方式净结算。包括选择不被抵消的资产。排除不受主净额净额安排约束的资产。 | Matrix | 36% | 113 |
| fn_derivative_fair_value_of_derivative_liability_a | 公允价值，在主净额安排生效之前，即与一个或多个标的金融负债或合同、名义金额或支付条款或两者兼有，合同可通过合同之外或资产交付以外的方式净结算。包括选择不抵扣的负债。排除不受主净额安排约束的负债。 | Matrix | 41% | 116 |
| fn_derivative_fair_value_of_derivative_liability_q | 公允价值，在主净额安排生效之前，即与一个或多个标的金融负债或合同、名义金额或支付条款或两者兼有，合同可通过合同之外或资产交付以外的方式净结算。包括选择不抵扣的负债。排除不受主净额安排约束的负债。 | Matrix | 40% | 123 |
| fn_derivative_notional_amount_a | 用于计算衍生品负债支付金额的名义金额或面值。 | Matrix | 37% | 180 |
| fn_derivative_notional_amount_q | 用于计算衍生品负债支付金额的名义金额或面值。 | Matrix | 37% | 133 |
| fn_eff_income_tax_rate_continuing_operations_a | 与持续运营相关的当前所得税费用（福利）和递延所得税费用（福利）的百分比。 | Matrix | 45% | 819 |
| fn_eff_income_tax_rate_continuing_operations_q | 与持续运营相关的当前所得税费用（福利）和递延所得税费用（福利）的百分比。 | Matrix | 34% | 119 |
| fn_effect_of_exchange_rate_on_cash_and_equiv_a | 汇率变动对现金及外币持有现金等价余额的影响增加（减少）金额。 | Matrix | 39% | 485 |
| fn_effect_of_exchange_rate_on_cash_and_equiv_q | 汇率变动对现金及外币持有现金等价余额的影响增加（减少）金额。 | Matrix | 38% | 151 |
| fn_employee_related_liab_a | 截至资产负债表日期，已发生的债务及应支付与员工所获得服务相关义务（如应计工资和奖金、工资税及附加福利）的账面价值总和。对于分类资产负债表，用于反映当前负债部分（1年内到期，或如更长则在正常运营周期内）;对于未分类资产负债表，用于反映总负债（无论到期日如何）。 | Matrix | 49% | 525 |
| fn_employee_related_liab_q | 截至资产负债表日期，已发生的债务及应支付与员工所获得服务相关义务（如应计工资和奖金、工资税及附加福利）的账面价值总和。对于分类资产负债表，用于反映当前负债部分（1年内到期，或如更长则在正常运营周期内）;对于未分类资产负债表，用于反映总负债（无论到期日如何）。 | Matrix | 36% | 500 |
| fn_entity_common_stock_shares_out_a | 说明各登记人类别资本、普通股或其他持股权益的流通股数或其他单位数，如相关定期报告封面所述。如果存在多个类别或单位，则通过在实体上市工具的“域名”中添加股票类别，如普通类别A（成员）、普通类别B（成员）或合伙权益[成员]来定义每个类别/权益。 | Matrix | 72% | 653 |
| fn_entity_common_stock_shares_out_q | 说明各登记人类别资本、普通股或其他持股权益的流通股数或其他单位数，如相关定期报告封面所述。如果存在多个类别或单位，则通过在实体上市工具的“域名”中添加股票类别，如普通类别A（成员）、普通类别B（成员）或合伙权益[成员]来定义每个类别/权益。 | Matrix | 69% | 505 |
| fn_finite_lived_intangible_assets_acq_a | 资产数量（不含金融资产和商誉），缺乏实体且寿命有限。 | Matrix | 30% | 163 |
| fn_finite_lived_intangible_assets_acq_q | 资产数量（不含金融资产和商誉），缺乏实体且寿命有限。 | Matrix | 30% | 261 |
| fn_finite_lived_intangible_assets_gross_a | 资产摊销前的金额，不包括金融资产和商誉，缺乏实质且寿命有限。 | Matrix | 46% | 793 |
| fn_finite_lived_intangible_assets_gross_q | 资产摊销前的金额，不包括金融资产和商誉，缺乏实质且寿命有限。 | Matrix | 32% | 388 |
| fn_finite_lived_intangible_assets_net_a | 有限活体无形资产，净资产 | Matrix | 45% | 228 |
| fn_finite_lived_intangible_assets_net_q | 有限活体无形资产，净资产 | Matrix | 34% | 294 |
| fn_goodwill_acquired_during_period_a | 资产增加的金额，代表未来经济利益，这些资产来自商业合并中未单独识别和确认的其他资产。 | Matrix | 38% | 405 |
| fn_goodwill_acquired_during_period_q | 资产增加的金额，代表未来经济利益，这些资产来自商业合并中未单独识别和确认的其他资产。 | Matrix | 26% | 212 |
| fn_income_from_equity_investments_a | 股权法投资收益 | Matrix | 31% | 693 |
| fn_income_from_equity_investments_q | 股权法投资收益 | Matrix | 26% | 300 |
| fn_income_tax_expense_a | 所得税费用（福利） | Matrix | 69% | 878 |
| fn_income_tax_expense_q | 所得税费用（福利） | Matrix | 70% | 554 |
| fn_income_taxes_paid_a | 当前期间支付给外国、联邦、州和地方当局的现金税额。 | Matrix | 64% | 349 |
| fn_income_taxes_paid_q | 当前期间支付给外国、联邦、州和地方当局的现金税额。 | Matrix | 41% | 154 |
| fn_intangible_assets_accum_amort_a | 累计摊销金额的资产，不包括金融资产和商誉，缺乏实质且寿命有限。 | Matrix | 50% | 231 |
| fn_intangible_assets_accum_amort_q | 累计摊销金额的资产，不包括金融资产和商誉，缺乏实质且寿命有限。 | Matrix | 36% | 322 |
| fn_interest_paid_net_a | 净利息 | Matrix | 65% | 571 |
| fn_interest_paid_net_q | 净利息 | Matrix | 40% | 200 |
| fn_interest_payable_a | 截至资产负债表日期的应计利息，涵盖所有已发生且未偿还的债务（包括贸易应付款）。对于分类资产负债表，用于反映当前负债部分（1年内到期，或如更长则在正常运营周期内）;对于未分类资产负债表，用于反映总负债（无论到期日如何）。 | Matrix | 26% | 271 |
| fn_interest_payable_q | 截至资产负债表日期，所有形式债务（包括贸易应付款）已发生且未偿还的应付利息的账面资产负债表日期。对于分类资产负债表，用于反映当前负债部分（1年内到期，或如更长则在正常运营周期内）;对于未分类资产负债表，用于反映总负债（无论到期日如何）。 | Matrix | 19% | 158 |
| fn_liab_fair_val_a | 负债公允价值、经常性、总额 | Matrix | 33% | 328 |
| fn_liab_fair_val_l1_a | 负债公允价值，经常性，第一级 | Matrix | 36% | 16534 |
| fn_liab_fair_val_l1_q | 负债公允价值，经常性，第一级 | Matrix | 36% | 164 |
| fn_liab_fair_val_l2_a | 负债公允价值，经常性，第二级 | Matrix | 40% | 332 |
| fn_liab_fair_val_l2_q | 负债公允价值，经常性，第二级 | Matrix | 40% | 133 |
| fn_liab_fair_val_l3_a | 负债公允价值，经常性，三级 | Matrix | 26% | 153 |
| fn_liab_fair_val_l3_q | 负债公允价值，经常性，三级 | Matrix | 26% | 264 |
| fn_liab_fair_val_q | 负债公允价值、经常性、总额 | Matrix | 32% | 217 |
| fn_line_of_credit_facility_amount_out_a | 截至资产负债表日期，在信用便利下借入的金额。 | Matrix | 51% | 421 |
| fn_line_of_credit_facility_amount_out_q | 截至资产负债表日期，在信用便利下借入的金额。 | Matrix | 48% | 206 |
| fn_line_of_credit_facility_max_borrowing_capacity_a | 信用便利的最高借款额度，不考虑当前可借款金额或当前未偿还金额的限制。 | Matrix | 48% | 126 |
| fn_line_of_credit_facility_max_borrowing_capacity_q | 信用便利的最高借款额度，不考虑当前可借款金额或当前未偿还金额的限制。 | Matrix | 50% | 989 |
| fn_mne_a | 用于生产商品和服务的有形个人财产的累计折旧前金额，包括但不限于工具、模具、计算机和办公设备。 | Matrix | 53% | 506 |
| fn_new_shares_issued_a | 该期间发行的新股票数量。 | Matrix | 37% | 1410 |
| fn_new_shares_options_a | 当前期间行使的股票期权（或股份单位）数量。 | Matrix | 63% | 728 |
| fn_new_shares_options_q | 当前期间行使的股票期权（或股份单位）数量。 | Matrix | 35% | 284 |
| fn_op_lease_min_pay_due_a | 对于初始或剩余不可取消信件条款超过1年的租约，最低租金支付金额。 | Matrix | 60% | 1428 |
| fn_op_lease_min_pay_due_after_5y_a | 对于初始或剩余不可取消租期超过一年的运营租赁，要求支付的最低租金金额，期限为最新财年后的第5个财年后到期。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 60% | 477 |
| fn_op_lease_min_pay_due_in_2y_a | 对于初始或剩余不可取消租期超过1年的运营租赁，要求支付的最低租金金额，该租赁期限应在最近财政年度后的第二个财政年度内缴纳。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 64% | 752 |
| fn_op_lease_min_pay_due_in_3y_a | 对于运营租赁期超过一年且初始或剩余不可取消租期，于最新财年后的第三个财政年度到期的最低租金金额。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 64% | 555 |
| fn_op_lease_min_pay_due_in_4y_a | 对于初始或剩余不可取消租期超过1年的运营租赁，要求支付的最低租金金额，期限为最新财年后的第四个财政年度。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 63% | 309 |
| fn_op_lease_min_pay_due_in_5y_a | 对于初始或剩余不可取消租期超过1年的运营租赁，要求支付的最低租金金额，应在最新财年后的第五个财政年度到期。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 62% | 566 |
| fn_op_lease_rent_exp_a | 报告期内根据运营租赁产生的租金费用，包括最低租金及任何或有租金费用，扣除相关转租收入。 | Matrix | 64% | 2335 |
| fn_oth_comp_fair_value_a | 年度基于股份的薪酬、股权工具、除期权授予外的期权、加权平均授予日期、公允价值 | Matrix | 55% | 384 |
| fn_oth_comp_forfeitures_fair_value_a | 年度基于股份的薪酬 股权工具 除期权外 没收 加权平均授予日期 公允价值 | Matrix | 50% | 167 |
| fn_oth_income_loss_net_of_tax_a | 税后金额及其他综合收入（损失）的重新分类调整。 | Matrix | 50% | 1192 |
| fn_oth_income_loss_net_of_tax_q | 税后金额及其他综合收入（损失）的重新分类调整。 | Matrix | 50% | 143 |
| fn_payments_for_repurchase_of_common_stock_a | 价值报告于现金流量表。可能包括作为回购计划一部分的股份，以及为员工薪酬购买的股份等。 | Matrix | 48% | 87 |
| fn_payments_for_repurchase_of_common_stock_q | 价值报告于现金流量表。可能包括作为回购计划一部分的股份，以及为员工薪酬购买的股份等。 | Matrix | 46% | 61 |
| fn_ppne_gross_a | 在累计折旧、耗尽和摊销前，用于正常营业且非转售的实物资产。例如，土地、建筑物、机械设备、办公设备以及家具和装置等。 | Matrix | 60% | 1017 |
| fn_ppne_gross_q | 在累计折旧、耗尽和摊销前的金额，用于正常业务运营且非用于转售的实物资产。例如，土地、建筑物、机械设备、办公设备以及家具和装置等。 | Matrix | 29% | 110 |
| fn_prepaid_expense_a | 未分类资产负债表支出日期的挂止金额，这些支出是在成本经济利益实现之前完成的，这些支出将在未来时间推移或触发事件发生时进行计费。对于分类资产负债表，代表预付费用中的非流动部分（当前部分有独立概念）。 | Matrix | 51% | 494 |
| fn_prepaid_expense_q | 未分类资产负债表支出日期的挂止金额，这些支出是在成本经济利益实现之前完成的，这些支出将在未来时间推移或触发事件发生时进行计费。对于分类资产负债表，代表预付费用中的非流动部分（当前部分有独立概念）。 | Matrix | 47% | 488 |
| fn_proceeds_from_issuance_of_common_stock_a | 即来自实体额外资本贡献的现金流入。 | Matrix | 43% | 314 |
| fn_proceeds_from_issuance_of_common_stock_q | 即来自实体额外资本贡献的现金流入。 | Matrix | 37% | 265 |
| fn_proceeds_from_issuance_of_debt_a | 该期间因额外借款而产生的现金流入。包括短期和长期债务的收益。 | Matrix | 57% | 200 |
| fn_proceeds_from_issuance_of_debt_q | 该期间因额外借款而产生的现金流入。包括短期和长期债务的收益。 | Matrix | 52% | 129 |
| fn_proceeds_from_lt_debt_a | 长期债务发行所得 | Matrix | 34% | 412 |
| fn_proceeds_from_lt_debt_q | 长期债务发行所得 | Matrix | 29% | 94 |
| fn_proceeds_from_stock_options_exercised_a | 与持有人行使股票期权所获得金额相关的现金流入。该项本质上排除了实体可能已实现并单独申报的任何超额税收优惠。 | Matrix | 41% | 145 |
| fn_proceeds_from_stock_options_exercised_q | 与持有人行使股票期权所获得金额相关的现金流入。该项本质上排除了实体可能已实现并单独申报的任何超额税收优惠。 | Matrix | 36% | 264 |
| fn_profit_loss_a | 该期间的合并盈亏，扣除所得税后，包括归属于非控股权益的部分。 | Matrix | 41% | 1028 |
| fn_profit_loss_q | 该期间的合并盈亏，扣除所得税后，包括归属于非控股权益的部分。 | Matrix | 42% | 152 |
| fn_repayments_of_debt_a | 即在偿还总额短期和长期债务时流出的现金。不包括资本租赁义务的支付。 | Matrix | 63% | 277 |
| fn_repayments_of_debt_q | 即在偿还总额短期和长期债务时流出的现金。不包括资本租赁义务的支付。 | Matrix | 59% | 127 |
| fn_repayments_of_lines_of_credit_a | 用于偿还贷款机构债务的现金流出金额，包括但不限于信用状、备用信用证和循环信用安排。 | Matrix | 39% | 261 |
| fn_repayments_of_lines_of_credit_q | 用于偿还贷款机构债务的现金流出金额，包括但不限于信用状、备用信用证和循环信用安排。 | Matrix | 45% | 131 |
| fn_repayments_of_lt_debt_a | 债务的现金流出，其到期时间在正常运营周期1年或之后，甚至更久。 | Matrix | 42% | 166 |
| fn_repayments_of_lt_debt_q | 债务的现金流出，其到期时间在正常运营周期1年或之后，甚至更久。 | Matrix | 39% | 113 |
| fn_repurchased_shares_a | 该期间回购的股票数量。 | Matrix | 47% | 159 |
| fn_repurchased_shares_q | 该期间回购的股票数量。 | Matrix | 33% | 71 |
| fn_repurchased_shares_value_a | 股票回购后要么退役，要么放入国库库存，可能是作为股票回购计划的一部分。 | Matrix | 49% | 112 |
| fn_repurchased_shares_value_q | 股票回购后要么退役，要么放入国库库存，可能是作为股票回购计划的一部分。 | Matrix | 37% | 238 |
| fn_taxes_payable_a | 以资产负债表日期为止，法定收入、销售、使用、工资、消费税、不动产、财产及其他税款的应付债务的账面价值。对于分类资产负债表，用于反映当前负债部分（1年内到期，或如更长则在正常运营周期内）;对于未分类资产负债表，用于反映总负债（无论到期日如何）。 | Matrix | 45% | 154 |
| fn_taxes_payable_q | 截至资产负债表日期的法定收入、销售、使用、工资、消费税、不动产、财产及其他税种的负债，其经营价值。对于分类资产负债表，用于反映当前负债部分（1年内到期，或如更长则在正常运营周期内）;对于未分类资产负债表，用于反映总负债（无论到期日如何）。 | Matrix | 36% | 130 |
| fn_treasury_stock_shares_a | 此前已发行并由发行实体回购并在财务报表日期持有于国库的普通股和优先股数量。该股票无投票权，也不收取股息。 | Matrix | 39% | 236 |
| fn_treasury_stock_shares_q | 此前已发行并由发行实体回购并在财务报表日期持有于国库的普通股和优先股数量。该股票无投票权，也不收取股息。 | Matrix | 34% | 274 |
| fn_unrecognized_tax_benefits_a | 未被认可的税收优惠数量。 | Matrix | 54% | 459 |
| fnd2_a_acmopclcchngcfectnt | 累计变动，扣除税后，来自被指定并符合现金流对冲有效部分的衍生工具的累计盈亏。包括实体在股权投资者递延对冲收益或减少中的份额。 | Matrix | 27% | 177 |
| fnd2_a_acmopcldbpoprpnt | 净收益（损失）、先前服务成本（信用）和过渡资产（义务）以及如果仍有的最低养老金负债，都计入与确定给付养老金或其他退休后计划相关的累计其他综合收入，因为它们尚未被认列为净周期性福利成本的组成部分。 | Matrix | 26% | 103 |
| fnd2_a_allfdbflaccrwriteoffs | 之前已核销的应收账款数量，这些催收款可能未被收回。 | Matrix | 31% | 216 |
| fnd2_a_alsbcmpexrsus | 分配的基于股份的薪酬费用，受限股票单位 | Matrix | 31% | 282 |
| fnd2_a_atdlsecexfcepsastkos | 反稀释性股份不计入每股收益，股票期权 | Matrix | 26% | 592 |
| fnd2_a_blgandiprtsg | 建筑结构在累计折旧前的金额，用于生产性用途，包括对建筑物的增建、改进或翻新，包括但不限于室内砌体、室内地板、电气和管道。 | Matrix | 34% | 262 |
| fnd2_a_bnsacqproformarvn | 形式收入在一定期间内，就像业务合并在该期初已完成一样。 | Matrix | 33% | 188 |
| fnd2_a_bnscbmacqrcsts | 该元素表示为实现业务合并而产生的与收购相关的成本，且在该期间已报销费用。这些费用包括介绍费;咨询、法律、会计、估值及其他专业或咨询费用;一般行政费用，包括维护内部采购部门的费用;并可能包括注册和发行债务及股权证券的成本。 | Matrix | 26% | 154 |
| fnd2_a_consinprogressg | 结构的数量或对正在建设的结构的修改。包括最近完工的结构或尚未投入使用的结构的改造。 | Matrix | 32% | 502 |
| fnd2_a_curritxexp | 当前所得税支出 | Matrix | 62% | 534 |
| fnd2_a_dbplanepdrtnplas | 该金额用于确定资产公允价值变动影响延迟确认的程度。计划资产的预期回报率是基于计划资产的预期长期回报率和计划资产的市场相关价值来确定的。 | Matrix | 25% | 68 |
| fnd2_a_dbplanintcst | 确定福利养老金计划的预计退休义务或确定退休后退休计划累计退休后福利义务的增加。 | Matrix | 28% | 108 |
| fnd2_a_dbplannpicbnfcst | 确定给付计划在该期间内的净定期给付总费用。定期福利成本包括以下组成部分：服务成本、利息成本、计划资产预期回报、收益（损失）、先前服务成本或抵免、过渡资产或义务，以及因结算或缩减而产生的收益（损失）。 | Matrix | 28% | 138 |
| fnd2_a_dbplanservicecst | 养老金福利公式归属于员工在该期间所提供的服务的精算现值。预期退休后福利义务中归属于该期间员工服务的部分。服务成本部分是福利义务的一部分，不受计划资金状态的影响。 | Matrix | 26% | 111 |
| fnd2_a_dbplctrbyemp | 雇主向确定福利计划缴纳的金额。 | Matrix | 30% | 97 |
| fnd2_a_dfdtxava | 递延纳税资产的数量，这些资产很可能无法实现税收优惠。 | Matrix | 60% | 947 |
| fnd2_a_eplsbvdcpcstnrgprg | 股权基础薪酬计划中未确认补偿预计被确认的加权平均期间，使用小数表示年数。 | Matrix | 33% | 138 |
| fnd2_a_eplsbvdcpcstnrgsbaoo | 未确认的其他基于股份的赔偿赔偿费用。 | Matrix | 28% | 234 |
| fnd2_a_eplsrbcpntxbnffcmpex | 该期间内认出的基于股权的支付安排的薪酬成本认可的税收利益。 | Matrix | 30% | 163 |
| fnd2_a_excesstxbnffsbcpnoprat | 与实体税表上股权工具报税时，因可扣除补偿成本相关的现金流出金额，超过了为财务报告目的确认的该工具的补偿成本。 | Matrix | 26% | 55 |
| fnd2_a_fedstyitxrt | 有效所得税率对调——联邦法定所得税率百分比 | Matrix | 56% | 284 |
| fnd2_a_flintasacmamtzcsrld | 有限生活无形资产 累计摊销，客户相关 | Matrix | 32% | 384 |
| fnd2_a_flintasamt1expay5 | 资产的摊销费用金额（不含金融资产和商誉）且缺乏实质且寿命有限的资产，预计将在最新财年后的第5个财年后确认。排除以滚动方式报告的中期和年度期间，从最新资产负债表日期起计算 | Matrix | 28% | 338 |
| fnd2_a_flintasamt1expnext12m | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限，预计将在最新财年之后的下一财政年度内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 56% | 226 |
| fnd2_a_flintasamt1expy5 | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限的资产，预计将在最新财年后的第五个财年内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 54% | 298 |
| fnd2_a_flintasamt1expyfour | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限，预计将在最新财年之后的第四财政年度内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 56% | 432 |
| fnd2_a_flintasamt1expythree | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限，预计将在最新财年后的第三个财年内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 56% | 232 |
| fnd2_a_flintasamt1expytwo | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限，预计将在最新财年之后的第二个财年内确认。排除以滚动方式报告的中期和年度期间，从最新资产负债表日期起计算 | Matrix | 57% | 238 |
| fnd2_a_flintasgcsrld | 有限生活无形资产总额，客户相关 | Matrix | 32% | 286 |
| fnd2_a_frtandfixturesg | 在办公室和商店常用的设备累计折旧前的金额，这些设备与建筑结构或公用设施没有永久连接。例如但不限于书桌、椅子、桌子和书架。 | Matrix | 35% | 338 |
| fnd2_a_gsles1xtinguishmentofd | 支付的公允金额与到期前消除的债务挂钩金额之间的差额。 | Matrix | 27% | 462 |
| fnd2_a_gwllimrml | 资产减记所产生的损失金额，代表因企业合并中获得的其他未单独识别和确认的资产所获得的未来经济利益。 | Matrix | 31% | 239 |
| fnd2_a_inventoryfinishedgoods | 预计在1年或运营周期内（如更长）销售的已完成商品或商品估价前和LIFO储备的金额。 | Matrix | 26% | 192 |
| fnd2_a_inventoryrawmaterials | 预计在1年或运营周期内（如更长）内销售或消耗的原材料估值前和LIFO储备的金额。 | Matrix | 27% | 253 |
| fnd2_a_landlandiprts | 累计折旧和耗尽前，用于生产用途的房地产以及为生产用途持有的房地产的增建或改进，例如但不限于人行道、车道、围栏和停车场。不包括待售土地 | Matrix | 42% | 369 |
| fnd2_a_lhdiprtsg | 在租赁安排下资产的增加或改进，扣除累计折旧前的金额。 | Matrix | 33% | 640 |
| fnd2_a_lineofcrfcyrmbrgcap | 当前信贷便利下可用的借款额度（当前借款额度减去未偿还借款额）。 | Matrix | 30% | 129 |
| fnd2_a_ltrmdmrepoplay5 | 持有人可以固定或确定价格和日期赎回的长期应付债务金额、偿还基金要求及其他证券，这些证券在最近财政年度之后的第五个财年后到期。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 33% | 159 |
| fnd2_a_ltrmdmrepoplinnext12m | 持有人可于最新财年后下一个财年到期的固定或确定价格和到期日赎回的长期应偿债务金额、偿还基金要求及其他发行证券。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 39% | 153 |
| fnd2_a_ltrmdmrepopliny5 | 持有人可于最新财年后第五个财年到期时以固定或确定价格赎回的长期应付债务金额、偿债基金要求及其他证券。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 40% | 124 |
| fnd2_a_ltrmdmrepoplinyfour | 持有人可在最新财政年度之后第四个财年以固定或确定价格和到期日赎回的长期应付债务金额、偿还基金要求及其他证券。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 41% | 177 |
| fnd2_a_ltrmdmrepoplinythree | 持有人可于最新财年后第三个财政年度到期时以固定或确定价格赎回的长期应付债务金额、偿付基金要求及其他证券。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 43% | 129 |
| fnd2_a_ltrmdmrepoplinytwo | 持有人可于最新财年后第二个财年到期的固定或确定价格和日期赎回的长期应付债务金额、偿债基金要求及其他证券。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 43% | 167 |
| fnd2_a_opclpsnprtmbnfplansajnt | 税后和重新分类调整后，与养老金及其他退休后确定福利计划相关的其他综合（收入）损失减少的金额。 | Matrix | 28% | 158 |
| fnd2_a_provisionfordbflact | 期间内可疑账户的规定 | Matrix | 41% | 252 |
| fnd2_a_ptoacqbnsesg | 与该期间业务收购相关的现金流出。现金部分仅占收购价。 | Matrix | 31% | 164 |
| fnd2_a_restructuringcharges | 根据授权计划进行退出或处置活动的费用金额。不包括与停止运营或资产退休义务相关的费用。 | Matrix | 25% | 199 |
| fnd2_a_rvndm | 国内收入 | Matrix | 35% | 490 |
| fnd2_a_sbcpnargmpmtwgtm | 所有计划未偿还的奖励从资产负债表日期到到期之间的加权平均期，可用小数点表示，表示年份。 | Matrix | 28% | 575 |
| fnd2_a_sbcpnargmpmtwopsffesip | 报告期内因与股票期权计划合同协议中规定的终止事件而被取消的期权股票数量。 | Matrix | 39% | 500 |
| fnd2_a_sbcpnargmpmtwstgm | 截至资产负债表日期，已完全归属并预计归属的未流通股数可以根据期权计划进行转换。 | Matrix | 29% | 341 |
| fnd2_a_sbcpnargmpmtwvadpgwepr | 截至资产负债表日期，已完全归属或预计归属的未发行股票期权的加权平均行权价格。 | Matrix | 27% | 169 |
| fnd2_a_sbcpnargmpmwggil | 标的股票当前公允价值超过完全归属且预期已归还期权的行权价的金额。 | Matrix | 27% | 731 |
| fnd2_a_sbcpnargmsawpfipwerpr | 被没收或到期期权的加权平均价格。 | Matrix | 26% | 225 |
| fnd2_a_sbcpnargmsptawervl | 在行使日期的标的股票公允价值与已行使（或转换为股份单位）期权的行权价格之间的累计差额。 | Matrix | 53% | 818 |
| fnd2_a_sbcpnargmtwfsptepddvdrt | 期权期限内应支付给标的股票持有人的预计股息率（股价的百分比）。 | Matrix | 51% | 208 |
| fnd2_a_sbcpnargtbysbpmtwpwrr | 受让人可就已到期计划股票期权购买基础股份的加权平均价格。 | Matrix | 38% | 313 |
| fnd2_a_sbcpnatqsttotnsvdptfv | 受让人通过满足服务和履行要求获得获得或保留股份或单位、其他工具或现金的权利的基于股份的奖赏的公允价值。 | Matrix | 31% | 117 |
| fnd2_a_sbcpnshardustoprgps | 股票期权计划授权的基于股票的薪酬股票行使已发行期权数量 | Matrix | 29% | 137 |
| fnd2_a_seniornotes | 包括流动和非流动部分，即在破产或清算时，对发行人资产索赔最高的票据的资产负债（到期日应在1年后或更长则超过运营周期）。资深票据持有人在向次级票据持有人支付任何款项前，先全额偿还。 | Matrix | 33% | 185 |
| fnd2_a_stkdrgprdvalnewissues | 新发行股票价值对该期间股权影响。包括首次公开募股或二级公开募股中发行的股份。 | Matrix | 37% | 353 |
| fnd2_a_stkrpeprogramardamt | 由实体董事会授权的股票回购计划金额。 | Matrix | 26% | 187 |
| fnd2_a_unrgtxbnfitxpenlintacd | 因少缴所得税及与税表中申报或预期申报的税务状况相关的罚款而产生的利息。 | Matrix | 30% | 149 |
| fnd2_a_unrgtxbnfthatwdiptetxr | 即未被认可的税收优惠总额，如果被认可，将影响实际税率。 | Matrix | 37% | 202 |
| fnd2_asdm | 资产，国内 | Matrix | 31% | 224 |
| fnd2_currfedtxexp | 当前所得税费用 - 联邦 | Matrix | 57% | 118 |
| fnd2_currfrtxexp | 当前所得税费用 - 外国 | Matrix | 41% | 248 |
| fnd2_currstatelocaltxexp | 当前所得税费用 - 州和地方 | Matrix | 52% | 285 |
| fnd2_dbplanactuarialgl | 确定给付计划、已支付的给付、计划资产 | Matrix | 26% | 767 |
| fnd2_dbplanamtsrginblsh | 资产负债表中与确定收益计划相关的总净金额。通常与确定福利计划、计划的资助状态、总额相同。 | Matrix | 25% | 79 |
| fnd2_dbplanartonplas | 确定给付计划、已支付的给付、计划资产 | Matrix | 25% | 132 |
| fnd2_dbplanbnfol | 1）对于确定给付养老金计划，福利义务为预计福利义务，即截至某日期，养老金福利公式归属于该日期之前员工服务的所有福利的精算现值。2）对于其他退休后确定福利计划，福利义务是累计的退休后福利义务，即归因于特定日期员工服务的福利的精算现值。 | Matrix | 29% | 131 |
| fnd2_dbplanbnfpaid | 参与者在养老金计划下有权获得的支付金额，包括养老金福利、死亡福利以及离职时应支付的福利。还包括退休后福利计划下的支付，包括处方药福利、医疗保健福利、人寿保险福利以及法律、教育和咨询服务。该项目代表计划义务的周期性减少和计划资产的减少。 | Matrix | 27% | 304 |
| fnd2_dbplanbnfpaid_ast | 参与者在养老金计划下有权获得的支付金额，包括养老金福利、死亡福利以及离职时应支付的福利。还包括退休后福利计划下的支付，包括处方药福利、医疗保健福利、人寿保险福利以及法律、教育和咨询服务。该项目代表计划义务的周期性减少和计划资产的减少。 | Matrix | 27% | 132 |
| fnd2_dbplanchgbnfolintcst | 确定福利计划福利义务利息成本的变化 | Matrix | 26% | 71 |
| fnd2_dbplanepdfbnfp5ytherea | 确定福利计划预计在最新财年之后的第5个财政年度内支付的福利金额。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 28% | 121 |
| fnd2_dbplanepdfbnfpnext12m | 确定给付计划预计在最新财年之后的下一财政年度内支付的福利金额。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 28% | 62 |
| fnd2_dbplanepdfbnfpy5 | 确定给付计划预计在最新财年后的第五个财政年度支付的福利金额。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 28% | 135 |
| fnd2_dbplanepdfbnfpyfour | 确定给付计划预计在最新财年之后的第四个财政年度支付的福利金额。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 28% | 221 |
| fnd2_dbplanepdfbnfpythree | 确定给付计划预计在最新财年后的第三个财政年度支付的福利金额。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 28% | 55 |
| fnd2_dbplanepdfbnfpytwo | 确定收益计划预计在最新财年后的第二个财政年度支付的福利金额。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 28% | 109 |
| fnd2_dbplanfvalpnas | 被隔离并限制用于提供养老金或退休后福利的资产的公允价值。资产包括但不限于股票、债券、其他投资、投资收益以及雇主和员工的缴款。 | Matrix | 28% | 78 |
| fnd2_dfctrbplancstrg | 确定缴款计划期间确认的费用金额。 | Matrix | 47% | 256 |
| fnd2_dfdfeditxexp | 所得税费用，递延——联邦 | Matrix | 54% | 179 |
| fnd2_dfdfritxexp | 所得税费用，递延 - 外国 | Matrix | 39% | 184 |
| fnd2_dfdlocalitxexp | 所得税费用，递延 | Matrix | 51% | 106 |
| fnd2_dfdtxasoprlcarryfwd | 归因于可扣除营业亏损结转的递延税资产估值扣除额前的金额。 | Matrix | 62% | 498 |
| fnd2_dfdtxastxcrcarryfwd | 在分配估值扣除额之前，归因于可扣除税收抵扣结转的递延税款资产金额，包括但不限于研究税、外国税、综合企业、替代最低税收及其他可扣除税收抵免结转 | Matrix | 38% | 311 |
| fnd2_dfdtxastxdfdexpcompbnf | 归因于可扣除临时差额的递延税资产估值扣除前的金额，用于报酬和福利成本。 | Matrix | 53% | 346 |
| fnd2_dfdtxastxdfdexprssaccrs | 归因于可扣除的临时差额与准备金和应计制的递延税资产估值扣除额前的金额。 | Matrix | 52% | 408 |
| fnd2_dfdtxlbsgwllandintas | 因应税暂时差额而产生的递延税负金额，包括商誉资产。 | Matrix | 36% | 176 |
| fnd2_dfdtxlbspropplteqm | 因应税暂时差异而产生的递延税款额。 | Matrix | 43% | 222 |
| fnd2_ebitdm | EBIT，国内 | Matrix | 42% | 537 |
| fnd2_ebitfr | EBIT，外国 | Matrix | 39% | 721 |
| fnd2_eixrtreclstatelocalitxes | 通过将国内联邦法定所得税税率应用于适用于州和地方所得税费用（福利）的持续经营所得（损失）计算出的报告所得税费用（福利）与预期所得税费用（福利）之间的差额百分比，扣除联邦税收费用（福利）。 | Matrix | 33% | 153 |
| fnd2_itxreclchgdfdtxava | 通过将国内联邦法定所得税税率应用于因递延税资产估值扣除增加（减少）而产生的持续经营税前收入（损失）计算得出的报告所得税费用（福利）与预期所得税费用（利益）之间的差额。 | Matrix | 26% | 501 |
| fnd2_itxreclnondeductibleexp | 通过将国内联邦法定所得税税率应用于因不可扣除费用而产生的持续经营所得（亏损）所得税前收入（损失），计算出报告所得税费用（福利）与预期所得税费用（福利）之间的差额。 | Matrix | 29% | 273 |
| fnd2_itxreclstatelocalitxes | 通过将国内联邦法定所得税税率应用于归属于州和地方所得税费用的持续经营所得（损失）所得，计算出报告所得税费用（福利）与预期所得税费用（利益）之间的差额。 | Matrix | 34% | 185 |
| fnd2_itxreexftfedstyitxrt | 所得税金额按联邦税率计算，未进行任何调整 | Matrix | 39% | 193 |
| fnd2_oprlsfmpdcurr | 对于初始或剩余不可取消租期超过1年的运营租赁，要求支付的最低租金金额，该租赁期限为下一个财政年度，且该租期在最新财年之后。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 64% | 1230 |
| fnd2_propplteqflublgland | 个人防护装备、建筑与土地、使用寿命、最高限制 | Matrix | 36% | 96 |
| fnd2_propplteqmuflmameqmt | PPE、设备、使用寿命、最大使用寿命 | Matrix | 48% | 135 |
| fnd2_propplteqmuflmamfrt | 个人防护装备、家具、使用寿命、最高限度 | Matrix | 27% | 153 |
| fnd2_propplteqmuflmblgland | 个人防护装备、建筑与土地、使用寿命、最低限度 | Matrix | 33% | 252 |
| fnd2_propplteqmuflmeqmt | 个人防护装备、设备、使用寿命、最低标准 | Matrix | 47% | 128 |
| fnd2_propplteqmuflmfrt | 个人防护装备、家具、使用寿命、最低限度 | Matrix | 26% | 137 |
| fnd2_q_atdlsecexfcepsastkos | 反稀释性股份不计入每股收益，股票期权 | Matrix | 27% | 336 |
| fnd2_q_bnsacqproformarvn | 形式收入在一定期间内，就像业务合并在该期初已完成一样。 | Matrix | 28% | 148 |
| fnd2_q_flintasamt1expy5 | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限的资产，预计将在最新财年后的第五个财年内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 29% | 347 |
| fnd2_q_flintasamt1expyfour | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限，预计将在最新财年之后的第四财政年度内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 31% | 768 |
| fnd2_q_flintasamt1expythree | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限，预计将在最新财年后的第三个财年内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 31% | 266 |
| fnd2_q_flintasamt1expytwo | 资产摊销费用金额，不包括金融资产和商誉，且缺乏实体且寿命有限，预计将在最新财年之后的第二个财年内确认。排除以滚动方式报告的中期和年度期间，且从最新资产负债表日期起报告。 | Matrix | 31% | 355 |
| fnd2_q_inventoryfinishedgoods | 预计在1年或运营周期内（如更长）销售的已完成商品或商品估价前和LIFO储备的金额。 | Matrix | 25% | 395 |
| fnd2_q_inventoryrawmaterials | 预计在1年或运营周期内（如更长）内销售或消耗的原材料估值前和LIFO储备的金额。 | Matrix | 26% | 225 |
| fnd2_q_lineofcrfcyrmbrgcap | 当前信贷便利下可用的借款额度（当前借款额度减去未偿还借款额）。 | Matrix | 27% | 180 |
| fnd2_q_ptoacqbnsesg | 与该期间业务收购相关的现金流出。现金部分仅占收购价。 | Matrix | 27% | 113 |
| fnd2_q_seniornotes | 包括流动和非流动部分，即在破产或清算时，对发行人资产索赔最高的票据的资产负债（到期日应在1年后或更长则超过运营周期）。资深票据持有人在向次级票据持有人支付任何款项前，先全额偿还。 | Matrix | 32% | 201 |
| fnd2_sbcpnshardpreops | 股票期权计划授权的基于股票的薪酬股票行使可行使期权数量 | Matrix | 27% | 145 |
| fnd2_unremittedfrer | 未汇出的外汇收入 | Matrix | 31% | 339 |
| fnd2_unrgtxbnfdcfpprdtxpss | 因当期报税表中已或将采取的税务立场而导致未被认可的税收优惠减少的金额。 | Matrix | 42% | 107 |
| fnd2_unrgtxbnfdecresfsttwtxauth | 与税务机关达成和解导致未确认税收优惠减少的金额。 | Matrix | 35% | 79 |
| fnd2_unrgtxbnfinregfcrps | 因当前期报税表中已采取或将采取的税务立场而导致未确认税收利益增加的金额。 | Matrix | 46% | 136 |
| fnd2_unrgtxbnfinregfprtxps | 因前一期税务申报表中采取的税务立场而导致未确认税收利益增加的金额。 | Matrix | 44% | 190 |
| fnd2_unrgtxbnfrdsrefpstf | 因适用诉讼时效过期而导致未确认税收利益减少的金额。 | Matrix | 38% | 196 |

### 财务基本面-年度 (fundamental6)（886 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| assets | 资产 - 总计 | Matrix | 50% | 133897 |
| assets_curr | 流动资产 - 总额 | Matrix | 50% | 14264 |
| bookvalue_ps | 每股账面价值 | Matrix | 50% | 9437 |
| capex | 资本支出 | Matrix | 50% | 26029 |
| cash | 现金 | Matrix | 50% | 11340 |
| cash_st | 现金与短期投资 | Matrix | 50% | 8131 |
| cashflow | 现金流（年度） | Matrix | 50% | 9244 |
| cashflow_dividends | 现金红利（现金流） | Matrix | 50% | 5673 |
| cashflow_fin | 融资活动 - 净现金流 | Matrix | 50% | 7309 |
| cashflow_invst | 投资活动 - 净现金流 | Matrix | 50% | 4762 |
| cashflow_op | 运营活动 - 净现金流 | Matrix | 50% | 13113 |
| cogs | 销售成本 | Matrix | 50% | 9741 |
| current_ratio | 电流比率 | Matrix | 50% | 6784 |
| debt | 债务 | Matrix | 50% | 26022 |
| debt_lt | 长期债务 - 总额 | Matrix | 50% | 14917 |
| debt_st | 流动负债中的债务 | Matrix | 50% | 9509 |
| depre_amort | 折旧与摊销 - 总计 | Matrix | 50% | 4473 |
| ebit | 息税前利润 | Matrix | 50% | 18992 |
| ebitda | 息前收益 | Matrix | 50% | 18975 |
| employee | 员工 | Matrix | 50% | 5125 |
| enterprise_value | 企业价值 | Matrix | 50% | 37001 |
| eps | 每股收益（基础）——包括非凡项目 | Matrix | 50% | 16102 |
| equity | 普通股本/普通股本 - 总额 | Matrix | 50% | 20855 |
| fnd6_acdo | 已停止运营的流动资产 | Matrix | 50% | 8339 |
| fnd6_acodo | 除已停止运营外的其他流动资产 | Matrix | 50% | 3078 |
| fnd6_acox | 流动资产 - 其他 - 杂项 | Matrix | 50% | 2693 |
| fnd6_acqgdwl | 已取得资产 - 商誉 | Matrix | 50% | 1273 |
| fnd6_acqintan | 已收购资产 - 无形资产 | Matrix | 50% | 607 |
| fnd6_adesinda_curcd | ISO货币代码 - 公司年度市场 | Matrix | 50% | 3817 |
| fnd6_aldo | 已停运运营的长期资产 | Matrix | 50% | 1265 |
| fnd6_am | 无形资产摊销 | Matrix | 50% | 1483 |
| fnd6_aodo | 其他资产（不含已停止运营） | Matrix | 50% | 853 |
| fnd6_aox | 资产 - 其他 - 杂项 | Matrix | 50% | 1300 |
| fnd6_aqc | 收购 | Matrix | 50% | 1370 |
| fnd6_aqi | 收购 - 收入贡献 | Matrix | 50% | 296 |
| fnd6_aqs | 收购 - 销售贡献 | Matrix | 50% | 391 |
| fnd6_beta | 测试版 | Matrix | 50% | 646 |
| fnd6_capxs | 资本支出 | Vector | 50% | 122 |
| fnd6_capxv | 资本支出 财产、工厂和设备 附表 V | Matrix | 50% | 1984 |
| fnd6_caxts | 成本与支出 - 总计 | Vector | 50% | 46 |
| fnd6_ceql | 普通股权 - 清算价值 | Matrix | 50% | 1924 |
| fnd6_ch | 现金 | Matrix | 50% | 1770 |
| fnd6_ci | 综合收入 - 总额 | Matrix | 50% | 1984 |
| fnd6_cibegni | Comp Inc - 初始净收入 | Matrix | 50% | 808 |
| fnd6_cicurr | Comp Inc - Currency Trans Adj | Matrix | 50% | 2310 |
| fnd6_cidergl | Comp Inc - 衍生品收益/亏损 | Matrix | 50% | 568 |
| fnd6_cik | 非重要的技术代码 | Matrix | 50% | 1907 |
| fnd6_cimii | 综合收益 - 非控制权益 | Matrix | 50% | 358 |
| fnd6_ciother | Comp. Inc. - 其他形容词 | Matrix | 50% | 5275 |
| fnd6_cipen | 综合收入 - 最低养老金调整 | Matrix | 50% | 853 |
| fnd6_cisecgl | Comp Inc - 证券收益/亏损 | Matrix | 50% | 1189 |
| fnd6_citotal | 综合收入 - 母公司 | Matrix | 50% | 660 |
| fnd6_city | 公司总部或总部所在的城市 | Matrix | 50% | 1767 |
| fnd6_cld2 | 资本化租赁——第二年到期 | Matrix | 50% | 1358 |
| fnd6_cld3 | 资本化租赁——第三年到期 | Matrix | 50% | 1515 |
| fnd6_cld4 | 资本化租赁——第四年到期 | Matrix | 50% | 1488 |
| fnd6_cld5 | 资本化租赁——第五年到期 | Matrix | 50% | 1264 |
| fnd6_cogss | 销售成本 | Vector | 50% | 57 |
| fnd6_cptmfmq_actq | 流动资产 - 总额 | Matrix | 50% | 679 |
| fnd6_cptmfmq_atq | 资产 - 总计 | Matrix | 50% | 1278 |
| fnd6_cptmfmq_ceqq | 普通股本/普通股本 - 总额 | Matrix | 50% | 1251 |
| fnd6_cptmfmq_dlttq | 长期债务 - 总额 | Matrix | 50% | 1166 |
| fnd6_cptmfmq_dpq | 折旧与摊销 - 总计 | Matrix | 50% | 509 |
| fnd6_cptmfmq_lctq | 流动负债 - 总额 | Matrix | 50% | 1355 |
| fnd6_cptmfmq_oibdpq | 折旧前营业收入 - 季度 | Matrix | 50% | 765 |
| fnd6_cptmfmq_opepsq | 运营每股收益 | Matrix | 50% | 1246 |
| fnd6_cptmfmq_saleq | 销售/营业额（净额） | Matrix | 50% | 877 |
| fnd6_cptnewqeventv110_actq | 流动资产 - 总额 | Vector | 50% | 47 |
| fnd6_cptnewqeventv110_apq | 应付账款/债权人 - 贸易 | Vector | 50% | 114 |
| fnd6_cptnewqeventv110_atq | 资产 - 总计 | Vector | 50% | 43 |
| fnd6_cptnewqeventv110_ceqq | 普通股本/普通股本 - 总额 | Vector | 50% | 50 |
| fnd6_cptnewqeventv110_dlttq | 长期债务 - 总额 | Vector | 50% | 140 |
| fnd6_cptnewqeventv110_dpq | 折旧与摊销 - 总计 | Vector | 50% | 45 |
| fnd6_cptnewqeventv110_epsf12 | 每股收益（稀释后）- 不含非常项目 - 12个月移动 | Vector | 50% | 65 |
| fnd6_cptnewqeventv110_epsfxq | 每股收益（稀释后）——不含特别项目 | Vector | 50% | 48 |
| fnd6_cptnewqeventv110_epsx12 | 每股收益（基础）- 不包括特别项目 - 12个月内搬迁 | Vector | 50% | 130 |
| fnd6_cptnewqeventv110_lctq | 流动负债 - 总额 | Vector | 50% | 852 |
| fnd6_cptnewqeventv110_ltq | 负债 - 总额 | Vector | 50% | 244 |
| fnd6_cptnewqeventv110_nopiq | 非营业收入（费用）- 总额 | Vector | 50% | 373 |
| fnd6_cptnewqeventv110_oeps12 | 运营每股收益 - 12个月移动 | Vector | 50% | 85 |
| fnd6_cptnewqeventv110_oiadpq | 折旧后营业收入 - 季度 | Vector | 50% | 50 |
| fnd6_cptnewqeventv110_oibdpq | 折旧前营业收入 - 季度 | Vector | 50% | 60 |
| fnd6_cptnewqeventv110_opepsq | 运营每股收益 | Vector | 50% | 52 |
| fnd6_cptnewqeventv110_rectq | 应收账款 - 总计 | Vector | 50% | 45 |
| fnd6_cptnewqeventv110_req | 留存收益 | Vector | 50% | 21 |
| fnd6_cptnewqeventv110_saleq | 销售/营业额（净额） | Vector | 50% | 227 |
| fnd6_cptnewqv1300_actq | 流动资产 - 总额 | Matrix | 50% | 576 |
| fnd6_cptnewqv1300_apq | 应付账款/债权人 - 贸易 | Matrix | 50% | 944 |
| fnd6_cptnewqv1300_atq | 资产 - 总计 | Matrix | 50% | 834 |
| fnd6_cptnewqv1300_ceqq | 普通股本/普通股本 - 总额 | Matrix | 50% | 800 |
| fnd6_cptnewqv1300_dlttq | 长期债务 - 总额 | Matrix | 50% | 1206 |
| fnd6_cptnewqv1300_dpq | 折旧与摊销 - 总计 | Matrix | 50% | 501 |
| fnd6_cptnewqv1300_epsf12 | 每股收益（稀释后）- 不含非常项目 - 12个月移动 | Matrix | 50% | 846 |
| fnd6_cptnewqv1300_epsfxq | 每股收益（稀释后）——不含特别项目 | Matrix | 50% | 918 |
| fnd6_cptnewqv1300_epsx12 | 每股收益（基础）- 不包括特别项目 - 12个月内搬迁 | Matrix | 50% | 682 |
| fnd6_cptnewqv1300_lctq | 流动负债 - 总额 | Matrix | 50% | 916 |
| fnd6_cptnewqv1300_ltq | 负债 - 总额 | Matrix | 50% | 770 |
| fnd6_cptnewqv1300_nopiq | 非营业收入（费用）- 总额 | Matrix | 50% | 1006 |
| fnd6_cptnewqv1300_oeps12 | 运营每股收益 - 12个月移动 | Matrix | 50% | 1028 |
| fnd6_cptnewqv1300_oiadpq | 折旧后营业收入 - 季度 | Matrix | 50% | 1100 |
| fnd6_cptnewqv1300_oibdpq | 折旧前营业收入 - 季度 | Matrix | 50% | 851 |
| fnd6_cptnewqv1300_opepsq | 运营每股收益 | Matrix | 50% | 922 |
| fnd6_cptnewqv1300_rectq | 应收账款 - 总计 | Matrix | 50% | 978 |
| fnd6_cptnewqv1300_req | 留存收益 | Matrix | 50% | 471 |
| fnd6_cptnewqv1300_saleq | 销售/营业额（净额） | Matrix | 50% | 532 |
| fnd6_cptrank_gvkeymap | 公司技术代码，不需要用来做研究 | Matrix | 50% | 109 |
| fnd6_cshpri | 用于计算每股收益的普通股 - 基础 | Matrix | 50% | 669 |
| fnd6_cshr | 普通股东/普通股东 | Matrix | 50% | 569 |
| fnd6_cshtr | 普通股交易量 - 年度 | Matrix | 50% | 1397 |
| fnd6_cshtrq | 普通股交易量 - 季度 | Matrix | 50% | 1175 |
| fnd6_cstkcv | 普通股资产负债 | Matrix | 50% | 753 |
| fnd6_cstkcvq | 普通股资产负债 | Matrix | 50% | 960 |
| fnd6_curcddv | ISO货币代码 - 股息 | Vector | 50% | 9 |
| fnd6_currencya_curcd | ISO货币代码 - 公司年度市场 | Matrix | 50% | 2765 |
| fnd6_currencyqv1300_curcd | ISO货币代码 - 公司年度市场 | Matrix | 50% | 1441 |
| fnd6_dc | 延期指控 | Matrix | 50% | 1043 |
| fnd6_dclo | 债务——资本化租赁义务 | Matrix | 50% | 860 |
| fnd6_dcpstk | 可转换债务与优先股 | Matrix | 50% | 570 |
| fnd6_dcvsr | 债务 - 高级可转换债券 | Matrix | 50% | 748 |
| fnd6_dcvsub | 债务 - 次级可转换债券 | Matrix | 50% | 481 |
| fnd6_dcvt | 债务 - 可转换债券 | Matrix | 50% | 936 |
| fnd6_dd | 债务 - 债券 | Matrix | 50% | 689 |
| fnd6_dd1 | 1年后到期的长期债务 | Matrix | 50% | 1612 |
| fnd6_dd1q | 1年后到期的长期债务 | Matrix | 50% | 840 |
| fnd6_dd2 | 二年级到期的债务 | Matrix | 50% | 633 |
| fnd6_dd3 | 三年级到期的债务 | Matrix | 50% | 1342 |
| fnd6_dd4 | 四年级到期的债务 | Matrix | 50% | 367 |
| fnd6_dd5 | 五年级到期的债务 | Matrix | 50% | 333 |
| fnd6_dilavx | 稀释可用——不包括特殊物品 | Matrix | 50% | 438 |
| fnd6_divd | 现金股息 - 每日 | Vector | 50% | 5 |
| fnd6_dlcch | 当前债务——变动 | Matrix | 50% | 249 |
| fnd6_dltis | 长期债务——发行 | Matrix | 50% | 602 |
| fnd6_dlto | 债务 - 长期 - 其他 | Matrix | 50% | 2265 |
| fnd6_dltp | 长期债务——与Prime挂钩 | Matrix | 50% | 356 |
| fnd6_dltr | 长期债务——减少 | Matrix | 50% | 1642 |
| fnd6_dm | 债务——抵押贷款及其他担保 | Matrix | 50% | 673 |
| fnd6_dn | 债务 - 注释 | Matrix | 50% | 432 |
| fnd6_donr | 非周期性椎间盘手术 | Matrix | 50% | 597 |
| fnd6_dps | 折旧与摊销 | Vector | 50% | 59 |
| fnd6_dpvieb | 累计折旧 - 期末余额（附表VI） | Matrix | 50% | 540 |
| fnd6_drc | 递延收入 - 当前 | Matrix | 50% | 8083 |
| fnd6_drlt | 递延收入——长期 | Matrix | 50% | 8563 |
| fnd6_ds | 债务 - 从属 | Matrix | 50% | 3497 |
| fnd6_dudd | 债务——未摊销债务折扣及其他 | Matrix | 50% | 820 |
| fnd6_dvpa | 优先股息的拖欠 | Matrix | 50% | 792 |
| fnd6_dvrated | 指示年股息率 - 每日 | Vector | 50% | 29 |
| fnd6_dxd2 | 债务（不含资本化租赁）——第二年到期 | Matrix | 50% | 283 |
| fnd6_dxd3 | 债务（不含资本化租赁）——第三年到期 | Matrix | 50% | 509 |
| fnd6_dxd4 | 债务（不含资本化租赁）——第四年到期 | Matrix | 50% | 344 |
| fnd6_dxd5 | 债务（不含资本化租赁）——第五年到期 | Matrix | 50% | 221 |
| fnd6_ein | 公司的雇主识别号码代码 | Matrix | 50% | 4569 |
| fnd6_emps | 员工 | Vector | 50% | 593 |
| fnd6_esopct | 常见员工持股计划义务 - 总额 | Matrix | 50% | 488 |
| fnd6_esopnr | 优先员工持股计划义务 - 不可兑换 | Matrix | 50% | 744 |
| fnd6_esopr | 优先员工持股计划义务 - 可兑换 | Matrix | 50% | 635 |
| fnd6_esubc | 净亏损中的股本 - 盈利 | Matrix | 50% | 498 |
| fnd6_esubs | 盈余中的公平 | Vector | 50% | 33 |
| fnd6_eventv110_aqdq | 收购/合并稀释EPS效应 | Vector | 50% | 8 |
| fnd6_eventv110_aqepsq | 收购/合并基本每股收益效应 | Vector | 50% | 13 |
| fnd6_eventv110_cstkcvq | 普通股 - 账面价值 | Vector | 50% | 402 |
| fnd6_eventv110_dd1q | 1年到期的长期债务 | Vector | 50% | 51 |
| fnd6_eventv110_dtedq | 债务稀释EPS效应的消除 | Vector | 50% | 172 |
| fnd6_eventv110_dteepsq | 债务消除基本每股收益效应 | Vector | 50% | 598 |
| fnd6_eventv110_gdwlid12 | 稀释EPS的损伤 - 12毫米 | Vector | 50% | 34 |
| fnd6_eventv110_gdwlidq | 商誉损减稀释每股收益效应 | Vector | 50% | 6 |
| fnd6_eventv110_gdwlieps12 | 商誉损减基础每股收益效应1200万 | Vector | 50% | 42 |
| fnd6_eventv110_gdwliepsq | 商誉基础每股收益受损效应 | Vector | 50% | 4 |
| fnd6_eventv110_gldq | 盈亏稀释EPS效应 | Vector | 50% | 148 |
| fnd6_eventv110_glepsq | 收益/亏损基础每股收益效应 | Vector | 50% | 68 |
| fnd6_eventv110_npq | 应付票据 | Vector | 50% | 835 |
| fnd6_eventv110_nrtxtdq | 非经常性所得税稀释每股收益效应 | Vector | 50% | 8 |
| fnd6_eventv110_nrtxtepsq | 非经常所得税基本每股收益效应 | Vector | 50% | 11 |
| fnd6_eventv110_optdrq | 股息率 - 假设（%） | Vector | 50% | 72 |
| fnd6_eventv110_optlifeq | 期权生涯 - 假设（# 年） | Vector | 50% | 1674 |
| fnd6_eventv110_optvolq | 波动率 - 假设（%） | Vector | 50% | 2579 |
| fnd6_eventv110_pncd12 | 核心养老金调整稀释每股收益效应1200万 | Vector | 50% | 35 |
| fnd6_eventv110_pncdq | 核心养老金调整稀释EPS效应 | Vector | 50% | 35 |
| fnd6_eventv110_pnceps12 | 核心养老金调整 基本每股收益效应 1200万 | Vector | 50% | 52 |
| fnd6_eventv110_pncepsq | 核心养老金调整 基本每股收益效应 | Vector | 50% | 34 |
| fnd6_eventv110_pncidq | 核心养老金利息调整稀释每股收益效应 | Vector | 50% | 5 |
| fnd6_eventv110_pncwidq | 核心养老金无利息调整 EPS稀释效应 | Vector | 50% | 3 |
| fnd6_eventv110_pncwiepsq | 核心养老金无利息调整 基本每股收益效应 | Vector | 50% | 5 |
| fnd6_eventv110_setdq | 和解（诉讼/保险）稀释EPS效应 | Vector | 50% | 85 |
| fnd6_eventv110_setepsq | 和解（诉讼/保险）基本EPS效应 | Vector | 50% | 156 |
| fnd6_eventv110_spced12 | 标普核心盈利每股净化1200万股 | Vector | 50% | 41 |
| fnd6_eventv110_spidq | 其他特殊物品稀释EPS效应 | Vector | 50% | 10 |
| fnd6_eventv110_spiepsq | 其他特殊物品 基础EPS效果 | Vector | 50% | 10 |
| fnd6_eventv110_txdbcaq | 当前递延税款资产 | Vector | 50% | 82 |
| fnd6_eventv110_txdbclq | 当前递延税负 | Vector | 50% | 347 |
| fnd6_eventv110_wddq | 减记稀释EPS效应 | Vector | 50% | 12 |
| fnd6_eventv110_wdepsq | 减记 基本每股收益效应 | Vector | 50% | 55 |
| fnd6_eventv110_xaccq | 应计费用 | Vector | 50% | 239 |
| fnd6_exre | 汇率效应 | Matrix | 50% | 1900 |
| fnd6_fatb | 工厂、物业和设备成本价——建筑物 | Matrix | 50% | 615 |
| fnd6_fatc | 工厂、财产和设备成本价——建设进行中 | Matrix | 50% | 554 |
| fnd6_fate | 工厂、物业和设备成本价 - 机械与设备 | Matrix | 50% | 339 |
| fnd6_fatl | 物业、工厂和设备——按成本租赁 | Matrix | 50% | 4604 |
| fnd6_fatn | 财产、工厂和设备——自然资源按成本计算 | Matrix | 50% | 284 |
| fnd6_fato | 工厂、财产和设备成本价 - 其他 | Matrix | 50% | 478 |
| fnd6_fatp | 工厂、物业和设备成本价——土地与改良 | Matrix | 50% | 467 |
| fnd6_fiao | 融资活动 - 其他 | Matrix | 50% | 509 |
| fnd6_fic | 标识公司注册或注册的国家 | Matrix | 50% | 1109 |
| fnd6_fopo | 运营资金 - 其他 | Matrix | 50% | 8894 |
| fnd6_fopox | 运营资金——其他排除期权税收优惠 | Matrix | 50% | 1502 |
| fnd6_fyrc | 无关紧要的技术代码，出于研究目的请忽略 | Matrix | 50% | 1420 |
| fnd6_gdwls | 善意 | Vector | 50% | 42 |
| fnd6_ias | 可识别（总资产） | Vector | 50% | 42 |
| fnd6_ibmii | 收入优先于非常物品和非控制权益 | Matrix | 50% | 711 |
| fnd6_ibs | 非凡物品之前的收入 | Vector | 50% | 30 |
| fnd6_idesindq_curcd | ISO货币代码 - 公司年度市场 | Matrix | 50% | 1666 |
| fnd6_idit | 利息及相关收入 - 总额 | Matrix | 50% | 410 |
| fnd6_iints | 利息收入 | Vector | 50% | 22 |
| fnd6_incorp | 注册 | Matrix | 50% | 1559 |
| fnd6_intan | 无形资产 - 总计 | Matrix | 50% | 892 |
| fnd6_intc | 资本化利息 | Matrix | 50% | 2165 |
| fnd6_intpn | 已支付利息 - 净额 | Matrix | 50% | 438 |
| fnd6_intseg | 跨段淘汰赛 | Vector | 50% | 97 |
| fnd6_invfg | 库存 - 成品 | Matrix | 50% | 444 |
| fnd6_invo | 库存 - 其他 | Matrix | 50% | 306 |
| fnd6_invrm | 库存 - 原材料 | Matrix | 50% | 516 |
| fnd6_invwip | 库存 - 在品 | Matrix | 50% | 559 |
| fnd6_itcb | 投资税收抵免（资产负债表） | Matrix | 50% | 555 |
| fnd6_itci | 投资税收抵免（收入账户） | Matrix | 50% | 1799 |
| fnd6_ivaco | 投资活动 - 其他 | Matrix | 50% | 7932 |
| fnd6_ivaeq | 投资与贷款 - 股权 | Matrix | 50% | 636 |
| fnd6_ivaeqs | 在Equity的投资 | Vector | 50% | 25 |
| fnd6_ivao | 投资与贷款 - 其他 | Matrix | 50% | 526 |
| fnd6_ivch | 投资增加 | Matrix | 50% | 264 |
| fnd6_ivst | 短期投资 - 总计 | Matrix | 50% | 430 |
| fnd6_ivstch | 短期投资——变革 | Matrix | 50% | 356 |
| fnd6_lcox | 流动负债 - 其他 - 杂项 | Matrix | 50% | 2822 |
| fnd6_lcoxdr | 流动负债 - 其他 - 不包括递延收入 | Matrix | 50% | 2264 |
| fnd6_lifr | 后进先出储备区 | Matrix | 50% | 1208 |
| fnd6_lno | 负债净额及其他调整 | Matrix | 50% | 259 |
| fnd6_loc | 用于定位公司总部的字符串 | Matrix | 50% | 1220 |
| fnd6_lol2 | 负债等级2（可观测） | Matrix | 50% | 318 |
| fnd6_loxdr | 负债 - 其他 - 不包括递延收入 | Matrix | 50% | 1948 |
| fnd6_lqpl1 | 负债等级1（报价） | Matrix | 50% | 323 |
| fnd6_lul3 | 负债等级3（不可观测） | Matrix | 50% | 320 |
| fnd6_mfma1_aoloch | 资产与负债 - 其他 - 净变动 | Matrix | 50% | 756 |
| fnd6_mfma1_apalch | 应付账款和应计负债——增加/（减少） | Matrix | 50% | 484 |
| fnd6_mfma1_at | 资产 - 总计 | Matrix | 50% | 1211 |
| fnd6_mfma1_capx | 资本支出 | Matrix | 50% | 600 |
| fnd6_mfma1_csho | 普通股流通 | Matrix | 50% | 879 |
| fnd6_mfma1_dp | 折旧与摊销 | Matrix | 50% | 472 |
| fnd6_mfma1_dpc | 折旧与摊销（现金流） | Matrix | 50% | 645 |
| fnd6_mfma1_invch | 抵押贷款 - 减少（增加） | Matrix | 50% | 556 |
| fnd6_mfma2_oancf | 运营活动 - 净现金流 | Matrix | 50% | 678 |
| fnd6_mfma2_opeps | 运营每股收益 | Matrix | 50% | 1015 |
| fnd6_mfma2_recch | 应收账款 - 减少（增加） | Matrix | 50% | 560 |
| fnd6_mfma2_revt | 收入 - 总额 | Matrix | 50% | 818 |
| fnd6_mfma2_txach | 所得税 - 应计税 - 增加/（减少） | Matrix | 50% | 434 |
| fnd6_mfmq_cheq | 现金与短期投资 | Matrix | 50% | 565 |
| fnd6_mfmq_cogsq | 销售成本 | Matrix | 50% | 433 |
| fnd6_mfmq_cshprq | 用于计算每股收益的普通股 - 基础 | Matrix | 50% | 1202 |
| fnd6_mfmq_dlcq | 流动负债中的债务 | Matrix | 50% | 232 |
| fnd6_mfmq_ibcomq | 特殊物品前的收入——适用于普通物品 | Matrix | 50% | 473 |
| fnd6_mfmq_mibtq | 非控股权益 - 总额 - 资产负债表 - 季度 | Matrix | 50% | 269 |
| fnd6_mfmq_piq | 税前收入 | Matrix | 50% | 687 |
| fnd6_mibn | 非控制权益 - 不可赎回 - 资产负债表 | Matrix | 50% | 780 |
| fnd6_mibt | 非控股权益 - 总额 - 资产负债表 | Matrix | 50% | 596 |
| fnd6_mkvalt | 市场价值 - 总额 | Matrix | 50% | 312 |
| fnd6_mkvaltq | 市场价值 - 总额 | Matrix | 50% | 139 |
| fnd6_mrc1 | 租金最低义务 - 第一年 | Matrix | 50% | 1458 |
| fnd6_mrc2 | 租金承诺 - 最低 - 第二年 | Matrix | 50% | 1900 |
| fnd6_mrc3 | 租金承诺 - 最低 - 第三年 | Matrix | 50% | 1317 |
| fnd6_mrc4 | 租金义务 - 最低 - 第4年 | Matrix | 50% | 1506 |
| fnd6_mrc5 | 租金承诺 - 最低 - 第五年 | Matrix | 50% | 1719 |
| fnd6_mrct | 租金承诺 - 最低 - 总计5年 | Matrix | 50% | 1326 |
| fnd6_mrcta | 之后的租赁部分 | Matrix | 50% | 5537 |
| fnd6_msa | 可流通证券调整 | Matrix | 50% | 707 |
| fnd6_naicss | NAICS代码 | Vector | 50% | 1620 |
| fnd6_newa1v1300_aco | 流动资产 - 其他 - 总额 | Matrix | 50% | 1212 |
| fnd6_newa1v1300_acominc | 累计其他综合收入（损失） | Matrix | 50% | 834 |
| fnd6_newa1v1300_act | 流动资产 - 总额 | Matrix | 50% | 1558 |
| fnd6_newa1v1300_ano | 资产净额及其他调整 | Matrix | 50% | 346 |
| fnd6_newa1v1300_ao | 资产 - 其他 | Matrix | 50% | 560 |
| fnd6_newa1v1300_aocidergl | Accum Other Comp Inc - 衍生品未实现盈亏 | Matrix | 50% | 294 |
| fnd6_newa1v1300_aociother | Accum 其他保险公司 - 其他调整 | Matrix | 50% | 396 |
| fnd6_newa1v1300_aocipen | Accum Other Comp Inc - Min Pension Liab Adj | Matrix | 50% | 359 |
| fnd6_newa1v1300_aol2 | 资产等级2（可观察） | Matrix | 50% | 200 |
| fnd6_newa1v1300_aoloch | 资产与负债 - 其他 - 净变动 | Matrix | 50% | 582 |
| fnd6_newa1v1300_ap | 应付账款 - 贸易 | Matrix | 50% | 671 |
| fnd6_newa1v1300_apalch | 应付账款和应计负债——增加/（减少） | Matrix | 50% | 588 |
| fnd6_newa1v1300_aqpl1 | 资产等级1（报价价格） | Matrix | 50% | 184 |
| fnd6_newa1v1300_at | 资产 - 总计 | Matrix | 50% | 854 |
| fnd6_newa1v1300_aul3 | 资产等级3（不可观察） | Matrix | 50% | 329 |
| fnd6_newa1v1300_bkvlps | 每股账面价值 | Matrix | 50% | 936 |
| fnd6_newa1v1300_caps | 资本盈余/股份权利金储备 | Matrix | 50% | 369 |
| fnd6_newa1v1300_capx | 资本支出 | Matrix | 50% | 660 |
| fnd6_newa1v1300_ceq | 普通股本/普通股本 - 总额 | Matrix | 50% | 771 |
| fnd6_newa1v1300_ceqt | 普通股权——有形资产 | Matrix | 50% | 460 |
| fnd6_newa1v1300_che | 现金与短期投资 | Matrix | 50% | 405 |
| fnd6_newa1v1300_chech | 现金及其等值现金——增加/（减少） | Matrix | 50% | 623 |
| fnd6_newa1v1300_cogs | 销售成本 | Matrix | 50% | 654 |
| fnd6_newa1v1300_cshfd | 用于计算每股收益的普通股——完全稀释 | Matrix | 50% | 726 |
| fnd6_newa1v1300_cshi | 发行普通股 | Matrix | 50% | 211 |
| fnd6_newa1v1300_csho | 普通股流通 | Matrix | 50% | 487 |
| fnd6_newa1v1300_cstk | 普通股/普通股（资本） | Matrix | 50% | 804 |
| fnd6_newa1v1300_dcom | 递延补偿 | Matrix | 50% | 1017 |
| fnd6_newa1v1300_dlc | 流动负债中的债务——总计 | Matrix | 50% | 1072 |
| fnd6_newa1v1300_dltt | 长期债务 - 总额 | Matrix | 50% | 1124 |
| fnd6_newa1v1300_dp | 折旧与摊销 | Matrix | 50% | 348 |
| fnd6_newa1v1300_dpact | 折旧、耗尽与摊销（累计） | Matrix | 50% | 334 |
| fnd6_newa1v1300_dpc | 折旧与摊销（现金流） | Matrix | 50% | 672 |
| fnd6_newa1v1300_dv | 现金红利（现金流） | Matrix | 50% | 433 |
| fnd6_newa1v1300_dvc | 普通/普通股息 | Matrix | 50% | 556 |
| fnd6_newa1v1300_dvt | 股息 - 总额 | Matrix | 50% | 279 |
| fnd6_newa1v1300_ebit | 息税前利润 | Matrix | 50% | 372 |
| fnd6_newa1v1300_ebitda | 息前收益 | Matrix | 50% | 437 |
| fnd6_newa1v1300_emp | 员工 | Matrix | 50% | 753 |
| fnd6_newa1v1300_epsfi | 每股收益（稀释后）——包括非凡项目 | Matrix | 50% | 719 |
| fnd6_newa1v1300_epsfx | 每股收益（稀释后）——不包括非常项 | Matrix | 50% | 614 |
| fnd6_newa1v1300_epspi | 每股收益（基础）——包括非凡项目 | Matrix | 50% | 621 |
| fnd6_newa1v1300_epspx | 每股收益（基础）——不包括特别项目 | Matrix | 50% | 435 |
| fnd6_newa1v1300_fca | 外汇收入（亏损） | Matrix | 50% | 178 |
| fnd6_newa1v1300_fincf | 融资活动 - 净现金流 | Matrix | 50% | 851 |
| fnd6_newa1v1300_gdwl | 善意 | Matrix | 50% | 388 |
| fnd6_newa1v1300_gp | 毛利（亏损） | Matrix | 50% | 2393 |
| fnd6_newa1v1300_ib | 非凡物品之前的收入 | Matrix | 50% | 313 |
| fnd6_newa1v1300_ibadj | 非凡项目前的收入——调整普通股等价项 | Matrix | 50% | 297 |
| fnd6_newa1v1300_ibc | 非凡项目前的收入（现金流） | Matrix | 50% | 693 |
| fnd6_newa1v1300_ibcom | 特殊物品前的收入——适用于普通物品 | Matrix | 50% | 234 |
| fnd6_newa1v1300_icapt | 投资资本 - 总额 | Matrix | 50% | 437 |
| fnd6_newa1v1300_intano | 其他无形资产 | Matrix | 50% | 517 |
| fnd6_newa1v1300_invch | 抵押贷款 - 减少（增加） | Matrix | 50% | 529 |
| fnd6_newa1v1300_invt | 库存 - 总计 | Matrix | 50% | 508 |
| fnd6_newa1v1300_ivncf | 投资活动 - 净现金流 | Matrix | 50% | 432 |
| fnd6_newa1v1300_lco | 流动负债 - 其他 - 总额 | Matrix | 50% | 827 |
| fnd6_newa1v1300_lct | 流动负债 - 总额 | Matrix | 50% | 931 |
| fnd6_newa1v1300_lo | 负债 - 其他 - 总额 | Matrix | 50% | 1343 |
| fnd6_newa1v1300_lse | 负债与股东权益 - 总计 | Matrix | 50% | 503 |
| fnd6_newa1v1300_lt | 负债 - 总额 | Matrix | 50% | 735 |
| fnd6_newa2v1300_mib | 少数股权（资产负债表） | Matrix | 50% | 779 |
| fnd6_newa2v1300_mii | 非控制性利息（收入账户） | Matrix | 50% | 626 |
| fnd6_newa2v1300_ni | 净收入（亏损） | Matrix | 50% | 1462 |
| fnd6_newa2v1300_nopi | 非营业收入（费用） | Matrix | 50% | 339 |
| fnd6_newa2v1300_oancf | 运营活动 - 净现金流 | Matrix | 50% | 578 |
| fnd6_newa2v1300_oiadp | 折旧后的营业收入 | Matrix | 50% | 1121 |
| fnd6_newa2v1300_oibdp | 折旧前营业收入 | Matrix | 50% | 2834 |
| fnd6_newa2v1300_opeps | 运营每股收益 | Matrix | 50% | 730 |
| fnd6_newa2v1300_optexd | 期权 - 已行使（-） | Matrix | 50% | 1662 |
| fnd6_newa2v1300_pi | 税前收入 | Matrix | 50% | 376 |
| fnd6_newa2v1300_ppegt | 物业、工厂和设备 - 总计（毛） | Matrix | 50% | 730 |
| fnd6_newa2v1300_ppent | 物业、厂房和设备 - 总计（净） | Matrix | 50% | 6938 |
| fnd6_newa2v1300_prsho | 赎回公益分成股份（000） | Matrix | 50% | 2102 |
| fnd6_newa2v1300_rdip | 在审研发费用 | Matrix | 50% | 706 |
| fnd6_newa2v1300_rdipa | 在批研发费用税后 | Matrix | 50% | 971 |
| fnd6_newa2v1300_rdipd | 在审理中研发费用稀释每股收益影响 | Matrix | 50% | 1960 |
| fnd6_newa2v1300_rdipeps | 在工时研发费用基础每股收益影响 | Matrix | 50% | 3632 |
| fnd6_newa2v1300_re | 留存收益 | Matrix | 50% | 522 |
| fnd6_newa2v1300_recch | 应收账款 - 减少（增加） | Matrix | 50% | 435 |
| fnd6_newa2v1300_rect | 应收账款 - 总计 | Matrix | 50% | 540 |
| fnd6_newa2v1300_reuna | 留存收益 - 未调整 | Matrix | 50% | 636 |
| fnd6_newa2v1300_revt | 收入 - 总额 | Matrix | 50% | 569 |
| fnd6_newa2v1300_sale | 销售/营业额（净额） | Matrix | 50% | 503 |
| fnd6_newa2v1300_seq | 股东权益 - 母公司 | Matrix | 50% | 952 |
| fnd6_newa2v1300_seqo | 其他股东权益调整 | Matrix | 50% | 662 |
| fnd6_newa2v1300_spced | 标普核心盈余每股收益被稀释 | Matrix | 50% | 206 |
| fnd6_newa2v1300_spceeps | 标普核心收益每股基础 | Matrix | 50% | 269 |
| fnd6_newa2v1300_spi | 特殊物品 | Matrix | 50% | 606 |
| fnd6_newa2v1300_stkco | 股票补偿费用 | Matrix | 50% | 497 |
| fnd6_newa2v1300_tstk | 国债股 - 总计（全部资本） | Matrix | 50% | 250 |
| fnd6_newa2v1300_tstkn | 国债 - 普通股数量 | Matrix | 50% | 205 |
| fnd6_newa2v1300_txach | 所得税 - 应计税 - 增加/（减少） | Matrix | 50% | 182 |
| fnd6_newa2v1300_txdb | 递延税款 - 资产负债表 | Matrix | 50% | 382 |
| fnd6_newa2v1300_txditc | 递延税款与投资税收抵免 | Matrix | 50% | 343 |
| fnd6_newa2v1300_txp | 应缴所得税 | Matrix | 50% | 342 |
| fnd6_newa2v1300_txt | 所得税 - 总计 | Matrix | 50% | 482 |
| fnd6_newa2v1300_wcap | 营运资金（资产负债表） | Matrix | 50% | 453 |
| fnd6_newa2v1300_xidoc | 非常项与已停止运营（现金流） | Matrix | 50% | 1540 |
| fnd6_newa2v1300_xint | 利息及相关费用 - 总额 | Matrix | 50% | 564 |
| fnd6_newa2v1300_xoptd | 隐含期权每股收益稀释 | Matrix | 50% | 130 |
| fnd6_newa2v1300_xopteps | 隐含期权EPS基础 | Matrix | 50% | 28 |
| fnd6_newa2v1300_xrd | 研发费用 | Matrix | 50% | 470 |
| fnd6_newa2v1300_xsga | 销售、一般及行政费用 | Matrix | 50% | 2784 |
| fnd6_newq_xoptdqp | 隐含期权每股收益稀释初步 | Matrix | 50% | 5 |
| fnd6_newq_xoptepsqp | 隐含期权EPS基础初步 | Matrix | 50% | 21 |
| fnd6_newq_xoptqp | 隐含期权费用初步报告 | Matrix | 50% | 20 |
| fnd6_newqeventv110_acchgq | 会计变更——累积影响 | Vector | 50% | 450 |
| fnd6_newqeventv110_acomincq | 累计其他综合收入（损失） | Vector | 50% | 87 |
| fnd6_newqeventv110_acoq | 流动资产 - 其他 - 总额 | Vector | 50% | 82 |
| fnd6_newqeventv110_altoq | 其他长期资产 | Vector | 50% | 230 |
| fnd6_newqeventv110_ancq | 非流动资产 - 总额 | Vector | 50% | 22 |
| fnd6_newqeventv110_anoq | 资产净额及其他调整 | Vector | 50% | 31 |
| fnd6_newqeventv110_aociderglq | 累计其他综合收益 - 衍生品未实现盈亏 | Vector | 50% | 374 |
| fnd6_newqeventv110_aociotherq | Accum 其他保险公司 - 其他调整 | Vector | 50% | 43 |
| fnd6_newqeventv110_aocipenq | Accum Other Comp Inc - Min Pension Liab Adj | Vector | 50% | 59 |
| fnd6_newqeventv110_aocisecglq | 积蓄。Other Comp. Inc. - Unreal G/L 注册国际资产 | Vector | 50% | 76 |
| fnd6_newqeventv110_aol2q | 资产等级2（可观察） | Vector | 50% | 71 |
| fnd6_newqeventv110_aoq | 资产 - 其他 - 总额 | Vector | 50% | 46 |
| fnd6_newqeventv110_aqaq | 税后收购/合并 | Vector | 50% | 24 |
| fnd6_newqeventv110_aqpl1q | 资产等级1（报价价格） | Vector | 50% | 211 |
| fnd6_newqeventv110_aqpq | 税前收购/合并 | Vector | 50% | 18 |
| fnd6_newqeventv110_aul3q | 资产等级3（不可观察） | Vector | 50% | 31 |
| fnd6_newqeventv110_capsq | 资本盈余/股份权利金储备 | Vector | 50% | 103 |
| fnd6_newqeventv110_cheq | 现金与短期投资 | Vector | 50% | 589 |
| fnd6_newqeventv110_chq | 现金 | Vector | 50% | 305 |
| fnd6_newqeventv110_cibegniq | Comp Inc - 初始净收入 | Vector | 50% | 45 |
| fnd6_newqeventv110_cicurrq | Comp Inc - Currency Trans Adj | Vector | 50% | 66 |
| fnd6_newqeventv110_ciderglq | 综合收益——衍生品收益/损失 | Vector | 50% | 21 |
| fnd6_newqeventv110_cimiiq | 综合收益 - 非控制权益 | Vector | 50% | 29 |
| fnd6_newqeventv110_ciotherq | 综合收入——其他调整 | Vector | 50% | 83 |
| fnd6_newqeventv110_cipenq | Comp Inc - 最低养老金附加项 | Vector | 50% | 50 |
| fnd6_newqeventv110_ciq | 综合收入 - 总额 | Vector | 50% | 70 |
| fnd6_newqeventv110_cisecglq | Comp Inc - 证券收益/亏损 | Vector | 50% | 31 |
| fnd6_newqeventv110_citotalq | 综合收入 - 母公司 | Vector | 50% | 45 |
| fnd6_newqeventv110_cogsq | 销售成本 | Vector | 50% | 217 |
| fnd6_newqeventv110_csh12q | 用于计算每股收益的普通股 - 12个月移动 | Vector | 50% | 66 |
| fnd6_newqeventv110_cshfdq | 稀释每股收益的普通股 | Vector | 50% | 56 |
| fnd6_newqeventv110_cshiq | 发行普通股 | Vector | 50% | 315 |
| fnd6_newqeventv110_cshopq | 季度回购总股份 | Vector | 50% | 461 |
| fnd6_newqeventv110_cshoq | 普通股流通 | Vector | 50% | 61 |
| fnd6_newqeventv110_cshprq | 用于计算每股收益的普通股 - 基础 | Vector | 50% | 63 |
| fnd6_newqeventv110_cstkeq | 普通股等价物 - 美元节省 | Vector | 50% | 757 |
| fnd6_newqeventv110_cstkq | 普通股/普通股（资本） | Vector | 50% | 29 |
| fnd6_newqeventv110_dcomq | 递延补偿 | Vector | 50% | 57 |
| fnd6_newqeventv110_diladq | 稀释调整 | Vector | 50% | 721 |
| fnd6_newqeventv110_dilavq | 稀释可用——不包括特殊物品 | Vector | 50% | 42 |
| fnd6_newqeventv110_dlcq | 流动负债中的债务 | Vector | 50% | 390 |
| fnd6_newqeventv110_doq | 已停止运营 | Vector | 50% | 15 |
| fnd6_newqeventv110_dpactq | 折旧、耗尽与摊销（累计） | Vector | 50% | 20 |
| fnd6_newqeventv110_drcq | 递延收入 - 当前 | Vector | 50% | 1075 |
| fnd6_newqeventv110_drltq | 递延收入——长期 | Vector | 50% | 2576 |
| fnd6_newqeventv110_dteaq | 税后债务的消灭 | Vector | 50% | 388 |
| fnd6_newqeventv110_dtepq | 税前债务的消除 | Vector | 50% | 333 |
| fnd6_newqeventv110_dvpq | 股息 - 优先/优先 | Vector | 50% | 30 |
| fnd6_newqeventv110_epsfiq | 每股收益（稀释后）——包括非凡项目 | Vector | 50% | 54 |
| fnd6_newqeventv110_epspiq | 每股收益（基础）——包括非凡项目 | Vector | 50% | 32 |
| fnd6_newqeventv110_epspxq | 每股收益（基础）——不包括特别项目 | Vector | 50% | 39 |
| fnd6_newqeventv110_esopctq | 常见员工持股计划义务 - 总额 | Vector | 50% | 51 |
| fnd6_newqeventv110_esopnrq | 优先员工持股计划义务 - 不可兑换 | Vector | 50% | 31 |
| fnd6_newqeventv110_esoprq | 优先员工持股计划义务 - 可兑换 | Vector | 50% | 837 |
| fnd6_newqeventv110_esoptq | 优先员工持股计划义务 - 总额 | Vector | 50% | 149 |
| fnd6_newqeventv110_fcaq | 外汇收入（亏损） | Vector | 50% | 26 |
| fnd6_newqeventv110_gdwlamq | 商誉摊销 | Vector | 50% | 13 |
| fnd6_newqeventv110_gdwlia12 | 税后商誉减损 - 1200万 | Vector | 50% | 41 |
| fnd6_newqeventv110_gdwliaq | 税后商誉损耗 | Vector | 50% | 13 |
| fnd6_newqeventv110_gdwlipq | 税前商誉损耗 | Vector | 50% | 11 |
| fnd6_newqeventv110_gdwlq | 善意（网络） | Vector | 50% | 108 |
| fnd6_newqeventv110_glaq | 税后盈亏 | Vector | 50% | 23 |
| fnd6_newqeventv110_glcea12 | 销售盈亏（核心收益调整后）税后1200万 | Vector | 50% | 228 |
| fnd6_newqeventv110_glceaq | 税后销售盈亏（核心收益调整后） | Vector | 50% | 67 |
| fnd6_newqeventv110_glced12 | 销售盈亏（核心利润调整后）稀释每股收益影响 1200万 | Vector | 50% | 106 |
| fnd6_newqeventv110_glcedq | 销售盈亏（核心收益调整后）稀释每股收益 | Vector | 50% | 169 |
| fnd6_newqeventv110_glceeps12 | 销售盈亏（核心收益调整后）基本每股收益影响1200万 | Vector | 50% | 53 |
| fnd6_newqeventv110_glceepsq | 销售盈亏（核心收益调整后）基本每股收益效应 | Vector | 50% | 309 |
| fnd6_newqeventv110_glcepq | 销售盈亏（核心收益调整后）税前 | Vector | 50% | 147 |
| fnd6_newqeventv110_glpq | 税前收益/损失 | Vector | 50% | 17 |
| fnd6_newqeventv110_hedgeglq | 无效对冲的收益/损失 | Vector | 50% | 15 |
| fnd6_newqeventv110_ibadj12 | 额外物品前的收入——普通股等价物的附加值 - 1200万 | Vector | 50% | 6 |
| fnd6_newqeventv110_ibadjq | 非凡项目前的收入——调整普通股等价项 | Vector | 50% | 21 |
| fnd6_newqeventv110_ibcomq | 特殊物品前的收入——适用于普通物品 | Vector | 50% | 16 |
| fnd6_newqeventv110_ibmiiq | 收入优先于非常物品和非控制权益 | Vector | 50% | 95 |
| fnd6_newqeventv110_ibq | 非凡物品之前的收入 | Vector | 50% | 24 |
| fnd6_newqeventv110_icaptq | 投资资本 - 总额 - 季度 | Vector | 50% | 27 |
| fnd6_newqeventv110_intanoq | 其他无形资产 | Vector | 50% | 310 |
| fnd6_newqeventv110_intanq | 无形资产 - 总计 | Vector | 50% | 67 |
| fnd6_newqeventv110_invfgq | 库存 - 成品 | Vector | 50% | 32 |
| fnd6_newqeventv110_invoq | 库存 - 其他 | Vector | 50% | 53 |
| fnd6_newqeventv110_invrmq | 库存 - 原材料 | Vector | 50% | 67 |
| fnd6_newqeventv110_invtq | 库存 - 总计 | Vector | 50% | 174 |
| fnd6_newqeventv110_invwipq | 库存——在品 | Vector | 50% | 31 |
| fnd6_newqeventv110_ivltq | 总长期投资 | Vector | 50% | 57 |
| fnd6_newqeventv110_ivstq | 短期投资 - 总计 | Vector | 50% | 48 |
| fnd6_newqeventv110_lcoq | 流动负债 - 其他 - 总额 | Vector | 50% | 143 |
| fnd6_newqeventv110_lltq | 长期负债（总额） | Vector | 50% | 28 |
| fnd6_newqeventv110_lnoq | 负债净额及其他调整 | Vector | 50% | 23 |
| fnd6_newqeventv110_lol2q | 负债等级2（可观测） | Vector | 50% | 25 |
| fnd6_newqeventv110_loq | 负债 - 其他 | Vector | 50% | 76 |
| fnd6_newqeventv110_loxdrq | 负债 - 其他 - 不包括递延收入 | Vector | 50% | 59 |
| fnd6_newqeventv110_lqpl1q | 负债等级1（报价） | Vector | 50% | 31 |
| fnd6_newqeventv110_lseq | 负债与股东权益 - 总计 | Vector | 50% | 44 |
| fnd6_newqeventv110_ltmibq | 负债——全部权益和非控制权益 | Vector | 50% | 314 |
| fnd6_newqeventv110_lul3q | 负债等级3（不可观测） | Vector | 50% | 90 |
| fnd6_newqeventv110_mibnq | 不可赎回非控制权益（资产负债表）- 季度 | Vector | 50% | 60 |
| fnd6_newqeventv110_mibq | 非控制权益 - 可赎回 - 资产负债表 | Vector | 50% | 23 |
| fnd6_newqeventv110_mibtq | 非控股权益 - 总额 - 资产负债表 - 季度 | Vector | 50% | 9 |
| fnd6_newqeventv110_miiq | 非控制性利息——收入账户 | Vector | 50% | 29 |
| fnd6_newqeventv110_msaq | Accum Other Comp Inc - 可流通证券调整 | Vector | 50% | 215 |
| fnd6_newqeventv110_nrtxtq | 非周期性所得税 - 税后 | Vector | 50% | 25 |
| fnd6_newqeventv110_oepf12 | 每股盈余 - 摊薄后 - 运营收益 - 1200万 | Vector | 50% | 108 |
| fnd6_newqeventv110_oepsxq | 每股收益 - 摊薄后 - 来自运营 | Vector | 50% | 37 |
| fnd6_newqeventv110_optfvgrq | 期权——已授予期权的公允价值 | Vector | 50% | 392 |
| fnd6_newqeventv110_optrfrq | 无风险利率 - 假设（%） | Vector | 50% | 1901 |
| fnd6_newqeventv110_piq | 税前收入 | Vector | 50% | 105 |
| fnd6_newqeventv110_pnc12 | 养老金核心调节 - 12毫米 | Vector | 50% | 28 |
| fnd6_newqeventv110_pnciapq | 核心养老金利息调整税后初步 | Vector | 50% | 7 |
| fnd6_newqeventv110_pnciaq | 核心养老金利息调整税后 | Vector | 50% | 4 |
| fnd6_newqeventv110_pncidpq | 核心养老金利息调整稀释每股收益初步影响 | Vector | 50% | 4 |
| fnd6_newqeventv110_pnciepspq | 核心养老金利息调整 基本每股收益影响 初步 | Vector | 50% | 12 |
| fnd6_newqeventv110_pnciepsq | 核心养老金利息调整基础每股收益效应 | Vector | 50% | 6 |
| fnd6_newqeventv110_pncippq | 核心养老金利息调整税前初步 | Vector | 50% | 1 |
| fnd6_newqeventv110_pncipq | 核心养老金利息调整税前 | Vector | 50% | 7 |
| fnd6_newqeventv110_pncpd12 | 核心养老金调整 1200万稀释每股收益初步影响 | Vector | 50% | 45 |
| fnd6_newqeventv110_pncpdq | 核心养老金调整稀释每股收益（EPS）初步影响 | Vector | 50% | 30 |
| fnd6_newqeventv110_pncpeps12 | 核心养老金调整 1200万 基本每股收益效果初步 | Vector | 50% | 31 |
| fnd6_newqeventv110_pncpepsq | 核心养老金调整 基本每股收益（EPS）初步影响 | Vector | 50% | 49 |
| fnd6_newqeventv110_pncpq | 核心养老金调整初步 | Vector | 50% | 44 |
| fnd6_newqeventv110_pncq | 核心养老金调整 | Vector | 50% | 18 |
| fnd6_newqeventv110_pncwiapq | 无利息调整的基础养老金 税后初步 | Vector | 50% | 5 |
| fnd6_newqeventv110_pncwiaq | 核心养老金，不含税后利息调整 | Vector | 50% | 4 |
| fnd6_newqeventv110_pncwidpq | 无利息调整的核心养老金 稀释每股收益（EPS）初步影响 | Vector | 50% | 5 |
| fnd6_newqeventv110_pncwiepq | 无利息调整的核心养老金基础每股收益（EPS）初步影响 | Vector | 50% | 3 |
| fnd6_newqeventv110_pncwippq | 无利息调整的基础养老金税前初步 | Vector | 50% | 2 |
| fnd6_newqeventv110_pncwipq | 税前无利息调整的核心养老金 | Vector | 50% | 3 |
| fnd6_newqeventv110_pnrshoq | 非红色公立股股东（000）- 季度 | Vector | 50% | 154 |
| fnd6_newqeventv110_ppegtq | 物业、厂房和设备 - 总额（总额）- 季度 | Vector | 50% | 41 |
| fnd6_newqeventv110_ppentq | 物业、设备和设备 - 总计（净） | Vector | 50% | 51 |
| fnd6_newqeventv110_prcaq | 退休后核心调整 | Vector | 50% | 15 |
| fnd6_newqeventv110_prcd12 | 核心退休后调整稀释每股收益效应 1200万 | Vector | 50% | 6 |
| fnd6_newqeventv110_prcdq | 核心退休后调整稀释每股收益效应 | Vector | 50% | 9 |
| fnd6_newqeventv110_prce12 | 核心退休后调整12毫米 | Vector | 50% | 29 |
| fnd6_newqeventv110_prceps12 | 核心退休后调整基础每股收益效应1200万 | Vector | 50% | 8 |
| fnd6_newqeventv110_prcepsq | 核心退休后调整基础每股收益效应 | Vector | 50% | 4 |
| fnd6_newqeventv110_prcpd12 | 核心退休后调整 1200万稀释每股收益 初步影响 | Vector | 50% | 8 |
| fnd6_newqeventv110_prcpdq | 核心退休后调整稀释每股收益初步 | Vector | 50% | 26 |
| fnd6_newqeventv110_prcpeps12 | 核心退休后调整 1200万基础每股收益效应初步 | Vector | 50% | 5 |
| fnd6_newqeventv110_prcpepsq | 核心退休后调整基础每股收益初步 | Vector | 50% | 16 |
| fnd6_newqeventv110_prcpq | 核心退休后调整初步 | Vector | 50% | 26 |
| fnd6_newqeventv110_prcraq | 回购价格 - 每股平均 | Vector | 50% | 1069 |
| fnd6_newqeventv110_prshoq | 赎回公益分成股份（000） | Vector | 50% | 73 |
| fnd6_newqeventv110_pstknq | 优先股/优先股 - 不可赎回 | Vector | 50% | 1211 |
| fnd6_newqeventv110_pstkq | 优先股/优先股（资本）- 总额 | Vector | 50% | 106 |
| fnd6_newqeventv110_pstkrq | 优先股/优先股 - 可赎回 | Vector | 50% | 60 |
| fnd6_newqeventv110_rcaq | 税后重组成本 | Vector | 50% | 7 |
| fnd6_newqeventv110_rcdq | 重组成本稀释EPS效应 | Vector | 50% | 5 |
| fnd6_newqeventv110_rcepsq | 重组成本 基本每股收益效应 | Vector | 50% | 6 |
| fnd6_newqeventv110_rcpq | 税前重组成本 | Vector | 50% | 65 |
| fnd6_newqeventv110_rdipaq | 正在进行的税后研发费用 | Vector | 50% | 101 |
| fnd6_newqeventv110_rdipdq | 在建研发费用稀释EPS效应 | Vector | 50% | 271 |
| fnd6_newqeventv110_rdipepsq | 在工研发费用基础每股收益效应 | Vector | 50% | 371 |
| fnd6_newqeventv110_rdipq | 研发中 | Vector | 50% | 280 |
| fnd6_newqeventv110_recdq | 应收账款——预计存疑 | Vector | 50% | 180 |
| fnd6_newqeventv110_rectaq | Accum Other Comp Inc - 累计平算调整 | Vector | 50% | 38 |
| fnd6_newqeventv110_rectoq | 应收账款 - 当前其他包括税款退款 | Vector | 50% | 289 |
| fnd6_newqeventv110_rectrq | 应收账款 - 贸易 | Vector | 50% | 326 |
| fnd6_newqeventv110_reunaq | 未调整留存收益 | Vector | 50% | 27 |
| fnd6_newqeventv110_revtq | 收入 - 总额 | Vector | 50% | 309 |
| fnd6_newqeventv110_rrpq | 逆转——重组/收购税前 | Vector | 50% | 11 |
| fnd6_newqeventv110_seqoq | 其他股东权益调整 | Vector | 50% | 125 |
| fnd6_newqeventv110_seqq | 股东权益 - 总额 - 季度 | Vector | 50% | 60 |
| fnd6_newqeventv110_seta12 | 税后和解（诉讼/保险）- 12毫米 | Vector | 50% | 22 |
| fnd6_newqeventv110_setaq | 和解（诉讼/保险）税后 | Vector | 50% | 9 |
| fnd6_newqeventv110_setd12 | 和解（诉讼/保险）稀释EPS效应1200万 | Vector | 50% | 123 |
| fnd6_newqeventv110_seteps12 | 和解（诉讼/保险）基本每股收益影响1200万 | Vector | 50% | 164 |
| fnd6_newqeventv110_setpq | 和解（诉讼/保险）税前 | Vector | 50% | 29 |
| fnd6_newqeventv110_spce12 | 标普核心收益1200万美元 | Vector | 50% | 107 |
| fnd6_newqeventv110_spcedpq | 标普核心盈余每股收益稀释后 - 初步数据 | Vector | 50% | 24 |
| fnd6_newqeventv110_spcedq | 标普核心盈余每股收益被稀释 | Vector | 50% | 61 |
| fnd6_newqeventv110_spceeps12 | 标普核心收益每股收益基础1200万 | Vector | 50% | 32 |
| fnd6_newqeventv110_spceepsp12 | S&P Core 12MM EPS - 基础 - 初步 | Vector | 50% | 37 |
| fnd6_newqeventv110_spceepspq | 标普核心收益每股收益基础 - 初步报告 | Vector | 50% | 33 |
| fnd6_newqeventv110_spceepsq | 标普核心收益每股基础 | Vector | 50% | 79 |
| fnd6_newqeventv110_spcep12 | 标普核心收益1200万 - 初步数据 | Vector | 50% | 219 |
| fnd6_newqeventv110_spcepd12 | 标普核心盈余1200万每股收益被稀释 - 初步数据 | Vector | 50% | 35 |
| fnd6_newqeventv110_spcepq | 标普核心财报 - 初步 | Vector | 50% | 72 |
| fnd6_newqeventv110_spceq | 标普核心收益 | Vector | 50% | 86 |
| fnd6_newqeventv110_spioaq | 其他税后特别项目 | Vector | 50% | 227 |
| fnd6_newqeventv110_spiopq | 其他税前特殊项目 | Vector | 50% | 15 |
| fnd6_newqeventv110_spiq | 特殊物品 | Vector | 50% | 31 |
| fnd6_newqeventv110_stkcoq | 股票补偿费用 | Vector | 50% | 443 |
| fnd6_newqeventv110_stkcpaq | 税后股票补偿 | Vector | 50% | 132 |
| fnd6_newqeventv110_teqq | 股东权益 - 总额 - 季度 | Vector | 50% | 130 |
| fnd6_newqeventv110_tfvaq | 公允价值资产总额 | Vector | 50% | 37 |
| fnd6_newqeventv110_tfvceq | 包括收益在内的总公允价值变动 | Vector | 50% | 4 |
| fnd6_newqeventv110_tfvlq | 总公允价值负债 | Vector | 50% | 68 |
| fnd6_newqeventv110_tstknq | 国债 - 普通股数量 | Vector | 50% | 108 |
| fnd6_newqeventv110_tstkq | 国债股 - 总计（全部资本） | Vector | 50% | 1661 |
| fnd6_newqeventv110_txdbaq | 递延税款资产——长期 | Vector | 50% | 15 |
| fnd6_newqeventv110_txdbq | 递延税款 - 资产负债表 | Vector | 50% | 16 |
| fnd6_newqeventv110_txdiq | 所得税 - 递延 | Vector | 50% | 12 |
| fnd6_newqeventv110_txditcq | 递延税款与投资税收抵免 | Vector | 50% | 23 |
| fnd6_newqeventv110_txpq | 应缴所得税 | Vector | 50% | 31 |
| fnd6_newqeventv110_txtq | 所得税 - 总计 | Vector | 50% | 23 |
| fnd6_newqeventv110_txwq | 消费税 | Vector | 50% | 34 |
| fnd6_newqeventv110_wcapq | 营运资金（资产负债表） | Vector | 50% | 58 |
| fnd6_newqeventv110_wdaq | 税后减记 | Vector | 50% | 34 |
| fnd6_newqeventv110_wdpq | 税前减记 | Vector | 50% | 728 |
| fnd6_newqeventv110_xidoq | 特殊物品与停止运营 | Vector | 50% | 299 |
| fnd6_newqeventv110_xintq | 利息及相关费用 - 总额 | Vector | 50% | 80 |
| fnd6_newqeventv110_xiq | 非凡物品 | Vector | 50% | 29 |
| fnd6_newqeventv110_xoprq | 运营费用 - 总额 | Vector | 50% | 45 |
| fnd6_newqeventv110_xopt12 | 隐含期权费用 - 12毫米 | Vector | 50% | 30 |
| fnd6_newqeventv110_xoptd12 | 隐含期权每股收益稀释1200万 | Vector | 50% | 38 |
| fnd6_newqeventv110_xoptd12p | 默示期权1200万每股收益稀释初步 | Vector | 50% | 43 |
| fnd6_newqeventv110_xoptdq | 隐含期权每股收益稀释 | Vector | 50% | 44 |
| fnd6_newqeventv110_xoptdqp | 隐含期权每股收益稀释初步 | Vector | 50% | 48 |
| fnd6_newqeventv110_xopteps12 | 隐含期权 EPS 基础 12MM | Vector | 50% | 34 |
| fnd6_newqeventv110_xoptepsp12 | 隐含选项 12MM EPS 基础初步 | Vector | 50% | 32 |
| fnd6_newqeventv110_xoptepsq | 隐含期权EPS基础 | Vector | 50% | 45 |
| fnd6_newqeventv110_xoptepsqp | 隐含期权EPS基础初步 | Vector | 50% | 37 |
| fnd6_newqeventv110_xoptq | 隐含期权费用 | Vector | 50% | 59 |
| fnd6_newqeventv110_xoptqp | 隐含期权费用初步报告 | Vector | 50% | 21 |
| fnd6_newqeventv110_xrdq | 研发费用 | Vector | 50% | 405 |
| fnd6_newqeventv110_xsgaq | 销售、一般及行政费用 | Vector | 50% | 36 |
| fnd6_newqv1300_acomincq | 累计其他综合收入（损失） | Matrix | 50% | 1343 |
| fnd6_newqv1300_acoq | 流动资产 - 其他 - 总额 | Matrix | 50% | 377 |
| fnd6_newqv1300_altoq | 其他长期资产 | Matrix | 50% | 453 |
| fnd6_newqv1300_ancq | 非流动资产 - 总额 | Matrix | 50% | 1621 |
| fnd6_newqv1300_anoq | 资产净额及其他调整 | Matrix | 50% | 223 |
| fnd6_newqv1300_aociderglq | Accum Other Comp Inc - 衍生品未实现盈亏 | Matrix | 50% | 350 |
| fnd6_newqv1300_aociotherq | 累计其他综合收入——其他调整 | Matrix | 50% | 591 |
| fnd6_newqv1300_aocipenq | Accum Other Comp Inc - Min Pension Liab Adj | Matrix | 50% | 280 |
| fnd6_newqv1300_aocisecglq | Accum Other Comp Inc - Unreal G/L Ret Int在Sec Assets中 | Matrix | 50% | 615 |
| fnd6_newqv1300_aol2q | 资产等级2（可观察） | Matrix | 50% | 232 |
| fnd6_newqv1300_aoq | 资产 - 其他 - 总额 | Matrix | 50% | 621 |
| fnd6_newqv1300_aqpl1q | 资产等级1（报价价格） | Matrix | 50% | 307 |
| fnd6_newqv1300_aul3q | 资产等级3（不可观察） | Matrix | 50% | 182 |
| fnd6_newqv1300_capsq | 资本盈余/股份权利金储备 | Matrix | 50% | 890 |
| fnd6_newqv1300_chq | 现金 | Matrix | 50% | 337 |
| fnd6_newqv1300_cibegniq | Comp Inc - 初始净收入 | Matrix | 50% | 376 |
| fnd6_newqv1300_cicurrq | Comp Inc - Currency Trans Adj | Matrix | 50% | 249 |
| fnd6_newqv1300_ciderglq | Comp Inc - 衍生品收益/亏损 | Matrix | 50% | 180 |
| fnd6_newqv1300_cimiiq | 综合收益 - 非控制权益 | Matrix | 50% | 136 |
| fnd6_newqv1300_ciotherq | Comp Inc - 其他 形容词 | Matrix | 50% | 705 |
| fnd6_newqv1300_cipenq | Comp Inc - 最低养老金附加项 | Matrix | 50% | 398 |
| fnd6_newqv1300_ciq | 综合收入 - 总额 | Matrix | 50% | 462 |
| fnd6_newqv1300_cisecglq | Comp Inc - 证券收益/亏损 | Matrix | 50% | 197 |
| fnd6_newqv1300_citotalq | 综合收入 - 母公司 | Matrix | 50% | 371 |
| fnd6_newqv1300_cogsq | 销售成本 | Matrix | 50% | 429 |
| fnd6_newqv1300_csh12q | 用于计算每股收益的普通股 - 12个月移动 | Matrix | 50% | 464 |
| fnd6_newqv1300_cshfdq | 稀释每股收益的普通股 | Matrix | 50% | 664 |
| fnd6_newqv1300_cshiq | 发行普通股 | Matrix | 50% | 477 |
| fnd6_newqv1300_cshopq | 季度回购总股份 | Matrix | 50% | 122 |
| fnd6_newqv1300_cshoq | 普通股流通 | Matrix | 50% | 283 |
| fnd6_newqv1300_cshprq | 用于计算每股收益的普通股 - 基础 | Matrix | 50% | 571 |
| fnd6_newqv1300_cstkq | 普通股/普通股（资本） | Matrix | 50% | 474 |
| fnd6_newqv1300_dcomq | 递延补偿 | Matrix | 50% | 725 |
| fnd6_newqv1300_dilavq | 稀释可用——不包括特殊物品 | Matrix | 50% | 655 |
| fnd6_newqv1300_dlcq | 流动负债中的债务 | Matrix | 50% | 491 |
| fnd6_newqv1300_dpactq | 折旧、耗尽与摊销（累计） | Matrix | 50% | 260 |
| fnd6_newqv1300_drcq | 递延收入 - 当前 | Matrix | 50% | 1354 |
| fnd6_newqv1300_drltq | 递延收入——长期 | Matrix | 50% | 4547 |
| fnd6_newqv1300_epsfiq | 每股收益（稀释后）——包括非凡项目 | Matrix | 50% | 649 |
| fnd6_newqv1300_epspiq | 每股收益（基础）——包括非凡项目 | Matrix | 50% | 416 |
| fnd6_newqv1300_epspxq | 每股收益（基础）——不包括特别项目 | Matrix | 50% | 487 |
| fnd6_newqv1300_esopnrq | 优先员工持股计划义务 - 不可兑换 | Matrix | 50% | 909 |
| fnd6_newqv1300_esoprq | 优先员工持股计划义务 - 可兑换 | Matrix | 50% | 1041 |
| fnd6_newqv1300_fcaq | 外汇收入（亏损） | Matrix | 50% | 65 |
| fnd6_newqv1300_gdwlq | 善意（网络） | Matrix | 50% | 514 |
| fnd6_newqv1300_glcea12 | 销售盈亏（核心收益调整后）税后1200万 | Matrix | 50% | 44 |
| fnd6_newqv1300_glced12 | 销售盈亏（核心利润调整后）稀释每股收益影响 1200万 | Matrix | 50% | 19 |
| fnd6_newqv1300_glceeps12 | 销售盈亏（核心收益调整后）基本每股收益影响1200万 | Matrix | 50% | 27 |
| fnd6_newqv1300_ibadj12 | 额外物品前的收入——普通股等价物的附加值 - 1200万 | Matrix | 50% | 641 |
| fnd6_newqv1300_ibadjq | 非凡项目前的收入——调整普通股等价项 | Matrix | 50% | 360 |
| fnd6_newqv1300_ibcomq | 特殊物品前的收入——适用于普通物品 | Matrix | 50% | 305 |
| fnd6_newqv1300_ibmiiq | 收入优先于非常物品和非控制权益 | Matrix | 50% | 644 |
| fnd6_newqv1300_ibq | 非凡物品之前的收入 | Matrix | 50% | 424 |
| fnd6_newqv1300_icaptq | 投资资本 - 总额 - 季度 | Matrix | 50% | 661 |
| fnd6_newqv1300_intanoq | 其他无形资产 | Matrix | 50% | 1010 |
| fnd6_newqv1300_intanq | 无形资产 - 总计 | Matrix | 50% | 556 |
| fnd6_newqv1300_invfgq | 库存 - 成品 | Matrix | 50% | 350 |
| fnd6_newqv1300_invoq | 库存 - 其他 | Matrix | 50% | 307 |
| fnd6_newqv1300_invrmq | 库存 - 原材料 | Matrix | 50% | 257 |
| fnd6_newqv1300_invtq | 库存 - 总计 | Matrix | 50% | 467 |
| fnd6_newqv1300_invwipq | 库存——在品 | Matrix | 50% | 351 |
| fnd6_newqv1300_ivltq | 总长期投资 | Matrix | 50% | 361 |
| fnd6_newqv1300_ivstq | 短期投资 - 总计 | Matrix | 50% | 100 |
| fnd6_newqv1300_lcoq | 流动负债 - 其他 - 总额 | Matrix | 50% | 1602 |
| fnd6_newqv1300_lltq | 长期负债（总额） | Matrix | 50% | 2606 |
| fnd6_newqv1300_lnoq | 负债净额及其他调整 | Matrix | 50% | 99 |
| fnd6_newqv1300_lol2q | 负债等级2（可观测） | Matrix | 50% | 158 |
| fnd6_newqv1300_loq | 负债 - 其他 | Matrix | 50% | 277 |
| fnd6_newqv1300_loxdrq | 负债 - 其他 - 不包括递延收入 | Matrix | 50% | 424 |
| fnd6_newqv1300_lqpl1q | 负债等级1（报价） | Matrix | 50% | 386 |
| fnd6_newqv1300_lseq | 负债与股东权益 - 总计 | Matrix | 50% | 548 |
| fnd6_newqv1300_ltmibq | 负债——全部权益和非控制权益 | Matrix | 50% | 453 |
| fnd6_newqv1300_lul3q | 负债等级3（不可观测） | Matrix | 50% | 451 |
| fnd6_newqv1300_mibnq | 不可赎回非控制权益（资产负债表）- 季度 | Matrix | 50% | 154 |
| fnd6_newqv1300_mibtq | 非控股权益 - 总额 - 资产负债表 - 季度 | Matrix | 50% | 127 |
| fnd6_newqv1300_miiq | 非控制性利息——收入账户 | Matrix | 50% | 467 |
| fnd6_newqv1300_msaq | 累计其他综合收益——可流通证券调整 | Matrix | 50% | 382 |
| fnd6_newqv1300_oepf12 | 每股盈余 - 摊薄后 - 运营收益 - 1200万 | Matrix | 50% | 913 |
| fnd6_newqv1300_oepsxq | 每股收益 - 摊薄后 - 来自运营 | Matrix | 50% | 519 |
| fnd6_newqv1300_optfvgrq | 期权——已授予期权的公允价值 | Matrix | 50% | 730 |
| fnd6_newqv1300_optrfrq | 无风险利率 - 假设（%） | Matrix | 50% | 148 |
| fnd6_newqv1300_piq | 税前收入 | Matrix | 50% | 500 |
| fnd6_newqv1300_pncq | 核心养老金调整 | Matrix | 50% | 13 |
| fnd6_newqv1300_ppegtq | 物业、厂房和设备 - 总额（总额）- 季度 | Matrix | 50% | 334 |
| fnd6_newqv1300_ppentq | 物业、设备和设备 - 总计（净） | Matrix | 50% | 607 |
| fnd6_newqv1300_prcaq | 核心退休后调整 | Matrix | 50% | 7 |
| fnd6_newqv1300_prcdq | 核心退休后调整稀释每股收益效应 | Matrix | 50% | 15 |
| fnd6_newqv1300_prcepsq | 核心退休后调整基础每股收益效应 | Matrix | 50% | 13 |
| fnd6_newqv1300_prcraq | 回购价格 - 每股平均 | Matrix | 50% | 241 |
| fnd6_newqv1300_rcpq | 税前重组成本 | Matrix | 50% | 131 |
| fnd6_newqv1300_rdipaq | 正在进行的税后研发费用 | Matrix | 50% | 153 |
| fnd6_newqv1300_rdipdq | 在审理中研发费用稀释每股收益影响 | Matrix | 50% | 303 |
| fnd6_newqv1300_rdipepsq | 在工研发费用基础每股收益效应 | Matrix | 50% | 125 |
| fnd6_newqv1300_rdipq | 研发中 | Matrix | 50% | 2195 |
| fnd6_newqv1300_recdq | 应收账款——预计存疑 | Matrix | 50% | 905 |
| fnd6_newqv1300_rectaq | Accum Other Comp Inc - 累计平算调整 | Matrix | 50% | 552 |
| fnd6_newqv1300_rectoq | 应收账款 - 当前其他包括税款退还 | Matrix | 50% | 342 |
| fnd6_newqv1300_rectrq | 应收账款 - 贸易 | Matrix | 50% | 361 |
| fnd6_newqv1300_reunaq | 未调整留存收益 | Matrix | 50% | 889 |
| fnd6_newqv1300_revtq | 收入 - 总额 | Matrix | 50% | 423 |
| fnd6_newqv1300_seqoq | 其他股东权益调整 | Matrix | 50% | 2205 |
| fnd6_newqv1300_seqq | 股东权益 - 总额 - 季度 | Matrix | 50% | 683 |
| fnd6_newqv1300_spcedpq | 标普核心盈余每股收益稀释后 - 初步数据 | Matrix | 50% | 271 |
| fnd6_newqv1300_spcedq | 标普核心盈余每股收益被稀释 | Matrix | 50% | 19 |
| fnd6_newqv1300_spceepsp12 | S&P Core 12MM EPS - 基础 - 初步 | Matrix | 50% | 7 |
| fnd6_newqv1300_spceepspq | 标普核心收益每股收益基础 - 初步报告 | Matrix | 50% | 114 |
| fnd6_newqv1300_spceepsq | 标普核心收益每股基础 | Matrix | 50% | 9 |
| fnd6_newqv1300_spcep12 | 标普核心收益1200万 - 初步数据 | Matrix | 50% | 6 |
| fnd6_newqv1300_spcepd12 | 标普核心盈余1200万每股收益被稀释 - 初步数据 | Matrix | 50% | 22 |
| fnd6_newqv1300_spcepq | 标普核心财报 - 初步 | Matrix | 50% | 246 |
| fnd6_newqv1300_spceq | 标普核心收益 | Matrix | 50% | 7 |
| fnd6_newqv1300_spiq | 特殊物品 | Matrix | 50% | 150 |
| fnd6_newqv1300_stkcoq | 股票补偿费用 | Matrix | 50% | 553 |
| fnd6_newqv1300_stkcpaq | 税后股票补偿 | Matrix | 50% | 214 |
| fnd6_newqv1300_teqq | 股东权益 - 总额 - 季度 | Matrix | 50% | 1031 |
| fnd6_newqv1300_tfvaq | 公允价值资产总额 | Matrix | 50% | 204 |
| fnd6_newqv1300_tfvceq | 包括收益在内的总公允价值变动 | Matrix | 50% | 81 |
| fnd6_newqv1300_tfvlq | 总公允价值负债 | Matrix | 50% | 186 |
| fnd6_newqv1300_tstknq | 国债 - 普通股数量 | Matrix | 50% | 363 |
| fnd6_newqv1300_tstkq | 国债股 - 总计（全部资本） | Matrix | 50% | 166 |
| fnd6_newqv1300_txdbaq | 递延税款资产——长期 | Matrix | 50% | 346 |
| fnd6_newqv1300_txdbq | 递延税款 - 资产负债表 | Matrix | 50% | 111 |
| fnd6_newqv1300_txdiq | 所得税 - 递延 | Matrix | 50% | 170 |
| fnd6_newqv1300_txditcq | 递延税款与投资税收抵免 | Matrix | 50% | 521 |
| fnd6_newqv1300_txpq | 应缴所得税 | Matrix | 50% | 420 |
| fnd6_newqv1300_txtq | 所得税 - 总计 | Matrix | 50% | 533 |
| fnd6_newqv1300_txwq | 消费税 | Matrix | 50% | 768 |
| fnd6_newqv1300_wcapq | 营运资金（资产负债表） | Matrix | 50% | 234 |
| fnd6_newqv1300_xintq | 利息及相关费用 - 总额 | Matrix | 50% | 461 |
| fnd6_newqv1300_xoprq | 运营费用 - 总额 | Matrix | 50% | 991 |
| fnd6_newqv1300_xoptdq | 隐含期权每股收益稀释 | Matrix | 50% | 7 |
| fnd6_newqv1300_xoptepsq | 隐含期权EPS基础 | Matrix | 50% | 20 |
| fnd6_newqv1300_xoptq | 隐含期权费用 | Matrix | 50% | 99 |
| fnd6_newqv1300_xrdq | 研发费用 | Matrix | 50% | 667 |
| fnd6_newqv1300_xsgaq | 销售、一般及行政费用 | Matrix | 50% | 801 |
| fnd6_niadj | 净收入调整普通股/普通股（资本）等值 | Matrix | 50% | 1602 |
| fnd6_nis | 净收入（亏损） | Vector | 50% | 31 |
| fnd6_nopio | 非营业收入（费用）- 其他 | Matrix | 50% | 562 |
| fnd6_nopxs | 非营业收入（费用）——不含利息 | Vector | 50% | 31 |
| fnd6_np | 应付票据 - 短期借款 | Matrix | 50% | 279 |
| fnd6_npq | 应付票据 | Matrix | 50% | 384 |
| fnd6_nxints | 净利息收入（支出） | Vector | 50% | 35 |
| fnd6_obs | 订单积压 | Vector | 50% | 24 |
| fnd6_ocaxs | 其他费用与开销 | Vector | 50% | 10 |
| fnd6_oelim | 其他淘汰（收入） | Vector | 50% | 60 |
| fnd6_oiadps | 折旧后的营业收入 | Vector | 50% | 220 |
| fnd6_oibdps | 折旧前营业收入 | Vector | 50% | 38 |
| fnd6_oprepsx | 每股收益 - 摊薄后 - 来自运营 | Matrix | 50% | 956 |
| fnd6_ops | 营业利润（亏损） | Vector | 50% | 52 |
| fnd6_optca | 选项 - 取消 （-） | Matrix | 50% | 1682 |
| fnd6_optdr | 股息率 - 假设（%） | Matrix | 50% | 1009 |
| fnd6_optdrq | 股息率 - 假设（%） | Matrix | 50% | 160 |
| fnd6_optex | 可行期权（000） | Matrix | 50% | 1156 |
| fnd6_optfvgr | 期权——已授予期权的公允价值 | Matrix | 50% | 628 |
| fnd6_optgr | 选项 - 已批准 | Matrix | 50% | 627 |
| fnd6_optlife | 期权生涯 - 假设（# 年） | Matrix | 50% | 748 |
| fnd6_optlifeq | 期权生涯 - 假设（# 年） | Matrix | 50% | 214 |
| fnd6_optosby | 期权未还 - 年初 | Matrix | 50% | 770 |
| fnd6_optosey | 期权未还 - 年终 | Matrix | 50% | 765 |
| fnd6_optprcby | 年初未结期权 - 价格 | Matrix | 50% | 643 |
| fnd6_optprcca | 期权取消 - 价格 | Matrix | 50% | 554 |
| fnd6_optprcex | 行使期权 - 价格 | Matrix | 50% | 614 |
| fnd6_optprcey | 年终未偿还期权 - 价格 | Matrix | 50% | 540 |
| fnd6_optprcgr | 授予的选项 - 价格 | Matrix | 50% | 585 |
| fnd6_optprcwa | 可行期权 - 加权平均价格 | Matrix | 50% | 608 |
| fnd6_optrfr | 无风险利率 - 假设（%） | Matrix | 50% | 748 |
| fnd6_optvol | 波动率 - 假设（%） | Matrix | 50% | 664 |
| fnd6_optvolq | 波动率 - 假设（%） | Matrix | 50% | 229 |
| fnd6_pidom | 税前收入 - 国内 | Matrix | 50% | 321 |
| fnd6_pifo | 税前收入 - 外国 | Matrix | 50% | 2465 |
| fnd6_pncdq | 核心养老金调整稀释EPS效应 | Matrix | 50% | 22 |
| fnd6_pncepsq | 核心养老金调整 基本每股收益效应 | Matrix | 50% | 37 |
| fnd6_pnrsho | 非红色Pfd股份出户（000） | Matrix | 50% | 730 |
| fnd6_ppents | 物业、厂房与设备 | Vector | 50% | 2367 |
| fnd6_ppeveb | 财产、工厂和设备 - 期末余额（附表五） | Matrix | 50% | 514 |
| fnd6_prcc | 价格收盘 - 年度 | Matrix | 50% | 859 |
| fnd6_prccq | 价格收盘 - 季度 | Matrix | 50% | 619 |
| fnd6_prch | 价格高 - 年度 | Matrix | 50% | 432 |
| fnd6_prchq | 价格高 - 四分之一 | Matrix | 50% | 504 |
| fnd6_prcl | 价格低 - 年价 | Matrix | 50% | 805 |
| fnd6_prclq | 价格低点 - 四分之一 | Matrix | 50% | 602 |
| fnd6_prstkc | 普通股和优先股的购买 | Matrix | 50% | 406 |
| fnd6_pstkc | 优先股 - 可转换股 | Matrix | 50% | 564 |
| fnd6_pstkl | 优先股 - 清算价值 | Matrix | 50% | 227 |
| fnd6_pstkrv | 优先股 - 赎回价值 | Matrix | 50% | 319 |
| fnd6_ptis | 税前收入 | Vector | 50% | 63 |
| fnd6_rank | SP排名含义如下：// 0----无效排名 //1----A+//2----A//3----A-//4----B+//5----B//6----B-//7----C+//8----C//9----C- | Matrix | 50% | 428 |
| fnd6_ranks | 排名 | Vector | 50% | 1400 |
| fnd6_rds | 研发 | Vector | 50% | 52 |
| fnd6_rea | 保留收益——重述 | Matrix | 50% | 5128 |
| fnd6_reajo | 保留收益——其他调整 | Matrix | 50% | 639 |
| fnd6_recco | 应收账款 - 当前账款 - 其他 | Matrix | 50% | 786 |
| fnd6_recd | 应收账款——预计存疑 | Matrix | 50% | 5270 |
| fnd6_recta | 留存收益 - 累计翻译调整 | Matrix | 50% | 988 |
| fnd6_rectr | 应收账款 - 贸易 | Matrix | 50% | 745 |
| fnd6_revts | 总收入 | Vector | 50% | 89 |
| fnd6_sales | 净销售额 | Vector | 50% | 113 |
| fnd6_salexg | 出口销售 | Vector | 50% | 7 |
| fnd6_sics | SIC代码 | Vector | 50% | 296 |
| fnd6_siv | 投资出售 | Matrix | 50% | 414 |
| fnd6_snms | 路段名称 | Vector | 50% | 113 |
| fnd6_spce | 标普核心收益 | Matrix | 50% | 133 |
| fnd6_spis | 特殊物品 | Vector | 50% | 91 |
| fnd6_sppe | 财产出售 | Matrix | 50% | 357 |
| fnd6_sppiv | 财产、厂房及设备及投资的出售——收益（亏损） | Matrix | 50% | 434 |
| fnd6_sstk | 普通股和优先股的出售 | Matrix | 50% | 1080 |
| fnd6_state | 整数用于识别公司的状态 | Matrix | 50% | 1797 |
| fnd6_stkcpa | 税后股票补偿 | Matrix | 50% | 357 |
| fnd6_stype | 段型 | Vector | 50% | 1335 |
| fnd6_teq | 股东权益 - 总额 | Matrix | 50% | 1837 |
| fnd6_tfva | 公允价值资产总额 | Matrix | 50% | 337 |
| fnd6_tfvce | 包括收益在内的总公允价值变动 | Matrix | 50% | 74 |
| fnd6_tfvl | 总公允价值负债 | Matrix | 50% | 272 |
| fnd6_tlcf | 税务损失结转 | Matrix | 50% | 347 |
| fnd6_tstkc | 国债股 - 普通股 | Matrix | 50% | 515 |
| fnd6_txbco | 超额税收优惠股票期权 - 现金流运营 | Matrix | 50% | 1492 |
| fnd6_txbcof | 股票期权的超额税收优惠——现金流融资 | Matrix | 50% | 742 |
| fnd6_txc | 所得税 - 现行 | Matrix | 50% | 493 |
| fnd6_txdba | 递延税款资产——长期 | Matrix | 50% | 374 |
| fnd6_txdbca | 递延税资产 - 当前 | Matrix | 50% | 599 |
| fnd6_txdbcl | 递延税负 - 当前 | Matrix | 50% | 125 |
| fnd6_txdbclq | 当前递延税负 | Matrix | 50% | 3436 |
| fnd6_txdc | 递延税款（现金流） | Matrix | 50% | 522 |
| fnd6_txdfed | 递延税款 - 联邦 | Matrix | 50% | 395 |
| fnd6_txdfo | 递延税款 - 外国 | Matrix | 50% | 301 |
| fnd6_txdi | 所得税 - 递延 | Matrix | 50% | 432 |
| fnd6_txds | 递延税款 - 州 | Matrix | 50% | 252 |
| fnd6_txfed | 联邦所得税 | Matrix | 50% | 290 |
| fnd6_txfo | 所得税 - 外国 | Matrix | 50% | 1321 |
| fnd6_txndb | 净递延税款资产（LIAB）- 总计 | Matrix | 50% | 331 |
| fnd6_txndba | 净递延税款资产 | Matrix | 50% | 402 |
| fnd6_txndbl | 净递延税负 | Matrix | 50% | 460 |
| fnd6_txndbr | 递延税款剩余 | Matrix | 50% | 995 |
| fnd6_txo | 所得税 - 其他 | Matrix | 50% | 1903 |
| fnd6_txpd | 已缴纳所得税 | Matrix | 50% | 660 |
| fnd6_txr | 所得税退税 | Matrix | 50% | 534 |
| fnd6_txs | 所得税 - 州 | Matrix | 50% | 315 |
| fnd6_txts | 所得税 | Vector | 50% | 131 |
| fnd6_txtubadjust | 其他未确认的税收优惠调整 | Matrix | 50% | 348 |
| fnd6_txtubbegin | Unrecog。税收优惠——年度的开始 | Matrix | 50% | 482 |
| fnd6_txtubend | Unrecog。税收优惠 - 年终 | Matrix | 50% | 590 |
| fnd6_txtubposdec | 减少 - 当前税务状况 | Matrix | 50% | 778 |
| fnd6_txtubposinc | 增加——当前税务立场 | Matrix | 50% | 303 |
| fnd6_txtubpospdec | 减少 - 先前税务职位 | Matrix | 50% | 489 |
| fnd6_txtubpospinc | 增加——先前的税务职位 | Matrix | 50% | 228 |
| fnd6_txtubsettle | 与税务机关的和解 | Matrix | 50% | 390 |
| fnd6_txtubsoflimit | 诉讼时效的过失 | Matrix | 50% | 560 |
| fnd6_txtubtxtr | 对有效税率的影响 | Matrix | 50% | 280 |
| fnd6_txtubxintbs | 利息及罚款 - B/S | Matrix | 50% | 230 |
| fnd6_txtubxintis | 认可的利息与罚款 - I/S | Matrix | 50% | 137 |
| fnd6_txw | 消费税 | Matrix | 50% | 853 |
| fnd6_txws | 消费税 | Vector | 50% | 142 |
| fnd6_weburl | 公司的网页URL代码 | Matrix | 50% | 2006 |
| fnd6_xacc | 应计费用 | Matrix | 50% | 1229 |
| fnd6_xaccq | 应计费用 | Matrix | 50% | 671 |
| fnd6_xad | 广告费用 | Matrix | 50% | 1018 |
| fnd6_xidos | 特殊物品与停止运营 | Vector | 50% | 105 |
| fnd6_xintopt | 隐含期权费用 | Matrix | 50% | 69 |
| fnd6_xints | 利息支出 | Vector | 50% | 128 |
| fnd6_xopr | 运营费用 - 总计 | Matrix | 50% | 1498 |
| fnd6_xpp | 预付费用 | Matrix | 50% | 587 |
| fnd6_xpr | 养老金与退休开支 | Matrix | 50% | 428 |
| fnd6_xrent | 租金费用 | Matrix | 50% | 3318 |
| fnd6_xsgas | 销售、综合与行政 | Vector | 50% | 43 |
| fnd6_zipcode | 与公司相关的邮政编码 | Matrix | 50% | 2386 |
| goodwill | 善意（网络） | Matrix | 50% | 13148 |
| income | 净收入 | Matrix | 50% | 12654 |
| income_beforeextra | 非凡物品之前的收入 | Matrix | 50% | 6597 |
| income_tax | 所得税 - 总计 | Matrix | 50% | 7162 |
| interest_expense | 利息及相关费用 - 总额 | Matrix | 50% | 2631 |
| inventory | 库存 - 总计 | Matrix | 50% | 8429 |
| inventory_turnover | 库存周转 | Matrix | 50% | 5965 |
| invested_capital | 投资资本 - 总额 - 季度 | Matrix | 50% | 5684 |
| liabilities | 负债 - 总额 | Matrix | 50% | 54826 |
| liabilities_curr | 流动负债 - 总额 | Matrix | 50% | 9815 |
| operating_expense | 运营费用 - 总额 | Matrix | 50% | 9079 |
| operating_income | 折旧后营业收入 - 季度 | Matrix | 50% | 42627 |
| ppent | 物业、设备和设备 - 总计（净） | Matrix | 50% | 9244 |
| pretax_income | 税前收入 | Matrix | 50% | 7106 |
| rd_expense | 《研究与发展》（季刊） | Matrix | 50% | 2765 |
| receivable | 应收账款 - 总计 | Matrix | 50% | 7892 |
| retained_earnings | 留存收益 | Matrix | 50% | 7309 |
| return_assets | 资产回报率 | Matrix | 50% | 6907 |
| return_equity | 股本回报率 | Matrix | 50% | 8152 |
| revenue | 收入 - 总额 | Matrix | 50% | 12088 |
| sales | 销售/营业额（净额） | Matrix | 50% | 33902 |
| sales_growth | 销售增长（季度） | Matrix | 50% | 7483 |
| sales_ps | 每股销售额（季度） | Matrix | 50% | 6224 |
| sga_expense | 销售、一般及行政费用 | Matrix | 50% | 7960 |
| working_capital | 营运资金（资产负债表） | Matrix | 50% | 5223 |

### 因子模型-排名 (model16)（24 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| analyst_revision_rank_derivative | 分析师修订排名和动量相较于前一时期的变化。 | Matrix | 100% | 175 |
| cashflow_efficiency_rank_derivative | 现金流生成和盈利能力排名较上一期有所变化。 | Matrix | 100% | 98 |
| composite_factor_score_derivative | 整体综合因子得分较上一时期发生变化。 | Matrix | 100% | 95 |
| earnings_certainty_rank_derivative | 盈利可持续性和确定性排名较上一期有所变化。 | Matrix | 100% | 96 |
| fscore_bfl_growth | 该指标的目的是评估该股票的预期MT增长潜力。 | Matrix | 38% | 15 |
| fscore_bfl_momentum | 该指标的目的是识别目前正在经历分析师上调或下调调整的股票。 | Matrix | 38% | 24 |
| fscore_bfl_profitability | 该指标的目的是根据股票产生现金流的能力进行排名。 | Matrix | 38% | 8 |
| fscore_bfl_quality | 该指标的目的是衡量盈利的可持续性和确定性。 | Matrix | 38% | 15 |
| fscore_bfl_surface | 静态乐谱。每只股票和每个综合因子都采用0到100之间的指数——第一个排名是基于五边形的表面分数。表面越大，等级越高。 | Matrix | 37% | 13 |
| fscore_bfl_surface_accel | 衍生分数。第二步，我们计算该分数的导数（例如：五边形表面较上月增加还是减少？）。 | Matrix | 37% | 55 |
| fscore_bfl_total | 最终得分M-Score是五角大楼地面得分和五角大楼加速得分的加权平均值。 | Matrix | 37% | 6 |
| fscore_bfl_value | 该指标的目的是根据多种知名估值标准判断股票是否被低估或高估。 | Matrix | 38% | 27 |
| fscore_growth | 该指标的目的是评估该股票的预期MT增长潜力。 | Matrix | 30% | 267 |
| fscore_momentum | 该指标的目的是识别目前正在经历分析师上调或下调调整的股票。 | Matrix | 30% | 429 |
| fscore_profitability | 该指标的目的是根据股票产生现金流的能力进行排名。 | Matrix | 30% | 315 |
| fscore_quality | 该指标的目的是衡量盈利的可持续性和确定性。 | Matrix | 30% | 1467 |
| fscore_surface | 静态乐谱。每只股票和每个综合因子都采用0到100之间的指数——第一个排名是基于五边形的表面分数。表面越大，等级越高。 | Matrix | 30% | 427 |
| fscore_surface_accel | 衍生分数。第二步，我们计算该分数的导数（例如：五边形表面较上月增加还是减少？）。 | Matrix | 29% | 212 |
| fscore_total | 最终得分M-Score是五角大楼地面得分和五角大楼加速得分的加权平均值。 | Matrix | 29% | 325 |
| fscore_value | 该指标的目的是根据多种知名估值标准判断股票是否被低估或高估。 | Matrix | 30% | 379 |
| growth_potential_rank_derivative | 中期增长潜力排名较前期有所变化。 | Matrix | 100% | 72 |
| multi_factor_acceleration_score_derivative | 多因素评分加速速度相较前一时期的变化。 | Matrix | 100% | 73 |
| multi_factor_static_score_derivative | 与上一时期相比，静态多因素评分发生变化。 | Matrix | 100% | 56 |
| relative_valuation_rank_derivative | 估值指标排名与上一期相比发生变化。 | Matrix | 100% | 50 |

### 因子模型-Beta (model51)（16 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| beta_last_30_days_spy | 30天内完成SPY测试版 | Matrix | 78% | 1281 |
| beta_last_360_days_spy | 360天内完成SPY测试版 | Matrix | 76% | 1228 |
| beta_last_60_days_spy | 60天后将通过SPY的测试版 | Matrix | 78% | 1500 |
| beta_last_90_days_spy | SPY测试版将在90天内发布 | Matrix | 78% | 1247 |
| correlation_last_30_days_spy | 30天内与SPY的相关性 | Matrix | 78% | 991 |
| correlation_last_360_days_spy | 与SPY的360天相关性 | Matrix | 76% | 1105 |
| correlation_last_60_days_spy | 与SPY的60天相关性 | Matrix | 78% | 1499 |
| correlation_last_90_days_spy | 90天内与SPY的相关性 | Matrix | 78% | 822 |
| systematic_risk_last_30_days | 系统性风险持续30天 | Matrix | 78% | 786 |
| systematic_risk_last_360_days | 系统性风险持续360天 | Matrix | 76% | 1085 |
| systematic_risk_last_60_days | 系统性风险持续60天 | Matrix | 78% | 1119 |
| systematic_risk_last_90_days | 系统性风险持续90天 | Matrix | 77% | 1414 |
| unsystematic_risk_last_30_days | 非系统性风险 30 天 - 相对于 SPY | Matrix | 78% | 1127 |
| unsystematic_risk_last_360_days | 非系统性风险持续360天——相对于SPY而言 | Matrix | 76% | 8461 |
| unsystematic_risk_last_60_days | 非系统性风险持续60天——相对于SPY | Matrix | 78% | 1712 |
| unsystematic_risk_last_90_days | 非系统性风险 90天 - 相对于SPY | Matrix | 77% | 3016 |

### 新闻行情 (news12)（322 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| news_all_vwap | 所有交易日的成交量加权平均价格 | Matrix | 73% | 1444 |
| news_atr14 | 14天平均真实范围 | Matrix | 89% | 3600 |
| news_atr_ratio | 今日区间与20天平均真实区间的比值 | Matrix | 80% | 2220 |
| news_cap | 本交易日日报告的市值 | Matrix | 83% | 6470 |
| news_close_vol | 主收盘体积 | Matrix | 69% | 1605 |
| news_curr_vol | 当天的会议量 | Matrix | 78% | 848 |
| news_dividend_yield | 年产量 | Matrix | 85% | 383 |
| news_eod_close | 交易日收盘价 | Matrix | 88% | 2843 |
| news_eod_high | 新闻发布至交易时段结束之间的最高价格 | Matrix | 97% | 1225 |
| news_eod_low | 新闻发布至交易期结束之间的最低价格 | Matrix | 97% | 845 |
| news_eod_vwap | 成交量加权平均价格，从新闻发布到交易日结束 | Matrix | 97% | 1055 |
| news_eps_actual | 新闻稿所传达的实际每股收益价值 | Matrix | 96% | 1295 |
| news_high_exc_stddev | （EODHigh - TONLast）/StdDev，其中StdDev是30日历日内收盘价的一个标准差 | Matrix | 97% | 1162 |
| news_indx_perf | （（爆炸 - 爆炸） / 爆炸） - （（爆炸 - 爆炸） / 爆炸） | Matrix | 97% | 1286 |
| news_low_exc_stddev | （TONLast - EODLow）/ StdDev，其中StdDev是30日历日内收盘价的一个标准差 | Matrix | 97% | 1050 |
| news_ls | 多头还是做空头位更有利：如果（EODHigh——最后）>（最后——EODLow），则LS=1;如果（EODHigh - 最后一次） = （最后 - 结束日期），则LS= 0;如果（EODHhigh - 最后一天）<（最后 - EODLow），那么LS = -1。 | Matrix | 49% | 666 |
| news_main_vwap | 主交易量加权平均价格 | Matrix | 97% | 904 |
| news_max_dn_amt | 新闻发布时的价格减去新闻发布后的低点 | Matrix | 97% | 1327 |
| news_max_dn_ret | 从新闻发布时价格到新闻低点后的百分比变化 | Matrix | 97% | 1072 |
| news_max_up_amt | 新闻发布后高点减去新闻发布时的价格 | Matrix | 97% | 859 |
| news_max_up_ret | 从新闻发布时的价格到新闻高点后的百分比变化 | Matrix | 85% | 1511 |
| news_mins_10_chg | 10分钟桶中L或S的最低点数 | Matrix | 74% | 1246 |
| news_mins_10_pct_dn | 价格下降10个百分点之前的分钟数 | Matrix | 4% | 7432 |
| news_mins_10_pct_up | 价格上涨10个百分点前的分钟数 | Matrix | 63% | 1538 |
| news_mins_1_chg | 1分钟桶的最低L或S值 | Matrix | 92% | 534 |
| news_mins_1_pct_dn | 价格下跌1个百分点之前的分钟数 | Matrix | 83% | 549 |
| news_mins_1_pct_up | 价格上涨1个百分点前的分钟数 | Matrix | 19% | 536 |
| news_mins_20_chg | 20分钟桶中L或S的最小值 | Matrix | 91% | 2141 |
| news_mins_20_pct_dn | 价格下跌20个百分点之前的分钟数 | Matrix | 97% | 930 |
| news_mins_20_pct_up | 价格上涨20个百分点前的分钟数 | Matrix | 97% | 387 |
| news_mins_2_chg | 2分钟桶的L或S最低点数 | Matrix | 53% | 312 |
| news_mins_2_pct_dn | 价格下跌2个百分点之前的分钟数 | Matrix | 44% | 329 |
| news_mins_2_pct_up | 价格上涨2个百分点前的分钟数 | Matrix | 28% | 503 |
| news_mins_3_chg | 3分钟桶的最低L或S值 | Matrix | 92% | 366 |
| news_mins_3_pct_dn | 价格下跌3个百分点前的分钟数 | Matrix | 92% | 341 |
| news_mins_3_pct_up | 价格上涨3个百分点前的分钟数 | Matrix | 92% | 692 |
| news_mins_4_chg | 4分钟桶的最低L或S。 | Matrix | 92% | 320 |
| news_mins_4_pct_dn | 价格下跌4个百分点前的分钟数 | Matrix | 97% | 351 |
| news_mins_4_pct_up | 价格上涨4个百分点前的分钟数 | Matrix | 97% | 464 |
| news_mins_5_chg | 5分钟桶的最低L或S数 | Matrix | 97% | 1107 |
| news_mins_5_pct_dn | 价格下降5个百分点之前的分钟数 | Matrix | 85% | 1000 |
| news_mins_5_pct_up | 价格上涨5个百分点前的分钟数 | Matrix | 92% | 1089 |
| news_mins_7_5_chg | 7.5分钟桶中最低L或S的次数 | Matrix | 30% | 473 |
| news_mins_7_5_pct_dn | 在价格下跌7.5个百分点之前，经过的分钟数 | Matrix | 88% | 881 |
| news_mins_7_5_pct_up | 在价格上涨7.5个百分点之前，经过的分钟数 | Matrix | 7% | 465 |
| news_mov_vol | 30天移动平均交易量 | Matrix | 80% | 1373 |
| news_open | 开盘价 | Matrix | 71% | 1020 |
| news_open_gap | （DayOpen - 上一关闭） / 上一关闭 | Matrix | 62% | 706 |
| news_open_vol | 主开卷 | Matrix | 44% | 343 |
| news_pct_10min | 新闻发布后前10分钟价格的百分比变化 | Matrix | 77% | 649 |
| news_pct_120min | 新闻发布后前120分钟价格的百分比变化 | Matrix | 91% | 989 |
| news_pct_1min | 新闻发布后第一分钟价格的百分比变化 | Matrix | 97% | 768 |
| news_pct_30min | 新闻发布后前30分钟价格的百分比变化 | Matrix | 97% | 533 |
| news_pct_30sec | 新闻发布后30秒内价格的百分比变化 | Matrix | 97% | 580 |
| news_pct_5_min | 新闻发布后前5分钟价格的百分比变化 | Matrix | 77% | 334 |
| news_pct_60min | 新闻发布后前60分钟价格的百分比变化 | Matrix | 97% | 562 |
| news_pct_90min | 新闻发布后前90分钟价格的百分比变化 | Matrix | 97% | 665 |
| news_pe_ratio | 本交易日日的报告市盈率 | Matrix | 97% | 2760 |
| news_post_vwap | 交易后成交量加权平均价格 | Matrix | 97% | 527 |
| news_pre_vwap | 会前成交量加权平均价格 | Matrix | 83% | 286 |
| news_prev_close | 前一交易日收盘价 | Matrix | 17% | 295 |
| news_prev_day_ret | 前一天开盘与收盘之间的百分比变化 | Matrix | 73% | 493 |
| news_prev_vol | 前一天的会议卷 | Matrix | 4% | 1322 |
| news_range_stddev | （RangeAmt - AvgRange） / RangeStdDev，其中AvgRange是每日范围的平均值，RangeStdDev是每日范围的一个标准差，两者均为30日历日 | Matrix | 62% | 551 |
| news_ratio_vol | Curr_Vol / Mov_Vol | Matrix | 51% | 530 |
| news_session_range | 交易日高价 - 交易日最低价 | Matrix | 42% | 1037 |
| news_session_range_pct | （交易时高价 - 交易日最低价）/ 交易日最低价。 | Matrix | 27% | 711 |
| news_short_interest | 卖空股份总数除以流通总股数 | Matrix | 87% | 393 |
| news_spy_close | 收盘时SPY价格 | Matrix | 97% | 1755 |
| news_spy_last | 新闻发布时SPY的最后价格 | Matrix | 97% | 1368 |
| news_ton_high | 新闻发布前交易时段达到的最高价格 | Matrix | 97% | 489 |
| news_ton_last | 新闻发布时的价格 | Matrix | 97% | 816 |
| news_ton_low | 新闻发布前交易时段中达到的最低价格 | Matrix | 97% | 458 |
| news_tot_ticks | 交易日的总抽数 | Matrix | 97% | 1975 |
| news_vol_stddev | （CurrentVolume - AvgVol）/VolStDev，其中AvgVol是日成交量的平均值，VolStdDev是每日成交量的一个标准差，两者均为30日历日 | Matrix | 97% | 891 |
| nws12_afterhsz_01l | 价格上涨10个百分点前的分钟数 | Vector | 71% | 836 |
| nws12_afterhsz_01p | 10分钟桶内L或S的最低点数 | Vector | 71% | 268 |
| nws12_afterhsz_01s | 价格下降10个百分点之前的分钟数 | Vector | 71% | 413 |
| nws12_afterhsz_02l | 价格上涨20个百分点前的分钟数 | Vector | 71% | 36 |
| nws12_afterhsz_02p | 20分钟桶中L或S的最小值 | Vector | 71% | 35 |
| nws12_afterhsz_02s | 价格下跌20个百分点之前的分钟数 | Vector | 71% | 40 |
| nws12_afterhsz_10_min | 新闻发布后前10分钟价格的百分比变化 | Vector | 37% | 323 |
| nws12_afterhsz_120_min | 新闻发布后前120分钟价格的百分比变化 | Vector | 46% | 159 |
| nws12_afterhsz_1_minute | 新闻发布后第一分钟价格的百分比变化 | Vector | 26% | 509 |
| nws12_afterhsz_1l | 价格上涨1个百分点前的分钟数 | Vector | 71% | 801 |
| nws12_afterhsz_1p | 1分钟桶的最低L或S值 | Vector | 71% | 144 |
| nws12_afterhsz_1s | 价格下跌1个百分点之前的分钟数 | Vector | 71% | 207 |
| nws12_afterhsz_2l | 价格上涨2个百分点前的分钟数 | Vector | 71% | 284 |
| nws12_afterhsz_2p | 2分钟桶的L或S最低点数 | Vector | 71% | 126 |
| nws12_afterhsz_2s | 价格下跌2个百分点之前的分钟数 | Vector | 71% | 94 |
| nws12_afterhsz_30_min | 新闻发布后前30分钟价格的百分比变化 | Vector | 42% | 42 |
| nws12_afterhsz_3l | 价格上涨3个百分点前的分钟数 | Vector | 71% | 180 |
| nws12_afterhsz_3p | 3分钟桶的最低L或S值 | Vector | 71% | 134 |
| nws12_afterhsz_3s | 价格下跌3个百分点前的分钟数 | Vector | 71% | 552 |
| nws12_afterhsz_41rta | 14天平均真实范围 | Vector | 71% | 54 |
| nws12_afterhsz_4l | 价格上涨4个百分点前的分钟数 | Vector | 71% | 89 |
| nws12_afterhsz_4p | 4分钟桶的最低L或S。 | Vector | 71% | 112 |
| nws12_afterhsz_4s | 价格下跌4个百分点前的分钟数 | Vector | 71% | 686 |
| nws12_afterhsz_57l | 在价格上涨7.5个百分点之前，经过的分钟数 | Vector | 71% | 382 |
| nws12_afterhsz_57p | 7.5分钟桶中最低L或S的次数 | Vector | 71% | 79 |
| nws12_afterhsz_57s | 在价格下跌7.5个百分点之前，经过的分钟数 | Vector | 71% | 2052 |
| nws12_afterhsz_5_min | 新闻发布后前5分钟价格的百分比变化 | Vector | 33% | 114 |
| nws12_afterhsz_5l | 价格上涨5个百分点前的分钟数 | Vector | 71% | 676 |
| nws12_afterhsz_5p | 5分钟桶的最低L或S数 | Vector | 71% | 98 |
| nws12_afterhsz_5s | 价格下降5个百分点之前的分钟数 | Vector | 71% | 237 |
| nws12_afterhsz_60_min | 新闻发布后前60分钟价格的百分比变化 | Vector | 44% | 36 |
| nws12_afterhsz_90_min | 新闻发布后前90分钟价格的百分比变化 | Vector | 45% | 105 |
| nws12_afterhsz_allticks | 交易日的总抽数 | Vector | 71% | 60 |
| nws12_afterhsz_atrratio | 今日区间与20天平均真实区间的比值 | Vector | 64% | 91 |
| nws12_afterhsz_close_vol | 主收盘体积 | Vector | 55% | 8 |
| nws12_afterhsz_curr_vol | 当天的会议量 | Vector | 71% | 39 |
| nws12_afterhsz_dayopen | 开盘价 | Vector | 71% | 30 |
| nws12_afterhsz_div_y | 年产量 | Vector | 33% | 18 |
| nws12_afterhsz_eodclose | 交易日收盘价 | Vector | 71% | 38 |
| nws12_afterhsz_eodhigh | 新闻发布至交易时段结束之间的最高价格 | Vector | 65% | 19 |
| nws12_afterhsz_eodlow | 新闻发布至交易期结束之间的最低价格 | Vector | 65% | 27 |
| nws12_afterhsz_eodvwap | 成交量加权平均价格，介于新闻发布时间到交易日结束之间。 | Vector | 56% | 18 |
| nws12_afterhsz_epsactual | 新闻稿所传达的实际每股收益价值 | Vector | 38% | 33 |
| nws12_afterhsz_highexcstddev | （EODHigh - TONLast）/StdDev，其中StdDev是30日历日内收盘价的一个标准差 | Vector | 65% | 89 |
| nws12_afterhsz_lowexcstddev | （TONLast - EODLow）/ StdDev，其中StdDev是30日历日内收盘价的一个标准差 | Vector | 65% | 68 |
| nws12_afterhsz_mainvwap | 主交易量加权平均价格 | Vector | 55% | 16 |
| nws12_afterhsz_maxdnamt | 新闻发布时的价格减去新闻发布后的低点 | Vector | 65% | 21 |
| nws12_afterhsz_maxdown | 从新闻发布时价格到新闻低点后的百分比变化 | Vector | 65% | 24 |
| nws12_afterhsz_maxup | 从新闻发布时的价格到新闻高点后的百分比变化 | Vector | 65% | 19 |
| nws12_afterhsz_maxupamt | 新闻发布后高点减去新闻发布时的价格 | Vector | 65% | 38 |
| nws12_afterhsz_mktcap | 本交易日日报告的市值 | Vector | 71% | 52 |
| nws12_afterhsz_mov_vol | 30天移动平均交易量 | Vector | 71% | 276 |
| nws12_afterhsz_newrecord | 追踪新闻是首次报道还是重复 | Vector | 71% | 53 |
| nws12_afterhsz_newssess | 报道该消息的会议索引 | Vector | 71% | 17 |
| nws12_afterhsz_open_vol | 主开卷 | Vector | 55% | 10 |
| nws12_afterhsz_opengap | （DayOpen - 上一页关闭）/ 上一页关闭。 | Vector | 71% | 74 |
| nws12_afterhsz_peratio | 报告的本日日历日市盈率 | Vector | 55% | 17 |
| nws12_afterhsz_postvwap | 盘后成交量加权平均价格 | Vector | 71% | 20 |
| nws12_afterhsz_prev_vol | 前一天的会议卷 | Vector | 67% | 70 |
| nws12_afterhsz_prevclose | 前一交易日收盘价 | Vector | 71% | 25 |
| nws12_afterhsz_prevday | 前一天开盘与收盘之间的百分比变化 | Vector | 71% | 45 |
| nws12_afterhsz_prevwap | 会前成交量加权平均价格 | Vector | 38% | 3 |
| nws12_afterhsz_provider | 新闻提供者名称索引 | Vector | 71% | 84 |
| nws12_afterhsz_range | 交易日高价 - 交易日低价）/交易日最低价。 | Vector | 65% | 50 |
| nws12_afterhsz_rangeamt | 交易日高价 - 交易日最低价 | Vector | 65% | 16 |
| nws12_afterhsz_rangestddev | （RangeAmt - AvgRange） / RangeStdDev，其中AvgRange是每日范围的平均值，RangeStdDev是每日范围的一个标准差，两者均为30日历日 | Vector | 62% | 39 |
| nws12_afterhsz_reportsess | 电子表格所报告的会议索引 | Vector | 71% | 22 |
| nws12_afterhsz_result1 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 71% | 917 |
| nws12_afterhsz_result2 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 71% | 845 |
| nws12_afterhsz_result_vs_index | （（爆炸 - 爆炸） / 爆炸） - （（爆炸 - 爆炸） / 爆炸） | Vector | 71% | 751 |
| nws12_afterhsz_short_interest | 卖空股份总数除以流通总股数 | Vector | 60% | 131 |
| nws12_afterhsz_sl | 多头还是做空头位更有利：如果（EODHigh——最后）>（最后——EODLow），则LS=1;如果 （EODHigh - 最后） = （最后 - EODLow），则 LS = 0;如果（EODHhigh - 最后一天）<（最后 - EODLow），那么LS = -1。 | Vector | 71% | 16967 |
| nws12_afterhsz_spyclose | 收盘时SPY价格 | Vector | 71% | 118 |
| nws12_afterhsz_spylast | 新闻发布时SPY的最后价格 | Vector | 71% | 45 |
| nws12_afterhsz_tonhigh | 新闻发布前交易时段达到的最高价格 | Vector | 71% | 103 |
| nws12_afterhsz_tonlast | 新闻发布时的价格 | Vector | 71% | 18 |
| nws12_afterhsz_tonlow | 新闻发布前交易时段中达到的最低价格 | Vector | 71% | 23 |
| nws12_afterhsz_vol_ratio | Curr_Vol / Mov_Vol | Vector | 71% | 69 |
| nws12_afterhsz_volstddev | （CurrentVolume - AvgVol）/VolStDev，其中AvgVol是日成交量的平均值，VolStdDev是每日成交量的一个标准差，两者均为30日历日 | Vector | 71% | 51 |
| nws12_allz_newrecord | 追踪新闻是首次报道还是重复 | Vector | 97% | 365 |
| nws12_allz_newssess | 报道该消息的会议索引 | Vector | 97% | 101 |
| nws12_allz_provider | 新闻提供者名称索引 | Vector | 97% | 345 |
| nws12_allz_reportsess | 电子表格所报告的会议索引 | Vector | 97% | 41 |
| nws12_allz_result1 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 97% | 80 |
| nws12_allz_result2 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 97% | 42 |
| nws12_mainz_01l | 价格上涨10个百分点前的分钟数 | Vector | 97% | 1261 |
| nws12_mainz_01p | 10分钟桶中L或S的最低点数 | Vector | 97% | 2042 |
| nws12_mainz_01s | 价格下降10个百分点之前的分钟数 | Vector | 97% | 137 |
| nws12_mainz_02l | 价格上涨20个百分点前的分钟数 | Vector | 97% | 326 |
| nws12_mainz_02p | 20分钟桶中L或S的最小值 | Vector | 97% | 81 |
| nws12_mainz_02s | 价格下跌20个百分点之前的分钟数 | Vector | 97% | 32 |
| nws12_mainz_10_min | 新闻发布后前10分钟价格的百分比变化 | Vector | 96% | 29 |
| nws12_mainz_120_min | 新闻发布后前120分钟价格的百分比变化 | Vector | 97% | 37 |
| nws12_mainz_1_minute | 新闻发布后第一分钟价格的百分比变化 | Vector | 94% | 28 |
| nws12_mainz_1l | 价格上涨1个百分点前的分钟数 | Vector | 97% | 67 |
| nws12_mainz_1p | 1分钟桶的最低L或S值 | Vector | 97% | 36 |
| nws12_mainz_1s | 价格下跌1个百分点之前的分钟数 | Vector | 97% | 49 |
| nws12_mainz_2l | 价格上涨2个百分点前的分钟数 | Vector | 97% | 70 |
| nws12_mainz_2p | 2分钟桶的L或S最小值 | Vector | 97% | 82 |
| nws12_mainz_2s | 价格下跌2个百分点之前的分钟数 | Vector | 97% | 59 |
| nws12_mainz_30_min | 新闻发布后前30分钟价格的百分比变化 | Vector | 97% | 32 |
| nws12_mainz_30_seconds | 新闻发布后30秒内价格的百分比变化 | Vector | 91% | 42 |
| nws12_mainz_3l | 价格上涨3个百分点前的分钟数 | Vector | 97% | 146 |
| nws12_mainz_3p | 3分钟桶的最低L或S值 | Vector | 97% | 97 |
| nws12_mainz_3s | 价格下跌3个百分点前的分钟数 | Vector | 97% | 87 |
| nws12_mainz_41rta | 14天平均真实范围 | Vector | 97% | 12 |
| nws12_mainz_4l | 价格上涨4个百分点前的分钟数 | Vector | 97% | 156 |
| nws12_mainz_4p | 4分钟桶上方最低L或S的点数 | Vector | 97% | 43 |
| nws12_mainz_4s | 价格下跌4个百分点前的分钟数 | Vector | 97% | 167 |
| nws12_mainz_57l | 在价格上涨7.5个百分点之前，经过的分钟数 | Vector | 97% | 726 |
| nws12_mainz_57p | 7.5分钟桶中最低L或S的次数 | Vector | 97% | 98 |
| nws12_mainz_57s | 在价格下跌7.5个百分点之前，经过的分钟数 | Vector | 97% | 64 |
| nws12_mainz_5_min | 新闻发布后前5分钟价格的百分比变化 | Vector | 96% | 66 |
| nws12_mainz_5l | 价格上涨5个百分点前的分钟数 | Vector | 97% | 38 |
| nws12_mainz_5p | 5分钟桶的最低L或S数 | Vector | 97% | 29 |
| nws12_mainz_5s | 价格下降5个百分点之前的分钟数 | Vector | 97% | 46 |
| nws12_mainz_60_min | 新闻发布后前60分钟价格的百分比变化 | Vector | 97% | 52 |
| nws12_mainz_90_min | 新闻发布后前90分钟价格的百分比变化 | Vector | 97% | 25 |
| nws12_mainz_allticks | 交易日的总抽数 | Vector | 97% | 7 |
| nws12_mainz_allvwap | 所有交易日的成交量加权平均价格 | Vector | 95% | 13 |
| nws12_mainz_atrratio | 今日区间与20天平均真实区间的比值 | Vector | 97% | 88 |
| nws12_mainz_close_vol | 主收盘体积 | Vector | 95% | 11 |
| nws12_mainz_curr_vol | 当天的会议量 | Vector | 97% | 498 |
| nws12_mainz_dayopen | 开盘价 | Vector | 97% | 77 |
| nws12_mainz_div_y | 年产量 | Vector | 48% | 25 |
| nws12_mainz_eodclose | 交易日收盘价 | Vector | 97% | 135 |
| nws12_mainz_eodhigh | 新闻发布至交易时段结束之间的最高价格 | Vector | 97% | 78 |
| nws12_mainz_eodlow | 最低价格在新闻发布至交易结束之间达到。 | Vector | 97% | 54 |
| nws12_mainz_eodvwap | 成交量加权平均价格，从新闻发布到交易日结束 | Vector | 97% | 94 |
| nws12_mainz_epsactual | 新闻稿所传达的实际每股收益价值 | Vector | 87% | 50 |
| nws12_mainz_highexcstddev | （EODHigh - TONLast）/StdDev，其中StdDev是30日历日内收盘价的一个标准差 | Vector | 97% | 99 |
| nws12_mainz_lowexcstddev | （TONLast - EODLow）/StdDev，其中StdDev是30个日历日内收盘价的一个标准差 | Vector | 97% | 145 |
| nws12_mainz_mainvwap | 主交易量加权平均价格 | Vector | 95% | 12 |
| nws12_mainz_maxdnamt | 新闻发布时的价格减去新闻发布后的低点 | Vector | 97% | 57 |
| nws12_mainz_maxdown | 新闻发布时价格与新闻发布后最低价的百分比变化 | Vector | 97% | 39 |
| nws12_mainz_maxup | 从新闻发布时的价格到新闻高点后的百分比变化 | Vector | 97% | 84 |
| nws12_mainz_maxupamt | 新闻发布后的最高价减去新闻发布时的价格 | Vector | 97% | 37 |
| nws12_mainz_mktcap | 本交易日日报告的市值 | Vector | 97% | 618 |
| nws12_mainz_mov_vol | 30天移动平均交易量 | Vector | 97% | 764 |
| nws12_mainz_newrecord | 追踪新闻是首次报道还是重复 | Vector | 97% | 38 |
| nws12_mainz_newssess | 报道该消息的会议索引 | Vector | 97% | 109 |
| nws12_mainz_open_vol | 主开卷 | Vector | 95% | 9 |
| nws12_mainz_opengap | （DayOpen - 上一关闭） / 上一关闭 | Vector | 97% | 112 |
| nws12_mainz_peratio | 本交易日日的报告市盈率 | Vector | 77% | 38 |
| nws12_mainz_postvwap | 交易后成交量加权平均价格 | Vector | 87% | 10 |
| nws12_mainz_prev_vol | 前一天的会议卷 | Vector | 97% | 656 |
| nws12_mainz_prevclose | 前一交易日收盘价 | Vector | 97% | 48 |
| nws12_mainz_prevday | 前一天开盘与收盘之间的百分比变化 | Vector | 97% | 47 |
| nws12_mainz_prevwap | 会前成交量加权平均价格 | Vector | 75% | 87 |
| nws12_mainz_provider | 新闻提供者名称索引 | Vector | 97% | 82 |
| nws12_mainz_range | 交易日高价 - 交易日低价）/交易日最低价。 | Vector | 97% | 120 |
| nws12_mainz_rangeamt | 交易日高价 - 交易日最低价 | Vector | 97% | 24 |
| nws12_mainz_rangestddev | （RangeAmt-AvgRange）/RangeStdDev，其中AvgRange是日程的平均值，RangeStdDev是每日范围的一个标准差，两者均为30日历日 | Vector | 97% | 132 |
| nws12_mainz_reportsess | 电子表格所报告的会议索引 | Vector | 97% | 18 |
| nws12_mainz_result1 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 97% | 55 |
| nws12_mainz_result2 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 97% | 38 |
| nws12_mainz_result_vs_index | （（爆炸 - 爆炸） / 爆炸） - （（爆炸 - 爆炸） / 爆炸） | Vector | 97% | 94 |
| nws12_mainz_short_interest | 卖空股份总数除以流通总股数 | Vector | 86% | 355 |
| nws12_mainz_sl | 多头还是做空头位更有利：如果（EODHigh——最后）>（最后——EODLow），则LS=1;如果 （EODHigh - 最后） = （最后 - EODLow），则 LS = 0;如果（EODHhigh - 最后一天）<（最后 - EODLow），那么LS = -1。 | Vector | 97% | 99 |
| nws12_mainz_spyclose | 收盘时SPY价格 | Vector | 97% | 84 |
| nws12_mainz_spylast | 新闻发布时SPY的最后价格 | Vector | 97% | 79 |
| nws12_mainz_tonhigh | 新闻发布前交易时段达到的最高价格 | Vector | 97% | 55 |
| nws12_mainz_tonlast | 新闻发布时的价格 | Vector | 97% | 111 |
| nws12_mainz_tonlow | 新闻发布前交易时段中达到的最低价格 | Vector | 97% | 62 |
| nws12_mainz_vol_ratio | Curr_Vol / Mov_Vol | Vector | 97% | 328 |
| nws12_mainz_volstddev | （CurrentVolume - AvgVol）/VolStDev，其中AvgVol是日成交量的平均值，VolStdDev是每日成交量的一个标准差，两者均为30日历日 | Vector | 97% | 70 |
| nws12_prez_01l | 价格上涨10个百分点前的分钟数 | Vector | 92% | 908 |
| nws12_prez_01p | 10分钟桶中L或S的最低点数 | Vector | 92% | 56 |
| nws12_prez_01s | 价格下降10个百分点之前的分钟数 | Vector | 92% | 154 |
| nws12_prez_02l | 价格上涨20个百分点前的分钟数 | Vector | 92% | 59 |
| nws12_prez_02p | 20分钟桶中L或S的最小值 | Vector | 92% | 37 |
| nws12_prez_02s | 价格下跌20个百分点之前的分钟数 | Vector | 92% | 18 |
| nws12_prez_10_min | 新闻发布后前10分钟价格的百分比变化 | Vector | 51% | 25 |
| nws12_prez_120_min | 新闻发布后前120分钟价格的百分比变化 | Vector | 63% | 37 |
| nws12_prez_1_minute | 新闻发布后第一分钟价格的百分比变化 | Vector | 41% | 31 |
| nws12_prez_1l | 价格上涨1个百分点前的分钟数 | Vector | 92% | 114 |
| nws12_prez_1p | 1分钟桶的最低L或S值 | Vector | 92% | 486 |
| nws12_prez_1s | 价格下跌1个百分点之前的分钟数 | Vector | 92% | 87 |
| nws12_prez_2l | 价格上涨2个百分点前的分钟数 | Vector | 92% | 103 |
| nws12_prez_2p | 2分钟桶的L或S最低点数 | Vector | 92% | 27 |
| nws12_prez_2s | 价格下跌2个百分点之前的分钟数 | Vector | 92% | 65 |
| nws12_prez_30_min | 新闻发布后前30分钟价格的百分比变化 | Vector | 57% | 109 |
| nws12_prez_30_seconds | 新闻发布后30秒内价格的百分比变化 | Vector | 37% | 47 |
| nws12_prez_3l | 价格上涨3个百分点前的分钟数 | Vector | 92% | 80 |
| nws12_prez_3p | 3分钟桶的最低L或S值 | Vector | 92% | 36 |
| nws12_prez_3s | 价格下跌3个百分点前的分钟数 | Vector | 92% | 52 |
| nws12_prez_41rta | 十四天平均真实范围 | Vector | 91% | 34 |
| nws12_prez_4l | 价格上涨4个百分点前的分钟数 | Vector | 92% | 1779 |
| nws12_prez_4p | 4分钟桶的最低L或S。 | Vector | 92% | 725 |
| nws12_prez_4s | 价格下跌4个百分点前的分钟数 | Vector | 92% | 502 |
| nws12_prez_57l | 在价格上涨7.5个百分点之前，经过的分钟数 | Vector | 92% | 1259 |
| nws12_prez_57p | 7.5分钟桶中最低L或S的次数 | Vector | 92% | 1792 |
| nws12_prez_57s | 在价格下跌7.5个百分点之前，经过的分钟数 | Vector | 92% | 411 |
| nws12_prez_5_min | 新闻发布后前5分钟价格的百分比变化 | Vector | 47% | 39 |
| nws12_prez_5l | 价格上涨5个百分点前的分钟数 | Vector | 92% | 414 |
| nws12_prez_5p | 5分钟桶的最低L或S数 | Vector | 92% | 589 |
| nws12_prez_5s | 价格下降5个百分点之前的分钟数 | Vector | 92% | 106 |
| nws12_prez_60_min | 新闻发布后前60分钟价格的百分比变化 | Vector | 61% | 21 |
| nws12_prez_90_min | 新闻发布后前90分钟价格的百分比变化 | Vector | 63% | 40 |
| nws12_prez_allticks | 交易日的总抽数 | Vector | 92% | 305 |
| nws12_prez_allvwap | 所有交易日的成交量加权平均价格 | Vector | 92% | 74 |
| nws12_prez_atrratio | 今日区间与20天平均真实区间的比值 | Vector | 77% | 64 |
| nws12_prez_close_vol | 主收盘体积 | Vector | 91% | 81 |
| nws12_prez_curr_vol | 当天的会议量 | Vector | 77% | 64 |
| nws12_prez_dayopen | 开盘价 | Vector | 77% | 35 |
| nws12_prez_div_y | 年产量 | Vector | 44% | 12 |
| nws12_prez_eodclose | 交易日收盘价 | Vector | 77% | 17 |
| nws12_prez_eodhigh | 新闻发布至交易时段结束之间的最高价格 | Vector | 77% | 21 |
| nws12_prez_eodlow | 最低价格在新闻发布至交易结束之间达到。 | Vector | 77% | 22 |
| nws12_prez_eodvwap | 新闻发布至交易日结束期间的成交量加权平均价格 | Vector | 77% | 20 |
| nws12_prez_epsactual | 新闻稿所传达的实际每股收益价值 | Vector | 76% | 87 |
| nws12_prez_highexcstddev | （EODHigh - TONLast）/StdDev，其中StdDev是30日历日内收盘价的一个标准差 | Vector | 77% | 37 |
| nws12_prez_lowexcstddev | （TONLast - EODLow）/StdDev，其中StdDev是30个日历日内收盘价的一个标准差 | Vector | 77% | 251 |
| nws12_prez_mainvwap | 主交易量加权平均价格 | Vector | 91% | 57 |
| nws12_prez_maxdnamt | 新闻发布时的价格减去新闻发布后的低点 | Vector | 77% | 29 |
| nws12_prez_maxdown | 从新闻发布时价格到新闻低点后的百分比变化 | Vector | 77% | 69 |
| nws12_prez_maxup | 从新闻发布时的价格到新闻高点后的百分比变化 | Vector | 77% | 41 |
| nws12_prez_maxupamt | 新闻发布后的最高价减去新闻发布时的价格 | Vector | 77% | 19 |
| nws12_prez_mktcap | 本交易日日报告的市值 | Vector | 92% | 79 |
| nws12_prez_mov_vol | 30天移动平均交易量 | Vector | 91% | 676 |
| nws12_prez_newrecord | 追踪新闻是首次还是重复 | Vector | 92% | 91 |
| nws12_prez_newssess | 报道该消息的会议索引 | Vector | 92% | 107 |
| nws12_prez_open_vol | 主开卷 | Vector | 91% | 36 |
| nws12_prez_opengap | （DayOpen - 上一页关闭）/ 上一页关闭。 | Vector | 92% | 77 |
| nws12_prez_peratio | 报告的本日日历日市盈率 | Vector | 72% | 51 |
| nws12_prez_postvwap | 交易后成交量加权平均价格 | Vector | 70% | 25 |
| nws12_prez_prev_vol | 前一天的会议卷 | Vector | 79% | 168 |
| nws12_prez_prevclose | 前一交易日收盘价 | Vector | 92% | 47 |
| nws12_prez_prevday | 前一天开盘与收盘之间的百分比变化 | Vector | 92% | 133 |
| nws12_prez_prevwap | 会前成交量加权平均价格 | Vector | 77% | 13 |
| nws12_prez_provider | 新闻提供者名称索引 | Vector | 92% | 558 |
| nws12_prez_range | 交易日高价 - 交易日低价）/交易日最低价。 | Vector | 77% | 52 |
| nws12_prez_rangeamt | 交易日高价 - 交易日最低价 | Vector | 77% | 49 |
| nws12_prez_rangestddev | （RangeAmt-AvgRange）/RangeStdDev，其中AvgRange是日程的平均值，RangeStdDev是每日范围的一个标准差，两者均为30日历日 | Vector | 72% | 24 |
| nws12_prez_reportsess | 电子表格所报告的会议索引 | Vector | 92% | 70 |
| nws12_prez_result1 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 77% | 70 |
| nws12_prez_result2 | 新闻发布时价格与交易日收盘价之间的百分比变化 | Vector | 77% | 344 |
| nws12_prez_result_vs_index | （（爆炸 - 爆炸） / 爆炸） - （（爆炸 - 爆炸） / 爆炸） | Vector | 77% | 65 |
| nws12_prez_short_interest | 卖空股份总数除以流通总股数 | Vector | 81% | 444 |
| nws12_prez_sl | 多头还是做空头位更有利：如果（EODHigh——最后）>（最后——EODLow），则LS=1;如果 （EODHigh - 最后） = （最后 - EODLow），则 LS = 0;如果（EODHhigh - 最后一天）<（最后 - EODLow），那么LS = -1。 | Vector | 92% | 110 |
| nws12_prez_spyclose | 交易时段收盘时SPY价格 | Vector | 77% | 84 |
| nws12_prez_spylast | 新闻发布时SPY的最后价格 | Vector | 77% | 146 |
| nws12_prez_tonhigh | 新闻发布前该交易日达到的最高价格 | Vector | 77% | 20 |
| nws12_prez_tonlast | 新闻发布时的价格 | Vector | 77% | 24 |
| nws12_prez_tonlow | 新闻发布前交易时段中达到的最低价格 | Vector | 77% | 19 |
| nws12_prez_vol_ratio | Curr_Vol / Mov_Vol | Vector | 78% | 49 |
| nws12_prez_volstddev | （CurrentVolume - AvgVol）/VolStDev，其中AvgVol是日成交量的平均值，VolStdDev是每日成交量的一个标准差，两者均为30日历日 | Vector | 77% | 183 |

### 新闻情绪 (news18)（75 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| nws18_acb | 专注于企业行动公告的新闻情绪 | Vector | 50% | 492 |
| nws18_bam | 专注于并购的新闻情绪 | Vector | 50% | 927 |
| nws18_bee | 专注于盈利增长的新闻情绪 | Vector | 50% | 470 |
| nws18_ber | 专注于盈利结果的新闻情绪 | Vector | 50% | 580 |
| nws18_event_relevance | 事件与故事的相关性 | Vector | 50% | 848 |
| nws18_event_similarity_days | 自从检测到类似事件已过去几天 | Vector | 50% | 574 |
| nws18_ghc_lna | 分析师推荐的变更 | Vector | 50% | 1364 |
| nws18_nip | 新闻的影响程度 | Vector | 50% | 1220 |
| nws18_qcm | 相关新闻的高度信心 | Vector | 50% | 599 |
| nws18_qep | 基于全球股市的正面和负面言论的新闻情绪 | Vector | 50% | 953 |
| nws18_qmb | 专注于全球市场社论的新闻情绪 | Vector | 50% | 464 |
| nws18_relevance | 新闻对公司的相关性 | Vector | 50% | 628 |
| nws18_ssc | 新闻情绪通过多种技术计算 | Vector | 50% | 703 |
| nws18_sse | 影响公司的词句情感 | Vector | 50% | 360 |
| rp_css_assets | 资产综合情绪评分 | Matrix | 50% | 1003 |
| rp_css_business | 商业相关新闻的综合情绪评分 | Matrix | 50% | 2984 |
| rp_css_credit | 信用新闻综合情绪评分 | Matrix | 50% | 247 |
| rp_css_credit_ratings | 信用评级新闻综合情绪评分 | Matrix | 50% | 1174 |
| rp_css_dividends | 股息新闻综合情绪评分 | Matrix | 50% | 190 |
| rp_css_earnings | 财报新闻综合情绪评分 | Matrix | 50% | 1502 |
| rp_css_equity | 股权行动新闻综合情绪评分 | Matrix | 50% | 912 |
| rp_css_insider | 内幕交易新闻综合情绪评分 | Matrix | 50% | 535 |
| rp_css_inverstor | 投资者关系新闻综合情绪评分 | Matrix | 50% | 1655 |
| rp_css_labor | 劳工议题新闻综合情绪评分 | Matrix | 50% | 343 |
| rp_css_legal | 法律新闻综合情绪评分 | Matrix | 50% | 201 |
| rp_css_marketing | 市场营销新闻的综合情绪评分 | Matrix | 50% | 462 |
| rp_css_mna | 并购相关新闻的综合情绪评分 | Matrix | 50% | 541 |
| rp_css_partner | 合作伙伴关系新闻的综合情绪评分 | Matrix | 50% | 628 |
| rp_css_price | 股价新闻综合情绪评分 | Matrix | 50% | 1052 |
| rp_css_product | 产品和服务相关新闻的综合情绪评分 | Matrix | 50% | 689 |
| rp_css_ptg | 目标价格新闻的综合情绪评分 | Matrix | 50% | 707 |
| rp_css_ratings | 分析师评级相关新闻的综合情绪评分 | Matrix | 50% | 1692 |
| rp_css_revenue | 收入新闻综合情绪评分 | Matrix | 50% | 1143 |
| rp_css_society | 社会相关新闻的综合情绪评分 | Matrix | 50% | 136 |
| rp_css_technical | 基于技术分析的综合情绪评分 | Matrix | 50% | 294 |
| rp_ess_assets | 资产新闻事件情绪评分 | Matrix | 50% | 692 |
| rp_ess_business | 商业相关新闻的事件情绪评分 | Matrix | 50% | 858 |
| rp_ess_credit | 信用新闻的事件情绪评分 | Matrix | 50% | 147 |
| rp_ess_credit_ratings | 事件情绪评分信用评级新闻 | Matrix | 50% | 150 |
| rp_ess_dividends | 股息新闻的事件情绪评分 | Matrix | 50% | 103 |
| rp_ess_earnings | 财报新闻的事件情绪评分 | Matrix | 50% | 1414 |
| rp_ess_equity | 股权行动新闻的事件情绪评分 | Matrix | 50% | 559 |
| rp_ess_insider | 内幕交易新闻的事件情绪评分 | Matrix | 50% | 533 |
| rp_ess_labor | 劳动议题新闻的事件情绪评分 | Matrix | 50% | 374 |
| rp_ess_legal | 法律新闻的事件情绪评分 | Matrix | 50% | 496 |
| rp_ess_mna | 并购相关新闻的事件情绪评分 | Matrix | 50% | 1159 |
| rp_ess_partner | 事件情绪评分 合作伙伴关系新闻 | Matrix | 50% | 1417 |
| rp_ess_price | 股价新闻的事件情绪评分 | Matrix | 50% | 988 |
| rp_ess_product | 产品和服务相关新闻的事件情绪评分 | Matrix | 50% | 955 |
| rp_ess_ptg | 目标价格新闻的事件情绪评分 | Matrix | 50% | 278 |
| rp_ess_ratings | 分析师评级相关新闻的事件情绪评分 | Matrix | 50% | 1768 |
| rp_ess_revenue | 事件情绪评分收入新闻 | Matrix | 50% | 773 |
| rp_ess_society | 社会相关新闻的事件情绪评分 | Matrix | 50% | 173 |
| rp_ess_technical | 基于技术分析的事件情绪评分 | Matrix | 50% | 196 |
| rp_nip_assets | 资产新闻影响预测 | Matrix | 50% | 859 |
| rp_nip_business | 商业相关新闻的新闻影响预测 | Matrix | 50% | 1052 |
| rp_nip_credit | 信用新闻的影响预测 | Matrix | 50% | 412 |
| rp_nip_credit_ratings | 信用评级新闻的影响预测 | Matrix | 50% | 127 |
| rp_nip_dividends | 股息新闻的影响预测 | Matrix | 50% | 141 |
| rp_nip_earnings | 新闻影响预测 | Matrix | 50% | 961 |
| rp_nip_equity | 股权行动新闻的新闻影响预测 | Matrix | 50% | 752 |
| rp_nip_insider | 内幕交易新闻的影响预测 | Matrix | 50% | 665 |
| rp_nip_inverstor | 投资者关系新闻的新闻影响预测 | Matrix | 50% | 2138 |
| rp_nip_labor | 新闻影响预测劳动问题新闻 | Matrix | 50% | 274 |
| rp_nip_legal | 法律新闻的影响预测 | Matrix | 50% | 172 |
| rp_nip_marketing | 营销新闻的新闻影响预测 | Matrix | 50% | 466 |
| rp_nip_mna | 新闻影响预测 并购相关新闻 | Matrix | 50% | 439 |
| rp_nip_partner | 合伙新闻的新闻影响预测 | Matrix | 50% | 364 |
| rp_nip_price | 股价新闻的影响预测 | Matrix | 50% | 618 |
| rp_nip_product | 产品和服务相关新闻的影响预测 | Matrix | 50% | 785 |
| rp_nip_ptg | 目标价格新闻的新闻影响预测 | Matrix | 50% | 331 |
| rp_nip_ratings | 分析师评级相关新闻的新闻影响预测 | Matrix | 50% | 1705 |
| rp_nip_revenue | 收入新闻的影响预测 | Matrix | 50% | 572 |
| rp_nip_society | 社会相关新闻的新闻影响预测 | Matrix | 50% | 142 |
| rp_nip_technical | 基于技术分析的新闻影响预测 | Matrix | 50% | 136 |

### 期权-波动率 (option8)（64 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| historical_volatility_10 | 10天内的近盘历史波动 | Matrix | 70% | 2479 |
| historical_volatility_120 | 120天的近盘历史波动 | Matrix | 70% | 3663 |
| historical_volatility_150 | 150天内的近盘历史波动 | Matrix | 70% | 2176 |
| historical_volatility_180 | 180天的近盘历史波动 | Matrix | 70% | 4249 |
| historical_volatility_20 | 20天内的近盘历史波动 | Matrix | 70% | 1611 |
| historical_volatility_30 | 30天近盘历史波动 | Matrix | 70% | 1687 |
| historical_volatility_60 | 60天近盘价历史波动率 | Matrix | 70% | 2386 |
| historical_volatility_90 | 90天内的近盘历史波动 | Matrix | 70% | 1877 |
| implied_volatility_call_10 | 看涨期权10天的平值期权隐含波动率 | Matrix | 70% | 4132 |
| implied_volatility_call_1080 | 1080天看涨期权的平值期权隐含波动率 | Matrix | 70% | 8002 |
| implied_volatility_call_120 | 120天看涨期权的平值期权隐含波动率 | Matrix | 70% | 9481 |
| implied_volatility_call_150 | 150天看涨期权的平值期权隐含波动率 | Matrix | 70% | 4305 |
| implied_volatility_call_180 | 180天看涨期权的平价期权隐含波动率 | Matrix | 70% | 5549 |
| implied_volatility_call_20 | 认购期权20天的平值期权隐含波动率 | Matrix | 70% | 1964 |
| implied_volatility_call_270 | 看涨期权的平值期权隐含波动率为270天 | Matrix | 70% | 10534 |
| implied_volatility_call_30 | 看涨期权30天的平价期权隐含波动率 | Matrix | 70% | 3596 |
| implied_volatility_call_360 | 看涨期权360天的平值期权隐含波动率 | Matrix | 70% | 3409 |
| implied_volatility_call_60 | 看涨期权的平值隐含波动率，期限为60天 | Matrix | 70% | 5754 |
| implied_volatility_call_720 | 认购期权的平值期权隐含波动率为720天 | Matrix | 70% | 2989 |
| implied_volatility_call_90 | 90天看涨期权的平值期权隐含波动率 | Matrix | 70% | 3435 |
| implied_volatility_mean_10 | 平值期权隐含波动率为10天 | Matrix | 69% | 6552 |
| implied_volatility_mean_1080 | 平值期权隐含波动率意味着3年 | Matrix | 69% | 1083 |
| implied_volatility_mean_120 | 平值期权隐含波动率为120天 | Matrix | 69% | 3427 |
| implied_volatility_mean_150 | 平值期权隐含波动率为150天 | Matrix | 69% | 1781 |
| implied_volatility_mean_180 | 平值期权隐含波动率为180天 | Matrix | 69% | 1747 |
| implied_volatility_mean_20 | 平值期权隐含波动率平均为20天 | Matrix | 69% | 1056 |
| implied_volatility_mean_270 | 平值期权隐含波动率为270天 | Matrix | 69% | 946 |
| implied_volatility_mean_30 | 平值期权隐含波动率为30天 | Matrix | 69% | 1220 |
| implied_volatility_mean_360 | 平值期权隐含波动率为360天 | Matrix | 69% | 1138 |
| implied_volatility_mean_60 | 平值期权隐含波动率为60天 | Matrix | 69% | 1424 |
| implied_volatility_mean_720 | 平值期权隐含波动率为720天 | Matrix | 69% | 919 |
| implied_volatility_mean_90 | 平值期权隐含波动率为90天 | Matrix | 69% | 1574 |
| implied_volatility_mean_skew_10 | 平价期权隐含波动率意味着10天的偏斜 | Matrix | 69% | 671 |
| implied_volatility_mean_skew_1080 | 平值期权隐含波动率意味着3年期的偏斜 | Matrix | 69% | 986 |
| implied_volatility_mean_skew_120 | 平值期权隐含波动率意味着120天的偏斜 | Matrix | 69% | 815 |
| implied_volatility_mean_skew_150 | 平值期权隐含波动率平均150天的偏斜 | Matrix | 69% | 750 |
| implied_volatility_mean_skew_180 | 平值期权隐含波动率平均偏斜180天 | Matrix | 69% | 855 |
| implied_volatility_mean_skew_20 | 平价期权隐含波动率意味着20天的偏斜 | Matrix | 69% | 641 |
| implied_volatility_mean_skew_270 | 平值期权隐含波动率为270天 | Matrix | 69% | 860 |
| implied_volatility_mean_skew_30 | 平值期权隐含波动率意味着30天的偏斜 | Matrix | 69% | 733 |
| implied_volatility_mean_skew_360 | 平值期权隐含波动率意味着360天的偏斜 | Matrix | 69% | 1178 |
| implied_volatility_mean_skew_60 | 平值期权隐含波动率意味着60天的偏斜 | Matrix | 69% | 884 |
| implied_volatility_mean_skew_720 | 平值期权隐含波动率意味着720天的偏斜 | Matrix | 69% | 850 |
| implied_volatility_mean_skew_90 | 平值期权隐含波动率意味着90天的偏斜 | Matrix | 69% | 1326 |
| implied_volatility_put_10 | 看跌期权10天的平值期权隐含波动率 | Matrix | 70% | 2376 |
| implied_volatility_put_1080 | 看跌期权3年期权的平值期权隐含波动率 | Matrix | 70% | 1985 |
| implied_volatility_put_120 | 看跌期权120天的平值期权隐含波动率 | Matrix | 70% | 5017 |
| implied_volatility_put_150 | 看跌期权150天的平值期权隐含波动率 | Matrix | 70% | 3505 |
| implied_volatility_put_180 | 180天的价值期权隐含波动率 | Matrix | 70% | 4544 |
| implied_volatility_put_20 | 看跌期权20天的平值期权隐含波动率 | Matrix | 70% | 1539 |
| implied_volatility_put_270 | 卖权期权的平值隐含波动率为270天 | Matrix | 70% | 10078 |
| implied_volatility_put_30 | 30天看跌期权的平值期权隐含波动率 | Matrix | 70% | 2677 |
| implied_volatility_put_360 | 看跌期权360天的平值期权隐含波动率 | Matrix | 70% | 2524 |
| implied_volatility_put_60 | 看跌期权60天的平值期权隐含波动率 | Matrix | 70% | 3642 |
| implied_volatility_put_720 | 720天的看跌期权价值隐含波动率 | Matrix | 70% | 2271 |
| implied_volatility_put_90 | 90天看跌期权的平值期权隐含波动率 | Matrix | 70% | 3247 |
| parkinson_volatility_10 | 帕金森模型两周内的历史波动率 | Matrix | 70% | 1605 |
| parkinson_volatility_120 | 帕金森模型120天的历史波动率 | Matrix | 70% | 3733 |
| parkinson_volatility_150 | 帕金森模型150天的历史波动率 | Matrix | 70% | 1666 |
| parkinson_volatility_180 | 帕金森模型180天的历史波动率 | Matrix | 70% | 2412 |
| parkinson_volatility_20 | 帕金森模型20天的历史波动率 | Matrix | 70% | 1425 |
| parkinson_volatility_30 | 帕金森模型30天的历史波动率 | Matrix | 70% | 1355 |
| parkinson_volatility_60 | 帕金森模型60天的历史波动率 | Matrix | 70% | 1614 |
| parkinson_volatility_90 | 帕金森模型90天的历史波动率 | Matrix | 70% | 1683 |

### 期权-定价 (option9)（74 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| call_breakeven_10 | 指一只股票的看涨期权在未来10天到期时，基于其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 2337 |
| call_breakeven_1080 | 指一只股票的看涨期权在未来1080天内到期时，基于其近期买卖均值实现收支平衡的价格。 | Matrix | 70% | 1083 |
| call_breakeven_120 | 指某股票在未来120天到期的看涨期权根据其近期买卖均值实现回本的价格。 | Matrix | 70% | 884 |
| call_breakeven_150 | 指某股票在未来150天到期的看涨期权根据其近期买卖平均值实现盈亏平衡的价格。 | Matrix | 70% | 634 |
| call_breakeven_180 | 指一只股票的看涨期权在未来180天内到期，基于其近期买卖平均值实现盈亏平衡的价格。 | Matrix | 70% | 830 |
| call_breakeven_20 | 指某股票在未来20天到期的看涨期权根据其近期买卖均值实现回本。 | Matrix | 70% | 1627 |
| call_breakeven_270 | 指某股票的买权在未来270天到期时，基于其近期买卖均值实现回本的价格。 | Matrix | 70% | 600 |
| call_breakeven_30 | 指某股票的看涨期权在未来30天到期时，基于其近期买卖均值实现盈本。 | Matrix | 70% | 911 |
| call_breakeven_360 | 指某股票的看涨期权在未来360天到期时，基于其近期买卖均值实现收支平衡的价格。 | Matrix | 70% | 549 |
| call_breakeven_60 | 指某股票未来60天到期的看涨期权根据其近期买卖均值实现收支平衡的价格。 | Matrix | 70% | 532 |
| call_breakeven_720 | 指股票720天后到期的看涨期权根据其近期买卖均值实现回本的价格。 | Matrix | 70% | 538 |
| call_breakeven_90 | 指股票90天后到期的看涨期权根据其近期买卖均值实现收支平衡的价格。 | Matrix | 70% | 392 |
| forward_price_10 | 10天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 1017 |
| forward_price_1080 | 1080天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 414 |
| forward_price_120 | 120天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 340 |
| forward_price_150 | 150天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 350 |
| forward_price_180 | 180天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 503 |
| forward_price_20 | 20天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 616 |
| forward_price_270 | 270天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 456 |
| forward_price_30 | 30天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 548 |
| forward_price_360 | 360天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 532 |
| forward_price_60 | 60天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 382 |
| forward_price_720 | 720天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 501 |
| forward_price_90 | 90天远期价格源自合成多头期权，收益类似于多头股票+期权动态。多头ATM看涨期权和空头ATM看跌期权的组合。 | Matrix | 70% | 352 |
| option_breakeven_10 | 指某股票未来10天到期期权根据其近期买卖均值实现收支平衡的价格。 | Matrix | 71% | 637 |
| option_breakeven_1080 | 指某股票到期1080天后期权的回转市盈率，基于其近期买卖均值。 | Matrix | 71% | 500 |
| option_breakeven_120 | 指股票到期120天的期权根据其近期买卖均值实现盈亏平衡的价格。 | Matrix | 71% | 511 |
| option_breakeven_150 | 指某股票未来150天到期期权根据其近期买卖均值实现收支平衡的价格。 | Matrix | 71% | 312 |
| option_breakeven_180 | 指一只股票在未来180天到期期权的期权根据其近期买卖平均值实现收支平衡的价格。 | Matrix | 71% | 436 |
| option_breakeven_20 | 指股票到期20天后期权根据近期买卖均值实现收支平衡的价格。 | Matrix | 71% | 395 |
| option_breakeven_270 | 指某股票未来270天到期期权根据近期买卖均值实现收支平衡的价格。 | Matrix | 71% | 557 |
| option_breakeven_30 | 指股票到期30天后期权根据其近期买卖平均值实现收支平衡的价格。 | Matrix | 71% | 371 |
| option_breakeven_360 | 指股票未来360天到期期权根据近期买卖均值实现收支平衡的价格。 | Matrix | 71% | 367 |
| option_breakeven_60 | 指股票未来60天到期期权根据近期买卖均值实现回本的价格。 | Matrix | 71% | 269 |
| option_breakeven_720 | 指股票未来720天到期期权的市盈率，基于其近期买卖均值实现收支平衡的价格。 | Matrix | 71% | 239 |
| option_breakeven_90 | 指股票90天后到期期权根据其近期买卖平均值实现收支平衡的价格。 | Matrix | 71% | 321 |
| pcr_oi_10 | 股票期权到期日10天时，看跌期权未平仓合约与赎回期权的比率。 | Matrix | 71% | 1307 |
| pcr_oi_1080 | 股票期权到期1080天后，看跌期权的未平仓合约与赎回未平仓合约的比率。 | Matrix | 71% | 1144 |
| pcr_oi_120 | 股票期权到期120天后，期权的买入未平合约与赎回期权的比率。 | Matrix | 71% | 1340 |
| pcr_oi_150 | 股票期权到期150天时，买权未平合约与赎回期权的比率。 | Matrix | 71% | 1242 |
| pcr_oi_180 | 到期日为未来180天的股票期权，买权平仓合约与赎回未平仓合约的比率。 | Matrix | 71% | 2367 |
| pcr_oi_20 | 指股票期权到期20天后，期权的买仓未平仓合约与未平仓合约的比率。 | Matrix | 71% | 582 |
| pcr_oi_270 | 指股票期权到期270天时，期权的未平仓合约与赎回期权的比率。 | Matrix | 71% | 10598 |
| pcr_oi_30 | 股票期权到期30天后，买权未平合约与赎回期权的比率。 | Matrix | 71% | 757 |
| pcr_oi_360 | 股票期权到期360天后，看跌期权未平合约与赎回未平仓合约的比率。 | Matrix | 71% | 953 |
| pcr_oi_60 | 股票期权到期60天后，看跌期权未平仓合约与赎回未平仓合约的比率。 | Matrix | 71% | 859 |
| pcr_oi_720 | 股票期权到期日为720天后，看跌期未收合约与赎回未平合约的比率。 | Matrix | 71% | 785 |
| pcr_oi_90 | 指股票期权到期90天后，期权的未平仓合约与赎回未平合约的比率。 | Matrix | 71% | 1102 |
| pcr_oi_all | 股票期权所有到期日的买权未平合约与买权未平仓合约的比率。 | Matrix | 71% | 847 |
| pcr_vol_10 | 指到期10天后股票期权的看跌成交量与看涨期权量的比率。 | Matrix | 70% | 407 |
| pcr_vol_1080 | 到期还有1080天的股票期权的看跌权成交量与赎回权量的比率。 | Matrix | 70% | 443 |
| pcr_vol_120 | 股票期权到期120天时，期权的卖权成交量与看涨期权量的比率。 | Matrix | 70% | 285 |
| pcr_vol_150 | 指股票期权到期时间为150天的期权卖权量与看涨成交量的比率。 | Matrix | 70% | 286 |
| pcr_vol_180 | 到期日为未来180天的股票期权的看跌权成交量与看涨期权量的比率。 | Matrix | 70% | 476 |
| pcr_vol_20 | 指股票期权到期20天时的看跌成交量与看涨期权量的比率。 | Matrix | 70% | 210 |
| pcr_vol_270 | 指未来270天到期股票期权的买权成交量与看涨期权量的比率。 | Matrix | 70% | 512 |
| pcr_vol_30 | 到期30天后股票期权的卖权量与赎回权量的比率。 | Matrix | 70% | 230 |
| pcr_vol_360 | 指到期日为未来360天的股票期权看跌期权量与赎回期权量的比率。 | Matrix | 70% | 433 |
| pcr_vol_60 | 指股票期权到期60天时，看跌成交量与赎回权成交量的比率。 | Matrix | 70% | 218 |
| pcr_vol_720 | 指未来720天到期的股票期权的卖权量与看涨期权量的比率。 | Matrix | 70% | 228 |
| pcr_vol_90 | 指股票期权到期90天后，期权的看跌成交量与看涨期权量的比率。 | Matrix | 70% | 174 |
| pcr_vol_all | 股票期权所有到期日的看跌期权成交量与看涨期权量的比率。 | Matrix | 70% | 363 |
| put_breakeven_10 | 指一只股票的看跌期权在未来10天到期时的盈亏平衡，基于其近期买卖均值。 | Matrix | 70% | 851 |
| put_breakeven_1080 | 指股票的看跌期权在未来1080天到期时，基于其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 730 |
| put_breakeven_120 | 指股票120天后到期的看跌期权根据其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 394 |
| put_breakeven_150 | 指股票150天后到期的看跌期权根据其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 347 |
| put_breakeven_180 | 指一只股票在未来180天到期的看跌期权根据其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 280 |
| put_breakeven_20 | 指股票的看跌期权在未来20天到期时，基于其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 333 |
| put_breakeven_270 | 指股票在未来270天到期的看跌期权根据其近期买卖均值实现回本的价格。 | Matrix | 70% | 311 |
| put_breakeven_30 | 指某股票的看跌期权在未来30天到期时，基于其近期买卖均值实现收支平衡的价格。 | Matrix | 70% | 324 |
| put_breakeven_360 | 指股票的看跌期权在未来360天到期时，基于其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 376 |
| put_breakeven_60 | 指某股票的卖权到期日为60天，基于其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 292 |
| put_breakeven_720 | 指某股票的看跌期权在未来720天到期时，基于其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 369 |
| put_breakeven_90 | 指股票90天后到期的看跌期权根据其近期买卖均值实现盈亏平衡的价格。 | Matrix | 70% | 375 |

### 价格成交量 (pv1)（23 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| adv20 | 过去20天的平均日销量 | Matrix | 100% | 96100 |
| cap | 每日市值（以百万计） | Matrix | 100% | 391861 |
| close | 日收价 | Matrix | 100% | 506708 |
| country | 国家分组 | Group | 100% | 19343 |
| currency | 货币 | Group | 100% | 3502 |
| cusip | CUSIP值 | Symbol | 100% | 35 |
| dividend | 股息 | Matrix | 100% | 11137 |
| exchange | 交换分组 | Group | 100% | 48609 |
| high | 日内最高价 | Matrix | 100% | 53301 |
| industry | 行业分组 | Group | 100% | 207718 |
| isin | ISIN价值 | Symbol | 100% | 0 |
| low | 日低价 | Matrix | 100% | 46173 |
| market | 市场分组 | Group | 100% | 114455 |
| open | 日均开盘价 | Matrix | 100% | 50627 |
| returns | 每日回报 | Matrix | 100% | 306753 |
| sector | 扇区分组 | Group | 100% | 313023 |
| sedol | 世都 | Symbol | 100% | 135 |
| sharesout | 每日流通股数（以百万计） | Matrix | 100% | 28518 |
| split | 股票拆分比率 | Matrix | 100% | 17343 |
| subindustry | 子行业分组 | Group | 100% | 251541 |
| ticker | 行情 | Symbol | 100% | 261 |
| volume | 日交易量 | Matrix | 100% | 281702 |
| vwap | 日成交量加权平均价格 | Matrix | 100% | 62753 |

### 行业分组 (pv13)（164 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| primary_sector_focused_company_count | 主要聚焦于某一行业的公司数量。 | Matrix | 35% | 12 |
| pv13_1l_scibr | 分组字段 | Group | 93% | 2763 |
| pv13_2l_scibr | 分组字段 | Group | 100% | 296 |
| pv13_3l_scibr | 分组字段 | Group | 100% | 1240 |
| pv13_4l_scibr | 分组字段 | Group | 100% | 613 |
| pv13_5l_scibr | 分组字段 | Group | 100% | 811 |
| pv13_6l_scibr | 分组字段 | Group | 100% | 641 |
| pv13_com_page_rank | 竞争对手的PageRank | Matrix | 90% | 1841 |
| pv13_com_rk_au | 参赛者的HITS权威评分 | Matrix | 90% | 2003 |
| pv13_custretsig_retsig | 客户回归的迹象 | Matrix | 93% | 2170 |
| pv13_di_5l | 分组字段 | Group | 100% | 8 |
| pv13_di_6l | 分组字段 | Group | 100% | 5 |
| pv13_h2_min2_1k_sector | 前1000名的分组 | Group | 37% | 1737 |
| pv13_h2_sector | 分组字段 | Group | 100% | 2418 |
| pv13_h_f1_sector | 分组字段 | Group | 100% | 5026 |
| pv13_h_f3_sector | 分组字段 | Group | 100% | 706 |
| pv13_h_min10_all_sector | 分组字段 | Group | 100% | 877 |
| pv13_h_min10_top3000_sector | 分组字段 | Group | 100% | 767 |
| pv13_h_min20_top3000_sector | 分组字段 | Group | 100% | 929 |
| pv13_h_min22_1000_sector | 前1000名的分组 | Group | 37% | 1174 |
| pv13_h_min24_500_sector | 前500名的分组 | Group | 19% | 772 |
| pv13_h_min2_3000_sector | 分组字段 | Group | 100% | 17818 |
| pv13_h_min2_focused_pureplay_3000_sector | 分组字段 | Group | 100% | 10461 |
| pv13_h_min2_focused_sector | 前200名的分组 | Group | 19% | 1359 |
| pv13_h_min30_3000_mapped_sector | 分组字段 | Group | 100% | 473 |
| pv13_h_min51_f3_sector | 分组字段 | Group | 100% | 679 |
| pv13_h_min52_1k_sector | 前1000名的分组 | Group | 37% | 911 |
| pv13_h_min52_3000_sector | 分组字段 | Group | 100% | 431 |
| pv13_h_min5_3000_sector | 分组字段 | Group | 100% | 585 |
| pv13_h_min5_500_sector | 分组字段 | Group | 19% | 235 |
| pv13_hierarchy23_513_sector | 分组字段 | Group | 99% | 60 |
| pv13_hierarchy23_sector | 分组字段 | Group | 100% | 1063 |
| pv13_hierarchy2_513_sector | 分组字段 | Group | 99% | 67 |
| pv13_hierarchy2_min2_1k_513_sector | 分组字段 | Group | 35% | 3 |
| pv13_hierarchy_f1_513_sector | 分组字段 | Group | 99% | 36 |
| pv13_hierarchy_f2_513_sector | 分组字段 | Group | 99% | 24 |
| pv13_hierarchy_f2_sector | 分组字段 | Group | 100% | 46 |
| pv13_hierarchy_f3_513_sector | 分组字段 | Group | 99% | 7 |
| pv13_hierarchy_f4_513_sector | 分组字段 | Group | 99% | 12 |
| pv13_hierarchy_f4_sector | 分组字段 | Group | 100% | 30 |
| pv13_hierarchy_min100_2000_513_sector | 分组字段 | Group | 69% | 8 |
| pv13_hierarchy_min100_corr21_513_sector | 分组字段 | Group | 63% | 24 |
| pv13_hierarchy_min100_corr21_sector | 分组字段 | Group | 65% | 7 |
| pv13_hierarchy_min10_1000_513_sector | 分组字段 | Group | 35% | 2 |
| pv13_hierarchy_min10_2k_513_sector | 分组字段 | Group | 69% | 14 |
| pv13_hierarchy_min10_2k_sector | 分组字段 | Group | 72% | 127 |
| pv13_hierarchy_min10_3k_all_sector | 分组字段 | Group | 100% | 23 |
| pv13_hierarchy_min10_513_sector | 分组字段 | Group | 69% | 53 |
| pv13_hierarchy_min10_industry_3000_513_sector | 分组字段 | Group | 99% | 34 |
| pv13_hierarchy_min10_industry_3000_sector | 分组字段 | Group | 100% | 35 |
| pv13_hierarchy_min10_sector | 分组字段 | Group | 72% | 75 |
| pv13_hierarchy_min10_sector_3000_513_sector | 分组字段 | Group | 99% | 22 |
| pv13_hierarchy_min10_sector_3000_sector | 分组字段 | Group | 100% | 28 |
| pv13_hierarchy_min10_top3000_513_sector | 分组字段 | Group | 99% | 21 |
| pv13_hierarchy_min20_3k_513_sector | 分组字段 | Group | 99% | 6 |
| pv13_hierarchy_min20_3k_sector | 分组字段 | Group | 100% | 29 |
| pv13_hierarchy_min20_513_sector | 分组字段 | Group | 69% | 8 |
| pv13_hierarchy_min20_f3_513_sector | 分组字段 | Group | 99% | 9 |
| pv13_hierarchy_min20_sector | 分组字段 | Group | 72% | 13 |
| pv13_hierarchy_min20_top3000_513_sector | 分组字段 | Group | 99% | 14 |
| pv13_hierarchy_min22_1000_513_sector | 分组字段 | Group | 35% | 5 |
| pv13_hierarchy_min22_513_sector | 分组字段 | Group | 69% | 4 |
| pv13_hierarchy_min22_sector | 分组字段 | Group | 72% | 22 |
| pv13_hierarchy_min25_513_sector | 分组字段 | Group | 69% | 6 |
| pv13_hierarchy_min25_sector | 分组字段 | Group | 72% | 18 |
| pv13_hierarchy_min2_1000_513_sector | 分组字段 | Group | 35% | 10 |
| pv13_hierarchy_min2_3000_513_sector | 分组字段 | Group | 99% | 16 |
| pv13_hierarchy_min2_513_sector | 分组字段 | Group | 69% | 13 |
| pv13_hierarchy_min2_focused_only_513_sector | 分组字段 | Group | 69% | 7 |
| pv13_hierarchy_min2_focused_only_sector | 分组字段 | Group | 72% | 1087 |
| pv13_hierarchy_min2_focused_pureplay_513_sector | 分组字段 | Group | 69% | 21 |
| pv13_hierarchy_min2_focused_pureplay_sector | 分组字段 | Group | 72% | 28 |
| pv13_hierarchy_min2_pureplay_only_513_sector | 分组字段 | Group | 69% | 111 |
| pv13_hierarchy_min2_pureplay_only_sector | 分组字段 | Group | 72% | 1059 |
| pv13_hierarchy_min2_sector | 分组字段 | Group | 72% | 108 |
| pv13_hierarchy_min30_3000_513_sector | 分组字段 | Group | 99% | 14 |
| pv13_hierarchy_min30_3000_mapped_513_sector | 分组字段 | Group | 99% | 13 |
| pv13_hierarchy_min30_513_sector | 分组字段 | Group | 69% | 7 |
| pv13_hierarchy_min30_sector | 分组字段 | Group | 72% | 11 |
| pv13_hierarchy_min40_3000_513_sector | 分组字段 | Group | 99% | 15 |
| pv13_hierarchy_min50_f3_513_sector | 分组字段 | Group | 99% | 17 |
| pv13_hierarchy_min51_f1_513_sector | 分组字段 | Group | 99% | 9 |
| pv13_hierarchy_min51_f1_sector | 分组字段 | Group | 100% | 49 |
| pv13_hierarchy_min51_f2_513_sector | 分组字段 | Group | 99% | 9 |
| pv13_hierarchy_min51_f2_sector | 分组字段 | Group | 100% | 18 |
| pv13_hierarchy_min51_f3_513_sector | 分组字段 | Group | 99% | 15 |
| pv13_hierarchy_min51_f4_513_sector | 分组字段 | Group | 99% | 25 |
| pv13_hierarchy_min51_f4_sector | 分组字段 | Group | 100% | 41 |
| pv13_hierarchy_min52_1k_513_sector | 分组字段 | Group | 35% | 4 |
| pv13_hierarchy_min52_2k_513_sector | 分组字段 | Group | 69% | 5 |
| pv13_hierarchy_min52_2k_sector | 分组字段 | Group | 72% | 12 |
| pv13_hierarchy_min52_513_sector | 分组字段 | Group | 99% | 8 |
| pv13_hierarchy_min52_sector | 分组字段 | Group | 100% | 23 |
| pv13_hierarchy_min54_3000_sector | 分组字段 | Group | 100% | 32 |
| pv13_hierarchy_min5_1000_513_sector | 分组字段 | Group | 35% | 23 |
| pv13_hierarchy_min5_3000_513_sector | 分组字段 | Group | 99% | 15 |
| pv13_hierarchy_min5_513_sector | 分组字段 | Group | 69% | 7 |
| pv13_hierarchy_min5_corr21_1000_513_sector | 分组字段 | Group | 35% | 4 |
| pv13_hierarchy_min5_f3g2_sector | 分组字段 | Group | 100% | 61 |
| pv13_hierarchy_min5_sector | 分组字段 | Group | 72% | 18 |
| pv13_hierarchy_sector | 分组字段 | Group | 100% | 100 |
| pv13_hierarchys32_513_sector | 分组字段 | Group | 99% | 10 |
| pv13_hierarchys32_sector | 分组字段 | Group | 100% | 71 |
| pv13_new_1l_scibr | 分组字段 | Group | 87% | 1236 |
| pv13_new_2l_scibr | 分组字段 | Group | 100% | 78 |
| pv13_new_3l_scibr | 分组字段 | Group | 100% | 56 |
| pv13_new_4l_scibr | 分组字段 | Group | 100% | 99 |
| pv13_new_5l_scibr | 分组字段 | Group | 100% | 122 |
| pv13_new_6l_scibr | 分组字段 | Group | 100% | 178 |
| pv13_ompetitorgraphrank_hub_rank | HITS中心竞赛者评分 | Matrix | 90% | 1357 |
| pv13_r2_liquid_min10_sector | 分组字段 | Group | 19% | 605 |
| pv13_r2_liquid_min2_sector | 分组字段 | Group | 19% | 79 |
| pv13_r2_liquid_min5_sector | 分组字段 | Group | 19% | 118 |
| pv13_r2_min10_1000_sector | 分组字段 | Group | 37% | 184 |
| pv13_r2_min10_3000_sector | 分组字段 | Group | 100% | 614 |
| pv13_r2_min20_1000_sector | 分组字段 | Group | 37% | 249 |
| pv13_r2_min20_3000_sector | 分组字段 | Group | 100% | 10864 |
| pv13_r2_min2_1000_sector | 分组字段 | Group | 37% | 187 |
| pv13_r2_min2_3000_sector | 分组字段 | Group | 100% | 17966 |
| pv13_r2_min5_1000_sector | 分组字段 | Group | 37% | 183 |
| pv13_r2_min5_3000_sector | 分组字段 | Group | 100% | 765 |
| pv13_rcsed_6l | 分组字段 | Group | 100% | 2 |
| pv13_revere_city | 城市代码 | Matrix | 100% | 1455 |
| pv13_revere_company_total | 该行业公司总数 | Matrix | 35% | 649 |
| pv13_revere_comproduct_company | 公司产品 | Matrix | 41% | 37 |
| pv13_revere_country | 国家代码 | Matrix | 100% | 1025 |
| pv13_revere_index_cap | 公司市值 | Matrix | 100% | 1735 |
| pv13_revere_index_value | 指定日期索引的值 | Matrix | 100% | 413 |
| pv13_revere_key_sector_total | 公司重点行业的数量 | Matrix | 100% | 3200 |
| pv13_revere_level | 部门在层级中的级别 | Matrix | 62% | 567 |
| pv13_revere_parent | 母部门代码 | Matrix | 62% | 470 |
| pv13_revere_term | 表示扇区为终端扇区（即无子扇区） | Matrix | 41% | 258 |
| pv13_revere_term_sector_total | 公司终端部门数量 | Matrix | 100% | 3065 |
| pv13_revere_zipcode | 邮政编码 | Matrix | 92% | 1114 |
| pv13_reveremap | 映射数据 | Matrix | 99% | 2879 |
| pv13_rha2_min10_1000_513_sector | 分组字段 | Group | 35% | 4 |
| pv13_rha2_min10_3000_513_sector | 分组字段 | Group | 99% | 17 |
| pv13_rha2_min10_513_sector | 分组字段 | Group | 70% | 6 |
| pv13_rha2_min10_sector | 分组字段 | Group | 72% | 14 |
| pv13_rha2_min20_3000_513_sector | 分组字段 | Group | 99% | 21 |
| pv13_rha2_min20_513_sector | 分组字段 | Group | 70% | 13 |
| pv13_rha2_min20_sector | 分组字段 | Group | 72% | 17 |
| pv13_rha2_min2_1000_513_sector | 分组字段 | Group | 35% | 7 |
| pv13_rha2_min2_3000_513_sector | 分组字段 | Group | 99% | 10 |
| pv13_rha2_min2_513_sector | 分组字段 | Group | 70% | 6 |
| pv13_rha2_min2_sector | 分组字段 | Group | 72% | 1569 |
| pv13_rha2_min30_3000_513_sector | 分组字段 | Group | 99% | 20 |
| pv13_rha2_min40_3000_513_sector | 分组字段 | Group | 99% | 33 |
| pv13_rha2_min5_1000_513_sector | 分组字段 | Group | 35% | 9 |
| pv13_rha2_min5_3000_513_sector | 分组字段 | Group | 99% | 11 |
| pv13_rha2_min5_513_sector | 分组字段 | Group | 70% | 2 |
| pv13_rha2_min5_sector | 分组字段 | Group | 72% | 1627 |
| pv13_ustomergraphrank_auth_rank | 客户的HITS（高级权威评分） | Matrix | 79% | 511 |
| pv13_ustomergraphrank_hub_rank | HITS Hub 客户评分 | Matrix | 79% | 937 |
| pv13_ustomergraphrank_page_rank | 客户的PageRank | Matrix | 79% | 867 |
| rel_num_all | 与该仪器产品有重叠的公司数量 | Matrix | 99% | 3845 |
| rel_num_comp | 该乐器的竞争对手数量 | Matrix | 89% | 1870 |
| rel_num_cust | 该乐器的客户数量 | Matrix | 51% | 2373 |
| rel_num_part | 乐器合作伙伴数量 | Matrix | 78% | 5991 |
| rel_ret_all | 产品与该工具重叠公司的平均一日回报率 | Matrix | 96% | 1864 |
| rel_ret_comp | 竞争公司平均一日回报率 | Matrix | 82% | 2623 |
| rel_ret_cust | 仪器用户的平均一天回报率 | Matrix | 49% | 564 |
| rel_ret_part | 该仪器合作伙伴的平均一天回报 | Matrix | 71% | 2645 |
| single_sector_pureplay_company_count | 仅在单一行业运营的公司数量。 | Matrix | 35% | 13 |

### 社交媒体-情感 (socialmedia12)（18 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| scl12_alltype_buzzvec | 情感量 | Vector | 95% | 80 |
| scl12_alltype_sentvec | 情感 | Vector | 95% | 22 |
| scl12_alltype_typevec | 工具类型指数 | Vector | 95% | 21 |
| scl12_buzz | 相对情绪量 | Matrix | 100% | 18898 |
| scl12_buzz_fast_d1 | 相对情绪量 | Matrix | 98% | 95 |
| scl12_buzzvec | 情感量 | Vector | 100% | 4066 |
| scl12_sentiment | 情感 | Matrix | 100% | 3070 |
| scl12_sentiment_fast_d1 | 情感 | Matrix | 98% | 93 |
| scl12_sentvec | 情感 | Vector | 100% | 577 |
| scl12_typevec | 工具类型指数 | Vector | 100% | 516 |
| snt_buzz | 负的相对情感体积，将nan填入0 | Matrix | 100% | 8551 |
| snt_buzz_bfl | 负的相对情绪体积，填满南 | Matrix | 100% | 5537 |
| snt_buzz_bfl_fast_d1 | 负的相对情绪体积，填满南 | Matrix | 100% | 83 |
| snt_buzz_fast_d1 | 负的相对情感体积，将nan填入0 | Matrix | 98% | 98 |
| snt_buzz_ret | 相对情绪成交量的负回报 | Matrix | 100% | 3759 |
| snt_buzz_ret_fast_d1 | 相对情绪成交量的负回报 | Matrix | 98% | 38 |
| snt_value | 负面情绪，把南填满0 | Matrix | 100% | 2278 |
| snt_value_fast_d1 | 负面情绪，把南填满0 | Matrix | 98% | 81 |

### 社交媒体-情绪 (socialmedia8)（2 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| snt_social_value | 情感的Z分 | Matrix | 86% | 4657 |
| snt_social_volume | 归一化推文量 | Matrix | 86% | 4635 |

### 股票池 (univ1)（6 个字段）

| 字段名 | 中文描述 | 类型 | 覆盖率 | Alpha引用 |
|--------|----------|------|--------|-----------|
| top1000 | 无现场描述 | Universe | 33% | 8 |
| top200 | 无现场描述 | Universe | 7% | 7 |
| top2000 | 无现场描述 | Universe | — | 0 |
| top3000 | 无现场描述 | Universe | 100% | 55 |
| top500 | 无现场描述 | Universe | 17% | 30 |
| topsp500 | 无现场描述 | Universe | 22% | 3 |

## 三、Alpha 高频引用字段 Top 30

按 Alpha 引用数排序，展示最常被量化策略使用的字段：

| 排名 | 字段名 | 数据集 | 中文描述 | Alpha引用 | 覆盖率 |
|------|--------|--------|----------|-----------|--------|
| 1 | anl4_qf_az_eps_mean | analyst4 | 每股收益——估算平均值 | 996 | 78% |
| 2 | fnd6_txndbr | fundamental6 | 递延税款剩余 | 995 | 50% |
| 3 | anl4_epsr_mean | analyst4 | GAAP每股收益——估算平均值 | 991 | 72% |
| 4 | fnd6_newqv1300_xoprq | fundamental6 | 运营费用 - 总额 | 991 | 50% |
| 5 | correlation_last_30_days_spy | model51 | 30天内与SPY的相关性 | 991 | 78% |
| 6 | anl4_basicdetaillt_person | analyst4 | 经纪人标识 | 99 | 68% |
| 7 | anl4_netdebt_high | analyst4 | 净债务——最高估计 | 99 | 52% |
| 8 | fnd6_newqv1300_lnoq | fundamental6 | 负债净额及其他调整 | 99 | 50% |
| 9 | fnd6_newqv1300_xoptq | fundamental6 | 隐含期权费用 | 99 | 50% |
| 10 | nws12_mainz_highexcstddev | news12 | （EODHigh - TONLast）/StdDev，其中StdDev是30日历日内收盘价的一个标准差 | 99 | 97% |
| 11 | nws12_mainz_sl | news12 | 多头还是做空头位更有利：如果（EODHigh——最后）>（最后——EODLow），则LS=1;如果 （EODHigh - 最后） = （最后 - EODLow），则 LS = 0;如果（EODHhigh - 最后一天）<（最后 - EODLow），那么LS = -1。 | 99 | 97% |
| 12 | pv13_new_4l_scibr | pv13 | 分组字段 | 99 | 100% |
| 13 | fn_line_of_credit_facility_max_borrowing_capacity_q | fundamental2 | 信用便利的最高借款额度，不考虑当前可借款金额或当前未偿还金额的限制。 | 989 | 50% |
| 14 | news_pct_120min | news12 | 新闻发布后前120分钟价格的百分比变化 | 989 | 91% |
| 15 | fnd6_recta | fundamental6 | 留存收益 - 累计翻译调整 | 988 | 50% |
| 16 | rp_ess_price | news18 | 股价新闻的事件情绪评分 | 988 | 50% |
| 17 | implied_volatility_mean_skew_1080 | option8 | 平值期权隐含波动率意味着3年期的偏斜 | 986 | 69% |
| 18 | liabilities_curr | fundamental6 | 流动负债 - 总额 | 9815 | 50% |
| 19 | cashflow_efficiency_rank_derivative | model16 | 现金流生成和盈利能力排名较上一期有所变化。 | 98 | 100% |
| 20 | nws12_afterhsz_5p | news12 | 5分钟桶的最低L或S数 | 98 | 71% |
| 21 | nws12_mainz_57p | news12 | 7.5分钟桶中最低L或S的次数 | 98 | 97% |
| 22 | snt_buzz_fast_d1 | socialmedia12 | 负的相对情感体积，将nan填入0 | 98 | 98% |
| 23 | fnd6_cptnewqv1300_rectq | fundamental6 | 应收账款 - 总计 | 978 | 50% |
| 24 | cogs | fundamental6 | 销售成本 | 9741 | 50% |
| 25 | fnd6_newa2v1300_rdipa | fundamental6 | 在批研发费用税后 | 971 | 50% |
| 26 | anl4_qf_az_wol_spfc | analyst4 | 每股现金流——最低估计 | 97 | 33% |
| 27 | fnd2_a_dbplctrbyemp | fundamental2 | 雇主向确定福利计划缴纳的金额。 | 97 | 30% |
| 28 | fnd6_intseg | fundamental6 | 跨段淘汰赛 | 97 | 50% |
| 29 | nws12_mainz_3p | news12 | 3分钟桶的最低L或S值 | 97 | 97% |
| 30 | anl4_dez1qfv4_est | analyst4 | 估计值 | 968 | 96% |

## 四、字段类型分布

| 类型 | 数量 | 说明 |
|------|------|------|
| Matrix | 1713 | 矩阵型（每只股票每天一个值） |
| Vector | 763 | 向量型 |
| Group | 141 | 分组型 |
| Universe | 6 | 股票池定义 |
| Symbol | 4 |  |
