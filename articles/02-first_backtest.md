# First backtest

## Objective

Investigate the correlation between `^TNX` and `BTC-USD`. Determine if price changes are caused by capital flows.

## Technology Stack

Since we are conducting a static study and do not need to track high-frequency data, we are using Yahoo Finance's data for simplicity.

Library: `github.com/piquette/finance-go`

Data visualization is a crucial tool for reviewing results. Having our own data visualization allows us to conduct more flexible analysis than relying on TradingView.

Library: `github.com/go-echarts/go-echarts/v2`

## Calculation Process

Starting with a simple approach, the data computation is divided into the following layers:

1. `^TNX` 3-year historical data
2. A 1-month sliding window of historical data with the cosine values of the first half-cycle of a sine function.
3. Local Max index

## Conclusion

This is a very rough result and not highly accurate. However, we have at least set up the infrastructure, layered computation, and data visualization.

[result](images/1.png)

## 目标

寻找 `^TNX` 和 `BTC-USD` 之间的相关性质. 是否因为资金流动导致价格变化. 

## 技术栈

因为我们是在做静态研究并不需要跟踪和高频率的获取最新数据, 所以我们很简单的使用Yahoo Finance的数据即可. 

库: `github.com/piquette/finance-go`

数据可视化是查看结果很重要的工具. 我们拥有自己的数据可视化可以脱离 TreadingView 获得更灵活的分析方法

库: `github.com/go-echarts/go-echarts/v2`


## 计算过程

先从最简单的想法开始, 数据计算分为如下几个层实现:

1. `^TNX` 3年历史数据
2. 1个月的滑动窗口的历史数据与Sin函数前1/2周期的向量Cos值.
3. Local Max index

## 结论

这是一个非常粗糙的结果. 识别并不准确. 
不过还好把基础设施和分层计算, 数据可视化准备好了. 

[result](images/1.png)