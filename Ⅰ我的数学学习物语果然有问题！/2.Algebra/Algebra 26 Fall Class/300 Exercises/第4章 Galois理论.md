---
tags:
  - Algebra
  - Exercises
---


## §1 基本定理

> [!question]- 4.1.1
> 求证:
> (1) $\text{Gal}(E/-\): $\Omega \longrightarrow \Gamma$ 和 $\text{Inv}:\Gamma \longrightarrow \Omega$ 是反序的映射, 即若 $M_1 \subseteq M_2$, 则 $\text{Gal}(E/M_1) \supseteq \text{Gal}(E/M_2)$; 若 $H_1 \subseteq H_2$, 则 $\text{Inv}(H_1) \supseteq \text{Inv}(H_2)$.
> (2) (作用 3 次等于作用 1 次) 对于 $M \in \Omega$, $H \in \Gamma$ 有
> $\text{Gal}(E/\text{Inv}(\text{Gal}(E/M))) = \text{Gal}(E/M)$, $\text{Inv}(\text{Gal}(E/\text{Inv}(H))) = \text{Inv}(H)$.


> [!question]- 4.1.2*
> 证明 Artin 引理: 设 $K$ 是域, $G$ 是 $K$ 的自同构群 $\text{Aut}(K)$ 的有限子群. 则有 $[K:\text{Inv}(G)] \leqslant |G|$, 这里 $\text{Inv}(G) = \{a \in K \mid \sigma(a) = a, \forall \sigma \in G\}$.


> [!question]- 4.1.3*
> 证明 Galois 理论基本定理:
> (1) $\text{Gal}(E/-\): $\Omega \longrightarrow \Gamma$ 和 $\text{Inv}:\Gamma \longrightarrow \Omega$ 是互逆的反序的映射.
> (2) $H$ 是 $G$ 的正规子群当且仅当 $\text{Inv}(H)/F$ 是正规扩张. 在这种情况下, 有
> $\text{Gal}(\text{Inv}(H)/F) \cong G/H$.


> [!question]- 4.1.4
> 设 $E = \mathbb{Q}(\sqrt{2}, \sqrt{3}, u)$, $u^2 = (9 - 5\sqrt{3})(2 - \sqrt{2})$. 求证 $E/\mathbb{Q}$ 是 Galois 扩张, 并决定 Galois 群 $\text{Gal}(E/\mathbb{Q})$.


> [!question]- 4.1.5
> 设 $E = \mathbb{C}(t)$ (复数域上有理函数域), $\sigma, \tau \in \text{Gal}(E/\mathbb{C})$, 其中 $\sigma(t) = \omega t$, $\omega = \mathrm{e}^{2\pi i/3}$, $\tau(t) = t^{-1}$. 求证:
> (1) $\tau$ 和 $\sigma$ 生成的群 $H$ 是 $\text{Gal}(E/\mathbb{C})$ 的 6 阶子群.
> (2) $\text{Inv}(H) = \mathbb{C}(t^3 + t^{-3})$.


> [!question]- 4.1.6
> 设域 $F$ 的特征为素数 $p$, $\sigma \in G = \text{Gal}(F(x)/F)$, 其中 $\sigma(x) = x + 1$. 令 $H$ 为由 $\sigma$ 生成的 $G$ 之子群, 求证 $|H| = p$. 试问: $\text{Inv}(H) = ?$


> [!question]- 4.1.7
> 设域 $F$ 的特征为素数 $p, a \in F$. 求证:
> (1) $x^p - x - a$ 是 $F[x]$ 中不可约多项式 $\Longleftrightarrow$ 不存在 $c \in F$, 使得 $a = c^p - c$.
> (2) 如果 $x^p - x - a$ 在 $F[x]$ 中不可约, 令 $\alpha$ 为 $x^p - x - a$ 的一个根, 求证 $F(\alpha)/F$ 为 Galois 扩张. 试决定 Galois 群 $\text{Gal}(F(\alpha)/F)$.


> [!question]- 4.1.8*
> 设 $L$ 和 $M$ 均是域 $E$ 的子域. 求证: 如果 $L/(L \cap M)$ 为有限 Galois 扩张, 则 $LM/M$ 也为有限 Galois 扩张, 并且 $\text{Gal}(LM/M) \cong \text{Gal}(L/(L \cap M))$.


