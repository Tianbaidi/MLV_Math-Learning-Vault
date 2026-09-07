---
tags:
  - Fourier_Analysis
  - Axiom_of_Choice
  - Functional_Analysis
---
> 事情的起因是今日如仓前干活，干完活被同学拉着去学泛函分析（大概是要应付期末考试吧）。看到一个此前学过的定理 “ 存在连续函数，其傅里叶级数在指定点发散 ” 。Stein 的傅里叶分析第三章对我而言相对较弱（其他也难评），主要是后面用的多，我会有一定印象。我们主要要解决的问题就写成这样。

> [!Question] Main Question
> 在给定的 $t_{0}\in[0,2\pi]$ 处，总有一个连续函数的 Fourier Series 在该点发散

Proof. 首先，我们定义在 $C(\mathbb{T})$ 上函数的范数 
$$||f||=\sup_{\theta\in \mathbb{T}} |f(\theta)|$$
固定点 $0$ , 定义一族线性泛函 
$$L_{N}(f)=S_{N}(f)(0)$$
其中 $S_{N}(f)$ 是 $Fourier$ 级数第 $N$ 个部分和, 有 $L_{N}(f)=S_{N}(f)(0)= \frac{1}{2\pi} \int_{-\pi}^{\pi} f(-t)D_{N}(t)dt$ 这里的 $D_{N}$ 是狄利克雷核。现在我们要做一件事，证明 
$$||L_{N}||\to \infty$$
我们可以分几步走：

- 一个估计，使得 $\sup_{N}||L_{N}||=\infty$
- 推广到给定任意点 $\theta_{0}\in \mathbb{T}$ 

这里我们可以做一个简简单的估计 
$$|L_{N}(f)|\leq \frac{1}{2\pi} \int_{-\pi}^{\pi} |f(-t)||D_{N}(t)| dt\leq \frac{M}{2\pi} \int_{-\pi}^\pi |D_{N}(t)|dt$$
我们对 Dirichilet 核有一个经典的估计 
$$||D_{N}||\geq c\log N$$
我们对上界的估计就此结束 , $||L_{N}||\leq \infty$ . 为了保证其能够足够大，我们还要对下界进行限制，简单的我们可以取一个连续函数 $f$ 令其满足 $||f_{N}||_{\infty}\leq {1}$  这里我们可以选取一个函数（即我们找到一个函数即可说明其为他的一个下界）此处我们可以特殊的，选择 $f(-t)=sgn D_{N}(t)$ 。于是就有 $|L_{N}(f)|\geq \frac{1}{2\pi} \int_{-\pi}^{\pi} |D_{N}(t)|dt$  于是我们估得其下界。**第一步完成。** 我们有 
$$\sup_{N}||L_{N}||=\infty$$
> 这里我要注意，我们选取的 $\text{sgn }D_{N}$ 并不是一个连续函数，所以我们需要采用连续函数逼近这个函数，实际上，我们与这个理想的值还差一些数值，严格来说是 $|L_{N}(f)|\geq \frac{1}{2\pi} \int_{-\pi}^{\pi} |D_{N}(t)|dt-\varepsilon$ 

第二步，我们要推广到给定点，我们令 $g(\theta)=f(\theta-\theta_{0})$ , 于是有 
$$\hat{g}(n)= \frac{1}{2\pi} \int_{-\pi}^\pi f(\theta-\theta_{0})e^{-in\theta}d\theta$$
令 $u=\theta-\theta_{0}$ 上式就变为 
$$\hat{g}(n)=e^{-in\theta_{0}}\hat{f}(n)$$
我们有 $S_{N}(g)(\theta)=\sum_{|n|\leq N} \hat{g}(n)e^{in\theta}=\sum_{|n|\leq N} \hat{f}(n)e^{in(\theta-\theta_{0})}=S_{N}(f)(\theta-\theta_{0})$
我们给定任意的 $\theta_{0}$ 都能指向 $S_{N}(f)(0)$ 于是我们完成了这个证明

另外的证明（不采用泛函分析的方法）我们可以看这篇笔记 ![[A Symmetry-Breaking Construction for Divergent Fourier Series]] 
# Functional Analysis Tools（kernel)
## Banach--Steinhaus 定理
> 我们发现，泛函分析的方法极大程度上缩小了我们证明上的难度和一些技巧的使用，我们对这里用到的定理进行补全。最核心的是Banach-Steinhaus 定理以及其逆否命题

