---
tags:
  - Topology
  - Mathematical_Analysis
  - un_complete_notes
  - Functional_Analysis
  - Real_analysis
  - Stone_Weierstrass
  - Hausdorff_Space
---
> 我们曾经在数学分析中学习过 Weierstrass 逼近定理（好像我们还没有学过，不过无所谓）。上一节中我们学习了 AA 定理，其为一个子族 $\displaystyle \mathcal{F} \subset \mathcal{C}(X)$ 具有紧闭包，当且仅当它是等度连续且有界的。那么在我们这一章节中，我们将从紧致性转向稠密性，从 Weierstrass 定理来研究存在一个多项式序列逼近我们的目标函数推广到一致收敛拓扑下, $\displaystyle \mathcal{C}(X)$ 的那些子代数可以稠密地逼近全体连续函数，为一致逼近问题提供代数学判别准则。

> 未完成说明，补充证明细节。

# 连续函数代数与 Stone-Wairestrass 定理

> [!Info] 申明
> 本节我们假设 $\displaystyle X$ 是紧的 Hausdroff 空间，考虑连续函数 $\displaystyle \mathcal{C}(X,\mathbb{R})$ ,在 $\displaystyle X$ 紧致时，度量 
> $$d_{\infty}(f,g):=\sup_{x\in X}|f(x)-g(x)|$$
> 与一致度量 $\displaystyle d_{u}$ 是等价的。$\displaystyle (\mathcal{C}(X,\mathbb{R}),d_{\infty})$ 是完备度量空间。本节我们谈及 $\displaystyle \mathcal{C}(X,\mathbb{R})$ 都将使用 $\displaystyle d_{\infty}$ 度量以及其生成的一致拓扑

### M-A Weierstrass 逼近定理
 在数学分析中，我们学过 Weierstrass 逼近定理 

> [!NOTE] Weierstrass 逼近定理 
> 多项式集合 $\displaystyle \mathcal{P}([0,1])$ 在 $\displaystyle (\mathcal{C}([0,1],d_{\infty}))$ 中是稠密的 i.e 对于任意的$\displaystyle \varepsilon>0$ 和任意的 $\displaystyle f\in \mathcal{C}([0,1],\mathbb{R})$, 存在一个多项式 $\displaystyle P$ s.t 
> $$\sup_{x\in[0,1]}|f(x)-P(x)|<\varepsilon$$

这个证明我们可以采用傅里叶分析的方法，类似的，我们的思路也可以想到用概率论的方式来证明这个式子。首先是原始方法

