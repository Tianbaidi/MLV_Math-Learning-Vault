---
tags:
  - Topology
  - Tietze
  - Urysohn
---
> 在分析中，我们将给定函数或者映射从较小区域扩张到较大区域是一个非常有用的技巧，在拓扑中是否也是如此？我们学了 Urysohn 引理构造了特殊的函数，但是我们可以通过这些函数延拓出更加有趣的东西。

> 相关笔记：[[11 Urysohn 引理与 Urysohn 度量化定理]]、[[13 仿紧性与单位分解]]、[[10 可数性公理与分离性公理]]。

## Tietze 扩张定理

### 扩张

我们定义扩张

> [!ABSTRACT] Definition （扩张）
> 设 $A \subset X$ 是一个子集，$f : A \to Y$ 是定义在 $A$ 上的一个映射。如果定义在全空间 $X$ 上的映射 $\tilde{f} : X \to Y$ 满足
> $$\tilde{f}(x) = f(x), \quad \forall x \in A,$$
> 则我们称映射 $\tilde{f}$ 是映射 $f$ 的一个**扩张**

对我们来说，最重要的性质是连续性，对于扩张我们要回答两个问题: 

- 给定子空间上的连续映射 $f : A \to Y$，是否存在连续扩张 $\tilde{f} : X \to Y$？
- 如果有，那么是否唯一？

显然，对于唯一，应该是要加入一些特定的条件，这里如果 $\displaystyle A$ 稠密，我们有 

> [!Success] Lemma （稠密子集扩张具有唯一性）
> 设 $Y$ 是 Hausdorff 空间，$A$ 是 $X$ 的稠密子集，$f : A \to Y$ 是连续映射。则至多存在一个连续扩张 $\tilde{f} : X \to Y$。

Proof. 设 $F, G : X \to Y$ 都是 $f : A \to Y$ 的连续扩张，即
$$\left.F\right\vert{}_A = \left.G\right\vert{}_A = f.$$
考虑集合
$$E = \{x \in X \mid F(x) = G(x)\}.$$
因为 $F, G$ 都在 $A$ 上等于 $f$，所以 $A \subseteq E$。又因为 $A$ 在 $X$ 中稠密，所以
$$\overline{A} = X.$$
因此 $E$ 是 $X$ 的稠密子集。

下面证明 $E$ 是闭集。由于 $Y$ 是 Hausdorff 空间，对角线
$$\Delta = \{(y, y) \mid y \in Y\} \subseteq Y \times Y$$
是闭集。定义连续映射
$$\Phi : X \to Y \times Y, \quad \Phi(x) = (F(x), G(x)).$$
则
$$E = \Phi^{-1}(\Delta).$$
因为 $\Delta$ 闭、$\Phi$ 连续，所以 $E$ 是 $X$ 中的闭集。于是 $E$ 既是闭集又是稠密子集，所以
$$E = \overline{E} \supseteq \overline{A} = X \implies E = X.$$
也就是说，对任意 $x \in X$，都有 $F(x) = G(x)$，因此 $F = G$。故连续扩张至多只有一个。


如果 $\displaystyle A$ 不是闭的，在 $\displaystyle A$ 上的连续函数扩张为定义在 $\displaystyle X$ 上的连续函数是可能失效的

> [!Example] EXAMPLE
> 我们定义 $\displaystyle X=\mathbb{R}$, $\displaystyle A=\mathbb{R}\backslash \{ 0 \}$, $\displaystyle Y=\mathbb{R}$ 且是 Hausdoff 的。容易证明 $\displaystyle \overline{A}=\mathbb{R}$, $\displaystyle A$ 在 $\displaystyle X$ 中稠密，且 $\displaystyle A$ 不是闭集。我们定义 $\displaystyle A$ 上的连续函数
> $$f:A\to \mathbb{R},\qquad f(x)=\frac{1}{x}.$$
> 假设存在连续扩张 $\tilde{f} : \mathbb{R} \to \mathbb{R}$，使得 $\left.\tilde{f}\right\vert{}_A = f$。
> 由于 $\tilde{f}$ 在 $0$ 处连续，那么 $\tilde{f}(0)$ 必须是一个实数，并且当 $x \to 0$ 时，$\tilde{f}(x)$ 的极限必须等于 $\tilde{f}(0)$。特别地，沿 $A$ 中的点趋于 $0$ 时，必须有
> $$\lim_{x \to 0} \tilde{f}(x) = \tilde{f}(0).$$
> 但因为在 $A$ 上 $\tilde{f}(x) = 1/x$，所以我们需要
> $$\lim_{x \to 0} \frac{1}{x}$$
> 存在且为有限实数。
> 然而显然：
> 
> - 当 $x \to 0^+$ 时，$1/x \to +\infty$；
>     
> - 当 $x \to 0^-$ 时，$1/x \to -\infty$。
>
>
> 左右极限不相等，且都不是有限实数。因此 $\lim_{x \to 0} \frac{1}{x}$ 在 $\mathbb{R}$ 中不存在，不可能存在实数 $\tilde{f}(0)$ 使其连续。

