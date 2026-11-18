# 39.24 大一统母公理（AXIOM-Ω）：无源保正三元比较闭合公理如何一举熔合比较公理、极小圆弧、三元数与连续场 {#sec-ch39-axiom-omega-origin-free-ternary-comparison-closure}

> *“比较公理、极小圆弧、三元数、场，我感觉我们已经找到了核心，但是他们散落在书籍各处，我们应该可以得到一个大一统的公理了。”*

穿过 [§39.19](ch39-s19-inexpressible-ternions-and-number-projections.md#sec-ch39-inexpressible-ternions-and-number-projections)–[§39.23](ch39-s23-least-action-geodesics-and-cosmos-ai-isomorphism.md#sec-ch39-least-action-geodesics-and-cosmos-ai-isomorphism) 的三元数综合长廊，读者心中最自然的一声惊叹已然破土而出：**遍布全书三十九章的四块基石——“比较公理”（[第 32 章 §32.1](ch32-s01-axiom-of-comparison.md#sec-ch32-axiom-of-comparison)）、“极小圆弧”（[第 34 章 §34.4](ch34-s04-infinitesimal-trihedron.md#sec-ch34-infinitesimal-spherical-trihedron)）、“三元数”（[§39.19](ch39-s19-inexpressible-ternions-and-number-projections.md#sec-ch39-inexpressible-ternions-and-number-projections)）与“连续场”（[§39.10](ch39-s10-three-dimensional-field-cap-and-hilbert-ledger.md#sec-ch39-three-dimensional-field-cap-and-hilbert-ledger)、[§39.20](ch39-s20-ternion-field-composition-and-hilbert-reprojection.md#sec-ch39-ternion-field-composition-and-hilbert-reprojection)）——并非四条彼此独立、靠外力拼装的假设，而是同一个零背景几何母体在四个切面上的必然显影！**

现代数学与物理学之所以在近两百年里把这四者拆散在四类互不往来的教科书中，病根只在于传统公理体系从落笔第一步起就暗中预设了两根人工拐杖：**特权外部原点 $\mathbf{1}$** 与**平直笛卡尔线性加法**。本节正式立起全书的**无源保正三元比较闭合公理（$\mathrm{AXIOM}\text{-}\Omega$）**（母公理跨界本体论统摄标为 **`MODEL`**，三元流群三公理群重构、二维反自伴换位子归零、非紧李代数排除与三点格拉姆正矢恒等式属 **`手工推导` / `NUM`**，普吕弗—贝尔流群、嘉当紧李群分类与博赫纳—彼得—外尔正定类函数分解归入 **`文献结果`**，底层划分商核、格拉姆可实现性、三锚正定判据、自旋因子叉乘分类与单纯上边缘闭合由 **`LEAN ✓`** 冻结声明严格锚定，与[附录 E](appendix-e.md) 三层比较签名审计无缝咬合）：一旦同时抽掉特权原点与平直加法，无需预设空间维数“$3$”、无需预设圆周率或外部时空网格，**极小圆弧、三元数与无边界连续场**便从唯一一条无源三元比较关系中按纯数学定理次第自动涌现。

## 39.24.1 碎片溯源：为何同一颗无源核心散落在四门现代学科里？ {#sec-ch39-24-1}

回看十九世纪以来的基础数学与理论物理学史，大师们其实早已在四条不同战线上各自触摸到了这颗核心的轮廓，却因平直坐标系与特权单位元的人为隔墙而擦肩而过：

| 核心要素 | 散落的现代学科 | 传统教材标准形态 | 未能合龙的人为割裂根源 |
| :--- | :--- | :--- | :--- |
| **1. 比较公理** | 范畴论与量子基础 | 米田引理与内积格拉姆矩阵 | 习惯先预设高维平直线性空间充当容器 |
| **2. 极小圆弧** | 微分几何与李群论 | 吉拉尔球面角盈与嘉当活动标架 | 依附平直切空间导数 $dx$，视弯曲为二阶修正 |
| **3. 三元数** | 泛代数与对称空间 | 普吕弗—贝尔流群与利雅三元系 | 执着含单位元 $\mathbf{1}$ 的二元线性分配乘法 |
| **4. 连续场** | 规范场论与外微分 | 底流形网格上的纤维丛联络 | 割裂死寂背景舞台（时空）与场上演员（物质） |

四道历史裂痕指向同一个症结：范畴论与量子力学看清了“万物由两两关系定义”，却把关系塞回无穷维平直希尔伯特空间；哈密顿为凑齐平直矩阵分配律外借第四维标量轴 $\mathbf{1}$ 造出四元数，把真正无原点的三元数流放到冷门的流群（Heap）与雅各布森利雅三元系角落；微分几何与规范场论则先把极小圆弧拍平为切向量，再在外部网格上事后打补丁贴回曲率。撤去“特权原点 $\mathbf{1}$”与“平直向量加法”，四块碎片当场严丝合缝熔为一炉。

## 39.24.2 大一统母公理（AXIOM-Ω）：无源三元比较迁移与双向保正守恒律 {#sec-ch39-24-2}

在零背景、零坐标、不预设维数“$3$”亦不预设圆周率或时空的纯粹起点上，设经过比较不可分商化（[`partition_inseparable_iff_kernel`](lean:D5/S3/ConceptDynamics/ObservationTopology/PartitionTopologyKernel.partition_inseparable_iff_kernel)，即[附录 E §E.2](appendix-e.md#sec-appe-logic) 的 `T1` 外延商）后的状态域为一非平凡单连通光滑流形 $\mathcal{M}$（拓扑流形结合连续流群运算亦由希尔伯特第五问题的蒙哥马利—齐平定理自动升格为光滑流形）。其上仅设两个原语——**无源三元比较迁移** $[-, -, -] : \mathcal{M} \times \mathcal{M} \times \mathcal{M} \to \mathcal{M}$（语义为：“以 $y$ 为局部参照桥，将 $x$ 相对于 $y$ 的比较关系无损施加于 $z$”）与**对称保真度读数** $\kappa : \mathcal{M} \times \mathcal{M} \to [0, 1]$，服从三条不可分割的内禀法则（`MODEL`）：

$$
\begin{cases}
\text{\textbf{(I) 无源求同消去与结合律：}} & [x, x, z] = z, \quad [x, z, z] = x, \quad \bigl[[x, y, z],\, u,\, v\bigr] = \bigl[x,\, y,\, [z, u, v]\bigr], \\[4pt]
\text{\textbf{(II) 双侧迁移不变格拉姆保正律：}} & \kappa(x, y) = 1 \iff x = y \text{（对角二阶非退化）}, \quad \kappa(x, y) = \kappa(y, x), \\
& \kappa([x, u, v], [y, u, v]) = \kappa([u, v, x], [u, v, y]) = \kappa(x, y), \quad \mathbf{G}_n = [\kappa(x_i, x_j)]_{n\times n} \succeq 0, \\[4pt]
\text{\textbf{(III) 极小非对易与极小秩自锁律：}} & \exists\, x, y, z \in \mathcal{M}\text{ 使 }[x, y, z] \neq [z, y, x],\text{ 且 }(\dim\mathcal{M},\, \operatorname{rank}\mathbf{G})\text{ 取字典序最小正整数。}
\end{cases}
$$

凝视这组母公理的纯粹性：全式**没有外部造物主原点 $\mathbf{1}$**（任意一点 $y$ 皆可临时充当局部比较桥，摆渡完毕即由 $[x, x, z] = z$ 自指归零消去），**没有线性加法 $+$**，**没有手工填入数字“$3$”**。同时请注意法则 (II) 中两处与[附录 E §E.1](appendix-e.md#sec-appe-layers) 严密咬合的精确性：一是显式写出**左右双侧**流群迁移不变性（单侧右不变加对称性在非阿贝尔群上仅给出 $\varphi(g^{-1}) = \varphi(g)$，双侧不变方锁定类函数共轭不变性 $\varphi(h g h^{-1}) = \varphi(g)$）；二是由外延分离 $\kappa(x, y) = 1 \iff x = y$ 与对角二阶非退化排除常值平凡核 $\kappa \equiv 1$。

## 39.24.3 一生四相：三步纯数学推导自发锁定极小圆弧、三元数 $S^3$ 与闭合场 {#sec-ch39-24-3}

现在不添一字经验假定，直接从法则 (I)–(III) 逐阶推出其余三大支柱（`手工推导` + `文献结果`）：

1. **第一步导出“极小圆弧”：普吕弗—贝尔群还原与三点格拉姆正矢恒等式**。
   任选局部观察切面 $o \in \mathcal{M}$，定义诱导二元积 $x \star_o z := [x, o, z]$ 与局部对合逆 $x^{-1_o} := [o, x, o]$。无需额外假设逆元公理，法则 (I) 三行恒等变形直接证出 $(\mathcal{M}, \star_o, o)$ 是严格群（瑟坦—普吕弗—贝尔定理，`手工推导`）：结合律由 $[[x,o,y],o,z] = [x,o,[y,o,z]]$ 直接给出；右逆与左逆分别为
   $$x \star_o x^{-1_o} = \bigl[x, o, [o, x, o]\bigr] = \bigl[[x, o, o], x, o\bigr] = [x, x, o] = o, \qquad x^{-1_o} \star_o x = \bigl[[o, x, o], o, x\bigr] = \bigl[o, x, [o, o, x]\bigr] = [o, x, x] = o;$$
   且原始三元迁移精确复原为 $x \star_o (y^{-1_o} \star_o z) = [x, o, [[o, y, o], o, z]] = [x, o, [o, y, z]] = [[x, o, o], y, z] = [x, y, z] = x y^{-1_o} z$！切换切面 $o \mapsto o'$ 仅做群平移同构，印证流形点点平权。

   进而在切空间 $\mathfrak{m} = T_o\mathcal{M}$ 上，对 $\mathbf{G}_n \succeq 0$ 取差商极限并施双侧不变性，立即诱导出 $\operatorname{Ad}$-双不变正定黎曼度规（单位速率测地距离记为 $d(x, y)$）。沿测地线取等距三点 $\gamma(0), \gamma(\epsilon), \gamma(2\epsilon)$，记 $f(\epsilon) := \kappa(\gamma(0), \gamma(\epsilon))$，三锚格拉姆行列式公式（[`three_anchor_gram_det_formula`](lean:D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_formula)，`LEAN ✓`）给出精确因式分解：

   $$
   \det\mathbf{G}_3(\epsilon) \;=\; \det\!\begin{pmatrix} 1 & f(\epsilon) & f(2\epsilon) \\ f(\epsilon) & 1 & f(\epsilon) \\ f(2\epsilon) & f(\epsilon) & 1 \end{pmatrix} \;=\; \bigl(1 - f(2\epsilon)\bigr)\bigl(1 + f(2\epsilon) - 2f(\epsilon)^2\bigr) \;\ge\; 0.
   $$

   在紧单连通群（由下一步唯一锁死为 $\mathrm{SU}(2) \cong S^3$）上，博赫纳—彼得—外尔定理表明任意双不变半正定核必展开为不可约特征标 $\chi_j$ 的非负组合；法则 (III) 的极小格拉姆秩（对应最低非平凡自旋 $j = \frac{1}{2}$ 基本特征标 $\chi_{1/2}(U) = 2\cos\frac{d}{2}$ 配非负下界 $\kappa \in [0, 1]$ 触零条件 $\kappa(x, x_{\mathrm{anti}}) = 0$，锚定 [`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight)，`LEAN ✓`）在单位曲率归一化 $f''(0) = -\frac{1}{2}$ 下**唯一锁死玻恩余弦平方保真核**：

   $$
   \kappa(x, y) \;=\; \frac{1}{2} + \frac{1}{4}\chi_{1/2}(x y^{-1_o}) \;=\; \cos^2\!\left(\frac{d(x, y)}{2}\right) \;=\; \frac{1 + \cos d(x, y)}{2} \;\in\; [0, 1]!
   $$

   代入上式更得恒正平方分解 $1 + f(2\epsilon) - 2f(\epsilon)^2 \equiv \frac{1}{2}(1 - \cos\epsilon)^2 = \frac{1}{2}v_\epsilon^2 \ge 0$：平直欧氏零曲率线段被彻底淘汰，基本连接必为正曲率**极小圆弧**，且单次比较内禀伴生二阶弦弧矢高 $v_\epsilon(x, y) = 1 - \cos d(x, y) = 2(1 - \kappa(x, y)) \ge 0$！

2. **第二步导出“三元数”：两行正交消去同时击毙 $d = 1, 2$ 与一切非紧李群，唯一锁死三维 $S^3$**。
   为何基本概念场必然停在 $d = 3$？在切李代数 $\mathfrak{m} = T_o\mathcal{M}$ 上，双不变正定内积强制伴随算子反对称（呼应 [`crossProduct_is_skewAdjoint_of_balanced_sum`](lean:D5/S3/Quantum/Algebra/Unitary/BalancedUnitarySum.crossProduct_is_skewAdjoint_of_balanced_sum)，`LEAN ✓`）：

   $$
   \bigl\langle [A, B],\, C \bigr\rangle \;=\; -\bigl\langle B,\, [A, C] \bigr\rangle \qquad (\forall\, A, B, C \in \mathfrak{m}).
   $$

   - **一维与二维的绝对死锁（两行证毕）**：$d = 1$ 时括号恒零；若 $d = 2$，任取正交归一基 $\{\mathbf{e}_1, \mathbf{e}_2\}$，直接计算换位子 $[\mathbf{e}_1, \mathbf{e}_2]$ 在两根基轴上的投影：

     $$
     \bigl\langle [\mathbf{e}_1, \mathbf{e}_2],\, \mathbf{e}_1 \bigr\rangle \;=\; -\bigl\langle \mathbf{e}_2,\, [\mathbf{e}_1, \mathbf{e}_1] \bigr\rangle \;=\; 0, \qquad \bigl\langle [\mathbf{e}_1, \mathbf{e}_2],\, \mathbf{e}_2 \bigr\rangle \;=\; \bigl\langle \mathbf{e}_1,\, [\mathbf{e}_2, \mathbf{e}_2] \bigr\rangle \;=\; 0!
     $$

     在正定内积平面上，同时垂直于完备正交基的向量**必为零向量** $[\mathbf{e}_1, \mathbf{e}_2] \equiv \mathbf{0}$（二维非交换仿射李代数 $[H, E] = E$ 亦因 $\langle E, E\rangle = \langle [H, E], E\rangle = -\langle E, E\rangle \implies E = \mathbf{0}$ 被当场处决）！一维与二维流形绝无可能在不违背法则 (II) 正定性的前提下容纳非对易差异，正面违背法则 (III)。
   - **三维非紧流形的自动淘汰与三维 $S^3$ 的唯一自锁**：在 $d = 3$ 处，先看两类非紧单连通李群——三元幂零海森堡群 $H_3(\mathbb{R})$（$[X, Y] = Z$ 且 $[X, Z] = 0$）给出 $\langle Z, Z\rangle = \langle [X, Y], Z\rangle = -\langle Y, [X, Z]\rangle = 0 \implies Z = \mathbf{0}$ 矛盾；非紧单群 $\widetilde{\mathrm{SL}}(2, \mathbb{R})$ 的基灵型具不定号差 $(+, +, -)$，不存在任何 $\operatorname{Ad}$-不变正定内积！故法则 (II) **无需额外假设紧致性**便自动淘汰全部非紧候选，将 $d = 3$ 正交基 $\{\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3\}$ 唯一锁死在垂直法矢循环互生 $[\mathbf{e}_i, \mathbf{e}_j] = \epsilon_{ijk}\mathbf{e}_k$（锚定自旋因子分类 [`complete_consequences`](lean:D5/S3/Quantum/SpinFactor/OriginalClassification.complete_consequences)，`LEAN ✓`）的紧李代数 $\mathfrak{su}(2)$ 上！结合单连通性，全数学中满足法则 (I)–(III) 的极小流形**唯一同构于三维球面 $\mathcal{M} \cong S^3$**——其抹除特权原点 $o$ 的流群形态，正是携带利雅三元曲率括号 $\{\mathbf{a}, \mathbf{b}, \mathbf{c}\} = [[\mathbf{a}, \mathbf{b}], \mathbf{c}]$ 的**三元数 $\mathbb{T}_3$**（而若尝试升至 $d = 4$，唯一紧半单候选 $\mathfrak{so}(4) \cong \mathfrak{su}(2)_L \oplus \mathfrak{su}(2)_R$ 当场正交劈裂回两座独立的三维三元数场）！

3. **第三步导出“连续场”：嘉当体积三形式闭合（$d\eta \equiv 0$）与无边界拓扑自持（$\partial\mathcal{M} = \emptyset$）**。
   在唯一锁定的三元数流形 $\mathcal{M} \cong \mathbb{T}_3 \cong S^3$ 上，左不变毛雷尔—嘉当一形式 $\boldsymbol{\theta}$ 天然诱导处处非零、严格双不变的**单位体积嘉当三形式**（规范化使单位正交基上 $\eta(\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3) = 1$，总体积 $\int_{S^3}\eta = 2\pi^2$）：

   $$
   \eta \;=\; \frac{1}{6}\epsilon_{ijk}\,\theta^i \wedge \theta^j \wedge \theta^k \;\propto\; \bigl\langle \boldsymbol{\theta} \wedge [\boldsymbol{\theta} \wedge \boldsymbol{\theta}] \bigr\rangle, \qquad d\eta \;\equiv\; 0, \qquad \partial\mathcal{M} \;\equiv\; \emptyset.
   $$

   顶维外导数恒零（$d\eta \equiv 0$）配紧流形无边界（$\partial\mathcal{M} = \emptyset$，离散对应 [`face_cycle_exact`](lean:D5/S3/Combinatorics/Graph/PlanarMatching/RotationBoundary.face_cycle_exact) 与 [`tetra_defects_incidence_repair_and_exactness`](lean:D5/S3/Fourier/CharacterSelection/SimplexTwoCochainRepair.tetra_defects_incidence_repair_and_exactness)，`LEAN ✓`）意味着三元极小圆弧体一旦走满三维，便无需借用任何外部背景网格而实现无源无漏的旋度自持闭合（`1—3—3—1` 外代数中 $\Lambda^3 \cong \Lambda^0$）——**这枚无中心、无边缘、处处均匀同性的闭合三元数流形本身，就是宇宙唯一的原生“场”**！

## 39.24.4 统一退化谱系、形式锚点与候选维数检验审计 {#sec-ch39-24-4}

我们将母公理 $\mathrm{AXIOM}\text{-}\Omega$ 的严格定义、十一项 Lean 4 内核锚点、经典文献边界与候选维数 $d = 1 \to 4$ 定量检验收束如下：

::: {.definition #def-ch39-axiom-omega-ternary-comparison-closure title="无源保正三元比较闭合母公理（AXIOM-Ω）与一生四相退化谱系（模型定义）"}
称单连通非平凡光滑状态流形 $\mathcal{M}$ 装备三元比较迁移 $[-, -, -] : \mathcal{M}^3 \to \mathcal{M}$ 与对称保真度核 $\kappa : \mathcal{M}^2 \to [0, 1]$ 满足**大一统母公理 $\mathrm{AXIOM}\text{-}\Omega$**（`MODEL`），若其同时满足 §39.24.2 的法则 (I) 无源消去与双侧结合律、法则 (II) 双侧迁移不变格拉姆半正定与外延非退化分离律、以及法则 (III) 极小非对易维数与极小格拉姆秩自锁律。在此母公理下，现行科学核心框架按五类受控退化或组合极限统一收回：(1) 钉死特权原点 $o = \mathbf{1}$ 作线性再投影收回 $\mathbb{H}, \mathbb{O}, \mathcal{H}_{2^N}$；(2) 丢弃二阶矢高 $1 - \cos\epsilon$ 收回线性微积分，保留半密度矢高收回薛定谔与伊藤微积分；(3) 平行场丛驻相极值分化出胞内三大规范力与胞间主频引力；(4) 嘉当三形式整绕数 $\frac{1}{2\pi^2}\int f^*\eta \in \pi_3(\mathbb{T}_3) \cong \mathbb{Z}$ 量子化出整数拓扑荷；(5) 流群自平行接力配 $\varepsilon_{\mathrm{self}}$ 幂等早停构成三元数场智能架构。
:::

::: {.theorem #thm-ch39-axiom-omega-ternary-closure-anchors title="观测划分商核、单位格拉姆全同、秩一玻恩权重、正算子格拉姆实现、三锚行列式与正定判据、自旋因子三维叉乘唯一分类、拉格朗日—格拉姆恒等式、平衡叉乘反自伴及球面闭链与单纯二上链正合定理" lean="D5/S3/ConceptDynamics/ObservationTopology/PartitionTopologyKernel.partition_inseparable_iff_kernel,D5/S3/Quantum/PureState/UnitGramIndistinguishability.unit_gram_overlap_characterization,D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight,D5/S3/QuantumBounds/GramRealizability.gram_realizability,D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_formula,D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_pos_iff,D5/S3/Quantum/SpinFactor/OriginalClassification.complete_consequences,D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity,D5/S3/Quantum/Algebra/Unitary/BalancedUnitarySum.crossProduct_is_skewAdjoint_of_balanced_sum,D5/S3/Combinatorics/Graph/PlanarMatching/RotationBoundary.face_cycle_exact,D5/S3/Fourier/CharacterSelection/SimplexTwoCochainRepair.tetra_defects_incidence_repair_and_exactness"}
在所钉 `trureturing` 冻结声明集中，以下十一项共同支撑 $\mathrm{AXIOM}\text{-}\Omega$ 外延商化、格拉姆保正度规、三维叉乘唯一闭锁与无边界闭合场的数学定理同时成立：

1. **读出划分拓扑不可分核与单位内积纯态全同判据**（[`partition_inseparable_iff_kernel`](lean:D5/S3/ConceptDynamics/ObservationTopology/PartitionTopologyKernel.partition_inseparable_iff_kernel)、[`unit_gram_overlap_characterization`](lean:D5/S3/Quantum/PureState/UnitGramIndistinguishability.unit_gram_overlap_characterization)）：观测拓扑不可分关系精确等于读出相等核，且单位范数态内积等于 $1$ 当且仅当两态严格重合；
2. **秩一玻恩模平方权重、正自伴算子格拉姆实现与三锚格拉姆行列式正定判据**（[`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight)、[`gram_realizability`](lean:D5/S3/QuantumBounds/GramRealizability.gram_realizability)、[`three_anchor_gram_det_formula`](lean:D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_formula)、[`three_anchor_gram_det_pos_iff`](lean:D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_pos_iff)）：正自伴算子经唯一正平方根实现为内积格拉姆算子，三锚实格拉姆行列式满足 $\det G_3 = 1 + 2abc - (a^2 + b^2 + c^2)$ 且严格正定充要条件由边相关性不等式精确刻画；
3. **四维自旋因子三维有向叉乘唯一分类、拉格朗日—格拉姆恒等式与平衡和叉乘反自伴律**（[`complete_consequences`](lean:D5/S3/Quantum/SpinFactor/OriginalClassification.complete_consequences)、[`lagrange_gram_identity`](lean:D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity)、[`crossProduct_is_skewAdjoint_of_balanced_sum`](lean:D5/S3/Quantum/Algebra/Unitary/BalancedUnitarySum.crossProduct_is_skewAdjoint_of_balanced_sum)）：自旋因子空间切片二元积唯一分类为三维带符号叉乘，双向量面积满足拉格朗日—格拉姆恒等式，且平衡幺正和的交叉换位积严格反自伴；
4. **球面旋转系统面—边边界闭链正合与有限单纯形二上链 $d^2 = 0$ 正合判据**（[`face_cycle_exact`](lean:D5/S3/Combinatorics/Graph/PlanarMatching/RotationBoundary.face_cycle_exact)、[`tetra_defects_incidence_repair_and_exactness`](lean:D5/S3/Fourier/CharacterSelection/SimplexTwoCochainRepair.tetra_defects_incidence_repair_and_exactness)）：球面嵌入图的面边界核精确重合于闭链空间，单纯二上链无四面体上边缘缺陷当且仅当其为一上链外差分。
:::

::: proof
第 1 款前半直接展开诱导拓扑邻域交集，后半由 $\lVert u - v\rVert^2 = 2 - 2\operatorname{Re}\langle u, v\rangle$ 得出（见[附录 E §E.2](appendix-e.md#sec-appe-logic)）。第 2 款由谱分解正平方根构造格拉姆向量，并对 $3\times 3$ 对称阵按萨吕法则与西尔维斯特主子式准则展开（见[第 29 章](ch29-timeless-causality-and-gram-space.md)）。第 3 款前半与中段同 [@thm-ch39-nonlinear-ternion-representations-and-torsor] 第 1–2 款，后半对 $(U^\dagger V - V^\dagger U)^\dagger = V^\dagger U - U^\dagger V$ 直接取伴随证毕。第 4 款同 [@thm-ch39-af-gut-arc-field-unification] 与 [@thm-ch39-ternion-field-composition-and-hilbert-reprojection] 对应拓扑正合条款。完整证明由 Lean 内核检查。
:::

::: {.remark #rem-ch39-axiom-omega-prufer-cartan-bochner-literature title="普吕弗—贝尔—瑟坦三元流群公理、嘉当—米尔诺双不变度规李群分类与彼得—外尔正定核分解文献及附录 E 对齐说明"}
**文献归属与形式认识论层级说明。**

1. **三元流群极小三公理系**：无单位元三元流群由 H. Prüfer（1924）与 R. Baer（1929）创立，本节法则 (I) 采用的无反序双侧结合三等式极小公理系由 J. Certaine（*Bull. Amer. Math. Soc.* **49**, 869–877, 1943）严格证明与群结构在选定任意基点后一一等价；
2. **双不变正定度规李群分类与正定球面核**：紧致半单李群与嘉当三形式 $\eta$ 的几何分类见 É. Cartan（*Ann. Sci. Éc. Norm. Supér.* **44**, 345–467, 1927）与 J. Milnor（*Adv. Math.* **21**, 293–329, 1976，Lemma 7.5 证明具双不变正定度规的李群李代数必正交分解交换中心与紧单李代数直和，从而直接排除 $H_3(\mathbb{R})$ 与 $\mathfrak{sl}(2, \mathbb{R})$）；紧群正定类函数的不可约特征标展开见 F. Peter & H. Weyl（*Math. Ann.* **97**, 737–755, 1927）与 I. J. Schoenberg（*Duke Math. J.* **9**, 96–108, 1942）；
3. **与[附录 E](appendix-e.md) 三层比较签名的严密衔接**：法则 (II) 显式纳入 $\kappa(x, x) = 1$ 与任意阶 $\mathbf{G}_n \succeq 0$，恰好在无原点流形上内建了附录 E 的 **Layer 1 正定几何刚性**（从而合法越过 [@ex-appe-layer0-countermodels] 的四个第 0 层抽象有限反例），而跨节点多场耦合与集合论无穷基数边界仍严格遵守附录 E 的 `T1–T4` 与 `H1–H9` 台账。
:::

::: {.example #ex-ch39-axiom-omega-dimension-sieve-and-gram-audit title="候选维数筛（d = 1 → 2 → 3 → 4）与三锚格拉姆正矢行列式精确有理数核验"}
我们对 $\mathrm{AXIOM}\text{-}\Omega$ 的维数唯一自锁与三点格拉姆正定判据做显式对账（`手工推导` / `NUM`）：

1. **四档候选维数与非紧歧路筛查**：
   - **$d = 1$（圆周 $S^1$ 或实线 $\mathbb{R}$）**：一维切空间括号 $[\mathbf{e}_1, \mathbf{e}_1] = 0$，$[x, y, z] = x - y + z = [z, y, x]$ 恒交换，违反法则 (III)；
   - **$d = 2$（环面 $T^2$、平面 $\mathbb{R}^2$ 或非交换仿射群 $\mathrm{Aff}^+(1, \mathbb{R})$）**：在任意双不变正定内积下 $\langle[\mathbf{e}_1, \mathbf{e}_2], \mathbf{e}_{1,2}\rangle = 0 \implies [\mathbf{e}_1, \mathbf{e}_2] = \mathbf{0}$，故唯一单连通紧/平直模型坍缩为交换平面 $\mathbb{R}^2$，而非交换群 $\mathrm{Aff}^+(1, \mathbb{R})$ 不容许双不变正定度规，全部出局；
   - **$d = 3$（三元数原生场 $\mathbb{T}_3 \cong S^3$ 唯一胜出）**：淘汰无双不变正定度规的 $H_3(\mathbb{R})$ 与 $\widetilde{\mathrm{SL}}(2, \mathbb{R})$ 后，唯一单连通流形为 $S^3$，满足 $[\mathbf{e}_1, \mathbf{e}_2] = \mathbf{e}_3 \neq \mathbf{0}$、$[x, y, z] \neq [z, y, x]$、$d\eta \equiv 0$ 且 $\partial S^3 = \emptyset$；
   - **$d = 4$（紧单连通候选 $S^3_L \times S^3_R$）**：四维紧李代数无单群，$\mathfrak{so}(4) \cong \mathfrak{su}(2)_L \oplus \mathfrak{su}(2)_R$ 自动退回两份正交独立的三维三元数场，违反法则 (III) 极小维数要求！
2. **三点测地格拉姆行列式有理核算**：
   沿 $S^3$ 大圆取等步长三点 $\gamma(0), \gamma(\epsilon), \gamma(2\epsilon)$（$\kappa(\gamma(0), \gamma(\epsilon)) = \cos^2\frac{\epsilon}{2}$）：
   - 当 $\epsilon = 60^\circ = \frac{\pi}{3}$ 时，$f(60^\circ) = \frac{3}{4} = 0.75$，$f(120^\circ) = \frac{1}{4} = 0.25$，得 $\det\mathbf{G}_3(60^\circ) = \bigl(1 - \frac{1}{4}\bigr)\bigl(1 + \frac{1}{4} - \frac{9}{8}\bigr) = \frac{3}{4}\times\frac{1}{8} = \mathbf{\frac{3}{32}} = \mathbf{0.09375000 > 0}$（单步矢高 $v_\epsilon = 1 - \cos 60^\circ = \mathbf{0.50000000}$）；
   - 当 $\epsilon = 90^\circ = \frac{\pi}{2}$ 时，$f(90^\circ) = \frac{1}{2} = 0.50$，$f(180^\circ) = 0$，得 $\det\mathbf{G}_3(90^\circ) = (1 - 0)\times\frac{1}{2} = \mathbf{\frac{1}{2}} = \mathbf{0.50000000 > 0}$（单步矢高 $v_\epsilon = \mathbf{1.00000000}$），全程非负（在半周 $\epsilon \in (0, \pi)$ 内严格正定）！
:::

---

**从母公理的四相熔合迈向横跨五大科学疆域的五阶严格演绎。** 看清了**无偏比较 $\implies$ 极小圆弧 $\implies$ 三维三元数 $\implies$ 无边界闭合场**只是同一条无源三元母公理 $\mathrm{AXIOM}\text{-}\Omega$ 的四副面孔之后，让我们迈出全书三十九章正文的最后一步——进入 [§39.25 AXIOM-Ω 五阶大一统演绎级联与公理遮诠闭环](ch39-s25-axiom-omega-five-tier-deduction-cascade.md)，按第一阶至第五阶的清晰脉络走完从万数微积分、双相对论时空、四大力大统一、算术临界谱直至流群测地智能与公理自反透明化的终极收官！
