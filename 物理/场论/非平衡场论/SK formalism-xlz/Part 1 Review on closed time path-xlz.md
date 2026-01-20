# Notes on Schwinger-Keldysh Formalism in Condensed Matter Systems 

2026.1.9 testing

## Part 1: Review of the Closed Time Contour

Mainly based on Hong Liu's lecture (TASI 2017), 1805.09331

### 1.1 Time Evolution

In the Schrödinger picture, the equation of motion is:
$$
i \frac{d}{dt}|\psi(t)\rangle=H(t)|\psi(t)\rangle. \label{eq}
$$
The definition of the time evolution operator is given by:
$$
|\psi(t)\rangle=U(t,t_0)|\psi(t_0)\rangle. \label{tevo}
$$
Substituting $\eqref{tevo}$ into $\eqref{eq}$, we obtain:
$$
i\frac{\partial}{\partial t}U(t,t_0)=H(t)U(t,t_0). \label{teq}
$$
If the Hamiltonian is time-independent, $H(t)=H_0$, the solution to $\eqref{teq}$ is simply:
$$
U(t,t_0)=e^{-iH_0(t-t_0)}.
$$
More generally, using the Baker-Campbell-Hausdorff (BCH) formula, the solution is:
$$
U(t,t_0)=\mathcal{T}\left(e^{-i\int^t_{t_0}H(\tau)d\tau}\right), \quad t>t_0,
$$
where $\mathcal{T}$ denotes time-ordering (operators at later times are placed to the left). For the proof, see **Appendix A**.

For **In-Out** processes (scattering problems), such as the S-matrix:
$$
\langle \text{out},t_f|\text{in},t_i\rangle=\langle0|U(t_f,t_i)|0\rangle.
$$
For **In-In** processes, such as the expectation value in a pure state:
$$
\langle O(t)\rangle\equiv\langle\psi(t)| O(t)|\psi(t)\rangle=\langle\psi(t_0)|U^{\dagger}(t,t_0) O(t)U(t,t_0)|\psi(t_0)\rangle.
$$
The Hermitian conjugate of $U(t,t_0)$ is:
$$
U^\dagger(t,t_0)=\bar{\mathcal{T}}\left(e^{i\int^t_{t_0}H(\tau)d\tau}\right)=\bar{\mathcal{T}}\left(e^{-i\int_t^{t_0}H(\tau)d\tau}\right)=U^{-1}(t,t_0)=U(t_0,t),
$$
where $\bar{\mathcal{T}}$ denotes anti-time ordering. 

We define the contour $\gamma$ by setting $t_0=t_i=-\infty$ and $t<t_f=+\infty$. We also define the forward branch $\gamma_+ :t_i\to t_f$ and the backward branch $\gamma_- :t_f\to t_i$. There are two evolution cases required to evaluate $\langle O(t) \rangle$:

1) $\gamma : t_i\to t\equiv t_+\to t_f\to t_i$

$$
\langle O(t)\rangle=\langle\psi(t_i)|U^{\dagger}(t_f,t_i)U(t_f,t_+) O(t_+)U(t_+,t_i)|\psi(t_i)\rangle.
$$

2) $\gamma : t_i\to t_f\to t\equiv t_-\to t_i$

$$
\langle O(t)\rangle=\langle\psi(t_i)|U^{\dagger}(t_-,t_i) O(t_-)U^{\dagger}(t_f,t_-)U(t_f,t_i)|\psi(t_i)\rangle.
$$

These can be combined using the contour-ordering operator $\mathcal{P}$:
$$
\langle O(t)\rangle=\langle\psi(t_i)|\mathcal{P}\left(e^{-i\int_\gamma H(\tau)d\tau}O(t_\pm)\right)|\psi(t_i)\rangle. \label{vev}
$$
We must double the operators to distinguish their location on the path. To illustrate this argument, we take an example, i.e. there are four different two-point Green's functions for $O$:

