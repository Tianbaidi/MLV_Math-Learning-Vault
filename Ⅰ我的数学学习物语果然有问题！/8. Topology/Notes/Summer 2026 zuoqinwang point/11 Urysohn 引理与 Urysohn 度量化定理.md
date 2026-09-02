---
tags:
  - Topology
  - Urysohn
  - Metrization
---
> 本章以 Urysohn 引理为起手，向核心的**度量化问题**发起总攻——只需辅以“第二可数”这一条件，我们便能将抽象的正规空间嵌入Hilbert立方体，赋予其真实可测的距离。这下从拓扑回到度量，坦坦荡荡见自己了。

> 相关笔记：[[10 可数性公理与分离性公理]]、[[12 Tietze 扩张定理]]、[[13 仿紧性与单位分解]]、[[点集拓扑地图]]。

## Urysohn 引理

> [!NOTE] Theorem （Urysohn 引理）
拓扑空间 $(X, \mathcal{T})$ 是正规的（满足 $T_4$ 条件）当且仅当对于 $X$ 中任意不相交的闭集 $A, B$，存在连续函数 $f: X \to [0, 1]$ 使得
$$f(A) = \{0\} \quad \text{且} \quad f(B) = \{1\}$$

在度量空间中，这个是白送的，我们显示得构造函数 
$$f(x)= \frac{d(x,A)}{d(x,A)+d(x,B)}$$
当且仅当 $\displaystyle x\in A$ 时为 $\displaystyle 0$ , $\displaystyle x\in B$ 时为 $\displaystyle 1$ 

但是对于正规孔空间，构造连续函数是非平凡的。我们的证明主要切入是函数的水平集——要构造连续函数，为函数指定足够密集且足够好的“等高线” i.e 下水平集——用特定的开集靠指定。

Proof. 设 $\displaystyle A,B$ 是 $\displaystyle X$ 中不交的闭集，且存在连续函数 $\displaystyle f:X\to[0,1]$ 使得 
$$A \subset f^{-1}(0), \quad B \subset f^{-1}(1)$$
则 $f^{-1}\left(\left[0, \frac{1}{3}\right)\right)$ 和 $f^{-1}\left(\left(\frac{2}{3}, 1\right]\right)$ 是 $A$ 和 $B$ 的不相交的开邻域，故 $(X, \mathcal{T})$ 是正规的。

**Step.1** 构造一列“下水平集”.
我们假设 $A$ 是闭集，$U$ 是开集且 $A \subset U$。我们记 $A = A_0, U = U_1$。由于 $X$ 是正规的，我们可以找到开集 $U_{1/2}$ 和闭集 $A_{1/2}$（比如可以取 $A_{1/2} = \overline{U}_{1/2}$），使得
$$A_0 \subset U_{1/2} \subset A_{1/2} \subset U_1.$$
再重复两次上述过程，我们得到
$$A_0 \subset U_{1/4} \subset A_{1/4} \subset U_{1/2} \subset A_{1/2} \subset U_{3/4} \subset A_{3/4} \subset U_1.$$
通过归纳，对于每个二进有理数
$$r \in D := \left\{ \frac{m}{2^n} \ \middle\vert{}\ n, m \in \mathbb{N}, 1 \le m \le 2^n \right\}$$
我们可以构造一个开集 $U_r$ 和一个闭集 $A_r$，使得
- ① $U_r \subset A_r, \quad \forall r \in D.$
    
