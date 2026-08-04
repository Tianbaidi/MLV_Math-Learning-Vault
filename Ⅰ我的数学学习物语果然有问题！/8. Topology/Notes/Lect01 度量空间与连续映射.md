---
tags:
  - Mathematical_Analysis
  - Topology
---
# 度量空间
> 1906 年，莫里斯·弗雷歇（Maurice Fréchet）引入了度量空间（metric space）的概念。

> [!ABSTRACT] Definition 1 (Metric)
> 设 $X$ 是一个集合。如果映射
> $$d:X\times X\to\mathbb{R}$$
> 满足以下条件，那么称 $d$ 是 $X$ 上的一个**度量（metric）**：
>
> - **（正定性，positivity）** $d(x,y)\geq 0$，并且 $d(x,y)=0$ 当且仅当 $x=y$；
> - **（对称性，symmetry）** $d(x,y)=d(y,x)$；
> - **（三角不等式，triangle inequality）** $d(x,z)\leq d(x,y)+d(y,z)$。

注：欧氏空间中很多与距离有关的概念，都可以很自然地推广到一般的度量空间。

> [!ABSTRACT] Definition 2 (Diameter and Boundedness)
> 设 $(X,d)$ 是一个度量空间，$A\subset X$ 是一个非空子集。定义 $A$ 的**直径（diameter）**为
> $$\operatorname{diam}(A):=\sup_{x,y\in A}d(x,y).$$
> 如果 $\operatorname{diam}(A)<+\infty$，就称 $A$ 是**有界集（bounded set）**；否则称其为无界集。
>
> 特别地，如果 $\operatorname{diam}(X)<+\infty$，就称 $(X,d)$ 是一个有界度量空间。

此外，一个度量还会自然地产生开球、闭球和球面等几何概念。

> [!ABSTRACT] Definition 3 (Balls and Spheres)
> 设 $x_0\in X$，$r>0$。分别定义以 $x_0$ 为中心、以 $r$ 为半径的**开球（open ball）**、**闭球（closed ball）**和**球面（sphere）**：
> $$\begin{aligned}
> B(x_0,r)&=\{x\in X\mid d(x,x_0)<r\},\\
> \bar B(x_0,r)&=\{x\in X\mid d(x,x_0)\leq r\},\\
> S(x_0,r)&=\{x\in X\mid d(x,x_0)=r\}.
> \end{aligned}$$

下面再引入之后会用到的开集与闭集。

> [!ABSTRACT] Definition 4 (Open and Closed Sets)
> 设 $(X,d)$ 是一个度量空间，$U\subset X$。如果对每个 $x\in U$，都存在 $\epsilon>0$，使得
> $$B(x,\epsilon)\subset U,$$
> 那么称 $U$ 是一个**开集（open set）**。如果 $F\subset X$ 的补集
> $$F^c=X\setminus F$$
> 是开集，那么称 $F$ 是一个**闭集（closed set）**。
>
> 由定义不难验证：在任意度量空间中，开球都是开集，闭球都是闭集。

> [!Warning] Remark 1 (Open Balls and Closed Balls)
> 这里容易混淆的一点是：开球的闭包不一定等于相应的闭球。例如，在离散度量空间中，
> $$B(x,1)=\{x\},\qquad \overline{B(x,1)}=\{x\},$$
> 而
> $$\bar B(x,1)=X.$$

下面来看一些例子。

1. **（离散度量）** 在任意集合 $X$ 上，都可以定义**离散度量（discrete metric）**
$$d(x,y)=
\begin{cases}
0,&x=y,\\
1,&x\neq y.
\end{cases}$$

> [!Question] Question 1 (Balls in the Discrete Metric)
> 在离散度量空间 $(X,d_{\mathrm{discrete}})$ 中，开球、闭球和球面分别是什么样子？

2. **（$\mathbb{R}^n$ 上的各种度量）**

在 $X=\mathbb{R}$ 上，除了上面的离散度量，还有最熟悉的绝对值度量
$$d(x,y)=|x-y|.$$

> 离散度量几乎看不出集合原本的几何结构，而绝对值度量又不是有界的。因此，我们自然会想到下面这些有界度量。

例如：
$$\bar d(x,y)=\min\{|x-y|,1\},$$
或者
$$\bar d(x,y)=\frac{|x-y|}{1+|x-y|}.$$

更一般地，在 $X=\mathbb{R}^n$ 上有：

- **（标准欧氏度量，standard Euclidean metric）**
  $$d_2(x,y)=\sqrt{(x_1-y_1)^2+\cdots+(x_n-y_n)^2};$$

- **（$\ell^1$ 度量，也叫出租车度量，taxicab metric）**
  $$d_1(x,y)=|x_1-y_1|+\cdots+|x_n-y_n|;$$