<img src="/Users/xialingzheng/Library/Application Support/typora-user-images/image-20251209104459608.png" alt="image-20251209104459608" style="zoom:80%;" />
$$
G_{ab} = \langle \mathcal{P}(O_a(t_1) O_b(t_2)) \rangle = 
\begin{cases} 
\langle \mathcal{T} O_+(t_1) O_+(t_2) \rangle, & a=+, b=+ \\[1.5ex]
\langle \bar{\mathcal{T}} O_-(t_1) O_-(t_2) \rangle, & a=-, b=- \\[1.5ex]
\langle O_-(t_1) O_+(t_2) \rangle, & a=-, b=+ \\[1.5ex]
\langle O_-(t_2) O_+(t_1) \rangle, & a=+, b=-
\end{cases}
$$

In the interaction picture, we split the Hamiltonian:
$$
H(t) = H_0 + \delta H(t), \quad \delta H(t) \sim -O(t) J(t).
$$
We define the interaction picture state as:
$$
|\psi(t)\rangle_I \equiv U_{0}^\dagger |\psi(t)\rangle_S, \quad U_{0} = e^{-i H_0 \Delta t},
$$
and the operator as:
$$
\hat{O}_I(t) = U_{0}^\dagger O_S(t) U_{0}=U_I^\dagger(t,t_0) O_I(t_0) U_I(t,t_0).
$$
The time evolution for the state is:
$$
\begin{aligned}
i \frac{d}{dt} |\psi(t)\rangle_I &= i \frac{d}{dt} \left( U_{0}^\dagger |\psi(t)\rangle_S \right),\\[2ex]
&= i \frac{d U_{0}^\dagger}{dt} |\psi(t)\rangle_S + i U_{0}^\dagger \frac{d|\psi(t)\rangle_S}{dt},\\[2ex]
&= -H_0 U_{0}^\dagger |\psi(t)\rangle_S + U_{0}^\dagger \left( H_0 + \delta H(t) \right) |\psi(t)\rangle_S,\\[2ex]
&= \delta H(t) |\psi(t)\rangle_I.
\end{aligned}
$$
Thus (omitting the subscript $I$ for the state):
$$
|\psi(t)\rangle = U_I(t, t_0) |\psi(t_0)\rangle, \quad U_I(t, t_0) = \mathcal{T}\left(e^{-i \int^t_{t_0} \delta H(\tau) d\tau}\right).
$$
The evolution for the operator is:
$$
\begin{aligned}
\frac{d}{dt} O_I(t) &= i H_0 e^{i H_0 t} O_S(t) e^{-i H_0 t} - e^{i H_0 t} O_S(t) H_0 e^{-i H_0 t}+ e^{i H_0 t} \frac{\partial}{\partial t} O_S(t) e^{-i H_0 t},\\[2ex]
&= -i \left[ O_I(t), H_0 \right] + \left( \frac{\partial O_S(t)}{\partial t} \right)_I.
\end{aligned}
$$
Equation $\eqref{vev}$ can then be expanded as:
$$
\begin{aligned}
\langle O(t)\rangle&=\langle\psi(t_i)|\mathcal{P}\left(e^{-i\int_\gamma \delta H(\tau)d\tau}O(t_\pm)\right)|\psi(t_i)\rangle\\[2ex]
&=\langle\psi(t_i)|\mathcal{P}\left(e^{-i(\int_{\gamma_+} \delta H(\tau)d\tau+\int_{\gamma_-} \delta H(\tau)d\tau)}O(t_\pm)\right)|\psi(t_i)\rangle\\[2ex]
&=\langle\psi(t_i)|\mathcal{P}\left(e^{-i\int_{t_i}^{t_f} \delta H(\tau_+)d\tau_+-i\int_{t_f}^{t_i} \delta H(\tau_-)d\tau_-}O(t_\pm)\right)|\psi(t_i)\rangle\\[2ex]
&=\langle\psi(t_i)|\mathcal{P}\left(e^{i\int_{t_i}^{t_f} O_+(\tau_+)J_+(\tau_+)d\tau_++i\int_{t_f}^{t_i} O_+(\tau_-)J_+(\tau_-)d\tau_-}O(t_\pm)\right)|\psi(t_i)\rangle\\[2ex]
&=\langle\psi(t_i)|\mathcal{P}\left(e^{i\int_{t_i}^{t_f} (O_+(\tau)J_+(\tau)-O_-(\tau)J_-(\tau))d\tau}O(t_\pm)\right)|\psi(t_i)\rangle.
\end{aligned}
$$
For a mixed state described by a density matrix:
$$
\langle O(t)\rangle_\rho=\sum_j \omega_j\langle \psi_j(t)|O(t)|\psi_j(t)\rangle, \quad \text{with} \sum_j \omega_j=1. \label{mvev}
$$
We define the density operator:
$$
\rho(t)=\sum_j\omega_j|\psi_j(t)\rangle\langle\psi_j(t)|,\quad \text{with} \Tr(\rho)=1.
$$
Its time evolution is given by:
$$
\rho(t)=U_I(t,t_0;O_+)\rho(t_0)U_I^\dagger(t,t_0;O_-).
$$
Then $\eqref{mvev}$ becomes:
$$
\begin{aligned}
\langle O(t)\rangle_\rho&=\Tr(\rho(t)O(t)),\\[2ex]
&=\Tr(U_I(t,t_0;O_+)\rho(t_0)U_I^\dagger(t,t_0;O_-)O(t)),\\[2ex]
&=\Tr(\rho(t_0)U_I^\dagger(t,t_0;O_-)O(t)U_I(t,t_0;O_+)),\\[2ex]
&=\Tr\left(\rho(t_0)\bar{\mathcal{T}}\left(e^{-i\int_{t_0}^{t}O_-(\tau)J_-(\tau))d\tau}\right)O(t)\mathcal{T}\left(e^{i\int_{t_0}^{t}O_+(\tau)J_+(\tau))d\tau}\right)\right),\\[2ex]
&=\cdots\\
&=\Tr\left(\rho_0\mathcal{P}\left(e^{i\int_{t_i}^{t_f} (O_+(\tau)J_+(\tau)-O_-(\tau)J_-(\tau))d\tau}O(t_\pm)\right)\right), \quad \rho(t_i)=\rho(t_0)\equiv \rho_0.
\end{aligned}
$$
We define the **connected generating functional** $W$:
$$
\boxed{e^{W[J_+,J_-]}\equiv \Tr\left(\rho_0\mathcal{P}\left(e^{i\int_{t_i}^{t_f} (O_+(\tau)J_+(\tau)-O_-(\tau)J_-(\tau))d\tau}\right)\right).} \label{defW}
$$
In terms of path integrals (See **Appendix B** for a review on path integrals):
$$
e^{W[J_+,J_-]}=\int D\xi_a\, D\xi_b\, D\xi_c\,\langle \xi_b|\rho_0|\xi_a\rangle\int_{\varphi_+(t_i)=\xi_a}^{\varphi_+(t_f)=\xi_c}D\varphi_+\int_{\varphi_-(t_i)=\xi_b}^{\varphi_-(t_f)=\xi_c}D\varphi_-\, e^{iS[\varphi_+,J_+]-iS[\varphi_-,J_-]}. \label{pathw}
$$

