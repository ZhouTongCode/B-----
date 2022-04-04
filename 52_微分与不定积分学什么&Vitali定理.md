# 52_微分与不定积分学什么&Vitali定理.md

## 微分与不定积分学什么

回忆黎曼积分: 微分与积分互为逆运算.

1. 对于函数 $f(x)$ , 若 R-可积, 则可定义变上限积分 $F(x)=\int_{a}^{x}f(t)dt$ . 在 $f(x)$ 的连续点处, $F'(x)=f(x)$ . 在前面知道, 对于 R 可积的函数, 不连续点集是零测集, 因此 $F'(x)=f(x)$ 几乎处处成立. 这说明先积分再微分可以还原函数.
2. 对于函数 $f(x)$ , 若 $f(x)$ 在 $[a,b]$ 上可微, $f'(x)$ 在 $[a,b]$ 上 R-可积 , 则 $f(x)-f(a)=\int_{a}^{x} f'(t)dt$ . 这说明先微分再积分可以还原函数. (Newton-Leibnitz 公式)

如何将此性质推广到勒贝格积分中?

要考虑以下几点.

对于勒贝格积分, 定义一般可测函数的

1. 变上限积分 $\int_{a}^{x}f(t)dt=\int_{a}^{x}f^+(t)dt-\int_{a}^{x}f^-(t)dt$ . 由 $f^+(t)$ 和 $f^-(t)$ 非负, 得 $\int_{a}^{x}f^+(t)dt$ 和 $\int_{a}^{x}f^-(t)dt$ 是关于 $x$ 的增函数.

   > 考虑增函数, 不妨考虑单调函数.

2. 单调函数可导吗? 后面将会看到, 根据 Vitali 定理, 可以证明单调函数几乎处处可导.

3. 有界变差函数. 即能写成两单调函数之差的函数.

4. 于是可以先积分再微分. 变上限积分函数是绝对连续函数, 可以先微分再积分. 这样, 就可以推广 Newton-Leibnitz 公式了.

## Vitali定理

**定义** ( Vitali 覆盖) 已知 $E\sub \mathbb{R}^1$ , $\mathcal{V}=\{I\}$ 是长度为正的区间族, 称 $\mathcal{V}$ 是 $E$ 的 Vitali 覆盖, 如果 $\forall x\in E,\forall \varepsilon>0,\exist I_x\in \mathcal{V},s.t. x\in I_x, m(I_x)<\varepsilon$ . 

等价定义: 已知 $E\sub \mathbb{R}^1$ , $\mathcal{V}=\{I\}$ 是长度为正的区间族, 称 $\mathcal{V}$ 是 $E$ 的 Vitali 覆盖, 如果 $\forall x\in E,\exist 一列区间 {I_n}\sub \mathcal{V},s.t. x\in I_n, m(I_n)\to 0(n\to \infty)$ . 

**定理** ( Vitali 覆盖定理) 已知 $E\sub \mathbb{R}^1$ , $m(E)<\infty$ , $\mathcal{V}$ 是 $E$ 的 Vitali 覆盖, 则存在 $\mathcal{V}$ 中的一列区间 $\{I_n\}$ , 使 $I_n$ 互不相交, 且 $m(E-\bigcup_{i=1}^{\infty} I_i)=0$ .

> 周彤: "一列"应改为至多可数

证: 由 $m^*(E-\bigcup_{i=1}^{\infty} I_i)=m^*(E-\bigcup_{i=1}^{\infty} \bar{I_i})$ , 只需对闭区间情况证明.

不妨设 $\mathcal{V}$ 中区间都包含于一个测度有限的开集 $U$ 中. $m^*(E)<\infty$ , 存在开集 $U\supset E$ , $m(U)<\infty$ . 则有新的区间族 $\mathcal{W}=\{I\in\mathcal{V}:I\sub U\}$ .

下面说明 $\mathcal{W}$ 非空, 且为 Vitali 覆盖.

