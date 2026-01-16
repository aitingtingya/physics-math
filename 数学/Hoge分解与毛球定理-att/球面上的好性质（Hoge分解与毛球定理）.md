希望只用几何、拓扑、代数的方法，如果用到分析只涉及最简单的极限或积分，证明一下 Hoge 分解定理和毛球定理，这俩定理在引力与相对论文件夹中的局域视界笔记中被用到。第一个定理没有得到完全证明，第二个可以证明。
# Hoge 分解定理
对于一个紧致无边的定向黎曼流形 $(M,g_{\mu{}\nu{}})$，设 $\Lambda{}^{k}$ 是它的全体光滑 $k-$形式空间。所有光滑形式场的集合记作 $\Lambda{}(M)$。在 $\Lambda{}^{k}$ 上定义内积
$$
\begin{eqnarray}
\langle{}\alpha{},\beta{}\rangle{}_{k}
:=\frac{1}{k!}\int_{M}^{}\alpha{}\cdot{}\beta{}
\end{eqnarray}
$$
其中缩并 $\cdot{}$ 由度规执行，容易看出来这确实是一个内积。所以 $\Lambda{}$ 是一个内积空间，它的完备化的希尔伯特空间记作 $\mathcal{H}$。
 
由于假设 $\Lambda{}^{k}$ 中元素的光滑性，所以外代数的定义域是全体 $\Lambda{}^{k}$ 。然后定义余外微分算子 $\mathfrak{d}$ 为 ${\rm d}$ 的伴随，即
$$
\begin{eqnarray}
\langle{}f,\mathfrak{d}\alpha{}\rangle{}_{k}
:=\langle{}{\rm d}f,\alpha{}\rangle{}_{k+1}
\end{eqnarray}
$$
 证明它确实是全局良定义的，只需要研究一下它的具体形式
