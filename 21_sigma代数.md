# 21_ $\sigma$ 代数

## 有用的知识

已证: 可测集类 $\mathcal M$ 在至多可数并, 至多可数交, 余集, 差集, 上下极限这些运算下封闭.

可以只关注至多可数并&余集两种运算, 因为其他运算封闭可以由这两种运算封闭推出.

已知: $\varnothing \in \mathcal{M}$ , $\mathbb{R}^n \in \mathcal{M}$ .

想: 给定一个集合 $X$ , 想找 $X$ 中的一些子集, 满足

1. 在至多可数并&余集下封闭
2. $\varnothing$ , $X$ 都在这些子集中.

> 注: 由条件 1 , 因此条件 2 可改为 $X$ 在这些子集中.
>
> 由条件 2 , $\varnothing$ 在这些子集中, 因此条件 1 可改为在可数并&余集下封闭. 
>
> > 这是因为有限并是可数并的特殊情况.
> >
> > 即 $A_1\cup A_2\cup\cdots\cup A_n=A_1\cup A_2\cup\cdots\cup A_n\cup \varnothing \cup \varnothing \cup \cdots$ .

**定义** $\Omega$ 是 $X$ 的某些子集所成的集合类, 满足

1. $X\in \Omega $ ;
2. 可数并下封闭;
3. 取余集下封闭.

则称 $\Omega$ 为 $X$ 上的一个 $\sigma$ 代数.

> **注** 可以推出 $\varnothing \in \Omega$ , $\Omega$ 在有限并, 至多可数交, 差, 上下极限 封闭.

## 无用的知识

为什么叫 $\sigma-$ 代数?

$\sigma$ 对应于德语中的 Summe , 是 "总和" 的意思. 首字母是 S , “并” 是集合 "求和" . 出现在 "可数并".

下一节中会出现 $F_{\sigma}$ , $G_\delta$ 集.

$F$ 对应于法语中的 fermé , 是 "闭" 的意思.

于是 $F_{\sigma}$ 型集: 闭集的可数并.

$G$ 对应于德语中的 Gebiet , 是 "区域" 的意思.

$\delta$ 对应于德语中的 Durchschnitt , 是 "横贯, 相交" 的意思, 表达的是集合的 "相交" .  出现在 "可数交" , 首字母是 D .

于是 $G_\delta$ 型集: 开集的可数交

## 有用的知识

可测集类是 $\mathbb{R}^n$ 上的 $\sigma $ 代数.

问: 可测集类到底是什么?

猜: 

1. 区间 (开, 闭, 半开半闭) 应该可测
2. 开集 = 可数个半开半闭区间的并, 应该可测. 开集做运算得到很多可测集, 这样得到的集合称为 Borel 集. Borel 集放在一起是一个  $\sigma$ 代数 = 包含所有开集的 "最小" 的  $\sigma$ 代数, 称为所有开集生成的 $\sigma$ 代数 .

**定义** $\Sigma$ 是 $X$ 中某些子集所组成的集合类, 称 $X$ 上所有包含 $\Sigma$ 的 $\sigma$ 代数之交, 为 $\Sigma$ 生成的 $\sigma$ 代数.

> **注1** $\Sigma$ 生成的 $\sigma$ 代数为包含 $\Sigma$ 的最小的 $\sigma$ 代数.
>
> **注2** 给定 $\Sigma$ , 确实存在 $\Sigma$ 生成的 $\sigma$ 代数. 因为取 $X$ 的幂集 $\mathcal{P}(X)=2^X$ ( 即 $X$ 所有子集的全体 ) , 则 $2^X$ 是 $X$ 上的一个 $\sigma-$ 代数, 而且 $\Sigma \sub 2^X$ . 因此 $\{\Omega  \supset \Sigma : \Omega 是 X 上的\sigma 代数\}\ne \varnothing$ . 因此 $\varnothing \ne \bigcap_{\Omega \supset \Sigma , \Omega 是 X 上的\sigma 代数} \Omega \supset \Sigma$ .

**定义** $\mathbb{R}^n$ 上所有开集生成的 $\sigma$ 代数称为 Borel $\sigma$ 代数, 其中的集合称为 Borel 集.

**例** Borel集的例子: 区间, 开集, 闭集, $G_\delta$ 型集, $F_{\sigma}$ 型集.

3. Borel 集应该是可测集.

$\mathcal{M}$ 中, 除了 Borel 集, 其他集合长啥样? 和 Borel 集有关系吗?

**总结** 

1. 从 $\mathbb{M}$ 的性质出发, 抽象出了 $\sigma$ 代数的概念. 
2. 想知道 $\mathbb{M}$ 中的集合有哪些? 猜: 开集应该可测, 经过运算得到更多可测集, 将其全体称为 Borel $\sigma$ 代数, 其中的每一个集合称为 Borel 集.
3. 想看 $\mathbb{M}$ 中还有什么集合, 和 Borel 集的关系.


