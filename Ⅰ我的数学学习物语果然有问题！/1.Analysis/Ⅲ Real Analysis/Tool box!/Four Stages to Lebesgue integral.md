---
tags:
  - Real_analysis
  - Lebesgue_Integral
---
> 我们将分四步构建一个完整的积分理论：
> - 简单函数( Simple Function )
> - 在有限测度集上有界的函数 ( Bounded Functions Supported on Set of Finite Measure )
> - 非负函数 ( Non-negative Functions )
> - 可积函数 ( The General Case of Integrable Functions )

# Stage One

我们有简单函数 $\displaystyle \varphi(x)=\sum_{k=1}^N a_{k} \chi_{E_{k}}(x)$ , 其中 $\displaystyle E_{k}$ 表示有限可测集、 $\displaystyle a_{k}$ 表示一个常数。这样的表示存在一定的歧义，即同一个简单函数可以写成多种这样的线性组合。于是，我们需要定义一个 $\displaystyle \varphi$ 的标准形式 **Canonical Form** 是形如上式的唯一分解，$\displaystyle a_{k}$ 互不相同且非零，各个 $\displaystyle E_{k}$ 不相交。

于是我们这样构造，我们令 $\displaystyle \varphi$ 取到有限多个非零值 $\displaystyle c_{1},c_{2}\cdots c_k$ ，再令 $\displaystyle F_{k}(x)=\{ x:\varphi (x)=c_{k} \}$ （此时 $\displaystyle F_{k}$ 无交 ）。我们得到标准形式 
$$\varphi(x)=\sum_{k=1}^N c_{k} \chi_{F_{k}}(x)$$
我们定义其勒贝格积分 
$$\int_{\mathbb{R}^d}\varphi(x)dx=\sum_{k=1}^N c_{k}m(F_{k})$$
若 $\displaystyle E$ 是 $\displaystyle \mathbb{R}^d$ 上的有限子集，我们的 $\displaystyle \varphi(x)\chi_{E}(x)$ 依旧为简单函数，定义 
$$\int_{E} \varphi(x)dx=\int \varphi(x)\chi_{E}(x)dx$$
>[!Warning] Remark 1
> 为了强调我们此处使用勒贝格测度，会将积分写作 
> $$\int_{\mathbb{R}^d}\varphi(x)dm(x)$$
> 我们为了方便时常写做 $\displaystyle \int \varphi(x)$ 或者 $\displaystyle \int \varphi$ 

> [!TIP] Propositions : 简单函数积分满足以下性质
>  (i) 表示的无关性：
>  若 $\varphi = \sum_{k=1}^{N} a_k \chi_{E_k}$ 是 $\varphi$ 的任意表示，则
>  $$ \int \varphi = \sum_{k=1}^{N} a_k m(E_k) $$ 
>  (ii) 线性：
>  若 $\varphi, \psi$ 简单，$a, b \in \mathbb{R}$，则 
>  $$ \int (a\varphi + b\psi) = a \int \varphi + b \int \psi $$ 
>  (iii) 可加性：
>  若 $E, F$ 是 $\mathbb{R}^d$ 中不相交的有限测度子集，则 
>  $$ \int_{E \cup F} \varphi = \int_E \varphi + \int_F \varphi $$ 
>  (iv) 单调性：
>  若简单函数满足 $\varphi \le \psi$，则 
>  $$\int \varphi \le \int \psi$$ 
>  (v) 三角不等式：
>  若 $\varphi$ 简单，则 $|\varphi|$ 亦简单，且 
>  $$ \left| \int \varphi \right| \le \int |\varphi| $$

