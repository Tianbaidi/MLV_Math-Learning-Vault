---
tags:
  - Mathematical_Analysis
  - Exercises
---
> 我不要读数分，我不要读数分，我不要读数分… 但是既然要考，那就要好好复习

考纲概览：

| 专题  | 小专题   | 考点  | 一筛  |
| --- | ----- | --- | --- |
|     | 不定积分  |     | √   |
|     | 定积分   |     |     |
| 微积分 | 变上限积分 |     |     |
|     | 微积分应用 |     |     |
|     | 反常积分  |     |     |
|     | 数项级数  |     |     |
| 级数  | 函数项级数 |     |     |
|     | 幂级数   |     |     |
|     | 傅里叶级数 |     |     |
这个笔记的结构为：定理定义例题，注意点
> [!NOTE] Theorem
> Contents
> 

> [!Danger] Corollary
> Contents

> [!Warning] Remark
> Contents

例题为考纲（期末复习）给的题目，补充为此前考试的原题。

---

# 不定积分

1. 不定积分不妨直接理解为求反导数，有几个公式需要注意一下 
$$\begin{align*}
\int a^x dx=&\frac{a^x}{\ln a}+C \\
\int \sec ^{2} ax dx=&\frac{1}{a}\tan ax+C \\
\int \csc ^{2} ax dx=&-\frac{1}{a}\cot ax+C \\
\int \sec ax\tan axdx=&\frac{1}{a}\sec ax+C \\
\int \csc ax \cot ax dx=&-\frac{1}{a} \csc ax +C \\
\int \frac{1}{\sqrt{ 1-x^{2} }} dx=&\arcsin x+C=-\arccos x+C \\
\int \frac{1}{1+x^{2}}=&-\arctan x+C
\end{align*}$$
> [!Example] EXAMPLE
> 1. 求 
> $$\int \tan xdx$$
> 2. 求
> $$\int \frac{dx}{\sqrt{ a^{2}-x^{2} }} (a>0)$$
> 3. 求 
> $$\int \sec x dx$$
> 4. 求 
> $$\int \sqrt{ a^{2}-x^{2} }dx$$
> 5. 求
> $$\int x\cos xdx$$
> 6. 求 
> $$\int x^3 \ln x dx$$
> 7. 求
> $$\int \frac{x^{2}+1}{(x^2-2x +2)^2}dx$$

