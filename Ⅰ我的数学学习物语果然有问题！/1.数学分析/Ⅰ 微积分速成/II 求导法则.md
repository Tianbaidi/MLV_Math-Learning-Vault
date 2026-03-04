---
tags:
  - 微积分
---

> 上一篇文章我们了解了一些朴素的微积分观念，并且引出了可微和导数的定义，那么在这篇文章种我们主要总结一下求导的法则，以及一些求导的技巧。总体理解的难度就没那么大了，一些小技巧是在他人面前非常拿分的条件小反射。

## 补充

> [!NOTE] 可导与可微
> 可微可以可导，且 $f'(x_0)=g(x_0).\ \ dy=f'(x_o)dy$
> 对可导可微的证明：
> $proof.$ $$\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x}=f'(x_0)$$
> $\lim_{\Delta x \to 0}(\frac{\Delta y}{\Delta x}-f'(x_0))=0$
> $$\frac{\Delta y}{\Delta x} -f(x_0)=o(1) (\Delta x \to 0)$$所以有$$\Delta y=f'(x_0)+o(1)·\Delta x=f'(x) \Delta x +o(\Delta x)$$
> 这种充要关系仅仅在一元导数成立

### 导数的意义与性质

 > 陈在此处提及其在物理学上的意义，我们看路程，速度，加速度的概念。在我们中学的时候，可能在物理上；就已经提及了，这里不再复述。随后他讲了在人口统计运用中的导数运用，体现一个增长率，这里也不过多阐述了。

**导数的几何意义** 莱布尼茨（$Leibniz$）在此处贡献在于发现了曲线切线斜率与函数导数间的关系，同时得到了一般的计算方法，这种方法我们中学解析几何中已经有所了解，这里再给出法线的定义

<font color="#8064a2">某点的法线</font> 即在该点与其切线垂直的直线。

#### 单侧导数

**定义1**  （左右导数）
由于$$f'(x_0)=\lim_{\Delta x \to 0} \frac{f(x_0+\Delta x) -f(x_0)}{\Delta x}$$我们根据左右极限的定义，定义左右导数，于是有$$f'_+(x_0)=\lim_{\Delta x \to 0^+} \frac{f(x_0+\Delta x) -f(x_0)}{\Delta x}\tag{右极限}$$和$$f'_-(x_0)=\lim_{\Delta x \to 0^-} \frac{f(x_0+\Delta x) -f(x_0)}{\Delta x}\tag{左极限}$$
自然的，我们有：点在 $x_o$ 处可导 $\Leftrightarrow$ $f$ 在 $x_0$ 的左右导数存在且相等

> [!NOTE] 区别
>  $f'_+(x_0) \ 与f'(x_0\ +)$
>  $f'_-(x_0) \ 与f'(x_0\ -)$
>  左是 $f(x)$ 在 $x_0$ 的左右导数，右是 $f'(x)$ 在 $x_0$ 的左右极限

**推论** $f(x)$ 在 $(a,b)$ 的每一点可导，则称 $f$ 在 $(a,b)$ 上可导
若， $f$ 在 $x=a$ 有**右导数** ,在 $x=b$ 有**左导数** ，则 $f$ 在 $[a,b]$ 上可导 

# 导数的四则运算和求导准则
#### 基本初等函数的求导


**正弦函数求导**
公式：$(\sin x)' = \cos x$
证明：
$$\sin(x + \Delta x) - \sin x = 2 \cos \left( x + \frac{\Delta x}{2} \right) \sin \frac{\Delta x}{2}$$

由 $\cos x$ 的连续性与 $\sin \frac{\Delta x}{2} \sim \frac{\Delta x}{2} (\Delta x \to 0)$，可知：

$$\lim_{\Delta x \to 0} \frac{\sin (x + \Delta x) - \sin x}{\Delta x} = \lim_{\Delta x \to 0} \cos \left( x + \frac{\Delta x}{2} \right) \cdot \lim_{\Delta x \to 0} \frac{\sin \frac{\Delta x}{2}}{\frac{\Delta x}{2}} = \cos x$$

因此：
$$(\sin x)' = \cos x$$

同理可得：
$$(\cos x)' = -\sin x$$

---

**自然对数函数求导**
公式：$(\ln x)' = \frac{1}{x}$
证明：
$$\ln (x + \Delta x) - \ln x = \ln \frac{x + \Delta x}{x} = \ln \left( 1 + \frac{\Delta x}{x} \right)$$

由 $\ln \left( 1 + \frac{\Delta x}{x} \right) \sim \frac{\Delta x}{x} (\Delta x \to 0)$，可知：
$$\lim_{\Delta x \to 0} \frac{\ln (x + \Delta x) - \ln x}{\Delta x} = \frac{1}{x} \lim_{\Delta x \to 0} \frac{\ln \left( 1 + \frac{\Delta x}{x} \right)}{\frac{\Delta x}{x}} = \frac{1}{x}$$

因此：
$$(\ln x)' = \frac{1}{x}$$
---

**指数函数求导**
公式：$(e^x)' = e^x$
证明：
利用等价关系式  $e^{\Delta x} - 1 \sim \Delta x (\Delta x \to 0)$ ，可得：
$$\lim_{\Delta x \to 0} \frac{e^{x + \Delta x} - e^x}{\Delta x} = e^x \cdot \lim_{\Delta x \to 0} \frac{e^{\Delta x} - 1}{\Delta x} = e^x$$

因此：
$$(e^x)' = e^x$$

进一步，利用等价关系 (对 $a^x$ 换底得到 $e^{x\ln a}$) $$a^{\Delta x} - 1 \sim \Delta x \cdot \ln a (a > 0, a \neq 1)$$ 可以得到：
$$(a^x)' = (\ln a)a^x$$

---

**幂函数求导**
公式：$(x^a)' = ax^{a-1}$（其中 a 为任意实数，x > 0）
证明：
利用等价关系 $\left(1 + \frac{\Delta x}{x}\right)^a - 1 \sim \frac{a \Delta x}{x} (\Delta x \to 0)$，有：
$$\lim_{\Delta x \to 0} \frac{(x + \Delta x)^a - x^a}{\Delta x} = \lim_{\Delta x \to 0} \frac{x^a \left[ \left(1 + \frac{\Delta x}{x}\right)^a - 1 \right]}{x \cdot \frac{\Delta x}{x}} = x^{a-1} \lim_{\Delta x \to 0} \frac{\left(1 + \frac{\Delta x}{x}\right)^a - 1}{\frac{\Delta x}{x}} = ax^{a-1}$$

因此：
$$(x^a)' = ax^{a-1}$$

#### 导数的四则运算

**定理 1** $f\ ,\ g$ 在同一区间内可导，则 $c_1f(x)+c_2g(x)$ 也在该区间可导，且有$$(c_1f(x)+c_2g(x))=c_1f'(x)+c_2g'(x)$$
$eg_{1}.\log_{a}x\ 的求导$
 我们可以对 $\log_{a}x$ 进行换底 ,得到：
 $$\log_{a}x=\frac{{\ln x}}{\ln a}$$对得到的式子进行求导，就有$$\left( \frac{{\ln x}}{\ln a} \right)'=\frac{1}{\ln a}\cdot \frac{1}{x}=\frac{1}{x\ln a}$$
**定理 2** $f\ ,\ g$ 在同一区间内可导，则 $f·g$ 也在该区间可导，且有
$$(f ·g)'=f'(x)g(x)+f(x)g'(x)$$<font color="#4f81bd">证明思路：</font>加一项减一项，一进一退的处理方法

**定理3** 假设 $g(x)$ 在某一区间可导， $g(x)\not =0$  则 $\frac{1}{g(x)}$ 也在该区间可导，且有
$$\left( \frac{1}{g(x)} \right)'=\frac{-g'(x)}{g(x)^2}$$
*在对三角函数我们有以下计算推导：*
已知 $(\sin x)'=\cos x$ , $(\cos x)'=-\sin x$ .
$$(\sec x)'=\left( \frac{1}{\cos x} \right)'=\frac{\sin x}{\cos^2 x}=\tan x\sec x$$同理有$$(\csc x)'=-\cot x \csc x$$

