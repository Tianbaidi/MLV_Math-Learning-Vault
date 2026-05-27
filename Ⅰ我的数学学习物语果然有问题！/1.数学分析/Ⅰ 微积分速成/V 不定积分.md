---
tags:
  - 微积分
  - Mathematical_Analysis
---

> 作为速成，我们就放过对函数性质的一些分析，直接进入积分的内容。从小学开始，我们就已经在接触名为逆运算的概念，所谓的 "加" 与 "减"、"除" 与 "乘" 。微分的逆运算就是积分：我们在最早的那一节举了一个朴素的例子，就是对圆面积的计算。我们要研究的就是积分为何可以做到这一点，以及在这一章，我们要掌握一些不定积分的基本运算。

# 圆为何如此？（这是一个朴素的思维）
我们此时已经知道了微分的概念，我们也知道了圆面积推导的基本方法。与我们第一次直观的由外 向内 "剥胶带" 不同，我们采用从内向外的方式来优化我们构造函数： $C=2\pi r$  . 我们让 $r$ 为未知量  $x$ ，便得到函数 
 $$f(x)=2\pi x$$
 他自身就是我们 "微分" 得到的产物。我们讲该函数乘以 "厚度" $dx$ 
 $$f(x)dx=2\pi xdx$$
 上述式子只要求和就能得到我们想要的结果，直接根据几何来做就是求三角形的面积 
 $$\frac{x}{2dx}f(x)dx=\pi x^2$$ 我们此时已经运用朴素的理解对微积分进行应用了，并且可以直接做下假设，微积分也不过如此（doge）

# 原函数与不定积分

Def.1  设 $f$ 是区间 $I$ 上有定义的函数，若 $F$ 也在 $I$ 上有定义，且满足 
$$F'(x)=f(x), \quad x\in I$$
则称 $F$ 为 $f$ 在区间 $I$ 上的一个 $\textbf{原函数}$ 

我们学过导数都知道，常数的导数计算是等于 $0$ 的，这也是初学者常常会犯的毛病 :  天哪，原函数竟然是不唯一的！后知后觉地因为积分没有加常数项而丢了分。

Def.2  $f$ 的原函数全体称为这个函数的不定积分, 记为 
$$\int f(x)dx$$这里 $\int$ 就是大名鼎鼎的 "积分号" ，$f(x)$ 为被积函数 ，$x$ 为积分变量，$f(x)dx$ 为被积表达式（原函数的微分）
其计算结果为 
$$\int f(x)dx=F(x)+C$$
其中的 $C$ 就是积分常数，这个数字是任意的

我们这个时候只能应付一些简单的方程，一些通过线性运算组合出来的方程要怎么办呢？这里，我们来论证

Thm.1 （$\textbf{积分的线性性}$） 若 $f$ 和 $g$ 都是在区间 $I$ 上有定义的函数且都存在原函数 , 其中 $k_{1}$ 与 $k_{2}$ 为两个任意常数 , 则 $k_{1}f+k_{2}g$ 在 $I$ 上也有原函数，当 $k_{1}$ 和 $k_{2}$ 不为 $0$ 时，有 
$$\int[k_{1}f(x)+k_{2}g(x)]dx=k_{1}\int f(x)dx+k_{2}\int g(x)dx$$
proof. 我们对后面得到的式子求导就能得到
$$[k_{1}\int f(x)dx+k_{2}\int g(x)dx]'=k_{1}(\int f(x)dx)'+k_{2}(\int g(x)dx)'=k_{1}f(x)+k_{2}g(x)$$
一般情况便是这样
$$\int\left( \sum_{i=1}^n k_{i}f_{i}(x) \right)dx=\sum_{i=1}^n k_{i}\int f_{i}(x)dx$$

这个定理能帮助我们进行一些相对复杂的运算了，但是这类情况的计算还是很简单。在高中我们就常常使用换元法来简化一些求导的计算，我们在进行逆运算的时候有没有类似的方法呢？

## 换元积分法与分部积分法

Thm. 2 （$\textbf{第一换元积分法-凑积分法}$）  $f$ 在区间 $I$ 上有定义 , $\varphi(t)$ 在区间 $J$ 上可导，且 $\varphi (J)\subseteq I$ . 如果不定积分 $\int f(x)dx=F(x)+C$ 在 $I$ 上存在，则不定积分 $\int f(\varphi(t))\varphi(t)dt$ 在 $J$ 上也存在，且有 
$$\int f(\varphi(t))\varphi(t)dt=F(\varphi(t))+C$$
proof. 用复合函数求导法进行验证 , $\forall t \in J$ 有
$$\frac{d}{dt}(F(\varphi(t)))=F'(\varphi(t))\varphi'(t)=f(\varphi(t))\varphi'(t)$$
在使用该公式时，就可以用如下形式：
$$\int f(\varphi(t))\varphi'(t)dt=\int f(\varphi(t))d\varphi(t)$$
我们令 $\varphi(t)=x$ 就有
$$\int f(x)dx=F(x)+C=F(\varphi(t))+C$$
凑微分法便如此得名