> [!question]- 4.1.9
> 设 $E/F$ 为有限 Galois 扩张, $N$ 和 $M$ 为中间域, $E \supseteq N \supseteq M \supseteq F$. 并且 $N$ 是 $M$ 在 $F$ 上的正规闭包. 求证:
> 
> $$\text{Gal}(E/N) = \bigcap_{\sigma \in \text{Gal}(E/F)} \sigma \text{Gal}(E/M) \sigma^{-1}.$$


> [!question]- 4.1.10
> 设 $E$ 为 $x^4 - 2$ 在 $\mathbb{Q}$ 上的分裂域.
> 
> (1) 试求出 $E/\mathbb{Q}$ 的全部中间域.
> 
> (2) 试问哪些中间域是 $\mathbb{Q}$ 的 Galois 扩张? 哪些域彼此共轭?


> [!question]- 4.1.11
> 设 $\zeta = \mathrm{e}^{\frac{2\pi i}{12}}$, 求证 $\mathbb{Q}(\zeta)/\mathbb{Q}$ 是 Galois 扩张. 求 $G = \text{Gal}(\mathbb{Q}(\zeta)/\mathbb{Q})$. 列出 $G$ 的全部子群和它们对应的 $\mathbb{Q}(\zeta)/\mathbb{Q}$ 的中间域.


> [!question]- 4.1.12
> 对 $\zeta = \mathrm{e}^{\frac{2\pi i}{9}}$ 做 4.1.11 题的事情.


> [!question]- 4.1.13
> 设 $n$ 为大于 2 的整数, $\zeta_n = \mathrm{e}^{\frac{2\pi i}{n}}$, $\mathbb{R}$ 为实数域. 求证: $\mathbb{Q}(\zeta_n) \cap \mathbb{R} = \mathbb{Q}(\zeta_n + \zeta_n^{-1})$.


> [!question]- 4.1.14*
> 设 $p$ 为奇素数, $\zeta_p = \mathrm{e}^{\frac{2\pi i}{p}}$. 求证 $\mathbb{Q}(\zeta_p)$ 有唯一的二次子域 $K$ (即 $K$ 为 $\mathbb{Q}(\zeta_p)$ 的子域并且 $[K : \mathbb{Q}] = 2$). 进而, $K$ 是实二次域 (即 $K \subseteq \mathbb{R}) \iff p \equiv 1 \pmod{4}$.


> [!question]- 4.1.15
> 设 $E/F$ 为有限 Galois 扩张. 如果对任一域 $K (F \subsetneq K \subseteq E)$, $K$ 对 $F$ 均有相同的扩张次数 $[K : F]$, 则 $[E : F] = p, p$ 为素数.


> [!question]- 4.1.16
> (1) 求证 $\mathbb{Q}(\sqrt{2}, \sqrt{3}, \sqrt{5})/\mathbb{Q}$ 是 Galois 扩张, 并求此扩张的 Galois 群.
> 
> (2) 求元 $\sqrt{6} + \sqrt{10} + \sqrt{15}$ 在 $\mathbb{Q}$ 上的极小多项式.
> 
> (3) 求证 $\sqrt{6} \in \mathbb{Q} (\sqrt{6} + \sqrt{10} + \sqrt{15})$.
> 
> (4) 求 $\sqrt{2} + \sqrt{3}$ 在 $\mathbb{Q} (\sqrt{6} + \sqrt{10} + \sqrt{15})$ 上的极小多项式.


## §2 方程的 Galois 群

> [!question]- 4.2.1
> 设 $F$ 是特征为 2 的域. 求 $f(x)$ 在 $F$ 上的 Galois 群, 其中
> 
> (1) $f(x) = x^3 + x + 1$.
> 
> (2) $f(x) = x^3 + x^2 + 1$.


> [!question]- 4.2.2
> 设 $f(x) \in \mathbb{R}[x]$ 是三次不可约多项式. 求证: $d(f) > 0$ 当且仅当 $f(x)$ 有三个实根; $d(f) < 0$ 当且仅当 $f(x)$ 只有一个实根.


> [!question]- 4.2.3
> 求 Galois 群 $\text{Gal}(\mathbb{Q}(\sqrt[4]{2}(1 + \mathrm{i}))/\mathbb{Q})$, 其中 $\mathrm{i} = \sqrt{-1}$.


