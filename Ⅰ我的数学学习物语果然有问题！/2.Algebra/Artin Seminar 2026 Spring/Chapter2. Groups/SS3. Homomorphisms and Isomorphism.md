---
tags:
  - Groups
  - Algebra
---
# Homomoprhisms

> [!ABSTRACT] Definition.3.1
> 令 $G$ 和 $G'$ 是两个群，我们将其写成乘法的形式。 **同态** (Homomoprhisms) $\varphi:G \to G'$ 是一个由 $G$ 到 $G'$ 的映射，对于所有的 $G$ 中的 $a,b$ 有 
$$\varphi(ab)=\varphi(a)\varphi(b)$$


![[1773806137806_edit_366218727996960.png]]
第一个区块为 $G$ 后面两个区块都为 $G'$

> [!Example] EXAMPLE
> 几个同态的例子：
>1. 行列式函数： $GL_{n}(\mathbb{R})\to \mathbb{R}^{\times}$
>2. 符号同态 $\sigma$ : $S_{n}\to \{ \pm {1} \}$ 这个主要运用在对 **置换** 的描述上 (奇偶置换)
>3. 指数映射  ( exponential map exp ) : $\mathbb{R}^+ \to \mathbb{R}^\times$ 定义为 $x \rightsquigarrow e^x$ 
>4. 映射 $\phi :\mathbb{Z}^{+}\to G$，定义为 $\phi (n) = a^{n}$，其中 $a$ 是 $G$ 中给定的元素
>5. 绝对值映射 $|\ \ |$ : $\mathbb{C}^\times \to \mathbb{R}^\times$ 

对于我们第三点和第四点，我们的合成法则在定义域中为加法，在值域中为乘法。我们需要同态的表示进行一定的修改 
$$\varphi(a+b)=\varphi(a)\varphi(b)$$
下面我们来了解以下同态映射的一个平凡映射 $\varphi:G\to G'$ 表示群 $G$ 中的所有元素都映射到 $G'$ 的单位元上。如果 $H$ 是单位元的子群，含有映射$i:H\to G$ 定义为对于所有$x$ 在 $H$ 中有 $i(x)=x$ 是一个同态