![[Pasted image 20260715111346.png]]

- **（$\ell^\infty$ 度量）**
  $$d_\infty(x,y)=\max\{|x_1-y_1|,\ldots,|x_n-y_n|\}.$$

当 $1\leq p<\infty$ 时，$\ell^p$ 度量定义为
$$d_p(x,y):=\left(|x_1-y_1|^p+\cdots+|x_n-y_n|^p\right)^{1/p}.$$

$p=\infty$ 的情形需要单独定义，也就是上面的最大值公式。

> [!Question] Question 2 (Limit of the $\ell^p$ Metrics)
> 怎样证明当 $p\to\infty$ 时，$\ell^p$ 度量会趋向 $\ell^\infty$ 度量？
>
> ![[Pasted image 20260715112052.png]]

3. **（$\mathbb{R}^{\mathbb{N}}$ 上的各种度量）**

考虑无限笛卡尔积
$$X=\mathbb{R}^{\mathbb{N}}
:=\{(x_1,x_2,\ldots,x_n,\ldots)\mid x_n\in\mathbb{R}\}.$$

我们不能直接照搬前面的公式，在整个空间上定义 $\ell^p$ 度量，因为相应的级数可能发散。不过，可以先把 $\mathbb{R}$ 上的度量变成有界度量，以避开收敛问题。

- **（一致度量，uniform metric）**
  $$d\big((x_n)_{n\in\mathbb{N}},(y_n)_{n\in\mathbb{N}}\big)
  :=\sup_{n\in\mathbb{N}}\bar d(x_n,y_n).$$

- **（无限乘积度量，infinite product metric）**
  $$d\big((x_n)_{n\in\mathbb{N}},(y_n)_{n\in\mathbb{N}}\big)
  :=\sum_{n=1}^{\infty}2^{-n}\bar d(x_n,y_n).$$

```python
x = [0, 0, 0, 0, 0]
y = [0, 0, 0, 100, 100]

# 一致度量：取各坐标距离的最大值
uniform = max(min(abs(a - b), 1.0) for a, b in zip(x, y))

# 乘积度量：对各坐标距离作加权求和
product = sum((1 / (2 ** i)) * min(abs(a - b), 1.0) for i, (a, b) in enumerate(zip(x, y), 1))

print(uniform)  # 1.0
print(product)  # 0.09375
```

另一种思路是：把 $\ell^p$ 度量限制在一个合适的子集上，从而保证级数收敛。

- **（$\ell^p$ 空间，$1\leq p<\infty$）** 定义
  $$\ell^p(\mathbb{R})
  :=\left\{(x_n)_{n\in\mathbb{N}}
  \ \middle|\
  \|x\|_p:=\left(\sum_n|x_n|^p\right)^{1/p}<+\infty
  \right\}
  \subset\mathbb{R}^{\mathbb{N}}.$$
  在这个空间上定义
  $$d(x,y)=\|x-y\|_p.$$

- **（希尔伯特立方，Hilbert cube）** 令
  $$X=\prod_n[0,1/n]\subset\mathbb{R}^{\mathbb{N}}.$$
  这个集合包含在 $\ell^2(\mathbb{R})$ 中，因此自然继承 $\ell^2$ 度量。

4. **（函数空间上的度量）**

在闭区间 $[a,b]$ 上的连续函数空间 $C([a,b])$ 中，可以考虑：

- **（$L^1$ 度量）**
  $$d(f,g)=\int_a^b|f(x)-g(x)|\,dx;$$

- **（$L^\infty$ 度量）**
  $$d(f,g)=\sup_{x\in[a,b]}|f(x)-g(x)|;$$

- **（$L^2$ 度量）**
  $$d(f,g)=\left(\int_a^b|f(x)-g(x)|^2\,dx\right)^{1/2}.$$

当 $1\leq p<\infty$ 时，$L^p$ 度量统一写成
$$d(f,g)=\left(\int_a^b|f(x)-g(x)|^p\,dx\right)^{1/p}.$$

$p=\infty$ 时仍然要用前面的上确界公式单独定义。

进一步地，在 $k$ 次连续可微函数组成的空间上，可以定义 **Sobolev $W^{k,p}$ 度量**：
$$d(f,g)
=\left(
\sum_{i=0}^k\int_a^b|f^{(i)}(x)-g^{(i)}(x)|^p\,dx
\right)^{1/p},
\qquad 1\leq p<\infty.$$

如果学过抽象代数，你可能还见过**字度量（word metric）**：给定一个群 $G$ 以及生成集 $S\subset G$，$S$ 会在 $G$ 上诱导出一个字度量。如果你对图度量感兴趣，我们助教的研究方向正好是几何群论。

## 从已有空间构造新空间

