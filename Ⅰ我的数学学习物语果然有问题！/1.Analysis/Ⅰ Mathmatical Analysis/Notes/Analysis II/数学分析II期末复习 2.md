---
tags:
  - Mathematical_Analysis
  - Exercises
---
# 数项级数

> [!ABSTRACT] Definition
> 将一个数列用 $+$ 连接起来，记作 $S_{n}$ , 或用求和记作 
> $$\sum a_{n}$$

> [!Example] EXAMPLE
> 证明：若数列 $\{ a_{n} \}$ 收敛于 $a$ , 则级数 $\sum (a_{n}-a_{n+1})=a_{1}-a$

证明：
设级数的部分和为  
$$
S_N = \sum_{n=1}^N (a_n - a_{n+1}).
$$
展开后逐项相消：
$$
S_N = (a_1 - a_2) + (a_2 - a_3) + \cdots + (a_N - a_{N+1}) = a_1 - a_{N+1}.
$$
由已知 $\{a_n\}$ 收敛于 $a$，即 $\lim_{n\to\infty} a_n = a$，所以  
$$
\lim_{N\to\infty} a_{N+1} = a.
$$
因此  
$$
\lim_{N\to\infty} S_N = \lim_{N\to\infty} (a_1 - a_{N+1}) = a_1 - a.
$$
故级数 $\sum_{n=1}^{\infty} (a_n - a_{n+1})$ 收敛，且其和为 $a_1 - a$，即
$$
\sum_{n=1}^{\infty} (a_n - a_{n+1}) = a_1 - a.
$$
证毕。

> [!Danger] Corollary ：需要注意的已知结论
> - 几何级数 
> $$\sum_{n=0}^{\infty} q^n \quad or \quad \sum_{n=1}^{\infty} q^n $$
> 	- 绝对收敛：当 $|q|<1$ 时，收敛且和为 $\frac{1}{1-q}$ （从0开始）或 $\frac{q}{1-q}$ （从1开始）。
> 	- 发散：当 $|q| \ge 1$ 时发散（$q=1$ 发散到 $+\infty$， $q=-1$ 因通项不趋于0而发散）。
> **特例**： $\sum(-1)^n$ 发散
> - p-级数 
> $$\sum_{n=1}^{\infty} \frac{1}{n^p}$$
> 	- **收敛** ：当 $p > 1$ 时，级数 $\sum_{n=1}^{\infty} \frac{1}{n^p}$ 收敛（绝对收敛）。
> 	- **发散** ：当 $p \le 1$ 时，级数 $\sum_{n=1}^{\infty} \frac{1}{n^p}$ 发散（特别地，$p=1$ 的情况是调和级数 $\sum_{n=1}^{\infty} \frac{1}{n}$，发散）。
> - 交错 p-级数 
> $$\sum_{n=1}^{\infty} \frac{(-1)^n}{n^p}\quad or \quad \sum_{n=1}^{\infty} \frac{{(-1)^{n+1}}}{n^p}$$
> 	- **收敛性：** 当 $p > 0$ 时，由莱布尼茨判别法可知级数 $\sum_{n=1}^{\infty} (-1)^{n+1} \frac{1}{n^p}$ 收敛（因为通项的绝对值 $|(-1)^{n+1} \frac{1}{n^p}| = \frac{1}{n^p}$ 是单调递减且趋于 $0$ 的）。
> 	- **绝对收敛：** 当 $p > 1$ 时，级数绝对收敛。这是因为其绝对值级数 $\sum_{n=1}^{\infty} |\frac{1}{n^p}| = \sum_{n=1}^{\infty} \frac{1}{n^p}$ 是一个 $p$-级数，且此时 $p > 1$。
> 	- **条件收敛：** 当 $0 < p \le 1$ 时，级数收敛，但其绝对值级数 $\sum_{n=1}^{\infty} \frac{1}{n^p}$ 发散（因为 $p \le 1$）。因此，在这种情况下，级数是条件收敛的。 
> 	- **发散：** 当 $p \le 0$ 时，级数发散。这是因为通项 $(-1)^{n+1} \frac{1}{n^p}$ 的绝对值 $|\frac{1}{n^p}| = n^{-p}$ 随着 $n$ 的增大而不趋于 $0$（当 $p=0$ 时为 $1$，当 $p<0$ 时趋于无穷大）。根据级数收敛的必要条件（通项必须趋于 $0$），该级数必然发散。
> **特例** ：$\sum \frac{{(-1)^n}}{n}$ 条件收敛


> [!TIP] Proposition：数项级数收敛的**必要**条件
> 若级数 $\sum_{n=1}^{\infty} a_n$ 收敛，则其通项 $a_n$ 必须趋于零，即： 
> $$ \lim_{n \to \infty} a_n = 0 $$

> [!Example] EXAMPLE
> 利用级数收敛的必要条件，证明下列等式 
> $$1) \lim_{ n \to \infty } \frac{n^n}{(n!)^{2}}=0 \qquad \qquad 2) \lim_{ n \to \infty } \frac{(2n)!}{a^{n!}}=0$$

Answer : 
1) 构造级数 
$$\sum_{n=1}^{\infty}  \frac{n^n}{(n!)^{2}}$$
设 $u_{n}= \frac{n^n}{(n!)^{2}}$ 用比值判别法 
$$\frac{u_{n+1}}{u_{n}}=\frac{(n+1)^{n-1}}{n^n}=\frac{1}{n}\cdot\frac{\left( 1+\frac{1}{n} \right)^n}{1+\frac{1}{n}}$$
由于 $\left( 1+\frac{1}{n} \right)^n \to e$ , $1+\frac{1}{n} \to {1}$  于是比值极限为 $0$ , 级数 $\sum u_{n}$ 收敛，由必要条件 
$$\lim_{ n \to \infty } \frac{n^n}{(n!)^{2}}=0$$
2) **注意：** 若 $0 < a \leq 1$，该极限不为 $0$（甚至发散至无穷），故以下证明默认 $a > 1$。
构造级数
$$\sum_{n=1}^{\infty} \frac{(2n)!}{a^{n!}}.$$
设 $v_n = \dfrac{(2n)!}{a^{n!}}$，计算比值：
$$
\frac{v_{n+1}}{v_n} = \frac{(2n+2)!}{a^{(n+1)!}} \cdot \frac{a^{n!}}{(2n)!} = \frac{(2n+2)(2n+1)}{a^{(n+1)! - n!}}.
$$
而
$$(n+1)! - n! = (n+1)n! - n! = n \cdot n!,$$
所以
$$\frac{v_{n+1}}{v_n} = \frac{(2n+2)(2n+1)}{a^{n \cdot n!}}.$$
当 $a > 1$ 时，分母 $a^{n \cdot n!}$ 的增长速度远快于分子（分子是二次多项式），故
$$\lim_{n \to \infty} \frac{v_{n+1}}{v_n} = 0 < 1.$$
由**比值判别法**，级数 $\sum v_n$ 收敛。根据级数收敛的必要条件（通项趋于 $0$），得到
$$\lim_{n \to \infty} \frac{(2n)!}{a^{n!}} = 0.$$
> [!Example] EXAMPLE
> 设正项级数 $\sum a_{n}$ 收敛 , 证明 $\sum a_{n}^2$ 也收敛 ，反之是否成立？

**证明正向结论**
设 $\sum a_n$ 是收敛的正项级数，则必有通项趋于零：
$$\lim_{n \to \infty} a_n = 0.$$
由极限定义，存在正整数 $N$，使得当 $n > N$ 时，有
$$
0 \leq a_n < 1.
$$

因为 $a_n$ 是非负的，当 $0 \leq a_n < 1$ 时，必有
$$
a_n^2 \leq a_n.
$$

由比较判别法，因为 $\sum_{n=N+1}^{\infty} a_n$ 收敛，且 $0 \leq a_n^2 \leq a_n$，所以 $\sum_{n=N+1}^{\infty} a_n^2$ 也收敛。去掉有限项不影响敛散性，故 $\sum a_n^2$ 收敛。

反之不成立。由 $\sum a_n^2$ 收敛，不能推出 $\sum a_n$ 收敛。
**反例：**
取正项级数
$$a_n = \frac{1}{n}.$$
则
$$
\sum a_n^2 = \sum \frac{1}{n^2}
$$
是 $p = 2 > 1$ 的 $p$-级数，收敛；
但
$$\sum a_n = \sum \frac{1}{n}$$
是调和级数，发散。
因此逆命题不成立。

> [!Danger] Corollary ：运算推论
> - 收敛级数 $+$ 收敛级数 $=$ 收敛级数
> - 收敛级数 $+$ 发散级数 $=$ 发散级数

## 正项级数收敛的判别方法

