---
tags:
  - Algebra
  - Groups
---
> **问题引入** : 此前我们的 **Lagrange Theorem** 指出：子群的阶必然整除群的阶 。如果我们反过来想，这是不一定成立的。比如我举交错群 $A_{4}$ , 其阶为 $12$ 但是我们如果想找它的一个 $6$ 阶子群这是不可能的。

其指数 $[G:H]$ 为 $2$ 意味着其必须为正规子群，而 $A_{4}$ 的正规子群只可能是其平凡子群以及 $V_{4}$ 。我们可以用反证法来证明：

**Proof.** 假设 $H$ 是 $A_{4}$ 一个阶为 $6$ 的子群，我们可以知到 $6$ 阶群群只有循环群 $C_{3}$ 和置换群 $S_{3}$ （我们可以用 **Cauchy Theorem** 得到）
显然不可能是 $C_{6}$ ,那么唯一的可能就是 $S_{3}$ . $S_{3}$ 的结构是 : 一个单位元，三个二阶元，两个三阶元。
我们首先往子群中引入二阶元，恰好有三个 $(12)(34)$ , $(13)(24)$ ,  $(14),(23)$ .
当我们向其中引入三阶元的时候就出现了问题，当我们引入 $(1,2,3)$ 的时候（我们就记为 $\sigma$）由于有克莱因四元群 $V_{4}$ 的存在，我们一旦引入一个三循环就生成了整个 $A_{4}$ 那就是说明 $A_{4}\subset H$ 。
这是显然矛盾的，于是六阶群不存在。

> Sylow Theorem 将帮助我们更好得了解群的结构。对于解决我们上述的问题或将提供更加简洁的思路。

> 稍微了解一下 **Sylow** 的生平：1832年出生在挪威的克里斯蒂安尼亚。在1858年大学毕业之后就职于弗雷德克利沙尔的一所中学中，他在1862年去得克里斯蒂安尼亚大学的临时教职，但其后36年仍然是中学教师的身份（未能获得终身教职）进行数学研究。可是牢笼岂能关住自由的鸟儿？1872年 **Sylow** 在《数学年刊 ***Mathematische Annalen*** （注意德语）》上发表《关于置换群的定理》。至此 **Sylow Theorem** 正式发表。在他 66 岁时候终于取得了大学教职，20年后在奥斯陆逝世。

> [!ABSTRACT] Definition： Sylow-p Subgroups
> 令群 $G$ 的阶为 $n$ , 令 $p$ 为一个整除 $n$ 的素整数 . 让 $p^e$ 为一个最大整除 $n$ 的数。于是我们有 
> $$n=p^e m$$
> 这里的 $m$ 为不被 $p$ 整除的整数。群 $G$ 阶为 $p^e$ 的子群就称之为群 $G$ 的 **Sylow p-Subgroup** . 显然其指数不被 $p$ 整除

### 存在性
> [!NOTE] Theorem.1 First Sylow Theorem
>  $n$ 阶有限群若其阶被素数 $p$ 整除则群包含 $Sylow\ p-subgroup$

当我们遇到一个群 $|G|=12$ 我们怎样找他的 Sylow p-subgroups ?
我们可以尝试对这个阶数进行分解 $12=2^2\times 3$ 以及 $12=3\times 4$ .我们想要一个阶为 $4$ 的群使其为为 p-sylow subgroup 。这个定理便是说明满足这个条件的子群是存在的。我们可以尝试先找一下这个子群。

> [!Example] EXAMPLE：$A_{4}$ 依旧是这个例子
> 我们的克莱因四元群 $V_{4}$ 加上单位元自然就满足这个条件了 $\{ e,(12)(34),(13)(24),(14)(23) \}$ . 第一希罗定理就是要说明这个事情的一般性

 为了优雅得证明 Sylow First Theorem, 我们需要一些引理：
 
> [!Success] Lemma.1.1
>  $U$ 是群 $G$ 的一个子集。在群 $G$ 通过左乘作用在其全体子集构成的集合上时，子集 $[U]$ 的稳定子 $\mathrm{Stab}([U])$ 的阶同时整除 $|U|$ 与 $|G|$。

**Proof.** 若 $H$ 是群 $G$ 的子群，那么 $G$ 中元素 $u$ 在 $H$ 的左乘作用下的 $H-orbit$ 即为右陪集 $Hu$ . 令 $H$ 为 $[U]$ 的稳定子。此时 $H$ 的左乘作用将 $U$ 中的元素进行置换，因而 $U$ 被划分为若干个 $H-orbit$ ，这些轨道都是右陪集。每个陪集的元素均为 $|H|$, 故 $|H|$ 整除 $|U|$ . 又因为 $H$ 是 $G$ 的子群，由 Lagrange Theorem 可知 $|H|$ 也整除 $|G|$。