Proof. 我们有 Fejér 核 
$$F_{N}(t)=\frac{1}{N+1}\sum^N_{n=0}D_{n}(t)$$
这是一个好核，这个好核实际上来自对 $\displaystyle f(x)$ 第 $\displaystyle N$ 阶 Fourier 展开部分和采用 Cesàro 算术平均后得到的核函数记为 $\displaystyle \sigma_{N}(f;x)$ 。由于 $\frac{1}{2\pi}\int_{-\pi}^{\pi} F_N(t)\,dt = 1$，作差估计：
$$\vert{}\sigma_N(f; x) - f(x)\vert{} \le \frac{1}{2\pi} \int_{-\pi}^{\pi} \vert{}f(x - t) - f(x)\vert{} F_N(t) \, dt$$
由 $f(x)$ 在 $\mathbb{R}$ 上一致连续（设界为 $M$）：
- 对任意的 $\displaystyle \varepsilon>0$ , 存在 $\displaystyle \delta>0$ , 当 $\displaystyle |t|<\delta$ 时，$\vert{}f(x - t) - f(x)\vert{} < \frac{\varepsilon}{2}$ 
- 将积分拆为 $\displaystyle |t|<\delta$ 和 $\displaystyle \delta \leq|t|\leq \pi$ 两个部分，有 
$$\vert{}\sigma_N(f; x) - f(x)\vert{} \le \frac{\varepsilon}{2} \cdot \underbrace{\frac{1}{2\pi}\int_{\vert{}t\vert{}<\delta} F_N(t) dt}_{\le 1} \;+\; 2M \cdot \frac{1}{2\pi}\int_{\delta \le \vert{}t\vert{} \le \pi} F_N(t) dt$$
当 $\displaystyle N$ 足够大时，左侧部分小于 $\displaystyle \frac{\varepsilon}{2}$. 于是我们有 
$$\sup_{x \in \mathbb{R}} \vert{}\sigma_N(f; x) - f(x)\vert{} < \varepsilon$$
这证明了：**任意周期连续函数 $f(x)$ 都可以被三角多项式 $\sigma_N(f; x)$ 一致逼近。** 现在我们要将其推广到任意多项式的逼近，设函数 $g(x)$ 是闭区间 $[a, b]$ 上的任意代数连续函数：
- 将 $\displaystyle [a,b]$ 映射到 $\displaystyle [0,\pi]$ 
- 将 $\displaystyle [0,\pi]$ 偶延拓到 $\displaystyle [-\pi,\pi]$ 再作 $2\pi$-周期延拓，得到周期连续函数 $\tilde{g}(x)$
- 我们存在三角多项式 $\displaystyle T(x)=\sum_{k=0}^M a_{k}\cos(kx)$, 使得对所有 $x \in [0, \pi]$ 均有 $\vert{}\tilde{g}(x) - T(x)\vert{} < \frac{\varepsilon}{2}$
- 由于 $\displaystyle \cos(kx)$ 是定义在 $\displaystyle \mathbb{R}$ 上的解析函数，其麦克劳林级数在闭区间上一致收敛，有限代数多项式一致逼近每一个 $\displaystyle \cos(kx)$ 利用三角不等式, 设 $P(x) = \sum_{k=0}^{M} a_k P_k(x)$，则 $P(x)$ 为标准代数多项式
$$\vert{}g(x) - P(x)\vert{} \le \vert{}\tilde{g}(x) - T(x)\vert{} + \vert{}T(x) - P(x)\vert{} < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon$$
即证明了任意闭区间上的连续函数都能用代数多项式一致逼近。

另外，这里给出 Bernstein 构造的多项式子。对任意 $f$，他显式构造了一列多项式，被称为 Bernstein 多项式：
$$B_n(f)(x) := \sum_{i=0}^n f\left(\frac{i}{n}\right) \binom{n}{i} x^i (1 - x)^{n-i}$$
并用概率论方法证明了这一列多项式一致收敛于 $f$。

> [!Danger] Corollary
> 对于任意 $0 < a < b$ 以及任意 $\epsilon > 0$，存在一个多项式 $q = q(t)$，满足 $q(0) = 0$ 且
> $$q([a, b]) \subset (1 - \epsilon, 1 + \epsilon).$$

Proof. 根据 Weierstrass 逼近定理，存在一个多项式 $q_1 \in \mathcal{P}([0, b])$ 使得：$\vert{}q_1(t) - f_0(t)\vert{} < \frac{\epsilon}{2},$ 其中
$$f_0(t) = \begin{cases} t/a, & t \in [0, a], \\ 1, & t \in [a, b]. \end{cases}$$
令 $q(t) = q_1(t) - q_1(0)$ 即可得证。

## 代数

我们想将这个定理推广到更加一般的拓扑空间（不过多项式的概念还是算了）我们有这样的一个问题：能否用一个相对简单的函数族来逼近 $\displaystyle \mathcal{C}(X,\mathbb{R})$ 里的函数？

在 $\displaystyle \mathbb{R}$ 上定义的函数空间自然继承了其加法和乘法，这也是 **Bernstein 多项式** 的基本条件。换言之，我们可以用 **代数** 来构建起这一基本结构。