> 在建立了度量空间的基本定义，并看过一些经典例子之后，一个很自然的问题是：怎样利用已有的空间构造新的度量空间？这一节讨论两个最基本的构造——子空间度量（subspace metric）与乘积度量（product metric）。

最常见的做法，一种是让子集直接继承原空间的度量；另一种是在笛卡尔积上，用各个分量的度量拼出一个新的度量。

> [!TIP] Proposition 1 (Subspace Metric)
> 设 $(X,d)$ 是一个度量空间，$Y\subset X$。那么
> $$d_Y:=d|_{Y\times Y}$$
> 是 $Y$ 上的一个度量。

Proof. 任取 $y_1,y_2,y_3\in Y$。因为 $Y\subset X$，所以 $d$ 的三个性质会直接继承下来：

- $d_Y(y_1,y_2)=0$ 当且仅当 $y_1=y_2$；

- 
  $$d_Y(y_1,y_2)
  =d(y_1,y_2)
  =d(y_2,y_1)
  =d_Y(y_2,y_1);$$

- 
  $$\begin{aligned}
  d_Y(y_1,y_3)
  &=d(y_1,y_3)\\
  &\leq d(y_1,y_2)+d(y_2,y_3)\\
  &=d_Y(y_1,y_2)+d_Y(y_2,y_3).
  \end{aligned}$$

$\square$

更一般地，给定一个单射 $f:Y\to X$，我们可以把 $Y$ 与子集 $f(Y)\subset X$ 认作同一个集合，并利用 $X$ 上的度量 $d_X$ 在 $Y$ 上定义诱导度量
$$d(y_1,y_2):=d_X(f(y_1),f(y_2)).$$

接下来看看怎样在笛卡尔积上构造一个合理的度量。

> [!TIP] Proposition 2 (Product Metric)
> 如果 $(X_1,d_1)$ 与 $(X_2,d_2)$ 都是度量空间，那么
> $$d\big((x_1,x_2),(y_1,y_2)\big)
> :=d_1(x_1,y_1)+d_2(x_2,y_2)$$
> 是 $X_1\times X_2$ 上的一个度量。

Proof. 任取
$$
(x_1,x_2),\ (y_1,y_2),\ (z_1,z_2)\in X_1\times X_2.
$$

- 首先，
  $$\begin{aligned}
  d\big((x_1,x_2),(y_1,y_2)\big)=0
  &\iff d_1(x_1,y_1)=0\ \text{且}\ d_2(x_2,y_2)=0\\
  &\iff x_1=y_1\ \text{且}\ x_2=y_2.
  \end{aligned}$$

- 其次，
  $$\begin{aligned}
  d\big((x_1,x_2),(y_1,y_2)\big)
  &=d_1(x_1,y_1)+d_2(x_2,y_2)\\
  &=d_1(y_1,x_1)+d_2(y_2,x_2)\\
  &=d\big((y_1,y_2),(x_1,x_2)\big).
  \end{aligned}$$

- 最后，
  $$\begin{aligned}
  d\big((x_1,x_2),(z_1,z_2)\big)
  &=d_1(x_1,z_1)+d_2(x_2,z_2)\\
  &\leq d_1(x_1,y_1)+d_1(y_1,z_1)
  +d_2(x_2,y_2)+d_2(y_2,z_2)\\
  &=d\big((x_1,x_2),(y_1,y_2)\big)
  +d\big((y_1,y_2),(z_1,z_2)\big).
  \end{aligned}$$

$\square$

与子空间度量不同，乘积空间通常可以配上好几种自然的度量。例如，还可以定义
$$d\big((x_1,x_2),(y_1,y_2)\big)
:=\sqrt{d_1(x_1,y_1)^2+d_2(x_2,y_2)^2}.$$

不难验证，它同样是 $X_1\times X_2$ 上的度量。

更一般地，如果 $(X_1,d_1),\ldots,(X_n,d_n)$ 都是度量空间，那么当 $1\leq p<\infty$ 时，可以在
$$X_1\times\cdots\times X_n$$
上定义 **$\ell^p$ 型乘积度量**
$$d_p\big((x_1,\ldots,x_n),(y_1,\ldots,y_n)\big)
:=\left(
d_1(x_1,y_1)^p+\cdots+d_n(x_n,y_n)^p
\right)^{1/p}.$$

当 $p=\infty$ 时，定义
$$d_\infty\big((x_1,\ldots,x_n),(y_1,\ldots,y_n)\big)
:=\max_{1\leq i\leq n}d_i(x_i,y_i).$$

> [!Question] Question 3 (Metric on a Countable Product)
> 对可数多个度量空间的乘积，我们该怎样构造度量？

