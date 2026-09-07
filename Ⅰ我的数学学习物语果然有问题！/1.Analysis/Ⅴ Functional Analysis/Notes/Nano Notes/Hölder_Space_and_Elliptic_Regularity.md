---
tags:
  - Analysis
  - Functional_Analysis
  - Elliptic_PDE
  - Schauder_Theory
---

> 论文 [[Chern's Conjecture with Constant Cubic Trace(Tan–Tang–Xie–Yan)]] 的 §4、§5 大量使用 Hölder 空间与 Schauder 椭圆理论:§4 把 $L=\Delta+n+S$ 作为 $C^{k,α}(M)\to C^{k−2,α}(M)$ 的 Fredholm 算子,§5 用"强解正则性 + Schauder 迭代"把 $C^{1,1}$ 的解提升到 $C^\infty$。这篇是支撑那两处的分析地基。

> 相关笔记:[[Fredholm_Operator]]、[[Lyapunov_Schmidt_Reduction]]。

## Hölder 空间 $C^{k,α}$

> [!ABSTRACT] Definition(Hölder 空间)
> 对非负整数 $k$ 与 $0<\alpha<1$,定义 $C^{k,α}(M)$ 为 $M$ 上 $k$ 阶导数连续、且最高阶导数满足 Hölder 条件的函数空间。其范数为
> $$ \|u\|_{C^{k,α}}=\|u\|_{C^k}+\sum_{|\beta|=k}\sup_{x\ne y}\frac{|D^\beta u(x)-D^\beta u(y)|}{d(x,y)^\alpha}. $$
> 论文中的 Hölder 范数都关于诱导度量 $g$ 取。

> [!TIP] 核心代数性质
> Hölder 空间在**逐点乘法**下是 **Banach 代数**:即存在常数 $C$ 使
> $$ \|uv\|_{C^{k,α}}\le C\|u\|_{C^{k,α}}\|v\|_{C^{k,α}}. $$
> 论文反复用它断言:乘积、矩阵求逆、正平方根这些运算把各阶 Hölder 范数"粘在一起",从而 $H$、$S(u)$、$f_3(u)$、$V_S(u)$、$V_3(u)$ 均随 $u$ **实解析**。

## 椭圆算子与 Schauder 估计

> [!NOTE] 为什么 $\Delta+n+S$ 是"好的"算子
> 主部 $\Delta$ 是(一致)椭圆的。闭流形上 **Schauder 估计**给出正则性提升:若 $Lu=f\in C^{k−2,α}$,则 $u\in C^{k,α}$,且
> $$ \|u\|_{C^{k,α}}\le C\bigl(\|Lu\|_{C^{k−2,α}}+\|u\|_{C^0}\bigr). $$
> 由此即得 $L:C^{k,α}(M)\to C^{k−2,α}(M)$ 是 [[Fredholm_Operator]]。

## 椭圆正则性的"升阶"机制

> [!Success] Lemma(升阶链条)
> 论文 §5 用到的链条是:
> $$ C^{1,1}\ \xrightarrow{\text{强解椭圆正则}}\ C^{2,α}\ \xrightarrow{\text{Schauder 迭代}}\ C^\infty. $$
> 具体是:因 $u\in C^{1,1}\subset W^{2,\infty}$,对(24)式做 Sobolev 链式法则,得非散度形式统一椭圆方程 $a^{βγ}(x)u_{βγ}=f(x)$,其中系数 $a^{βγ}$、$f$ 是 Lipschitz 的。由内部强解正则性定理([Gilbarg–Trudinger, Thm 9.19]),$u\in C^{2,α}$;再对方程逐次求导 + Schauder 估计,得 $u\in C^\infty$。

> [!WARNING] 这里的两个"黑盒"结论
> 1. **Sobolev 链式法则**:$u\in C^{1,1}\subset W^{2,\infty}$ 时,(24)式几乎处处给出非散度方程。
> 2. **强解正则性定理**:非散度统一椭圆方程在 Lipschitz 系数下的内部正则性,见 Gilbarg–Trudinger §9。
>
> 第一遍读论文时这两处可先当作黑盒接受,不影响理解 §5 的结论。

> [!NOTE] 本节关系
> $$ \boxed{C^{k,α}\text{ 是 Banach 代数}}\ +\ \boxed{\Delta\text{ 椭圆}}\ \xrightarrow{\text{Schauder}}\ \boxed{L=C^{k,α}\to C^{k−2,α}\text{ Fredholm}}\ \xrightarrow{\text{迭代}}\ \boxed{C^{1,1}\Rightarrow C^\infty}. $$
