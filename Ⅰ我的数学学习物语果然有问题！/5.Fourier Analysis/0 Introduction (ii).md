---
tags:
  - Fourier_Analysis
---
> 此前我们采用行波法来进行波动方程的推演 . 现在，现在我们将使用驻波叠加法来进行分析。然后我们将分析 "拨弦" ( $\textbf{The plucked string}$ ) 的例子 。我不明白，问什么讲傅里叶分析看的人就多起来了。还有怎么老是有人要去看我之前发的反思小文章，我自己都执行不了（哭死）

翻译参考：[[Chapter 1. Genesis]] 

上一篇文章有些小迷糊，**为什么线性方程组是线性的呢？** 这里在文章开头再做一个解释。

在数学上，判断一个方程是否为线性，标准是看它是否满足**齐次性和可加性**（合称**叠加原理**），我们以一维波动方程为例 
$$\frac{{\partial^{2}u}}{\partial t^{2}}=c^{2} \frac{{\partial^{2}u}}{\partial x^{2}}$$
我们将其写成算符的形式 $L(u)=0$ , 就有 
$$L(u)=\frac{{\partial^{2}u}}{\partial t^{2}}-c^{2} \frac{{\partial^{2}u}}{\partial x^{2}}=0$$
由于这个式子满足 : 
1. **齐次性** : 如果 $u$ 是解，那么 $k \cdot u$ 也是解
2. **可加性** : 如果 $u_{1}$ 和 $u_{2}$ 都是解，那么 $(u_{1}+u_{2})$ 也是解
这成立的原因在于 **导数** 本身的运算是线性的 ，只要式子中不出现如 $u^{2} ,\sin (u),u \frac{{\partial u}}{\partial x}$ 这类非线性项即可。

或者就物理现象来看，两列不同的波在相遇时，在相互“干扰”后能再度像啥也没发生一样穿过去。两波相遇处呈现的波形实际上时他们单独振动的矢量和。

# Superposition of Standing Waves

要通过驻波法解波动方程，首先要复习两个点：
1. 对于驻波波的形式 
   $$u(x,t)=\varphi(x)\psi(t)$$
   这就是我们上文提到的**分离变量法** (separation of variables) 
2. 对于线性性的理解：我们的一个 “复杂波” 可以理解为多个波——或者用音乐中的纯音(pure tones), 以及和声来解释——的叠加形式
这里的分离变量的方法对于解热传导方程同样优雅 .

我们解此方程的想法时通过构建 **特解** 的和来取得方程的通解。

## 再度理解驻波

### 驻波方程

我们关注波动方程可以知道 
$$\frac{{\partial^{2}u}}{\partial t^{2}}=c^{2} \frac{{\partial^{2}u}}{\partial x^{2}}$$
其中一边只与 $t$ 相关，另一边则于 $x$ 相关：这两个分别代表时间和位移。我们此时的思路是将一个偏微分方程转化为更简单常微分方程组成的系统来求解，我们于是可以构建这样的方程 $u(x,t) = \varphi (x)\psi (t)$ （就是分离变量法）。我们得到 
$$\varphi(x)\psi''(t)=\varphi''(x)\psi(t)$$
因此 
$$\frac{\psi^{\prime\prime}(t)}{\psi(t)} = \frac{\varphi^{\prime\prime}(x)}{\varphi(x)}.$$
我们再度观察这个式子，可以令这个式子等于一常数 $\lambda$ . 实际上，这个式子必定满足存在一个常数 $\lambda$ 时其成立，于是我们就得到了 
$$\begin{cases}
\psi''(t)-\lambda \psi (t)=0 \\
\varphi''(x)-\lambda \varphi(x)=0
\end{cases}$$
此时这个式子就和我们此前研究简谐运动的得到的的形式差不多了。我们观察第一个式子，只有当常数 $\lambda<0$ 时这个式子才可能成立。于是我们可以设 $\lambda=-m^{2}$ .于是我们解出 
$$\psi(t)=A\cos mt+B\sin mt$$
第二个式子时同理的 
$$\varphi(x)=\widetilde{A}\cos mx+\widetilde{B}\sin mx$$
我们考虑到这弦固定在 $x=0$ 于 $x=\pi$ 处，我们就能带入并且解出 $\widetilde{A}=0$  $\widetilde{B} \not=0$ . 此时这个 $m$ 必定为整数，如果 $m=0$  我们就得到了一个直线，若 $m<-1$ 就将其化简为 $m>1$ 的情况，我们可以直觉得到**驻波的波动方程**为 
$$u_{m}(x,t)=(A_{m}\cos mt+B_{m}\sin mt)\sin mx$$
但是对于这个这个式子的处理结果 
$$\frac{\psi^{\prime\prime}(t)}{\psi(t)} = \frac{\varphi^{\prime\prime}(x)}{\varphi(x)}.$$
我们进行了一个风险操作，这里我可以通过对我们得到的方程进行二阶偏导数来验证。此处的计算就当作偏导数的练习吧，我就不展示了。