考虑可数个度量空间 $(X_n,d_n)$ 的笛卡尔积
$$\prod_{n=1}^{\infty}X_n.$$
为了在它上面写出一个明确的度量，可以先把每个 $d_n$ 替换成有界度量
$$\tilde d_n(x,y)=\min\{d_n(x,y),1\}.$$

随后可以定义**一致度量**
$$d_u\big((x_n)_{n\in\mathbb{N}},(y_n)_{n\in\mathbb{N}}\big)
=\sup_{n\in\mathbb{N}}\tilde d_n(x_n,y_n).$$

这里要留意：一致度量诱导的是一致拓扑，它可能严格细于乘积拓扑。一个能够诱导标准乘积拓扑的度量是
$$d\big((x_n),(y_n)\big)
:=\sum_{n=1}^{\infty}2^{-n}\tilde d_n(x_n,y_n).$$

## 等距、嵌入与 Lipschitz 映射

> [!ABSTRACT] Definition 5 (Isometry)
> 设 $(X,d_X)$ 与 $(Y,d_Y)$ 是度量空间。一个双射 $f:X\to Y$ 称为**等距映射（isometry）**，如果对任意 $x_1,x_2\in X$，
> $$d_Y\big(f(x_1),f(x_2)\big)=d_X(x_1,x_2).$$

两个等距的度量空间具有完全相同的度量性质，因此通常可以把它们看作等价的空间。下面给出两种对等距条件的放宽。

> [!ABSTRACT] Definition 6 (Isometric Embedding)
> 一个单射 $f:X\to Y$ 称为**等距嵌入（isometric embedding）**，如果对任意 $x_1,x_2\in X$，
> $$d_Y\big(f(x_1),f(x_2)\big)=d_X(x_1,x_2).$$

如果 $f:(X,d_X)\to(Y,d_Y)$ 是等距嵌入，那么 $f$ 是 $(X,d_X)$ 到子空间
$$\big(f(X),d_Y|_{f(X)\times f(X)}\big)$$
上的等距映射。

> [!ABSTRACT] Definition 7 (Lipschitz Map)
> 映射 $f:X\to Y$ 称为 **Lipschitz 映射（Lipschitz map）**，如果存在常数 $L\geq0$，使得对任意 $x_1,x_2\in X$，
> $$d_Y\big(f(x_1),f(x_2)\big)
> \leq L\,d_X(x_1,x_2).$$
> 此时称 $L$ 为一个 Lipschitz 常数。

> [!Warning] Remark 2 (Lipschitz Maps and Continuity)
> 在区间上——更一般地，在凸区域上——导数有界的可微函数是 Lipschitz 的。此外，
> $$\text{Lipschitz}
> \implies\text{一致连续}
> \implies\text{连续}.$$

> [!Example] Example 1 (Identity Maps between Metrics)
> 令 $X=\mathbb{R}$，并考虑
> $$d(x,y)=|x-y|,
> \qquad
> \bar d(x,y)=\min\{1,|x-y|\}.$$
>
> - 恒等映射
>   $$\operatorname{id}:(\mathbb{R},d)\to(\mathbb{R},d)$$
>   与
>   $$\operatorname{id}:(\mathbb{R},\bar d)\to(\mathbb{R},\bar d)$$
>   都是等距映射；
>
> - 映射
>   $$\operatorname{id}:(\mathbb{R},d)\to(\mathbb{R},\bar d)$$
>   是 Lipschitz 映射，但不是等距映射；
>
> - 映射
>   $$\operatorname{id}:(\mathbb{R},\bar d)\to(\mathbb{R},d)$$
>   不是 Lipschitz 映射。

# 度量空间之间的连续映射

和欧氏空间中一样，我们先定义点列的收敛，再利用收敛来刻画度量空间之间的**连续映射（continuous map）**。

> [!ABSTRACT] Definition 8 (Convergence)
> 设 $(X,d)$ 是一个度量空间，$(x_n)$ 是 $X$ 中的一个点列。如果对任意 $\epsilon>0$，都存在 $N\in\mathbb{N}$，使得当 $n\geq N$ 时，
> $$d(x_n,x_0)<\epsilon,$$
> 那么称点列 $(x_n)$ **收敛（converge）**到 $x_0\in X$，记作
> $$x_n\to x_0.$$

> [!ABSTRACT] Definition 9 (Continuity)
> 设 $(X,d_X)$ 与 $(Y,d_Y)$ 是度量空间，$f:X\to Y$ 是一个映射。
>
> 1. 如果对任意收敛到 $x_0$ 的点列 $(x_n)$，点列 $(f(x_n))$ 都收敛到 $f(x_0)$，那么称 $f$ 在 $x_0\in X$ 处连续；
>
> 2. 如果 $f$ 在 $X$ 的每一点都连续，那么称 $f$ 是一个连续映射。

