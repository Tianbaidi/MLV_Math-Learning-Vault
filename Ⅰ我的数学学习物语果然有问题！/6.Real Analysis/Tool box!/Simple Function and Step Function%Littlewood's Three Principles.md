---
tags:
  - Measure_Theorem
  - Real_analysis
---
> [!NOTE] Theorem
> 令 $f$ 是一个 $\mathbb{R}^d$ 上的非负可测函数，存在一个非负的递增函数列 $\{ \varphi_{k} \}_{k=1}^{\infty}$ 逐点收敛 $f$  
> $$\varphi_{k}(x)\leq \varphi_{k+1}(x) \quad \text{and} \quad \\lim_{ k \to \infty } \varphi_{k}(x)=f(x)\, ,\, for~all~x$$


**Proof.** 对于任意的 $N\ge{1}$ ,令 $Q_{N}$ 为以原点为中心，边长为 $N$ 的立方体，我们构造以下函数 
$$F_{N}(x)\begin{cases}
f(x) \quad \text{if }x\in Q_{N} \text{ and } f(x)\leq N  \\
N \quad \text{if }x\in Q_{N} \text{ and } f(x)>N  \\
0 \quad \text{otherwise}
\end{cases}$$
当 $N$ 足够大的情况下，$F_{N}(x) \to f(x)$ .我们定义一系列 $F_{N}$ 的分块 $M,N>1$ 有 
$$E_{l.m}=\left\{  x\in Q_{N}: \frac{l}{M}< F_{N}(x)\leq \frac{l+1}{M}  \right\}$$
这里 $l\in(0,MN)$ , 于是定义简单函数 
$$F_{N,M}(x)=\sum_{l} \frac{l}{M}\chi_{E_{lm}}(x)$$
-  $\chi$ 表示
$$\begin{cases}
1,\quad x\in E \\
0,\quad x\not\in E
\end{cases}$$
于是, 对于简单函数，必然有 
$$0\leq F_{N}(x)-F_{N,M}(x)\leq \frac{1}{M}$$
我们令 $M=N=2^k$ 定义 $\varphi_{k}=F_{2^k,2^k}$ ,于是得到了 $0<F_{M}(x)-\varphi_{k}(x)\leq \frac{1}{2^k}$ . 对于任意的 $x$  $\{ \varphi_{k} \}$ 是递增的。于是定理得证.

下一条定理则是对这条定理的补充，

> [!NOTE] Theorem
> 令 $f$ 是 $\mathbb{R}^d$ 上的可测函数，存在一系列简单函数 $\{ \varphi_{k} \}_{k=1}^{\infty}$ 满足 
> $$|\varphi_{k}(x)|\leq |\varphi_{k+1}(x)| \qquad \text{and} \qquad \lim_{ k \to \infty } \varphi(k)(x)=f(x) , for~all~x$$
> 特别的 ，我们有 $|\varphi_{k}(x)|\leq |f(x)|$ 对于所有的 $x$ 与 $k$ 成立 

我们定义一个函数的正负部分分别为 $f: f(x)=f^+(x)-f^-(x)$ 这里分别取其非符号部分。即都是非负的。参考上一定理的证明
**Proof.**  我们令 $\{ \varphi^{1.}_{k}(x) \}_{k=1}^{\infty}$ , $\{ \varphi_{k}^{2.} (x)\}_{k=1}^{\infty}$ 逐点收敛我们定义的 $\pm$ 函数，于是，我们有 
$$\varphi_{k}(x)=\varphi^{1.}_{k}(x) - \varphi_{k}^{2.} (x)$$
$\varphi_{k}(x)$ 对任意的 $x$ 都收敛到 $f(x)$ . 同理 $\{ |\varphi_{k}| \}$ 是递增的。

让我们更进一步，下面一个定理将介绍阶梯函数（一类特殊的简单函数）

