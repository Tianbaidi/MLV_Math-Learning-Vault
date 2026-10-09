

## 1.1 $\mathbb{R}^n$ 中的基本概念

> [!question] 例 1.1.1
>
> 设 $E = \left\{(x, y) \mid y = \sin \frac{1}{x}, 0 < x < \frac{2}{\pi}\right\}$, 则 $\overline{E}$ 是连通的而非道路连通的.

这是著名的拓扑学家的正弦曲线，我们再利用拓扑学中介于闭包连通集合连通的定理可以证明 $\displaystyle E$ 也是连通的，解决，其道路连通主要说明其在 $\displaystyle x_{0}\to t_{0}$ 时候震荡。




## 1.2 $\mathbb{R}^n$ 中的基本定理

> [!question] 例 1.2.1
>
> 用闭集套定理证明三角形三条边上的中线交于一点.

个人认为是通过中点与邻中线构造新三角形，然后通过取极限得道 $\displaystyle x$ 以及 $\displaystyle \text{中点们}\to x$ 

> [!question] 例 1.2.2
>
> 若 $f$ 在 $[a,b]$ 上 Riemann (黎曼) 可积, 则 $f$ 的连续点在 $[a,b]$ 上稠密.

recall Daroux的定义，构造不稠密区见，后得出与可积矛盾。Lebesgue 判别也是可以，不连续点为零测，但是非稠密部分不连续且测度大于0 矛盾。


> [!question] 例 1.2.3
>
> 设 $D \subseteq \mathbb{R}^n, D$ 的内部和外部都非空，$P \in D^\circ, Q \in (\mathcal{C}D)^\circ$。证明：连接 $P$ 和 $Q$ 的连续曲线段 $\Gamma$ 与 $D$ 的边界 $\partial D$ 的交非空。

GPT写了我的答案，但是不是obsidian markdown 
```katex
对，你这个思路是对的，而且本质上就是用**连通性**来证。不过有一个地方要稍微改严谨：

不是说“\(D\) 的内部与补集是连通的”，而是说：

> 连续曲线 \(\Gamma\) 本身是连通的，但如果它不碰边界，就会被 \(D^\circ\) 和 \((\mathcal CD)^\circ\) 分成两个非空、互不相交的开部分，于是 \(\Gamma\) 不连通，矛盾。

最关键的公式是

\[ \mathbb R^n\setminus \partial D = D^\circ\cup(\mathcal CD)^\circ. \]

而且这两个集合互不相交：

\[ D^\circ\cap(\mathcal CD)^\circ=\varnothing. \]

现在设连续曲线可以参数化为

\[ \gamma:[0,1]\to\mathbb R^n, \qquad \gamma(0)=P,\quad \gamma(1)=Q, \]

并记

\[ \Gamma=\gamma([0,1]). \]

因为 \([0,1]\) 是连通的，而连续映射保持连通性，所以

\[ \Gamma \]

是连通集。

现在反证，假设

\[ \Gamma\cap\partial D=\varnothing. \]

那么

\[ \Gamma\subseteq\mathbb R^n\setminus\partial D = D^\circ\cup(\mathcal CD)^\circ. \]

于是

\[ \Gamma = (\Gamma\cap D^\circ) \cup \bigl(\Gamma\cap(\mathcal CD)^\circ\bigr). \]

这两个集合：

\[ \Gamma\cap D^\circ,\qquad \Gamma\cap(\mathcal CD)^\circ \]

互不相交，而且都是 \(\Gamma\) 中的相对开集。

同时它们都非空，因为

\[ P\in\Gamma\cap D^\circ, \]

而

\[ Q\in\Gamma\cap(\mathcal CD)^\circ. \]

这样就把连通集 \(\Gamma\) 分成了两个互不相交的非空开集，矛盾。

因此必有

\[ \boxed{\Gamma\cap\partial D\neq\varnothing}. \]

你刚才关于“内部、外部、边界”的图像理解其实很好，可以记成：

\[ \boxed{ \mathbb R^n = D^\circ \;\dot\cup\; \partial D \;\dot\cup\; (\mathcal CD)^\circ } \]

即空间被分成 **内部 + 边界 + 外部** 三块。

所以从内部 \(P\) 到外部 \(Q\)，如果连续曲线不经过中间的 \(\partial D\)，就相当于一个连通的东西同时待在两个彼此分开的区域里，这是不可能的。

不过你说的

> “内部和外部的闭包都是加上 \(\partial D\)”

对于一般的任意集合 \(D\) 来说不一定能直接写成严格等号，所以这道题最好不要靠这个来证明。上面这个

\[ \mathbb R^n\setminus\partial D = D^\circ\cup(\mathcal CD)^\circ \]

才是最稳、最干净的切入点。
```

他写的比我的清晰www

> [!question] 例 1.2.4
>
> 设 $E \subseteq \mathbb{R}^n$ 为非空闭集，则对于 $x \in \mathbb{R}^n$，存在 $x_0 \in E$ 使得 $|x_0 - x| = d(x, E)$。

由于是闭集，我们取到边界即可，当然这里隐含的意思是分类讨论，在E中则取到同一点，在E外则取边界上的点

> [!question] 例 1.2.5
>
> 设函数 $f$ 在 $[a,b]$ 上有定义, 且对任意的 $x \in [a,b]$, 存在 $\delta_x > 0$, 使得 $f$ 在 $[x - \delta_x, x + \delta_x] \cap [a,b]$ 上递增. 证明: $f$ 在 $[a,b]$ 上递增.