> [!NOTE] Banach--Steinhaus Theorem (一致有界原理)
> 设 $\{ f_{n} \}$ 是 Banach 空间 $X$ 的一列泛函，如果 $\{ f_{n} \}$ 在 $X$ 的每点 $x$ 都有界，那么 $\{ f_{n} \}$ 一致有界

- 若 $\{T_{N}\}$ 是 Banach 空间 $X$ 到赋范线性空间 $Y$ 的一列有界线性算子。如果对每个 $x\in X$ 都有 $\sup_{N}|T_{N}x|<\infty$ 则 $\sup_{N} ||T_{N}||<\infty$

其有逆反命题
> [!Danger] Corollary
> 设 $X$ 是 Banach 空间 , $T_{N}\in B(X,Y)$ 若 $\sup_{N} ||T_{N}||=\infty$ 则存在某个 $x\in X$ 使得 $\sup_{N} |T_{N}x|=\infty$
> - $Y$ 是赋范线性空间

---

我们只需要证明第一个即可,首先我们要知道 **Baire** 纲定理
- 如果集合 $E$ 可以表示为至多可数个疏集的并，i.e 
$$E=\bigcup_{n=1}^{\infty} E_{n}$$
其中 $E_{n}$ 是疏集，那么 $E$ 为第一纲集
- 若非第一纲集，便合称为第二纲集

> [!NOTE] Theorem Baire
> 完备的距离空间是第二纲集

若完备的距离空间是第一纲集，那么我们可以这样表示 
$$X=\bigcup_{n=1}^{\infty} E_{n}$$
这里每个 $E_{n}$ 都是疏集，于是我们有 ：
- 对于任意开球 $S$ , $E_{1}$ 在 $S$ 中不稠密 i.e. 存在 $S$ 中的点不在 $\overline{E}_{1}$ 中，由于 $S$ 是开球，存在一个闭球 $\overline{S}_{1}\cap E_{1}=\varnothing \quad$ 且 $\overline{S_{1}}$ 的半径小于 $1$  
- 我们反复进行如上操作，得到闭球套（类似区间套）逐步缩小我们的闭球，我们可以知道一定存在某一个点 s.t. $x_{0}\in X \quad ,x\in \bigcap_{n=1}^{\infty} \overline{S}_{n}$
- 但是 $\overline{S}_{n} \cap E_{n}=\varnothing$ ,由于 $\forall n , x\in \overline{S}_{n}$ 这表明 $x_{0}\not\in E_{n}$ 这里是矛盾的
于是 Baire 纲定理成立，且这个定理可以运用到 **Banach** 空间
---

首先我们构造闭集族，对 $k\in \mathbb{N}$ ，定义 $E_{k}=\{ x\in X:\sup_{n}||T_{n}x||\le k \}$ . 对每个 $x\in X$ 都有 $\sup_{n}||T_{n}x||< \infty$ , 故存在某个 $k$ 使得 $X=\bigcup_{k=1}^{\infty} E_{k}$  每一个 $E_{k}$ 都是闭集。由于 $X$ 是 Banach 空间 , 由 Baire 纲定理，完备度量空间不能表示为可数个闭且无内点集和的并，那么必然存在 $k_{0}\in \mathbb{N}$ 有 
$$E_{k_{0}}\neq \varnothing$$
于是，存在 $x_{0}\in X$ 且 $r>0$ ,使得 $B(x_{0},r)\subset E_{k_{0}}$ , 对任意的 $h$ 满足 $|h|<r$  ,我们有 $\mid T_{n}(x_{0}+h)\mid\leq k_{0}$ .

- 由于 $x\in E_{k_{0}}$ , 有$|T_{n}x_{0}|\leq k_{0}$ 对所有的 $n$ 成立
- 对所有的 $|h|<r$ 我们有 
$$|T_{n}h|\leq |T_{n}(x_{0}+h)|+|T_{n}x_{0}|\leq k_{0}+k_{0}=2k_{0}$$
- 取任意的非零 $x\in X$ 令 $h=\frac{r}{2} \frac{x}{|x|}$ , 则 $|h|=\frac{r}{2}<r$ 于是有 
$$|T_{n}h|=\left|T_{n}\left(  \frac{r}{2} \frac{x}{|x|}  \right)\right|=\frac{r}{2} \frac{|T_{n}x|}{|x|}\leq {2}k_{0}$$
对于所有的的 $|T_{n}x|\leq \frac{4k_{0}}{r}|x|$ 我们就有 
$$|T_{n}|\leq \frac{4k_{0}}{r} (\forall n), \quad \sup_{n}|T_{n}|\leq \frac{4k_{0}}{r}< \infty$$
于是得证，推论即为逆否。