> [!ABSTRACT] Definition（Algebra）
> 设 $(A, +)$ 是数域 $\mathbb{R}$（或 $\mathbb{C}$）上的一个向量空间，且 $A$ 上还有一个乘法运算
> $$\cdot : A \times A \to A.$$
> 1) 如果对任意 $x, y, z \in A$ 和标量 $a, b$，都有
> 	**(分配律)** $(x + y) \cdot z = x \cdot z + y \cdot z, \quad x \cdot (y + z) = x \cdot y + x \cdot z.$
> 	**(相容性)** $(ax) \cdot (by) = (ab)(x \cdot y).$
> 则我们称三元组 $(A, +, \cdot)$ 为一个**代数**。换言之，代数就是一个赋有满足分配律的双线性乘法运算的向量空间 $A$。
> 2) 如果 $(A, +, \cdot)$ 是一个代数，$B \subset A$ 是一个乘法封闭的向量子空间，则称 $B$ 为 $A$ 的一个**子代数**。
> 3) 如果代数 $A$ 中存在关于乘法的单位元，即存在元素 $1 \in A$ 使得
> $$1 \cdot x = x \cdot 1 = x,$$
> 则称代数 $A$ 是**含幺代数**，并称 $1$ 为该代数的**么元**。
> 4) 如果代数 $A$ 也是一个拓扑向量空间，且拓扑结构与乘法运算也相容，即
> $$\cdot : A \times A \to A$$
> 是连续映射，则我们称 $A$ 是一个**拓扑代数**。
> 5) 如果拓扑代数 $A$ 的子代数 $B$ 是它的闭子空间，则称 $B$ 是 $A$ 的**闭子代数**。

例如 $\mathcal{C}([0, 1], \mathbb{R})$（在赋予一致拓扑的情况下）是一个含幺拓扑代数，子代数 $\mathcal{P}([0, 1])$ 是 $\mathcal{C}([0, 1], \mathbb{R})$ 的含幺子代数，但不是闭子代数。

利用拓扑结构和向量空间结构、乘法运算的相容性，可以证明 
> [!TIP] Proposition（子代数的闭包是闭子代数）
> 设 $\mathcal{A}$ 为拓扑代数，$\mathcal{A}_1 \subset \mathcal{A}$ 为子代数。那么闭包 $\overline{\mathcal{A}_1}$ 是 $\mathcal{A}$ 的（闭）子代数。

### 稠密

>现在设 $\mathcal{A} \subset \mathcal{C}(X, \mathbb{R})$ 是一个子代数。我们想要找出使得 $\mathcal{A}$ 在 $\mathcal{C}(X, \mathbb{R})$ 中稠密的条件。

我们可以先看如下例子：

> [!Example] EXAMPLE 1
> 1) 考虑
> $$\mathcal{A} = \left\{ f = \sum_{k=1}^n a_k x^k \;\middle\vert{}\; n \in \mathbb{N}, a_k \in \mathbb{R} \right\} \subset C([0, 1], \mathbb{R}).$$
> 那么 $\mathcal{A}$ 是 $C([0, 1], \mathbb{R})$ 中的一个子代数，但它不是稠密的：因为
> $$f(0) = 0, \quad \forall f \in \mathcal{A},$$
> 所以 $\mathcal{A}$ 中的函数无法（在度量 $d_\infty$ 下）逼近任意在 $x = 0$ 处非零的函数。
> 2) 考虑
> $$\mathcal{A} = \left\{ f = \sum_{k=0}^n (a_k \cos(kx) + b_k \sin(kx)) \;\middle\vert{}\; n \in \mathbb{N}, a_k, b_k \in \mathbb{R} \right\} \subset C([0, 2\pi], \mathbb{R}).$$
> 那么 $\mathcal{A}$ 是 $C([0, 2\pi], \mathbb{R})$ 中的一个子代数，但它不是稠密的：因为
> $$f(0) = f(2\pi), \quad \forall f \in \mathcal{A},$$
> 所以 $\mathcal{A}$ 中的函数无法（在度量 $d_\infty$ 下）逼近任意满足 $f(0) \neq f(2\pi)$ 的函数 $f$。