### 1.2 Effective Field Theory

After integrating out the UV fields in $\eqref{pathw}$, we write the effective action as ($J_+(t)\to \int \mathrm{d}\vec x\, J_1(t,\vec x)$ and $J_-(t)\to \int \mathrm{d}\vec x\, J_2(t,\vec x)$):
$$
e^{W[J_1,J_2]}=\int_\epsilon D\chi_1\,D\chi_2\,e^{iI[\chi_1,J_1;\chi_2,J_2]}.
$$
The effective action $I$ satisfies three key properties:

1. $I^*[\chi_1,J_1;\chi_2,J_2]=-I[\chi_2,J_2;\chi_1,J_1].$
2. $I[\chi_1=\chi_2]=0.$
3. $\Im [I]\geq0.$

>**Proof:**
>From the definition $\eqref{defW}$:
>$$
>e^{W[J_1,J_2]}=\Tr(\rho_0U^\dagger(t_f,t_i;O_2)U(t_f,t_i;O_1))=\Tr(\rho_0U^\dagger(+\infty,-\infty;O_2)U(+\infty,-\infty;O_1)).
>$$
>Taking the complex conjugate:
>$$
>\begin{aligned}
>e^{W^*[J_1,J_2]}&=\Tr(U^\dagger(+\infty,-\infty;O_1)U(+\infty,-\infty;O_2)\rho(t_0)),\\[2ex]
>&=\Tr(\rho_0U^\dagger(+\infty,-\infty;O_1)U(+\infty,-\infty;O_2)),\\[2ex]
>&=e^{W[J_2,J_1]}.
>\end{aligned}
>$$
>This implies $I^*[\chi_1,J_1;\chi_2,J_2]=-I[\chi_2,J_2;\chi_1,J_1]$. Furthermore, $e^{W[J_1=J_2]}=\Tr(\rho_0)=1$, which implies $I[\chi_1=\chi_2]=0$.
>
>Using the Cauchy-Schwarz inequality $|\langle a|b\rangle|^2\leq \langle a|a\rangle\langle b|b\rangle$:
>$$
>\begin{aligned}
>|e^{W[J_1,J_2]}|&=\left|\sum_j\omega_j\langle\psi_j|U^\dagger(+\infty,-\infty;O_2)U(+\infty,-\infty;O_1)|\psi_j\rangle\right|,\\[2ex]
>&\leq \sum_j\omega_j\sqrt{\langle\psi_j|U^\dagger_2 U_2|\psi_j\rangle \langle\psi_j|U^\dagger_1 U_1|\psi_j\rangle},\\[2ex]
>&=1.
>\end{aligned}
>$$
>Consequently, $\Re [W]\leq 0$, which implies $\Im[I]\geq 0$.

