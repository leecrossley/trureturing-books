# 16.3 The central-defect path: how an endpoint controls the spectrum {#sec-central-defect-gap}

Equations (25)–(27) of Childs et al. use tree depth $d\ge1$ and $2d+2$ columns, indexed by $j=0,\ldots,2d+1$, with sizes $N_j=2^{\min(j,2d+1-j)}$. With normalised column vectors $|q_j\rangle=N_j^{-1/2}\sum_{v\text{ in column }j}|v\rangle$ and the graph Hamiltonian equal to $\gamma$ times adjacency, $\gamma=1/\sqrt2$, the paper's column reduction gives ordinary weights $\sqrt2\gamma=1$ and central weight $2\gamma=\sqrt2$. Thus the path parameter here is $n=d+1$, and column $j$ is zero-based path coordinate $j$.

From column $i$ to $i+1$, each vertex has two neighbours in the next column for $i\le d$ and one for $i>d$. In the reverse direction, each vertex of column $i+1$ has one neighbour in column $i$ for $i<d$ and two for $i\ge d$. All neighbours lie in adjacent columns. Given these counts and column sizes, the column isometry intertwines the graph and path evolutions. Their matrix entries agree between the two singleton end columns. A concrete graph must satisfy both counting hypotheses. [Column evolution](lean:D5/S3/Quantum/Dynamics/WeldedColumnEvolution.central_defect_column_evolution)

Separate the glued-trees claim into questions that can be checked individually. Spectral separation, transfer probability between endpoints, and efficient implementation with a specified oracle each require their own argument. Here we first address spectral separation, then derive a bound on the time-averaged endpoint probability. For $n\ge1$, let $J_n$ be the real symmetric matrix on $2n$ positions $0,\ldots,2n-1$. Its diagonal is zero. Adjacent positions have weight $1$ except for the central edge $(n-1,n)$, whose weight is $\sqrt2$. All other entries vanish. Here $n$ is half the number of path vertices. A comparison with a paper's tree-depth parameter requires a separate identification.

The smallest case makes the object explicit:

$$
J_1=\begin{pmatrix}0&\sqrt2\\\sqrt2&0\end{pmatrix},
\qquad \lambda_\pm=\pm\sqrt2.
$$

