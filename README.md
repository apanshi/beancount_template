## 记账神器 Beancount 学习及模板

**NOTICE: Archived！ 改用这个项目写 [记账神器 Beancount 学习及模板](https://github.com/geekpanshi/panshiji)**

> 这个博客主要是个人 Beancount 学习及模板分享。（Beancount：一个文本记账的复式记账软件）
>
> 记账使用 [Beancount](https://github.com/beancount/beancount)，记账查询和展示使用 [Fava， 一个 beancount 的 WEB 界面](https://beancount.github.io/fava/)。

### 1. 记账方法的分类

#### 1.1 单式记账法

单式记账法，对发生经济业务之后所产生会计要素的增减变动，只在一个账户中进行登记的方法。
> 如用 50 元钱买了豆子，单式记账法，只记录钱的减少 50 元。

单式记账的特点：

1. 记账手续简便；

2. 只反映经济活动的一个侧面，不能全面系统的反应经济活动。

适用范围：个人、家庭、个体商店或手动业者等简单的经济活动场景。

#### 1.2 复式记账法

复式记账法是单式记账法的对称。

复式记账法，对每项经济业务按相等的金额在两个或两个以上有关账户中同时进行登记的方法。复式记账法又分为借贷记账法、收付记账法和增减记账法。
> 如用 50 元钱买了豆子，复式记账法，记录豆子的增加 50 元、钱的减少 50 元。

复式记账的特点：

1. 对经济活动进行相互联系的双重记录，能够反映经济活动的全貌；

2. 能够根据 会计恒等式（资产 = 负债 + 所有者权益）的平衡关系，检查账户记录的正确性；

3. 复式记账的缺点是复杂，每次都需要记录相关的账户变动（**但是 用了 [Beancount](https://github.com/beancount/beancount) 后，这个会变得很简单**）。

适用范围：企业、事业单位等复杂的经济活动场景。**其他场景使用的话，也是可以，会更加具体的反应经济活动，对自己的经济状况做到心中有数。**

#### 1.3 举个例子

假设： 1 月 18 日，打车花费 30 元，使用了 银行卡支付。

- 单式记账，一般包括 日期、收支分类和金额，如下：

```txt
2022-01-18 交通-打车  -30 元
```

- 复式记账，同样包括 日期、收支分类和金额，不过，**复式记账增加了账户变化的情况**，如下：

```txt
2022-01-18
    交通-打车   30 元
    银行卡     -30 元
```

复式记账，会记录每笔交易的资金流动。**各账户变化“有正有负，正负相等”，这便是复式记账的基本原理，称之为“会计恒等式”。**

复式记账这种方式能够保证记账准确无误，也能提供更详细的财务分析。

**注意**：上面描述中账户是“广义的”，也可理解为分类，“银行卡” 和 “交通-打车” 都是账户。下文中出现账户，若无特别说明，均指广义的账户。

#### 1.4 广义的账户

所谓“广义的账户”，就是指不仅仅是我们日常中理解“现金、银行卡、支付宝、微信”等，买菜、打车、吃饭、旅游等消费类型也是一种账户，房子、车子、股票等资产也是一种账户，房贷、信用卡欠款、借款、借出去的钱也都是一种账户，总之在复式记账的概念中，只要发生经济活动（买卖、借贷）涉及的两个类型，都是账户。

当然，我们这里说的“广义的账户”是可以自己根据自己的需要去定义，并不像会计科目中那些科目规定的那么详细和“死板”。

#### 1.5 常见的记账软件

此处只是推荐一些记账的软件，不是本博客的主要内容。

1. [随手记](https://www.sui.com/)
2. [挖财- 我的资产管家，家庭财务综合服务平台](https://www.wacai.com/)
3. [鲨鱼记账](https://www.shayujizhang.com/)
4. [口袋记账](https://www.qeeniao.com/)
5. [圈子账本](https://www.jizhangapp.com/)
6. [有鱼记账](https://jz.yofish.com/homepage.html)
7. [叨叨官网：一款能聊天的记账本](https://www.daodao.cn/index)
8. [松鼠记账](http://www.soonbook.cn/)
9. [钱迹](https://qianjiapp.com/)
10. [TIMI时光记账](Timi时光记账)

#### 1.6 App Store 精选十佳：记帐工具
1. [MoneyWiz 2022 - 个人财务](https://apps.apple.com/cn/app/moneywiz-2022-%E4%B8%AA%E4%BA%BA%E8%B4%A2%E5%8A%A1/id1511185140)
2. [专业记账助手Money Pro：家庭及个人理财一站式解决](https://apps.apple.com/cn/app/%E4%B8%93%E4%B8%9A%E8%AE%B0%E8%B4%A6%E5%8A%A9%E6%89%8Bmoney-pro-%E5%AE%B6%E5%BA%AD%E5%8F%8A%E4%B8%AA%E4%BA%BA%E7%90%86%E8%B4%A2%E4%B8%80%E7%AB%99%E5%BC%8F%E8%A7%A3%E5%86%B3/id918609651)
3. [MOZE 3.0 最美记账](https://apps.apple.com/cn/app/moze-3-0/id1460011387)
4. [Pixiu 记账（貔貅，助您实现财富自由）](https://apps.apple.com/cn/app/pixiu%E8%AE%B0%E8%B4%A6/id1461452315)
5. [随手记–记账财务专业软件](https://apps.apple.com/cn/app/%E9%9A%8F%E6%89%8B%E8%AE%B0-%E8%AE%B0%E8%B4%A6%E8%B4%A2%E5%8A%A1%E4%B8%93%E4%B8%9A%E8%BD%AF%E4%BB%B6/id372353614)
6. [记账城市 Fortune City 用每笔收支，建造你的城市](https://apps.apple.com/cn/app/%E8%AE%B0%E8%B4%A6%E5%9F%8E%E5%B8%82-fortune-city-%E7%94%A8%E6%AF%8F%E7%AC%94%E6%94%B6%E6%94%AF-%E5%BB%BA%E9%80%A0%E4%BD%A0%E7%9A%84%E5%9F%8E%E5%B8%82/id1172713884)
7. [Pennies – 个人资金、预算和财务管理工具](https://apps.apple.com/cn/app/pennies-%E4%B8%AA%E4%BA%BA%E8%B5%84%E9%87%91-%E9%A2%84%E7%AE%97%E5%92%8C%E8%B4%A2%E5%8A%A1%E7%AE%A1%E7%90%86%E5%B7%A5%E5%85%B7/id916741290)
8. [喵喵记账-超可爱的萌宠记账 app](https://apps.apple.com/cn/app/%E5%96%B5%E5%96%B5%E8%AE%B0%E8%B4%A6-%E8%B6%85%E5%8F%AF%E7%88%B1%E7%9A%84%E8%90%8C%E5%AE%A0%E8%AE%B0%E8%B4%A6app/id1483024444)
9. [Spentable 超好用的开支追踪工具](https://apps.apple.com/cn/app/spentable/id500630565)
10. [Percento - 轻松管理你的资产](https://apps.apple.com/cn/app/percento-%E8%BD%BB%E6%9D%BE%E7%AE%A1%E7%90%86%E4%BD%A0%E7%9A%84%E8%B5%84%E4%BA%A7/id1494319934)

### 2. 关于 Beancount 记账的基本概念

#### TO BE Continued……