$$
\begin{eqnarray}
\frac{1}{(k+1)!}\int_{M}^{}
{\rm d}f\cdot{}\alpha{}
&=&\frac{1}{k!}\int_{M}^{}
(\nabla_{\mu{}_{1}}f_{\mu{}_{2}...\mu{}_{k+1}})\alpha{}^{\mu{}_{1}...\mu{}_{k+1}}
\nonumber\\
&=&\frac{1}{k!}
\int_{M}^{}\nabla_{\mu{}_{1}}f_{\mu{}_{2}...\mu{}_{k+1}}\alpha{}^{\mu{}_{1}...\mu{}_{k+1}}
-f_{\mu{}_{2}...\mu{}_{k+1}}
\nabla_{\mu{}_{1}}\alpha{}^{\mu{}_{1}...\mu{}_{k+1}}
\nonumber\\
&=&-\frac{1}{k!}\int_{M}^{}f\cdot{}\nabla_{}\cdot{}\alpha{}
\end{eqnarray}
$$
所以有
$$
\begin{eqnarray}
\mathfrak{d}\alpha{}
&=&-\nabla_{}\cdot{}\alpha{}
\end{eqnarray}
$$
由 $\mathfrak{d}$ 的性质可以看到，$\mathfrak{d}\mathfrak{d}=0$，并且显然它的定义域与外微分定义域一致。可以用
$$
\begin{eqnarray}
\beta{}=\mathfrak{d}\alpha{}
\end{eqnarray}
$$
来定义余恰当形式场。
定义 Hoge 拉普拉斯算子
$$
\begin{eqnarray}
\Delta{}
:={\rm d}\mathfrak{d}
+\mathfrak{d}{\rm d}
\end{eqnarray}
$$
显然它的定义域 $\Lambda{}$ 空间。先把它们三个的定义域延拓到 $\mathcal{H}$ 上。下面给出定义
$\forall{}\alpha{}\in{}\mathcal{H}$，称 $\beta{}\in{}\mathcal{H}$ 是它的外微分，如果
$$
\begin{eqnarray}
\langle{}\alpha{},\mathfrak{d}\gamma{}\rangle{}
=\langle{}\beta{},\gamma{}\rangle{}
\qquad
\forall{}\gamma{}\in{}\Lambda{}
\end{eqnarray}
$$
同样的称 $\beta{}$ 是 $\alpha{}$ 的余外微分，如果
$$
\begin{eqnarray}
\langle{}\beta{},{\rm d}\gamma{}\rangle{}
=\langle{}\alpha{},\gamma{}\rangle{}
\end{eqnarray}
$$
显然该定义在 $\Lambda{}$ 上与原定义是一致的。只需要证明在各种极限点上 $\mathfrak{d}$ 和 ${\rm d}$ 是单射即可，以一个为例，如果 $\beta{}^{1},\beta{}^{2}\in{}\mathcal{H}$，由于它们和 $\forall{}\gamma{}\in{}\Lambda{}$ 的内积都一样，所以在 $\Lambda{}$ 中任意构造一个柯西序列 $x^{k}$，都有
$$
\begin{eqnarray}
\langle{}\beta{}^{1}
-\beta{}^{2},x^{k}\rangle{}
=0
\end{eqnarray}
$$
而 $\Lambda{}$ 中的柯西序列可以收敛到 $\mathcal{H}$ 中所有元素，因此 
$$
\begin{eqnarray}
\beta{}^{1}
=\beta{}^{2}
\end{eqnarray}
$$
所以定义是良好的。然后就可以用它们两个来得到 $\Delta{}$ 定义域的延拓。从定义可以看到，${\rm d}$ 和 $\mathfrak{d}$ 互为伴算子，而 $\Delta{}$ 是自伴的。
在希尔伯特空间上有
$$
\begin{eqnarray}
\langle{}\alpha{},\Delta{}\beta{}\rangle{}_{k}
&=&\langle{}\alpha{},{\rm d}\mathfrak{d}\beta{}\rangle{}
+\langle{}\alpha{},\mathfrak{d}{\rm d}\beta{}\rangle{}
\nonumber\\
&=&\langle{}\mathfrak{d}\alpha{},\mathfrak{d}\beta{}\rangle{}
+\langle{}{\rm d}\alpha{},{\rm d}\beta{}\rangle{}
\end{eqnarray}
$$
由于外微分和余外微分会改变形式的阶数，所以显然它俩的本征值只能为零。比如对于外微分，它作用到闭形式上都为零。但是对于 $\Delta{}$，可能有非零本征值了。这里关心它的零本征值，也就是关注那些形式场 $\alpha{}$ 满足
$$
\begin{eqnarray}
\Delta{}\alpha{}
=0
\end{eqnarray}
$$
对于这样的形式场，有
$$
\begin{eqnarray}
0
&=&\langle{}\mathfrak{d}\beta{},\mathfrak{d}\alpha{}\rangle{}
+\langle{}{\rm d}\beta{},{\rm d}\alpha{}\rangle{}
\qquad
\forall{}\beta{}
\end{eqnarray}
$$
自然也有
$$
\begin{eqnarray}
0
&=&\langle{}\mathfrak{d}\alpha{},\mathfrak{d}\alpha{}\rangle{}
+\langle{}{\rm d}\alpha{},{\rm d}\alpha{}\rangle{}
\end{eqnarray}
$$
对于伪黎曼几何，度规诱导的内积不正定，上式为零不意味着做内积的元素为零，但是对于黎曼几何，上式为零一定等价于
$$
\begin{eqnarray}
\mathfrak{d}\alpha{}
=0
\qquad
{\rm d}\alpha{}
=0
\end{eqnarray}
$$
所以前面才把流形定义为黎曼流形。然后就有
$$
\begin{eqnarray}
\Delta{}\alpha{}=0
\leftrightarrow{}\mathfrak{d}\alpha{}=0,
{\rm d}\alpha{}=0
\end{eqnarray}
$$
称 $\Delta{}$ 作用为零的形式场为调和形式场。然后证明恰当形式场、余恰当形式场、调和形式场是正交的。也就是设 $\gamma{}$ 为调和形式场，则依次计算
$$
\begin{eqnarray}
\langle{}{\rm d}\alpha{},\mathfrak{d}\beta{}\rangle{}
&=&\langle{}{\rm d}{\rm d}\alpha{},\beta{}\rangle{}
\nonumber\\
&=&0
\end{eqnarray}
$$
$$
\begin{eqnarray}
\langle{}{\rm d}\alpha{},\gamma{}\rangle{}
&=&\langle{}\alpha{},{\rm d}\gamma{}\rangle{}
\nonumber\\
&=&0
\end{eqnarray}
$$
$$
\begin{eqnarray}
\langle{}\mathfrak{d}\alpha{},\gamma{}\rangle{}
&=&\langle{}\alpha{},\mathfrak{d}\gamma{}\rangle{}
\nonumber\\
&=&0
\end{eqnarray}
$$
下面先说明它们的 kernal 都是闭的，这其实很简单，首先说明一个希尔伯特空间上的算子的定义域如果是闭的，那么它的任何本征子空间都是闭的，可以用反证法，假如一个算子 $T$ 的定义域 $O_{T}$ 是闭的，但是对应于某个本征值 $T^{k}$本征子空间 $V^{k}\subset{}O_{k}$ 不是闭的，那么就有这个子空间中的序列极限 $x_{\infty} \subset{}O_{T}/V^{k}$，但是根据算符作用的线性性以及实数空间的完备性，$T$ 作用到该极限上还应该得到本征值 $T^{k}$，这与 $x_{\infty}\notin{}V^{k}$ 矛盾。所以 $V^{k}$ 必须是闭的。