The two spectral lines are $2\sqrt2$ apart. For general $n$, we seek one lower bound controlling every pair, including whether repeated roots can occur, without assuming distinctness. The matrix family comes from Childs et al., [arXiv:quant-ph/0209131v2, the fourth subsection of Section III, equation (42) and Lemma 2](https://arxiv.org/abs/quant-ph/0209131v2). The explicit bound below holds for every $n\ge1$; no literature novelty or optimal constant is claimed.

**Control the endpoint of a half-path first.** Coordinates of a free-path eigenvector satisfy a second-order recurrence. Impose the exterior boundary $y(0)=0$ on the left and close the right end with $y(n+1)=b\,y(n)$. The resulting estimate does not restrict the energy parameter $t$ to the usual oscillatory interval.

::: {.theorem #thm-robin-endpoint-observability title="Endpoint control for a finite path recurrence" lean="D5/S3/Quantum/Matrix/CentralSqrtTwoDefectGap.recurrence_endpoint_observability"}

Let $n\in\mathbb N$, $n\ge1$, $t,b\in\mathbb R$, and $y:\mathbb N\to\mathbb R$ satisfy $y(0)=0$ and

$$
\begin{aligned}
y(j+2)&=t\,y(j+1)-y(j)
&&\bigl(j\in\mathbb N,\ j+2\le n+1\bigr),\\
y(n+1)&=b\,y(n).
\end{aligned}
$$

Then

$$
\sum_{j=1}^{n}y(j)^2
\le (1+|b|)^2n^3y(n)^2.
$$
:::

::: proof
For $|t|\le2$, run the recurrence backwards from the right endpoint. The second-kind Chebyshev bound $|U_k(x)|\le k+1$ for $|x|\le1$ gives $|y(j)|\le(1+|b|)n|y(n)|$ at every interior coordinate. Square and sum the $n$ terms. For $|t|>2$, the recurrence starting at the zero left boundary makes the coordinate magnitudes nondecreasing; the absolute-value argument covers both exterior regimes. The first case includes both boundaries $|t|=2$. The full proof is checked by the Lean kernel.
:::

Fold $J_n$ at its central edge. Reflection-even and reflection-odd vectors give two $n$-dimensional paths $H_+$ and $H_-$. Their ordinary edges still have weight $1$; their final diagonal entries are $+\sqrt2$ and $-\sqrt2$, respectively. Writing $e$ for the final coordinate vector gives

$$
H_+-H_-=2\sqrt2\,ee^{\mathsf T}.
$$

Apply [@thm-robin-endpoint-observability] with $b=\pm\sqrt2$. Every unit eigenvector has final-coordinate square at least $1/K$, where $K=(1+\sqrt2)^2n^3$. This endpoint weight is derived from the actual recurrence rather than supplied as an overlap assumption.

::: {.theorem #thm-central-defect-spectral-gap title="Full spectral separation for the central square-root-two defect path" lean="D5/S3/Quantum/Matrix/CentralSqrtTwoDefectGap.central_spectral_gap"}

Let $m\in\mathbb N$, $n=m+1$, and let $J_n$ be the real symmetric $2n\times2n$ matrix defined above. Suppose the real list $\lambda_0,\ldots,\lambda_{2n-1}$ is exactly the multiset of all roots of its characteristic polynomial, retaining every algebraic multiplicity. For any distinct indices $i\ne j$,

$$
|\lambda_i-\lambda_j|
\ge \frac{2\sqrt2}{(1+\sqrt2)^2n^3}>0.
$$
:::

::: proof
For $H_-u=\lambda u$ and $H_+v=\mu v$, real symmetry and the rank-one difference imply

$$
(\mu-\lambda)\langle u,v\rangle
=2\sqrt2\,u_{n-1}v_{n-1}.
$$

Unit normalization gives $|\langle u,v\rangle|\le1$, while endpoint control gives $|u_{n-1}v_{n-1}|\ge1/K$. Opposite-sector spectral lines are therefore at least $2\sqrt2/K$ apart. Pairs in the same sector still require an argument: the source proof bounds the difference between the two sectors' eigenvalue counts above any threshold by $1$. Two excessively close lines in one sector, together with opposite-sector separation, would force a count difference of at least $2$. Finally, the sum and difference basis after folding gives an exact characteristic-polynomial factorization, transporting both complete sector root multisets, with multiplicity, back to $J_n$. The full proof is checked by the Lean kernel.
:::

The real symmetric spectral theorem supplies the complete real root list, so the hypothesis is inhabited; the strictly positive conclusion then establishes that every root is simple. The estimate holds for every $n\ge1$, retains exterior energies, and uses no fixed-index asymptotic expansion as a uniform bound. In the usual asymptotic formulation it supplies the common constant $c=2\sqrt2/(1+\sqrt2)^2$ and threshold $N=1$.

**Averaging the phases.** The off-diagonal terms come in complex conjugate pairs. Their real parts give the endpoint bound below once $\tau\ge 2n/(\varepsilon\delta_n)$. Childs et al. prove it for $\tau\ge 4n/(\varepsilon\delta_n)$ in Lemma 1, equations (42) to (49). [Childs et al., Section III.D](https://arxiv.org/abs/quant-ph/0209131v2) [Published paper](https://doi.org/10.1145/780542.780552)

::: {.theorem #thm-central-defect-endpoint-average title="Finite-time endpoint average for the central-defect path" lean="D5/S3/Quantum/Matrix/Jacobi/ReflectedSpectralWindow.central_defect_endpoint_average"}
Let $n\in\mathbb N$, $n\ge1$, and let $J_n$ be the real symmetric matrix indexed by $0,\ldots,2n-1$, with zero diagonal, nearest-neighbour weights $1$ except for the central edge $(n-1,n)$ and its symmetric entry, whose weight is $\sqrt2$, and all other entries zero. Let the real list $\lambda_0,\ldots,\lambda_{2n-1}$ be exactly its full eigenvalue multiset, retaining algebraic multiplicities, and define the actual minimum gap

$$
\delta_n=\min_{\substack{0\le i,j<2n\\i\ne j}}
|\lambda_i-\lambda_j|.
$$

Then $\delta_n>0$. Embed $J_n$ entrywise into the complex numbers to obtain $J_n^{\mathbb C}$, and let $U_n(t)=\exp(-itJ_n^{\mathbb C})$ be the actual matrix exponential. For every real $\varepsilon>0$ and every real

$$
\tau\ge\frac{2n}{\varepsilon\delta_n},
$$

the transition probability from coordinate $0$ to coordinate $2n-1$ has real uniform average over $[0,\tau]$ satisfying

$$
\frac1\tau\int_0^\tau
\bigl|U_n(t)_{2n-1,0}\bigr|^2\,dt
>\frac{1-\varepsilon}{2n}.
$$
:::

::: {.proof #pf-central-defect-endpoint-average}
As in Lemma 1 of Childs et al., reflection determines the endpoint weights. Pairing conjugate terms before estimating the time average gives the shorter sufficient window.

Set $N=2n\ge2$. The real symmetric spectral theorem gives a real orthonormal eigenbasis $v_0,\ldots,v_{N-1}$ corresponding to the full eigenvalue list. Applying [@thm-central-defect-spectral-gap] with $m=n-1$ bounds every distinct-index eigenvalue distance below by $2\sqrt2/((1+\sqrt2)^2n^3)>0$. Thus every eigenvalue is simple. The set defining $\delta_n$ is finite and nonempty, so its minimum is strictly positive. Distinctness was derived rather than assumed.

Define coordinate reversal by $Re_x=e_{N-1-x}$. The reflected edge weights agree, so $RJ_n=J_nR$, and $R^2=I$. Hence $Rv_j$ lies in the same one-dimensional real eigenspace as $v_j$, giving $Rv_j=s_jv_j$; applying $R^2=I$ yields $s_j\in\{-1,1\}$. In particular,

$$
v_j(N-1)=s_jv_j(0).
$$

This derives endpoint spectral pairing from the actual matrix. Put $w_j=v_j(0)^2\ge0$. Orthonormality and $\|e_0\|=1$ give $\sum_jw_j=1$. Cauchy–Schwarz gives

$$
1=\Bigl(\sum_jw_j\Bigr)^2
\le N\sum_jw_j^2,
\qquad D:=\sum_jw_j^2\ge\frac1N>0.
$$

Substituting $J_n=\sum_j\lambda_jv_jv_j^{\mathsf T}$ into the power series for the matrix exponential and summing in this same eigenbasis gives the actual endpoint amplitude

$$
A(t):=U_n(t)_{N-1,0}
=\sum_j e^{-it\lambda_j}v_j(N-1)v_j(0)
=\sum_j s_jw_j e^{-it\lambda_j}.
$$

The row is the arrival endpoint and the column the starting endpoint; the reflection signs remain in the amplitude. The function $|A(t)|^2$ is real and continuous, hence integrable on the finite interval. Since $\varepsilon,\delta_n>0$, the time hypothesis implies $\tau>0$. For a nonzero real frequency $\omega$, the finite-window factor is

$$
\begin{aligned}
F_\tau(\omega)
&:=\frac1\tau\int_0^\tau e^{-it\omega}\,dt
=\frac{1-e^{-i\tau\omega}}{i\tau\omega},\\
|F_\tau(\omega)|&\le\frac{2}{\tau|\omega|}.
\end{aligned}
$$

Expanding the modulus squared and interchanging finite sums with integration gives

$$
\begin{aligned}
\overline P_\tau
&:=\frac1\tau\int_0^\tau |A(t)|^2\,dt=D+Q_\tau,\\
Q_\tau
&=\sum_{i\ne j}s_is_jw_iw_j
F_\tau(\lambda_i-\lambda_j).
\end{aligned}
$$

The coefficients $s_i s_j w_i w_j$ are real, and the terms for $(i,j)$ and $(j,i)$ are conjugate. Thus $Q_\tau$ is the sum of these coefficients times $\operatorname{Re}F_\tau(\lambda_i-\lambda_j)$. For $\omega\ne 0$, the real part is $\sin(\tau\omega)/(\tau\omega)$. Since every off-diagonal frequency has magnitude at least $\delta_n$, the triangle inequality gives

$$
\begin{aligned}
|Q_\tau|
&\le\frac{1}{\tau\delta_n}\sum_{i\ne j}w_iw_j
=\frac{1}{\tau\delta_n}(1-D),\\
0&\le1-D<1.
\end{aligned}
$$

Put $a=1/(\tau\delta_n)>0$. The time hypothesis gives $a\le\varepsilon/N$. Since $D>0$,

$$
\begin{aligned}
\overline P_\tau
&\ge D-a(1-D)\\
&>D-a\\
&\ge\frac1N-a\\
&\ge\frac{1-\varepsilon}{N}.
\end{aligned}
$$

The strict step uses $aD>0$, including at $\tau=2n/(\varepsilon\delta_n)$. This also proves the bound at the longer window in Lemma 1 of Childs et al. The argument covers every $\varepsilon>0$ and includes $n=1$. The full proof is checked by the Lean kernel.
:::

**Applicability.** [@thm-central-defect-endpoint-average] concerns a measurement at a uniformly random time in $[0,\tau]$ on this weighted path, starting at $0$. Its denominator contains the actual minimum gap $\delta_n$. Substituting the inverse-cubic lower bound gives a longer sufficient observation time. The case $n=1$ is a statement about the matrix. For a glued-trees oracle algorithm, one must verify the graph’s column counts, specify access to the oracle and the Hamiltonian time normalisation, and prove efficient simulation, identification of `EXIT`, and the success probability under repetition. The classical lower bound requires its own oracle argument. The complete algorithmic separation is the literature result cited in [@rem-qsvt-walks-literature].