```tikz
\usepackage{pgfplots}
\usepackage{amsmath}
\pgfplotsset{compat=1.16}

\begin{document}
\begin{tikzpicture}
    
    % 子图 (a) —— 左侧
    \begin{scope}[xshift=-5cm]
    \begin{axis}[
        title={\textbf{(a)}},
        xlabel={$x$},
        ylabel={$u$},
        domain=-2*pi:2*pi,
        samples=200,
        axis lines=middle,
        width=6.5cm,
        height=4.5cm,
        ymin=-1.2, ymax=1.2,
        xtick={-6.283, -3.1416, 0, 3.1416, 6.283},
        xticklabels={$-2\pi$, $-\pi$, $0$, $\pi$, $2\pi$},
        ytick={-1,0,1},
        grid=none
    ]
        \addplot[black, thick] {sin(deg(x))};
        \addplot[black, dashed, thick] {0.2*sin(deg(x))};
        \addplot[black, dotted, thick] {-0.5*sin(deg(x))};
    \end{axis}
    \end{scope}
    
    % 子图 (b) —— 右侧
    \begin{scope}[xshift=5cm]
    \begin{axis}[
        title={\textbf{(b)}},
        xlabel={$x$},
        ylabel={$u$},
        domain=-2*pi:2*pi,
        samples=300,
        axis lines=middle,
        width=6.5cm,
        height=4.5cm,
        ymin=-1.2, ymax=1.2,
        xtick={-6.283, -3.1416, 0, 3.1416, 6.283},
        xticklabels={$-2\pi$, $-\pi$, $0$, $\pi$, $2\pi$},
        ytick={-1,0,1},
        grid=none
    ]
        \addplot[black, thick] {sin(2*deg(x))};
        \addplot[black, dashed, thick] {0.2*sin(2*deg(x))};
        \addplot[black, dotted, thick] {-0.5*sin(2*deg(x))};
    \end{axis}
    \end{scope}
\end{tikzpicture}
\end{document}
```
在我们展开进一步研究之前，我们再看一下这个波的形态：

### 音乐课开课啦！！！

我们来看图像 $a$

对于我们的研究，我们如果令 ${m}=1$ 与初始位移就能得到新方程 $u(x,t)=\cos t\sin x$ ——这里又假设了 $A_{m}=1$ . 倘若我们以观测固定的位的位置，就会发现其位置会随着 $t$ 的变化周期摆动。这个是我们很早就知道的。

现在我们来思考一个问题，既然音都是 do，re，mi ……为什么不同的乐器发出的声音不同呢？这里其实可以从音乐的角度来思考：假设我们有一把弦乐器，忽略弦之间的共振的影响

