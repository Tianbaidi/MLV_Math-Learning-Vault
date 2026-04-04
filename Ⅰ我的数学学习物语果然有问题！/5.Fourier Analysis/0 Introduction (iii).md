---
tags:
  - Fourier_Analysis
---
翻译参考：[[Chapter 1. Genesis]] 

> 有个问题，为什么我们从波来到了热方程？似乎这已经是两个世界的东西。我们上一个章节不是还在研究怎么拨弦发出声音吗？其实对我我们本章节的任务而言（引出傅里叶分析的起源）来说，这两个物理问题是一致的。我们要怎样去理解 **函数的傅里叶展开** 。小剧场请翻到结尾喵~ 

不知道大家有没有用平底锅煎蛋的经验，当我们的燃气灶开小火对着锅的中心加热时候——这里我们分为两种情况：
1. 我加热后关闭燃气，对锅的温度进行观察 - 这里就是我们热方程的第一个问题 。这里平底锅实际上不太合适，应该是坏了的铁板烧炉子（只有一点热源了的那种）
2. 我们回到平底锅，如果我们一直开着火对这个锅加热。那么等到稳定后，我的锅温度范围又如何？
这两个问题就是我们在热方程处要研究的两个问题：
- Derivation of the heat equation : Time-dependent heat equation
- Steady-state heat equation in the disc(现在年轻人会不会不知道碟片为何物？此处翻译为圆盘)

# Derivation of the heat equation : Time-dependent heat equation

我们假定有一个铁板烧（bushi）
## The problem of teppanyaki

我们假定有一块无限大质地均匀的金属板（那能烤很多东西了），我们将其抽象为平面 $\mathbb{R}^{2}$ . 并且在时间开始流动时 $t=0$ 给定的初始的热分步 .我们设点 $(x,t)$ 在 $t$ 时的温度为 $u(x,y,t)$  (be denote by u(x,y,t)) 

这里我们要介入微分的思想了。假设如果我们以 $(x_{0},y_{0})$ 为中心构建一个小正方形，其边长为 $h$ . 其中蕴含的热量可以用下面的公式表达
$$H(t) = \sigma \int \int_{S}u(x,y,t)dxdy,$$
- $\sigma$ ：为材料的比热 .

## What is double integral

对于像我这种什么都不会的人来说，我们还要理解一下二重积分是个什么东西.

对于我们熟悉的单变量积分，我们求的是一个函数的面积。对于一个二重积分，我们求的就是一种类似体积的东西。其实我们现在这个问题就是对二重积分的简单理解，不过我现在给出一个更加简单的例子 
$$\int_{0}^1 \int_{0}^1 2dxdy$$
```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\begin{document}
\begin{tikzpicture}
\begin{axis}[
    xlabel=$x$, ylabel=$y$, zlabel=$z$,
    xmin=-0.2, xmax=1.2,
    ymin=-0.2, ymax=1.2,
    zmin=-0.2, zmax=2.3,
    view={135}{30},
    width=14cm,
    grid=none,
    axis lines=center,
    ticks=none,              % hide automatic ticks; we'll add custom labels
    enlargelimits=false,
]
% Draw the base square at z=0 (edges only)
\draw[thick, black] (0,0,0) -- (1,0,0) -- (1,1,0) -- (0,1,0) -- cycle;
% Vertical edges
\draw[thick, black] (0,0,0) -- (0,0,2);
\draw[thick, black] (1,0,0) -- (1,0,2);
\draw[thick, black] (1,1,0) -- (1,1,2);
\draw[thick, black] (0,1,0) -- (0,1,2);
% Top square edges
\draw[thick, black] (0,0,2) -- (1,0,2) -- (1,1,2) -- (0,1,2) -- cycle;

% --- Three semi‑transparent faces to suggest volume ---
% Front face (y=0)
\addplot3[patch, patch type=rectangle, faceted color=black, 
    fill=blue!40, opacity=0.3] 
    coordinates {(0,0,0) (1,0,0) (1,0,2) (0,0,2)};

% Right face (x=1)
\addplot3[patch, patch type=rectangle, faceted color=black, 
    fill=green!40, opacity=0.3] 
    coordinates {(1,0,0) (1,1,0) (1,1,2) (1,0,2)};

% Top face (z=2)
\addplot3[patch, patch type=rectangle, faceted color=black, 
    fill=red!50, opacity=0.5] 
    coordinates {(0,0,2) (1,0,2) (1,1,2) (0,1,2)};

% --- Add some labels ---
\node at (axis cs:0.5,0.5,2.1) [color=white!100!black, font=\large] {$z=2$};
\node at (axis cs:0.5,-0.2,0) [below] {$(0,0)$};
\node at (axis cs:1,1,2.2) [above] {$(1,1,2)$};

\end{axis}
\end{tikzpicture}
\end{document}
```