### Tietze 扩张定理

若 $\displaystyle X$ 是正规的且 $\displaystyle A$ 是 $\displaystyle X$ 中的闭集，则 $\displaystyle A$ 上任何连续函数 $\displaystyle f$ 都可以连续扩张为 $\displaystyle X$ 上的连续函数，且若 $\displaystyle f$ 是有界的，则扩张之后的函数可以具有相同的界，这就是我们的 Tietze 扩张定理

> [!NOTE] Theorem （Tietze 扩张定理）
> 拓扑空间 $(X, \mathcal{T})$ 是正规空间当且仅当对于任意闭集 $A \subset X$，$A$ 上的任意连续函数 $f : A \to [-1, 1]$ 都可以被扩张为 $X$ 上的连续函数 $\tilde{f} : X \to [-1, 1]$。

Tietze 扩张定理可以看作是 Urysohn 引理的推广。这可以直接适用与很多情况。我们 **构造扩张** 的想法如下：
我们考虑“限制映射”
$$r_A : C(X, [-1, 1]) \to C(A, [-1, 1]), \quad g \mapsto \left.g\right\vert{}_A.$$
我们只要证明 $r_A$ 是满射即可，换言之，我们需要求解方程
$$r_A(g) = f.$$
为此，我们应用分析中的标准技巧：
1. **第一步：** 首先找该方程的一个近似解；
	直接对 $f$ 操作是不方便的。为此，我们把 $f$ 做一个“截断”，即 $\bar{f} : A \to [-1/3, 1/3]$，
$$\bar{f}(x) := \begin{cases} 1/3, & \text{若 } f(x) \geqslant 1/3, \\ f(x), & \text{若 } \vert{}f(x)\vert{} \leqslant 1/3, \\ -1/3, & \text{若 } f(x) \leqslant -1/3. \end{cases}$$
	由定义，它是函数 $f$ 的一个“近似”：
$$\vert{}f(x) - \bar{f}(x)\vert{} \leqslant 2/3, \quad \forall x \in A.$$
	接下来我们用 Urysohn 引理构造连续函数 $g : X \to [-1/3, 1/3]$，使得 $r_A(g) \approx \bar{f}$。根据构造，$\bar{f}$ 在一个闭子集上达到最大值 $1/3$，在另一个闭子集上达到最小值 $-1/3$。对这两个闭集用 Urysohn 引理即可得到我们想要的函数。
	
2. 然后迭代地寻找一列越来越好的近似解；
	
3. 最后证明这一列近似解收敛到真正的解.

Proof. 设 $A, B$ 是在 $X$ 中不相交的闭集。那么 $A \cup B$ 在 $X$ 中是闭集，并且
$$f : A \cup B \to [-1, 1], \quad f(x) = \begin{cases} -1, & x \in A, \\ 1, & x \in B \end{cases}$$
是 $A \cup B$ 上的连续函数。根据假设，$f$ 可以扩张为连续函数 $\tilde{f} : X \to [-1, 1]$，且在 $A \cup B$ 上 $\tilde{f} = f$。于是 $\tilde{f}^{-1}((-\infty, 0))$ 和 $\tilde{f}^{-1}((0, +\infty))$ 是 $A$ 和 $B$ 的不相交的开邻域，从而 $X$ 是正规的。

反过来，我们运用我们的思路：

1. 构造一个近似解：
	我们取
$$A_1 := \{x \in A \mid f(x) \geqslant 1/3\} \quad \text{和} \quad B_1 := \{x \in A \mid f(x) \leqslant -1/3\},$$
	则 $A_1$ 和 $B_1$ 是 $X$ 中不相交的闭集。由 Urysohn 引理，存在连续函数 $g : X \to [-1/3, 1/3]$ 使得
$$g(A_1) = \{1/3\} \quad \text{且} \quad g(B_1) = \{-1/3\}.$$
	不难验证，$g(x)$ 还满足
$$\vert{}f(x) - r_A(g)(x)\vert{} \leqslant 2/3, \quad \forall x \in A.$$
	