**引理** 对 $x\in E,x\in U$ , 其中 $U$ 是开集, 对 Vitali 覆盖 $\mathcal{V}$ 来说, 一定存在  $I_x\in \mathcal{V}$ , 使 $x\in I_x$ , 且 $I_x\sub U$ .

> 证: 由 $x\in U$ , 且 $U$ 是开集, 于是存在 $\varepsilon>0$ , 使 $(x-\varepsilon,x+\varepsilon)\sub U$ . $\mathcal{V}$ 是 $E$ 的 Vitali 覆盖, 存在 $I_x\in \mathcal{V}$ , 使 $x\in I_x$ , 且 $m(I_x)<\frac{\varepsilon}{4}$ . 则 $I_x\sub (x-\varepsilon,x+\varepsilon)\sub U$ . 证毕.

$\forall x\in E$ ,  $\exist I_x\in \mathcal{V}$ , 使 $I_x\sub (x-\varepsilon,x+\varepsilon)\sub U$ , 于是 $I_x\in \mathcal{W}$ , 于是 $\mathcal{W}$ 非空, 且是覆盖. 下说明其为 Vitali 覆盖.

任取  $\delta>0$ , 能取到 $\tilde{I}_x\in \mathcal{V},x\in \tilde{I}_x,m(\tilde{I})<\min\{\frac{\varepsilon}{4},\delta \}$ , 则 $\tilde{I}_x\in \mathcal{W}$ , 则 $\mathcal{W}$ 是 Vitali 覆盖. 这样, 就转化为只需要考虑子覆盖 $\mathcal{W}$ .

想证: 要构造一列 $\{I_n\}$ , 希望 (1) 互不相交; (2) "尽可能大". 按 $I_1,I_2,I_3,\cdots$ 的顺序一步一步构造.

任取 $I_1\in \mathcal{V}$ , 

若 $E-I_1=\varnothing$ , 则任务完成.

若 $E-I_1\ne \varnothing$ , 则存在 $x\in E-I_1$ , 想找与 $I_1$ 不相交的区间, 由 $I_1^C$ 是开集, 根据引理, 存在 $I_x\in \mathcal{V}$ , 使 $x\in I_x$ , $I_x\sub I_1^C$ , 即 $I_x\cap I_1=\varnothing$ . 于是 $\{I\in \mathcal{V}:I\cap I_1=\varnothing\}\ne \varnothing$ , 希望在其中找测度最大的. 令 $r_1=\sup \{m(I): I\in \mathcal{V},I\cap I_1=\varnothing\}\le m(U)<\infty$ , 可取 $I_2\in \mathcal{V},I_2\cap I_1=\varnothing$ , 使 $m(I_2)>\frac{r_1}{2}$ . 用类似的方法去找 $I_3,I_4,\cdots$ .

假设找到 $I_1,\cdots,I_n\in \mathcal{V}$ , $r_i=\sup \{m(I): I\in \mathcal{V},I与I_1,\cdots,I_i都不相交\},i=1,\cdots,n-1$ , $I_1,\cdots,I_n$ 互不相交, $m(I_i)>\frac{r_{i-1}}{2}$ . 若 $E-\bigcup_{i=1}^{n} I_i=\varnothing$ , 则任务完成. 若 $E-\bigcup_{i=1}^{n} I_i\ne \varnothing$ , 则存在 $x\in E-\bigcup_{i=1}^{n} I_i\sub (\bigcup_{i=1}^{n} I_i)^C$ , 而 $(\bigcup_{i=1}^{n} I_i)^C$ 是开集, 由引理, $\{I\in \mathcal{V}:I\cap I_1=\varnothing,\cdots,I\cap I_n=\varnothing\}\ne \varnothing$ . 令 $r_n=\sup \{m(I): I\in \mathcal{V},I与I_1,\cdots,I_n都不相交\}$ , 可知 $r_n<\infty$ . 取 $I_{n+1}\in \mathcal{V}$ , $I_{n+1}$ 与 $I_1,\cdots,I_n$ 都不相交, $m(I_{n+1})>\frac{r_n}{2}$ .