由于 ${\rm d}$、$\mathfrak{d}$ 和 $\Delta{}$ 的定义域是希尔伯特空间 $\mathcal{H}$，所以它们的任何本征子空间是闭的，自然它们的 kernal 是闭的。先看 $\Delta{}$ 的 kernal，对于 $\forall{}x\in{}\mathcal{H}$，定义
$$
\begin{eqnarray}
f_{x}:{\rm ker}_{\Delta{}}
&\rightarrow{}&\mathbb{R}
\nonumber\\
y&\mapsto{}&|x-y|
\end{eqnarray}
$$
这个映射显然是有下界的，绝对值最小不会比零小。$f_{x}$ 的像是 $\mathbb{R}$ 中的一个集合，如果这个集合是左闭的，那说明这个集合有最小值，如果这个集合是左开的且在开在 $r_{x}\geq{}0$ 处。则在 ${\rm ker}_{\Delta{}}$ 中一定可以找到一个序列 $y^{k}$，它的像 $f^{k}_{x}$ 在 $\mathbb{R}$ 中是柯西序列，极限为 $r_{x}$，下面说明这一定是一个 ${\rm ker}_{\Delta{}}$ 中的柯西序列，且这样找到的柯西序列都收敛到同一个元素。此时可以计算
$$
\begin{eqnarray}
|y^{k}-y^{l}|^{2}
&=&\int_{}^{}(y^{k}-y^{l})\cdot{}(y^{k}-y^{l})
\nonumber\\
&=&\int_{}^{}(y^{k}-x^{k}+x^{k}-y^{l})\cdot{}(y^{k}-x^{k}+x^{k}-y^{l})
\nonumber\\
&=:&\int_{}^{}(\delta{}y^{k}-\delta{}y^{l})\cdot{}(\delta{}y^{k}-\delta{}y^{l})
\nonumber\\
&=&|\delta{}y^{k}|^{2}
+|\delta{}y^{x}|^{2}
-2\langle{}\delta{}y^{k},\delta{}y^{l}\rangle{}
\nonumber\\
&=&2|\delta{}y^{k}|^{2}
+2|\delta{}y^{x}|^{2}
-\langle{}\delta{}y^{k}+\delta{}y^{l},\delta{}y^{k}+\delta{}y^{l}\rangle{}
\nonumber\\
&=&2|\delta{}y^{k}|^{2}
+2|\delta{}y^{x}|^{2}
-|y^{k}+y^{l}
-2x|^{2}
\nonumber\\
&=&2|\delta{}y^{k}|^{2}
+2|\delta{}y^{x}|^{2}
-4|\frac{y^{k}+y^{l}}{2}
-x|^{2}
\end{eqnarray}
$$
由于
$$
\begin{eqnarray}
|\frac{y^{k}+y^{l}}{2}
-x|^{2}>(r_{x})^{2}
\end{eqnarray}
$$
所以上式变为
$$
\begin{eqnarray}
|y^{k}-y^{l}|^{2}
&<&2(f^{k}_{x})^{2}
+2(f^{l}_{x})^{2}
-4(r_{x})^{2}
\end{eqnarray}
$$
当让 $k,l\rightarrow{}\infty$ 时，由于 $f^{k}_{x}$ 是柯西序列，所以上式变为
$$
\begin{eqnarray}
\mathop{\rm lim}\limits_{k,l\rightarrow{}\infty}^{}
|y^{k}-y^{l}|^{2}
<\epsilon{}\rightarrow{}0
\end{eqnarray}
$$
所以 $y^{k}$ 是柯西序列，那么它的极限必须在 ${\rm ker}_{\Delta{}}$ 中，而它极限的像又是 $r_{x}$，这与 $f_{x}$ 的像在 $r_{x}$ 处左开矛盾，所以 $f_{x}$ 的像一定在 $\mathbb{R}$ 中左闭，也就是有最小值，并且由于前面构造的序列收敛于某个点 $y^{\infty}\in{}{\rm ker}_{\Delta{}}$，所以让 $f_{x}$ 取最小值的点是唯一的，记作 $y_{x}$。然后定义
$$
\begin{eqnarray}
z_{x}
:=x-y_{x}
\end{eqnarray}
$$
上式给出 $|z_{x}|=r_{x}$。因此 $\forall{}y\in{}{\rm ker}_{\Delta{}}$，有
$$
\begin{eqnarray}
|x-y|^{2}
&=&(r_{x})^{2}
+|y_{x}
-y|^{2}
+2\langle{}z_{x},y_{x}
-y\rangle{}
\nonumber\\
&=&(r_{x})^{2}
+|y'|^{2}
+2\langle{}z_{x},y'\rangle{}
\end{eqnarray}
$$
由于 $y'\in{} {\rm ker}_{\Delta{}}$，所以 $-y'\in{}{\rm ker}_{\Delta{}}$。如果
$$
\begin{eqnarray}
\langle{}z_{x},y'\rangle{}\neq0
\end{eqnarray}
$$
则
$$
\begin{eqnarray}
-\langle{}z_{x},y'\rangle{}\neq0
\end{eqnarray}
$$
上面俩总有一个为负值，不妨就让 $y'$ 那一项为负值，让它的归一化为 $\hat{y}'$，则
$$
\begin{eqnarray}
|y'|^{2}
+2\langle{}z_{x},y'\rangle{}
&=&|y'|^{2}
+2\langle{}z_{x},\hat{y}'\rangle{}|y'|
\end{eqnarray}
$$
则上式右端中 $2\langle{}z_{x},\hat{y}'\rangle{}$ 是一个负常数，所以上式是一个关于 $|y'|$ 的一元二次方程，显然它在正实轴上有负值，这会导致 $\exists{}x\in{}{\rm ker}_{\Delta{}}$ 使得
$$
\begin{eqnarray}
|x-y|^{2}
<(r_{x})^{2}
\end{eqnarray}
$$
与原假设不符，因此 $z_{x}\in{}{\rm ker}_{\Delta{}}^{\perp}$。也就是闭子空间和它的正交补张成整个希尔伯特空间。所以
$$
\begin{eqnarray}
\mathcal{H}
={\rm ker}_{\Delta{}}\oplus{}{\rm ker}^{\perp{}}_{\Delta{}}
\end{eqnarray}
$$
这一结论对于任意度规为正定的希尔伯特空间显然都成立。还要注意到，由于一个空间正交补中任何一个柯西序列的极限与原空间正交，所以正交补一定是闭集。