2. 我们再进行迭代
	记 $f = f_1$。由步骤 1，我们得到了一个连续函数 $g_1 : X \to [-1/3, 1/3]$，使得
$$\vert{}f_1(x) - r_A(g_1)(x)\vert{} \leqslant 2/3, \quad \forall x \in A.$$
	将 $f_1$ 替换为 $f_2 = f_1 - r_A(g_1)$ 并重复步骤 1，我们可以得到连续函数 $g_2 : X \to \left[-\frac{1}{3} \cdot \frac{2}{3}, \frac{1}{3} \cdot \frac{2}{3}\right]$，使得
$$\vert{}f_2(x) - r_A(g_2)(x)\vert{} \leqslant \left(\frac{2}{3}\right)^2, \quad \forall x \in A.$$
	继续重复这个过程，我们可以找到一列连续函数
$$g_n : X \to \left[-\frac{1}{3}\left(\frac{2}{3}\right)^{n-1}, \frac{1}{3}\left(\frac{2}{3}\right)^{n-1}\right]$$
	使得：如果我们记 $f_n = f_{n-1} - r_A(g_{n-1})$，则
$$\vert{}f_n(x) - r_A(g_n)(x)\vert{} \leqslant \left(\frac{2}{3}\right)^n, \quad \forall x \in A.$$
	
3. 收敛到解
	定义函数
$$\tilde{f}(x) := \sum_{n=1}^{\infty} g_n(x).$$
	因为每个 $g_n$ 在 $X$ 上都是连续的，并且
$$\vert{}g_n(x)\vert{} \leqslant \frac{1}{3}\left(\frac{2}{3}\right)^{n-1},$$
	所以该级数一致收敛，从而 $\tilde{f}$ 在 $X$ 上是连续的，并且
$$\vert{}\tilde{f}(x)\vert{} \leqslant \sum_{n=1}^{\infty} \frac{1}{3}\left(\frac{2}{3}\right)^{n-1} = 1, \quad \forall x \in X.$$
	最后，对于 $\forall x \in A$ 以及 $\forall N \in \mathbb{N}$，我们有

$$\left\vert{} f(x) - \sum_{n=1}^{N} g_n(x) \right\vert{} = \left\vert{} f_2(x) - \sum_{n=2}^{N} g_n(x) \right\vert{} = \vert{}f_N(x) - g_N(x)\vert{} \leqslant \left(\frac{2}{3}\right)^N.$$
	所以对于 $x \in A$，有 $f(x) = \tilde{f}(x)$。

### 扩张无界连续函数

我们能把 $\displaystyle [-1,1]$ 替换为任意闭区间的 $\displaystyle [a,b]$ 是否可以将其扩到 $\displaystyle \mathbb{R}$ 上？

> [!NOTE] Theorem （无界连续函数的 Tietze 扩张定理）
> 设 $X$ 是正规空间，且 $A \subset X$ 是闭集，则任意连续函数 $f : A \to \mathbb{R}$ 都可以扩张为连续函数 $\tilde{f} : X \to \mathbb{R}$。

Proof.将 $f$ 与反正切函数 $\arctan : \mathbb{R} \to \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 复合，我们得到一个连续函数
$$f_1 := \arctan \circ f : A \to \left(-\frac{\pi}{2}, \frac{\pi}{2}\right).$$
由 Tietze 扩张定理，$f_1$ 可以被扩张为连续函数
$$\tilde{f}_1 : X \to \left[-\frac{\pi}{2}, \frac{\pi}{2}\right].$$
令
$$B = \tilde{f}_1^{-1}\left(\left\{-\frac{\pi}{2}, \frac{\pi}{2}\right\}\right).$$
则 $B$ 是 $X$ 的闭子集且 $B \cap A = \emptyset$。由 Urysohn 引理，存在连续函数 $g : X \to [0, 1]$ 使得
$$g(A) = \{1\} \quad \text{且} \quad g(B) = \{0\}.$$
定义
$$h(x) = \tilde{f}_1(x) g(x).$$
那么 $h$ 是将 $X$ 映射到开区间 $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ 的连续函数。最后我们令
$$\tilde{f}(x) = \tan h(x).$$
则 $\tilde{f} : X \to \mathbb{R}$ 是连续的，并且对于 $\forall x \in A$，我们有
$$\tilde{f}(x) = \tan h(x) = \tan \tilde{f}_1(x) = \tan f_1(x) = f(x).$$

我们可以类似的进行其他的扩张，就等以后再来探索吧！

### LCH 空间的 Tietze 扩张定理

