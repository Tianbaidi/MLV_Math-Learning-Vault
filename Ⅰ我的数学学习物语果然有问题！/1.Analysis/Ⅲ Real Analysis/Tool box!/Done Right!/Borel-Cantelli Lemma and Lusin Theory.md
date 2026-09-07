---
tags:
  - Real_analysis
  - Measure_Theorem
  - Borel_Cantelli_Lemma
---
> 这个引理来自 Stein.Real Analysis 的课后习题. 考虑到和 Lusin Theory 之间有所联系，就将其放在一起写。我们Lusin Teory 在 [[Simple Function and Step Function%Littlewood's Three Principles]] 里面就有存在。

# Reference
> [!NOTE] Theorem (Lusin)
> 假设 $f$ 是定义在有限测度集 $E$ 上的可测函数，且在 $E$ 上取有限值。那么对于任意的 $\epsilon > 0$，存在一个闭集 $F_\epsilon$，满足：
> $$F_\epsilon \subset E, \quad \text{and} \quad m(E - F_\epsilon) \leq \epsilon$$
> 并且使得限制函数 $f|_{F_\epsilon}$ 是连续的。我们用 $f|_{F_\epsilon}$ 表示将函数 $f$ 的定义域限制在集合 $F_\epsilon$ 上。

**Proof.** 令 $\{f_n\}$ 为一列阶梯函数，使得 $f_n \to f$ 几乎处处（a.e.）成立。然后我们可以找到集合 $E_n$，使得 $m(E_n) < 1/2^n$，并且 $f_n$ 在 $E_n$ 之外（即 $E_n^c$ 上）是连续的。根据叶戈罗夫定理，我们可以找到一个集合 $A_{\epsilon/3}$，在此集合上 $f_n \to f$ 是一致收敛的，且满足 $m(E - A_{\epsilon/3}) \leq \epsilon/3$。

然后，对于足够大的 $N$，使得 $\sum_{n \geq N} 1/2^n < \epsilon/3$，我们考虑集合：

$$F' = A_{\epsilon/3} - \bigcup_{n \geq N} E_n$$

现在，对于每一个 $n \geq N$，函数 $f_n$ 在 $F'$ 上都是连续的；因此，$f$（作为连续函数列 $\{f_n\}$ 的一致极限）在 $F'$ 上也是连续的。为了完成证明，我们仅仅需要用一个闭子集 $F_\epsilon \subset F'$ 去逼近集合 $F'$，使得 $m(F' - F_\epsilon) < \epsilon/3$ 即可。

> [!Success] Borel-Cantelli Lemma
> 令 $\{ E_{k} \}_{k=1}^{\infty}$ 是一族 $\mathbb{R}^d$ 的可测子集且 
> $$\sum_{k=1}^{\infty} m(E_{k})< \infty$$
> 令 
> $$E=\{ x\in \mathbb{R}^d : x\in E_{k} , \text{for infinitely many k}\}=\limsup_{ n \to \infty }\{ E_{k} \} $$
> $E$ 是可测的且 $m(E)=0$ 

**Proof.** 对于任意的 $n\geq 1$ ,有 
$$F_{n}=\bigcup_{k\geq n} E_{k}$$
便有 
$$E=\limsup_{ k \to \infty }E_{k}=\bigcap_{n=1}^{\infty}\bigcup_{k\geq n} E_{k}=\bigcap_{n=1}^{\infty} F_{n} $$
由于任意的 $E_{k}$ 都是可测的，任意 $F_{n}$ 都是可测的，因此 $E$ 也是可测的。此外，有 
$$m(F_{n})=m\left(\bigcup_{k\geq n}E_{k}\right)\leq \sum_{k=n}^{\infty} m(E_{k})$$
由于这个级数是收敛的，那么其尾部有 
$$\sum_{k=n}^{\infty}m(E_{k})\longrightarrow 0$$
集和 $F_{n}$ 是递减的 
$$F_{1}\supset F_{2}\supset\cdots$$
且 $m(F_{1})\leq \sum_{k=1}^{\infty}m(E_{k})< \infty$ ,测度的自上连续性适用，我们就有 
$$m(E)=m\left(\bigcap_{n=1}^{\infty}F_{n}\right)=\lim_{ n \to \infty } m(F_{n})\leq \lim_{ n \to \infty } \sum_{k=n}^{\infty}m(E_{k})=0$$
故 $m(E)=0$ .

### A Tool will Be Used "Bad Set"
