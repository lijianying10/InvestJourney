# How It Began

## 刚开始的学习

从我小的时候我就看到我爸投资中国A股市场至今亏损, 因此我对二级市场避而远之. 后来也有人因为我的基础设施能力和高可用相关的工程经验邀请我加入量化交易团队, 但是也因此被我婉拒. 虽然以为工作原因大概读到过一本书 https://www.goodreads.com/book/show/34602335 我发现高频交易并不是和独立玩家自己玩. 所以一直以来我几乎都没碰过投资. 

最近我在研究自己的副业时推荐系统给我推荐了 `https://x.com/BitDanceUp` 和 `https://www.youtube.com/@speculation` 尤其从youtube video `https://www.youtube.com/watch?v=UEEqPTInB6w` 中第一次看到专业的量化交易者, 我发现看起来从基本面和数据面上做风险可控的交易并没有想的成本那么搞那么难, 尤其是我的工作经验和技能有很大的相关性.

### My Journey into Learning

Growing up, I watched my dad invest in the Chinese A-share market and consistently incur losses. This experience made me wary of the secondary market, and I steered clear of it. Despite being invited to join a quantitative trading team due to my expertise in infrastructure and high availability engineering, I declined. My perception was that high-frequency trading wasn't something for independent players. Consequently, I never ventured into investing.

However, while exploring side projects, recommendation systems led me to `https://x.com/BitDanceUp` and `https://www.youtube.com/@speculation`. A YouTube video, `https://www.youtube.com/watch?v=UEEqPTInB6w`, introduced me to professional quantitative traders. I realized that making risk-controlled trades based on fundamentals and data isn't as costly or difficult as I thought, especially given the relevance of my work experience and skills.

## 第一本书

我的第一本书是希望能够带我尽快进入交易, 给我一个创建自己模型的方法. 经过多次比较之后我选择了 `Ernest P. Chan - Quantitative trading _ how to build your own algorithmic trading business.-John Wiley & Sons (2021)`. 

从这里我获得了重要的信息: 

1. 一些投资顾问传播了一个误解，认为如果你的目标是实现最大化的长期资本增长，那么最好的策略就是买入并持有。这个观念在数学上已被证明是错误的。实际上，最大化长期增长是通过找到具有最大夏普比率的策略（在下一节中定义），前提是你可以获得足够高的杠杆。因此，即使你的目标是长期增长，比较一个持有期非常短、年回报小，但夏普比率非常高的短期策略与一个持有期长、年回报高但夏普比率较低的长期策略，仍然更倾向于选择短期策略，除非考虑到税务和对你的保证金借款的限制（关于这一令人吃惊的事实将在第6章关于资金和风险管理中进一步讨论）。
2. 市场上也好论文上也好的交易手段都是过期的都需要自己的twist
3. Sharp Ratio / Info Ratio 
4. 回撤如何计算
5. Sensitivity Analysis
6. 凯利公式

虽然上面这些概念因为在听新闻或者朋友聊天的时候有所耳闻, 但这次是第一次整合到一起思考. 

### My First Book on Trading

Diving into the world of trading, I sought a guide to quickly immerse myself and develop my own models. After much deliberation, I chose "Quantitative Trading: How to Build Your Own Algorithmic Trading Business" by Ernest P. Chan (2021).

Key insights from the book include:

1. The myth that long-term capital growth is best achieved through a buy-and-hold strategy is mathematically flawed. Instead, maximizing long-term growth involves strategies with the highest Sharpe ratio, assuming sufficient leverage is available. Surprisingly, even for long-term goals, short-term strategies with high Sharpe ratios are preferable unless tax and margin borrowing constraints are considered.
2. Trading methods found in the market or academic papers are often outdated and require personal adaptation.
3. Understanding the Sharpe Ratio and Information Ratio is crucial.
4. Learning how to calculate drawdowns is essential.
5. Sensitivity Analysis is a key tool.
6. The Kelly Criterion offers valuable insights.

These concepts, though familiar from news or conversations, were integrated into my thinking for the first time through this book.

## 接下来要做的事情

Learning by doing. 这是我的一个重要朋友教给我的原则(Thanks MYW)

1. 搭建用于计算之前学到的所有公式用于计算的基础软件包. 
2. 实现 `https://www.youtube.com/@speculation` 中最近几个提到的策略, 并且按照书中提到的方法自己 Twist 看看能拿到什么结果.
3. 自己对接交易所, 亲自确认API交易延迟, 数据干净程度. 对接模拟盘. 
4. 准备基础设施
   1. 直接基于Go语言开发, 关键性能部分使用zag开发. 
   2. Grafana全套数据可视化准备. CEP (Complex Event Processing) 基本模块准备. 报警系统准备. 
   3. 默认使用K8s, 保持迁移可机动, 高可用, 交易所在那个Location我们就到那个最近的机房部署我们的程序. 
   4. 如果我在回测中的策略 Sharp Ratio 的到1.6的策略开发成功就尝试在这套基础设施中部署策略. 1000USD本金开始灰度测试. 看看我们能得到什么结果. 
5. 接下来我对风险控制相关的书更感兴趣. 

## Next Steps

Learning by doing. This is a principle taught to me by an important friend (Thanks MYW).

1. Set up a foundational software package for calculating all the formulas learned previously.
2. Implement the strategies mentioned in the recent videos on `https://www.youtube.com/@speculation`, and try to twist them as mentioned in the book to see what results can be achieved.
3. Connect to exchanges personally to verify API trading latency and data cleanliness. Integrate with a simulation platform.
4. Prepare the infrastructure:
   1. Develop directly based on the Go language, using zag for key performance parts.
   2. Prepare a full set of data visualization with Grafana. Prepare basic modules for CEP (Complex Event Processing) and an alert system.
   3. Use K8s by default to maintain mobility and high availability. Deploy our programs in the nearest data center to the exchange's location.
   4. If I successfully develop a strategy with a Sharpe Ratio of 1.6 in backtesting, attempt to deploy the strategy on this infrastructure. Start gray testing with a capital of 1000 USD to see what results we can achieve.
5. I am more interested in books related to risk control next.