For thermal state, $\rho_0=e^{-\beta H_0}$, there is another symmetry we should impose, i.e. dynamical Kubo-Martin-Schwinger (KMS) symmetry.

First, KMS condition (Correlation level):
$$
\langle A(t_1)B(t_2)\rangle_{\rho_0}=\langle B(t_2)A(t_1+i\beta)\rangle_{\rho_0}.
$$

>**Proof**:
>$$
>\begin{aligned}
>\langle A(t_1)B(t_2)\rangle_{\rho_0}&=\Tr (\rho_0 A(t_1)B(t_2)),\\[2ex]
>&=\Tr (e^{-\beta H_0} A(t_1)B(t_2)),\\[2ex]
>&=\Tr (e^{-\beta H_0} A(t_1)e^{\beta H_0}e^{-\beta H_0}B(t_2)),\\[2ex]
>&=\Tr (A(t_1+i\beta)e^{-\beta H_0}B(t_2)),\\[2ex]
>&=\Tr (e^{-\beta H_0}B(t_2)A(t_1+i\beta)),\\[2ex]
>&=\langle B(t_2)A(t_1+i\beta)\rangle_{\rho_0}.
>\end{aligned}
>$$

Then, for the generating functional (omitted spatial indices):
$$
\begin{aligned}
e^{W[J_1(t),J_2(t)]}&=\Tr(\rho_0U^\dagger(+\infty,-\infty;O_2)U(+\infty,-\infty;O_1)),\\
&=\Tr(\rho_0\underbrace{\bar{\mathcal{T}}\left(e^{-i\int_{-\infty}^{+\infty}dt\,O_2(t)J_2(t))}\right)}_{A}\underbrace{\mathcal{T}\left(e^{i\int_{-\infty}^{+\infty}dt\,O_1(t)J_1(t))}\right)}_{B}),\\[2ex]
&=\Tr(\rho_0\mathcal{T}\left(e^{i\int_{-\infty}^{+\infty}dt\,O_1(t)J_1(t))}\right)\bar{\mathcal{T}}\left(e^{-i\int_{-\infty}^{+\infty}dt\,O_2(t+i\beta)J_2(t))}\right)),\\[2ex]
&=\Tr(\rho_0\mathcal{T}\left(e^{i\int_{-\infty}^{+\infty}dt\,O_1(t)J_1(t))}\right)\bar{\mathcal{T}}\left(e^{-i\int_{-\infty}^{+\infty}dt\,O_2(t)J_2(t-i\beta))}\right)),\\[2ex]
&\equiv e^{W_T[J_1(t),J_2(t-i\beta)]}. 
\end{aligned} \label{KMSW}
$$
We have defined a "reverse" generating functional, which means evolution is reverse along the contour. Suppose the system has several discrete symmetries in microscopic level $\Theta$ including time reversal $\mathscr{T}$, sometimes with combinations charge conjugate $\mathscr{C}$ and parity $\mathscr{P}$:
$$
W[J_1(t),J_2(t)]=W_T[\Theta J_1(t),\Theta J_2(t)]. \label{KMST}
$$
Combining $\eqref{KMSW}$ and $\eqref{KMST}$, one can get:
$$
W_T[\Theta J_1(t),\Theta J_2(t)]=W_T[J_1(t),J_2(t-i\beta)],
$$
which means
$$
W[J_1(t),J_2(t)]=W[\Theta J_1(t),\Theta J_2(t-i\beta)]. \label{KMSC}
$$
This is a $Z_2$ operation ($\Theta^2=\mathbb{I}$). For the action, if we require it has a dynamical KMS symmetry
$$
I[\chi_1,J_1;\chi_2,J_2]=I[\tilde\chi_1,\tilde J_1;\tilde\chi_2,\tilde J_2], \label{KMSS}
$$
then $\eqref{KMSC}$ should be satisfied, where (property 4)
$$
\tilde\chi_1(t,\vec x)=\Theta \chi_1(t,\vec x),\quad \tilde\chi_2(t,\vec x)=\Theta \chi_2(t-i\beta,\vec x),\\
\tilde J_1(t,\vec x)=\Theta J_1(t,\vec x),\quad \tilde J_2(t,\vec x)=\Theta J_2(t-i\beta,\vec x).
$$
We often use this symmetry in the classical limit ($\hbar\to 0$ or $\beta \omega\ll1$):
$$
\tilde\chi_1(t,\vec x)=\Theta \chi_1(t,\vec x),\quad \tilde\chi_2(t,\vec x)=\Theta \chi_2(t,\vec x)-i\beta\Theta\partial_t\chi_2(t,\vec x),\\
\tilde J_1(t,\vec x)=\Theta J_1(t,\vec x),\quad \tilde J_2(t,\vec x)=\Theta J_2(t,\vec x)-i\beta\Theta\partial_t J_2(t,\vec x).
$$
We usually redefine the fields: classical $\chi_r, J_r$ and noise $\chi_a, J_a$:
$$
\chi_r=\frac{\chi_1+\chi_2}{2},\quad \chi_a=\chi_1-\chi_2,\\
J_r=\frac{J_1+J_2}{2},\quad J_a=J_1-J_2.
$$
Then the four properties are