> [!question]- 4.2.4
> 设 $p$ 为素数, $a \in \mathbb{Q}$, $x^p - a$ 为 $\mathbb{Q}[x]$ 中不可约多项式. 求 $x^p - a$ 在 $\mathbb{Q}$ 上的 Galois 群.


> [!question]- 4.2.5
> 决定 $f(x)$ 在 $\mathbb{Q}$ 上的 Galois 群, 其中
> (1) $f(x) = x^5 - 6x + 3$.
> (2) $f(x) = x^5 - 15x^2 + 9$.


> [!question]- 4.2.6
> 决定 $f(x)$ 在域 $F$ 上的 Galois 群, 其中
> (1) $f(x) = x^4 - 5$, $F = \mathbb{Q}$.
> (2) $f(x) = x^4 - 5$, $F = \mathbb{Q}(\sqrt{5})$.
> (3) $f(x) = x^4 - 5$, $F = \mathbb{Q}(\sqrt{5}\mathrm{i})$.
> (4) $f(x) = x^4 - 10x^2 + 4$, $F = \mathbb{Q}$.


> [!question]- 4.2.7
> 设 $n \geqslant 2$ 是正整数, 域 $F$ 的特征为零或与 $n$ 互素, $\xi$ 是 $n$ 次本原单位根, $E$ 是 $f(x) = x^n - 1$ 在 $F$ 上的分裂域. 则
> $$\operatorname{Gal}(f(x), F) = \begin{cases} (\mathbb{Z}_n)^*, & \xi \notin F, \\ \{1\}, & \xi \in F, \end{cases}$$
> 其中 $(\mathbb{Z}_n)^*$ 是 $\mathbb{Z}_n$ 的单位群.


> [!question]- 4.2.8
> 设 $n \geqslant 2$ 是正整数, 域 $F$ 的特征为零或与 $n$ 互素, $\xi$ 是 $n$ 次本原单位根且 $\xi \in F$, $E$ 是 $f(x) = x^n - a \in F[x]$ 在 $F$ 上的分裂域. 则 $\operatorname{Gal}(f(x), F)$ 是循环群; 且当 $f(x)$ 在 $F$ 上不可约时, $\operatorname{Gal}(f(x), F)$ 是 $n$ 阶循环群.


> [!question]- 4.2.9*
> 设 $p^n$ ($p$ 为素数, $n \geqslant 1$) 次 Galois 扩张 $E/F$ 的 Galois 群 $\operatorname{Gal}(E/F)$ 是 $p^n$ 阶循环群, $L$ 是 $E/F$ 的中间域且 $[E : L] = p$. 若 $E = L(u)$, 则 $E = F(u)$.


> [!question]- 4.2.10*
> 设 $E/F$ 是有限次 Galois 扩张, 其 Galois 群 $\operatorname{Gal}(E/F)$ 含有最小子群 $A$, $L = \operatorname{Inv}(A)$. 若 $E = L(u)$, 则 $E = F(u)$.


> [!question]- 4.2.11
> 任一有限群均是某个域上可分多项式的 Galois 群.


## §3 方程的根式可解性

> [!question]- 4.3.1*
> 设 $p$ 次 Galois 扩张 $E/F$ 的 Galois 群 $\operatorname{Gal}(E/F)$ 是 $p$ 阶循环群 ($p$ 为素数), 且 $F$ 含有 $p$ 次本原单位根 $\xi$. 则存在 $d \in E$ 使得 $E = F(d)$, $d^p \in F$. 故 $E/F$ 是根式扩张.


> [!question]- 4.3.2*
> 设域 $F$ 的特征为零, $E$ 是 $F$ 上正次数多项式 $f(x)$ 在 $F$ 上的分裂域. 若 $\operatorname{Gal}(E/F)$ 是可解群, 则 $f(x) = 0$ 在 $F$ 上根式可解.


> [!question]- 4.3.3*
> 设 $F$ 是任意特征的域, $E/F$ 是有限可分扩张. 若 $E/F$ 有根式扩张链, 则存在 $E$ 的有限扩域 $N$, 使得 $N/F$ 是有限正规扩张, 且 $N/F$ 也有根式扩张链.


> [!question]- 4.3.4*
> 设域 $F$ 的特征为零, $E$ 是 $F$ 上正次数多项式 $f(x)$ 在 $F$ 上的分裂域. 若 $f(x) = 0$ 在 $F$ 上根式可解, 则 $\operatorname{Gal}(E/F)$ 是可解群.
