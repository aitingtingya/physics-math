# 量子构型空间
给定一个光滑的联络场 $A^{i}_{a}\in{}\mathfrak{A}$ 和支撑集为紧集的解析曲线 $c:[0,1]\rightarrow{}\Sigma{}$，对应的和乐是平移方程
$$
\begin{equation}
\frac{d}{dt}A(c,t)=-[A^{i}_{a}\dot{c}^{a}\tau{}_{i}]A(c,t)
\end{equation}
$$
的初值为 $1$ 的解，其中 $t$ 是曲线参数，$\dot{c}^{a}$ 是曲线切矢，$\{\tau{}_{i}\}$ 是对应于嘉当度规的满足 $[\tau{}_{i},\tau{}_{j}]=\epsilon{}^{k}_{ij}\tau{}_{k}$ 的预选的正交基矢。根据定义，显然每一个和乐都是群 $SU(2)$ 的群元，解为
$$
\begin{equation}
A(c,t)=\mathcal{P}exp(-\int_{0}^{t}[A^{i}_{a}\dot{c}^{a}\tau{}_{i}]dt)
\end{equation}
$$
设 $c_{1}、c_{2}$ 是两段相连的解析曲线，则 $A(c_{1}\circ{}c_{2})=A(c_{1})A(c_{2})$，$A(c^{-1})=A(c)^{-1}$。称两段解析曲线 $c、c'$ 是等价的，若它们具有相同的起点 $s(c)$ 和终点 $t(c)$ ，且 $A(c)=A(c')，\forall{}A^{i}_{a}\in{}\mathfrak{A}$。一个解析曲线的等价类称为一条**边**，多条边首尾相连组成的元素叫**分段解析曲线**。把所有具有紧支撑集的分段解析曲线的集合记作 $\mathscr{P}$。以 $\Sigma{}$ 上所有点为对象，把每条边 $e$ 看作从对象 $s(e)$ 到对象 $t(e)$ 的态射，则显然它们满足结合律且有恒等态射（独点边），所有起点为 $s(e)$，终点为 $t(e)$ 的分段解析曲线的集合构成这两个点之间的态射全体 ${\rm Hom}(s(e),t(e))$，因此 $\mathscr{P}$ 成为一个**范畴**。还可以验证所有 ${\rm Hom}$ 的并是一个集合，也就是全体态射成为一个集合，从而这是一个**小范畴**。又因为所有态射可逆，所以 $\mathscr{P}$ 事实上成为一个**群胚**。
![[Loop 1 2024-06-22 15.30.52.excalidraw]]
如图，由于
$$
\eta{}_{0}(0)=A(c)^{-1}\eta{}_{1}(0)=g(s(c))\sigma{}_{0}(0)=g(s(e))A’(e)^{-1}\sigma{}_{1}(0)=g(s(e))A’(e)^{-1}g(t(e))^{-1}\eta{}_{1}(0);
$$
所以在由 $SU(2)$ 值函数 $g:\Sigma{}\rightarrow{}SU(2)$ 生成的内部规范变换和空间微分同胚变换 $\varphi{}:\Sigma{}\rightarrow{}\Sigma{}$ 下有 $A'(e)=g(t(e))^{-1}A(e)g(s(e))$ 和 $A'(e)=A(\varphi{}\circ{}e),\forall{}e\in{}\mathscr{P}$。
量子构型空间 $\bar{\mathfrak{A}}$ 定义为从 $\mathscr{P}$ 到 $SU(2)$ 群的所有量子联络 $A$ 的集合，要求 $\forall{}A\in{}\bar{\mathfrak{A}}$，$\forall{}e\in{}\mathscr{P}$，$A(e)$ 按主丛的转换函数进行变换，且
$$
\begin{equation}
A(e_{1}\circ{}e_{2})
=A(e_{1})A(e_{2})
\qquad
A(e^{-1})
=A(e)^{-1}
\end{equation}
$$
其中等号右边使用群的乘法和逆元。
做下列定义：
1. 称边的有限集 $E=\{e_{1},…e_{N}\}$ 是独立的，如果 $\forall{}e_{i},e_{j}\in{}E$ 只能在起点和终点相交。
2. 称边的独立有限集和它们的顶点为一个**图** $\gamma{}$。$\gamma{}$ 的独立边的有限集记做 $E(\gamma{})$，顶点的集合记做 $V(\gamma{})$，$N_{\gamma{}}$ 表示 $E(\gamma{})$ 的元素个数。
3. 给定一个图 $\gamma{}$，上面可能的所有分段解析路径及它们的逆路径可以生成 $\mathscr{P}$ 的一个子群胚 $\alpha{}(\gamma{})$，叫做 **$tame$ 子群胚**。也就是 $\alpha{}(\gamma{})$ 独立于 $\gamma{}$ 上边的定向。一个 $tame$ 子群胚 $\alpha{}$ 配以定向可以还原出一个图 $\gamma{}$，被还原出的图 $\gamma{}$ 的 $E(\gamma{})$ 中元素个数记做 $N_{\alpha{}}$。
4. $\mathscr{P}$ 中所有的 $tame$ 子群胚记做 $\mathcal{L}$。