1. **定义法** i.e  $S_{n}$ 有界
2. **比较法** （放缩，等价）
3. **根式法\比式法** ( $n!$ 用比式 )
4. **积分法** （ $f(x)$ 单调减 ）

> [!Example] EXAMPLE
> 1. 证明：级数 $\sum \sin \frac{1}{n}$ 是发散的
> 2. 讨论级数 $\sum nx^{n-1} ,\quad(x>0)$ 的敛散性
> 3. 判断下面级数的敛散性 
> $$1) \sum_{n=1}^{\infty} \frac{(n!)^{2}}{(2n)!}; \qquad \qquad 2) \sum_{n=1}^{\infty} \frac{n^{2}}{\left( 2+ \frac{1}{n} \right)^n}$$
> 4. 讨论 $p$ 级数的敛散性 .
> 5. 设级数 $\sum a_{n}^{2}$ 收敛，证明 $\sum \frac{a_{n}}{n},\quad(a_{n}>0)$ 也收敛

5. 任意项：
	- 莱布尼茨判别法
	- A\D 判别法
	$\Rightarrow$ 绝对收敛 或 条件收敛
6. 绝对收敛 &条件收敛 （$\sum U_{n}=\sum {v_{n}}-\sum w_{n}$）
$$\begin{cases}
\text{绝对收敛} \Leftrightarrow \sum v_{n} ,\sum w_{n}收敛  \\
\text{条件收敛} \Rightarrow \sum v_{n},\sum w_{n} \text{发散}
\end{cases}$$
> [!Example] EXAMPLE
> 1. 讨论级数 $\sum(-1)^n \sin \frac{2}{n}$ 的敛散性（区分绝对和条件）
> 2. 若数列 $\{ a_{n} \}$ 具有以下性质 
> $$a_{1}\geq a_{2}\geq \cdots\geq a_{n}\geq,\quad \lim_{ n \to \infty } a_{n}=0$$
> 则级数 $\sum a_{n}\sin nx$ 和 $\sum a_{n}\cos nx$ 对任何 $x\in(0,2\pi)$ 都收敛
> 3. 应用Able或Dirichlet判别法来判断级数 $\sum \frac{\sin nx}{n^\alpha},\quad x\in(0,2\pi),\alpha>0$ 的敛散性

# 函数项级数
### 收敛的定义与一致收敛
若函数列 $f_{n}$ 的函数极限趋于 $f$ , 我们则称 $f_{n}$ 收敛于 $f$ ,以下两个表述等价 
$$\lim_{ n \to \infty } f_{n}(x)=f(x) \quad[f_{n}(x)\to f(x)]\quad \Leftrightarrow \quad|f_{n}(x)-f(x)|<\varepsilon$$
我们也称 $\{ f_{n} \}$ 在 $D$ 上 **一致收敛** 到 $f$ 记作 
$$f_{n}(x)\rightrightarrows f(x)\quad(n\to \infty)$$
#### 函数项级数和一致收敛性
我们将函数项级数记为 $\sum u_{n}(x)$ , 称
$$S_{n}(x)=\sum_{k=1}^n u_{k}(x)$$
为部分和函数列。其收敛表示为部分和 $S_{n}$ 当 $n \to \infty$ 的情况下函数存在极限，我们就称其在 $x_{0}$ 处收敛，$x_{0}$ 为收敛点。若级数发散，就称级数在 $x_{0}$ 处发散。若级数在某个子集 $D$ 上收敛，那么我们称 $D$ 为级数的收敛域。（以上应当区分是一个点还是整个函数）

> [!ABSTRACT] Definition ：一致收敛与内闭一致收敛
> 设 $\{ S_{n}(x) \}$ 是函数项级数 $\sum u_{n}(x)$ 的部分和函数列。若 $\{ S_{n}(x) \}$ 在数集 $D$ 上一致收敛于 $S(x)$ , 则称 $\sum u_{n}(x)$ 在 $D$ 上一致收敛到 $S(x)$ 若在一个闭区间 $[a,b]\subset I$ 上一致收敛 , 我们就称在 $I$ 上内闭一致收敛。


#### 判别法 
1. 知道 $S_{n}(x)$ 或求 $\{ f_{n}(x) \}$ : 用余项定理 （一致\非一致） 
$$\lim_{ n \to \infty } \sup |S_{n}(x)-S(x)|=0$$
2. 不知道 $S_{n}(x)$ : ( 判一致 ) 
	- **M 判别法**：设 $\sum u_{n}(x)$ 定义在数集 $D$ 上， $\sum M_{n}$ 为收敛的正项级数，若对一切 $x\in D$ ，有 
$$|u_{n}(x)|\leq M_{n}$$
	则该级数在 $D$ 上一致收敛
	- **阿贝尔判别法**：设
		1) $\sum u_{n}(x)$ 在区间 $I$ 上一致收敛；
		2) 对于每一个 $x\in I$ , $\{ v_{n}(x) \}$ 是单调的
		3) $\{  v_{n}(x) \}$ 在 $I$ 上一致有界，即存在正数 $M$ , 使得对一切 $x\in I$ 和正整数 $n$ 有 
$$|v_{n}(x)|\leq M$$
	则级数 $\sum u_{n}(x)v_{n}(x)$ 在 $I$ 上一致收敛
	- **迪利克雷判别法** ：设 
		1) $\sum u_{n}(x)$ 的部分和数列 
$$S_{n}(x)=\sum _{k=1}^{n}u_{k}(x)$$
		在 $I$ 上一致有界
		2) 对于每一个 $x\in I$ , $\{ v_{n}(x) \}$ 是单调的
		3) 在 $I$ 上有 $v_{k}(x) \rightrightarrows 0$
	则级数 $\sum u_{n}(x)v_{n}(x)$ 在 $I$ 上一致收敛
注意 : 一致收敛不等同于绝对收敛，两者也不可互推

> [!Example] EXAMPLE
> 1. 讨论 $f_{n}(x)= \frac{x}{1+n^{2}x^{2}}, D=(-\infty,+\infty)$ 在区间内是否一致收敛或者内闭一致收敛。
> 2. 函数项级数 $\sum \frac{{\sin nx}}{n^{2}},\quad \sum \frac{{\cos nx}}{n^{2}}$ 在 $(-\infty,+\infty)$ 的敛散性
> 3. 判断 $\sum \frac{x^n}{(n-1)!}$ 在 $(-r,r)$ 的一致收敛性
> 4. 判断 $\sum \frac{(-1)^{n-1}}{x^{2}+n}$ 在 $(-\infty,+\infty)$ 的一致收敛性 
> 5. 判断 $\sum \frac{(-1)^n(x+n)^n}{n^{n+1}}$ 在 $[0,1]$ 上的一致收敛性
> 6. 证明 $\{ a_{n} \}$ 单调且收敛于 $0$ , 则级数 $\sum a_{n}\cos nx$ 在 $[a,2\pi-a]\quad(0<a<\pi)$ 上一致收敛

