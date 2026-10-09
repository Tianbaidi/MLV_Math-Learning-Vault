# 第 5 章 Riemann 积分、曲线积分及曲面积分

## 5.1 Riemann 积分

> [!question] 例 5.1.1
>
> 设 $0 < \alpha < 1$, 证明数列
>
> $$a_{n} = \frac{1}{1+n^{\alpha}} + \frac{1}{2+n^{\alpha}} + \cdots + \frac{1}{n+n^{\alpha}}, \quad n = 1, 2, \cdots$$
>
> 发散.

> [!question] 例 5.1.2
>
> 计算
>
> $$\lim_{n \rightarrow +\infty} \left( \frac{n}{1^{2} + \sqrt{n} + n^{2}} + \frac{n}{2^{2} + 2\sqrt{n} + n^{2}} + \cdots + \frac{n}{n^{2} + n\sqrt{n} + n^{2}} \right).$$

> [!question] 例 5.1.3
>
> 求证 $\lim_{n \rightarrow +\infty} \prod_{k=1}^{n} \left(1 + \frac{k}{n}\right)^{1/n}$ 收敛.

> [!question] 例 5.1.4
>
> 设 $\varphi$ 在 $\left[0, \frac{\pi}{2}\right]$ 可积, 满足 $\lim_{x \to \frac{\pi}{2}} \varphi(x) = 0$. 求证:
>
> $$\lim_{n \to +\infty} \frac{\int_{0}^{\pi/2} \sin^n x \varphi(x) \mathrm{d}x}{\int_{0}^{\pi/2} \sin^n x \mathrm{d}x} = 0.$$

> [!question] 例 5.1.5
>
> 设 $f: [0, +\infty) \to [0, +\infty)$ 是连续函数，且满足
> $$\lim_{x \to +\infty} f(x) \int_{0}^{x} f(t) \mathrm{d}t = a \in (0, +\infty).$$
> 求证：$\lim_{x \to +\infty} \sqrt{x} f(x)$ 存在且为正数.

> [!question] 例 5.1.6
>
> 设 $\varphi$ 是 $\mathbb{R}$ 上周期为 1 的函数，且在 $[0, 1]$ 上可积，$f$ 在 $[0, 1]$ 上可积.求证：
> $$\lim_{n \to +\infty} \int_{0}^{1} f(x) \varphi(nx) \mathrm{d}x = \int_{0}^{1} f(x) \mathrm{d}x \int_{0}^{1} \varphi(x) \mathrm{d}x.$$

> [!question] 例 5.1.7
>
> (Riemann-Lebesgue 引理) 设 $f$ 在 $[a,b]$ 上可积，则有
>
> $$\lim_{p \to \infty} \int_a^b f(x)\sin(px)\mathrm{d}x = 0, \lim_{p \to \infty} \int_a^b f(x)\cos(px)\mathrm{d}x = 0.$$

> [!question] 例 5.1.8
>
> 设 $\varphi$ 是 $\mathbb{R}$ 上周期为 1 的函数，在 $[0,1]$ 上可积，且 $\int_0^1 \varphi(x)\mathrm{d}x = 0, f$ 在 $[0,1]$ 上可导且 $f'$ 可积. 求证:
>
> $$\lim_{n \to +\infty} n \int_0^1 f(x)\varphi(nx)\mathrm{d}x = \int_0^1 f'(x)\mathrm{d}x \int_0^1 x\varphi(x)\mathrm{d}x.$$

> [!question] 例 5.1.9
>
> 设 $f$ 是 $[0,1]$ 上的单调函数. 求证: 对任意实数 $a$ 有
>
> $$\int_0^1 |f(x) - a| \mathrm{d}x \geqslant \int_0^1 \left|f(x) - f\left(\frac{1}{2}\right)\right| \mathrm{d}x. \quad (5.1.1)$$

> [!question] 例 5.1.10
>
> 计算积分 $I = \int_{-1}^{2} \frac{1+x^2}{1+x^4} \mathrm{d}x$.

> [!question] 例 5.1.11
>
> 若 $[a, b]$ 上的可积函数列 $\{f_n\}$ 在 $[a, b]$ 上一致收敛于函数 $f$, 则 $f$ 在 $[a, b]$ 上可积.

> [!question] 例 5.1.12
>
> 设 $f$ 在 $[a,b]$ 上非负可积. 求证: 数列 $I_n = \left(\frac{1}{b-a} \int_a^b f^n(x) \mathrm{d}x\right)^{\frac{1}{n}}$ 是单调递增的.

> [!question] 例 5.1.13
>
> 设 $f$ 在 $[a,b]$ 上连续可导，且 $f(a)=0$. 求证：对 $p \geqslant 1$ 有
>
> $$\int_{a}^{b}|f(x)|^{p} \mathrm{d}x \leqslant \frac{1}{p} \int_{a}^{b}[(b-a)^{p}-(x-a)^{p}]|f'(x)|^{p} \mathrm{d}x.$$

> [!question] 例 5.1.14
>
> 设 $f$ 是 $[0,a]$ 上的连续函数，且存在正常数 $M,c$ 使得
>
> $$|f(x)| \leqslant M + c \int_{0}^{x}|f(t)| \mathrm{d}t,$$
>
> 求证：$|f(x)| \leqslant M \mathrm{e}^{cx} (\forall x \in [0,a])$.

> [!question] 例 5.1.15
>
> 设 $f$ 在区间 $[0, 1]$ 上可积且满足
>
> $$\int_{0}^{1} f(x) \mathrm{d}x = \int_{0}^{1} xf(x) \mathrm{d}x = 1.$$
>
> 求证: $\int_{0}^{1} f^{2}(x) \mathrm{d}x \geqslant 4.$

> [!question] 例 5.1.16
>
> 设 $f$ 在区间 $[0, 1]$ 上连续且对任意 $x, y \in [0, 1]$, 有
>
> $$xf(y) + yf(x) \leqslant 1.$$
>
> 求证: $\int_{0}^{1} f(x) \mathrm{d}x \leqslant \frac{\pi}{4}.$

> [!question] 例 5.1.17
>
> 设 $f$ 在区间 $[0, 1]$ 上有可积的导函数且满足 $f(0) = 0, f(1) = 1$. 求证: 对任意 $a \geqslant 0$ 有
>
> $$\int_{0}^{1} \left| a f(x) + f'(x) \right| \mathrm{d}x \geqslant 1.$$

> [!question] 例 5.1.18
>
> 设 $f$ 是 $[a, b]$ 上单调递增的连续函数. 求证
>
> $$\int_{a}^{b} x f(x) \mathrm{d}x \geqslant \frac{a+b}{2} \int_{a}^{b} f(x) \mathrm{d}x.$$