Answer：
1. 首先将其展开 $\tan=\frac{\sin x}{\cos x}$ ，随后，注意到 $(\cos x)'=-\sin x$ 于是我们采用 **凑微分法** ，有 
$$\int \tan xdx=-\int \frac{(\cos x)'dx}{\cos x}=-\ln |\cos x|+C$$
2. 不妨提取 $\frac{1}{a}$ 我们得到 , 凑微分 $u=\frac{x}{a}$ 有
$$\frac{1}{a} \int \frac{dx}{\sqrt{ 1-\left( \frac{x}{a} \right)^{2} }} =\arcsin \frac{x}{a}+C$$
3. 这是我们期中考试题 
$$\int \frac{1}{\cos x}dx=\int \frac{\cos x}{1-\sin ^{2}x}dx=\int \frac{1}{1-u^{2}}du=\frac{1}{2}\ln \left|\frac{{1+\sin x}}{1-\sin x}\right|+C$$
4. 这题我们的算法是 **带入换元法** ，我们可以去掉其根号 
$$\int \sqrt{ a^{2}-x^{2} }=\int a\cos t d(a\sin t)=a^{2}\int \cos ^{2}tdt=\frac{a^{2}}{2} \left( t+\frac{1}{2}\sin 2t \right)+C$$
5. 这题我们的做法就是 **分部积分法** ,其推导为复合函数的逆过程，我们令 $u=x$ , $v'=\cos x$ 则 $u'=1$ $v=\sin x$ . 我们有 
$$\int x\cos xdx=x\sin x-\int \sin xdx=x\sin x+\cos x+C$$
6. 我们令 $u=\ln x$ , $v'=x^3$ 于是我们有 
$$\int x^3\ln xdx=\int \ln xd\left( \frac{x^4}{4} \right)=\frac{1}{4}\left( x^4 \ln x-\int x^3 dx \right)=\frac{x^4}{16} (4\ln x-1)+C$$
7. 这是有理函数的不定积分，首先我们要想办法将其化为我们想要的形式，这题我们这样处理 
$$\begin{align}
&\frac{x^2+1}{(x^{2}-2x+2)^{2} }=\frac{x^2-2x+2+2x-1}{(x^{2}-2x+2)^{2} }= \frac{1}{(x^{2}-2x+2) }+\frac{2x-1}{(x^{2}-2x+2)^{2} } \\
&\int \frac{dx}{x^2-2x+2}=\int \frac{d(x-1)}{(x-1)^{2}+1}=\arctan(x-1)+C \\
&\int \frac{2x-2+1}{(x^2-2x+2)^{2}}=\int \frac{d(x^{2}-2x+2)}{(x^{2}-2x+2)^{2}}+\int \frac{dx}{[(x-1)^{2}+1]^{2}}= \frac{-1}{x^{2}-2x+2}+\int \frac{dt}{(t^{2}+1)^{2}}
\end{align}$$
对于最后一个积分，我们需要利用递推公式 
$$\int \frac{dt}{(t^{2}+1)^{2}}= \frac{x-1}{2(x^{2}-2x+2)}+\frac{1}{2}\arctan(x-1)+C$$
于是得到 
$$I=\frac{x-3}{2(x^{2}-2x+2)}+\frac{3}{2}\arctan(x-1)+C$$

> [!Warning] Remark 1
> **关于分部积分** ：
> 我们的分部积分选取 u 的参考标准为 LIATE 原则，即 Logarithmic （对数函数）, Inverse trigonometric （反三角函数）, Algebraic （代数函数）,Trigonometric （三角函数）, Exponential （指数函数）的优先级依次递减

> [!Warning] Remark 2
> **关于递推式** ：
> 针对多项式积分 
> $$I_{k}=\int \frac{dt}{(t^{2}+r^{2})^{k}}$$
> 我们通过分部积分的方法 $u= \frac{1}{(t^{2}+r^{2})^k}$ , $dv=dt$ .
> $du=-\frac{2kt}{(t^{2}+r^{2})^{k+1}}dt$ ,  $v=t$
> 于是我们有 
> $$I_{k}= \frac{t}{(t^{2}+r^{2})^k}+\int \frac{2kt^{2}}{(t^{2}+r^{2})^{k+1}}dt$$
> 我们可以继续分解第二项得到 
> $$\int \frac{2kt^{2}}{(t^{2}+r^{2})^{k+1}}dt=2kI_{k}-2kr^{2}I_{k+1}$$
> 统筹以上结果，我们得到降阶公式 
> $$I_{k}= \frac{t}{2r^{2}(k-1)(t^{2}+r^{2})^{k-1}}+\frac{{2k-3}}{2(k-1)r^{2}}I_{k-1}$$
> 当 $r=1$ 的时候，我们可以很好得做好降阶工作

> [!Warning] Remark 3
> 当我们遇到一些三角函数的等式的时候，我们可以考虑三角换元

# 定积分
> [!Warning] Remark 1
> 1. 可积一定能推出其有界
> 2. 原函数存在与可积之间不存在互推关系

> [!Danger] Corollary ：可积函数类
> - 连续函数可积
> - 函数有有限间断点可积
> - 单调函数可积
> - 特殊的，Riemann 函数可积（积分结果为）、Dirichlet 函数不可积

> [!NOTE] Theorem ：可积的充要条件
> 对于任意的 $\varepsilon>0$ , 总存在某个分割 P 使得其上和与下和之差小于 $\varepsilon$ 
> $$f\in R[a,b]\quad \Longleftrightarrow \quad \lim_{ ||P|| \to 0 }\sum^n \omega_{i}\Delta x_{i}=0$$

> [!TIP] Proposition
> 1. 中值定理： ($f$ 连续，$g$ 可积且在 $[a,b]$ 上不变号)
> $$\int_{a}^b f(x)\cdot g(x) dx=f(\xi)\int_{a}^b g(x)dx$$
> 如果我们要证明后续的迪利克雷判别法和阿贝尔判别法，我们会用到第二中值定理 
> $$ \int_{a}^{b} f(x)g(x)dx = g(a) \int_{a}^{\xi} f(x)dx + g(b) \int_{\xi}^{b} f(x)dx $$ 
> 2. 对奇函数和偶函数的积分可以进行化简——基函数 $\to {0}$ 偶函数 $\to 2\int f (x>0 )$ 
> 3. 周期函数的性质

> [!ABSTRACT] Definition ：变限积分
> $F(x)=\int_{a}^x f(t)dt$ 
> - $f$ 可积 $\Rightarrow$ $F$ 连续 
> - $f$ 连续 $\Rightarrow$ $F$ 可导
> - 求 $F(a)=0$ 或者对其求导

> [!Example] EXAMPLE 1
> 1. 求下列极限 
> $$(i)\lim_{ x \to 0 } \frac{1}{x}\int_{0}^x \cos t^{2}dt \qquad \qquad (ii)\lim_{ x \to \infty } \frac{\left( \int_{0}^x e^{t^2}dt\right)^{2}}{\int_{0}^xe^{2t^2}dt}$$


> [!Example] EXAMPLE 2
> 计算：
> 1. $*$
> $$\int_{0}^1 \sqrt{ 1-x^{2} }dx$$
> 2. $*$
>$$\int_{0}^{\pi/2}\sin t\cos ^{2}t dt$$
>3. 
> $$J=\int_{0}^1 \frac{\ln(1+x)}{1+x^{2}}dx$$
> 4. $*$
> $$\int_{1}^e x^{2}\ln x dx$$
> 5.  
> $$\int_{0}^{\pi/2} \sin^{n}xdx \quad\text{and}\quad \int_{0}^{\pi/2}\cos^{n}x dx $$ 


> [!Example] EXAMPLE 3
> 1. 利用定积分求极限 
> $$\lim_{ n \to \infty } \left( \frac{1}{n+1}+\frac{1}{n+2}+\cdots+\frac{1}{2n} \right)$$
> 2. 利用定积分求极限 
> $$\lim_{ n \to \infty } \frac{1}{n^4}(1+2^3+3^3+\cdots+n^3)$$

Answer：
1.1 令 $F(x)=\int_{0}^x \cos t^2dt$ ，$F(0)=0$  ，有 
$$\lim_{ x \to 0 } \frac{F(x)-F(0)}{x}=F'(0) $$
而 $F'(x)=\cos x^{2}$ 所以原极限为 
$$1$$
1.2 设 $A(x)=\int_{0}^x e^{t^2}dt$ , $B(x)=\int_{0}^xe^{2t^{2}}dt.$ 分子分母都趋近无穷大，则原式为 
$$\lim_{ x \to \infty }  \frac{A^{2}}{B}=\lim_{ x \to \infty } \frac{2A(x)e^{x^{2}}}{e^{2x^{2}}}=\lim_{ x \to \infty }  \frac{2A(x)}{e^{x^{2}}}$$
再次利用洛必达法则 
$$\lim_{ x \to \infty } \frac{1}{x}=0 $$

2.1 我们这里采用换元法，将令 $x=\sin t$ 我们有 
$$\int_{0}^{\pi/2} \cos ^{2} tdt=\frac{\pi}{4} $$
另有看法，其实这个积分就表示单位圆在第一象限的面积，于是 
$$\frac{\pi}{4}$$
2.2 令 $u=\cos t$ 有 $du=-\sin t dt$ , 积分变限 
$$\int_{0}^1 u^{2}du=\frac{1}{3}$$
2.3 令 $x=\tan t$ 于是 $dx=\sec ^{2}tdt$ ， $1+x^{2}=\sec ^{2}t$ 对原积分进行换元 
$$J=\int_{0}^{\pi/4} \ln(1+\tan t)dt$$
令  $u=\frac{\pi}{4}-t$ 我们有 
$$J=\int_{0}^{\pi/4}\ln\left( 1+\tan\left( \frac{\pi}{4}-u \right) \right)du=\int_{0}^{\pi/4}\ln\left( 1+ \frac{1-\tan u}{1+\tan u} \right)du=\int_{0}^{\pi/4}\ln\left( \frac{2}{1+\tan u} \right)du$$
我们发现 
$$J=\frac{\pi}{4}\ln 2-J$$
于是 $J=\frac{\pi}{8} \ln 2$

2.4 由 LIATE 法则 我们选取 $u=\ln x$ 于是 $dv=x^{2}dx$ $v=\frac{1}{3}x^{4}$ 根据公式，我们有 
$$\int_{1}^e x^{2}\ln xdx=\left[ \frac{x^{3}}{3}\ln x \right]_{1}^e -\int_{1}^e \frac{x^{2}}{3}dx$$
于是得到答案 $\int_{1}^e x^{2}\ln xdx= \frac{{2e^3+1}}{9}$

2.5 说白了这里就是 Wallis 公式，我们利用分部积分可以得到递推式 
$$I_{n}=\frac{{n-1}}{n}I_{n-2},\quad n>2$$
$$\begin{cases}
\frac{(n-1)!!}{n!!}\cdot \frac{\pi}{2} , \quad n \text{为偶数} \\
\frac{(n-1)!!}{n!!} ， \quad n\text{为奇数}
\end{cases}$$
3.1 我们将原式写成 
$$S_{n}=\sum_{k=1}^n \frac{1}{n} \frac{1}{1+\frac{k}{n}}$$ 我们令 $f(x)=\frac{1}{1+x}$ 于是得到求和部分为 $f\left( \frac{k}{n} \right)$ 该式子可以写成黎曼和的形式
$$\lim_{ n \to \infty } S_{n}=\int_{0}^1 \frac{1}{x+1}dx$$
于是结果为 $\ln 2$ 

3.2 显然，这个式子可以写成 
$$\frac{1}{n}\sum_{k=1}^n\left( \frac{k}{n} \right)^3$$
令 $f(x)=x^{3}$ , 则得到 
$$\lim_{ n \to \infty }  \frac{1}{n^4}\sum_{k=1}^n x^3 dx=\int_{0}^1 x^{3}dx=\frac{1}{4}$$
> [!Warning] Remark 1
> 变上限积分我们通常将其视为一个函数，其具备以下性质 :
> - 若 $f$ 在 $x_{0}$ 处连续，则 $F'(x_{0})=f(x_{0})$ 
> - 若 $x_{0}$ 为 $f$ 的跳跃间断点，那么 $F$ 在 $x_{0}$ 处连续但是不可导
> - 若 $x_{0}$ 为可去间断点，那么 $F(x)$ 在 $x_{0}$ 处可导，且导数等于其在 $f(x_{0})$ 的极限值
> - 若上限为一个函数，那么其满足复合函数的求导法则 
> $$F'(x)=\frac{d}{dx} \int_{a}^{\varphi(x)} f(t)dt=f(\varphi(x))\cdot \varphi'(x)$$
> - 若上下限都为一个函数，我们有口诀 **上限带入上限导-下限带入下限导**
> 
> 1. 我们在做题过程中要注意观察 $x\to ?$ 的值，我们常常会使用求极限中的洛必达法则来简化这个极限（我们此类题多数是利用其求导的性质）
> 2. 其次就是多加观察式子，想办法让它求导

> [!Warning] Remark 2
> 1. 我们主要要注意换元 令 $x=\tan \theta$ 我们的 $dx=\sec ^{2}x dx$ 恰巧 $\tan ^{2} \theta+1=\sec ^{2} x$  我们只留下了分母。随后，主要要注意我们用正切函数进行的对称换元。如果我们令 $\theta=\frac{\pi}{4}-t$ 对我们机积分结果没有什么影响，但是我们可以得到 $1+\tan t$ 从而再次得到 $J$ 。完成不积分求积分。
> 2. Wallis 公式在后续的定积分应用中有绝佳的用处。这个得记啊
> 3. 级数求极限应该不会为为难人吧（）

# 定积分在求面积时候的应用

> [!Danger] Corollary
> 1. 求平面面积 : 
>     - $\int_{a}^b |f-g|dx$ 平面坐标
>     - $\frac{1}{2} \int_{\alpha}^\beta (r_{1}^{2}(\theta)-r_{2}^{2}(\theta))d\theta$ 极坐标
> 2. 求弧长 : （微分思想和勾股定理 $ds=\sqrt{ dx^{2}+dy^{2} }$）
> 	- $\int_{a}^b \sqrt{ [x'(t)]^{2}+[y'(t)]^{2} }dt$ 参数表示
> 	- $\int_{a}^b \sqrt{ 1+[f'(x)]^{2} }dx$ 平面方程
> 	- $\int_{\alpha}^\beta \sqrt{ r^{2}(\theta)+[r'(\theta)]^{2} }d\theta$ 极坐标
> 3. 旋转体 : 
> 	- 求体积绕 $x$ 轴 
> $$\int_{a}^b \pi y^{2} dx$$
> 	- 求体积绕 $y$ 轴 
> $$\int_{c}^d \pi x^{2} dy $$
> 	-  求侧面积绕 $x$ 轴 
> $$\int_{a}^b 2\pi y ds =\int_{a}^b 2\pi y \sqrt{ dx^{2}+dy^{2} }$$
> 	- 求侧面积绕 $y$ 轴 
> $$\int_{c}^d 2\pi xds=\int_{c}^d 2\pi x\sqrt{ dx^{2}+dy^{2} }$$ 

> [!Example] EXAMPLE 1
> 1. 求 $y^{2}=x$ 与直线 $x-2y-3=0$ 围成的平面图形面积 $A$
> 
> 2. 求双曲线 $r^{2}=a^{2}\cos 2\theta$ 所围成的平面图形的面积 
> 
> 3. 求内摆线 $x=a\cos ^{3}t$ , $y=a\sin ^{3} t$ $(a>0)$ 所围成的图形的：
> 	- 面积
> 	- 弧长
> 	- 绕 $x$ 轴（$y$ 轴） 旋转的体积
> 	- 绕 $x$ 轴（$y$ 轴） 旋转的面积

Answer :
1. 分割区域 
$$A_{1}=\int_{0}^1 [\sqrt{ x }-(-\sqrt{ x })]dx=\frac{4}{3}$$ $$A_{2}=\int_{1}^9\left( \sqrt{ x }- \frac{x-3}{2} \right)dx=\frac{28}{3}$$
综合得到 $A=\frac{32}{3}$ 
如果我们转换坐标 $x=y^{2}=g_{1}(y)$ , $x=2y+3=g_{2}(y)$ 于是有 
$$A=\int_{-1}^3 [g_{2}(y)-g_{1}(y)]dy= \frac{32}{3}$$
2. 利用對稱性和公式，我們有 
$$A=4\cdot \frac{1}{2}\int_{0}^{\pi/4} a^{2} \cos 2\theta d\theta=\left.a^{2} \sin 2\theta\right|^{\pi/4}_{0}=a^{2}$$
3. 
	- 求面积  
     1. 利用格林公式，有
     $$ A = \frac{1}{2} \oint (x\,dy - y\,dx) $$
     其中
     $$ dx = -3a\cos^2 t \sin t\,dt,\quad dy = 3a\sin^2 t \cos t\,dt $$
     代入得
     $$ x\,dy - y\,dx = 3a^2 \sin^2 t \cos^2 t\,dt $$
     因此
     $$ A = \frac{1}{2} \int_0^{2\pi} 3a^2 \sin^2 t \cos^2 t\,dt
        = \frac{3a^2}{8} \int_0^{2\pi} \sin^2 2t\,dt
        = \frac{3\pi a^2}{8} $$
    2.利用对称性，只需求第一象限面积再乘以4。第一象限内，$t$ 从 $0$ 到 $\frac{\pi}{2}$，此时 $x$ 从 $a$ 到 $0$，$y$ 从 $0$ 到 $a$。  
	  面积微元为 $dA = y\,dx$（取正），故  
  $$
  A_1 = \int_0^a y\,dx = \int_{\frac{\pi}{2}}^0 a\sin^3 t \cdot (-3a\cos^2 t \sin t)\,dt = 3a^2 \int_0^{\frac{\pi}{2}} \sin^4 t \cos^2 t \, dt
  $$  
	  计算积分：  
  $$
  \int_0^{\frac{\pi}{2}} \sin^4 t \cos^2 t \, dt = \int_0^{\frac{\pi}{2}} \sin^4 t (1-\sin^2 t)\,dt = \frac{3\pi}{16} - \frac{5\pi}{32} = \frac{\pi}{32}
  $$  
	  所以 $A_1 = 3a^2 \cdot \frac{\pi}{32} = \frac{3\pi a^2}{32}$，总面积  
  $$
  A = 4A_1 = \frac{3\pi a^2}{8}
  $$ 
	- 弧长
     弧长微元
     $$ ds = \sqrt{(dx)^2+(dy)^2} = 3a|\sin t \cos t|\,dt $$
     故
     $$ L = \int_0^{2\pi} ds = 3a \int_0^{2\pi} |\sin t \cos t|\,dt = 6a $$
	  - 绕 \(x\) 轴旋转的体积（绕 \(y\) 轴同理）
     利用体积公式，取上半部分：
     $$ V_x = \pi \int_{-a}^{a} y^2\,dx = 2\pi \int_0^a y^2\,dx $$
     参数化，令 $x=a\cos^3 t,\ y=a\sin^3 t$，当 $t: 0\to \frac{\pi}{2}$，$x: a\to 0$
     $$ V_x = 2\pi \int_{\pi/2}^{0} (a^2\sin^6 t)(-3a\cos^2 t \sin t)\,dt
           = 6\pi a^3 \int_0^{\pi/2} \sin^7 t \cos^2 t\,dt $$
     计算积分
     $$ \int_0^{\pi/2} \sin^7 t \cos^2 t\,dt = \frac{16}{315} $$
     所以
     $$ V_x = 6\pi a^3 \cdot \frac{16}{315} = \frac{32\pi a^3}{105} $$
     同理
     $$ V_y = \frac{32\pi a^3}{105} $$
	  - 绕 $x$ 轴旋转的侧面积（绕 $y$ 轴同理）
     侧面积公式，取上半支（$0\le t\le \pi$）：
     $$ S_x = 2\pi \int_{\text{上半支}} y\,ds = 2\pi \int_0^\pi a\sin^3 t \cdot 3a|\sin t \cos t|\,dt
           = 6\pi a^2 \int_0^\pi \sin^4 t |\cos t|\,dt $$
     计算
     $$ \int_0^\pi \sin^4 t |\cos t|\,dt = \frac{2}{5} $$
     故
     $$ S_x = 6\pi a^2 \cdot \frac{2}{5} = \frac{12\pi a^2}{5} $$
     同理
     $$ S_y = \frac{12\pi a^2}{5} $$


# 反常积分

## 无穷积分
反常积分的计算也是牛顿莱布尼茨公式，但是我们对于反常积分主要还是判断其敛散性。

> [!Info] 可直接作用例子
> 讨论无穷积分 
> $$\int_{1}^{\infty} \frac{dx}{x^p}$$
> 的敛散性

Answer:
由于 $\int_{1}^u \frac{dx}{x^p}=\begin{cases} \frac{1}{1-p}(u^{1-p}-1), \quad p\neq 1\\ \ln u,\qquad \qquad p=1 \end{cases}$ . 所以当 $p>1$ 时收敛，$p\leq0$ 的时候发散至 $+\infty$ 

对于收敛，我们有如下分类 :
- 当 $\int_{a}^u |f(x)|dx$ 收敛时，我们称 $\int_{a}^{\infty}f(x)dx$ **绝对收敛**
- 若 $\int _a^{\infty}f(x)dx$ 收敛而其绝对值不收敛，则为**条件收敛**

### 比较法（Cauchy,等价）
几乎所有的判别法都保持着同一种共性，那就是差的绝对值小于 $\varepsilon$ .

> [!NOTE] Theorem : 比较原则
> 定义在 $[a,+\infty)$ 的两个非负函数 $f$ 和 $g$ 都在任何有限区间 $[a,u]$ 上可积，且满足 
> $$f(x)\leq g(x),x \in [a,+\infty)$$
> 则当 $\int_{a}^{\infty}g(x)dx$ 收敛时，$\int_{a}^{\infty} f(x)dx$ 也收敛，若 $f$ 发散 , $g$ 必然发散

> [!Danger] Corollary
> 1. **做商** :
> 	若 $f$ 和 $g$ 在任何区间 $[a,u]$ 可积，当 $x\in[a,+\infty]$ 时，$f(x)\geq{0}$ , $g(x)>0$ ，且 $\lim_{ x \to +\infty } \frac{f(x)}{g(x)}=c$ , 若 
> 		- $0<c<+\infty$ , $f(x)$ 与 $g(x)$ 的积分同敛态
> 		- $c=0$ , $g(x)$ 的积分收敛可退 $f(x)$ 的收敛
> 		- $c=+\infty$ , $g(x)$ 的积分发散可推 $f(x)$ 的也发散
> 	若我们选取 $\int_{1}^{\infty} \frac{dx}{x^p}$ 作为比较对象, 我们有两个推论 
> 2.  ( 柯西判别法 i )
> 	设 $f$ 定义在 $[a,+\infty]$ 上的非负函数 ，在任意有限区间 $[a,u]$ 上可积 ，则有：
> 		- 当 $1\leq f(x)\leq \frac{1}{x^p}$ , $x\in[a,+\infty)$ ,且 $p>1$ 时 $\int_{a}^{+\infty}f(x)dx$ 收敛 
> 		- 当 $f(x)>\frac{1}{x^p}$ , $x\in[a,+\infty)$ ,且 $p<1$ 时 $\int_{a}^{+\infty}f(x)dx$ 发散
> 3. ( 柯西判别法 ii )
> 	设 $f$ 定义在 $[a,+\infty]$ 上的非负函数 ，在任意有限区间 $[a,u]$ 上可积 ，且 
>$$\lim_{ x \to +\infty } x^p f(x)=\chi$$
>	则有
>		- 当 $p>1$ , $0\leq \chi<+\infty$ 时，$\int_{a}^{+\infty}f(x)dx$ 收敛 
>		- 当 $p\leq1$ , $0<\chi\leq+\infty$ 时，$\int_{a}^{+\infty}f(x)dx$ 发散 

> [!Example] EXAMPLE 1
> 4. 讨论 $\int_{o}^{\infty} \frac{{\sin x}}{1+x^{2}}dx$ 的敛散性 
> 
> 5. 讨论下述无穷积分的敛散性 
> $$\text{1)~} \int_{1}^{+\infty} x^a e^{-x} dx \text{~;~} \qquad \qquad \text{2)~} \int_{0}^{+\infty} \frac{x^{2}}{\sqrt{ x^{5}+1 }}dx$$

Answer :
1. 由于 $\left|\frac{{\sin x}}{1+x^{2}}\right|< \frac{1}{1+x^{2}}$ 由于 $\frac{1}{1+x^{2}}$ 收敛，由比较原则可知原积分必收敛
2.  1）我们可以利用推论 3 ,
$$\lim_{ x \to +\infty } x^{2}\cdot x^{\alpha} e^{-x}=0$$
显然收敛
   2）由于 $\lim_{ x \to +\infty }x^{1/2}\cdot \frac{x^{2}}{\sqrt{ x^5 +1}}=1$ ,立即可知其发散

> [!NOTE] Theorem ：A\D 判别法
> - Dirichlet 判别法 ： 若 $F(u)=\int_{a}^uf(x)dx$ 在 $[a,+\infty)$ 上有界，$g(x)$ 在 $[a,+\infty)$ 上单调趋于零 , 则 $\int_{a}^{+\infty} f(x)g(x)dx$ 收敛
> - Abel 判别法：若 $\int_{a}^{+\infty}f(x)dx$ 收敛 ，$g(x)$ 在 $[a,+\infty)$ 上单调有界，则 $\int_{a}^{+\infty} f(x)g(x)dx$ 收敛

> [!Example] EXAMPLE 2
> 讨论 $\displaystyle \int_{1}^{+\infty} \frac{{\sin x}}{x^p}dx$ 与  $\displaystyle \int_{1}^{+\infty} \frac{{\cos x}}{x^p}dx$ $p>0$ 的敛散性。

Answer :
1)  当 $p>1$ 时，$\displaystyle\int_{1}^{+\infty} \frac{\sin x}{x^p} d$ 绝对收敛
2) 当 $0<p\leq {1}$ 时，$\displaystyle \int_{1}^{+\infty} \frac{{\sin x}}{x^p}$ 条件收敛。
   当 $0 < p \le 1$ 时，由 Dirichlet 判别法，
$$ \int_{1}^{\infty} \frac{\sin x}{x^p} dx $$
   有界且 $\frac{1}{x^p}$ 单调递减趋于 0，故原积分收敛；但它并非绝对收敛，因为在每个区间 $[k\pi + \frac{\pi}{6}, k\pi + \frac{5\pi}{6}]$ 上 $|\sin x| \ge \frac{1}{2}$，于是
$$ \int_{1}^{\infty} \frac{|\sin x|}{x^p} dx \ge \sum_{k} \frac{C}{k^p} $$
   发散（$p \le 1$），所以该积分条件收敛。

## 瑕积分
设函数 $f(x)$ 在 $(a,b]$ 上有定义，在 $a$ 的任意右邻域内无界，但在任意闭区间 $[a+\varepsilon,b]$（$\varepsilon>0$）上可积。则称
$$
\int_a^b f(x)\,dx=\lim_{\varepsilon\to0^+}\int_{a+\varepsilon}^{b} f(x)\,dx
$$
为该瑕积分（若极限存在）。类似地可定义右端点 $b$ 为瑕点的情况，以及内部瑕点（需分段处理）。
> [!Info] 可直接作用例子
> 讨论瑕积分  
> $$
> \int_{0}^{1} \frac{dx}{x^p}
> $$
> 的敛散性。
>
> 计算：
> $$
> \int_{\varepsilon}^1 \frac{dx}{x^p}=
> \begin{cases}
> \dfrac{1}{1-p}(1-\varepsilon^{1-p}), & p\ne1,\\[6pt]
> -\ln\varepsilon, & p=1.
> \end{cases}
> $$
> 因此当 $p<1$ 时收敛（极限为 $\frac1{1-p}$），当 $p\ge1$ 时发散（$p=1$ 发散至 $+\infty$，$p>1$ 发散至 $+\infty$）。

若 $\displaystyle \int_a^b |f(x)|\,dx$ 收敛，则称原瑕积分 **绝对收敛**；若原积分收敛而绝对值积分发散，则称 **条件收敛**。

> [!NOTE] Theorem：比较原则
> 设 $f,g$ 在 $(a,b]$ 上非负，在任意 $[a+\varepsilon,b]$ 上可积，且  
> $$
> 0\le f(x)\le g(x),\quad x\in(a,b].
> $$
> 则：
> - 若 $\displaystyle \int_a^b g(x)\,dx$ 收敛，则 $\displaystyle \int_a^b f(x)\,dx$ 也收敛；
> - 若 $\displaystyle \int_a^b f(x)\,dx$ 发散，则 $\displaystyle \int_a^b g(x)\,dx$ 必发散。

> [!Danger] Corollary（极限比较法）
> 1. 若 $f(x)\ge0,\; g(x)>0$，且  
> $$
> \lim_{x\to a^+}\frac{f(x)}{g(x)}=c,
> $$
> 则：
> - 当 $0<c<+\infty$ 时，两积分同敛散；
> - 当 $c=0$ 时，若 $\int g$ 收敛则 $\int f$ 收敛；
> - 当 $c=+\infty$ 时，若 $\int g$ 发散则 $\int f$ 发散。
>
> 常用比较对象为 $\displaystyle \frac1{(x-a)^p}$（或 $\frac1{(b-x)^p}$），由此得到如下柯西判别法。
> 2. ( 柯西判别法i )
> 	-设 $f\ge0$ 且在任意 $[a+\varepsilon,b]$ 上可积。
> 	- 若存在 $p<1$，使得  
 > $$f(x)\le \frac{1}{(x-a)^p},\quad x\in(a,b],$$
 > 	则 $\displaystyle \int_a^b f(x)\,dx$ 收敛；
> 	- 若存在 $p\ge1$，使得  
  > $$f(x)\ge \frac{1}{(x-a)^p},\quad x\in(a,b],$$
>  则积分发散。
>  3. (柯西判别法ii)
> 	 若  
> $$\lim_{x\to a^+}(x-a)^p f(x)=\lambda,$$
>则：
> 	- 当 $p<1$ 且 $0\le\lambda<+\infty$ 时，积分收敛；
> 	 - 当 $p\ge1$ 且 $0<\lambda\le+\infty$ 时，积分发散。
>（右端点瑕点类似，将 $(x-a)$ 换为 $(b-x)$ 即可。）

> [!Example] EXAMPLE 1
> 判断下面瑕积分的敛散性： 
> $$1) \int_{0}^1 \frac{{\ln x}}{\sqrt{ x }}dx; \quad\quad\quad 2)\int_{1}^2 \frac{{\sqrt{ x }}}{\ln x}dx$$