Answer :
1) 逐点极限：对任意 $x \in \mathbb{R}$，有 $$ \lim_{n \to \infty} f_n(x) = 0. $$ 求一致收敛性： $$ \sup_{x \in \mathbb{R}} |f_n(x)| = \sup_{x \ge 0} \frac{x}{1+n^2x^2}. $$ 令 $g_n(x) = \frac{x}{1+n^2x^2}$，求导得 $$ g_n'(x) = \frac{1-n^2x^2}{(1+n^2x^2)^2}, $$ 故最大值在 $x = \frac{1}{n}$ 处取得，最大值为 $$ g_n\left(\frac{1}{n}\right) = \frac{1/n}{1+1} = \frac{1}{2n} \to 0. $$ 因此 $$ \sup_{x \in \mathbb{R}} |f_n(x) - 0| = \frac{1}{2n} \to 0, $$ 所以 $f_n$ 在 $\mathbb{R}$ 上一致收敛于 $0$，自然也内闭一致收敛。
2) 因为 $$ \left|\frac{\sin nx}{n^2}\right| \le \frac{1}{n^2}, \quad \left|\frac{\cos nx}{n^2}\right| \le \frac{1}{n^2}, $$ 且 $\sum \frac{1}{n^2}$ 收敛，由 Weierstrass M 判别法，这两个级数在 $\mathbb{R}$ 上绝对一致收敛，因此当然收敛。
3) 设 $r > 0$。对任意 $x \in (-r, r)$， $$ \left|\frac{x^n}{(n-1)!}\right| \le \frac{r^n}{(n-1)!}. $$ 而 $$ \sum_{n=1}^{\infty} \frac{r^n}{(n-1)!} = r \sum_{n=1}^{\infty} \frac{r^{n-1}}{(n-1)!} = r e^r < +\infty. $$ 由 Weierstrass M 判别法，该级数在 $(-r, r)$ 上一致收敛。
4) 令 $$ u_n(x) = \frac{1}{x^2+n}. $$ 对每个固定的 $x$， $u_n(x)$ 关于 $n$ 单调递减且趋于 $0$，所以原交错级数逐点收敛。由 Leibniz 余项估计： $$ \left|\sum_{k=n+1}^{\infty} \frac{(-1)^{k-1}}{x^2+k}\right| \le u_{n+1}(x) = \frac{1}{x^2+n+1} \le \frac{1}{n+1}. $$ 因此余项的上确界趋于 $0$，所以该级数在 $\mathbb{R}$ 上一致收敛。
5) 将通项拆分为： $$ \frac{(-1)^n (x+n)^n}{n^{n+1}} = \frac{(-1)^n}{n} \cdot \left(1+\frac{x}{n}\right)^n. $$ 令 $$ a_n(x) = \frac{(-1)^n}{n}, \quad b_n(x) = \left(1+\frac{x}{n}\right)^n. $$ 验证 Abel 判别法的两个条件： 
	1. 级数 $\sum a_n(x)$ 在 $[0, 1]$ 上一致收敛 因为 $a_n(x)$ 与 $x$ 无关，而数项级数 $\sum \frac{(-1)^n}{n}$ 收敛（Leibniz 判别法），所以它在任意区间上（当然包括 $[0, 1]$）一致收敛。 
	2. 函数列 $b_n(x)$ 关于 $n$ 单调且一致有界 
		- **一致有界性：** 当 $x \in [0, 1]$ 时， $$ 1 \le \left(1+\frac{x}{n}\right)^n \le \left(1+\frac{1}{n}\right)^n < e. $$ 所以 $|b_n(x)| \le e$ 对所有 $n$ 和 $x \in [0, 1]$ 成立。 
		- **关于 $n$ 的单调性：** 对固定的 $x \ge 0$，数列 $(1+\frac{x}{n})^n$ 关于 $n$ 单调递增。 简证：令 $f(t) = t \ln\left(1+\frac{x}{t}\right)$ ($t > 0$)，则 $$ f'(t) = \ln\left(1+\frac{x}{t}\right) - \frac{x}{t+x}. $$ 设 $u = \frac{x}{t} \ge 0$，则 $f'(t) = \ln(1+u) - \frac{u}{1+u} \ge 0$ (因为 $\ln(1+u) \ge \frac{u}{1+u}$)，故 $f(t)$ 递增，从而 $b_n(x) = e^{f(n)}$ 关于 $n$ 递增。
由 Abel 判别法（若 $\sum a_n(x)$ 一致收敛，且 $b_n(x)$ 对每个固定的 $x$ 单调且一致有界，则 $\sum a_n(x)b_n(x)$ 一致收敛），可知原级数在 $[0, 1]$ 上一致收敛。
6) 令部分和 $$ S_n(x) = \sum_{k=1}^n \cos kx. $$ 由三角恒等式： $$ S_n(x) = \frac{\sin\left(\left(n+\frac{1}{2}\right)x\right) - \sin\frac{x}{2}}{2 \sin\frac{x}{2}}. $$ 当 $x \in [a, \, 2\pi-a]$ 时，有 $\frac{x}{2} \in [\frac{a}{2}, \, \pi-\frac{a}{2}]$，因此 $$ \left|\sin\frac{x}{2}\right| \ge \sin\frac{a}{2} > 0. $$ 所以部分和一致有界： $$ |S_n(x)| \le \frac{1}{\sin(a/2)}, \quad \forall n \ge 1, \, \forall x \in [a, 2\pi-a]. $$ 又因为 $\{a_n\}$ 单调收敛于 0，所以对于每个固定的 $x$， $a_n$ 是关于 $n$ 的单调数列且一致趋于 0（因与 $x$ 无关）。 
由 Dirichlet 一致收敛判别法（若部分和一致有界，且 $a_n(x)$ 单调一致趋于 0，则 $\sum a_n(x) \cos nx$ 一致收敛），可知 $$ \sum_{n=1}^{\infty} a_n \cos nx $$ 在 $[a, 2\pi-a]$ 上一致收敛。

> [!Question] Remark
> $u_{n}(x)$ 中带 $(-1)^n$ , $\sin nx$ , $\cos nx$ ,我们如何选择采用M或者A-D判别法？
> - 出现 $|\cdot|$ 时，放缩用 $M$ 判别法
> - 出现 $\sum (\cdot)$ 期中由有界部分的采用 A-D 判别法

#### 一致收敛的性质
> [!TIP] Proposition：一致收敛下连续性、可积性、可导性的传递定理
> 
> **1. 连续性的传递（极限运算与极限点交换）**
> - **定理条件**：设函数列（或级数部分和）$S_n(x)$ 在点 $x_0$（或区间 $I$）处连续，且 $S_n(x) \rightrightarrows S(x)$（在 $I$ 上一致收敛）。
> - **定理结论**：则极限函数 $S(x)$ 在点 $x_0$（或区间 $I$）处连续。
> - **核心等式**：极限号与函数号可交换，即
>   $$ \lim_{x \to x_0} \lim_{n \to \infty} S_n(x) = \lim_{n \to \infty} \lim_{x \to x_0} S_n(x). $$
> - **注意**：若仅有点态收敛（逐点收敛），连续性不一定能传递。
> 
> **2. 黎曼可积性的传递（极限运算与积分号交换）**
> - **定理条件**：设 $S_n(x)$ 在闭区间 $[a, b]$ 上（黎曼）可积，且 $S_n(x) \rightrightarrows S(x)$。
> - **定理结论**：则极限函数 $S(x)$ 在 $[a, b]$ 上（黎曼）可积，并且积分号与极限号可以交换顺序。
> - **核心等式**：
>   $$ \int_a^b S(x) \, dx = \int_a^b \lim_{n \to \infty} S_n(x) \, dx = \lim_{n \to \infty} \int_a^b S_n(x) \, dx. $$
> - **注意**：一致收敛保证了“积分极限等于极限积分”；若不一致收敛，即使极限函数可积，等式也未必成立（如 $S_n(x)=n x (1-x^2)^n$ 在 $[0,1]$ 上，逐点收敛于 $0$，但积分极限不为 $0$）。
> 
> **3. 可导性的传递（极限运算与导数号交换）—— 需注意更强的条件**
> - **定理条件**（必须同时满足三条）：
>   1. $S_n(x)$ 在 $[a, b]$ 上处处可导；
>   2. $S_n(x)$ 在 $[a, b]$ 上**逐点收敛**于 $S(x)$（至少存在一点收敛，结合下一条推逐点）；
>   3. **导函数列** $S'_n(x)$ 在 $[a, b]$ 上**一致收敛**于某个函数 $g(x)$。
> - **定理结论**：则极限函数 $S(x)$ 在 $[a, b]$ 上可导，且导数等于导函数列的极限，即
>   $$ S'(x) = g(x) = \lim_{n \to \infty} S'_n(x). $$
> - **核心等式**：
>   $$ \left( \lim_{n \to \infty} S_n(x) \right)' = \lim_{n \to \infty} S'_n(x). $$
> - **特例警示**：若只知道 $S_n$ 一致收敛且可导，但 $S'_n$ 不一致收敛，则 $S$ 不一定可导。
>   - 反例：$S_n(x) = \sqrt{x^2 + \frac{1}{n}}$ 在 $[-1,1]$ 上一致收敛于 $|x|$，但 $|x|$ 在 $x=0$ 处不可导（且 $S'_n(0)=0$，但 $S'(0)$ 不存在）。