由这两个坏的例子，我们定义 **无处消失与分离点** 

> [!ABSTRACT] Definition
> 设 $X$ 是拓扑空间，而 $\mathcal{A}$ 是 $C(X, \mathbb{R})$ 的一个子代数。
> 1. 若对任意 $x \in X$，存在 $f \in \mathcal{A}$ 使得 $f(x) \neq 0$，则我们称 $\mathcal{A}$ 是**无处消失的**。
>	
> 2. 若对任意 $x \neq y \in X$，存在 $f \in \mathcal{A}$ 使得 $f(x) \neq f(y)$，则我们称 $\mathcal{A}$ 是**分离点的**。

如果 $\displaystyle X$ 不是 Hausdoff 的，则 $\displaystyle \mathcal{C}(X,\mathbb{R})$ 是没有分离点的子代数，这是显然的。

#### $\displaystyle \mathcal{C}(X,\mathbb{R})$ 的含幺闭子代数

对于 $\displaystyle \mathcal{C}(X,\mathbb{R})$ 的任何含幺子代数 $\displaystyle \mathcal{A}$ 是无处消失的 

> [!TIP] Proposition （$\mathcal{A}$ 无处消失 $\implies$ $\mathcal{A}$ 含幺）
> 设 $X$ 是紧拓扑空间。如果 $C(X, \mathbb{R})$ 的子代数 $\mathcal{A}$ 无处消失，那么 $1 \in \overline{\mathcal{A}}$，即 $\overline{\mathcal{A}}$ 含幺。

Proof. 对任意 $x \in X$，存在 $f_x \in \mathcal{A}$ 使得 $f_x(x) \neq 0$。设
$$U_x = \{y \mid f_x(y) \neq 0\}.$$
则 $\{U_x\}$ 是 $X$ 的开覆盖。所以存在点 $x_1, \dots, x_m$ 使得 $X \subset U_{x_1} \cup \dots \cup U_{x_m}$。令
$$f_1(x) = f_{x_1}^2 + \dots + f_{x_m}^2 \in \mathcal{A}.$$
则对所有 $x \in X$ 有 $f_1(x) > 0$。由 $X$ 的紧性，存在 $a, b > 0$ 使得对所有 $x \in X$ 有 $a \leqslant f_1(x) \leqslant b$。对于任意 $\epsilon > 0$，由推论 2.6.2，存在 $q \in \mathcal{P}([a, b])$ 满足 $q(0) = 0$，且使得
$$f(x) := q(f_1(x)) \in (1 - \epsilon, 1 + \epsilon),$$
即 $d_\infty(f, 1) < \epsilon$。最后，因为 $q$ 是多项式且 $q(0) = 0$，所以 $f \in \mathcal{A}$。于是 $1 \in \overline{\mathcal{A}}$。 $\square$ 


对于 $\displaystyle \mathcal{C}(X,\mathbb{R})$ 的含幺闭子代数，同时使用代数结构和拓扑结构，我们有

> [!TIP] Proposition （含幺子代数的性质）
> 设 $X$ 是紧拓扑空间，$\mathcal{A}$ 是 $C(X, \mathbb{R})$ 的一个含幺闭子代数，则：
> 1. $f \in \mathcal{A} \implies \vert{}f\vert{} \in \mathcal{A}$.
>
> 2. $f_1, \dots, f_n \in \mathcal{A} \implies \max\{f_1, \dots, f_n\} \in \mathcal{A}, \; \min\{f_1, \dots, f_n\} \in \mathcal{A}$.

