---
tags:
  - Algebra
  - Groups
---
# Product Groups

令 $G,G'$ 为两个群，其乘积群 $G\times G'$ 元素记为 $(a,a')$ , 其中 $a\in G$ and $a'\in G'$ . 这个乘积群可以通过分量乘法 (component-wise mupltiplication) 来令其构成一个新的群——我们对这二元对的乘法记为： 
$$(a,a')\cdot(b,b')=(ab,a'b')$$
对 $(1,1)$ 是单位元，$(a,a^{\prime})$ 的逆是 $(a^{- 1},a^{\prime - 1})$。$G\times G^{\prime}$ 中的结合律由它在 $G$ 和 $G^{\prime}$ 中成立推出。

这样得到的群称为 $G$ 和 $G^{\prime}$ 的**乘积**，记为 $G\times G^{\prime}$。它通过一些同态以简单的方式与两个因子 $G$ 和 $G^{\prime}$ 相关联。

```tikz
\usepackage{tikz-cd}

\begin{document}
\begin{tikzcd}
     G \arrow[dr, "i"]& & G \\
      & G \times G  \arrow[ur, "p"]  \arrow[dr, "p'"] & \\
    G' \arrow[ur, "i'"'] & & G'
\end{tikzcd}
\end{document}
```


它们由 $i(x) = (x,1)$，$i^{\prime}(x^{\prime}) = (1,x^{\prime})$，$p(x,x^{\prime}) = x$，$p^{\prime}(x,x^{\prime}) = x^{\prime}$ 定义。单射同态 $i$ 和 $i^{\prime}$ 可用于将 $G$ 和 $G^{\prime}$ 等同于它们的像，即 $G\times G^{\prime}$ 的子群 $G\times 1$ 和 $1\times G^{\prime}$ ，此为 **嵌入** 。映射 $p$ 和 $p^{\prime}$ 是满射的，$p$ 的核是 $1\times G^{\prime}$，$p^{\prime}$ 的核是 $G\times 1$, 此为 **投影** (Projection)。

将给定的群 $G$ 分解为乘积是可取的，即找到群 $H$ 和 $H^{\prime}$，使得 $G$ 同构于乘积 $H\times H^{\prime}$。群 $H$ 和 $H^{\prime}$ 会更简单，并且 $H\times H^{\prime}$ 与其因子的关系很容易理解。


> [!example] EXAMPLE
> 一个 6 阶循环群 $C_{6}$ 同构于 2 阶和 3 阶循环群的乘积 $C_{2}\times C_{3}$。为了看到这一点，设 $C_{2} = \langle y\rangle$ 且 $C_{3} = \langle z\rangle$，其中 $y^{2} = 1$，$z^{3} = 1$，并令 $x$ 表示乘积群 $C_{2}\times C_{3}$ 中的元素 $(y,z)$。使得 $x^{k} = (y^{k},z^{k})$ 为单位元 $(1,1)$ 的最小正整数 $k$ 是 $k = 6$。所以 $x$ 的阶为 6。由于 $C_{2}\times C_{3}$ 的阶也是 6，它等于由 $x$ 生成的循环群 $\langle x\rangle$。$x$ 的幂依次为
$$(1,1),(y,z),(1,z^{2}),(y,1),(1,z),(y,z^{2}).$$

这个例子告诉我们


> [!important] Propostion.5.1
> 设 $r$ 和 $s$ 是 **互素** 的整数。一个 $r s$ 阶循环群同构于一个 $r$ 阶循环群和一个 $s$ 阶循环群的乘积。

这个命题是显然的


> [!important] Proposition.5.2
> 设 $H$ 和 $K$ 是群 $G$ 的子群，并设 $f\colon H\times K\to G$ 是乘法映射，定义为 $f(h,k) = hk$。它的像是集合 $H K = \{h k\mid h\in H,k\in K\}$。
>1. $f$ 是单射当且仅当 $H\cap K = \{1\}$。
>2.  $f$ 是从乘积群 $H\times K$ 到 $G$ 的同态当且仅当 $K$ 中的元素与 $H$ 中的元素交换：$hk = kh$。
>3.  如果 $H$ 是 $G$ 的一个正规子群，那么 $HK$ 是 $G$ 的一个子群。
>4.  $f$ 是从乘积群 $H\times K$ 到 $G$ 的同构当且仅当 $H\cap K = \{1\}$，$HK = G$，并且 $H$ 和 $K$ 是 $G$ 的正规子群。

! 注意，乘法映射可能是双射的，尽管它不是群同态。例如，当 $G = S_{3}$ 时，用常用记号，$H = \langle x\rangle$ 和 $K = \langle y\rangle$，就会发生这种情况。

**Proof.** 

1.  如果 $H\cap K$ 包含一个元素 $x\neq 1$，那么 $x^{- 1}$ 在 $H$ 中，并且 $f(x^{- 1},x) = 1 = f(1,1)$，所以 $f$ 不是单射。假设 $H\cap K = \{1\}$。设 $(h_{1},k_{1})$ 和 $(h_{2},k_{2})$ 是 $H\times K$ 中的元素，使得 $h_{1}k_{1} = h_{2}k_{2}$。我们在该等式左边乘以 $h_{1}^{- 1}$，右边乘以 $k_{2}^{- 1}$，得到 $k_{1}k_{2}^{- 1} = h_{1}^{- 1}h_{2}$。左边是 $K$ 的元素，右边是 $H$ 的元素。由于 $H\cap K = \{1\}$，$k_{1}k_{2}^{- 1} = h_{1}^{- 1}h_{2} = 1$。那么 $k_{1} = k_{2}$，$h_{1} = h_{2}$，且 $(h_{1},k_{1}) = (h_{2},k_{2})$。
2.  设 $(h_{1},k_{1})$ 和 $(h_{2},k_{2})$ 是乘积群 $H\times K$ 中的元素。这些元素在乘积群 $H\times K$ 中的乘积是 $(h_{1}h_{2},k_{1}k_{2})$，而 $f(h_{1}h_{2},k_{1}k_{2}) = h_{1}h_{2}k_{1}k_{2}$，同时 $f(h_{1},k_{1})f(h_{2},k_{2}) = h_{1}k_{1}h_{2}k_{2}$。这两个元素相等当且仅当 $h_{2}k_{1} = k_{1}h_{2}$。
3. 假设 $H$ 是一个正规子群。我们注意到 $KH$ 是左陪集 $kH$ 的并集，其中 $k$ 在 $K$ 中，而 $HK$ 是右陪集 $Hk$ 的并集。由于 $H$ 是正规的，$kH = Hk$，因此 $HK = KH$。$HK$ 在乘法下的封闭性随之而来，因为 $HKHK = HHKK = HK$。此外，$(hk)^{- 1} = k^{- 1}h^{- 1}$ 在 $KH = HK$ 中。这证明了 $HK$ 对逆元的封闭性。
4. 假设 $H$ 和 $K$ 满足给定的条件。那么 $f$ 既是单射又是满射，所以它是双射。根据 (b)，它是一个同构当且仅当对于所有 $h$ 在 $H$ 中，$k$ 在 $K$ 中，有 $hk = kh$。考虑换位子 $(hkh^{-1})k^{-1} = h(kh^{-1}k^{-1})$。由于 $K$ 是正规的，左边在 $K$ 中，由于 $H$ 是正规的，右边在 $H$ 中。由于 $H\cap K = \{1\}$，$hkh^{-1}k^{-1} = 1$，且 $hk = kh$。反之，如果 $f$ 是一个同构，可以在同构的群 $H\times K$ 中验证列出的条件，而不是在 $G$ 中验证。

We use this propostion to classify groups of order 4:


> [!Important] Proposition.5.3
> 有两个 4 阶群的同构类，即 4 阶循环群 $C_4$ 的类和克莱因四元群的类，后者同构于两个 2 阶群的乘积 $C_2 \times C_2$。

**Proof.** 设 $G$ 是一个 4 阶群。$G$ 中任何元素 $x$ 的阶整除 4，所以需要考虑两种情况 :

1. $G$ contains an element of order 4. Then $G$ is a cyclic group of order 4.
2. Every element of $G$ except the identity has order 2.

在这种情况下，对于 $G$ 的每个元素 $x$，有 $x = x^{- 1}$。设 $x$ 和 $y$ 是 $G$ 的两个元素。那么 $xy$ 的阶为 2，所以 $xyx^{- 1}y^{- 1} = (xy)(xy) = 1$。这表明 $x$ 和 $y$ 交换 <>，并且由于这些是任意元素，$G$ 是阿贝尔的。所以每个子群都是正规的。我们在 $G$ 中选择两个不同的元素 $x$ 和 $y$，并让 $H$ 和 $K$ 分别是由它们生成的 2 阶循环群。命题 <> 表明 $G$ 同构于乘积群 $H \times K$。

# Quotient Groups

> 这里我们想到了此前的模运算，我们用 $\mathbb{Z}/n\mathbb{Z}$ 的方式来表示模的同余类集合。这个表示方法和我们后面见到的好像啊（或者说就是同种东西吧！就是一个例子！）

**主要任务**：任何群 $G$ 的正规子群 $N$ 的陪集集合上定义一个合成律。这个合成律将正规子群的陪集集合构成一个群，称为**商群**。
> [!ABSTRACT]  Definition.5.1
> 群 $G$ 的正规子群 $N$ 的陪集集合通常记为 $G / N$。
> 当我们把一个陪集 $C$ 视为陪集集合中的一个元素时，可以使用括号记号 $[C]$。如果 $C = aN$，我们也可以使用横线记号将元素 $[C]$ 记为 $\overline{a}$，那么我们将陪集集合记为 $\overline{G}$： 
>$$\overline{G} = G / N$$

> [!NOTE] Thorem.5.1
> 设 $N$ 是群 $G$ 的一个正规子群，并设 $\overline{G}$ 表示 $N$ 在 $G$ 中的陪集的集合。在 $\overline{G}$ 上存在一个合成律，使该集合成为一个群，并且由 $\pi (a) = \overline{a}$ 定义的映射 $\pi :G \to \overline{G}$ 是一个满射同态，其核为 $N$
> - 映射 $\pi$ 通常称为从 $G$ 到 $\overline{G}$ 的**典范映射**。“典范”一词表明这是我们可能合理讨论的唯一映射。

**Proof.** 首先，我们定义合成律：如果 $A$ 和 $B$ 是群 $G$ 的子集，那么 $AB$ 表示乘积 $ab$ 的集合：
$$AB = \{x\in G\mid x = ab\text{ 对于某个 }a\in A\text{ 和 }b\in B\} .$$

> [!success] Lemma.5.1.1
> 设 $N$ 是群 $G$ 的一个正规子群，并设 $aN$ 和 $bN$ 是 $N$ 的陪集。乘积集 $(aN)(bN)$ 也是一个陪集。它等于陪集 $abN$。

注意到 , 集合 $(aN)(bN)$ 由 $G$ 中所有可以写成 $anbn'$ 形式的元素组成，其中 $n$ 和 $n'$ 在 $N$ 中。
**Proof.1** 由于 $N$ 是一个子群，$NN = N$。由于 $N$ 是正规的，左陪集和右陪集相等：$Nb = bN$ (2.8.17)。该引理通过以下形式推导得到证明： 
$$(aN)(bN) = a(Nb)N = a(bN)N = abNN = abN.$$
我们在集合 $\overline{G} = G / N$ 上定义乘法。使用括号记号 (2.7.8)，定义如下：如果 $C_1$ 和 $C_2$ 是陪集，那么 $[C_1][C_2] = [C_1C_2]$。其中 $C_1C_2$ 是乘积集。引理表明这个乘积集是另一个陪集。为了计算乘积 $[C_1][C_2]$，取 $C_1$ 中的任意元素 $a$ 和 $C_2$ 中的任意元素 $b$。那么 $C_1 = aN$，$C_2 = bN$，并且 $C_1C_2$ 是包含 $ab$ 的陪集 $abN$。所以我们得到了非常自然的公式 
$$[aN][bN] = [abN]\quad \text{或}\quad \bar{a}\bar{b} = \overline{ab}$$
于是有 
$$\pi (a)\pi (b) = \bar{a}\bar{b} = \overline{ab} = \pi (ab)$$
一旦我们证明了 $\overline{G}$ 是一个群，$\pi$ 是一个同态这一事实将紧随 (2.12.7) 得出。由于典范映射 $\pi$ 是满射的 (2.7.8)，下一个引理证明了这一点。

> [!success] Lemma.5.1.2
> 设 $G$ 是一个群，$Y$ 是一个具有合成律的集合，两个律都用乘法记号书写。设 $\varphi :G\to Y$ 是一个具有同态性质的满射映射，即对于 $G$ 中所有 $a$ 和 $b$，有 $\varphi (ab) = \varphi (a)\varphi (b)$。那么 $Y$ 是一个群，且 $\varphi$ 是一个同态。

**Proof.2** $G$ 中成立的群公理通过满射映射 $\varphi$ 传递到 $Y$。以下是结合律的证明：设 $y_{1},y_{2},y_{3}$ 是 $Y$ 中的元素。由于 $\varphi$ 是满射，对于 $G$ 中的某些 $x_{i}$，有 $y_{i} = \varphi (x_{i})$。那么
$$(y_{1}y_{2})y_{3} = (\varphi (x_{1})\varphi (x_{2}))\varphi (x_{3}) = \varphi (x_{1}x_{2})\varphi (x_{3}) = \varphi ((x_{1}x_{2})x_{3})$$
$$\qquad \overset{*}{=} \phi (x_{1}(x_{2}x_{3})) = \phi (x_{1})\phi (x_{2}x_{3}) = \phi (x_{1})(\phi (x_{2})\phi (x_{3})) = y_{1}(y_{2}y_{3}).$$
标有星号的等式是 $G$ 中的结合律。其他等式由 $\varphi$ 的同态性质推出。其他群公理的验证类似。


这里我们验证子群 $N$ 是映射 $\pi$ 的核 $\pi (a) = \pi (1)$ 当且仅当 $\overline{a} = \overline{1}$，或 $[aN] = [1N]$，而这成立当且仅当 $a$ 是 $N$ 的一个元素。

![[Pasted image 20260415173729.png]]

> 我们假设 $N$ 是 $G$ 的正规子群对引理 2.12.5 至关重要。如果 $H$ 不是正规的，则存在 $H$ 在 $G$ 中的左陪集 $C_{1}$ 和 $C_{2}$，使得乘积集 $C_{1}C_{2}$ 不包含在单个左陪集中。再次回到 $S_{3}$ 的子群 $H = \langle y\rangle$，乘积集 $(1H)(xH)$ 包含四个元素：$\{1,y\} \{x,xy\} = \{x,xy,x^{2}y,x^{2}\}$。它不是一个陪集。子群 $H$ 不是正规的。

> [!danger] Corollary.5.1
> 设 $N$ 是群 $G$ 的一个正规子群，并设 $\overline{G}$ 表示 $N$ 在 $G$ 中的陪集的集合。设 $\pi :G \to \overline{G}$ 是典范同态。设 $a_{1}, \ldots , a_{k}$ 是 $G$ 中的元素，使得乘积 $a_{1} \cdots a_{k}$ 在 $N$ 中。那么 $\overline{a_{1}} \cdots \overline{a_{k}} = \overline{1}$。

**Proof.** 设 $p = a_{1} \cdots a_{k}$。那么 $p$ 在 $N$ 中，所以 $\pi (p) = \overline{p} = \overline{1}$。由于 $\pi$ 是一个同态，$\overline{a_{1}} \cdots \overline{a_{k}} = \overline{p}$。这是易证的。

> [!NOTE] Theorem **First Isomorphism Theorem**
> 设 $\varphi :G\to G^{\prime}$ 是一个满射群同态，其核为 $N$。商群 $\overline{G} = G / N$ 同构于像 $G^{\prime}$。准确地说，设 $\pi :G\to \overline{G}$ 是典范映射。存在唯一的同构 $\overline{\varphi} :\overline{G}\to G^{\prime}$，使得 $\varphi = \overline{\varphi}\circ \pi$

**Proof.**  $\overline{G}$ 的元素是 $N$ 的陪集，它们也是映射 $\phi$ 的 **纤维** 。定理中提到的映射 $\overline{\varphi}$ 是将非空纤维送到其像的映射：$\overline{\varphi} (\overline{x}) = \varphi (x)$。对于任何满射集合映射 $\varphi :G \to G'$，我们可以构造纤维的集合 $\overline{G}$，然后得到如上图，其中 $\overline{\varphi}$ 是将纤维送到其像的双射映射。当 $\varphi$ 是一个群同态时，$\overline{\varphi}$ 是一个同构，因为 $\overline{\varphi} (ab) = \varphi (ab) = \varphi (a)\varphi (b) = \overline{\varphi} (\overline{a})\overline{\varphi} (\overline{b})$。

```tikz

```
```tikz
\usepackage{tikz-cd}

\begin{document}
\begin{tikzcd}
G \arrow[rr,"\varphi"]\arrow[dr,"\pi"] && G'\\
& \bar{G} \arrow[ur,"\bar{\varphi}"',dashed]
\end{tikzcd}
\end{document}
```

> [!Danger] Corollary.5.2
> 设 $\phi :G \to G'$ 是一个群同态，其核为 $N$，像为 $H'$。商群 $\overline{G} = G / N$ 同构于像 $H'$。

> [!Example] EXAMPLE
> 绝对值映射 $\mathbb{C}^{\times} \to \mathbb{R}^{\times}$ 的像是正实数群，其核是单位圆 $U$。该定理断言商群 $\mathbb{C}^{\times} / U$ 同构于正实数的乘法群。行列式是一个满射同态 $G L_{n}(\mathbb{R}) \to \mathbb{R}^{\times}$，其核是特殊线性群 $S L_{n}(\mathbb{R})$。所以商群 $G L_{n}(\mathbb{R}) / S L_{n}(\mathbb{R})$ 同构于 $\mathbb{R}^{\times}$

===EXERCISES===
---