---
tags:
  - Real_analysis
  - Measure_Theorem
---
本则笔记用到的skills： [[ɛ-management ɛ-distribution technique]] 

> [!ABSTRACT] Definition (Exterior Maesure)
> 如果 $E$ 是任意 $\mathbb{R}^d$ 的子集，其 $E$ 外测度为
> $$m_{*}(E)=\inf\sum_{j=1}^{\infty}|Q_{j}|.$$
> 下界包含了所有的可数闭方块 $E\subset\bigcup_{j=1}^\infty Q_{j}$  .外测度通常是非负且可能等于 $+\infty$ . i.e. 广义正数 （Extended positive numbers）

外测度通常符合我们的一些直觉（有些会超越直觉）
- 与体积一致且不受到 “边界” 影响（开or闭）
- $\mathbb{R}^d$ 本身的外测度为 $\infty$
- 康托尔集 $\mathcal{C}$ 的外测度为 $0$

这里我们浅谈 $Cantor~Set$ 的情况. 这个集和的特点在于无限在一个集和中消去 $\frac{1}{3}$ :
- $\mathcal{C}_{0}$ : $[0,1]$ ,其长度为 $\mathbf{1}$ 
- $\mathcal{C}_{1}$ : 消去其中的 $\left( \frac{1}{3}, \frac{2}{3} \right)$ ,我们得到的长度为 $\frac{2}{3}$
  $\vdots$ 
- $\mathcal{C_{k}}\cdots$
这是反复迭代后我们得到了一堆离散的 “点” 由外测度的定义 
$$m_{*}{(\mathcal{C}_{k})}\leq \sum_{j=1}^{2k} \frac{1}{3^k}=\left( \frac{2}{3} \right)^k\sim 0$$

---
# Properties of The Exterior Measure

> [!TIP] Proposition (Monotonicity)
> 单调性意味着，如果 $E_{1} \subset E_{2}$ ,于是我们有 $m_{{*}}(E_{1})\leq m_{*}(E_{2})$ 

任何对 $E_2$ 的可数方块覆盖同时也必然是 $E_1$ 的覆盖，结论便随之成立。特别地，单调性意味着 $\mathbb{R}^d$ 中的每一个有界子集都具有有限的外测度。

> [!TIP] Proposition (Countable Sub-additivity)
> 若 $E=\bigcup_{j=1}^\infty E_{j}$ , 于是有 $m_{*}(E)\leq\sum_{j=1}^\infty m_{*}(E_{j})$

若 $m_{*}(E_{j})=\infty$ 那么结论显然， 我们讨论不为无穷得情况。
我们可以讨论 $E_{j}<\infty$ ，$E_{j}$ 必存在一个闭方块的覆盖 $E_{j}\subset \bigcup_{k=1}^{\infty}Q_{k,j}$ ,满足不等式 
$$\sum_{k=1}^{\infty}|Q_{k,j}|\leq m_{*}(E_{j})+ \frac{\varepsilon}{2^j}$$
于是我们有 $E \subset \bigcup_{j,k=1}^{\infty}Q_{j,k}$ 是 $E$ 的一个闭方块覆盖，因此： 
$$\begin{align*}
m_*(E) \le &\sum_{j,k} |Q_{k,j}| = \sum_{j=1}^{\infty} \sum_{k=1}^{\infty} |Q_{k,j}|\\
\le& \sum_{j=1}^{\infty} \left( m_*(E_j) + \frac{\epsilon}{2^j} \right)\\
= &\sum_{j=1}^{\infty} m_*(E_j) + \epsilon
\end{align*}$$
 这里的 $\varepsilon$ 是任意的，于是成立
  
> [!TIP] Proposition 
> 若 $E \subset \mathbb{R}^d$，则 $m_*(E) = \inf m_*(\mathcal{O})$，其中下确界取自所有包含 $E$ 的开集 $\mathcal{O}$。

这个证明会类似于上一个证明，根据单调性，我们可以知道 $m_*(E) \le \inf m_*(\mathcal{O})$ 。令 $\varepsilon > 0$，并选择方块 $Q_j$ 使得 $E \subset \bigcup_{j=1}^{\infty} Q_j$，且满足：
$$\sum_{j=1}^{\infty} |Q_j| \le m_*(E) + \frac{\varepsilon}{2}$$
令 $Q_j^0$ 表示一个包含 $Q_j$ 的开方块，且满足 $|Q_j^0| \le |Q_j| + \frac{\varepsilon}{2^{j+1}}$。那么 $\mathcal{O} = \bigcup_{j=1}^{\infty} Q_j^0$ 是开集，再由上一命题可以得到 
$$\begin{align*}
m_*(\mathcal{O}) \le& \sum_{j=1}^{\infty} m_*(Q_j^0) = \sum_{j=1}^{\infty} |Q_j^0|\\
\le &\sum_{j=1}^{\infty} \left( |Q_j| + \frac{\epsilon}{2^{j+1}} \right)\\
\le &\sum_{j=1}^{\infty} |Q_j| + \frac{\epsilon}{2}\\
\le &m_*(E) + \epsilon
\end{align*}
$$
于是得证