Answer :
两个瑕积分的被积函数在各自的积分区间上下分别同号： $\frac{{\ln x}}{\sqrt{ x }}$ 在 $(0,1]$ 上恒为负， $\frac{{\sqrt{ x }}}{\ln{2}}$ 在  $(1,2]$ 上恒为正，他们的瑕积分收敛的绝对条件是一致的。
	1） 瑕点为 $0$ 由推论 $3$ 可知， 取 $p= \frac{3}{4}<1$  有 
$$\chi=\lim_{ x \to 0^+ }x^{3/4} \left|\frac{{\ln x}}{\sqrt{ x }}\right|= -\lim_{ x \to 0^+ } \frac{{\ln x}}{x^{-1/4}}=\lim_{ x \to 0^+ }(4x^{1/4}) =0  $$
上述式子采用了等价无穷小替换故第一个积分收敛
	2）瑕点为 $x=1$ ， 当取 $p=1$ 时 ，有 
$$\chi=\lim_{ x \to 1^+ } (x-1) \cdot \frac{\sqrt{ x }}{1+x}=\lim_{ x \to 1^+ } \frac{{x-1}}{\ln x}=1 $$
发散

瑕积分中也可使用分部积分或变换化为无穷积分，但直接形式如下：
> [!NOTE] Theorem
> **Dirichlet 判别法（瑕积分版）**  
> 设 $F(u)=\int_a^u f(x)\,dx$ 在 $(a,b]$ 上有界，$g(x)$ 在 $(a,b]$ 上单调且趋于 $0$（当 $x\to a^+$），则  
> $$
> \int_a^b f(x)g(x)\,dx
> $$
> 收敛。
>
> **Abel 判别法（瑕积分版）**  
> 若 $\displaystyle \int_a^b f(x)\,dx$ 收敛，$g(x)$ 在 $(a,b]$ 上单调有界，则  
> $$
> \int_a^b f(x)g(x)\,dx
> $$
> 收敛。

