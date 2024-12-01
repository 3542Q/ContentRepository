<div style="text-align:center;font-weight:bold;font-size:2em"> 纳什均衡研究笔记（三） </div>

<div style="text-align:center;">2024-11-30</div>

回忆策略型博弈的定义

<img src="https://s2.loli.net/2024/12/01/Q2P65JgfiuCVdEF.png"/>

N={1,2,...,n}是玩家的有限集

S<sub>i</sub>是玩家i的纯策略集。

u<sub>i</sub>是所有S<sub>i</sub>的笛卡尔积到实数的映射，其对应是玩家i在某个策略组合时的效用函数（utility functions）或支付函数（payoff functions）

这里为了方便起见，记S为所有S<sub>i</sub>的笛卡尔积，一个经典的策略组记作(s<sub>1</sub>,...,s<sub>n</sub>)，另外我们记S<sub>-i</sub>为所有除了i以外的S<sub>j</sub>的笛卡尔积，表示除了参与人i以外的所有其他人的策略集，当我们关注特定参与人时，我们就可以用(s<sub>i</sub>,s<sub>-i</sub>)来表示，其中s<sub>i</sub>属于S<sub>i</sub>，s<sub>-i</sub>属于S<sub>-i</sub>。

<img src="https://s2.loli.net/2024/12/01/BmLMt9KZCvG4Ncj.png"/>

给定一个两人博弈，如果对所有的s<sub>1</sub>属于S<sub>1</sub>，s<sub>2</sub>属于S<sub>2</sub>，有S<sub>1</sub>=S<sub>2</sub>且u<sub>1</sub>(s<sub>1</sub>,s<sub>2</sub>)=u<sub>2</sub>(s<sub>1</sub>,s<sub>2</sub>)，那么这个博弈就是对称博弈。

注意：策略集并不一定必须离散，也可能是连续的区间，或者是空间等等。

零和博弈：所有参与者的效用之和为0。

<img src="https://s2.loli.net/2024/12/01/BCXUM6er1JfYOAo.png"/>

注：

<img src="https://s2.loli.net/2024/12/01/PxW6KZCL2og49we.png"/>

<img src="https://s2.loli.net/2024/12/01/s8WixDlOTv2ZRIw.png"/>

(2) 
参与人集合N = {1,2,...,n}

每个参与人可选择的策略为{1,2,...,K}

即s = 2/3 * (s<sub>1</sub>+...+s<sub>n</sub>) / n

参与人i的效用函数为
u(s<sub>1</sub>,...,s<sub>n</sub>) = 

{
    1/|{k| |s<sub>k</sub> - s| <= |s<sub>j</sub> - s|, for all j != k}|, if |s<sub>i</sub> - s| <= |s<sub>j</sub> - s|, for all j != i,
    0, otherwise
}
即如果i选取的数最接近s,那么1将平分给所有最接近的人,此时i的效用即为这些人的平均，否则为0。

(3)
每个人都可以选择路线A，或者路线B，即两个策略。

记选A为1，而选B为0，则A路线的c(x)=(s<sub>1</sub> +... + s<sub>n</sub>) / n。

对于代理人i，其效用如下,这里因为是cost，所以是负值：

u(s<sub>1</sub>,...,s<sub>n</sub>) = 
{
    -(s<sub>1</sub> +... + s<sub>n</sub>) / n, if s<sub>i</sub> = 1,
    -1, if s<sub>i</sub> = 0
}

(4)
完全图：

对于节点i而言，因为其直接连接到所有其他节点，故其策略为N\\{i}，并且最短路径中链接个数均为1。

所以该图的策略组为：(N\\{1},N\\{2},...,N\\{n})

对于任意节点i， 其效用为(n-1)δ - (n-1)c，这里d<sub>i</sub>(g)=n-1, l<sub>ij</sub>(g)=1。

直线图：

设节点1是第一个，节点n是最后一个。

又l<sub>ij</sub>(g) = |i-j|, d<sub>i</sub>(g)=
{
    1, if i = 1, or i = n
    2, otherwise
}

对应的策略组为：({2},{1,3},{2,4},...,{n-1})

(严格来说，S<sub>1</sub>里除了2也可以有其他元素，只需要保证对应的代理的策略组里没有1即可，其他同理，但是这样写起来就很复杂，理解意思就行。)

对应效用代入即可得到。

星形图：

l<sub>ij</sub>(g) = min{|i-j|, |i+j-n|}

d<sub>i</sub>(g) = 2

对应的策略组为：({2,n},{1,3},{2,4},...,{n-1,1})

(同上，S<sub>1</sub>里除了2,n其实也可以有其他元素，只需要保证对应的代理的策略组里没有1即可，其他参与人同理)

效用代入即可得到

---
**封面图片**: [https://s2.loli.net/2024/11/29/q12wTVZQSlWpcgn.png]

**标签**: [纳什均衡, 算法, 博弈论, 学习 , 笔记]

**分类**: [文章]