类似我们 LCH 空间的 Urysohn 引理，一般而言我们无法将所有定义在 $X$ 的闭集上的连续函数作连续扩张，但是我们可以将所有定义在 $X$ 的紧集上的连续函数做连续扩张，而且，我们还能让扩张后的连续函数具有紧支集：

> [!NOTE] Theorem（LCH 空间的 Tietze 扩张定理）
> 设 $X$ 为 LCH 空间，$K$ 为 $X$ 的紧子集。那么任意连续函数 $f : K \to [-1, 1]$ 都可以被扩张为具有紧支集的连续函数 $\tilde{f} : X \to [-1, 1]$。

Proof.取开集 $V$ 使得 $\overline{V}$ 是紧集，且 $K \subset V \subset \overline{V} \subset X$。然后对子空间 $\overline{V}$（它是紧 Hausdorff 空间，从而也是正规空间）应用 Tietze 扩张定理：$K \cup (\overline{V} \setminus V)$ 是 $\overline{V}$ 中的闭集，函数
$$f_1(x) = \begin{cases} f(x), & x \in K, \\ 0, & x \in \overline{V} \setminus V \end{cases}$$
是定义在该闭集上的连续函数，从而可以被扩张为连续函数 $\tilde{f}_1 : \overline{V} \to [-1, 1]$。最后将 $\tilde{f}_1$ 做零扩张得到函数 $\tilde{f} : X \to [-1, 1]$。
由粘结引理，$\tilde{f}$ 是连续函数，而且 $\operatorname{supp}(\tilde{f}) \subset \overline{V}$ 是紧集的闭子集，从而也是紧集。 $\square$


#### 扩张连续映射的注记

> [!Warning] Remark
> 显然我们可以把“向量值”连续函数
> $$f : A \to [0, 1]^n, \quad f : A \to \mathbb{R}^n, \quad \text{或} \quad f : A \to [0, 1]^S$$
> 扩张为 $X$ 上相应的向量值连续函数，即扩张为
> $$\tilde{f} : X \to [0, 1]^n, \quad \tilde{f} : X \to \mathbb{R}^n, \quad \text{或} \quad \tilde{f} : X \to [0, 1]^S,$$
> 其中 $S$ 是任意集合。为此，我们只需分别扩张 $f$ 的每个分量即可。


> [!Warning] Remark
> 另一方面，对于一般的拓扑空间 $Y$，我们不能期望将闭子集 $A$ 上的任意连续函数 $f : A \to Y$ 都扩张为 $X$ 上的连续函数 $\tilde{f} : X \to Y$。例如：
> 赋予 $\{0, 1\}$ 离散拓扑。为了将函数 $f : \{0, 1\} \to Y$ 扩张为连续函数
> $$\tilde{f} : [0, 1] \to Y,$$
> 一个必要条件是：存在一个连续函数 $\gamma : [0, 1] \to Y$ 满足
> $$\gamma(0) = f(0), \quad \gamma(1) = f(1).$$
> 后面代数拓扑的语言，我们需要 $f(0)$ 和 $f(1)$ 位于 $Y$ 的同一个**道路连通分支**中。
> 为了将连续函数 $f : S^1 \to Y$ 扩张为连续函数 $\tilde{f} : D^2 \to Y$（其中 $D^2$ 是平面上的单位圆盘），我们需要像集 $f(S^1)$ 在 $Y$ 中是**可缩的**（这是一种更高级别的连通性）。特别地，我们将会看到恒等映射
> $$f : S^1 \to S^1, \quad x \mapsto x$$
> 不能被扩张为连续映射 $\tilde{f} : D^2 \to S^1$。

## Tietze 扩张定理与 Urysohn 引理的应用

### 连续函数逼近可测函数

在实分析里，Lusin 定理告诉我们：“可测函数在很大一块区域上是连续函数”。结合 LCH 版本的 Tietze 扩张定理，就能得到“用紧支连续函数几乎处处逼近可测函数”。

> [!NOTE] Theorem （Lusin 定理）
> 设 $X$ 是 LCH 空间，$\mu$ 是 $X$ 上的一个正则 Radon 测度，$f : X \to \mathbb{R}$ 是 $X$ 上的可测函数，且存在具有有限测度的 Borel 集 $E$ 使得 $f$ 在 $E^c$ 上为 $0$。则对于任意 $\varepsilon > 0$，存在紧集 $K \subset E$ 使得 $\mu(E \setminus K) < \varepsilon$，且 $f$ 在 $K$ 上连续。

> [!Note] 正则 Radon 测度
> 即 $\mu$ 是一个定义在全体 Borel 集上的测度，满足：对紧集 $K$，$\mu(K) < +\infty$；**外正则性** $\mu(A) = \inf\{\mu(U) \mid A \subset U, \ U \text{ 是开集}\}$；**内正则性** $\mu(A) = \sup\{\mu(K) \mid K \subset A, \ K \text{ 是紧集}\}$。