> [!DANGER] Corollary ：利用不连续极限函数判断非一致收敛（逆否命题应用）
> 
> **1. 逻辑原理（逆否命题）**
> - 根据上述“连续性传递定理”的逆否命题，可得：
>   > 若每一项 $S_n(x)$ 都在区间 $I$ 上连续，但极限函数 $S(x)$ 在 $I$ 上**至少存在一个不连续点**，则 $S_n(x)$ 在 $I$ 上**必不可能**一致收敛于 $S(x)$。
> - 这是因为：若一致收敛，则连续性能传递，$S$ 必须连续，矛盾。因此，极限函数一旦出现间断，就立刻宣告非一致收敛。
> 
> **2. 经典范例（特例）**：$S_n(x) = x^n$，定义在 $[0, 1]$ 上。
> - **连续性检查**：每一 $S_n(x) = x^n$ 均为多项式，在 $[0,1]$ 上连续。
> - **极限函数**：
>   $$ S(x) = \lim_{n \to \infty} x^n = \begin{cases} 0, & 0 \le x < 1 \\ 1, & x = 1 \end{cases} $$
>   显然，$S(x)$ 在 $x=1$ 处间断（左极限为 $0$，函数值为 $1$）。
> - **结论**：由上述判据，$S_n(x)$ 在 $[0, 1]$ 上**非一致收敛**。
> - **对比**：若将定义域缩小为 $[0, r]$（其中 $0 < r < 1$），则极限函数变为 $S(x) \equiv 0$（连续），此时 $S_n(x)$ 一致收敛于 $0$。
> 
> **3. 另一经典范例**：几何级数的部分和 $S_n(x) = 1 + x + \cdots + x^{n-1}$，定义在 $[0, 1)$ 上。
> - 每一 $S_n(x)$ 连续。
> - 极限函数 $S(x) = \frac{1}{1-x}$ 在 $x \to 1^-$ 时无界，故在 $[0,1)$ 上非一致连续（更谈不上一致收敛）。
> - **结论**：该级数在 $[0,1)$ 上非一致收敛（但在任意 $[0, r]$（$0<r<1$）上一致收敛）。
> 
> **总结判别口诀**：
> *连续、积分看一致*（一致收敛就能传）；
> *求导还需看导列*（导函数列一致收敛才能传导数）；
> *极限间断必不一*（极限函数有间断点，则原列必非一致收敛）。


> [!Example] EXAMPLE
> 1. 设 $S(x)=\sum_{n=1}^{\infty} ne^{-nx}$ , $x>0$ , 计算$\displaystyle\int_{\ln{2}}^{\ln 3}S(t)dt$
> 2. 证明 ：函数 $f(x)=\sum \frac{{\sin nx}}{n^3}$ 在 $(-\infty,+\infty)$ 上连续，且有连续的导数
> 3. 设 $f_{n}(x)=x^n$ 为定义在 $(-\infty,+\infty)$ 上的函数列，证明它的收敛域是 $(-1,1]$ ,且有极限函数

1. 设 $$ S(x) = \sum_{n=1}^{\infty} n e^{-nx}, \quad x > 0. $$ 令 $r = e^{-x} \in (0, 1)$，则 $$ S(x) = \sum_{n=1}^{\infty} n r^n = \frac{r}{(1-r)^2} = \frac{e^{-x}}{(1-e^{-x})^2} = \frac{e^x}{(e^x-1)^2}. $$ 所以 $$ \int_{\ln 2}^{\ln 3} S(t) \, dt = \int_{\ln 2}^{\ln 3} \frac{e^t}{(e^t-1)^2} \, dt = \left[-\frac{1}{e^t-1}\right]_{\ln 2}^{\ln 3} = -\frac{1}{e^{\ln 3}-1} - \left(-\frac{1}{e^{\ln 2}-1}\right) = -\frac{1}{3-1} + \frac{1}{2-1} = -\frac{1}{2} + 1 = \frac{1}{2}. $$
2. 设 $$ f(x) = \sum_{n=1}^{\infty} \frac{\sin nx}{n^3}. $$ 因为 $$ \left|\frac{\sin nx}{n^3}\right| \le \frac{1}{n^3}, $$ 而 $\sum_{n=1}^{\infty} \frac{1}{n^3}$ 收敛，所以原级数在 $\mathbb{R}$ 上一致收敛。又每一项连续，故 $f(x)$ 在 $\mathbb{R}$ 上连续。 逐项求导得 $$ f'(x) = \sum_{n=1}^{\infty} \frac{\cos nx}{n^2}. $$ 而 $$ \left|\frac{\cos nx}{n^2}\right| \le \frac{1}{n^2}, $$ 且 $\sum_{n=1}^{\infty} \frac{1}{n^2}$ 收敛，所以 $\sum_{n=1}^{\infty} \frac{\cos nx}{n^2}$ 在 $\mathbb{R}$ 上一致收敛。因此 $$ f'(x) = \sum_{n=1}^{\infty} \frac{\cos nx}{n^2}, $$ 且该级数每一项连续、一致收敛，所以 $f'(x)$ 连续。 故 $f(x)$ 在 $\mathbb{R}$ 上连续且有连续导数。
3. 设 $$ f_n(x) = x^n, \quad n = 1, 2, \dots. $$ 逐点讨论：
* 若 $|x| < 1$，则 $\lim_{n \to \infty} x^n = 0$。 * 若 $x = 1$，则 $1^n \to 1$。
* 若 $x = -1$，则 $(-1)^n$ 不收敛。 * 若 $|x| > 1$，则 $|x|^n \to +\infty$，也不收敛。 所以收敛域为 $(-1, 1]$。极限函数为 $$ \lim_{n \to \infty} x^n = \begin{cases} 0, & -1 < x < 1, \\ 1, & x = 1. \end{cases} $$ 综上，收敛域是 $(-1, 1]$，极限函数为 $$ f(x) = \begin{cases} 0, & -1 < x < 1, \\ 1, & x = 1. \end{cases} $$

# 幂级数
> [!ABSTRACT] Definition
> 幂级数是一类形如 $\sum_{n=0}^{\infty} a_n (x-x_0)^n$ 的函数项级数，其中：
>  * $a_n$ 称为系数（与 $x$ 无关的常数）； 
>  * $x_0$ 称为中心点（展开中心）； 
>  * $x$ 是自变量。 
>  特别地，当 $x_0 = 0$ 时，标准形式为 $\sum_{n=0}^{\infty} a_n x^n$。
>  注意，级数从 $n=0$ 开始，若缺项（如只有奇数次幂），需视为“缺项幂级数”，计算半径时不能直接套用系数比，需转化为数项级数处理。

> [!ABSTRACT] Definition
> 收敛半径 $R$ ($0 \le R \le +\infty$) 是唯一确定的值，使得：
>  * 当 $|x-x_0| < R$ 时，级数**绝对收敛**； 
>  * 当 $|x-x_0| > R$ 时，级数**发散**； 
>  * 当 $|x-x_0| = R$ 时，敛散性不定（需单独判断）。

> [!Quote] 收敛半径求法
> **根值法（柯西-阿达马定理）：** 
>  $$ \frac{1}{R} = \limsup_{n \to \infty} |a_n|^{1/n} $$ 
>  （若极限为 $0$，则 $R = +\infty$；若极限为 $+\infty$，则 $R = 0$）。
>   **比值法（达朗贝尔）：** 
>   当 $\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right|$ 存在（或为无穷）时，可用：
>    $$ R = \lim_{n \to \infty} \left|\frac{a_n}{a_{n+1}}\right| $$
>     ⚠️ **避坑指南（缺项幂级数）：** 若级数为 $\sum a_n x^{2n}$ 或 $\sum a_n x^{kn}$，不能直接取系数的比值。正确做法是令新变量 $t = x^k$，先求 $t$ 的收敛半径 $R_t$，再解 $|x^k| < R_t$ 得到 $x$ 的半径 $R_x = R_t^{1/k}$。或者直接用后项与前项的绝对值比（带上次数）。

> [!ABSTRACT] Definition
> 收敛域是指所有使得级数收敛的 $x$ 的取值集合。它等于收敛区间 $(x_0-R, x_0+R)$ 再并上端点处收敛的部分。

> [!Quote] 求收敛域
> **求解三步法（务必按顺序操作）：** 
> 1. **求半径：** 用上述公式算出 $R$，得到开区间 $(x_0-R, x_0+R)$（该区间内绝对收敛）。 
> 2. **代入左端点：** 令 $x = x_0 - R$，原级数变为数项级数 $\sum a_n (-R)^n$，用莱布尼茨判别法或数项级数审敛法判断是否收敛。 
> 3. **代入右端点：** 令 $x = x_0 + R$，原级数变为 $\sum a_n R^n$，同样判断敛散性。 
> **最终收敛域的形态（4种可能）：** 
> * $(x_0-R, x_0+R)$ （两端都发散） 
> * $[x_0-R, x_0+R)$ （左端收敛，右端发散） 
> * $(x_0-R, x_0+R]$ （左端发散，右端收敛） 
> * $[x_0-R, x_0+R]$ （两端都收敛）

> [!Example] EXAMPLE
> 求下列级数的收敛半径和收敛域 :
> $$1)\sum_{n=1}^{\infty} \frac{x^n}{n^2\cdot 2^n},\qquad \qquad 2) \sum_{n=1}^{\infty} \frac{{(n!)^2}}{(2n)!}x^n$$