> [!question] 例 5.1.19
>
> 设 $f$ 是区间 $[0,1]$ 上的连续函数并满足 $0 \leqslant f(x) \leqslant x$. 求证:
>
> $$\int_{0}^{1} f(x) \mathrm{d}x - \left(\int_{0}^{1} f(x) \mathrm{d}x\right)^{2} \geqslant \int_{0}^{1} x^{2} f(x) \mathrm{d}x \geqslant \left(\int_{0}^{1} f(x) \mathrm{d}x\right)^{2}.$$
>
> 并求使上式成为等式的所有正连续函数 $f$.

> [!question] 例 5.1.20
>
> 求在 $[0,1]$ 上的可导函数, 并且满足 $f(0) = 0, 0 < f'(x) \leqslant 1 (x > 0)$ 以及
>
> $$\int_{0}^{1} f^{3}(x) \mathrm{d}x = \left(\int_{0}^{1} f(x) \mathrm{d}x\right)^{2}.$$

> [!question] 例 5.1.21
>
> 设 $f$ 在 $[a,b]$ 上连续且 $0 \leqslant f \leqslant M$. 求证:
>
> $$0 \leqslant \left[ \int_a^b f(x) \mathrm{d}x \right]^2 - \left[ \int_a^b f(x) \cos x \mathrm{d}x \right]^2 - \left[ \int_a^b f(x) \sin x \mathrm{d}x \right]^2 \leqslant \frac{M^2(b-a)^4}{12}.$$

> [!question] 例 5.1.22
>
> 设 $f$ 在 $[0,1]$ 上正的单调递减函数. 求证:
>
> $$\frac{\int_{0}^{1} x f^{2}(x) \mathrm{d}x}{\int_{0}^{1} x f(x) \mathrm{d}x} \leqslant \frac{\int_{0}^{1} f^{2}(x) \mathrm{d}x}{\int_{0}^{1} f(x) \mathrm{d}x}.$$ (5.1.2)

> [!question] 例 5.1.23
>
> 设 $f$ 在 $[0,2]$ 上可导且 $|f'| \leqslant 1, f(0) = f(2) = 1$. 求证:
>
> $$1 \leqslant \int_{0}^{2} f(x) \mathrm{d}x \leqslant 3.$$