- ② $A_r \subset U_{r'}, \quad \forall r < r' \in D.$
- 
**Step.2** 从“下水平集”构造连续函数.
现在我们定义
$$f(x) = \inf\{r \mid x \in U_r\} = \inf\{r \mid x \in A_r\},$$
其中第二个等号来自于 ① 和 ②，且我们在这里“定义” $\inf \emptyset = 1$。于是显然有
$$A \subset f^{-1}(0) \quad \text{且} \quad B = U^c \subset f^{-1}(1).$$
下面证明 $f$ 是连续的。因为
$$\{[0, \alpha) \mid \alpha \in D\} \cup \{(\alpha, 1] \mid \alpha \in D\}$$
是 $[0, 1]$ 上标准拓扑的一个子基，故只需证明：对 $\forall \alpha \in D$，$f^{-1}([0, \alpha))$ 和 $f^{-1}((\alpha, 1])$ 都是开集。这两条可由如下事实得到：
$$f^{-1}([0, \alpha)) = \bigcup_{r < \alpha} U_r \quad \text{且} \quad f^{-1}((\alpha, 1]) = \bigcup_{r > \alpha} A_r^c.$$

如果我们考虑正则空间,这一性质并不成立。若成立我们则定义完全正则空间

> [!ABSTRACT] Definition
> 如果对于拓扑空间 $X$ 中的任意闭子集 $A$ 和任意 $x_0 \notin A$，都存在连续函数 $f: X \to [0, 1]$ 使得
$$f(x_0) = 0 \quad \text{且} \quad f(A) = \{1\}$$
> 则称拓扑空间 $X$ 是**完全正则空间**

### $F_\sigma$ 集与 $G_\delta$ 集

我们从 Urysohn 引理得到一个直接的结论
$$A \subset f^{-1}(0), \quad B \subset f^{-1}(1).$$
那么对于正规空间里不相交的闭集 $A$ 和 $B$，是否存在连续函数 $f$ 使得
$$A = f^{-1}(0), \quad B = f^{-1}(1)$$
度量空间这是显然的，但是对于一般的正规空间是否成立?我们又有如下问题拓扑空间里的子集 $A$ 是某个连续函数零点集的必要条件是什么？我们肯定要求 $\displaystyle A$ 是一个闭集且需要 $\displaystyle f^{-1}(0)=\bigcap^{\infty}_{n=1}f^{-1}\left( \left( -\frac{1}{n}, \frac{1}{n}  \right) \right)$. 于是我们定义

> [!ABSTRACT] Definition （$G_\delta$-集与 $F_\sigma$-集）
> 设 $(X, \mathcal{T})$ 是拓扑空间，$A \subset X$：
> 1. 如果 $A$ 可以被表示成可数多个开集的交集，我们称 $A$ 是 $G_\delta$-集；
>      
> 2. 如果 $A$ 可以被表示成可数多个闭集的并集，我们称 $A$ 是一个 $F_\sigma$-集。

> [!Example] EXAMPLE
> 1. 有理数集合 $\mathbb{Q} \subset \mathbb{R}$ 是 $F_\sigma$-集，而无理数集合 $\mathbb{R} \setminus \mathbb{Q} \subset \mathbb{R}$ 是 $G_\delta$-集。
>     
> 2. 度量空间 $(X, d)$ 中的任意闭子集 $F$ 都是 $G_\delta$-集，因为由习题 1.1，$x \in F$ 当且仅当 $d_F(x) = 0$，从而我们有
>     
>     $$F = \bigcap_{n=1}^\infty \left\{ x \ \middle\vert{}\ d_F(x) < \frac{1}{n} \right\}.$$
>     
> 3. 考虑赋有乘积拓扑的空间 $X = \{0, 1\}^{\mathbb{R}}$，则 $X$ 是紧 Hausdorff 空间，从而它是 $T_4$ 空间，且每个单点集 $\{a\}$ 都是闭集。然而，$\{a\}$ 不是 $G_\delta$-集。事实上，$X$ 的每个非空 $G_\delta$-集一定是无穷集：由乘积拓扑定义，$X$ 中的每个开集 $U$ 仅在有限多个位置处取值不是整个 $\{0, 1\}$，这意味着每个 $G_\delta$-集仅在可数多的位置处取值不是整个 $\{0, 1\}$，因此它包含（不可数）无穷多个元素。特别地，我们发现，$\{0, 1\}^{\mathbb{R}}$ 上任意一个有零点的连续函数一定同时在不可数多个点处为零。

实际上

> [!TIP] Proposition （水平集 $\iff$ 闭 $G_\delta$-集）
> 设 $X$ 是正规空间。则存在连续函数 $f: X \to [0, 1]$ 满足 $f^{-1}(0) = A$ 当且仅当 $A$ 是 $X$ 中的闭 $G_\delta$-集。

Proof.正规空间里的闭 $G_\delta$-集都是连续函数的零点集。由于 $A$ 是 $G_\delta$-集，在 $X$ 中存在一族开集 $U_n$ 使得
$$A = \bigcap_{n=1}^\infty U_n.$$
根据 Urysohn 引理，存在连续函数 $g_n : X \to [0, 1]$ 使得
$$A \subset g_n^{-1}(0), \quad U_n^c \subset g_n^{-1}(1).$$
现在我们定义
$$f(x) = \sum_{n=1}^\infty \frac{1}{2^n} g_n(x).$$
则 $f$ 是连续的（因为连续函数列 $\sum_{n=1}^m \frac{1}{2^n} g_n(x)$ 一致收敛到 $f(x)$），且 $f(A) = 0$。此外，对于任意 $x \notin A$，存在 $n$ 使得 $x \in U_n^c$，即 $g_n(x) = 1$，因此 $f(x) \neq 0$。于是
$$f^{-1}(0) = A.$$

### Urysohn 引理的一个变体

就此，我们可以回答此前未解决的问题

> [!NOTE] Theorem（Urysohn 引理的变体）
> 设 $(X, \mathcal{T})$ 为正规空间，$A, B \subset X$。则存在连续函数 $f: X \to [0, 1]$ 使得
$$f^{-1}(0) = A, \quad f^{-1}(1) = B$$
> 当且仅当 $A, B$ 是 $X$ 中不相交的闭 $G_\delta$-集。

Proof.存在函数则显然，反之，设 $A, B$ 是不相交的闭 $G_\delta$-集。存在连续函数 $f_i : X \to [0, 1] \ (i = 1, 2)$ 使得
$$f_1^{-1}(0) = A, \quad f_2^{-1}(0) = B.$$
因为 $A \cap B = \emptyset$，所以在 $X$ 上恒有 $f_1 + f_2 > 0$。于是我们可以定义
$$f(x) = \frac{f_1(x)}{f_1(x) + f_2(x)}, \quad \forall x \in X.$$
显然 $f : X \to [0, 1]$ 是连续的，而且 $f^{-1}(0) = A, \quad f^{-1}(1) = B$。

### Urysohn 引理的 LCH 版本

虽然局部紧的 Hausdoff 空间不一定是正规的，但是其依旧具有很好的分离性质 [[8 映射空间的拓扑#^fca4a7]] 我们可以将不相交的紧集与闭集分开,从而我们考虑用连续函数分离不相交的紧集和闭集。我们可以定义仅仅再紧集上取非零值的函数，我们定义

> [!ABSTRACT] Definition （紧支撑函数）
> 设 $X$ 是拓扑空间，$f \in C(X, \mathbb{R})$ 是连续函数。我们称闭集
$$\operatorname{supp}(f) := \overline{\{x \mid f(x) \neq 0\}}$$
> 为 $f$ 的支撑集。如果 $f$ 的支撑集 $\operatorname{supp}(f)$ 是紧集，则我们称 $f$ 是一个紧支函数。

拓扑空间 $X$ 上所有紧支函数的集合记为 $C_c(X, \mathbb{R})$，它是有界连续函数集合的子集。现在我们可以陈述 LCH 空间的 Urysohn 引理：

> [!NOTE] Theorem （LCH 空间的 Urysohn 引理）
> 设 $X$ 是 LCH 空间，$K, F$ 是 $X$ 中的不相交子集，其中 $K$ 是紧集且 $F$ 是闭集，那么存在一个紧支的连续函数 $f : X \to [0, 1]$ 使得 $f(K) = 1$ 和 $f(F) = 0$。

Proof.存在开集 $V$ 使得 $\overline{V}$ 是紧集，且 $K \subset V \subset \overline{V} \subset F^c$。注意到子空间 $\overline{V}$ 是紧 Hausdorff 空间，从而是正规空间。于是在 $\overline{V}$ 中对 $K \subset V$ 应用 Urysohn 引理，存在连续函数 $f_0 : \overline{V} \to [0, 1]$ 使得
$$f_0(K) = 1, \quad f_0(\overline{V} \setminus V) = 0.$$
令 $f_1 : V^c \to [0, 1]$ 为恒零函数。则 $f_0, f_1$ 分别为定义在闭集 $\overline{V}$ 和 $V^c$ 上的连续函数，且在交集 $\overline{V} \cap V^c = \overline{V} \setminus V$ 上相同。于是由粘结引理，可得到连续函数 $f : X \to [0, 1]$。最后因为 $\operatorname{supp}(f)$ 是紧集 $\overline{V}$ 中的闭集，所以是紧集，即 $f$ 是紧支函数。

>[!Warning] Remark
> >[!Success] Lemma **pasting lemma**
> > 如果 $X = A \cup B$，其中 $A, B$ 都是 $X$ 中的闭集，并且有连续函数 $f_A : A \to Y, f_B : B \to Y$ 满足在交集 $A \cap B$ 上 $f_A = f_B$，那么可以定义一个连续函数 $f : X \to Y$，使得
> > $$f(x) = \begin{cases} f_A(x), & x \in A, \\ f_B(x), & x \in B. \end{cases}$$

任意 LCH 空间都是完全正则空间。

## Urysohn 度量化定理

### 可度量化性质

若拓扑空间的拓扑可以由度量生成，那么这个空间是可度量的

> [!ABSTRACT] Definition （可度量化空间）
> 设 $(X, \mathcal{T})$ 是拓扑空间。如果在 $X$ 上存在度量结构 $d$ 使得度量拓扑 $\mathcal{T}_d$ 与 $\mathcal{T}$ 一致，则我们称 $(X, \mathcal{T})$ 是可度量化的。

> [!example] Example（可度量化与第一可数性）
> 
> $([0, 1]^\mathbb{N}, \mathcal{T}_{\text{product}})$ 是可度量化的；而 $([0, 1]^\mathbb{N}, \mathcal{T}_{\text{box}})$ 与 $(\{0, 1\}^\mathbb{R}, \mathcal{T}_{\text{product}})$ 都**不是**可度量化的，因为它们不是第一可数的。
> 
> 可度量化的拓扑空间必须是第一可数的、Hausdorff 和正规的，但这些条件并不充分。


> [!example] （Sorgenfrey 直线）
> 
> Sorgenfrey 直线 $(\mathbb{R}, \mathcal{T}_{\text{sorgenfrey}})$ 是第一可数的、Hausdorff 的、正规的，但**不是**可度量化的：
> 
> - **第一可数性：** 由例 2.7.1(2)，其在每点处均有可数局部基 $\{[x, x + \frac{1}{n})\}_{n=1}^\infty$。
>     
> - **不可度量化：** 由例 2.7.8，它是可分的但不是第二可数的，从而由命题 2.7.9（可分度量空间必为第二可数）可知其不可度量化。
>     
> - **Hausdorff 性：** 任意 $x < y$，可取开集 $[x, y)$ 和 $[y, y + 1)$ 将其分隔开。
>     
> - **正规性：** 设 $A, B$ 是不相交的闭集。
>       
>     - 对任意 $a \in A$，因 $a \in B^c$ 且 $B^c$ 是开集，可取 $\varepsilon_a > 0$ 使得 $[a, a + \varepsilon_a) \cap B = \emptyset$。
>         
>     - 对任意 $b \in B$，同理可取 $\varepsilon_b > 0$ 使得 $[b, b + \varepsilon_b) \cap A = \emptyset$。
>         
> 对于任意 $a \in A$ 和 $b \in B$，总有 $[a, a + \varepsilon_a) \cap [b, b + \varepsilon_b) = \emptyset$。若不然，假设存在交集元素，则必有 $b \in [a, a + \varepsilon_a)$ 或 $a \in [b, b + \varepsilon_b)$，这与 $\varepsilon_a, \varepsilon_b$ 的选取矛盾。
> 
> 因此，构造开集：
> $$U_A := \bigcup_{a \in A} [a, a + \varepsilon_a) \quad \text{与} \quad U_B := \bigcup_{b \in B} [b, b + \varepsilon_b)$$
> 即为分隔 $A$ 与 $B$ 的不相交开集。


### Urysohn 度量化定理

对于第二可数空间，我们有

> [!NOTE] Theorem （Urysohn 度量化定理）
> 
> 第二可数拓扑空间 $(X, \mathcal{T})$ 是可度量化的当且仅当它是 Hausdorff 且正规的。

> 第二可数不可改为可分离！

由于紧 Hausdoff 空间是正规的，我们有

> [!Danger] Corollary （CH 空间：可度量化 ⇐⇒(A2)）
> 紧 Hausdorff 空间是可度量化的当且仅当它是第二可数的。

证明略

在这个省略的证明中，我们有一个发现

> [!TIP] Proposition （完全正则 +Hausdorff=⇒ 嵌入方体）
> 若 $X$ 是 Hausdorff 且完全正则空间，则 $X$ 可以被拓扑嵌入某个“方体” $[0, 1]^J$ 中。

特别地，任何 LCH 空间可以被拓扑嵌入方体中，任何 (T2) 且 (T4) 空间可以被嵌入
方体中.