Answer:
1. **第一步：求收敛半径 $R$** 
系数 $a_n = \frac{1}{n^2 2^n}$，因为含指数和多项式，用比值法最顺手： 
$$ R = \lim_{n \to \infty} \left|\frac{a_n}{a_{n+1}}\right| = \lim_{n \to \infty} \frac{(n+1)^2 2^{n+1}}{n^2 2^n} = \lim_{n \to \infty} 2 \left(1 + \frac{1}{n}\right)^2 = 2 $$
所以收敛区间为 $(-2, 2)$。
**第二步：判断端点（收敛域的关键）** 
* **右端点 $x=2$：** 
	代入得 $\sum \frac{2^n}{n^2 2^n} = \sum \frac{1}{n^2}$。这是 $p=2$ 的调和级数，收敛。
* **左端点 $x=-2$：** 
	代入得 $\sum \frac{(-2)^n}{n^2 2^n} = \sum \frac{(-1)^n}{n^2}$。由于 $\sum \left|\frac{(-1)^n}{n^2}\right| = \sum \frac{1}{n^2}$ 收敛，所以原级数绝对收敛。 
**结论：** 收敛半径 $R=2$；收敛域为 $[-2, 2]$ （两端点均收敛）。

1. **第一步：求收敛半径 
   $R$** 系数 $a_n = \frac{(n!)^2}{(2n)!}$，阶乘结构强烈暗示使用比值法（注意化简时的“错位相消”）： $$ R = \lim_{n \to \infty} \left|\frac{a_n}{a_{n+1}}\right| = \lim_{n \to \infty} \frac{(n!)^2}{(2n)!} \cdot \frac{(2n+2)!}{((n+1)!)^2} $$ 逐项展开化简（核心技巧）： $$ (2n+2)! = (2n+2)(2n+1)(2n)! $$ $$ ((n+1)!)^2 = (n+1)^2 (n!)^2 $$ 代入得： $$ R = \lim_{n \to \infty} \frac{(2n+2)(2n+1)}{ (n+1)^2} = \lim_{n \to \infty} \frac{2(n+1)(2n+1)}{(n+1)^2} = \lim_{n \to \infty} \frac{2(2n+1)}{n+1} = 4 $$ 所以收敛区间为 $(-4, 4)$。 
**第二步：判断端点（这里有大坑！）** 不要想当然觉得端点也收敛，必须代入验算。 
* **右端点 $x=4$：** 
	代入得 $\sum \frac{(n!)^2}{(2n)!} 4^n$。令通项为 $u_n$，看后项与前项比值的极限（判断通项是否趋于 0）： $$ \frac{u_{n+1}}{u_n} = \frac{((n+1)!)^2}{(2n+2)!} 4^{n+1} \cdot \frac{(2n)!}{(n!)^2 4^n} = \frac{(n+1)^2}{(2n+2)(2n+1)} \cdot 4 = \frac{(n+1)^2}{2(n+1)(2n+1)} \cdot 4 = \frac{2(n+1)}{2n+1} = \frac{2n+2}{2n+1} > 1 $$ 因为后项比前项恒大于 1，说明数列 $\{u_n\}$ 严格单调递增，因此通项 $u_n \not\to 0$。
	由级数收敛的必要条件（通项须趋于 0）可知，该级数发散。
* **左端点 $x=-4$：**
	代入得 $\sum \frac{(n!)^2}{(2n)!} (-4)^n = \sum (-1)^n u_n$。虽然多了交错符号，但绝对值 $|(-1)^n u_n| = u_n$ 仍然严格递增且不趋于 0，所以通项 $(-1)^n u_n$ 同样不趋于 0。故该级数也发散。 
**结论（题2）：** 收敛半径 $R=4$；收敛域为 $(-4, 4)$ （两端点均发散，开区间）。

## 求和函数
我们有两个类型 :
1. $\frac{1}{1\pm x}=\sum(\mp x)^n$ 逐项求导，积分
	**若级数分母有 $n$（如 $\sum \frac{x^n}{n}$）：** 
	先把原材料 $\frac{1}{1-x} = \sum x^n$ 从 $0$ 到 $x$ 积分，得到 $\sum \frac{x^n}{n} = -\ln(1-x)$。 
	（注：$\frac{1}{1+x}$ 积分则对应 $\ln(1+x)$） 
	**若级数分子有 $n$（如 $\sum nx^{n-1}$ 或 $\sum nx^n$）：** 
	对原材料逐项求导，得到 $\sum nx^{n-1} = \frac{1}{(1-x)^2}$。 
	（若题目给的是 $\sum nx^n$，只需再乘一个 $x$ 即可）
2. $e^x=\sum \frac{x^n}{n!}$ 
	把 $e^x = \sum \frac{x^n}{n!}$ 当作万能模板。当题目给的级数带有阶乘 $n!$ 在分母时，通常只能由 $e^x$ 演变而来。此时，处理分子上多余的 $n$（如 $n^2$、$n(n-1)$）也是通过逐项求导，因为 $(x^n)' = nx^{n-1}$。 
	**考场上的经典套路：** 
	* 若题目是 $\sum \frac{n}{n!} x^n$： 因为 $\frac{n}{n!} = \frac{1}{(n-1)!}$，直接用 $e^x$ 的展开式，令 $n-1=k$ 即可凑出 $xe^x$。 
	* 若题目是 $\sum \frac{n^2}{n!} x^n$ ： 这时需要“求导一次，乘一个 $x$”的算子操作
	  因为 $(xe^x)' = e^x + xe^x$ 会给出 $n+1$ 的因子，以此递推消去 $n^2$。
	
	* 一句话总结：分母有阶乘 $n!$ → 目标函数一定是 $e^x$ 及其导数/乘以 $x$ 的组合。

> [!Example] EXAMPLE
> 1. 求级数 $\displaystyle \sum_{n=1}^{\infty}(-1)^{n-1}n^{2}x^n$ 的和函数
> 2. 求 $\displaystyle \sum_{n=1}^{\infty} \frac{x^n}{n(n+1)}$ 的收敛半径和和函数
> 3. 应用幂级数的性质求 $\displaystyle \sum_{n=1}^{\infty} \frac{n}{(n+1)!}$ 以及 $\displaystyle \sum \frac{n}{(n+1)!}x^n$ 的和

Answer: 
1. **题型识别：** 无阶乘 $n!$，有分子 $n^2$ → 类型1（几何级数求导）。
	**母函数构造：** 先看系数符号 $(-1)^{n-1}$，对应的几何级数模板是 $\frac{1}{1+x} = \sum_{n=0}^\infty (-1)^n x^n$。 为了对齐 $n$ 从 1 开始，令： $$ S_0(x) = \sum_{n=1}^\infty (-1)^{n-1} x^n = \frac{x}{1+x} \quad (|x|<1) $$ **“求导消 $n$”算子：** 为了把 $n^2$ 变出来，我们使用算子 $(x \frac{d}{dx})$。它对 $x^n$ 作用一次得 $nx^n$，作用两次得 $n^2x^n$。 $$ S(x) = \sum_{n=1}^\infty (-1)^{n-1} n^2 x^n = \left(x \frac{d}{dx}\right)^2 \left(\frac{x}{1+x}\right) $$ **计算过程：** 先算一次： $$ x \cdot \left(\frac{x}{1+x}\right)' = x \cdot \frac{(1+x) \cdot 1 - x \cdot 1}{(1+x)^2} = x \cdot \frac{1}{(1+x)^2} = \frac{x}{(1+x)^2} $$ 再算第二次（注意这是对 $\frac{x}{(1+x)^2}$ 求导后乘 $x$）： $$ S(x) = x \cdot \left[\frac{x}{(1+x)^2}\right]' = x \cdot \frac{(1+x)^2 \cdot 1 - x \cdot 2(1+x)}{(1+x)^4} = x \cdot \frac{(1+x) - 2x}{(1+x)^3} = x \cdot \frac{1-x}{(1+x)^3} = \frac{x(1-x)}{(1+x)^3} $$ **收敛域：** 原级数收敛半径 $R=1$（因为 $\lim_{n \to \infty} \left|\frac{a_n}{a_{n+1}}\right| = 1$）。 
	端点 $x=\pm 1$ 时，通项绝对值 $|(-1)^{n-1} n^2 (\pm 1)^n| = n^2 \to \infty \neq 0$，发散。
	 **最终答案：** 和函数 $\frac{x(1-x)}{(1+x)^3}$，收敛域 $(-1, 1)$。
