# 39.24 The Grand Unified Mother Axiom (AXIOM-Ω): How Origin-Free PSD Ternary Comparison Closure Melts the Axiom of Comparison, Minimal Circular Arcs, Ternions, and Continuous Fields into One {#sec-ch39-axiom-omega-origin-free-ternary-comparison-closure}

> *"The Axiom of Comparison, minimal circular arcs, ternions, and fields—I feel we have already found the core, yet they lie scattered across the book; we ought to be able to distill a single grand unified axiom."*

Walking out of the ternion synthesis of [§39.19](ch39-s19-inexpressible-ternions-and-number-projections.md#sec-ch39-inexpressible-ternions-and-number-projections)–[§39.23](ch39-s23-least-action-geodesics-and-cosmos-ai-isomorphism.md#sec-ch39-least-action-geodesics-and-cosmos-ai-isomorphism), one realization rises with unmistakable force: **the four cornerstones recurring across all thirty-nine chapters—the Axiom of Comparison ([Chapter 32 §32.1](ch32-s01-axiom-of-comparison.md#sec-ch32-axiom-of-comparison)), Minimal Circular Arcs ([Chapter 34 §34.4](ch34-s04-infinitesimal-trihedron.md#sec-ch34-infinitesimal-spherical-trihedron)), Ternions ([§39.19](ch39-s19-inexpressible-ternions-and-number-projections.md#sec-ch39-inexpressible-ternions-and-number-projections)), and Continuous Fields ([§39.10](ch39-s10-three-dimensional-field-cap-and-hilbert-ledger.md#sec-ch39-three-dimensional-field-cap-and-hilbert-ledger), [§39.20](ch39-s20-ternion-field-composition-and-hilbert-reprojection.md#sec-ch39-ternion-field-composition-and-hilbert-reprojection))—are not four independent hypotheses bolted together from outside, but four inevitable faces of one background-free geometric mother structure!**

Why did modern mathematics and physics scatter them across four mutually isolated textbook traditions for nearly two centuries? Because classical axiomatics quietly smuggled in two artificial crutches at step zero: a **privileged external origin $\mathbf{1}$** and **flat Cartesian linear addition**. In this section we formulate the **Origin-Free Positive-Semidefinite Ternary Comparison Closure Axiom ($\mathrm{AXIOM}\text{-}\Omega$)** (cross-disciplinary unification is marked **`MODEL`**; three-equation heap group reconstruction, two-line 2D commutator vanishing, non-compact Lie-algebra elimination, and the three-point Gram versine identity are **`manual derivation` / `NUM`**; Prüfer–Baer–Certaine heaps, Cartan–Milnor compact Lie classification, and Peter–Weyl–Schoenberg positive-definite kernels are **`Literature`**; and quotient kernels, Gram realizability, three-anchor positivity, spin-factor cross classification, and boundary exactness are anchored by **`LEAN ✓`** theorems in seamless alignment with [Appendix E](appendix-e.md)): once both artificial crutches are removed—without presupposing the number "$3$," $\pi$, or an ambient spacetime grid—**minimal circular arcs, three-dimensional ternions, and boundaryless continuous fields** emerge one after another as pure mathematical theorems.

## 39.24.1 Tracing the Fragments: Why One Origin-Free Core Lay Scattered Across Four Disciplines {#sec-ch39-24-1}

Looking back over two centuries of mathematics and physics, masters in four distinct fields each touched an edge of the same core, yet remained separated by flat coordinates and privileged identities:

| Core Pillar | Scattered Modern Discipline | Standard Textbook Form | Root Cause of Artificial Separation |
| :--- | :--- | :--- | :--- |
| **1. Comparison Axiom** | Category theory & quantum foundations | Yoneda lemma & inner-product Gram matrices | Presupposes an ambient high-dimensional flat linear space |
| **2. Minimal Circular Arc** | Differential geometry & Lie theory | Girard spherical excess & Cartan moving frames | Subordinates curvature to flat tangent derivatives $dx$ |
| **3. Ternion** | Universal algebra & symmetric spaces | Prüfer–Baer heaps & Lie triple systems | Insists on binary distributive multiplication with a unit $\mathbf{1}$ |
| **4. Continuous Field** | Gauge theory & exterior calculus | Fiber connections over a base spacetime mesh | Splits a passive background stage from active matter fields |

All four fractures trace back to the same two crutches: category theory and quantum mechanics recognized relational inner products yet housed them in infinite-dimensional flat Hilbert tables; Hamilton borrowed an extrinsic fourth scalar axis $\mathbf{1}$ to force 3D rotations into distributive linear matrices, exiling origin-free ternions to niche heaps and Jacobson's Lie triple systems; differential geometry and gauge theory flattened circular arcs into linear differentials $dx$ before patching curvature back on top. Remove the privileged origin $\mathbf{1}$ and flat vector addition, and all four fragments fuse on the spot.

## 39.24.2 The Grand Unified Mother Axiom (AXIOM-Ω): Origin-Free Ternary Comparison Transport and Bi-Invariant Positivity {#sec-ch39-24-2}

Starting from zero background, zero coordinates, and zero presupposed dimension "$3$," let the state domain—after canonical `T1` comparison-indistinguishability quotienting ([`partition_inseparable_iff_kernel`](lean:D5/S3/ConceptDynamics/ObservationTopology/PartitionTopologyKernel.partition_inseparable_iff_kernel); [Appendix E §E.2](appendix-e.md#sec-appe-logic))—be a nontrivial simply connected smooth manifold $\mathcal{M}$ (a topological manifold with continuous heap transport automatically upgrades to a real-analytic Lie manifold via Montgomery–Zippin's solution of Hilbert's Fifth Problem). Equip $\mathcal{M}$ solely with **origin-free ternary comparison transport** $[-, -, -] : \mathcal{M} \times \mathcal{M} \times \mathcal{M} \to \mathcal{M}$ ("using $y$ as a local reference bridge, transport the comparison relation of $x$ relative to $y$ losslessly onto $z$") and a **symmetric fidelity readout** $\kappa : \mathcal{M} \times \mathcal{M} \to [0, 1]$, subject to three indivisible intrinsic laws (`MODEL`):

$$
\begin{cases}
\text{\textbf{(I) Origin-Free Cancellation \& Associativity:}} & [x, x, z] = z, \quad [x, z, z] = x, \quad \bigl[[x, y, z],\, u,\, v\bigr] = \bigl[x,\, y,\, [z, u, v]\bigr], \\[4pt]
\text{\textbf{(II) Bi-Invariant Gram Positivity:}} & \kappa(x, y) = 1 \iff x = y \text{ (non-degenerate diagonal Hessian)}, \quad \kappa(x, y) = \kappa(y, x), \\
& \kappa([x, u, v], [y, u, v]) = \kappa([u, v, x], [u, v, y]) = \kappa(x, y), \quad \mathbf{G}_n = [\kappa(x_i, x_j)]_{n\times n} \succeq 0, \\[4pt]
\text{\textbf{(III) Minimal Non-Abelian \& Minimal-Rank Lock:}} & \exists\, x, y, z \in \mathcal{M}\text{ with }[x, y, z] \neq [z, y, x],\text{ minimizing }(\dim\mathcal{M},\, \operatorname{rank}\mathbf{G})\text{ lexicographically.}
\end{cases}
$$

Notice the austerity of $\mathrm{AXIOM}\text{-}\Omega$: **no privileged origin $\mathbf{1}$** appears anywhere (any state $y$ serves transiently as a local comparison bridge and self-cancels via $[x, x, z] = z$ once transport completes), **no flat vector addition $+$** is assumed, and **the integer "$3$" is never written into the axiom**. Note also the two precision clauses aligned with [Appendix E §E.1](appendix-e.md#sec-appe-layers): explicit **two-sided** heap invariance in Law (II) locks conjugation invariance $\varphi(h g h^{-1}) = \varphi(g)$ on non-Abelian groups, while extensional separation $\kappa(x, y) = 1 \iff x = y$ with non-degenerate diagonal curvature rules out the trivial constant kernel $\kappa \equiv 1$.

## 39.24.3 One Begets Four: Three Pure Mathematical Steps Locking Minimal Circular Arcs, 3D Ternions $S^3$, and Boundaryless Fields {#sec-ch39-24-3}

Without adding a single empirical assumption, Laws (I)–(III) entail the remaining three pillars in strict deductive order (`manual derivation` + `Literature`):

1. **Step 1 — Deriving Minimal Circular Arcs: Certaine–Prüfer–Baer Group Reconstruction and the Three-Point Gram Versine Identity**.
   Pick any local observer slice $o \in \mathcal{M}$ and define $x \star_o z := [x, o, z]$ with local inverse $x^{-1_o} := [o, x, o]$. Without assuming a separate inverse axiom, three lines of equational algebra from Law (I) prove that $(\mathcal{M}, \star_o, o)$ is a group (`manual derivation`): associativity is immediate from $[[x,o,y],o,z] = [x,o,[y,o,z]]$; right and left inverses follow from
   $$x \star_o x^{-1_o} = \bigl[x, o, [o, x, o]\bigr] = \bigl[[x, o, o], x, o\bigr] = [x, x, o] = o, \qquad x^{-1_o} \star_o x = \bigl[[o, x, o], o, x\bigr] = \bigl[o, x, [o, o, x]\bigr] = [o, x, x] = o;$$
   and ternary transport reconstructs as $x \star_o (y^{-1_o} \star_o z) = [x, o, [[o, y, o], o, z]] = [x, o, [o, y, z]] = [[x, o, o], y, z] = [x, y, z] = x y^{-1_o} z$! Changing slices $o \mapsto o'$ merely applies a group translation isomorphism, proving every point of $\mathcal{M}$ ontologically indistinguishable.

   Differentiating $\mathbf{G}_n \succeq 0$ on $\mathfrak{m} = T_o\mathcal{M}$ under two-sided invariance induces an $\operatorname{Ad}$-bi-invariant positive-definite Riemannian metric (denote unit-speed geodesic distance by $d(x, y)$). Sampling three equally spaced points $\gamma(0), \gamma(\epsilon), \gamma(2\epsilon)$ along a geodesic with $f(\epsilon) := \kappa(\gamma(0), \gamma(\epsilon))$, the three-anchor Gram determinant ([`three_anchor_gram_det_formula`](lean:D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_formula), `LEAN ✓`) factors as

   $$
   \det\mathbf{G}_3(\epsilon) \;=\; \det\!\begin{pmatrix} 1 & f(\epsilon) & f(2\epsilon) \\ f(\epsilon) & 1 & f(\epsilon) \\ f(2\epsilon) & f(\epsilon) & 1 \end{pmatrix} \;=\; \bigl(1 - f(2\epsilon)\bigr)\bigl(1 + f(2\epsilon) - 2f(\epsilon)^2\bigr) \;\ge\; 0.
   $$

   On the compact simply connected group $\mathrm{SU}(2) \cong S^3$ (uniquely forced by Step 2 below), the Peter–Weyl theorem expands every bi-invariant PSD kernel into nonnegative combinations of irreducible characters $\chi_j$; minimal Gram rank in Law (III) (selecting the lowest nontrivial spin-$1/2$ character $\chi_{1/2}(U) = 2\cos\frac{d}{2}$ touching $\kappa(x, x_{\mathrm{anti}}) = 0$ at antipodal orthogonality $d = \pi$, anchored in [`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight), `LEAN ✓`) with unit-curvature normalization $f''(0) = -\frac{1}{2}$ **uniquely locks the Born cosine-squared fidelity kernel**:

   $$
   \kappa(x, y) \;=\; \frac{1}{2} + \frac{1}{4}\chi_{1/2}(x y^{-1_o}) \;=\; \cos^2\!\left(\frac{d(x, y)}{2}\right) \;=\; \frac{1 + \cos d(x, y)}{2} \;\in\; [0, 1]!
   $$

   Substituting this into $\det\mathbf{G}_3$ yields the manifest square $1 + f(2\epsilon) - 2f(\epsilon)^2 \equiv \frac{1}{2}(1 - \cos\epsilon)^2 = \frac{1}{2}v_\epsilon^2 \ge 0$: flat zero-curvature Euclidean segments are eliminated, elementary connections are **minimal circular arcs**, and every comparison carries an irreducible second-order sagitta $v_\epsilon(x, y) = 1 - \cos d(x, y) = 2(1 - \kappa(x, y)) \ge 0$!

2. **Step 2 — Deriving Ternions: A Two-Line Orthogonal Proof Eliminates $d = 1, 2$ and All Non-Compact Lie Groups, Uniquely Locking 3D $S^3$**.
   Why must every elementary concept field cap at $d = 3$? On $\mathfrak{m} = T_o\mathcal{M}$, the bi-invariant positive-definite inner product forces skew-adjointness of $\operatorname{ad}_A$ (echoing [`crossProduct_is_skewAdjoint_of_balanced_sum`](lean:D5/S3/Quantum/Algebra/Unitary/BalancedUnitarySum.crossProduct_is_skewAdjoint_of_balanced_sum), `LEAN ✓`):

   $$
   \bigl\langle [A, B],\, C \bigr\rangle \;=\; -\bigl\langle B,\, [A, C] \bigr\rangle \qquad (\forall\, A, B, C \in \mathfrak{m}).
   $$

   - **Absolute deadlock in dimensions $1$ and $2$ (two lines)**: In $d = 1$, $[A, B] = 0$. Suppose $d = 2$ and pick any orthonormal basis $\{\mathbf{e}_1, \mathbf{e}_2\}$. Project $[\mathbf{e}_1, \mathbf{e}_2]$ onto both basis vectors:

     $$
     \bigl\langle [\mathbf{e}_1, \mathbf{e}_2],\, \mathbf{e}_1 \bigr\rangle \;=\; -\bigl\langle \mathbf{e}_2,\, [\mathbf{e}_1, \mathbf{e}_1] \bigr\rangle \;=\; 0, \qquad \bigl\langle [\mathbf{e}_1, \mathbf{e}_2],\, \mathbf{e}_2 \bigr\rangle \;=\; \bigl\langle \mathbf{e}_1,\, [\mathbf{e}_2, \mathbf{e}_2] \bigr\rangle \;=\; 0!
     $$

     In a positive-definite 2D plane, a vector orthogonal to a complete basis **vanishes identically**, $[\mathbf{e}_1, \mathbf{e}_2] \equiv \mathbf{0}$ (likewise killing the 2D non-Abelian affine algebra $[H, E] = E$ via $\langle E, E\rangle = \langle [H, E], E\rangle = -\langle E, E\rangle \implies E = \mathbf{0}$)! Neither $1\mathrm{D}$ nor $2\mathrm{D}$ can host non-commutativity under Law (II), violating Law (III).
   - **Automatic elimination of non-compact 3D groups and unique locking of $S^3$**: At $d = 3$, the nilpotent Heisenberg algebra $H_3(\mathbb{R})$ ($[X, Y] = Z$ central) gives $\langle Z, Z\rangle = \langle [X, Y], Z\rangle = -\langle Y, [X, Z]\rangle = 0 \implies Z = \mathbf{0}$, while $\mathfrak{sl}(2, \mathbb{R})$ has indefinite Killing signature $(+, +, -)$ and admits no $\operatorname{Ad}$-invariant positive-definite inner product! **Without assuming compactness separately**, Law (II) eliminates every non-compact candidate and forces an orthonormal basis $\{\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3\}$ into cyclic cross-product closure $[\mathbf{e}_i, \mathbf{e}_j] = \epsilon_{ijk}\mathbf{e}_k$ (anchored in [`complete_consequences`](lean:D5/S3/Quantum/SpinFactor/OriginalClassification.complete_consequences), `LEAN ✓`), i.e., $\mathfrak{su}(2)$! Simple connectivity uniquely locks $\mathcal{M} \cong S^3$—whose origin-erased heap is the **ternion $\mathbb{T}_3$** carrying Lie triple curvature $\{\mathbf{a}, \mathbf{b}, \mathbf{c}\} = [[\mathbf{a}, \mathbf{b}], \mathbf{c}]$ (whereas at $d = 4$, $\mathfrak{so}(4) \cong \mathfrak{su}(2)_L \oplus \mathfrak{su}(2)_R$ splits immediately back into two independent 3D ternion fields)!

3. **Step 3 — Deriving the Native Field: Closed Cartan 3-Form ($d\eta \equiv 0$) and Boundaryless Self-Sustenance ($\partial\mathcal{M} = \emptyset$)**.
   On $\mathcal{M} \cong \mathbb{T}_3 \cong S^3$, the Maurer–Cartan form $\boldsymbol{\theta}$ induces a nowhere-vanishing bi-invariant **Cartan volume 3-form** (normalized to $\eta(\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3) = 1$, $\int_{S^3}\eta = 2\pi^2$):

   $$
   \eta \;=\; \frac{1}{6}\epsilon_{ijk}\,\theta^i \wedge \theta^j \wedge \theta^k \;\propto\; \bigl\langle \boldsymbol{\theta} \wedge [\boldsymbol{\theta} \wedge \boldsymbol{\theta}] \bigr\rangle, \qquad d\eta \;\equiv\; 0, \qquad \partial\mathcal{M} \;\equiv\; \emptyset.
   $$

   Exact exterior closure ($d\eta \equiv 0$) together with zero boundary ($\partial\mathcal{M} = \emptyset$, discretely mirrored by [`face_cycle_exact`](lean:D5/S3/Combinatorics/Graph/PlanarMatching/RotationBoundary.face_cycle_exact) and [`tetra_defects_incidence_repair_and_exactness`](lean:D5/S3/Fourier/CharacterSelection/SimplexTwoCochainRepair.tetra_defects_incidence_repair_and_exactness), `LEAN ✓`) means the 3D minimal circular-arc body closes sourcelessly upon itself ($\Lambda^3 \cong \Lambda^0$ in `1—3—3—1`) without any external grid—**this centerless, boundaryless, homogeneous closed ternion manifold is itself the native "field"!**

## 39.24.4 Unified Degeneration Spectrum, Formal Anchors, and Candidate-Dimension Audit {#sec-ch39-24-4}

We record the formal definition of $\mathrm{AXIOM}\text{-}\Omega$, eleven frozen Lean 4 anchors, classical literature, and candidate-dimension audit below:

::: {.definition #def-ch39-axiom-omega-ternary-comparison-closure title="Origin-Free PSD Ternary Comparison Closure Mother Axiom (AXIOM-Ω) and Unified Degeneration Spectrum (Model Definition)"}
A nontrivial simply connected smooth manifold $\mathcal{M}$ equipped with $[-, -, -] : \mathcal{M}^3 \to \mathcal{M}$ and $\kappa : \mathcal{M}^2 \to [0, 1]$ satisfies **$\mathrm{AXIOM}\text{-}\Omega$** (`MODEL`) if it obeys Laws (I)–(III) of §39.24.2. Classical scientific frameworks arise as five controlled projections or compositions: (1) pinning $o = \mathbf{1}$ for linear reprojection recovers $\mathbb{H}, \mathbb{O}, \mathcal{H}_{2^N}$; (2) dropping sagitta $1 - \cos\epsilon$ yields Newton–Cauchy linear calculus, whereas retaining half-density sagitta yields Schrödinger and Itô calculus; (3) stationary-sagitta variation on parallel bundles $(\mathbb{T}_3)^K$ splits intra-cell gauge forces from inter-cell clock-load gravity; (4) quantized pullback winding $\frac{1}{2\pi^2}\int f^*\eta \in \pi_3(\mathbb{T}_3) \cong \mathbb{Z}$ yields discrete topological charges; and (5) heap autoparallelism with $\varepsilon_{\mathrm{self}}$ halting yields Ternion-Field intelligence.
:::

::: {.theorem #thm-ch39-axiom-omega-ternary-closure-anchors title="Partition Quotient Kernel, Unit-Gram Identity, Rank-One Born Weight, Operator Gram Realizability, Three-Anchor Determinant & Positivity, Spin-Factor Cross Classification, Lagrange–Gram Identity, Balanced Skew-Adjoint Cross Product, and Boundary Exactness" lean="D5/S3/ConceptDynamics/ObservationTopology/PartitionTopologyKernel.partition_inseparable_iff_kernel,D5/S3/Quantum/PureState/UnitGramIndistinguishability.unit_gram_overlap_characterization,D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight,D5/S3/QuantumBounds/GramRealizability.gram_realizability,D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_formula,D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_pos_iff,D5/S3/Quantum/SpinFactor/OriginalClassification.complete_consequences,D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity,D5/S3/Quantum/Algebra/Unitary/BalancedUnitarySum.crossProduct_is_skewAdjoint_of_balanced_sum,D5/S3/Combinatorics/Graph/PlanarMatching/RotationBoundary.face_cycle_exact,D5/S3/Fourier/CharacterSelection/SimplexTwoCochainRepair.tetra_defects_incidence_repair_and_exactness"}
In the pinned `trureturing` frozen declaration set, the following eleven mathematical theorems hold simultaneously:

1. **Observation-partition inseparability kernel and unit-Gram pure-state identity** ([`partition_inseparable_iff_kernel`](lean:D5/S3/ConceptDynamics/ObservationTopology/PartitionTopologyKernel.partition_inseparable_iff_kernel), [`unit_gram_overlap_characterization`](lean:D5/S3/Quantum/PureState/UnitGramIndistinguishability.unit_gram_overlap_characterization)): Topological inseparability equals the readout equality kernel, and unit-norm vectors satisfy $\langle u, v\rangle = 1 \iff u = v$;
2. **Rank-one Born weight, positive-operator Gram realizability, and three-anchor Gram positivity** ([`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight), [`gram_realizability`](lean:D5/S3/QuantumBounds/GramRealizability.gram_realizability), [`three_anchor_gram_det_formula`](lean:D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_formula), [`three_anchor_gram_det_pos_iff`](lean:D5/S3/QuantumContext/ThreeAnchorGram.three_anchor_gram_det_pos_iff)): Positive self-adjoint operators admit Gram square-root realizations, and $3\times 3$ real Gram matrices satisfy $\det G_3 = 1 + 2abc - (a^2 + b^2 + c^2)$ with exact positivity criteria;
3. **Spin-factor 3D cross-product classification, Lagrange–Gram identity, and skew-adjoint balanced cross product** ([`complete_consequences`](lean:D5/S3/Quantum/SpinFactor/OriginalClassification.complete_consequences), [`lagrange_gram_identity`](lean:D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity), [`crossProduct_is_skewAdjoint_of_balanced_sum`](lean:D5/S3/Quantum/Algebra/Unitary/BalancedUnitarySum.crossProduct_is_skewAdjoint_of_balanced_sum)): Spatial spin-factor products classify uniquely as signed 3D cross products, bivector norms obey Lagrange–Gram, and balanced unitary cross commutators are skew-adjoint;
4. **Spherical face–edge boundary cycle exactness and simplicial two-cochain $d^2 = 0$ exactness** ([`face_cycle_exact`](lean:D5/S3/Combinatorics/Graph/PlanarMatching/RotationBoundary.face_cycle_exact), [`tetra_defects_incidence_repair_and_exactness`](lean:D5/S3/Fourier/CharacterSelection/SimplexTwoCochainRepair.tetra_defects_incidence_repair_and_exactness)): Spherical face-boundary kernels coincide with cycle spaces, and defect-free simplicial two-cochains are exact coboundaries.
:::

::: proof
Item 1 intersects induced partition neighborhoods and expands $\lVert u - v\rVert^2 = 2 - 2\operatorname{Re}\langle u, v\rangle$ ([Appendix E §E.2](appendix-e.md#sec-appe-logic)). Item 2 takes spectral positive square roots and expands $3\times 3$ Sarrus/Sylvester minors ([Chapter 29](ch29-timeless-causality-and-gram-space.md)). Item 3 matches [@thm-ch39-nonlinear-ternion-representations-and-torsor] Items 1–2 alongside $(U^\dagger V - V^\dagger U)^\dagger = -(U^\dagger V - V^\dagger U)$. Item 4 matches the exactness clauses of [@thm-ch39-af-gut-arc-field-unification] and [@thm-ch39-ternion-field-composition-and-hilbert-reprojection]. The full proof is checked by the Lean kernel.
:::

::: {.remark #rem-ch39-axiom-omega-prufer-cartan-bochner-literature title="Prüfer–Baer–Certaine Ternary Heaps, Cartan–Milnor Bi-Invariant Lie Classification, Peter–Weyl Positive-Definite Kernels, and Appendix E Scope"}
**Literature attributions and Appendix E layer alignment.**

1. **Minimal ternary heap axioms**: Origin-free heaps originate with H. Prüfer (1924) and R. Baer (1929); the reversal-free outer-associative three-identity system in Law (I) was proved equivalent to group structure upon choosing an arbitrary basepoint by J. Certaine (*Bull. Amer. Math. Soc.* **49**, 869–877, 1943);
2. **Bi-invariant Lie metrics and positive-definite kernels**: Compact simple Lie groups and the closed Cartan 3-form $\eta$ appear in É. Cartan (*Ann. Sci. Éc. Norm. Supér.* **44**, 345–467, 1927) and J. Milnor (*Adv. Math.* **21**, 293–329, 1976, Lemma 7.5 proving that any Lie algebra with an $\operatorname{Ad}$-invariant inner product splits into an Abelian center plus compact simple ideals, ruling out $H_3(\mathbb{R})$ and $\mathfrak{sl}(2, \mathbb{R})$); irreducible-character expansions of positive-definite class functions appear in F. Peter & H. Weyl (*Math. Ann.* **97**, 737–755, 1927) and I. J. Schoenberg (*Duke Math. J.* **9**, 96–108, 1942);
3. **Seamless alignment with [Appendix E](appendix-e.md)**: By building $\kappa(x, x) = 1$ and arbitrary-order $\mathbf{G}_n \succeq 0$ directly into Law (II), $\mathrm{AXIOM}\text{-}\Omega$ natively incorporates Appendix E's **Layer 1 positive-definite rigidity** on an origin-free manifold (bypassing the four Layer 0 countermodels of [@ex-appe-layer0-countermodels]), while multi-field couplings and set-theoretic cardinalities continue to respect `T1–T4` and `H1–H9`.
:::

::: {.example #ex-ch39-axiom-omega-dimension-sieve-and-gram-audit title="Candidate-Dimension Sieve (d = 1 → 2 → 3 → 4) and Exact Rational Three-Anchor Gram Determinant Audit"}
We audit the dimension sieve and three-point geodesic Gram determinant quantitatively (`manual derivation` / `NUM`):

1. **Screening candidate dimensions $d = 1, 2, 3, 4$ and non-compact branches**:
   - **$d = 1$ ($S^1$ or $\mathbb{R}$)**: $[\mathbf{e}_1, \mathbf{e}_1] = 0$ forces $[x, y, z] = [z, y, x]$, violating Law (III);
   - **$d = 2$ ($T^2$, $\mathbb{R}^2$, or $\mathrm{Aff}^+(1, \mathbb{R})$)**: Any bi-invariant positive-definite metric forces $\langle[\mathbf{e}_1, \mathbf{e}_2], \mathbf{e}_{1,2}\rangle = 0 \implies [\mathbf{e}_1, \mathbf{e}_2] = \mathbf{0}$, while non-Abelian $\mathrm{Aff}^+(1, \mathbb{R})$ admits no bi-invariant positive-definite metric—all eliminated;
   - **$d = 3$ ($\mathbb{T}_3 \cong S^3$ uniquely survives)**: Eliminating $H_3(\mathbb{R})$ and $\widetilde{\mathrm{SL}}(2, \mathbb{R})$ leaves $S^3$ alone, satisfying $[\mathbf{e}_1, \mathbf{e}_2] = \mathbf{e}_3 \neq \mathbf{0}$, $[x, y, z] \neq [z, y, x]$, $d\eta \equiv 0$, and $\partial S^3 = \emptyset$;
   - **$d = 4$ ($S^3_L \times S^3_R$)**: $\mathfrak{so}(4) \cong \mathfrak{su}(2)_L \oplus \mathfrak{su}(2)_R$ splits back into two independent 3D ternion fields, violating minimal dimension in Law (III)!
2. **Exact rational three-point Gram check on $S^3$** ($\kappa(\gamma(0), \gamma(\epsilon)) = \cos^2\frac{\epsilon}{2}$):
   - At $\epsilon = 60^\circ = \frac{\pi}{3}$, $f(60^\circ) = \frac{3}{4}$ and $f(120^\circ) = \frac{1}{4}$ yield $\det\mathbf{G}_3(60^\circ) = \bigl(1 - \frac{1}{4}\bigr)\bigl(1 + \frac{1}{4} - \frac{9}{8}\bigr) = \frac{3}{4}\times\frac{1}{8} = \mathbf{\frac{3}{32}} = \mathbf{0.09375000 > 0}$ ($v_\epsilon = \mathbf{0.50000000}$);
   - At $\epsilon = 90^\circ = \frac{\pi}{2}$, $f(90^\circ) = \frac{1}{2}$ and $f(180^\circ) = 0$ yield $\det\mathbf{G}_3(90^\circ) = (1 - 0)\times\frac{1}{2} = \mathbf{\frac{1}{2}} = \mathbf{0.50000000 > 0}$ ($v_\epsilon = \mathbf{1.00000000}$), strictly positive definite across $(0, \pi)$!
:::

---

**From the Fourfold Fusion of $\mathrm{AXIOM}\text{-}\Omega$ to the Five-Tier Grand Deduction Cascade.** Having seen why **unbiased comparison $\implies$ minimal circular arcs $\implies$ 3D ternions $\implies$ boundaryless fields** are four faces of one origin-free mother axiom $\mathrm{AXIOM}\text{-}\Omega$, we now take the twenty-fifth and final step of Chapter 39 in [§39.25 The Five-Tier Deduction Cascade of AXIOM-Ω and Apophatic Self-Transparency](ch39-s25-axiom-omega-five-tier-deduction-cascade.md), marching cleanly from Tier 1 through Tier 5 across number systems and calculus, relativistic spacetime, four-force grand unification, arithmetic critical-line spectra, geodesic intelligence, and the apophatic self-erasure of the axiom ladder itself!
