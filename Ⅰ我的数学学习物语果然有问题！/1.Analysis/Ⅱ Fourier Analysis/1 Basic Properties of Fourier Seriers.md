---
tags:
  - Fourier_Analysis
---
> 我们此前已经学习了两个物理模型和三种推导方法 , 并且从我们的求解过程中初识了傅里叶级数的诞生，但是我们此前的研究还是缺乏严谨的。解释不清的东西我们当时就称为萝卜了（一个萝卜一个坑），不过现在我们已经不再是什么都不知道的孩子了（不好说）。我们将从直观的物理模型走出来，进入数学的学习（确信）

# Examples and Fourmulation of the Problem

我们此前讲傅里叶级数定义为 
$$a_{n}=\frac{1}{L}\int_{0}^L f(x)e^{-2\pi inx/L}dx$$
其中 $f$ 是在 $\left[ 0,L \right]$ 上的复值函数，我们需要对其进行进行可积性的限定。在后续内容中我们假设所有函数至少是黎曼可积的。
有时我们回更加关注一些 **“正则”** 的函数（某些具有连续性和可微性的函数）, 它们会更具有启发性 (?) . 下面我们按照普遍性顺序列出几类函数，也不局限在实数领域里，这些函数通常取 $\in \mathbb{C}$ 的函数。此外，我们也会将函数定义在一个圆周上，而不是一个区间。（**圆是一维流形，确信**）
*这里我翻译有些怪，见谅*
### 处处连续函数 **Everywhere continuous functions**

处处连续函数指的是在区间 $[0,L]$ 上每一点都连续的复值函数。我们此后会指出，圆周上的连续函数满足 $f(0)=f(l)$ 
### 分段连续函数 **Piecewise continuous functions**

分段函数指的是在区间 $[0,L]$ 上仅有**有限个**间断点的的**有界**函数。这类函数足够宽泛，足矣解释下面几章我们要提到的定理。但是，为了逻辑的完备性，我们还要考虑黎曼可积类函数——这样的拓展是非常自然的——我们傅里叶级数在形式上采用了积分。
### 黎曼可积函数 **Riemann integrable functions**

