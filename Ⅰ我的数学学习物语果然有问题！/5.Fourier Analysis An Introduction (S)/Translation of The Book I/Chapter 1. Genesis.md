---
tags:
---
[[0 Introduction （i）]]

===== Page 18 =====

1 The Genesis of Fourier Analysis

Regarding the researches of d'Alembert and Euler could one not add that if they knew this expansion, they made but a very imperfect use of it. They were both persuaded that an arbitrary and discontinuous function could never be resolved in series of this kind, and it does not even seem that anyone had developed a constant in cosines of multiple arcs, the first problem which I had to solve in the theory of heat.

J. Fourrier, 1808- 9

1 傅里叶分析的起源

关于达朗贝尔和欧拉的研究，难道我们不能补充说，即使他们知道这种展开，他们也仅仅是非常不完善地运用了它。他们两人都相信，一个任意的、不连续的函数永远不能分解成这种级数，甚至似乎也没有人将常数展开为倍弧的余弦级数，而这是我必须在热理论中解决的第一个问题。

—— J. 傅里叶，1808-9年

In the beginning, it was the problem of the vibrating string, and the later investigation of heat flow, that led to the development of Fourier analysis. The laws governing these distinct physical phenomena were expressed by two different partial differential equations, the wave and heat equations, and these were solved in terms of Fourier series.

起初，正是振动弦问题以及后来对热流的研究，导致了傅里叶分析的发展。支配这些不同物理现象的定律由两个不同的偏微分方程——波动方程和热传导方程——所表达，而这些方程是通过傅里叶级数求解的。

Here we want to start by describing in some detail the development of these ideas. We will do this initially in the context of the problem of the vibrating string, and we will proceed in three steps. First, we describe several physical (empirical) concepts which motivate corresponding mathematical ideas of importance for our study. These are: the role of the functions $\cos t$ , $\sin t$ , and $e^{it}$ suggested by simple harmonic motion; the use of separation of variables, derived from the phenomenon of standing waves; and the related concept of linearity, connected to the superposition of tones. Second, we derive the partial differential equation which governs the motion of the vibrating string. Finally, we will use what we learned about the physical nature of the problem (expressed mathematically) to solve the equation. In the last section, we use the same approach to study the problem of heat diffusion.

在此，我们首先详细描述这些思想的发展过程。我们将从振动弦问题的背景出发，分三步进行。首先，我们描述几个物理（经验）概念，这些概念激发了对于我们研究具有重要意义的相应数学思想。它们是：由简谐运动所提示的函数 $\cos t$ 、 $\sin t$ 和 $e^{it}$ 的作用；由驻波现象推导出的分离变量法的使用；以及与声音叠加相关的线性概念。其次，我们推导出支配振动弦运动的偏微分方程。最后，我们将利用我们所了解到的关于该问题（用数学表达）的物理性质来求解方程。在最后一节中，我们使用相同的方法来研究热扩散问题。

Given the introductory nature of this chapter and the subject matter covered, our presentation cannot be based on purely mathematical reasoning. Rather, it proceeds by plausibility arguments and aims to provide the motivation for the further rigorous analysis in the succeeding chapters. The impatient reader who wishes to begin immediately with the theorems of the subject may prefer to pass directly to the next chapter.

考虑到本章的导论性质及其涵盖的主题，我们的阐述不能完全基于纯数学推理。相反，它将通过似是而非的论证展开，旨在为后续章节中更严格的分析提供动机。那些希望立即开始学习本学科定理的没有耐心的读者，可以直接进入下一章。

===== Page 19 =====

2 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

## 1 The vibrating string

The problem consists of the study of the motion of a string fixed at its end points and allowed to vibrate freely. We have in mind physical systems such as the strings of a musical instrument. As we mentioned above, we begin with a brief description of several observable physical phenomena on which our study is based. These are:

simple harmonic motion, standing and traveling waves, harmonics and superposition of tones.

Understanding the empirical facts behind these phenomena will motivate our mathematical approach to vibrating strings.

2 第1章 傅里叶分析的起源

## 1 振动弦

该问题旨在研究一根两端固定并可自由振动的弦的运动。我们设想的是诸如乐器弦这样的物理系统。如上所述，我们首先简要描述作为我们研究基础的几个可观测物理现象。它们是：

简谐运动、驻波和行波、谐波以及声音的叠加。

理解这些现象背后的经验事实，将为我们研究振动弦的数学方法提供动机。

## Simple harmonic motion

Simple harmonic motion describes the behavior of the most basic oscillatory system (called the simple harmonic oscillator), and is therefore a natural place to start the study of vibrations. Consider a mass $\{m\}$ attached to a horizontal spring, which itself is attached to a fixed wall, and assume that the system lies on a frictionless surface.

Choose an axis whose origin coincides with the center of the mass when it is at rest (that is, the spring is neither stretched nor compressed), as shown in Figure 1. When the mass is displaced from its initial equilibrium

<center>Figure 1. Simple harmonic oscillator </center>

position and then released, it will undergo simple harmonic motion. This motion can be described mathematically once we have found the differential equation that governs the movement of the mass.

Let $y(t)$ denote the displacement of the mass at time $t$ . We assume that the spring is ideal, in the sense that it satisfies Hooke's law: the restoring force $F$ exerted by the spring on the mass is given by $F = - ky(t)$ . Here

## 简谐运动

简谐运动描述的是最基本的振荡系统（称为简谐振子）的行为，因此是研究振动的自然起点。考虑一个质量为 $\{m\}$ 的物体连接在水平弹簧上，弹簧另一端固定在墙上，并假设系统位于无摩擦的表面上。

选择一个坐标轴，其原点与物体静止时的中心重合（即弹簧既未被拉伸也未被压缩），如图1所示。当物体从其初始平衡位置被移开然后释放时，它将进行简谐运动。一旦我们找到支配物体运动的微分方程，就可以用数学描述这种运动。

设 $y(t)$ 表示物体在时间 $t$ 的位移。我们假设弹簧是理想的，即它满足胡克定律：弹簧作用在物体上的恢复力 $F$ 由 $F = - ky(t)$ 给出。这里

===== Page 20 =====

1. The vibrating string

$k > 0$ is a given physical quantity called the spring constant. Applying Newton's law (force $=$ mass $\times$ acceleration), we obtain

$$-ky(t) = my''(t),$$

where we use the notation $y^{\prime \prime}$ to denote the second derivative of $y$ with respect to $t$ .With $c = \sqrt{k / m}$ , this second order ordinary differential equation becomes

$$y^{\prime \prime}(t) + c^{2}y(t) = 0. \quad (1)$$

1. 振动弦

$k > 0$ 是一个给定的物理量，称为弹簧常数。应用牛顿定律（力 $=$ 质量 $\times$ 加速度），我们得到

$$-ky(t) = my''(t),$$

这里我们用符号 $y^{\prime \prime}$ 表示 $y$ 对 $t$ 的二阶导数。令 $c = \sqrt{k / m}$ ，这个二阶常微分方程变为

$$y^{\prime \prime}(t) + c^{2}y(t) = 0. \quad (1)$$

The general solution of equation (1) is given by

$$y(t) = a\cos ct + b\sin ct,$$

where $a$ and $b$ are constants. Clearly, all functions of this form solve equation (1), and Exercise 6 outlines a proof that these are the only (twice differentiable) solutions of that differential equation.

方程(1)的通解为

$$y(t) = a\cos ct + b\sin ct,$$

其中 $a$ 和 $b$ 是常数。显然，所有这种形式的函数都满足方程(1)，并且练习6概述了一个证明，表明这些是该微分方程仅有的（二次可微）解。

In the above expression for $y(t)$ , the quantity $c$ is given, but $a$ and $b$ can be any real numbers. In order to determine the particular solution of the equation, we must impose two initial conditions in view of the two unknown constants $a$ and $b$ . For example, if we are given $y(0)$ and $y'(0)$ , the initial position and velocity of the mass, then the solution of the physical problem is unique and given by

