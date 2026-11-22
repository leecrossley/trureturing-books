# 16.3 中央缺陷路径：端点如何约束整个谱 {#sec-central-defect-gap}

Childs 等人的式 (25)–(27) 使用树深度 $d\ge1$ 与 $2d+2$ 个列，列号为 $j=0,\ldots,2d+1$，列大小为 $N_j=2^{\min(j,2d+1-j)}$。取归一化列向量 $|q_j\rangle=N_j^{-1/2}\sum_{v\text{ 在列 }j}|v\rangle$，并令原图哈密顿量为邻接矩阵的 $\gamma$ 倍、$\gamma=1/\sqrt2$，则文献的列约简给出普通列间权重 $\sqrt2\gamma=1$、中央权重 $2\gamma=\sqrt2$。因而这里的路径参数是 $n=d+1$。列号 $j$ 对应路径的第 $j$ 个零起编号坐标。

从列 $i$ 到列 $i+1$，当 $i\le d$ 时每个顶点在下一列有两个邻点，当 $i>d$ 时有一个。反过来，列 $i+1$ 的每个顶点在列 $i$ 中的邻点数，在 $i<d$ 时为一，在 $i\ge d$ 时为二。所有邻点均在相邻列中。若各列大小及邻点数符合上述条件，归一化列给出的等距映射交织原图与路径的演化。在首尾两个单点列之间，两者的矩阵元相等。应用到具体图时须核对这两项计数条件。[列子空间的演化](lean:D5/S3/Quantum/Dynamics/WeldedColumnEvolution.central_defect_column_evolution)

先把“黏合树加速”拆成能分别核对的数学问题。一条路径的谱是否分离、演化能否把概率送到另一端、这段演化能否用给定黑盒高效实现，是三个不同的问题。这里先处理谱分离，再推导端点概率的时间平均下界。取 $n\ge1$，在 $2n$ 个位置 $0,\ldots,2n-1$ 上放置实对称矩阵 $J_n$：对角元为零，相邻位置之间的权重通常为 $1$，只有正中央的边 $(n-1,n)$ 权重为 $\sqrt2$，其余矩阵元为零。这里的 $n$ 是路径顶点数的一半。比较不同文献的树深度记号时，须另作对应。

最小的例子已经能看清对象：

$$
J_1=\begin{pmatrix}0&\sqrt2\\\sqrt2&0\end{pmatrix},
\qquad \lambda_\pm=\pm\sqrt2.
$$