**推论** 形如 $\frac{f(x)}{g(x)}$ 的求导，我们可以从定理 2、3 得到
$$[\frac{f(x)}{g(x)}]'=\frac{f'(x)g(x)-g'(x)f(x)}{g^2(x)}$$
*利用该推论我们可以有三角函数的推导*

$$(\tan x)'=\left( \frac{\sin x}{\cos x} \right)'=\frac{{\cos^2x+\sin^2x}}{\cos^2 x}=\sec^2x$$同理$$(\cot x)'=-\csc^2 x$$
**定理 4** *反函数求导定理*  $f(x)$ 在 $(a,b)$ 严格单调并，且可导, $f'(x)\not=0$ .
$\alpha=min(f(a+),f(b-))$  又 $\beta=max(f(a+),f(b-))$ . 则 $f^{-1}(y)$ 在 $(\alpha,\beta)$ 上可导，且
$$(f^{-1}(y))'=\frac{1}{f'(x)}(x=f^{-1}(y))$$
$proof.$ 
$$(f^{-1}(y))'=\lim_{ \Delta y \to 0 } \frac{f^{-1}(y+\Delta y)-f^{-1}(y)}{\Delta y} $$由于 $f$ 严格单调，故有 $\Delta x \not= 0  \Leftrightarrow \Delta y \not =0$ 
由于连续，有 $\Delta x \to 0\Leftrightarrow \Delta y \to 0$ 
于是有$$(f^{-1}(y))'=\lim_{ \Delta x \to 0 } \frac{\Delta x}{f(x+\Delta x)-f(x)}  =\frac{1}{f'(x)}$$