在 $\mathcal{L}$ 上配以偏序，也就是若 $\alpha{},\alpha{}’\in{}\mathcal{L}$，定义 $\alpha{}\prec{}\alpha{}’$ 若 $\alpha{}$ 是 $\alpha{}’$ 的子群胚。可以定义子群胚的量子构型空间
$$
\begin{equation}
\bar{\mathfrak{A}}_{\alpha{}}:={\rm Hom}(\alpha{},SU(2))
\end{equation}
$$
由于量子构型空间是从支撑集到规范群的映射，对于作用域相同的映射来说，映射可以由作用到作用域上每一个元素的结果唯一的定义，所以 $A_{\alpha{}}\in{}\bar{\mathfrak{A}}_{\alpha{}}(\alpha{}=\alpha{}(\gamma{}))$ 由 $\{A_{e}|e\in{}E(\gamma{})\}$ 唯一的确定。因此一条边上的所有量子联络的集合其实等价于规范群，而群胚上的量子联络等价于所有独立边作为规范群的直积。也就是 $\exists{}\lambda{}:\bar{\mathfrak{A}}_{\alpha{}}\rightarrow{}SU(2)^{N_{\alpha{}}}$ 为双射并在 $\bar{\mathfrak{A}}_{a}$ 上诱导一个拓扑 s.t. $\lambda{}$ 成为一个拓扑同胚。
对于 $a\prec{}\alpha{}’$，定义投影映射
$$
\begin{eqnarray}
P_{\alpha{}’\alpha{}}:\bar{\mathfrak{A}}_{\alpha{}’}\rightarrow{}\bar{\mathfrak{A}}_{\alpha{}}
\nonumber\\
A_{\alpha{}’}\mapsto{}A_{\alpha{}’}|_{\alpha{}}
\end{eqnarray}
$$
这会让一些 $\bar{\mathfrak{A}}_{\alpha{}'}$ 上的量子联络被模为 $\bar{\mathfrak{A}}_{\alpha{}}$ 上的同一个联络。显然投影映射是满射，且满足一致性条件，也就是
$$
\begin{equation}
P_{\alpha{}'\alpha{}}\circ{}P_{\alpha{}''\alpha{}'}
=P_{\alpha{}''\alpha{}}
\end{equation}
$$
下面说明投影映射是连续的。根据乘积拓扑的定义，$\bar{\mathfrak{A}}_{\alpha{}}$ 上的开集等于 $N_{\alpha{}}$ 个 $SU(2)$ 拓扑空间开集的所有可能的笛卡尔积。对于映射 $P_{\alpha{}'\alpha{}}$ 来说，因为它是满射，所以整个 $\bar{\mathfrak{A}}_{\alpha{}}$ 都是它的像，在上面取任何一个开集 $O_{\alpha{}}$，则逆像等于 $O_{\alpha{}}\times{}\bar{\mathfrak{A}}_{\alpha{}'-\alpha{}}$，由于每一个 $SU(2)$ 拓扑空间本身是开集，所以它们的笛卡尔积 $\bar{\mathfrak{A}}_{\alpha{}'-\alpha{}}$ 是开集，所以 $O_{\alpha{}}\times{}\bar{\mathfrak{A}}_{\alpha{}'-\alpha{}}$ 是开集。因此投影映射是连续的。

由于定义子群胚的量子构型空间的时候，各个子群胚的构型空间是独立定义的，为了把它们关联起来，可以使用投影映射来定义投影极限，也就是投影族 $\{\bar{\mathfrak{A}}_{\alpha{}}P_{\alpha{}’\alpha{}}\}_{\alpha{}\prec{}\alpha{}’}$ 的**投影极限** ${\rm lim}_{\alpha{}}(\bar{\mathfrak{A}}_{\alpha{}})\in{}\bar{\mathfrak{A}}_{\infty}:=\prod_{_{\alpha{}\in{}\mathcal{L}}}^{}\bar{\mathfrak{A}}_{\alpha{}}$ 定义为
$$
\begin{equation}
{\rm lim}_{\alpha{}}(\bar{\mathfrak{A}}_{\alpha{}}):=\{\{A_{\alpha{}}\}_{\alpha{}\in{}\mathcal{L}}|P_{\alpha{}’\alpha{}}A_{\alpha{}’}=A_{\alpha{}},\forall{}\alpha{}\prec{}\alpha{}’\}
\end{equation}
$$
这个投影不是平凡的，假如最大有两条边，规范群为有限群 $G$，元素为则可以有两个构型空间 $\bar{\mathfrak{A}}_{\alpha{}_{1}}$ 和 $\bar{\mathfrak{A}}_{\alpha{}_{2}}$，其中 $\alpha{}_{1}\prec{}\alpha{}_{2}$。则它们的直积空间是 $G^{3}$，元素个数为 $o(G)^{3}$。但是按照投影极限，由于最大的子群胚，也就是 $\bar{\mathfrak{A}}_{\alpha{}_{2}}$ 中的一个元素给出投影极限中的一个元素，所以投影极限的拓扑是和 $\bar{\mathfrak{A}}_{\alpha{}_{2}}$ 的一样的，元素为 $o(G)^{2}$ 个。显然， $\bar{\mathfrak{A}}_{\infty}$ 以 $\bar{\mathfrak{A}}_{\alpha{}}$的乘积拓扑（称为 $Tychonov$ 拓扑）成为豪斯道夫拓扑空间。而量子构型空间，因为存在双射
$$
\begin{eqnarray}
\Phi{}:\bar{\mathfrak{A}}\rightarrow{}{\rm lim}_{\alpha{}}(\bar{\mathfrak{A}}_{\alpha{}})
\nonumber\\
A\mapsto{}\{A|_{\alpha{}}\}_{\alpha{}\in{}\mathcal{L}}
\end{eqnarray}
$$
而被投影极限上 $SU(2)$ 的乘积拓扑而诱导 $\bar{\mathfrak{A}}$ 成为豪斯道夫空间。
# 柱函数与运动学希尔伯特空间
## 度规和赋范线性空间
## 度规空间
定义集合 $M$ 和 $M\times{}M$ 上的一个满足下述要求的实值函数 $d(\cdot{},\cdot{})$ 构成一个**度规空间**：
1. $d(x,y)\geq{}0$;
2. $d(x,y)=0\leftrightarrow{}x=y$;
3. $d(x,y)=d(y,x)$;
4. $d(x,z)\leq{}d(x,y)+d(y,z)$。
其中函数 $d$ 称为 $M$ 上的**度规**。

称度规空间 $<M,d>$ 的元素序列 $\{x_{n}\}_{n=1}^{\infty}$ 收敛于 $x\in{}M$，如果 $d(x,x_{n})\rightarrow{}0$, $n\rightarrow{}\infty$。这里趋于零的意思是 $\mathbb{R}$ 上的柯西收敛。记作$\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}x_{n}=x$。进一步的，称 $c\in{}M$ 是 $E\subset{}M$ 的一个**聚点**或**极限点**或**簇点**，若 
$$
\begin{equation}
(\forall{}\varepsilon{}\in{}R^{+})
,
(\exists{}a\in{}E) 
\rm{s.t.}
a\neq c,d(a,c)<\varepsilon{}
\end{equation}
$$
因为存在即可，所以 $E$ 中所有元素不需要都靠近它的极限点，比如 $(R,|\cdot{}-\cdot{}|)$（其中两个竖线指绝对值符号），则 $2$ 是 $(0,2)\cup^{}_{}\{3\}$ 的聚点。聚点的一个等价定义为 $\exists{}\{x_{k}\}_{k=1}^{\infty}{}_{x_{k}\neq x_{k'},k\neq k'}\subset{}E$，s.t. $\mathop{{\rm lim}}\limits_{k\rightarrow{}\infty}^{}x_{k}=x$。这是比较好证明的，首先为了构造这样的序列， $E$ 必须有无穷元素，由于极限点的定义要求 $a\neq c$，所以如果 $E$ 是一个有限元素的集合，$x \in{}E-\{c\}$ 总存在一个 $d(x,c)$ 的下限，导致无法满足极限点的定义，因此如果 $E$ 要存在极限点，它就必须是无穷元素的集合。然后根据收敛的定义，任意小的数总有一个 $n_{0}$ 后面的点距离 $x_{0}$ 的距离比这个数小，所以 $x_{0}$ 就是一个聚点。度规空间 $<M,d>$ 中的元素序列 $\{x_{n}\}$ 称为**柯西序列**，如果
$$
\begin{equation}
(\forall{}\varepsilon{}>0)(\exists{}N)n,m>N\rightarrow{}d(x_{n},x_{m})<\varepsilon{}
\end{equation}
$$
 对于收敛序列来说，对于 $\forall{}\varepsilon{}>0$，$\exists{}N$ 使得 $\forall{}n>N$ 有 $d(x_{n},x_{0})<\frac{\varepsilon{}}{2}$ ，因此 $\forall{}n,m>N$，有
$$
\begin{equation}
d(x_{n},x_{m})
\leq{}d(x_{n},x_{0})+d(x_{m},x_{0})
<\varepsilon{}
\end{equation}
$$
所以任何收敛序列都是柯西的。反过来，如果序列 $\{x_{n}\},x_{n}\neq x_{0}$ 是度规空间 $<X,d>$ 上的一个收敛到 $x_{0}$ 的序列，容易看到 $<X-\{x_{0}\},d>$ 依旧是一个度规空间，但是此时序列 $\{x_{n}\}$ 只是一个柯西序列，却由于在 $X$ 上没有收敛值而不收敛。称所有柯西序列都收敛的度规空间叫**完备度规空间**。
根据聚点和柯西序列的定义，聚点的等价定义中构造的那个序列因为收敛，所以就是一个柯西序列。

对于一个完备的度规空间来说，由于它的一个有界的无穷集合一定有柯西序列，因此一定有收敛序列，所以完备的度规空间中的有界无穷集合必有聚点，聚点就是收敛序列的收敛值。（但是聚点是否在该空间内就不知道了）。对于完备度规空间中只有一个聚点的有界无穷集合，在剔除收敛向聚点的子序列后，剩下的点构造一个序列，如果是有限序列则无论它们是什么值，与被剔除的序列可以粘贴为一个收敛序列，收敛值为聚点。如果这个序列是无限的，则其中的点作为一个集合依旧是有界无穷集合，还会有至少一个聚点，由于已经剔除了收敛向原集合的聚点的序列，所以新聚点与原聚点不同，这与只有一个聚点矛盾。因此只有一个聚点的有界无穷集合整体是收敛的。

有了度规后可以给集合 $X$ 诱导出一个拓扑，也就是**度规拓扑**。用度规定义的开球即可定义该拓扑的基，也就是假如
$$
\begin{equation}
B_{d}(x,\varepsilon{})
=\{y\in{}M
|d(x,y)
<\varepsilon{}\}
\end{equation}
$$
是 $x \in{}M$ 的一个 $\varepsilon{}$ 开球，则定义 $U\subset{}M$ 是开集，当且仅当
$$
\begin{equation}
(\forall{}x \in{}U)
(\exists{}\varepsilon{}>0)
[B_{d}(x,\varepsilon{})
\subset{}U]
\end{equation}
$$
由于 $\mathbb{R}$ 上自然拓扑的性质，显然上面定义符合开集的性质。把所有的开集收集在一起记做 $\mathscr{T}_{d}$，则 $(M,\mathscr{T}_{d})$ 成为一个拓扑空间。称集合 $V\subset{}M$ 是 $x \in{}M$ 的邻域，如果 $\exists{}U\in{}\mathscr{T}_{d}$，使得 $x \in{}U\subset{}V$，称 $x$ 为 $V$ 的内地。设 $<X,d>$ 是一个度规空间，称集合 $F\subset{}X$ 是闭的，如果它包含自己所有的极限点（注意极限点的定义要求它首先是度规空间中的一个点，所以如果一个度规空间是非完备的，尽管度规空间本身的柯西序列并不全部收敛，但是不妨碍它包括自身的所有极限点）。设 $<X,d>$ 是一个度规空间，则
5. 开集的补集是闭集；
6. 任意集合全部内点的集合是一个开集；
7. 任意集合和它全部极限点的并集是一个闭集，称为该集合的闭包；
8. 一个集合是开的，当且仅当它是它所有内点的邻域。
证明一下这几个陈述，对于全空间和空集陈述满足，下面分析 $M$ 的真子集。设 $O$ 是一个开集，则证明第五条就需要证明 $M-O$ 包含它所有的极限点，等价于它的所有收敛的柯西序列的收敛点都在其中。采用反证法，假如有一个极限点 $x$ 不在其中，则它就必须在 $O$ 中，又由于 $O$ 是一个开集，所以根据定义存在一个截止半径 $\varepsilon{}$ 使得 $B_{d}(x,\varepsilon{})\subset{}O$，因此这个开球不在 $M-O$中，因此 $M-O$ 中无法构造一个柯西序列逼近 $x$，矛盾。至于第五条因为内点的定义就是用开集来定义，所以当然成立。第七条只需要说明极限点的引入所构造的新的柯西序列不会带来新的极限点即可，这是显然的。第八条也很容易证明。

 称集合 $B$ 在度规空间 $M$ 中**稠密**，如果 $\forall{}m\in{}M$ 都是 $B$ 中元素的极限。此时称 $B$ 是$M$ 的**稠密子集**，如果 $M$ 是全空间，称 $B$ 为**稠密集**。
 下面说明一个非完备的度规空间 $<X,d>$ 一定同构于某个完备度规空间的稠密子集。对于空间的所有柯西序列构成的集合记做
$$
\begin{equation}
\mathcal{C}
:=\{\{x_{n}\}_{0}^{\infty}是<X,d>的柯西序列\}
\end{equation}
$$
在这个集合上定义等价关系：也就是称$\{x_{n}\}\in{}\mathcal{C}$ 和 $\{y_{n}\}\in{}\mathcal{C}$ 是等价的，如果
$$
\begin{equation}
\mathop{{\rm lim}}\limits_{n\rightarrow{}0}^{}d(x_{n},y_{n})=0
\end{equation}
$$
记做 $\{x_{n}\}\sim \{y_{n}\}$。显然这一关系具有自反性、对称性、传递性，所以是一个等价关系。定义新的集合 $\hat{X}:=\mathcal{C}/\sim$。其中的元素简记为 $\hat{x}:=|\{x_{n}\}|$接着可以在这个新集合上定义度规，也就是定义
$$
\begin{eqnarray}
\hat{d}:
\hat{X}\times{}\hat{X}
&\rightarrow{}&
\mathbb{R^{\geq{}0}}
\nonumber\\
(\hat{x},\hat{y})
&\mapsto{}&
\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}d(x_{n},y_{n})
\end{eqnarray}
$$
其中极限中可以选取任意的等价类。下面证明这个定义良好且确实是一个度规，首先说明定义中的极限是存在的，也就是证明序列 $\{d(x_{n},y_{n})\}^{\infty}_{0}$ 在 $\mathbb{R}$ 上的极限存在且与等价类选取无关。先简单说明与等价类选取无关，根据三角不等式，有
$$
\begin{eqnarray}
d(x_{n},y_{n})
&\leq{}&
d(x'_{n},y_{n})
+d(x'_{n},x_{n})
\end{eqnarray}
$$
结合等价类的定义，可以得到
$$
\begin{equation}
\mathop{{\rm lim}}_{n\rightarrow{}\infty}
[d(x_{n},y_{n})
-d(x'_{n},y_{n})]
\leq{}0
\end{equation}
$$
由等价类的对称性很容易得到
$$
\begin{equation}
\mathop{{\rm lim}}_{n\rightarrow{}\infty}
[d(x'_{n},y_{n})
-d(x_{n},y_{n})]
\leq{}0
\end{equation}
$$
因此极限与等价类选取无关。
根据三角不等式有
$$
\begin{equation}
d(x_{n},y_{n})
-d(x_{m},y_{m})
\leq{}
d(x_{n},x_{m})
+d(x_{m},y_{n})
-d(x_{m},y_{m})
\end{equation}
$$
进一步的对右式第二项应用三角不等式得
$$
\begin{eqnarray}
d(x_{n},y_{n})
-d(x_{m},y_{m})
\leq{}
d(x_{n},x_{m})
+d(x_{m},y_{m})
+d(y_{n},y_{m})
-d(x_{m},y_{m})
=d(x_{n},x_{m})
+d(y_{n},y_{m})
\end{eqnarray}
$$
所以
$$
\begin{equation}
(\forall{}\varepsilon{}>0)(\exists{}N)(n,m>0)(d(x_{n},x_{m})<\frac{\varepsilon{}}{2},d(y_{n},y_{m})<\frac{\varepsilon{}}{2})
\end{equation}
$$
因此
$$
\begin{equation}
d(x_{n},y_{n})<\varepsilon{}
\end{equation}
$$
所以该极限是存在的。然后说明它是一个度规，首先正定性显然是成立的，然后根据 $\hat{X}$ 的定义可知度规定义的第二条也是满足的，因为等价类被模掉了。至于度规定义第三条当然也成立，然后再检验第四条，由于
$$
\begin{eqnarray}
\hat{d}(\hat{x},\hat{y})
&=&\mathop{{\rm lim}}_{n\rightarrow{}\infty}
d(x_{n},y_{n})
\nonumber\\
&\leq{}&\mathop{{\rm lim}}_{n\rightarrow{}\infty}
[d(x_{n},z_{n})
+d(y_{n},z_{n})]
\nonumber\\
&=&\hat{d}(\hat{x},\hat{z})
+\hat{d}(\hat{y},\hat{z})
\end{eqnarray}
$$
所以三角不等式成立。因此 $<\hat{X},\hat{d}>$ 成为一个度规空间。接下来说明这个度规空间是完备的，也就是所有柯西序列都是收敛的，如果该柯西序列收敛到 $\hat{X}$ 上的某一个元素，则应该有
$$
\begin{equation}
(\exists{}\{x_{n}\}\in{}\mathcal{C})
(\forall{}\varepsilon{}>0)
(\exists{}N>0)
(\forall{}k>N)
[\mathop{{\rm lim}}_{n\rightarrow{}\infty}d(x^{k}_{n},x_{n})
<\varepsilon{}]
\end{equation}
$$
下面说明可以用 $\{x^{k}_{n}\}$ 的元素来构造这样的序列。$\hat{X}$ 中的柯西序列的元素都是 $X$ 中的柯西序列的等价类。对于一个柯西序列 $\{\hat{x}^{k}\}$ 来说，有
$$
\begin{equation}
(\forall{}k>l>0)
(\exists{}\varepsilon{}_{l}>0)
[\hat{d}(\hat{x}^{k},\hat{x}^{l})
<\frac{\varepsilon{}_{l}}{3}]
\end{equation}
$$
上面一串陈述可以得到
$$
\begin{equation}
(\forall{}k>l>0)
(\exists{}\varepsilon{}_{l}
>0)
(\exists{}z_{l}
>0)
(\forall{}n
>z_{l})
[|d(x^{k}_{n},x^{l}_{n})
-\frac{\varepsilon{}_{l}}{3}|<\frac{\varepsilon{}_{l}}{3}]
\end{equation}
$$
也就是
$$
\begin{equation}
(\forall{}k>l>0)
(\exists{}\varepsilon{}_{l}
>0)
(\exists{}z_{l}
>0)
(\forall{}n
>z_{l})
[d(x^{k}_{n},x^{l}_{n})
<\frac{2\varepsilon{}_{l}}{3}]
\end{equation}
$$
又由于 $\{x^{k}_{n}\}$ 是 $X$ 上的柯西序列，所以有陈述
$$
\begin{equation}
(\exists{}N_{k}>0)
(\forall{}m,n>N_{k})
[d(x^{k}_{m},x^{k}_{n})<\frac{\varepsilon{}_{k}}{3}]
\end{equation}
$$
定义
$$
\begin{equation}
y_{1}
=x^{1}_{n_{1}}
\qquad
n_{1}:={\rm max}(z_{1},N_{1})
\qquad
y_{l}
=x^{l}_{n_{l}},\forall{}l>1
\qquad
n_{l}
:={\rm max}(z_{l},N_{l},n_{l-1})
\end{equation}
$$
就可以得到一个序列 $\{y_{k}\}$。对 $\forall{}k>l$ ，这个序列有
$$
\begin{eqnarray}
d(y_{k},y_{l})
&=&
d(x^{k}_{n_{k}},x^{l}_{n_{l}})
\end{eqnarray}
$$
由定义可知 $n_{k}\geq{}n_{l}$，则根据三角不等式有
$$
\begin{eqnarray}
d(y_{k},y_{l})
&\leq&{}d(x^{l}_{n_{k}},x^{l}_{n_{l}})
+d(x^{l}_{n_{k}},x^{k}_{n_{k}})
\nonumber\\
&<&\frac{\varepsilon{}_{l}}{3}
+\frac{2\varepsilon{}_{l}}{3}
\nonumber\\
&=&\varepsilon{}_{l}
\end{eqnarray}
$$
这里 $\varepsilon{}_{l}$ 是一个被 $l$ 标记的数，且它不能任意取，对每一个 $l$ 它有下限。但是根据它的定义可以知道，总可以选择一些 $\mathbb{R}$ 上的序列 $\{\varepsilon{}_{l}\}$ 满足
$$
\begin{equation}
(\forall{}\varepsilon{}>0)
(\exists{}N>0)
(\forall{}k>N)
(\varepsilon{}_{k}<\varepsilon{})
\end{equation}
$$
所以该序列是柯西序列。因此它的等价类 $\hat{y}$ 自然就是 $\hat{X}$ 中的一个元素。然后证明 $\{x^{k}\}$ 收敛到这个元素，根据 $\hat{y}$ 的构造可以有
$$
\begin{eqnarray}
\hat{d}(\hat{x}^{k},\hat{y})
&=&\mathop{{\rm lim}}_{n\rightarrow{}\infty}
d(x^{k}_{n},y_{n})
\nonumber\\
&=&\mathop{{\rm lim}}_{n\rightarrow{}\infty}
d(x^{k}_{n},x^{n}_{n_{n}})
\end{eqnarray}
$$
由于 $n$ 趋于无穷时大于 $k$ 且 $n_{n}\geq{}n$，又因为 $\{x^{k}_{n}\}$ 是柯西序列，所以有
$$
\begin{eqnarray}
\hat{d}(\hat{x}^{k},\hat{y})
&\leq{}&\mathop{{\rm lim}}_{n\rightarrow{}\infty}
d(x^{k}_{n},x^{n}_{n})
+\mathop{{\rm lim}}_{n\rightarrow{}\infty}
d(x^{n}_{n},x^{n}_{n_{n}})
\nonumber\\
&<&\varepsilon{}_{k}
\end{eqnarray}
$$
因此 $\{\hat{x}^{k}\}$ 确实收敛向 $\hat{y}$，所以 $\hat{X}$ 是完备的。由于在 $X$ 中，$\{x_{n}\equiv{}x\}^{\infty}_{n=1}$ 本身也是柯西序列，它的等价类自然是 $\hat{X}$ 中的一个元素，所以存在 $X$ 到 $\hat{X}$ 的自然保度规嵌入 $\iota{}(X)$，所以 $X$ 是 $\hat{X}$ 的一个子空间的稠密子集。下面说明其 $\iota{}(X)$ 是 $\hat{X}$ 的稠密，也就是证明 $\hat{X}$ 中的点都是 $\iota{}(X)$ 中柯西序列的极限。这个证明是非常直接的，因为 $\hat{X}$ 中的元素都是 $X$ 中柯西序列的等价类，所以只需要选择任意 $\hat{x}^{k}\in{}\hat{X}$ 的一个代表元 $\{x^{k}_{n}\}$ ，它是 $X$ 中的一个可惜序列，它的每个元素的无穷常数列也是一个柯西序列，在 $\iota{}(X)$ 中对应一个元素$\hat{x}^{k}_{n}$，则可以构造一个 $\iota{}(X)$ 中的柯西序列 $\{\hat{x}^{k}_{n}\}$，显然它的极限就是 $\hat{x}^{k}$。

 若度规空间 $<M,d>$ 中所有点的任意邻域都包含 $B\subset{}M$ 的点，则它的所有开球也都和 $B$ 相交，因此可以在 $B$ 中构造柯西序列极限为该点，也就是 $M$ 是 $B$ 的极限点构成的，此时 $B$ 是 $M$ 的稠密子集。
 称度规空间 $<X,d>$ 到度规空间 $<Y,\rho{}>$ 的函数 $f$ 是**连续**的，如果
$$
\begin{equation}
\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}x_{n}=x\rightarrow{}\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}y_{n}=y
\end{equation}
$$
容易证明度规空间 $<X,d>$ 到 $<Y,\rho{}>$ 的函数 $f$ 是连续的，当且仅当在度规拓扑下， $Y$ 中任意开集的逆向是 $X$ 中的开集。
## 赋范空间和线性变换
在度规空间的基础上可以进一步定义**赋范空间**，一个赋范线性空间由一个矢量空间 $V$ 和 $V$ 上的一个满足下列条件的实值函数 $||\cdot{}||$ 构成
1. $||v||\geq{}0$,
2. $||v||=0\leftrightarrow{}v=0$,
3. $||\alpha{}v||=|\alpha{}|~||v||$,
4. $||v+w||\leq{}||v|| + ||w ||$,
$\forall{}\alpha{}\in{}\mathbb{C}，v,w\in{}V$。
一个赋范线性空间 $<V,||\cdot{}||>$ 可以诱导一个度规空间，只需把度规定义为 $d(v,w)=||v-w||$。但是度规空间不一定是矢量空间，自然不一定是赋范空间。赋范空间是矢量空间，矢量空间上重要的结构是线性变换，定义从一个赋范线性空间 $<V_{1},||\cdot{}||_{1}>$ 到一个赋范线性空间 $<V_{2},||\cdot{}||_{2}>$ 的**有界线性变换**（或**有界算子**）$T$ 是一个满足下列条件的从 $V_{1}$ 到 $V_{2}$ 的函数
5. 线性性，
6. $\exists{}C\geq{}0,||Tv||_{2}\leq{}C||v||_{1}$,
称最小的 $C$ 为 $T$ 的**范数**，记做 $||T||$。接下来求解 $||T||$，先寻找它的下限，对于 $||v||_{1}=1$ 的那些元素来说，有
$$
\begin{equation}
||Tv||_{2}
\leq{}||T||
\end{equation}
$$
因此 $||T||\geq{}\mathop{\rm sup}_{||v||_{1}=1}||Tv||_{2}$。令 $C'=\mathop{\rm sup}_{||v||_{1}=1}||Tv||_{2}$。则
$$
\begin{eqnarray}
\frac{||Tu||_{2}}{C'||u||_{1}}
&=&\frac{||Tu||_{2}}{C'||u||_{1}}
\nonumber\\
&=&\frac{||u||_{1}||T\frac{u}{||u||_{1}}||_{2}}{C'||u||_{1}||\frac{u}{||u||_{1}}||_{1}}
\nonumber\\
&=&\frac{||T\frac{u}{||u||_{1}}||_{2}}{C'}
\end{eqnarray}
$$
根据 $C'$ 的定义可得上式小于等于 $1$。所以 $C'$ 满足有界算子定义的第二条，因此 $||T||=C'$。也就是
$$
\begin{equation}
||T||
=\mathop{\rm sup}_{||v||_{1}=1}||Tv||_{2}
\end{equation}
$$设 $T:V_{1}\rightarrow{}V_{2}$ 是两个赋范线性空间的线性算子，以范数诱导的度规所定义的拓扑来衡量，可以证明下面命题等价
7. $T$ 在一点连续，
8. $T$ 在点点连续，
9. $T$ 是有界的。
$1\rightarrow{}2:$设 $T$ 在 $x_{0}$ 连续，则 $\forall{}x\in{}V_{1},x_{n}\rightarrow{}x$，有 $T(x_{n}-x+x_{0})\rightarrow{}T(x_{0})$，由 $T$ 的线性性有$T(x_{n})-T(x)\rightarrow{}0$，即$T(x_{n})\rightarrow{}T(x)$。
$2\rightarrow{}1$ 显然。
$3\rightarrow{}2:$$T$ 是有界的，则 $\forall{}x\rightarrow{}x_{0},||T(x-x_{0})||\leq{}C||x-x_{0}||\rightarrow{}0$。
$2\rightarrow{}3:$$\forall{}\varepsilon{}<0,\exists{}x_{0},x\in{}V_{1},\delta{}>0\rightarrow{}||T(x-x_{0})||<\varepsilon{}$  $\forall{}y\in{}V_{1},\exists{}x'\in{}N_{x_{0}},x'-x_{0}=\frac{\delta{}y}{2||y||}\rightarrow{}||x'-x_{0}||=\frac{\delta{}}{2}\rightarrow{}||T(\frac{\delta{}y}{2||y||})||<\varepsilon{}\rightarrow{}||T(y)||\leq{}C(\varepsilon{},\delta{}{})||y||$。

由度规空间的性质可知，任何赋范线性空间总可借助它诱导的度规空间完备化，且同构于它的完备化的一个稠密子集。

设 $T$ 是从一个赋范线性空间 $<V_{1},||\cdot{}||_{1}>$ 到一个完备的赋范线性空间$<V_{2},||\cdot{}||_{2}>$的有界算子，则 $T$ 可以唯一的延拓为一个从 $V_{1}$ 的完备化到 $V_{2}$ 的有界算子。
这是因为在 $V_{1}$ 的完备化中，每个 $V_{1}$ 的极限点都至少有一个点列向他靠近，那么极限点的像就必须是点列的像的极限，只需证明这个像存在即可，因为存在就唯一。下面说明这个事情：
由于原本的 $T$ 是有界的，所以它至少在一点连续，所以延拓后（至少 $V_{1}$ 的完备化中的那些可以被延拓的区域）也是有界的，另 $C$ 是这个延拓后的 $T$ 的范数。则 $(\forall{}\varepsilon{}>0)(\exists{}N>0)m,n>N\rightarrow{}d_{1}(x_{m},x_{n})<\varepsilon{}/C$，从而 $d_{2}(T(m)-T(n))<C\varepsilon{}/C<\varepsilon{}$，所以点列的像是柯西列，由于 $V_{2}$ 是完备的，所以柯西序列的极限一定存在。
然后简单说明一下极限的唯一性：如果换一个点列也在 $V_{1}$ 的完备化中逼近同一个极限点，则由极限点的的定义有
$$
\begin{eqnarray}
&&\forall{}\varepsilon{}>0,\exists{}N>0,\forall{}n>N,d_{1}(x_{n},x_{0})<\varepsilon{}/2C,d_{1}(x_{n}',x_{0})<\varepsilon{}/2C\\
\rightarrow{}&&d_{1}(x_{n},x_{n}')<\varepsilon{}/C\\
\rightarrow{}&&d_{2}(T(x_{n}),T(x_{n}'))<C\varepsilon{}/C_{sup}\leq{}\varepsilon{}
\end{eqnarray}
$$
所以它和之前的点列在 $V_{2}$ 中的像的极限唯一。
## 拓扑空间的泛网
设 $(X,\mathcal{U})$ 是一个拓扑空间，称 $\mathcal{N}$ 是 $x\in{}X$ 的一个**邻域基** $\leftrightarrow{}\forall{}N_{x}\in{}\mathcal{U}$，$\exists{}N\in{}\mathcal{N},N\subset{}N_{x}$。这里之所以不说 $N\in{}\mathcal{U}$ 是为了允许 $\mathcal{N}$ 的元素可以以闭集的形式存在。

根据拓扑空间中不同点的分离程度，可以给出**分离公理**，也就是 一个拓扑空间 
$(X,\mathcal{U})$ 被称为
1. $T_{1}\leftrightarrow{}(\forall{}x,y\in{}X)(x\neq y)\exists{}O\in{}\mathcal{U},x\notin{}O,y\in{}O$,
2. $T_{2}\leftrightarrow{}(\forall{}x,y\in{}X)(x\neq y)\exists{}O,V\in{}\mathcal{U},O\cap_{}^{}V=\varnothing{},x\in{}O,y\in{}V$,
3. $T_{3}\leftrightarrow{}$ 是 $T_{1}$ 的且对每一个闭集 $C,X-C$ 满足 $T_{2}$的条件,
4. $T_{4}\leftrightarrow{}$ 是$T_{1}$ 的且对于任意两个不相交闭集 $C_{1},C_{2}$, $\exists{}O_{1}$, $O_{2}\in{}\mathcal{U},O_{1}\cap_{}^{}O_{2}=\varnothing{}$, $C_{1}\subset{}O_{1}$, $C_{2\subset{}}O_{2}$。
容易证明  空间的定义等价于任何单点集都是闭集，对于集合 $\{x\}$，它的补集中每个元素都有一个开邻域不包含 $x$，而 $-\{x\}$ 就等于这些开邻域的并集，因此是一个开集，因此 $\{x\}$ 是一个闭集。反过来，如果每个单点集都是闭集，那么它的补集一定是开集，而它的补给一定包含任意不等于其元素但属于拓扑空间中的点，因此可以得到该空间是 $T_{1}$ 的。此外很容易看出来这四种定义是越来越强的，后面的可以得到前面的。

根据拓扑空间中元素的可数情况，又可以做如下定义：
一个拓扑空间被称为
5. 可分的 $\leftrightarrow{}$ 它的一个稠密集有可数个点,
6. 第一可数的 $\leftrightarrow{}$ 如果每一个点有一个可数邻域基,
7. 第二可数的 $\leftrightarrow{}X$ 有一个可数基。
对于一个度规空间来说，其中任意的一个点 $x$，$\{B_{\frac{1}{n}}(x)|n\in{}\mathbb{N}^{>0}\}$ 满足邻域基的任何要求，且是可数的，因此在度规诱导的拓扑下，**度规空间是第一可数的**。进一步的，如果一个度规看空间是可分的，那么它的可数那个稠密集中所有点的上述邻域基的并集也是可数的，因为它们的数量可以映射到 $\mathbb{N}\times{}\mathbb{N}$ 上去，而后者是可数的。只需要证明这个集合是度规空间的一个基即可，这是简单的，由于稠密集中序列的极限组成整个度规空间，而极限点与稠密集中相应的柯西序列中一个点的距离可以被一个任意小的正数限制，只要选取一个半径比该距离大的该点的一个开球就会包含极限点，因此前面所提的这个并集是一个基，因此**可分的度规空间在该拓扑下是第二可数的**。
用有限覆盖引理定义**紧拓扑空间**，也就是如果拓扑空间 $(X,\mathcal{U})$ 的每个开覆盖都有一个有限子覆盖，那么称该空间为一个紧的拓扑空间。

拓扑空间中没有距离的概念，所以没法直接定义序列的收敛性等内容，但是相关的技术又在研究很多问题的时候很方便，所以引入了拓扑空间中 “网” 的概念，也就是
设$(X,\mathcal{U})$是一个拓扑空间，做以下定义
8. 拓扑空间 $X$ 中的一个**网** $(x_\alpha)$ 是一个从一个偏序且有向的索引集 $A$ （关系为 $\geq{}$）到 $X$ 的映射 $\alpha \to x_\alpha$；
9. 一个网 $(x_\alpha)$ 收敛于 $x$，记为 $\lim_\alpha x_\alpha = x$，如果对于 $x$ 的每个开邻域 $U \subset X$，存在 $\alpha(U) \in A$，使得对于每个 $\alpha \ge \alpha(U)$ 都有 $x_\alpha \in U$（我们说 $(x_\alpha)$ 最终在 $U$ 中）；
10.  一个网 $(x_\alpha)$ 的子网 $(x_{\alpha(\beta)})$ 是通过一个映射 $B \to A$；$\beta \to \alpha(\beta)$ 定义的，其中 $B$ 和 $A$ 都是偏序且有向的索引集，使得对于任何 $\alpha_0 \in A$，存在 $\beta(\alpha_0) \in B$，使得对于任何 $\beta \ge \beta(\alpha_0)$ 都有 $\alpha(\beta) \ge \alpha_0$（我们说 $B$ 对 $A$ 是共尾的）；
11. 称一个网 $(x^{\alpha{}})$ 是**泛网**，如果 $\forall{}Y\subset{}X，(x^{\alpha{}})$ 最终要么全在 $Y$ 中要么全在 $-Y$ 中。就是柯西列的推广。
需要注意的是，子网的定义中并没有强调映射的承担集是一个序列，只要求它是一个满足定义的索引集即可。

有了网的概念可以很方便的去研究一些拓扑性质。比如可以证明下面几个引理：
8. 拓扑空间 $X$ 的一个子集 $Y$ 是闭的，等价于对于 $X$ 中每个收敛的网 $(x_\alpha)$，其中 $\forall \alpha, x_\alpha \in Y$，其极限实际上也位于 $Y$ 中；
9. 拓扑空间之间的一个函数 $f:X\rightarrow{}Y$，如果对于 $X$ 中的每个收敛的网 $(x_{\alpha{}})$，它的像 $(f(x_{\alpha{}}))$ 在 $Y$ 中是收敛的，则它一定收敛到 $(x_{\alpha{}})$ 的像。
10. 拓扑空间之间的一个函数 $f: X \to Y$ 是连续的，等价于对于 $X$ 中每个收敛的网 $(x_\alpha)$，网 $(f(x_\alpha))$ 在 $Y$ 中是收敛的；
11. 一个拓扑空间 $X$ 是紧的，如果每个网都有一个收敛的子网（Bolzano–Weierstrass 定理）。收敛子网的极限点被称为原始网的聚点（极限点）。
先证明第一条引理从左到右，如果有一个收敛网的极限不在 $Y$ 中，那么它就在 $-Y$ 中，根据收敛网的定义，这个极限点的每一个开集都与 $Y$ 相交，这与 $-Y$ 是开集矛盾。反过来，如果集合 $Y$ 所有收敛网的聚点都在 $Y$ 内且它不是一个闭集，那么 $-Y$ 中应该存在一些点，它们的所有开邻域都与 $Y$ 相交，选一个这样的点 $x$，选一个它的开邻域序列，满足后面的开邻域是前面的开邻域的子集，也就是这是一个逐渐搜索的开临域序列。每一个这样的开邻域都与 $Y$ 有交集，从交集中选取各不相等的代表点构成网，则这个网显然收敛到 $x$，但是由于代表点都在 $Y$ 中，因此这是 $Y$ 中的一个网，它的聚点应该在 $Y$ 中，因此矛盾。
然后证明第二个引理，假设 $(x_{\alpha{}})$ 收敛到 $x$，那么网 $(x_{\alpha{}})$ 与常元素网 $(x)$ 交替插值的网 $(\tilde{x}_{\alpha{}})$ 一定也收敛到 $x$，而它的像 $(f(\tilde{x}_{\alpha{}}))$ 有一个子网是 $(f(x))$，由于后者是常元素网，所以一定收敛到 $f(x)$，又由于原网 $(f(\tilde{x}_{\alpha{}}))$ 收敛，因此它肯定和 $(f(x))$ 收敛到一个像点，也就是收敛到 $f(x)$。
再证第三个引理，若满足引理条件但函数不连续，那么存在 $Y$ 中的开集 $O_{Y}$的逆像 $O_{X}=f^{-1}[O_{Y}]$ 不是 $X$ 中的开集，则类似上面的讨论 $O_{X}$ 有一些点是 $-O_{X}$ 中网的极限，对于一个这样的网 $(x^{\alpha{}})$，它的像是 $-O_{Y}$ 中的网，但是它的像收敛到 $O_{Y}$ 上，因此根据第一个引理，$-O_{Y}$ 不是闭集，这与 $O_{Y}$ 是开集矛盾。然后再看反过来的情况，如果函数是连续的，那么如果网 $(x^{\alpha{}})$ 收敛到 $x$，则对于 $f(x)$ 的任何一个开邻域 $V$，它的逆像一定是 $x$ 的一个开邻域，则一定有一个 $\alpha{}_{0}$，当 $\alpha{}\geq{}\alpha{}_{0}$ 时，$x^{\alpha{}}\in{}f^{-1}[V]$，因此这些 $x^{\alpha{}}$ 的像都在 $V$ 中，所以 $(f(x^{\alpha{}}))$ 收敛到 $f(x)$。
第四个引理证明比较复杂，不证明了。但是要注意的一点是，子网与原网共尾只要求子网的“尾巴”是原网的“尾巴”中选出一些即可，不要求严格相等，因此子网收敛原网不一定收敛，且不同子网可能有不同的聚点，因此原网可能有多个聚点。

关于泛网也有几个引理，设 $(X,\mathcal{U}),(Y,\mathcal{V})$是两个拓扑空间，则
16. $T_{2}$ 空间中泛网最多只有一个聚点，并且它会收敛于该点；
17. $\forall{}f:X\rightarrow{}Y$，若 $(x^{\alpha{}})$ 是泛网则，网 $(f(x^{\alpha{}}))$ 是泛网；
18. 任何网有泛子网。
第一个引理的证明很简单，假设 $x_{1}$ 和 $x_{2}$ 都是泛网 $(x^{\alpha{}})$ 的聚点，那么存在 $O_{x_{1}}$ 是第一个聚点的开邻域但是不包含第二个聚点，根据聚点的定义，$(x^{\alpha{}})$ 必须有一个子网最终落在这个开邻域中，又根据泛网的定义，这会导致整个网 $(x^{\alpha{}})$ 最终落在这个开邻域中，同样的还可以构造一个 $O_{x_{2}}$ 让整个网落入这里面，$T_{2}$ 空间的性质保证了这两个开集可以选择为交为空集，这会导致泛网最终落在一个空集里。蒂曼书对这里的表述是错误的，他没有加上 $T_{2}$ 空间的条件，可以举一个反例来说明一般的拓扑空间中该引理不成立。考虑一个无限集上的余有限拓扑（空集、全集、任何补集为有限集的集合为开集），比如自然数集 $\mathbb{N}$ 上的余有限拓扑。由于单点集是有限集，所以单点集的补集是开机，从而单点集是闭集，因此这是一个 $T_{1}$ 空间。先定义 $\mathbb{N}$ 上一个自由超滤子 $\mathcal{F}$，它是 $\mathbb{N}$ 上集合的集合，不包含任何有限集，且包含任何无限集。因此 $\forall{}A\subset{}\mathbb{N}$ 要么 $A\in{}\mathcal{F}$ 要么 $A\notin{}\mathcal{F}$。使用反包含关系可以赋予这个集合偏序，也就是 $A\geq{}B$ 当且仅当 $A\subset{}B$。这确实是一个偏序关系，因为 $\forall{}A,B\in{}\mathcal{F}$，若 $A\cap_{}^{}B$ 为有限集，则 $-(A\cap_{}^{}B)=(-A)\cup^{}_{}(-B)$ 为无限集，这与 $-A$ 和 $-B$ 都是有限集矛盾，因此 $A\cap_{}^{}B$ 为无限集，从而也是 $\mathcal{F}$ 中的元素，从而 $A,B\leq{}A\cap_{}^{}B$，因此 $\forall{}A,B\in{}\mathcal{F}$，有公共上界，从而确实是一个偏序，因此 $\mathcal{F}$ 就是一个偏序集，从它的每个元素 $A$ 中选择一个 $\mathbb{N}$ 中的元素 $x^{A}$ 作为代表元，则 $(x^{A})$ 就是一个网。然后说明这是一个泛网，$\forall{}S\subset{}X$，如果 $S\in{}\mathcal{F}$，则 $\forall{}A\geq{}S$，根据偏序的定义有 $A\subset{}S$，从而有 $(x^{A})\in{}S$，所以 $(x^{A})$ 最终全部在 $S$ 中。如果 $S\notin{}\mathcal{F}$，则 $-S\in{}\mathcal{F}$，就会导致 $(x^{A})$ 最终全部在 $-S$ 中。因此该网是一个泛网。然后证明它是收敛的且有很多收敛点，$\forall{}x \in{}\mathbb{N}$，随便取它一个开邻域 $O_{x}$，根据余有限拓扑的定义可知 $O_{x}\in{}\mathcal{F}$，因此根据前面关于 $S$ 的推导，泛网一定落入 $O_{x}$，根据 $O_{x}$ 的任意性可知泛网收敛到 $x$，因此实际上泛网收敛到 $\mathbb{N}$ 上的每一个点。所以蒂曼的陈述是错的。
然后证明第二个引理，假如 $(x^{\alpha{}})$ 是泛网，$\forall{}S\subset{}Y$，如果它和 $f$ 的像无交，则当然 $(f(x^{\alpha{}}))$ 不在其中且在它的补集中。如果它和 $f$ 的像交为 $S_{X}$，则 $(x^{\alpha{}})$ 要么最终在 $f^{-1}[S_{X}]$ 中要么在 $-f^{-1}[S_{X}]$ 中，从而 $(f(x^{\alpha{}}))$ 要么最终在 $S_{X}$ 中要么最终在 $f[X]-S_{X}$ 中从而在 $-S_{X}$ 中，所以 $(f(x^{\alpha{}}))$ 是泛网。
第三个定理也要用超滤子来证明，不证明了。

有了这些引理就可以证明一个重要的推论，即一个**拓扑空间 $X$ 是紧的当且仅当每个泛网都收敛**。
一方面，紧空间中每个网都有收敛的子网，因此每个泛网都有聚点，由于每个泛网最多只有一个聚点且收敛到该聚点，所以紧空间中每个泛网都收敛。另一方面，假如每个泛网都收敛，由于每个网都有泛子网，所以每个网都有一个收敛的子网，也就是该空间是紧的。

有了上面知识，就可以重新表述一下**乘积拓扑**，也就是拓扑空间 $X_l$（$L$ 为任意索引集）的直积 $X_\infty = \prod_{l \in L} X_l$ 上的 Tychonov 拓扑是使得所有投影
$$
p_l : X_\infty \to X_l; (x_{l'})_{l' \in L} \mapsto x_l
$$
都连续的最弱拓扑，也就是说，一个网 $x_\alpha = (x_\alpha^l)_{l \in L}$ 收敛于 $x = (x_l)_{l \in L}$ 当且仅当对每个 $l \in L$，$x_\alpha^l \to x_l$ 逐点收敛（不一定在 $L$ 中一致收敛）。等价地，集合 $p_l^{-1}(U_l) = [\prod_{l' \neq l} X_{l'}] \times U_l$ 被定义为开集，并构成 $X_\infty$ 拓扑的一个基（任何开集都可以通过这些集合的有限交和任意并得到）。
进一步可以得到一个重要的定理，即**Tychonov定理**：紧拓扑空间的直积拓扑是紧的。
证明比较简单，设 $(x_\alpha) = (x_\alpha^l)_{l \in L}$ 是 $X_\infty = \prod_{l \in L} X_l$ 中的任意泛网。根据前面的引理，网 $p_l((x_\alpha)) = (x_\alpha^l)$ 在 $X_l$ 中是泛网。由于 $X_l$ 是紧的，它收敛于某个 $x_l$。定义 $x := (x_l)_{l \in L}$。根据 Tychonov 拓扑的定义，$x_\alpha \to x$ 当且仅当对任何 $l \in L$，$x_\alpha^l \to x_l$，因此 $(x_\alpha)$ 收敛。
对于一个紧拓扑空间 $X$ 的闭子集 $V$，通过原空间的诱导拓扑可以成为一个拓扑空间。由于存在天然的从 $V$ 到 $X$ 的映射，即限制在 $V$ 上的恒等映射，因此 $V$ 中的泛网也是 $X$ 中的泛网。由于 $X$ 是闭的，所以这些泛网都收敛，又由于 $V$ 是闭的，所以其上每个收敛的网都收敛到其中。因此对于 $V$ 上的任意一个泛网 $(x^{\alpha{}})$， $\exists{}x\in V$ 满足任何 $x$ 的开邻域 $O_{x}$ 都会让网最终落入其中，由于网和 $x$ 都在 $V$ 内，自然也会落入到 $O_{x}\cap_{}^{}V$ 中，又由于 $O_{x}\cap_{}^{}V$ 根据诱导拓扑定义是 $V$ 上的开集，因此是 $x$ 在诱导拓扑下的开邻域，从而网收敛到 $(x^{\alpha{}})$，从而 $V$ 上任何泛网在诱导拓扑下都收敛，也就是其为一个紧空间了。 
## 测度
物理中的希尔伯特空间是构型空间的函数空间，所以是一个泛函空间。为了把这种空间变成一个希尔伯特空间就需要定义其上的内积，通常是通过定义一个测度来诱导定义内积的。这里简单说一下相关的测度的知识。
## 博雷尔测度
 Def 对任意定义域为 $R$ 的单增函数 $\alpha{}(\cdot{})$，定义抽象大小函数 $\mu{}_{\alpha{}}((a,b))=\alpha{}(b-0)-\alpha{}(a+0)$，其中 $\alpha{}(x\pm0):=\mathop{{\rm lim}}\limits_{\varepsilon{}\rightarrow{}0}^{}\alpha{}(x\pm0)$，对于紧边界区域的作用则不需要取极限。
 Def 集合 $\mathscr{B}$ 称为大小函数的可测集，若它满足下面条件
1. 如果$A\in{}\mathscr{B}$，则$(R-A)\in{}\mathscr{B}$;
2. $\mathscr{B}$ 包括 $R$ 所有的开集;
3. 若 $A_{n}\in{}\mathscr{B}$，则 $\cup^{\infty}_{n=1}A_{n}\in{}\mathscr{B}$ 且当它们互不相交时，$\mu_{\alpha{}}{}(\cup^{\infty}_{n=1}A_{n})=\sum\limits_{n=1}^{\infty}\mu_{\alpha{}}{}(A_{n})$。
由于满足上面条件的集合可能是间断的，如 $(2,5]\cup^{}_{}[7,11]$，上面第三条则定义了对这种集合的作用，即 $\mu{}_{\alpha{}}((2,5]\cup^{}_{}[7,3])=\alpha{}(5)+\alpha{}(11)-\alpha{}(3+0)-\alpha{}(7)$。
Def 博雷尔集族是 $R$ 上满足下列条件的最小子集族
4. 该族对求补集封闭；
5. 该族对可数次求并集封闭；
6. 该族包括$R$上所有开区间。
定义博雷尔集上的抽象测度定义为 $\mu{}_{\alpha{}}(\cup^{}_{}B_{i})=\sum\limits_{i}^{}\mu{}_{\alpha{}}(B_{i})$，若它们互不相交且 $\mu{}_{\alpha{}}(\varnothing{})=0$。
大小函数的可测集并不是博雷尔集族，尽管其满足上面三个条件，但是其不一定是满足上面三个条件的最小集族。所谓 “最小” 是一定存在的，首先它包含所有开区间，所以非空，然后所有满足该要求的集合求交集即可。

 Def 称 $\mathscr{B}$ 上的一个测度 $\mu{}$ 为博雷尔测度，若它满足下列条件
7. 若 $C$ 为紧集，则 $\mu{}(C)<\infty$;
8. $\mu{}(B)=\rm{sup}\{\mu{}(C)|C\subset{}B,C是紧的\}$;
9. $\mu{}(B)=\rm{inf\{\mu{}(O)|B\subset{}O,O是开集\}}$。
可以证明 $\mu{}_{\alpha{}}$是博雷尔测度， 由于测度有可加性，所以用一个连续区间来证明即可。其实只需要证明如果 $O$ 是开集，则 $\mu{}(O)={\rm sup}\{\mu{}(C)|C\subset{}O,C是紧的\}$ 即可。对于 $(a,b)$ 来说，由于 $\alpha{}$ 是单增的，所以如果 $\varepsilon{}_{1}<\varepsilon{}_{2}$，则显然有 $\mu{}_{\alpha{}}([a+\varepsilon{}_{1},b-\varepsilon{}_{1}])>\mu{}_{\alpha{}}([a+\varepsilon{}_{2},b-\varepsilon{}_{2}])$，而开集的抽象大小函数的定义可以改写为 $\mu{}_{\alpha{}}((a,b))=\mathop{{\rm lim}}\limits_{\varepsilon{},\epsilon{}\rightarrow{}0}^{}\mu{}_{\alpha{}}[a+\varepsilon{},b-\epsilon{}]$，右侧其实就是它所包含的所有闭区间的抽象大小的上限。

有了大小函数这个博雷尔测度后，勒贝格-斯蒂尔吉斯积分用 $\mu{}_{\alpha{}}$ 定义为
$$
\begin{equation}
\int_{}^{}fd\mu{}_{\alpha{}}
=\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}\sum\limits_{m=1}^{\infty}\frac{m}{n}\mu{}_{\alpha{}}(f^{-1}[[\frac{m}{n},\frac{m+1}{n})])
\end{equation}
$$
该式可以改造为
$$
\begin{eqnarray}
\int_{}^{}fd\mu{}_{\alpha{}}&=&\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}\sum\limits_{m=1}^{\infty}\frac{m}{n}\frac{\mu{}_{\alpha{}}(f^{-1}[[\frac{m}{n},\frac{m+1}{n})])}{f^{-1}[[\frac{m}{n},\frac{m+1}{n})}f^{-1}[[\frac{m}{n},\frac{m+1}{n})
\nonumber\\
&=&\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}\sum\limits_{m=1}^{\infty}\sum\limits_{_{i}}^{}\frac{m}{n}\frac{\mu{}_{\alpha{}}(f_{i}^{-1}[[\frac{m}{n},\frac{m+1}{n})])}{f_{i}^{-1}[[\frac{m}{n},\frac{m+1}{n})}f_{i}^{-1}[[\frac{m}{n},\frac{m+1}{n})
\nonumber\\
&=&\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}\sum\limits_{m=1}^{\infty}\sum\limits_{_{i}}^{}\frac{m}{n}\alpha{}'(f_{i}^{-1}[[\frac{m}{n},\frac{m+1}{n})])f_{i}^{-1}[[\frac{m}{n},\frac{m+1}{n})
\nonumber\\
&=&\int_{}^{}f\alpha{}'dx
\end{eqnarray}
$$
其中指标 $i$ 用来标记每一段逆回来的时候可能的连续区间的个数。所以这就回到了通常所熟悉的积分的形式。
## 海尔测度
定义一下排列算子 $U_{\pi{}}(v_{1}\otimes{}...\otimes{}v_{m})=v_{\pi{}(1)}\otimes{}...\otimes{}v_{\pi{}(m)}$
Def $\Lambda{}^{m}:=\{\eta{}\in{}\otimes{}^{m}V|U_{\pi{}}(\eta{})=(-1)^{\pi{}}\eta{}\}$。
 Thm 设 $G$ 是 $n$ 维李群，则 $G$ 上存在一个左不变的处处非零形式场 $\omega{}（\omega{}(gh)\equiv{}(\Lambda{}^{n}(L_{g}^{*}))(\omega{}(h))）$。存在 $G$ 上的函数 $\Delta{}$ s.t. $\Lambda{}^{n}(R_{g}^{*})\omega{}=\Delta{}(g)\omega{}$。当 $G$ 是紧群时，$\Delta{}(g)=1$。
左不变矢量场的对偶矢量的楔积自然也是左不变的，且是处处非零的n形式场。由于左平移和右平移作为算符可以交换，所以 $\Lambda{}^{n}(R^{*}_{g})\omega{}$ 也是左不变的，只能与 $\omega{}$ 差一个常数。
右不变意味着 $\int_{}^{}f(yx)d\mu{}(y)=\Delta{}(x)\int_{}^{}f(y)d\mu{}(y)$，当 $f$ 为常数且 $G$ 为紧群时，积分结果有限且逼出 $\Delta{}(x)=1$。

Def 当群 $G$ 为紧群时，称左不变处处非零形式场 $\omega{}$ 生成的满足 $\int_{G}^{}d\mu{}(x)$ 的测度为**海尔测度**。
有了海尔测度后就有了群上的积分，从而可以分析紧李群的平方可积空间的结构，在此之前先证明重要的**舒尔引理**，也就是设 $G$ 是群，$\rho{}_{1}:G\rightarrow{}GL(V_{1})$ 和 $\rho{}_{2}:G\rightarrow{}GL(V_{2})$ 是两个不可约表示。若线性映射 $\phi{}:V_{1}\rightarrow{}V_{2}$ 满足：  
$$
\begin{equation}
\phi{}\circ{}\rho{}_{1}(g)
=\rho{}_{2}(g)\circ{}\phi{}
,\qquad
\forall{}g\in{}G
\end{equation}
$$
则称 $\phi{}$ 为 **intertwining 算子**，其满足
1. 若 $\rho{}_{1}$ 与 $\rho{}_{2}$ 不等价，则 $\phi{}=0$；
2. 若 $\rho{}_{1}$ 与 $\rho{}_{2}$ 等价，则 $\phi{}$ 是同构映射。
证明是比较直接的，由于要证明它可能是两个极端：$0$ 和同构映射，所以分析它的核和它的像。先看它的核，$\forall{}v\in{}{\rm ker}\phi{}$，$\forall{}g\in{}G$，有
$$
\begin{equation}
\phi{}(\rho{}_{1}(g)v)
=\rho{}_{2}(g)\phi{}(v)
=0
\end{equation}
$$
所以 $\rho{}_{1}(g)v\in{}{\rm ker}\phi{}$。也就是 ${\rm ker}\phi{}$ 是一个该群的表示空间，由于 $V_{1}$ 是不可约表示空间，所以 ${\rm ker}\phi{}$ 要么是平凡表示，要么是 $V_{1}$。
然后看它的像，$\forall{}\omega{}=\phi{}(v)\in{}{\rm img}\phi{}$，$\forall{}g\in{}G$，有
$$
\begin{equation}
\rho{}_{2}(g)\omega{}
=\rho{}_{2}(g)\phi{}(v)
=\phi{}(\rho{}_{1}(g)v)
\end{equation}
$$
因此 ${\rm img}\phi{}$ 是 $V_{2}$ 的子表示空间，要么是平凡表示，要么是 $V_{2}$。
当 $\rho{}_{1}$ 与 $\rho{}_{2}$ 不等价时，若 ${\rm ker}\phi{}=V_{1}$，则 $\phi{}=0$，从而 ${\rm img}\phi{}=\{0_{2}\}$ 无矛盾。若 ${\rm ker}\phi{}=\{0_{1}\}$，则意味着
3. $\phi{}$ 必须是单射；
4. 当 $V_{1}$ 不是平凡表示时， ${\rm img}\phi{}\neq\{0\}$；
而第二个条件又导致 ${\rm img}\phi{}=V_{2}$，因此 $\phi{}$ 是一个双射，也就是是一个同构映射，这意味着两个表示等价，矛盾。
当 $\rho{}_{1}$ 与 $\rho{}_{2}$ 等价时，类似的讨论就可以得到 $\phi{}$ 必须是一个同构映射。
注意由于两个表示等价时它们本来就可以通过一个同构映射联系起来，所以总存在一个映射可以把 $\phi{}$ 变为常数映射。

接下来证明紧群表示论中的重要的不可约表示矩阵元的正交定理，也就是**彼得-外耳定理**（Peter-Weyl Theorem），它分为两段段陈述
5. 紧群的任何不可约表示都是有限维的
6. 不可约表示的矩阵元在 $L^{2}(G)$ 中构成一个完备正交系，正交关系为 $\int_{}^{}\rho{}_{m}(g)_{ij}\rho{}_{n}(g)^{\dagger}_{\alpha{}\beta{}}=\delta{}_{mn}\frac{\delta{}_{i\beta{}}\delta{}_{j\alpha{}}}{{\rm dim}\rho{}_{m}}$。
首先是第一段表述的证明，
然后是第二段表述的证明，只需要证明第二段表示中所提到的积分是一个 intertwining 算子即可。也就是令 $T=\int_{}^{}\rho{}_{1}(g)_{ij}\rho{}_{2}(g)^{\dagger}_{\alpha{}\beta{}}dg$，则有
$$
\begin{eqnarray}
\rho{}_{1}(h)T\rho{}_{2}(h^{-1})
&=&\int_{}^{}\rho{}_{1}(h)\rho{}_{1}(g)_{ij}\rho{}_{2}(g)^{\dagger}_{\alpha{}\beta{}}\rho{}_{2}(h^{-1})dg
\nonumber\\
&=&\int_{}^{}\rho{}_{1}(hg)_{ij}\rho{}_{2}(gh^{-1})^{\dagger}_{\alpha{}\beta{}}dg
\nonumber\\
&=&\int_{}^{}\rho{}_{1}(g)_{ij}\rho{}_{2}(g)^{\dagger}_{\alpha{}\beta{}}dg
\nonumber\\
&=&T
\end{eqnarray}
$$
因此可以得到 $\rho{}_{1}(h)T=T\rho{}_{2}(h)$，也就是 $T$ 是一个 intertwining 算子，因此根据舒尔引理，若 $\rho{}_{1}$ 与 $\rho{}_{2}$ 不等价，则 $T=0$，否则 $T$ 是一个同构映射。由于 $\rho{}_{1}(g)_{ij}$ 和 $\rho{}_{2}(g)_{\alpha{}\beta{}}$ 都是矩阵元，所以它们的值域都是复数域，因此 $T$ 是一个从复数域到复数域的线性映射，因此它要么是零映射，要么是常数映射 $K\delta{}_{i\beta{}}\delta{}_{j\alpha{}}$。至于常数映射的大小，只需要对 $T$ 求迹即可。
## 交换$C^{*}$-代数
## 巴拿赫代数
 1 Def 称代数$\mathfrak{A}$的一个子代数$\mathfrak{J}$为左（右）理想若$aj\in{}\mathfrak{I},\forall{}a\in{}\mathfrak{A},\forall{}j\in{}\mathfrak{I}$（$jb\in{}\mathfrak{I},\forall{}b\in{}\mathfrak{A},\forall{}j\in{}\mathfrak{I}$）。称一个理想为双边理想若它既是左理想又是右理想。称一个理想为最大的，若它不含于$\mathfrak{A}$和它自己之外的理想。
 2 Prop $a\mathfrak{A},\forall{}a\in{}\mathfrak{A}$是一个右理想，$\mathfrak{A}a,\forall{}a\in{}\mathfrak{A}$是一个左理想。
 3 Def 代数$\mathfrak{A}$的一个对合$*$是一个映射$*:\mathfrak{A}\rightarrow{}\mathfrak{A},a\mapsto{}a^{*}$满足下列条件
1. $(za+z'b)*=\bar{z}a^{*}+\bar{z'}b^{*}$，
2. $(ab)^{*}=b^{*}a^{*}$，
3. $(a^{*})^{*}=a$，
$\forall{}a,b\in{}\mathfrak{A},z,z'\in{}\mathbb{C}$。具有对合的代数叫$^{*}-$代数。
 4 Def 两个$^{*}-$代数之间的保对合的同态（$\phi{}(a^{*})=\phi{}(a)^{*}$）叫做$^{*}-$同态。
 5 Def 具有范数结构的代数叫赋泛代数，若一个赋范代数$\mathfrak{A}$还是一个$^{*}-$代数且$||a^{*}||=||a||$，则称其为赋范$^{*}-$代数。额外要求单位元的范数为$1$。
 6 Def 如果一个赋泛代数是完备的，则称其为巴拿赫代数。
 7 Def 称一个巴那赫$^{*}-$代数为一个$C^{*}-$代数若它的范数和对合满足$||a^{*}a||=||a||^{2}$。
 8 Def 若$\mathfrak{I}$是代数$\mathfrak{A}$的双边理想，则可以定义商代数$\mathfrak{A/I}:=\{a+\mathfrak{I}|\forall{}a\in{}\mathfrak{A}\}$。
 9 Def 称含幺巴那赫代数的全部非零$^{*}-$同态为它的谱$\Delta{}(\mathfrak{A})$。谱的元素叫做特征。
 10 Thm $\chi{}(1)=1,\chi{}(a^{-1})=\chi{}(a)^{-1},\chi{}(0)=0$。
 11 Def 含幺巴那赫代数$\mathfrak{A}$的一个特征$\chi{}$的核定义为$\{a\in{}\mathfrak{A}|\chi{}(a)=0\}$。
 12 Def 特征的核都是双边最大理想
$双边理想显然，把\mathfrak{A}视作线性空间$，$则\chi{}是上面的非零线性函数$，$其核是余维为一的线性子空间$。$若有一个更大的理想\mathfrak{I}真包含ker(\chi{})$，$则\exists{}i\in{}\mathfrak{I}-ker(\chi{})$，$从而\mathfrak{A}=span\{ker(\chi{}),i\}$，$从而\mathfrak{I}=\mathfrak{A。}$
 13 Def $\mathfrak{A}$是一个赋范含幺代数，$a\in{}\mathfrak{A}$的谱$\sigma{}(a)$定义为$\mathbb{C}-\rho{}(a)$，其中$\rho{}(a):=\{z\in{}\mathbb{C}|(a-z\cdot{}1)^{-1}\in{}\mathfrak{A}\}$称为$a$的可解集。
 14 Def 对于$z\in{}\rho{}(a)$，称$r_{z}(a):=(a-z)^{-1}$为$a$在$z$处的解，$r(a):=\rm{sup}(\{|z||z\in{}\sigma{}(a)\})$为$a$的谱半径。
 15 Thm $r(a)=\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}||a^{n}||^{1/n}$。
首先证明等号右边收敛。取两个数$n>m\geq{}1$，则$\exists{}r<m$ s.t. $n=km+r$。此时有不等式
$$
||a^{n}||^{1/n}\leq{}||a^{km}||^{1/n}||a^{r}||^{1/n}\leq{}||a^{m}||^{k/n}||a^{r}||^{1/n}
$$
然后保持$m$不动让$n\rightarrow{}\infty$，则有$||a^{n}||^{1/n}\leq{}||a^{m}||^{1/m},\forall{}m\geq{}1$。这意味着数列$\{x_{n}=||a^{n}||^{1/n}\}|_{n>m}$有界因此必有聚点，令${\rm lim}_{n}{\rm sup}(x_{n})$为这些聚点中最大值，则有${\rm lim}_{n}{\rm sup}(x_{n})\leq{}m$。再令${\rm lim}_{m}{\rm inf}(x_{m})$为$\{x_{m}=||a^{m}||^{1/m}\}|_{m>1}$的聚点的最小值，则有${\rm lim}_{n}{\rm sup}(x_{n})\leq{}{\rm lim}_{m}{\rm inf}(x_{m})$，从而只有一个聚点所以数列收敛记作$x=\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}||a^{n}||^{1/n}$。
然后证明等号成立，$r_{z}(a)=(a-z)^{-1}=-\frac{1}{z}\sum\limits_{n=0}^{\infty}(\frac{a}{z})^{n}$，收敛的前提是$||a^{n}||^{1/n}<|z|$，所以$|z|>x,\forall{}z\in{}\rho{}(a)$，从而$\rm{sup}(|-\rho{}(a)|)=x$。
## Gel’fand 定理
 1 Thm 含幺巴那赫代数理想的闭包也是理想，从而每个最大理想都是闭的。
以左理想为例，$aj\in{}\mathfrak{J}\subset{}\bar{\mathfrak{J}},\forall{}a\in{}\mathfrak{A},j\in{}\mathfrak{J}$，设$b\in{}\bar{\mathfrak{J}}-\mathfrak{J}$，则$\forall{}\varepsilon{}>0,\exists{}j\in{}\mathfrak{J},||aj-ab||\leq{}||aj||\cdot{}||ab||\leq{}\varepsilon{}$，从而$ab\in{}\mathfrak{\bar{J}}$。
 2 Thm 含幺巴那赫代数$\mathfrak{A}$闭的双边理想$\mathfrak{I}$的商代数$\mathfrak{A/I}$以$||[a]||:=\mathop{inf}\limits_{b\in{}[a]}^{}||b||$为范数成为一个巴那赫代数。
$$
||z[a]||=||z(a+\mathfrak{I})||=||za+\mathfrak{I}||=||[za]||=\mathop{inf}\limits_{b\in{}[za]}^{}||b||=z~\mathop{inf}\limits_{b\in{}[a]}^{}||b||=z||[a]||
$$
$$
||[a]+[a']||=\mathop{inf}\limits_{b\in{}[a],b'\in{}[a']}^{}||b+b'||\leq{}\mathop{inf}\limits_{b\in{}[a],b'\in{}[a']}^{}(||b||+||b'||)=\mathop{inf}\limits_{b\in{}[a]}^{}||b||+\mathop{inf}\limits_{b'\in{}[a']}^{}||b'||=||[a]||+||[a']||
$$
$$
0=||[a]||\rightarrow{}0\in{}[a]\rightarrow{}[a]=[0]
$$
$\forall{}\varepsilon{}>0,\exists{}N~s.t.~\forall{}n>N,\varepsilon{}>||[a_{n+1}]-[a_{n}]||=\mathop{inf}\limits_{b_{n+1}\in{}[a_{n+1}],b_{n}\in{}[a_{n}]}^{}||b_{n+1}-b_{n}||$。$设满足最小值条件的那对(b_{n+1},b_{n})为(c_{n+1},c_{n})$，$则可以在\mathfrak{A}中构造一个点列\{c_{n}\}为柯西列，设它的极限为a。$
$由于理想是闭的，所以极限在理想中$。$则||[a_{n}]-[a]||=\mathop{inf}\limits_{b_{n}\in{}[a_{n}],b\in{}[a]}^{}||b_{n}-b||\leq{}\mathop{inf}\limits_{b\in{}[a]}^{}||c_{n}-b||\leq{}||c_{n}-a||$，$所以该柯西列的极限为a。$

 3 Lemma 含幺代数的非平凡左（右）理想一定不含左（右）可逆元素。
$$
j\in{}\mathfrak{I},\exists{}j'\in{}\mathfrak{A}~s.t.j'j=1\rightarrow{}1\in{}\mathfrak{I}\rightarrow{}\mathfrak{I=AI=A}
$$
 4 Thm 若$\mathfrak{A}$是一个交换含幺巴那赫代数，则$\mathfrak{I}$是它的一个最大理想当且仅当$\mathfrak{A/I}-[0]$所有元素可逆。
由商代数定义易证这个商代数是交换和含幺的。最大理想是闭得所以它是一个含幺交换巴那赫代数。若$\mathfrak{A/I}$有一个非平凡理想$\mathfrak{k}$，设$\pi{}$为投影映射，则$\pi{}[\mathfrak{k}]^{-1}$是$\mathfrak{A}$的一个理想且真包含$\mathfrak{I}$，与$\mathfrak{I}$是最大理想矛盾。$\forall{}a+\mathfrak{I}\in{}\mathfrak{A/I},a+\mathfrak{I}\neq0$有$\mathfrak{A/I}(a+\mathfrak{A})$是一个非零理想，从而是商代数自己。商代数含幺意味着$a+\mathfrak{I}$必有逆元。
若右边成立左边不成立，则$\exists{}\mathfrak{J}\subset{}\mathfrak{A}$是一个理想且$\mathfrak{I}$是它的真子集，$\mathfrak{A/I}-[0]$所有元素可逆意味着$\mathfrak{J/I}$也是，因此$\mathfrak{J}$中有可逆元素，只能是平凡理想。
 5 Thm若$\mathfrak{A}$是一个交换含幺巴那赫代数，$\mathfrak{I}$是它的一个最大理想，则$\forall{}a\in{}\mathfrak{A/I},\sigma{}(a)$为单点集且$\sigma{}([0])=0$。
$设\sigma{}(a)=\varnothing{}$,$则\rho{}(a)=\mathbb{C}$，$即r_{z}(a)是解析的$，$考虑其上一个连续线性算子\phi{}:\mathfrak{A/I}\rightarrow{}\mathbb{C}$,$则\phi_{r(b)}{}:\mathbb{C}\rightarrow{}\mathbb{C},z\mapsto{}{}\phi{}(r_{z}(b))是解析的$，$又由于连续算子必有界$，$所以\phi{}_{r(b)}的像是独点集\{c\}$。$当z\rightarrow{}\infty时，$$r_{z}(b)\rightarrow{}0$，$所以c\equiv{}0$。$而线性算子的性质s.t.r_{z}(b)=[0],\forall{}z\in{}\mathbb{C}$。$那么r_{z}(b)就无逆$，$这与假设矛盾$。$所以由于其它元素的可逆性$，$\forall{}a\in{}\mathfrak{A/I},\exists{}z_{a}\in{}\mathbb{C},a-z_{a}\cdot{}1=[0]$，$显然z_{a}是唯一的。$
 6 Thm (Gel'fand 定理) 若$\mathfrak{A}$是一个交换含幺巴那赫代数，$\mathfrak{I}$是它的一个最大理想，则商代数与$\mathbb{C}$同构。
$$
容易验证\varphi{}:\mathfrak{A/I}\rightarrow{}\mathbb{C},a\mapsto{}z_{a}是同构映射。
$$
 7 Cor 一个交换含幺巴那赫代数的谱和全部最大理想的集合$I(\mathfrak{A})$之间有自然的双射。
$谱到核的映射就是一个从谱到I(\mathfrak{A})的一个自然映射$，$而有一个最大理想\mathfrak{I}$，$它的商空间自然诱导一个\mathfrak{A}到\mathbb{C}的以\mathfrak{I}为核的非零映射$，$是前一个映射的逆$，$因此是双射。$
 8 Lemma 若$\mathfrak{A}$是一个含幺交换巴那赫代数，$\forall{}a\in{}\mathfrak{A},z\in{}\sigma{}(a)\leftrightarrow{}\exists{}\chi{}\in{}\Delta{}(\mathfrak{A}),\chi{}(a)=z$。
$$
\chi{}(a)=z\leftrightarrow{}\chi{}(a-z\cdot{}1)=0\leftrightarrow{}(a-z)\in{}
ker(\chi{})\leftrightarrow{}(a-z)不可逆$$
 9 Def 对于含幺交换巴那赫代数$\mathfrak{A}$的一个特征$\chi{}$，定义它的范数$||\chi{}||:=\mathop{sup}\limits_{0\neq a\in{}\mathfrak{A}}^{}\frac{|\chi{}(a)|}{||a||}$。
 10 Lemma 含幺交换巴那赫代数$\mathfrak{A}$的谱$\Delta{}(\mathfrak{A})$是它作为一个拓扑矢量空间的连续线性泛函$\mathfrak{A}'$中单位球壳的子集。
$$
\begin{eqnarray}
||\chi{}||&=&\mathop{sup}\limits_{0\neq a\in{}\mathfrak{A}}^{}\frac{|\chi{}(a)|}{||a||}\\
&\leq{}&\mathop{sup}\limits_{0\neq a\in{}\mathfrak{A}}^{}\frac{sup\{\chi'{}(a)|\chi{}'\in{}\Delta{}(\mathfrak{A})\}}{||a||}\\
&=&\mathop{sup}\limits_{0\neq a\in{}\mathfrak{A}}^{}\frac{sup \{\sigma{}(a)\}}{||a||}\\
&=&\mathop{sup}\limits_{0\neq a\in{}\mathfrak{A}}^{}\frac{r(a)}{||a||}\\
&=&\mathop{sup}\limits_{0\neq a\in{}\mathfrak{A}}^{}\frac{\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}||a^{n}||^{1/n}}{||a||}\\
&\leq{}&1
\end{eqnarray}

$$
$由于\chi{}(1)=1$，$所以||\chi{}||=1,\forall{}\chi{}\in{}\Delta{}(\mathfrak{A})$。$因此它们都有界所以都连续。$
## Gel’fand 拓扑和Gel'fand变换
 1 Def 称拓扑矢量空间$X$的全体连续有界线性泛函为$X$的拓扑对偶$X'$。
 2 Def 拓扑对偶上的弱$^{*}-$拓扑定义为 s.t. $\forall{}x\in{}X,x:X'\rightarrow{}\mathbb{C},\phi{}\mapsto{}\phi{}(x)$连续的最弱拓扑。
 3 Thm 拓扑对偶上定义了弱拓扑$\leftrightarrow{}X'$上的一个网$(\phi{}^{\alpha{}})\rightarrow{}\phi{}$当且仅当$\forall{}x\in{}X,(\phi{}^{\alpha{}}(x))\rightarrow{}\phi{}(x)$。
 4 Def 称含幺交换巴那赫代数$\mathfrak{A}$的对偶$\mathfrak{A'}$上的弱$^{*}-$拓扑在的谱$\Delta{}(\mathfrak{A})$上诱导拓扑为$Gel'fand$拓扑。
 5 Thm 数列的上极限（数列极限值的上确界）小于等于数列的上确界（数列上确界的极限值）
 6 Lemma 巴那赫空间的拓扑对偶的单位球在弱拓扑下是闭的。
$单位球B:=\{\phi{}\in{}X'|~||\phi{}||=\mathop{sup}\limits_{x\in{}X}^{}\frac{|\phi{}(x)|}{||x||}\leq{}1\}$。$在X'中找一个通用网(\phi{}^{\alpha{}})$，$\forall{}x\in{}X,x[(\phi{}^{\alpha{}})]是\mathbb{C}中的通用网$，$\mathbb{C}是紧的所以通用网极限在\mathbb{C}中存在$，$所以\phi{}_{{\rm lim}}:=\mathop{{\rm lim}}\limits_{\alpha{}}^{}\phi{}^{\alpha{}}\in{}X'存在$，$则||\phi{}_{{\rm lim}}||=\mathop{sup}\limits_{x\in{}X}^{}\frac{\mathop{{\rm lim}}\limits_{\alpha{}}^{}|\phi{}^{\alpha{}}(x)|}{||x||}\leq{}\mathop{{\rm lim}}\limits_{\alpha{}}^{}\frac{\mathop{{\rm sup}}\limits_{x\in{}X}^{}|\phi{}^{\alpha{}}(x)|}{||x||}=\mathop{{\rm lim}}\limits_{\alpha{}}^{}||\phi{}^{\alpha{}}||\leq{}1$。$因此\phi{}_{{\rm lim}}\in{}B。$
 7 Thm 在$Gel'fand$拓扑下，含幺交换巴那赫代数的谱是紧的。
$紧空间的闭集是紧的$，$所以只需要检验谱是闭的$，$也就是任何非零同态网的极限还是非零同态网$，$这是容易的。$
 8 Def $X$是一个拓扑空间，$\mathcal{C}$是其一个函数集，如果$\forall{}x,y\in{}X,x\neq y,\exists{}{C}\in{}\mathcal{C},C(x)\neq C(y)$，则称该函数集将拓扑空间的点分离。
 9 Lemma 能被连续函数将点分离的拓扑空间$X,\mathcal{U}$是豪斯道夫空间。
$\forall{}x,y\in{}X,x\neq y，\exists{}f\in{}\mathcal{C}，f(x)\neq f(y)$。$由于f是连续的$，$所以\exists{}O_{fx},O_{fy}\subset{}\mathbb{C}是开的，U_{x},U_{y}\in{}\mathcal{U}~s.t.O_{fx}\cap_{}^{}O_{fy}=\varnothing{},f^{-1}[O_{x}]=U_{x} ,f^{-1}[O_{y}]=U_{y}$,$设U_{x}\cap_{}^{}U_{y}=V$,$则f[V]\subset{}O_{fx},f[V]\subset{}O_{fy}$，$所以$$f[V]=\varnothing{}$。$所以V=\varnothing{}。$
 10 Def 由于弱$^{*}-$拓扑对连续性的保证，可以定义$Gel'fand$变换 $V:\mathfrak{A}\rightarrow{}(\Delta{}(\mathfrak{A}))',a\mapsto{}\check{a},\check{a}(\chi{}):=\chi{}(a),\forall{}\chi{}\in{}\Delta{}(\mathfrak{A})$。
 11 Thm $Gel'fand$变换是一个代数同构，且具有下列性质
1. $Ran(\check{a})=\sigma{}(a)$,
2. $||\check{a}||:=\mathop{sup}\limits_{\chi{}\in{}\Delta{}(\mathfrak{A})}^{}|\check{a}(\chi{})|=r(a)$,
3. $img(V)将\Delta{}(\mathfrak{A})的点分离。$
 12 Cor 含幺交换巴那赫代数的谱空间在$Gel'fand$拓扑下是豪斯道夫空间。
 13 Thm 如果$\mathfrak{A}$是一个含幺交换$C^{*}-$代数，则$Gel'fand$变换是一个保度规同构变换。
$对于C^{*}-代数，||a^{2n}||^{1/2n}=||a||，所以||\check{a}||=r(a)=||a||$。
 14 Cor 每一个紧致的豪斯道夫空间$X$成为一个含幺交换$C^{*}-$代数$\mathfrak{A}$的谱空间，特别的$\mathfrak{A}=C(X),\Delta{}(\mathfrak{A})=X$。
## 柱函数
设 $C(\bar{\mathfrak{A}}_{\alpha{}})$ 是 $\bar{\mathfrak{A}}_{\alpha{}}$ 上全体连续复函数的集合，称 $f_{a}\in{}C(\bar{\mathfrak{A}}_{\alpha{}})，f_{\alpha{}'}\in{}C(\bar{\mathfrak{A}}_{\alpha{}'})$ 为等价的若$P_{\alpha{}''\alpha{}}^{*}f_{\alpha{}}=P^{*}_{\alpha{}''\alpha{}'}f_{\alpha{}'},\forall{}\alpha{},\alpha{}'\prec{}\alpha{}''$。这里拉回的含义是 $P^{*}_{\alpha{}''\alpha{}}f_{\alpha{}}(A_{\alpha{}''})=f_{\alpha{}}(P_{\alpha{}''\alpha{}}A_{\alpha{}''})$，也就是它们俩等价当且仅当从任意一个更大的包含它们俩的图群胚过来一个构型后，作用上去的结果相同。要实现这种等价，这俩函数的非平凡的作用域就要相等，且这个唯一的非平凡作用域是两个群胚 $\alpha{}$ 和 $\alpha{}'$ 的共同子群胚。由此可以定义投影极限 ${\rm lim}\bar{\mathfrak{A}}$ 的柱函数空间 $Cyl(\bar{\mathfrak{A}}):=[\cup^{}_{\alpha{}}C(\bar{\mathfrak{A}}_{\alpha{}})]/\sim{}$。
通过投影到共同有定义的群胚上，柱函数的元素可以定义代数运算和 $^{*}$ 运算，从而构成一个$^{*}-$代数，定义它的上确界范数：$||f||:=\mathop{sup}\limits_{A_{\alpha{}}\in{}\bar{\mathfrak{A}}_{\alpha{}}}^{}|f_{\alpha{}}(A_{\alpha{}})|$，该范数满足 $||f\bar{f}||=||f||^{2}$，因此以生成的度规进行完备化后的 $\bar{Cyl(\bar{\mathfrak{A}})}$ 可定义一个含幺交换 $C^{*}-$代数。
由于含幺交换 $C^{*}-$代数可以通过度规同构认同为它的谱空间上的连续函数空间，所以量子构型空间就是柱函数生成的 $C^{*}-$代数的谱空间，因此柱函数生成的 $C^{*}-$ 代数同构于 $\mathfrak{\bar{A}}'$，也就是量子构型空间的对偶空间。
## 运动学希尔伯特空间
对于一个群胚 $\alpha{}$，它不同边上的量子构型空间可以认同为对称群，因此每一个边上面都有一个海尔测度，称归一化的海尔测度的直积 $d\mu{}_{\alpha{}}=d\mu{}_{e_{1}}...d\mu{}_{e_{N_{\alpha{}}}}$ 为群胚 $\alpha{}$ 的**柱一致测度**。由于
$$
\begin{eqnarray}
\int_{\bar{\mathfrak{A}_{\alpha{}}'}}^{}(P^{*}_{\alpha{}'\alpha{}}f_{\alpha{}})d\mu{}_{\alpha{}'}
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}'}}^{}f_{\alpha{}}(A(e_{1}),...,A(e_{N_{\alpha{}}}))d\mu{}_{e_{1}}...d\mu{}_{e_{N_{\alpha{}'}}}\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}'}}^{}f_{\alpha{}}(A(e_{1}),...,A(e_{N_{\alpha{}}}))d\mu{}_{e_{1}}...d\mu{}_{e_{N_{\alpha{}}}}\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(A(e_{1}),...,A(e_{N_{\alpha{}}}))d\mu{}_{e_{1}}...d\mu{}_{e_{N_{\alpha{}}}}\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}d\mu{}_{\alpha{}}
\end{eqnarray}
$$
 所以对于一个投影族，同一柱函数在不同群胚的积分相等，即柱一致测度是柱一致的。量子构型空间认同为投影极限空间后，被柱一致测度诱导的测度称为**阿什塔卡-莱万测度**。
 容易证明阿什塔卡-莱万测度在内部变换和空间微分同胚变换下不变：
$$
\begin{eqnarray}
&&\int_{\bar{\mathfrak{A}}}^{}g\circ{}fd\mu{}\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(g^{-1}(t(e_{1}))A(e_{1})g(s(e_{1})),...,g^{-1}(t(e_{N_{\alpha{}}}))A(e_{N_{\alpha{}}}))g(s(e_{N_{\alpha{}}}))d\mu{}_{e_{1}}(A(e_{1}))...d\mu{}_{e_{N_{\alpha{}}}}(A(e_{N_{\alpha{}}}))\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(A(e_{1})g(s(e_{1})),...,A(e_{N_{\alpha{}}}))g(s(e_{N_{\alpha{}}}))d\mu{}_{e_{1}}(g(t(e_{1}))A(e_{1}))...d\mu{}_{e_{N_{\alpha{}}}}(g(t(e_{N_{\alpha{}}}))A({e_{N_{\alpha{}}}}))\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(A(e_{1}),...,A(e_{N_{\alpha{}}}))d\mu{}_{e_{1}}(A(e_{1}))...d\mu{}_{e_{N_{\alpha{}}}}(A({e_{N_{\alpha{}}}}))\\
&=&\int_{\bar{\mathfrak{A}}}^{}fd\mu{}
\end{eqnarray}
$$
所以该测度在内部变换下是不变的，又因为
$$
\begin{eqnarray}
&&\int_{\mathfrak{\bar{A}}}^{}\varphi{}\circ{}fd\mu{}\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(A(\varphi{}[e_{1}]),...,A(\varphi{}[e_{N_{\alpha{}}}]))d\mu{}_{\varphi{}[e_{1}]}(A(\varphi{}[e_{1}]))...d\mu{}_{\varphi{}[e_{N_{\alpha{}}}]}(A({\varphi{}[e_{N_{\alpha{}}}]}))\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(A(e_{1})\cdot{}A(\varphi{}[e_{1}])^{-1}\cdot{}A(\varphi{}[e_{1}]),...,A(e_{N_{\alpha{}}})\cdot{}A(\varphi{}[e_{N_{\alpha{}}}])^{-1}\\
&&\cdot{}A(\varphi{}[e_{N_{\alpha{}}}]))d\mu{}_{\varphi{}[e_{1}]}(A(e_{1})\cdot{}A(\varphi{}[e_{1}])^{-1}\cdot{}A(\varphi{}[e_{1}]))...d\mu{}_{\varphi{}[e_{N_{\alpha{}}}]}(A(e_{N_{\alpha{}}})\cdot{}A(\varphi{}[e_{N_{\alpha{}}}])^{-1}\cdot{}A(\varphi{}[e_{N_{\alpha{}}}]))\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(A(e_{1}),...,A(e_{N_{\alpha{}}}))d\mu{}_{\varphi{}[e_{1}]}(A(e_{1}))...d\mu{}_{\varphi{}[e_{N_{\alpha{}}}]}(A(e_{N_{\alpha{}}}))\\
&=&\int_{\bar{\mathfrak{A}_{\alpha{}}}}^{}f_{\alpha{}}(A(e_{1}),...,A(e_{N_{\alpha{}}}))d\mu{}_{[e_{1}}(A(e_{1}))...d\mu{}_{e_{N_{\alpha{}}}}(A(e_{N_{\alpha{}}}))\\
&=&\int_{\mathfrak{\bar{A}}}^{}fd\mu{}
\end{eqnarray}
$$
所以该测度在空间微分同胚变换下也是不变的。

有了良好的测度，就可以在 $\bar{Cyl(\bar{\mathfrak{A}})}$ 上定义内积，也就是 $\langle f|f'\rangle:=\int_{\bar{\mathfrak{A}}_{\alpha{}''}}^{}(P^{*}_{\alpha{}''\alpha{}}\bar{f}_{\alpha{}})(P^{*}_{\alpha{}''\alpha{}'}{f}_{\alpha{}'}')d\mu{}_{\alpha{}''}$。可以证明 $\bar{Cyl(\bar{\mathfrak{A}})}$ 以内积 $\langle\cdot{}|\cdot{}\rangle$ 形成一个希尔伯特空间，称为**运动学希尔伯特空间**，记作$\mathscr{H}_{kin}=L^{2}(\bar{\mathfrak{A}},d\mu{})$。
# 运动学希尔伯特空间的自旋网络分解
## 单边的自旋-网络分解
测度那一节证明过彼得外耳定理，这个定理可以把运动学希尔伯特空间进行自旋-网络分解。以一条边上的运动学希尔伯特空间为例，它同构于 $L^{2}(SU(2),d\mu{}_{H})$，而后者的基矢由彼得外耳定理给出，为全体不可约表示的魏格纳矩阵元函数，因此定义
 $$
\begin{equation}
\psi{}^{(j)}_{mn}:=\sqrt{ 2j+1 }\pi{}^{(j)}_{mn}
\end{equation}
$$
为自旋-网络基矢。它们满足在海尔测度定义的内积意义下正交归一化条件，且能够张成整个单边希尔伯特空间。除了基矢外，还可以定义作用到运动学希尔伯特空间上的算符，首先可以定义构型算符，也就是乘法算符
$$
\begin{eqnarray}
\hat{f}(A(e)):L^{2}(SU(2),d\mu{})的稠密子集&\rightarrow{}&L^{2}(SU(2),d\mu{})的稠密子集,
\nonumber\\
\psi{}(A(e))&\mapsto{}&f(A(e))\psi{}(A(e))
\end{eqnarray}
$$
由于运动学希尔伯特空间可以用自旋-网络基矢展开，所以自然的可以定义规范群的生成元对应的算符。在一个李群中，生成元分为两种，左不变生成元和右不变生成元，它们分别生成李群的左不变矢量场和右不变矢量场，对于左不变矢量场的定义式
$$
\begin{equation}
L_{g*}\bar{A}
=\bar{A}
\end{equation}
$$
两边都取 $g$ 点可以得到
$$
\begin{eqnarray}
L_{g*}\bar{A}_{e}
&=&\bar{A}_{g}
\nonumber\\
L_{g*}\frac{d}{dt}|_{t=0}e^{\bar{A}t}
&=&\bar{A}_{g}
\nonumber\\
\frac{d}{dt}|_{t=0}L_{g}(e^{\bar{A}t})&=&\bar{A}_{g}
\nonumber\\
(\frac{d}{dt}ge^{\bar{A}t})_{g}&=&\bar{A}_{g}
\end{eqnarray}
$$
因此左不变矢量场其实就是 $e^{\bar{A}t}$ 被左平移后的切矢量场，右不变矢量场同理可得，假设右不变矢量场用波浪号代替，则有
$$
\begin{equation}
\tilde{B}_{g}
=(\frac{d}{dt}e^{\tilde{B}t}g)|_{g}
\end{equation}
$$
因此任何一个原点处的切矢都可以通过左平移或者右平移的方式得到左不变或者右不变矢量场。也就是左不变和右不变矢量场在原点处的生成元是相同的，但是它们的对易子却不一样。假如左不变矢量场的一组基底记作 $l_{\mu{}}$，其对易子满足 $[l_{\mu{}},l_{\nu{}}]=c_{\mu{}\nu{}}{}^{\alpha{}}l_{\alpha{}}$，则右不变矢量场切矢与左不变矢量场在原点处对应切矢相同的那组基底记作 $r_{\mu{}}$，计算其李代数：
$$
\begin{eqnarray}
[r_{\mu{}},r_{\nu{}}]
&=&\mathcal{L}_{r_{\mu{}}}r_{\nu{}}
\nonumber\\
&=&\mathcal{L}_{r_{\mu{}}}(L^{*}_{e^{tr_{\mu{}}}}R_{e^{tr_{\mu{}}}*}r_{\nu{}})
\nonumber\\
&=&\frac{d}{dt}\mathbf{ad}_{e^{-tr_{\mu{}}}}r_{\nu{}}
\nonumber\\
&=&c_{\nu{}\mu{}}{}^{\alpha{}}r_{\alpha{}}
\end{eqnarray}
$$
因此它们的对易子差一个负号。定义它们所对应的算符的时候，为了有一致的对易关系，定义**左不变矢量场算符**
$$
\begin{eqnarray}
\hat{L}^{(\xi{})}:C^{1}(SU(2))&\rightarrow{}&C^{0}(SU(2))
\nonumber\\
\psi{}(A(e))&\mapsto{}&\frac{d}{dt}|_{t=0}\psi{}(A(e)e^{t\xi{}})
\end{eqnarray}
$$
和**右不变矢量场算符**
$$
\begin{eqnarray}
\hat{R}^{(\xi{})}:C^{1}(SU(2))&\rightarrow{}&C^{0}(SU(2))
\nonumber\\
\psi{}(A(e))&\mapsto{}&\frac{d}{dt}|_{t=0}\psi{}(A(e)e^{-t\xi{}})
\end{eqnarray}
$$
具体的，使用嘉当度规 $\tau{}_{i}$ 把它们的基矢定义为**角动量算符**
$$
\begin{equation}
\hat{J}^{(L)}_{i}
:=i\hat{L}^{(\tau{}_{i})},
\qquad
\hat{J}^{(R)}_{i}:=i\hat{R}^{(\tau{}_{i})}
\end{equation}
$$
右不变矢量场算符定义时的负号可以保证下列的对易关系
$$
\begin{equation}
[\hat{J}^{(L)}_{i},\hat{J}^{(L)}_{j}]
=i\epsilon{}_{ij}{}^{k}\hat{J}^{(L)}_{k},
\qquad
[\hat{J}^{(R)}_{i},\hat{J}^{(R)}_{j}]
=i\epsilon{}_{ij}{}^{k}\hat{J}^{(R)}_{k}
\end{equation}
$$
和
$$
\begin{equation}
[\hat{J}^{(L)}_{i},\hat{J}^{(R)}_{j}]
=0
\end{equation}
$$
然后可以定义**平方动量算符**也就是 $su(2)$ 的卡西米尔算符
$$
\begin{equation}
\hat{J}^{2}:=\delta{}^{ij}\hat{J}^{(L)}_{i}\hat{J}^{(L)}_{j}
\end{equation}
$$
由于
$$
\begin{eqnarray}
\hat{J}^{2}\psi{}(A(e))
&=&\psi{}(-A(e)(\tau{}_{1}^{2}+\tau{}_{2}^{2}+\tau{}_{3}^{2}))\\
&=&\psi{}(-(\tau{}_{1}^{2}+\tau{}_{2}^{2}+\tau{}_{3}^{2})A(e))\\
&=&\delta{}^{ij}\hat{J}^{(R)}_{i}\hat{J}^{(R)}_{j}\psi{}(A(e))
\end{eqnarray}
$$
所以 $\hat{J}^{2}$ 也可以写成右不变矢量场算符的形式。

考虑 $SU(2)$ 的不可约表示空间和它的对偶空间的张量积空间 $\mathcal{H}_{j}\otimes{}\mathcal{H}^{*}_{j}$，其中的元素有自然的对 $\mathcal{H}^{j}$ 的作用
$$
\begin{equation}
v^{m}\otimes{}\omega{}^{*n}(v^{l})
:=v^{m}\omega{}^{*n}(v^{l})
\end{equation}
$$
从而成为 $\mathcal{H^{j}}$ 上的线性算符。此外，$\mathcal{H}_{j}\otimes{}\mathcal{H}^{*}_{j}$ 上还有自然的 $SU(2)$ 的左作用和右作用，利用这些性质可以建立起 $\mathcal{H}_{j}\otimes{}\mathcal{H}^{*}_{j}$ 和 $\rho{}^{(j)}_{mn}$ 之间的同构关系，同构映射为
$$
\begin{eqnarray}
\phi{}:\mathcal{H}_{j}\otimes{}\mathcal{H}^{*}_{j}
&\rightarrow{}&\rho{}^{(j)}_{mn}
\nonumber\\
v^{m}\otimes{}\omega{}^{*n}&\mapsto{}&\sqrt{ 2j+1 }\pi{}^{(j)}_{mn}
\end{eqnarray}
$$
因此最终可以得到 $L^{2}(SU(2),d\mu{})=\oplus_{j}[\mathcal{H}_{j}\otimes{}\mathcal{H}_{j}^{*}]$。也就是 $L^{2}(SU(2),d\mu{})=\oplus_{j}\{\{\pi{}^{j}_{mn}\}\}=\oplus_{j}[\mathcal{H}_{j}\otimes{}\mathcal{H}_{j}^{*}]$。
根据角动量算符的定义容易证明
$$
\begin{equation}
\hat{J}^{2}\pi{}^{i}_{mn}=j(j+1)\pi{}^{j}_{mn},
\qquad
\hat{J}_{3}^{(L)}\pi{}^{j}_{mn}=m\pi{}^{j}_{mn},
\qquad
\hat{J}_{3}^{(R)}\pi{}^{j}_{mn}=n\pi{}^{j}_{mn}
\end{equation}
$$
只需要注意 $-\tau{}_{i}=\tau{}_{i}^{\dagger}$ 即可。
## 有限图和运动学希尔伯特空间的自旋-网络分解
 一条边的自旋-网络分解推广到有限图只需要把单边的表示扩展为张量积即可，从而得到有限图的希尔伯特空间，在此基础上可以先定义有限图构的型算符
$$
\begin{equation}
\hat{f}(A(e_{i})):\psi{}_{\alpha{}}(A(e_{1})...A(e_{N_{\alpha{}}})):=f(A(e_{i}))\psi{}(A(e_{1})...A(e_{N_{\alpha{}}}))
\end{equation}
$$
然后定义动量算符
$$
\begin{equation}
\hat{J}_{i}^{(e,v)}:=(1\otimes{}...\otimes{}\hat{J}_{i}\otimes{}...\otimes{}1)
\end{equation}
$$
其中$\hat{J}_{i}=\hat{J}_{i}^{(L)}$ 如果  $v=s(e)$，$\hat{J}_{i}=\hat{J}_{i}^{(R)}$ 如果 $v=t(e)$，$\hat{J}_{i}=0$，其它情况。当然还可以定义顶点的总角动量算符$[\hat{J}^{v}]^{2}:=\delta{}^{ij}\hat{J}^{v}_{i}\hat{J}^{v}_{j}$，其中$\hat{J}^{v}_{i}=\sum\limits_{e'~at~v}^{}\hat{J}_{i}^{(e',v)}$。
由于
$$
\begin{eqnarray}
\mathcal{H}_{\alpha{}}
&=&\otimes{}_{e}\mathcal{H}^{e}\\
&=&\otimes{}_{e}[\oplus{}_{j}(\mathcal{H}^{e}_{j}\otimes{}\mathcal{H}^{e*}_{j})]\\
&=&\oplus_{j}[\otimes{}_{e}(\mathcal{H}^{e}_{j}\otimes{}\mathcal{H}^{e*}_{j})]
\end{eqnarray}$$
所以 $\mathcal{H}_{\alpha{}}=\oplus{}_{j}[\oplus_{l}\mathcal{H}_{\alpha{},j,l}]$，其中 $\mathcal{H}_{\alpha{},j,l}=\otimes{}_{v}\mathcal{H}^{v}_{j(v),l}$，而 $[\hat{J}^{e}]^{2}\mathcal{H}^{v}_{j(v),l}=j(v)(j(v)+1)\mathcal{H}^{v}_{j(v),l}$，$[\hat{J}^{v}]^{2}\mathcal{H}^{v}_{j(v),l}=l(l+1)\mathcal{H}^{v}_{j(v),l}$。如果有两个群胚 $\alpha{}$ 和 $\alpha{}'$，它们在时空流形上的承担集不重合，比如群胚 $\alpha{}$ 有边 $e$ 而群胚 $\alpha{}'$ 没有，这样的话可以看作群胚 $\alpha{}'$ 上的边 $e$ 的自旋为零，也就是处于平凡表示。这样的话很容易使用前面定义的阿什塔卡-莱万测度来证明两个非平凡的边的承担集不完全重合的群胚的的自旋-网络态互相正交。进一步的，动力学希尔伯特空间的所有非平凡态可以分解为所有子群胚的非平凡态的直和，再考虑平凡态后，总的分解就变成了
$$
\begin{equation}
\mathcal{H}_{kin}
=\oplus_{\alpha{}\in{}\mathcal{L}}\mathcal{H}'_{\alpha{}}
\oplus{}\mathbb{C}
\end{equation}
$$
其中带撇的意思是说只考虑对应群胚上每个边都是非平凡表示的子空间。有了这个分解后，运动学希尔伯特空间的基矢是很清楚的，定义其归一化的基态和激发态为
$$
\begin{equation}
\Pi{}_{0}:=\Omega{}=1,
\qquad
\Pi{}_{s}:=\mathop{\Pi{}}\limits_{e\in{}E(\gamma{}(s))}^{}\sqrt{ 2j_{e}+1 }\pi{}^{j_{e}}_{m_{e}n_{e}}
\end{equation}
$$
其中 $s=(\gamma{}(s),\mathbf{j_{s}},\mathbf{m_{s}},\mathbf{n_{s}})$，全体$s$的集合记作$S$。这些基矢满足 $\langle\Pi{}_{s}|\Pi{}_{s'}\rangle_{kin}=\delta{}_{ss'}$。这样就得到了运动学希尔伯特空间的自旋-网络分解。
由于运动学希尔伯特空间的态可以用集合 $S$ 中的元素来标记，每个运动学希尔伯特空间中的态 $\Psi{}$ 可以看作一个一个从 $S$ 到 $\mathbb{C}$ 的函数 $\tilde{\Psi{}}$，也就是柱函数的**自旋-网络表示**。它的具体定义为
$$
\begin{eqnarray}
\tilde{\Psi{}}:S&\rightarrow{}&\mathbb{C}
\nonumber\\
s&\mapsto{}&\langle\Pi{}_{s}|\Psi{}\rangle_{kin}
\end{eqnarray}
$$
这些函数所在的空间记作 $\tilde{\mathcal{H}}$，其上配备的内积为
$$
\begin{equation}
\langle\tilde{\Psi{}}|\tilde{\Psi'{}}\rangle:=\mathop{\sum\limits_{}^{}}\limits_{s\in{}S}^{}\bar{\tilde{\psi{}}(s)}\tilde{\Psi'{}}(s)
\end{equation}
$$
由于柱函数的表示和自旋-网络表示是运动学希尔伯特空间的两个表示，所以关联这两个表示的变换，也就是**自旋-网络变换**
$$
\begin{eqnarray}
T:\mathcal{H}_{kin}&\rightarrow{}&\tilde{\mathcal{H}}
\nonumber\\
\Psi{}&\mapsto{}&\tilde{\Psi{}}(s)
\end{eqnarray}
$$
就是一个幺正变换。
# 和乐-通量代数和量子算符
## 经典和乐-通量泊松代数
量子构型空间是边上的和乐，是联络在一维边上抹匀的结果，抹匀后的和乐在规范变换和微分同胚变换下是不变的，运动学希尔伯特空间是它们的平方可积函数张成的。为了与这种理念一致，对标架也进行抹匀，并得到一个微分同胚不变的量，也就是定义标架场穿过一个二维面 $S$ 的**通量**：
$$
\begin{equation}
P_{i}(S):=\int_{S}^{}\epsilon{}_{abc}\tilde{P}^{c}_{i}
\end{equation}
$$
通量是微分同胚不变的，虽然它在规范变换下按照矢量变换，但是它的模长是不变的，而后面可以看到它的模长与面积有关，才是真正的可观测量。

要把通量提升为量子算符，就必须先得到它和量子构型空间的经典对应的泊松代数，而量子构型空间是和乐的平方可积空间，根据泊松括号的性质，容易得到
$$
\begin{equation}
\{P_{i}(S),f(A(e)\}=\frac{\partial{}f}{\partial{}A(e)_{mn}}\{P_{i}(S),A(e)_{mn}\}
\end{equation}
$$
因此只需要得到经典的**和乐-通量泊松代数**即可。由于已有的泊松代数是联络和标架的，所以需要先计算抹匀函数与原式基本变量之间的泊松代数，先计算它们各自对被抹匀变量的泛函导数。对于 $\frac{\delta{}A_{e}}{\delta{}{A}^{i}_{a}(x)}$，有 
$$  
\begin{eqnarray}  
\frac{\delta{}A_{e}}{\delta{}A^{i}_{a}(x,\lambda{}’)}
&=&\delta{}^{3}(0)\frac{\partial{}A_{e}}{\partial{}A^{i}_{a}(x,\lambda{}’)}\\  
&=&\delta{}^{3}(0)\mathop{lim}\limits_{\epsilon{}\rightarrow{}0}^{}\frac{\partial{}A(1,\lambda{}’-\epsilon{})A(\lambda{}’-\epsilon{},\lambda{}’+\epsilon{})A(\lambda{}’+\epsilon{},0)}{\partial{}A^{i}_{a}(x,\lambda{}’)}\\  
&=&\delta{}^{3}(0)A(1,\lambda{}’-\epsilon{})\mathop{lim}\limits_{\epsilon{}\rightarrow{}0}^{}\frac{\partial{}A(\lambda{}’-\epsilon{},\lambda{}’+\epsilon{})}{\partial{}A^{i}_{a}(x,\lambda{}’)}A(\lambda{}’+\epsilon{},0)\\  
&=&\delta{}^{3}(0)A(1,\lambda{}’)\mathop{lim}\limits_{\epsilon{}\rightarrow{}0}^{}\frac{\partial{}\mathcal{P}e^{-\int_{\lambda{}’-\epsilon{}}^{\lambda{}’+\epsilon{}}A^{j}_{b}(s)\tau{}_{i}\dot{e}_{j}(s)ds}}{\partial{}A^{i}_{a}(x,\lambda{}’)}A(\lambda{}’,0)\\  
&=&\delta{}^{3}(0)A(1,\lambda{}’)\mathop{lim}\limits_{\epsilon{}\rightarrow{}0}^{}\frac{\partial{}\mathcal{P}e^{-A^{j}_{b}(\lambda{}’)\int_{\lambda{}’-\epsilon{}}^{\lambda{}’+\epsilon{}}\tau{}_{j}\dot{e}^{b}(s)ds}}{\partial{}A^{i}_{a}(x,\lambda{}’)}A(\lambda{}’,0)\\  
&=&\delta{}^{3}(0)A(1,\lambda{}’)\mathop{lim}\limits_{\epsilon{}\rightarrow{}0}^{}[-\int_{\lambda{}’-\epsilon{}}^{\lambda{}’+\epsilon{}}\tau{}_{i}\dot{e}^{a}(s)ds]A(\lambda{}’,0)\\  
&=&\delta{}^{3}(0)[-A(1,\lambda{}’)\int_{\lambda{}_{s}}^{\lambda{}_{t}}\delta{}_{x(e(s)),(x,\lambda{}’)}\tau{}_{i}\dot{e}^{a}(s)ds]A(\lambda{}’,0)\\  
&=&-A(1,\lambda{}’)\int_{\lambda{}_{s}}^{\lambda{}_{t}}\delta{}^{3}((x,\lambda’{})-x(e(s)))\tau{}_{i}\dot{e}^{a}(s)dsA(\lambda{}’,0)
\end{eqnarray}  
$$
所以有  $\frac{\delta{}A_{e}}{\delta{}A^{i}_{a}(x,\lambda{})}=-\int_{0}^{1}\delta{}^{3}(x(e(s))-(x,\lambda{}))\dot{e}^{a}A(1,\lambda{})\tau{}_{i}A(\lambda{},0)ds$  。而对于 $\frac{\delta{}P_{i}}{\tilde{P}^{a}_{J}(x)}$，则有
$$
\begin{eqnarray}
&&\frac{\delta{}P_{i}}{\delta{}\tilde{P}^{a}_{j}(x)}\\
&=&\delta{}^{3}(0)\int_{S}^{}\eta{}_{bda}\delta{}^{j}_{i}\delta{}_{p,p^{-1}(x)}\\
&=&\int_{S}^{}\eta{}_{bda}\delta{}^{j}_{i}\delta{}^{3}(p-p^{-1}(x))  
\end{eqnarray}
$$
也就是 $\frac{\delta{}P_{i}}{\delta{}\tilde{P}^{a}_{j}}=\delta{}^{j}_{i}\int_{S}^{}\eta{}_{abd}\delta{}^{3}(p-p^{-1}(x))$ 。有了这两个关系后，就可以计算和乐-通量泊松代数： 
$$
\begin{eqnarray}
\{P_{i}(S),A(e)\}&=&\int_{}^{}d^{3}x(\frac{\delta{}P_{i}(S)}{\delta{}A^{j}_{a}(x)}\frac{\delta{}A(e)}{\delta{}\tilde{P}^{a}_{j}(x)}-\frac{\delta{}P_{i}(S)}{\delta{}\tilde{P}^{a}_{j}(x)}\frac{\delta{}A(e)}{\delta{}A^{j}_{a}(x)})\\
&=&-\int_{}^{}d^{3}x\frac{\delta{}P_{i}(S)}{\delta{}\tilde{P}^{a}_{j}(x)}\frac{\delta{}A(e)}{\delta{}A^{j}_{a}(x)}\\
&=&\int_{}^{}d^{3}x\delta{}^{j}_{i}\int_{S}^{}\eta{}_{abd}\delta{}^{3}(p-p^{-1}(x))\int_{0}^{1}\delta{}^{3}(x(e(s))-x)\dot{e}^{a}A(1,\lambda{}(x^{3}))\tau{}_{j}A(\lambda{}(x^{3}),0)ds\\
&=&\int_{}^{}d^{3}x\int_{S}^{}\eta{}_{abd}\delta{}^{3}(p-p^{-1}(x))\int_{0}^{1}\delta{}^{3}(x(e(s))-x)\dot{e}^{a}A(1,\lambda{}(x^{3}))\tau{}_{i}A(\lambda{}(x^{3}),0)ds\\
&=&\int_{S}^{}\eta{}_{abd}\int_{0}^{1}\delta{}^{3}(x(e(s))-x)\dot{e}^{a}A(1,\lambda{}(x^{3}))\tau{}_{i}A(\lambda{}(x^{3}),0)ds\\
&=&\int_{S}^{}d^{2}xn_{a}\int_{0}^{1}\delta{}^{3}(x(e(s))-x)\dot{e}^{a}A(1,s)\tau{}_{i}A(s,0)ds
\end{eqnarray}
$$
 结果为 $\{P_{i}(S),A(e)\}=\int_{S}^{}n_{a}(x)d^{2}x\int_{0}^{1}\delta^{3}{}(x(e(s))-x)\dot{e}^{a}A(1,\lambda{})\tau{}_{i}A(\lambda{},0)d\lambda{}$。
 在最终表示通量与和乐的平方可积函数的泊松代数前，先定义一个面 $S$ 和一个边的 $e$ 符号函数$\sigma{}(S,e)$为
$$
\begin{align*}\begin{split}\sigma{}(S,e) = \left \{\begin{array}{ll}
1,&e\cap_{}^{}S=\{p\},边在面上面 \\
-1,& e\cap_{}^{}S=\{p\},边在面下面\\
0,&\dot{e}^{a}n_{a}|_{p}=0,\forall{}p\in{}M
\end{array}\right.\end{split}\end{align*}
$$
 这里的 “上面” 和 “下面” 指面的定向也就是其法矢所给出的那个上下，是绝对的，与边的定向无关。然后就可以证明：若面和边只相交于的起点或终点，则
$$
\{P_{i}(s),f(A(e))\}=[\frac{\partial{}f(A(e))}{\partial{}A(e)_{mn}}]\frac{\sigma{}(S,e)}{2}\cdot{}\begin{align*}\begin{split}\left\{\begin{array}{ll}[\tau{}_{i}A(e)]_{mn}，p=s(e)\\
-[A(e)\tau{}_{i}]_{mn}，p=t(e)
\end{array}\right.\end{split}\end{align*}
$$
简单证明下，设 $\dot{e}^{a}n_{a}|_{p}=cos\theta{}$，则 $ds|_{p}=\frac{dy}{cos\theta{}}|_{p}$，其中 $\{x^{1},x^{2},y\}$ 是一个直角坐标系。设 $ds=f(y)dy$，$f(y(p))=\frac{1}{cos\theta{}}$ 因此
$$
\begin{eqnarray}
\{P_{i}(S),A(e)\}
&=&\int_{S}^{}d^{2}x\int_{y(s)}^{y(t)}\delta^{3}{}(y-x^{3})cos\theta{}A(1,\lambda{}(y))\tau{}_{i}A(\lambda{}(y),0)f(y)dy\\
&=&\frac{1}{2}{\rm sign}[y(t)-y(s])A(1,\lambda{}(p))\tau{}_{i}A(\lambda{}(p),0)cos\theta{}f(y(p))\\
&=&\frac{1}{2}{\rm sign}[y(t)-y(s])A(1,\lambda{}(p))\tau{}_{i}A(\lambda{}(p),0)
\end{eqnarray}
$$
## 量子和乐-通量代数
有了经典泊松代数后，就可以把通量提升为量子算符，也就是定义**通量算符**
$$
\begin{equation}
\hat{P}_{i}(S):C^{1}(\mathfrak{\bar{A}})\rightarrow{}C(\bar{\mathfrak{A}})，\psi{}\mapsto{}i\hbar{}\{P_{i}(S),\psi{}\}
\end{equation}
$$
此外定义图的**构型算子**，也就是**乘法算子**
$$
\begin{equation}
\hat{f}_{\gamma{}'}\psi{}_{\gamma{}}=f_{\gamma{}'}\psi{}_{\gamma{}}
\end{equation}
$$
后者的作用就是数乘，推导一下前者的作用，把它直接作用到态上
$$
\begin{eqnarray}
\hat{P}_{i}(S)\psi{}_{\gamma{}}&=&\frac{i\hbar{}}{2}\sum\limits_{v\in{}V(\gamma{})\cap_{}^{}S}^{}\sum\limits_{e\in{}\gamma{}}^{}\sigma{}(S,e_{I})\frac{\partial{}\psi{}_{i}}{\partial{}A(e_{I})_{mn}}\begin{split}\left\{\begin{array}{ll}[\tau{}_{i}A(e_{I})]_{mn}\\
-[A(e_{I})\tau{}_{i}]_{mn}\end{array}\right.\end{split}\\
&=&\frac{i\hbar{}}{2}\sum\limits_{v\in{}V(\gamma{})\cap_{}^{}S}^{}\sum\limits_{e\in{}\gamma{}}^{}\sigma{}(S,e_{I})\frac{\hat{J}_{i}^{(e_{I},v)}}{i}\psi{}_{\gamma{}}\\
&=&\frac{\hbar{}}{2}\sum\limits_{v\in{}V(\gamma{})\cap_{}^{}S}^{}\sum\limits_{e\in{}\gamma{}}^{}\sigma{}(S,e_{I})\hat{J}^{(e_{I},v)}_{i}\psi{}_{\gamma{}}
\end{eqnarray}
$$
所以得到 $\hat{P}_{i}(S)\psi{}_{\gamma{}}=\frac{\hbar{}}{2}\sum\limits_{v\in{}V(\gamma{})\cap_{}^{}S}^{}\sum\limits_{e\in{}\gamma{}}^{}\sigma{}(S,e_{I})\hat{J}^{(e_{I},v)_{i}}\psi{}_{\gamma{}}$。有了对态的作用后，就可以计算它们的对易括号，乘法算子的作用是阿贝尔的，所以自然的有
$$
\begin{equation}
[\hat{f},\hat{f}']
=0
\end{equation}
$$
至于这两种算子的对易关系，也可以容易的看出来，即
$$
\begin{equation}
[\hat{P}_{i}(S),\hat{f}_{e}]=\hat{P}_{i}(S)f_{e}
\end{equation}
$$
至于两个面的通量算符的对易关系，可以计算为
$$
[\hat{P}_{i}(S),\hat{P}_{j}(S')]f_{e}=\frac{\hbar{}^{2}}{4}\sum\limits_{v\in{}\gamma{}\cap_{}^{}S,v'\in{}\gamma{}\cap_{}^{}S'}^{}\sigma{}(S,e)\sigma{}(S',e)[\hat{J}_{i}^{(e,v)},\hat{J}_{j}^{(e,v')}]f_{e}
$$
当 $v=v'$ 且同为终点或同为起点时，上面对易不为 $0$，此时 $\hat{J}^{S}=\hat{J}^{S'}$，则
$$
\begin{eqnarray}
[\hat{P}_{i}(S),\hat{P}_{j}(S')]f_{e}
&=&\frac{\hbar{}^{2}}{4}\sum\limits_{v\in{}\gamma{}\cap_{}^{}S}^{}\sigma{}(S,e)\sigma{}(S',e)i\epsilon{}^{k}_{ij}\hat{J}_{k}^{(e,v)}f_{e}\\
&=&\frac{i\hbar{}}{2}\sigma{}(S',e)\epsilon{}^{k}_{ij}\frac{\hbar{}}{2}\sum\limits_{v\in{}\gamma{}\cap_{}^{}S}^{}\sigma{}(S,e)\hat{J}_{k}^{(e,v)}f_{e}\\
&=&\frac{i\hbar{}}{2}\sigma{}(S',e)\epsilon{}^{k}_{ij}\hat{P}_{k}(S)f_{e}
\end{eqnarray}
$$
所以最终得到
$$
\begin{equation}
[\hat{P}_{i}(S),\hat{P}_{j}(S')]f_{e}=i\hbar{}\frac{\sigma{}(S',e)}{2}\epsilon{}^{k}_{ij}\hat{P}_{k}(S)f_{e}
\end{equation}
$$
注意这里两个面不要求只有一个交点。
## 面积和体积算子
所有算符最后还是要和我们们熟悉的几何量联系起来，面积和体积是最基本的几何量，经典情形下它们都可以用标架表示。所以下面用通量来构造面积和体积算子。从通量的定义来说，它等于标架在一个二维面上的积分，先在平直空间中理解它的几何意义。设是一个平面，$\tilde{P}^{a}_{i}$ 是一个平直空间中的标架场，则标架场穿过这个面时与面垂直，则标架场在这个面上的积分实际上是标架场的对偶在面上的积分，从而实际上等于与标架场垂直的那两个方向的积分，因此就是面的大小。也就是对于平直时空来说，标架在面上的积分其实等于面的面积在标架的垂直面上的投影。对于一个平直空间的面，它的面积可以表示为
$$
\begin{eqnarray}
S
&=&\int_{\mathbf{s}}^{}d\mathbf{s}
\end{eqnarray}
$$
而它在不同方向的投影可以表示为
$$
\begin{equation}
S^{i}
=\int_{\mathbf{s}}^{}n^{i}d\mathbf{s}
\end{equation}
$$
其中 $n^{i}$ 为其归一化法市场。通常
$$
\begin{eqnarray}
S^{i}S_{i}
&=&(\int_{\mathbf{s}}^{}n^{x}d\mathbf{s})^{2}
+(\int_{\mathbf{s}}^{}n^{y}d\mathbf{s})^{2}
+(\int_{\mathbf{s}}^{}n^{z}d\mathbf{s})^{2}
\nonumber\\
&\neq&(\int_{\mathbf{s}}^{}
d\mathbf{s})^{2}
\nonumber\\
&=&S^{2}
\end{eqnarray}
$$
但是特殊情况，当该面为平面时，法矢可以提到积分号外面去，有
$$
\begin{equation}
S^{i}S_{i}
=S^{2}
\end{equation}
$$
而由于任何弯曲流形局域总可以看作平直的，所以对于一个很小的面元，它的面积可以表示为
$$
\begin{equation}
S
=\kappa{}\beta{}\sqrt{ P_{i}(S)P_{j}(S) \delta{}^{ij}}
\end{equation}
$$
至于一个有限大小的面元，则可以将其剖分为无限个小面元，然后求极限，也就是
$$
\begin{equation}
S
=\kappa{}\beta{}\mathop{{\rm lim}}\limits_{N\rightarrow{}\infty}^{}
\sum\limits_{I=1}^{N}\sqrt{ P_{i}(S_{I}) P_{j}(S_{I})\delta{}^{ij}}
\end{equation}
$$
由此启发可以把量子**面子算子**定义为
$$
\begin{equation}
\hat{A}_{S}:=\mathop{{\rm lim}}\limits_{N\rightarrow{}\infty}^{}[A_{S}]_{N}=\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}\kappa{}\beta{}\sum\limits_{I=1}^{N}\sqrt{ \hat{P}_{i}(S_{I})\hat{P}_{j}(S_{I})\delta{}^{ij} }
\end{equation}
$$
由于
$$
\begin{eqnarray}
\kappa{}\beta{}\sum\limits_{I=1}^{}\sqrt{ \hat{P}_{i}(S_{I})\hat{P}_{j}(S_{I})\delta{}^{ij} }
&=&\frac{8\pi{}\hbar{}G\beta{}}{2}\sum\limits_{I}^{}\sqrt{ \sigma{}^{2}(\hat{J}^{(u)}_{i}-\hat{J}^{(d)}_{i})(\hat{J}^{(u)i}-\hat{J}^{(d)i}) }\\
&=&4\pi{}\beta{}l_{p}^{2}\sqrt{ (\hat{J}^{(u)})^{2}+(\hat{J}^{(d)})^{2}-2\hat{J}^{(u)}\hat{J}^{(d)} }\\
&=&4\pi{}\beta{}l_{p}^{2}\sqrt{ 2(\hat{J}^{(u)})^{2}+2(\hat{J}^{(d)})^{2}-(\hat{J}^{(u)}+\hat{J}^{(d)})^{2} }。
\end{eqnarray}
$$
所以面积算符本征谱为
$$
\begin{equation}
a_{S}=4\pi{}\beta{}l_{p}^{2}\sum\limits_{I}^{}\sqrt{ 2j_{I}^{(u)}(j_{I}^{(u)}+1)+2j_{I}^{(d)}(j_{I}^{(d)}+1)- j_{I}^{(u+d)}(j_{I}^{(u+d)}+1)}
\end{equation}
$$
，其中$j^{(u)}_{I},j^{(d)}_{I}$为第$I$个小面的总的上面或者下面的总角动量，$j_{I}^{(u+d)}$为它们两个的直和表示的角动量。
面积算符完了再考虑体积算符，任何一个三维的封闭图形，都可以通过局域微分同胚变换变为一个平行六面体，所以可以考虑一个很小的在局域平直坐标系下形状为平行六面体的区域。对于平直空间中的一个平行六面体，以其体心为基点，按右手方向做三条棱 $\vec{l}_{a}$ ，其中 $a=1,2,3$。它的分量为 $l^{i}_{a}$，其中 $i=x,y,z$ 为右手直角坐标系的方向。则这三条棱和它们的反向棱 $\vec{l}'_{a}$ 把六面体划分为八个部分。注意 $\vec{l}'_{a}$ 的关系为左手关系。棱 $\vec{l}^{a}$ 所对的那个六面体的面记作 $S^{a}$，则有
$$
\begin{equation}
\vec{S}^{a}
=2\epsilon{}^{abc}\vec{l}_{b}\times{}
\vec{l}_{c}
=-\vec{S}'^{a}
=2\epsilon{}^{abc}\vec{l}_{b}'\times{}\vec{l}_{c}'
\end{equation}
$$
至于它在 $i$ 方向的投影则为
$$
\begin{equation}
\kappa{}\beta{}P_{i}(S^{a})=\vec{S}^{a}_{i}=2\epsilon{}^{abc}\epsilon{}_{ijk}l^{j}_{b}l^{k}_{c}
\end{equation}
$$
整个六面体的体积可以表示为
$$
\begin{equation}
V
=\frac{2}{3}\vec{S}^{a}\vec{l}_{a}
\end{equation}
$$
然后可以计算
$$
\begin{eqnarray}
(\kappa{}\beta{})^{3}\epsilon{}^{ijk}\epsilon{}_{abc}P_{i}(S^{a})P_{j}(S^{b})P_{k}(S^{c})
&=&2\epsilon{}^{ijk}\epsilon{}_{abc}\epsilon{}^{ade}\epsilon{}_{imn}l^{m}_{d}l^{n}_{e}P_{j}(S^{b})P_{k}(S^{c})
\nonumber\\
&=&4(l^{j}_{b}l^{k}_{c}
-l^{j}_{c}l^{k}_{b})
P_{j}(S^{b})P_{k}(S^{c})
\nonumber\\
&=&4[\frac{9}{4}V^{2}
-l^{j}_{c}l^{k}_{b}P_{j}(S^{b})P_{k}(S^{c})]
\end{eqnarray}
$$
对于 $\vec{S}^{a}_{i}l^{i}_{b}$ 的缩并，由于 $\vec{S}^{a}_{i}$ 是另外两条边的叉乘来的，所以只有 $a$ 和 $b$ 是相同指标的时候缩并才不为零，因此有
$$
\begin{eqnarray}
(\kappa{}\beta{})^{3}\epsilon{}^{ijk}\epsilon{}_{abc}P_{i}(S^{a})P_{j}(S^{b})P_{k}(S^{c})
&=&4[\frac{9}{4}V^{2}
-\delta{}^{b}_{c}\frac{1}{2}Vl^{k}_{b}P_{k}(S^{c})]
\nonumber\\
&=&4[\frac{9}{4}V^{2}
-\frac{1}{2}V\frac{3}{2}V)]
\nonumber\\
&=&6V^{2}
\end{eqnarray}
$$
如果直接用积分的方式得到体积，用最简单的正方体计算，就是
$$
\begin{eqnarray}
V&=&(2|l|)^{3}\sqrt{ q }
\nonumber\\
V&=&\sqrt{ (2|l|)^{6} \frac{1}{3!}\epsilon{}^{ijk}\epsilon{}_{abc}e^{a}_{i}e^{b}_{j}e^{c}_{k}}
\nonumber\\
V&=&\sqrt{ \frac{1}{3!}\epsilon{}^{ijk}
\epsilon{}_{abc}(2|l|)^{2}e^{a}_{i}
\epsilon{}_{abc}(2|l|)^{2}e^{b}_{j}
\epsilon{}_{abc}(2|l|)^{2}e^{c}_{k}
}
\nonumber\\
V&=&\sqrt{ \frac{(\kappa{}\beta{})^{3}}{3!}
|\epsilon{}^{ijk}\epsilon{}_{abc}
P_{i}(S^{a})P_{j}(S^{b})P_{k}(S^{c})|
}
\nonumber\\
6V^{2}&=&(\kappa{}\beta{})^{3}
|\epsilon{}^{ijk}\epsilon{}_{abc}
P_{i}(S^{a})P_{j}(S^{b})P_{k}(S^{c})|
\end{eqnarray}
$$
两种方式一致。所以比较直接的方式是把体积在经典的时候写为
$$
\begin{equation}
V
=(\kappa{}\beta{})^{\frac{3}{2}}\sqrt{ \frac{1}{3!}
|\epsilon{}^{ijk} \epsilon{}_{abc}
P_{i}(S^{a})P_{j}(S^{b})P_{k}(S^{c})|
}
\end{equation}
$$
但是这种定义依赖于坐标系的选取，也就是是在使得区域形状为平行六面体的特殊形状下得到的。选取不同的坐标系可能得到不同的系数，这里面有一个问题，对于一个封闭的多面体来说，通过局域的微分同胚变换可以把它变为一个面的数量不同的多面体乃至一个球形这样的弯曲形状（无数面体），但是后面求解微分同胚变换的时候所定义的微分同胚作用并不会增加一个顶点上多面体面数的上限（连接顶点的非平凡边的个数）。在这种框架下，将区域分解为无数个小正方体后，它任意顶点的三个面全部可能的定向的集合记作 $s$， 讨论出来的**体积算符**为
$$
\begin{equation}
\hat{V}_{T}:=\sqrt{ 6 }\mathop{{\rm lim}}\limits_{N\rightarrow{}\infty}^{}[V_{C}]_{N}=\sqrt{ 6 }\mathop{{\rm lim}}\limits_{N\rightarrow{}\infty}^{}\sum\limits_{C=1,s\in{}S}^{N}\sqrt{ |q_{C,s}| }
\end{equation}
$$
其中$\hat{q}_{C,s}:=\frac{(\kappa{}\beta{})^{3}}{3!}\epsilon{}^{ijk}\epsilon{}_{abc}\hat{P}_{i}(S^a)\hat{P}_{j}(S^b)\hat{P}_{k}(S^c)$。
# 引力的代数量子化
## 算符分析
假设 $(H,\langle\cdot{},\cdot{}\rangle)$ 是一个希尔伯特空间，线性算子 $T:D(T)\subset{}H\rightarrow{}H$ 的定义域 $D(T)$ 是一个稠密线性子空间，下面来定义它的 **伴随算子** $T^{*}$ ，先定义其伴随算子的定义域
$$
\begin{eqnarray}
D(T^{*})
:=\{y,|\langle Tx|y\rangle=\langle x,z\rangle,\forall{}x,\exists{}z\in{}H\}
\end{eqnarray}
$$
也就是如果 $\forall{}x \in{}H$，其被算子 $T$ 作用后和 $y$ 的内积都等于 $x$ 和某个固定的 $z\in{}H$ 的内积，则 $y$ 属于定义域。可以证明 $y$ 和 $z$ 之间的对应是单射，也即是 $z(y)$ 是唯一的，因此可以用这个唯一的映射来定义 $T$ 的伴随算子，也就是 $\forall{}x \in{}D(T)$，$y\in{}D(T^{*})$
$$
\begin{equation}
\langle Tx,y\rangle
=\langle x,T^{*}y\rangle
\end{equation}
$$
**自伴算子** 则定义为 $T=T^{*}$ 的算子。下面把伴随算子的分量求出来，由于 $T$ 的定义域稠密，所以任何 $H$ 中的元素总可以用 $D(T)$ 中元素的线性展开来逼近，所以可以在 $D(T)$ 中选择一组正交基 $\tilde{x}^{i}$，它的线性展开的闭包是 $H$。这组正交基不一定是完全的，可以把其完全化为正交完全集 $x^{i}$ ，把落在 $D(T)$ 之外的那些成员记作 $\hat{x}^{i}$ ，则 $\forall{} y\in{}D(T^{*})$ 有
$$
\begin{eqnarray}
T^{*}y
&=&\langle x^{i},T^{*}y\rangle x^{i}
\nonumber\\
&=&\langle T\tilde{x}^{i},y\rangle \tilde{x}^{i}
+\langle \hat{x}^{i},T^{*}y\rangle x^{i}
\end{eqnarray}
$$
注意这里的求和不一定是爱因斯坦求和，因为完全集的指标不一定可数，也可能是其它合适的展开形式，比如积分。由于 $T^{*}y\in{}H$，所以它一定可以被 $D(T)$ 中元素逼近，也就是存在无穷级数 $y_{n}$ 满足
$$
\begin{equation}
\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}y_{n}=T^{*}y
\end{equation}
$$
简单的反证法可以证明 $\tilde{x}^{i}$ 一定可以线性展开 $D(T)$ 中的元素，所以 $y_{n}$ 一定可以被 $\tilde{x}^{i}$ 展开。设 $y_{n}=y^{i}_{n}\tilde{x}^{i}$，则有
$$
\begin{equation}
\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}y^{i}_{n}\tilde{x}^{i}=T^{*}y
\end{equation}
$$
与前式做差得
$$
\begin{eqnarray}
\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}y^{i}_{n}\tilde{x}^{i}-\langle T\tilde{x}^{i},y\rangle \tilde{x}^{i}
-\langle \hat{x}^{i},T^{*}y\rangle x^{i}
&=&0
\nonumber\\
(\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}y^{i}_{n}
-\langle T\tilde{x}^{i},y\rangle)\tilde{x}^{i}
&=&\langle \hat{x}^{i},T^{*}y\rangle x^{i}
\end{eqnarray}
$$
由于左右两侧无法彼此线性表出，所以必有左右两侧都为零，也就是
$$
\begin{equation}
\langle \hat{x}^{i},T^{*}y\rangle x^{i}
=0
\end{equation}
$$
和
$$
\begin{eqnarray}
(\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}y^{i}_{n}
-\langle T\tilde{x}^{i},y\rangle)\tilde{x}^{i}
&=&0
\nonumber\\
\langle T\tilde{x}^{i},y\rangle\tilde{x}^{i}
&=&\mathop{{\rm lim}}\limits_{n\rightarrow{}\infty}^{}y^{i}_{n}\tilde{x}^{i}
\end{eqnarray}
$$
即
$$
\begin{eqnarray}
\langle T\tilde{x}^{i},y\rangle\tilde{x}^{i}=T^{*}y
\end{eqnarray}
$$
定义一个算子为 **闭算子**，如果它的图像
$$
\begin{eqnarray}
\Gamma{}(T)
=\{(x,Tx)\in{}H\times{}H|x\in D(T)\}
\end{eqnarray}
$$
在 $H\times{}H$ 中是闭集。
可以得到闭算子伴随的伴随是它自己。
然后是 **对称算子**，一个算子 $T$ 是对称的，如果它的定义域是稠密的，且 $\forall{}x,y\in{}D(T)$，都有
$$
\begin{eqnarray}
\langle Tx,y\rangle
=\langle x,Ty\rangle
\end{eqnarray}
$$
设 $z=Ty$，则这意味着，$\forall{}y\in{}D(T)$，$\exists{}z\in{}H$ 使得 $\forall{}x \in{}D(T)$满足
$$
\begin{equation}
\langle Tx,y\rangle
=\langle x,z\rangle
\end{equation}
$$
因此 $D(T)\subset{}D(T^{*})$ 且 $T|_{D(T)}=T^{*}|_{D(T)}$，特别的，假如 $D(T)$ 也是一个希尔伯特空间，则 $T$ 在自己的定义域上是自伴的。
## 规范场论的代数正则量子化
### 约束系统与辛几何
### 勒让德变换与约束系统
 Prop 设$\mathscr{E}$为$m$维位形空间配以坐标系$\{q^{1},...,q^{m}\}$，并在切丛诱导坐标系$\{q^{1},...,q^{m},v^{1},...,v^{m}\}$其上一条曲线$\eta{}(t)$在切丛$T\mathscr{E}$的水平提升$\tilde{\eta{}}(t)=(q^{1}(t),...,q^{m}(t),\dot{q}^{1}(t),...,\dot{q}^{m}(t))$。
$$
\begin{eqnarray}
&&\tilde{\eta{}}(t)\\
&=&(q(t),\frac{\partial{}}{\partial{}t}q(t))\\
&=&(q^{1},...,q^{m},\frac{dq^{1}}{dt},...,\frac{dq^{m}}{dt})
\end{eqnarray}
$$
 Claim $T\mathscr{E}$中的曲线$\tilde{\eta{}}(t)$是演化曲线$\leftrightarrow{}$它是某条曲线的水平提升且满足拉氏方程。
 Def 给定一个系统的拉氏函数$\mathcal{L}$后，$p_{i}:=\frac{\partial{}\mathcal{L}}{\partial{}v^{i}}$
 Claim 物理相空间$\Gamma{}$是位形空间的余切丛$T^{*}\mathscr{E}$。
$位形空间进行坐标变换后$，$动量的变换为$
$$
\begin{eqnarray}
&&p'_{i}\\
&=&\frac{\partial{}\mathcal{L}}{\partial{}v'^{i}}\\
&=&\frac{\partial{}\mathcal{L}}{\partial{}\frac{\partial{}q'^{i}}{\partial{}q^{j}}\frac{dq^{j}}{dt}}\\
&=&\frac{\partial{}q^{j}}{\partial{}q'^{i}}\frac{\partial{}\mathcal{L}}{\partial{}v^{j}}\\
&=&\frac{\partial{}q^{j}}{\partial{}q'^{i}}p_{j}
\end{eqnarray}
$$
$p_{a}:=p_{i}(dx^{i})_{a}是一个余矢量$。
 Def 称映射$f:T\mathscr{E}\rightarrow{}\Gamma{},(q,v(q))\mapsto{}(q,p(v,q))$为勒让德变换。
 Def 勒让德变换对应的雅可比矩阵$J_{ij}=\frac{\partial{}p_{i}}{\partial{}v^{j}}$的行列式为$0$的物理系统称为约束系统，此时勒让德变换的像$\bar{\Gamma{}}\subset{}\Gamma{}$称为约束面。
 Claim 无论系统是否为约束系统，勒让德变换的像上有唯一的哈氏函数$\mathcal{H}:=p_{a}v^{a}-\mathcal{L}$。
 Thm $q^{i}$和$p_{i}$可以表示哈氏函数。
$$
\begin{eqnarray}
&&d\mathcal{H}\\
&=&d(p_{a}v^{a}-\mathcal{L})\\
&=&p_{a}dv^{a}+dp_{a}v^{a}-\frac{\partial{}\mathcal{L}}{\partial{}q^{i}}dq^{i}-\frac{\partial{}\mathcal{L}}{\partial{}v^{i}}dv^{i}\\
&=&p_{a}dv^{a}+\dot{q}^{a}dp_{a}-\dot{p_{i}}dq^{i}-p_{i}dv^{i}\\
&=&\dot{q}^{a}dp_{a}-\dot{p}_{a}dq^{a}
\end{eqnarray}
$$
 Def 将哈氏函数延拓到整个相空间，记作$H$。
 Claim 有约束系统的哈氏正则方程为$\dot{q}^{i}=\frac{\partial{}H}{\partial{}p_{i}}+\lambda{}_{m}(t)\frac{\partial{}\phi{}^{m}}{\partial{}p_{i}},\dot{p}^{i}=-\frac{\partial{}H}{\partial{}q_{i}}-\lambda{}_{m}(t)\frac{\partial{}\phi{}^{m}}{\partial{}q_{i}}$，其中$\lambda{}^{m}$为待定乘子，$\phi{}^{m}$是约束。
$整个相空间\Gamma{}上有dH=\frac{\partial{}H}{\partial{}q^{i}}dq^{i}+\frac{\partial{}H}{\partial{}p_{i}}dp_{i}$，$而在约束面\tilde{\Gamma{}}上有dH=\dot{q}^{i}dp_{i}-\dot{p}_{i}dq^{i}$，$所以有$
$$
\begin{eqnarray}
&&0|_{\tilde{\Gamma{}}}\\
&=&d(H-H)|_{\tilde{\Gamma{}}}\\
&=&(\dot{q}^{i}-\frac{\partial{}H}{\partial{}p_{i}})dq^{i}|_{\tilde{\Gamma{}}}-(\dot{p}_{i}+\frac{\partial{}H}{\partial{}q^{i}})dp_{i}|_{\tilde{\Gamma{}}}
\end{eqnarray}
$$
$给定约束面上一个坐标系\{r^{1},...,r^{n}\}$，$则$
$$
\begin{eqnarray}
&&0\\
&=&(\dot{q}^{i}-\frac{\partial{}H}{\partial{}p_{i}})\frac{\partial{}q^{i}}{\partial{}r^{j}}dr^{j}-(\dot{p}_{i}+\frac{\partial{}H}{\partial{}q^{i}})\frac{\partial{}p_{i}}{\partial{}r^{j}}dr^{j}\\
&=&[(\dot{q}^{i}-\frac{\partial{}H}{\partial{}p_{i}})\frac{\partial{}q^{i}}{\partial{}r^{j}}-(\dot{p}_{i}+\frac{\partial{}H}{\partial{}q^{i}})\frac{\partial{}p_{i}}{\partial{}r^{j}}]dr^{j}
\end{eqnarray}
$$
$定义\Gamma{}上的余矢场\zeta{}_{A}=(\dot{q}^{i}-\frac{\partial{}H}{\partial{}p_{i}})(dp_{i})_{A}-(\dot{p}_{i}+\frac{\partial{}H}{\partial{}q^{i}})(dq^{i})_{A}$，$（约束面外的动量已经不由勒让德变换得到）$，$则有\zeta{}_{A}(\frac{\partial{}}{\partial{}r})^{A}|_{\tilde{\Gamma{}}}=0$，$因此$
$$
\begin{eqnarray}
&&\zeta{}_{A}|_{\tilde{\Gamma{}}}\\
&=&\lambda{}^{m}\nabla_{A}\phi{}_{m}|_{\tilde{\Gamma{}}}\\
&=&\lambda{}^{m}[\frac{\partial{}\phi{}_{m}}{\partial{}q^{i}}(dq^{i})_{A}+\frac{\partial{}\phi{}_{m}}{\partial{}p_{i}}(dp_{i})_{A}]|_{\tilde{\Gamma{}}}
\end{eqnarray}
$$
 Claim 约束系统演化曲线$\gamma{}(t)$上的函数$f(t)$有$\dot{f}(t)=\{f,H\}+\lambda{}_{m}\{f,\phi{}^{m}\}$
 Def 称$\{\phi{}_{m},H\}+\lambda{}^{n}\{\phi{}_{m},\phi{}_{n}\}\approx{}0$为自洽性条件，约等于指算完了泊松括号再取值，约定记号$h_{m}:=\{H,\phi{}_{m}\}、\Phi{}_{mn}:=\{\phi{}_{m},\phi{}_{n}\}$，则自洽性条件变为$h_{m}=\Phi{}_{mn}\lambda{}^{n}$。
 Remark 自洽性条件对拉氏函数的选择提出了要求，本质上应该是变分原理的一部分？
 Thm $det(\Phi{}_{mn}(P))\neq0,\forall{}P\in{} \tilde{\Gamma{}}$时，$\dot{q}^{i}=\frac{\partial{}H}{\partial{}p_{i}}+\frac{\partial{}\phi{}_{m}}{\partial{}p_{i}}(\Phi{}^{-1})^{mn}h_{n},\dot{p}_{i}=-\frac{\partial{}H}{\partial{}q^{i}}-\frac{\partial{}\phi{}_{m}}{\partial{}q^{i}}(\Phi{}^{-1})^{mn}h_{n}$
 Def $det(\Phi{}_{mn}(P))\approx{}0,\forall{}P\in{} \tilde{\Gamma{}}$时，为了满足自洽性条件的$h_{m}=0$称为次级约束。
 Def 相空间中满足所有约束自洽性条件的部分叫做最终约束面。
 Def 相空间上与所有约束的泊松括号弱为零的的函数叫做第一类的，否则叫做第二类的。
 Thm 有多少个第一类初级约束就有多少个自由的拉氏乘子，也就是系统具有多大的规范自由度。
### 哈密顿力学的几何表述
 1 1 Def 2$N$维流形$\Gamma{}$上的非退化的2形式场$\Omega{}_{AB}$称为$\Gamma{}$上的辛形式，$(\Gamma{},\Omega{}_{AB})$称为辛流形。  
 2 2 Def $\Omega{}^{AB}\Omega{}_{BC}=\delta{}^{A}_{C}$  
 3 3 Claim $\Omega{}_{AB}\Omega{}^{BC}=\delta{}^{C}_{A}$  
 4 4 Def 微分同胚$\psi{}:\Gamma{}\rightarrow{}\Gamma{}$称为正则变换，若$\psi{}^{*}\Omega{}_{AB}=\Omega{}_{AB}$  
 5 5 Def $(\Gamma{},\Omega{}_{AB})$上的矢量场$v^{A}$称为无限小对称性，若它生出的单参微分同胚族的每个微分同胚都是正则变换。  
 6 6 Claim $v^{A}$是无限小对称性，若$\mathcal{L}_{v}\Omega{}_{AB}=0$。  
 7 7 Def $f$是$\Gamma{}$上的实函数，称矢量场$X^A_{f}:=\Omega{}^{AB}_{}\nabla_{B}f$为$f$的哈式矢量场，其中$\nabla_{A}$是$\Gamma{}$上的任意无挠导数算符。  
 8 8 Claim 局域的说，$\Gamma{}$上的矢量场$v^{A}$是无限小对称性$\leftrightarrow{}$它是某函数$f$的哈氏矢量场。  
$$  
\begin{eqnarray}  
&&\mathcal{L}_{v}\Omega{}_{AB}\\  
&=&d(v\cdot{}\Omega{})_{AB}+v^{C}\cdot{}(d\Omega{})_{CAB}\\  
&=&d(v\cdot{}\Omega{})_{AB}  
\end{eqnarray}  
$$  
$若v^{A}是无限小对称性$，$则局域的\exists{}f,v^{A}\Omega{}_{AB}=\nabla_{B}f\rightarrow{}v^{A}=-X^{A}_{f}$  
$若v^{A}局域是某函数f的哈氏矢量场$，$则d(v\cdot{}\Omega{})_{AB}=d(\Omega{}^{CD}\nabla_{D}f\Omega{}_{C})_{AB}=-(d\circ{}df)_{AB}=0$
 9 Def $(\Gamma{},\Omega{}_{AB})$上的两个函数$f,g$的泊松括号定义为$\{f,g\}:=\Omega{}^{AB}\nabla_{A}f\nabla_{B}g$
 10 Prop $\{f,g\}=\mathcal{L}_{X_{g}}f=-\mathcal{L}_{X_{f}}g$
 11 Thm （$Darboux$定理）$\forall{}p\in{}\Gamma{}$，必有局域坐标系$\{x^{1},...,x^{N},y^{1},...,y^{N}\}$ s.t. $\Omega{}_{AB}=(dy_{i})_{A}\wedge{}(dx^{i})_{B}$。
 12 Def 满足$Darboux$定理的坐标称为正则坐标。
 13 Claim 设$\psi{}:\Gamma{}\rightarrow{}\Gamma{}$是正则变换，$x^{i},y^{i}$是$O\subset{}\Gamma{}$上的正则坐标，则$\psi{}^{*}x^{i},\psi{}^{*}y^{i}$是$\psi{}^{-1}[O]$上额正则坐标。
$$
\begin{eqnarray}
&&\Omega{}_{AB}|_{\psi{}^{-1}[O]}\\
&=&\psi{}^{*}\Omega{}_{AB}|_{O}\\
&=&\psi{}^{*}[(dy_{i})_{A}\wedge{}(dx^{i})_{B}]
\end{eqnarray}
$$
$由于\psi{}^{*}d=d\psi{}^{*}$，$所以\Omega{}_{AB}|_{\psi{}^{-1}[O]}=d(\psi{}^{*}y_{i})\wedge{}d(\psi{}^{*}x^{i})$
 14 Claim $X^{A}_{\{f,g\}}=-[X_{f},X_{g}]^{A}$
$$
\begin{eqnarray}
&&\Omega{}_{AB}(X^{A}_{\{f,g\}}+[X_{f},X_{g}]^{A})\\
&=&\Omega{}_{AB}\Omega{}^{AC}d_{C}\{f,g\}+\Omega{}_{AB}\mathcal{L}_{X_{f}}X_{g}^{A}\\
&=&-\delta{}^{C}_{B}d_{C}(\mathcal{L}_{X_{g}}f)+\mathcal{L}_{X_{f}}(-\nabla_{B}g)\\
&=&d_{B}(\mathcal{L}_{X_{f}}g)-\mathcal{L}_{X_{f}}(d_{B}g)\\
&=&0
\end{eqnarray}
$$
 1 Def 设$\mathscr{E}$为$m$维位形空间，则定义它的相空间$\Gamma{}=T^{*}\mathscr{E}$。
 2 Def $\forall{}P=(p,\omega{}_{a})\in{}T^{*}\mathscr{E},\theta{}_{A}|_{P}X^{A}:=\omega{}_{a}(\pi{}_{*}X)^{a},\forall{}X^{A}\in{}V_{P}$
 3 Def $\Omega{}_{AB}:=(d\theta{})_{AB}$
 4 Claim $\mathscr{E}$中选定坐标系$\{q^{i}\}$后，$\theta{}_{A}=\omega{}_{i}(dq^{i})_{A}$
$$
\begin{eqnarray}
&&\omega{}_{i}(dq^{i})_{A}X^{A}\\
&=&\omega{}_{i}X^{i}\\
&=&\omega{}_{a}(\pi{}_{*}X)^{a}
\end{eqnarray}
$$
 5 Convention 下面用$p_{i}$代替$\omega{}_{i}$，即$\theta{}_{A}=p_{i}(dq^{i})^{A}$。
 6 Cor $\Omega{}_{AB}=(dp_{i})_{A}\wedge{}(dq^{i})_{B}$，因此$\mathscr{E}$在$\Gamma{}$上诱导的坐标系天然是与$\Omega{}_{AB}$相适配的正则坐标。
 7 Claim $\Omega{}_{AB}(\frac{\partial{}}{\partial{}q^{i}})^{A}(\frac{\partial{}}{\partial{}q^{j}})^{B}=\Omega{}_{AB}(\frac{\partial{}}{\partial{}p^{i}})^{A}(\frac{\partial{}}{\partial{}p^{j}})^{B}=0;\Omega{}_{AB}(\frac{\partial{}}{\partial{}q^{i}})^{A}(\frac{\partial{}}{\partial{}p^{j}})^{B}=-\delta{}^{i}_{j}$
 8 Cor $\Omega{}^{AB}=(\frac{\partial{}}{\partial{}q^{i}})^{A}\wedge{}(\frac{\partial{}}{\partial{}p_{i}})^{B}$
$$
\begin{eqnarray}
&&(\frac{\partial{}}{\partial{}q^{i}})^{A}\wedge{}(\frac{\partial{}}{\partial{}p_{i}})^{B}(dp_{j})_{B}\wedge{}(dq^{j})_{C}\\
&=&(\frac{\partial{}}{\partial{}q^{i}})^{A}\delta{}^{j}_{i}(dq^{j})_{C}\\
&=&(\frac{\partial{}}{\partial{}q^{i}})^{A}(dq^{i})_{C}\\
&=&\delta{}^{A}_{C}
\end{eqnarray}
$$
 9 Claim $X^{A}_{f}=\frac{\partial{}f}{\partial{}p^{i}}(\frac{\partial{}}{\partial{}q_{i}})^{A}-\frac{\partial{}f}{\partial{}q^{i}}(\frac{\partial{}}{\partial{}p_{i}})^{A}$
$$
\begin{eqnarray}
&&X^{A}_{f}\\
&=&\Omega{}^{AB}\nabla_{B}f\\
&=&\left( \frac{\partial{}}{\partial{}q^{i}} \right)^{A}\frac{\partial{}f}{\partial{}p_{i}}-\left( \frac{\partial{}}{\partial{}p^{i}} \right)^{A}\frac{\partial{}f}{\partial{}q_{i}}
\end{eqnarray}
$$
 Claim $\{f,g\}=\frac{\partial{}f}{\partial{}q^{i}}\frac{\partial{}g}{\partial{}p_{i}}-\frac{\partial{}f}{\partial{}p^{i}}\frac{\partial{}g}{\partial{}q_{i}}$
### 约束系统的几何表示
 Def 约束系统$(\Gamma{},\Omega{}_{AB},H,\bar{\Gamma{}},\{C_{r}\})$称为第一类的，若$\bar{\Gamma{}}$上的每一法余矢$n_{A}$对应的矢量$n^{A}=\Omega{}^{AB}n_{B}$都切于$\bar{\Gamma{}}$，其中$\{\nabla_{A}C_{r}\}$构成法余矢空间的一组基底。
 Prop $\Gamma{}$上的函数$f$是第一类的$\leftrightarrow{}X^{A}_{f}$切于$\bar{\Gamma{}}$。
$$
\begin{eqnarray}
&&\Gamma{}上的函数f是第一类的\\
&\leftrightarrow{}&\{f,C_{r}\}=0\\
&\leftrightarrow{}&\Omega{}^{AB}\nabla_{A}f\nabla_{B}C_{r}=0\\
&\leftrightarrow{}&-X^{A}_{f}d_{B}C_{r}=0\\
&\leftrightarrow{}&X^{A}_{f}|_{\bar{\Gamma{}}}n_{A}=0
\end{eqnarray}
$$
 Prop 系统是第一类的$\leftrightarrow{}$所有约束是第一类约束。
 Claim 第一类约束函数的哈氏函数是第一类的。
$$
h_{m}=0
$$
 Claim 第一类约束系统的相空间$\Gamma{}$上局域存在函数$f^{t}_{rs}$ s.t. $\{C_{r},C_{s}\}=f^{t}_{rs}C_{t}$。
 Def 第一类约束系统的约束的哈氏矢量场称为约束矢量场，$\{C_{r}\}$对应的约束矢量场的集合记作$\{X^{A}_{r}\}$，以$\{X^{A}_{r}|_{p}\}$为基底构成的现象空间记作$\Delta{}_{p}$，$p\in{}\bar{\Gamma{}}$的所有切于$\bar{\Gamma{}}$的矢量的集合记作$W_{p}$。
 Claim $\Delta{}_{p}\subset{}W_{p}$。
 Def $\Omega{}_{AB}$在$\bar{\Gamma{}}$上的限制定义为$\bar{\Omega{}}_{AB}\bar{v}^{A}\bar{u}^{B}:=\Omega{}_{AB}\bar{v}^{A}\bar{u^{B}},\forall{}\bar{v}^{A}、\bar{u}^{A}\in{}W_{p}$。
 Def 满足$\bar{\Omega{}}_{AB}\bar{v}^{A}=0_{W}$的$\bar{v}^{A}\in{}W_{p}$称为退化矢量。
 Claim 法余矢对应的矢量都是退化矢量。
 Thm $\bar{n}^{A}$为退化矢量$\leftrightarrow{}\Omega{}_{AB}\bar{n}^{A}$为法余矢。
$$
\forall{}\bar{v}^{A}\in{}W_{p},\Omega{}_{AB}\bar{n}^{A}\bar{v}^{B}=0
$$
 Def 定义$\bar{\Gamma{}}$上的哈氏矢量场$\bar{X}^{A}_{f}$满足$\bar{\Omega{}}_{AB}\bar{X}^{B}_{H}=\bar{\nabla}_{A}H$。
$$
\begin{eqnarray}
&&\bar{\Omega{}}_{AB}X^{B}_{f}\bar{v}^{A}\\
&=&\Omega{}_{AB}X^{B}_{f}\bar{v}^{A}\\
&=&\nabla_{A}H\bar{v}^{A}\\
&=&\bar{\nabla}_{A}H\bar{v}^{A}
\end{eqnarray}
$$
$所以至少X^{A}_{f}是一个\bar{\Gamma{}}上的哈氏矢量场$，$定义是良好的$。
 Claim $\bar{\Gamma{}}$不同的哈氏矢量场之间差一个约束矢量场。
 Claim 与$X^{A}_{f}$差一个初级约束矢量场的$\bar{\Gamma{}}$上的哈氏矢量场的积分曲线是演化线。
 Thm $\Delta{}$作为$\bar{\Gamma{}}$上的分布是可积的。
$$
\begin{eqnarray}
&&[X_{r},X_{s}]^{A}\\
&=&-X^{A}_{\{C_{r},C_{s}\}}\\
&=&-X^{A}_{f^{t}_{rs}C_{t}}
\end{eqnarray}
$$
 Def $\bar{\Gamma{}}$上所有最大积分子流形的集合记作$\hat{\Gamma{}}$，称为约化相空间。
 Claim $\bar{\Gamma{}}$以$\hat{\Gamma{}}$为底流形成为一个纤维丛，投影映射$\pi{}(p)=S(p)$，其中$S(p)$为包含$p$的那个唯一的最大积分子流形。
 Def 定义约化相空间上的辛形式$\hat{\Omega{}}_{AB}=\pi{}_{*}(\bar{\Omega{}}_{AB})$
 Prop 哈氏函数在每一最大积分子流形上为常数，所以约化相空间上有自然的哈氏函数的定义$\hat{H}(S)=H_{S}$。
$$
\begin{eqnarray}
&&\mathcal{L}_{k^{r}X_{r}}H\\
&=&\{H,k^{r}C_{r}\}\\
&=&0
\end{eqnarray}
$$
 Claim $\pi{}_{*}(\bar{X}^{A}_{H})=X_{\hat{H}}^{A}$。
$$
\begin{eqnarray}
&&\pi{}_{*}(\bar{X}^{A}_{H})\hat{v}_{A}\\
&=&\pi{}_{*}(\bar{X}^{A}_{H})\hat{\Omega{}}^{BC}\hat{\Omega{}}_{CA}\hat{v}_{B}\\
&=&\pi{}_{*}(\bar{X}^{A}_{H}\hat{\Omega{}}_{CA})\hat{\Omega{}}^{BC}\hat{v}_{B}\\
&=&\pi{}_{*}(d_{C}H)\hat{\Omega{}}^{BC}\hat{v}_{B}\\
&=&d_{C}\hat{H}\hat{\Omega{}}^{BC}\hat{v}_{B}\\
&=&X^{B}_{\hat{H}}\hat{v}_{B}
\end{eqnarray}
$$
 Lemma 设$\gamma{}$、$\hat{\gamma{}}$分别为$X^{A}_{H}$和$X_{\hat{H}}^{A}$的积分曲线且$\pi{}(\gamma{}(0))=\hat{\gamma{}}(0)$，则$\pi{}(\gamma{})=\hat{\gamma{}}$。
$$
\begin{eqnarray}
&&\pi{}_{*}((\frac{\partial{}}{\partial{}t})^{A})\\
&=&\pi{}_{*}(X^{A}_{H})\\
&=&X^{A}_{\hat{H}}
\end{eqnarray}
$$
$所以\pi{}(\gamma{})是以\hat{\gamma{}}(0)为起点，以X^{A}_{\hat{H}}为切矢的积分曲线$。
 Thm 设$\gamma{}$、$\gamma{}'$分别为$X^{A}_{H}$和$\bar{X}^{A}_{H}$的积分曲线且$\pi{}(\gamma{}(0))=\pi{}(\gamma{}'(0))$，则$\gamma{}'(t)$和$\gamma{}(t)$必在同一个纤维上。
## $GNS-$表示与运动学希尔伯特空间
 1 Def 设$(\mathcal{M},\{\cdot{},\cdot{}\})$为相空间，基本可观测量代数$\mathbf{P}$定义为相空间上的一个满足下列条件的函数集合$\{f\}$：
1. $f\in{}\mathbf{P}可以将\mathcal{M}中的点分离$；
2. $\mathbf{P}以泊松括号形成一个泊松代数$；
3. $f\in{}\mathbf{P}\rightarrow{}\bar{f}\in{}\mathbf{P}$。
 2 Prop $\mathbf{P}$是一个$*-$泊松代数。
 3 Def 定义$\mathbf{P}$的自由$*-$代数$F(\mathbf{P})$，它以$\mathbf{P}$中序列$\{f_{1},...,f_{n}\}$为基矢张成，并按下面定义代数运算和对合运算：
$$
(f_{1},...,f_{n})\cdot{}(f_{1}',...,f_{m}'):=(f_{1},...,f_{n},f_{1}',...f_{m}')
$$
$$
(f_{1},...,f_{n})^{*}=(\bar{f}_{n},...,\bar{f}_{1})
$$
 4 Thm $\forall{}f,f'\in{}F(\mathbf{P})$，$(f+f')-(f)-(f)'、(zf)-z(f)、[(f),(f')]-i\hbar{}(\{f,f'\})$张成的空间$\mathcal{Z}$称为$F(\mathbf{P})$的一个双边理想，其中$[(f),(f')]:=(f)\cdot{}(f')-(f')\cdot{}(f)=(f,f')-(f',f)$。
 5 Def 基本可观测量的量子代数$\mathbf{A}$定义为商$*-$代数$F(\mathbf{P})/\mathcal{Z}$。
 6 Def 对于一个矢量空间$\mathcal{H}$，称线性映射$\pi{}:\mathbf{A}\rightarrow{}\mathcal{L}(\mathcal{H})$是一个$*-$表示$\leftrightarrow{}\exists{}\mathcal{D}$是$\mathcal{H}$的一个稠密，$\mathcal{D}\subset{}\cap_{a\in{}A}^{}D(\pi{}(a))$，其中$D(\pi{}(a))$表示$\pi{}(a)$的定义域，且满足下列条件
4. $\pi{}(a\cdot{}b)=\pi{}(a)\pi{}(b)$，
5. $\pi{}(a^{*})=\pi{}(a)^{^{\dagger}}$，
$\forall{}a,b\in{}\mathbf{A}$。
 Def $*-$代数$\mathfrak{A}$上的一个正线性泛函$\omega{}:\mathfrak{A}\rightarrow{}\mathbb{C}$是指满足$\omega{}(a^{*}a)\geq{}0$的线性泛函
 Def $*-$代数$\mathfrak{A}$上的一个态是一个正线性泛函$\omega{}$，且$\omega{}(a^{*})=\bar{\omega{}(a)},\omega{}(1)=1$。
 7 Def 给定$\mathbf{A}$一个上态$\omega{}$，定义$(\mathbf{A},\omega{})$的零空间$\mathcal{N}_{\omega{}}:=\{a\in{}\mathbf{A}|\omega{}(a^{*}\cdot{}a)=0\}$。称$*-$表示$\pi{}_{\omega{}}:\mathbf{A}\rightarrow{}\mathcal{L}(\mathcal{H}_{\omega{}}),\pi{}(a)[b]:=[a\cdot{}b],\forall{}b\in{}\mathcal{H}_{\omega{}}$为$\omega{}$在$\mathbf{A}$上诱导的$GNS-$表示，其中$\mathcal{H}_{\omega{}}:=<\mathbf{A}/\mathcal{N}_{\omega{}}>$。$\mathcal{H}_{\omega{}}$有自然的内积$\langle[a]|[b]\rangle_{\mathcal{H}_{\omega{}}}:=\omega{}(a^{*}\cdot{}b)$成为希尔伯特空间。
 8 Def 称$*-$表示$\pi{}:\mathbf{A}\rightarrow{}\mathcal{L}(\mathcal{H})$是循环表示，如果$\exists{}\Omega{}\in{}\mathcal{H},<\{\pi{}(a)\Omega{}|a\in{}\mathbf{A}\}>=\mathcal{H}$ ，称$\Omega{}$为该表示空间的循环矢量。
 9 Thm $GNS-$表示是循环表示，且$\Omega{}_{\omega{}}:=[1]$是循环矢量。
 Remark 由于全部全部算符作用到循环矢量上可以还原整个希尔伯特空间，所以才可以建立算符和希尔伯特空间矢量之间的对应。
 10 Thm 每一个非退化的表示都是循环表示的正交直和。
 11 Def $G$是系统的规范对称群，$\alpha{}:G\rightarrow{}Aut(\mathbf{A})$是群作用，$\omega{}$是规范不变的线性泛函（$\omega{}\circ{}\alpha{}_{g}=\omega{}$）。定义$G$在$\mathcal{H}_{\omega{}}$上的表示$U$，满足$U(g)\pi{}_{\omega{}}(a)\Omega{}_{\omega{}}:=\pi{}_{\omega{}}(\alpha{}_{g}(a))\Omega{}_{\omega{}}$。
 12 Def 半经典态

## 约束系统量子化
 1 Def 设$\{\hat{C}_{r}\}$为线性无关的约束对应量子算符的集合，物理希尔伯特空间$\mathcal{H}_{phys}\subset{}\mathcal{H}_{kin}$定义为$\mathcal{H}_{phys}:=\cap_{r}^{}{\rm ker}(\hat{C^{r}})$。
 2 Def 弱狄拉克可观测量和强狄拉克可观测量定义为
1. $称\mathcal{O}\in{}\mathscr{F}(\bar{\Gamma{}})为弱狄拉克可观测量\leftrightarrow{}\{\mathcal{O},C_{r}\}|_{\bar{\Gamma{}}}=0$。$对于量子情况$，$一个自伴随算子称为弱狄拉克可观测量算子\leftrightarrow{}它在物理希尔伯特空间上有良好的定义$。
2. 称$\mathcal{O}\in{}\mathscr{F}(\Gamma{})为强狄拉克可观测量\leftrightarrow{}她是第一类的$。$对于量子情况$，$一个自伴随算子\hat{\mathcal{O}}称为强狄拉克可观测量算子\leftrightarrow{}它可以被定义在整个运动学希尔伯特空间上$，$且[\hat{\mathcal{O}},\hat{C}_{r}]=0$。
## 圈量子运动学的代数构造
 Def $su(2)-$值函数$f^{i}$在紧的面$S$上的抹匀通量定义为$P_{f}:=\int_{S}^{}\epsilon{}_{abc}\tilde{P}^{a}_{i}f^{i}$。
 Thm 抹匀通量与合乐的泊松代数为$$\{P_{f}(S),A(e)\}=\int_{S}^{}n_{a}f^{i}(x)d^{2}x\int_{0}^{1}\delta^{3}{}(x(e(s))-x)\dot{e}^{a}A(0,\lambda{})\tau{}_{i}A(\lambda{},1)d\lambda{}$$
 Def 抹匀通量矢量场定义为$Y_{f}(S):=\{P_{f}(S),\cdot{}\}$。
 Def 经典$ACZ$合乐-通量$*-$代数承担集为矢量空间$\mathbf{P}_{ACZ}:=Cyl(\bar{\mathfrak{A}})\times{}\mathcal{V}^{C}(\bar{\mathfrak{A}})$，其中$\mathcal{V}^{C}(\bar{\mathfrak{A}}):=\{\psi{}Y_{f}(S)|\psi{}\in{}Cyl(\bar{\mathfrak{A}})\}$，并配以$*-$李代数结构：
1. $其上李括号的作用定义为\{(\psi{},Y),(\psi{}',Y')\}:=(Y\circ{}\psi'{}-Y'\circ{}\psi{},[Y,Y'])$。
2. $其上的对合运算定义为\bar{a}:=(\bar{\psi{}},\bar{Y}),\forall{}a\in{}\mathbf{P}_{ACZ}$，$其中\bar{Y}\circ{}\psi{}:=\bar{Y\circ{}\psi{}}$。
3. $柱函数在上面有自然的作用\psi'{}\circ{}(\psi{},Y):=(\psi{}'\psi{},\psi{}'Y)$。
 Def $F(\mathbf{P}_{ACZ})$的双边理想$\mathbf{Z}$由下面操作生成
$$
(a+a')-(a)-(a');z(a)-(za);[(a),(a')]-i\hbar{}(\{a,a'\});((\psi{},0),a)-(\psi{}\circ{}a)。
$$
$其中对易括号定义为[(a),(a')]:=(a)\cdot{}(a')-(a')\cdot{}(a)$。
 Def 量子合乐-通量$*-$代数定义为$\mathbf{A}:F(\mathbf{P}_{ACZ})/\mathbf{Z}$。
 Convention 简单起见后面把$(\psi{},0)$和$(0,Y)$简记作$(\psi{})$和$(Y)$。
 Def 定义量子代数$\mathbf{A}$上的代数

# 量子高斯约束
## SU(2)的平凡表示
高斯约束最终求解完后得到的空间是 $SU(2)$ 的平凡表示空间，所以在这之前先补充一些 $SU(2)$ 表示论的知识，并分析一下它的平凡表示。  
## 旋量法
$2$ 阶全反称张量保 $GL(2,\mathbb{C})$ 的基本表示矩阵不变，特别的 $SU(2)$ 作为 $GL(2,\mathbb{C})$ 的子群，其基本表示矩阵还保全反称张量不变，而不变性在几何和代数研究中都很重要，因此要研究 $SU(2)$ 的性质 $2$ 阶全反称张量就很重要。首先给它选择一个表示来明确记号，也就是把 $\epsilon{}^{AB}$ 的分量为 $\epsilon{}^{-\frac{1}{2}\frac{1}{2}}=1$，然后可以定义下指标的 $2$ 阶全反称张量 $\epsilon{}_{AB}\epsilon{}^{AC}=\delta{}^{C}_{B}$。接着在旋量空间上，约定使用全反称张量进行指标的升降：
$$
\begin{equation}
\omega{}^{A}:=\omega{}_{B}\epsilon{}^{BA}，
\qquad
\omega{}_{C}:=\epsilon{}_{CD}\omega{}^{D}
\end{equation}
$$
可以证明在我们的记号下，指标升降的定义是良好的:
$$
\begin{eqnarray}
\omega{}_{A}
&=&\epsilon{}_{AB}\omega{}^{B}\\
&=&\epsilon{}_{AB}\omega{}_{C}\epsilon{}^{CB}\\
&=&\omega{}_{A}
\end{eqnarray}
$$
$$
\begin{eqnarray}
\omega{}^{A}
&=&\omega{}_{B}\epsilon{}^{BA}\\
&=&\epsilon{}_{BC}\omega{}^{C}\epsilon{}^{BA}\\
&=&\omega{}^{A}
\end{eqnarray}
$$
也就是任何一个旋量经过两次升降后可以回到自身。

设 $U^{A}{}_{B}$ 是 $SU(2)$ 的基本表示矩阵，由于
$$
\begin{eqnarray}
-U_{B}{}^{A}U^{B}{}_{E}&=&-\epsilon{}_{BD}U^{D}{}_{C}\epsilon{}^{CA}U^{B}{}_{E}\\
&=&-\epsilon{}_{EC}\epsilon{}^{CA}\\
&=&\delta{}^{A}_{E}
\end{eqnarray}
$$
所以 $SU(2)$ 基本表示矩阵的逆矩阵可以计算为 $(U^{-1})^{A}{}_{B}=-U_B{}^{A}$。可以用基本表示的张量积表示来把这一性质扩展到任意表示的情况：
$$
\begin{eqnarray}
(U^{-1})^{A_{1}}{}_{B_{1}}...(U^{-1})^{A_{m}}{}_{B_{m}}U^{B_{1}}{}_{C_{1}}...U^{B_{m}}{}_{C_{m}}&=&\delta{}^{A_{1}}_{C_{1}}...\delta{}^{A_{m}}_{C_{m}}
\end{eqnarray}
$$
也就是若定义 $U^{A_{1}...A_{m}}{}_{B_{1}...B_{m}}:=U^{A_{1}}{}_{B_{1}}\otimes{}...\otimes{}U^{A_{m}}{}_{B_{m}}$，则 $(U^{-1})^{A_{1}...A_{m}}{}_{B_{1}...B_{m}}=(U^{-1})^{A_{1}}{}_{B_{1}}...(U^{-1})^{A_{m}}{}_{B_{m}}$。不可约表示的张量积所对应的表示空间是不可约表示空间的张量积空间。

最小的基本表示空间的张量积空间是两个基本表示空间的张量积，可以用双指标旋量 $\psi{}^{AB}:=\psi{}^{A}\otimes{}\psi{}^{B}$ 来表示其中的元素，由于
$$
\begin{eqnarray}
U^{A}{}_{C}U^{B}{}_{D}f\epsilon{}^{CD}&=&f\epsilon{}^{AB},\forall{}f\in{}\mathbb{C}
\end{eqnarray}
$$
所以双指标旋量 $\psi{}^{AB}$ 按对称部分和反称部分 $\psi{}^{AB}=\psi{}_{0}\epsilon{}^{AB}+\psi{}_{1}^{AB}$ 分解为平凡表示和矢量表示，其中 $\psi{}_{0}=\frac{1}{2}\epsilon{}_{AB}\psi{}^{AB}$。从这可以看出来全反称张量本身就是双指标旋量空间的平凡子表示中的元素。

接下来分析一个重要的事情，也就是如何从 $SU(2)$ 基本表示空间的张量积空间中提取出任意的不可约表示子空间。首先根据对称化操作的性质，有
$$
\begin{eqnarray}
U^{A_{1}}{}_{B_{1}}...U^{A_{2j}}{}_{B_{2j}}\psi{}^{(B_{1}...B_{2j})}&=&U^{A_{1}}{}_{(B_{1}}...U^{A_{2j}}{}_{B_{2j})}\psi{}^{B_{1}...B_{2j}}\\
&=&U^{(A_{1}}{}_{B_{1}}...U^{A_{2j})}{}_{B_{2j}}\psi{}^{B_{1}...B_{2j}}
\end{eqnarray}
$$
所以指标数量相同的张量积空间上的全对称化元素的全体成为一个不变子空间，因而是一个表示空间。接下来说明它是不可约表示空间。首先用旋量空间的基矢 $\{\psi{}^{A}_{\frac{1}{2}},\psi{}^{A}_{-\frac{1}{2}}\}$ 来构造这个空间的基矢 $\{\psi{}^{A_{1}...A_{2j}}_{-j+m}=\psi{}_{1/2}^{(A_{1}}...\psi{}_{1/2}^{A_{m}}\psi{}_{-1/2}^{A_{m+1}}...\psi{}_{-1/2}^{A_{2j})}\}^{2j}_{m=0}$，显然它们是对称化后的空间中的正交完备基矢。由于
$$
\begin{equation}
J_{+}\psi{}_{-j+m}
=\sqrt{ (2j-m)(m+1) }\psi{}_{-j+m+1}
\end{equation}
$$
可以从最小的 $\psi{}_{-j}$ 开始一直生成到 $\psi{}_{j}$，因此该子空间对 $su(2)$ 来说不存在兼并，当然也对 $SU(2)$ 没有兼并，所以这是一个不可约子空间。由于该空间基矢的数量为 $2j+1$，所以其对应着 $SU(2)$ 的 $j$ 表示空间。

接下来证明一个重要的**表示分解定理**，即 $j_{1}\otimes{}j_{2}=|j_{1}-j_{2}|\oplus|j_{1}-j_{2}|+1\oplus...\oplus(j_{1}+j_{2})$。
不妨令 $j_{1}\leq{}j_{2}$。先假设 $\psi{}^{C_{1}...C_{k}A_{k+1}...A_{2j_{1}}}\phi{}_{C_{1}...C_{k}}{}^{B_{k+1}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{k}B_{k}}\in{}(j_{2}-j_{1})...\oplus(j_{2}+j_{1}-k)$，其中 $\psi{}\in{}V^{(j_{1})}$，$\phi{}\in{}V^{(j_{2})}$，则
$$
\begin{eqnarray}
&&\psi{}^{C_{1}...C_{k-1}A_{k}...A_{2j_{1}}}\phi{}_{C_{1}...C_{k-1}}{}^{B_{k}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{k-1}B_{k-1}}\\
&=&(\frac{1}{2}\psi{}^{C_{1}...C_{k}A_{k+1}...A_{2j_{1}}}\phi{}_{C_{1}...C_{k}}{}^{B_{k+1}...B_{2j_{2}}}\epsilon{}^{A_{k}B_{k}}+\psi{}^{C_{1}...C_{k-1}(A_{k}...A_{2j_{1}}}\phi{}_{C_{1}...C_{k-1}}{}^{B_{k}...B_{2j_{2}})})\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{k-1}B_{k-1}}\\
&\in{}&(j_{2}-j_{1})\oplus...\oplus(j_{2}+j_{1}-k+1)
\end{eqnarray}
$$
而
$$
\begin{eqnarray}
&&(\frac{1}{2})^{2j_{1}}\epsilon{}_{C_{1}D_{1}}...\epsilon{}_{C_{2j_{1}}D{2j_{1}}}\psi{}^{C_{1}...C_{2j_{1}}}\phi{}^{D_{1}...D_{2j_{1}}B_{2j_{1}+1}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{2j_{1}}B_{2j_{1}}}\\
&=&(\frac{1}{2})^{2j_{1}}\psi{}^{C_{1}...C_{2j_{1}}}\phi{}_{C_{1}...C_{2j_{1}}}{}^{B_{2j_{1}+1}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{2j_{1}}B_{2j_{1}}}\\
&=:&\varphi{}_{2j_{1}}^{(B_{2j_{1}+1}...B_{2j_{2}})}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{2j_{1}}B_{2j_{1}}}\\
&\in{}&(j_{2}-j_{1})\otimes{}0^{k}\\
&=&j_{2}-j_{1}
\end{eqnarray}
$$
所以假设成立，且容易看出来每增加一个全反称张量，就增加一个直和表示空间，因此这种态对应的那些不同表示空间都是单重的。然后来说明假设上面假设的这种态和全对称态张成整个张量积空间 $V^{(j_{1})}\otimes{}V^{(j_{2})}$。$\forall{}\psi{}\otimes{}\phi{}\in{}V^{(j_{1})}\otimes{}V^{(j_{2})}$，由于指标 $\psi{}$ 的指标对称性和指标 $\phi{}$ 的指标对称性，有
$$
\begin{eqnarray}
\psi{}^{A_{1}...A_{2j_{1}}}\phi{}^{B_{1}...B_{2j_{2}}}
&=&\psi{}^{(A_{1}|...A_{2j_{1}}|}\phi{}^{B_{1})...B_{2j_{2}}}
+\psi{}^{[A_{1}|...A_{2j_{1}}|}\phi{}^{B_{1}]...B_{2j_{2}}}
\nonumber\\
&=&\psi{}^{(A_{1}|...A_{2j_{1}}|}\phi{}^{B_{1})...B_{2j_{2}}}
+\frac{1}{2}\psi{}^{C_{1}A_{2}...A_{2j_{1}}}\phi{}_{C_{1}}{}^{B_{2}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}
\nonumber\\
&...&
\nonumber\\
&=&\psi{}^{(_{1}A_{1}(_{2}A_{2}...(_{2j_{1}}A_{2j_{1}}|}\phi{}^{B_{1})_{1}B_{2})_{2}...B_{2j_{2}})_{2j_{2}}}
+\frac{1}{2}\psi{}^{C_{1}A_{2}...A_{2j_{1}}}\phi{}_{C_{1}}{}^{B_{2}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}
\nonumber\\
&&+\frac{1}{2^{2}}\psi{}^{C_{1}C_{2}A_{3}...A_{2j_{1}}}\phi{}_{C_{1}C_{2}}{}^{B_{3}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}\epsilon{}^{A_{2}B_{2}}+...
\nonumber\\
&&+(\frac{1}{2})^{2j_{1}}\psi{}^{C_{1}...C_{2j_{1}}}\phi{}_{C_{1}...C_{2j_{1}}}{}^{B_{2j_{1}+1}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{2j_{1}}B_{2j_{1}}}
\end{eqnarray}
$$
也就是它可以被逐级分解为对称部分和反对称部分，对于对称部分来说，$A_{i}$ 和 $B_{i}$ 各自内部的对称性是本就有的。任选一个 $A_{i_{0}}$ 和一个 $B_{j_{0}}$ 两个指标，可以通过先交换 $A_{i_{0}}$ 和 $B_{i_{0}}$，然后交换 $B_{i_{0}}$ 和 $B_{j_{0}}$ 的方式来实现对换而与原值相等。所以对称部分是完全对称的，因此其张成一个表示为 $j_{1}+j_{2}$ 的空间。其中的基矢就是前面定义的 $\{\psi{}_{-j_{1}-j_{2}+m}\}$，然后定义 $\varphi{}_{k}^{A_{1}...A_{2j_{1}}B_{1}...B_{2j_{2}}}:=(\frac{1}{2})^{k}\psi{}^{C_{1}...C_{k}A_{k+1}...A_{2j_{1}}}\phi{}_{C_{1}...C_{k}}{}^{B_{k+1}...B_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{k}B_{k}}$，则根据前面的分解 $\{\psi{}_{-j_{1}-j_{2}+m};\varphi{}_{k}\}_{k=1}^{2j_{1}}$ 是一组基矢，所以定理得证。

表示分解定理的一个推论是 **CG条件**，也就是若角动量 $j_{3}$ 由 $j_{1}$ 和 $j_{2}$ 耦合而来，则它们满足
1. $j_{1}+j_{2}+j_{3}=N$;
2. $|j_{1}-j_{2}|<j_{3}<(j_{1}+j_{2})$。
推导表示分解定理的过程中可以注意到，若 $\psi{}^{A_{1}...A_{2j}}$ 是 $2j$ 个 $\frac{1}{2}$ 空间依次耦合的空间中的元素，则它的 $j$ 表示空间的分量只能取全对称的形式，因此 $SU(2)$ 的 $2j$ 个指标的 $j$ 表示空间只能是全对称张量张成的空间。
此外还可以知道 两个表示空间耦合，形如$\psi{}_{1}^{A_{1}...A_{2j_{1}}}\psi{}_{2}^{B_{1}...B_{2j_{2}}}$ 的元素中，所有的属于平凡表示的不变态为 $v(\psi{}_{1}\psi{}_{2})=\delta{}_{j_{1}j_{2}}(\frac{1}{4})^{j_{1}}\psi{}_{1}^{C_{1}...C_{j_{1}}}\psi{}_{2C_{1}...C_{j_{1}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{j_{1}}B_{j_{1}}}$。
这是因为若两个角动量不相等，则由对称性有
$$
\begin{eqnarray}
&&v(\psi{}_{1}\psi{}_{2})\\
&=&(\frac{1}{2})^{j_{1}+j_{2}}[\theta{}(j_{1}-j_{2})\psi{}_{1}^{C_{1}...C_{2j_{2}}C_{2j_{2}+1}...C_{j_1+j_2}}{}_{C_{2j_{2}+1}...C_{j_{1}+j_{2}}}\psi{}_{2C_{1}...C_{2j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{2j_{2}}B_{2j_{2}}}\epsilon{}^{A_{2j_{2}+1}A_{j_{1}+j_{2}+1}}...\epsilon{}^{A_{j_{1}+j_{2}}A_{2j_{1}}}\\
&&+\theta{}(j_{2}-j_{1})\psi{}_{1}^{C_{1}...C_{2j_{1}}}\psi{}_{2C_{1}...C_{2j_{1}}}{}^{C_{2j_{1}+1}...C_{j_{1}+j_{2}}}{}_{C_{2j_{1}+1}...C_{j_{1}+j_{2}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{2j_{1}}B_{2j_{1}}}\epsilon{}^{A_{2j_{2}+1}A_{j_{1}+j_{2}+1}}...\epsilon{}^{A_{j_{1}+j_{2}}A_{2j_{2}}}]\\
&=&0
\end{eqnarray}
$$

$CG$ 条件也可以等价为 $\exists{}a,b,c\in{}N$，$2j_{1}=a+c$，$2j_{2}=a+b$，$2j_{3}=b+c$，这种表示有的时候比较方便。由于 $CG$ 条件给出了两个角动量耦合为第三个角动量的条件，而第三个角动量可以和自身耦合出不变子空间，因此实际上告诉我们满足 $CG$ 条件的三个角动量一定可以共同耦合出不变子空间。若 $\psi{}_{1}^{A_{1}...A_{2j_{1}}}\psi{}_{2}^{B_{1}...B_{2j_{2}}}\psi{}_{3}^{C_{1}...C_{2j_{3}}}$ 为这样一个空间的元素，则它其中的那部分不变部分为
$$
\begin{eqnarray}
&&v(\psi{}_{1}\psi{}_{2}\psi{}_{3})^{A_{1}...A_{2j_{1}};B_{1}...B_{2j_{2}};C_{1}...C_{2j_{3}}}:=(\frac{1}{2})^{j_{1}+j_{2}+j_{3}}\epsilon{}_{D_{1}E_{1}}...\epsilon{}_{D_{a}E_{a}}\epsilon{}_{E_{a+1}F_{1}}...\epsilon{}_{E_{a+b}F_{b}}\epsilon{}_{F_{b+1}D_{a+1}}...\epsilon{}_{F_{b+1}D_{a+c}}\\
&\times{}&\psi{}_{1}^{D_{1}...D_{2j_{1}}}\psi{}_{2}^{E_{1}...E_{2j_{2}}}\psi{}_{3}^{F_{1}...F_{2j_{3}}}\epsilon{}^{A_{1}B_{1}}...\epsilon{}^{A_{a}B_{a}}\epsilon{}^{B_{a+1}C_{1}}...\epsilon{}^{B_{a+b}C_{b}}\epsilon{}^{C_{b+1}A_{a+1}}...\epsilon{}^{C_{b+c}A_{a+c}}
\end{eqnarray}
$$
证明很简单，先让两个角动量耦合，并选取和第三个角动量相同的那个分量，再和第三个角动量耦合即可。

在 $j$ 表示空间上指定基矢 $\{\psi{}_{j,k}^{A_{1}...A_{2j}}\}_{k=0}^{2j}$，定义 **$3j$ 符号**
$$
\begin{eqnarray}
l^{(j_{1}j_{2}j_{3})}_{\alpha{}_{1}\alpha{}_{2}\alpha{}_{3}}\equiv{}\begin{pmatrix}
j_{1}&j_{2}&j_{3}\\
\alpha{}_{1}&\alpha{}_{2}&\alpha{}_{3}
\end{pmatrix}:=Kv^{}(\psi{}_{j_{1},\alpha{}_{1}}\psi{}_{j_{2},\alpha{}_{2}}\psi{}_{j_{3},\alpha{}_{3}})^{A_{1}...A_{a}}{}_{A_{a+1}...A_{a+c};A_{1}...A_{a}}{}^{B_{a+1}...B_{a+b};}{}_{B_{a+1}...B_{a+b}}{}^{A_{a+1}...A_{a+c}}
\end{eqnarray}，
$$
其中 $K$ 保证
$$
\begin{eqnarray}
\sum\limits_{\alpha{}_{1}\alpha{}_{2}\alpha{}_{3}}^{}\begin{pmatrix}
j_{1}&j_{2}&j_{3}\\
\alpha{}_{1}&\alpha{}_{2}&\alpha{}_{3}
\end{pmatrix}^{*}\begin{pmatrix}
j_{1}&j_{2}&j_{3}\\
\alpha{}_{1}&\alpha{}_{2}&\alpha{}_{3}
\end{pmatrix}=1。
\end{eqnarray}
$$
即可，通常不是唯一的。下面用两个例子算一下 $3j$ 符号。
3. 一般把 $j=\frac{1}{2}$ 的基矢选做 $\psi{}^{A}_{\frac{1}{2},B}=\delta{}^{A}_{B}$，把 $j=1$ 的基矢选作 $\psi{}_{1,i}^{AB}=\frac{1}{\sqrt{ 2 }}\sigma{}_{i}^{AB}:=\frac{1}{\sqrt{ 2 }}\sigma{}_{i}^{A}{}_{C}\epsilon{}^{CB}$，求
$$
\begin{eqnarray}
\begin{pmatrix}
\frac{1}{2}&\frac{1}{2}&1\\
A&B&i
\end{pmatrix}
\end{eqnarray}
$$
**解**
$$
\begin{eqnarray}
&&v^{}(\psi{}_{\frac{1}{2},A}\psi{}_{\frac{1}{2},B}\psi{}_{1,i}){}_{C;}{}^{D;}{}_{D}{}^{C}\\
&=&\frac{1}{4}\epsilon{}_{CE}\epsilon{}_{DF}\psi{}_{\frac{1}{2},A}^{E}\psi{}_{\frac{1}{2},B}^{D}\psi{}_{1}^{FC}\\
&=&\frac{1}{4}\epsilon{}_{CA}\epsilon{}_{BF}\frac{1}{\sqrt{ 2 }}\sigma{}^{FC}_{i}\\
&=&-\frac{1}{4\sqrt{ 2 }}\sigma{}_{iBA}\\
&=&-\frac{1}{4\sqrt{ 2 }}\sigma{}_{iAB}
\end{eqnarray}
$$
$$
\begin{eqnarray}
&&\sigma{}_{i}^{AB}(\sigma{}^{iAB})^{*}\\
&=&\sigma{}_{i}^{A}{}_{C}\epsilon{}^{CB}(\sigma{}^{iA}{}_{D})^{*}\epsilon{}^{DB}\\
&=&\delta{}^{CD}\sigma{}_{i}^{A}{}_{C}(\sigma{}^{iA}{}_{D})^{*}\\
&=&\sigma{}^{A}_{i}{}_{D}\sigma{}^{iD}{}_{A}\\
&=&6
\end{eqnarray}
$$
$所以$
$$
\begin{eqnarray}
\begin{pmatrix}
\frac{1}{2}&\frac{1}{2}&1\\
A&B&i
\end{pmatrix}=\frac{1}{\sqrt{ 6 }}\sigma{}_{iAB}
\end{eqnarray}
$$
4. 求
$$
\begin{eqnarray}
\begin{pmatrix}
1&1&1\\
i&j&k
\end{pmatrix}
\end{eqnarray}
$$
**解**
$$
\begin{eqnarray}
&&\epsilon{}_{A_{1}B_{1}}\epsilon{}_{B_{2}C_{1}}\epsilon{}_{C_{2}A_{2}}\psi{}_{1,i}^{A_{1}A_{2}}\psi{}_{1,j}^{B_{1}B_{2}}\psi{}_{1,k}^{C_{1}C_{2}}\\
&=&\frac{1}{2\sqrt{ 2 }}\epsilon{}_{A_{1}B_{1}}\epsilon{}_{B_{2}C_{1}}\epsilon{}_{C_{2}A_{2}}\sigma{}_{i}^{A_{1}}{}_{D}\epsilon{}^{DA_{2}}\sigma{}_{j}^{B_{1}}{}_{E}\epsilon{}^{EB_{2}}\sigma{}_{k}^{C_{1}}{}_{F}\epsilon{}^{FC_{2}}\\
&=&\frac{1}{2\sqrt{ 2 }}\epsilon{}_{A_{1}B_{1}}\delta{}^{E}_{C_{1}}\delta{}^{F}_{A_{2}}\sigma{}_{i}^{A_{1}}{}_{D}\epsilon{}^{DA_{2}}\sigma{}_{j}^{B_{1}}{}_{E}\sigma{}_{i}^{C_{1}}{}_{F}\\
&=&\frac{1}{2\sqrt{ 2 }}\epsilon{}_{A_{1}B_{1}}\sigma{}_{i}^{A_{1}}{}_{D}\epsilon{}^{DA_{2}}\sigma{}_{j}^{B_{1}}{}_{C_{1}}\sigma{}_{k}^{C_{1}}{}_{A_{2}}\\
&=&\frac{1}{2\sqrt{ 2 }}\epsilon{}_{A_{1}B_{1}}\sigma{}_{i}^{A_{1}}{}_{D}\epsilon{}^{DA_{2}}(\delta{}_{jk}+i\epsilon{}_{jk}{}^{l}\sigma{}_{l})^{B_{1}}{}_{A_{2}}\\
&=&\frac{1}{2\sqrt{ 2 }}(\delta{}_{jk}\epsilon{}_{A_{1}B_{1}}\sigma{}_{i}^{A_{1}}{}_{D}\epsilon{}^{DB_{1}}+i\epsilon{}_{jk}{}^{l}\sigma{}_{l}^{B_{1}}{}_{A_{2}}\epsilon{}_{A_{1}B_{1}}\sigma{}_{i}^{A_{1}}{}_{D}\epsilon{}^{DA_{2}})\\
&=&\frac{1}{2\sqrt{ 2 }}(\delta{}_{jk}\sigma{}_{i}^{A_{1}}{}_{A_{1}}-i\epsilon{}_{jk}{}^{l}\sigma{}_{l}^{B_{1}}{}_{A_{2}}\sigma{}_{iB_{1}}{}^{A_{2}*})\\
&=&-\frac{i}{2\sqrt{ 2 }}\epsilon{}_{jk}{}^{l}\sigma{}_{l}^{B_{1}}{}_{A_{2}}\sigma{}_{i}{}^{A_{2}}{}_{B_{1}}\\
&=&-\frac{i}{2\sqrt{ 2 }}\epsilon{}_{jk}{}^{l}(\delta{}_{li}+i\epsilon{}_{li}{}^{p}\sigma{}_{p})^{B_{1}}{}_{B_{1}}\\
&=&-\frac{i}{\sqrt{ 2 }}\epsilon{}_{ijk}
\end{eqnarray}
$$
所以归一化后为 $\frac{1}{\sqrt{ 6 }}\epsilon{}^{ijk}$。
前面已经定义了类似磁量子数基矢的不可约表示空间的基矢，现在把它的记号和常用记号靠近一下，并且归一化，由于
$$
\begin{eqnarray}
\psi{}_{m}^{A_{1}...A_{2j}}&=&\psi{}_{\frac{1}{2}}^{(A_{1}}...\psi{}_{\frac{1}{2}}^{A_{m}}\psi{}_{-\frac{1}{2}}^{A_{m+1}}...\psi{}_{-\frac{1}{2}}^{A_{2j})}\\
&=&\frac{1}{(2j)!}\sum\limits_{\sigma{}}^{}\psi{}_{\frac{1}{2}}^{\sigma{}(A_{1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}(A_{2j})}\\
&=&\frac{1}{(2j)!}\sum\limits_{\sigma{}}^{}\psi{}_{\frac{1}{2}}^{(\sigma{}(A_{1})}...\psi{}_{\frac{1}{2}}^{\sigma{}(A_{j+m}))}\psi{}_{\frac{1}{2}}^{(\sigma{}(A_{m+1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}(A_{2j}))}\\
&=&\frac{1}{(2j)!}\sum\limits_{k=1}^{C^{j+m}_{2j}}(j+m)!(j-m)!\psi{}_{\frac{1}{2}}^{\sigma{}_{k}(A_{1})}...\psi{}_{\frac{1}{2}}^{\sigma{}_{k}(A_{j+m})}\psi{}_{\frac{1}{2}}^{\sigma{}_{k}(A_{m+1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}_{k}(A_{2j})}\\
&=&\frac{1}{C_{2j}^{j+m}}\sum\limits_{k=1}^{C^{j+m}_{2j}}\psi{}_{\frac{1}{2}}^{\sigma{}_{k}(A_{1})}...\psi{}_{\frac{1}{2}}^{\sigma{}_{k}(A_{m})}\psi{}_{\frac{1}{2}}^{\sigma{}_{k}(A_{m+1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}_{k}(A_{2j})}\\
\end{eqnarray}
$$
所以
$$
\begin{eqnarray}
|\psi{}_{m}^{A_{1}...A_{2j}}|^{2}
&=&\frac{1}{(C^{j+m}_{2j})^{2}}C^{j+m}_{2j}\\
&=&\frac{1}{C^{j+m}_{2j}}
\end{eqnarray}
$$
因此可以把其归一化系数取为 $\alpha{}^{j,m}=\sqrt{ C^{j+m}_{2j} }$，从而定义 $j$ 表示空间的**磁量子数基矢** $\{\psi{}_{j,m}^{A_{1}...A_{2j}}:=\alpha{}^{j,m}\psi{}^{A_{1}...A_{2j}}_{m}\}$。

由于 $3j$ 符号的值由 $(j_{1}+j_{2}+j_{3})$ 个 $\epsilon{}_{AB}$ 与三个矢量缩并而成，由反称性可知，在磁量子数基矢下，每个 $\epsilon{}_{AB}$ 必须同时与一个 $\psi{}^{A}_{\frac{1}{2},\frac{1}{2}}$ 和 $\psi{}^{A}_{\frac{1}{2},-\frac{1}{2}}$ 缩并整体才不为零。所以 $\psi{}^{A}_{\frac{1}{2},\frac{1}{2}}$ 和 $\psi{}^{A}_{\frac{1}{2},-\frac{1}{2}}$ 必须数量相等，设前者数量为 $k$，后者为 $l$，则有 $-j_{i}+k_{i}=m_{i}$，$l_{i}=2j_{i}-k_{i}$。从而有
$$
\begin{eqnarray}
j_{1}+m_{1}+j_{2}+m_{2}+j_{3}+m_{3}&=&j_{1}-m_{1}+j_{2}-m_{2}+j_{3}-m_{3}\\
m_{1}+m_{2}+m_{3}&=&0
\end{eqnarray}
$$
 因此可以得到
 $$
\begin{eqnarray}
\begin{pmatrix}
j_{1}&j_{2}&j_{3}\\
m_{1}&m_{2}&m_{3}
\end{pmatrix}\neq0\leftrightarrow{}m_{1}+m_{2}+m_{3}=0
\end{eqnarray}
$$
然后来具体确定一下系数 $K$ 完成该基矢下 $3j$ 符号的定义，把它形式化的带进基矢中，然后根据 $a$，$b$，$c$ 在缩并时候的排列，小心处理一下对称化就可以得到可以把 $K$ 选择为
$$
\begin{equation}
K_{j_{1}j_{2}j_{3}}
=2^{j_{1}+j_{2}+j_{3}}N_{j_{1}j_{2}j_{3}}
\end{equation}
$$
其中 $N_{j_{1}j_{2}j_{3}}=\sqrt{ \frac{(2j_{1})!(2j_{2})!(2j_{3})!}{(j_{1}+j_{2}+j{3}+1)!(j_{1}+j_{2}-j{3})!(j_{2}+j_{3}-j{3})!(j_{1}+j_{3}-j{2})!} }$。

磁量子数基矢的好处很多，比如在该基矢下可以证明列维奇维塔符号为
$$
\begin{eqnarray}
\epsilon{}_{ijk}=\sqrt{ 6 }\begin{pmatrix}
1&1&1\\
i&j&k
\end{pmatrix}
\end{eqnarray}
$$
证明逻辑很简单，这组基矢是前面例题基矢的线性组合$，$所以可以写成泡利矩阵的升指标的线性组合$，$利用泡利矩阵的对易反对易关系用一样的套路可以容易的验证结果。

注意到从一个不可约表示的张量积空间到平凡子空间的投影事实上就是用 $2$ 阶全反称张量的张量积来实现的，所以可以定义从多个角动量空间到平凡子空间的投影算符：
1. $l^{j}_{A_{1}...A_{2j}B_{1}...B_{2j}}=N_{j}\epsilon{}_{A_{1}B_{1}}...\epsilon{}_{A_{2j}B_{2j}}$
2. $l^{j_{1}j_{2}j_{3}}_{A_{1}...A_{2j_{1}};B_{1}...B_{2j_{2}};...;C_{1}...C_{2j_{3}}}:=N_{j_{1}j_{2}j_{3}}\epsilon{}_{A_{1},B_{1}}...\epsilon{}_{A_{a}B_{a}}\epsilon{}_{B_{a+1}C_{1}}...\epsilon{}_{B_{a+b}C_{b}}\epsilon{}_{C_{b+1}A_{a+1}}...\epsilon{}_{C_{b+c}A_{a+c}}$。
不需要定义太多的算符，因为更多角动量的耦合总可以通过多次三个角动量的耦合来实现，比如容易证明 $l^{j_{1}j_{2}j_{3}j_{4}}=\sqrt{ d_{k} }l^{j_{1}j_{2}j_{k}}l_{j_{k}}{}^{j_{3}j_{4}}$。因此三个及以上角动量的耦合可以放在后面的章节中专门说。
先研究两个角动量耦合到平凡子空间的投影算符。两个角动量想耦合出平凡子空间，根据 $CG$ 条件，必须有 $m_{1}+m_{2}=0$。设这两个不可约子空间的元素各有 $k_{1}$、$k_{2}$ 个指标在 $-\frac{1}{2}$，有 $l_{1}$、$l_{2}$ 个在 $\frac{1}{2}$，则得到 $-j+k_{1}=m_{1}$，$-j+k_{2}=m_{2}$ 以及 $l_{1}=2j-k_{1}$ 和 $l_{2}=2j-k_{2}$。把投影算符作用到张量积的结果去后会得到
$$
\begin{eqnarray}
l^{j}\cdot{}\psi{}_{j,m}\psi{}_{j,n}&=&\delta{}_{m,-n}l^{j}\cdot{}\psi{}_{j,m}\psi{}_{j,-m}\\
&=&\delta{}_{m,-n}N_{j}C^{j+m}_{2j}\frac{1}{(C^{j+m}_{2j})^{2}}\sum\limits_{p,q=1}^{C_{2j}^{j+m}}\psi{}_{\frac{1}{2}}^{\sigma{}_{p}(A_{1})}...\psi{}_{\frac{1}{2}}^{\sigma{}_{p}(A_{j+m})}\psi{}_{-\frac{1}{2}}^{\sigma{}_{p}(A_{j+m+1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}_{p}(A_{2j})}\\
&&\cdot{}\psi{}_{-\frac{1}{2}}^{\sigma{}_{q}(A_{1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}_{q}(A_{j+m})}\psi{}_{\frac{1}{2}}^{\sigma{}_{q}(A_{j+m+1})}...\psi{}_{\frac{1}{2}}^{\sigma{}_{q}(A_{2j})}\\
&=&\delta{}_{m,-n}N_{j}\frac{1}{C^{j+m}_{2j})}\sum\limits_{p,q=1}^{C_{2j}^{j+m}}\delta{}_{pq}\psi{}_{\frac{1}{2}}^{\sigma{}_{p}(A_{1})}...\psi{}_{\frac{1}{2}}^{\sigma{}_{p}(A_{j+m})}\psi{}_{-\frac{1}{2}}^{\sigma{}_{p}(A_{j+m+1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}_{p}(A_{2j})}\\
&&\cdot{}\psi{}_{-\frac{1}{2}}^{\sigma{}_{q}(A_{1})}...\psi{}_{-\frac{1}{2}}^{\sigma{}_{q}(A_{j+m})}\psi{}_{\frac{1}{2}}^{\sigma{}_{q}(A_{j+m+1})}...\psi{}_{\frac{1}{2}}^{\sigma{}_{q}(A_{2j})}\\
&=&\delta{}_{m,-n}N_{j}\frac{1}{C^{j+m}_{2j})}\sum\limits_{p=1}^{C_{2j}^{j+m}}1^{j+m}(-1)^{j-m}\\
&=&N_{j}\delta{}_{m,-n}(-1)^{j-m}
\end{eqnarray}
$$
  $l^{j}\cdot{}\psi{}_{j,m}\psi{}_{j,n}=N_{j}\delta{}_{m,-n}(-1)^{j-m}=:N_j\epsilon{}_{mn}^{(j)}=:N_j\epsilon{}^{(j)mn}$。新定义的这个符号在 $j=\frac{1}{2}$ 的时候就退化为 $\epsilon{}_{AB}$，所以它可以看作 $\epsilon{}_{AB}$ 在更高表示空间的推广。容易验证它满足 $\epsilon{}^{(j)}_{mn}=(-1)^{2j}\epsilon{}^{(j)}_{nm}$ 和$\epsilon{}^{(j)}_{mm'}\epsilon{}^{(j)m'n}=(-1)^{2j}\delta{}^{n}_{m}$。为了保证算符的投影是归一化的，容易算出来 $N_{j}=\frac{1}{\sqrt{ d_{j} }}$。 
## CG系数
所有多个角动量的耦合都可以通过多次三个角动量的耦合来实现，因此这里专门研究一下三个角动量的耦合，在这里面 $CG$ 系数发挥了重要作用。在研究 $CG$ 系数时，狄拉克符号很方便，这里做一下约定，用 $|jm\rangle$ 代替 $\psi{}_{jm}^{A_{1}...A_{2j}}$，则 $|\psi{}_{j}\rangle=\sum\limits_{m}^{}\psi{}^{j,m}|jm\rangle$。这两种方法本身可以独立的研究 $SU(2)$ 的表示，但是这里继承一些前面的结论。前面算过泡利矩阵可以用 $3j$ 符号表示，泡利矩阵相当于 $\frac{1}{2}$ 表示空间上的角动量算符，因此可以想象更一般的角动量算符也可以用 $3j$ 符号表示，下面来计算一下。 
设 $J_{\pm1}=\mp\frac{1}{2\sqrt{ 2 }}(J_{x}\pm iJ_{y})$，$J_0=J_z$。因为
$\langle jm|J_{\mu{}}|jn\rangle=\delta{}^{-1}_{\mu{}}\sqrt{ (j+n)(j-n+1) }\delta{}_{n-1,m}+\delta{}^{0}_{\mu{}}n\delta{}_{n,m}+\delta{}^{1}_{\mu{}}\sqrt{ (j-n)(j+n+1) }\delta{}_{n+1,m}$，而
$$
\begin{eqnarray}
J_{-1}^{AB}&=&\frac{1}{\sqrt{ 2 }}(J_{x}-iJ_{y})^{AB}\\
&=&\frac{1}{\sqrt{ 2 }}\delta{}^{A}_{-\frac{1}{2}}\delta{}_{C\frac{1}{2}}\epsilon{}^{CB}\\
&=&-\frac{1}{\sqrt{ 2 }}\delta{}^{A}_{-\frac{1}{2}}\delta{}^{B}_{-\frac{1}{2}}\\
&=&-\frac{1}{\sqrt{ 2 }}\psi{}_{1,-1}^{AB}
\end{eqnarray}
$$
$$
\begin{eqnarray}
J^{AB}_{0}&=&J_{z}^{A}{}_{C}\epsilon{}^{CB}\\
&=&\frac{1}{2}(\delta{}^{A}_{\frac{1}{2}}\delta{}_{C\frac{1}{2}}-\delta{}^{A}_{-\frac{1}{2}}\delta{}_{C-\frac{1}{2}})\epsilon{}^{CB}\\
&=&-\frac{1}{2}(\delta{}^{A}_{\frac{1}{2}}\delta{}^{B}_{-\frac{1}{2}}+\delta{}^{A}_{-\frac{1}{2}}\delta{}^{B}_{\frac{1}{2}})\\
&=&-\frac{1}{\sqrt{ 2 }}\psi{}^{AB}_{1,0}
\end{eqnarray}
$$
$$
\begin{eqnarray}
J^{AB}_{1}&=&-\frac{1}{\sqrt{ 2 }}(J_{x}+iJ_{y})^{AB}\\
&=&-\frac{1}{\sqrt{ 2 }}\delta{}^{A}_{\frac{1}{2}}\delta{}_{C-\frac{1}{2}}\epsilon{}^{CB}\\
&=&-\frac{1}{\sqrt{ 2 }}\psi{}^{AB}_{1,1}
\end{eqnarray}
$$
所以
$$
\begin{eqnarray}
-W_{j}\begin{pmatrix}
j&1&j\\
n&\mu{}&-m
\end{pmatrix}&=&\sqrt{ 2 }W_{j}N_{j,1,j}\epsilon{}_{A_{1},B_{1}}\epsilon{}_{B_{2}C_{1}}\epsilon{}_{C_{2}A_{2}}...\epsilon{}_{C_{2j}A_{2j}}\psi{}_{j,n}^{A_{1}...A_{2j}}J_{\mu{}}^{B_{1}B_{2}}\psi{}_{j,-m}^{C_{1}...C_{2j}}\\
&=&-\sqrt{ 2 }W_{j}N_{j,1,j}\epsilon{}_{A_{1},B_{1}}\epsilon{}_{C_{2}A_{2}}...\epsilon{}_{C_{2j}A_{2j}}\psi{}_{j,n}^{A_{1}...A_{2j}}J_{\mu{}}^{B_{1}}{}_{C_{1}}\psi{}_{j,-m}^{C_{1}...C_{2j}}\\
&=&\sqrt{ 2 }W_{j}N_{j,1,j}\frac{1}{2j}\sum\limits_{i=1}^{2j}\epsilon{}_{C_{i},A_{i}}\epsilon{}_{C_{2}A_{2}}...\epsilon{}_{C_{i-1}A_{i-1}}\epsilon{}_{C_{1}A_{1}}...\epsilon{}_{C_{2j}A_{2j}}
\nonumber\\
&&\times{}\psi{}_{j,n}^{A_{1}...A_{2j}}J_{\mu{}}^{C_{i}}{}_{C}\psi{}_{j,-m}^{C...C_{i-1}C_{1}C_{i+1}...C_{2j}}\\
&=&\sqrt{ \frac{1}{2j^{2}} }\sqrt{ j(j+1)(2j+1) }\sqrt{ \frac{(2j)!2!(2j)!}{(2j+2)!(2j-1)!} }\epsilon{}_{C_{1}A_{1}}...\epsilon{}_{C_{2j}A_{2j}}
\nonumber\\
&&\times{}\psi{}_{j,n}^{A_{1}...A_{2j}}(J_{\mu{}}\psi{}_{j,-m})^{C_{1}...C_{2j}}\\
&=&\sqrt{ \frac{1}{2j^{2}} }\sqrt{ \frac{j(j+1)(2j+1) 4j}{(2j+2)(2j+1)} }\epsilon{}_{C_{1}A_{1}}...\epsilon{}_{C_{2j}A_{2j}}\psi{}_{j,n}^{A_{1}...A_{2j}}(\delta{}^{-1}_{\mu{}}
\nonumber\\
&&\times{}\sqrt{ (j-m)(j+m+1) }\psi{}_{j,-m-1}-\delta{}^{0}_{\mu{}}m\psi{}_{j,-m}\\
&&+\delta{}^{1}_{\mu{}}\sqrt{ (j+m)(j-m+1) }\psi{}_{j,-m+1})^{C_{1}...C_{2j}}\\
&=&\delta{}^{-1}_{\mu{}}\sqrt{ (j-m)(j+m+1) }\delta{}^{j+m+1}\delta{}_{m+1,n}-\delta{}^{0}_{\mu{}}m\delta{}^{j+m}\delta{}_{m,n}
\nonumber\\
&&+\delta{}^{1}_{\mu{}}\sqrt{ (j+m)(j-m+1) }\delta{}^{j+m-1}\delta{}_{m-1,n}\\
&=&\delta{}^{-1}_{\mu{}}\sqrt{ (j-n+1)(j+n) }(-1)^{j+m+1}\delta{}_{m,n-1}+\delta{}^{0}_{\mu{}}n(-1)^{j+m+1}\delta{}_{m,n}\\
&&+\delta{}^{1}_{\mu{}}\sqrt{ (j+n+1)(j-n) }(-1)^{j+m+1}\delta{}_{m,n+1}\\
&=&(-1)^{j+m+1}(\delta{}^{-1}_{\mu{}}\sqrt{ (j-n+1)(j+n) }\delta{}_{m,n-1}+\delta{}^{0}_{\mu{}}n\delta{}_{m,n}
\nonumber\\
&&+\delta{}^{1}_{\mu{}}\sqrt{ (j+n+1)(j-n) }\delta{}_{m,n+1})\\
&=&(-1)^{j+m+1}\langle jm|J_{\mu{}}|jn\rangle
\end{eqnarray}
$$
因此最终可以得到
$$
\begin{equation}
\langle jm|J_{\mu{}}|jn\rangle=-(-1)^{1-j-m}W_{j}\begin{pmatrix}
j&1&j\\
n&\mu{}&-m
\end{pmatrix}
\end{equation}
$$

魏格纳矩阵的矩阵元函数可以用狄拉克符号与表示的像缩并得到，也就是可以定义 $D^{(j)m}{}_{n}(g)=\langle jm|e^{-i\alpha{}n_{i}J^{i}}|jn\rangle$，其中 $g=e^{-i\alpha{}n_{i}J^{i}}$。则 $D^{(j)m}{}_{n}$ J就是魏格纳矩阵元函数。由于
 $$
\begin{eqnarray}
&&\delta{}_{A_{1}C_{1}}...\delta{}_{A_{2j}C_{2j}}(U^{-1})^{A_{1}...A_{2j}}{}_{B_{1}...B_{2j}}\psi{}_{j,m}^{C_{1}...C_{2j}}\psi{}_{j,n}^{B_{1}...B_{2j}}\\
&=&\delta{}_{A_{1}C_{1}}...\delta{}_{A_{2j}C_{2j}}(\epsilon{}_{E_{1}B_{1}}U^{E_{1}}{}_{D_{1}}\epsilon{}^{D_{1}A_{1}}...\epsilon{}_{E_{2j}B_{2j}}U^{E_{2j}}{}_{D_{2j}}\epsilon{}^{D_{2j}A_{2j}})\psi{}_{j,m}^{C_{1}...C_{2j}}\psi{}_{j,n}^{B_{1}...B_{2j}}\\
&=&(-1)^{j-n}\delta{}_{A_{1}C_{1}}...\delta{}_{A_{2j}C_{2j}}(\delta{}_{(E_{1}-\frac{1}{2}}U^{E_{1}}{}_{|D_{1}|}\epsilon{}^{D_{1}A_{1}}...\delta{}_{E_{j+n}-\frac{1}{2}}U^{E_{j+n}}{}_{|D_{j+n}|}\epsilon{}^{D_{j+n}A_{j+n}}\\
&&\times{}\delta{}_{E_{j+n+1}\frac{1}{2}}U^{E_{j+n+1}}{}_{|D_{j+n+1}|}\epsilon{}^{D_{j+n+1}A_{j+n+1}}...\delta{}_{E_{2j})\frac{1}{2}}U^{E_{2j}}{}_{D_{2j}}\epsilon{}^{D_{2j}A_{2j}})\psi{}_{j,m}^{C_{1}...C_{2j}}\\
&=&(-1)^{j-n}(-1)^{j-m}(\delta{}_{(E_{1}-\frac{1}{2}}U^{E_{1}}{}_{|D_{1}|}\delta{}^{(D_{1}-\frac{1}{2}}......\delta{}_{E_{2j})\frac{1}{2}}U^{|E_{2j}|}{}_{D_{2j}}\epsilon{}^{D_{2j})\frac{1}{2}})\\
&=&(-1)^{2(j-m)+m-n}U^{-m}{}_{-n}\\
&=&(-1)^{m-n}U^{-m}{}_{-n}
\end{eqnarray}
$$
 
所以 $(U^{-1})^{n}{}_{m}=(-1)^{m-n}U^{-n}{}_{-m}$。从 $3j$ 符号的定义可以看出  符号是三个不可约表示空间的张量积空间到平凡子空间的投影算符的矩阵元，因此它在 $SU(2)$ 变换下不变，即
$$
D^{(j_{1})m_{1}}{}_{n_{1}}(g)D^{(j_{2})m_{2}}{}_{n_{2}}(g)D^{(j_{3})m_{3}}{}_{n_{3}}(g)\begin{align*}\begin{split}\left (\begin{array}{ll}
j_{1}&j_{2}&j_{3} \\
m_{1}&m_{2}&m_{3}
\end{array}\right)=\end{split}\begin{split}\left (\begin{array}{ll}
j_{1}&j_{2}&j_{3} \\
n_{1}&n_{2}&n_{3}
\end{array}\right)\end{split}\end{align*}
$$
用新的记号可以方便的证明这个结论
$$
\begin{eqnarray}
&&D^{(j_{1})m_{1}}{}_{n_{1}}(g)D^{(j_{2})m_{2}}{}_{n_{2}}(g)D^{(j_{3})m_{3}}{}_{n_{3}}(g)\begin{pmatrix}
j_{1}&j_{2}&j_{3}\\
m_{1}&m_{2}&m_{3}
\end{pmatrix}\\
&=&D^{(j_{1})m_{1}}{}_{n_{1}}(g)D^{(j_{2})m_{2}}{}_{n_{2}}(g)D^{(j_{3})m_{3}}{}_{n_{3}}(g)l_{A_{1}...A_{2j_{1}};B_{1},...,B_{2j_{2}};C_{1}...C_{2j_{3}}}\psi{}^{A_{1}...A_{2j_{1}}}_{j_{1},m_{1}}\psi{}^{B_{1}...B_{2j_{2}}}_{j_{2},m_{2}}\psi{}^{C_{1}...C_{2j_{3}}}_{j_{3},m_{3}}\\
&=&l_{A_{1}...A_{2j_{1}};B_{1},...,B_{2j_{2}};C_{1}...C_{2j_{3}}}(D\psi{}_{j_{1},n_{1}})^{A_{1}...A_{2j_{1}}}(D\psi{}_{j_{1},n_{2}})^{B_{1}...B_{2j_{2}}}(D\psi{}_{j_{1},n_{3}})^{C_{1}...C_{2j_{3}}}\\
&=&\begin{pmatrix}
j_{1}&j_{2}&j_{3}\\
n_{1}&n_{2}&n_{3}
\end{pmatrix}
\end{eqnarray}
$$
当然也可以证明投影算符是不变的，即 
 $$
\begin{eqnarray}
D^{(j_{1})n_{1}}{}_{m_{1}}D^{(j_{1})n_{2}}{}_{m_{2}}D^{(j_{1})n_{3}}{}_{m_{3}}l_{m_{1}m_{2}m_{3}}=l_{n_{1}n_{2}n_{3}}
\end{eqnarray}
$$
证明是直接的：
$$
\begin{eqnarray}
&&D^{(j_{1})n_{1}}{}_{m_{1}}(g)D^{(j_{2})n_{2}}{}_{m_{2}}(g)D^{(j_{3})n_{3}}{}_{m_{3}}(g)l_{m_{1}m_{2}m_{3}}\\
&=&D^{(j_{1})n_{1}}{}_{m_{1}}(g)D^{(j_{2})n_{2}}{}_{m_{2}}(g)D^{(j_{3})n_{3}}{}_{m_{3}}(g)l_{A_{1}...A_{2j_{1}};B_{1},...,B_{2j_{2}};C_{1}...C_{2j_{3}}}\psi^{\dagger}{}^{A_{1}...A_{2j_{1}}}_{j_{1},m_{1}}\psi^{\dagger}{}^{B_{1}...B_{2j_{2}}}_{j_{2},m_{2}}\psi^{\dagger}{}^{C_{1}...C_{2j_{3}}}_{j_{3},m_{3}}\\
&=&l_{A_{1}...A_{2j_{1}};B_{1},...,B_{2j_{2}};C_{1}...C_{2j_{3}}}(\psi^{\dagger}{}_{j_{1},n_{1}}D^{\dagger})^{A_{1}...A_{2j_{1}}}(\psi^{\dagger}{}_{j_{1},n_{2}}D^{\dagger})^{B_{1}...B_{2j_{2}}}(\psi^{\dagger}{}_{j_{1},n_{3}}D^{\dagger})^{C_{1}...C_{2j_{3}}}\\
&=&l_{A_{1}...A_{2j_{1}};B_{1},...,B_{2j_{2}};C_{1}...C_{2j_{3}}}\psi^{\dagger}{}_{j_{1},n_{1}}^{D_{1}...D_{2j_{1}}}D^{\dagger A_{1}...A_{2j_{1}}}{}_{D_{1}...D_{2j_{1}}}\psi^{\dagger}{}^{E_{1}...D_{2j_{2}}}_{j_{1},n_{2}}D^{\dagger B_{1}...B_{2j_{2}}}{}_{E_{1}...E_{2j_{2}}}\psi^{\dagger}{}^{F_{1}...F_{2j_{3}}}_{j_{1},n_{3}}D^{\dagger C_{1}...C_{2j_{3}}}{}_{F_{1}...F_{2j_{3}}}\\
&=&l_{D_{1}...D_{2j_{1}};E_{1},...,E_{2j_{2}};F_{1}...F_{2j_{3}}}\psi{}_{j_{1},n_{1}}^{D_{1}...D_{2j_{1}}}\psi{}^{E_{1}...D_{2j_{2}}}_{j_{1},n_{2}}\psi{}^{F_{1}...F_{2j_{3}}}_{j_{1},n_{3}}\\
&=&l_{n_{1}n_{2}n_{3}}
\end{eqnarray}
$$
称其为 $3$ 阶 **intertwiner**。多个 $l_{m_{1}m_{2}m_{3}}$ 通过 $\epsilon{}_{mn}$ 的缩并所得的高阶张量依旧是 $SU(2)$ 不变的，所以可以生成高阶 intertwiner。

我们的希尔伯特空间是一个矢量空间，任意一个元素都可以用魏格纳矩阵元函数来展开。前面定义过乘法算符，它的直接表达式并不是魏格纳矩阵元函数的线性展开，而是它们相乘。所以其实需要证明这个定义是良好的，也就是需要证明两个魏格纳矩阵元函数的乘积可以展开为魏格纳矩阵元函数的线性组合。这个结论其实是 $CG$ 定理的直接推论，下面给出证明。
证明CG定理的时候其实给出了两个角动量耦合的具体展开，就是依次用逐渐变少的 $\epsilon{}_{AB}$ 去缩并，这里无非是进行两遍两个角动量的耦合，也就是
$$
\begin{eqnarray}
D^{(j_{1})m_{1}}{}_{n_{1}}D^{(j_{2})m_{2}}{}_{n_{2}}D^{(j)m}{}_{n}\begin{pmatrix}
j_{1}&j_{2}&j\\
m_{1}&m_{2}&m
\end{pmatrix}&=&\begin{pmatrix}
j_{1}&j_{2}&j\\
n_{1}&n_{2}&n
\end{pmatrix}\\

D^{(j_{1})m_{1}}{}_{n_{1}}D^{(j_{2})m_{2}}{}_{n_{2}}D^{(j)m}{}_{n}(D^{(j)-1})^{n}{}_{l}\begin{pmatrix}
j_{1}&j_{2}&j\\
m_{1}&m_{2}&m
\end{pmatrix}&=&-\begin{pmatrix}
j_{1}&j_{2}&j\\
n_{1}&n_{2}&n
\end{pmatrix}(D^{(j)-1})^{n}{}_{l}\\

D^{(j_{1})m_{1}}{}_{n_{1}}D^{(j_{2})m_{2}}{}_{n_{2}}\begin{pmatrix}
j_{1}&j_{2}&j\\
m_{1}&m_{2}&m
\end{pmatrix}&=&\begin{pmatrix}
j_{1}&j_{2}&j\\
n_{1}&n_{2}&n
\end{pmatrix}(D^{(j)-1})^{n}{}_{m}\\


D^{(j_{1})m_{1}}{}_{n_{1}}D^{(j_{2})m_{2}}{}_{n_{2}}\sum\limits_{jm}^{}d_{j}\begin{pmatrix}
j_{1}&j_{2}&j\\
m_{1}&m_{2}&m
\end{pmatrix}\begin{pmatrix}
j_{1}&j_{2}&j\\
m'_{1}&m'_{2}&m
\end{pmatrix}&=&\sum\limits_{j}^{}d_{j}\begin{pmatrix}
j_{1}&j_{2}&j\\
n_{1}&n_{2}&n
\end{pmatrix}(-1)^{m-n}D^{(j)-m}{}_{-n}\\
&&\times{}\begin{pmatrix}
j_{1}&j_{2}&j\\
m'_{1}&m'_{2}&m
\end{pmatrix}\\

\sum\limits_{j}^{}d_{j}\begin{pmatrix}
j_{1}&j_{2}&j\\
n_{1}&n_{2}&n
\end{pmatrix}\begin{pmatrix}
j_{1}&j_{2}&j\\
m_{1}&m_{2}&m
\end{pmatrix}(-1)^{m-n}D^{(j)-m}{}_{-n}&=&D^{(j_{1})m_{1}}{}_{n_{1}}D^{(j_{2})m_{2}}{}_{n_{2}}\\
\end{eqnarray}
$$
 所以就可以得到结论，即任何两个表示矩阵的直积可以展开为
$$
\begin{eqnarray}
D^{(j_{1})m_{1}}{}_{n_{1}}D^{(j_{1})m}{}_{n_{2}}=\sum\limits_{j}^{}d_{j}(-1)^{m-n}\begin{pmatrix}
j_{1}&j_{2}&j\\
m_{1}&m_{2}&-m
\end{pmatrix}\begin{pmatrix}
j_{1}&j_{2}&j\\
n_{1}&n_{2}&-n
\end{pmatrix}D^{(j)m}{}_{n}
\end{eqnarray}
$$
当然了，有限个表示矩阵的直积都可以通过多次使用上面的公式展开为表示矩阵的线性组合。现在所掌握的信息可以定义并理解 $CG$ 系数了，$SU(2)$ 表示的 $CG$ 系数 $C^{(j_{1}j_{2}j)}_{m_{1}m_{2}}{}^{m}$ 定义为 $|j_{1}m_{1}\rangle|j_{2}m_{2}\rangle=\sum\limits_{jm}^{}C^{j_{1}j_{2}j}_{m_{1}m_{2}}{}^{m}|j_{1}j_{2};m\rangle$，$C^{(j_{1}j_{2}j)m_{1}m_{2}}{}_{m}$ 由逆变换定义 $|j_{1}j_{2};m\rangle=\sum\limits_{m_{1}m_{2}}^{}C^{(j_{1}j_{2}j)m_{1}m_{2}}{}_{m}|j_{1}m_{1}\rangle|j_{2}m_{2}\rangle$。根据 $CG$ 定理容易知道非零的系数满足 $|j_{1}-j_{2}|<j<j_{1}+j_{2};j_{1}+j_{2}+j$ 为整数 $;m=m_{1}+m_{2}$。
正向 $3j$ 系数的定义有一定的自由度，$CG$ 系数也是一样的，约定其为实的且 
$C^{(j_{1}j_{2}j)}_{j_{1},j-j_{1}}{}^{j}>0$，则可以得到 $C^{(j_{1}j_{2}j)m_{1}m_{2}}{}_{m}=C^{(j_{1}j_{2}j)}_{m_{1}m_{2}}{}^{m}$，后面一律采用这个约定。

把 $SU(2)$ 的表示矩阵作用到 $3j$ 符号和 $CG$ 系数上，会看到他俩遵循相同的变换，所以应该只差一个系数，然后由于两边都是归一化的，所以选择上可以通过调整系数使得他俩相等。也就是可以有魏格纳 $3j-$符号和 $CG$ 系数的关系
$$
\begin{align*}\begin{split}l_{m_{1}m_{2}m_{3}}^{(j^{1}j^{2}j^{3})}=\left (\begin{array}{ll}
j_{1}&j_{2}&j_{3} \\
m_{1}&m_{2}&m_{3}
\end{array}\right)=\frac{1}{\sqrt{ d_{j3} }}(-1)^{j_{1}-j_{2}-m_{3}}C^{(j_{1}j_{2}j_{3})}_{m_{1}m_{2}}{}^{-m_{3}}\end{split}\end{align*}
$$

仔细算一下可以证明 $CG$ 系数有这些性质
1. $C^{(j_{1}j_{2}j)}_{m_{1}m_{2}}{}^{m}=(-1)^{j_{2}+j_{1}-j}C^{(j_{2}j_{1}j)}_{m_{2}m_{1}}{}^{m};$
2. $C^{(j_{1}j_{2}j)}_{m_{1}m_{2}}{}^{m}=(-1)^{j_{2}+j_{1}-j}C^{(j_{1}j_{2}j)}_{-m_{1}-m_{2}}{}^{m};$
3. $C^{(j_{1}j_{2}j)}_{m_{1}m_{2}}{}^{m}C^{(j_{1}j_{2}j')m_{1}m_{2}}{}_{m'}=\delta{}^{jj'}\delta{}^{m}_{m'};$
4. $C^{(j_{1}j_{2}j)}_{m_{1}m_{2}}{}^{m}C^{(j_{1}j_{2}j)m'_{1}m'_{2}}{}_{m}=\delta{}^{m_{1}'}_{m_{1}}\delta{}^{m'_{2}}_{m_{2}};$
5. $D^{(j_{1})m_{1}}{}_{n_{1}}(g)D^{(j_{2})m_{2}}{}_{n_{2}}(g)C^{(j_{1}j_{2}j)}_{m_{1}m_{2}}{}^{m}=C^{(j_{1}j_{2}j)}_{n_{1}n_{2}}{}^{n}D^{(j)m}{}_{n}(g)$。
## 求解量子高斯约束
有了前面的知识，我们就可以开始求解量子高斯约束了。首先要把它提升为量子算符，在此之前要知道它在希尔伯特空间上的作用，因此定义柱一致的**高斯约束矢量场** $Y_{DA}:=\{\mathcal{G},\cdot{}\}$。
由于假设时空流形是无边的，所以有
$$
\begin{eqnarray}
\mathcal{G}&=&\int_{\Sigma{}}^{}\Lambda{}^{i}G_{i}\\
&=&\int_{\Sigma{}}^{}\Lambda{}^{i}(\partial{}_{a}\tilde{P}^{a}_{i}+\epsilon{}^{k}_{ij}\tilde{P}^{a}_{k}A^{j}_{a})\\
&=&-\int_{\Sigma{}}^{}\tilde{P}^{a}_{i}(\partial{}_{a}\Lambda{}^{i}+\epsilon{}^{i}_{jk}A^{j}_{a}\Lambda{}^{k})
\end{eqnarray}
$$
然后可以把它作用到和乐上，也就是
$$
\begin{eqnarray}
Y_{DA}\circ{}A(e)&=&\int_{\Sigma{}}^{}d^{3}x\frac{\partial{}\tilde{P}^{a}_{i}D_{a}\Lambda{}^{i}}{\partial{}\tilde{P}^{b}_{j}(x)}\frac{\delta{}A(e)}{\delta{}A^{j}_{b}(x)}\\
&=&\int_{\Sigma{}}^{}d^{3}xD_{a}\Lambda{}^{i}\frac{\delta{}A(e)}{\delta{}A^{i}_{a}(x)}\\
&=&-\int_{\Sigma{}}^{}d^{3}xD_{a}\Lambda{}^{i}\int_{0}^{1}\delta{}^{3}(x(e(s))-(x,\lambda{}))\dot{e}^{a}A(1,s)\tau{}_{i}A(s,0)ds\\
&=&-\int_{0}^{1}D_{a}\Lambda{}^{i}\dot{e}^{a}A(1,s)\tau{}_{i}A(s,0)ds\\
&=&-\int_{0}^{1}\partial{}_{s}\Lambda{}^{i}A(0,s)\tau{}_{i}A(s,1)+\epsilon{}^{i}_{jk}A^{j}_{a}\Lambda{}^{k}\dot{e}^{a}A(1,s)\tau{}_{i}A(s,0)ds\\
&=&-\int_{0}^{1}\partial{}_{s}\Lambda{}^{i}A(0,s)\tau{}_{i}A(s,1)+\Lambda{}^{k}A(1,s)\dot{e}^{a}A^{j}_{a}[\tau{}_{j},\tau{}_{k}]A(s,0)ds\\
&=&-\int_{0}^{1}\partial{}_{s}\Lambda{}^{i}A(1,s)\tau{}_{i}A(s,0)+\Lambda{}^{k}\partial{}_{s}(A(0,s)\tau{}_{k}A(s,1))ds\\
&=&-\int_{0}^{1}\partial{}_{s}(\Lambda{}^{i}A(1,s)\tau{}_{i}A(s,0))ds\\
&=&-\Lambda{}^{i}(\tau{}_{i}A(e)-A(e)\tau{}_{i})\\
&=&\Lambda{}^{i}[A(e),\tau{}_{i}]
\end{eqnarray}
$$

 即 $Y_{DA}\circ{}A(e)=\Lambda{}^{i}[A(e),\tau{}_{i}]$，可以看到这其实就是一个 $SU(2)$ 的规范变换。定义**量子高斯约束算符** $\hat{\mathcal{G}}:=i\hbar{}Y_{DA}$。则根据前面的推导有 $\hat{\mathcal{G}}=\hbar{}\sum\limits_{v\in{}V(\gamma{})}^{}\hat{J}^{v}_{i}$。要注意这是高斯约束和通量不一样的地方，通量算符需要涉及对一个面上面的边和下面的边用不一样的方式处理，但是高斯约束算符就是单纯的角动量算符。
 
因此如果要求解高斯约束算符，就需要图上每一个顶点的总角动量算符为零，也就是量子态处处都是 intertwiner。对于平凡顶点，比如边以外的位置，或者一条边内部的点，这是天然符合的。平凡顶点本就是平凡表示的，至于一条边内的点，它上面的态记作 $\psi{}_{e}=\sum\limits_{j}^{}\alpha{}^{(j)n}{}_{m}D^{(j)m}_{e}{}_{n}$，其中 $\alpha{}$ 为展开系数，则它可以表示为
$$
\begin{equation}
\psi{}_{e}=\sum\limits_{j}^{}\alpha{}^{(j)n}{}_{m}D^{(j)m}_{b_{e}}{}_{p}D^{(j)p}_{f_{e}}{}_{n}
\end{equation}
$$
其中 $D^{(j)m}_{b_{e}}{}_{n}$ 是这个顶点为界，这条边前面部分的魏格纳矩阵元函数，$D^{(j)p}_{f_{e}}{}_{n}$ 是后面部分的魏格纳矩阵元函数。这一点的角动量则可以表示为 
$$
\begin{equation}
\hat{J}^{v}_{i}=\hat{J}^{(b_{e})}_{i}+\hat{J}^{(f_{e})}_{i}
\end{equation}
$$
右边第一项为所在边终点的角动量，第二项为起点的角动量，容易验证这个角动量作用上去为零。所以求解高斯约束真正非平凡的部分就是要求每一个非平凡顶点上的态都是一个 intertwiner。解完高斯约束后的希尔伯特空间为 $\mathcal{H}^{G}=\oplus_{\alpha{},j}\mathcal{H}'_{\alpha{},j,l=0}\oplus{}\mathbb{C}$。由于每一个非平凡顶点的边都是 intertwiner，所以 $\mathcal{H}^{G}$中的态可以表示为 $T_{s=(\gamma{},j,i)}=\otimes{}_{v\in{}V(\gamma{})}l_{v}^{n_{1}...n_{N_{t(v)}}}{}_{m_{1}...m_{s(v)}}\otimes{}_{e\in{}E(\gamma{})}\pi{}^{j_{e}}$。
# 量子微分同胚约束
LQG 中标准的求解微分同胚约束的方式是使用群平均的方法，也就是直接求解微分同胚群的不动点而不是把微分同胚约束量子化为量子微分同胚变换的生成元来求解。我不喜欢现在求解微分同胚约束的方式，但是先说一下它的合理性。这种操作最根本的原因是，如果量子微分同胚变换是经典微分同胚变换的对应物，那么将不存在非平凡量子微分同胚算符的无穷小生成元。这是因为非平凡的微分同胚变换会改变群胚的像，把群胚的边的形状和位置改变，而我们定义的运动学希尔伯特中间中任意两个像不相同的群胚的态都是正交的，这会导致
$$
\begin{equation}
\langle \hat{U}_{\varphi{}}\psi{}_{\gamma{}}|\psi{}_{\gamma{}}\rangle
=\langle\psi{}_{\varphi{}\circ{}\gamma{}}|\psi{}_{\gamma{}}\rangle
=0,
\qquad
\varphi{}\circ{}\gamma{}\neq{}\gamma{}
\end{equation}
$$
因此无法定义一个有界算符
$$
\begin{equation}
\hat{X}=\lim\limits_{\epsilon{}\rightarrow{}0}^{}\frac{\hat{U}_{\varphi{}(\epsilon{})}-1}{\epsilon{}}
\end{equation}
$$
 这一陈述的一个推论是量子化的微分同胚算符不是弱连续的。
 
 在进行标准的求解微分同胚约束的步骤之前，先分析一下微分同胚变换对量子希尔伯特空间的影响。同胚变换要求有一个连续双射，而微分同胚变换不但要求双射连续，还要求映射是光滑的。所以对于流形上一个单连通局域来说，基本任何一个直觉上认为良好的形变都可以看作一个微分同胚变换。对于一个有限着色图 $\gamma{}$ 来说，一个顶点周围的小邻域内任何边的良好形变（除了改变边和边之间非有限点的重合或者分离关系）几乎都可以看作是微分同胚变换。至于会改变边和边之间非有限点的重合或者分离关系那些形变，比如让两个本来不同向的外向边变为同向，那么可能涉及一个二维区域到一维区域的收缩，这会导致生成这个形变的映射不可逆。因此就不是一个同胚变换了，自然不是一个微分同胚变换。这种形变是那些雅可比为正得连续形变。但是微分同胚变换还会有一些“跳跃”，比如空间反演变换，它会把雅可比变为负的，且与正的在微分同胚变换群的两个不连通分支上。即使具有同号的雅可比，微分同胚映射也可能和恒等映射不在一个连通区域，比如局域总可以找到一个小的平直坐标，在这里面可以构造一个映射
$$
\begin{equation}
\phi{}(x,y,z)=(1-x,-y,z)
\end{equation}
$$
显然这个映射是可逆的，且它和它的逆映射都是光滑的，它的雅可比是正的且为正一，但是由于 $x$ 方向的坐标反演和 $x$ 方向的恒等映射在一维微分同胚群的两个不连通区域，$y$ 方向也一样，因此这个映射和恒等映射也不在同一个连通区域内，所以可以看到微分同胚群是一个非常不连通的复杂的群。这里举得例子事实上和 
$$
\begin{equation}
\varphi{}(x,y,z)
=(-x,-y,z)
\end{equation}
$$
在同一个连通区域内，因为可以构造一个函数
$$
\begin{equation}
\phi{}_{\delta{}}
(x,y,z)
=(\delta{}-x,-y,z),
\end{equation}
$$
来连续地把前面得两个映射连接起来。这种非连通性会改变空间流形得定向，有时候具体的会导致连通两个顶点得边得定向得改变。而改变边的定向是可能改变一个量子态的，比如考虑一个圈和乐与一个边相接，且相接处那个顶点是规范不变的。那么如果圈和乐上面的量子数为 $\frac{1}{2}$，则改变圈上的定向后，整个态会变为原本的负值。由于微分同胚的基础是同胚，所以它不会改变图的拓扑，因此尽管它可以改变边的定向，但是无法改变边与顶点之间的连接关系。

下面说一下如何用群平均的方法求解量子微分同胚约束，设 $Diff_{\gamma{}}$ 为一个有限着色图（图和上面的柱函数） $\gamma{}$ 的微分同胚不变群，$TDiff_{\gamma{}}$ 是其中平凡作用到 $\gamma{}$ 上的部分，则定义$GS_{\gamma{}}:=Diif_{\gamma{}}/TDiff_{\gamma{}}$。即这是全体保着色图 $\gamma{}$ 但是除了恒等元外并不平凡作用于其的集合。显然其中任何一个元素的逆都在这个集合中，且对任意两个元素的复合封闭，因此这也是一个群。然后就可以对这个群进行群平均了，首先可以定义群平均投影算子
$$
\begin{equation}
\hat{P}_{Diff,\gamma{}}:=\frac{1}{o(GS_{\gamma{}})}\sum\limits_{\varphi{}\in{}GS_{\gamma{}}}^{}\hat{U}_{\varphi{}}
\end{equation}
$$
 这个定义是良好的，因为对于一张有限图来，保它不变的前提是保它的像不变，因此模掉对它的平凡作用后，剩下那些保它的像不变的操作只能交换它的顶点、交换它的边、改变它的定向等等，这些不等价操作的个数是有限的。根据重排定理，有
$$
\begin{eqnarray}
\hat{U}_{\varphi{}'}\hat{P}_{Diff,\gamma{}}\psi{}_{\gamma{}}&=&\frac{1}{o(GS_{\gamma{}})}\sum\limits_{\varphi{}\in{}GS_{\gamma{}}}^{}\hat{U}_{\varphi{}'}\hat{U}_{\varphi{}}\psi{}_{\gamma{}}\\
&=&\frac{1}{o(GS_{\gamma{}})}\sum\limits_{\phi{}\in{}GS_{\gamma{}}}^{}\hat{U}_{\phi{}}\psi{}_{\gamma{}}\\
&=&\hat{P}_{Diff,\gamma{}}\psi{}_{\gamma{}}
\end{eqnarray}
$$
 所以群平均投影算子的像是 $GS_{\gamma{}}$ 作用下不变的。但是要想让一个物理态是微分同胚不变的，它必须在整个流形的微分同胚群的映射下不变而不是 $GS_{\gamma{}}$，因此后面必须用微分流形的微分同胚群层面的群来对它进行群平均。这会带来一个问题，如果对运动学希尔伯特空间的一个元素进行这样的群平均，由于像不相等的微分同胚群元是不可数的，这会导致像的自我内积发散，因此任意运动学希尔伯特空间的元素经过这样的群平均后都不在运动学希尔伯特空间中。但是下面可以说明这种 “像” 于任意运动学希尔伯特空间中的元素的内积都是有限的，因此可以把这种 “像” 看作是运动学希尔伯特空间的对偶空间中的元素。也就是微分同胚约束可以在运动学希尔伯特空间的对偶空间中去求解。
 首先定义装备映射
$$
\begin{eqnarray}
\eta{}:Cyl(\bar{\mathfrak{A}}/\mathcal{G})
&\rightarrow{}&Cyl^{*}(\mathfrak{\bar{A}}/\mathcal{G}),
\nonumber\\
\eta{}(\psi{}_{\gamma{}})[\phi{}_{\gamma{}'}]&:=&\sum\limits_{\varphi{}\in{}Diff(\Sigma{})/D_{iff_{\gamma{}}}}^{}\langle\hat{U}_{\varphi{}}\hat{P}_{Diff,\gamma{}}\psi{}_{\gamma{}}|\phi{}_{\gamma{}'}\rangle
\end{eqnarray}
$$
并将它的像记作$Cyl^{*}_{Diff}$。显然如果要把这样的一个定义放在运动学希尔伯特空间上，它的自我内积一定发散。可以在 $Cyl^{*}_{Diff}$ 上配备内积 
$$
\begin{equation}
\langle\eta{}(\psi{}_{\gamma{}})|\eta{}(\phi{}_{\gamma{}'})\rangle:=\eta{}(\psi{}_{\gamma{}})[\phi{}_{\gamma{}'}]
\end{equation}
$$
 这个内积的定义是良好的，因为集合 $Diff(\Sigma{})/Diff_{\gamma{}}$ 的含义是那些不等价的改变 $\gamma{}$ 的微分同胚操作各自只取一个。而最终的内积如果要不为零，就是说明 $\gamma{}$ 和 $\gamma{}'$ 的像相差一个这样的微分同胚变换 $\varphi{}$，由于不等价的变换每种只取一个它会把 $\gamma{}$ 映射为 $\gamma{}'$，因此最终得到的结果是
$$
\begin{eqnarray}
\langle\hat{U}_{\varphi{}}\hat{P}_{Diff,\gamma{}}\psi{}_{\gamma{}}|\phi{}_{\gamma{}'}\rangle
&=&\langle\hat{P}_{Diff,\gamma{}}\psi{}_{\gamma{}}|\hat{U}_{\varphi{}^{-1}}\phi{}_{\gamma{}'}\rangle\\
\nonumber\\
&=&\langle\hat{P}_{Diff,\gamma{}}\psi{}_{\gamma{}}|\phi{}_{\gamma{}}\rangle\\
\end{eqnarray}
$$
又由于 $GS_{\gamma{}}$ 的元素个数是有限的，所以这个内积是有限的。然后就可以对 $Cyl^{*}_{Diff}$ 完备化，得到一个新的希尔伯特空间 。这个希尔伯特空间就是量子微分同胚约束的解空间。
可观测量得是任何一个理论中最重要的那些物理量，而可观测量要想具有 “可观测意义” 就必须在理论的规范约束下不变。而微分同胚是广义相对论最重要的规范对称性，因此可观测量必须在微分同胚约束下不变。下面给出可观测量的定义，下面给出两个基于这种微分同胚变换定义的可观测量，称一个算子 $\hat{O}\in{}\mathcal{L}(\mathcal{H}_{kin})$ 为
1. **强可观测量**，如果 $\hat{U}^{-1}_{\varphi{}}\hat{O}\hat{U}_{\varphi{}}=\hat{O},\forall{}\varphi{}\in{}Diff_{\Sigma{}}$；
2. **弱可观测量**，如果 $\hat{O}[\mathcal{H}_{Diff}]=\mathcal{H}_{Diff}$。
# 量子哈密顿约束（标量约束）
## 圈量子方法
在量子化哈密顿约束之前，先梳理一下圈量子化方法的框架。因为前面分析过，一个边内部的点一定是 $SU(2)$ 规范不变的，而下面说的**非阿贝尔斯托克斯定理**可以把杨-米尔斯曲率在面上的积分转化为联络在面的闭合回路边界上的积分，从而得到一个圈和乐算符。它是一个乘法算符，作用到量子态上的时候会以群表示直积的方式直积到原本的量子态上，因此保持 $\mathcal{H}^{G}$ 不变。所以把经典物理量使用圈量子化的方式提升为算符就天然是规范不变的。
### 非阿贝尔斯托克斯定理
证明一般的非阿贝尔斯托克斯定理之前，先证明一个引理，即对于一个如图所示的包围二维单联通面 $\mathbf{s}$ 的小回路
![[圈表示 2025-06-03 21.17.54.excalidraw|center|300]]
总可以通过坐标重新选取把它参数化为一个边长为 $\epsilon{}$ 的正方形，如图
![[圈表示 2025-06-03 20.45.07.excalidraw|center|300]]
此时有
$$
\begin{eqnarray}
\mathcal{P}_{O}e^{\oint_{\partial{}_{\mathfrak{s}}}^{}A}&=&[1-A_{x}(0,0)\epsilon{}+\frac{1}{2}(A_{x}(0,0)\epsilon{})^{2}+\mathcal{O}(\epsilon{}^{3})][1-A_{y}(-\epsilon{},0)\epsilon{}+\frac{1}{2}(A_{y}(-\epsilon{},0)\epsilon{})^{2}+\mathcal{O}(\epsilon{}^{3})]\nonumber\\
&&\times{}[1+A_{x}(0,-\epsilon{})\epsilon{}+\frac{1}{2}(A_{x}(0,-\epsilon{})\epsilon{})^{2}+\mathcal{O}(\epsilon{}^{3})][1+A_{y}(0,0)\epsilon{}+\frac{1}{2}(A_{y}(0,0)\epsilon{})^{2}+\mathcal{O}(\epsilon{}^{3})]\nonumber\\
&=&1-[A_{x}(0,0)+A_{y}(-\epsilon{},0)-A_{x}(0,-\epsilon{})-A_{y}(0,0)]\epsilon{}+[A_{x}(0,0)A_{y}(-\epsilon{},0)-A_{x}(0,0)A_{x}(0,-\epsilon{})\nonumber\\
&&-A_{x}(0,0)A_{y}(0,0)-A_{y}(-\epsilon{},0)A_{x}(0,-\epsilon{})-A_{y}(-\epsilon{},0)A_{y}(0,0)+A_{x}(0,-\epsilon{})A_{y}(0,0)\nonumber\\
&&+\frac{1}{2}A_{x}(0,0)^{2}+\frac{1}{2}A_{y}(-\epsilon{},0)^{2}+\frac{1}{2}A_{x}(0,-\epsilon{})^{2}+\frac{1}{2}A_{y}(0,0)^{2}]\epsilon{}^{2}+\mathcal{O}(\epsilon{}^{3})\nonumber\\
&=&1+[\partial{}_{x}A_{y}(0,0)-\partial{}_{y}A_{x}(0,0)]\epsilon{}^{2}-A_{x}(0,0)A_{x}(0,-\epsilon{})\epsilon{}^{2}-A_{y}(-\epsilon{},0)A_{y}(0,0)\epsilon{}^{2}\nonumber\\
&&+\frac{1}{2}A_{x}(0,0)[A_{x}(0,-\epsilon{})+\partial{}_{y}A_{x}(0,-\epsilon{})\epsilon{}]\epsilon{}^{2}+...+\mathcal{O}(\epsilon{}^{2})\nonumber\\
&=&1+F_{xy}(0,0)\epsilon{}^{2}+\mathcal{O}(\epsilon{}^{2})\nonumber\\
&=&e^{\int_{\mathbf{s}}^{}\Omega{}}+\mathcal{O}(\epsilon{}^{2})
\end{eqnarray}
$$
其中 $\mathcal{P}_{O}e^{\oint_{\partial{}_{\mathfrak{s}}}^{}A}$ 表示以$O$为基点积分得到的和乐。由于 $F_{xy}(0,0)$ 和曲面里任何一个点的曲率值都只差 $\epsilon{}$ 量级，所以对于小面元来说，$h_{e}$的起点终点事实上可以随便选择。无论怎么选都有
$$
\begin{equation}
\mathcal{P}e^{\oint_{\partial{}_{\mathfrak{s}}}^{}A}=e^{\int_{\mathbf{s}}^{}\Omega{}}
\end{equation}
$$
然后来证明任意一个二维单联通面 $\mathbf{s}$ 上的非阿贝尔斯托克斯定理。对于这样的一个面，如图，我们总可以把它重参数化为一个坐标域为 $[1,0]\times{}[1,0]$ 的正方形，然后用足够大的整数 $N$ 等分它的横纵坐标，形成 $N^{2}$ 个小正方形 ，其中 $\mathbf{s}_{mn}$ 表示右上角坐标为 $(\frac{m}{N},\frac{n}{N})$ 的那个小正方形。
![[圈表示 2025-06-03 15.18.11.excalidraw|center|300]]
定义横移算符 $L_{mn}=e^{\int_{(0,\frac{n}{N})}^{(\frac{m}{N},\frac{n}{N})}A}$ 和纵移算符 $S_{mn}=e^{\int_{(\frac{m}{N},0)}^{(\frac{m}{N},\frac{n}{N})}A}$，以及平易算符$U_{mn}:=L_{mn}S_{0n}$。对于每一个小正方形，可以定义平易依赖的和乐 
$$
\begin{equation}
\mathfrak{h}_{mn}=U_{mn}^{-1}h_{mn}U_{mn}=S_{0n}^{-1}L^{-1}_{mn}4_{mn}3_{mn}2_{mn}1_{mn}L_{mn}S_{0n}
\end{equation}
$$
其中数字代表第几段边上的和乐。对于 $n$ 固定的同一排小正方形，可以计算
$$
\begin{eqnarray}
\prod_{m=1}^{N}\mathfrak{h}_{mn}&=&\prod_{m=1}^{N}S_{0n}^{-1}L^{-1}_{mn}4_{mn}3_{mn}2_{mn}1_{mn}L_{mn}S_{0n}\nonumber\\
&=&S_{0n}^{-1}(\prod_{m=1}^{N}L^{-1}_{mn}4_{mn}3_{mn}2_{mn}1_{mn}L_{mn})S_{0n}\nonumber\\
&=&S_{0n}^{-1}L^{-1}_{Nn}4_{Mn}3_{Nn}2_{Nn}1_{Nn}1_{Nn}^{-1}4_{N-1n}3_{N-1n}2_{N-1n}1_{N-1n}\times{}...\times{}1_{2n}^{-1}4_{1n}3_{1n}2_{1n}1_{1n}1_{1n}^{-1}S_{0n}\nonumber\\
&=&S_{0n}^{-1}L^{-1}_{Nn}4_{Mn}3_{Nn}2_{Nn}4_{N-1n}3_{N-1n}2_{N-1n}\times{}...\times{}4_{1n}3_{1n}2_{1n}S_{0n}
\end{eqnarray}
$$
由于前一个边的第四段边和后一个边的第二段边互逆，所以有 $2_{mn}4_{m-1n}=\mathbb{1}$，因此上式变为
$$
\begin{eqnarray}
\prod_{m=1}^{N}\mathfrak{h}_{mn}&=&S_{0n}^{-1}L^{-1}_{Nn}4_{Nn}3_{Nn}3_{N-1n}\times{}...\times{}3_{1n}2_{1n}S_{0n}\nonumber\\
&=&S_{0n}^{-1}L^{-1}_{Nn}4_{Nn}3_{Nn}3_{N-1n}\times{}...\times{}3_{1n}S_{0n-1}\nonumber\\
&=&S_{0n}^{-1}L^{-1}_{Nn}4_{Nn}L_{Nn-1}S_{0n-1}
\end{eqnarray}
$$
因此如果我们再把$n$也进行求和可以得到
$$
\begin{eqnarray}
\prod_{n=1}^{N}\prod_{m=1}^{N}\mathfrak{h}_{mn}&=&\prod_{n=1}^{N}S_{0n}^{-1}L^{-1}_{Nn}4_{Mn}L_{Nn-1}S_{0n-1}\nonumber\\
&=&S^{-1}_{0N}L^{-1}_{NN}4_{NN}4_{N1}S_{00}\nonumber\\
&=&\mathcal{P}_{O}e^{\oint_{\partial{}_{\mathfrak{s}}}^{}A}
\end{eqnarray}
$$
因此可以得到
$$
\begin{equation}
\mathcal{P}_{O}e^{\oint_{\partial{}_{\mathfrak{s}}}^{}A}=\prod_{n=1}^{N}\prod_{m=1}^{N}U_{mn}^{-1}e^{\int_{\mathbf{s_{mn}}}^{}\Omega{}}U_{mn}=:\prod_{n=1}^{N}\prod_{m=1}^{N}e^{\int_{\mathbf{s}_{mn}}^{}\mathscr{\Omega{}}}
\end{equation}
$$
注意我们对曲面做的剖分其实是非常任意的，所谓正方形只是参数空间的正方形，但是只要我们划分的时候保证内部每个小曲面都和四个小曲面相邻，边上每个小曲面都和三个小曲面相邻，角上每个小曲面都和两个小曲面相邻，那么我们的结论就成立，所以在这种意义下 $\mathscr{\Omega{}}$ 可以不依赖于剖分而定义为
$$
\begin{equation}
\mathscr{\Omega{}}_{p}:=U^{-1}_{p}\Omega{}_{p}U_{p}
\end{equation}
$$
其中 $U_{p}$ 取决于路径，而路径的选取是任意的，只要符合右手定则，先遍历第一个坐标，再遍历第二个坐标即可。即然乘法与路径无关，则上面的表达式也可以化为积分的形式，即
$$
\begin{equation}
\mathcal{P}_{O}e^{\oint_{\partial{}_{\mathfrak{s}}}^{}A}=:\mathcal{P}_{O}e^{\int_{\mathfrak{s}}^{}\mathscr{\Omega{}}}
\end{equation}
$$
事实上右边的积分序是用左边来定义的。但是要注意的是，与一个微小曲面上的积分不同，该表达式中等号左边圈积分得到的和乐的基点决定了等号右边积分序和 $\mathscr{\Omega{}}$ 的定义。
要进行圈量子化就要先把曲率的积分变为和乐，设一个小区域 $\mathfrak{s}$ 的周长为 $\delta{}$，则有
$$
\begin{eqnarray}
\mathop{{\rm lim}}\limits_{\mathfrak{s}\rightarrow{}0}^{}\int_{\mathfrak{s}}^{}\Omega{}=\mathcal{P}e^{\oint_{\partial{}_{\mathfrak{s}}}^{}A}-1=1+\delta{}A_{t}-1=\frac{1}{2}(1+\delta{}A_{t})-\frac{1}{2}(1-\delta{}A_{t})=\frac{1}{2}(h^{-1}_{e}-h_{e})
\end{eqnarray}
$$
该表达式要注意两点：
1. 我们证明前面的定理的时候，积分得到和乐是用的符号为 $\mathfrak{s}=1$，但是为了与 $loop$ 相一致，所以这里用的符号为 $\mathfrak{s}=-1$，不同约定得到的结果是不一样的。
2. 上面的关系不等价于
$$
\begin{equation}
\mathop{{\rm lim}}\limits_{\mathfrak{s}\rightarrow{}0}^{}\int_{\mathfrak{s}}^{}\Omega{}=h^{-1}_{e}=-h_{e}
\end{equation}
$$
因为对于该式，等号左边在 $\mathfrak{s}\rightarrow{}0$ 时趋于零，但是等号右边在该极限下趋于 $1$。
### 量子化
从经典到量子过渡的时候，选取什么样的表示不重要，在借助生成元的迹来表述经典理论的时候，可以取任意的表示。但是重要的是经典的泊松代数必须和量子化的对易关系相一致，也就是要保证
$$
\begin{equation}
\hat{\tilde{P}}^{a}_{i}(x)h^{(j)}_{e}=-i\hbar{}\frac{\delta{}h^{(j)}_{e}}{\delta{}A^{i}_{a}(x)}=i\hbar{}\int_{0}^{\delta{}}\delta{}(x,x(t))\dot{e}^{a}(t)h^{(j)}_{\delta{},t}\tau{}^{(j)}_{i}h^{(j)}_{t,0}dt
\end{equation}
$$
从而有对易关系
$$
\begin{equation}
[\hat{\tilde{P}}^{a}_{i}(x),\hat{h}^{(j)}_{e}]=i\hbar{}\int_{0}^{\delta{}}\delta{}(x,x(t))\dot{e}^{a}(t)\hat{h}^{(j)}_{\delta{},t}\tau{}^{(j)}_{i}\hat{h}^{(j)}_{t,0}dt
\end{equation}
$$
要注意 $\hat{h}^{(z)}_{e}$ 是和乐的乘法算符，它和非算符的和乐是有区别的。利用上面的关系，可以对曲率项进行量子化，在此之前算一下共轭动量在一个剖分后的原胞内的积分作用到一个端点在该原胞中心 $v$ 的和乐上：
$$
\begin{eqnarray}
\int_{C_{\epsilon{}}}^{}\hat{\tilde{P}}^{a}_{i}h^{(j)}_{e}=i\hbar{}\int_{C_{\epsilon{}}}^{}\int_{0}^{\delta{}}\delta{}(x,x(t))\dot{e}^{a}(t)h^{(j)}_{\delta{},t}\tau{}^{(j)}_{i}h^{(j)}_{t,0}dt
\end{eqnarray}
$$
这里不存在左右手的问题，因为 $\delta{}$ 函数可以直接对外层的右手原胞进行体积分，从而只得到里面那一层积分。对于里面那层积分，又可以根据和乐是参数区间为 $[0,\epsilon{}]$ 的前半段在原胞内还是$[\delta{}-\epsilon{},\epsilon{}]$ 的后半段在原胞内变为
$$
\int_{C_{\epsilon{}}}^{}\hat{\tilde{P}}^{a}_{i}h^{(j)}_{e}=i\hbar{}\dot{e}^{a}\epsilon{}\cdot{}\begin{align*}\begin{split}\left\{\begin{array}{ll}h^{(j)}_{e}\tau{}^{(j)}_{i}，v=s(e)\\
\tau{}^{(j)}_{i}h^{(j)}_{e}，v=t(e)
\end{array}\right.\end{split}\end{align*}=:i\hbar{}{\rm sgn}(e,v)\dot{e}^{a}\epsilon{}J^{v,e}_{i}h^{(j)}_{e}
$$
然后可以尝试圈量子化曲率项，最简单的曲率项就是哈密顿约束中的欧式项，也就是可以把哈密顿约束分为
$$
\begin{equation}
\mathcal{S}(N):=\frac{\kappa{}\beta{}^{2}}{2}\int_{\Sigma{}}^{}N\frac{\tilde{P}^{a}_{i}\tilde{P}^{b}_{j}}{(e)}[\epsilon{}^{ij}{}_{k}F^{k}_{ab}-2(1+\beta{})K^{i}_{[a}K^{j}_{b]}]=\mathcal{S}_{E}(N)-2(1+\beta{}^{2})\mathcal{T}(N)
\end{equation}
$$
其中第一项就叫做欧式项。忽略前面的系数后这一项为
$$
\begin{equation}
\frac{\epsilon{}^{ij}{}_{k}\tilde{P}^{a}_{i}\tilde{P}^{b}_{j}}{\sqrt{ q }}\Omega{}^{k}_{ab}
\end{equation}
$$
这里先分析一下马老师“新哈密顿算符”文章里的方法，这种方法需要依赖一个可逆的体积算符，也是在他们自己文章里提出来的。有了可逆的体积算符，哈密顿约束的圈量子化可以大大简化。分析完这个方法后再分析蒂曼等人开发的标准方法。
首先利用
$$
\begin{equation}
{\rm tr}(\tau{}^{(j)}_{i}\tau{}^{(j)}_{j})=\mathcal{N}_{j}\delta{}_{ij}
\end{equation}
$$
其中 $\mathcal{N}^{(j)}=-\frac{d_{j}J^{2}}{3}$，可以将欧式项变为
$$
\begin{equation}
\frac{4\epsilon{}^{ijk}\tilde{P}^{a}_{i}\tilde{P}^{b}_{j}}{\mathcal{N}_{j}\sqrt{ q }}{\rm tr}(\tau{}^{(j)}_{k}\tau{}^{(j)}_{l})\Omega{}^{l}_{ab}=\frac{4\epsilon{}^{ijk}\tilde{P}^{a}_{i}\tilde{P}^{b}_{j}}{\mathcal{N}_{j}\sqrt{ q }}{\rm tr}(\tau{}^{(j)}_{k}\Omega{}^{(j)}_{ab})
\end{equation}
$$
从而在最简单的情况下，在一个剖分后的原胞内可以积分为
$$
\begin{eqnarray}
&&\frac{4\epsilon{}^{ijk}}{\mathcal{N}_{j}\sqrt{ V }}\int_{C_{\epsilon{}}}^{}{\rm tr}(\tau{}^{(j)}_{k}\Omega{}^{(j)}_{ab})\tilde{P}^{a}_{i}\int_{C_{\epsilon{}}}^{}\tilde{P}^{b}_{j}\frac{1}{\sqrt{ V }}
\nonumber\\
&=&-\frac{4\hbar{}^{2}\epsilon{}^{ijk}}{\mathcal{N}_{j}\sqrt{ V }}{\rm tr}(\tau{}^{(j)}_{k}\Omega{}^{(j)}_{ab})\epsilon{}^{2}{\rm sgn}(e,v){\rm sgn}(e',v)\dot{e}^{a}\dot{e}'^{b}J^{v,e}_{i}J^{v,e'}_{j}\frac{1}{\sqrt{ V }}
\end{eqnarray}
$$
我们要用公式
$$
\mathop{{\rm lim}}\limits_{\mathfrak{s}\rightarrow{}0}^{}\int_{\mathfrak{s}}^{}\Omega{}=\frac{1}{2}(h^{-1}_{e}-h_{e})
$$
的话，就需要让 $\Omega{}^{(j)}_{ab}$ 与沿着两个边外向方向的切失缩并来得到 $\Omega{}^{(j)}_{ee'}$，而对于终点在 $v$ 的边来说，切失差的负号正好与 ${\rm sgn}(e,v)$ 的负号抵消，也就是
$$
\begin{equation}
\Omega{}^{(j)}_{ab}{\rm sgn}(e,v)\dot{e}^{a}=\Omega{}^{(j)}_{eb}
\end{equation}
$$
所以最终可以得到
$$
\begin{equation}
\int_{C_{\epsilon{}}}^{}\frac{4\epsilon{}^{ijk}\tilde{P}^{a}_{i}\tilde{P}^{b}_{j}}{\mathcal{N}_{j}\sqrt{ q }}{\rm tr}(\tau{}^{(j)}_{k}\Omega{}^{(j)}_{ab})=\frac{2\hbar{}^{2}\epsilon{}^{ijk}}{\mathcal{N}_{j}\sqrt{ V }}{\rm tr}[\tau{}^{(j)}_{k}(h^{(j)}_{\alpha{}_{ee'}}-h^{(j)}_{\alpha{}_{e'e}})]J^{v,e}_{i}J^{v,e'}_{j}\frac{1}{\sqrt{ V }}
\end{equation}
$$
其中 $\alpha{}_{ee'}$ 表示从 $e$ 方向出发，从 $e'$ 方向回来的小环路。
至于哈密顿约束中的剩下一项，也就是外曲率项，则要稍微曲折一下。可以先定义外曲率泛函
$$
\begin{equation}
K:=\kappa{}\beta{}\int_{\Sigma{}}^{}\tilde{P}^{a}_{i}K^{i}_{a}
\end{equation}
$$
可以看到外曲率可以从中得到
$$
\begin{equation}
K^{i}_{a}(x)
=\frac{1}{\kappa{}\beta{}}[A^{i}_{a}(x),K]
\end{equation}
$$
通过直接的计算容易证明
$$
\begin{equation}
K
=\beta{}^{-2}[\mathcal{S}_{E},V_{\Sigma{}}]
\end{equation}
$$
因此可以通过欧式项和体积算符来构造出外曲率项。
### 蒂曼的方法
由于都是圈量子化的方法，所以蒂曼的方法也需要使用非阿贝尔斯托克斯定理。它们当时没有可逆的体积算符，所以需要用一些小技巧来处理 $\frac{1}{\sqrt{ q }}$ 这一项。通过计算可以发现，使用余标架可以很好的把这一项处理掉，也就是
$$
\begin{equation}
e^{i}_{a}(x)=\frac{(\kappa{}\beta{})^{2}}{2}\epsilon{}_{abc}\epsilon{}^{ijk}\frac{\tilde{P}^{b}_{j}\tilde{P}^{c}_{k}}{(e)}(x)
\end{equation}
$$
而前者又可以计算为
$$
\begin{equation}
e^{i}_{a}(x)=\frac{2}{\kappa{}\beta{}}[A^{i}_{a}(x),V_{R_{x}}]
\end{equation}
$$
其中 $V_{R_{x}}$ 是包含 $x$ 的任意区域的体积。由于
$$
\begin{eqnarray}
\epsilon{}^{ij}{}_{k}\frac{\tilde{P}^{a}_{i}\tilde{P}^{b}_{j}}{(e)}F^{k}_{ab}&=&\frac{\epsilon{}^{ij}{}_{k}}{2(e)}(\delta{}^{a}_{c}\delta{}^{b}_{d}-\delta{}^{a}_{d}\delta{}^{b}_{c})\tilde{P}^{c}_{i}\tilde{P}^{d}_{j}F^{k}_{ab}\\
&=&\frac{\epsilon{}^{ijk}}{2(e)}\epsilon{}^{abe}\epsilon{}_{cde}\tilde{P}^{c}_{i}\tilde{P}^{d}_{j}F_{abk}\\
&=&\frac{2}{(\kappa{}\beta{})^{3}}[A^{k}_{e},V_{R_{x}}]\epsilon{}^{abe}F_{abk}\\
&=&\frac{2}{(\kappa{}\beta{})^{3}}[A^{i}_{e},V_{R_{x}}]\epsilon{}^{abe}F_{ab}^{j}\delta{}_{ij}\\
&=&\frac{2}{(\kappa{}\beta{})^{3}}\epsilon{}^{abc}F_{ab}^{i}[A^{j}_{c},V_{R_{x}}](-2Tr[\tau{}_{i}\tau{}_{j}])\\
&=&-\frac{4}{(\kappa{}\beta{})^{3}}\epsilon{}^{abc}Tr(F_{ab}[A_{c},V_{R_{x}}])
\end{eqnarray}
$$
所以可以把欧式项和外曲率项写为
$$
\begin{equation}
\mathcal{S}_{E}(N)=-\frac{2}{\kappa{}^{2}\beta{}}\int_{\Sigma{}}^{}d^{3}xN(x)\epsilon{}^{abc}Tr(F_{ab}(x)\{A_{c}(x),V_{R_{x}}\})
\end{equation}
$$
和
$$
\begin{equation}
\mathcal{T}(N)=-\frac{2}{\kappa{}^{4}\beta{}^{3}}\int_{\Sigma{}}^{}d^{3}xN(x)\epsilon{}^{abc}Tr(\{A_{a},K\}\{A_{b},K\}\{A_{c},K\})
\end{equation}
$$
蒂曼的量子化方法比较复杂一点，接着要处理联络和体积的泊松括号，由于
$$
\begin{eqnarray}
\frac{\partial{}\mathop{{\rm lim}}\limits_{s\rightarrow{}0}^{}\int_{0}^{s}A_{a}\dot{e}^{a}_{i}dt}{\partial{}A(s)}&=&\frac{\partial{}\mathop{{\rm lim}}\limits_{s\rightarrow{}0}^{}\int_{0}^{s}-\dot{A}A^{-1}dt}{\partial{}A(s)}\\
&=&\frac{\partial{}\mathop{{\rm lim}}\limits_{s\rightarrow{}0}^{}\int_{0}^{s}-\dot{(lnA)}dt}{\partial{}A(s)}\\
&=&-\frac{\partial{}(lnA(s)-ln1)}{\partial{}A(s)}\\
&=&-A(s)^{-1}
\end{eqnarray}
$$
所以有代数关系 $\{\mathop{{\rm lim}}\limits_{s\rightarrow{}0}^{}\int_{0}^{s}A_{a}\dot{e}^{a}_{i}dt,\cdot{}\}=-A(s)^{-1}\{A(s),\cdot{}\}$。结合非阿贝尔斯托可以定理，在对空间流形进行三角剖分后，一个四面体 $\Delta{}(v)$ 中有
$$
\begin{equation}
\int_{P_{ab}}^{}\int_{s_{c}}^{}\pi{}_{abc}=3V(\Delta{})
\end{equation}
$$
其中 $\pi{}_{abc}$ 为排列符号，$abc$ 互相不能相等。所以对于每一个顶点 $v$，欧式项可以计算为
$$
\begin{eqnarray}
3\mathcal{S}^{v,\epsilon{}}_{E}(N)&=&
-\frac{2}{\kappa{}^{2}\beta{}}3V(\Delta{})N(v)\epsilon{}^{abc}F_{ab}\{A_{c},V_{R}\}\\
&=&-\frac{2}{\kappa{}^{2}\beta{}}N(v)\epsilon{}^{abc}\int_{P_{ab}}^{}\int_{s_{c}}^{}F_{ab}\{A_{c},V_{R}\}\\
&=&-\frac{2}{\kappa{}^{2}\beta{}}N(v)\epsilon{}^{abc}\frac{1}{2}(A(\alpha{}_{ab})^{-1}-A(\alpha{}_{ab}))(-A(s_{c})^{-1}\{A(s_{c}),V_{R}\})\\
&=&\frac{2}{\kappa{}^{2}\beta{}}N(v)\epsilon{}^{abc}\frac{1}{2}(A(\alpha{}_{ab})^{-1}-A(\alpha{}_{ba})^{-1})A(s_{c})^{-1}\{A(s_{c}),V_{R}\}\\
&=&\frac{2}{\kappa{}^{2}\beta{}}N(v)\frac{1}{2}(\epsilon{}^{abc}A(\alpha{}_{ab})^{-1}+\epsilon{}^{bac}A(\alpha{}_{ba})^{-1})A(s_{c})^{-1}\{A(s_{c}),V_{R}\}\\
&=&\frac{2}{\kappa{}^{2}\beta{}}N(v)\epsilon{}^{abc}A(\alpha{}_{ab})^{-1}A(s_{c})^{-1}\{A(s_{c}),V_{R}\}
\end{eqnarray}
$$
从而得到欧式项为
$$
\begin{equation}
\mathcal{S}^{v,\epsilon{}}_{E}(N)=\frac{2}{3\kappa{}^{2}\beta{}}N(v)\epsilon{}^{ijk}Tr(A(\alpha{}_{ij}))^{-1}A(s_{k})^{-1}\{A(s_{k}),V_{R_{v}}\}
\end{equation}
$$
同理可以得到
$$
\begin{equation}
\mathcal{T}^{v,\epsilon{}}(N)=\frac{\sqrt{ 2 }}{6\kappa{}^{4}\beta{}^{3}}N(v)\epsilon{}^{ijk}Tr(A(s_{i})^{-1}\{A(s_{i}),K\})A(s_{j})^{-1}\{A(s_{j}),K\})A(s_{k})^{-1}\{A(s_{k}),K\})
\end{equation}
$$
但是要注意，这种方式得到的哈密顿量依赖于剖分的参数 $\epsilon{}$ 。所以如果最终想等一一个定义良好的哈密顿量，必须证明它和剖分无关。这一点在运动学希尔伯特空间或者规范不变希尔伯特空间上是做不到，但是下面说明在微分同胚不变的希尔伯特空间上是可以的。
设 $\eta{}(\phi{})\in{}\mathcal{H}_{Diff}$，则有
$$
\begin{eqnarray}
\eta{}(\phi{})[\mathcal{\hat{S}}^{\epsilon{}}(N)\psi{}_{\gamma{}}]
&=&\sum\limits_{\varphi{}\in{}GS_{\gamma{}}}^{}\langle\hat{U}_{\varphi{}}\phi{}|\hat{U}_{\epsilon{}'\rightarrow{}\epsilon{}}\mathcal{\hat{S}}^{\epsilon{}'}(N)\psi{}_{\gamma{}}\rangle\\
&=&\sum\limits_{\varphi{}\in{}GS_{\gamma{}}}^{}\langle\phi{}|\hat{U}^{\dagger}_{\varphi{}}\hat{U}_{\epsilon{}'\rightarrow{}\epsilon{}}\mathcal{\hat{S}}^{\epsilon{}'}(N)\psi{}_{\gamma{}}\rangle\\
&=&\sum\limits_{\varphi{}'\in{}GS_{\gamma{}}}^{}\langle\phi{}|\hat{U}^{\dagger}_{\varphi{}'}\mathcal{\hat{S}}^{\epsilon{}'}(N)\psi{}_{\gamma{}}\rangle\\
&=&\sum\limits_{\varphi{}'\in{}GS_{\gamma{}}}^{}\langle\hat{U}_{\varphi{}'}\phi{}|\mathcal{\hat{S}}^{\epsilon{}'}(N)\psi{}_{\gamma{}}\rangle\\
&=&\eta{}(\phi{})[\hat{\mathcal{S}}^{\epsilon{}'}(N)\psi{}_{\gamma{}}]
\end{eqnarray}
$$
原因就在于不同的剖分尺寸，对应着选取路径 $\alpha{}_{ij}(\Delta{})$ 时，圈算符横跨过原本两条边的那条第三条边的位置会发生变化。但是这种变化在微分同胚意义下是等价的，所以 $\eta{}(\phi{})[\mathcal{\hat{S}}^{\epsilon{}}(N)\psi{}_{\gamma{}}]$ 与  无关。所以在 $\mathcal{H}_{Diff}$ 上哈密顿约束算符极限存在。由于外曲率项也使用精神一样的量子化方案，所以可以证明它的极限也是存在的。