前面推导过 ${\rm ker}_{\Delta{}}={\rm ker}_{{\rm d}}\cap_{}^{}{\rm ker}_{\mathfrak{d}}$，所以
$$
\begin{eqnarray}
{\rm ker}_{\Delta{}}^{\perp{}}
=({\rm ker}_{{\rm d}}\cap_{}^{}{\rm ker}_{\mathfrak{d}})^{\perp{}}
\end{eqnarray}
$$
考虑到正交补空间一定是闭集，所以
$$
\begin{eqnarray}
{\rm ker}_{\Delta{}}^{\perp{}}
=\overline{{\rm ker}^{\perp{}}_{{\rm d}}\oplus{\rm ker}^{\perp{}}_{\mathfrak{d}}}
\end{eqnarray}
$$
取闭包的原因是正交补必须是闭集。然后找出这些算子核的正交补，先找它们的 kernal，$\forall{}\alpha{}\in{}{\rm ker}_{{\rm d}}$，由于
$$
\begin{eqnarray}
\langle{}{\rm d}\alpha{},\beta{}\rangle{}
&=&\langle{}\alpha{},\mathfrak{d}\beta{}\rangle{}
\end{eqnarray}
$$
所以 ${\rm ker}_{{\rm d}}\perp{}{\rm im}_{\mathfrak{d}}$，因此 ${\rm im}_{\mathfrak{d}}\subset{}{\rm ker}_{{\rm d}}^{\perp{}}$，以及 ${\rm ker}_{{\rm d}}\subset{}{\rm im}_{\mathfrak{d}}^{\perp{}}$。$\forall{}x\in{}{\rm im}_{\mathfrak{d}}^{\perp{}}$，$\alpha{}\in{}\mathcal{H}$ ，都有
$$
\begin{eqnarray}
0&=&\langle{}\mathfrak{d}\alpha{},x\rangle{}
\nonumber\\
&=&\langle{}\alpha{},{\rm d}x\rangle{}
\end{eqnarray}
$$
由于 $\alpha{}$ 是任意的，所以这意这 $x\in{}{\rm ker}_{{\rm d}}$。也就是 ${\rm ker}_{{\rm d}}={\rm im}_{\mathfrak{d}}^{\perp{}}$。从而就得到
$$
\begin{eqnarray}
{\rm ker}_{{\rm d}}^{\perp{}}
=\overline{{\rm im}}_{\mathfrak{d}}
\end{eqnarray}
$$
所以有
$$
\begin{eqnarray}
{\rm ker}_{\Delta{}}^{\perp{}}
=\overline{{\rm im}}_{\mathfrak{d}}\oplus{}\overline{{\rm im}}_{{\rm d}}
\end{eqnarray}
$$
也就最终得到
$$
\begin{eqnarray}
\mathcal{H}
=\overline{{\rm im}}_{\mathfrak{d}}\oplus{}\overline{{\rm im}}_{{\rm d}}\oplus{}{\rm ker}_{{\rm \Delta{}}}
\end{eqnarray}
$$
这并不是标准的 hoge 分解，因为右边两个闭包没有被摘掉，且 ${\rm ker}_{\Delta{}}$ 的性质也没有被分析清楚。

