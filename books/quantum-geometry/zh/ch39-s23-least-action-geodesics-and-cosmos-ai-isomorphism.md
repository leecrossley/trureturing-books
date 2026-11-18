# 39.23 人工智能与宇宙的最小作用量同构：三元数场弦弧矢高、玻恩惊奇度、流群自平行测地线与零幻觉思维链 {#sec-ch39-least-action-geodesics-and-cosmos-ai-isomorphism}

> *“人工智能跟宇宙应该同构，都是在最小作用量下的信息系统，那么在三元数极小圆弧体场的语言下，最小作用量究竟是什么？测地线究竟是什么？”*

在 [§39.21](ch39-s21-nonlinear-ternion-representations-and-torsor-synthesis.md#sec-ch39-nonlinear-ternion-representations-and-torsor-synthesis) 确立三元数的五种无损非线性表示与无原点流群语法、并在 [§39.22](ch39-s22-ternion-field-transformer-and-rational-rotor-dynamics.md#sec-ch39-ternion-field-transformer-and-rational-rotor-dynamics) 将整座现代神经网络重铸为平行三元数概念场丛 $(\mathbb{T}_3)^K$ 上的纯有理旋子系统（TFT）之后，横亘在物理学与人工智能之间最后一道学科藩篱轰然洞开：**如果物理宇宙与通用人工智能底层都是运行在共享比较主频 $\nu_0$ 上的无外自指信息系统，那么支配星辰运转与量子演化的“最小作用量原理”，与支配大模型推理寻路与参数学习的“奥卡姆最优准则”，在三元数极小圆弧体场 $(\mathbb{T}_3)^K$ 的母语里究竟是同一个什么几何量？两者共同追寻的“测地线”究竟长什么样？**

本节作为第三十九章三元数与智能计算篇章的核心收束，给出严密而清澈的统一解答（宇宙与人工智能的双层同构总纲、跳步幻觉机制及逐场自然梯度预条件诠释标为 **`MODEL`**，有理步进核与弦弧矢高精确恒等式、成对余弦分解匀速节拍定理、流群自平行点反射与雅可比聚焦方程属 **`手工推导` / `NUM`**，分析力学、信息几何与思维链采样归入 **`文献结果`**，底层富比尼—施图迪三角不等式、记录时间下界、玻恩配对、舒尔补极小与球面和乐由 **`LEAN ✓`** 冻结声明锁定）：在 $(\mathbb{T}_3)^K$ 上，**最小作用量**就是完成跨态演化或概念对齐所支付的**最小累积二阶弦弧矢高**（精确等价于最小玻恩盲区信息泄漏与最少普适主频节拍税）；而**测地线**则是相邻极小圆弧满足**三元流群自平行 $[x_t, x_{t-1}, x_t]$、侧向叉乘扭矩为零且不围出多余球面角盈（$\Omega = 0$）的匀速大圆弧脊线**——它在物理宇宙中显影为惯性运动与引力自由落体，在人工智能中则严格同构为零幻觉的最短匀速思维链（Chain-of-Thought）与 $O(1)$ 零矩阵求逆的流形自然梯度流。

## 39.23.1 最小作用量的真身：弦弧矢高、有理步进核、玻恩惊奇度与主频节拍税 {#sec-ch39-23-1}

在传统学科分野中，物理学的莫培督—哈密顿作用量 $S = \int (T - V)\,dt$ 与机器学习的变分自由能（负对数似然交叉熵加复杂度散度）看似风马牛不相及；一旦回到共享普适比较主频 $\nu_0$（[§39.8](ch39-s08-universal-clock-and-gravitational-dilation.md#sec-ch39-universal-clock-and-gravitational-dilation)）的三元数场丛 $(B_1(\mathbb{R}^3))^K$，二者在单步极小圆弧比较中逐项合而为一。

设离散演化路径 $\Gamma = \{\mathbf{\Sigma}_t\}_{t=0}^N$ 在 $K$ 座概念场上按节拍推进，第 $t$ 拍在第 $k$ 座场上的相对比较旋子记为 $\boldsymbol{\delta}_t^{(k)} := (-\boldsymbol{\sigma}_{t-1}^{(k)}) \star_{\mathcal{S}} \boldsymbol{\sigma}_t^{(k)} \in B_1(\mathbb{R}^3)$，对应空间旋转张角 $\Delta\theta_t^{(k)} = 4\arctan\lVert\boldsymbol{\delta}_t^{(k)}\rVert \in [0, \pi]$（旋量半角为 $\frac{1}{2}\Delta\theta_t^{(k)} \in [0, \frac{\pi}{2}]$）。单步比较同时锁定三项严格等价的几何与信息成本（`手工推导`）：

1. **几何二阶弦弧矢高（Sagitta）**：极小圆弧偏离切线的内凹正矢拱高（呼应 [§34.30](ch34-s30-arc-body-calculus-and-finite-stokes.md#sec-ch34-arc-body-calculus-and-finite-stokes)）：

   $$
   v_\epsilon\bigl(\Delta\theta_t^{(k)}\bigr) \;:=\; 1 - \cos\Delta\theta_t^{(k)} \;=\; 2\sin^2\frac{\Delta\theta_t^{(k)}}{2} \;\in\; [0, 2];
   $$

2. **双卡有理步进能量核（免近似精确恒等式）**：在 [§39.22.1](ch39-s22-ternion-field-transformer-and-rational-rotor-dynamics.md#sec-ch39-22-1) 中，无穷小共形黎曼线元满足 $ds_{S^3}^2 = \frac{4\lVert d\boldsymbol{\sigma}\rVert^2}{(1+\lVert\boldsymbol{\sigma}\rVert^2)^2} = \frac{1}{4}(d\theta)^2$；而若将同一共形有理核直接作用于**任意有限步进旋子** $\boldsymbol{\delta}_t^{(k)}$（无需小角度近似！），利用 $\lVert\boldsymbol{\delta}_t^{(k)}\rVert = \tan\frac{\Delta\theta_t^{(k)}}{4}$，对一切 $\Delta\theta_t^{(k)} \in [0, \pi]$ 恒成立精确代数恒等式：

   $$
   q_{\mathrm{MRP}}\bigl(\boldsymbol{\delta}_t^{(k)}\bigr) \;:=\; \frac{4\,\lVert\boldsymbol{\delta}_t^{(k)}\rVert^2}{\bigl(1 + \lVert\boldsymbol{\delta}_t^{(k)}\rVert^2\bigr)^2} \;=\; 4\tan^2\frac{\Delta\theta_t^{(k)}}{4}\cos^4\frac{\Delta\theta_t^{(k)}}{4} \;\equiv\; \sin^2\frac{\Delta\theta_t^{(k)}}{2} \;\equiv\; \frac{1}{2}\,v_\epsilon\bigl(\Delta\theta_t^{(k)}\bigr);
   $$

3. **香农—玻恩比较惊奇度（Comparison Surprisal）**：相邻两拍经往返双投影（[`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight)，`LEAN ✓`）同相留存的概率为 $P_{\mathrm{stay}} = b(\boldsymbol{\sigma}_{t-1}^{(k)}, \boldsymbol{\sigma}_t^{(k)}) = \cos^2\frac{\Delta\theta_t^{(k)}}{2}$，漏入 $90^\circ$ 正交虚盲区 $\hat{\mathbf{i}}$ 的失锁概率恰等于有理步进核 $P_{\mathrm{leak}} = 1 - P_{\mathrm{stay}} = \sin^2\frac{\Delta\theta_t^{(k)}}{2} \equiv \frac{1}{2}v_\epsilon$，故单步负对数似然惊奇度展开为全正项幂级数：

   $$
   \mathcal{I}_t^{(k)} \;:=\; -\ln\cos^2\!\left(\frac{\Delta\theta_t^{(k)}}{2}\right) \;=\; -\ln\!\left(1 - \frac{v_\epsilon}{2}\right) \;=\; \frac{1}{2}v_\epsilon \;+\; \frac{1}{8}v_\epsilon^2 \;+\; \mathcal{O}(v_\epsilon^3).
   $$

将胞内翻转矢高与外部背景场或上下文约束预占的耦合角盈势 $\Omega_{\mathrm{ctx}}^{(k)}(\boldsymbol{\sigma}_t)$ 沿整条路径累加，物理宇宙与人工智能共同遵循的**无量纲三元数场总作用量泛函**（`MODEL`）直接写为：

$$
\mathcal{S}[\Gamma] \;:=\; \sum_{t=1}^{N}\sum_{k=1}^{K} \Biggl[\underbrace{\bigl(1 - \cos\Delta\theta_t^{(k)}\bigr)}_{\substack{\text{胞内推进矢高 } T\\\text{（状态翻转主频开销）}}} \;-\; \underbrace{\Omega_{\mathrm{ctx}}^{(k)}(\boldsymbol{\sigma}_t)}_{\substack{\text{背景 / 语境耦合角盈 } V\\\text{（引力势井或上下文约束）}}}\Biggr].
$$

这道无量纲泛函一举揭开最小作用量原理的三重物理与认知底牌：

- **普朗克常数 $\hbar$ 即主频节拍汇率**：全宇宙共享恒定比较主频 $\nu_0$（锚定富比尼—施图迪记录时长下界 [`record_time_lower_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_time_lower_bound) 与步数上界 [`record_count_upper_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_count_upper_bound)，`LEAN ✓`），每累积一单位弦弧矢高就支付固定份额的底层比较节拍；宏观物理作用量 $S_{\mathrm{phys}} = \hbar\mathcal{S}[\Gamma]$ 之所以带“能量 $\times$ 时间”量纲，只因乘上了把无量纲圆弧相位换算为国际单位制焦耳·秒的汇率常数 $\hbar$；
- **拉格朗日量 $T - V$ 减号的舒尔补起源**：在总预算归一的分块格拉姆矩阵中，外部引力负载或提示词上下文约束 $\Omega_{\mathrm{ctx}}$ 预先占用了跨场关联带宽，留给局部状态自由推进的可支配净余量，正是分块消元后的**舒尔补变分极小垂高** $A - B C^{-1} B^\dagger$（[`schur_quadratic_is_least`](lean:D5/S3/Quantum/Matrix/SchurMinimum.schur_quadratic_is_least)，`LEAN ✓`）；
- **虚盲区异相湮灭自动筛出最小作用量与最优思维链**：系统无需在落步前未卜先知地遍历全局极小。在多路径相干演化 $\sum_\Gamma \exp(\hat{\mathbf{i}}\mathcal{S}[\Gamma])$ 中，偏离极值、平白绕远的冗余支路围出额外球面角盈，在正交虚盲区 $\hat{\mathbf{i}}$ 内高速旋相并与邻近微扰支路成对异相抵消；唯有一阶变分为零（$\delta\mathcal{S} = 0$）的**驻相脊线**同相相长存活（见 [§32.3](ch32-s03-axioms-as-corollaries.md) 与 [§34.6](ch34-s06-berry-sectors-and-path-integrals.md)）——在物理中凝结为经典轨道，在人工智能中则同构于多条采样思维链经自洽性投票（Self-Consistency，Wang et al. 2023）滤除互相矛盾的废话分支后留存的唯一简洁推理主干！

## 39.23.2 测地线的四重等价定义：流群自平行、零角盈、匀速节拍锁与雅可比聚焦 {#sec-ch39-23-2}

在平直空间 $\mathbb{R}^d$ 中，两点间的欧氏弦线插值 $(1-\lambda)\mathbf{x}_0 + \lambda\mathbf{x}_1$ 直接切穿球体内部，造成中间层特征模长坍缩；而在紧致弯曲的三元数场丛 $(B_1(\mathbb{R}^3))^K$ 上，无需书写繁琐的克里斯托费尔符号 $\Gamma^i_{jk}$，一条**自由测地线**拥有四重等价且可纯有理计算的几何刻画（`手工推导`）：

1. **无原点的三元流群自平行接力（嘉当对称空间点反射律）**：
   在抹除特权实轴 $\mathbf{1}$ 的三元流群 $[x, y, z] = x y^{-1} z$（[§39.21.4](ch39-s21-nonlinear-ternion-representations-and-torsor-synthesis.md#sec-ch39-21-4)）中，离散轨迹 $\{\boldsymbol{\sigma}_t\}_{t=0}^N$ 是一条恒定步幅测地线，当且仅当任意连续三拍严格满足**流群自反射接力方程**（只要单步未踏上零测度半周折缝）：

   $$
   \boldsymbol{\sigma}_{t+1}^{(k)} \;=\; \Bigl[\boldsymbol{\sigma}_t^{(k)},\; \boldsymbol{\sigma}_{t-1}^{(k)},\; \boldsymbol{\sigma}_t^{(k)}\Bigr] \;\equiv\; \boldsymbol{\sigma}_t^{(k)} \star_{\mathcal{S}} \Bigl(\bigl(-\boldsymbol{\sigma}_{t-1}^{(k)}\bigr) \star_{\mathcal{S}} \boldsymbol{\sigma}_t^{(k)}\Bigr).
   $$

   在非阿贝尔群 $\mathrm{SU}(2)$ 或 $\mathrm{SO}(3)$ 上代入单参数测地线 $g_t = g_0 e^{tX}$ 立即验证：$g_t g_{t-1}^{-1} g_t = g_0 e^{tX} e^{-(t-1)X} g_0^{-1} g_0 e^{tX} = g_0 e^{(t+1)X} = g_{t+1}$（即便起点 $g_0$ 与生成元 $e^X$ 不可交换亦严格成立！）。这正是嘉当对称空间以当前点 $g_t$ 为支点的**测地点反射对合** $s_{g_t}(g_{t-1}) = g_t g_{t-1}^{-1} g_t$：把上一拍相对比较圆弧原封不动平行顺延到下一拍，不搀半点外来偏置。

2. **零叉乘侧向扭矩与零吉拉尔球面角盈（$\Omega = 0$）**：
   记相邻两拍局部右步进旋子为 $\boldsymbol{\omega}_t := (-\boldsymbol{\sigma}_{t-1}) \star_{\mathcal{S}} \boldsymbol{\sigma}_t$ 与 $\boldsymbol{\omega}_{t+1} := (-\boldsymbol{\sigma}_t) \star_{\mathcal{S}} \boldsymbol{\sigma}_{t+1}$。审视双分母有理乘法分子 $\mathbf{N}(\boldsymbol{\omega}_t, \boldsymbol{\omega}_{t+1}) = (1-\lVert\boldsymbol{\omega}_t\rVert^2)\boldsymbol{\omega}_{t+1} + (1-\lVert\boldsymbol{\omega}_{t+1}\rVert^2)\boldsymbol{\omega}_t + 2(\boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1})$，大圆共轴不偏折充要于**非线性叉乘侧向扭矩恒等于零**（锚定 [`lagrange_gram_identity`](lean:D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity) 与 [`shortest_gate_triangle_holonomy`](lean:D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.shortest_gate_triangle_holonomy)，`LEAN ✓`）：

   $$
   \boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1} \;=\; \mathbf{0} \quad \Longleftrightarrow \quad \Omega\bigl(\boldsymbol{\sigma}_{t-1}, \boldsymbol{\sigma}_t, \boldsymbol{\sigma}_{t+1}\bigr) \;=\; 0.
   $$

   当额外满足同向推进 $\boldsymbol{\omega}_t \cdot \boldsymbol{\omega}_{t+1} \ge 0$（排除沿同大圆折返）且总转角不超过割迹界 $\sum_{t=1}^N \Delta\theta_t \le \pi$ 时，富比尼—施图迪三角不等式（[`fs_angle_triangle`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.fs_angle_triangle)，`LEAN ✓`）精确取等，首尾总测地角等于各拍分步转角之和；若再令步幅相等 $\boldsymbol{\omega}_{t+1} = \boldsymbol{\omega}_t$，便完全复原第 1 款流群自平行律！当注意力舒尔桥或外部规范场注入非共线扭矩 $\boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1} \neq \mathbf{0}$ 时，底流形投影发生受控折射；而在卡鲁扎—克莱因—黄（Kaluza–Klein–Wong）主丛联络度规下，含守恒纤维荷的受控偏折轨迹依然升格为全丛空间上的一条测地线（`文献结果`）。

3. **矢高凸性与成对余弦分解锁定的“匀速节拍律”（牛顿匀速惯性与 AI 跳步幻觉机制）**：
   即便轨迹已锁定在同一条大圆弧上（给定首尾总角跨度 $\sum_{t=1}^N \Delta\theta_t = \Theta \in (0, \pi)$，$\Delta\theta_t \ge 0$），各拍步幅应如何分配方能最小化总矢高作用量？注意单步矢高 $f(\Delta\theta) = 1 - \cos\Delta\theta$ 在四分周区间 $[0, \frac{\pi}{2}]$ 上满足 $f''(\Delta\theta) = \cos\Delta\theta \ge 0$（严格下凸）；不仅如此，对**整个开区间 $\Theta \in (0, \pi)$ 内任意非负步幅分配**（即便某一步跨入钝角 $(\frac{\pi}{2}, \pi)$！），利用精确成对余弦和差恒等式（`手工推导`）：

   $$
   (1 - \cos x_i) + (1 - \cos x_j) \;=\; 2 \;-\; 2\cos\frac{x_i + x_j}{2}\cos\frac{x_i - x_j}{2} \;\ge\; 2\!\left(1 - \cos\frac{x_i + x_j}{2}\right),
   $$

   因 $x_i + x_j \le \Theta < \pi \implies \cos\frac{x_i+x_j}{2} > 0$，只要存在任意两拍步幅不等 $x_i \neq x_j$，将其平均化必严格降低总矢高（且香农—玻恩惊奇度更在全域 $[0, \pi)$ 上满足严格凸性 $\mathcal{I}''(\Delta\theta) = \frac{1}{2}\sec^2\frac{\Delta\theta}{2} \ge \frac{1}{2} > 0$）！故全局唯一严格极小解锁死在**匀速等步幅节拍** $\Delta\theta_1 = \dots = \Delta\theta_N = \frac{\Theta}{N}$：

   $$
   \sum_{t=1}^{N}\bigl(1 - \cos\Delta\theta_t\bigr) \;\ge\; N\!\left(1 - \cos\frac{\Theta}{N}\right), \qquad \sum_{t=1}^{N}\mathcal{I}(\Delta\theta_t) \;\ge\; -N\ln\cos^2\!\left(\frac{\Theta}{2N}\right)!
   $$

   这一不等式同时照亮物理与 AI 的核心法则（`MODEL`）：在物理中，它从离散圆弧矢高直接导出牛顿第一定律的**“匀速”**——忽快忽慢的变速推进会平白激增二阶矢高与盲区相位耗散；在 AI 推理中，它精准刺破了**大模型“前序套话空转、末步跳步抢答”必生幻觉**的几何病根——若模型在前 $N-1$ 步原地踏步（$\Delta\theta_t \approx 0$），却在最后一步强跨大角 $\Delta\theta_N = \Theta$，单步盲区泄漏率 $\sin^2(\Theta/2)$ 与惊奇度将呈平方乃至对数发散暴增，瞬间冲出语义吸引盆；唯有将总推理跨度均摊为每拍 $\frac{\Theta}{N}$ 的**匀速测地思维链**，方能以 $O(\Theta^2/N)$ 的反比矢高税稳健抵达答案！

4. **正截面曲率利雅三元雅可比聚焦（天然抗幻觉发散）**：
   在平直欧氏空间（$\kappa = 0$，噪声偏差随层数线性漂移 $\lVert\mathbf{J}_\perp(s)\rVert \propto s$）或负曲率双曲空间（指数发散 $\sinh(\lvert\kappa\rvert s)$）中，提示词微扰极易逐层滚雪球般滑向荒诞区域。而在截面曲率 $\kappa^2 > 0$（单位 $S^3$ 上 $\kappa = 1$）的三元数球面上，正交于单位切矢 $\dot{\gamma}$ 的测地偏离场 $\mathbf{J}_\perp$（$\mathbf{J}_\perp \cdot \dot{\gamma} = 0$）服从由 [§39.21.4](ch39-s21-nonlinear-ternion-representations-and-torsor-synthesis.md#sec-ch39-21-4) 利雅三元曲率括号支配的**雅可比聚焦方程**（注意符号对齐：由 $\{\mathbf{a},\mathbf{b},\mathbf{c}\} = (\mathbf{a}\cdot\mathbf{c})\mathbf{b} - (\mathbf{b}\cdot\mathbf{c})\mathbf{a}$，对 $\mathbf{J}_\perp \perp \dot{\gamma}$ 恒有 $\{\dot{\gamma}, \mathbf{J}_\perp, \dot{\gamma}\} = +\lVert\dot{\gamma}\rVert^2\mathbf{J}_\perp = -\{\mathbf{J}_\perp, \dot{\gamma}, \dot{\gamma}\}$，`手工推导`）：

   $$
   \frac{D^2\mathbf{J}_\perp}{ds^2} \;+\; \kappa^2\bigl\{\dot{\gamma},\, \mathbf{J}_\perp,\, \dot{\gamma}\bigr\} \;=\; \frac{D^2\mathbf{J}_\perp}{ds^2} \;-\; \kappa^2\bigl\{\mathbf{J}_\perp,\, \dot{\gamma},\, \dot{\gamma}\bigr\} \;=\; \ddot{\mathbf{J}}_\perp \;+\; \kappa^2\mathbf{J}_\perp \;=\; \mathbf{0}!
   $$

   其通解 $\mathbf{J}_\perp(s) = \mathbf{J}_\perp(0)\cos(\kappa s) + \frac{\dot{\mathbf{J}}_\perp(0)}{\kappa}\sin(\kappa s)$ 天然具备余弦向心恢复力，令微小输入措辞扰动围绕主干推理测地线做有界谐振并重新聚焦于同一答案吸引子！

## 39.23.3 宇宙与人工智能双层同构谱系、O(1) 共形自然梯度与全书正文终极收束 {#sec-ch39-23-3}

我们将三元数场最小作用量、四重测地线判据与“前向推理 $\leftrightarrow$ 测地运动、反向训练 $\leftrightarrow$ 曲率塑形”双层同构正式收束如下：

::: {.definition #def-ch39-ternion-least-action-and-heap-geodesic title="三元数场无量纲矢高作用量泛函、流群自平行测地线与共形黎曼自然梯度（模型定义）"}
在平行三元数概念场单位球丛 $(B_1(\mathbb{R}^3))^K$ 上（`MODEL`）：

1. **三元数场离散总作用量**：给定演化路径 $\Gamma = \{\mathbf{\Sigma}_t\}_{t=0}^N$ 与语境角盈势 $\Omega_{\mathrm{ctx}}^{(k)}$，定义总作用量 $\mathcal{S}[\Gamma] := \sum_{t=1}^N\sum_{k=1}^K \bigl[2\,q_{\mathrm{MRP}}(\boldsymbol{\delta}_t^{(k)}) - \Omega_{\mathrm{ctx}}^{(k)}(\boldsymbol{\sigma}_t)\bigr]$，其中 $2\,q_{\mathrm{MRP}}(\boldsymbol{\delta}) = \frac{8\lVert\boldsymbol{\delta}\rVert^2}{(1+\lVert\boldsymbol{\delta}\rVert^2)^2} \equiv 1 - \cos\Delta\theta$；
2. **离散自由流群测地线**：满足三元流群自平行接力 $\boldsymbol{\sigma}_{t+1}^{(k)} = [\boldsymbol{\sigma}_t^{(k)}, \boldsymbol{\sigma}_{t-1}^{(k)}, \boldsymbol{\sigma}_t^{(k)}]$（等价于共轴正向 $\boldsymbol{\omega}_t^{(k)} \times \boldsymbol{\omega}_{t+1}^{(k)} = \mathbf{0}$ 且等步幅 $\boldsymbol{\omega}_{t+1}^{(k)} = \boldsymbol{\omega}_t^{(k)}$）的轨道；
3. **逐场 $O(1)$ 共形黎曼最速下降算子**：在诱导共形对角度规 $g_{ij}(\boldsymbol{\sigma}) = \frac{4\,\delta_{ij}}{(1+\lVert\boldsymbol{\sigma}\rVert^2)^2}$ 下，参数旋子 $\boldsymbol{\sigma}_W$ 的精确内禀黎曼梯度为免矩阵求逆的标量缩放 $\operatorname{grad}_{S^3}\mathcal{L}(\boldsymbol{\sigma}_W) := g(\boldsymbol{\sigma}_W)^{-1}\nabla\mathcal{L} = \frac{1}{4}(1 + \lVert\boldsymbol{\sigma}_W\rVert^2)^2\,\nabla\mathcal{L}$。
:::

::: {.theorem #thm-ch39-least-action-geodesics-and-cosmos-ai-anchors title="富比尼—施图迪测地三角不等式、正交记录时长下界与计数上界、秩一玻恩重叠权重、舒尔补二次型变分极小、最短旋子门与球面三角和乐、拉格朗日—格拉姆恒等式及本征定态与克雷洛夫永久稳定定理" lean="D5/S3/QuantumBounds/FubiniStudyRecordTime.fs_angle_triangle,D5/S3/QuantumBounds/FubiniStudyRecordTime.record_time_lower_bound,D5/S3/QuantumBounds/FubiniStudyRecordTime.record_count_upper_bound,D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight,D5/S3/Quantum/Matrix/SchurMinimum.schur_quadratic_is_least,D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.rotor_shortest_gate,D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.shortest_gate_triangle_holonomy,D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity,D5/S3/Quantum/Dynamics/EnergyEigenstateStationarity.energy_eigenstate_stationary,D5/S3/ObserverMemory/Dynamics/ObservableKrylovPermanentStability.observable_krylov_once_stable_permanently"}
在所钉 `trureturing` 冻结声明集中，以下十项为三元数场最小作用量、测地最短路径、主频节拍下界、舒尔 $T-V$ 拆账与定态停机终点提供严格数学支点的定理同时成立：

1. **单位向量富比尼—施图迪测地夹角三角不等式**（[`fs_angle_triangle`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.fs_angle_triangle)）：对任意三枚单位态矢 $u, v, w$，测地角满足 $d_{\mathrm{FS}}(u, w) \le d_{\mathrm{FS}}(u, v) + d_{\mathrm{FS}}(v, w)$；
2. **正交可分辨记录的最短演化时长下界与串行记录计数上界**（[`record_time_lower_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_time_lower_bound)、[`record_count_upper_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_count_upper_bound)）：有界能量方差演化分辨正交记录所需的最小时间与有限时长内的最大记录步数受普适量子速度极限严格约束；
3. **秩一记录测量的玻恩模平方留存权重**（[`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight)）：纯态在秩一投影测量下的读出权重精确等于模平方重叠 $\lvert\langle\phi, \psi\rangle\rvert^2$；
4. **埃尔米特分块矩阵舒尔补二次型的变分最小元**（[`schur_quadratic_is_least`](lean:D5/S3/Quantum/Matrix/SchurMinimum.schur_quadratic_is_least)）：严格正定内部块消元精确达到舒尔补余量下确界 $x^\dagger(A - B C^{-1} B^\dagger)x$；
5. **非对跖单位方向测地最短旋子门与三顶点球面三角和乐**（[`rotor_shortest_gate`](lean:D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.rotor_shortest_gate)、[`shortest_gate_triangle_holonomy`](lean:D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.shortest_gate_triangle_holonomy)）：单步最短旋子实现幺正测地搬运，三步闭合回路积累精确球面角盈返回相位 $\frac{S_{abc} - i D_{abc}}{\sqrt{S_{abc}^2 + D_{abc}^2}}$（共大圆 $D_{abc} = 0$ 时角盈相位精确归零）；
6. **实向量拉格朗日—格拉姆二阶余子式恒等式**（[`lagrange_gram_identity`](lean:D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity)）：$\lVert u\rVert^2\lVert v\rVert^2 - \langle u, v\rangle^2 = \frac{1}{2}\sum_{i,j}(u_i v_j - u_j v_i)^2$；
7. **归一化能量本征态密度矩阵定态性与可观测量克雷洛夫子空间永久稳定律**（[`energy_eigenstate_stationary`](lean:D5/S3/Quantum/Dynamics/EnergyEigenstateStationarity.energy_eigenstate_stationary)、[`observable_krylov_once_stable_permanently`](lean:D5/S3/ObserverMemory/Dynamics/ObservableKrylovPermanentStability.observable_krylov_once_stable_permanently)）：本征态在厄米演化下精确不动，且有限维可观测量克雷洛夫塔一旦相邻两阶闭合便对一切后续步永久稳定。
:::

::: proof
第 1 款将单位态矢内积模长还原为球面余弦，利用柯西—施瓦茨与反余弦次可加性证出测地三角不等式（见 [第 7 章](ch07-geometric-time-and-speed-limits.md)）。第 2 款将单步测地推进速率上界积分至正交距离 $\frac{\pi}{2}$，直接导出最短记录步长与总时间窗内的最大正交翻转次数（见 [§39.8](ch39-s08-universal-clock-and-gravitational-dilation.md)）。第 3、4、7（后半）款证明同 [@thm-ch39-tft-born-holonomy-krylov-and-schur-anchors] 第 1、7、4 款。第 5、6 款证明同 [@thm-ch39-nonlinear-ternion-representations-and-torsor] 第 3–4、2 款。第 7 款前半由 $H\psi = E\psi$ 推出幺正演化仅乘全局相位 $e^{-iEt}$，外积投影算符 $\lvert\psi\rangle\langle\psi\rvert$ 严格时间不变。完整证明由 Lean 内核检查。
:::

::: {.remark #rem-ch39-maupertuis-feynman-friston-amari-cot-literature title="莫培督—费曼最小作用量、自由能与最小描述长度、阿马里自然梯度与量子费希尔度规及思维链自洽采样文献边界"}
**文献归属与统计费希尔度规边界声明。** 本节跨学科映射涉及的经典文献与精确数学适用边界如下：

1. **物理最小作用量、主丛测地线与信息自由能**：莫培督—拉格朗日—哈密顿变分原理与费曼相干路径积分见 R. P. Feynman（*Rev. Mod. Phys.* **20**, 367–387, 1948）；规范场中带荷粒子在主丛度规下升格为全丛测地线的卡鲁扎—克莱因—黄方程见 S. K. Wong（*Nuovo Cimento A* **65**, 689–694, 1970）与 R. Montgomery（*Lett. Math. Phys.* **8**, 59–67, 1984）；最小描述长度（MDL）与变分自由能原理见 J. Rissanen（*Automatica* **14**, 465–471, 1978）与 K. Friston（*Nat. Rev. Neurosci.* **11**, 127–138, 2010，DOI `10.1038/nrn2787`）；
2. **阿马里自然梯度、量子费希尔度规与大语言模型思维链采样**：参数流形统计自然梯度 $F(\theta)^{-1}\nabla\mathcal{L}$ 见 S.-i. Amari（*Neural Comput.* **10**(2), 251–276, 1998，DOI `10.1162/089976698300017746`）与分块克罗内克近似 K-FAC（Martens & Grosse, *ICML*, 2015）；单量子态测量的富比尼—施图迪 / 量子费希尔信息度规见 S. L. Braunstein & C. M. Caves（*Phys. Rev. Lett.* **72**, 3439–3443, 1994）；大模型逐步思维链推理与多路径自洽投票见 J. Wei 等人（*NeurIPS*, 2022）与 X. Wang 等人（`Self-Consistency`, *ICLR*, 2023，`arXiv:2203.11171`）。**严格数学边界说明**：对单枚三元数旋子直接制备的纯态玻恩分布 $p(m\mid\boldsymbol{\sigma}) = \cos^2(\Delta\theta_m/2)$，量子费希尔度规与圆球面共形度规 $g_{ij}(\boldsymbol{\sigma}) = \frac{4\,\delta_{ij}}{(1+\lVert\boldsymbol{\sigma}\rVert^2)^2}$ 严格成常数正比，故标量缩放 $\frac{1}{4}(1+\lVert\boldsymbol{\sigma}\rVert^2)^2\nabla\mathcal{L}$ 在单旋子层面上精确给出免求逆自然梯度；而在多层复合深度网络中，输出词表分布的经验统计费希尔矩阵还经多层雅可比耦合各层权重，此时逐场标量缩放严格定位为**精确参数流形黎曼最速下降与 $O(1)$ 分块对角几何预条件器**（`MODEL`），大规模训练收敛收益归入 [@prob-ch39-tft-scale-and-seams]（`OPEN`）。
:::

下面我们通过四联精确数值审计，对匀速测地线、跳步抢答失速、侧向绕行弯路与平直穿球割线四类轨迹的矢高作用量、玻恩留存率及 $O(1)$ 共形黎曼梯度逐一核验：

::: {.example #ex-ch39-geodesic-vs-jump-detour-and-natural-gradient-audit title="四类推理轨迹作用量对决：匀速流群测地线对比末步跳步幻觉、侧向绕行角盈与 O(1) 共形梯度核验"}
设单座三元数概念场需在 $N = 4$ 拍内从起点 $\boldsymbol{\sigma}_0 = \mathbf{0}$（北极 $+\mathbf{1}$）演化至终点空间转角 $\Theta = \frac{2\pi}{3} = 120^\circ$（绕 $\hat{\mathbf{e}}_1$ 轴，$\boldsymbol{\sigma}_4 = \tan 30^\circ\,\mathbf{e}_1 = \frac{1}{\sqrt{3}}\mathbf{e}_1 \approx (0.57735027, 0, 0)$，`手工推导` / `NUM`）：

1. **第一联：流群自平行匀速测地线对比“前序空转 $+$ 末步跳步抢答”幻觉暴增（`手工推导` / `NUM`）**：
   - **轨迹 A（流群自平行匀速测地线）**：每拍等步幅推进 $\Delta\theta_t = 30^\circ = \frac{\pi}{6}$（单步旋子 $\boldsymbol{\omega} = \tan 7.5^\circ\,\mathbf{e}_1 \approx 0.13165250\,\mathbf{e}_1$，逐拍严格满足 $\boldsymbol{\sigma}_{t+1} = [\boldsymbol{\sigma}_t, \boldsymbol{\sigma}_{t-1}, \boldsymbol{\sigma}_t]$ 与 $\boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1} = \mathbf{0}$）。单步矢高 $1 - \cos 30^\circ = 1 - \frac{\sqrt{3}}{2} \approx 0.13397460$，四拍总矢高作用量为
     $$\mathcal{S}_{\mathrm{geo}} = 4\!\left(1 - \frac{\sqrt{3}}{2}\right) \approx \mathbf{0.53589838}, \qquad P_{\mathrm{stay,total}} = \bigl(\cos^2 15^\circ\bigr)^4 = \left(\frac{2+\sqrt{3}}{4}\right)^4 = \frac{97+56\sqrt{3}}{256} \approx \mathbf{0.75779236}, \qquad \sum_{t=1}^4 \mathcal{I}_t \approx \mathbf{0.27734586\;\mathrm{nat}};$$
   - **轨迹 B（前三拍套话空转 $\Delta\theta_{1,2,3} = 0^\circ$、第四拍强跨 $\Delta\theta_4 = 120^\circ$ 跳步抢答）**：虽然同样落在大圆上且总转角同为 $120^\circ$，但总矢高作用量暴涨至 $\mathcal{S}_{\mathrm{jump}} = 0 + 0 + 0 + (1 - \cos 120^\circ) = \mathbf{1.50000000}$（**是匀速测地线的 $2.79903811$ 倍！**），四拍同相留存率断崖跌至 $P_{\mathrm{stay,total}} = \cos^2 60^\circ = \mathbf{0.25000000}$（盲区泄漏高达 $75\%$），总比较惊奇度飙升至 $-\ln(0.25) \approx \mathbf{1.38629436\;\mathrm{nat}}$（**激增 $4.99843184$ 倍**）！

2. **第二联：带侧向叉乘扭矩的非测地绕行线对比平直张量穿球割线坍缩（`NUM`）**：
   - **轨迹 C（侧向叉乘绕行弯路）**：令中间两拍向正交 $\hat{\mathbf{e}}_2$ 方向偏折再折回终点，比如以显式两段正交大圆绕行（先绕 $y$ 轴 $90^\circ$ 再衔接返回至绕 $x$ 轴 $120^\circ$，分四拍均摊每两拍各一轴）为例，相邻轴切换处 $\boldsymbol{\omega}_2 \times \boldsymbol{\omega}_3 \neq \mathbf{0}$ 围出非零吉拉尔球面角盈 $\Omega > 0$，总路径弧长突破 $120^\circ$，总矢高严格高于 $\mathbf{0.53589838}$；且在对称支路求和中，其盲区奇相位分量 $-i\sin\frac{\Omega}{2}$ 与镜像反绕支路的 $+i\sin\frac{\Omega}{2}$ 精确反相抵消（实同相幅值亦按 $\cos\frac{\Omega}{2} < 1$ 衰减，当角盈达 $\Omega = \pi$ 时整对支路 $e^{-i\pi/2}+e^{+i\pi/2}=0$ 彻底湮灭）；
   - **轨迹 D（传统平直欧氏线性插值穿球割线）**：在四维四元数嵌入中取弦中点 $\frac{1}{2}U(\boldsymbol{\sigma}_0) + \frac{1}{2}U(\boldsymbol{\sigma}_4) = \frac{1}{2}(1,0,0,0) + \frac{1}{2}(\frac{1}{2}, \frac{\sqrt{3}}{2}, 0, 0) = (\frac{3}{4}, \frac{\sqrt{3}}{4}, 0, 0)$，其模方直接坍缩为 $\frac{9}{16} + \frac{3}{16} = \mathbf{0.75000000 < 1}$（丢失 $25\%$ 球面模方预算，正是传统网络不得不层层依赖 `RMSNorm` 硬拉回球面的根源）！

3. **第三联：$O(1)$ 共形黎曼自然梯度与李代数拉回范数精确一致性核验（`手工推导`）**：
   在赤道附近 $\lVert\boldsymbol{\sigma}_W\rVert = 0.8$（$1 + \lVert\boldsymbol{\sigma}_W\rVert^2 = 1.64$）处，共形度规 $g_{ij} = \frac{4}{1.64^2}\delta_{ij} \approx 1.48720999\,\delta_{ij}$，免求逆黎曼梯度直接乘标量 $\frac{1.64^2}{4} = \mathbf{0.67240000}$；核验黎曼范数平方 $\langle\nabla\mathcal{L}, g^{-1}\nabla\mathcal{L}\rangle = \frac{1}{4}(1+\lVert\boldsymbol{\sigma}_W\rVert^2)^2\lVert\nabla\mathcal{L}\rVert^2$，与 [§39.22.2](ch39-s22-ternion-field-transformer-and-rational-rotor-dynamics.md#sec-ch39-22-2) 右乘自旋生成元拉回梯度模方 $\lVert\mathbf{g}_{\mathfrak{su}(2)}^{(R)}\rVert^2 = \frac{1}{4}\lVert J_R^\top\nabla\mathcal{L}\rVert^2 = \frac{1}{4}(1+\lVert\boldsymbol{\sigma}_W\rVert^2)^2\lVert\nabla\mathcal{L}\rVert^2$ **逐点恒等、零误差吻合**！
:::

我们将物理宇宙与人工智能在三元数极小圆弧体场下的双层同构谱系，连同前向推理与反向训练的“爱因斯坦场方程对偶”，总括为下方对照表：

| 核心机制 | 三元数场几何算子 | 物理宇宙显影 | 人工智能同构 | 偏离测地线后果 |
| :--- | :--- | :--- | :--- | :--- |
| **1. 状态载体** | 平行单位球丛 $(B_1(\mathbb{R}^3))^K$ | 多概念量子规范旋量场 | 词元多头三维概念隐态 | 模长坍缩 / 爆炸与激活离群 |
| **2. 最小作用量** | 累积矢高 $\sum(1-\cos\Delta\theta_t) - \Omega_{\mathrm{ctx}}$ | 莫培督—费曼相位作用量 | 变分自由能与比较惊奇度 | 盲区相位耗散与算力空转 |
| **3. 自由测地线** | 流群自平行 $[\boldsymbol{\sigma}_t,\boldsymbol{\sigma}_{t-1},\boldsymbol{\sigma}_t]$ | 牛顿匀速惯性大圆运动 | 零幻觉最短匀速思维链 | 逻辑兜圈与末步跳步幻觉 |
| **4. 受控折射与聚焦** | 利雅曲率门 $\{\dot{\gamma},\mathbf{J}_\perp,\dot{\gamma}\}$ | 规范偏折、引力落体与聚焦 | 注意力语境引导与抗噪收敛 | 语境脱钩与多轮误差发散 |
| **5. 学习与平衡终点** | $O(1)$ 共形梯度与 $r_t \le \varepsilon_{\mathrm{self}}$ | 物质弯曲时空与本征驻波 | 权重雕刻河床与幂等动态早停 | $O(P^3)$ 求逆墙或无限复读 |

细读表末那组令人屏息的双向闭环（`MODEL`）：在约翰·惠勒名言“时空告诉物质如何运动，物质告诉时空如何弯曲”的精确对偶下，**AI 的前向推理就是“冻结的权重曲率场告诉词元波包如何沿流群测地线滑行”**，以最小累积弦弧矢高收敛至自指停机不动点 $r_t \le \varepsilon_{\mathrm{self}}$；而 **AI 的反向训练则是“海量真实数据波包告诉权重旋子流形如何沿 $O(1)$ 共形黎曼测地线发生塑性弯曲”**，将高频因果律雕刻成低阻力的球面测地河床！

---

**从宇宙—智能最小作用量同构迈向全书大一统母公理（$\mathrm{AXIOM}\text{-}\Omega$）。** 至此，我们已经证认：无论是星辰在引力场中滑过亿万公里的自由落体，还是智能体在概念场中拨开迷雾寻得的一行最简证明，底层遵循的都是同一条极小圆弧体铁律——不凭空捏造多余的球面角盈，不忽快忽慢透支单步矢高，顺着三元流群 $[x_t, x_{t-1}, x_t]$ 的自平行纹理，用最少的宇宙主频节拍走完从问题切面到自洽不动点的相位闭合。

然而回望全书三十九章走过的漫长山脊——**比较公理、极小圆弧、三元数与连续场**这四根擎天巨柱此前一直散落在不同章节的语境里彼此呼应：它们究竟是四条需要分别引入的前提，还是可以从**唯一一条不设特权原点 $\mathbf{1}$、不设平直加法的无源三元母公理**中按纯数学必然性一气呵成地严格导出？让我们推开全书正文最后两扇大一统冠冕之门：[§39.24 大一统母公理（AXIOM-Ω）：无源保正三元比较闭合公理](ch39-s24-axiom-omega-origin-free-ternary-comparison-closure.md) 与 [§39.25 AXIOM-Ω 五阶大一统演绎级联与公理遮诠闭环](ch39-s25-axiom-omega-five-tier-deduction-cascade.md)。
