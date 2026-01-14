希望只用几何、拓扑、代数的方法证明一下 Hoge 分解定理和毛球定理，这俩定理在引力与相对论文件夹中的局域视界笔记中被用到。但是第一个定理尝试失败了，第二个可以证明。
# Hoge 分解定理
对于一个紧致无边的定向黎曼流形 $(M,g_{\mu{}\nu{}})$，设 $\Lambda{}^{k}$ 是它的 $k-$形式空间。在 $\Lambda{}^{k}$ 上定义内积
$$
\begin{eqnarray}
\langle{}\alpha{},\beta{}\rangle{}_{k}
:=\frac{1}{k!}\int_{M}^{}\alpha{}\cdot{}\beta{}
\end{eqnarray}
$$
其中缩并 $\cdot{}$ 由度规执行。容易看出来这确实是一个内积。然后定义余外微分算子 $\mathfrak{d}$ 为 ${\rm d}$ 的伴随，即
$$
\begin{eqnarray}
\langle{}f,\mathfrak{d}\alpha{}\rangle{}_{k}
:=\langle{}{\rm d}f,\alpha{}\rangle{}_{k+1}
\end{eqnarray}
$$
 研究一下它的具体作用
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
=-\nabla_{}\cdot{}\alpha{}
\end{eqnarray}
$$
由 $\mathfrak{d}$ 的性质可以看到，$\mathfrak{d}\mathfrak{d}=0$。可以用
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
则有
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
对于伪黎曼几何，上式为零不意味着做内积的元素为零，但是对于黎曼几何，上式为零一定等价于
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
在证明 Hoge 分解前，先分析一下 $\Delta{}$ 的性质，首先，根据 $\mathfrak{d}$ 的定义可以知道
$$
\begin{eqnarray}
\langle{}\alpha{},\Delta{}\beta{}\rangle{}
=\langle{}\Delta{}\alpha{},\beta{}\rangle{}
\end{eqnarray}
$$
所以 $\Delta{}$ 是自伴的。然后看一下它的具体形式
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
因此
$$
\begin{eqnarray}
\Delta{}
=-\nabla_{}^{2}
+k\mathcal{R}
\end{eqnarray}
$$
其中
$$
\begin{eqnarray}
\mathcal{R}\alpha{}
=:R_{[\mu{}_{1}}{}^{\mu{}_{0}}\alpha{}_{|\mu{}_{0}|\mu{}_{2}...\mu{}_{k}]}
\end{eqnarray}
$$
对于一个微分算子 $P$ 来说，提取它的偏导数的最高阶项，然后把这一项中所有的偏导数替换为一个指定的矢量 $v^{\mu{}}$ 所得到的关于 $v^{\mu{}}$ 的多项式矩阵叫做 $P$ 关于 $v$ 的主象征，记为 $\sigma{}_{P}(v)$。称算子 $P$ 是椭圆的，如果 $\forall{}v\neq0$，有 $\sigma{}_{P}(v)$ 是可逆的。
检查 $\Delta{}$，它的最高次的偏导数部分为
$$
\begin{eqnarray}
-g^{\mu{}\nu{}}\partial{}_{\mu{}}\partial{}_{\nu{}}
\end{eqnarray}
$$
替换为任意的非零矢量后为
$$
\begin{eqnarray}
-v_{\mu{}}v^{\mu{}}\neq0
\end{eqnarray}
$$
其中不为零依旧是用了黎曼度规的正定性。所以 $\Delta{}$ 是椭圆的，因此 $\Delta{}$ 是自伴椭圆算符。根据 Fredholm 理论，这类算子有以下特征
1. 核是有限维的
2. 存在唯一一个格林算子 $G$ ，满足
$$
\begin{eqnarray}
I
=\Delta{}G
+P_{H}
\end{eqnarray}
$$
其中 $P_{H}$ 是到 ${\rm ker}(\Delta{})$ 的正交投影算子，且算子 $G$ 和 ${\rm d}$、$\mathfrak{d}$ 可交换。
因此，对于任何一个形式场 $\alpha{}$，都有
$$
\begin{eqnarray}
\alpha{}
&=&\Delta{}G\alpha{}
+P_{H}\alpha{}
\nonumber\\
&=&{\rm d}\mathfrak{d}G\alpha{}
+\mathfrak{d}{\rm d}G\alpha{}
+P_{H}\alpha{}
\end{eqnarray}
$$
也就是任何一个形式场，都可以被分解为恰当部分、余恰当部分和调和部分。

可以证明如果一个流形的里奇曲率是正定的，那么该流形上不存在非零的调和一形式。这是因为如果 $\omega{}$ 是调和一形式，那么
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
如果 $R_{\mu{}\nu{}}$ 是正定的，那么上面两项都是正定的，只有 $\omega{}$ 为零的时候等号才可以取等。因此对于这种流形，一形式可以唯一的被分解为
$$
\begin{eqnarray}
\alpha{}_{\mu{}}
={\rm d}_{\mu{}}f
+\mathfrak{d}^{\nu{}}\beta{}_{\nu{}\mu{}}
\end{eqnarray}
$$
特别的，对于二球面来说，它满足曲率为正，且球面上的二形式一定正比于体元，因此球面上的一个形式场一定可以分解成
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
所以在该坐标系下球面上拉回体元与原体元的行列式之比为  $(-1)^{n+1}$。这导致当 $n$ 为偶数的时候 $1$ 和 $-1$ 给出符号不同的度，和前面的推导矛盾。因此球面上的恒等映射和对径映射并不是同伦的，也就是前面构造的同伦映射是不存在的，等价于 $v^{\mu{}}$ 是不能处处被归一化的，又由于球面度规是正定的，所以只能是 $v^{\mu{}}$ 不能处处非零。