> [!NOTE] Theorem
> 令 $f$ 是 $\mathbb{R}^d$ 上的可测函数，存在一系列阶梯函数 $\{ \psi_{k} \}_{k=1}^{\infty}$ 满足对几乎处处 $x$ 下 $f(x)$ 逐点收敛 

根据前一个结论（注：即任何可测函数都可以被简单函数逐点逼近），我们只需证明：若 $E$ 是一个有限测度的可测集，则函数 $f = \chi_E$ 可以被阶梯函数逼近。

为此，我们回顾 [[Lebesgue Measure and Measurable Sets#140#142|定理 3.4 iv]]，该定理指出：对于任意的 $\epsilon$，存在（有限个）立方体 $Q_1, \dots, Q_N$，使得：
$$m\left(E \Delta \bigcup_{j=1}^N Q_j\right) \leq \epsilon$$
通过考虑将这些立方体的边进行延伸所形成的网格，我们可以看到，存在互相几乎不相交（注：指内部不相交，边界可重合）的矩形 $\tilde{R}_1, \dots, \tilde{R}_M$，使得它们的并集完全等于原本立方体的并集：
$$\bigcup_{j=1}^N Q_j = \bigcup_{j=1}^M \tilde{R}_j$$
我们在 $\tilde{R}_j$ 内部取一系列尺寸稍小一点的（严格）不相交矩形 $R_j$，可以找到这样一组互不相交的矩形族，使其满足：
$$m\left(E \Delta \bigcup_{j=1}^M R_j\right) \leq 2\epsilon$$
因此，除了可能在一个测度 $\leq 2\epsilon$ 的集合上之外，我们有：
$$f(x) = \sum_{j=1}^M \chi_{R_j}(x)$$
由此可知，对于每一个 $k \geq 1$，都存在一个阶梯函数 $\psi_k(x)$，使得如果我们定义“坏集”（即函数值不相等的地方）为：
$$E_k = \{x : f(x) \neq \psi_k(x)\}$$
则该坏集的测度满足 $m(E_k) \leq 2^{-k}$。

如果我们令 $F_K = \bigcup_{j=K+1}^\infty E_j$，并定义最终的坏集为 $F = \bigcap_{K=1}^\infty F_K$，那么由于 $m(F_K) \leq 2^{-K}$，可得 $m(F) = 0$。并且，对于所有属于 $F$ 的补集（即 $F^c$）中的 $x$，都有 $\psi_k(x) \to f(x)$。

---

尽管可测集和可测函数的概念代表了新的工具，但我们不应该忽视它们与它们所取代的旧概念之间的关系。Littlewood 将这些联系精辟地概括为三个原理，这些原理在该理论的初步学习中提供了有用的直观指导。

- 每个**可测集**都几乎是有限个区间的并集。
    
- 每个**可测函数**都几乎是连续的。**(注：即鲁辛定理 Lusin's Theorem)**
    
- 每个**几乎处处收敛**的函数列都几乎是一致收敛的。**(注：即叶戈罗夫定理 Egorov's Theorem)**
    
上面提到的集合和函数当然都被假定是可测的。关键在于“几乎（nearly）”这个词，必须在具体的上下文中赋予其恰当的理解。

> [!NOTE] Theorem (Egorov)
>假设 $\{f_k\}_{k=1}^\infty$ 是定义在有限测度可测集 $E$（即 $m(E) < \infty$）上的一列可测函数，并假设在 $E$ 上 $f_k \to f$ 几乎处处（a.e.）成立。给定任意 $\epsilon > 0$，我们可以找到一个闭集 $A_\epsilon \subset E$，使得 $m(E - A_\epsilon) \leq \epsilon$，且 $f_k \to f$ 在 $A_\epsilon$ 上一致收敛。


**Proof.**，我们可以假设在 $E$ 中的每一个点 $x$ 处都有 $f_k(x) \to f(x)$（注：即直接挖掉了原先那个测度为 0 的不收敛点集）。对于每一对非负整数 $n$ 和 $k$，令：
$$E_k^n = \{x \in E : |f_j(x) - f(x)| < 1/n, \quad \text{for all  } j > k\}$$
现在固定 $n$，注意到 $E_k^n \subset E_{k+1}^n$，且当 $k$ 趋于无穷大时，$E_k^n \nearrow E$（单调递增趋于 $E$）。根据推论 3.3（注：测度的连续性），我们发现存在一个正整数 $k_n$，使得：
$$m(E - E_{k_n}^n) < 1/2^n$$
根据构造，我们随后可以得到：
$$ \quad |f_j(x) - f(x)| < 1/n \quad \text{ whenever}\quad j > k_n \text{ and } x \in E_{k_n}^n ，$$
我们选择一个足够大的整数 $N$，使得 $\sum_{n=N}^\infty 2^{-n} < \epsilon/2$，并令：
$$\tilde{A}_\epsilon = \bigcap_{n \geq N} E_{k_n}^n$$
我们首先观察到：
$$m(E - \tilde{A}_\epsilon) \leq \sum_{n=N}^\infty m(E - E_{k_n}^n) < \epsilon/2$$接下来，若 $\delta > 0$，我们选择一个足够大的 $n \geq N$ 使得 $1/n < \delta$。注意到 $x \in \tilde{A}_\epsilon$ 意味着 $x \in E_{k_n}^n$。因此我们看到，只要 $j > k_n$，就有 $|f_j(x) - f(x)| < \delta$。由此可知，$f_k$ 在 $\tilde{A}_\epsilon$ 上一致收敛到 $f$。

最后，利用 [[Lebesgue Measure and Measurable Sets#140#142|定理 3.4 iv]]，选择一个闭子集 $A_\epsilon \subset \tilde{A}_\epsilon$，使得 $m(\tilde{A}_\epsilon - A_\epsilon) < \epsilon/2$。结果表明，我们有 $m(E - A_\epsilon) < \epsilon$，定理得证。

接下来的定理证明了 Littlewood 第二原理的有效性。

> [!NOTE] Theorem (Lusin)
> 假设 $f$ 是定义在有限测度集 $E$ 上的可测函数，且在 $E$ 上取有限值。那么对于任意的 $\epsilon > 0$，存在一个闭集 $F_\epsilon$，满足：
> $$F_\epsilon \subset E, \quad \text{and} \quad m(E - F_\epsilon) \leq \epsilon$$
> 并且使得限制函数 $f|_{F_\epsilon}$ 是连续的。我们用 $f|_{F_\epsilon}$ 表示将函数 $f$ 的定义域限制在集合 $F_\epsilon$ 上。

**Proof.** 令 $\{f_n\}$ 为一列阶梯函数，使得 $f_n \to f$ 几乎处处（a.e.）成立。然后我们可以找到集合 $E_n$，使得 $m(E_n) < 1/2^n$，并且 $f_n$ 在 $E_n$ 之外（即 $E_n^c$ 上）是连续的。根据叶戈罗夫定理，我们可以找到一个集合 $A_{\epsilon/3}$，在此集合上 $f_n \to f$ 是一致收敛的，且满足 $m(E - A_{\epsilon/3}) \leq \epsilon/3$。

然后，对于足够大的 $N$，使得 $\sum_{n \geq N} 1/2^n < \epsilon/3$，我们考虑集合：

$$F' = A_{\epsilon/3} - \bigcup_{n \geq N} E_n$$

现在，对于每一个 $n \geq N$，函数 $f_n$ 在 $F'$ 上都是连续的；因此，$f$（作为连续函数列 $\{f_n\}$ 的一致极限）在 $F'$ 上也是连续的。为了完成证明，我们仅仅需要用一个闭子集 $F_\epsilon \subset F'$ 去逼近集合 $F'$，使得 $m(F' - F_\epsilon) < \epsilon/3$ 即可。