Proof.
1) 因为 $f$ 是有界的，根据 Weierstrass 逼近定理，在 $[0, \Vert{}f\Vert{}_\infty^2]$ 上存在一列多项式 $p_n(t)$ 一致收敛到函数 $h(t) = \sqrt{t}$。于是函数列 $p_n \circ f^2$ 一致收敛到函数 $\sqrt{f^2} = \vert{}f\vert{}$。但是因为 $\mathcal{A}$ 是含幺子代数且 $f \in \mathcal{A}$，所以 $p_n \circ f^2 \in \mathcal{A}$。由 $\mathcal{A}$ 的闭性，我们得到 $\vert{}f\vert{} \in \mathcal{A}$。

2) 这是因为
$$\max\{f, g\} = \frac{f + g + \vert{}f - g\vert{}}{2}, \quad \min\{f, g\} = \frac{f + g - \vert{}f - g\vert{}}{2}.$$
	结合 1) 以及归纳法即得欲证。 $\square$

## Stone-Weierstrass 定理
对于 Stone-Weierstrass 定理我们有三个等价的版本分别为

> [!NOTE] Theorem（Stone-Weierstrass Theorem for Compact Hausdorff Spaces-1）
> 设 $X$ 为任意紧 Hausdorff 空间。若 $C(X, \mathbb{R})$ 的子代数 $\mathcal{A}$ 无处消失且分离点，那么 $\mathcal{A}$ 在 $C(X, \mathbb{R})$ 中是稠密的。

> [!NOTE] Theorem（Stone-Weierstrass Theorem in Compactly Convergent Topology）
> 设 $X$ 是 Hausdorff 拓扑空间，$\mathcal{A}$ 是 $(C^\infty(X, \mathbb{R}), \mathcal{T}_{\text{c.c.}})$ 中无处消失且分离点的子代数，则 $\mathcal{A}$ 在 $(C^\infty(X, \mathbb{R}), \mathcal{T}_{\text{c.c.}})$ 中稠密。

> [!NOTE] Theorem（Stone-Weierstrass Theorem for Compact Hausdorff Spaces-2）
> 设 $X$ 是紧致 Hausdorff 空间，$\mathcal{A} \subset C(X, \mathbb{R})$ 是一个分离点的含幺闭子代数。则
> $$\mathcal{A} = C(X, \mathbb{R}).$$

> [!NOTE] Theorem（Stone-Weierstrass Theorem for Compact Hausdorff Spaces-3）
> 设 $X$ 是紧 Hausdorff 空间，$\mathcal{A} \subset C(X, \mathbb{R})$ 是一个分离点的子代数。如果 $\mathcal{A}$ 不稠密，则存在唯一的 $x_0 \in X$ 使得
> $$\overline{\mathcal{A}} = \{f \in C(X, \mathbb{R}) \mid f(x_0) = 0\}.$$

### 复值函数的 Stone-Weierstrass 定理

对于一般的实指函数，$\displaystyle \mathcal{A}$ 是代数自然包含了其共轭封闭，但是对于复值函数，代数运算不能产生共轭运算。对此，我们需要让复子代数 $\displaystyle \mathcal{A}$ 获得自伴性(对共轭封闭) i.e $\displaystyle f\in \mathcal{A}\implies \bar{f}\in \mathcal{A}$ .于是有 

> [!NOTE] Theorem (Stone-Weierstrass Theorem for Complex-valued Functions.)
> 设 $X$ 为紧 Hausdorff 空间，$\mathcal{A} \subset C(X, \mathbb{C})$ 为分离点且无处消失的复子代数。如果 $\mathcal{A}$ 还是自伴的，那么 $\mathcal{A}$ 在 $C(X, \mathbb{C})$ 中是稠密的。

有了自伴性的假设之后，我们可以证明 $\displaystyle f+i(f-\bar{f})$ 是分离点的实值函数，从而可以证明实值形式下的 Stone-Weierstrass 定理。

### LCH 上的 Stone-Weierstrass 定理