应用 LCH 版本的 Tietze 扩张定理，我们可以得到

> [!NOTE] Theorem （连续函数几乎处处逼近可测函数）
> 在 Lusin 定理的假设下，存在一列紧支连续函数几乎处处收敛于 $f$。

Proof. 根据 Lusin 定理，存在满足 $\mu(E \setminus K) < \varepsilon$ 的紧集 $K \subset E$，使得 $f$ 在 $K$ 上连续。由 LCH 空间的 Tietze 扩张定理（定理 2.9.6），存在 $g \in C_c(X, \mathbb{R})$ 使得 $\left.g\right|_K = f$。另一方面，由外正则性，存在开集 $U \supset E$ 使得 $\mu(U \setminus E) < \varepsilon$。

对于紧集 $K$ 跟闭集 $U^c$ 应用 LCH 空间的 Urysohn 引理，可得连续函数 $h \in C_c(X, \mathbb{R})$ 使得
$$h(K) = 1, \qquad h(U^c) = 0.$$
于是，对任意 $\varepsilon > 0$，我们得到紧支连续函数 $gh \in C_c(X, \mathbb{R})$ 使得
$$\mu\left(\{x \mid g(x)h(x) \neq f(x)\}\right) < 2\varepsilon.$$
最后分别取 $\varepsilon = \frac{1}{n}$，我们得到一列紧支函数 $g_n$ 依测度收敛于 $f$。再由 Riesz 定理，$g_n$ 有子列几乎处处收敛于 $f$。$\square$


### 度量空间中的伪紧性

我们定义

> [!ABSTRACT] Definition（伪紧）
> 若拓扑空间 $X$ 上的所有连续函数 $f : X \to \mathbb{R}$ 都是有界的，则称 $X$ 是**伪紧的**

> [!Example] EXAMPLE
> 考虑 $X = \mathbb{R} \cup \{\infty\}$，赋以拓扑
> $$\mathcal{T} = \{U \subseteq X \mid \infty \in U \text{ 或 } U = \emptyset\}.$$
> 则 $X$ 上不存在不相交的非空开集（因为任何非空开集都包含点 $\infty$），于是 $X$ 上的任意连续函数 $f : X \to \mathbb{R}$ 必须是常数，从而 $X$ 是**伪紧空间**。
> 
> 但显然 $X$ **不是紧空间**，因为开集族
> $$\{\{x, \infty\}\}_{x \in \mathbb{R}}$$
> 构成 $X$ 的一个开覆盖，且该开覆盖不存在任何有限子覆盖。

在度量空间中，我们是紧的当且仅当他是伪紧的。如果度量空间是伪紧的但是不是紧的，则 $\displaystyle (X,d)$ 不是极限点紧的。我们有无限子集 $\displaystyle A=\{ x_{1},x_{2},\cdots \}$ ,使得 $\displaystyle A'=\varnothing$. 又由于 $\displaystyle A$ 闭，每个 $\displaystyle x_{n}$ 在 $\displaystyle A$ 中都是孤立的，于是 
$$f:A\to \mathbb{R},\qquad f(x_{n})=n$$
是闭集 $\displaystyle A$ 上的连续函数。由 Tietze 扩张定理，$\displaystyle f$ 可以被扩张为连续函数 $\tilde{f} : X \to \mathbb{R}$。于是 $\tilde{f}$ 是 $X$ 上的无界连续函数，产生矛盾。

我们其实得到了更强的结论：（T4）+ 极限点紧 $\displaystyle \implies$ 伪紧

### Cantor 集的应用

我们的第三个应用涉及到 Cantor 集
$$C = [0, 1] \setminus \bigcup_{n=1}^{\infty} \bigcup_{k=0}^{3^{n-1}-1} \left( \frac{3k+1}{3^n}, \frac{3k+2}{3^n} \right).$$
在第 2.2 节的习题中，我们证明了映射
$$g : \{0, 1\}^{\mathbb{N}} \to C \subset [0, 1], \quad a = (a_1, a_2, \cdots) \mapsto \sum_{k=1}^{\infty} \frac{2}{3^k} a_k$$
是从 $(\{0,1\}^{\mathbb{N}}, \mathcal{T}_{\text{product}})$ 到 Cantor 集 $C$ 的同胚，并证明了映射
$$h : \{0, 1\}^{\mathbb{N}} \to [0, 1]^2, \quad a \mapsto \left( \sum_{k=1}^{\infty} \frac{a_{2k-1}}{2^k}, \ \sum_{k=1}^{\infty} \frac{a_{2k}}{2^k} \right)$$
是一个连续满射。于是，我们得到一个连续满射 $h \circ g^{-1} : C \to [0, 1]^2$。由于 $C$ 在 $[0, 1]$ 中是闭集，因此由 Tietze 扩张定理，存在一个连续满射
$$f : [0, 1] \to [0, 1]^2.$$
一般而言，我们把从 $[0, 1]$ 到拓扑空间的连续映射叫做**曲线**，于是我们得到了一条填满单位正方形的曲线！这种能填满正方形的曲线最早是 Peano 在 1890 年发现的。