> [!ABSTRACT] Definition 10 (Equivalent Characterizations of Continuity at a Point)
> 对于映射 $f:X\to Y$ 和点 $x_0\in X$，下列条件等价：
> $$\begin{aligned}
> f\text{ 在 }x_0\text{ 处连续}
> &\iff
> \forall\epsilon>0,\ \exists\delta>0,\ 
> \forall x\in X,\ 
> d_X(x,x_0)<\delta
> \implies
> d_Y(f(x),f(x_0))<\epsilon\\
> &\iff
> \forall\epsilon>0,\ \exists\delta>0,\ 
> f(B_X(x_0,\delta))
> \subset
> B_Y(f(x_0),\epsilon)\\
> &\iff
> \forall\epsilon>0,\ \exists\delta>0,\ 
> B_X(x_0,\delta)
> \subset
> f^{-1}(B_Y(f(x_0),\epsilon)).
> \end{aligned}$$

> [!Example] Example 2 (Basic Continuous Maps)
> 连续映射的概念，是欧氏空间中连续函数的自然推广。下面通过几个简单例子来体会这个定义。

（1）设 $(X,d)$ 是任意度量空间。

- 固定一点 $\bar x\in X$，考虑函数
  $$d_{\bar x}:X\to\mathbb{R},
  \qquad
  x\mapsto d(x,\bar x).$$
  这个函数是连续的。事实上，它还是 $1$-Lipschitz 的。

Proof. 对任意 $x,x_0\in X$，由反三角不等式，
  $$\begin{aligned}
  |d_{\bar x}(x)-d_{\bar x}(x_0)|
  &=|d(x,\bar x)-d(x_0,\bar x)|\\
  &\leq d(x,x_0).
  \end{aligned}$$
  因此 $d_{\bar x}$ 是 $1$-Lipschitz 的，从而连续。$\square$

- 更一般地，对任意非空子集 $A\subset X$，可以定义点到集合的距离函数
  $$d_A:X\to\mathbb{R},
  \qquad
  d_A(x):=\inf\{d(x,y):y\in A\}.$$
  由反三角不等式可以证明，$d_A$ 同样是 $1$-Lipschitz 的，因此连续。

> [!Question] Question 4 (Distance to a Set)
> 设 $A\subset X$ 是一个非空子集，定义
> $$d_A(x):=\inf_{y\in A}d(x,y).$$
> 证明 $d_A:X\to\mathbb{R}$ 是 $1$-Lipschitz 的，因而连续。如果 $A$ 还是闭集，再证明
> $$d_A(x)=0\iff x\in A.$$

> [!Question] Question 5 (Continuity of the Metric)
> 在 $X\times X$ 上定义和度量
> $$d_{X\times X}\big((x_1,x_2),(y_1,y_2)\big)
> :=d(x_1,y_1)+d(x_2,y_2).$$
> 证明度量本身
> $$d:X\times X\to\mathbb{R}$$
> 是连续函数。

（2）在函数空间
$$X=C([a,b])$$
上取 $L^\infty$ 度量
$$d(f,g):=\sup_{x\in[a,b]}|f(x)-g(x)|.$$

积分泛函
$$I:X\to\mathbb{R},
\qquad
I(f):=\int_a^b f(x)\,dx$$
是连续的，因为
$$\begin{aligned}
|I(f)-I(g)|
&=\left|\int_a^b f(x)\,dx-\int_a^b g(x)\,dx\right|\\
&\leq\int_a^b|f(x)-g(x)|\,dx\\
&\leq(b-a)\,d(f,g).
\end{aligned}$$

（3）设 $X$ 是任意集合，$d_X$ 是 $X$ 上的离散度量；另设 $(Y,d_Y)$ 是任意度量空间。

- 任意映射 $f:X\to Y$ 都连续。

Proof. 给定 $\epsilon>0$，只需取 $\delta=1$。如果
  $$d_X(x,x_0)<1,$$
  那么根据离散度量的定义，只可能有 $x=x_0$。因此
  $$d_Y(f(x),f(x_0))=0<\epsilon.$$
  所以 $f$ 连续。$\square$

- 反过来，如果值域 $X$ 带有离散度量，那么映射 $f:Y\to X$ 连续，当且仅当它是**局部常值的（locally constant）**。

  这里“局部常值”是指：对任意 $y_0\in Y$，都存在 $\delta>0$，使得
  $$d_Y(y_0,y)<\delta
  \implies
  f(y)=f(y_0).$$

## 强等价度量与拓扑等价度量

> 乍看起来，一个映射是否连续，似乎取决于定义域和值域上具体选择了什么度量。不过，下面的例子会说明：两个不同的度量可能产生完全相同的连续映射。

