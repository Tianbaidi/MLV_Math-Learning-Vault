---
tags:
  - Algebra
  - Groups
---

设，$\sigma$ 为群 $G$ 到 $\tilde{G}$ 的一个同态，则有以下性质  
$\mathrm{Im}\sigma$ 是 Abel 的，当且仅当下面几条性质等价 
1. $\sigma(x)\sigma(y)=\sigma(y)\sigma(x)$
2. $\sigma(xy)\sigma(x)^{-1}\sigma(y)^{-1}=\tilde{e}$
3. $\sigma(xyx^{-1}y^{-1})=\tilde{e}$
4. $xyx^{-1}y^{-1} \in \ker \sigma$
5. $\{ xyx^{-1}y^{-1} \mid x,y \in G\}\subset\ker\sigma$
我们称 $xyx^{-1}y^{-1}$ 为 $x,y$ 的 **换位子** 记为 $[x,y]$ , 有 
$$xy=yx \Longleftrightarrow xyx^{-1}y^{-1}=e$$


> [!ABSTRACT] Definition
> 群 $G$ 的所有换位子组成的子集生成的子群称为 $G$ 的 **换位子群** 或者 **导群** ，记作 $G'$ 或者 $[G,G]$ , ie
> $$G'=\{ xyx^{-1}y^{-1} \mid x,y \in G \}$$
> 即有  $\text{If }G\text{ is Abel Grop} \Longleftrightarrow G'=\{ e \}$ 

我们得到如下命题 

> [!TIP] Proposition
> 1. 群 $G$ 到 $\tilde{G}$ 的一个同态，则 $\mathrm{Im}\sigma$ 是 Able 的当且仅当 $G'\subset \ker \sigma$
> 2. $G'\lhd G$ 
> 3. $G/G'$ 是 Abel 的
> 4. 设 $N \lhd G$ ,则有 $G/N\text{ is Abel Group} \Longleftrightarrow G'\subset N$

> [!ABSTRACT] Definition
> 设 $G$ 是一个群，$G'$ 的换位子群记作 $G^{(2)}$ …… $G^{(i-1)}$ 的换位子群记为 $G{(i)}$ . 如果存在一个正整数 $k$ 使得 $G^{(k)}=\{ e \}$ ,那么称 $G$ 是 **可解群** , 否则则称为 *不可解群*
> 显然 , 若群是 Abel 的，那么自然 $G'=\{ e \}$ ,从而 Abel 群都是可解群

我们得到如下定理 

> [!NOTE] Theorem
> 群 $G$ 是可解群当且仅当 $G$ 存在如下递降子群列, 使得 
> $$G=G_{0}\rhd G_{1} \rhd\cdots\rhd G_{s}=\{ e \}$$
> 并且每个商群 $G_{i-1}/G_{i}$ 都是 Abel 的

> [!NOTE] Theorem
> 可解群的每个子群和同态像都是可解群

> [!Danger] Corollary
> 可解群的商群是可解群

> [!NOTE] Theorem
> 设 $N$ 是可解群 $G$ 的任一正规子群, 若 $N$ 和 $G/N$ 都是可解群, 则 $G$ 是可解群

> [!ABSTRACT] Definition
> 群 $G$ 只有平凡子群 $\{ e \}$ 和 $G$ , 那么称为单群

> [!NOTE] Theorem
> Abel 群 $G$ 是单群当且仅当 $G$ 是素数阶循环群

> [!NOTE] Theorem
> 若非 Abel 群是单群，则 $G$ 是不可解群

> [!Danger] Corollary
> 非 Abel 群的可解群不是单群

> [!ABSTRACT] Definition
> 群 $G$ 的一个递降子群列
> $$G=G_{0}\rhd G_{1}\rhd \cdots \rhd G_{r}=\{ e \}$$
> 称为 $G$ 的一个 **次正规子群列** .  该商群组 
>$$G_{0}/G_{1}\cdots$$
>称为上述子群列的 **因子群组** ,其中含有单位圆的因子群的个数称为次正规子群列的 **长度** 

> [!NOTE] Theorem（Jordan-Hölder 定理）
> 若两条次正规子群列的因子群组均为单群（这样的列称为 **合成列**），则这两条列的长度相等，且因子群组按重排列后逐项同构。