> [!ABSTRACT] Definition （Peano 曲线）
> 我们称任意一个从 $[0, 1]$ 到 $[0, 1]^2$ 的连续满射为一条 **Peano 曲线**（也叫空间填充曲线）。

所以，我们用 Cantor 集构造出的函数 $f$ 是一条 Peano 曲线！存在 Peano 曲线这一事实，使得人们不得不仔细思考下面这个问题：**什么是维数？** 连续映射可以把低维集合映满高维集合，那维数还是拓扑不变量吗？幸运的是，欧氏空间的维数确实是拓扑不变量——这个命题的证明远比我们想象的要复杂，我们将会在后面的章节中给出详细证明。

> [!Warning] Remark
> 1. 我们给出的是 Peano 曲线存在性的**非构造性**证明。文献中也有许多“构造性证明”，可以从简单的曲线出发，迭代地构造一系列曲线，其极限正是 Peano 曲线。
> 2. 空间填充曲线并不只是理论上的怪物，它们在现实生活中也有重要应用。例如，它可被用于将多维数据（如地图数据）存储到计算机中（线性排列）：我们希望相近的地图数据（高维数据）被存储在数据库相近的位置【这就是连续性！】，以便在使用地图时不必同时读取分散在很多不同地方的数据。

用类似的方法，可以构造连续满射 $f : [0, 1] \to [0, 1]^n$，甚至可以构造连续满射 $f : [0, 1] \to [0, 1]^{\mathbb{N}}$。为此，我们只要把 $\mathbb{N}$ 分解成可数个 $\mathbb{N}$ 的无交并，例如
$$\mathbb{N} = \bigcup_{n} \{ 2^n (2k+1) \mid k \in \mathbb{N} \},$$
然后由 1.4 节习题可以得到同胚 $h_\infty : \{0,1\}^{\mathbb{N}} \to (\{0,1\}^{\mathbb{N}})^{\mathbb{N}}$，从而得到一个连续满射
$$f_\infty = (h, h, \cdots) \circ h_\infty \circ g^{-1} : C \to [0, 1]^{\mathbb{N}}.$$

作为应用，我们证明

> [!NOTE] Theorem （Cantor 集的“通有”性）
> 对任意紧度量空间 $(X, d)$，均存在从 Cantor 集 $C$ 到 $X$ 的连续满射。

Proof. 根据定理 2.7.11，$X$ 同胚于 $[0, 1]^{\mathbb{N}}$ 的某个闭子集 $F$。由 $f_\infty$ 的连续性，$f_\infty^{-1}(F)$ 是 $C$ 的闭子集。根据习题 2.2，存在连续映射 $f : C \to F$ 使得 $f|_F$ 是恒等映射。于是 $f_\infty \circ f$ 就是从 Cantor 集 $C$ 到 $X$ 的连续满射。$\square$


### Stone-Cech 紧化.

我们先回忆一下习题 2.1 中引入的概念：

> [!ABSTRACT] Definition （紧化）
> 设 $X$ 是拓扑空间，$Y$ 是紧拓扑空间，且存在拓扑嵌入 $f : X \to Y$ 使得 $\overline{f(X)} = Y$，则我们称紧拓扑空间 $Y$（以及嵌入映射 $f$）是拓扑空间 $X$ 的**紧化**。

注意紧化实际上包含两个数据：空间 $Y$ 以及嵌入映射 $f$。

我们学过如何用单点紧化（又称 Alexandrov 紧化）的方式去紧化任意一个非紧的拓扑空间 $X$。直觉上来说，单点紧化 $X^*$ 是把 $X$ 的所有“非紧的端口”粘接在一个“无穷远点”处。在很多应用中，这种“不分青红皂白全部粘在一起”的紧化方式是不便于使用的。