如上图所示，我们可以先理解为这个二重积分是这样计算的：
1. 计算对 $x$ 的积分 
   $$\int _{0}^1 2dx=2$$
2. 再计算对 $y$ 的积分 
   $$\int_{0}^1 (\int _{0}^1 2dx)dy=\int _{0}^1 2dy=2$$
3. 总结，计算二重积分可以采用分别采用单积分的方法来进行运算
   $$\iint_S u(x,y) \, dx \, dy = \int_c^d \left[ \int_a^b u(x,y) \, dx \right] dy$$

但是就理解来看，我们还可以这样想：
将积分区域划分成许多非常小的方块，每个小方块的面积记为 $\Delta A$，那么二重积分就近似等于这些小方块上的函数值乘以面积的累加和：
$$
\iint_S u(x,y) \, dxdy \approx \sum_{i=1}^{n} u(x_i, y_i) \, \Delta A
$$
当小方块越分越细，$n \to \infty$ 且 $\Delta A \to 0$ 时，这个和就趋近于精确的积分值。

这其实就是黎曼和的思想，只不过我们把一维的“小区间”换成了二维的“小方块”。如果你非要把这种求和想象成一维的，也可以理解为我们将所有小方块按某种顺序排成一列，然后对它们求和.

我们只需要记住：二重积分就是先沿着一个方向积分，再沿着另一个方向积分（累次积分），或者直接看成小区域上求和取极限，这两种理解都能帮我们了解其本质。
![[Figure_1 1.png]]

带着这种简单的理解，我们就能接着推进了，

## Back to the problem of teppanyaki

我们能得到 
$$\frac{{\partial H}}{\partial t}= \sigma \int \int_{S} \frac{{\partial u}}{\partial t}  dxdy,$$
我们可以知道，这其实就近似代表了进入我们一个小方格的热量 
$$\sigma h^2\frac{\partial u}{\partial t} (x_0,y_0,t)$$
这其实是我们进行这类似微积分里面的运算，当我们 $h$ 取得足够小时，我们可以认为此时的温度是一定的，这个估算是成立的。


我们利用牛顿冷却定律（Newton's law of cooling）,这个定律揭示了热量是从高温物体流向低温物体。或者说由高温流向低温，并且与温差成正比：    
$$ \frac{dT}{dt} = -k (T - T_{\text{env}}) $$
- $T$：物体温度
-  $T_{\text{env}}$：环境温度
- $k$：正常数
- 负号：表示温度在降低（热量流失）

这里我们得到的式子是（右侧垂直侧面的热流量）：
$$ -\kappa h \frac{\partial u}{\partial x} (x_0 + h / 2, y_0, t) $$
*   $h$：边界长度（二维情况下是边长，三维是面积）
*   $\frac{\partial u}{\partial x}$：垂直于边界的温度梯度（温差的变化率）
*   $\kappa$：比例系数

这样的面有四面，因此我们传过这个面的热流总量为 
$$\kappa h\left[\frac{\partial u}{\partial x} (x_0 + h / 2,y_0,t) - \frac{\partial u}{\partial x} (x_0 - h / 2,y_0,t)\right.\left. + \frac{\partial u}{\partial y} (x_0,y_0 + h / 2,t) - \frac{\partial u}{\partial y} (x_0,y_0 - h / 2,t)\right].$$

我们取 $h\to {0}$ 得到  ,且结合此前得到的式子
$$\frac{\sigma}{\kappa}\frac{\partial u}{\partial t} = \frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2}$$
这被称为与时间相关的热传导方程（Time-dependent heat equation），通常简称为热传导方程。

# Steady-state heat equation in the disc

当时间过来很久很久，我们的铁板温度逐渐趋于稳定，所以此时的 $\frac{{\partial u}}{\partial t}$ 为 $0$ 。此时的方程就和变量 $t$ 无关啦，我们要了解的就是 **稳态热传导方程** （Steady-state heat equation） 
$$ \frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2}=0$$
这里的方程很特殊，我们将其称为 **拉普拉斯算子** (Laplace operator or **Laplacian**) . 通常我们记为 $\Delta$ , 那么我们的方程就可记为 
$$\Delta u=0$$
该方程的解我们就称为 **调和函数** （Harmonic Functions）