2. **收敛半径：** 
	系数 $a_n = \frac{1}{n(n+1)}$，用比值法： $$ R = \lim_{n \to \infty} \left|\frac{a_n}{a_{n+1}}\right| = \lim_{n \to \infty} \frac{n(n+1)}{(n+1)(n+2)} = \lim_{n \to \infty} \frac{n}{n+2} = 1 $$ **端点判断：** 
	* $x=1$ 时，$\sum \frac{1}{n(n+1)}$ 收敛（与 $\sum \frac{1}{n^2}$ 比较）。 
	* $x=-1$ 时，$\sum \frac{(-1)^n}{n(n+1)}$ 绝对收敛（因为 $\sum |\frac{(-1)^n}{n(n+1)}| = \sum \frac{1}{n(n+1)}$ 收敛）。 
	 故收敛域为 $[-1, 1]$。 
	**求和函数（技巧：裂项相消 + 已知和函数）：** 看到分母是 $n(n+1)$，联想到裂项： $$ \frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1} $$ 于是： $$ S(x) = \sum_{n=1}^\infty \frac{x^n}{n(n+1)} = \sum_{n=1}^\infty \left(\frac{1}{n} - \frac{1}{n+1}\right) x^n = \sum_{n=1}^\infty \frac{x^n}{n} - \sum_{n=1}^\infty \frac{x^n}{n+1} $$ **第一项：** $$ \sum_{n=1}^\infty \frac{x^n}{n} = -\ln(1-x) \quad (\text{这是类型1的积分结果}) $$ **第二项：** 为了凑出 $\ln(1-x)$，把 $\frac{1}{n+1}$ 升阶，先乘 $x$ 再处理： $$ \sum_{n=1}^\infty \frac{x^n}{n+1} = \frac{1}{x} \sum_{n=1}^\infty \frac{x^{n+1}}{n+1} = \frac{1}{x} \sum_{k=2}^\infty \frac{x^k}{k} $$ 我们知道 $\sum_{k=1}^\infty \frac{x^k}{k} = -\ln(1-x)$。 所以， $$ \sum_{k=2}^\infty \frac{x^k}{k} = \left(\sum_{k=1}^\infty \frac{x^k}{k}\right) - \frac{x^1}{1} = -\ln(1-x) - x $$ 因此： $$ \sum_{n=1}^\infty \frac{x^n}{n+1} = \frac{1}{x} (-\ln(1-x) - x) = -\frac{\ln(1-x)}{x} - 1 $$ 代回原式： $$ S(x) = -\ln(1-x) - \left(-\frac{\ln(1-x)}{x} - 1\right) = -\ln(1-x) + \frac{\ln(1-x)}{x} + 1 = 1 + \left(\frac{1}{x} - 1\right)\ln(1-x) $$ 注意定义 $x=0$ 时，原级数为 0，且上述表达式在 $x \to 0$ 时极限也为 0。 $$ \lim_{x \to 0} \left(1 + \left(\frac{1}{x} - 1\right)\ln(1-x)\right) = \lim_{x \to 0} \left(1 + \frac{1-x}{x}\ln(1-x)\right) $$ 使用洛必达法则对 $\frac{(1-x)\ln(1-x)}{x}$ 求极限： $$ \lim_{x \to 0} \frac{-\ln(1-x) + (1-x)\frac{-1}{1-x}}{1} = \lim_{x \to 0} (-\ln(1-x) - 1) = -1 $$ 所以， $$ S(x) = 1 + \lim_{x \to 0} \left(\frac{1}{x} - 1\right)\ln(1-x) = 1 + (-1) = 0 $$ 因此，当 $x=0$ 时，和为 0。 
	**最终答案：** 和函数 $S(x) = 1 + \frac{1-x}{x}\ln(1-x)$ （$x \neq 0$，且 $S(0)=0$），收敛域 $[-1, 1]$。
3. **题型识别：** 
	分母带 $n!$ → 类型2 ($e^x$ 模板)。
	核心技巧是拆分系数，把 $\frac{n}{(n+1)!}$ 拆成两个能匹配 $e^x$ 的形式。
	 **拆分系数：** $$ \frac{n}{(n+1)!} = \frac{(n+1)-1}{(n+1)!} = \frac{n+1}{(n+1)!} - \frac{1}{(n+1)!} = \frac{1}{n!} - \frac{1}{(n+1)!} $$ **先求幂级数 $S(x) = \sum_{n=1}^\infty \frac{n}{(n+1)!} x^n$ （包含 $x$）：** $$ S(x) = \sum_{n=1}^\infty \left(\frac{1}{n!} - \frac{1}{(n+1)!}\right) x^n = \sum_{n=1}^\infty \frac{x^n}{n!} - \sum_{n=1}^\infty \frac{x^n}{(n+1)!} $$ **第一项：** $$ \sum_{n=1}^\infty \frac{x^n}{n!} = \left(\sum_{n=0}^\infty \frac{x^n}{n!}\right) - \frac{x^0}{0!} = e^x - 1 $$ **第二项：** 令 $k = n+1$，则 $n = k-1$。当 $n=1$ 时，$k=2$。 $$ \sum_{n=1}^\infty \frac{x^n}{(n+1)!} = \sum_{k=2}^\infty \frac{x^{k-1}}{k!} = \frac{1}{x} \sum_{k=2}^\infty \frac{x^k}{k!} $$ 我们知道 $\sum_{k=0}^\infty \frac{x^k}{k!} = e^x$。 所以， $$ \sum_{k=2}^\infty \frac{x^k}{k!} = \left(\sum_{k=0}^\infty \frac{x^k}{k!}\right) - \frac{x^0}{0!} - \frac{x^1}{1!} = e^x - 1 - x $$ 因此： $$ \sum_{n=1}^\infty \frac{x^n}{(n+1)!} = \frac{1}{x} (e^x - 1 - x) $$ **代入得：** $$ S(x) = (e^x - 1) - \frac{1}{x} (e^x - 1 - x) = e^x - 1 - \frac{e^x}{x} + \frac{1}{x} + 1 = e^x - \frac{e^x}{x} + \frac{1}{x} = \frac{xe^x - e^x + 1}{x} $$ 同样，当 $x=0$ 时，原级数项为 0。我们计算极限： $$ \lim_{x \to 0} S(x) = \lim_{x \to 0} \frac{xe^x - e^x + 1}{x} $$ 这是一个 $\frac{0}{0}$ 型不定式，使用洛必达法则： $$ \lim_{x \to 0} \frac{e^x + xe^x - e^x}{1} = \lim_{x \to 0} xe^x = 0 $$ 所以，补齐定义 $S(0)=0$。
	 **再求常数项级数 $\sum_{n=1}^\infty \frac{n}{(n+1)!}$：
	 **这其实就是幂级数在 $x=1$ 处的取值（因为在收敛域内，显然收敛）：** 
	 $$ \sum_{n=1}^\infty \frac{n}{(n+1)!} = S(1) = \frac{1 \cdot e^1 - e^1 + 1}{1} = \frac{e - e + 1}{1} = 1 $$         **最终答案：** 幂级数和函数为 $\frac{xe^x - e^x + 1}{x}$ （$x \neq 0$，且 $S(0)=0$）； 常数项级数和为 $1$。

## 幂级数展开（间接法）
我们早就知道了泰勒展开的级数形式 
$$f(x)=\sum_{n=0}^{\infty} \frac{{f^{(n)}(x_{0})}}{n!}(x-x_{0})^n$$
( 麦克劳林展开式 i.e 中心为 $0$ 的展开 ) 
**我们有两种主要的方法** 
1. 代入式 （$k\cdot x^m$ 带入 - 麦克劳林；$k\cdot(x-x_{0})^m$ 带入 - 泰勒）
	**寻找母板（Identify the Base Template）：** 
	* **盯着目标函数**：
	  问自己“它长得最像哪个标准公式？”（例如，是 $\frac{1}{1-u}$、$e^u$、还是 $\sin u$？）。
	* **令换元（Perform Substitution）：** 
	  把标准公式里的自变量 $u$，整体设为题目函数里复杂的那一坨（即 $u = k \cdot x^m$ 或 $u = k \cdot (x - x_0)^m$）。 
	* **逐项代入（Substitute Term-by-Term）：** 
	  将标准展开式 $\sum a_n u^n$ 里的每一个 $u$ 都换成 $k \cdot x^m$。 
	  注意 $(k x^m)^n = k^n x^{mn}$ （系数 $k$ 也要跟着乘方！）。 
	* **求新收敛域（Determine the New Convergence Domain）：** 
	  解不等式 $|u| < R_{母板}$，得到 $|x| < R_{新}$，再单独判断端点。
2. 逐项求导，积分
	设幂级数 $S(x) = \sum_{n=0}^\infty a_n x^n$ 的收敛半径为 $R$（$R>0$），则在收敛区间 $(-R, R)$ 内： 
	**逐项求导**：可以对级数逐项求导，且收敛半径不变。 $$ S'(x) = \sum_{n=1}^\infty n a_n x^{n-1} $$ **逐项积分**：可以对级数逐项积分，且收敛半径不变。 $$ \int_0^x S(t)\,dt = \sum_{n=0}^\infty \frac{a_n}{n+1} x^{n+1} $$ ⚠️ **核心结论**：求导或积分不改变收敛半径 $R$，但极有可能改变端点 $x=\pm R$ 的敛散性（这是考试必考点）。