> [!TIP] Proposition3.1
>  令 $\varphi:G\to G'$ 是群的同态
>1. 如果 $a_{1},\dots,a_{k}$ 是群 $G$ 中的元素，有 $\varphi(a_{1}\cdot\cdot\cdot a_{k})=\varphi(a_{1})\cdots \varphi(a_{k})$ 
>2. $\varphi$ 将单位元映射到单位元：$\varphi(1_{G})=1_{G'}$
>3. $\varphi$ 将逆元映射为逆元: $\varphi(a^{-1})=\varphi(a)^{-1}$

**Proof.** 第一条证明可由定义给出，第二条为 $\varphi(1)=\varphi(1\cdot {1})=\varphi(1)\varphi(1)$ 我们两边消去 $\varphi(1)$ 就有 $\varphi(1)=1$ ；第三条关于逆元的证明，我们利用第二条有 $\varphi(1)=\varphi(a^{-1}a)=\varphi(a^{-1})\varphi(a)=1$ ,于是得到 $\varphi(a^{-1})=\varphi(a)^{-1}$ 

## ker and Im

群同态确定了两个重要的子群，我们用 $Kernel$ 和 ${Image}$ 来表示，我们这样表示像 

> [!ABSTRACT] Definition.3.2
> $$\mathrm{Im}\varphi=\{ x\in G'\mid x=\varphi(a) \text{ for some }a \text{ in } G \}$$
>像的另一种记号是 $\varphi(G)$ .

映射 $\mathbb{Z}^+ \to G$ 的像是 $n\rightsquigarrow a^n$ 由 $a$ 生成的循环子群 $\langle {a} \rangle$ 

同态的**像** (Image)是值域的一个子群，我们将验证其封闭性：如果 $x,y$ 是像中的元素，存在 $G$ 中的元素 $a$ 和 $b$ 使得 $x=\varphi(a)$ 和 $y=\varphi(b)$ . 由于 $\varphi(a)$ 是一个同态，$xy=\varphi(a)\varphi(b)=\varphi(ab)$ 于是我们验证了其封闭性

同态的**核** (kernel) 相对而言更加微妙且重要，我们常常这样表示核 

> [!ABSTRACT] Definition.3.3
> $$\ker \varphi=\{ a\in G \mid \varphi(a)=1 \}$$
>这表示 $G$ 中映射到 $G'$ 单位元的元素的集合
>核也是群 $G$ 的子群，我们可以比像更加直观的的证明（由于都是1）

行列式同态 $G L_{n}(\mathbb{R}) \to \mathbb{R}^{\times}$ 的核是特殊线性群 $S L_{n}(\mathbb{R})$ ； 符号同态 $S_{n} \to \{\pm 1\}$ 的核称为**交错群** (alternating)。它由偶置换组成，记为 $A_{n}$： 
$$\text{The alternating group $A_{n}$ is the group of even permutations.}$$
核控制着整个同态：$G$ 中哪些元素被映射到 $G'$ 的单位元，哪些元素在 $G'$ 中有相同的像。

- 如果 $H$ 是群 $G$ 的一个子群，$a$ 是 $G$ 中的一个元素，记号 $aH$ 将表示所有乘积 $ah$ 的集合，其中 $h$ 在 $H$ 中： 
  $$aH=\{ g\in G \mid g=ah \text{ for some }h \text{ in } H\}$$
   这个集合称为 $H$ 在 $G$ 的**左陪集** (left coset) , 左指的是元素出现在左边

> [!TIP] Proposition.3.2
> 令 $\varphi:G\to G'$ 为群的一个 **同构** ，令 $a,b$ 为 $G$ 中的元素，$K$ 为 $\varphi$ 的核。下面情况是等价的：
   >- $\varphi(a)=\varphi(b)$ ,
   >- $a^{-1}b$ 为 $K$ 中的元素
   >- $b$ 在陪集 $aK$ 中
   >- 陪集 $bK$ 与 $aK$ 相等

这里证明是容易的

> [!Danger] Corollary.3.1
> 同态 $\varphi :G\to G'$ 是单射的当且仅当核 $K$ 是 $G$ 的平凡子群 $\{ 1 \}$ 

这里的证明可以利用上述命题

> [!ABSTRACT] Definition.3.4
> 群 $G$ 的子群 $N$ 为一个正规子群表示任意 $N$ 中元素 $a$ 与任意 $G$ 中元素 $g$ . 有共轭 $gag^{-1}$ 为 $N$ 中元素

> [!TIP] Proposition.3.3
> 群同态的核是一个正规子群


证明依旧显然

> [!Example] EXAMPLE
>   - 特殊线性群 $SL_{n}(\mathbb{R})$ 是一般线性群 $GL_{n}(\mathbb{R})$ 的正规子群，交错群 $A_{n}$ 是对称群 $S_{n}$ 的正规子群
  > - 如果群是阿贝尔的，那么他的所有子群都是正规子群。非阿贝尔的则不一定如此

> [!ABSTRACT] Definition.3.5
> 群的中心表示与 $G$ 中每一个元素都可交换的的元素的集合，通常用 $Z$ 来表示 
>$$Z=\{ z\in G \mid zx=xz \ ,\forall x\in G \}$$
>它总是 $G$ 的正规子群。特殊线性群 $SL_{2}(\mathbb{R})$ 的中心包含两个矩阵 $I,-I$ , 对称群 $S_{n}$ 的中心是平凡的 (Trivial)

这一小节的最后，看看我们的一个例子 

> [!EXAMPLE] **EXAMPLE** $\varphi:S_{4}\to S_{3}$ 是一个群同态
> 一个阶为 $4$ 的对称群 $\{ 1,2,3,4 \}$ 我们若将其看成两个二元子集的并，就有 
>$$\Pi_{1}:\{ 1,2 \}\cup \{ 3,4 \}\quad \Pi_{2}:\{ 1,3 \}\cup \{ 2,4 \}\quad \Pi_{3}=\{ 1,4 \}\cup \{ 2,3 \}$$
>我们对元素进行 $\sigma=\{ 1,2,3 \}$ 置换，于是就有 $\sigma(\Pi_{1})=\sigma \{ \{ 1,2 \}\cup \{ 3,4 \} \}=\{ 2,3 \}\cup \{ 1,4 \}=|\Pi_{3}$ 我们居然得到了 $S_{3}$ 的结构！
>$$\varphi:S_{4}\to Sym(\{ \Pi_{1},\Pi_{2},\Pi_{3} \})\cong S_{3}$$



# Isomorphism

>我们学习了同态之后应该会有一个直觉，那就是我对 $\mathrm{Im}$ 中取了某一个元素，当我想要取其原像即 $\varphi^{-1}(a)$ 的时候，会发现我们不止对应了一个元素。自然的，我们会想着进一步的压缩条件...

> [!ABSTRACT] Definition3.6
>  一个双射映射且满足同态关系 $\varphi(a)\varphi(b)=\varphi(ab)$  ,我们就称其为同构 (Isomorphism) 

如果我们想要验证一个同态是一个同构，结合此前的推论，我们只需要验证其单射（injective）- 用 $\ker \varphi=\{ 1 \}$ 来验证以及满射 $\mathrm{Im}{\varphi}=G'$ 

如果我们举一个例子，比如说 $\mathbb{Z}_{12}$ 和 $R_{12}$ 的同构（后者为正多边形的旋转群）
![[Screenshot_20260325_105802_com.huawei.hinote.png]]

对于这个 **定义** 我们有一个引理

> [!Success] Lemma.3.6.1
> 如果 $\varphi:G\to G'$ 是一个同构，其逆映射 $\varphi^{-1}:G'\to G$ 也是一个一个同构

**Proof.** 这个证明是不难的，我们主要是证明其逆也是一个同态（因为他们本身是双射的），对于所有在 $G'$ 的元素 $x$ 和 $y$ , 我们希望有 $\varphi^{-1}(x)\varphi^{-1}(y)=\varphi^{-1}(xy)$ . 我们设 $a=\varphi^{-1}(x)$ , $b=\varphi^{-1}(y)$ 且 $c=\varphi^{-1}(xy)$ 我们要有 $ab=c$ 由于 $\varphi$ 是一个同态y，于是有 
$$\varphi(ab)=\varphi(a)\varphi(b)=xy=\varphi(c)$$
后面这段我也不知道 Artin 他是什么意思 , 又是神谕（Oracle）又是盒子（box）啥的。
总之，如果我们要表达两个群是同构的，我们能用约等号来表示 (不是怎么你又不按主流？)，记为 
$$G\approx G'$$
由于与一个群同构的不一定是单一的，我们就将与一个群同构的群称为同构类

> [!ABSTRACT] Definition3.7
> 与群 $G$ 同构的一些群我们称为**同构类** (Isomorphism class) 

同构类中任意两个群都是同构的，当我们谈及对群进行分类时，隐含的意思就是划分同构类

其实我们还是很能注意到一间事情——为什么同构就一定要同构于其他群呢？自己自己不能同构吗？于是我们就定义了**自同构**(Automorphism)，即 一个 $\varphi:G\to G$ . 对于一个自同构，比较重要的就是**共轭**

> [!ABSTRACT] Definition
> 群中一个确定的元素，如果群 $G$ 一个映射满足 
>$$\varphi(x)=gxg^{-1}$$
>这就是**共轭** (Conjugation), 它是一个自同构：要对其验证只需要证明其同态与双射。由于这是群中的运算，最终还是回到群元素的本身


> [!missing] 一个特殊情况
> 如果我们的群是阿贝尔的（Abelian），即 **可交换的** . 这类群的共轭回到本身的元素
> 
> 如果一个群是交换的，我们会得到一个有趣的结论如果 $aba^{-1}=b$ ，我们有 $aba^{-1}b^{-1}$ 

群中的共轭的元素将会与原来的元素有着类似的性质

===EXERCISES===
---