## Consider The  Unit Disc in The Plane


$$D_{isk}=\{(x,y) \in \mathbb{R}^{2}:x^{2}+y^{2}<1 \}$$

不妨考虑一下极坐标的方式

> 极坐标，不妨按照其字面意思来思考。当我身处地球南极点（地理）我可以怎么描述方位呢？地球上所有的经线都穿过我，我是不是可以用经线来处理位置问题？( 注意：这里只是在考虑平面的情况 ) . 此时我面向西经 $90\degree$ 我们描述西经 $30\degree$ 距离我 3000km 的一个建筑就可以这样记住 $\left( 3\ 000 km,\frac{6}{\pi}  \right)$ . 我们在一些情况下采用极坐标，能比传统坐标更加高效简洁（比如说打游戏）

我们这个区间的边界为 $r=1$ 的圆 $C$ . 我们有 
$$D=\{(r,\theta): 0\leq r\leq 1\}\quad C=\{(r,\theta):r=1\}$$
该问题通常称为**单位圆盘上的狄利克雷问题**（Dirichlet problem (for the Laplacian on the unit disc)），即求解单位圆盘内的稳态热传导方程，使得在边界 $C$ 上满足 $u = f$。这相当于在圆周上固定一个给定的温度分布，历经充分长时间后，考察圆盘内部的温度分布。

这里我们将拉普拉斯算子转化为极坐标的形式，这个边界条件即为 $u(1,\theta)=f(\theta)$ .我们再将拉普拉斯算子转化为极坐标的形式 .这里要补充偏导数的链式法则 ( 见后 ) .