如果我们要演奏一个泛音，对于一个吉他手而言，有分为12品泛音和7品泛音。演奏时我们轻触弦（在7品或者12品的位置），后拨弦，拨弦后（或者几乎可以说同时）触弦的手立刻离开。我们就能听到比拨空弦高得多的音。那么具体是多高呢？12品（琴弦的 $\frac{1}{2}$ 处 ）音为高八度音，7品（琴弦的 $\frac{1}{3}$ 处 ）为高12度音 . 
```tikz
\usepackage{tikz}
\usepackage{amsmath}
\usepackage{amssymb}

\begin{document}

% ==========================================
% Figure 1: Fundamental Tone (1st Harmonic)
% ==========================================
\begin{tikzpicture}[scale=0.9]
    % Title
    \node[anchor=west] at (0, 2.2) {\small \textbf{Fundamental ($m=1$)}};

    % String boundaries
    \draw[thick] (0, 0) -- (6, 0);
    \filldraw[black] (0, 0) circle (0.08);
    \filldraw[black] (6, 0) circle (0.08);

    % Standing wave pattern
    \draw[thick, domain=0:6, samples=100] plot (\x, {0.5*sin(180*\x/6)});
    \draw[thick, domain=0:6, samples=100] plot (\x, {-0.5*sin(180*\x/6)});

    % Labels
    \node[below] at (0, -0.1) {Node};
    \node[below] at (6, -0.1) {Node};
    \node[above] at (3, 0.5) {Anti-node};

    % Length label
    \draw[<->] (0, -1.2) -- (6, -1.2) node[midway, below] {\small $L$};

    % Info
    \node[anchor=west] at (0, -1.8) {\small $f_1,\ \lambda_1=2L$};
\end{tikzpicture}

\vspace{0.3cm}

% ==========================================
% Figure 2: 12th Fret Harmonic (2nd Harmonic)
% ==========================================
\begin{tikzpicture}[scale=0.9]
    % Title
    \node[anchor=west] at (0, 2.2) {\small \textbf{12th Fret ($m=2$)}};

    % String boundaries
    \draw[thick] (0, 0) -- (6, 0);
    \filldraw[black] (0, 0) circle (0.08);
    \filldraw[black] (6, 0) circle (0.08);

    % Node at midpoint
    \draw[dashed, thick] (3, -0.5) -- (3, 0.5);
    \filldraw[black] (3, 0) circle (0.08);
    \node[above] at (3, 0.5) {Node};

    % Standing wave pattern
    \draw[thick, domain=0:3, samples=100] plot (\x, {0.4*sin(180*\x/3)});
    \draw[thick, domain=0:3, samples=100] plot (\x, {-0.4*sin(180*\x/3)});
    \draw[thick, domain=3:6, samples=100] plot (\x, {0.4*sin(180*(\x-3)/3)});
    \draw[thick, domain=3:6, samples=100] plot (\x, {-0.4*sin(180*(\x-3)/3)});

    % Antinodes
    \node[above] at (1.5, 0.4) {Anti-node};
    

    % Length labels
    \draw[<->] (0, -1.2) -- (3, -1.2) node[midway, below] {\small $L/2$};
    \draw[<->] (3, -1.2) -- (6, -1.2) node[midway, below] {\small $L/2$};

    % Info
    \node[anchor=west] at (0, -1.8) {\small $f_2=2f_1,\ \lambda_2=L$};
\end{tikzpicture}

\vspace{0.3cm}

% ==========================================
% Figure 3: 7th Fret Harmonic (3rd Harmonic)
% ==========================================
\begin{tikzpicture}[scale=0.9]
    % Title
    \node[anchor=west] at (0, 2.2) {\small \textbf{7th Fret ($m=3$)}};

    % String boundaries
    \draw[thick] (0, 0) -- (6, 0);
    \filldraw[black] (0, 0) circle (0.08);
    \filldraw[black] (6, 0) circle (0.08);

    % Nodes at 1/3 and 2/3
    \draw[dashed, thick] (2, -0.5) -- (2, 0.5);
    \draw[dashed, thick] (4, -0.5) -- (4, 0.5);
    \filldraw[black] (2, 0) circle (0.08);
    \filldraw[black] (4, 0) circle (0.08);
    \node[above] at (2, 0.5) {Node};
    \node[above] at (4, 0.5) {Node};

    % Standing wave pattern
    \draw[thick, domain=0:2, samples=100] plot (\x, {0.35*sin(180*\x/2)});
    \draw[thick, domain=0:2, samples=100] plot (\x, {-0.35*sin(180*\x/2)});
    \draw[thick, domain=2:4, samples=100] plot (\x, {0.35*sin(180*(\x-2)/2)});
    \draw[thick, domain=2:4, samples=100] plot (\x, {-0.35*sin(180*(\x-2)/2)});
    \draw[thick, domain=4:6, samples=100] plot (\x, {0.35*sin(180*(\x-4)/2)});
    \draw[thick, domain=4:6, samples=100] plot (\x, {-0.35*sin(180*(\x-4)/2)});

    % Antinodes
    \node[above] at (1, 0.35) {Anti-node};
   

    % Length labels
    \draw[<->] (0, -1.2) -- (2, -1.2) node[midway, below] {\small $L/3$};
    \draw[<->] (2, -1.2) -- (4, -1.2) node[midway, below] {\small $L/3$};
    \draw[<->] (4, -1.2) -- (6, -1.2) node[midway, below] {\small $L/3$};

    % Info
    \node[anchor=west] at (0, -1.8) {\small $f_3=3f_1,\ \lambda_3=\frac{2L}{3}$};
\end{tikzpicture}

\vspace{0.3cm}


\end{document}
```