这样, 就可以得到区间列 $\{I_n\}\sub \mathcal{V}$ , 使 $I_n$ 互不相交,  令 $r_n=\sup \{m(I): I\in \mathcal{V},I与I_1,\cdots,I_n都不相交\}$ , $m(I_{n+1})>\frac{r_n}{2}$ . 下证 $\{I_n\}$ 即为所求, 即证 $m(E-\bigcup_{i=1}^{\infty} I_i)=0$ .

取 $y\in E-\bigcup_{i=1}^{\infty}I_i$ , 则任取 $k\in \mathbb{N}$ , 则 $y\notin \bigcup_{i=1}^{k}I_i$ , 

于是 $y\in (\bigcup_{i=1}^{k}I_i)^C$ , 且 $y\in E$. 由引理, 存在 $I_y\in \mathcal{V}$ , 使 $y\in I_y$ , 且 $I_y\sub (\bigcup_{i=1}^{k}I_i)^C$ . 固定 $k$ , 固定 $I_y\ni y$ , 则 $I_y$ 与 $I_1,\cdots,I_k$ 不交. $I_y$ 是否与所有的 $I_n$ 都不交? 答案是否定的. 下面用反证法说明.

> 反设 $I_y$ 与所有的 $I_n$ 都不交, 由引理, $m(I_y)\le r_n$ .
>
> 由 $\sum_{i=1}^{\infty} m(I_i)=m(\bigcup_{i=1}^{\infty} I_i\le m(U))<\infty$ , 这说明 $m(I_i)\to 0, i\to \infty$ . 这说明 $m(I_y)=0$ , 与 $\mathcal{V}$ 是长度为正的区间族矛盾.

记 $n(y)$ 是这样的数, $I_y\cap I_{n(y)}\neq \varnothing$ , 且 $I_y$ 与 $I_1,\cdots,I_{n(y)-1}$ 不交. 显然 $n(y)>k$ . 

![image-20220306220129022](52_微分与不定积分学什么&Vitali定理.assets/image-20220306220129022.png)

可能 $y\notin I_{n(y)}$ , 但是扩大 $I_{n(y)}$ 几倍可能 $y$ 就进去了. 取 $I_{n(y)}$ 的中点, 记为 $x_{n(y)}$ . 有
$$
|y-x_{n(y)}|
\le m(I_y) + \frac{1}{2}m(I_n(y))
\le r_{n(y)-1} + \frac{1}{2}m(I_n(y))\\
< 2m(I_{n(y)}) + \frac{1}{2}m(I_n(y))
=\frac{5}{2}m(I_n(y))
$$
设 $J_n$ 是以 $I_n$ 的中点为中点, 长度为 $I_n$ 的 5 倍的区间, 则 $|y-x_{n(y)}|<\frac{1}{2}m(J_{n(y)})$ , 于是 $y\in J_{n(y)}$ , $n(y)>k$ , 即 $y\in \bigcup_{i=k+1}^{\infty}J_i$ . 则 $E-\bigcup_{i=1}^{\infty}I_i\sub \bigcup_{i=k+1}^{\infty}J_i$ . 

而 $m(\bigcup_{i=k+1}^{\infty}J_i)\le \sum_{i=k+1}^{\infty}m(J_i)=5\sum_{i=k+1}^{\infty}m(I_i)$ . 前面看到, $\sum_{i=1}^{\infty}m(I_i)<\infty$ , 则 $\sum_{i=k+1}^{\infty}m(I_i)\to 0,k\to \infty$ . 从而 $m^*(E-\bigcup_{i=1}^{\infty}I_i)=0$ . 证毕.

> 写过程, 逆着想的写.