我们求得的新 $\Delta u$ 为 
$$\triangle u = \frac{\partial^2u}{\partial r^2} +\frac{1}{r}\frac{\partial u}{\partial r} +\frac{1}{r^2}\frac{\partial^2u}{\partial\theta^2}$$
由 $\Delta u=0$ 我们令两端都乘以 $r^2$ 得到 
$$r^2\frac{\partial^2u}{\partial r^2} +r\frac{\partial u}{\partial r} = -\frac{\partial^2u}{\partial\theta^2}$$
利用我们的分离变量法，得到 $u(r,\theta)=F(r)G(\theta)$ 形式的解，我们可以得到 
$$\frac{r^2F''(r) + rF'(r)}{F(r)} = -\frac{G''(\theta)}{G(\theta)}.$$
好了，这下熟悉了，我们令其等于 $\lambda$ , 就有 
$$\begin{cases}
G''(\theta) + \lambda G(\theta) = 0, \\
r^2 F''(r) + r F'(r) - \lambda F(r) = 0.
\end{cases}$$
对于 $G$ 函数，就必须满足，周期为 $2\pi$ . 和此前一样，我们令 $\lambda=m^{2}$ , 又会有 
$$G(\theta) = \tilde{A}\cos m\theta +\tilde{B}\sin m\theta .$$
用欧拉公式表示 
$$G(\theta) = \tilde{A}\cos m\theta +\tilde{B}\sin m\theta $$
那对于 $F$ 的函数要怎么办呢？这里就只能直接请出通天法宝了。我将开启翻译模式：

关于 $F$ 的方程有两个简单解：$F(r) = r^m$ 和 $F(r) = r^{- m}$ 。若 $m = 0$，则 $F(r) = 1$ 和 $F(r) = \log r$ 为该方程的两个解。当 $m > 0$ 时，我们注意到随着 $r$ 趋于零，$r^{- m}$ 会无界地增大，从而导致 $F(r)G(\theta)$ 在原点处无界；当 $m = 0$ 且 $F(r) = \log r$ 时，情形亦同。鉴于这些解与直观认知相悖，我们将其舍弃。因此，最终保留的特定函数如下： 
$$u_{m}(r,\theta) = r^{|m|}e^{im\theta},\quad m\in \mathbb{Z}.$$

很明显，这个结果是线性的，于是我们试想叠加特殊解得到假定的通解 
$$u(r,\theta) = \sum_{m = -\infty}^{\infty}a_{m}r^{|m|}e^{im\theta}.$$
如此，对于一个合理的 $f$ , 应该有 
$$u(1,\theta) = \sum_{m = -\infty}^{\infty}a_{m}e^{im\theta} = f(\theta).$$
**萝卜** **Luobo** 萝卜 luobo 来了。给定 $[0,2\pi ]$ 上任何合理的函数 $f$ （满足 $f(0) = f(2\pi)$ ），我们能否找到系数 $a_{m}$ 使得 
$$f(\theta) = \sum_{m = -\infty}^{\infty}a_{m}e^{im\theta} \quad  ?$$
这就是我们之后要回答的问题了。 ^b6592e
### Multi-variavle Chain Rule

```tikz
\begin{document}
\begin{tikzpicture}[line width=1pt]

% 三个关键点
\coordinate (L) at (0,0);
\coordinate (M) at (5,0);
\coordinate (R) at (10,0);

% 连线
\draw[->] (L) -- (M);
\draw (M) -- (R);

% 圆点
\fill (L) circle (2pt);
\fill (R) circle (2pt);

% 标签
\node at (0,1.5) {\textbf{Dependent Variable}};
\node at (5,1.5) {\textbf{Intermediate Variable}};
\node at (10,1.5) {\textbf{Independent Variable}};
\node at (0,-1) {$y = f(x)$};
\node at (5,-1) {$x$};
\node at (10,-1) {$t$};
\node at (0,-2) {$\displaystyle\frac{dy}{dx}$};
\node at (10,-2) {$\displaystyle\frac{dx}{dt}$};
\node at (5,-3) {Fig. 1  $\displaystyle\frac{dy}{dt} = \frac{dw}{dx} \cdot \frac{dx}{dt}$};

\end{tikzpicture}
\end{document}
```
对于一元导数，我们能够知道他的求导链式法则，如果我们对 $f(\varphi(t))$ 求导，其结果为 
$$f'(\varphi(t))\varphi'(t)\quad or  \quad \frac{dy}{dt}=\frac{dy}{dx}\cdot \frac{dx}{dt}$$
```tikz
\begin{document}
\begin{tikzpicture}[line width=1.2pt, font=\sffamily]
% 定义节点（实心圆点）
\node[circle, fill=black, inner sep=2pt] (w) at (0,0) {};
\node[circle, fill=black, inner sep=2pt] (x) at (6,1.5) {};
\node[circle, fill=black, inner sep=2pt] (y) at (6,-1.5) {};
\node[circle, fill=black, inner sep=2pt] (r) at (12,2.5) {};
\node[circle, fill=black, inner sep=2pt] (s) at (12,0) {};
\node[circle, fill=black, inner sep=2pt] (t) at (12,-2.5) {};

% 绘制连线
% 通过 x 的路径（实线）
\draw[solid] (w) -- (x);
\draw[solid] (x) -- (r);
\draw[solid] (x) -- (s);
\draw[solid] (x) -- (t);
% 通过 y 的路径（虚线）
\draw[dashed] (w) -- (y);
\draw[dashed] (y) -- (r);
\draw[dashed] (y) -- (s);
\draw[dashed] (y) -- (t);

% 添加节点标签
\node at (-0.5,0.5) {\Large$w(x,y)$};          % w 左上方
\node at (6,2.0)   {\Large$x$};                 % x 正上方
\node at (6,-1.0)  {\Large$y$};                 % y 正上方
\node at (12.5,2.5) {\Large$r$};                 % r 右侧
\node at (12.5,0)   {\Large$s$};                 % s 右侧
\node at (12.5,-2.5) {\Large$t$};                 % t 右侧

% 顶部标题（使用 \parbox 实现两行居中）
\node at (0,4.5) {\parbox{3cm}{\centering\bfseries\large Dependent\\Variable}};
\node at (6,4.5) {\parbox{4cm}{\centering\bfseries\large Intermediate\\Variables}};
\node at (12,4.5) {\parbox{4cm}{\centering\bfseries\large Independent\\Variables}};

% 底部图例
\draw[solid] (3.5,-4.5) -- (4.5,-4.5);
\node at (4.7,-4.5) [anchor=west] {Path through $x$};
\draw[dashed] (7.5,-4.5) -- (8.5,-4.5);
\node at (8.7,-4.5) [anchor=west] {Path through $y$};

\end{tikzpicture}
\end{document}
```

但是对于二元的导数，我们就要考虑的多得多，不过我们也可以解剖麻雀。从研究特例开始

#### 两个中间变量，一个独立变量
```tikz
\begin{document}
\begin{tikzpicture}[line width=1pt]
% 定义坐标
\coordinate (W) at (0,0);
\coordinate (X) at (5,2);
\coordinate (Y) at (5,-2);
\coordinate (T) at (10,0);

% 绘制实心圆点
\fill (W) circle (2pt);
\fill (X) circle (2pt);
\fill (Y) circle (2pt);
\fill (T) circle (2pt);

% 变量标签
\node at (-0.8,0.5) {\Large$w = f(x, y)$};
\node at (5,2.5) {\Large$x$};
\node at (5,-2.5) {\Large$y$};
\node at (10.5,0) {\Large$t$};

% 连接线及导数标签
% 路径1: w -> x (实线, 标签在上方)
\draw[->, line width=1pt] (W) -- (X) node[midway, above, sloped] {$\frac{\partial w}{\partial x}$};
% 路径1: x -> t (实线, 标签在上方)
\draw[->, line width=1pt] (X) -- (T) node[midway, above, sloped] {$\frac{dx}{dt}$};

% 路径2: w -> y (虚线, 标签在下方)
\draw[->, line width=1pt, dashed] (W) -- (Y) node[midway, below, sloped] {$\frac{\partial w}{\partial y}$};
% 路径2: y -> t (虚线, 标签在下方)
\draw[->, line width=1pt, dashed] (Y) -- (T) node[midway, below, sloped] {$\frac{dy}{dt}$};

% 顶部标题（使用 \parbox 实现多行，无衬线加粗）
\node at (0,3.5) {\parbox{3cm}{\centering\sffamily\bfseries Dependent\\Variable}};
\node at (5,4) {\parbox{3.5cm}{\centering\sffamily\bfseries Intermediate\\Variables}};
\node at (10,3.5) {\parbox{3.5cm}{\centering\sffamily\bfseries Independent\\Variable}};
\end{tikzpicture}
\end{document}
```
如果 $w=f(x,y)$ 是可导的，且 $x=x(t)$ 、$y=y(t)$ 是关于 $t$ 的可导函数，那么对于复合函数 $f(x(t),y(t))$ 关于 $t$ 的导数就是 
$$\frac{dw}{dt}=\frac{{\partial f}}{\partial x}\cdot \frac{dx}{dt}+ \frac{{\partial f}}{\partial y}\cdot \frac{dy}{dt}$$
#### 三个中间变量，一个独立变量
```tikz
\begin{document}
\begin{tikzpicture}[line width=1pt, font=\Large]
% 坐标定义（三列布局）
\coordinate (w) at (0,0);
\coordinate (x) at (5,2);
\coordinate (y) at (5,0);
\coordinate (z) at (5,-2);
\coordinate (t) at (10,0);

% 绘制圆点（统一为黑色）
\fill (w) circle (2pt);
\fill (x) circle (2pt);
\fill (y) circle (2pt);
\fill (z) circle (2pt);
\fill (t) circle (2pt);

% 绘制连接线，用不同线型区分三条路径：
% 上路径（w→x→t）用实线
\draw[->] (w) -- (x);
\draw[->] (x) -- (t);
% 中路径（w→y→t）用虚线
\draw[->, dashed] (w) -- (y);
\draw[->, dashed] (y) -- (t);
% 下路径（w→z→t）用点线
\draw[->, dotted] (w) -- (z);
\draw[->, dotted] (z) -- (t);

% 三列标题（无衬线加粗，\parbox 实现换行）
\node at (0,2.5) {\parbox{2.8cm}{\centering\sffamily\bfseries Dependent\\Variable}};
\node at (5,3.0) {\parbox{3.0cm}{\centering\sffamily\bfseries Intermediate\\Variables}};
\node at (10,2.5) {\parbox{3.0cm}{\centering\sffamily\bfseries Independent\\Variable}};

% 变量标签
\node[left]  at (-0.8,0)   {$w = f(x,y)$};   % w 左侧
\node[above] at (5,2.3)    {$x$};            % x 上方
\node[above] at (5,0.3)    {$y$};            % y 上方
\node[below] at (5,-2.3)   {$z$};            % z 下方
\node[right] at (10.5,0)   {$t$};            % t 右侧

% 导数标签（根据路径分别标注）
\node[above] at (2.5,1.2) {$\frac{\partial w}{\partial x}$};   % w→x（实线）
\node[above] at (7.5,1.2) {$\frac{dx}{dt}$};                  % x→t（实线）
\node[above] at (2.5,0.3) {$\frac{\partial w}{\partial y}$};   % w→y（虚线）
\node[above] at (7.5,0.3) {$\frac{dy}{dt}$};                  % y→t（虚线）
\node[below] at (2.5,-1.2){$\frac{\partial w}{\partial z}$};   % w→z（点线）
\node[above] at (7.5,-0.8){$\frac{dz}{dt}$};                  % z→t（点线）

\end{tikzpicture}
\end{document}
```
在这种情况下，我们有 
$$\frac{dw}{dt}=\frac{{\partial f}}{\partial x}\cdot \frac{dx}{dt}+\frac{{\partial f}}{\partial y}\cdot \frac{dy}{t}+\frac{{\partial f}}{\partial z}\cdot \frac{dz}{t}$$
#### 两个中间变量，两个独立变量
```tikz
\begin{document}
\begin{tikzpicture}[line width=1.2pt, font=\Large]
% 坐标定义（三列布局）
\coordinate (w) at (0,0);
\coordinate (x) at (5,2);
\coordinate (y) at (5,-2);
\coordinate (r) at (10,2);
\coordinate (s) at (10,-2);

% 绘制连接线（先画线，避免覆盖节点）
% 路径A（实线）：w -> x, x -> r, x -> s
\draw[->] (w) -- (x);
\draw[->] (x) -- (r);
\draw[->] (x) -- (s);
% 路径B（虚线）：w -> y, y -> r, y -> s
\draw[->, dashed] (w) -- (y);
\draw[->, dashed] (y) -- (r);
\draw[->, dashed] (y) -- (s);

% 节点圆点（黑色实心）
\fill (w) circle (2.5pt);
\fill (x) circle (2.5pt);
\fill (y) circle (2.5pt);
\fill (r) circle (2.5pt);
\fill (s) circle (2.5pt);

% 三列标题（无衬线加粗，\parbox 实现换行）
\node at (0,3.2) {\parbox{2.8cm}{\centering\sffamily\bfseries Dependent\\Variable}};
\node at (5,3.8) {\parbox{3.2cm}{\centering\sffamily\bfseries Intermediate\\Variables}};
\node at (10,3.2) {\parbox{3.2cm}{\centering\sffamily\bfseries Independent\\Variables}};

% 变量标签
\node[left]  at (-0.8,0)   {$w = f(x,y)$};          % w 左侧
\node[above] at (5,2.5)    {$x = g(r,s)$};          % x 上方
\node[below] at (5,-2.5)   {$y = h(r,s)$};          % y 下方
\node[right] at (10.5,2)   {$r$};                   % r 右侧
\node[right] at (10.5,-2)  {$s$};                   % s 右侧

% 导数标签（使用 \frac 代替 \dfrac）
\node[below] at (2.5,-0.4) {$\frac{\partial w}{\partial x}$};   % w→x 下方
\node[above] at (2.5,0.4)  {$\frac{\partial w}{\partial y}$};   % w→y 上方
\node[below] at (7.3,1.8)  {$\frac{\partial x}{\partial s}$};   % x→r 下方（靠近交叉点上方）
\node[above] at (7.3,-1.7) {$\frac{\partial y}{\partial s}$};   % y→s 上方

\end{tikzpicture}
\end{document}
```
此时我们要写两个偏导数，我们就这样写 
$$\begin{cases}
\frac{{\partial w}}{\partial r}=\frac{{\partial w}}{\partial x}\cdot \frac{{\partial x}}{\partial r}+\frac{{\partial w}}{\partial y}\cdot \frac{{\partial y}}{\partial r} \\
\frac{{\partial w}}{\partial s}=\frac{{\partial w}}{\partial x}\cdot \frac{{\partial x}}{\partial s}+\frac{{\partial w}}{\partial y}\cdot \frac{{\partial y}}{\partial s} 
\end{cases}$$
#### 单中间变量、双独立变量

$$\begin{cases}
\frac{{\partial w}}{\partial r}=\frac{{d w}}{d x}\cdot \frac{{\partial x}}{\partial r} \\
\frac{{\partial w}}{\partial s}=\frac{{d w}}{d x}\cdot \frac{{\partial x}}{\partial s} 
\end{cases}$$