对于这个泛音，不难发现的是，高多少度音往往取决于我们手指轻触弦的位置。如此巧妙难道其中有什么数学原理？有的兄弟有的。我们直接看最后得到空间部分方程
$$\varphi(x)=\sin mx$$
这样，我们就能赋予 $m$ 一些物理上的意义。它控制着我们一个条弦上有多少 "零点" 控制着波长，影响着频率。人对声音的感知是对数的，我们我们零点个数从 $0\to 1$ 时，波长变为原来的一半，频率就变为原先的 $2$ 倍。可以借此公式 
$$\text{感知音高} \propto \log_2(\text{频率})$$
那么我们12品泛音恰恰好就是一个八度——amazing啊？！ 学来了说是（）

我们从音乐的层面回到数学（好像就没有离开过数学，数学真的是太奇妙了）

于是我们定义，当 $m=1$ 时，此时拨弦发出的声音为 **基音** （Fundamental Tone）或者称之为 **第一谐波** （First Harmonic）
对应的，当 $m=2$ 时，此时就称为 **第一泛音** （First Overtone）或者 **第二谐波** （Second Harmonic）
以此类推的……

我们在图上的有些特殊的点也有自己的定义 ：
1. **节点** （Nodes）在驻波中保持静止的点
2. **反节点** （Anti-nodes）能取到最大运动幅度的点
- 我们在高中时候也有这样类似的定义，但是当时行波研究似乎更多

> 这里作为补充，对于更高的 $m$ 值，我们得到更多的泛音或更高次谐波。注意随着 $m$ 的增加，频率增加，周期 $\frac{2\pi}{m}$ 减小。因此，基音的频率低于泛音。

### 我们回到驻波

我们已经研究了所谓的 *一个特解* ，是时候推进下去来完成我们的最终猜想了！
我们寻求的时一个一般波的叠加态，于是根据波动方程的线性性，我们可以得到这样的一个式子 
$$u(x,t)=\sum_{m=1}^\infty (A_{m}\cos mt+B_{m}\sin mt)\sin mx$$
对于一个稳定的驻波，我们只要研究 $x$ 控制的部分 ( 或者说，进行了一个物理上的限定 )
$$\varphi(x)=\sum_{m=1}^\infty A_{m}\sin mt \quad ¿?$$
>Note that the above sum is infinite, so that questions of convergence arise, but since most of our arguments so far are formal, we will not worry about this point now.This question is stated loosely, but a lot of our effort in the next two chapters of this book will be to formulate the question precisely and attempt to answer it. This was the basic problem that initiated the study of Fourier analysis.( 这里不想翻译 )