> [!NOTE] 在我们学习了复合函数之后，这个推导更有趣
> 有反函数 $y=f(x)$  $x=f^{-1}(y)$ 所以
> $$x=f^{-1}(f(x))$$ 我们对两边同时求导 $$
1=f^{-1}(y)' \cdot f'(x)
$$于是得到上式

*利用该定理我们可以进行反三角函数的导数推导*

$$(\arctan x)'=\frac{1}{(\tan y)'}=\frac{1}{\sec^2y}=\frac{1}{1+\tan ^2y}=\frac{1}{1+x^2}$$
同理 $$(arccot \ x)'=-\frac{1}{1+x^2}$$
$$(\arcsin x)'=\frac{1}{(\sin y)'}=\frac{1}{\cos y}=\frac{1}{\sqrt{ 1-\sin^2 y }}=\frac{1}{\sqrt{ 1-x^2 }}$$
同理$$(\arccos x)'=-\frac{1}{\sqrt{ 1-x^2 }}$$

##### $*$双曲正弦和双曲余弦的求导
我们有函数$$sh\ x=\frac{e^x-e^{-x}}{2}\ ,\ ch\ x=\frac{e^x+e^{-x}}{2}$$有类三角函数性质$$ch^2\ x-sh^2\ x=1$$
已知 $(e^{-x})'=\left( \frac{1}{e^x} \right)'=-\frac{(e^x)'}{e^{2x}}=-e^{-x}$ ,我们有
$$(sh\ x)'=\frac{1}{2}(e^x+e^{-x})=ch \ x, \ 同理 (ch\ x)'=sh\ x$$
推广到**双曲正切和双曲余切**
$$th\ x=\frac{sh\ x}{ch\ x}\ ,\ \coth x=\frac{ch\ x}{sh\ x} $$
带入求导公式可以得到$$(th\ x)'=\frac{ch^2\ x-sh^2\ x}{ch^2\ x}=sech^2\ x$$
同理$$(\coth x)'=-csch^2\ x$$
那么，我们对于反函数有
$$(sh^{-1}\ x)'=\frac{1}{(sh\ y)'}=\frac{1}{ch\ y}=\frac{q}{\sqrt{ 1+sh^2\ y }}=\frac{1}{\sqrt{ 1+x^2 }}$$同理$$(ch^{-1}\ x)=\frac{1}{\sqrt{ x^2 -1}},$$ $$(th^{-1 x})'=(\coth^{-1} x)'=\frac{1}{1-x^2}$$