黎曼可积类函数是我们关注最一般的函数类，他们有界，但可能拥有无数个间断点。我们这里复习一下可积的定义  $\to$ [[VI 定积分#可积 "可不" 积？]] 

定义在 $[0, L]$ 上的实值函数 $f$ 是黎曼可积的（我们简称为可积 $^2$），如果它是有界的，并且对于每个 $\epsilon > 0$，存在区间 $[0, L]$ 的一个分割 $0 = x_0 < x_1 < \dots < x_{N - 1} < x_N = L$，使得如果 $\mathcal{U}$ 和 $\mathcal{L}$ 分别是 $f$ 关于此分割的上和与下和，即
$$\mathcal{U} = \sum_{j = 1}^{N}\left[\sup_{x_{j - 1}\leq x\leq x_{j}}f(x)\right](x_{j} - x_{j - 1})$$
$$\mathcal{L} = \sum_{j = 1}^{N}\left[\inf_{x_{j - 1}\leq x\leq x_{j}}f(x)\right](x_{j} - x_{j - 1}),$$
那么我们有 $\mathcal{U} - \mathcal{L}< \epsilon$。

如果我们说一个复值函数是可积的，那么它的实部和虚部都是是可积的。此时值得注意的是，两个可积函数的和与积都是可积的。

这里就省略一下例子，

在一个精确的意义上，他们的间断点是 "可忽略" 的——可积函数不连续的点 "**测度为0**" 这些在实分析中足矣涉猎。Tao 的实分析就很适合休闲看（bushi$[虽然我没看]$）

我要给你们设置一个提示词：~~你是一只猫……~~ ，我们之后提到的所有的函数都是可积的 .
### 圆周上的函数 **Functions on the circle**

**如果一切都会重复，如果每一次结束都是开始，那么生命是否还有意义？**

加缪曾经在西西弗神话中给出了这样的解释

> 我把西西弗留在山脚下！我们总是看到他身上的重负。而西西弗告诉我们，最高的虔诚是否认诸神而且搬掉石头，他也认为自己是幸福的。这个从此没有主宰的世界对他来讲既不是荒漠，也不是沃土。这块巨石上的每一颗粒、这黑黝黝的高山上的每一颗矿砂惟有对西西弗才形成一个世界。他爬上山顶所要进行的斗争本身就足以使一个人心里感到充实。应该认为，西西弗是幸福的。

尼采将首尾相接的蛇视为存在主义的图腾，我们能否在数学上定义一个首尾相接的蛇？

对于我们 $\mathbb{R}$ 上周期为 $2\pi$ 的函数，我们可以建立它与单位圆的联系——以函数 $e^{i\theta}$ 为例

单位圆上的点 $e^{i\theta}$ , 其中 $\theta$ 是一个实数——他在相差为 $2\pi$ 之前是唯一的。如果 $F$ 是圆周上的一个函数，他们就能这样定义 
$$f(\theta)=F(e^{i\theta})$$
单纯看式子似乎不太好理解，我们可以在一张纸上画上一个函数，然后保证两点的 **距离** 和你手头的杯子的周长是一样的（你可以先试着卷一下做一个标记）然后再纸上画一个函数。当我们再次将函数卷起来后会发现它就成了一个首尾相接的 “环” 这个在圆上的函数所有性质与我们在平面上的一致。

我们要注意的是，区间 $[0,2\pi]$ 上的的连续函数要是在圆上也连续就必须满足 $f(0)=f(2\pi)$ 

由于我公式的形式与教材一致，我需要再此声明后文的符号使用：当我们的函数定义在直线上的一个区间时，我们通常使用 $x$ 作为自变量；然而，当我们把它们看作是圆周上的函数时，我们通常将变量 $x$ 替换为 $\theta$。我们并非严格遵循此规则，主要看用起来方不方便。
## Main definitions and some examples

是时候来定义我们的傅里叶级数的函数了！我们首先要对这个函数进行一个最初的限定——如果 $f$ 是定义再 $[a,b]$ 这个长度为 $L$ 的区间内。我们的傅里叶级数就是 
$$\hat{f}(n)=\frac{1}{L}\int_{a}^b f(x)e^{-2\pi inx/L},\quad n\in \mathbb{Z}$$
$f$ 的傅里叶级数的形式由下表述（我们在此不考虑级数的收敛） 
$$\sum_{n=-\infty}^{\infty}\hat{f}(x)e^{2\pi inx/L}$$
我们有的时候会将 $f$ 的傅里叶系数记为 $a_{n}$ ,并且用记号 
$$f(x) \sim \sum_{n=-\infty}^{\infty}\hat{f}(x)e^{2\pi inx/L}$$
来表示右边级数是 $f$ 的傅里叶级数

**Example**. 如果 $f$ 是区间 $[-\pi,\pi]$ 上的可积函数，那么 $f$ 的第 $n$ 个傅里叶系数是 
$$\hat{f}(x)=a_{n}=\frac{1}{2\pi} \int_{-\pi}^\pi f(\theta)e^{in\theta}d\theta ,\quad n\in \mathbb{Z}$$
它的傅里叶级数是 
$$f(\theta) \sim \sum_{n=-\infty}^{\infty} a_{n}e^{-in\theta}$$
这里我们采用 $\theta$ 为变量
如果我们选择定义再 $[0,\pi]$ 的函数，我们的公式依然类似，唯一的变化是积分的上下限为 $2\pi$ 与 $0$

当然我们也可以考虑将函数定义在圆上，十分幸运的是，对于定义再圆上的和函数（或者说周期为$2\pi$ 的周期函数，我们得到的积分是一样的）

那要是函数定义在 $[0,1]$ 上呢？？？这里 $g$ 定义在这个区间内 
$$\hat{g}(n)=a_{n}=\int_{0}^{1}g(x)e^{-2\pi inx}dx\quad and \quad g(x)\sim \sum_{n=-\infty}^{\infty}a_{n}e^{2\pi inx}.$$
我们可以采用变量替换的方法将定义在 $[0,2\pi]$ 上的函数定义在 $[0,1]$ 上，只需要令 $g(x)=f(2\pi x)$ .并且我们可以说明 $f$ 的 $n$ 级傅里叶系数就是 $g$ 的 $n$ 级傅里叶系数

---
在傅里叶级数之外，是我们的三角级数 (Trigonometric Series). 

**Def.1** . 三角级数是形如 
$$\sum_{n=-\infty}^{\infty}=c_{n}e^{2\pi inx/L}\quad,c\in \mathbb{C}$$
的表达式。如果三角级数只包含有限多个非零项，即对所有足够大的 $|n|$ 有 $c_{n}=0$ . 就称之为三角多项式。其次数就是令 $c_{n} \neq 0$ 的 $|n|$ 的最大值。

那么我们的傅里叶级数的第 $N^{th}$ ( $N$ 为正整数 ) 部分和实际上式三角多项式的一个特例 , 为 
$$S_{N}(f)(x)=\sum_{n=-N}^{N}\hat{f}(x)e^{2\pi inx/L}$$

> 注意我们的定义，$n$ 的取值范围式对称的 $[-N,N]$ , 这样的选择导致我们的傅里叶级数分解为正弦级数和余弦级数。我们在本书中的傅里叶级数收敛便理解为这个对称和趋于无穷时的极限
> 借此，我们可以重新讨论第一章的基本问题

---
**Problem** : In what sense does $S_{n}(f)$ converge to $f$ as $N \to a$
在探讨问题之前我们先看几个傅里叶级数的的例子：
#### Example.1
我们令 $f(\theta)=\theta$ 且定义在 $[-\pi,\pi]$ 上。我们尝试对其积分（分部积分的使用） 
$$
\begin{align}
\hat{f}(x)=&\frac{1}{2\pi}\int_{-\pi}^{\pi} \theta e^{-in\theta}d\theta \\
=&\frac{1}{2\pi}\left[ - \frac{\theta}{in}e^{-in\theta} \right]^{\pi}_{-\pi} +\frac{1}{2\pi in} \int_{-\pi}^{\pi} e^{-in\theta}d\theta  \\
=&\frac{(-1)^{n+1}}{in}
\end{align}$$
当 $n=0$ 时，我们显然有 
$$\hat{f} (0) = \frac{1}{2\pi}\int_{-\pi}^{\pi}\theta d\theta = 0$$
因此我们关于 $f$ 的傅里叶级数是 
$$f(\theta)\sim \sum_{n\neq 0}\frac{(-1)^{n + 1}}{in} e^{in\theta} = 2\sum_{n = 1}^{\infty}(-1)^{n + 1}\frac{\sin n\theta}{n}.$$
我们的第二个和是通过欧拉恒等式得到的。
#### Example.2
定义 $f(\theta) = (\pi - \theta)^2 /4$ 对于 $0 \leq \theta \leq 2\pi$。然后类似于上一个例子进行连续的分部积分得到 
$$f(\theta)\sim \frac{\pi^2}{12} +\sum_{n = 1}^{\infty}\frac{\cos n\theta}{n^2}.$$
#### Example.3
只要 $\alpha$ 不是整数,函数

$$f(\theta) = \frac{\pi}{\sin\pi\alpha} e^{i(\pi -\theta)\alpha}$$

 在$[0,2\pi ]$ 上的傅里叶级数是 
$$f(\theta)\sim \sum_{n = -\infty}^{\infty}\frac{e^{in\theta}}{n + \alpha}$$

#### Example.4
定义在 $x \in [-\pi , \pi ]$ 上的三角多项式 
$$D_{N}(x) = \sum_{n = -N}^{N}e^{inx}$$
被称为第 $N$ 阶狄利克雷核，这将是我们后面理论的重要基础。注意傅里叶系数的 $a_{n}$ 具有的性质：如果 $|n|\leq N$ 则 $a_{n}=1$ , 否则 $a_{n}=0$ . **Dirichlet Kernel** 的一个闭式公式是 : 
$$D_{N}(x)=\frac{{\sin\left( \left( N+\frac{1}{2} \right)x \right)}}{\sin \frac{x}{2}}$$
我们可以通过求和级数得到 
$$\sum_{n=0}^N \omega^n \quad and \quad \sum_{n=-N}^{-1}\omega^{n}$$
其中 $\omega=e^{ix}$ , 这些和分别等于 
$$\frac{{1-\omega^{N+1}}}{1-\omega} \quad an d \quad \frac{{\omega^{-N}-1}}{1-\omega}$$
那么他们的和为 
$$\frac{\omega^{-N} - \omega^{N + 1}}{1 - \omega} = \frac{\omega^{-N - 1 / 2} - \omega^{N + 1 / 2}}{\omega^{-1 / 2} - \omega^{1 / 2}} = \frac{\sin((N + \frac{1}{2})x)}{\sin(x / 2)}$$
即是我们的结果
#### Example.5
函数 $P_{r}(\theta)$ , 我们称为泊松核 ( Poisson Kernal ) , 对于 $\theta \in [-\pi,\pi]$ 和 $0\leq r<1$ 有绝对一致收敛的级数定义 
$$P_{r}(\theta)=\sum_{n=-\infty}^{\infty}r^{|n|}e^{in\theta}$$
这个函数在第一章我们此前谈论单位圆盘上的稳态热传导方程的解时就已经隐式地出现过了
[[0 Introduction (iii)#^b6592e]] 
在计算 $P_{r}(\theta)$ 的傅里叶系数时，我们可以交换积分和求和的顺序，因为对于每个固定的 $r$，该和在 $\theta$ 上一致收敛，并得到 $n^{th}$ 傅里叶系数等于 $r^{|n|}$。我们也可以对 $P_{r}(\theta)$ 的级数求和，并看到 
$$P_{r}(\theta) = \frac{1 - r^{2}}{1 - 2r\cos\theta + r^{2}}.$$
实际上 
$$P_{r}(\theta) = \sum_{n = 0}^{\infty}\omega^{n} + \sum_{n = 1}^{\infty}\overline{\omega}^{n}\quad \mathrm{with}\quad\omega = re^{i\theta},$$
这两个级数都绝对收敛。第一个（无穷几何级数）等于 $1 / (1 - \omega)$，类似地，第二个等于 $\overline{\omega} /(1 - \overline{\omega})$ .它们结合在一起得到
$$\frac{1 - \overline{\omega} + (1 - \omega)\overline{\omega}}{(1 - \omega)(1 - \overline{\omega})} = \frac{1 - |\omega|^2}{|1 - \omega|^2} = \frac{1 - r^2}{1 - 2r\cos\theta + r^2},$$
我们此后也会再相见

--- 
我们回到此前的问题。对于函数 $f$ 的傅里叶级数的定义是存粹形式上的，它是否收敛到 $f$ 并不明显。解决这个问题取决于我们期望级数以何种形式收敛，或者我们如何对 $f$ 施加一些额外的限制。

（原文有： In fact, the solution of this problem can be very hard, or relatively easy, depending on ...）

让我们精确些说，假设为了讨论方便，函数 $f$ (我们假设它是黎曼可积的) 定义再 $[-\pi,\pi]$ 上，我们首先的疑问是 $f$ 的傅里叶级数的部分和是不是都收敛到 $f$ ? 
$$\lim_{N\to \infty}S_N(f)(\theta) = f(\theta)\quad \mathrm{for~every~}\theta ?$$
一般而言我们不会期望这个结果在每一个 $\theta$ 上都是是成立的，我们总是能做到改变一个可积函数在某一点的值而不改变其傅里叶级数。我们往往也会对连续且周期的 $f$  发出一个同样的问题。曾经（我也不知道是什么时候）人们往往认为在这些条件限定下答案是 " 是 " 。但是知道一个狠人出现 ( Du Bois-Reymond ) , 他的证明论证了存在一个连续函数其傅里叶级数在某一点发散。在下一章我们会给出相应的例子 - 尽管这是一个负面的例子。我们或许会问，如果我们引入更多的光滑性条件会怎样？比如这里我们设 $f$ 是一个连续可微（或者说是二次可微的）

我们还将通过证明傅里叶级数在其所有连续点处，按切萨罗（Cesàro）或阿贝尔（Abel）意义收敛于函数 $f$，来阐释上述极限。这种方法涉及对 $f$ 的傅里叶级数的部分和进行适当的平均 。

在下一章中我们还会在均方根的意义下定义上述极限，即存在 
$$\frac{1}{2\pi}\int_{-\pi}^{\pi}|S_N(f)(\theta) - f(\theta)|^2 d\theta \to 0\quad \mathrm{as}\quad N\to \infty .$$
> It is of interest to know that the problem of pointwise convergence of Fourier series was settled in 1966 by L. Carleson, who showed, among other things, that if $f$ is integrable in our sense, the Fourier series of $f$ converges to $f$ except possibly on a set of "measure 0." The proof of this theorem is difficult and beyond the scope of this book.(原文，意思大概是表明收敛问题被这个人解决了。但是证明不会在这本书里涉及)
# Uniqueness of Fourier Series

这一部分我们讨论的是傅里叶级数的唯一性，一般而言我们唯一性的讨论遵循这样的流程：
**转化叙述:** 如果 $f$ 和 $g$ 有着相同的傅里叶级数，那么 $f$ 和 $g$ 必然相等，我们考虑将计算 $f-g$ 
**表述命题:** 对于所有 $n\in \mathbb{Z}$ 有 $\hat{f}(n)=0$ , 那么 $f=0$ . 
这个断言并非是无条件正确的吗，我们在计算的系数的时候需要计算积分——这会导致两个在有限点处不同的函数有相同的傅里叶级数。不过 , 我们确实有以下正面的结果

**Theorem.2.1** 假设 $f$ 是定义在圆周上的一个可积函数，对于所有 $n\in \mathbb{Z}$ 有 $\hat{f}(n)=0$ 。那么，只要 $f$ 在点 $\theta_0$ 处连续，就有 $f(\theta_0) = 0$。

根据我们对可积函数间断点集的了解，我们可以得出 : $f$ 对 "大多数" 的 $\theta$ 取值为 0 . { 好像不怎么方便 }

**Proof** . 我们对 $f$ 进行限定 —— 首先他是实值，定义在 $[-\pi,\pi]$ 上 , 有 $\theta_{0}=0$ 且 $f(0)>0$ .
我们就定义一族三角多项式 $\{p_{k}\}$ , 他们在 0 处取到 "峰值" ，且当 $k\to \infty$ 时，$\int p_{k}(\theta)f(\theta)d\theta \to \infty$ 这同我们的设想（积分等0）相矛盾从而**反向论证**

下面为论证的结构 ：

> [!NOTE]  整体证明结构
> 
>1. **简化与假设**：不妨设 $f$ 是实值的，通过平移和伸缩令 $\theta_0 = 0$，且 $f(0) > 0$（否则考虑 $-f$）。用反证法。
>2. **利用连续性**：存在 $0 < \delta \leq \pi/2$，使得当 $|\theta| < \delta$ 时 $f(\theta) > f(0)/2$。
>3. **构造基本函数**：令 $p(\theta) = \epsilon + \cos\theta$，选择 $\epsilon > 0$ 足够小，使得：
  > - 当 $\delta \leq |\theta| \leq \pi$ 时，$|p(\theta)| < 1 - \epsilon/2$；
  > - 存在 $\eta < \delta$，使得当 $|\theta| < \eta$ 时，$p(\theta) \geq 1 + \epsilon/2$。
>4. **构造峰值函数族**：定义 $p_k(\theta) = [p(\theta)]^k$，每个 $p_k$ 是三角多项式。
>5. **已知条件导出积分恒为零**：由于 $\hat{f}(n) = 0$ 对所有 $n \in \mathbb{Z}$ 成立，且 $p_k$ 是三角多项式，故
  > $$
   \int_{-\pi}^{\pi} f(\theta) p_k(\theta) d\theta = 0 \quad \text{对一切 } k.
> $$
>6. **积分估计导出矛盾**：
>   - **远离原点部分**：在 $|\theta| \geq \delta$ 上，$|f(\theta)| \leq B$（$f$ 可积故有界），于是
> $$\left|\int_{|\theta| \geq \delta} f p_k\right| \leq 2\pi B (1 - \epsilon/2)^k \xrightarrow{k\to\infty} 0.$$
  > - **中间环带**：在 $\eta \leq |\theta| < \delta$ 上，$f(\theta) > 0$ 且 $p(\theta) > 0$，故积分非负。
   >- **峰值邻域**：在 $|\theta| < \eta$ 上，$f(\theta) \geq f(0)/2$，$p_k(\theta) \geq (1 + \epsilon/2)^k$，从而
   >$$\int_{|\theta| < \eta} f p_k \geq 2\eta \cdot \frac{f(0)}{2} \cdot (1 + \epsilon/2)^k = \eta f(0) (1 + \epsilon/2)^k \xrightarrow{k\to\infty} \infty.$$
   >
   >综合得 $\int f p_k \to \infty$，与步骤5矛盾。
>7. **实值情形结论**：因此 $f(0)=0$，即实值函数在连续点处为零。
>8. **推广到复值函数**：设 $f = u + iv$，由 $\hat{\overline{f}}(n) = \overline{\hat{f}(-n)}$ 可知 $u$ 和 $v$ 的所有傅里叶系数也为零，故在连续点处 $u=v=0$，从而 $f=0$。

现在开始书写证明
由于 $f$ 在 0 处连续，选择 $0< \delta \leq \pi /2$，只要 $|\theta |< \delta$ 就有 $f(\theta) > f(0) / 2$。令
$$p(\theta) = \epsilon +\cos \theta ,$$
其中 , 我们的 $\epsilon>0$ 且足够小 , 只要让 $\delta\leq |\theta|<\pi$ 就有 $|p(\theta)|<1- \frac{\epsilon}{2}$ 。选择一个正数 $\eta$ 满足 $\eta<\delta$ ,使得 $|\theta|<\eta$ 有 $p(\theta)\geq {1}+\frac{\epsilon}{2}$.我们令 
$$p_k(\theta) = [p(\theta)]^k,$$
我们选择 $B$ 令 $|f(\theta)|<B$ 对任意 $\theta$ 成立。对于一个可积函数（有界）这是可能的。
![[bandicam 2026-03-07 14-57-29-696 00_00_00-00_00_30.gif]]
<center>为上式图像</center>
对于所有 $n$ 有 $\hat{f}(n)=0$ , 我们就必须有 
$$\int_{-\pi}^{\pi}f(\theta)p_k(\theta)d\theta = 0\quad \mathrm{for~all~}k.$$ 但是，我们估计的结果是 
$$\left|\int_{\delta \leq |\theta |}f(\theta)p_k(\theta)d\theta \right|\leq 2\pi B(1 - \epsilon /2)^k.$$
我们还对 $\delta$ 的选择保证了只要 $|\theta |< \delta$，$p(\theta)$ 和 $f(\theta)$ 是非负的，因此 
$$\int_{\eta \leq |\theta |< \delta}f(\theta)p_k(\theta)d\theta \geq 0.$$
不得不提的是 
$$\int_{|\theta |< \eta}f(\theta)p_k(\theta)d\theta \geq 2\eta \frac{f(0)}{2} (1 + \epsilon /2)^k.$$
因此，当 $k\rightarrow \infty$ 时 $\int p_k(\theta)f(\theta)d\theta \rightarrow \infty$，这就完成了 $f$ 为实值时的证明。
一般情况下，记 $f(\theta) = u(\theta) + iv(\theta)$，其中 $u$ 和 $v$ 是实值的。如果我们定义 $\overline{f} (\theta) = \overline{f(\theta)}$，那么  
$$u(\theta) = \frac{f(\theta) + \overline{f}(\theta)}{2}\quad \mathrm{and}\quad v(\theta) = \frac{f(\theta) - \overline{f}(\theta)}{2i},$$
并且由于 $\hat{\overline{f}} (n) = \overline{\hat{f} (- n)}$，我们得出结论：$u$ 和 $v$ 的所有傅里叶系数都为零，因此在其连续点处 $f = 0$。

> 构造一族在原点处达到峰值且具有其他良好性质的函数（此处为三角多项式）的想法将在本书中发挥重要作用。我们将在后面第4节结合卷积的概念来讨论这类函数族

下面，我们要关注几个关于上述定理的推论（）
#### Corollary.2.2
如果 $f$ 是定义在圆上的连续函数，且对所有的 $n\in \mathbb{Z}$ 有 $\hat{f}(n)=0$ 那么 $f=0$ 
#### Corollary.2.3
如果 $f$ 是定义在圆上的连续函数，且 $f$ 的傅里叶级数绝对收敛，$\sum_{n = -\infty}^{\infty}|\hat{f} (n)|< \infty$ 那么 , 傅里叶级数一定收敛点到 $f$ , 即 
$$\lim_{N\to \infty}S_N(f)(\theta) = f(\theta)\quad \text{uniformly in } \theta .$$
在傅里叶级数绝对收敛的限定下，对此前的问题有一个更加简单的肯定解答。

**Proof** . 如果一系列的连续函数是一致收敛的，其极限也是连续的。我们观察假设的 $\sum|\hat{f} (n)|< \infty$ （ 意味着这是傅里叶级数的部分和 ）$f$ 的傅里叶级数的部分和是**绝对收敛**且**一致收敛**的。我们定义一个函数 $g$  
$$g(\theta) = \sum_{n = -\infty}^{\infty}\hat{f} (n)e^{in\theta} = \lim_{N\to \infty}\sum_{n = -N}^{N}\hat{f} (n)e^{in\theta}$$
它在圆上是连续的，于是我们可以交换无穷级数与积分。和我们想的那样，将前一个推论应用在 $f-g$ 得到 $f=g$ 。

怎样的 $f$ 能确保它的傅里叶级数绝对收敛？从直觉来看，函数越是光滑（Smoothness）, 级数的衰减系数就越快。我们因此可以预期，相对光滑的函数就等于其傅里叶级数。事实确实如此，现在我们来证明。

为了简洁地**表述结论**，我们引入标准的"O"记号，本书余下部分将**自由使用这一记号**。例如，**表述** $\hat{f} (n) = O(1 / |n|^2)$（当 $|n|\to \infty$ 时）意味着左式受右式的常数倍控制；即存在 $C > 0$，使得对所有**充分大**的 $|n|$，**均有** $|\hat{f} (n)|\leq C / |n|^2$。更一般地，当 $x\to a$ 时 $f(x) = O(g(x))$ 意味着存在**常数** $C$，使得当 $x$ **趋近于** $a$ 时**满足** $|f(x)|\leq C|g(x)|$。特别地，$f(x) = O(1)$ 意味着 $f$ **是有界的**。

#### Corollary.2.4
假设 $f$ 是圆周上的二次可微的连续函数，那么有 
$$\hat{f} (n) = O(1 / |n|^2)\quad as\ |n|\to \infty ,$$
那么，我们 $f$ 的傅里叶级数就绝对且一致收敛到了 $f$ 上

**proof** . 傅里叶系数的估计是通过对 $n \neq 0$ 进行两次分部积分证明的。我们有 
$$\begin{align}
2\pi\hat{f}(n)=& \int_{0}^{2\pi} f(\theta)e^{-in\theta}d\theta \\
=&\left[ f(\theta)\cdot \frac{{-e^{-in\theta}}}{in} \right]^{2\pi}_{0}+\frac{1}{in}\int_{0}^{2\pi}f'(\theta)e^{-in\theta}d\theta \\
=& \frac{1}{in}\int_{0}^{2\pi}f'(\theta)e^{-in\theta}d\theta \\
=&\left[ f'(\theta)\cdot \frac{{-e^{-in\theta}}}{in} \right]^{2\pi}_{0}+\frac{1}{(in)^{2}}\int_{0}^{2\pi}f''(\theta)e^{-in\theta}d\theta \\ \\
=& \frac{1}{(in)^{2}}\int_{0}^{2\pi}f''(\theta)e^{-in\theta}d\theta
\end{align}$$
我们有 
$$2\pi |n|^2 |\hat{f} (n)| \leq \left| \int_0^{2\pi} f''(\theta) e^{-in\theta} d\theta \right| \leq \int_0^{2\pi} |f''(\theta)| d\theta \leq C,$$
其中常数 $C$ 与 $n$ 无关。（我们可以取 $C = 2\pi B$，其中 $B$ 是 $f''$ 的一个界。）由于 $\sum 1 / n^2$ 收敛，推论的证明完成。

在上式的证明过程中，我们建立了如下等式 
$$\hat{f} '(n) = in\hat{f} (n),\quad \mathrm{for~all~}n\in \mathbb{Z}.$$

> 如果 $n$ 等于 0 会怎样？

如果 $f$ 可微且 $f \sim \sum a_n e^{in\theta}$，那么 $f' \sim \sum a_n in e^{in\theta}$。同样，如果 $f$ 两次连续可微，那么 $f'' \sim \sum a_n (in)^2 e^{in\theta}$，依此类推。这也就表明我们的直觉是没问题的。

对于这个推论我们还有更强的版本，下面为一个示例：

假设 $f$ 有一个连续导数，$f$ 的傅里叶级数绝对收敛。更一般地，如果 $f$ 满足阶数为 $\alpha$ 的赫尔德条件（Hölder condition），且 $\alpha > \frac{1}{2}$，即
$$\sup_{\theta}|f(\theta +t) - f(\theta)|\leq A|t|^{\alpha}\quad \mathrm{for~all~}t.$$

在这一点上，我们引入一个常见的记号：用 **$C^k$** 来表示 ‘ 求导 $k$ 次依然连续 ’ 
用 **Hölder 条件** 来表示 ‘ 虽然可能不可导，但变化率受控 ’ 。
这两个概念都用来量化**光滑性**。


> 我们这章的学习已经经过一大半了呢，我们后面要介绍一些傅里叶级数的一些概念，这将会帮助我们在之后的研究。预计直接将傅里叶级数的内容结束。即将开启新的章节
# Convolutions

>卷积在傅里叶分析中起到基础的作用，他非常自然得出现在傅里叶级数中，但是在其他设定下得函数分析中，我们也常常会用到 **卷积** (Convolutions)

给定 $\mathbb{R}$ 上两个周期为 $2\pi$ 的可积函数 $f$ 和 $g$ , 我们在 $[-\pi,\pi]$ 上定义他们的卷积 $f*g$ 为 
$$(f*g)(x)=\frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)g(x-y)dy \tag{1}$$
上述积分对每个 $x$ 都有意义（两个可积函数的积分仍然是可积的）。由于函数是周期的，我们可以通过变量替换得到 
$$(f*g)(x)=\frac{1}{2\pi}\int_{-\pi}^{\pi}f(x-y)g(y)dy$$
简而言之，我们的 **卷积** 便可以理解为 “加权平均 (Weighted averages) ” . 如果 (1) 式中我们定义 $g$ 为常函数，且 $g=1$ , 那么我们的卷积就变成 
$$(f*g)(x)=\frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)dy$$
我们可以理解为 $f$ 在圆周上的平均值。卷积的作用类似于 $f\cdot g$ 但是我们的视角更加全面，倘若直接相乘，我们只等确定某个时间状态下的函数情况，但是一旦我们采用卷积的形式，时间就开始流动。

我们先举一个离散的例子，我们假定有两列数：就记为是 $f$ 和 $g$  . 我们定义卷积公式为
$$(f * g)[n] = \sum_{k} f[k] \cdot g[n-k]$$

| $T$        | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| ---------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| $f$        | 1   | 0   | 0   | 4   | 0   | 0   | 3   | 0   | 1   | 0   |
| $g$        | 10  | 9   | 8   | 7   | 6   | 5   | 4   | 3   | 2   | 1   |
| $f\cdot g$ | 10  | 0   | 0   | 28  | 0   | 0   | 12  | 0   | 2   | 0   |
| $f*g$      | 10  | 9   | 8   | 47  | 42  | 37  | 62  | 54  | 56  | 47  |

如果我们的函数是可积的，就能表示成我们此前的形式。我们回归正题，对于卷积的利用，我们的灵感主要来自之前对核的研究：

傅里叶级数的部分和可以这样表示 
$$\begin{align}
S_N(f)(x) =& \sum_{n = -N}^{N}\hat{f} (n)e^{inx} \\
\qquad = &\sum_{n = -N}^{N}\left(\frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)e^{-iny}dy\right)e^{inx} \\
\qquad = & \frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)\left(\sum_{n = -N}^{N}e^{in(x - y)}\right)dy \\
\qquad =& (f*D_N)(x),
\end{align}$$
其中 $D_{N}$ 是第 $N$ 个狄利克雷核（见例4），由下式给出
$$D_{N}(x) = \sum_{n = -N}^{N}e^{inx}.$$
自此，理解 $S_{N}(f)$ 的问题就转变为理解卷积 $f * D_{N}$。

**Proposition.3.1** **卷积的性质** : 假设 $f$、$g$ 和 $h$ 是 $2\pi$ 周期可积函数。那么 
$$\begin{align}
(i)&\quad \quad f*g(h)=(f*g)+(f*h). \\
(ii)&\quad\quad(cf)*g=c(f*g)=f*(cg),\quad for\ any\ c\in\mathbb{C}. \\
(iii)&\quad\quad f*g=g*f. \\
(iv)&\quad\quad (f*g)*h=f*(g*h). \\
(v)&\quad\quad f*g\quad is\ continuous. \\
(vi)& \quad\quad \widehat{f*g}(n)=\hat{f}(n)\hat{g}(n).
\end{align}$$

> 前四点描述了卷积的代数性质：线性性、交换性和结合性。性质(v)展示了一个重要原则：$f*g$ 的卷积比 $f$ 或 $g$ “更正则( **regular** )”。这里，$f*g$ 是连续的，而 $f$ 和 $g$ 仅仅是（黎曼）可积的。最后，(vi) 是傅里叶级数研究中的关键。一般来说，乘积 $fg$ 的傅里叶系数不是 $f$ 和 $g$ 的傅里叶系数的乘积。然而，(vi) 表明，如果我们用两个函数 $f$ 和 $g$ 的卷积 $f*g$ 代替它们的乘积，那么这个关系成立。

对于命题的证明，我们主要看 (vi) 这个的证明 

**Proof.**  我们假设 $f$ 和 $g$ 是连续的
$$\begin{align}
\widehat{f*g}(n) = &\frac{1}{2\pi}\int_{-\pi}^{\pi}(f*g)(x)e^{-inx}dx  \\
= &\frac{1}{2\pi}\int_{-\pi}^{\pi}\frac{1}{2\pi}\left(\int_{-\pi}^{\pi}f(y)g(x - y)dy\right)e^{-inx}dx \\
= &\frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)e^{-inx}\left(\frac{1}{2\pi}\int_{-\pi}^{\pi}g(x - y)e^{-inx(-y)}dx\right)dy \\
=& \frac{1}{2\pi}\int_{-\pi}^{\pi}f(y)e^{-inx}\left(\frac{1}{2\pi}\int_{-\pi}^{\pi}g(x)e^{-inx}dx\right) \\
= &\hat{f}(n)\hat{g}(n).
\end{align}$$
于是得证，
这是建立在连续的情况下的证明 —— 在这种情况下，我们能自由地交换积分地顺序，这大大地简化了我们的证明。但是实际上，我们可以在原有的条件下进行推导，需要用到我们下面的逼近定理：