由 $\bigcup_{i=1}^{\infty}I_i\sub U$ , 知 $\sum_{i=1}^{\infty}m(I_i)=m(\bigcup_{i=1}^{\infty}(I_i))\le m(U)<\infty$ . 故

- $m(I_i)\to 0,i\to \infty$ ;
- $\sum_{i=k+1}^{\infty}m(I_i)\to 0, k\to \infty$ .

任取 $y\in E-\bigcup_{i=1}^{\infty}I_i$ , 固定$k\in \mathbb{N}$ , 则 $y\notin \bigcup_{i=1}^{k}I_i$ ,  于是 $y\in (\bigcup_{i=1}^{k}I_i)^C$ , 且 $y\in E$. 由引理, 存在 $I_y\in \mathcal{V}$ , 使 $y\in I_y$ , 且 $I_y\sub (\bigcup_{i=1}^{k}I_i)^C$ , 即 $I_y$ 与 $I_1,\cdots,I_k$ 不交. 

断言存在 $n>k$ , 使 $I_y\cap I_n\neq \varnothing$ . 若不然, $m(I_y)\le r_n$ , 而已证 $r_n\to 0, n\to \infty$ . 故 $m(I_y)=0$ , 矛盾.

取 $n(y)$ 是使 $I_y\cap I_{n(y)}\neq \varnothing$ , 且 $I_y$ 与 $I_1,\cdots,I_{n(y)-1}$ 不交得正整数. 显然 $n(y)>k$ . 令 $x_{n(y)}$ 为 $I_{n(y)}$ 的中点, 则
$$
|y-x_{n(y)}|
\le m(I_y) + \frac{1}{2}m(I_n(y))
\le r_{n(y)-1} + \frac{1}{2}m(I_n(y))\\
< 2m(I_{n(y)}) + \frac{1}{2}m(I_n(y))
=\frac{5}{2}m(I_n(y))
$$
设 $J_n$ 是以 $I_n$ 的中点为中点, 长度为 $I_n$ 的 5 倍的区间, 则 $y\in J_{n(y)}$ , $n(y)>k$ , 故 $y\in \bigcup_{i=k+1}^{\infty}J_i$ , 故 $E-\bigcup_{i=1}^{\infty}I_i\sub \bigcup_{i=k+1}^{\infty}J_i$ . 于是 $m^*(E-\bigcup_{i=1}^{\infty}I_i)\le m(\bigcup_{i=k+1}^{\infty}J_i)\le \sum_{i=k+1}^{\infty}m(J_i)=5\sum_{i=k+1}^{\infty}m(I_i)$ . 而已证 $\sum_{i=k+1}^{\infty}m(I_i)\to 0,k\to \infty$ , 故 $m^*(E-\bigcup_{i=1}^{\infty}I_i)=0$ . 证毕.

 **推论** 条件与 Vitali 覆盖定理相同. 结论为 $\forall \varepsilon >0$ , 存在 $\mathcal V$ 中有限个互不相交的区间 $I_1,\cdots,I_n$ , 使 $m(E-\bigcup_{i=1}^{n}I_i)<\varepsilon$ .

> 证: 取区间列 $\{I_n\}$ 同定理, 由 $\bigcup_{i=1}^{\infty}\sub U$ , 知 $\sum_{i=1}^{\infty}m(I_i)=m(\bigcup_{i=1}^{\infty}(I_i))\le m(U)<\infty$ , 于是  $\forall \varepsilon >0,\exist n,s.t. \sum_{i=n+1}^{\infty}m(I_i)<\varepsilon$ . 于是
> $$
> m(E-\bigcup_{i=1}^{n}I_i)
> \le m^*(E-\bigcup_{i=1}^{\infty}I_i) + m(\bigcup_{i=n+1}^{\infty}I_i)\\
> =m(\bigcup_{i=n+1}^{\infty}I_i)
> \le \sum_{i=n+1}^{\infty}m(I_i)
> <\varepsilon
> $$
> 证毕.

**总结**

1. Vitali 覆盖
2. Vitali 定理