> [!Success] Lemma.1.2
> 令 $n$ 为 $p^em$ 中的一个整数。当 $e>0$ 且 $p$ 不整除 $m$. 从一个含 $n$ 个元素的集合中，选取含 $p^e$ 个元素的子群，其个数 $N$ 不能被 $p$ 整除

**Proof.** 数字 $N$ 是一个二项式系数 
$$\begin{pmatrix}
n \\
p^e
\end{pmatrix}=\frac{n(n-1)\cdots(n-k)\cdots(n-p^e+1)}{p^e(p^e-1)\cdots (p^e-k)\cdots1}$$
若将 $k$ 写成 $k=p^ia$ 的形式，分子中每一项 $(n-k)$ 被 $p$ 整除时，分母中对应的项 $(p^e-k)$ 也会被 $p$ 整除相同的系数, 其必有 $i<e$ . 因此 $(p^e-k)$ 与 $(n-k)=(p^em-k)$ 恰好能被 $p^i$ 整除而不能被 $p^{i+1}$ 整除。
 
结合这两个引理，我们开始对 $\text{First Sylow Theorem}$ 证明：

> [!Info] Proof of the First Sylow Theorem

令 $\mathcal{S}$ 是群 $G$ 所有阶为 $p^e$ 的子群的集合，其中一个子群为 Sylow p-Subgroup . 我们将群 $G$ 左乘作用在集合 $\mathcal{S}$ 上，其中一个子群 $[U]$ 是阶为 $p^e$ 的稳定子 —— 这就是我们要找的那个子群

我们将 $\mathcal{S}$ 通过左乘作用的轨道进行分解，可以得到形如 : 
$$N=|S|=\sum_{orbits~O}|O|$$
的式子，依据 $lemma.1.2$ 我们可以知道 $p$ 不整除 $N$ , 则至少有一个轨道的大小不被 $p$ 整除，我们记子集 $[U]$ 的轨道为 $\mathcal{O}_{[U]}$ ，令 $H$ 为 $[U]$ 的稳定子。再依据 $lemma.1.1$ 我们知道 $H$ 整除 $U$ 的元素个数为 $p^e$ —— $H$ 是 $p$ 的幂。由轨道-稳定子定理可知 $|H|\cdot |\mathcal{O}_{[U]}|=G=p^em$ , 其中 $|\mathcal{O}_{[U]}|$ 必然是 $m$ . 那么 $H$ 是 $sylow \text{ p-subgroup}$ 是 Trivial 的。

> [!Danger] Corollary.1.3 Cauchy Theorem
> 若有限群的阶能被素数 $p$ 整除，则该群中必含有一个 $p$ 阶元

这个说是 Theorem.1 的推论，但是实际上还是我们的 Cauchy Theorem ，甚至是期中考的题目。我们必然可以不通过 Sylow Theorem 来证明。相反我们可以尝试用这条引理来推出 Sylow Theorem.


## 共轭性

在讨论第二 Sylow 定理之前，先引入正规化子。

> [!ABSTRACT] Definition：Normalizer
> 设 $H\leq G$。定义 $H$ 在 $G$ 中的正规化子为
> $$
> N_G(H)=\{g\in G:gHg^{-1}=H\}.
> $$
> 容易验证
> $$
> H\leq N_G(H)\leq G.
> $$
> 并且
> $$
> H\triangleleft N_G(H).
> $$

---

> [!NOTE] Theorem 2：Second Sylow Theorem
> 设 $G$ 为有限群，$p$ 为素数。
>
> 1. 若 $P$ 是 $G$ 的一个 Sylow $p$-subgroup，$Q$ 是 $G$ 的任意 $p$-subgroup，则存在 $g\in G$，使得
> $$
> g^{-1}Qg\leq P.
> $$
>
> 2. 特别地，$G$ 的任意两个 Sylow $p$-subgroup 彼此共轭。  
> 即若 $P_1,P_2\in\operatorname{Syl}_p(G)$，则存在 $g\in G$，使得
> $$
> P_2=gP_1g^{-1}.
> $$

---

> [!Info] Proof of the Second Sylow Theorem

设 $P$ 是 $G$ 的一个 Sylow $p$-subgroup。令 $Q$ 是 $G$ 的任意 $p$-subgroup。