如果这个是对的，我们就可以提供一个对 $A_{m}$ 的观测.我们两边同时乘一个 $\sin nx$ 并且在 $[0,\pi]$ 上积分 
$$\int_{0}^{\pi}\varphi(x)\sin nxdx = \int_{0}^{\pi}\left(\sum_{m = 1}^{\infty}A_{m}\sin mx\right)\sin nxdx$$
$$= \sum_{m = 1}^{\infty}A_{m}\int_{0}^{\pi}\sin mx\sin nxdx = A_{n}\cdot \frac{\pi}{2},$$
这里就不得不提三角函数积分的一个性质了 —— **正交性** （话说我还没遇到，暴露刷题量了www）

当 $m=n$ 时，也就是我们逐项求和一直到 $m=n$ 时，出现了唯一结果不等于 $0$ 的积分。这个时候是这样的 
$$A_{n}\frac{\pi}{2}=\int_{0}^{\pi}\varphi(x)\sin nxdx $$
我们就有 $A_{n}=\frac{2}{\pi}\int_{0}^{\pi}\varphi(x)\sin nxdx$ 
我们这个 $A_{n}$ 就称为 **第n级傅里叶正弦系数** （the $n^{th}$ Fourier sine coefficient）
一个萝卜一个坑，这个问题等以后再细说吧（至少原书是这样写的）

**Make it Odd！！！** 这是我们将问题一般化的方法，操作实际于我们上一篇的一模一样，这里就不展开叙述了。不过我们可以类似有一个余弦的操作，我们定义 
$$\widetilde{\varphi}(x)=\sum_{m=0}^\infty A'_{m}\cos mx$$
那这个延拓方式就变成了 **Make it Even! ! !** 

任意一个定义在 $[-\pi,\pi]$ 的函数 ，都可以分解为一个奇函数和一个偶函数的和。那么我们就能写出 
$$F(x)=\sum_{m=1}^\infty A_{m}\sin mx+\sum_{m=0}^\infty A'_{m}\cos mx$$
那么，欧拉公式就快端上来罢（喜），我已经等不及了。学完有奖励，不学完有惩罚（）
我们希望是这样的一个形式 
$$F(x)=\sum_{m=-\infty}^\infty a_{m}e^{imx} \quad ¿?$$
这样看来，这个式子可能成为后续聊聊的一类东西了。定义为 **萝卜** 

但是我们又可以聊聊系数了 
类比我们此前的方法，欧拉公式依旧有这样的性质 
$$\frac{1}{2\pi}\int_{-\pi}^\pi e^{imx}e^{-inx}dx$$
当且仅当 $m=n$ 时，能求得非零结果，我们期望有
$$a_{n}=\frac{1}{2\pi}\int_{-\pi}^\pi F(x)e^{-inx}dx$$
我们这个 $a_{n}$ 就称为函数 $F$ 的**第n级傅里叶系数** （the $n^{th}$ Fourier  coefficient of F）

我们再回到波动方程，为了正确地表述问题，我们必须限定两个初始条件，我们在简谐运动和行波的操作经验。这些条件应该是弦的初始位置和速度。也就是说，我们要求 $u$ 满足一个微分方程和两个条件
$$u(x,0) = f(x)\quad \mathrm{and}\quad \frac{\partial u}{\partial t} (x,0) = g(x)$$
其中 $f$ 和 $g$ 是指定的函数，可以表示为
$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx\quad \mathrm{and}\quad g(x) = \sum_{m = 1}^{\infty}mB_{m}\sin mx.$$

# Example: The Plucked String