**Lemma.3.2** 假设 $f$ 在圆周上可积且以 $B$ 为界。那么存在一列圆周上的连续函数 $\{f_k\}_{k = 1}^{\infty}$，使得
$$\sup_{x\in [-\pi ,\pi ]}|f_k(x)|\leq B\quad \text{for all}\quad k = 1,2,\ldots ,$$
并且
$$\int_{-\pi}^{\pi}|f(x) - f_k(x)|dx\to 0\quad as \quad k\to \infty .$$
  利用这个结果，我们可以如下完成命题的证明。将引理3.2应用于 $f$ 和 $g$，得到逼近连续函数序列 $\{f_k\}$ 和 $\{g_k\}$。那么
$$f*g - f_k*g_k = (f - f_k)*g + f_k*(g - g_k).$$
根据序列 $\{f_k\}$ 的性质
$$\begin{align}
|(f - f_k)*g(x)|\leq&\frac{1}{2\pi}\int_{-\pi}^{\pi}|f(x - y) - f_k(x - y)||g(y)|dy \\

\leq& \frac{1}{2\pi}\sup_y|g(y)|\int_{-\pi}^{\pi}|f(y) - f_k(y)|dy \\
\to& 0\quad \mathrm{as}\ k\to \infty .
\end{align}$$
  因此 $(f - f_k)*g\to 0$ 关于 $x$ 一致成立。类似地，$f_k*(g - g_k)\to 0$ 一致成立，因此 $f_k*g_k$ 一致趋于 $f*g$。由于每个 $f_k*g_k$ 是连续的，可得 $f*g$ 也是连续的，这就得到了 (v)
  
  接下来，我们建立 (vi)。对每个固定的整数 $n$，由于 $f_k*g_k$ 一致收敛到 $f*g$，当 $k$ 趋于无穷时必须有 $\widehat{f_k*g_k}(n)\to \widehat{f*g}(n)$。然而，我们之前发现 $\widehat{f_k}(n)\widehat{g_k}(n) = \widehat{f_k*g_k}(n)$，因为 $f_k$ 和 $g_k$ 都是连续的。因此