> [!NOTE] 求导的线性运算   {二式可归纳得出}
>  $$\left( \sum^n_{i=1} a_{i}f_{i}(x)\right)'=\sum_{i=1}^n a_{1}f_{i}'(x)\tag{1}$$
>  $$\left( \prod^n_{i=1}\ f_{i}(x) \right)'=\sum_{j=1}^{n} f_{j}'\cdot \prod^{n}_{i=1,i \not = j}f_{i}\tag{2}$$

**定理5** *复合函数求导准则*   $u=g(x)$ 在 $x=x_{0}$ 可导， $g(x_{0})=u_{0}$ 
   $y=f(u)$ 在 $u=u_{0}$ 可导，则 $y=f(g(x))$ 在 $x=x_{0}$ 可导 . 有$$[f(g(x))]'=f'(u_{0})\cdot g'(x_{0})$$
$proof.$ 
  由 $f(u)$ 可微， $\Delta y=f(u_{0}+\Delta u)-f(u_{0})=f'(u_{0})\Delta u+o(\Delta u)$
  令 $$\alpha=\frac{o(\Delta u)}{\Delta u}$$于是有$$\lim_{ \Delta u \to 0,\Delta u\not=0 } \alpha=0 $$再令，当 $\Delta u=0$ 时，$\alpha =0$ .于是上式$$\Delta y=f'(u_{0})\Delta u+\alpha\Delta u$$在对于 $\Delta u=0$ 也成立。 得到式子$$\frac{\Delta y}{\Delta x}=f'(u_{0}) \frac{\Delta u}{\Delta x}+\alpha\frac{ \Delta u}{\Delta x}$$令 $\Delta x\to 0 \implies \Delta u \to 0 \begin{cases}\Delta u\not=0\\\Delta u=0\end{cases} \implies \lim_{ \Delta z \to 0 }\alpha=0$  于是得证$$[f(g(x))]'=f'(u_{0})\cdot g'(x_{0})$$
我们可以记为$$y=f(u)\ ,\ u=g(x)$$ $$y=f(g(x))=f \circ g(x)\ ,$$ $$[f(g(x))]'=\frac{dy}{dx}=\frac{dy}{du}\cdot \frac{du}{dx}$$于是我们又将复合函数的运算法则称为 **链式法则**