> [!Example] Example 3 (The Metrics $d_1$ and $d_\infty$)
> 考虑函数
> $$f:\mathbb{R}^n\to\mathbb{R},$$
> 以及 $\mathbb{R}^n$ 上的两个度量 $d_1$ 与 $d_\infty$。事实是：
> $$f:(\mathbb{R}^n,d_1)\to\mathbb{R}$$
> 连续，当且仅当
> $$f:(\mathbb{R}^n,d_\infty)\to\mathbb{R}$$
> 连续。

Proof. 对任意 $x,y\in\mathbb{R}^n$，
$$d_\infty(x,y)
\leq d_1(x,y)
\leq n\max_i|x_i-y_i|
=n\,d_\infty(x,y).$$

因此，$(\mathbb{R}^n,d_1)$ 与 $(\mathbb{R}^n,d_\infty)$ 之间两个方向的恒等映射都是 Lipschitz 的，从而都是连续的。所以，$f$ 关于 $d_1$ 连续，当且仅当它关于 $d_\infty$ 连续。$\square$

回顾这个例子，我们可以抽象出下面的关系。

> [!ABSTRACT] Definition 11 (Strongly Equivalent Metrics)
> 设 $d_1$ 与 $d_2$ 是集合 $X$ 上的两个度量。如果存在常数 $C_1,C_2>0$，使得对任意 $x,y\in X$，
> $$C_1d_1(x,y)
> \leq d_2(x,y)
> \leq C_2d_1(x,y),$$
> 那么称 $d_1$ 与 $d_2$ **强等价（strongly equivalent）**。

> [!Question] Question 6 (Strongly Equivalent Metrics)
> 证明下列命题。设 $d_X$ 与 $\tilde d_X$ 是 $X$ 上的强等价度量，$d_Y$ 与 $\tilde d_Y$ 是 $Y$ 上的强等价度量。那么
> $$f:(X,d_X)\to(Y,d_Y)$$
> 连续，当且仅当
> $$f:(X,\tilde d_X)\to(Y,\tilde d_Y)$$
> 连续。

> 强等价足以保证两个度量产生相同的连续映射，但它并不是必要条件。下面这个例子会引出一种更弱的等价关系。

> [!Example] Example 4 (The Metrics $d_2$ and $\bar d_2$)
> 考虑 $\mathbb{R}^n$ 上的欧氏度量
> $$d_2(x,y)=\|x-y\|_2,$$
> 以及由它得到的有界度量
> $$\bar d_2(x,y):=\min\{1,d_2(x,y)\}.$$
>
> 显然，
> $$\bar d_2(x,y)\leq d_2(x,y).$$
> 但是 $d_2$ 与 $\bar d_2$ 并不强等价。事实上，如果存在常数 $c>0$，使得对任意 $x,y$ 都有
> $$c\,d_2(x,y)\leq\bar d_2(x,y),$$
> 那么只要选择满足
> $$d_2(x,y)>1/c$$
> 的 $x,y$，就会得到
> $$c\,d_2(x,y)>1=\bar d_2(x,y),$$
> 这与假设矛盾。
>
> 不过，$d_2$ 与 $\bar d_2$ 会诱导相同的拓扑。因此，函数
> $$f:\mathbb{R}^n\to\mathbb{R}$$
> 关于 $d_2$ 连续，当且仅当它关于 $\bar d_2$ 连续。

> [!Question] Question 7 (Topological Equivalence of $d_2$ and $\bar d_2$)
> 证明这个事实。

# 邻域的公理化与拓扑的引入

> 我们其实不必一直盯着度量本身。也可以改用邻域系统来讨论连续性，而这正是走向一般拓扑空间的第一步。

> [!ABSTRACT] Definition 12 (Neighborhoods)
> 设 $x\in X$，$N\subset X$。如果存在开集 $U\subset X$，使得
> $$x\in U\subset N,$$
> 那么称 $N$ 是 $x$ 的一个**邻域（neighborhood）**。
>
> 记 $\mathcal{N}(x)$ 为 $x$ 的全部邻域组成的集合，也就是 $x$ 的**邻域系（neighborhood system）**。由定义很容易验证：
>
> （N1）如果 $N\in\mathcal{N}(x)$，那么 $x\in N$；
>
> （N2）如果 $M\supset N$ 且 $N\in\mathcal{N}(x)$，那么 $M\in\mathcal{N}(x)$；
>
> （N3）如果 $N_1,N_2\in\mathcal{N}(x)$，那么
> $$N_1\cap N_2\in\mathcal{N}(x);$$
>
> （N4）如果 $N\in\mathcal{N}(x)$，那么存在 $M\in\mathcal{N}(x)$，使得 $M\subset N$，并且对每个 $y\in M$，都有
> $$N\in\mathcal{N}(y).$$