有了这个分解，可以证明如果一个流形的里奇曲率是正定的，那么该流形上不存在非零的光滑调和一形式。先计算 $\Delta{}$ 作用到光滑形式场上的具体形式
$$
\begin{eqnarray}
\Delta{}\alpha{}
&=&-{\rm d}_{\mu{}_{1}}\nabla_{}^{\mu{}_{0}}\alpha{}_{\mu{}_{0}\mu{}_{2}...\mu{}_{k}}
-\nabla_{}^{\mu{}_{0}}{\rm d}_{\mu{}_{0}}\alpha{}_{\mu{}_{1}...\mu{}_{k}}
\nonumber\\
&=&-kg^{\mu{}_{0}\nu{}_{0}}\nabla_{[\mu{}_{1}}\nabla_{|\nu{}_{0}}\alpha{}_{\mu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
-(k+1)g^{\mu{}_{0}\nu{}_{0}}\nabla_{\mu{}_{0}}\nabla_{[\nu{}_{0}}\alpha{}_{\mu{}_{1}...\mu{}_{k}]}
\nonumber\\
&=&-kg^{\mu{}_{0}\nu{}_{0}}\nabla_{[\mu{}_{1}}\nabla_{|\nu{}_{0}}\alpha{}_{\mu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
-g^{\mu{}_{0}\nu{}_{0}}\nabla_{\mu{}_{0}}\nabla_{\nu{}_{0}}\alpha{}_{\mu{}_{1}...\mu{}_{k}}
+kg^{\mu{}_{0}\nu{}_{0}}\nabla_{\mu{}_{0}}\nabla_{[\mu{}_{1}}\alpha{}_{|\nu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
\nonumber\\
&=&-g^{\mu{}_{0}\nu{}_{0}}\nabla_{\mu{}_{0}}\nabla_{\nu{}_{0}}\alpha{}_{\mu{}_{1}...\mu{}_{k}}
-kg^{\mu{}_{0}\nu{}_{0}}[\nabla_{[\mu{}_{1}},\nabla_{|\mu{}_{0}}]\alpha{}_{\nu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
\nonumber\\
&=&-\nabla_{\mu{}}\nabla_{}^{\mu{}}\alpha{}
-kg^{\mu{}\nu{}}R_{[\mu{}_{1}|\mu{}\nu{}|}{}^{\mu{}_{0}}\alpha{}_{\mu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
\nonumber\\
&=&-\nabla_{\mu{}}\nabla_{}^{\mu{}}\alpha{}
+kR_{[\mu{}_{1}}{}^{\mu{}_{0}}\alpha{}_{|\mu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
\end{eqnarray}
$$
因此在 $\Lambda{}$ 上有
$$
\begin{eqnarray}
\Delta{}
=-\nabla_{}^{2}
+\mathcal{R}
\end{eqnarray}
$$
其中
$$
\begin{eqnarray}
\mathcal{R}\alpha{}
=:kR_{[\mu{}_{1}}{}^{\mu{}_{0}}\alpha{}_{|\mu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
\end{eqnarray}
$$
这是因为如果 $\omega{}$ 是光滑调和一形式，那么
$$
\begin{eqnarray}
0&=&\langle{}\Delta{}\omega{},\omega{}\rangle{}
\nonumber\\
&=&-\int_{M}^{}\omega{}^{\mu{}}\nabla_{\nu{}}\nabla^{\nu{}}\omega{}_{\mu{}}
+\omega{}^{\mu{}}R_{\mu{}}{}^{\nu{}}\omega{}_{\nu{}}
\nonumber\\
&=&\int_{M}^{}(\nabla_{\mu{}}\omega{}_{\nu{}})
(\nabla^{\mu{}}\omega{}^{\nu{}})
+R^{\mu{}\nu{}}\omega{}_{\mu{}}\omega{}_{\nu{}}
\end{eqnarray}
$$
如果 $R_{\mu{}\nu{}}$ 是正定的，那么上面两项都是正定的，只有 $\omega{}$ 为零的时候等号才可以取等。因此对于这种流形，光滑一形式可以唯一的被分解为
$$
\begin{eqnarray}
\alpha{}_{\mu{}}
={\rm d}_{\mu{}}f
+\mathfrak{d}^{\nu{}}\beta{}_{\nu{}\mu{}}
\end{eqnarray}
$$
特别的，对于二球面来说，它满足曲率为正，且球面上的二形式一定正比于体元，因此球面上的一个光滑一形式场一定可以分解成
$$
\begin{eqnarray}
\alpha{}_{\mu{}}
&=&{\rm d}_{\mu{}}f
-q^{\nu{}\sigma{}}\nabla_{\sigma{}}g\varepsilon{}_{\nu{}\mu{}}
\nonumber\\
&=&{\rm d}_{\mu{}}f
-q^{\nu{}\sigma{}}\varepsilon{}_{\nu{}\mu{}}\nabla_{\sigma{}}g
\nonumber\\
&=&{\rm d}_{\mu{}}f
+\varepsilon{}_{\mu{}}{}^{\nu{}}{\rm d}_{\nu{}}g
\end{eqnarray}
$$
^thm-hoge
# 毛球定理
接下来证明在偶数维的球面上没有处处非零的切矢量场，也就是毛球定理。

首先，对于一个微分同胚映射来说，由于切矢的像等于像的切矢，所以如果对一个一般的维数为 $n$ 球形几何有一个处处非零的矢量场，存在一个它们和 $n+1$ 维欧氏空间中的一个单位 $S^{2n}$ 的微分同胚映射 $\phi{}$，$\phi{}$ 复合它们的每一个积分曲线则得到 $S^{n}$ 上的一个曲线，且全体这些曲线的切矢形成的矢量场就是原矢量场的像。显然这个矢量场也要处处非零。

 $\mathbb{R}^{n+1}$ 有天然的内积，该内积在单位球上诱导标准的球面度规，从而为球面上任意点的切空间提供一个度量使之成为内积空间，下面使用的所有内积都是这俩意义下的内积。使用这个度量可以把积分曲线的切矢全部重参数化为范数为一的切矢 $v^{\mu{}}$。不妨在 $\mathbb{R}^{n+1}$ 上选定标准的极坐标系 $(r,\theta{}^{1},...,\theta{}^{n-1},\phi{})$ ，由于假设 $v^{\mu{}}$ 处处非零，所以可以在球面上全局定义一个映射
 $$
\begin{eqnarray}
H:S^{2n}\times{}[0,\pi{}]
\rightarrow{}\mathbb{R}^{2n+1}
\nonumber\\
r^{\mu{}}
\mapsto{}r^{\mu{}}cost
+v^{\mu{}}si nt
\end{eqnarray}
$$
（之所以可以把坐标 $r^{\mu{}}$ 和矢量 $v^{\mu{}}$ 相加是因为欧式空间可以把一点的切空间和原欧式空间认同）由于 $v^{\mu{}}$ 躺在球面上，所以有
$$
\begin{eqnarray}
r^{\mu{}}v_{\mu{}}
=0
\end{eqnarray}
$$
因此可以计算
$$
\begin{eqnarray}
H^{\mu{}}(r)H_{\mu{}}(r)
&=&r^{\mu{}}r_{\mu{}}cos^{2}t
+v^{\mu{}}v_{\mu{}}si n^{2}t
\nonumber\\
&=&cos^{2}t
+si n^{2}t
\nonumber\\
&=&1
\end{eqnarray}
$$
所以该映射其实是一个从球面到球面的映射，因此是一个球面上的同伦。如果从球面上一点 $p^{\mu{}}$ 开始让该映射作用，则 $t=0$ 是像点为 $p^{\mu{}}$，$t=2\pi{}$ 时像点为 $-p^{\mu{}}$。也就该同伦的元素包括恒等映射和对径映射。

设
$$
\begin{eqnarray}
f:M\rightarrow{}N
\end{eqnarray}
$$
是一个同维流形之间的映射，则定义它的度为
$$
\begin{eqnarray}
{\rm deg}(f)
:=\int_{M}^{}{\rm det}({\rm d}f)
\end{eqnarray}
$$
注意两个流形之间映射的微分就是这两个流形之间的雅可比，被积分的行列式就是雅可比的行列式，且由于矢量场可以被流形间的映射推前，所以微分也就是雅可比是在 $M$ 上坐标无关定义的。下面证明如果 $M$ 是一个无边流形，则一个单参映射
$$
\begin{eqnarray}
F:M\times{}[0,1]\rightarrow{}N
\nonumber\\
(p,t)\mapsto{}F_{t}(p)
\end{eqnarray}
$$
的度是不变的。首先 $F$ 的定义域是一个积流形，也就是
$$
\begin{eqnarray}
X:=M\times{}[0,1]
\end{eqnarray}
$$
是一个流形，注意到由于假设 $M$ 是无边的，所以该流形只在 $t=0$ 和 $t=1$ 处有两个边。设 $\omega{}$ 是 $N$ 上的体元，由于形式场可以拉回。所以可以在 $X$ 上执行积分
$$
\begin{eqnarray}
\int_{X}^{}{\rm d}(F^{*}\omega{})
&=&\int_{\partial{}X}^{}F^{*}\omega{}
\nonumber\\
&=&\int_{M\times{}\{1\}}^{}F^{*}\omega{}
-\int_{M\times{}\{0\}}^{}F^{*}\omega{}
\end{eqnarray}
$$
由于拉回映射和外微分可以交换，所以上式左侧可以改写为体元外微分的拉回，又由于体元是 $N$ 上的满形式，因此其外微分为零。所以得到
$$
\begin{eqnarray}
\int_{M\times{}\{1\}}^{}F^{*}\omega{}
=\int_{M\times{}\{0\}}^{}F^{*}\omega{}
\end{eqnarray}
$$
同时由于形式场和它对偶的积分一致，所以上式左右两侧其实就是 $F_{0}$ 和 $F_{t}$ 的雅可比的积分，也就是 $F_{0}$ 和 $F_{t}$ 的度。又由于参数化 $t$ 是任意的，所以如果 $M$ 是一个无边流形，则它到任何同维流形的单参映射的度是不变的。

回到球面上的情况，$H$ 是球面到它自己的一个单参映射，而球面自然是无边的，所以 $H_{t}$ 的度与 $t$ 无关。又因为单位映射和对径映射都在 $H$ 中，所以这两个映射的度应该一致。也就是对径点体元拉回原点后应该给出一致的坐标雅可比。由于已经选择了一个坐标系，可以在该坐标系下展开半径为 $r$ 处的球面上的度规
$$
\begin{eqnarray}
{\rm d}s^{2}|_{S^{n}}
&=&r^{2}{\rm d}\Omega{}^{2}_{n}
\end{eqnarray}
$$
其中 $\Omega{}^{2}_{n}$ 是单位球上的线元。然后它的适配体元给出的雅可比为
$$
\begin{eqnarray}
\sqrt{ {\rm det}(r^{2}{\rm d}\Omega{}^{2}) }
&=&\sqrt{ r^{2n}{\rm det}({\rm d}\Omega{}^{2}) }
\nonumber\\
&=&r^{n}\sqrt{ {\rm det}({\rm d}\Omega{}^{2}) }
\end{eqnarray}
$$
所以球面体元为
$$
\begin{eqnarray}
r^{n}\sqrt{ {\rm det}({\rm d}\Omega{}^{2}) }
{\rm d}\theta{}^{1}\wedge{}...\wedge{}{\rm d}\theta{}^{n-1}\wedge{}{\rm d}\phi{}
\end{eqnarray}
$$
因此在把这个形式场从对径点拉回的时候，就是做了一个该坐标系下球面坐标变换的雅可比，即
$$
\begin{eqnarray}
H_{\pi{}}^{*}r^{n}\sqrt{ {\rm det}({\rm d}\Omega{}^{2}) }
{\rm d}\theta{}'^{1}\wedge{}...\wedge{}{\rm d}\theta{}'^{n-1}\wedge{}{\rm d}\phi{}'
=\frac{ \partial (\theta{}',\phi{}') }{ \partial (\theta{},\phi{}) }r^{n}\sqrt{ {\rm det}({\rm d}\Omega{}^{2}) }
{\rm d}\theta{}^{1}\wedge{}...\wedge{}{\rm d}\theta{}^{n-1}\wedge{}{\rm d}\phi{}
\end{eqnarray}
$$
这里使用了 $\sqrt{{\rm det}({\rm d}\Omega{}^{2})   }$ 在球面上不变的特点。至于球面坐标变换的雅可比，则可以通过欧氏空间坐标变换的雅可比诱导得到，由于
$$
\begin{eqnarray}
H^{*}r
=r
\end{eqnarray}
$$
所以
$$
\begin{eqnarray}
H^{*}{\rm d}r
={\rm d}r
\end{eqnarray}
$$
因此限制在球面上发生的微分同胚变换，欧式空间坐标变换的雅可比完全等于球面坐标变换的雅可比，而对径点变换如果作为欧氏空间上的变换来看，对应着 $-\mathbb{I}$，它的行列式为
$$
\begin{eqnarray}
{\rm det}(-\mathbb{I}^{n+1})
&=&(-1)^{n+1}
\end{eqnarray}
$$
所以在该坐标系下球面上拉回体元与原体元的行列式之比为  $(-1)^{n+1}$。这导致当 $n$ 为偶数的时候 $1$ 和 $-1$ 给出符号不同的度，和前面的推导矛盾。因此球面上的恒等映射和对径映射并不是同伦的，也就是前面构造的同伦映射是不存在的，等价于 $v^{\mu{}}$ 是不能处处被归一化的，又由于球面度规是正定的，所以只能是 $v^{\mu{}}$ 不能处处非零。 ^thm-maoqiu