> **幂指函数的求导** -*提供一种求导思路*
> 形如 $$y=f(x)=u(x)^{v(x)}$$我们就称为幂指函数，求导时我们对齐两边取对数$$\ln y=v(x)\ln u(x)$$现在，我们同时对两边求导（对同一个变量- $x$）$\to$ 注意到左侧是一个复合函数，我们设为“$y(x)$”
>于是有$$\frac{1}{y}\cdot y'(x)=v'(x)\ln u(x)+v(x) \frac{u'(x)}{u(x)}$$ $$y'(x)=u(x)^{v(x)}[v'(x)]$$

#### 一阶微分的形式不变形

现在有函数 $y=f(u)$ 有导数 $y'(u)=f'(u)$ , $dy=f'(u)du$   (其中 $u$ 为自变量)
$y=f(u)$ , $u=g(x)$ 于是 $y=f(g(x))$ ,其求导
$$y'(x)=f'(u)g'(x)=f'(g(x))g'(x)$$ $$dy=f'(g(x))g'(x)dx=f'(g(x))dg(x)=f'(u)du\tag{这里u是中间变量}$$
**我们以隐函数求导和求微分为例子：**

有隐函数$$F(x,y)=0\ \;\ \ 例如\ \ \frac{x^2}{a^2}+\frac{y^2}{b^2}=1$$我们对例子进行两边同时求微分
$$
d\left( \frac{x^2}{a^2}+\frac{y^2}{b^2} \right)=0
$$ $$
\frac{1}{a^2} \cdot 2xdx+\frac{1}{b^2}\cdot 2ydy=0
$$ 于是我们可以得到 $$
dy=- \frac{b^2}{a^2}\cdot \frac{x}{y} dx
$$
故有 $$
\frac{dy}{dx}=- \frac{b^2}{a^2} \cdot \frac{x}{y}$$
**再有例子**  $$
e^{xy}+x^2y-1=0
$$
我们左右两边同时对 $x$ 求导 $$
\frac{d}{dx}(e^{xy}+x^2y)=0
$$
有 $$
e^{xy}\cdot(xy'+y)+(2xy+x^2y')=0
$$
我们有 $$
y'(x)=\frac{{-(2xy+y e^{xy})}}{xe^{xy}+x^2}
$$
*如此，我们总结思路：* 对于隐函数求微分（或导），我们有如下步骤，再以 $\sin y^2=\cos \sqrt{ x }$ 为例
1. 两边同时求微分（导） $$
2y\cos y^2 dy=-\sin \sqrt{ x }\ \cdot \frac{1}{2\sqrt{ x }} dx
$$
2. 进行变换，得到 $$
\frac{dy}{dx}=\frac{-\sin \sqrt{ x }}{4 \sqrt{ x }\ \cdot y\cos y^2}
$$
#### 函数的参数表示及其求导

我们有参数方程 $$
\begin{cases}
x=\phi (t) \\
y=\psi(t)
\end{cases}
$$ $t \in(\alpha,\beta)$ 且 $\phi\ , \psi$ 可导，$\phi$ 严格单调且 $\phi'(t)\not =0$ 

由反函数的可导定理， $t=\phi^{-1}(x)$ 我们形式上可以得到 $$
y=\psi(\phi^{-1}(x))
$$复合函数求导的链式方程 $$
\frac{dy}{dx}=\psi'(t) \cdot (\phi^{-1}(x))'=\psi'(t)\cdot \frac{1}{\phi(t)}=\frac{\psi'(t)}{\phi'(t)}
$$
或者我们可以直接求导
$$
\begin{cases}
dx=\phi'(t) dt \\
dy=\psi'(t)dt
\end{cases}
$$我们可以直接得到 $$
\frac{dy}{dx}=\frac{\psi'(t)}{\phi'(t)} $$ 

> [!NOTE] 注意
> 我们对函数的表示有 显函数，隐函数，参数表示，
> 在计算过程中可以进行选择，以求简便的方法


#### 高阶导数（微分）

**定义**  $y=f(x)$ , 若 $f'(x)$ 仍然可导，着记它的导数为 $$[f'(x)]'=f''(x)$$我们称它为 $f(x)$ 的二阶导数.
同理，我们可以写出其他表现形式 $$
\frac{d}{dx}\left( \frac{dy}{dx} \right)\ =\ \frac{d^2x}{dx^2}\ ,\ \frac{d}{dx}\left( \frac{df}{dx} \right)= \frac{d^2f}{dx^2}  
$$

**推广** 若 $f''(x)$ 仍然可导，则其导数为 $f(x)$ 的三阶导数，记为 $$
f'''(x)\left( 或 y'''(x), \frac{d}{dx}\left( \frac{d^2y}{dx^2} \right)=\frac{d^3y}{dx^3}, \frac{d}{dx}\left( \frac{d^2f}{dx^2} \right)=\frac{d^3f}{dx^3} \right).
$$从四阶导数开始，我们的导数就记为 $$
f^{(n)}(x)
$$

**定义**   (高阶导数) 设 $f$ 的 $n-1$ 阶导数仍然可导，则它的导数记为 $$ [f^{(n-1)}(x)]'=f^{(n)}(x) \quad \left( 或 y^{(n)}(x), \frac{d^nf}{dx^n}, \frac{d^ny}{dx^n} \right)$$

> [!NOTE] 注意
> 如果一个函数在一个点高阶可导，那么它在这个点必定低阶可导

##### 高阶导数的运算法则

**定理** 有函数 $f(x)$ , $g(x)$ 都 $n$ 阶可导，则
1.  $[c_{1}f(x)+c_{2}g(x)]^{(n)}=c_{1}f^{(n)}(x)+c_{2}g^{(n)}(x)$
2.   $Leibniz \textbf{公式}$
   $$
(f(x)\cdot g(x))^{(n)}=\sum_{k=0}^{n} C^{k}_{n}f^{(n-k)}g^{(k)}
$$
> 记忆可以参考二项式展开 . 