$$y(t) = y(0)\cos ct + \frac{y'(0)}{c}\sin ct.$$

在上述 $y(t)$ 的表达式中，量 $c$ 是给定的，但 $a$ 和 $b$ 可以是任意实数。为了确定方程的特解，鉴于有两个未知常数 $a$ 和 $b$ ，我们必须施加两个初始条件。例如，如果我们知道 $y(0)$ 和 $y'(0)$ ，即物体的初始位置和速度，那么该物理问题的解是唯一的，并由下式给出

$$y(t) = y(0)\cos ct + \frac{y'(0)}{c}\sin ct.$$

One can easily verify that there exist constants $A > 0$ and $\phi \in \mathbb{R}$ such that

$$a\cos ct + b\sin ct = A\cos (ct - \phi).$$

Because of the physical interpretation given above, one calls $A = \sqrt{a^{2} + b^{2}}$ the "amplitude" of the motion, $c$ its "natural frequency," $\phi$ its "phase" (uniquely determined up to an integer multiple of $2\pi$ ), and $2\pi /c$ the "period" of the motion.

可以很容易地验证，存在常数 $A > 0$ 和 $\phi \in \mathbb{R}$ 使得

$$a\cos ct + b\sin ct = A\cos (ct - \phi).$$

根据上面给出的物理解释，我们称 $A = \sqrt{a^{2} + b^{2}}$ 为运动的"振幅"， $c$ 为其"固有频率"， $\phi$ 为其"相位"（在相差 $2\pi$ 的整数倍的意义下唯一确定）， $2\pi /c$ 为运动的"周期"。

The typical graph of the function $A\cos (ct - \phi)$ , illustrated in Figure 2, exhibits a wavelike pattern that is obtained from translating and stretching (or shrinking) the usual graph of $\cos t$ .

函数 $A\cos (ct - \phi)$ 的典型图形如图2所示，它呈现出一种波状模式，这是通过平移和拉伸（或压缩）通常的 $\cos t$ 图形得到的。

We make two observations regarding our examination of simple harmonic motion. The first is that the mathematical description of the most elementary oscillatory system, namely simple harmonic motion, involves

关于我们对简谐运动的考察，我们做两点评论。首先，最基本的振荡系统，即简谐运动的数学描述，涉及

===== Page 21 =====

4 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

<center>Figure 2. The graph of $A\cos (ct - \phi)$ </center>

the most basic trigonometric functions $\cos t$ and $\sin t$ . It will be important in what follows to recall the connection between these functions and complex numbers, as given in Euler's identity $e^{it} = \cos t + i\sin t$ . The second observation is that simple harmonic motion is determined as a function of time by two initial conditions, one determining the position, and the other the velocity (specified, for example, at time $t = 0$ ). This property is shared by more general oscillatory systems, as we shall see below.

4 第1章 傅里叶分析的起源

<center>图2. $A\cos (ct - \phi)$ 的图形 </center>

最基础的三角函数 $\cos t$ 和 $\sin t$ 。在接下来的内容中，回忆这些函数与复数之间的联系（如欧拉恒等式 $e^{it} = \cos t + i\sin t$ 所示）将非常重要。其次，简谐运动作为时间的函数，由两个初始条件决定，一个确定位置，另一个确定速度（例如，在时间 $t = 0$ 时指定）。正如我们将在下面看到的，更一般的振荡系统也具有此性质。

## Standing and traveling waves

As it turns out, the vibrating string can be viewed in terms of one- dimensional wave motions. Here we want to describe two kinds of motions that lend themselves to simple graphic representations.

First, we consider standing waves. These are wavelike motions described by the graphs $y = u(x,t)$ developing in time $t$ as shown in Figure 3.

In other words, there is an initial profile $y = \phi (x)$ representing the wave at time $t = 0$ , and an amplifying factor $\psi (t)$ , depending on $t$ , so that $y = u(x,t)$ with

$$u(x,t) = \phi (x)\psi (t).$$

The nature of standing waves suggests the mathematical idea of "separation of variables," to which we will return later.

## 驻波和行波

事实证明，振动弦可以用一维波动来描述。这里我们想要描述两种便于用简单图形表示的运动。

首先，我们考虑驻波。这些是由图形 $y = u(x,t)$ 描述的波状运动，其随时间 $t$ 的演变如图3所示。

换句话说，存在一个初始轮廓 $y = \phi (x)$ 表示时间 $t = 0$ 时的波形，以及一个依赖于 $t$ 的放大因子 $\psi (t)$ ，使得 $y = u(x,t)$ 且有

$$u(x,t) = \phi (x)\psi (t).$$

驻波的性质提示了"分离变量法"这一数学思想，我们稍后将回到这一点。

A second type of wave motion that is often observed in nature is that of a traveling wave. Its description is particularly simple:

自然界中常观察到的第二种波动是行波。它的描述特别简单：

===== Page 22 =====

1. The vibrating string

<center>Figure 3. A standing wave at different moments in time: $t = 0$ and $t = t_0$ </center>

there is an initial profile $F(x)$ so that $u(x,t)$ equals $F(x)$ when $t = 0$ . As $t$ evolves, this profile is displaced to the right by $ct$ units, where $c$ is a positive constant, namely

$$u(x,t) = F(x - ct).$$

Graphically, the situation is depicted in Figure 4.

1. 振动弦

<center>图3. 不同时刻的驻波：$t = 0$ 和 $t = t_0$ </center>

存在一个初始轮廓 $F(x)$ ，使得当 $t = 0$ 时 $u(x,t)$ 等于 $F(x)$ 。随着 $t$ 的演变，该轮廓向右移动 $ct$ 个单位，其中 $c$ 是一个正常数，即

$$u(x,t) = F(x - ct).$$

图4描绘了这种情况。

<center>Figure 4. A traveling wave at two different moments in time: $t = 0$ and $t = t_0$ </center>

Since the movement in $t$ is at the rate $c$ , that constant represents the velocity of the wave. The function $F(x - ct)$ is a one- dimensional traveling wave moving to the right. Similarly, $u(x,t) = F(x + ct)$ is a one- dimensional traveling wave moving to the left.

<center>图4. 不同时刻的行波：$t = 0$ 和 $t = t_0$ </center>

由于随 $t$ 的运动速率为 $c$ ，该常数代表波的速度。函数 $F(x - ct)$ 是向右运动的一维行波。类似地，$u(x,t) = F(x + ct)$ 是向左运动的一维行波。

===== Page 23 =====

6 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

## Harmonics and superposition of tones

The final physical observation we want to mention (without going into any details now) is one that musicians have been aware of since time immemorial. It is the existence of harmonics, or overtones. The pure tones are accompanied by combinations of overtones which are primarily responsible for the timbre (or tone color) of the instrument. The idea of combination or superposition of tones is implemented mathematically by the basic concept of linearity, as we shall see below.

We now turn our attention to our main problem, that of describing the motion of a vibrating string. First, we derive the wave equation, that is, the partial differential equation that governs the motion of the string.

### 1.1 Derivation of the wave equation

Imagine a homogeneous string placed in the $(x,y)$ - plane, and stretched along the $x$ - axis between $x = 0$ and $x = L$ . If it is set to vibrate, its displacement $y = u(x,t)$ is then a function of $x$ and $t$ , and the goal is to derive the differential equation which governs this function.

For this purpose, we consider the string as being subdivided into a large number $N$ of masses (which we think of as individual particles) distributed uniformly along the $x$ - axis, so that the $n^{\mathrm{th}}$ particle has its $x$ - coordinate at $x_{n} = nL / N$ . We shall therefore conceive of the vibrating string as a complex system of $N$ particles, each oscillating in the vertical direction only; however, unlike the simple harmonic oscillator we considered previously, each particle will have its oscillation linked to its immediate neighbor by the tension of the string.

6 第1章 傅里叶分析的起源

## 谐波与声音的叠加

我们要提到的最后一个物理观察（现在不深入细节）是音乐家们自古以来就知道的。那就是谐波或泛音的存在。纯音伴随着泛音的组合，这些组合主要负责乐器的音色（或音质）。声音的组合或叠加的思想在数学上通过线性的基本概念来实现，我们将在下面看到。

现在我们把注意力转向主要问题，即描述振动弦的运动。首先，我们推导波动方程，即支配弦运动的偏微分方程。

### 1.1 波动方程的推导

设想一根均匀的弦放置在 $(x,y)$ - 平面内，沿着 $x$ - 轴从 $x = 0$ 到 $x = L$ 拉紧。如果使它振动，其位移 $y = u(x,t)$ 就是 $x$ 和 $t$ 的函数，我们的目标是推导出支配该函数的微分方程。

为此，我们将弦细分为大量 $N$ 个质量点（我们将其视为单个粒子），它们均匀分布在 $x$ - 轴上，使得第 $n^{\mathrm{th}}$ 个粒子的 $x$ - 坐标为 $x_{n} = nL / N$ 。因此，我们将振动弦设想为一个由 $N$ 个粒子组成的复杂系统，每个粒子仅在垂直方向振荡；然而，与我们之前考虑的简谐振子不同，每个粒子的振荡将通过弦的张力与其紧邻的粒子耦合。

<center>Figure 5. A vibrating string as a discrete system of masses </center>

<center>图5. 作为离散质量系统的振动弦 </center>

===== Page 24 =====

1. The vibrating string

We then set $y_{n}(t) = u(x_{n},t)$ , and note that $x_{n + 1} - x_{n} = h$ , with $h =$ $L / N$ . If we assume that the string has constant density $\rho >0$ , it is reasonable to assign mass equal to $\rho h$ to each particle. By Newton's law, $\rho h y_{n}^{\prime \prime}(t)$ equals the force acting on the $n^{\mathrm{th}}$ particle. We now make the simple assumption that this force is due to the effect of the two nearby particles, the ones with $x$ - coordinates at $x_{n - 1}$ and $x_{n + 1}$ (see Figure 5). We further assume that the force (or tension) coming from the right of the $n^{\mathrm{th}}$ particle is proportional to $(y_{n + 1} - y_{n}) / h$ , where $h$ is the distance between $x_{n + 1}$ and $x_{n}$ ; hence we can write the tension as

$$\left(\frac{\tau}{h}\right)\left(y_{n + 1} - y_{n}\right),$$

where $\tau >0$ is a constant equal to the coefficient of tension of the string. There is a similar force coming from the left, and it is

$$\left(\frac{\tau}{h}\right)\left(y_{n - 1} - y_{n}\right).$$

1. 振动弦

然后我们设 $y_{n}(t) = u(x_{n},t)$ ，并注意到 $x_{n + 1} - x_{n} = h$ ，其中 $h =$ $L / N$ 。如果我们假设弦具有恒定密度 $\rho >0$ ，那么为每个粒子分配质量 $\rho h$ 是合理的。根据牛顿定律，$\rho h y_{n}^{\prime \prime}(t)$ 等于作用在第 $n^{\mathrm{th}}$ 个粒子上的力。现在我们做一个简单的假设，即这个力是由于两个邻近粒子（$x$ - 坐标在 $x_{n - 1}$ 和 $x_{n + 1}$ 处的粒子）的影响（见图5）。我们进一步假设，来自第 $n^{\mathrm{th}}$ 个粒子右侧的力（或张力）与 $(y_{n + 1} - y_{n}) / h$ 成正比，其中 $h$ 是 $x_{n + 1}$ 和 $x_{n}$ 之间的距离；因此我们可以将张力写为

$$\left(\frac{\tau}{h}\right)\left(y_{n + 1} - y_{n}\right),$$

其中 $\tau >0$ 是一个常数，等于弦的张力系数。有一个类似的来自左侧的力，即

$$\left(\frac{\tau}{h}\right)\left(y_{n - 1} - y_{n}\right).$$

Altogether, adding these forces gives us the desired relation between the oscillators $y_{n}(t)$ , namely

$$\rho h y_{n}^{\prime \prime}(t) = \frac{\tau}{h}\left\{y_{n + 1}(t) + y_{n - 1}(t) - 2y_{n}(t)\right\} . \quad (2)$$

将这些力加起来，就得到了振荡器 $y_{n}(t)$ 之间所需的关系，即

$$\rho h y_{n}^{\prime \prime}(t) = \frac{\tau}{h}\left\{y_{n + 1}(t) + y_{n - 1}(t) - 2y_{n}(t)\right\} . \quad (2)$$

On the one hand, with the notation chosen above, we see that

$$y_{n + 1}(t) + y_{n - 1}(t) - 2y_{n}(t) = u(x_{n} + h,t) + u(x_{n} - h,t) - 2u(x_{n},t).$$

On the other hand, for any reasonable function $F(x)$ (that is, one that has continuous second derivatives) we have

$$\frac{F(x + h) + F(x - h) - 2F(x)}{h^2}\to F''(x)\quad \mathrm{as} h\to 0.$$

Thus we may conclude, after dividing by $h$ in (2) and letting $h$ tend to zero (that is, $N$ goes to infinity), that

$$\rho \frac{\partial^2u}{\partial t^2} = \tau \frac{\partial^2u}{\partial x^2},$$

or

$$\frac{1}{c^2}\frac{\partial^2u}{\partial t^2} = \frac{\partial^2u}{\partial x^2},\quad \mathrm{with} c = \sqrt{\tau / \rho}.$$

This relation is known as the one- dimensional wave equation, or more simply as the wave equation. For reasons that will be apparent later, the coefficient $c > 0$ is called the velocity of the motion.

一方面，使用上面选择的符号，我们看到

$$y_{n + 1}(t) + y_{n - 1}(t) - 2y_{n}(t) = u(x_{n} + h,t) + u(x_{n} - h,t) - 2u(x_{n},t).$$

另一方面，对于任何性质良好的函数 $F(x)$ （即具有连续二阶导数的函数），我们有

$$\frac{F(x + h) + F(x - h) - 2F(x)}{h^2}\to F''(x)\quad \mathrm{as} h\to 0.$$

因此，在(2)式中除以 $h$ 并令 $h$ 趋于零（即 $N$ 趋于无穷大）后，我们可以得出结论：

$$\rho \frac{\partial^2u}{\partial t^2} = \tau \frac{\partial^2u}{\partial x^2},$$

或

$$\frac{1}{c^2}\frac{\partial^2u}{\partial t^2} = \frac{\partial^2u}{\partial x^2},\quad \mathrm{with} c = \sqrt{\tau / \rho}.$$

这个关系式被称为一维波动方程，或简称为波动方程。出于以后会明确的原因，系数 $c > 0$ 被称为运动的速度。

===== Page 25 =====

8 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

In connection with this partial differential equation, we make an important simplifying mathematical remark. This has to do with scaling, or in the language of physics, a "change of units." That is, we can think of the coordinate $x$ as $x = aX$ where $a$ is an appropriate positive constant. Now, in terms of the new coordinate $X$ , the interval $0\leq x\leq L$ becomes $0\leq X\leq L / a$ . Similarly, we can replace the time coordinate $t$ by $t = bT$ where $b$ is another positive constant. If we set $U(X,T) = u(x,t)$ , then

$$\frac{\partial U}{\partial X} = a\frac{\partial u}{\partial x},\qquad \frac{\partial^2U}{\partial X^2} = a^2\frac{\partial^2u}{\partial x^2},$$

and similarly for the derivatives in $t$ . So if we choose $a$ and $b$ appropriately, we can transform the one- dimensional wave equation into

$$\frac{\partial^2U}{\partial T^2} = \frac{\partial^2U}{\partial X^2},$$

which has the effect of setting the velocity $c$ equal to 1. Moreover, we have the freedom to transform the interval $0\leq x\leq L$ to $0\leq X\leq \pi$ . (We shall see that the choice of $\pi$ is convenient in many circumstances.) All this is accomplished by taking $a = L / \pi$ and $b = L / (c\pi)$ . Once we solve the new equation, we can of course return to the original equation by making the inverse change of variables. Hence, we do not sacrifice generality by thinking of the wave equation as given on the interval $[0,\pi ]$ with velocity $c = 1$ .

8 第1章 傅里叶分析的起源

关于这个偏微分方程，我们做一个重要的简化数学说明。这与缩放有关，或者用物理学的语言说，是"单位变换"。也就是说，我们可以将坐标 $x$ 视为 $x = aX$ ，其中 $a$ 是一个适当的正常数。现在，用新坐标 $X$ 表示，区间 $0\leq x\leq L$ 变为 $0\leq X\leq L / a$ 。类似地，我们可以用 $t = bT$ 替换时间坐标 $t$ ，其中 $b$ 是另一个正常数。如果我们设 $U(X,T) = u(x,t)$ ，那么

$$\frac{\partial U}{\partial X} = a\frac{\partial u}{\partial x},\qquad \frac{\partial^2U}{\partial X^2} = a^2\frac{\partial^2u}{\partial x^2},$$

并且对 $t$ 的导数也有类似关系。因此，如果我们恰当地选择 $a$ 和 $b$ ，就可以将一维波动方程变换为

$$\frac{\partial^2U}{\partial T^2} = \frac{\partial^2U}{\partial X^2},$$

其效果是将速度 $c$ 设为1。此外，我们还可以自由地将区间 $0\leq x\leq L$ 变换为 $0\leq X\leq \pi$ 。（我们将看到，在许多情况下选择 $\pi$ 是方便的。）所有这些通过取 $a = L / \pi$ 和 $b = L / (c\pi)$ 即可实现。一旦我们解出了新方程，当然可以通过逆变量变换返回到原始方程。因此，将波动方程视为定义在区间 $[0,\pi ]$ 上且速度 $c = 1$ ，并不会损失一般性。

### 1.2 Solution to the wave equation

Having derived the equation for the vibrating string, we now explain two methods to solve it:

using traveling waves, using the superposition of standing waves.

While the first approach is very simple and elegant, it does not directly give full insight into the problem; the second method accomplishes that, and moreover is of wide applicability. It was first believed that the second method applied only in the simple cases where the initial position and velocity of the string were themselves given as a superposition of standing waves. However, as a consequence of Fourier's ideas, it became clear that the problem could be worked either way for all initial conditions.

### 1.2 波动方程的解

推导出振动弦的方程后，我们现在解释两种求解方法：

使用行波，使用驻波的叠加。

虽然第一种方法非常简单和优雅，但它不能直接给出问题的完整洞察；第二种方法做到了这一点，而且具有广泛的适用性。最初人们认为，第二种方法仅适用于弦的初始位置和速度本身被表示为驻波叠加的简单情况。然而，作为傅里叶思想的结果，很明显，对于所有初始条件，该问题都可以用任何一种方法解决。

===== Page 26 =====

1. The vibrating string

## Traveling waves

To simplify matters as before, we assume that $c = 1$ and $L = \pi$ , so that the equation we wish to solve becomes

$$\frac{\partial^2u}{\partial t^2} = \frac{\partial^2u}{\partial x^2}\quad \mathrm{on} 0\leq x\leq \pi .$$

The crucial observation is the following: if $F$ is any twice differentiable function, then $u(x,t) = F(x + t)$ and $u(x,t) = F(x - t)$ solve the wave equation. The verification of this is a simple exercise in differentiation. Note that the graph of $u(x,t) = F(x - t)$ at time $t = 0$ is simply the graph of $F$ , and that at time $t = 1$ it becomes the graph of $F$ translated to the right by 1. Therefore, we recognize that $F(x - t)$ is a traveling wave which travels to the right with speed 1. Similarly, $u(x,t) = F(x + t)$ is a wave traveling to the left with speed 1. These motions are depicted in Figure 6.

1. 振动弦

## 行波

像之前一样简化问题，我们假设 $c = 1$ 且 $L = \pi$ ，这样我们要求解的方程变为

$$\frac{\partial^2u}{\partial t^2} = \frac{\partial^2u}{\partial x^2}\quad \mathrm{on} 0\leq x\leq \pi .$$

关键的观察如下：如果 $F$ 是任意二次可微函数，那么 $u(x,t) = F(x + t)$ 和 $u(x,t) = F(x - t)$ 都满足波动方程。验证这一点是微分中的一个简单练习。注意，$u(x,t) = F(x - t)$ 在时间 $t = 0$ 时的图形就是 $F$ 的图形，而在时间 $t = 1$ 时，它变成了 $F$ 的图形向右平移1个单位。因此，我们认识到 $F(x - t)$ 是一个以速度1向右传播的行波。类似地，$u(x,t) = F(x + t)$ 是一个以速度1向左传播的行波。这些运动如图6所示。

<center>Figure 6. Waves traveling in both directions </center>

<center>图6. 向两个方向传播的波 </center>

Our discussion of tones and their combinations leads us to observe that the wave equation is linear. This means that if $u(x,t)$ and $v(x,t)$ are particular solutions, then so is $\alpha u(x,t) + \beta v(x,t)$ , where $\alpha$ and $\beta$ are any constants. Therefore, we may superpose two waves traveling in opposite directions to find that whenever $F$ and $G$ are twice differentiable functions, then

$$u(x,t) = F(x + t) + G(x - t)$$

is a solution of the wave equation. In fact, we now show that all solutions take this form.

我们对声音及其组合的讨论引导我们观察到波动方程是线性的。这意味着，如果 $u(x,t)$ 和 $v(x,t)$ 是特解，那么 $\alpha u(x,t) + \beta v(x,t)$ 也是解，其中 $\alpha$ 和 $\beta$ 是任意常数。因此，我们可以叠加两个反向传播的波，发现只要 $F$ 和 $G$ 是二次可微函数，那么

$$u(x,t) = F(x + t) + G(x - t)$$

就是波动方程的一个解。事实上，我们现在证明所有解都具有这种形式。

We drop for the moment the assumption that $0\leq x\leq \pi$ , and suppose that $u$ is a twice differentiable function which solves the wave equation

我们暂时去掉 $0\leq x\leq \pi$ 的假设，并假设 $u$ 是满足波动方程的二次可微函数

===== Page 27 =====

10 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

for all real $x$ and $t$ . Consider the following new set of variables $\xi = x + t$ , $\eta = x - t$ , and define $v(\xi ,\eta) = u(x,t)$ . The change of variables formula shows that $v$ satisfies

$$\frac{\partial^2v}{\partial\xi\partial\eta} = 0.$$

Integrating this relation twice gives $v(\xi ,\eta) = F(\xi) + G(\eta)$ , which then implies

$$u(x,t) = F(x + t) + G(x - t),$$

for some functions $F$ and $G$ .

10 第1章 傅里叶分析的起源

对于所有实数 $x$ 和 $t$ 。考虑以下新变量组 $\xi = x + t$ , $\eta = x - t$ ，并定义 $v(\xi ,\eta) = u(x,t)$ 。变量替换公式表明 $v$ 满足

$$\frac{\partial^2v}{\partial\xi\partial\eta} = 0.$$

将这个关系式积分两次得到 $v(\xi ,\eta) = F(\xi) + G(\eta)$ ，进而推出

$$u(x,t) = F(x + t) + G(x - t),$$

其中 $F$ 和 $G$ 是某个函数。

We must now connect this result with our original problem, that is, the physical motion of a string. There, we imposed the restrictions $0\leq x\leq \pi$ , the initial shape of the string $u(x,0) = f(x)$ , and also the fact that the string has fixed end points, namely $u(0,t) = u(\pi ,t) = 0$ for all $t$ . To use the simple observation above, we first extend $f$ to all of $\mathbb{R}$ by making it odd $^1$ on $[-\pi ,\pi ]$ , and then periodic $^2$ in $x$ of period $2\pi$ , and similarly for $u(x,t)$ , the solution of our problem. Then the extension $u$ solves the wave equation on all of $\mathbb{R}$ , and $u(x,0) = f(x)$ for all $x\in \mathbb{R}$ . Therefore, $u(x,t) = F(x + t) + G(x - t)$ , and setting $t = 0$ we find that

$$F(x) + G(x) = f(x).$$

Since many choices of $F$ and $G$ will satisfy this identity, this suggests imposing another initial condition on $u$ (similar to the two initial conditions in the case of simple harmonic motion), namely the initial velocity of the string which we denote by $g(x)$ :

$$\frac{\partial u}{\partial t} (x,0) = g(x),$$

where of course $g(0) = g(\pi) = 0$ . Again, we extend $g$ to $\mathbb{R}$ first by making it odd over $[-\pi ,\pi ]$ , and then periodic of period $2\pi$ . The two initial conditions of position and velocity now translate into the following system:

我们现在必须将这个结果与我们最初的问题，即弦的物理运动联系起来。在那里，我们施加了限制 $0\leq x\leq \pi$ ，弦的初始形状 $u(x,0) = f(x)$ ，以及弦具有固定端点的事实，即对所有 $t$ 有 $u(0,t) = u(\pi ,t) = 0$ 。为了利用上面的简单观察，我们首先将 $f$ 扩展到整个 $\mathbb{R}$ ，方法是在 $[-\pi ,\pi ]$ 上使其成为奇函数 $^1$ ，然后在 $x$ 上使其成为周期为 $2\pi$ 的周期函数 $^2$ ，对我们问题的解 $u(x,t)$ 也做类似处理。那么扩展后的 $u$ 在整个 $\mathbb{R}$ 上满足波动方程，并且对所有 $x\in \mathbb{R}$ 有 $u(x,0) = f(x)$ 。因此，$u(x,t) = F(x + t) + G(x - t)$ ，令 $t = 0$ 我们得到

$$F(x) + G(x) = f(x).$$

由于许多 $F$ 和 $G$ 的选择都能满足这个恒等式，这表明需要对 $u$ 施加另一个初始条件（类似于简谐运动情况下的两个初始条件），即弦的初始速度，我们记为 $g(x)$ ：

$$\frac{\partial u}{\partial t} (x,0) = g(x),$$

当然其中 $g(0) = g(\pi) = 0$ 。同样，我们首先将 $g$ 扩展到 $\mathbb{R}$ ，方法是在 $[-\pi ,\pi ]$ 上使其成为奇函数，然后使其成为周期为 $2\pi$ 的周期函数。位置和速度的两个初始条件现在转化为以下方程组：

$^1$ 这意味着 $f(-x) = -f(x)$ 。$^2$ 因此 $f(x + 2\pi k) = f(x)$ 对所有整数 $k$ 成立。

$^1$ This means that $f(-x) = -f(x)$ . $^2$ So that $f(x + 2\pi k) = f(x)$ for all integers $k$ .

===== Page 28 =====

1. The vibrating string

Differentiating the first equation and adding it to the second, we obtain

$$2F^{\prime}(x) = f^{\prime}(x) + g(x).$$

Similarly

$$2G^{\prime}(x) = f^{\prime}(x) - g(x),$$

and hence there are constants $C_1$ and $C_2$ so that

$$F(x) = \frac{1}{2}\left[f(x) + \int_0^x g(y)dy\right] + C_1$$

and

$$G(x) = \frac{1}{2}\left[f(x) - \int_0^x g(y)dy\right] + C_2.$$

Since $F(x) + G(x) = f(x)$ we conclude that $C_1 + C_2 = 0$ , and therefore, our final solution of the wave equation with the given initial conditions takes the form

$$u(x,t) = \frac{1}{2}\left[f(x + t) + f(x - t)\right] + \frac{1}{2}\int_{x - t}^{x + t}g(y)dy.$$

1. 振动弦

对第一个方程求导并加到第二个方程，我们得到

$$2F^{\prime}(x) = f^{\prime}(x) + g(x).$$

类似地

$$2G^{\prime}(x) = f^{\prime}(x) - g(x),$$

因此存在常数 $C_1$ 和 $C_2$ 使得

$$F(x) = \frac{1}{2}\left[f(x) + \int_0^x g(y)dy\right] + C_1$$

且

$$G(x) = \frac{1}{2}\left[f(x) - \int_0^x g(y)dy\right] + C_2.$$

由于 $F(x) + G(x) = f(x)$ ，我们得出结论 $C_1 + C_2 = 0$ ，因此，在给定初始条件下，我们波动方程的最终解形式为

$$u(x,t) = \frac{1}{2}\left[f(x + t) + f(x - t)\right] + \frac{1}{2}\int_{x - t}^{x + t}g(y)dy.$$

The form of this solution is known as d'Alembert's formula. Observe that the extensions we chose for $f$ and $g$ guarantee that the string always has fixed ends, that is, $u(0,t) = u(\pi ,t) = 0$ for all $t$ .

该解的形式被称为达朗贝尔公式。注意我们为 $f$ 和 $g$ 选择的扩展保证了弦始终具有固定端点，即对所有 $t$ 有 $u(0,t) = u(\pi ,t) = 0$ 。

A final remark is in order. The passage from $t\geq 0$ to $t\in \mathbb{R}$ , and then back to $t\geq 0$ , which was made above, exhibits the time reversal property of the wave equation. In other words, a solution $u$ to the wave equation for $t\geq 0$ , leads to a solution $u^{- }$ defined for negative time $t< 0$ simply by setting $u^{- }(x,t) = u(x, - t)$ , a fact which follows from the invariance of the wave equation under the transformation $t\mapsto - t$ . The situation is quite different in the case of the heat equation.

最后需要说明一点。上面进行的从 $t\geq 0$ 到 $t\in \mathbb{R}$ ，再回到 $t\geq 0$ 的过程，展示了波动方程的时间反演性质。换句话说，波动方程对于 $t\geq 0$ 的一个解 $u$ ，可以通过简单地设置 $u^{- }(x,t) = u(x, - t)$ 导出一个定义在负时间 $t< 0$ 的解 $u^{- }$ ，这一事实源于波动方程在变换 $t\mapsto - t$ 下的不变性。热传导方程的情况则完全不同。

## Superposition of standing waves

We turn to the second method of solving the wave equation, which is based on two fundamental conclusions from our previous physical observations. By our considerations of standing waves, we are led to look for special solutions to the wave equation which are of the form $\phi (x)\psi (t)$ . This procedure, which works equally well in other contexts (in the case of the heat equation, for instance), is called separation of variables and constructs solutions that are called pure tones. Then by the linearity

## 驻波的叠加

我们转向求解波动方程的第二种方法，它基于我们之前物理观察的两个基本结论。通过对驻波的考虑，我们被引导去寻找形如 $\phi (x)\psi (t)$ 的波动方程的特解。这个过程被称为分离变量法，它在其他情况下（例如热传导方程的情况）也同样有效，并构造出称为纯音的解。然后通过线性

===== Page 29 =====

12 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

of the wave equation, we can expect to combine these pure tones into a more complex combination of sound. Pushing this idea further, we can hope ultimately to express the general solution of the wave equation in terms of sums of these particular solutions.

12 第1章 傅里叶分析的起源

波动方程的线性性质，我们可以预期将这些纯音组合成更复杂的声音组合。进一步推广这个想法，我们最终希望用这些特解的和来表示波动方程的通解。

Note that one side of the wave equation involves only differentiation in $x$ , while the other, only differentiation in $t$ . This observation provides another reason to look for solutions of the equation in the form $u(x,t) = \phi (x)\psi (t)$ (that is, to "separate variables"), the hope being to reduce a difficult partial differential equation into a system of simpler ordinary differential equations. In the case of the wave equation, with $u$ of the above form, we get

$$\phi (x)\psi^{\prime \prime}(t) = \phi^{\prime \prime}(x)\psi (t),$$

and therefore

$$\frac{\psi^{\prime\prime}(t)}{\psi(t)} = \frac{\phi^{\prime\prime}(x)}{\phi(x)}.$$

注意波动方程的一边只涉及对 $x$ 的微分，而另一边只涉及对 $t$ 的微分。这一观察为寻找形如 $u(x,t) = \phi (x)\psi (t)$ 的解（即"分离变量"）提供了另一个理由，希望将一个困难的偏微分方程简化为一个由更简单的常微分方程组成的系统。在波动方程的情况下，对于上述形式的 $u$ ，我们得到

$$\phi (x)\psi^{\prime \prime}(t) = \phi^{\prime \prime}(x)\psi (t),$$

因此

$$\frac{\psi^{\prime\prime}(t)}{\psi(t)} = \frac{\phi^{\prime\prime}(x)}{\phi(x)}.$$

The key observation here is that the left- hand side depends only on $t$ and the right- hand side only on $x$ . This can happen only if both sides are equal to a constant, say $\lambda$ . Therefore, the wave equation reduces to the following

$$\left\{ \begin{array}{ll}\psi^{\prime \prime}(t) - \lambda \psi (t) = 0\\ \phi^{\prime \prime}(x) - \lambda \phi (x) = 0. \end{array} \right. \quad (3)$$

这里的关键观察是左边只依赖于 $t$ ，右边只依赖于 $x$ 。这只有当两边都等于一个常数，比如说 $\lambda$ 时才可能发生。因此，波动方程简化为以下形式

$$\left\{ \begin{array}{ll}\psi^{\prime \prime}(t) - \lambda \psi (t) = 0\\ \phi^{\prime \prime}(x) - \lambda \phi (x) = 0. \end{array} \right. \quad (3)$$

We focus our attention on the first equation in the above system. At this point, the reader will recognize the equation we obtained in the study of simple harmonic motion. Note that we need to consider only the case when $\lambda < 0$ , since when $\lambda \geq 0$ the solution $\psi$ will not oscillate as time varies. Therefore, we may write $\lambda = - m^2$ , and the solution of the equation is then given by

$$\psi (t) = A\cos mt + B\sin mt.$$

Similarly, we find that the solution of the second equation in (3) is

$$\phi (x) = \tilde{A}\cos mx + \tilde{B}\sin mx.$$

Now we take into account that the string is attached at $x = 0$ and $x = \pi$ . This translates into $\phi (0) = \phi (\pi) = 0$ , which in turn gives $\tilde{A} = 0$ , and if $\tilde{B} \neq 0$ , then $m$ must be an integer. If $m = 0$ , the solution vanishes identically, and if $m \leq - 1$ , we may rename the constants and reduce to

我们把注意力集中在上方程组中的第一个方程。此时，读者会认出我们在研究简谐运动时得到的方程。注意我们只需要考虑 $\lambda < 0$ 的情况，因为当 $\lambda \geq 0$ 时，解 $\psi$ 不会随时间变化而振荡。因此，我们可以写 $\lambda = - m^2$ ，然后方程的解为

$$\psi (t) = A\cos mt + B\sin mt.$$

类似地，我们发现方程(3)中第二个方程的解为

$$\phi (x) = \tilde{A}\cos mx + \tilde{B}\sin mx.$$

现在我们考虑到弦固定在 $x = 0$ 和 $x = \pi$ 处。这转化为 $\phi (0) = \phi (\pi) = 0$ ，这进而给出 $\tilde{A} = 0$ ，并且如果 $\tilde{B} \neq 0$ ，那么 $m$ 必须是整数。如果 $m = 0$ ，解恒为零；如果 $m \leq - 1$ ，我们可以重新命名常数并简化为

===== Page 30 =====

1. The vibrating string

the case $m \geq 1$ since the function $\sin y$ is odd and $\cos y$ is even. Finally, we arrive at the guess that for each $m \geq 1$ , the function

$$u_{m}(x,t) = (A_{m}\cos mt + B_{m}\sin mt)\sin mx,$$

which we recognize as a standing wave, is a solution to the wave equation. Note that in the above argument we divided by $\phi$ and $\psi$ , which sometimes vanish, so one must actually check by hand that the standing wave $u_{m}$ solves the equation. This straightforward calculation is left as an exercise to the reader.

1. 振动弦

到 $m \geq 1$ 的情况，因为函数 $\sin y$ 是奇的，$\cos y$ 是偶的。最后，我们猜测对于每个 $m \geq 1$ ，函数

$$u_{m}(x,t) = (A_{m}\cos mt + B_{m}\sin mt)\sin mx,$$

我们将其视为一个驻波，是波动方程的一个解。注意在上述论证中，我们除以了 $\phi$ 和 $\psi$ ，它们有时可能为零，所以必须实际检验驻波 $u_{m}$ 是否满足方程。这个直接的计算留给读者作为练习。

Before proceeding further with the analysis of the wave equation, we pause to discuss standing waves in more detail. The terminology comes from looking at the graph of $u_{m}(x,t)$ for each fixed $t$ . Suppose first that $m = 1$ , and take $u(x,t) = \cos t \sin x$ . Then, Figure 7 (a) gives the graph of $u$ for different values of $t$ .

在进一步分析波动方程之前，我们停下来更详细地讨论驻波。这个术语来源于观察每个固定 $t$ 下 $u_{m}(x,t)$ 的图形。首先假设 $m = 1$ ，取 $u(x,t) = \cos t \sin x$ 。那么，图7(a)给出了 $u$ 在不同 $t$ 值下的图形。

<center>Figure 7. Fundamental tone (a) and overtones (b) at different moments in time </center>

<center>图7. 不同时刻的基音(a)和泛音(b) </center>

The case $m = 1$ corresponds to the fundamental tone or first harmonic of the vibrating string.

We now take $m = 2$ and look at $u(x,t) = \cos 2t \sin 2x$ . This corresponds to the first overtone or second harmonic, and this motion is described in Figure 7 (b). Note that $u(\pi /2,t) = 0$ for all $t$ . Such points, which remain motionless in time, are called nodes, while points whose motion has maximum amplitude are named anti- nodes.

$m = 1$ 的情况对应于振动弦的基音或一次谐波。

我们现在取 $m = 2$ 并观察 $u(x,t) = \cos 2t \sin 2x$ 。这对应于一次泛音或二次谐波，其运动如图7(b)所示。注意对所有 $t$ 有 $u(\pi /2,t) = 0$ 。这些在时间上保持静止的点称为节点，而运动幅度最大的点称为反节点。

For higher values of $m$ we get more overtones or higher harmonics. Note that as $m$ increases, the frequency increases, and the period $2\pi /m$

对于更高的 $m$ 值，我们得到更多的泛音或更高次谐波。注意随着 $m$ 的增加，频率增加，周期 $2\pi /m$

===== Page 31 =====

14 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

decreases. Therefore, the fundamental tone has a lower frequency than the overtones.

14 第1章 傅里叶分析的起源

减小。因此，基音的频率低于泛音。

We now return to the original problem. Recall that the wave equation is linear in the sense that if $u$ and $v$ solve the equation, so does $\alpha u + \beta v$ for any constants $\alpha$ and $\beta$ . This allows us to construct more solutions by taking linear combinations of the standing waves $u_{m}$ . This technique, called superposition, leads to our final guess for a solution of the wave equation

$$u(x,t) = \sum_{m = 1}^{\infty}(A_{m}\cos mt + B_{m}\sin mt)\sin mx. \quad (4)$$

Note that the above sum is infinite, so that questions of convergence arise, but since most of our arguments so far are formal, we will not worry about this point now.

现在我们回到最初的问题。回顾一下，波动方程是线性的，这意味着如果 $u$ 和 $v$ 是方程的解，那么对于任意常数 $\alpha$ 和 $\beta$ ，$\alpha u + \beta v$ 也是解。这允许我们通过取驻波 $u_{m}$ 的线性组合来构造更多的解。这种称为叠加的方法，引导我们得到波动方程解的最终猜测

$$u(x,t) = \sum_{m = 1}^{\infty}(A_{m}\cos mt + B_{m}\sin mt)\sin mx. \quad (4)$$

注意上述和是无穷的，因此出现了收敛性问题，但由于我们到目前为止的大部分论证都是形式上的，我们现在不用担心这一点。

Suppose the above expression gave all the solutions to the wave equation. If we then require that the initial position of the string at time $t = 0$ is given by the shape of the graph of the function $f$ on $[0,\pi ]$ , with of course $f(0) = f(\pi) = 0$ , we would have $u(x,0) = f(x)$ , hence

$$\sum_{m = 1}^{\infty}A_{m}\sin mx = f(x).$$

Since the initial shape of the string can be any reasonable function $f$ , we must ask the following basic question:

Given a function $f$ on $[0,\pi ]$ (with $f(0) = f(\pi) = 0$ ), can we find coefficients $A_{m}$ so that

$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx? \quad (5)$$

假设上述表达式给出了波动方程的所有解。如果我们要求弦在时间 $t = 0$ 时的初始位置由函数 $f$ 在 $[0,\pi ]$ 上的图形形状给出，当然有 $f(0) = f(\pi) = 0$ ，那么我们就得到 $u(x,0) = f(x)$ ，因此

$$\sum_{m = 1}^{\infty}A_{m}\sin mx = f(x).$$

由于弦的初始形状可以是任何合理的函数 $f$ ，我们必须问以下基本问题：

给定一个定义在 $[0,\pi ]$ 上的函数 $f$ （且 $f(0) = f(\pi) = 0$ ），我们能找到系数 $A_{m}$ 使得

$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx? \quad (5)$$

This question is stated loosely, but a lot of our effort in the next two chapters of this book will be to formulate the question precisely and attempt to answer it. This was the basic problem that initiated the study of Fourier analysis.

这个问题表述得比较宽泛，但本书接下来两章的大量工作将致力于精确地表述这个问题并试图回答它。这是引发傅里叶分析研究的基本问题。

A simple observation allows us to guess a formula giving $A_{m}$ if the expansion (5) were to hold. Indeed, we multiply both sides by $\sin nx$

一个简单的观察使我们能够猜测如果展开式(5)成立，那么给出 $A_{m}$ 的公式。实际上，我们将两边乘以 $\sin nx$

===== Page 32 =====

1. The vibrating string

and integrate between $[0,\pi ]$ ; working formally, we obtain

$$\int_{0}^{\pi}f(x)\sin nxdx = \int_{0}^{\pi}\left(\sum_{m = 1}^{\infty}A_{m}\sin mx\right)\sin nxdx$$ $$= \sum_{m = 1}^{\infty}A_{m}\int_{0}^{\pi}\sin mx\sin nxdx = A_{n}\cdot \frac{\pi}{2},$$

where we have used the fact that

$$\int_{0}^{\pi}\sin mx \sin nx dx = 0 \quad \text{when } m \neq n, \quad \text{and } = \frac{\pi}{2} \quad \text{when } m = n.$$

Therefore, the guess for $A_{n}$ , called the $n^{\mathrm{th}}$ Fourier sine coefficient of $f$ , is

$$A_{n} = \frac{2}{\pi}\int_{0}^{\pi}f(x)\sin nxdx.$$

1. 振动弦

并在 $[0,\pi ]$ 上积分；形式地进行计算，我们得到

$$\int_{0}^{\pi}f(x)\sin nxdx = \int_{0}^{\pi}\left(\sum_{m = 1}^{\infty}A_{m}\sin mx\right)\sin nxdx$$ $$= \sum_{m = 1}^{\infty}A_{m}\int_{0}^{\pi}\sin mx\sin nxdx = A_{n}\cdot \frac{\pi}{2},$$

这里我们利用了事实

$$\int_{0}^{\pi}\sin mx \sin nx dx = 0 \quad \text{当 } m \neq n, \quad \text{且 } = \frac{\pi}{2} \quad \text{当 } m = n.$$

因此，对 $A_{n}$ 的猜测，称为 $f$ 的第 $n^{\mathrm{th}}$ 傅里叶正弦系数，为

$$A_{n} = \frac{2}{\pi}\int_{0}^{\pi}f(x)\sin nxdx.$$

We shall return to this formula, and other similar ones, later.

One can transform the question about Fourier sine series on $[0,\pi ]$ to a more general question on the interval $[- \pi ,\pi ]$ . If we could express $f$ on $[0,\pi ]$ in terms of a sine series, then this expansion would also hold on $[- \pi ,\pi ]$ if we extend $f$ to this interval by making it odd. Similarly, one can ask if an even function $g(x)$ on $[- \pi ,\pi ]$ can be expressed as a cosine series, namely

$$g(x) = \sum_{m = 0}^{\infty}A_{m}^{\prime}\cos mx.$$

More generally, since an arbitrary function $F$ on $[- \pi ,\pi ]$ can be expressed as $f + g$ , where $f$ is odd and $g$ is even, we may ask if $F$ can be written as

$$F(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx + \sum_{m = 0}^{\infty}A_{m}^{\prime}\cos mx,$$

or by applying Euler's identity $e^{ix} = \cos x + i\sin x$ , we could hope that $F$ takes the form

$$F(x) = \sum_{m = -\infty}^{\infty}a_{m}e^{imx}.$$

我们将在后面回到这个公式以及其他类似的公式。

我们可以将关于 $[0,\pi ]$ 上傅里叶正弦级数的问题转化为一个在 $[- \pi ,\pi ]$ 区间上更一般的问题。如果我们能够用正弦级数表示 $[0,\pi ]$ 上的 $f$ ，那么通过将 $f$ 奇延拓到这个区间，这个展开式也将在 $[- \pi ,\pi ]$ 上成立。类似地，我们可以问，$[- \pi ,\pi ]$ 上的偶函数 $g(x)$ 是否可以用余弦级数表示，即

$$g(x) = \sum_{m = 0}^{\infty}A_{m}^{\prime}\cos mx.$$

更一般地，由于 $[- \pi ,\pi ]$ 上的任意函数 $F$ 可以表示为 $f + g$ ，其中 $f$ 是奇函数，$g$ 是偶函数，我们可以问 $F$ 是否能写为

$$F(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx + \sum_{m = 0}^{\infty}A_{m}^{\prime}\cos mx,$$

或者通过应用欧拉恒等式 $e^{ix} = \cos x + i\sin x$ ，我们可以期望 $F$ 具有形式

$$F(x) = \sum_{m = -\infty}^{\infty}a_{m}e^{imx}.$$

===== Page 33 =====

16 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

By analogy with (6), we can use the fact that

$$\int_{-\pi}^{\pi} e^{imx} e^{-inx} dx = 0 \quad \text{when } m \neq n, \quad \text{and } = 2\pi \quad \text{when } m = n.$$

to see that one expects that

$$a_{n} = \frac{1}{2\pi}\int_{-\pi}^{\pi}F(x)e^{-inx}dx.$$

16 第1章 傅里叶分析的起源

与(6)式类比，我们可以利用事实

$$\int_{-\pi}^{\pi} e^{imx} e^{-inx} dx = 0 \quad \text{当 } m \neq n, \quad \text{且 } = 2\pi \quad \text{当 } m = n.$$

可以看出我们期望

$$a_{n} = \frac{1}{2\pi}\int_{-\pi}^{\pi}F(x)e^{-inx}dx.$$

The quantity $a_{n}$ is called the $n^{\mathrm{th}}$ Fourier coefficient of $F$ . We can now reformulate the problem raised above:

Question: Given any reasonable function $F$ on $[-\pi ,\pi ]$ , with Fourier coefficients defined above, is it true that

$$F(x) = \sum_{m = -\infty}^{\infty}a_{m}e^{imx}? \quad (7)$$

This formulation of the problem, in terms of complex exponentials, is the form we shall use the most in what follows.

量 $a_{n}$ 被称为 $F$ 的第 $n^{\mathrm{th}}$ 傅里叶系数。我们现在可以重新表述上面提出的问题：

问题：给定 $[-\pi ,\pi ]$ 上任何合理的函数 $F$ ，其傅里叶系数如上定义，是否真的有

$$F(x) = \sum_{m = -\infty}^{\infty}a_{m}e^{imx}? \quad (7)$$

这个问题以复指数形式的表述，是我们在后续内容中最常使用的形式。

Joseph Fourier (1768- 1830) was the first to believe that an "arbitrary" function $F$ could be given as a series (7). In other words, his idea was that any function is the linear combination (possibly infinite) of the most basic trigonometric functions $\sin mx$ and $\cos mx$ , where $m$ ranges over the integers.⁴ Although this idea was implicit in earlier work, Fourier had the conviction that his predecessors lacked, and he used it in his study of heat diffusion; this began the subject of "Fourier analysis." This discipline, which was first developed to solve certain physical problems, has proved to have many applications in mathematics and other fields as well, as we shall see later.

约瑟夫·傅里叶 (1768-1830) 是第一个相信一个"任意的"函数 $F$ 可以表示为级数(7)的人。换句话说，他的思想是任何函数都是最基本的三角函数 $\sin mx$ 和 $\cos mx$ 的（可能是无穷）线性组合，其中 $m$ 取遍整数。⁴ 尽管这个想法在早期的工作中已有暗示，但傅里叶拥有其前辈所缺乏的信念，并将其应用于他对热扩散的研究；这开创了"傅里叶分析"这一学科。正如我们稍后将看到的，这个最初为解决某些物理问题而发展的学科，已被证明在数学和其他领域也有许多应用。

We return to the wave equation. To formulate the problem correctly, we must impose two initial conditions, as our experience with simple harmonic motion and traveling waves indicated. The conditions assign the initial position and velocity of the string. That is, we require that $u$ satisfy the differential equation and the two conditions

$$u(x,0) = f(x)\quad \mathrm{and}\quad \frac{\partial u}{\partial t} (x,0) = g(x),$$

我们回到波动方程。为了正确地表述问题，我们必须施加两个初始条件，正如我们从简谐运动和行波的经验中所知。这些条件指定了弦的初始位置和速度。也就是说，我们要求 $u$ 满足微分方程和两个条件

$$u(x,0) = f(x)\quad \mathrm{and}\quad \frac{\partial u}{\partial t} (x,0) = g(x),$$

⁴ 严格来说，傅里叶考虑的是余弦和正弦级数，而不是复指数形式。

⁴ Strictly speaking, Fourier considered cosine and sine series, not the complex form.

===== Page 34 =====

1. The vibrating string

where $f$ and $g$ are pre- assigned functions. Note that this is consistent with (4) in that this requires that $f$ and $g$ be expressible as

$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx\quad \mathrm{and}\quad g(x) = \sum_{m = 1}^{\infty}mB_{m}\sin mx.$$

1. 振动弦

其中 $f$ 和 $g$ 是预先指定的函数。注意这与(4)式一致，因为它要求 $f$ 和 $g$ 可以表示为

$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx\quad \mathrm{and}\quad g(x) = \sum_{m = 1}^{\infty}mB_{m}\sin mx.$$

### 1.3 Example: the plucked string

We now apply our reasoning to the particular problem of the plucked string. For simplicity we choose units so that the string is taken on the interval $[0,\pi ]$ , and it satisfies the wave equation with $c = 1$ . The string is assumed to be plucked to height $h$ at the point $p$ with $0< p< \pi$ ; this is the initial position. That is, we take as our initial position the triangular shape given by

$$f(x) = 
\begin{cases} 
\frac{h}{p} x & \text{for } 0 \le x \le p, \\
\frac{h}{\pi - p} (\pi - x) & \text{for } p \le x \le \pi,
\end{cases}
$$

which is depicted in Figure 8.

### 1.3 例子：拨弦

现在我们将推理应用于拨弦的具体问题。为简化起见，我们选择单位，使得弦位于区间 $[0,\pi ]$ 上，并且满足 $c = 1$ 的波动方程。假设弦在点 $p$ （ $0< p< \pi$ ）处被拨到高度 $h$ ；这就是初始位置。也就是说，我们将初始位置取为由下式给出的三角形形状

$$f(x) = 
\begin{cases} 
\frac{h}{p} x & \text{对于 } 0 \le x \le p, \\
\frac{h}{\pi - p} (\pi - x) & \text{对于 } p \le x \le \pi,
\end{cases}
$$

如图8所示。

<center>Figure 8. Initial position of a plucked string </center>

<center>图8. 拨弦的初始位置 </center>

We also choose an initial velocity $g(x)$ identically equal to 0. Then, we can compute the Fourier coefficients of $f$ (Exercise 9), and assuming that the answer to the question raised before (5) is positive, we obtain

$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx\quad \mathrm{with}\quad A_{m} = \frac{2h}{m^{2}}\frac{\sin mp}{p(\pi - p)}.$$

我们还选择初始速度 $g(x)$ 恒等于0。然后，我们可以计算 $f$ 的傅里叶系数（练习9），并假设前面(5)提出的问题的答案是肯定的，我们得到

$$f(x) = \sum_{m = 1}^{\infty}A_{m}\sin mx\quad \mathrm{with}\quad A_{m} = \frac{2h}{m^{2}}\frac{\sin mp}{p(\pi - p)}.$$

===== Page 35 =====

18 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

Thus

$$u(x,t) = \sum_{m = 1}^{\infty}A_{m}\cos mt\sin mx,$$

and note that this series converges absolutely. The solution can also be expressed in terms of traveling waves. In fact

$$u(x,t) = \frac{f(x + t) + f(x - t)}{2}.$$

18 第1章 傅里叶分析的起源

因此

$$u(x,t) = \sum_{m = 1}^{\infty}A_{m}\cos mt\sin mx,$$

并且注意这个级数是绝对收敛的。解也可以用行波表示。实际上

$$u(x,t) = \frac{f(x + t) + f(x - t)}{2}.$$

Here $f(x)$ is defined for all $x$ as follows: first, $f$ is extended to $[- \pi ,\pi ]$ by making it odd, and then $f$ is extended to the whole real line by making it periodic of period $2\pi$ , that is, $f(x + 2\pi k) = f(x)$ for all integers $k$ .

这里 $f(x)$ 对所有 $x$ 定义如下：首先，通过奇延拓将 $f$ 扩展到 $[- \pi ,\pi ]$ ，然后通过周期延拓（周期为 $2\pi$ ）将 $f$ 扩展到整个实直线，即对所有整数 $k$ 有 $f(x + 2\pi k) = f(x)$ 。

Observe that (8) implies (9) in view of the trigonometric identity

$$\cos v\sin u = \frac{1}{2} [\sin (u + v) + \sin (u - v)].$$

注意，根据三角恒等式

$$\cos v\sin u = \frac{1}{2} [\sin (u + v) + \sin (u - v)],$$

由(8)式可推出(9)式。

As a final remark, we should note an unsatisfactory aspect of the solution to this problem, which however is in the nature of things. Since the initial data $f(x)$ for the plucked string is not twice continuously differentiable, neither is the function $u$ (given by (9)). Hence $u$ is not truly a solution of the wave equation: while $u(x,t)$ does represent the position of the plucked string, it does not satisfy the partial differential equation we set out to solve! This state of affairs may be understood properly only if we realize that $u$ does solve the equation, but in an appropriate generalized sense. A better understanding of this phenomenon requires ideas relevant to the study of "weak solutions" and the theory of "distributions." These topics we consider only later, in Books III and IV.

最后要说的是，我们应该注意到这个问题的解存在一个不尽人意的方面，但这却是事物的本质。由于拨弦的初始数据 $f(x)$ 不是二次连续可微的，函数 $u$ （由(9)式给出）也不是。因此，$u$ 并不是波动方程的真正解：虽然 $u(x,t)$ 确实代表了拨弦的位置，但它并不满足我们最初要求解的偏微分方程！只有当我们意识到 $u$ 确实在某种适当的广义意义下满足该方程时，这种情况才能被正确理解。更好地理解这一现象需要研究"弱解"和"分布"理论相关的思想。我们只在后面的卷III和卷IV中讨论这些主题。

## 2 The heat equation

We now discuss the problem of heat diffusion by following the same framework as for the wave equation. First, we derive the time- dependent heat equation, and then study the steady- state heat equation in the disc, which leads us back to the basic question (7).

### 2.1 Derivation of the heat equation

Consider an infinite metal plate which we model as the plane $\mathbb{R}^2$ , and suppose we are given an initial heat distribution at time $t = 0$ . Let the temperature at the point $(x,y)$ at time $t$ be denoted by $u(x,y,t)$ .

## 2 热传导方程

现在我们按照与波动方程相同的框架来讨论热扩散问题。首先，我们推导出与时间相关的热传导方程，然后研究圆盘中的稳态热传导方程，这将我们带回基本问题(7)。

### 2.1 热传导方程的推导

考虑一个无限大的金属板，我们将其建模为平面 $\mathbb{R}^2$ ，并假设在时间 $t = 0$ 时给定了初始热分布。设点 $(x,y)$ 在时间 $t$ 的温度为 $u(x,y,t)$ 。

===== Page 36 =====

2. The heat equation

Consider a small square centered at $(x_0,y_0)$ with sides parallel to the axis and of side length $h$ , as shown in Figure 9. The amount of heat energy in $S$ at time $t$ is given by

$$H(t) = \sigma \int \int_{S}u(x,y,t)dxdy,$$

where $\sigma >0$ is a constant called the specific heat of the material. Therefore, the heat flow into $S$ is

$$\frac{\partial H}{\partial t} = \sigma \int_{S}\frac{\partial u}{\partial t} dxdy,$$

which is approximately equal to

$$\sigma h^2\frac{\partial u}{\partial t} (x_0,y_0,t),$$

since the area of $S$ is $h^2$ . Now we apply Newton's law of cooling, which states that heat flows from the higher to lower temperature at a rate proportional to the difference, that is, the gradient.

2. 热传导方程

考虑一个以 $(x_0,y_0)$ 为中心、边平行于坐标轴、边长为 $h$ 的小正方形，如图9所示。在时间 $t$ ，$S$ 中的热能总量为

$$H(t) = \sigma \int \int_{S}u(x,y,t)dxdy,$$

其中 $\sigma >0$ 是一个常数，称为材料的比热。因此，流入 $S$ 的热流量为

$$\frac{\partial H}{\partial t} = \sigma \int_{S}\frac{\partial u}{\partial t} dxdy,$$

由于 $S$ 的面积是 $h^2$ ，这近似等于

$$\sigma h^2\frac{\partial u}{\partial t} (x_0,y_0,t).$$

现在我们应用牛顿冷却定律，该定律指出热量以与温差（即梯度）成正比的速率从高温流向低温。

<center>Figure 9. Heat flow through a small square </center>

<center>图9. 通过一个小正方形的热流 </center>

The heat flow through the vertical side on the right is therefore

$$-\kappa h\frac{\partial u}{\partial x} (x_0 + h / 2,y_0,t),$$

where $\kappa >0$ is the conductivity of the material. A similar argument for the other sides shows that the total heat flow through the square $S$ is

因此，通过右侧垂直侧面的热流量为

$$-\kappa h\frac{\partial u}{\partial x} (x_0 + h / 2,y_0,t),$$

其中 $\kappa >0$ 是材料的导热系数。对其他边进行类似论证表明，通过正方形 $S$ 的总热流量为

===== Page 37 =====

20 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

given by

$$\kappa h\left[\frac{\partial u}{\partial x} (x_0 + h / 2,y_0,t) - \frac{\partial u}{\partial x} (x_0 - h / 2,y_0,t)\right.$$ $$\left. + \frac{\partial u}{\partial y} (x_0,y_0 + h / 2,t) - \frac{\partial u}{\partial y} (x_0,y_0 - h / 2,t)\right].$$

Applying the mean value theorem and letting $h$ tend to zero, we find that

$$\frac{\sigma}{\kappa}\frac{\partial u}{\partial t} = \frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2};$$

this is called the time- dependent heat equation, often abbreviated to the heat equation.

20 第1章 傅里叶分析的起源

由下式给出

$$\kappa h\left[\frac{\partial u}{\partial x} (x_0 + h / 2,y_0,t) - \frac{\partial u}{\partial x} (x_0 - h / 2,y_0,t)\right.$$ $$\left. + \frac{\partial u}{\partial y} (x_0,y_0 + h / 2,t) - \frac{\partial u}{\partial y} (x_0,y_0 - h / 2,t)\right].$$

应用中值定理并令 $h$ 趋于零，我们得到

$$\frac{\sigma}{\kappa}\frac{\partial u}{\partial t} = \frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2};$$

这被称为与时间相关的热传导方程，通常简称为热传导方程。

### 2.2 Steady-state heat equation in the disc

After a long period of time, there is no more heat exchange, so that the system reaches thermal equilibrium and $\partial u / \partial t = 0$ . In this case, the time- dependent heat equation reduces to the steady- state heat equation

$$\frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2} = 0. \quad (10)$$

### 2.2 圆盘中的稳态热传导方程

经过很长一段时间后，不再有热交换，因此系统达到热平衡，并且 $\partial u / \partial t = 0$ 。在这种情况下，与时间相关的热传导方程简化为稳态热传导方程

$$\frac{\partial^2u}{\partial x^2} +\frac{\partial^2u}{\partial y^2} = 0. \quad (10)$$

The operator $\partial^2 /\partial x^2 +\partial^2 /\partial y^2$ is of such importance in mathematics and physics that it is often abbreviated as $\Delta$ and given a name: the Laplace operator or Laplacian. So the steady- state heat equation is written as

$$\Delta u = 0,$$

and solutions to this equation are called harmonic functions.

算子 $\partial^2 /\partial x^2 +\partial^2 /\partial y^2$ 在数学和物理学中非常重要，以至于经常缩写为 $\Delta$ 并赋予一个名称：拉普拉斯算子。因此稳态热传导方程写为

$$\Delta u = 0,$$

并且该方程的解被称为调和函数。

Consider the unit disc in the plane

$$D = \{(x,y)\in \mathbb{R}^2:x^2 +y^2 < 1\} ,$$

whose boundary is the unit circle $C$ . In polar coordinates $(r,\theta)$ , with $0\leq r$ and $0\leq \theta < 2\pi$ , we have

$$D = \{(r,\theta):0\leq r< 1\} \quad \mathrm{and} \quad C = \{(r,\theta):r = 1\} .$$

The problem, often called the Dirichlet problem (for the Laplacian on the unit disc), is to solve the steady- state heat equation in the unit

考虑平面上的单位圆盘

$$D = \{(x,y)\in \mathbb{R}^2:x^2 +y^2 < 1\} ,$$

其边界是单位圆 $C$ 。在极坐标 $(r,\theta)$ 下，其中 $0\leq r$ 且 $0\leq \theta < 2\pi$ ，我们有

$$D = \{(r,\theta):0\leq r< 1\} \quad \mathrm{and} \quad C = \{(r,\theta):r = 1\} .$$

该问题通常称为（单位圆盘上拉普拉斯算子的）狄利克雷问题，即求解单位圆盘中的稳态热传导方程

===== Page 38 =====

2. The heat equation

disc subject to the boundary condition $u = f$ on $C$ . This corresponds to fixing a predetermined temperature distribution on the circle, waiting a long time, and then looking at the temperature distribution inside the disc.

2. 热传导方程

，满足边界条件 $u = f$ 在 $C$ 上。这对应于在圆上固定一个预先确定的温度分布，等待很长时间，然后观察圆盘内部的温度分布。

<center>Figure 10. The Dirichlet problem for the disc </center>

<center>图10. 圆盘的狄利克雷问题 </center>

While the method of separation of variables will turn out to be useful for equation (10), a difficulty comes from the fact that the boundary condition is not easily expressed in terms of rectangular coordinates. Since this boundary condition is best described by the coordinates $(r, \theta)$ , namely $u(1, \theta) = f(\theta)$ , we rewrite the Laplacian in polar coordinates. An application of the chain rule gives (Exercise 10):

$$\triangle u = \frac{\partial^2u}{\partial r^2} +\frac{1}{r}\frac{\partial u}{\partial r} +\frac{1}{r^2}\frac{\partial^2u}{\partial\theta^2}.$$

虽然分离变量法对于方程(10)将是有效的，但一个困难来自于边界条件不易用直角坐标表示。由于这个边界条件最好用坐标 $(r, \theta)$ 描述，即 $u(1, \theta) = f(\theta)$ ，我们将拉普拉斯算子改写成极坐标形式。应用链式法则得到（练习10）：

$$\triangle u = \frac{\partial^2u}{\partial r^2} +\frac{1}{r}\frac{\partial u}{\partial r} +\frac{1}{r^2}\frac{\partial^2u}{\partial\theta^2}.$$

We now multiply both sides by $r^2$ , and since $\triangle u = 0$ , we get

$$r^2\frac{\partial^2u}{\partial r^2} +r\frac{\partial u}{\partial r} = -\frac{\partial^2u}{\partial\theta^2}.$$

Separating these variables, and looking for a solution of the form $u(r, \theta) = F(r)G(\theta)$ , we find

$$\frac{r^2F''(r) + rF'(r)}{F(r)} = -\frac{G''(\theta)}{G(\theta)}.$$

现在我们将两边乘以 $r^2$ ，由于 $\triangle u = 0$ ，我们得到

$$r^2\frac{\partial^2u}{\partial r^2} +r\frac{\partial u}{\partial r} = -\frac{\partial^2u}{\partial\theta^2}.$$

分离这些变量，并寻找形式为 $u(r, \theta) = F(r)G(\theta)$ 的解，我们得到

$$\frac{r^2F''(r) + rF'(r)}{F(r)} = -\frac{G''(\theta)}{G(\theta)}.$$

===== Page 39 =====

22 Chapter 1. THE GENESIS OF FOURIER ANALYSIS

Since the two sides depend on different variables, they must both be constant, say equal to $\lambda$ . We therefore get the following equations:

$$
\begin{cases}
G''(\theta) + \lambda G(\theta) = 0, \\
r^2 F''(r) + r F'(r) - \lambda F(r) = 0.
\end{cases}
$$

22 第1章 傅里叶分析的起源

由于两边依赖于不同的变量，它们必须都等于一个常数，比如 $\lambda$ 。因此我们得到以下方程：

$$
\begin{cases}
G''(\theta) + \lambda G(\theta) = 0, \\
r^2 F''(r) + r F'(r) - \lambda F(r) = 0.
\end{cases}
$$

Since $G$ must be periodic of period $2\pi$ , this implies that $\lambda \geq 0$ and (as we have seen before) that $\lambda = m^2$ where $m$ is an integer; hence

$$G(\theta) = \tilde{A}\cos m\theta +\tilde{B}\sin m\theta .$$

由于 $G$ 必须是周期为 $2\pi$ 的周期函数，这意味着 $\lambda \geq 0$ 并且（正如我们之前所见） $\lambda = m^2$ ，其中 $m$ 是整数；因此

$$G(\theta) = \tilde{A}\cos m\theta +\tilde{B}\sin m\theta .$$

An application of Euler's identity, $e^{ix} = \cos x + i\sin x$ , allows one to rewrite $G$ in terms of complex exponentials,

$$G(\theta) = Ae^{im\theta} + Be^{-im\theta}.$$

应用欧拉恒等式 $e^{ix} = \cos x + i\sin x$ ，我们可以用复指数形式重写 $G$ ，

$$G(\theta) = Ae^{im\theta} + Be^{-im\theta}.$$

With $\lambda = m^2$ and $m\neq 0$ , two simple solutions of the equation in $F$ are $F(r) = r^m$ and $F(r) = r^{- m}$ (Exercise 11 gives further information about these solutions). If $m = 0$ , then $F(r) = 1$ and $F(r) = \log r$ are two solutions. If $m > 0$ , we note that $r^{- m}$ grows unboundedly large as $r$ tends to zero, so $F(r)G(\theta)$ is unbounded at the origin; the same occurs when $m = 0$ and $F(r) = \log r$ . We reject these solutions as contrary to our intuition. Therefore, we are left with the following special functions:

$$u_{m}(r,\theta) = r^{|m|}e^{im\theta},\quad m\in \mathbb{Z}.$$

对于 $\lambda = m^2$ 且 $m\neq 0$ ，关于 $F$ 的方程的两个简单解是 $F(r) = r^m$ 和 $F(r) = r^{- m}$ （练习11给出了这些解的更多信息）。如果 $m = 0$ ，那么 $F(r) = 1$ 和 $F(r) = \log r$ 是两个解。如果 $m > 0$ ，我们注意到当 $r$ 趋于零时，$r^{- m}$ 无限增长，因此 $F(r)G(\theta)$ 在原点无界；当 $m = 0$ 且 $F(r) = \log r$ 时也是如此。这些解与我们的直觉相悖，故舍弃。因此，我们剩下以下特殊函数：

$$u_{m}(r,\theta) = r^{|m|}e^{im\theta},\quad m\in \mathbb{Z}.$$

We now make the important observation that (10) is linear, and so as in the case of the vibrating string, we may superpose the above special solutions to obtain the presumed general solution:

$$u(r,\theta) = \sum_{m = -\infty}^{\infty}a_{m}r^{|m|}e^{im\theta}.$$

If this expression gave all the solutions to the steady- state heat equation, then for a reasonable $f$ we should have

$$u(1,\theta) = \sum_{m = -\infty}^{\infty}a_{m}e^{im\theta} = f(\theta).$$

We therefore ask again in this context: given any reasonable function $f$ on $[0,2\pi ]$ with $f(0) = f(2\pi)$ , can we find coefficients $a_{m}$ so that

$$f(\theta) = \sum_{m = -\infty}^{\infty}a_{m}e^{im\theta}?$$

现在我们做一个重要的观察：(10)是线性的，因此与振动弦的情况一样，我们可以叠加上述特解，得到假定的通解：

$$u(r,\theta) = \sum_{m = -\infty}^{\infty}a_{m}r^{|m|}e^{im\theta}.$$

如果这个表达式给出了稳态热传导方程的所有解，那么对于一个合理的 $f$ ，我们应该有

$$u(1,\theta) = \sum_{m = -\infty}^{\infty}a_{m}e^{im\theta} = f(\theta).$$

因此，我们再次在这个背景下提问：给定 $[0,2\pi ]$ 上任何合理的函数 $f$ （满足 $f(0) = f(2\pi)$ ），我们能否找到系数 $a_{m}$ 使得

$$f(\theta) = \sum_{m = -\infty}^{\infty}a_{m}e^{im\theta}?$$

===== Page 40 =====

3. Exercises

Historical Note: D'Alembert (in 1747) first solved the equation of the vibrating string using the method of traveling waves. This solution was elaborated by Euler a year later. In 1753, D. Bernoulli proposed the solution which for all intents and purposes is the Fourier series given by (4), but Euler was not entirely convinced of its full generality, since this could hold only if an "arbitrary" function could be expanded in Fourier series. D'Alembert and other mathematicians also had doubts. This viewpoint was changed by Fourier (in 1807) in his study of the heat equation, where his conviction and work eventually led others to a complete proof that a general function could be represented as a Fourier series.

3. 练习

历史注记：达朗贝尔（1747年）首先使用行波法求解了振动弦的方程。这个解法在一年后由欧拉进行了详细阐述。1753年，D. 伯努利提出了一个解，实际上就是(4)式给出的傅里叶级数，但欧拉并不完全相信它的普遍性，因为这只有在"任意"函数可以展开为傅里叶级数时才成立。达朗贝尔和其他数学家也有疑虑。这种观点被傅里叶（1807年）在他对热传导方程的研究中改变了，他的信念和工作最终引导其他人完整证明了一般函数可以表示为傅里叶级数。