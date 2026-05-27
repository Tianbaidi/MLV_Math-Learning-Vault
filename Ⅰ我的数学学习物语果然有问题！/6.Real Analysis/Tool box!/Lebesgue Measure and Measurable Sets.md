---
tags:
  - Real_analysis
  - Measure_Theorem
---
> 本则笔记是 [[The Exterior Measure]] 的延续。 为了解决 [[The Exterior Measure#Remark]] 中提到的“不相交集合外测度不可加”的病态问题，本节正式通过 [[The Exterior Measure#Proposition (开集外逼近)]] 的思想，引入勒贝格可测集。

> [!ABSTRACT] Definition（Lebesgue measurable）
> 即对于任意给定的 $\varepsilon > 0$，都存在一个开集 $\mathcal{O}$ 满足 $E \subset \mathcal{O}$，且：
> $$m_*(\mathcal{O} - E) \le \varepsilon$$
> 这个 $\mathbb{R}^d$ 的子集 $E$ 被称为是**勒贝格可测的（Lebesgue measurable）** 简称可测。我们可以记为 
> $$m(E)=m_{*}(E)$$
> 显然继承了外测度的五条性质

# Measurable Set

除去外测度的几条性质以外，我们将继续探索其对集合运算的 **封闭性** 。

> [!TIP] Proposition
> 任一 $\mathbb{R}^d$ 上的开集都是可测的

这个结论毋庸置疑，我们若取其本身结果显然。

> [!TIP] Proposition
> 若 $m_*(E) = 0$，则 $E$ 是可测的。特别地，如果 $F$ 是一个外测度为 0 的集合的子集，那么 $F$ 是可测的。

由外测度第三条命题可得对于每一个 $\varepsilon > 0$，都存在一个开集 $\mathcal{O}$ 满足 $E \subset \mathcal{O}$ 且 $m_*(\mathcal{O}) \le \varepsilon$。由于 $(\mathcal{O} - E) \subset \mathcal{O}$，单调性意味着 $m_*(\mathcal{O} - E) \le \varepsilon$，从而完成了证明。

> [!TIP] Proposition
> 可测集的可数并是可测的

假设 $E = \bigcup_{j=1}^{\infty} E_j$，其中每一个 $E_j$ 都是可测的。给定 $\varepsilon > 0$，我们可以为每一个 $j$ 选择一个开集 $\mathcal{O}_j$，满足 $E_j \subset \mathcal{O}_j$ 且 $m_*(\mathcal{O}_j - E_j) \le \varepsilon / 2^j$。那么并集 $\mathcal{O} = \bigcup_{j=1}^{\infty} \mathcal{O}_j$ 是开集，$E \subset \mathcal{O}$，并且 $(\mathcal{O} - E) \subset \bigcup_{j=1}^{\infty} (\mathcal{O}_j - E_j)$。因此，外测度的单调性和可数次可加性意味着：
$$m_*(\mathcal{O} - E) \le \sum_{j=1}^{\infty} m_*(\mathcal{O}_j - E_j) \le \varepsilon.$$
这里再次运用了我们的工具 [[ɛ-management ɛ-distribution technique]]

> [!TIP] Proposition
> 闭集是可测的

首先我们引入以下引理，后再讲解其思路

> [!Success] Lemma
> 若 $F$ 是闭集，$K$ 是紧集，且这两个集合互不相交，则 $d(F, K) > 0$

因为 $F$ 是闭集，对于 $K$ 中的每一个点 $x \in K$，都存在一个 $\delta_x > 0$ 满足 $d(x, F) > 3\delta_x$。由于并集 $\bigcup_{x \in K} B_{2\delta_x}(x)$ 覆盖了 $K$，且 $K$ 是紧集，我们可以从中找到一个有限子覆盖，我们将其记为 $\bigcup_{j=1}^{N} B_{2\delta_j}(x_j)$。如果我们令 $\delta = \min(\delta_1, \dots, \delta_N)$，那么我们必然有 $d(K, F) \ge \delta > 0$。
如果 $x \in K$ 且 $y \in F$，那么对于某一个下标 $j$，我们有 $|x_j - x| \le 2\delta_j$，并且根据构造，有 $|y - x_j| \ge 3\delta_j$。因此：
$$|y - x| \ge |y - x_j| - |x_j - x| \ge 3\delta_j - 2\delta_j \ge \delta,$$

性质的证明思路在于将闭集进一步缩紧为紧集，这里的思路类似于我们处理反常积分的情况：

首先，我们注意到只需证明紧集是可测的即可。任何闭集 $F$ 都可以写成紧集的并集，即 $F = \bigcup_{k=1}^{\infty} F \cap B_k$，其中 $B_k$ 表示以原点为中心、半径为 $k$ 的闭球；然后应用上一性质。

因此，假设 $F$ 是紧集（有 $m_*(F) < \infty$），并令 $\varepsilon > 0$ ，我们可以选择一个开集 $\mathcal{O}$ 满足 $F \subset \mathcal{O}$ 且 $m_*(\mathcal{O}) \le m_*(F) + \varepsilon$。因为 $F$ 是闭集，所以差集 $\mathcal{O} - F$ 是开集，并且根据定理 1.4，我们可以将这个差集写成可数个几乎不相交方块的可数并集：
$$\mathcal{O} - F = \bigcup_{j=1}^{\infty} Q_j.$$
对于一个固定的 $N$，有限并集 $K = \bigcup_{j=1}^{N} Q_j$ 是紧集；因此 $d(K, F) > 0$（我们将在下文的一个引理中单独证明这一小事实）。由于 $(K \cup F) \subset \mathcal{O}$，
$$\begin{align*}
m_{*}(\mathcal{O})\geq& m_{*}(F)+m_{*}(K)\\
=& m_{*}(F)+\sum_{j=1}^{N} m_{*}(Q_{j})
\end{align*}$$
因此，$\sum_{j=1}^{N} m_*(Q_j) \le m_*(\mathcal{O}) - m_*(F) \le \varepsilon$，并且这在 $N$ 趋于无穷大的极限下同样成立。此时，调用外测度的次可加性（sub-additivity）性质，最终产生：
$$m_*(\mathcal{O} - F) \le \sum_{j=1}^{\infty} m_*(Q_j) \le \varepsilon,$$
从而完成了证明。

> [!TIP] Proposition
> 可测集的补集是可测的

若 $E$ 是可测的，那么对于每一个正整数 $n$，我们都可以选择一个开集 $\mathcal{O}_n$ 满足 $E \subset \mathcal{O}_n$ 且 $m_*(\mathcal{O}_n - E) \le 1/n$。其补集 $\mathcal{O}_n^c$ 是闭集，因而根据性质 4 是可测的，这意味着并集 $S = \bigcup_{n=1}^{\infty} \mathcal{O}_n^c$ 根据性质 3 也是可测的。现在我们只需注意到 $S \subset E^c$，并且：
$$(E^c - S) \subset (\mathcal{O}_n - E),$$
从而对于所有的 $n$，都有 $m_*(E^c - S) \le 1/n$。因此，$m_*(E^c - S) = 0$，并且根据性质 2，$E^c - S$ 是可测的。因此 $E^c$ 是可测的，因为它是由两个可测集组成的并集，即 $S$ 和 $(E^c - S)$。

> [!TIP] Proposition
> 可测集的可数交是可测的

因为：
$$\bigcap_{j=1}^{\infty} E_j = \left(\bigcup_{j=1}^{\infty} E_j^c\right)^c$$
就是那么任性，我们用了性质三和上一条性质。上述公式来自于  [[Chapter.1.1 Set Theory and Logic.Set#任意并和任意交]]  的 De Margan 公式

> 至此，我们完成了对可测集集合家族的在集合运算下是封闭的

# Properties of Sequences of Measurable Sets and Approximation Theorems

> [!NOTE] Theorem
>  若 $E_{1}，E_{2},\cdots$ 是无交可测集，且 $E=\bigcup_{j=1}^{\infty}E_{j}$ 有 
> $$m(E)=\sum_{j=1}^{\infty} m(E_{j})$$

 
首先，我们进一步假设每个 $E_j$ 都是有界的。此时，对于每个 $j$，通过对 $E_j^c$ 应用可测性的定义，我们可以选择一个 $E_j$ 的闭子集 $F_j$，满足 $m_*(E_j - F_j) \le \varepsilon/2^j$。对于每个固定的 $N$，集合 $F_1, \dots, F_N$ 是紧集且互不相交的，因此有 $m\left(\bigcup_{j=1}^N F_j\right) = \sum_{j=1}^N m(F_j)$。由于 $\bigcup_{j=1}^N F_j \subset E$，我们必然拥有：
$$m(E) \ge \sum_{j=1}^N m(F_j) \ge \sum_{j=1}^N m(E_j) - \varepsilon.$$
令 $N$ 趋于无穷大，由于 $\varepsilon$ 是任意的，我们发现
$$m(E) \ge \sum_{j=1}^{\infty} m(E_j).$$
又因为此前外测度得到的不等式，我们反向的等号总是成立

更一般的，如果我们的集合是无界的。我们选取逐渐怎加到整个 $\mathbb{R}^d$ 的方块序列 $\{ Q_{j} \}^{\infty}_{k=1}$ , 即对任意 $k>1$ 我们都有 $Q_{k}\subset Q_{k+1}$ , 并且 $\bigcup_{k=1}^{\infty} Q_k = \mathbb{R}^d$ 后我们令 $S_1 = Q_1$，并且对于 $k \ge 2$ 令 $S_k = Q_k - Q_{k-1}$。如果我们通过 $E_{j,k} = E_j \cap S_k$ 来定义可测集，那么
$$E = \bigcup_{j,k} E_{j,k}.$$
上述并集是互不相交的，并且每一个 $E_{j,k}$ 都是有界的。此外，$E_j = \bigcup_{k=1}^{\infty} E_{j,k}$，且该并集同样是互不相交的。我们就此得到 
$$m(E)=\sum_{j,k}m(E_{jk})=\sum_{j}\sum_{j}m(E_{j,k})=\sum_{j}(E_{j})$$
我们以及确立了勒贝格测度的可列可加性，这比外测度可有趣多了。

以上证明我们引入入一个集合工具，记录在 [[non-decreasing（increasing） sequence of sets]] 中

> [!Danger] Corollary 测度的连续性
> 设 $E_1, E_2, \dots$ 是 $\mathbb{R}^d$ 的可测子集。
> - **(i) 极限上升**：若 $E_k \nearrow E$，则 $m(E) = \lim_{N\to\infty} m(E_N)$。
> - **(ii) 极限下降**：若 $E_k \searrow E$，且对某个 $k$ 有 $m(E_k) < \infty$，则
> $$m(E) = \lim_{N\to\infty} m(E_N)$$

这个也是在上文的双链接中出现，我们在这里给出证明
**构造不相交集：** 令 $G_1 = E_1$，$G_2 = E_2 - E_1$，一般地，对于 $k \ge 2$，令：
$$G_k = E_k - E_{k-1}$$
这样构造出来的集合族 $\{G_k\}$ 具有很好的性质：它们彼此**两两不相交**，并且它们的无穷并集正好就是 $E$，即 $E = \bigcup_{k=1}^{\infty} G_k$。不仅如此，前 $N$ 个 $G_k$ 的并集刚好就是 $E_N$，即 $\bigcup_{k=1}^N G_k = E_N$。
**利用可列可加性：**
$$m(E) = \sum_{k=1}^{\infty} m(G_k)$$
根据无穷级数的定义，无穷项求和等于部分和的极限：
$$= \lim_{N \to \infty} \sum_{k=1}^N m(G_k)$$
因为前 $N$ 个 $G_k$ 是两两不相交的，所以它们的测度之和等于它们并集的测度（有限可加性）：
$$= \lim_{N \to \infty} m\left(\bigcup_{k=1}^N G_k\right)$$
因为 $\bigcup_{k=1}^N G_k = E_N$，所以最终得到：
$$= \lim_{N \to \infty} m(E_N)$$
第一部分证毕。我们可以用类似的方法来证明第二部分
令 $G_k = E_k - E_{k+1}$（每次剥掉外面的一层）。这样大集合 $E_1$ 就可以表示为最终缩减到的核心 $E$ 与所有剥掉的 “环” 的**不相交并集**：
$$E_1 = E \cup \bigcup_{k=1}^{\infty} G_k$$
由于它们两两不相交，由可列可加性可得：
$$m(E_1) = m(E) + \lim_{N \to \infty} \sum_{k=1}^{N-1} m(G_k)$$
把 $m(G_k) = m(E_k) - m(E_{k+1})$ 代入（这里需要利用 $m(E_{k+1}) < \infty$ 的性质才能做减法）：
$$= m(E) + \lim_{N \to \infty} \sum_{k=1}^{N-1} (m(E_k) - m(E_{k+1}))$$
这是**裂项相消** ，中间的项全部消掉了，只剩下第一项和最后一项：
$$\sum_{k=1}^{N-1} (m(E_k) - m(E_{k+1})) = m(E_1) - m(E_N)$$
所以：
$$m(E_1) = m(E) + m(E_1) - \lim_{N \to \infty} m(E_N)$$
因为假设了 $m(E_1) < \infty$，我们可以在等式两边同时减去 $m(E_1)$，移项后直接得到：
$$m(E) = \lim_{N \to \infty} m(E_N)$$
第二部分证毕。

在之后的定理我们可以知道，任意可测集都可以被包含它的开集很好地逼近，反过来也可以被它包含的闭集很好地逼近。

> [!NOTE] Theorem
> 设 $E$ 是 $\mathbb{R}^d$ 的一个可测子集。那么，对于任意的 $\epsilon > 0$：
> - **(i)** 存在一个开集 $\mathcal{O}$，满足 $E \subset \mathcal{O}$ 且 $m(\mathcal{O} - E) \le \epsilon$。 
> - **(ii)** 存在一个闭集 $F$，满足 $F \subset E$ 且 $m(E - F) \le \epsilon$。 
> - **(iii)** 如果 $m(E)$ 是有限的，则存在一个紧集 $K$，满足 $K \subset E$ 且 $m(E - K) \le \epsilon$。 
> - **(iv)** 如果 $m(E)$ 是有限的，则存在有限个闭方块的并集 $F = \bigcup_{j=1}^N Q_j$，使得：
> $$m(E \Delta F) \le \epsilon$$
> 这里 $\Delta$ 被称为两个集合的对称差，表示为 $E\Delta F=(E-F)\cup(F-E)$ 即非交部分


这里 i 就是测度的定义，对于 ii 我们可知 $E^c$ (补集) 是可测的，故存在一个包含 $E^C$ 的开集 $\mathcal{O}$  且有 $m(\mathcal{O}-E^C)<\varepsilon$ . 我们令 $F=\mathcal{O}$ , 这个结论是显然的。

对于 iii 我们选取一个 $F$ 令其 $F \subset E$ 我们有 $m(E-F)\leq \frac{\varepsilon}{2}$ . 对于任意的 $B$ 我们让其为中心半径为 $n$ 的球 $B_{n}$ 与 $F$ 做交集记 $K_{n}=F\cap B_{n}$ . 于是 $E-K_{n}$ 是一个紧集合且是一个逐渐收敛到 $E-F$ 的可测集序列，由于 $m(E)< \infty$ , 对于所有充分大的 $n$ 都有 $m(E-K_n)\leq \varepsilon$ 

对于 iv 选择一族闭方块 $\{Q_j\}_{j=1}^{\infty}$ 使得：
$$E \subset \bigcup_{j=1}^{\infty} Q_j \quad \text{且} \quad \sum_{j=1}^{\infty} |Q_j| \le m(E) + \epsilon/2$$
由于 $m(E) < \infty$，该级数是收敛的，因此存在一个正整数 $N > 0$ 使得：
$$\sum_{j=N+1}^{\infty} |Q_j| < \epsilon/2$$
如果令 $F = \bigcup_{j=1}^N Q_j$，那么：
$$\begin{aligned} m(E \Delta F) &= m(E - F) + m(F - E) \\ &\le m\left(\bigcup_{j=N+1}^{\infty} Q_j\right) + m\left(\bigcup_{j=1}^{\infty} Q_j - E\right) \\ &\le \sum_{j=N+1}^{\infty} |Q_j| + \sum_{j=1}^{\infty} |Q_j| - m(E) \\ &\le \epsilon. \end{aligned}$$
证明完毕。

> [!TIP] Invariance properties of Lebesgue measure
> - Invariance properties of Lebesgue measure
> 	如果 $E$ 是一个可测集，将其沿着向量 $h \in \mathbb{R}^d$ 整体平移，得到新集合 $E_h = E + h = \{x + h : x \in E\}$。这个平移后的集合 $E_h$ **依然是可测的**，且它的测度（体积）保持不变：
> $$m(E + h) = m(E)$$
> - Dilation-Invariance
> 	假设缩放因子 $\delta > 0$，将集合 $E$ 中的所有点乘以 $\delta$，得到新集合 $\delta E = \{\delta x : x \in E\}$。只要 $E$ 是可测的，缩放后的 $\delta E$ **也必然是可测的**。此时它的体积会变为原来的 $\delta^d$ 倍（因为在 $d$ 维空间中，每个维度都乘了 $\delta$）：
> $$m(\delta E) = \delta^d m(E)$$
> - Reflection-Invariance
> 	将集合 $E$ 关于原点做对称翻转，得到新集合 $-E = \{-x : x \in E\}$。只要 $E$ 可测，$-E$ **也必然可测**，且翻转不改变图形的体积大小：
> $$m(-E) = m(E)$$

以上内容为勒贝格测度对于刚体运动的不变性。