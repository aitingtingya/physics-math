本文
 
Reissner–Nordström (RN)-AdS 黑洞的线元
$$
ds^{2}=-f(r)dt^{2}+\frac{dr^{2}}{f(r)}+r^{2}d\Omega^{2}
$$
其中$\displaystyle d\Omega^{2}$是2-球面的度规、$\displaystyle f(r)$表达式
$$
f(r)=1-\frac{2M}{r}+\frac{q^{2}}{r^{2}}+\frac{r^{2}}{l^{2}}
$$
其中$\displaystyle M,q$分别为黑洞的ADM质量和电荷。
将线元的时间分量$(g_{tt})$取$\displaystyle 0$可以得到视界半径
$$
f(r_{+})=1-\frac{2M}{r_{+}}+\frac{q^{2}}{r_{+}^{2}}+\frac{r^{2}_{+}}{l^{2}}=0
$$
使用"Euclidean trick"可以计算黑洞的温度$\displaystyle T$
$$
T=\frac{1}{\beta}=\frac{f'(r_{+})}{4\pi}
=\frac{1}{4\pi r_{+}}\left( 1+\frac{3r^{2}_{+}}{l^{2}}-\frac{q^{2}}{r_{+}^{2}} \right)
$$
熵$\displaystyle S$
$$
S=\frac{A}{4}=\pi r_{+}^{2}
$$
当然，从热力学公式计算同样可以得到这个结果：
$$
T=\frac{ \partial M }{ \partial S } 
=\frac{ \partial M }{ \partial r_{+} }\frac{ \partial r_{+} }{ \partial S }  
=-\frac{f'(r_{+})}{f'(M)}\frac{ \partial r_{+} }{ \partial S }
=\frac{f'(r_{+})}{2/r_{+}} \frac{1}{2\pi r_{+}}
=\frac{f'(r)}{4\pi}
$$
黑洞化学将AdS半径$\displaystyle l$认同为热力学压力$\displaystyle P$,经由公式：
$$
P=-\frac{\Lambda}{8\pi}=\frac{3}{8\pi l^{2}}
$$
# Smarr formula
第一定律(通过在KN-AdS黑洞中取$\displaystyle J=0$也可得到)
$$
dH=TdS+VdP+\Phi dQ
$$
在黑洞化学语境下，$\displaystyle H$为黑洞的焓，其就是ADM质量$\displaystyle M$.
由上文的视界面公式，有
$$
M=\frac{r_{+}}{2}\left( 1+\frac{q^{2}}{r_{+}^{2}}+\frac{r^{2}_{+}}{l^{2}} \right)
=\frac{1}{2\sqrt{ \pi S }}\left( S+\pi q^{2}+\frac{8}{3}PS^{2} \right)
$$
而诸热力学量$\displaystyle S,P,Q$的共轭量也可定义。在这里我们使用这种新的定义，$\displaystyle Q=q^{2}$，为热力学广延量用于后续的分析，而非$\displaystyle q$.
$$
T=\frac{ \partial M }{ \partial S } \bigg|_{q^{2},P}
=\frac{1}{4\sqrt{ \pi }}\left( 8 P \sqrt{ S }+\frac{1}{ \sqrt{S}} -\frac{\pi Q}{S^{3/2}}\right)
=\frac{8 P S^2-\pi  Q^{2}+S}{4 \sqrt{\pi } S^{3/2}}
$$
$$
V = \frac{ \partial M }{ \partial P }  \bigg|_{q^{2},S}
= \frac{4 S^{3/2}}{3 \sqrt{\pi }}
\left( =\frac{4}{3}\pi r_{+}^{3} \right)
$$
$$
\Phi= \frac{ \partial M }{ \partial Q }=\frac{Q\sqrt{ \pi }}{\sqrt{ S }} 
$$

$$
\Psi = \frac{ \partial M }{ \partial Q } \bigg|_{S,P}
=\frac{ \partial M }{ \partial (q^{2}) } \bigg|_{S,P}
=\frac{1}{2}\sqrt{ \frac{\pi}{S} }
\left( =\frac{1}{2r_{+}} \right)
$$
这里可以看到$\displaystyle \Psi$的表达式大大简化。
由此可以还原出($\displaystyle Q=q^{2}$的)Smarr公式
$$
M=2(TS+\Phi Q-PV)
$$
# State equation
$\displaystyle T$的表达式等价于
$$
P = \frac{T}{2r_{+}}-\frac{1}{8\pi r_{+}^{2}}+\frac{Q}{8\pi r_{+}^{4}}
$$
我们知道范德华流体（Van der Waals fluid）的状态方程
$$
\left( P+\frac{a}{v^{2}} \right)(v-b)=kT
$$
我们可以令$\displaystyle v$为比体积
$$
v=2r_{+}=\frac{1}{\Phi}
$$
于是RN-AdS黑洞也有"状态方程"
$$
P = \frac{T}{v}-\frac{1}{2\pi v^{2}}+\frac{2q^{2}}{\pi v^{4}}=\frac{T}{v}-\frac{1}{2\pi v^{2}}+\frac{2Q}{\pi v^{4}} 
$$
定义一个新量，热荷密度$\displaystyle \sigma$
$$
\sigma=\frac{\pi q^{2}}{S}=\frac{\pi Q}{S}=\frac{4Q}{v^{2}}
$$
由于$\displaystyle S \propto \mathcal{A}$，所以$\displaystyle \sigma$有电荷在视界面上的面密度的含义。
$$
\begin{align}
P&=\frac{T}{v}-\frac{1}{2\pi v^{2}}+\frac{\sigma}{2\pi v^{2}} \\
&=\frac{T}{v}-\frac{1-\sigma}{2\pi v^{2}}
\end{align}
$$
这和VdW的状态方程很相似。对比发现
$$
a\to \frac{1-\sigma}{2\pi}, \quad b\to 0
$$
$\displaystyle a>0$量度了“分子”间的吸引力的大小。可以想见，电荷的面密度越大，其静电排斥力越强，则$\displaystyle a$越小。当$\displaystyle \sigma\to 1$时，黑洞实际上成为了极端黑洞，此时$\displaystyle a\to 0$.

# Critical phenomenon
画出$P-v$图像，代入判别式：
$$
\frac{ \partial P }{ \partial v }=\frac{ \partial^{2} P }{ \partial v^{2} } =0
$$
可以得到临界点条件。
此外，由热容发散也可算出相同的结果。

	定义了Gibbs自由能
	$$G=M-TS$$

热容
$$
C_{Q,P}=T \frac{\partial S}{\partial T}
=\frac{2 S \left(8 P S^2-\pi  Q+S\right)}{S (8 P S-1)+3 \pi  Q}
$$
其分母是熵$\displaystyle S$的二次函数，该方程存在正实数根的条件（判别式）是
$$
P\leq \frac{1}{96\pi Q^{2}}
$$
于是，等号对应VdW-like的相变临界点。
也就是说，当$\displaystyle P$足够大时，$\displaystyle C_{c}$在全空间取值，不会发散。这使得热容存在发散点的条件就对应类范德华流体的$\displaystyle P-V$临界点。在该条件下，RN-AdS黑洞发生二级相变。$\displaystyle P$在该点以上，不发生相变，黑洞只有一个相（热容不发散）。$\displaystyle P$在该点以下，发生一级相变，热容有发散点。
由此可以计算出诸热力学量的临界点：
$$
\begin{align}
P_{c}&=\frac{1}{96\pi Q^{2}} \\
v_{c}&=2\sqrt{ 6 }Q=2r_{c} \to r_{c}=\sqrt{ 6 }Q\\ 
V_{c}&=\frac{4}{3}\pi r_{c}^{3}=8\sqrt{ 6 }\pi Q^{3} \\
T_{c}&=\frac{\sqrt{ 6 }}{18\pi Q} \\
S_{c}&=\pi r_{c}^{2}=6\pi Q^{2}
\end{align}
$$
【临界比(critical ratio)】
$$
\rho_{c}=\frac{P_{c}v_{c}}{T_{c}}=\frac{3}{8}
$$
其与VdW流体相同。

关于其他响应系数：
特别地，
$$
C_{P}=V/\frac{ \partial V }{ \partial P }.
$$
由于把$\displaystyle P$取为变量后，共轭量$\displaystyle V$并不是$\displaystyle P$的函数，所以分母始终为$\displaystyle 0$.


$$
t(s,p)=\frac{T}{T_{c}}=\frac{3ps^{2}+6s-1}{8s\sqrt{ s }}
$$
$$
h(s,p,q)=\frac{H}{H_{c}}=\frac{ps^{2}+6s+1}{8\sqrt{ s }}
$$

## 临界点共存曲线
临界点处，根据语言应该能看到自由能的燕尾图。
$$
F=M-TS=
$$



# 热力学几何
Ruppeiner几何线元的表达式$\displaystyle X^{i} \in (S,Q,P)$
$$
\Delta l^{2} = \frac{ \partial^{2} S }{ \partial X^{i} \partial X^{j} } 
\Delta X^{i}\Delta X^{j}
=\frac{1}{T} \frac{ \partial^{2} H }{ \partial X^{i} \partial X^{j} } 
\Delta X^{i}\Delta X^{j}
$$
## Ruppeiner度规
若采用原始的Ruppeiner度规，会出现标量曲率$\displaystyle R$与热容$\displaystyle C$的发散点不对应的问题。如果我们还想要使其对应，就要更换其他度规。
NTG度规是一个选择。他将Ruppeiner度规改为对角分块矩阵的形式，使得有关熵$\displaystyle S$的交叉项在度规中全置为$\displaystyle 0$.

## 度规退化
此外，从定义式可以看出，由于$\displaystyle V=\frac{4}{3}\pi r_+^3$,
$$
\frac{ \partial^{2} M }{ \partial P^{2} }= \frac{ \partial V }{ \partial P }=0, \quad
\frac{ \partial^{2} M }{ \partial P \partial Q }=\frac{ \partial V }{ \partial Q }=0
$$
所以这两项退化掉了。
所以如果采用NTG度规，有关$\displaystyle P$的一行将会全部为$\displaystyle 0$($\displaystyle V$只与$\displaystyle S$有关，所以只有$\displaystyle \frac{ \partial V }{ \partial S }$项不为零，但该项又被NTG置为零).
所以如果在$(S,Q,P)$空间计算NTG就会有度规退化的问题，我们只好退而求其次，算$\displaystyle (S,Q)$的Ruppeiner度规。
$$
R=\frac{8 P S \left(\pi  Q^2 S (32 P S-3)+8 P S^3 (8 P S-3)+3 \pi ^2 Q^4\right)}{\left(S (8 P S-1)+\pi  Q^2\right)^2 \left(\pi  Q^2-S (8 P S+1)\right)}
$$
	另附：这是把电荷变量$\displaystyle Q$替换为$\displaystyle Q^2$后，在$\displaystyle (S,Q^2)$空间计算的Ruppeiner标量曲率
	$$
R=\frac{16 P S+1}{\pi Q^2-S (8 P S+1)}
$$
可以证明，原版的Ruppeiner度规在$(S,Q)$中等价于这个度规
$$
ds^2=\frac{1}{T}\left(  \frac{ \partial^{2} G }{ \partial S^{2} }   \right)dS^2-\frac{1}{T}\frac{ \partial^{2} G }{ \partial \Phi^{2} } d\Phi^2
$$
其中$\displaystyle G=M-\Phi Q$. 这个度规是对角的。用这个度规计算的曲率标量$\displaystyle R$与上面的相同，又证明这俩度规确实是等价的。
但是这个$\displaystyle R$不与$\displaystyle C_{Q,P}$有相同的发散点。按照NTG说的，这个$\displaystyle R$实际上与$\displaystyle C_{\Phi,P}$有相同发散点。观察其表达式
$$
C_{\Phi,P}=T \frac{ \partial S }{ \partial T }|_{\Phi,P}
= \frac{2 S \left(8 P S + 1-\Phi^2\right)}{8 P S - 1 +\Phi^2}
=\frac{2 \left(8 P S^2-\pi  Q^2+S\right)}{S (8 P S-1)+\pi Q^2}
$$
发现确实如此。所以$\displaystyle C_{Q,P}$对应的估计是换一个热力学势的度规。




然后是$\displaystyle (S,Q,P)$空间的Ruppeiner曲率.
$$
R =\frac{17\pi Q^2 - 7S + 24PS^2}{4\pi Q^2S - 4S^2 - 32PS^3}
=\frac{80 P S+5}{2 \pi  Q^2-2 S (8 P S+1)}+\frac{17}{4 S}
=\frac{17}{4S}-\frac{5(16PS+1)}{6\pi TV}
$$
很奇怪，在热力学空间多了一维之后，曲率$\displaystyle R$的发散点反而消失了。这是为什么？




计算定容热容
$$
C_{V} = T \frac{ \partial S }{ \partial T } \bigg |_{V} \equiv 0
$$
这是因为$\displaystyle V,S$ 不独立。当$\displaystyle V$固定即等价于$\displaystyle S$固定，这时求导就是0了。
当选取$\displaystyle T,V$作为热力学变量时，线元表达式
$$
dl^{2} = -\frac{1}{T} \frac{ \partial^{2} f }{ \partial T^{2} } dT^{2}
+\frac{1}{T}\frac{ \partial^{2} f }{ \partial V^{2} } dV^{2}
$$
where,
$$
df = -sdT - PdV
$$
所以
$$
dl^{2} = \frac{1}{T} \frac{ \partial S }{ \partial T } dT^{2} -\frac{1}{T}\frac{ \partial P }{ \partial V } dV^{2}
=\frac{C_{V}}{T^{2}} dT^{2} -\frac{1}{T}\frac{ \partial P }{ \partial V } dV^{2}
$$



所以有文章发明了一个新变量，
$$
R_{N} = RC_{V}
$$
通过将$\displaystyle C_{V}$视为很小的小量（可视为$\displaystyle k_{B}\to 0$的极限以达到）拉平R的发散，从而观察新的热力学。