由于 $\displaystyle x$ 是任意的，我们取到 $\displaystyle {x_{1}+\delta_{x_{1}}=x_{2}-\delta _{x_{2}}}$ 该店函数值相同，前后都是单调增的，总体就是单调增的。GPT补充说，此处我们可以更弱的利用 $\displaystyle [a,b]$ 间的紧性只要有所叠加即可

> [!question] 例 1.2.6
>
> 若 $F$ 是 $[a,b]$ 上的连续函数, $A$ 为 $[a,b]$ 中的可列集且当 $x \in [a,b] \setminus A$ 时, $F'(x)=0$, 则 $F$ 在 $[a,b]$ 上恒为常数.

探讨了一下思路
```katex
而且这里 **\(A\) 可列** 的作用会非常清楚：把

\[ A=\{x_1,x_2,x_3,\dots\} \]

列出来，然后**一个一个把这些坏点排除掉**。

假设 \(F\) 不是常数。那就存在 \(u<v\) 使得，比如

\[ F(v)>F(u). \]

取一个正数 \(c\)，满足

\[ 0<c<\frac{F(v)-F(u)}{v-u}. \]

于是

\[ F(v)-F(u)>c(v-u). \]

也就是说，区间 \([u,v]\) 上的“平均斜率”大于 \(c>0\)。

现在我们要做一个很巧的操作：不断缩小区间。

先记

\[ I_0=[u,v]. \]

我们想选出

\[ I_0\supset I_1\supset I_2\supset\cdots \]

使得每个 \(I_n=[a_n,b_n]\) 都满足

\[ \frac{F(b_n)-F(a_n)}{b_n-a_n}>c, \]

同时

\[ x_n\notin I_n, \]

并且让区间长度越来越小，比如

\[ |I_n|\le \frac12|I_{n-1}|. \]

为什么能做到？

因为如果一个区间满足

\[ F(q)-F(p)>c(q-p), \]

把它分成两段，那么不可能两段的平均斜率都 \(\le c\)，否则加起来就会得到整个区间平均斜率也 \(\le c\)。

所以至少有一段仍然满足

\[ F(s)-F(r)>c(s-r). \]

如果刚好 \(x_n\) 在里面，就在 \(x_n\) 附近挖掉一个很小的小区间。由于 \(F\) 连续，这个小区间造成的函数值变化可以做得任意小，因此剩下左右两边至少有一边仍保持“平均斜率 \(>c\)”。

于是我们每一步都能：

\[ \boxed{\text{排掉一个 }x_n\text{，同时保留一个平均斜率}>c\text{的小区间。}} \]

由于区间嵌套且长度趋于 \(0\)，存在唯一一点

\[ x_* \in \bigcap_{n=1}^\infty I_n. \]

但每一步都排除了 \(x_n\)，所以

\[ x_*\neq x_n\qquad\forall n. \]

因此

\[ x_*\notin A. \]

这就是可列性真正用到的地方：

\[ A=\{x_1,x_2,\dots\} \]

使得我们可以一轮一轮把所有坏点全部排掉。

于是根据题设，

\[ F'(x_*)=0. \]

可是另一方面，\(a_n,b_n\to x_*\)，而始终有

\[ \frac{F(b_n)-F(a_n)}{b_n-a_n}>c>0. \]

这和 \(F'(x_*)=0\) 矛盾。

因为如果 \(F'(x_*)=0\)，那么当 \(a_n,b_n\) 都越来越靠近 \(x_*\) 时，

\[ \frac{F(b_n)-F(a_n)}{b_n-a_n}\to0. \]

不可能永远大于固定的 \(c>0\)。

所以假设“\(F\) 不是常数”错误，于是

\[ \boxed{F\text{ 在 }[a,b]\text{ 上恒为常数}.} \]

你可以把整个证明的核心压缩成一句：

\[ \boxed{ \text{若 }F\text{ 真有变化，就能不断缩区间并逐个避开可列坏点，} \\ \text{最终找到一个 }x_*\notin A\text{，但在那里函数仍表现出正斜率，矛盾。} } \]

这也解释了为什么把“可列”换成“零测集”就不行——Cantor 函数正是那个经典反例。
```

> [!question] 例 1.2.7
> 设 $p > 1$. 证明数列 $\left\{\sum_{k=1}^n \frac{1}{k^p}\right\}$ 收敛.

我的想法是证明， $\displaystyle \lim_{ k \to \infty } \frac{1}{k^p}=0$  这里自然想到用夹逼近的办法，但是怎样做到呢？这个思路其实并不怎么好，我们显然有能找到调和级数这个反例。

这里采用分块的方法来求，我们令其按 $\displaystyle 1,\ 2\ 3 \ ,4\ 5\ 6\ 7\ ,\cdots,2^m\ 2^m+1 \cdots\ 2^{m+1}-1\ ,\cdots$
来分组，对于每一组，我们都有 $\displaystyle \sum_{k=2m}^{2^{m+1}-1} \frac{1}{k}\leq 2^m \frac{1}{2^{mp}}=\frac{1}{2^{m(p-1)}}$ 这就得到了一个等比数列。对于这个等比数列，由于 $\displaystyle p>1$ 我们可知这个等比数列是油界且单调的，由单调有界可以得到原来的级数收敛