> 我们一致都在考虑紧 Hausdoff 上的 Stone-Weierstrass 定理, 倘若紧性减弱很多证明是难以成立的。幸运的是，我们有可以采用局部紧的策略 i.e 局部紧的 Hausdoff 空间：根据非紧 LCH 空间的结构定理，只要对非紧 LCH 空间做单点紧致化，就可以得到紧 Hausdorff 空间，从而可以应用紧 Hausdorff 空间上的 Stone-Weierstrass 定理。

为此，我们考虑空间
$$C_0(X, \mathbb{R}) := \left\{ f \in C(X, \mathbb{R}) \;\middle\vert{}\; \forall \varepsilon > 0, \, \exists \text{ 紧集 } K \subset X, \text{ 使得 } \sup_{x \in K^c} \vert{}f(x)\vert{} < \varepsilon \right\}.$$
我们称 $\displaystyle \mathcal{C}_{0}(X,\mathbb{R})$ 里的元素为在无穷远处消失的元素。可以证明，他是一个代数。另外，易见 $\mathcal{C}_0(X, \mathbb{R})$ 是有界连续函数空间 $(\mathcal{B}(X, \mathbb{R}) \cap \mathcal{C}(X, \mathbb{R}), d_\infty)$ 的一个闭子空间，从而 $d_\infty$ 是 $\mathcal{C}_0(X, \mathbb{R})$ 上的一个完备度量。应用上面所提及的单点紧致化以及版本 3 不难得到

> [!NOTE] Theorem（非紧 LCH 上的 Stone-Weierstrass 定理）
> 设 $X$ 是一个非紧 LCH 空间。若 $\mathcal{A}$ 是 $\mathcal{C}_0(X, \mathbb{R})$ 中的一个无处消失且分离点的子代数，则 $\mathcal{A}$ 在 $\mathcal{C}_0(X, \mathbb{R})$ 中稠密。

## 阅读材料：拓扑的代数化

回到紧 Hausdorff 空间 $X$ 的情况。注意 $\mathcal{C}(X, \mathbb{C})$ 是关于范数
$$\lVert f \rVert_\infty := d_\infty(f, 0)$$
的 Banach 空间。显然，如果 $X, Y$ 是同胚的拓扑空间，则 $\mathcal{C}(X, \mathbb{C})$ 和 $\mathcal{C}(Y, \mathbb{C})$ 作为 Banach 空间是同构的：若 $\varphi : X \to Y$ 是一个同胚映射，我们考虑拉回映射
$$T : \mathcal{C}(Y, \mathbb{C}) \to \mathcal{C}(X, \mathbb{C}), \quad Tf(x) := f(\varphi(x)),$$
则易验证它是 $\mathcal{C}(X, \mathbb{C})$ 和 $\mathcal{C}(Y, \mathbb{C})$ 之间的保范线性同构：
$$\lVert T(f) \rVert_\infty = \sup_{x \in X} \lvert Tf(x) \rvert = \sup_{x \in X} \lvert f(\varphi(x)) \rvert = \sup_{y \in Y} \lvert f(y) \rvert = \lVert f \rVert_\infty.$$
反之，Banach 和 Stone 证明了 $\mathcal{C}(X_1, \mathbb{C})$ 事实上决定了 $X$：

> [!NOTE] Theorem （Banach-Stone 定理）
> 两个紧 Hausdorff 空间 $X_1$ 和 $X_2$ 是同胚的当且仅当 Banach 空间 $\mathcal{C}(X_1, \mathbb{C})$ 和 $\mathcal{C}(X_2, \mathbb{C})$ 是同构的。

事实上，$\mathcal{C}(X, \mathbb{C})$ 除了是 Banach 空间（即向量空间结构、范数结构且度量完备）外，还有乘积结构（从而是一个代数）和共轭，且这些结构都是“相容的”，例如
$$\lVert fg \rVert \leqslant \lVert f \rVert \cdot \lVert g \rVert \quad \text{且} \quad \lVert \bar{f} f \rVert^2 = \lVert f \rVert^2.$$
对这样的对象，我们称之为 $C^*$-代数：