**混合型**
> [!Example] EXAMPLE 2
> 1. 判断下列积分的敛散性 
> $$1)\int_{0}^{+\infty} \frac{dx}{^3\sqrt{(x-1)^{2}x^{2}  }}\qquad \qquad 2)\int_{0}^{+\infty} \frac{{\ln x}}{x^p |1-x|^q}dx (p>0,q>0)$$
> 2. 若 $f(x)$ 在 $[a,+\infty)$ 上单调，且 $\displaystyle \int_{a}^{+\infty}f(x)dx$ 收敛 ，则当 $x\to +\infty$ 时， $f(x)$ 趋于 0

Answer :
1. 1） 被积函数分母在 $x=0$ 和 $x=1$ 的时候为 $0$ ，这两个点就是瑕点，同时我们要考虑无穷远处。首先对其进行切割 
$$\int_{0}^{+\infty}f(x)dx=\int_{0}^{1/2}f(x)dx+\int_{\frac{1}{2}}^{{3/2}}f(x)dx+\int_{\frac{3}{2}}^{+\infty}f(x)dx$$
- 在 $x=0$ 附近，当 $x\to 0^{+}$ 时, $(x-1)^{2}\to 1$ ,故 **收敛**
- 在 $x=1$ 附近，当 $x\to 1$ 时，与上述情况类似，也收敛
- 当 $x\to+\infty$ , $\displaystyle \int_{\frac{3}{2}}^{+\infty} \frac{dx}{x^{4/3}}$ 显然收敛。
故这个级数绝对收敛
1) 我们分三段讨论这个积分，瑕点分别可能为 $x=1,x=0$ 以及考虑无穷远处
- 在 $x=0$ 附近：$|1-x|\to 1$ 原式等价于 
$$\frac{|\ln x|}{x^p}$$
其收敛当且仅当 $p<0$ , 得到条件 ①
- 在 $x=1$ 附近：令 $t=x-1$ ，$\ln(1+t)\sim t$ ，$x^p\sim 1$ 于是有 
$$|t|^{1-q}$$
于是得到条件 ② ：$q<2$
- $x$ 趋于无穷 ，有等价 
$$\frac{|\ln x|}{x^p|1-x|^q}\sim \frac{{\ln x}}{x^{p+q}}$$
于是得到条件 ③ ：$p+q>1$
故其发散的充要条件为 $0<p<1,\quad 0<q<2,\quad p+q>1$  

3. 由于 $f$ 单调，故极限 
$$ L = \lim_{x \to +\infty} f(x) $$存在（可为有限值或 $+\infty$ 或 $-\infty$）。 假设 $L \neq 0$。则存在 $\varepsilon > 0$，使得 $|L| > \varepsilon$（若 $L = \pm\infty$ 也类似）。 若 $L > 0$（或 $L = +\infty$），则存在 $X > a$，当 $x \ge X$ 时， $f(x) > \frac{L}{2} > 0$（若 $L = +\infty$，则 $f(x) > 1$）。于是
$$ \int_{X}^{T} f(x) \, dx \ge \frac{L}{2} (T-X) \to +\infty \quad (T \to +\infty), $$与积分收敛矛盾。 若 $L < 0$（或 $L = -\infty$），则存在 $X > a$，当 $x \ge X$ 时， $f(x) < \frac{L}{2} < 0$，于是 $$ \int_{X}^{T} f(x) \, dx \le \frac{L}{2} (T-X) \to -\infty, $$也与积分收敛矛盾。 因此必有 $L=0$。故 $$ \lim_{x \to +\infty} f(x) = 0. $$证毕。

![[数学分析II期末复习 2]]