> [!Danger] Corollary ：基本的泰勒展开
> *   $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$ (收敛域: $(-\infty, +\infty)$)
> *   $\sin x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}$ (收敛域: $(-\infty, +\infty)$)
> *   $\cos x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$ (收敛域: $(-\infty, +\infty)$)
> *   $\ln(1+x) = \sum_{n=1}^{\infty} \frac{(-1)^{n-1} x^n}{n}$ (收敛域: $(-1, 1]$)
> *   $(1+x)^\mu = 1 + \mu x + \frac{\mu(\mu-1)}{2!}x^2 + \dots$ (收敛域: 一般 $|x|<1$)

> [!Example] EXAMPLE
> 1. 求函数  $(1-x)\ln(1-x)$ 在 $x=0$ 处的幂级数展开式
> 2. 用间接法求非初等函数 
> $$F(x)=\int_{0}^{x} e^{-t^2} dt$$
> 的幂级数展开式
> 3. 利用已知的幂级数展开式，求下列函数在 $x=0$ 处的幂级数展开式，并且确定它收敛于该函数的区间 
>$$1) \sin ^{2} x \qquad \qquad 2) \frac{x}{1+x-2x^{2}} $$
>4. 求下列级数在 $x=1$ 处的泰勒展开式
>$$1) f(x)= \frac{1}{x}\qquad \qquad f(x)=\sqrt{ x^3 }$$

**Answer**
1. 
- **题型识别**：乘积形式，含有 $\ln(1-x)$，利用已知展开式  
$$\ln(1-x)=-\sum_{n=1}^{\infty}\frac{x^n}{n}$$
  再乘以 $(1-x)$。
- **操作步骤**
$$(1-x)\ln(1-x)=-(1-x)\sum_{n=1}^{\infty}\frac{x^n}{n} =-\sum_{n=1}^{\infty}\frac{x^n}{n}+\sum_{n=1}^{\infty}\frac{x^{n+1}}{n}$$
  将第二个求和改写为与第一个同次（令 $k=n+1$，则 $n=k-1$）：
$$ =-\sum_{n=1}^{\infty}\frac{x^n}{n}+\sum_{k=2}^{\infty}\frac{x^k}{k-1}$$
  令 $k$ 为 $n$，并分离出第一个求和的第一项（$n=1$）：
  $$=-x-\sum_{n=2}^{\infty}\frac{x^n}{n}+\sum_{n=2}^{\infty}\frac{x^n}{n-1}$$
  合并 $n\ge 2$ 的部分
  $$ =-x+\sum_{n=2}^{\infty}\left(-\frac{1}{n}+\frac{1}{n-1}\right)x^n=-x+\sum_{n=2}^{\infty}\frac{1}{n(n-1)}x^n$$
- **收敛域**：  
  $\ln(1-x)$ 的收敛域为 $[-1,1)$，乘以 $(1-x)$ 不改变收敛域。  
  当 $x=1$ 时，级数 $\sum_{n=2}^{\infty}\frac{1}{n(n-1)}$ 收敛（$p$-级数，$p=2>1$），故整体在 $x=1$ 处也收敛。  
  因此收敛域为 $[-1,1]$。
- **最终答案**：
 $$(1-x)\ln(1-x)=-x+\sum_{n=2}^{\infty}\frac{x^n}{n(n-1)},\qquad x\in[-1,1]$$
 2. 
- **题型识别**：变上限积分，被积函数为 $e^{\square}$，先展开 $e^{-t^2}$，再逐项积分。
- **操作步骤**：  
  展开被积函数（令 $u=-t^2$ 代入 $e^u$）：
$$e^{-t^2}=\sum_{n=0}^{\infty}\frac{(-t^2)^n}{n!}=\sum_{n=0}^{\infty}\frac{(-1)^n t^{2n}}{n!}$$
  逐项积分（从 $0$ 到 $x$）：
$$F(x)=\int_{0}^{x}\sum_{n=0}^{\infty}\frac{(-1)^n t^{2n}}{n!}\,dt=\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}\int_{0}^{x}t^{2n}\,dt=\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}\cdot\frac{x^{2n+1}}{2n+1}$$
- **收敛域**：  
  $e^u$ 的收敛域为 $\mathbb{R}$，代入 $u=-t^2$ 后仍为 $\mathbb{R}$；逐项积分不改变收敛半径。  
  故收敛域为 $\mathbb{R}$。
- **最终答案**：
$$F(x)=\sum_{n=0}^{\infty}\frac{(-1)^n x^{2n+1}}{n!(2n+1)},\qquad x\in\mathbb{R}$$
3. 
 3.1
- **技巧**：用三角恒等式降幂，避免直接平方的卷积运算：
$$\sin^2 x=\frac{1-\cos(2x)}{2}$$
  已知
 $$\cos u=\sum_{n=0}^{\infty}\frac{(-1)^n u^{2n}}{(2n)!}$$
  令 $u=2x$，得
$$\cos(2x)=\sum_{n=0}^{\infty}\frac{(-1)^n (2x)^{2n}}{(2n)!}=\sum_{n=0}^{\infty}\frac{(-1)^n 2^{2n} x^{2n}}{(2n)!}$$
  代入恒等式：
$$\sin^2 x=\frac{1}{2}-\frac{1}{2}\sum_{n=0}^{\infty}\frac{(-1)^n 2^{2n} x^{2n}}{(2n)!} $$
  将 $n=0$ 项单独提出：
$$ \frac{1}{2}\cdot\frac{(-1)^0 2^0 x^0}{0!}=\frac{1}{2}$$
  与前面的 $\frac{1}{2}$ 抵消，得到
$$\sin^2 x=\frac{1}{2}-\frac{1}{2}\left(1+\sum_{n=1}^{\infty}\frac{(-1)^n 2^{2n} x^{2n}}{(2n)!}\right)=-\frac{1}{2}\sum_{n=1}^{\infty}\frac{(-1)^n 2^{2n} x^{2n}}{(2n)!}=\sum_{n=1}^{\infty}\frac{(-1)^{n+1}2^{2n-1} x^{2n}}{(2n)!}$$
- **收敛域**：$\cos u$ 的收敛域为 $\mathbb{R}$，故 $\sin^2 x$ 的展开式收敛域也为 $\mathbb{R}$。
- **最终答案**：
$$\sin^2 x=\sum_{n=1}^{\infty}\frac{(-1)^{n+1}2^{2n-1} x^{2n}}{(2n)!},\qquad x\in\mathbb{R}$$
3.2
- **技巧**：分母因式分解，再拆为部分分式。
  分母：
$$1+x-2x^2=(1-x)(1+2x)$$
  设  
$$\frac{x}{(1-x)(1+2x)}=\frac{A}{1-x}+\frac{B}{1+2x}$$
  解得
$$A=\frac{1}{3},\qquad B=-\frac{1}{3}$$
（计算过程：$x=A(1+2x)+B(1-x)$。令 $x=1$ 得 $1=3A\Rightarrow A=\frac{1}{3}$；令 $x=-\frac{1}{2}$ 得 $-\frac{1}{2}=\frac{3}{2}B\Rightarrow B=-\frac{1}{3}$。）
  于是
$$f(x)=\frac{1}{3}\cdot\frac{1}{1-x}-\frac{1}{3}\cdot\frac{1}{1+2x}$$
  展开：
$$f(x)=\frac{1}{3}\sum_{n=0}^{\infty}x^n-\frac{1}{3}\sum_{n=0}^{\infty}(-2x)^n=\sum_{n=0}^{\infty}\frac{1-(-2)^n}{3}x^n$$
- **收敛域**：  
  第一项要求 $|x|<1$，第二项要求 $|2x|<1\Rightarrow |x|<\frac{1}{2}$。  
  取交集得收敛半径 $R=\frac{1}{2}$。  
  端点 $x=\pm\frac{1}{2}$ 时，通项 $\frac{1-(-2)^n}{3}\left(\pm\frac{1}{2}\right)^n$ 不趋于 $0$，故发散。  
  因此收敛域为 $\left(-\frac{1}{2},\frac{1}{2}\right)$。
- **最终答案**：
$$\frac{x}{1+x-2x^2}=\sum_{n=0}^{\infty}\frac{1-(-2)^n}{3}x^n,\qquad x\in\left(-\frac{1}{2},\frac{1}{2}\right)$$
4. 
4.1
- **核心操作**：令 $t=x-1$，则 $x=1+t$，原函数变为
$$f(x)=\frac{1}{1+t}$$
  利用几何级数公式（注意这里是 $\frac{1}{1+t}$）：