一般而言，我们希望紧化的空间 $Y$ 是 Hausdorff 的，因为我们知道紧 Hausdorff 空间具有诸多良好的性质。为此，我们假设 $X$ 是 LCH 空间，或者更一般地，假设 $X$ 是 Hausdorff 且完全正则的空间。根据命题 2.8.16，映射
$$\beta : X \to Q = [0, 1]^{C(X,[0,1])}, \quad x \mapsto \operatorname{ev}_x$$
是一个拓扑嵌入。注意到方体 $Q = [0, 1]^{C(X,[0,1])}$，作为紧 Hausdorff 空间 $[0,1]$ 的乘积空间，依然是紧 Hausdorff 空间。特别地，
$$\beta X := \overline{\beta(X)} \subset [0, 1]^{C(X,[0,1])}$$
是一个紧 Hausdorff 空间，且映射 $\beta : X \to \beta X$ 是一个稠密的拓扑嵌入。于是 $\beta X$ 是 $X$ 的一个紧化。这种紧化最早由 M. Stone 和 E. Čech 在 1937 年分别显式给出。

> [!ABSTRACT] Definition （Stone-Čech 紧化）
> 设 $X$ 是 LCH 空间（或者更一般地，是 Hausdorff 且完全正则的空间）。我们称由上式所定义的空间 $\beta X$ 为 $X$ 的 **Stone-Čech 紧化**。

注意如果 $X$ 本身是紧 Hausdorff 的，那么 $\beta X$ 跟 $X$ 是同胚的。

给定任意连续函数 $f : X \to [0, 1]$，考虑“向 $f$ 分量的投影映射” $\pi_f : [0, 1]^{C(X,[0,1])} \to [0, 1]$，则我们有
$$\pi_f \circ \beta(x) = \pi_f(\operatorname{ev}_x) = f(x).$$
换而言之，如果我们把 $X$ 跟它的同胚像 $\beta(X)$ 等同起来，则 $\pi_f$ 是 $f$ 在 $Q$ 上的一个扩张。当然，因为 $Q$ 太大，一般而言扩张是不唯一的。但是，如果我们限制在 Stone-Čech 紧化 $\beta X$ 上，则扩张是唯一的：【于是这是一个“任意连续函数存在唯一扩张”的例子！】

> [!TIP] Proposition （有界连续函数向紧化空间扩张）
> 设 $X$ 是 LCH 空间（或者更一般地，是 Hausdorff 且完全正则的空间），则任意连续函数 $f : X \to [0, 1]$ 可以被唯一扩张为连续函数 $\tilde{f} = \pi_f|_{\beta X} : \beta X \to [0, 1]$。

Proof. 上面已经说明了 $\tilde{f} = \pi_f|_{\beta X}$ 是 $f$ 的“扩张”，其唯一性由引理 2.9.2 可得。$\square$

下面假设 $\varphi : X \to Y$ 是一个连续映射。则对任意 $g \in C(Y, [0, 1])$，复合映射 $g \circ \varphi \in C(X, [0, 1])$，从而由命题 2.9.19，存在唯一的扩张 $\widetilde{g \circ \varphi} : \beta X \to [0, 1]$。把所有这些函数放在一起，我们得到一个映射
$$\beta\varphi : \beta X \to [0, 1]^{C(Y,[0,1])},$$
使得 $\pi_g(\beta\varphi) = \widetilde{g \circ \varphi}$。由定义，对于任意 $x \in X$，
$$\beta\varphi(\beta(x)) = \left( \widetilde{g \circ \varphi}(\operatorname{ev}_x) \right)_g = (g \circ \varphi(x))_g = \operatorname{ev}_{\varphi(x)} = \beta_Y(\varphi(x)).$$
根据命题 1.5.20，$\beta\varphi$ 的像落在 $\beta Y$ 里面。换而言之，我们得到

> [!TIP] Proposition （$\varphi : X \to Y$ 提升为 $\beta\varphi : \beta X \to \beta Y$）
> 设 $X, Y$ 是 LCH 空间（或者更一般地，是 Hausdorff 且完全正则的空间），则任意连续映射 $\varphi : X \to Y$ 可以被唯一“提升”为连续映射 $\beta\varphi : \beta X \to \beta Y$，使得
> $$\beta\varphi \circ \beta = \beta \circ \varphi.$$

Proof. 上面已经说明了“提升映射”$\beta\varphi : \beta X \to \beta Y$ 的存在性。至于唯一性，因为 $\beta\varphi$ 在稠密子集 $\beta(X)$ 上是由上式所唯一确定，故由引理 2.9.2 可得 $\beta\varphi$ 在 $\beta X$ 上的唯一性。$\square$

作为推论，我们证明 Stone-Čech 紧化的如下重要性质：