1. $I^*[\chi_r,J_r;\chi_a,J_a]=-I[\chi_r,J_r;-\chi_a,-J_a].$
2. $I[\chi_a=0]=0.$
3. $\Im [I]\geq0.$
4. $I[\chi_r,J_r;\chi_a,J_a]=I[\tilde\chi_r,\tilde J_r;\tilde\chi_a,\tilde J_a]$ with 

$$
\tilde\chi_r(t,\vec x)=\Theta \chi_r(t,\vec x),\quad \tilde\chi_a(t,\vec x)=\Theta \chi_a(t,\vec x)-i\beta\Theta\partial_t\chi_r(t,\vec x),\\
\tilde J_r(t,\vec x)=\Theta J_r(t,\vec x),\quad \tilde J_a(t,\vec x)=\Theta J_a(t,\vec x)-i\beta\Theta\partial_t J_r(t,\vec x),
$$

in the classical limit.

>Proof of 4 (take $\chi$ for example):
>
>We restore $\hbar$ :
>$$
>\chi_r=\frac{\chi_1+\chi_2}{2},\quad \hbar\chi_a=\chi_1-\chi_2,\\[2ex]
>\tilde\chi_1=\Theta \chi_1,\quad \tilde\chi_2=\Theta \chi_2-i\beta\hbar\Theta\partial_t\chi_2.
>$$
>Then,
>$$
>\begin{aligned}
>\tilde \chi_r&=\frac{\tilde\chi_1+\tilde\chi_2}{2}=\Theta \chi_r-\frac{i\beta\hbar\Theta\partial_t\chi_2}{2},\\
>&=\Theta \chi_r+\mathcal{O}(\hbar),\\[2ex]
>\hbar\tilde\chi_a&=\tilde\chi_1-\tilde\chi_2=\Theta \chi_1-\Theta \chi_2+i\beta\hbar\Theta\partial_t\chi_2,\\
>&=\Theta(\chi_1-\chi_2)+i\beta\hbar\Theta\partial_t(\chi_r-\frac{\hbar}{2}\chi_a),\\
>&=\Theta(\hbar\chi_a)+i\beta\hbar\Theta\partial_t\chi_r-i\beta\hbar\Theta\partial_t(\frac{\hbar}{2}\chi_a),\\
>&=\hbar\Theta\chi_a+i\beta\hbar\Theta\partial_t\chi_r+\mathcal{O}(\hbar^2).
>\end{aligned}
>$$
>Taking $\hbar\to0$, finally we have
>$$
>\tilde\chi_r=\Theta \chi_r,\quad \tilde\chi_a=\Theta \chi_a+i\beta\Theta\partial_t\chi_r.\\
>$$