> [!ABSTRACT] Definition （$C^*$-代数）
> 设 $(A, +, \cdot)$ 是一个复结合代数。
> 1. 若 $A$ 上具有对合运算 $* : A \to A$，使得
>    $$x^{**} = x, \quad (x+y)^* = x^* + y^*, \quad (xy)^* = y^* x^*, \quad (\lambda x)^* = \bar{\lambda} x^*,$$
>    则我们称 $(A, +, \cdot, *)$ 是一个 $*$-代数。
> 2. 若 $A$ 上有范数 $\lVert \cdot \rVert$，使得 $(A, +, \lVert \cdot \rVert)$ 是一个 Banach 空间，且 $\lVert xy \rVert \leqslant \lVert x \rVert \lVert y \rVert$，则我们称 $(A, +, \cdot, \lVert \cdot \rVert)$ 是一个 Banach 代数。
> 3. 若 $(A, +, \cdot, *)$ 是一个 $*$-代数，$(A, +, \cdot, \lVert \cdot \rVert)$ 是一个 Banach 代数，且 $*$-代数结构与 Banach 范数结构相容，即
>    $$\lVert x^* x \rVert = \lVert x^* \rVert \lVert x \rVert,$$
>    则我们称 $(A, +, \cdot, *, \lVert \cdot \rVert)$ 是一个 $C^*$-代数。
> 4. 若 $C^*$-代数里的乘法是交换的，即 $xy = yx$，则我们称它为**交换 $C^*$-代数**。

所以 $\mathcal{C}(X, \mathbb{C})$ 是一个含幺交换 $C^*$-代数。事实上，前苏联数学家 I. Gelfand 和 M. Naimark 在 1943 年证明了：任何（抽象）含幺交换 $C^*$-代数都是以这种方式出现的，并给出了从 $\mathcal{C}(X, \mathbb{C})$ 到 $X$ 的显式构造：

> [!NOTE] Theorem （Gelfand-Naimark 定理，交换版本）
> 对任意含幺交换 $C^*$-代数 $A$，都存在紧 Hausdorff 空间 $X$ 使得 $A$ 同构于 $\mathcal{C}(X, \mathbb{C})$。

Proof. 概要如下：考虑由 $A$ 的非零特征 $\varphi : A \to \mathbb{C}$（即保乘法的线性泛函，也称代数同态）组成的集合 $\Sigma$。可以证明：每个特征 $\varphi$ 都是连续映射，于是每个特征都是 Banach 空间 $A$ 的对偶空间 $A^*$ 中的一个元素；接着证明每个特征 $\varphi$ 在 $A^*$ 中都有对偶范数 $\leqslant 1$，于是 $\Sigma$ 事实上是 $A^*$ 中的闭单位球 $B(A^*)$ 的子集；然后证明 $\Sigma$ 关于弱-$*$ 拓扑是 $B(A^*)$ 的闭子集。根据 Banach-Alaoglu 定理，$B(A^*)$ 关于弱-$*$ 拓扑是紧 Hausdorff 空间，因此 $\Sigma$（关于弱-$*$ 拓扑）也是紧 Hausdorff 的。最后证明 $A$ 与 $\mathcal{C}(\Sigma, \mathbb{C})$ 同构：对 $A$ 中的每个元素 $a$，由 Gelfand 变换 $\hat{a}(\varphi) := \varphi(a)$ 给出 $A$ 与 $\mathcal{C}(\Sigma, \mathbb{C})$ 的同构。$\square$

> 由函数所组成的代数与作为背景的几何空间之间也存在着一种相互决定的对偶关系：人们可以通过研究函数代数而得到背景空间的所有信息。这样的对偶关系不仅出现在拓扑中，也出现在代数几何等其他学科。更进一步地，数学家们将这种“对偶性”思想延拓到研究更复杂的非交换代数，并由此导向了一个新的数学分支：**非交换几何**。