映射在一点处的连续性，也可以完全用邻域来刻画。

> [!TIP] Proposition 3 (Neighborhoods and Continuity at a Point)
> 设
> $$f:(X,d_X)\to(Y,d_Y)$$
> 是度量空间之间的映射。那么 $f$ 在 $x\in X$ 处连续，当且仅当 $f(x)$ 的任意邻域的原像都是 $x$ 的邻域。

Proof. 先设 $f$ 在 $x$ 处连续，并令 $M\subset Y$ 是 $f(x)$ 的一个邻域。根据邻域的定义，存在开集 $V\subset Y$，使得
$$f(x)\in V\subset M.$$
因为 $V$ 是开集，所以存在 $\varepsilon>0$，使得
$$B(f(x),\varepsilon)\subset V.$$
再由 $f$ 在 $x$ 处连续，存在 $\delta>0$，使得
$$\begin{aligned}
B(x,\delta)
&\subset f^{-1}(B(f(x),\varepsilon))\\
&\subset f^{-1}(V)\\
&\subset f^{-1}(M).
\end{aligned}$$
因此，$f^{-1}(M)$ 是 $x$ 的一个邻域。

反过来，假设 $f(x)$ 的每个邻域的原像都是 $x$ 的邻域。特别地，对任意 $\varepsilon>0$，
$$f^{-1}(B(f(x),\varepsilon))$$
都是 $x$ 的邻域。因此，它包含某个含有 $x$ 的开集 $U$。因为 $U$ 是开集，所以存在 $\delta>0$，使得
$$B(x,\delta)\subset U.$$
于是
$$B(x,\delta)
\subset
f^{-1}(B(f(x),\varepsilon)).$$
因此，$f$ 在 $x$ 处连续。$\square$

### 利用开集刻画整体连续性

作为上一个命题的推论，可以得到度量空间之间连续映射的下面这个刻画。

> [!NOTE] Theorem 1 (Characterization of Continuous Maps)
> 映射
> $$f:(X,d_X)\to(Y,d_Y)$$
> 连续，当且仅当 $Y$ 中每个开集 $V$ 的原像
> $$f^{-1}(V)$$
> 都是 $X$ 中的开集。

Proof. 假设 $f$ 连续，并令 $V\subset Y$ 是开集。对任意
$$x\in f^{-1}(V),$$
由上一个命题，$f^{-1}(V)$ 是 $x$ 的邻域，因此它包含 $x$ 的某个开邻域。于是 $f^{-1}(V)$ 是 $X$ 中的开集。

反过来，假设 $Y$ 中每个开集的原像都是 $X$ 中的开集。任取 $x\in X$，再任取 $f(x)$ 的开邻域 $V\subset Y$。那么 $f^{-1}(V)$ 是 $x$ 的开邻域。因此 $f$ 在 $x$ 处连续。由于 $x$ 是任意的，所以 $f$ 连续。$\square$

这提示我们：连续性从根本上说，并不依赖度量取出的具体数值，而是依赖这个度量所诱导的开集族。于是有下面的定义。

> [!ABSTRACT] Definition 13 (Topologically Equivalent Metrics)
> 设 $d_1$ 与 $d_2$ 是集合 $X$ 上的两个度量。如果它们诱导出的开集族完全相同，那么称 $d_1$ 与 $d_2$ **拓扑等价（topologically equivalent）**。

> [!Question] Question 8 (Continuity and Uniform Continuity)
> 说明“连续”是一个拓扑概念，也就是说，它只依赖定义域和值域中的开集族；并说明“一致连续”不是拓扑概念。

由此立刻得到下面的推论。

> [!Danger] Corollary 1 (Continuity under Topologically Equivalent Metrics)
> 设 $\tilde d_X$ 与 $d_X$ 是 $X$ 上的拓扑等价度量，$\tilde d_Y$ 与 $d_Y$ 是 $Y$ 上的拓扑等价度量。那么
> $$f:(X,d_X)\to(Y,d_Y)$$
> 连续，当且仅当
> $$f:(X,\tilde d_X)\to(Y,\tilde d_Y)$$
> 连续。

### 邻域的公理化

> 这一节不再从度量出发，而是把邻域和开集直接公理化。这样得到的，就是一般的拓扑空间（topological space）。

受到邻域系 $\mathcal{N}(x)$ 的性质启发，我们列出下面四条公理：

（N1）如果 $N\in\mathcal{N}(x)$，那么 $x\in N$；

（N2）如果 $M\supset N$ 且 $N\in\mathcal{N}(x)$，那么 $M\in\mathcal{N}(x)$；

（N3）如果 $N_1,N_2\in\mathcal{N}(x)$，那么
$$N_1\cap N_2\in\mathcal{N}(x);$$