Thm.3 $(\textbf{第二积分换元法-代入换元})$   $f$ 在区间 $I$ 上有定义 , $\varphi(t)$ 在区间 $J$ 上可导 , $\varphi(J)=I$ , 且 $x=\varphi(t)$ 在区间 $J$ 上存在反函数 $t=\varphi^{-1}(x)$ , $x\in I$ . 如果不定积分 $\int f(x)dx$ 在 $I$ 上存在 , 则当不定积分 $\int f(\varphi(t))\varphi'(t)dt=G(t)+C$ 在 $J$ 上存在时 , 在 $I$ 上有 
$$\int f(x)dx=G(\varphi^{-1}(x))+C$$
proof. 设 $\int f(x)dx=F(x)+C.$ 对于任何 $t\in J$ ，有
$$\frac{d}{dt}(F(\varphi(t))-G(t))=F'(\varphi(t)\varphi'(t))-G(t)=f(\varphi(t))\varphi'(t)-f(\varphi(t))\varphi'(t)=0$$
因此存在常数 $C_{1}$ , 使得 $F(\varphi(t))-G(t)=C_{1}$ 对于任意 $t\in J$ 成立 ，从而 $G(\varphi^{-1}(x))=F(x)-C_{1}$ 对于任何 $x\in I$ 成立. 因此，对于任何 $x\in I$ 有
$$\frac{d}{dx}(G(\varphi^{-1}(x)))=F'(x)=f(x)$$
即 $G(\varphi^{-1}(x))$ 为 $f(x)$ 的原函数. 


> [!NOTE] 注意
> 1. 定理中不定积分存在是一个必须条件，否则结论不成立
> 2. 若条件加强 $\varphi'(t)\neq_{0} ，x\in J$ ，则当不定积分 $\int f(\varphi(t))\varphi'(t)dt=G(t)+C$ 在 $J$ 上存在时，不定积分 $\int f(x)dx$ 在 $I$ 上也存在，且有 (使用复合函数和反函数求导法则)
> $$\int f(x)dx=G(\varphi^{-1}(x))+C$$

同样有简化方法
$$\int d(x)dx=\int f(\varphi(t))\varphi'(t)dt$$
令 $x=\varphi(t)$ 
$$=G(t)+C=G(\varphi^{-1}(x))+C.\ (t=\varphi^{-1}(x))$$
因此第二换元法又称 $\textbf{代入换元法}$


> 以上，我们掌握了一些基本的求不定积分的方法，现在我们将要学习一些特殊类型的不定积分。

## 有理函数的不定积分

有理函数是由两个多项式函数的商所表示的函数，其一般形式为
$$R(x)=\frac{P(x)}{Q(x)}=\frac{\alpha_{0}x^n+\alpha_{1}x^{n-1}+\cdots+\alpha_{n}}{\beta_{0}x^m+\beta_{1}x^{m-1}+\cdots+\beta_{m}}$$
其中 $n,m$ 是非负整数 , $\alpha_{0},\alpha_{1}…,\alpha_{n}$ 和 $\beta_{0}, \beta_{1},…,\beta m$ 都是常数 , 且 $\alpha_{0}\neq 0$ , $\beta_{0}\neq_{0}$ . 若 $m>n$ , 则称它为**真分式** ; 若 $m\leq n$ , 则称它为**假分式** . 由多项式的除法可知 , 假分式总能化成一个多项式与一个真分式之和 .  我们只需要研究真分式之和即可。

在后续可能更新的基础数论模块，我们会知道一个知识叫做 "互素" . 如果 $Q_{1}(x),Q_{2}(x)$ 是互素的，那么就有多项式 $P_{1}(x),P_{2}(x)$ 使得 ${P_{1}(x)Q_{1}(x)+P_{2}(x)Q_{2}(x)}=1$ 就有 
$$\frac{1}{Q_{1}(x)Q_{2}(x)}=\frac{{P_{1}(x)Q_{1}(x)+P_{2}(x)Q_{2}(x)}}{Q_{1}(x)Q_{2}(x)}=\frac{P_{1}(x)}{Q_{2}(x)}+\frac{P_{2}(x)}{Q_{1}(x)}$$
这个步骤称之为**部分分式分解** . 我们求本部分式的不定积分即可，我们如下分步：
1. 对分母 $Q(x)$ 在实数系内做标准分解 
   $$Q(x)=(x-a_{1})^{\lambda_{1}}\cdots (x-a_{x})^{\lambda s}(x^2+p_{1}x+q_{1})^{\mu_{1}}\cdots(x^2+p_{t}x+q_{t})^{\mu_{t}}$$
   其中 $\beta_{0}=1$ , $\lambda_{i}, \mu _j$ 都是自然数，且有 
   $$\sum_{i=1}^s \lambda_{i}+2 \sum_{j=1}^t\mu_{j}=m \ ; \quad p_{j}^2-4q_{j}<0 ,\quad j=1,2,\cdots t$$