$$\begin{align}
\vert \hat{f} (n) - \hat{f}_k(n)\vert = &\frac{1}{2\pi}\left|\int_{-\pi}^{\pi}(f(x) - f_k(x))e^{-inx}dx\right| \qquad  \\
\leq &\frac{1}{2\pi}\int_{-\pi}^{\pi}|f(x) - f_k(x)|dx,
\end{align}$$
我们发现当 $k$ 趋于无穷时 $\widehat{f_k} (n) \to \hat{f} (n)$。类似地 $\widehat{g_k} (n) \to \hat{g} (n)$，当我们让 $k$ 趋于无穷时，性质得证。

最后，性质 (iii) 和 (iv) 由同样的论证得出。
## 音乐上的 “卷积” 
如果我们玩弄音乐，就能考虑一种特殊的演奏手法 —— 卡农

> 同一旋律以同度或五度等不同的高度在各声部先后出现，造成此起彼落连续不断的模仿；一个声部的曲调自始至终追逐着另一声部,直到最后,它们会融合在一起，永不分离”，一如人世间至死不渝的爱情，相爱的两人生死相随，缠绵至极。

按照B站某位up主的科普来看，卡农这种技法就很好地诠释了我们卷积的概念（延时-倍率-叠加）
我们可以看B站的这个可视化视频