> [!NOTE] Theorem （Stone-Čech 紧化的泛性质）
> 设 $X$ 是 LCH 空间，则对于任意紧 Hausdorff 空间 $Y$ 以及任意连续映射 $\varphi : X \to Y$，存在唯一的连续映射 $\tilde{\varphi} : \beta X \to Y$ 使得 $\tilde{\varphi} \circ \beta = \varphi$。进一步，Stone-Čech 紧化 $\beta X$ 是唯一具有该性质的 Hausdorff 紧化。

Proof. 存在唯一性是命题 2.9.20 的直接推论，因为对于紧 Hausdorff 空间，$\beta Y$ 与 $Y$ 同胚。

下面证明 $\beta X$ 是唯一满足该性质的紧 Hausdorff 空间：假设还有紧 Hausdorff 空间 $Z$ 以及映射 $\gamma : X \to Z$ 满足同样的性质。则连续映射 $\beta : X \to \beta X$ 可被扩张为连续映射 $\tilde{\beta} : Z \to \beta X$，使得
$$\tilde{\beta} \circ \gamma = \beta.$$
同理 $\gamma : X \to Z$ 可被扩张为 $\tilde{\gamma} : \beta X \to Z$，使得
$$\tilde{\gamma} \circ \beta = \gamma.$$
注意到 $\tilde{\beta} \circ \tilde{\gamma} : \beta X \to \beta X$ 是连续映射，且在稠密子集 $\beta(X)$ 上有 $\tilde{\beta} \circ \tilde{\gamma} = \operatorname{Id}$。于是由引理 2.9.2，我们在整个 $\beta X$ 上有 $\tilde{\beta} \circ \tilde{\gamma} = \operatorname{Id}$。同理 $\tilde{\gamma} \circ \tilde{\beta} = \operatorname{Id}$。于是 $Z$ 跟 $\beta X$ 同胚。$\square$

> [!Warning] Remark
> 非紧空间的紧化一般是不唯一的。若 $X$ 有两个紧化 $\iota_i : X \to X_i$，$i = 1, 2$，且存在连续映射 $g : X_1 \to X_2$ 使得 $g \circ \iota_1 = \iota_2$，则我们称紧化 $\iota_2$ 比紧化 $\iota_1$ **更精细**。可以证明：对于非紧 LCH 空间，单点紧化是最粗糙的紧化，而 Stone-Čech 紧化是最精细的紧化。


### 单位分解 

我们称集族 $\{U_\alpha\}$ 是**局部有限**的，如果它满足：
	对任意 $x \in X$，存在开集 $U_x \ni x$ 使得仅有有限个 $\alpha$满足 $U_x \cap U_\alpha \neq \varnothing$。

> [!NOTE] Theorem (单位分解)
> 设 $X$ 是正规空间，且闭集族 $\{F_\alpha\}$ 覆盖 $X$（即 $\bigcup_\alpha F_\alpha = X$）。设 $U_\alpha$ 是 $F_\alpha$ 的开邻域，且 $\{U_\alpha\}$ 是局部有限的，则存在连续函数 $\rho_\alpha : X \to [0, 1]$ 使得：
> 1. $\left.\rho_\alpha\right\vert{}_{F_\alpha} > 0$；
>     
> 2. $\rho_\alpha(U_\alpha^c) = \{0\}$；
>    
> 3. $\sum_\alpha \rho_\alpha(x) = 1, \quad \forall x \in X$。

Proof.由 Urysohn 引理，由于 $F_\alpha$ 与 $U_\alpha^c$ 是不相交的闭集，存在连续函数 $g_\alpha : X \to [0, 1]$ 使得
$$g_\alpha(F_\alpha) = \{1\} \quad \text{且} \quad g_\alpha(U_\alpha^c) = \{0\}.$$
令
$$g(x) = \sum_\alpha g_\alpha(x).$$
在每个点 $x$ 的开邻域 $U_x$ 上，该求和只有有限项非零，因此 $g(x)$ 是良好定义的，且在每个 $U_x$ 上均为连续函数的有限和，从而 $g$ 是 $X$ 上的连续函数。
此外，因为 $\bigcup_\alpha F_\alpha = X$，对任意 $x \in X$，必存在某个 $\alpha_0$ 使得 $x \in F_{\alpha_0}$，故 $g_{\alpha_0}(x) = 1$，从而
$$g(x) \geqslant 1, \quad \forall x \in X.$$
最后，定义
$$\rho_\alpha(x) = \frac{g_\alpha(x)}{g(x)}.$$
这些 $\rho_\alpha$ 即为所求。 