我们这里主要证明 (i) . 首先我们放宽条件，令 $\displaystyle E_{k}$ 是非交的，不对 $\displaystyle a_{k}$ 进行限制。对与在 $\displaystyle \{ a_{k} \}$ 的不同 $\displaystyle a$ 我们定义 $\displaystyle E'_{a}=\bigcup E_{k}$ ，此处遍历 $\displaystyle a=a_{k}$ —— 于是，我们得到 $\displaystyle E_{a}'$ 是无交的，且 $\displaystyle m(E_{a}')=\sum m(E_{k})$ . 这里的和遍历 $\displaystyle k$ ，于是我们得到 $\displaystyle \varphi=\sum a\chi_{E_{a}'}$ , 和遍历所有非零值，显然 
$$\int \varphi=\sum am(E_{a}')=\sum_{k=1}^N a_{k}m(E_{k})$$
我们再尝试不对 $\displaystyle E_{k}$ 进行限制，我们可以细化来分解我们的 $\displaystyle \bigcup_{k=1}^N E_{k}$ ,即找到 $\displaystyle E^*_{1},E_{2}^*,\cdots,E^*_{n}$ 使得 $\displaystyle \bigcup_{k=1}^N E_{k}=\bigcup_{j=1}^n E_{j}^*$ ,其中，我们的 $\displaystyle E^*_{1},E_{2}^*,\cdots,E^*_{n}$ 是非交的且有 $\displaystyle \bigcup E^*_{j}=E_{k}$ 。于是我们得到了一族非交的 $\displaystyle E^*_{j}$ , 我们再令 $\displaystyle a^*_{j}=\sum a_{k}$ , 我们就有 $\displaystyle \varphi=\sum_{j=1}^n a_{j}^* \chi_{E^*_{j}}$ , 根据我们此前的结论，我们有 
$$\int \varphi =\sum a_{j}^* m(E^*_{j})=\sum \sum_{E_{k} \supset E^*_{j}}a_{k}m(E^*_{j})=\sum a_{k} m(E_{k})$$
于是第一条得证，后续几条就很方便了。
对于第二条，$\displaystyle \varphi,\psi$ 为任意表示，利用第一点的结论，结果显然。
对于三条，若 $\displaystyle E$ 和 $\displaystyle F$ 都是非交的，显然有 
$$\chi_{E\cup F}=\chi_{E}+\chi_{F} $$
于是，我们有 $\displaystyle \int_{E \cup F} \varphi=\int_{E} \varphi+\int_{F}\varphi$ .
对于第四条，实际利用了线性性，结论显然。第五条三角不等式也是显然且简单的，

> 若两个简单函数几乎处处相等，则它们的积分相等。这一事实对后续各阶段积分的定义也将成立。

# Stage Two
Bounded function supported on set of finite measure.
The support of measurable function $\displaystyle f$ is defined to be the set of all points where $\displaystyle f$ dose not vanish, 
$$supp(f)=\{ x:f(x)\neq 0 \}$$
We shall also say that $\displaystyle f$ is **supported** on set $\displaystyle E$ , if $\displaystyle f(x)=0$ whenever $\displaystyle x \notin E$ .
由于 $\displaystyle f$ 是可测的，支撑集 $\displaystyle supp(f)$ 也是可测的。我们接下来要关注那些满足 $\displaystyle m(supp(f))<\infty$ 有界可测函数 ：

[[Simple Function and Step Function%Littlewood's Three Principles#32#35|Theorem 4.2]] 阐述了对以 $\displaystyle M$ 为界且支撑在集合 $\displaystyle E$ 上的函数 $\displaystyle f$ 存在一系列简单函数 $\displaystyle \{ \varphi_{n} \}$ , 任意的 $\displaystyle \varphi_{n}$ 都有界 $\displaystyle M$ 且以 $\displaystyle E$ 为支撑，使得 
$$\varphi_{n}(x)\to f(x)\quad \text{for all }x$$
我们有以下引理 
> [!Success] Lemma
> 令 $\displaystyle f$ 为有界函数且支撑在有限测度集合 $\displaystyle E$ 上。如果 $\displaystyle \{ \varphi_{n} \}_{n=1}^{\infty}$ 为任意系列的有界 $\displaystyle M$ 的简单函数且支撑在 $\displaystyle E$ 上，若 $\displaystyle \varphi_{n}(x)\to f(x)$ 对 $\displaystyle x$ 几乎处处成立，我们有 