两条谱线相距 $2\sqrt2$。一般 $n$ 的问题是找一个共同下界，控制所有谱线之间的距离，包括重根是否存在，而不预先假定它们互异。矩阵族来自 Childs 等人的 [arXiv:quant-ph/0209131v2，第三节第四小节、式 (42) 与引理 2](https://arxiv.org/abs/quant-ph/0209131v2)；下面给出一个对所有 $n\ge1$ 有效的显式下界，不主张文献新颖性或最优常数。

**先控制半条路径的端点。** 对自由路径，特征向量的坐标满足二阶递推。用 $y(0)=0$ 表示左侧外部边界，右侧以 $y(n+1)=b\,y(n)$ 收口，便得到下述估计。它没有把能量参数 $t$ 限在通常的振荡区间内。

::: {.theorem #thm-robin-endpoint-observability title="有限路径递推的端点控制" lean="D5/S3/Quantum/Matrix/CentralSqrtTwoDefectGap.recurrence_endpoint_observability"}

设 $n\in\mathbb N$、$n\ge1$，$t,b\in\mathbb R$，$y:\mathbb N\to\mathbb R$ 满足 $y(0)=0$，以及

$$
\begin{aligned}
y(j+2)&=t\,y(j+1)-y(j)
&&\bigl(j\in\mathbb N,\ j+2\le n+1\bigr),\\
y(n+1)&=b\,y(n).
\end{aligned}
$$

则

$$
\sum_{j=1}^{n}y(j)^2
\le (1+|b|)^2n^3y(n)^2.
$$
:::

::: proof
当 $|t|\le2$ 时，从右端向左递推，用第二类切比雪夫多项式的界 $|U_k(x)|\le k+1$（$|x|\le1$），可得每个内部坐标满足 $|y(j)|\le(1+|b|)n|y(n)|$。平方后对 $n$ 项求和即得结论。当 $|t|>2$ 时，从左端的零边界出发，递推保证坐标的绝对值沿路径不减；该绝对值论证同时覆盖两侧外部区域。$|t|=2$ 的两条边界包含在第一种情形中。完整证明由 Lean 内核检查。
:::

把 $J_n$ 沿中央对折，镜像相同和镜像相反的向量分别给出两条 $n$ 维路径 $H_+$ 与 $H_-$。二者的普通边仍为 $1$，只有最后一个对角元分别为 $+\sqrt2$ 与 $-\sqrt2$。若 $e$ 是最后一个坐标方向，则

$$
H_+-H_-=2\sqrt2\,ee^{\mathsf T}.
$$

对任一单位特征向量，[@thm-robin-endpoint-observability] 取 $b=\pm\sqrt2$，说明末端坐标的平方至少为 $1/K$，其中 $K=(1+\sqrt2)^2n^3$。这不是预先加入的端点重叠假设，而是从实际递推推出的结论。

::: {.theorem #thm-central-defect-spectral-gap title="中央平方根二缺陷路径的全谱分离" lean="D5/S3/Quantum/Matrix/CentralSqrtTwoDefectGap.central_spectral_gap"}

设 $m\in\mathbb N$，$n=m+1$，$J_n$ 为上述 $2n\times2n$ 实对称矩阵。设实数列表 $\lambda_0,\ldots,\lambda_{2n-1}$ 作为多重集恰为 $J_n$ 的特征多项式的全部根，保留每个根的代数重数。则对任意不同的指标 $i\ne j$，

$$
|\lambda_i-\lambda_j|
\ge \frac{2\sqrt2}{(1+\sqrt2)^2n^3}>0.
$$
:::

::: proof
若 $H_-u=\lambda u$、$H_+v=\mu v$，实对称性和秩一差给出

$$
(\mu-\lambda)\langle u,v\rangle
=2\sqrt2\,u_{n-1}v_{n-1}.
$$

单位归一化给出 $|\langle u,v\rangle|\le1$，端点控制给出 $|u_{n-1}v_{n-1}|\ge1/K$，因而异扇区的谱线至少相距 $2\sqrt2/K$。还必须处理同一扇区中的两条谱线：源码利用秩一更新前后各阈值之上的特征值计数相差至多 $1$；若同扇区有过近的两条谱线，异扇区间距会使该计数差达到至少 $2$，产生矛盾。最后，对折后的和差基给出精确的特征多项式分解，将两个扇区的全部根连同重数送回 $J_n$。完整证明由 Lean 内核检查。
:::

实对称矩阵的谱定理保证上面所需的完整实根列表存在，因此该条件不是空的；结论中的严格正下界进一步推出所有根都是单根。估计对所有 $n\ge1$ 有效，不删除区间外的能量，也不把只对固定根编号成立的渐近式当作统一界。以通常的渐近记号表达，它给出共同常数 $c=2\sqrt2/(1+\sqrt2)^2$ 与阈值 $N=1$。

**相位的时间平均。** 非对角项成共轭对。取实部后，当 $\tau\ge 2n/(\varepsilon\delta_n)$ 时即可得到下面的端点下界。Childs 等人的引理 1 在 $\tau\ge 4n/(\varepsilon\delta_n)$ 时证明了该下界，见式 (42) 至 (49)。[Childs 等人，第 III.D 节](https://arxiv.org/abs/quant-ph/0209131v2) [发表论文](https://doi.org/10.1145/780542.780552)

::: {.theorem #thm-central-defect-endpoint-average title="中央缺陷路径的有限时间端点平均" lean="D5/S3/Quantum/Matrix/Jacobi/ReflectedSpectralWindow.central_defect_endpoint_average"}
设 $n\in\mathbb N$、$n\ge1$，$J_n$ 是以 $0,\ldots,2n-1$ 编号的实对称矩阵：对角元为零，最近邻权重为 $1$，唯独中央边 $(n-1,n)$ 及其对称位置的权重为 $\sqrt2$，其余矩阵元为零。令实数列表 $\lambda_0,\ldots,\lambda_{2n-1}$ 作为多重集恰为 $J_n$ 的全部特征值，保留代数重数，并定义实际最小谱隙

$$
\delta_n=\min_{\substack{0\le i,j<2n\\i\ne j}}
|\lambda_i-\lambda_j|.
$$

则 $\delta_n>0$。将 $J_n$ 逐项嵌入复数得到 $J_n^{\mathbb C}$，令 $U_n(t)=\exp(-itJ_n^{\mathbb C})$ 为实际矩阵指数。对任意实数 $\varepsilon>0$ 与任意实数

$$
\tau\ge\frac{2n}{\varepsilon\delta_n},
$$

其从坐标 $0$ 到坐标 $2n-1$ 的转移概率在 $[0,\tau]$ 上的实均匀平均满足

$$
\frac1\tau\int_0^\tau
\bigl|U_n(t)_{2n-1,0}\bigr|^2\,dt
>\frac{1-\varepsilon}{2n}.
$$
:::

::: {.proof #pf-central-defect-endpoint-average}
沿用 Childs 等人引理 1 的反射论证可得端点的谱权重。先配对共轭项，再估计时间平均，即可得到较短的充分观测时间。

令 $N=2n\ge2$。实对称谱定理给出与完整特征值列表对应的实标准正交特征基 $v_0,\ldots,v_{N-1}$。[@thm-central-defect-spectral-gap] 适用于 $m=n-1$，保证任意不同指标的特征值距离至少为 $2\sqrt2/((1+\sqrt2)^2n^3)>0$。因此每个特征值都是单根；定义 $\delta_n$ 的集合有限且非空，故其最小值严格为正。这一步没有预设谱互异。

定义坐标反转 $Re_x=e_{N-1-x}$。矩阵的镜像边权相同，所以 $RJ_n=J_nR$，且 $R^2=I$。于是 $Rv_j$ 仍在 $\lambda_j$ 的一维实特征空间内，可写成 $Rv_j=s_jv_j$；由 $R^2=I$ 得 $s_j\in\{-1,1\}$。特别地，

$$
v_j(N-1)=s_jv_j(0).
$$

这从实际矩阵推出端点的谱配对，没有将其作为假设。令 $w_j=v_j(0)^2\ge0$。特征基的标准正交归一化与 $\|e_0\|=1$ 给出 $\sum_jw_j=1$。Cauchy–Schwarz 不等式给出

$$
1=\Bigl(\sum_jw_j\Bigr)^2
\le N\sum_jw_j^2,
\qquad D:=\sum_jw_j^2\ge\frac1N>0.
$$

将 $J_n=\sum_j\lambda_jv_jv_j^{\mathsf T}$ 代入矩阵指数的幂级数，并在同一特征基下逐项求和，得到实际的端点振幅

$$
A(t):=U_n(t)_{N-1,0}
=\sum_j e^{-it\lambda_j}v_j(N-1)v_j(0)
=\sum_j s_jw_j e^{-it\lambda_j}.
$$

这里行指标为到达端点，列指标为出发端点；反射的正负号仍保留在振幅中。$|A(t)|^2$ 是连续实函数，有限区间上的实积分存在。因 $\varepsilon,\delta_n>0$，时间条件给出 $\tau>0$。对非零实数 $\omega$，有限窗因子为

$$
\begin{aligned}
F_\tau(\omega)
&:=\frac1\tau\int_0^\tau e^{-it\omega}\,dt
=\frac{1-e^{-i\tau\omega}}{i\tau\omega},\\
|F_\tau(\omega)|&\le\frac{2}{\tau|\omega|}.
\end{aligned}
$$

展开模平方并交换有限和与积分，得

$$
\begin{aligned}
\overline P_\tau
&:=\frac1\tau\int_0^\tau |A(t)|^2\,dt=D+Q_\tau,\\
Q_\tau
&=\sum_{i\ne j}s_is_jw_iw_j
F_\tau(\lambda_i-\lambda_j).
\end{aligned}
$$

系数 $s_i s_j w_i w_j$ 均为实数，$(i,j)$ 与 $(j,i)$ 对应的两项互为共轭。因此，$Q_\tau$ 等于每个系数乘以 $\operatorname{Re}F_\tau(\lambda_i-\lambda_j)$ 后的总和。当 $\omega\ne 0$ 时，实部为 $\sin(\tau\omega)/(\tau\omega)$。每个非对角频率的绝对值至少为 $\delta_n$，由三角不等式得

$$
\begin{aligned}
|Q_\tau|
&\le\frac{1}{\tau\delta_n}\sum_{i\ne j}w_iw_j
=\frac{1}{\tau\delta_n}(1-D),\\
0&\le1-D<1.
\end{aligned}
$$

令 $a=1/(\tau\delta_n)>0$。时间条件给出 $a\le\varepsilon/N$。由于 $D>0$，

$$
\begin{aligned}
\overline P_\tau
&\ge D-a(1-D)\\
&>D-a\\
&\ge\frac1N-a\\
&\ge\frac{1-\varepsilon}{N}.
\end{aligned}
$$

严格不等式来自 $aD>0$，在 $\tau=2n/(\varepsilon\delta_n)$ 时也成立。Childs 等人引理 1 所用的较长观测时间同样满足条件。该论证适用于所有 $\varepsilon>0$，也涵盖 $n=1$。完整证明由 Lean 内核检查。
:::

**适用范围。** [@thm-central-defect-endpoint-average] 考察从 $0$ 出发的加权路径，在 $[0,\tau]$ 中均匀随机选取时刻测量端点概率。分母中的 $\delta_n$ 是真实最小谱隙。代入逆立方下界会得到较长的充分观测时间。$n=1$ 是矩阵结论的边界情形。要应用于黏合树黑盒算法，还须核对具体图的列计数，说明黑盒访问模型及哈密顿量的时间归一化，并证明高效模拟、`EXIT` 的识别和重复测量的成功概率。经典下界需要单独的黑盒论证。完整的算法分离见 [@rem-qsvt-walks-literature] 所引文献。