2. 根据分母的各个因式分别写出之前相应的分式 : 对于每一个形如 $(x-a)^k$ 的因式，他们对应的分式是 
   $$\frac{A_{1}}{x-a}+\frac{A_{2}}{(x-a)^2}+\cdots+{A_{k}}{(x-a)^k}$$
   对于形如 $(x^2+px+q)^k$ 的因式 , 它所对应的部分分式是 
   $$\frac{{B_{1}x+C_{1}}}{x^2+p+q}+\frac{{B_{2}x+C_{2}}}{(x^2+p+q)^2}+\cdots+\frac{{B_{k}x+C_{k}}}{(x^2+p+q)^k}$$
   我们把所有部分加起来，使之等于 $R(x)$ 
3. 确定待定系数 : 将所有部分的分式通分相加，所得分母即为原分母 $Q(x)$ , 分子对应 $P(x)$ ,于是我们得到一组关于待定系数的线性方程，此解即为要确定的系数。
4. 我们来求不定积分 
   $$\int \frac{dx}{(x-a)^k}\ ,\quad \int \frac{{Lx+M}}{(x^2+px+q)^k}dx $$
   $$\int \frac{dx}{(x-a)^k}=\begin{cases}
\ln |x-a|+C \ ,\quad k=1 \\
\frac{1}{(1-k)(x-a)^{k-1}}+C\ , \quad k>1
\end{cases}$$
   我们令 $t=x+ \frac{p}{2}$ , 可化为  
   $$\int\frac{{Lx+M}}{(x^2+px+q)^k}dx=\int \frac{{Lt+N}}{(t^2+r^2)^k}dt=L\int \frac{t}{(t^2+r^2)^k}dt+N\int \frac{dt}{(t^2+r^2)^k}$$
   当 $k=1$ 时 , 就有 
   $$\begin{matrix}
   \int \frac{t}{t^2+r^2}dt=\frac{1}{2}\ln(t^2+r^2)+C,\\
   \int \frac{dt}{t^2+r^2}=\frac{1}{r}\arctan \frac{t}{r}+C .
   \end{matrix}$$
   当 $k>1$ 时， 
   $$\begin{matrix}
   \frac{1}{2(k-1)(t^2+r^2)^{k-1}}+C\\
   记\quad I_{k}=\int \frac{dt}{(t^2+r^2)^k} \\
递推可以得到 \\
I_{k}=\frac{t}{2r^2(k-1)(t^2+r^2)^{k-1}}+\frac{{2k-3}}{2r^2(k-1)}I_{k-1}
   \end{matrix}$$
   反复使用最终可以使用 $I_{1}$ ,带回即可求解。

## 三角函数有理式的不定积分

我们可以采用换元的方法将其化为有理函数的不定积分，对于三角函数，我们有 
$$\sin x=\frac{{2\sin{\frac{x}{2}}\cos{\frac{x}{2}}}}{\sin^2{\frac{x}{2}}+\cos^2{\frac{x}{2}}}=\frac{{2\tan {\frac{x}{2}}}}{1+\tan ^2{\frac{x}{2}}}$$ 
$$\cos x=\frac{{1-\tan^2{\frac{x}{2}}}}{1+\tan^2{\frac{x}{2}}}$$
我们让 $t=\tan \frac{x}{2}$ 换元即可 。对于具体解题情况需要特殊换元自行斟酌。

## 某些无理根式的不定积分

1. 对于 $\int R\left( x, ^n\sqrt{\frac{{ax+b}}{cx+d}} \right)dx$ 型的不定积分 , 令 $t=^n\sqrt{\frac{{ax+b}}{cx+d}}$ 
2. 对于 $\int(x, \sqrt{ ax^2+bx+c })dx$ 型的不定积分 , 由于 
$$ax^2+bx+c=a\left[ \left( x+\frac{b}{2a} \right)+\frac{{4ac-b^2}}{4a^2} \right]$$
若记 $u=x+\frac{b}{2a} , k^2=|\frac{{4ac-b^2}}{4a^2}|$ , 则此时二次三项式必为以下情况之一 
$$|a|(u^2+k^2)\ ,\ |a|(u^2-k^2)\ ,\ |a|(k^2-u^2)$$ 我们令 $u=k\tan t$ , $u=k\sec t$ ,  $u=k\sin t$  后，都可化为三角有理式的不定积分

   2.1. 令 $\sqrt{ ax^2+bx+c }=\sqrt{ a }x\pm t$  或  $\sqrt{ ax^2+bx+c }=xt\pm \sqrt{ c }$ .这类变化我们称之为 $欧拉变化(Euler\ transformation)$  

至此，不定积分已通关，我们即将开启定积分的章节，感谢大家一路陪伴。