考虑 $Q$ 在左陪集空间 $G/P$ 上的左乘作用：

$$
q\cdot gP=qgP,
$$

其中 $q\in Q$，$gP\in G/P$。

陪集空间的元素个数为

$$
|G/P|=[G:P].
$$

由于 $P$ 是 Sylow $p$-subgroup，设

$$
|G|=p^e m,\qquad |P|=p^e,
$$

则

$$
[G:P]=m,
$$

且

$$
p\nmid m.
$$

$Q$ 是 $p$-群，因此 $Q$ 在 $G/P$ 上的每个轨道大小都是 $p$ 的幂。

由于所有轨道大小之和为 $m$，而 $m$ 不被 $p$ 整除，所以至少有一个轨道的大小不被 $p$ 整除。

但轨道大小又是 $p$ 的幂，因此这个轨道的大小只能是 $1$。

于是存在某个陪集 $gP$，使得它被 $Q$ 中所有元素固定：

$$
qgP=gP,\qquad \forall q\in Q.
$$

这意味着

$$
g^{-1}qg\in P,\qquad \forall q\in Q.
$$

因此

$$
g^{-1}Qg\leq P.
$$

这证明了第一条。

若 $Q$ 也是 Sylow $p$-subgroup，则

$$
|Q|=|P|=p^e.
$$

又因为

$$
g^{-1}Qg\leq P,
$$

两边阶数相同，所以

$$
g^{-1}Qg=P.
$$

即

$$
Q=gPg^{-1}.
$$

因此任意两个 Sylow $p$-subgroup 共轭。$\square$

---

> [!summary] 第二 Sylow 定理的意义
> 所有 Sylow $p$-subgroup 构成一个共轭类。  
> 因此，研究其中一个 Sylow $p$-subgroup，往往就可以研究所有同类子群。

---

## 数量

> [!NOTE] Theorem 3：Third Sylow Theorem
> 设
> $$
> |G|=p^e m,
> $$
> 其中 $p\nmid m$。令
> $$
> n_p=|\operatorname{Syl}_p(G)|
> $$
> 表示 $G$ 的 Sylow $p$-subgroup 的个数。则：
>
> 1. 
> $$
> n_p\equiv 1\pmod p;
> $$
>
> 2. 
> $$
> n_p\mid m;
> $$
>
> 3. 对任意 Sylow $p$-subgroup $P$，有
> $$
> n_p=[G:N_G(P)].
> $$
>
> 4. 
> $$
> n_p=1
> $$
> 当且仅当 $G$ 的 Sylow $p$-subgroup 是正规子群。

---

> [!Info] Proof of the Third Sylow Theorem

令

$$
X=\operatorname{Syl}_p(G).
$$

群 $G$ 通过共轭作用作用于 $X$：

$$
g\cdot P=gPg^{-1}.
$$

由第二 Sylow 定理，所有 Sylow $p$-subgroup 彼此共轭，因此这个作用是传递的。

取定 $P\in X$。其稳定子为

$$
\operatorname{Stab}_G(P)=N_G(P).
$$

由轨道-稳定子定理，

$$
n_p=|X|=[G:N_G(P)].
$$

这证明了第三条。

由于

$$
P\leq N_G(P)\leq G,
$$

设

$$
|N_G(P)|=p^e r,
$$

其中 $r\mid m$。于是

$$
n_p=[G:N_G(P)]
=
\frac{p^e m}{p^e r}
=
\frac{m}{r}.
$$

因此

$$
n_p\mid m.
$$

这证明了第二条。

下面证明

$$
n_p\equiv 1\pmod p.
$$

令 $P$ 通过共轭作用作用于 $X=\operatorname{Syl}_p(G)$：

$$
p_0\cdot Q=p_0Qp_0^{-1},
$$

其中 $p_0\in P$，$Q\in X$。

由于 $P$ 是 $p$-群，所以每个轨道的大小都是 $p$ 的幂。

我们考察这个作用的固定点。

若 $Q\in X$ 是固定点，则对所有 $p_0\in P$，都有

$$
p_0Qp_0^{-1}=Q.
$$

也就是说

$$
P\leq N_G(Q).
$$

注意：

- $Q$ 是 $G$ 的 Sylow $p$-subgroup；
- 因此 $Q$ 也是 $N_G(Q)$ 的 Sylow $p$-subgroup；
- 并且由正规化子定义，
$$
Q\triangleleft N_G(Q).
$$