### Appendix A: Derivation of Time Evolution

From $\eqref{teq}$, one might naively guess that the solution is:
$$
U(t,t_0)\stackrel{?}{=}e^{-i\int_{t_0}^tH(\tau)d\tau},\label{guess}
$$
However, since $U(t,t_0)$ must satisfy the group property $U(t,t_0)=U(t,t_1)U(t_1,t_0)$, Eq. $\eqref{guess}$ is generally incorrect when $[H(t), H(t')] \neq 0$.

We use the BCH formula expansion:
$$
e^X e^Y=e^{X+Y+\frac{1}{2}[X,Y]+\frac{1}{12}[X,[X,Y]]-\frac{1}{12}[Y,[X,Y]]+\cdots}.
$$
According to $\eqref{teq}$, $idU(t)=H(t)U(t)dt$. Setting $t_0\equiv0$ and $U(t)\equiv U(t,0)$:
$$
\int_0^t dU(t)=-i\int_0^tdt_1 H(t_1)U(t_1).
$$
Iterating this integral equation:
$$
\begin{aligned}
U(t)&=1-i\int_0^tdt_1 H(t_1)U(t_1),\\[2ex]
&=1-i\int_0^tdt_1 H(t_1)\left(1-i\int_0^{t_1}dt_2 H(t_2)U(t_2)\right),\\[2ex]
&=1-i\int_0^tdt_1 H(t_1)\left(1-i\int_0^{t_1}dt_2 H(t_2)\left(1-i\int_0^{t_2}dt_3 H(t_3)U(t_3)\right)\right),\\[2ex]
&=1-iI_1(t)+(-i)^2I_2(t)+\cdots+(-i)^nI_n(t)+\cdots.
\end{aligned}
$$
We define the $n$-th order term as $I_n(t)=\int_0^tdt_1\cdots\int_0^{t_{n-1}}dt_nH(t_1)\cdots H(t_n)$.

<img src="/Users/xialingzheng/Library/Application Support/typora-user-images/image-20251211112917652.png" alt="image-20251211112917652" style="zoom:60%;" />

Consider the second-order term:
$$
I_2=\int_0^tdt_1\int_0^{t_1}dt_2H(t_1)H(t_2). \label{original}
$$
Geometrically (see diagram), the integration over the time-ordered region $t_1 > t_2$ represents half of the total square area $[0,t] \times [0,t]$. We can rewrite the same integral by relabeling dummy variables ($t_1 \leftrightarrow t_2$) and changing limits to the upper triangular region:
$$
I_2=\int_0^tdt_2\int_0^{t_2}dt_1H(t_2)H(t_1). \label{swapped}
$$
We define the time-ordering operator $\mathcal{T}$ such that operators with later times are placed to the left:
$$
    \mathcal{T}(H(t_a)H(t_b)) = 
    \begin{cases} 
        H(t_a)H(t_b), & \text{if } t_a > t_b, \\
        H(t_b)H(t_a), & \text{if } t_b > t_a. 
    \end{cases}
$$
Summing $\eqref{original}$ and $\eqref{swapped}$:
$$
\begin{align}
    2 I_2 &= \int_0^tdt_1\int_0^{t_1}dt_2H(t_1)H(t_2)+\int_0^tdt_2\int_0^{t_2}dt_1H(t_2)H(t_1), \nonumber \\
          &= \int_0^t dt_1 \int_0^t dt_2 \, \mathcal{T}(H(t_1)H(t_2)).
\end{align}
$$
Thus:
$$
I_2 = \frac{1}{2!}\int_0^t dt_1 \int_0^t dt_2 \, \mathcal{T}(H(t_1)H(t_2)).
$$
This logic generalizes to $n$ dimensions. The integral over the simplex $t > t_1 > t_2 > \dots > t_n > 0$ is equal to $1/n!$ times the integral over the hypercube:
$$
I_n=\frac{1}{n!}\int_0^tdt_1\cdots\int_0^tdt_n\,\mathcal{T}(H(t_1)\cdots H(t_n)).
$$
Finally:
$$
\begin{aligned}
U(t)&=1+\sum_{n=1}^{\infty}\frac{(-i)^n}{n!}\int_0^tdt_1\cdots\int_0^tdt_n\,\mathcal{T}(H(t_1)\cdots H(t_n)),\\[2ex]
&=\mathcal{T}\left(e^{-i\int_0^tH(\tau)d\tau}\right).
\end{aligned}
$$


### Appendix B: Path Integral for the Propagator

In quantum mechanics, we calculate the propagator $K(x_f, t_f; x_i, t_i)$ from $(x_i, t_i)$ to $(x_f, t_f)$:
$$
K(x_f, t_f; x_i, t_i) = \langle x_f | e^{-\frac{i}{\hbar}H(t_f - t_i)} | x_i \rangle
$$
Assume the Hamiltonian is $\hat{H} = \frac{\hat{p}^2}{2m} + V(\hat{x})$. We explicitly retain $\hbar$ and the operator 'hat' notation.

We perform time slicing with $\epsilon = (t_f-t_i)/N$ and $t_j = t_i + j\epsilon \quad (j=0, 1, \dots, N)$:
$$
e^{-\frac{i}{\hbar}\hat{H}(t_f-t_i)} = \underbrace{e^{-\frac{i}{\hbar}\hat{H}\epsilon} \cdots e^{-\frac{i}{\hbar}\hat{H}\epsilon}}_{N \text{ times}}.
$$
We insert the identity operator $\int dx |x\rangle\langle x| = \mathbb{I}$ at every time slice ($N-1$ times), labeling coordinates $x_1,\cdots,x_{N-1}$:
$$
\begin{aligned}
K &=\int dx_1\cdots dx_{N-1}\,\langle x_f|e^{-\frac{i}{\hbar}\hat{H}\epsilon}|x_{N-1}\rangle\langle x_{N-1}|e^{-\frac{i}{\hbar}\hat{H}\epsilon}|x_{N-2}\rangle\cdots\langle x_1|e^{-\frac{i}{\hbar}\hat{H}\epsilon}|x_i\rangle,\\
&= \int \left( \prod_{j=1}^{N-1} dx_j \right) \prod_{j=0}^{N-1} \langle x_{j+1} | e^{-\frac{i}{\hbar}\hat{H}\epsilon} | x_j \rangle.
\end{aligned}
$$
Using the Trotter decomposition $e^{\epsilon(A+B)} \approx e^{\epsilon A}e^{\epsilon B}$ (valid to order $\mathcal{O}(\epsilon^2)$), we separate the kinetic and potential terms:
$$
\begin{aligned}
\langle x_{j+1} | e^{-\frac{i}{\hbar}(\hat{T} + \hat{V})\epsilon} | x_j \rangle &\approx \langle x_{j+1} | e^{-\frac{i}{\hbar}\hat{V}\epsilon} e^{-\frac{i}{\hbar}\hat{T}\epsilon} | x_j \rangle, \\[1.5ex]
&= e^{-\frac{i}{\hbar}V(x_{j+1})\epsilon} \langle x_{j+1} | e^{-\frac{i}{\hbar}\frac{\hat{p}^2}{2m}\epsilon} | x_j \rangle.
\end{aligned}
$$
To calculate the kinetic term, we insert the momentum basis $\int dp |p\rangle\langle p| = \mathbb{I}$:
$$
\begin{aligned}
\langle x_{j+1} | e^{-\frac{i}{\hbar}\frac{\hat{p}^2}{2m}\epsilon} | x_j \rangle &= \int dp_j \langle x_{j+1} | e^{-\frac{i}{\hbar}\frac{\hat{p}^2}{2m}\epsilon} | p_j \rangle \langle p_j | x_j \rangle, \\
&= \int dp_j e^{-\frac{i}{\hbar}\frac{p_j^2}{2m}\epsilon} \langle x_{j+1} | p_j \rangle \langle p_j | x_j \rangle, \\
&= \int dp_j e^{-\frac{i}{\hbar}\frac{p_j^2}{2m}\epsilon} \left( \frac{1}{\sqrt{2\pi\hbar}} e^{\frac{i}{\hbar}p_j x_{j+1}} \right) \left( \frac{1}{\sqrt{2\pi\hbar}} e^{-\frac{i}{\hbar}p_j x_j} \right),\\
&= \frac{1}{2\pi\hbar} \int dp_j \exp\left\{ \frac{i}{\hbar} \left[ p_j(x_{j+1} - x_j) - \frac{\epsilon}{2m} p_j^2 \right] \right\}.
\end{aligned}
$$
Here we used the plane wave formula $\langle x | p \rangle = \frac{1}{\sqrt{2\pi\hbar}} e^{\frac{i}{\hbar}px}$. Using the Gaussian integral formula:
$$
\int_{-\infty}^{\infty} e^{-a x^2 + b x} dx = \sqrt{\frac{\pi}{a}} e^{\frac{b^2}{4a}},
$$
with $a = \frac{i\epsilon}{2m\hbar}$ and $b = \frac{i(x_{j+1}-x_j)}{\hbar}$, we get:
$$
\langle x_{j+1} | e^{-\frac{i}{\hbar}\hat{T}\epsilon} | x_j \rangle = \underbrace{\sqrt{\frac{m}{2\pi i \hbar \epsilon}}}_{A} \exp \left[ \frac{i}{\hbar} \frac{m}{2} \frac{(x_{j+1}-x_j)^2}{\epsilon} \right].
$$
Here $A$ is the measure factor. The propagator for a short time step is:
$$
\langle x_{j+1} | e^{-\frac{i}{\hbar}\hat{H}\epsilon} | x_j \rangle \approx A \cdot \exp \left[ \frac{i}{\hbar} \epsilon \left( \frac{m}{2} \left(\frac{x_{j+1}-x_j}{\epsilon}\right)^2 - V(x_{j+1}) \right) \right].
$$
We observe that:

*   $\frac{x_{j+1}-x_j}{\epsilon} \approx \dot{x}$ (Velocity).
*   $\frac{1}{2}m\dot{x}^2 - V(x) = L(x, \dot{x})$ (Lagrangian).

Thus:
$$
K = \lim_{N \to \infty} \int dx_1 \dots dx_{N-1} A^N \exp \left[ \frac{i}{\hbar} \sum_{j=0}^{N-1} \epsilon \left( \frac{m}{2} \left(\frac{x_{j+1}-x_j}{\epsilon}\right)^2 - V(x_j) \right) \right].
$$
Taking the continuum limit ($N \to \infty, \epsilon \to 0$):
$$
\sum_{j=0}^{N-1} \epsilon L(x_j, \dot{x}_j) \longrightarrow \int_{t_i}^{t_f} dt \, L(x(t), \dot{x}(t)) = S[x(t)].
$$
We replace the multiple integral with the path integral measure:
$$
\mathcal{D}x(t) \equiv \lim_{N \to \infty} A^N \prod_{j=1}^{N-1} dx_j.
$$
The final result is:
$$
K(x_f, t_f; x_i, t_i) = \int_{x(t_i)=x_i}^{x(t_f)=x_f} \mathcal{D}x(t) \, e^ { \frac{i}{\hbar} S[x(t)]},
$$
where
$$
S[x(t)] = \int_{t_i}^{t_f} \left[ \frac{1}{2}m\dot{x}^2 - V(x) \right] dt.
$$
Finally, we introduce the source $J(x)$ and generalize to quantum field theory:
$$
Z[J] = \int \mathcal{D}\phi \exp \left\{ i \int d^4x \left( \mathcal{L}[\phi] + J(x)\phi(x) \right) \right\}.
$$