如果我们看巴赫的某个谱子 “蟹形卡农the crab canon”，我们发现视频他可以像莫比乌斯环一样由中间截断后首尾首尾连接（你可以详细看一下下面的事实上的内容，实际上并不是）。等待以后我可能开坑了解这些特殊的形状。
![[屏幕截图 2026-03-08 141737.png]]
![[Pasted image 20260308142013.png]]

>但是事实上： Our Canons 3 and 5 from BWV 1087 have this property: their steady states can be read from Möbius strips. Other Bach contrary-motion canons, for example Canons 3 and 9 from the Musical Offering, do not have this property, nor do Variations 12 and 15 from the _Goldberg_ set. This corrects an erroneous statement in our _Musical Times_ article, where we stated that they did.

>  A [beautiful video](https://www.bilibili.com/video/BV16h41197x1/?spm_id_from=333.337.search-card.all.click&vd_source=4612c37942a20cf43b1d8e3315de0629)) has been posted on YouTube showing that Bach's "Crab Canon" (Canon 1 from the Musical Offering) can be read from a Möbius strip. In the Crab Canon, the follower plays the leader backwards, from finish to start. This is an amazing piece of music, but it really has nothing to do with a Möbius strip. The flaw in the construction is that the score ends up written on _both sides_ of a Möbius strip, so it is really written on the connected double cover of the Möbius strip, i.e. a cylinder. Any repeating text can be so

>来自：https://www.ams.org/publicoutreach/feature-column/fc-2016-10（这里对原文链接进行换源处理）

--- 

# Good Kernels

现在，让我们回到对这个公式的理解上来。在上一章我们有一个定理

**Theorem.2.1** 假设 $f$ 是定义在圆周上的一个可积函数，对于所有 $n\in \mathbb{Z}$ 有 $\hat{f}(n)=0$ 。那么，只要 $f$ 在点 $\theta_0$ 处连续，就有 $f(\theta_0) = 0$。

我们构建了一列三角多项式 $\{p_{k}\}$ 来求解，三角多项式 $p_k$ 有在原点处达到峰值的性质：因此，我们可以分离出 $f$ 在原点的行为。现在，我们回到类函数，但是我们这次讨论的环境更加一般，我们的流程如下：
- 定义 **好核** (Good Kernels) , 并且讨论其具有的性质
- 利用卷积，展示如何使用这些核来恢复函数

**Def.2** 如果一族核 $\{K_n(x)\}_{n = 1}^{\infty}$ 满足如下性质，那么他们被称为好核
- 对于任意 $n>1$  
$$\frac{1}{2\pi}{\int_{-\pi}^{\pi}K_{n}(x)dx}=1$$
- 存在 $M>0$ 使得当 $n>1$ 时，有 
$$\int_{-\pi}^\pi |K_{n}(x)|dx<M$$
- 对于任意 $\delta>0$ 
$$\int_{\delta\leq |x|\leq \pi} |K_{n}(x)|dx \to 0\ ,\quad n \to {\infty}$$ 当核 $K_{n}(x)\geq {0}$ 时，第二条就是第一条的推论。

我们将核解释为圆周上的权重分步：
1. 第一条性质为圆周分配了单位质量
2. 而第三条性质则表明质量集中在原点附近
我们下图为一族好核的分配特征：![[Figure_1 1.png]]

> 好核的重要性通过他们在卷积中的应用得以体现

**Theorem.4.1** 令 $\{K_{n}\}^{\infty}_{n=1}$ 为一族好核，并且 $f$ 是圆周上的可积函数. 只要 $f$ 在 $x$ 处连续，我们有 
$$\lim_{ n \to \infty } (f*K_{n})(x)=f(x)$$
如果 $f$  处处连续，那么上述的的极限是一致的

对于这个结果，族 $\{K_{n}\}$ 有时被称为 **恒等逼近** ( Approximation to the identity ) 

此前我们将卷积定义为加权平均。在这里，卷积是 $f(x-y)$ 的平均，其中权重由 $K_{n}(y)$ 给出。随着 $n$ 变大，权重分布 $K_{n}$ 将其质量集中在 $y = 0$ 处。因此，在积分中，当 $n\to \infty$ 时，值 $f(x)$ 被赋予了全部质量
现在我们来证明这个定理 
**Proof.** 如果 $\epsilon>0$ 且 $f$ 在 $x$ 处连续，选取 $\delta$ 令 $|y|<\delta$ implies（蕴含？）$|f(x-y)-f(x)|< \epsilon$  根据好核的第一条性质，我们有 
$$\begin{align}
(f*K_{n})(x)-f(x)=&\frac{1}{2\pi}\int_{-\pi}^\pi K_{n}(y)f(x-y)dy-f(x) \\
=& \frac{1}{2\pi}\int_{-\pi}^\pi K_{n}(y)[f(x-y)-f(x)]dy
\end{align}$$
因此  
$$\begin{array}{r l} & {|(f*K_{n})(x) - f(x)| = \left|\frac{1}{2\pi}\int_{-\pi}^{\pi}K_{n}(y)[f(x - y) - f(x)]dy\right|}\\  &{\qquad \leq \frac{1}{2\pi}\int_{|y|< \delta}|K_{n}(y)||f(x - y) - f(x)|dy}\\ & {\qquad +\frac{1}{2\pi}\int_{\delta \leq |y|\leq \pi}|K_{n}(y)||f(x - y) - f(x)|dy}\\ & {\qquad \leq \frac{\epsilon}{2\pi}\int_{-\pi}^{\pi}|K_{n}(y)|dy + \frac{2B}{2\pi}\int_{\delta \leq |y|\leq \pi}|K_{n}(y)|dy,} \end{array} \quad $$
这里的 $B$ 是 $f$ 的一个界。我们利用好核的性质得到 , 第一项被 $\epsilon M / 2\pi$ 界定 , 对所有足够大的 $n$，第二项将小于 $\epsilon$ , 因此，对某个常数 $C > 0$ 和所有足够大的 $n$，我们有
$$|(f*K_n)(x) - f(x)| \leq C\epsilon,$$
从而证明了定理的一个断言。如果 $f$ 处处连续，那么它是一致连续的，并且 $\delta$ 可以选择与 $x$ 无关。这给出结论：$f*K_n \to f$ **一致收敛**。

## Is it the Dirichlet Kernel a good kernel ?

**Dirichlet kernel** 我们将其表示为 
$$D_{N}(x) = \sum_{n = - N}^{N}e^{inx}$$
他是否是一个好核将被我们验证。不过很遗憾 —— 他不满足好核的第二条性质。我们下面尝试验证

- 对于第一条性质 , 由于只有在 $n=0$ 的时候才有贡献 （正交性），我们应当立即得出
$$\frac{1}{2\pi}\int_{-\pi}^{\pi}D_{N}(x)dx = 1,$$
故第一条性质满足
- 不过我们不得不注意到其绝对值积分会惊人得大，准确来说 
$$\int_{-\pi}^{\pi}|D_{N}(x)|dx\geq c\log N,\quad \mathrm{as}\ N\to \infty .$$
不妨我们画个图看看
![[Figure_2.png]]

这个观察表明傅里叶级数的逐点收敛是复杂的，甚至在连续点处也是如此。
# Applications to Fourier Series - Cesaro and Abel Summability
由于傅里叶级数可能在个别点处不收敛，我们试图通过以下方式在不同的意义下来解释极限，来克服这个失败
$$\lim_{N\to \infty}S_N(f) = f$$
## Cesàro Means and Summation

我们首先取部分和的普通平均，现在将会更详细地描述这种技法

假设我们给定了一个复数项系数： 
$$c_0 + c_1 + c_2 + \dots = \sum_{k = 0}^{\infty}c_k.$$
我们定义第 $n$ 个部分和 $s_n$ 为
$$s_n = \sum_{k = 0}^{n}c_k,$$
如果  $\lim_{n\to \infty}s_n = s$ 就说级数收敛到 $s$ 。这是最自然且常用 (commonly) 的“可和性”类型。然而，考虑级数的例子
$$1 - 1 + 1 - 1 + \dots = \sum_{k = 0}^{\infty}(-1)^k. \quad (3)$$
它的部分和形成序列 $\{1,0,1,0,\ldots \}$，该序列没有极限。因为这些部分和在 1 和 0 之间均匀交替，人们因此可能建议 $1 / 2$ 是该序列的“极限”。
我们通过定义前 $N$ 个部分和的平均来给这个一个精确的意义 
$$\sigma_{N} = \frac{s_{0} + s_{1} + \dots + s_{N - 1}}{N}.$$
$\sigma_{N}$ 被称为序列 $\{s_k\}$ 的第 $N$ 个切萨罗平均或级数 $\sum_{k = 0}^{\infty}c_k$ 的第 $N$ 个切萨罗和。

如果当 $N$ 趋于无穷时 $\sigma_{N}$ 收敛到极限 $\sigma$，我们说级数 $\sum c_n$ 是切萨罗可和到 $\sigma$。我们将根据情况在逐点或一致收敛的意义上理解极限。

读者不难验证，在上述例子 (3) 中，级数是切萨罗可和到 $1 / 2$ 的。此外，可以证明切萨罗求和是一个比收敛更具包容性的过程。事实上，如果一个级数收敛到 $s$，那么它也是切萨罗可和到同一个极限 $s$ 
## Fejér's theorem
An interesting application of Cesaro summability appears in the context of Fourier series.
此前我们提到迪利克雷核不是一个好核，但是我们一旦对其采取平均，他便能构成好核
我们构造傅里叶级数的第 $N$ 个切萨罗平均，根据定义它是
$$\sigma_{N}(f)(x) = \frac{S_{0}(f)(x) + \dots + S_{N - 1}(f)(x)}{N}.$$
我们发现
$$\sigma_{N}(f)(x) = (f * F_{N})(x),$$
其中 $F_{N}(x)$ 是第 $N$ 个费耶核，由下式给出
$$F_{N}(x) = \frac{D_{0}(x) + \dots + D_{N - 1}(x)}{N}.$$
**Lemma.5.1** 我们有
$$F_{N}(x) = \frac{1}{N}\frac{\sin^{2}(Nx / 2)}{\sin^{2}(x / 2)},$$
并且**费耶核** (Fejér Kernel) 是一个好核 , 我们主要证明第二条性质：如果 $\delta \leq |x|\leq \pi$，则 $\sin^{2}(x / 2)\geq c_{\delta} > 0$，因此 $F_{N}(x)\leq 1 / (Nc_{\delta})$，由此可得
$$\int_{\delta \leq |x|\leq \pi}|F_{N}(x)|dx\to 0\quad \mathrm{as}N\to \infty .$$
利用这个定理，我们可以得到
**Theorem.5.2**  如果 $f$ 在圆周上可积，那么 $f$ 的傅里叶级数在 $f$ 的每个连续点处切萨罗可和到 $f$ ; 如果 $f$ 在圆周上连续，那么 $f$ 的傅里叶级数一致切萨罗可和到 $f$。

我们现在可以给出两个推论：
**Corollary.5.3** 如果 $f$ 在圆周上可积且对所有 $n$ 有 $\hat{f} (n) = 0$，那么 $f$ 在其所有连续点处等于 0 .

**Corollary.5.4**圆周上的连续函数可以被三角多项式一致逼近 .
这意味着如果 $f$ 在 $[- \pi ,\pi ]$ 上连续，且 $f(- \pi) = f(\pi)$，并且 $\epsilon >0$，那么存在一个三角多项式 $P$ 使得
$$|f(x) - P(x)|< \epsilon \quad \mathrm{for~all} - \pi \leq x\leq \pi .$$
这直接从定理得出，因为部分和，以及切萨罗平均，都是三角多项式。推论5.4是多项式魏尔斯特拉斯逼近定理的周期版本
## Abel means and summation

另一种求和方法是阿贝尔首先考虑的，实际上早于切萨罗方法
一个复数项级数 $\sum_{k = 0}^{\infty}c_{k}$ 被称为阿贝尔可和到 $s$，如果对每个 $0\leq r< 1$，级数
$$A(r) = \sum_{k = 0}^{\infty}c_{k}r^{k}$$
收敛，并且
$$\lim_{r\to 1}A(r) = s.$$
 $A(r)$ 被称为该级数的阿贝尔平均。可以证明，如果级数收敛到 $s$，那么它是阿贝尔可和到 $s$ 的。
 
 值得一提的是阿贝尔可和性方法甚至比切萨罗方法更强大：当级数切萨罗可和时，它总是和阿贝尔和到同一个和。
但是，如果我们考虑级数
$$1 - 2 + 3 - 4 + 5 - \dots = \sum_{k = 0}^{\infty}(-1)^{k}(k + 1),$$
可以证明它是阿贝尔可和到 $1 / 4$ 的，因为
$$A(r) = \sum_{k = 0}^{\infty}(-1)^{k}(k + 1)r^{k} = \frac{1}{(1 + r)^{2}},$$
但是这个级数不是切萨罗可和的
## The Poisson kernel and Dirichlet's problem in the unit disc

我们定义函数 $f(\theta) \sim \sum_{n = -\infty}^{\infty} a_n e^{in\theta}$ 的阿贝尔平均为
$$A_r(f)(\theta) = \sum_{n = -\infty}^{\infty} r^{|n|} a_n e^{in\theta}.$$
指标 $n$ 取正值和负值，很自然地写 $c_0 = a_0$，并且对于 $n > 0$ 写 $c_n = a_n e^{in\theta} + a_{- n} e^{- in\theta}$，这样傅里叶级数的阿贝尔平均对应于前一节中给数值级数的定义。
注意到，由于 $f$ 是可积的，$|a_n|$ 在 $n$ 中一致有界，因此对于每个 $0 \leq r < 1$，$A_r(f)$ 绝对且一致收敛。就像切萨罗平均的情况一样，阿贝尔平均可以写成卷积的形式
$$A_r(f)(\theta) = (f * P_r)(\theta),$$
其中 $P_r(\theta)$ 是泊松核，由下式给出
$$P_r(\theta) = \sum_{n = -\infty}^{\infty} r^{|n|} e^{in\theta}. \quad (4)$$
In fact， 
$$\begin{align}
A_r(f)(\theta) = & \sum_{n = -\infty}^{\infty} r^{|n|} a_n e^{in\theta} \\
 =& \sum_{n = -\infty}^{\infty} r^{|n|} \left(\frac{1}{2\pi} \int_{-\pi}^{\pi} f(\phi) e^{-in\phi} d\phi\right) e^{in\theta} \\
\qquad =& \frac{1}{2\pi} \int_{-\pi}^{\pi} f(\phi) \left(\sum_{n = -\infty}^{\infty} r^{|n|} e^{-in(\phi -\theta)}\right) d\phi ,
\end{align}$$
其中积分与无穷和交换是由于级数是一致收敛的

**Lemma.5.5** 如果 $0 \leq r < 1$，那么
$$P_r(\theta) = \frac{1 - r^2}{1 - 2r \cos \theta + r^2}.$$
当 $r$ 从下方趋于 1 时，泊松核是一个好核。

**Proof.**  等式 $P_{r}(\theta) = \frac{1 - r^{2}}{1 - 2r\cos\theta + r^{2}}$ 已在此前推到过。注意
$$1 - 2r\cos \theta +r^{2} = (1 - r)^{2} + 2r(1 - \cos \theta).$$
因此，如果 $1 / 2\leq r\leq 1$ 且 $\delta \leq |\theta |\leq \pi$，那么
$$1 - 2r\cos \theta +r^{2}\geq c_{\delta} > 0.$$
当 $\delta \leq |\theta |\leq \pi$ 时 $P_{r}(\theta)\leq (1 - r^{2}) / c_{\delta}$，并且好核的第三个性质被验证。显然 $P_{r}(\theta)\geq 0$，并且逐项积分表达式(4)（由级数的绝对收敛性证明）得到
$$\frac{1}{2\pi}\int_{-\pi}^{\pi}P_{r}(\theta)d\theta = 1,$$
$\square$
与定理4.1结合，我们可以得到。

**Theorem.5.6** 圆周上可积函数的傅里叶级数在其每个连续点处阿贝尔可和到 $f$。此外，如果 $f$ 在圆周上连续，那么 $f$ 的傅里叶级数一致阿贝尔可和到 $f$。

我们回到此前讨论过的一个问题，在那里我们概述了单位圆盘中稳态热传导方程 $\Delta u = 0$ 的解，边界条件为圆上 $u = f$。我们用极坐标表示了拉普拉斯算子，分离了变量，并期望解由下式给出
$$u(r,\theta) = \sum_{m = -\infty}^{\infty}a_{m}r^{|m|}e^{im\theta}, \quad (5)$$
其中 $a_{m}$ 是 $f$ 的第 $m$ 个傅里叶系数。即
$$u(r,\theta) = A_{r}(f)(\theta) = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(\phi)P_{r}(\theta -\phi)d\phi .$$
现在能够证明情况确实如此。（此前这被称为萝卜）

**Theorem.5.7**  设 $f$ 是定义在单位圆周上的一个可积函数。那么由泊松积分在单位圆盘中定义的函数 $u$ $$u(r,\theta) = (f*P_r)(\theta) \quad (6)$$
具有以下性质：
1. $u$ 在单位圆盘内具有两个连续导数，并满足 $\Delta u = 0$ 
2. 如果 $\theta$ 是 $f$ 的任意一个连续点，那么
   $$\lim_{r\to 1}u(r,\theta) = f(\theta).$$
如果 $f$ 处处连续，那么这个极限是一致的。
3. 如果 $f$ 连续，那么 $u(r,\theta)$ 是圆盘中满足条件 (i) 和 (ii) 的稳态热传导方程的唯一解。

**Proof.** 
对于**性质1** ：
 在每个以原点为中心、半径 $r < \rho < 1$ 的圆盘内，$u$ 的级数可以逐项微分，并且微分后的级数是一致且绝对收敛的。因此 $u$ 可以多次微分，并且由于这对所有 $\rho < 1$ 成立 . 此外，在极坐标中，
$$\Delta u = \frac{\partial^2u}{\partial r^2} +\frac{1}{r}\frac{\partial u}{\partial r} +\frac{1}{r^2}\frac{\partial^2u}{\partial\theta^2},$$
逐项积分可以证明 $\Delta u=0$ 

对于**性质2** ：我们可以简单利用定理得证

对于**性质3** ：我们如下论证。假设 $v$ 在圆盘中解稳态热传导方程，并且当 $r$ 从下方趋于 1 时一致收敛到 $f$。对每个固定的 $0 < r < 1$，函数 $v(r,\theta)$ 有一个傅里叶级数
$$\sum_{n = -\infty}^{\infty}a_{n}(r)e^{in\theta}\quad \mathrm{where}\quad a_{n}(r) = \frac{1}{2\pi}\int_{-\pi}^{\pi}v(r,\theta)e^{-in\theta}d\theta .$$
考虑到 $v(r,\theta)$ 解方程
$$\frac{\partial^2v}{\partial r^2} +\frac{1}{r}\frac{\partial v}{\partial r} +\frac{1}{r^2}\frac{\partial^2v}{\partial\theta^2} = 0, \quad (7)$$
我们发现
$$a_n''(r) + \frac{1}{r} a_n'(r) - \frac{n^2}{r^2} a_n(r) = 0 ,\quad (8)$$
实际上，我们可以先将 (7) 乘以 $e^{- in\theta}$ 并在 $\theta$ 上积分。然后，由于 $v$ 是周期的，两次分部积分给出
$$\frac{1}{2\pi}\int_{-\pi}^{\pi}\frac{\partial^2v}{\partial\theta^2} (r,\theta)e^{-in\theta}d\theta = -n^2a_n(r).$$
最后，由于 $v$ 有两个连续导数，我们可以交换微分和积分的顺序，得到 (8)。

因此，当 $n\neq 0$ 时，我们必须有 $a_{n}(r) = A_{n}r^{n} + B_{n}r^{- n}$，其中 $A_{n}$ 和 $B_{n}$ 是某个常数。为了计算这些常数， 由于 $v$ 是有界的我们首先要观察每个项 $a_{n}(r)$ 都是有界的，因此 $B_{n} = 0$。为找到 $A_{n}$，我们令 $r\rightarrow 1$。当 $r\rightarrow 1$ 时 $v$ 一致收敛到 $f$，我们发现
$$A_{n} = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(\theta)e^{-in\theta}d\theta .$$
类似，当 $n = 0$ 时这个公式也成立。

于是，对每个 $0< r< 1$，$v$ 的傅里叶级数由 $u(r,\theta)$ 的级数给出，根据连续函数傅里叶级数的唯一性，我们必 $u = v$。

> 根据定理的第 (iii) 部分，我们可以得出结论：如果 $u$ 在圆盘中解 $\triangle u = 0$，并且当 $r\rightarrow 1$ 时一致收敛到 0，那么 $u$ 必须恒为 0。然而，如果一致收敛被逐点收敛所取代，这个结论可能不成立


