# WorldQuant BRAIN 平台模拟运行机制详解

**文档版本**: 1.0  
**创建日期**: 2026-04-04  
**适用平台**: WorldQuant BRAIN  
**标签**: `simulation` `position` `neutralization` `rank-operator` `market-neutral`

---

## 📖 目录
1. [头寸（Position）管理](#头寸position管理)
2. [表达式计算流程](#表达式计算流程)
3. [市场中性化（Market Neutralization）](#市场中性化market-neutralization)
4. [实战操作指南](#实战操作指南)

---

## 🎯 一、头寸（Position）管理

### 1.1 核心概念
当启动模拟时，BRAIN 通过设置**头寸（Positions）**计算每只股票的投资金额。

### 1.2 头寸类型

| 头寸类型 | 英文名称 | 操作 | 预期 |
|---------|---------|------|------|
| **多头** | Long Position | 买入股票 | 押注股价**上涨** |
| **空头** | Short Position | 卖出股票 | 押注股价**下跌** |

### 1.3 计算流程
点击 **Simulate** 按钮后，BRAIN 按以下步骤计算头寸：

`Alpha 值计算 → 减去均值 → 中心化 → 绝对值 → 标准化权重 → 资本分配 → 利润计算`

### 1.4 计算示例（8只股票）

![example](https://api.worldquantbrain.com/content/images/MbmDbBPhnUIIHmlONixQvzKlCr4=/391/original/Navigator_Whats_Going_On.png)


#### 关键计算步骤说明：

1. **Alpha 值计算**：`rank(-returns)` 生成 0 到 1 的排名值
2. **减去均值**：每个值减去平均值 0.50
3. **中心化**：将数值围绕 0 对称分布（负值为空头，正值为多头）
4. **绝对值**：取中心化后的绝对值用于权重计算
5. **标准化权重**：确保所有权重之和为 1.0
6. **资本分配**：按权重分配`$20Mn`资本（多头+\$10M，空头-\$10M）
7. **利润计算**：根据次日回报计算盈亏

---

## 🔢 二、表达式计算流程

### 2.1 rank() 算子工作机制

**功能**：对输入值进行排名，并按降序从 1 到 0 均匀排列。

#### 示例：5 只股票的 rank() 输出

| 股票 | 原始输入值 | 排名顺序 | rank() 输出 |
|:----:|:----------:|:--------:|:-----------:|
| A | 最低值 | 1 | **0** |
| B | 次低值 | 2 | **0.25** |
| C | 中间值 | 3 | **0.5** |
| D | 次高值 | 4 | **0.75** |
| E | 最高值 | 5 | **1** |

**映射公式**：
`rank_value = (ranking_position - 1) / (total_stocks - 1)`

### 2.2 计算流程示意
原始数据 (returns)
↓
取反 (-returns)
↓
排名 (rank)
↓
输出 [0, 0.25, 0.5, 0.75, 1]
↓
中性化 (Neutralization)
↓
最终头寸分配

---

## 🌐 三、市场中性化（Market Neutralization）

### 3.1 什么是中性化？

**Neutralization（中性化）** = 从 Alpha 中**移除特定影响**

#### 为什么需要中性化？

| 问题 | 风险 | 解决方案 |
|------|------|---------|
| 整体市场走势影响股价 | 仅持有多头头寸 → 高市场暴露风险 | 构建多空组合（Long-Short Portfolio） |
| 行业/板块轮动影响 | 组合偏向特定行业 | 行业中性化 |
| 市值因子偏差 | 偏向大盘股或小盘股 | 市值中性化 |

### 3.2 BRAIN 的中性化策略

**默认设置**：构建**多空组合**
- **50% 多头头寸**（Long Positions）
- **50% 空头头寸**（Short Positions）
- **净市场暴露 ≈ 0%**（市场中性）

#### 多空组合的优势

✅ **隔离 Alpha 能力**：剥离市场方向性影响，纯粹考验选股能力  
✅ **降低系统性风险**：市场涨跌对组合影响相互抵消  
✅ **提高 Sharpe 比率**：风险调整后收益更高  
✅ **资本效率**：同时做多优质股 + 做空劣质股

### 3.3 中性化设置对比

| 设置项 | 组合类型 | 头寸范围 | 适用场景 |
|--------|---------|---------|---------|
| **Neutralization: Market** | 多空组合 | [-1, +1] | ✅ 默认推荐，市场中性 |
| **Neutralization: None** | 仅多头组合 | [0, +1] | 测试纯多头策略 |
| **Neutralization: Sector** | 行业中性 | 组内多空 | 避免行业暴露 |

---

## 🛠️ 四、实战操作指南

### 4.1 如何测试不同中性化设置？

#### 步骤 1：进入设置
1. 点击编辑器上方的 **Settings** 按钮
2. 找到 **NEUTRALIZATION** 下拉菜单

#### 步骤 2：修改设置
设置界面：
![example2](https://api.worldquantbrain.com/content/images/RgRWklm-wIGrsldmSpKxqcIFxXc=/392/original/Navigator_Market_Neutralization_None.png)

#### 步骤 3：对比结果
1. **第一次模拟**：`Neutralization = Market`（默认）
2. **第二次模拟**：`Neutralization = None`
3. **对比指标**：
   - Sharpe Ratio
   - Returns
   - Drawdown
   - Turnover

### 4.2 观察要点

#### 仅多头组合（Neutralization: None）
- `rank()` 输出范围：**0 到 1**
- 所有头寸 ≥ 0（无空头）
- 组合表现受市场方向影响大
- 适合测试**纯多头策略**

#### 多空组合（Neutralization: Market）
- 中心化后范围：**-0.5 到 +0.5**
- 多头（正值）+ 空头（负值）平衡
- 市场中性，纯粹 Alpha 收益
- **推荐用于正式提交**

---

## 📊 五、关键指标解读

### 5.1 从模拟结果中看什么？

| 指标 | 含义 | 多空组合 vs 仅多头 |
|------|------|-------------------|
| **Sharpe** | 风险调整后收益 | 多空通常更高（风险更低） |
| **Returns** | 总收益率 | 仅多头可能更高（但有市场风险） |
| **Drawdown** | 最大回撤 | 多空通常更小（对冲风险） |
| **Turnover** | 换手率 | 两者相近（取决于信号） |
| **Market Beta** | 市场暴露 | 多空 ≈ 0，仅多头 > 0 |

### 5.2 判断标准

✅ **好的 Alpha 特征**：
- 多空组合 Sharpe > 1.0
- 仅多头与多空组合收益差异不大（说明 Alpha 独立于市场）
- Drawdown < 15%
- Turnover < 0.6

⚠️ **警惕信号**：
- 仅多头 Sharpe 高，但多空 Sharpe 低 → 可能只是赌市场方向
- 多空组合 Turnover 极高 → 信号不稳定

---

## 💡 六、实战案例解析

### 案例：rank(-returns) 的完整流程

#### 第 1 天（20-Mar）
```python
# 原始数据
Stock A: returns = -2.0%
Stock B: returns = +1.5%
Stock C: returns = -0.5%

# Step 1: 取反
Stock A: -(-2.0%) = +2.0%  ← 最高
Stock B: -(+1.5%) = -1.5%  ← 最低
Stock C: -(-0.5%) = +0.5%

# Step 2: 排名
Stock A: rank = 1.0  (最高)
Stock C: rank = 0.5
Stock B: rank = 0.0  (最低)

# Step 3: 中心化（减去均值 0.5）
Stock A: 1.0 - 0.5 = +0.5  → 多头
Stock C: 0.5 - 0.5 =  0.0  → 中性
Stock B: 0.0 - 0.5 = -0.5  → 空头

# Step 4: 分配资本（假设 $10M 总资本）
Stock A: +$3.33M (做多)
Stock C: $0      (不交易)
Stock B: -$3.33M (做空)
```
#### 第 2 天（21-Mar）
```python
# 假设次日回报
Stock A: +2%  → 盈利 $3.33M × 2% = +$0.067M
Stock B: -2%  → 空头盈利 $3.33M × 2% = +$0.067M
Stock C:  0%  → 无盈亏

# 总利润
Total PnL = +$0.134M
```
## 🎯 七、核心记忆口诀
>"rank 排好序，中心化归零；
>多空各一半，市场中性行。
>仅多头测试，多空真本领；
>Sharpe 要看清，Beta 要归零。"
## 📌 八、常见问题 FAQ
### Q1: 为什么 rank() 后还要中心化？
A: rank() 输出 [0, 1]，全为正值。中心化（减去均值 0.5）后变为 [-0.5, +0.5]，才能构建多空组合。
### Q2: Neutralization: None 时，为什么还能看到空头？
A: 严格来说，Neutralization: None 时所有头寸 ≥ 0（无空头）。如果看到负值，可能是其他设置（如 Pasteurization）的影响。
### Q3: 多空组合一定比仅多头好吗？
A: 不一定。多空组合 Sharpe 通常更高，但 Returns 可能较低。选择取决于：
 - 风险偏好（多空风险更低）
 - 资本限制（空头需要保证金）
 - 市场环境（牛市仅多头可能更好）
### Q4: 如何查看具体股票的头寸？
A: 模拟完成后，点击 RESULTS 标签页，查看 Positions 或 Holdings 表格。