> [!question] 例 5.1.24
>
> 设 $f$ 在区间 $[0, 1]$ 上连续可导，且 $f(0) = f(1) = 0$. 求证:
>
> $$\left(\int_{0}^{1} f(x) \mathrm{d}x\right)^{2} \leqslant \frac{1}{12} \int_{0}^{1} \left(f'(x)\right)^{2} \mathrm{d}x,$$
>
> 且等号成立当且仅当 $f(x) = Ax(1 - x)$，其中 $A$ 是常数.

> [!question] 例 5.1.25
>
> 设 $f, g$ 是区间 $[0, 1]$ 上的连续函数，使得对 $[0, 1]$ 上任意满足 $\varphi(0) = \varphi(1) = 0$ 的连续可导函数 $\varphi$ 有
>
> $$\int_{0}^{1}\left[f(x)\varphi'(x) + g(x)\varphi(x)\right] \mathrm{d}x = 0.$$
>
> 求证: $f$ 可导，且 $f' = g$.

> [!question] 例 5.1.26
>
> 设 $f$ 是区间 $[a,b]$ 上的严格单调递减连续函数，$f(a)=b, f(b)=a, g$ 是 $f$ 的反函数. 求证:
>
> $$\int_{a}^{b} f(x) \mathrm{d}x = \int_{a}^{b} g(x) \mathrm{d}x.$$

> [!question] 例 5.1.27
>
> 设 $f$ 是区间 $[a,b]$ 上的连续可微函数. 求证:
>
> $$\max_{a \leqslant x \leqslant b} f(x) \leqslant \frac{1}{b-a} \left( \int_{a}^{b} f(x) \mathrm{d}x + \int_{a}^{b} |f'(x)| \mathrm{d}x \right).$$

> [!question] 例 5.1.28
>
> 设 $\alpha \in \left[0, \frac{1}{2}\right], f \in C^{1}[0,1]$ 且满足 $f(1)=0$. 求证:
>
> $$\int_{0}^{1} |f(x)|^{2} \mathrm{d}x + \left(\int_{0}^{1} |f(x)| \mathrm{d}x\right)^{2} \leqslant \frac{4}{3-4\alpha} \int_{0}^{1} x^{2\alpha+1} |f'(x)|^{2} \mathrm{d}x.$$

> [!question] 例 5.1.29
>
> 设 $f$ 在 $[0,1]$ 上非负且连续可导. 求证:
>
> $$\left| \int_{0}^{1} f^{3}(x) \mathrm{d}x - f^{2}(0) \int_{0}^{1} f(x) \mathrm{d}x \right| \leqslant \max_{0 \leqslant x \leqslant 1} |f'(x)| \left( \int_{0}^{1} f(x) \mathrm{d}x \right)^{2}.$$

> [!question] 例 5.1.30
>
> 设 $f$ 在 $[0,1]$ 上非负单调递增连续函数, $0 < \alpha < \beta < 1$. 求证:
>
> $$\int_{0}^{1} f(x) \mathrm{d}x \geqslant \frac{1-\alpha}{\beta-\alpha} \int_{\alpha}^{\beta} f(x) \mathrm{d}x,$$
>
> 并且 $\frac{1-\alpha}{\beta-\alpha}$ 不能换为更大的数.

> [!question] 例 5.1.31
>
> 设函数 $f$ 在 $[0,1]$ 上连续的二阶导函数，$f(0)=f(1)=0, f'(1)=\frac{a}{2}$. 求证：
>
> $$\int_{0}^{1} x(f''(x))^{2} \mathrm{d}x \geqslant \frac{a^{2}}{2}.$$
>
> 并求上式成为等式的 $f$.

> [!question] 例 5.1.32
>
> 设 $n$ 是正整数，且 $m>2$. 求证：
>
> $$\int_{0}^{\pi/2} t \left| \frac{\sin nt}{\sin t} \right|^{m} \mathrm{d}t \leqslant \left( \frac{m \cdot n^{m-2}}{8(m-2)} - \frac{1}{4(m-2)} \right) \pi^{2}.$$

> [!question] 例 5.1.33
>
> 设 $n \geqslant 1$ 是自然数. 求证:
>
> $$\frac{1}{\pi} \int_{0}^{\pi/2} \frac{|\sin(2n+1)t|}{\sin t} \mathrm{d}t < \frac{2n^{2}+1}{2n^{2}+n} + \frac{1}{2} \ln n.$$

> [!question] 例 5.1.34
>
> 设 $f \neq 0$, 在 $[a,b]$ 上可微, $f(a) = f(b) = 0$. 求证: 至少存在一点 $c \in [a,b]$ 使
>
> $$|f'(c)| > \frac{4}{(b-a)^2} \int_{a}^{b} |f(x)| \mathrm{d}x.$$

> [!question] 例 5.1.35
>
> 设 $f$ 是区间 $[0, 1]$ 上的凸函数. 求证：对一切 $t \in [0, 1]$，有
>
> $$t(1-t)f(t) \leqslant (1-t)^2 \int_{0}^{t} f(x) \mathrm{d}x + t^2 \int_{t}^{1} f(x) \mathrm{d}x.$$

> [!question] 例 5.1.36
>
> 设 $f$ 在区间 $[0,a)$ 上有二阶连续导数, 满足 $f(0) = f'(0) = 0$ 且 $f''(x) > 0 (0 < x < a)$. 求证: 对任意 $x \in (0,a)$, 有
>
> $$\int_{0}^{x} \sqrt{1+(f'(t))^{2}} \mathrm{d}t < x + \frac{f(x)f'(x)}{\sqrt{1+(f'(x))^{2}}+1}.$$
>
> (5.1.15)

> [!question] 例 5.1.37
>
> 设 $a > 1$, 计算积分 $\int_{0}^{\frac{\pi}{2}} \ln(a^{2}-\cos^{2}x) \mathrm{d}x$.

> [!question] 例 5.1.38
>
> 计算积分 $I = \int_{0}^{1} \frac{\ln(1+x)}{1+x^{2}} \mathrm{d}x.$

> [!question] 例 5.1.39
>
> 设 $f$ 和 $g$ 是 $[0,1]$ 上单调函数，且单调性相同，求证:
> $$\int_{0}^{1} f(x)g(x) \mathrm{d}x \geqslant \int_{0}^{1} f(x) \mathrm{d}x \int_{0}^{1} g(x) \mathrm{d}x.$$

> [!question] 例 5.1.40
>
> $f$ 是区间 $[0,1]$ 上的正连续函数，$k \geqslant 1$. 求证:
> $$\int_{0}^{1} \frac{1}{1 + f(x)} \mathrm{d}x \int_{0}^{1} f(x) \mathrm{d}x \leqslant \int_{0}^{1} \frac{f^{k+1}(x)}{1 + f(x)} \mathrm{d}x \int_{0}^{1} \frac{1}{f^{k}(x)} \mathrm{d}x,$$
> (5.1.19)
>
> 并讨论等号成立的条件.

> [!question] 例 5.1.41
>
> 设 $b \geqslant a + 2$. 函数 $f$ 在 $[a, b]$ 上为正连续函数, 且
>
> $$\int_{a}^{b} \frac{1}{1+f(x)} \mathrm{d}x = 1.$$
>
> 求证:
> $$\int_{a}^{b} \frac{f(x)}{b-a-1+f^2(x)} \mathrm{d}x \leqslant 1.$$ (5.1.21)
>
> 并求式 (5.1.21) 成为等式的条件.

> [!question] 例 5.1.42
>
> 设 $f$ 是 $[0, \pi]$ 上连续函数, 且满足
>
> $$\int_0^\pi f(x)\sin x\mathrm{d}x = \int_0^\pi f(x)\cos x\mathrm{d}x = 0.$$
>
> 求证: $f$ 在 $(0, \pi)$ 中至少有两个零点.

> [!question] 例 5.1.43
>
> 设 $f \in C([0, \pi])$, 证明: 不能同时有
>
> $$\int_0^\pi |f(x) - \sin x|^2\mathrm{d}x < \frac{\pi}{4} \quad \text{和} \quad \int_0^\pi |f(x) - \cos x|^2\mathrm{d}x < \frac{\pi}{4}. \tag{5.1.22}$$
>
> 又问何时上面的两个不等式成为等式?

> [!question] 例 5.1.44
>
> 设 $f$ 是 $(-\infty, +\infty)$ 上连续函数, 且在 $(-\infty, a] \cup [b, +\infty)$ 上等于零.
>
> 又设
>
> $$\varphi(x) = \frac{1}{2h} \int_{x-h}^{x+h} f(t) \mathrm{d}t \quad (h > 0).$$
>
> 求证: $\int_{a}^{b} |\varphi(x)| \mathrm{d}x \leqslant \int_{a}^{b} |f(x)| \mathrm{d}x$.

> [!question] 例 5.1.45
>
> 设 $f$ 在区间 $[1, +\infty)$ 上连续并满足
>
> $$x\int_{1}^{x}f(t)\mathrm{d}t = (x+1)\int_{1}^{x}tf(t)\mathrm{d}t.$$ (5.1.23)
>
> 求 $f$.

> [!question] 例 5.1.46
>
> 设 $f$ 在任意有限区间上可积, 且对任意 $x$ 及任意 $a \neq 0$ 满足
>
> $$\frac{1}{2a} \int_{x-a}^{x+a} f(t) \mathrm{d}t = f(x).$$
>
> 试求函数 $f$.

> [!question] 例 5.1.47
>
> 设 $f$ 是 $\mathbb{R}$ 上有下界的连续函数. 若存在常数 $a \in (0,1]$ 使得
>
> $$f(x) - a \int_{x}^{x+1} f(t) \mathrm{d}t$$
>
> 为常数, 则 $f$ 无穷可微且它的任意阶导函数都是非负的.

> [!question] 例 5.1.48
>
> 求所有连续函数 $f: \mathbb{R} \rightarrow \mathbb{R}$ 使得对任意 $x \in \mathbb{R}$ 和任意正整数 $n$, 有
> $$n^2 \int_x^{x+\frac{1}{n}} f(t) \mathrm{d}t = n f(x) + \frac{1}{2}.$$

> [!question] 例 5.1.49
>
> 设 $f \in C[-1,1]$ 且对任意整数 $n$ 满足
>
> $$\int_{0}^{1} f(\sin(nx)) \mathrm{d}x = 0.$$
>
> (5.1.36)
>
> 求证: 对任意 $x \in [-1,1]$ 有 $f(x) = 0$.

> [!question] 例 5.1.50
>
> 设 $f$ 是 $[0,2\pi]$ 上可导的凸函数, $f'$ 有界, 试证
>
> $$a_n = \frac{1}{\pi} \int_0^{2\pi} f(x) \cos nx \mathrm{d}x \geqslant 0.$$

> [!question] 例 5.1.51
>
> 设 $f$ 是 $[0,1]$ 上正的可导函数, 且满足 $|f'| \leqslant 1$. 记
>
> $$m = \min f(x), \quad M = \max f(x), \quad \beta = \int_0^1 \frac{1}{f(x)} \mathrm{d}x.$$
>
> 求证: $M \leqslant m \mathrm{e}^{\beta}.$

> [!question] 例 5.1.52
>
> 设 $f$ 是 $[0,1]$ 上正的可导函数，且满足 $|f'| \leqslant 1$. 记
>
> $$m = \min f(x), \quad M = \max f(x), \quad \beta = \int_{0}^{1} \frac{1}{f(x)} \mathrm{d}x. \tag{5.1.37}$$
>
> 求证：对 $n > -1$，有
>
> $$\int_{0}^{1} f^{n}(x) \mathrm{d}x \leqslant \frac{m^{n+1}}{n+1}\left(\mathrm{e}^{(n+1)\beta} - 1\right). \tag{5.1.38}$$

> [!question] 例 5.1.53
>
> 设 $f \in C[a,b]$ 是一个正的连续函数, 且满足 Lipschitz 条件
>
> $$|f(x) - f(y)| \leqslant L |x - y|.$$
>
> 对于区间 $[c,d] \subset [a,b]$, 记
>
> $$\beta = \int_{a}^{b} \frac{1}{f(x)} \mathrm{d}x, \quad \alpha = \int_{c}^{d} \frac{1}{f(x)} \mathrm{d}x.$$
>
> 求证:
>
> $$\int_{a}^{b} f(x) \mathrm{d}x \leqslant \frac{\mathrm{e}^{2L\beta}-1}{2L\alpha} \int_{c}^{d} f(x) \mathrm{d}x. \tag{5.1.42}$$

> [!question] 例 5.1.54
>
> 设 $f$ 在 $[0,1]$ 上连续可微, $f(0) = 0$. 求证:
>
> $$\int_0^1 \frac{f^2(x)}{x^2} \mathrm{d}x \leqslant 4 \int_0^1 \left(f'(x)\right)^2 \mathrm{d}x,$$
>
> 且右边的系数 4 是最佳的.

> [!question] 例 5.1.55
>
> 设 $f, g: [a, b] \to (0, +\infty)$ 都是连续函数，且 $f \neq g$, $\int_{a}^{b} f(x) \mathrm{d}x = \int_{a}^{b} g(x) \mathrm{d}x$. 定义数列
> $$I_{n} = \int_{a}^{b} \frac{f^{n+1}(x)}{g^{n}(x)} \mathrm{d}x, \quad n = 0, 1, \dots.$$
> 求证: $\{I_{n}\}$ 严格单调递增，且 $\lim_{n \to +\infty} I_{n} = +\infty$.

> [!question] 例 5.1.56
>
> 设 $f: \mathbb{R} \rightarrow \mathbb{R}$ 连续, 定义 $g(x) = f(x) \int_{0}^{x} f(t) \mathrm{d}t (x \in \mathbb{R})$. 如果 $g$ 是 $\mathbb{R}$ 上的递减函数, 求证: $f \equiv 0$.

> [!question] 例 5.1.57
>
> 设 $f \in C[0,1]$. 如果对任意 $x \in [0,1]$ 有
>
> $$\int_{0}^{x} f(t) \mathrm{d}t \geqslant f(x) \geqslant 0,$$
>
> 求证: $f(x) \equiv 0$.

> [!question] 例 5.1.58
>
> 设 $f$ 是区间 $[a,b]$ 上的可积函数. 求证: 对任意正数 $\varepsilon$, 存在多项式 $P(x)$ 使得
>
> $$\int_{a}^{b}|f(x)-P(x)|\mathrm{d}x \leqslant \varepsilon.$$

> [!question] 例 5.1.59
>
> 区间 $[a,b]$ 上可积函数 $f$ 的 $n$ 次矩定义为 $\int_{a}^{b} x^{n} f(x) \mathrm{d}x = 0, n = 0, 1, 2, \cdots$. 设 $f$ 是 $[a,b]$ 上的连续函数, 且所有次矩都为零. 求证: $f(x) \equiv 0$.

> [!question] 例 5.1.60
>
> 设 $f \in C[0,\pi]$ 满足: 对 $n = 0,1,2,\cdots$, 有 $\int_{0}^{\pi} f(x) \cos nx \mathrm{d}x = 0$. 求证: $f(x) \equiv 0$.

> [!question] 例 5.1.61
>
> 设 $g$ 是 $[0,1]$ 上的连续函数且 $\lim_{x \to 0^{+}} \frac{g(x)}{x}$ 收敛. 求证: 对任意 $[0,1]$ 上的连续函数 $f$, 有
>
> $$\lim_{n \to +\infty} n \int_{0}^{1} f(x) g(x^{n}) \mathrm{d}x = f(1) \int_{0}^{1} \frac{g(x)}{x} \mathrm{d}x.$$

> [!question] 例 5.1.62
>
> 设 $f(x)$ 是 $[0,1]$ 上的凹函数, 且 $f(1) = 1$. 求证:
>
> $$\int_{0}^{1} f^2(x) \mathrm{d}x \geqslant \frac{1}{4},$$
>
> (5.1.49)
>
> $$\int_{0}^{1} f^2(x) \mathrm{d}x \geqslant \frac{2}{3} \int_{0}^{1} f(x) \mathrm{d}x.$$
>
> (5.1.50)

> [!question] 例 5.1.63
>
> (Favard (法瓦尔) 不等式) 若 $f$ 是区间 $[0,1]$ 上的非负凹函数, 则有对 $p \geqslant 1$,
>
> $$\int_0^1 f^p(x) \mathrm{d}x \leqslant \frac{2^p}{p + 1} \left( \int_0^1 f(x) \mathrm{d}x \right)^p.$$

> [!question] 例 5.1.64
>
> 求定义在星形区域 $D = \{(x,y) | x^{\frac{2}{3}} + y^{\frac{2}{3}} \leqslant 1\}$ 上满足 $f(1,0) = 1$ 的正值连续函数 $f$ 使得 $\iint_{D} \frac{f(x,y)}{f(y,x)} \mathrm{d}x \mathrm{d}y$ 达到最小, 并求出这个最小值.

> [!question] 例 5.1.65
>
> 求证: $\iint_{[0,1]^2} (xy)^{xy} \mathrm{d}x \mathrm{d}y = \int_0^1 t^t \mathrm{d}t$.

> [!question] 例 5.1.66
>
> 计算二重积分 $I = \iint_D \operatorname{sgn} \left(x^2 - y^2 + 2\right) \mathrm{d}x \mathrm{d}y$, 其中
>
> $$D = \{(x,y) | x^2 + y^2 \leqslant 4\}.$$

> [!question] 例 5.1.67
>
> 设 $D = \{(x, y) \mid x^2 + y^2 \leqslant 1\}$. 求 $I = \iint_{D} \left| \frac{x + y}{\sqrt{2}} - x^2 - y^2 \right| \mathrm{d}x \mathrm{d}y$.

> [!question] 例 5.1.68
>
> 试求圆盘 $(x-a)^{2}+(y-a)^{2} \leqslant a^{2}$ 与曲线 $(x^{2}+y^{2})^{2}=8a^{2}xy$ 所围部分相交的区域 $D$ 的面积 $S$.

> [!question] 例 5.1.69
>
> 计算曲面 $(x^2 + y^2)^2 + z^4 = y$ 所围的区域 $V$ 的体积 $\sigma(V)$.

> [!question] 例 5.1.70
>
> 计算三重积分
> $$\iiint_V (x^2 + y^2)^5 z \mathrm{d}x \mathrm{d}y \mathrm{d}z,$$
>
> 其中 $V$ 是圆柱体 $x^2 + y^2 \leqslant 1$ 被曲面 $z = \sqrt{3x^2 + y^2 + 1}$ 及 $Oxy$ 平面所截下的部分.

> [!question] 例 5.1.71
>
> 求曲面 $(x^2 + y^2 + z^2)^2 = a^3 z (a > 0)$ 所围成的立体体积.

> [!question] 例 5.1.72
>
> 如图 5.1.3, 设 $P$ 是圆 $(x-a)^2+y^2=a^2 (a>0)$ 上的动点. 从原点往圆过 $P$ 点的切线作垂线, 垂足为 $Q$. 当 $P$ 沿圆运动时, 点 $Q$ 的轨迹是 $Oxy$ 平面上一条封闭曲线. 求此封闭曲线围成区域 $D$ 的面积.
>
> ![[assets/图5.1.3.png]]

> [!question] 例 5.1.73
>
> 如图 5.1.4, 设 $P$ 是球面 $B: x^2+y^2+(z-a)^2=a^2 (a>0)$ 上的动点. 从原点往球面过 $P$ 点的切平面作垂线, 垂足为 $Q$. 当 $P$ 在球面上运动时, 点 $Q$ 的轨迹是 $\mathbb{R}^3$ 中一个包含 $B$ 封闭曲面 $S$. 求 $S$ 所围成的区域 $V$ 的体积.
>
> ![[assets/图5.1.4.png]]

> [!question] 例 5.1.74
>
> 设 $a, b$ 是不全为 0 的常数. 求证:
>
> $$\iint_{x^2+y^2 \leqslant 1} f(ax+by+c) \mathrm{d}x \mathrm{d}y = 2 \int_{-1}^{1} \sqrt{1-t^2} f\left(t \sqrt{a^2+b^2}+c\right) \mathrm{d}t.$$

> [!question] 例 5.1.75
>
> 计算三重积分
>
> $$I = \iiint_{x^2 + 4y^2 + 9z^2 \leqslant 4x + 8y + 6z} \left(x^2 + y^2 + z^2\right) \mathrm{d}x \mathrm{d}y \mathrm{d}z.$$

> [!question] 例 5.1.76
>
> 设 $a,b,c$ 是常数, $k = \sqrt{a^2 + b^2 + c^2}$. 函数 $f$ 在 $[-k,k]$ 上连续. 求证:
>
> $$\iiint_{V} f\left(\frac{ax + by + cz}{\sqrt{x^2 + y^2 + z^2}}\right) \mathrm{d}x \mathrm{d}y \mathrm{d}z = \frac{2}{3}\pi \int_{-1}^{1} f(kt) \mathrm{d}t,$$
>
> 其中 $V: x^2 + y^2 + z^2 \leqslant 1$ 是单位球体.

> [!question] 例 5.1.77
>
> 求椭球 $\frac{x^2}{2} + \frac{y^2}{3} + \frac{z^2}{4} \leqslant 1$ 被平面 $x+y+z=1$ 切下的两部分中体积较小的那一部分的体积.

> [!question] 例 5.1.78
>
> 计算三重积分
>
> $I = \iiint_{[0,1]^3} \frac{\mathrm{d}u \mathrm{d}v \mathrm{d}w}{(1 + u^2 + v^2 + w^2)^2}$.

> [!question] 例 5.1.79
>
> 设 $f$ 是定义在 $[a,b] \times [c,d]$ 上的连续函数. 求证:
> $$\left[ \int_{a}^{b} \mathrm{d}x \left( \int_{c}^{d} f(x,y) \mathrm{d}y \right)^{2} \right]^{\frac{1}{2}} \leqslant \int_{c}^{d} \mathrm{d}y \left( \int_{a}^{b} f^{2}(x,y) \mathrm{d}x \right)^{\frac{1}{2}}.$$ (5.1.52)

> [!question] 例 5.1.80
>
> 设 $f$ 是定义在正方形 $S = \{(x,y)|0 \leqslant x \leqslant 1,0 \leqslant y \leqslant 1\}$ 上的四阶连续可微函数, 在 $S$ 的边界上为零, 并且
> $$\left| \frac{\partial^{4} f}{\partial x^{2} \partial y^{2}} \right| \leqslant M.$$
> 求证: $\left| \iint_{S} f(x,y) \mathrm{d}x \mathrm{d}y \right| \leqslant \frac{1}{144} M.$

> [!question] 例 5.1.81
>
> (Poincaré (庞加莱) 不等式) 设 $\varphi, \psi$ 是 $[a,b]$ 上的连续函数, $f$ 在区域 $D = \{(x,y) | a \leqslant x \leqslant b, \varphi(x) \leqslant y \leqslant \psi(x)\}$ 上连续可微, 且有 $f(x, \varphi(x)) = 0 (x \in [a,b])$. 则存在 $M > 0$, 使得
> $$\iint_D f^2(x,y) \mathrm{d}x \mathrm{d}y \leqslant M \iint_D \left(f_y'(x,y)\right)^2 \mathrm{d}x \mathrm{d}y.$$

> [!question] 例 5.1.82
>
> 设 $a > 0, \Omega_n(a): x_1 + x_2 + \cdots + x_n \leqslant a, x_i \geqslant 0 (i = 1, 2, \cdots, n)$. 求积分
>
> $$I_n(a) = \int_{\Omega_n(a)} \cdots \int x_1 x_2 \cdots x_n \mathrm{d}x_1 \mathrm{d}x_2 \cdots \mathrm{d}x_n.$$

## 5.2 曲线积分

> [!question] 例 5.2.1
>
> 求第一型曲线积分 $\int_{L} \sqrt{x^2+y^2} \mathrm{d}s$，其中 $L$ 是圆周 $x^2+y^2=ax (a>0)$.

> [!question] 例 5.2.2
>
> 设曲线 $L$ 为椭圆 $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 (a>0, b>0)$ 在第一象限的弧段，计算曲线积分 $\int_{L} xy \mathrm{d}s$.

> [!question] 例 5.2.3
>
> 求曲线积分 $\int_{L} x \mathrm{d}s$，其中 $L$ 是以平面上 $O(0,0), A(1,0), B(0,1)$ 为顶点的三角形的边界.

> [!question] 例 5.2.4
>
> 求曲线积分 $\int_{L} xy \mathrm{d}s$, 其中 $L$ 是球面 $x^2 + y^2 + z^2 = a^2$ 与平面 $x + y + z = 0$ 交成的圆周.

> [!question] 例 5.2.5
>
> 求第一型曲线积分 $I = \int_{L} z \mathrm{d}s$, 其中 $L$ 是曲面 $x^2 + y^2 = z^2$ 与 $y^2 = ax (a > 0)$ 交线上点 $(0, 0, 0)$ 到 $(a, a, a\sqrt{2})$ 的弧段.

> [!question] 例 5.2.6
>
> 计算第二型曲线积分 $\int_{L} xy \mathrm{d}x + x^{2} \mathrm{d}y$, 如图 5.2.3, $L$ 是三角形 $OAB$ 的正向周界, 其中 $A = (1, 2), B = (0, 2)$.
>
> ![[assets/图5.2.3.png]]

> [!question] 例 5.2.7
>
> 计算第二型曲线积分
>
> $$I = \int_{L} (y - z) \mathrm{d}x + (z - x) \mathrm{d}y + (x - y) \mathrm{d}z,$$
>
> 其中 $L$ 是球面 $x^{2} + y^{2} + z^{2} = R^{2}$ 与平面 $y = x \tan \alpha$ 的交线, 方向为从 $x$ 轴正向看去为顺时针, $0 < \alpha < \frac{\pi}{2}$.

> [!question] 例 5.2.8
>
> 设 $f$ 有连续的导函数, $f(0) = 0$, 且曲线积分
> $$\int_C \left( \mathrm{e}^x + f(x) \right) y \mathrm{d}x + f(x) \mathrm{d}y$$
> 与路径无关. 求
> $$\int_{(0,0)}^{(1,1)} \left( \mathrm{e}^x + f(x) \right) y \mathrm{d}x + f(x) \mathrm{d}y.$$

> [!question] 例 5.2.9
>
> 设 $L$ 是圆周 $(x-1)^2 + (y-1)^2 = 1$ 方向为逆时针方向, $f$ 是一个正值可微函数, 且满足
>
> $$\int_{L} -\frac{y}{f(x)} \mathrm{d}x + xf(y) \mathrm{d}y = 2\pi.$$
>
> 求 $f$.

> [!question] 例 5.2.10
>
> 设 $a,b,c$ 是正数. 求由曲线 $L: (x/a)^2+y/b)^2=n$ 围成的区域 $D$ 的面积 $\sigma(D)$.

> [!question] 例 5.2.11
>
> 如图 5.2.5, 求平面上两个椭圆 $L_1: \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ 和 $L_2: \frac{x^2}{b^2} + \frac{y^2}{a^2} = 1 (a > b)$ 内部公共区域的面积.
>
> ![[assets/图5.2.5.png]]

> [!question] 例 5.2.12
>
> 如图 5.2.6, 计算积分 $A = \oint_{L} \frac{x \mathrm{d}y - y \mathrm{d}x}{4x^2 + y^2}$, 其中 $L$ 是以点 $(1,0)$ 为中心, $R$ 为半径的圆周 $(R \neq 1)$, 取逆时针方向为正向.
>
> ![[assets/图5.2.6.png]]

> [!question] 例 5.2.13
>
> 设 $D$ 是 $Oxy$ 平面上有限条逐段光滑曲线围成的区域, $f$ 在 $\overline{D}$ 上有二阶连续偏导数且满足方程
> $$\frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} = 2a \frac{\partial f}{\partial x} + 2b \frac{\partial f}{\partial y} + cf,$$
> 其中 $a,b,c$ 为常数且 $c \geqslant 0$. 求证: 若 $f$ 在 $\partial D$ 上恒为零, 则 $f$ 在 $D$ 上恒为零.

> [!question] 例 5.2.14
>
> 设 $D$ 是由光滑封闭曲线 $L$ 所围的区域, 函数 $f$ 在 $\overline{D}$ 上有二阶连续偏导数, 且满足 $\mathrm{e}^y \frac{\partial^2 f}{\partial x^2} + \mathrm{e}^x \frac{\partial^2 f}{\partial y^2} = 0$, 并且 $f$ 在 $L$ 上恒为零. 证明:
>
> (1) 存在有连续偏导数的函数 $P(x, y), Q(x, y)$ 使得
>
> $$\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = \mathrm{e}^y \left( \frac{\partial f}{\partial x} \right)^2 + \mathrm{e}^x \left( \frac{\partial f}{\partial y} \right)^2, \quad (x, y) \in D;$$
>
> (2) $f$ 在 $D$ 上恒为零.

> [!question] 例 5.2.15
>
> 设 $D: x^2 + y^2 \leqslant a^2 (a > 0), f$ 在 $D$ 上有连续偏导数, 且在 $D$ 的边界上 $f(x, y) = 0$. 求证:
>
> $$\left| \iint_D f(x, y) \mathrm{d}x \mathrm{d}y \right| \leqslant \frac{\pi a^3}{3} \max_{(x, y) \in D} \left\{ \left[ \left( \frac{\partial f}{\partial x} \right)^2 + \left( \frac{\partial f}{\partial y} \right)^2 \right]^{\frac{1}{2}} \right\}.$$

> [!question] 例 5.2.16
>
> (Poincaré 不等式) 设 $D$ 是由简单光滑闭曲线 $L$ 围成的区域, $f$ 在 $\overline{D}$ 上有连续偏导数, 且在 $L$ 上 $f(x,y) = 0$. 求证:
>
> $$\iint_D f^2(x,y) \mathrm{d}x \mathrm{d}y \leqslant \max_D \{x^2 + y^2\} \iint_D \left[ \left( \frac{\partial f}{\partial x} \right)^2 + \left( \frac{\partial f}{\partial y} \right)^2 \right] \mathrm{d}x \mathrm{d}y.$$

## 5.3 曲面积分

> [!question] 例 5.3.1
>
> 设 $S$ 是第一卦限的球面 $x^2+y^2+z^2=R^2 (x \geqslant 0, y \geqslant 0, z \geqslant 0)$，计算曲面积分 $\iint_S (x^2+y^2) \mathrm{d}S$.

> [!question] 例 5.3.2
>
> 设 $S$ 是锥面 $z^2=k^2(x^2+y^2)(z \geqslant 0)$ 被柱面 $x^2+y^2=2ax (a > 0)$ 所截得的曲面，计算曲面积分 $\iint_S (y^2z^2+z^2x^2+x^2y^2) \mathrm{d}S$.

> [!question] 例 5.3.3
>
> 设 $S$ 是柱面 $x^2 + y^2 = a^2$ 被平面 $z = 0$ 和 $z = h (h > 0)$ 所截下的一块柱面. 计算曲面积分 $\iint_S (x^4 + y^4) \mathrm{d}S$.

> [!question] 例 5.3.4
>
> 设 $S(t)$ 是平面 $M(t)$: $x + y + z = t$ 被球面 $x^2 + y^2 + z^2 = 1$ 截下的部分, 且
>
> $$F(x, y, z) = 1 - (x^2 + y^2 + z^2).$$
>
> 求证: 当 $|t| \leqslant \sqrt{3}$ 时, 有
>
> $$\iint_S F(x, y, z) \mathrm{d}S = \frac{\pi}{18} (3 - t^2)^2.$$

> [!question] 例 5.3.5
>
> (第一型曲面积分的正交变换) 设 $S$ 是光滑曲面, 其参数方程为
> $$x = x(u, v), \quad y = y(u, v), \quad z = z(u, v), \quad (u, v) \in D \subset \mathbb{R}^2.$$
> $f$ 是 $S$ 上的连续函数. $A = \left(a_{ij}\right)$ 是三阶正交方阵. 作正交变换
> $$\tilde{X} = \begin{pmatrix} \tilde{x} \\ \tilde{y} \\ \tilde{z} \end{pmatrix} = A \begin{pmatrix} x \\ y \\ z \end{pmatrix} = A X,$$
> 使得 $S$ 变为
> $$\tilde{S} : \tilde{x} = \tilde{x}(u, v), \tilde{y} = \tilde{y}(u, v), \tilde{z} = \tilde{z}(u, v).$$
> 则有
> $$\iint_{S} f(X) \mathrm{d}S = \iint_{\tilde{S}} f(A^{\mathrm{T}}\tilde{X}) \mathrm{d}\tilde{S}.$$

> [!question] 例 5.3.6
>
> (Poisson (泊松) 公式) 设 $S$ 是单位球面 $x^2 + y^2 + z^2 = 1, f(t)$ 是 $\mathbb{R}$ 上的连续函数. 求证:
>
> $$\iint_S f(ax + by + cz) \mathrm{d}S = 2\pi \int_{-1}^{1} f(kt) \mathrm{d}t,$$
>
> 其中 $k = \sqrt{a^2 + b^2 + c^2}$.

> [!question] 例 5.3.7
>
> 求曲面积分
>
> $$I = \iint_S x^2 \mathrm{d}y \mathrm{d}z + y^2 \mathrm{d}z \mathrm{d}x + z^2 \mathrm{d}x \mathrm{d}y,$$
>
> 其中 $S$ 是半球面 $x^2 + y^2 + z^2 = a^2 (z \geqslant 0)$ 的上侧.

> [!question] 例 5.3.8
>
> 计算曲面积分
> $$I = \iint_S x^3 \mathrm{d}y \mathrm{d}z + y^3 \mathrm{d}z \mathrm{d}x,$$
>
> 其中 $S$ 是上半椭球面 $\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1 (z \geqslant 0)$ 的上侧.

> [!question] 例 5.3.9
>
> 计算 $A = \iint_S x \mathrm{d}y \mathrm{d}z + y \mathrm{d}z \mathrm{d}x + z \mathrm{d}x \mathrm{d}y$, 其中 $S = \{(x, y, z) | x, y, z \geqslant 0, x + y + z = 1\}$, 法向与 $(1, 1, 1)$ 同向.

> [!question] 例 5.3.10
>
> 计算 $A = \iint_S xy^2 \mathrm{d}y \mathrm{d}z + yz^2 \mathrm{d}z \mathrm{d}x + zx^2 \mathrm{d}x \mathrm{d}y$, 其中 $S$ 是球体 $V = \{(x, y, z) | x^2 + y^2 + z^2 \leqslant z\}$ 的表面, 方向朝外.

> [!question] 例 5.3.11
>
> 计算曲面积分 $I = \iint_S \frac{\cos(r, n)}{r^2} \mathrm{d}S$, 其中 $S$ 是光滑封闭曲面, 原点不在 $S$ 上, $r = (x, y, z)$, $r = \sqrt{x^2 + y^2 + z^2}$, $n$ 是曲面 $S$ 的单位外法向.

> [!question] 例 5.3.12
>
> 设曲面 $S = \{(x, y, z) \in \mathbb{R}^3 \mid x^2 + y^2 + z^2 = 1, z > 0\}$, 它的定向与 $z$ 轴正向同侧. 设 $f(x, y) = \frac{1 + z}{1 + x^2 + y^2}$, $g(x, y) = xy + yz + zx$, 求积分 $\int_{S} \nabla f \times \nabla g \cdot \mathrm{d}S$.

> [!question] 例 5.3.13
>
> 设 $f$ 在 $\overline{B}(P_0, R)$ 上有二阶连续偏导数，且满足 Laplace（拉普拉斯）方程 $\Delta f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2} = 0$，证明有
>
> $$f(P_0) = \frac{1}{4\pi r^2} \iint_S f(x, y, z) \mathrm{d}S,$$
>
> 其中 $P_0 = (x_0, y_0, z_0)$，$S: (x - x_0)^2 + (y - y_0)^2 + (z - z_0)^2 = r^2, 0 \leqslant r \leqslant R.$

> [!question] 例 5.3.14
>
> 设曲面 $S$ 为 $\{(x, y, z) | x + y + z = 1, x \geqslant 0, y \geqslant 0, z \geqslant 0\}$, 法向与 $(1, 1, 1)$ 同向. 求力场 $F = (y^2, z^2, x^2)$ 绕 $S$ 的正向边界 $\partial S$ 一周所做的功.

> [!question] 例 5.3.15
>
> 设曲线 $L$ 是椭圆抛物面 $z = 3x^2 + 4y^2$ 与椭圆柱面 $4x^2 + y^2 = 4y$ 的交线，从 $z$ 轴的正向看，$L$ 的方向是顺时针方向. 求向量场 $F = (y(z+1), xz, xy-z)$ 沿 $L$ 的环量.

> [!question] 例 5.3.16
>
> 计算 $I = \int_{L} (y^2 + z^2) \mathrm{d}x + (z^2 + x^2) \mathrm{d}y + (x^2 + y^2) \mathrm{d}z$, 其中
> $L: \begin{cases} x^2 + y^2 + z^2 = 2ax, \\ x^2 + y^2 = 2bx, \end{cases}$ $z \geqslant 0, 0 < b < a.$
>
> 从 $x$ 轴正向看过去, $L$ 的方向是逆时针方向.

> [!question] 例 5.3.17
>
> 计算第二型曲线积分 $I = \int_L (y - z) \mathrm{d}x + (z - x) \mathrm{d}y + (x - y) \mathrm{d}z,$
> 其中 $L$ 是柱面 $S_z: x^2 + y^2 = a^2$ 与平面 $\pi_y: \frac{x}{a} + \frac{z}{h} = 1 (a, h > 0)$ 的交线, 从 $x$ 轴正向看去沿逆时针方向.

> [!question] 例 5.3.18
>
> 设 $a, b, c$ 不全为零, $L$ 是球面 $S: x^2 + y^2 + z^2 = R^2 (R > 0)$ 与平面 $\Sigma: ax + by + cz = 0$ 的交线, 其方向这样来定: 质点在 $L$ 上运动的正方向与平面 $\Sigma$ 的法向 $(a, b, c)$ 成右手系. 计算第二型曲线积分
>
> $$\oint_L (bz + c) \mathrm{d}x + (cx + a) \mathrm{d}y + (ay + b) \mathrm{d}z.$$

## 5.4 真题选讲

> [!question] 例 5.4.1
>
> (第一届全国初赛题) 设 $a_n = \int_0^{\frac{\pi}{2}} t \left( \frac{\sin nt}{\sin t} \right)^3 \mathrm{d}t$, 证明 $\sum_{n=1}^{\infty} \frac{1}{a_n}$ 发散.

> [!question] 例 5.4.2
>
> (第一届全国决赛题) 设函数 $f$ 在区间 $[a, b]$ 上连续. 由积分中值公式有
>
> $$\int_a^x f(t) \mathrm{d}t = (x - a)f(\xi) \quad (a \leqslant \xi \leqslant x \leqslant b).$$
>
> 若右导数 $f'_+ (a)$ 存在且非零, 则求 $\lim_{x \to a^+} \frac{\xi - a}{x - a}$.

> [!question] 例 5.4.3
>
> (第二届全国初赛题) 设 $f$ 在 $[0,1]$ 上可积且 $0 \leqslant f \leqslant 1$. 求证: 对任意 $\varepsilon > 0$, 存在只取值为 0 和 1 的分段 (段数有限) 常值函数 $g(x)$, 使得对任意 $[\alpha, \beta] \subset [0,1]$ 有
>
> $$\left| \int_\alpha^\beta (f(x) - g(x)) \mathrm{d}x \right| < \varepsilon.$$

> [!question] 例 5.4.4
>
> （第二届全国初赛题）设 $f$ 在 $[0,1]$ 上 Riemann 可积, 在 $x=1$ 可导, $f(1)=0, f'(1)=a$. 证明: $\lim_{n \to +\infty} n^2 \int_{0}^{1} x^n f(x) \mathrm{d}x = -a.$

> [!question] 例 5.4.5
>
> （第三届全国初赛题）设 $f_1, f_2, \cdots, f_n$ 为 $[0, 1]$ 上的非负连续函数. 求证: 存在 $\xi \in [0, 1]$ 使得
>
> $$\prod_{k=1}^{n} f_k(\xi) \leqslant \prod_{k=1}^{n} \int_{0}^{1} f_k(x) \mathrm{d}x.$$

> [!question] 例 5.4.6
>
> (第五届全国初赛题) 设 $f: [-1,1] \to \mathbb{R}$ 为偶函数, 且在 $[0,1]$ 上单调递增, 又设 $g$ 是 $[-1,1]$ 上的凸函数, 即对任意 $x,y \in [-1,1]$ 及 $t \in (0,1)$ 有
>
> $$g(tx + (1-t)y) \leqslant tg(x) + (1-t)g(y).$$
>
> 求证:
>
> $$2 \int_{-1}^{1} f(x)g(x) \mathrm{d}x \geqslant \int_{-1}^{1} f(x) \mathrm{d}x \int_{-1}^{1} g(x) \mathrm{d}x.$$

> [!question] 例 5.4.7
>
> (第七届全国初赛题) 设 $f$ 是 $\mathbb{R}$ 上有下界或者有上界的连续函数，且存在正数 $a$ 使得
> $$f(x) + a \int_{x-1}^{x} f(t) \mathrm{d}t$$
>
> 为常数. 求证: $f$ 必为常数.

> [!question] 例 5.4.8
>
> (第八届全国初赛题) 设 $f, g$ 是 $[0,1]$ 上单调递增函数, 满足 $0 \leqslant f, g \leqslant 1$,
>
> $$\int_{0}^{1} f(x) \mathrm{d}x = \int_{0}^{1} g(x) \mathrm{d}x.$$
>
> 求证: $\int_{0}^{1} |f(x) - g(x)| \mathrm{d}x \leqslant \frac{1}{2}$.

> [!question] 例 5.4.9
>
> （第九届全国初赛题）设 $f(x)=1-x^2+x^3$. 计算极限
> $$\lim_{n \to +\infty} \frac{\int_{0}^{1} f^n(x) \ln(x+2) \mathrm{d}x}{\int_{0}^{1} f^n(x) \mathrm{d}x}.$$

> [!question] 例 5.4.10
>
> (第六届全国决赛题) 设 $f$ 在区间 $[0,1]$ 上连续可导，且 $f(0) = f(1) = 0$。求证：
>
> $$\left(\int_{0}^{1} x f(x) \mathrm{d}x\right)^{2} \leq \frac{1}{45} \int_{0}^{1}\left(f^{\prime}(x)\right)^{2} \mathrm{d}x,$$
>
> 等号当且仅当 $f(x) = A(x - x^{3})$ 时成立，其中 $A$ 是常数。

> [!question] 例 5.4.11
>
> (第七届全国决赛题) 设 $D: x^{2} + 2y^{2} \leqslant 2x + 4y$. 求积分
>
> $$I = \iint_{D} (x + y) \mathrm{d}x \mathrm{d}y.$$

> [!question] 例 5.4.12
>
> (第七届全国决赛题) 设 $f$ 是定义在 $\mathbb{R}$ 上的连续函数, 且满足方程
>
> $$xf(x) = 2 \int_{\frac{x}{2}}^{x} f(t) \mathrm{d}t + \frac{x^{2}}{4}.$$
>
> 求 $f$.

> [!question] 例 5.4.13
>
> (第九届全国决赛题) 设 $f$ 在 $[0, 1]$ 上有二阶连续导函数, 且 $f(0)f(1) \geqslant 0$. 求证:
>
> $$\int_{0}^{1} |f'(x)| \mathrm{d}x \leqslant 2 \int_{0}^{1} |f(x)| \mathrm{d}x + \int_{0}^{1} |f''(x)| \mathrm{d}x.$$

> [!question] 例 5.4.14
>
> (第十一届全国决赛题) (1) 证明: 函数方程 $x^3 - 3x = t$ 存在三个在闭区间 $[-2,2]$ 上连续, 在开区间 $(-2,2)$ 上连续可导的解, $\varphi_1, \varphi_2, \varphi_3$ 满足
>
> $$\varphi_1(-t) = -\varphi_3(t), \quad \varphi_2(-t) = -\varphi_2(t), \quad t \in [-2,2].$$
>
> (2) 设 $f$ 是 $[-2,2]$ 上连续偶函数. 证明:
>
> $$\int_{1}^{2} f(x^3 - 3x) \mathrm{d}x = \int_{0}^{1} f(x^3 - 3x) \mathrm{d}x.$$

> [!question] 例 5.4.15
>
> (第九届全国决赛题) 计算第二型曲线积分
>
> $$I = \int_{\Gamma} \mathrm{e}^{\sin x} \left( \cos x \cos y \mathrm{d}x - \sin y \mathrm{d}y \right) + \cos z \mathrm{d}z,$$
>
> 其中 $\Gamma: x = \pi \sin(t/2), y = t - \sin t, z = \sin 2t, 0 \leqslant t \leqslant \pi$.

> [!question] 例 5.4.16
>
> (第八届全国决赛题) 计算曲面积分
>
> $$I = \iint_{S} \frac{ax \mathrm{d}y \mathrm{d}z + (z+a)^{2} \mathrm{d}x \mathrm{d}y}{\sqrt{x^{2}+y^{2}+z^{2}}}$$
>
> $(a > 0$ 是常数), 其中 $S: z = -\sqrt{a^{2}-x^{2}-y^{2}}$, 方向朝上.