对 $Leibniz$ 公式的证明 (数学归纳法)
当导数为一阶时，这个结论是显然的
###### 证明
我们设 $Leibniz$ 公式对 $n$ 阶导数成立，即
$$
(f(x)\cdot g(x))^{(n)}=\sum_{k=0}^{n} C^{k}_{n}f^{(n-k)}g^{(k)}
$$那么其 $n+1$ 阶导数有 $$
(f\cdot g)^{(n+1)}=[(f\cdot g)^{n}]'=[\sum_{k=0}^nC_{n}^{k}f^{(n-k)}g^{(k)}]'
$$ 我们对其处理 $$
\sum_{k=0}^{n} C^k_{n}(f^{(n+1-k)}g^{(k)}+f^{(n-k)}g^{(k+1)})
$$ $$=f^{(n+1)}g^{(0)}+\sum_{k=1}^{n} C^k_{n}f^{(n+1-k)}g^{(k)}+\sum_{k=1}^{n} C^{k-1}_{n}f^{(n+1-k)}g^{(k)}+f^{(0)}g^{(n+1)}
$$ 由式子 $C_{n}^k+C_{n}^{k-1}=C_{n+1}^k$  整理式子得到数学归纳法证明 

**推论**
3.  $\left[  \frac{f(x)}{g(x)} \right]^{(n)}=\left[ f(x) \cdot \frac{1}{g(x)} \right]^{(n)}=\cdot\cdot\cdot$

##### 各种函数表示形式的高阶导数表示

**复合函数**  $y=f(u),u=g(x).$
$$
\frac{dy}{dx}= \frac{dy}{du}\cdot \frac{du}{dx}
$$ 运用链式法则和乘法法则$$
y''(x)=
\frac{d}{dx}\left(  \frac{dy}{dx} \right)= 
\frac{d}{dx}\left(  \frac{dy}{du}\cdot \frac{du}{dx} \right)=
\frac{d}{dx}\left(  \frac{dy}{du} \right)\cdot \left(  \frac{du}{dx} \right)+ \frac{dy}{du}\cdot \frac{d}{dx}\left(  \frac{du}{dx} \right)
$$于是我们有 $$
=f''(u)\cdot (g'(x))^2+f'(u)g''(x)
$$ 对于更高阶的求导一致使用链式法则和乘法法则可以得到。

--- 
 
**隐函数**  以  $e^{xy}+x^2y-1=0$ 为例，求 $\frac{d^2y}{dx^2}$ 

首先求一阶导数 $$
e^{xy}(y+xy')+(2xy+x^2y')=0
$$其中， $$
y'= \frac{-(ye^{xy}+2xy)}{xe^{xy}+x^2}=- \frac{y(e^{xy}+2x)}{x(e^{xy}+x)}
$$
再关于  $x$ 求导 $$e^{xy}(y+xy')^2+e^{xy}(y'+y'+xy'')+(2y+2xy'+2xy'+x^2y'')
=0$$
于是有 $$
y''=- \frac{e^{xy}[(y+xy')^2+2y']+(2y+4xy')}{x(e^{xy}+x)}
$$再将 $y’$ 带入可得

---

**参数表示** 形如 $$
\begin{cases}
x=\psi(t) \\
y=\phi(t)
\end{cases},\quad a\leq t\leq b
$$我们已知 $$
\frac{dy}{dx}= \frac{\phi'(t)}{\psi'(t)}
$$求 $\frac{d^2y}{dx^2}= \frac{d}{dx}\left(  \frac{dy}{dx} \right)$ 其等于 $$
\frac{{\left( \frac{\phi'(t)}{\psi'(t)} \right)}}{\psi'(t)}
$$

### 高阶微分
**定义** $y=f(x)$ , $y$ 的高阶微分为 $$
d^ny=d(d^{n-1}y)=\cdots=d(f^{(n-1)}(x)dx^{n-1})=f^{(n)}(x)dx^n
$$ 
> 注意：高阶微分不具有**形式不变性**，其高阶微分会产生新的项。