（N4）如果 $N\in\mathcal{N}(x)$，那么存在 $M\in\mathcal{N}(x)$，使得 $M\subset N$，并且对每个 $y\in M$，都有
$$N\in\mathcal{N}(y).$$

第四条公理把不同点处的邻域联系起来。从某种意义上说，它在拓扑结构中扮演了类似于度量结构中三角不等式的角色。

1912 年，豪斯多夫（Hausdorff）对邻域概念进行了公理化，用它描述一种更一般的空间概念，使 $\mathbb{R}^n$、黎曼曲面、无限维空间和函数空间等都成为特例。这样做有两个好处：一是简化理论，二是避免误用几何直觉。

> [!ABSTRACT] Definition 14 (Neighborhood Structure)
> 设映射
> $$\mathcal{N}:X\to
> \mathcal{P}(\mathcal{P}(X))\setminus\{\emptyset\}$$
> 满足公理（N1）—（N4），那么称 $\mathcal{N}$ 是 $X$ 上的一个**邻域结构（neighborhood structure）**。称 $\mathcal{N}(x)$ 为 $x$ 处的邻域系（或邻域滤子），其中的每个元素都是 $x$ 的一个邻域。
>
> 给定集合 $X$ 上的邻域结构 $\mathcal{N}$，称 $(X,\mathcal{N})$ 是一个由邻域结构定义的拓扑空间。

#### 开集公理

> [!ABSTRACT] Definition 15 (Interior)
> 设 $(X,\mathcal{N})$ 是一个由邻域结构定义的拓扑空间。对任意 $A\subset X$，定义 $A$ 的**内部（interior）**为
> $$\operatorname{Int}(A)
> :=\{x\in A\mid A\in\mathcal{N}(x)\}.
> \qquad (1.2.1)$$

由定义和公理（N1）—（N4），映射
$$\operatorname{Int}:\mathcal{P}(X)\to\mathcal{P}(X),
\qquad
A\mapsto\operatorname{Int}(A)$$
满足：

（I1）$\operatorname{Int}(A)\subset A$；

（I2）
$$\operatorname{Int}(A)\cap\operatorname{Int}(B)
=\operatorname{Int}(A\cap B);$$

（I3）
$$\operatorname{Int}(\operatorname{Int}(A))
=\operatorname{Int}(A);$$

（I4）$\operatorname{Int}(X)=X$。

> [!ABSTRACT] Definition 16 (Interior Structure)
> 设 $X$ 是一个集合。如果映射
> $$\operatorname{Int}:\mathcal{P}(X)\to\mathcal{P}(X)$$
> 满足公理（I1）—（I4），那么称它是 $X$ 上的一个**内部结构（interior structure）**。
>
> 给定 $X$ 上的内部结构 $\operatorname{Int}$，称 $(X,\operatorname{Int})$ 是一个由内部结构定义的拓扑空间。

邻域结构与内部结构这两种表述其实是等价的。一个邻域结构按照上面的方式确定一个内部结构；反过来，一个内部结构也可以通过
$$\mathcal{N}(x)
=\{A\subset X\mid x\in\operatorname{Int}(A)\}$$
确定一个邻域结构。

> [!Question] Question 9 (Neighborhood and Interior Structures)
> 证明：任意邻域结构 $\mathcal{N}$ 都会按照上述方式给出一个内部结构 $\operatorname{Int}$；反过来，任意内部结构也会给出一个邻域结构。进一步证明，这两个构造互为逆过程。

有了内部结构之后，就可以定义开集。

> [!ABSTRACT] Definition 17 (Open Sets)
> 在由邻域结构定义的拓扑空间中，如果
> $$U\in\mathcal{N}(x)
> \qquad\text{对每个 }x\in U,$$
> 那么称 $U$ 是开集。

利用邻域结构与内部结构的等价性，可以立刻得到下面的刻画。

> [!TIP] Proposition 4 (Open Sets and Interior)
> 集合 $U$ 是开集，当且仅当
> $$\operatorname{Int}(U)=U.$$

给定 $(X,\mathcal{N})$，记
$$\mathcal{T}
:=\{U\subset X\mid U\text{ 是开集}\}$$
为其中全部开集组成的集合族。那么：

（O1）$\emptyset\in\mathcal{T}$ 且 $X\in\mathcal{T}$；

（O2）如果 $U_1,U_2\in\mathcal{T}$，那么
$$U_1\cap U_2\in\mathcal{T};$$

（O3）如果
$$\{U_\alpha:\alpha\in\Lambda\}\subset\mathcal{T},$$
那么
$$\bigcup_{\alpha\in\Lambda}U_\alpha\in\mathcal{T}.$$

下一节中，我们将正式给出拓扑的定义。
