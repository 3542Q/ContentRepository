<div style="text-align:center;font-weight:bold;font-size:2em"> 纳什均衡研究笔记（一） </div>

<div style="text-align:center;">2024-11-29</div>

<!-- TOC -->
- [内容简介](#内容简介)
- [下载地址](#下载地址)
- [目录](#目录)
<!-- /TOC -->

# 简介<a name="简介"></a>

博弈论（Game Theory）可以定义为对理性、智能决策者之间相互作用的数学模型的研究。决策者通常被称为玩家（players）或代理（agent）。互动既可以包括冲突，也可以包括合作。博弈论提供了通用数学技术，用于分析两个或多个参与者做出影响彼此福利的决策的情况。博弈论中已经提出并讨论了许多类型的博弈。我们首先介绍一类称为策略型博弈（strategic form games）或常态型博弈（normal form games）的游戏，它们可能是所有类型游戏中最常被研究的。

# 策略型博弈<a name="策略型博弈"></a>
主要重点是strategic form games（策略型博弈）

<img src="https://s2.loli.net/2024/11/29/B7LJkzVYeQroiqZ.png"/>

N={1,2,...,n}是玩家的有限集

S<sub>i</sub>是玩家i的纯策略集。

u<sub>i</sub>是所有S<sub>i</sub>的笛卡尔积到实数的映射，其对应是玩家i在某个策略组合时的效用函数（utility functions）或支付函数（payoff functions）

注意：代理的效用并不仅取决于自己，也取决于其他代理。

如果N和所有的S<sub>i</sub>均为有限集，则称这个博弈是有限（finite）的。

我们可以这样看待战略形式游戏的玩法：每个玩家同时在一张纸上写下选定的策略，并将其交给裁判，然后由裁判计算所有玩家的效用。


# 关键概念<a name="关键概念"></a>

## 效用<a name="效用"></a>

效用（也称为收益）使玩家的偏好能够以某种效用规模的实数来表达。

von Neumann and Morgenster提出了一个expected utility maximization theorem（期望效用最大化定理）

该定理简单来讲就是如下内容：

1.效用函数代表个人对不同结果的偏好。

2.结果是不确定的，因此个人为每个可能的结果分配概率。

3.预期效用是所有可能结果的效用的加权平均值，其中权重是每个结果的概率。

4.代理人的目标是最大化他们的预期效用。

该定理假设理性主体总是选择最大化其预期效用的选项。

## 智力<a name="智力"></a>

这个概念意味着游戏中的每个玩家都知道博弈论学家所知道的关于游戏的一切，并且玩家有足够的能力做出博弈论学家可以做出的关于游戏的任何推论。

每个代理都能充分考虑他人行动并做出最优反应策略（best response strategy）

## 公共知识<a name="公共知识"></a>

Aumann将公共知识（Common Knowledge）定义如下：事实是参与者之间的公共知识，如果每个参与者都知道它，每个参与者都知道每个参与者都知道它，等等。也就是说，“每个玩家都知道每个玩家都知道……每个玩家都知道”这种形式的每个陈述都为真。

如果碰巧某个事实为所有参与者所知，而不要求所有参与者都知道所有参与者都知道该事实，等等，那么这样的事实称为相互知识（mutual knowledge.）。

参与者的私人信息（private infomation）是指他个人拥有的信息

完全信息策略型博弈中：集合N，所有的策略S<sub>i</sub>和效用u<sub>i</sub>都是公共知识。

## 有限理性<a name="有限理性"></a>

bounded rationality（有限理性）：

博弈论最常见的形式是假设所有参与者都是对称的。也就是说，它们具有相同的感知和计算能力。它不会模拟能力或对情况的看法的不对称。

# 分类<a name="分类"></a>

## 非合作博弈与合作博弈<a name="非合作博弈与合作博弈"></a>

Non-cooperative Games（非合作博弈）：个人行动为基元，即每个代理单独行动做出决策。

Cooperative Games（合作博弈）：团队联合行动为基元，即参与者之间可以联合行动，即作为一个团体来做出决策，换言之，如果参与者之间的协议（如承诺，或威胁）可执行，则为合作博弈。

注意：判断Non-cooperative Games和Cooperative Games并不在于之间是否有合作或冲突，仅在于判断博弈基元是什么。

## 静态博弈与动态博弈<a name="静态博弈与动态博弈"></a>

static Games（静态博弈）：所有人同时行动，并且在博弈过程中无法获得任何信息。

dynamic Games（动态博弈）：也称multi-stage games（多阶段博弈），参与人的行动可以有先后，或者在博弈时获得之前博弈结果的信息。

## 不同形式<a name="不同形式"></a>

我们在本章中介绍的策略型博弈（strategic form game）（也称为同时移动博弈或标准博弈，simultaneous move game or normal from game）是一种模型或情况，其中每个玩家一劳永逸地选择行动计划，并且所有玩家都同时执行他们的决定。

展开型博弈（extensive form game）指定了可能的事件顺序，并且每个玩家在必须做出决定时都可以考虑他的行动计划。（其视为动态博弈）

联盟型博弈（coalitional form game）或特征型博弈（characteristic form game ）是通过将值与每个玩家子集相关联来表示玩家的每个玩家子集的博弈。这种形式适合合作博弈。

## 完美信息博弈和不完美信息博弈<a name="完美信息博弈和不完美信息博弈"></a>

当玩家完全了解整个过去的历史时（每个玩家在采取行动之前，知道所有其他玩家的过去的行动以及他自己过去的行动），则该游戏被称为完美信息。否则，该博弈就被认为是不完美的。

## 完全信息和不完全信息<a name="完全信息和不完全信息"></a>

信息不完全的博弈是指，在玩家可以开始计划其行动的第一个时间点，一些玩家拥有其他玩家不知道的有关游戏的私人信息。在完全信息的游戏中，博弈的各个方面都是公共知识。

## 其他分类<a name="其他分类"></a>

博弈还有很多其他类别，例如动态博弈、重复博弈、随机博弈、交流博弈、多层博弈（Stackelberg博弈）、微分博弈等。

---
**封面图片**: [https://s2.loli.net/2024/11/29/q12wTVZQSlWpcgn.png]

**标签**: [纳什均衡, 算法, 博弈论, 学习 , 笔记]

**分类**: [文章]