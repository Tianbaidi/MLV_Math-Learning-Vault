---
tags:
  - Analysis
  - Real_Analysis
  - Subanalytic_Set
  - Curve_Selection
---

> 论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §4,在把约束集 $Z$ 化到有限维后,关键一步是:**"若 $S$ 的取值在 $s_0$ 处有聚点,则由曲线选择引理得到一条实解析路径,再矛盾于路径刚性。"** 这里靠的就是 real analytic / semianalytic / subanalytic 集合的语言和 Hironaka 的**曲线选择引理**。

> 相关笔记:[[Lyapunov_Schmidt_Reduction]]、[[Path_Rigidity_of_S]]、[[Fredholm_Operator]]。

## 三类集合

> [!ABSTRACT] Definition(实解析集)
> 设 $U\subset\mathbb R^N$ 开,一族实解析函数 $f_1,\dots,f_m:U\to\mathbb R$ 的公共零点集
> $$ X=\{x\in U:f_1(x)=\cdots=f_m(x)=0\} $$
> 称为 $U$ 中的**实解析集**。它是"局部由解析方程刻画的集合"。

> [!ABSTRACT] Definition(semianalytic / subanalytic)
> - **semianalytic**:局部由有限个解析的等式与不等式刻画,如 $\{x:\kappa(z)=0,\ V_S(z)>0\}$。
> - **subanalytic**:semianalytic 集在**真解析映射**下的像。semianalytic 集投影后一般不保持 semianalytic,但保持 subanalytic。
>
> 关键链条:
> $$ \boxed{\text{实解析}}\ \subset\ \boxed{\text{semianalytic}}\ \subset\ \boxed{\text{subanalytic}}. $$

## 曲线选择引理(Hironaka)

> [!Success] Lemma(曲线选择引理, curve selection lemma)
> 设 $A$ 是一个 subanalytic 集,且 $0\in\overline{A}\setminus A$(或 $0\in\overline{A}$)。则存在 $\epsilon>0$ 与一条**实解析曲线** $\gamma:(-\epsilon,\epsilon)\to\mathbb R^N$,使得
> $$ \gamma(0)=0,\qquad \gamma\bigl((0,\epsilon)\bigr)\subset A. $$

> [!NOTE] 论文里的用法 (§4, Theorem 4.1)
> 设反例成立,则存在 $z_j\in Z$,$z_j\to0$,使得 $s(z_j)\ne s(0)=s_0$。取子列使 $s(z_j)>s_0$ 恒成立,于是 $0$ 落在
> $$ Z_+=Z\cap\{z:s(z)>s_0\} $$
> 的闭包中。$Z_+$ 是 semianalytic,故 subanalytic。由曲线选择引理,存在实解析曲线 $\gamma$ 满足 $\gamma(0)=0$ 且 $\gamma((0,\epsilon))\subset Z_+$。则 $F_{u(\gamma(t))}$ 是一族 $C^1$ 取值于 $C^3$ 的极小嵌入,且 $S$、$f_3$ 空间常数——于是可对 $(0,\epsilon)$ 用 [[Path_Rigidity_of_S]],得 $s(\gamma(t))$ 恒为常数;又 $\gamma(t)\to0$ 且 $s$ 连续,故 $s(\gamma(t))=s_0$,**与** $\gamma(t)\in Z_+$(即 $s>s_0$)$\ $**矛盾**。

## 为什么需要 subanalytic(而不只是实数解析)

> [!WARNING] 投影不保 semianalytic
> 若只有 semianalytic,曲线选择不一定奏效。subanalytic 有更好的"紧化/闭包"性质(如真映射下的行为、闭包仍 subanalytic),才能保证"若 $0$ 在闭包里,就能找到穿过 $0$ 的解析曲线"。这是论文 §4 用 Hironaka 而非更弱工具的原因。

> [!NOTE] 本节关系
> $$ \boxed{Z_+=\{\kappa=0,V_S=0,V_3=0,s>s_0\}}\ \subset\ \boxed{\text{subanalytic}}\ \xrightarrow{\text{curve selection}}\ \boxed{\text{解析路径 }\gamma}\ \xrightarrow{\text{路径刚性}}\ \boxed{\text{矛盾}}. $$