$$\frac{1}{1+t}=\sum_{n=0}^{\infty}(-1)^n t^n,\qquad |t|<1$$
  代回 $t=x-1$：
$$\frac{1}{x}=\sum_{n=0}^{\infty}(-1)^n (x-1)^n$$
- **收敛域**：  
  $|x-1|<1\Rightarrow 0<x<2$。  
  端点 $x=0$ 和 $x=2$ 时通项不趋于 $0$，发散。  
  故收敛域为 $(0,2)$。
- **最终答案**：
$$\boxed{\frac{1}{x}=\sum_{n=0}^{\infty}(-1)^n (x-1)^n,\qquad x\in(0,2)}$$
4.2
- **核心操作**：令 $t=x-1$，则 $x=1+t$，
$$f(x)=(1+t)^{3/2}$$
  用二项式定理（$\mu=\frac{3}{2}$）：
$$(1+t)^{3/2}=\sum_{n=0}^{\infty}\binom{3/2}{n}t^n$$
  其中二项式系数为
$$\binom{3/2}{n}=\frac{\frac{3}{2}\left(\frac{3}{2}-1\right)\cdots\left(\frac{3}{2}-n+1\right)}{n!}$$
  前几项：
$$n=0:\ 1;\qquad n=1:\ \frac{3}{2};\qquad n=2:\ \frac{\frac{3}{2}\cdot\frac{1}{2}}{2!}=\frac{3}{8};\qquad n=3:\ \frac{\frac{3}{2}\cdot\frac{1}{2}\cdot(-\frac{1}{2})}{3!}=-\frac{1}{16}$$
  代回 $t=x-1$：
$$x^{3/2}=\sum_{n=0}^{\infty}\binom{3/2}{n}(x-1)^n$$
- **收敛域**：  
  二项式展开的收敛半径为 $R=1$（唯一奇点在 $t=-1$，即 $x=0$）。  
  端点情况（二项式级数特有的考点）：  
  当 $\mu=\frac{3}{2}>0$ 时，  
  - 在 $t=1$（即 $x=2$）处，级数条件收敛（$\sum \binom{3/2}{n}$ 收敛）；  
  - 在 $t=-1$（即 $x=0$）处，级数也收敛（$\sum (-1)^n\binom{3/2}{n}$ 收敛）。  
  故收敛域为 $|x-1|\le 1$，即 $[0,2]$。
- **最终答案**：
$$x^{3/2}=\sum_{n=0}^{\infty}\binom{3/2}{n}(x-1)^n,\qquad x\in[0,2]$$

# Fourier Series

 1. **系数公式**
设 $f(x)$ 以 $2\pi$ 为周期，则
$$f(x)\sim \frac{a_0}{2}+\sum_{n=1}^{\infty}\bigl(a_n\cos nx+b_n\sin nx\bigr)$$
其中
$$
a_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\cos nx\,dx,\qquad n=0,1,2,\cdots
$$

$$
b_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin nx\,dx,\qquad n=1,2,\cdots
$$
设 $f(x)$ 以 $2L$ 为周期，则
$$
f(x)\sim \frac{a_0}{2}+\sum_{n=1}^{\infty}\left(a_n\cos\frac{n\pi x}{L}+b_n\sin\frac{n\pi x}{L}\right)
$$
其中

$$
a_n=\frac{1}{L}\int_{-L}^{L}f(x)\cos\frac{n\pi x}{L}\,dx,\qquad n=0,1,2,\cdots
$$

$$
b_n=\frac{1}{L}\int_{-L}^{L}f(x)\sin\frac{n\pi x}{L}\,dx,\qquad n=1,2,\cdots
$$


- **1. 利用奇偶性**  
  - 若 $f(x)$ 为奇函数，则 $a_n=0$，展开式只含正弦项（正弦级数）；  
  - 若 $f(x)$ 为偶函数，则 $b_n=0$，展开式只含余弦项（余弦级数）。

- **2.  特殊值求和**  
  利用傅里叶级数在特定点（连续点、间断点、端点）的值，可求出某些数项级数的和。

- **余弦级数 / 正弦级数（补全）**  
  对定义在 $[0,L]$ 上的函数，进行  
  - **偶延拓** → 得到余弦级数；  
  - **奇延拓** → 得到正弦级数。

2. **收敛定理（狄利克雷充分条件，结论）**
若 $f(x)$ 在 $[-\pi,\pi]$ 上满足：
- 连续或只有有限个第一类间断点；
- 只有有限个极值点（即分段单调），
则其傅里叶级数收敛，且
- 在连续点 $x$ 处，收敛于 $f(x)$；
- 在间断点 $x$ 处，收敛于 $\dfrac{f(x^+)+f(x^-)}{2}$。

2. 黎曼-勒贝格定理（结论）
若 $f(x)$ 在 $[-\pi,\pi]$ 上可积（或绝对可积），则其傅里叶系数满足
$$
a_n\to 0,\qquad b_n\to 0\qquad (n\to\infty).
$$
该定理说明傅里叶系数趋于零，是傅里叶级数收敛的必要条件。

> [!Example] EXAMPLE
> 1. 将 $f(x)=x$ 分别于 $-\pi<x<\pi$ 和 $0<x<2\pi$ 展开傅里叶级数
> 2. 把 $f(x)=x$ 在 $(0,2)$ 分别展开成
> 	- 正弦级数
> 	- 余弦级数


 1. 函数 $f(x)=x$ 在区间 $(-\pi,\pi)$ 上展开，并以 $2\pi$ 为周期进行周期延拓。由于 $f(x)=x$ 是奇函数，有
$$
a_0=0,\qquad a_n=0\quad (n=1,2,\cdots)
$$
$$
b_n=\frac{1}{\pi}\int_{-\pi}^{\pi}x\sin(nx)\,dx
=\frac{2}{\pi}\int_{0}^{\pi}x\sin(nx)\,dx
=\frac{2(-1)^{n+1}}{n}
$$
因此傅里叶级数为
$$
x\sim 2\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n}\sin(nx),\qquad -\pi<x<\pi
$$
在 $x=\pm\pi$ 处，级数收敛到 $0$。

 2. 函数 $f(x)=x$ 在区间 $(0,2\pi)$ 上展开，并以 $2\pi$ 为周期进行周期延拓。
$$
a_0=\frac{1}{\pi}\int_{0}^{2\pi}x\,dx=2\pi
$$
$$
a_n=\frac{1}{\pi}\int_{0}^{2\pi}x\cos(nx)\,dx=0
$$
$$
b_n=\frac{1}{\pi}\int_{0}^{2\pi}x\sin(nx)\,dx=-\frac{2}{n}
$$
所以傅里叶级数为
$$
x\sim \pi-2\sum_{n=1}^{\infty}\frac{\sin(nx)}{n},\qquad 0<x<2\pi
$$
在 $x=0,2\pi$ 处，级数收敛到 $\pi$。

3. 在区间 $(0,2)$ 上将 $f(x)=x$ 展开成正弦级数。取奇延拓，周期为 $4$，即 $L=2$。
$$
b_n=\int_{0}^{2}x\sin\left(\frac{n\pi x}{2}\right)\,dx
=\frac{4(-1)^{n+1}}{n\pi}
$$
因此正弦级数为
$$
x\sim \frac{4}{\pi}\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n}\sin\left(\frac{n\pi x}{2}\right),\qquad 0<x<2
$$
在端点 $x=0,2$ 处，正弦级数收敛到 $0$。

4. 
在区间 $(0,2)$ 上将 $f(x)=x$ 展开成余弦级数。取偶延拓，周期为 $4$，即 $L=2$。
$$
a_0=\int_{0}^{2}x\,dx=2
$$
常数项为 $\displaystyle \frac{a_0}{2}=1$。
$$
a_n=\int_{0}^{2}x\cos\left(\frac{n\pi x}{2}\right)\,dx
=
\begin{cases}
-\dfrac{8}{n^2\pi^2}, & n\text{ 为奇数},\\[6pt]
0, & n\text{ 为偶数}.
\end{cases}
$$
因此余弦级数为
$$
x\sim 1-\frac{8}{\pi^2}\sum_{k=0}^{\infty}
\frac{\cos\left(\frac{(2k+1)\pi x}{2}\right)}{(2k+1)^2},
\qquad 0\le x\le 2
$$
即
$$
x\sim 1-\frac{8}{\pi^2}
\left[
\frac{\cos\left(\frac{\pi x}{2}\right)}{1^2}
+\frac{\cos\left(\frac{3\pi x}{2}\right)}{3^2}
+\frac{\cos\left(\frac{5\pi x}{2}\right)}{5^2}
+\cdots
\right]
$$
余弦级数在端点也收敛到 $f(x)$，所以在 $[0,2]$ 上成立。