> [!TIP] Proposition 
> 若 $E = E_1 \cup E_2$，且 $d(E_1, E_2) > 0$，则 
> $$m_*(E) = m_*(E_1) + m_*(E_2)$$
> $d(E_{1},E_{2})$ 表示两个集合间元素差最小的那个 $d(E_1, E_2) = \inf \{ |x - y| : x \in E_1, y \in E_2 \}$ , 直接理解为两个集合间的距离

这个由可加性可以得到 $m_*(E) \le m_*(E_1) + m_*(E_2)$ 。

我们首先选择一个 $\delta$，使得 $d(E_1, E_2) > \delta > 0$ 。我们再选择一个由闭方块构成的覆盖 $E \subset \bigcup_{j=1}^{\infty} Q_j$，满足 $\sum_{j=1}^{\infty} |Q_j| \le m_*(E) + \varepsilon$ . 

假设每个 $Q_j$ 的边长都小于 $\delta$。在这种情况下，每个 $Q_j$ 最多只能与 $E_1$ 或 $E_2$ 这两个集合中的一个相交。

如果我们用 $J_1$ 和 $J_2$ 分别表示那些与 $E_1$ 和 $E_2$ 相交的下标 $j$ 的集合，那么 $J_1 \cap J_2$ 为空集，并且我们有
$$E_1 \subset \bigcup_{j \in J_1} Q_j \quad \text{as well as} \quad E_2 \subset \bigcup_{j \in J_2} Q_j$$
因此，
$$\begin{align*}
m_*(E_1) + m_*(E_2) \le & \sum_{j \in J_1} |Q_j| + \sum_{j \in J_2} |Q_j| \\
\le& \sum_{j=1}^{\infty} |Q_j| \\
\le &m_*(E) + \varepsilon
\end{align*}
$$
由于 $\varepsilon$ 是任意的, 故成立.

> [!TIP] Proposition 
> 若集合 $E$ 是可数个几乎不相交方块的可数并集 $E = \bigcup_{j=1}^{\infty} Q_j$，则
> $$m_*(E) = \sum_{j=1}^{\infty} |Q_j|$$

由第二条性质，我们且知道 $m_{*}(E)\leq \sum_{j=1}^{\infty}|Q_{j}|$ .
任意给定 $\varepsilon$ , 令 $\tilde{Q}_j$ 为一个严格包含在 $Q_j$ 内部的方块，且满足 $|Q_j| \le |\tilde{Q}_j| + \varepsilon/2^j$，那么，对于每一个 $N$，方块 $\tilde{Q}_1, \tilde{Q}_2, \dots, \tilde{Q}_N$ 是互不相交的，其满足 $d(Q_{x},Q_{y})>0$ . 我们重复利用上一个命题可以得到 
$$m_*\left( \bigcup_{j=1}^N \tilde{Q}_j \right) = \sum_{j=1}^N |\tilde{Q}_j| \ge \sum_{j=1}^N \left( |Q_j| - \frac{\varepsilon}{2^j} \right)$$
由于 $\bigcup_{j=1}^N \tilde{Q}_j \subset E$，我们得出
$$m_*(E) \ge \sum_{j=1}^N |Q_j| - \varepsilon$$
若 $N \to \infty$ , 对每一个 $\varepsilon > 0$ 均有 $\sum_{j=1}^{\infty} |Q_j| \le m_*(E) + \varepsilon$，故 $\sum_{j=1}^{\infty} |Q_j| \le m_*(E)$ 。

> [!Warning] Remark
> 尽管有 4 和 5 的结论，但在一般情况下，**不能** 因为 $E_1 \cup E_2$ 是 $\mathbb{R}^d$ 的不相交子集的并集，就得出：
> $$m_*(E_1 \cup E_2) = m_*(E_1) + m_*(E_2)$$
> 只有当所讨论的集合不是高度不规则或“病态（pathological）”的，而是满足可测（measurable）意义时，这个式子才会成立。

