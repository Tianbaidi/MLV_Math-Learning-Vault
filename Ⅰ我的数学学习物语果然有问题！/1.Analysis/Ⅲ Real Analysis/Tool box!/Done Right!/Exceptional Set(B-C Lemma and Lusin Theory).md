---
tags:
  - Real_analysis
  - Measure_Theorem
  - Borel_Cantelli_Lemma
  - Exceptional_Set
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

### A Tool will Be Used —— "Exceptional Set"
设简单函数 
$$\varphi_{n}(x)=\sum_{k=1}^{N_{n}} a_{n,k}\chi_{E_{n.k}}(x)$$
对于每一个固定的 $(n,k)$ 根据 $Lusin$ 定理，选择一个连续函数 $g_{n,k}$ ,s.t 
$$g_{n,k}(x)=\chi_{E_{n,k}}(x)$$
这里除了对一个很小的集和都成立,我们定义 : 
$$B_{n,k}=\{ x\in \mathbb{R}^d :g_{n,k}(x)\neq \chi_{E_{n,k}}(x) \}.$$
这就是我们所言的 **“Exceptional Set”** . 根据 lusin 定理我们可以保证选择 $g_{n,k}$ , s.t 
$$m(B_{n,k}) < \frac{1}{2^n N_{n}(|a_{n,k}|+1)}$$
我们可以进而进行一个更强的估计 
$$\sum_{k=1}^{N_{n}}|a_{a,k}|m(B_{n,k})<2^{-n}$$
在另一篇笔记 [[ɛ-management ɛ-distribution technique]] 我们详细得记录了这个 $2^{-n}$ 的的作用，这会导致 $m(B_{n})\leq \sum_{k=1}^{N_{n}}m(B_{n,k})\leq \sum_{n=1}^{\infty} \frac{1}{2^n}< \infty$ .
由我们的 $Borel-Cante lli ~ lemma$ 可以得到 
$$m(\limsup_{ n \to \infty } B_{n})=0$$
我们再令 $B=\limsup_{ n \to \infty }B_{n}=\bigcap_{N=1}^{\infty }\bigcup_{n\geq N}B_{n}$ , 当我们 $n$ 选取足够大的情况下，有
$$g_{n}(x)=\varphi_{n}(x)$$
故 $\varphi_{n}(x)\to f(x)$ 几乎处处成立，就有 
$$g_{n}(x)\to f(x)$$
对于 $x\in \mathbb{R}^d$ 几乎处处成立. 我们从此有路径将一个连续函数 $g_{n}$ 收敛到 $f$ 上。

我们的强度逐渐增强 ：
可测函数可以由简单函数逼近 $\longrightarrow$ 可测函数可以由连续函数逼近。

# Example : Fourier Analysis
我让 GPT 写了一个例题我们可以尝试做一下：

> [!Quote] Extending Fejer's Theorem from Contionous Function to $L_{1}$
> Let $\mathbb{T}=(-\pi,\pi)$ be the 1-dim torus, and let $F_{N}$ denote the Fejer kernel. For $f\in L^{1}(\mathbb{T})$ , define the Fejer mean of $f$ by 
> $$\sigma_{N}f(x)=\frac{1}{2\pi} \int_{-\pi}^{\pi} f(x-t)F_{N}(t)dt$$
> Assume the following two fact ：
> 1. If $g\in C(\mathbb{T})$ , then 
> $$\sigma_{N}g \to g$$
> uniformly on $\mathbb{T}$
> 2. For every $h\in L^{1}$ ,
> $$||\sigma_{N}h||_{L^1}\leq ||h||_{L^1}$$
> Using the density of continous functions in $L^{1}(\mathbb{T})$ , prove that for every $f\in L^{1}\in \mathbb{T}$ ,
> $$\sigma_{N}f \to f \quad \text{in} L^{1}(\mathbb{T}) \qquad \text{or we can say } \lim_{ N \to \infty } ||\sigma_{N}f -f||_{L^1}=0$$ 

**Proof.** 令 $f\in L^1(\mathbb{T})$ , 且 $\varepsilon>0$ . 由于 连续函数在 $L^1(\mathbb{T})$ 是稠密的。因此存在一个 $g\in C(\mathbb{T})$ 使得，$||f-g||_{L^1}<\varepsilon$ . 我们有 $\sigma_{N}f=\sigma_{N}f-\sigma_{N}g+\sigma_{N} g-g+g-f=\sigma_{N}(f-g)+(\sigma_{N}g-g)+(g-f)$ 利用三角不等式我们得到 
$$||\sigma_{N}f-f||_{L^1}\leq ||\sigma_{N}(f-g)||_{L^1}+||(\sigma_{N}g-g)||_{L^1}+||(g-f)||_{L^1}$$
我们利用其有界我们知道
$$||\sigma_{N}(f-g)||_{L^1}\leq ||f-g||_{L^1}<\varepsilon$$
另外有 $||g-f||_{L_{1}}<\varepsilon$ ，再由 Fact 可知 $||\sigma_{N}g-g||_{L^1}<\varepsilon$ . 因此 
$$||\sigma_{N}f-f||_{L^1}\leq 3 \varepsilon$$
于是得证。

> 我们花大量篇幅证明了 **可测函数可以用连续函数逼近**（通过 Lusin 定理 + 例外集 + Borel‑Cantelli），而傅里叶分析的这个例题就是这一结论的典型应用。  
>   
> 具体来说：  
> - 想要证明 Fejér 均值 $\sigma_N f$ 在 $L^1$ 中收敛到 $f$，我们不能直接对一般的 $f\in L^1$ 下手，因为 Fourier 级数的好性质（一致收敛）只对连续函数成立。  
> - 但正因为连续函数在 $L^1$ 中稠密（这正是前文的结果），我们才可以用一个连续函数 $g$ 去逼近 $f$，然后用算子 $\sigma_N$ 的有界性把误差控制住，最后再把连续函数上的结论（$\sigma_N g \to g$ 一致收敛）传递到 $f$ 上。  
>   如果没有前面 Lusin 定理和例外集技巧建立起的连续函数逼近，这个推广就无法完成。


## Exercise : ？？？
> [!Quote] Exercise:
> let $\delta>0$. Prove that for almost every $x\in [0,1]$, the inequality 
> $$\left|x- \frac{p}{q} \right| <\left| \frac{1}{q^{2+\delta}} \right| $$
> has only finitely many rational solutions $\frac{p}{q}$ with $q\geq {1}$ and $0\leq p\leq q$