现在 $P\leq N_G(Q)$，且 $P$ 的阶也是 $p^e$，所以 $P$ 也是 $N_G(Q)$ 的 Sylow $p$-subgroup。

由于 $Q\triangleleft N_G(Q)$，$Q$ 是 $N_G(Q)$ 中唯一的 Sylow $p$-subgroup。于是

$$
P=Q.
$$

因此，在 $P$ 对 $X$ 的共轭作用下，唯一的固定点就是 $P$ 本身。

于是轨道分解为：

$$
X=\{P\}\cup\text{若干个大小被 }p\text{ 整除的轨道}.
$$

所以

$$
n_p=|X|\equiv 1\pmod p.
$$

这证明了第一条。

最后，若

$$
n_p=1,
$$

则 Sylow $p$-subgroup 唯一。由于共轭子群仍然是 Sylow $p$-subgroup，所以它在共轭作用下不变，故为正规子群。

反过来，若某个 Sylow $p$-subgroup $P$ 正规，则对所有 $g\in G$，

$$
gPg^{-1}=P.
$$

由第二 Sylow 定理，所有 Sylow $p$-subgroup 都是 $P$ 的共轭，因此只能有 $P$ 一个。

所以

$$
n_p=1
$$

当且仅当 Sylow $p$-subgroup 正规。$\square$

---

> [!summary] Third Sylow Theorem 的核心
> 若
> $$
> |G|=p^e m,\qquad p\nmid m,
> $$
> 且 $n_p$ 是 Sylow $p$-subgroup 的个数，则
> $$
> n_p\equiv 1\pmod p,
> $$
> $$
> n_p\mid m.
> $$
> 这两个条件常常足以限制群的结构。

---

## 应用：回到 $A_4$ 为什么没有 $6$ 阶子群

我们现在用 Sylow 定理重新看一开始的问题。

已知

$$
|A_4|=12=2^2\cdot 3.
$$

设 $n_3$ 为 $A_4$ 中 Sylow $3$-subgroup 的个数。

由第三 Sylow 定理，

$$
n_3\equiv 1\pmod 3,
$$

并且

$$
n_3\mid 4.
$$

因此

$$
n_3=1\quad\text{或}\quad n_3=4.
$$

另一方面，$A_4$ 中有 $8$ 个三循环。每个 $3$ 阶子群包含恰好 $2$ 个非单位的三循环，因此

$$
n_3=\frac{8}{2}=4.
$$

所以

$$
n_3=4.
$$

现在假设存在 $H\leq A_4$，且

$$
|H|=6.
$$

则

$$
[A_4:H]=2,
$$

所以

$$
H\triangleleft A_4.
$$

在 $H$ 中考虑 Sylow $3$-subgroup。因为

$$
|H|=6=2\cdot 3,
$$

由第三 Sylow 定理，$H$ 中 $3$-Sylow subgroup 的个数 $n_3(H)$ 满足

$$
n_3(H)\equiv 1\pmod 3,
$$

且

$$
n_3(H)\mid 2.
$$

因此

$$
n_3(H)=1.
$$

设 $P$ 是 $H$ 中唯一的 $3$ 阶子群。于是

$$
P\triangleleft H.
$$

又因为 $H\triangleleft A_4$，对任意 $g\in A_4$，有

$$
gHg^{-1}=H.
$$

因此

$$
gPg^{-1}\leq gHg^{-1}=H.
$$

而 $gPg^{-1}$ 仍然是一个 $3$ 阶子群。由于 $H$ 中 $3$ 阶子群唯一，所以

$$
gPg^{-1}=P.
$$

这说明

$$
P\triangleleft A_4.
$$

但这意味着 $A_4$ 中只有一个 Sylow $3$-subgroup，即

$$
n_3=1,
$$

与我们前面得到的

$$
n_3=4
$$

矛盾。

因此，$A_4$ 中不存在 $6$ 阶子群。$\square$

---

> [!IMPORTANT] 本笔记核心结论
> 设
> $$
> |G|=p^e m,\qquad p\nmid m.
> $$
>
> 1. **存在性**：$G$ 中存在阶为 $p^e$ 的子群，即 Sylow $p$-subgroup。
> 2. **共轭性**：所有 Sylow $p$-subgroup 彼此共轭。
> 3. **数量**：若 $n_p$ 为 Sylow $p$-subgroup 的个数，则
> $$
> n_p\equiv 1\pmod p,
> $$
> $$
> n_p\mid m.
> $$
> 4. 
> $$
> n_p=1
> $$
> 当且仅当 Sylow $p$-subgroup 是正规子群。