问题非常其实可以是我们此前音乐课里的问题，因为它至少翻译下来叫 **“拨弦”** 。不过确实如此，电吉他那什么单单双，双双啥都有区分拾音器的位置。我们如果以单拾音器为例子（不考虑双拾音对音色的影响）我们选择拾音器不同并且拨弦后输出的音色是有不同的，这个背后就是现在讨论的问题

考虑一根两端固定的弦，位于区间 $[0, \pi]$ 上，波速 $c = 1$。弦的振动由波动方程描述：
$$\frac{\partial^2 u}{\partial t^2} = \frac{\partial^2 u}{\partial x^2}, \quad 0 < x < \pi, \ t > 0,$$
其中
$$u(0,t) = 0, \quad u(\pi,t) = 0.$$
- **初始位移**：弦在点 $p$（$0 < p < \pi$）处被拨到高度 $h$，形状为三角形：

$$
f(x) = 
\begin{cases} 
\dfrac{h}{p}\, x, & 0 \le x \le p, \\[1em]
\dfrac{h}{\pi-p}\, (\pi - x), & p \le x \le \pi.
\end{cases}
$$

- **初始速度**：静止释放，即 $g(x) = 0$。

**目标是求弦的位移** $u(x,t)$
## 用傅里叶级数求解

根据分离变量法，满足边界条件的通解为：
$$u(x,t) = \sum_{m=1}^{\infty} \bigl( A_m \cos(m t) + B_m \sin(m t) \bigr) \sin(m x).$$
由初始速度 $u_t(x,0) = 0$ 得 $B_m = 0$，所以
$$u(x,t) = \sum_{m=1}^{\infty} A_m \cos(m t) \sin(m x).$$
初始位移给出：
$$u(x,0) = \sum_{m=1}^{\infty} A_m \sin(m x) = f(x).$$
因此 $C_m$ 是 $f(x)$ 的正弦级数系数：
$$A_m = \frac{2}{\pi} \int_0^\pi f(x) \sin(m x) \, dx.$$
计算该积分得到：
$$A_m = \frac{2h}{m^2} \cdot \frac{\sin(m p)}{p(\pi - p)}.$$
于是解为：
$$u(x,t) = \sum_{m=1}^{\infty} \frac{2h}{m^2} \frac{\sin(m p)}{p(\pi - p)} \cos(m t) \sin(m x).$$
该级数绝对收敛
## 行波解表示
利用三角恒等式 $\cos v \sin u = \frac{1}{2} [\sin(u+v) + \sin(u-v)]$，可将级数解改写为行波形式：
$$u(x,t) = \frac{1}{2} \sum_{m=1}^{\infty} A_m \bigl[ \sin(m(x+t)) + \sin(m(x-t)) \bigr] = \frac{1}{2} \bigl[ f(x+t) + f(x-t) \bigr],$$
其中 $f$ 需经过老办法定义在全体实数上：

1. 将 $f$ 从 $[0,\pi]$ 奇延拓到 $[-\pi,\pi]$
2. 再将此函数周期延拓到整个实轴，周期为 $2\pi$。

这样得到的 $f$ 是奇函数且周期为 $2\pi$，则行波解形式成立，且满足初始条件和边界条件。

## 关于解的光滑性( 分析自 AI )

初始位移 $f(x)$ 在 $x=p$ 处有一个尖点（一阶导数不连续），因此 $f \notin C^2$。由它构造的 $u(x,t)$ 也不具有连续的二阶偏导数，因此不是经典意义下波动方程的解。

然而物理上弦确实会这样运动。数学上，需要引入**广义解**（弱解）的概念：$u$ 满足积分形式的方程，或作为分布意义下的解。这属于“弱解”和“分布”理论的研究范畴。


内容就到这里了，后面就是热方程的东西了。看起来有一定的延续性，尽可能我讲的直白些。

# 再说句话

![[Pasted image 20260301012324.png]]

很好的游戏，令我的时间旋转。