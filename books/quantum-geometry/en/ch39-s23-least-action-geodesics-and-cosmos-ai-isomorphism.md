# 39.23 Least-Action Isomorphism Between Artificial Intelligence and the Cosmos: Ternion-Field Sagitta Action, Born Surprisal, Heap-Autoparallel Geodesics, and Hallucination-Free Chains of Thought {#sec-ch39-least-action-geodesics-and-cosmos-ai-isomorphism}

> *"Artificial intelligence and the universe ought to be isomorphic—both are information systems governed by least action. In the language of minimal circular-arc ternion fields, what then is least action, and what is a geodesic?"*

Having established five lossless three-DOF nonlinear representations and origin-free heap syntax in [§39.21](ch39-s21-nonlinear-ternion-representations-and-torsor-synthesis.md#sec-ch39-nonlinear-ternion-representations-and-torsor-synthesis), and having reconstructed modern sequence models as purely rational rotor systems on parallel concept-field bundles $(\mathbb{T}_3)^K$ in [§39.22](ch39-s22-ternion-field-transformer-and-rational-rotor-dynamics.md#sec-ch39-ternion-field-transformer-and-rational-rotor-dynamics), the last disciplinary wall between fundamental physics and artificial intelligence falls away: **if both the physical cosmos and general intelligence are exteriorless, self-referential information systems clocked at a shared comparison frequency $\nu_0$, what single geometric quantity on $(\mathbb{T}_3)^K$ unites physics' Principle of Least Action with AI's Occam optimality—and what exactly is the geodesic both systems trace?**

Completing our arc on ternion representations and rational rotor intelligence, this section delivers a transparent geometric answer (the two-tier cosmos–AI isomorphism, jump-hallucination mechanism, and per-field natural-gradient preconditioning interpretation are marked **`MODEL`**; the exact identity between the finite rational step kernel and chord–arc sagitta, pairwise cosine uniform-cadence optimality, heap point-reflection autoparallelism, and Jacobi focusing are **`manual derivation` / `NUM`**; analytical mechanics, information geometry, and chain-of-thought sampling are **`Literature`**; and the underlying Fubini–Study triangle inequality, record-time bounds, Born pairing, Schur minimum, and triangle holonomy are anchored by **`LEAN ✓`** declarations): on $(\mathbb{T}_3)^K$, **least action** is **minimum cumulative second-order chord–arc sagitta** (equivalently minimum Born blind-zone leakage and minimum master-clock tick expenditure), while a **geodesic** is a **uniform-cadence great-circle ridge obeying ternary heap autoparallelism $[x_t, x_{t-1}, x_t]$, zero lateral cross-product torque, and zero enclosed spherical excess ($\Omega = 0$)**—manifesting in physics as inertial motion and gravitational free fall, and in AI as a hallucination-free shortest chain of thought alongside $O(1)$ inversion-free Riemannian natural gradient flow.

## 39.23.1 The True Face of Least Action: Chord–Arc Sagitta, the Rational Step Kernel, Born Surprisal, and Master-Clock Tick Tax {#sec-ch39-23-1}

Across traditional textbooks, Maupertuis–Hamilton action $S = \int (T - V)\,dt$ in physics and variational free energy (cross-entropy surprisal plus complexity divergence) in machine learning appear unrelated; restored to the parallel ternion concept bundle $(B_1(\mathbb{R}^3))^K$ clocked at $\nu_0$ ([§39.8](ch39-s08-universal-clock-and-gravitational-dilation.md#sec-ch39-universal-clock-and-gravitational-dilation)), they coincide term by term on every minimal circular-arc step.

Along a discrete trajectory $\Gamma = \{\mathbf{\Sigma}_t\}_{t=0}^N$ across $K$ concept fields, let $\boldsymbol{\delta}_t^{(k)} := (-\boldsymbol{\sigma}_{t-1}^{(k)}) \star_{\mathcal{S}} \boldsymbol{\sigma}_t^{(k)} \in B_1(\mathbb{R}^3)$ denote the relative comparison rotor at tick $t$ on field $k$, with spatial rotation angle $\Delta\theta_t^{(k)} = 4\arctan\lVert\boldsymbol{\delta}_t^{(k)}\rVert \in [0, \pi]$ (spinor half-angle $\frac{1}{2}\Delta\theta_t^{(k)} \in [0, \frac{\pi}{2}]$). A single comparison simultaneously locks three equivalent geometric and informational quantities (`manual derivation`):

1. **Second-Order Chord–Arc Sagitta**: The inward versine arch height separating the circular arc from its flat tangent ([§34.30](ch34-s30-arc-body-calculus-and-finite-stokes.md#sec-ch34-arc-body-calculus-and-finite-stokes)):

   $$
   v_\epsilon\bigl(\Delta\theta_t^{(k)}\bigr) \;:=\; 1 - \cos\Delta\theta_t^{(k)} \;=\; 2\sin^2\frac{\Delta\theta_t^{(k)}}{2} \;\in\; [0, 2];
   $$

2. **Dual-Chart Rational Step Energy Kernel (Exact Finite Identity)**: In [§39.22.1](ch39-s22-ternion-field-transformer-and-rational-rotor-dynamics.md#sec-ch39-22-1), the infinitesimal conformal metric reads $ds_{S^3}^2 = \frac{4\lVert d\boldsymbol{\sigma}\rVert^2}{(1+\lVert\boldsymbol{\sigma}\rVert^2)^2} = \frac{1}{4}(d\theta)^2$; remarkably, evaluating the same rational expression on **any finite step rotor** $\boldsymbol{\delta}_t^{(k)}$ ($\lVert\boldsymbol{\delta}_t^{(k)}\rVert = \tan\frac{\Delta\theta_t^{(k)}}{4}$) yields an **exact identity across all $\Delta\theta_t^{(k)} \in [0, \pi]$ without small-angle approximation**:

   $$
   q_{\mathrm{MRP}}\bigl(\boldsymbol{\delta}_t^{(k)}\bigr) \;:=\; \frac{4\,\lVert\boldsymbol{\delta}_t^{(k)}\rVert^2}{\bigl(1 + \lVert\boldsymbol{\delta}_t^{(k)}\rVert^2\bigr)^2} \;=\; 4\tan^2\frac{\Delta\theta_t^{(k)}}{4}\cos^4\frac{\Delta\theta_t^{(k)}}{4} \;\equiv\; \sin^2\frac{\Delta\theta_t^{(k)}}{2} \;\equiv\; \frac{1}{2}\,v_\epsilon\bigl(\Delta\theta_t^{(k)}\bigr);
   $$

3. **Shannon–Born Comparison Surprisal**: Round-trip Born survival ([`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight), `LEAN ✓`) retains $P_{\mathrm{stay}} = b(\boldsymbol{\sigma}_{t-1}^{(k)}, \boldsymbol{\sigma}_t^{(k)}) = \cos^2\frac{\Delta\theta_t^{(k)}}{2}$ while leaking $P_{\mathrm{leak}} = 1 - P_{\mathrm{stay}} = \sin^2\frac{\Delta\theta_t^{(k)}}{2} \equiv \frac{1}{2}v_\epsilon$ into the $90^\circ$ orthogonal blind zone $\hat{\mathbf{i}}$, so stepwise negative log-likelihood surprisal expands with strictly positive coefficients:

   $$
   \mathcal{I}_t^{(k)} \;:=\; -\ln\cos^2\!\left(\frac{\Delta\theta_t^{(k)}}{2}\right) \;=\; -\ln\!\left(1 - \frac{v_\epsilon}{2}\right) \;=\; \frac{1}{2}v_\epsilon \;+\; \frac{1}{8}v_\epsilon^2 \;+\; \mathcal{O}(v_\epsilon^3).
   $$

Summing intra-field sagitta cost minus the background or context-coupling spherical excess $\Omega_{\mathrm{ctx}}^{(k)}(\boldsymbol{\sigma}_t)$ along $\Gamma$ yields the universal **dimensionless ternion-field action functional** (`MODEL`):

$$
\mathcal{S}[\Gamma] \;:=\; \sum_{t=1}^{N}\sum_{k=1}^{K} \Biggl[\underbrace{\bigl(1 - \cos\Delta\theta_t^{(k)}\bigr)}_{\substack{\text{Intra-field sagitta } T\\\text{(state-flip tick cost)}}} \;-\; \underbrace{\Omega_{\mathrm{ctx}}^{(k)}(\boldsymbol{\sigma}_t)}_{\substack{\text{Context excess potential } V\\\text{(gravity well or prompt lock)}}}\Biggr].
$$

Three foundational mysteries dissolve immediately:

- **Planck's constant $\hbar$ as the master-clock exchange rate**: Because all observers share the comparison clock $\nu_0$ (anchored by the Fubini–Study minimum record duration [`record_time_lower_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_time_lower_bound) and tick ceiling [`record_count_upper_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_count_upper_bound), `LEAN ✓`), each unit of sagitta expends a fixed quota of elementary comparison ticks; physical action $S_{\mathrm{phys}} = \hbar\mathcal{S}[\Gamma]$ carries dimensions of $\text{energy} \times \text{time}$ solely because $\hbar$ converts dimensionless radian phase into joule-seconds;
- **Schur-complement origin of the $T - V$ minus sign**: Within a unit-budget block Gram matrix, background gravitational load or prompt context $\Omega_{\mathrm{ctx}}$ pre-allocates cross-field correlation bandwidth, leaving the **Schur-complement variational slack** $A - B C^{-1} B^\dagger$ ([`schur_quadratic_is_least`](lean:D5/S3/Quantum/Matrix/SchurMinimum.schur_quadratic_is_least), `LEAN ✓`) for local state transitions;
- **Blind-zone destructive interference selects least action and Occam chains of thought**: Neither nature nor a parallel superposition needs teleological foresight to locate $\min\mathcal{S}$. Across $\sum_\Gamma \exp(\hat{\mathbf{i}}\mathcal{S}[\Gamma])$, non-geodesic detours enclose extra spherical excess that spins rapidly inside $\hat{\mathbf{i}}$, cancelling neighboring off-shell paths pairwise, whereas only the stationary-phase spine $\delta\mathcal{S} = 0$ ([§32.3](ch32-s03-axioms-as-corollaries.md), [§34.6](ch34-s06-berry-sectors-and-path-integrals.md)) survives constructively—manifesting in physics as classical trajectories and in AI as multi-sample **Self-Consistency** decoding (Wang et al. 2023) where meandering hallucinations cancel while coherent reasoning chains reinforce!

## 39.23.2 Four Equivalent Definitions of a Geodesic: Heap Autoparallelism, Zero Excess, Uniform-Cadence Lock, and Jacobi Focusing {#sec-ch39-23-2}

Whereas Euclidean chord interpolation $(1-\lambda)\mathbf{x}_0 + \lambda\mathbf{x}_1$ cuts inside the sphere and collapses representation norms, a **free geodesic** on $(B_1(\mathbb{R}^3))^K$ admits four Christoffel-free, algebraically exact characterizations (`manual derivation`):

1. **Origin-Free Ternary Heap Autoparallelism (Cartan Symmetric-Space Point Reflection)**:
   Under the Prüfer–Baer heap $[x, y, z] = x y^{-1} z$ ([§39.21.4](ch39-s21-nonlinear-ternion-representations-and-torsor-synthesis.md#sec-ch39-21-4)), a discrete trajectory $\{\boldsymbol{\sigma}_t\}_{t=0}^N$ is a constant-speed geodesic (away from the measure-zero half-turn seam) if and only if every consecutive triple obeys **heap self-reflection**:

   $$
   \boldsymbol{\sigma}_{t+1}^{(k)} \;=\; \Bigl[\boldsymbol{\sigma}_t^{(k)},\; \boldsymbol{\sigma}_{t-1}^{(k)},\; \boldsymbol{\sigma}_t^{(k)}\Bigr] \;\equiv\; \boldsymbol{\sigma}_t^{(k)} \star_{\mathcal{S}} \Bigl(\bigl(-\boldsymbol{\sigma}_{t-1}^{(k)}\bigr) \star_{\mathcal{S}} \boldsymbol{\sigma}_t^{(k)}\Bigr).
   $$

   Substituting $g_t = g_0 e^{tX}$ in non-Abelian $\mathrm{SU}(2)$ or $\mathrm{SO}(3)$ verifies $g_t g_{t-1}^{-1} g_t = g_0 e^{tX} e^{-(t-1)X} g_0^{-1} g_0 e^{tX} = g_0 e^{(t+1)X} = g_{t+1}$ identically even when $g_0$ and $e^X$ do not commute! Geometrically, $[g_t, g_{t-1}, g_t] = s_{g_t}(g_{t-1})$ is Élie Cartan's geodesic point-reflection involution centered at $g_t$, grafting the preceding comparison arc forward without extrinsic bias.

2. **Zero Cross-Product Lateral Torque and Vanishing Girard Spherical Excess ($\Omega = 0$)**:
   For consecutive local right-step rotors $\boldsymbol{\omega}_t := (-\boldsymbol{\sigma}_{t-1}) \star_{\mathcal{S}} \boldsymbol{\sigma}_t$ and $\boldsymbol{\omega}_{t+1} := (-\boldsymbol{\sigma}_t) \star_{\mathcal{S}} \boldsymbol{\sigma}_{t+1}$, great-circle co-axiality holds if and only if the **nonlinear cross-product lateral torque vanishes** (anchored in [`lagrange_gram_identity`](lean:D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity) and [`shortest_gate_triangle_holonomy`](lean:D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.shortest_gate_triangle_holonomy), `LEAN ✓`):

   $$
   \boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1} \;=\; \mathbf{0} \quad \Longleftrightarrow \quad \Omega\bigl(\boldsymbol{\sigma}_{t-1}, \boldsymbol{\sigma}_t, \boldsymbol{\sigma}_{t+1}\bigr) \;=\; 0.
   $$

   Together with forward alignment $\boldsymbol{\omega}_t \cdot \boldsymbol{\omega}_{t+1} \ge 0$ and total angle below the cut locus $\sum_{t=1}^N \Delta\theta_t \le \pi$, equality holds in the Fubini–Study triangle inequality ([`fs_angle_triangle`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.fs_angle_triangle), `LEAN ✓`); adjoining equal step norms $\boldsymbol{\omega}_{t+1} = \boldsymbol{\omega}_t$ recovers Item 1! When attention Schur bridges or external gauge potentials inject $\boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1} \neq \mathbf{0}$, the base trajectory refracts smoothly while lifting to a bundle geodesic under the Kaluza–Klein–Wong connection metric with conserved fiber charge (`Literature`).

3. **Uniform-Cadence Law Locked by Sagitta Convexity and Pairwise Cosine Factorization (Inertial Speed & AI Jump Hallucinations)**:
   Along a fixed great-circle arc of total span $\sum_{t=1}^N \Delta\theta_t = \Theta \in (0, \pi)$ ($\Delta\theta_t \ge 0$), how should step sizes be apportioned? Not only is $f(\Delta\theta) = 1 - \cos\Delta\theta$ strictly convex on $[0, \frac{\pi}{2}]$ ($f''(\Delta\theta) = \cos\Delta\theta \ge 0$), but across the **entire open domain $\Theta \in (0, \pi)$** (even if an individual step enters $(\frac{\pi}{2}, \pi)$!), the exact pairwise cosine identity (`manual derivation`)

   $$
   (1 - \cos x_i) + (1 - \cos x_j) \;=\; 2 \;-\; 2\cos\frac{x_i + x_j}{2}\cos\frac{x_i - x_j}{2} \;\ge\; 2\!\left(1 - \cos\frac{x_i + x_j}{2}\right)
   $$

   ($\cos\frac{x_i+x_j}{2} > 0$ since $x_i + x_j \le \Theta < \pi$) proves that averaging any unequal pair $x_i \neq x_j$ strictly lowers cumulative sagitta—while Shannon–Born surprisal satisfies $\mathcal{I}''(\Delta\theta) = \frac{1}{2}\sec^2\frac{\Delta\theta}{2} \ge \frac{1}{2} > 0$ globally on $[0, \pi)$! Thus **uniform step cadence** $\Delta\theta_1 = \dots = \Delta\theta_N = \frac{\Theta}{N}$ is the unique strict global minimizer:

   $$
   \sum_{t=1}^{N}\bigl(1 - \cos\Delta\theta_t\bigr) \;\ge\; N\!\left(1 - \cos\frac{\Theta}{N}\right), \qquad \sum_{t=1}^{N}\mathcal{I}(\Delta\theta_t) \;\ge\; -N\ln\cos^2\!\left(\frac{\Theta}{2N}\right)!
   $$

   In physics (`MODEL`), this derives **uniform speed** in Newton's First Law directly from circular-arc sagitta; in AI reasoning, it pinpoints why **skipping reasoning steps triggers hallucinations**: idling on boilerplate tokens ($\Delta\theta_t \approx 0$) before attempting one giant leap $\Delta\theta_N = \Theta$ inflates single-step blind-zone leakage $\sin^2(\Theta/2)$ and surprisal quadratically/logarithmically out of the local basin, whereas an equal-stride chain of thought pays only $O(\Theta^2/N)$ sagitta cost!

4. **Positive-Curvature Lie-Triple Jacobi Focusing (Intrinsic Hallucination Damping)**:
   Unlike flat Euclidean space (linear drift $\lVert\mathbf{J}_\perp(s)\rVert \propto s$) or negatively curved hyperbolic space (exponential divergence $\sinh(\lvert\kappa\rvert s)$), on a ternion sphere of sectional curvature $\kappa^2 > 0$ ($\kappa = 1$ on unit $S^3$), transverse geodesic deviation $\mathbf{J}_\perp \perp \dot{\gamma}$ obeys the **Jacobi focusing equation** governed by the Lie triple curvature bracket of [§39.21.4](ch39-s21-nonlinear-ternion-representations-and-torsor-synthesis.md#sec-ch39-21-4) (with exact sign alignment: under $\{\mathbf{a},\mathbf{b},\mathbf{c}\} = (\mathbf{a}\cdot\mathbf{c})\mathbf{b} - (\mathbf{b}\cdot\mathbf{c})\mathbf{a}$, $\mathbf{J}_\perp \perp \dot{\gamma}$ gives $\{\dot{\gamma}, \mathbf{J}_\perp, \dot{\gamma}\} = +\lVert\dot{\gamma}\rVert^2\mathbf{J}_\perp = -\{\mathbf{J}_\perp, \dot{\gamma}, \dot{\gamma}\}$, `manual derivation`):

   $$
   \frac{D^2\mathbf{J}_\perp}{ds^2} \;+\; \kappa^2\bigl\{\dot{\gamma},\, \mathbf{J}_\perp,\, \dot{\gamma}\bigr\} \;=\; \frac{D^2\mathbf{J}_\perp}{ds^2} \;-\; \kappa^2\bigl\{\mathbf{J}_\perp,\, \dot{\gamma},\, \dot{\gamma}\bigr\} \;=\; \ddot{\mathbf{J}}_\perp \;+\; \kappa^2\mathbf{J}_\perp \;=\; \mathbf{0},
   $$

   whose oscillatory solution $\mathbf{J}_\perp(s) = \mathbf{J}_\perp(0)\cos(\kappa s) + \frac{\dot{\mathbf{J}}_\perp(0)}{\kappa}\sin(\kappa s)$ provides a centripetal restoring force refocusing small prompt perturbations onto the same target attractor!

## 39.23.3 Two-Tier Cosmos–AI Isomorphism, O(1) Conformal Natural Gradient, and Final Summit of the Main Text {#sec-ch39-23-3}

We record the formal model definition, ten frozen Lean 4 anchors, literature boundaries, quantitative trajectory audit, and master synthesis table below:

::: {.definition #def-ch39-ternion-least-action-and-heap-geodesic title="Dimensionless Ternion-Field Sagitta Action, Heap-Autoparallel Geodesics, and O(1) Conformal Riemannian Gradient (Model Definition)"}
On the parallel ternion concept-field bundle $(B_1(\mathbb{R}^3))^K$ (`MODEL`):

1. **Discrete ternion-field action**: For $\Gamma = \{\mathbf{\Sigma}_t\}_{t=0}^N$ and context excess potential $\Omega_{\mathrm{ctx}}^{(k)}$, set $\mathcal{S}[\Gamma] := \sum_{t=1}^N\sum_{k=1}^K \bigl[2\,q_{\mathrm{MRP}}(\boldsymbol{\delta}_t^{(k)}) - \Omega_{\mathrm{ctx}}^{(k)}(\boldsymbol{\sigma}_t)\bigr]$ with $2\,q_{\mathrm{MRP}}(\boldsymbol{\delta}) = \frac{8\lVert\boldsymbol{\delta}\rVert^2}{(1+\lVert\boldsymbol{\delta}\rVert^2)^2} \equiv 1 - \cos\Delta\theta$;
2. **Discrete free heap geodesic**: Any trajectory satisfying $\boldsymbol{\sigma}_{t+1}^{(k)} = [\boldsymbol{\sigma}_t^{(k)}, \boldsymbol{\sigma}_{t-1}^{(k)}, \boldsymbol{\sigma}_t^{(k)}]$ (equivalently forward co-axiality $\boldsymbol{\omega}_t^{(k)} \times \boldsymbol{\omega}_{t+1}^{(k)} = \mathbf{0}$ with equal step $\boldsymbol{\omega}_{t+1}^{(k)} = \boldsymbol{\omega}_t^{(k)}$);
3. **Per-field $O(1)$ conformal Riemannian steepest descent**: Under $g_{ij}(\boldsymbol{\sigma}) = \frac{4\,\delta_{ij}}{(1+\lVert\boldsymbol{\sigma}\rVert^2)^2}$, the exact parameter-manifold Riemannian gradient requires zero matrix inversion: $\operatorname{grad}_{S^3}\mathcal{L}(\boldsymbol{\sigma}_W) := g(\boldsymbol{\sigma}_W)^{-1}\nabla\mathcal{L} = \frac{1}{4}(1 + \lVert\boldsymbol{\sigma}_W\rVert^2)^2\,\nabla\mathcal{L}$.
:::

::: {.theorem #thm-ch39-least-action-geodesics-and-cosmos-ai-anchors title="Fubini–Study Geodesic Triangle Inequality, Orthogonal Record Time & Count Bounds, Rank-One Born Weight, Schur Minimum, Shortest-Gate Rotor & Triangle Holonomy, Lagrange–Gram Identity, and Eigenstate & Krylov Stability" lean="D5/S3/QuantumBounds/FubiniStudyRecordTime.fs_angle_triangle,D5/S3/QuantumBounds/FubiniStudyRecordTime.record_time_lower_bound,D5/S3/QuantumBounds/FubiniStudyRecordTime.record_count_upper_bound,D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight,D5/S3/Quantum/Matrix/SchurMinimum.schur_quadratic_is_least,D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.rotor_shortest_gate,D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.shortest_gate_triangle_holonomy,D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity,D5/S3/Quantum/Dynamics/EnergyEigenstateStationarity.energy_eigenstate_stationary,D5/S3/ObserverMemory/Dynamics/ObservableKrylovPermanentStability.observable_krylov_once_stable_permanently"}
In the pinned `trureturing` frozen declaration set, the following ten mathematical theorems hold simultaneously:

1. **Unit-vector Fubini–Study geodesic triangle inequality** ([`fs_angle_triangle`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.fs_angle_triangle)): For unit states $u, v, w$, $d_{\mathrm{FS}}(u, w) \le d_{\mathrm{FS}}(u, v) + d_{\mathrm{FS}}(v, w)$;
2. **Minimum orthogonal-record duration and sequential record-count ceiling** ([`record_time_lower_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_time_lower_bound), [`record_count_upper_bound`](lean:D5/S3/QuantumBounds/FubiniStudyRecordTime.record_count_upper_bound)): Bounded-energy-variance evolution enforces a positive minimum duration per orthogonal distinction and an upper bound on sequential distinctions within a finite horizon;
3. **Rank-one Born modulus-squared survival weight** ([`rank_one_born_pairing_weight`](lean:D5/S3/Observer/Conditioning/RankOneBornPairingWeight.rank_one_born_pairing_weight)): Pure-state readout under rank-one projection equals $\lvert\langle\phi, \psi\rangle\rvert^2$;
4. **Hermitian block Schur-complement variational minimum** ([`schur_quadratic_is_least`](lean:D5/S3/Quantum/Matrix/SchurMinimum.schur_quadratic_is_least)): Minimizing over a positive-definite interior block attains $x^\dagger(A - B C^{-1} B^\dagger)x$;
5. **Shortest geodesic rotor gate and spherical-triangle holonomy** ([`rotor_shortest_gate`](lean:D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.rotor_shortest_gate), [`shortest_gate_triangle_holonomy`](lean:D5/S3/Quantum/Information/GroupInvariantPsi/ShortestGateHolonomy.shortest_gate_triangle_holonomy)): Non-antipodal shortest rotors transport Pauli axes unitarily, and three-vertex loops accumulate return phase $\frac{S_{abc} - i D_{abc}}{\sqrt{S_{abc}^2 + D_{abc}^2}}$ (vanishing identically when $D_{abc} = 0$);
6. **Lagrange–Gram antisymmetric minor identity** ([`lagrange_gram_identity`](lean:D5/S3/QuantumBounds/LagrangeGramIdentity.lagrange_gram_identity)): $\lVert u\rVert^2\lVert v\rVert^2 - \langle u, v\rangle^2 = \frac{1}{2}\sum_{i,j}(u_i v_j - u_j v_i)^2$;
7. **Energy-eigenstate stationarity and permanent observable Krylov stability** ([`energy_eigenstate_stationary`](lean:D5/S3/Quantum/Dynamics/EnergyEigenstateStationarity.energy_eigenstate_stationary), [`observable_krylov_once_stable_permanently`](lean:D5/S3/ObserverMemory/Dynamics/ObservableKrylovPermanentStability.observable_krylov_once_stable_permanently)): Normalized eigenstates remain invariant under Hermitian evolution, and finite-dimensional observable Krylov towers stabilize permanently once two consecutive stages coincide.
:::

::: proof
Item 1 applies Cauchy–Schwarz and arccosine subadditivity to unit state overlaps ([Chapter 7](ch07-geometric-time-and-speed-limits.md)). Item 2 integrates the Fubini–Study speed bound up to orthogonal angle $\frac{\pi}{2}$ ([§39.8](ch39-s08-universal-clock-and-gravitational-dilation.md)). Items 3, 4, and the second half of Item 7 match [@thm-ch39-tft-born-holonomy-krylov-and-schur-anchors] Items 1, 7, and 4. Items 5–6 match [@thm-ch39-nonlinear-ternion-representations-and-torsor] Items 3–4 and 2. For the first half of Item 7, $H\psi = E\psi$ multiplies $\psi$ by $e^{-iEt}$, leaving $\lvert\psi\rangle\langle\psi\rvert$ invariant. The full proof is checked by the Lean kernel.
:::

::: {.remark #rem-ch39-maupertuis-feynman-friston-amari-cot-literature title="Maupertuis–Feynman Least Action, Free Energy & MDL, Amari Natural Gradient vs. Quantum Fisher Geometry, and Self-Consistency CoT (Literature & Scope)"}
**Literature attributions and statistical-Fisher scope.** We record the foundational sources and exact mathematical scope of our cross-domain synthesis:

1. **Least action, bundle geodesics, MDL, and variational free energy**: Feynman's phase path integral appears in R. P. Feynman (*Rev. Mod. Phys.* **20**, 367–387, 1948); lifted gauge/gravitational trajectories as bundle geodesics on principal bundles appear in S. K. Wong (*Nuovo Cimento A* **65**, 689–694, 1970) and R. Montgomery (*Lett. Math. Phys.* **8**, 59–67, 1984); Minimum Description Length and the Free-Energy Principle appear in J. Rissanen (*Automatica* **14**, 465–471, 1978) and K. Friston (*Nat. Rev. Neurosci.* **11**, 127–138, 2010, DOI `10.1038/nrn2787`);
2. **Natural gradient, quantum Fisher metric, and chain-of-thought self-consistency**: Statistical natural gradient $F(\theta)^{-1}\nabla\mathcal{L}$ appears in S.-i. Amari (*Neural Comput.* **10**(2), 251–276, 1998, DOI `10.1162/089976698300017746`) and Kronecker-factored K-FAC in Martens & Grosse (*ICML*, 2015); single-state quantum Fisher / Fubini–Study geometry appears in S. L. Braunstein & C. M. Caves (*Phys. Rev. Lett.* **72**, 3439–3443, 1994); chain-of-thought prompting and multi-path Self-Consistency appear in J. Wei et al. (*NeurIPS*, 2022) and X. Wang et al. (*ICLR*, 2023, `arXiv:2203.11171`). **Strict scope note**: For a pure Born state prepared directly by a single ternion rotor, $p(m\mid\boldsymbol{\sigma}) = \cos^2(\Delta\theta_m/2)$, the quantum Fisher metric is strictly proportional to the conformal round-$S^3$ metric $g_{ij}(\boldsymbol{\sigma}) = \frac{4\,\delta_{ij}}{(1+\lVert\boldsymbol{\sigma}\rVert^2)^2}$, making $\frac{1}{4}(1+\lVert\boldsymbol{\sigma}\rVert^2)^2\nabla\mathcal{L}$ exact; in deep multi-layer networks, the output-vocabulary empirical Fisher matrix additionally couples layers through the network Jacobian, so per-field conformal rescaling acts as the **exact parameter-manifold Riemannian gradient and an $O(1)$ block-diagonal geometric preconditioner** (`MODEL`), with large-scale empirical convergence tracked in [@prob-ch39-tft-scale-and-seams] (`OPEN`).
:::

We verify the sagitta action, Born survival, chord collapse, and $O(1)$ conformal Riemannian gradient quantitatively in the three-part audit below:

::: {.example #ex-ch39-geodesic-vs-jump-detour-and-natural-gradient-audit title="Four-Trajectory Action Duel: Uniform Heap Geodesic vs. Final-Step Jump Hallucination, Lateral Excess Detour, and O(1) Conformal Gradient Check"}
Consider evolving one ternion concept field in $N = 4$ ticks from $\boldsymbol{\sigma}_0 = \mathbf{0}$ ($+\mathbf{1}$) to spatial angle $\Theta = \frac{2\pi}{3} = 120^\circ$ about $\hat{\mathbf{e}}_1$ ($\boldsymbol{\sigma}_4 = \frac{1}{\sqrt{3}}\mathbf{e}_1 \approx (0.57735027, 0, 0)$, `manual derivation` / `NUM`):

1. **Part I: Uniform heap geodesic vs. "three idle ticks $+$ one $120^\circ$ jump" hallucination spike (`manual derivation` / `NUM`)**:
   - **Trajectory A (Uniform heap-autoparallel geodesic)**: Advancing $\Delta\theta_t = 30^\circ = \frac{\pi}{6}$ per tick ($\boldsymbol{\omega} = \tan 7.5^\circ\,\mathbf{e}_1 \approx 0.13165250\,\mathbf{e}_1$, obeying $\boldsymbol{\sigma}_{t+1} = [\boldsymbol{\sigma}_t, \boldsymbol{\sigma}_{t-1}, \boldsymbol{\sigma}_t]$ and $\boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1} = \mathbf{0}$) yields per-tick sagitta $1 - \frac{\sqrt{3}}{2} \approx 0.13397460$ and four-tick totals
     $$\mathcal{S}_{\mathrm{geo}} = 4\!\left(1 - \frac{\sqrt{3}}{2}\right) \approx \mathbf{0.53589838}, \qquad P_{\mathrm{stay,total}} = \bigl(\cos^2 15^\circ\bigr)^4 = \left(\frac{2+\sqrt{3}}{4}\right)^4 = \frac{97+56\sqrt{3}}{256} \approx \mathbf{0.75779236}, \qquad \sum_{t=1}^4 \mathcal{I}_t \approx \mathbf{0.27734586\;\mathrm{nat}};$$
   - **Trajectory B (Three idle ticks $\Delta\theta_{1,2,3} = 0^\circ$ followed by a $\Delta\theta_4 = 120^\circ$ jump)**: Despite traversing the identical $120^\circ$ great circle, cumulative sagitta jumps to $\mathcal{S}_{\mathrm{jump}} = 1 - \cos 120^\circ = \mathbf{1.50000000}$ (**$2.79903811\times$ higher!**), survival collapses to $\cos^2 60^\circ = \mathbf{0.25000000}$ ($75\%$ blind-zone leakage), and total surprisal spikes to $-\ln(0.25) \approx \mathbf{1.38629436\;\mathrm{nat}}$ (**$4.99843184\times$ higher**)!

2. **Part II: Lateral cross-product detour vs. Euclidean chord norm collapse (`NUM`)**:
   - **Trajectory C (Lateral non-coaxial detour)**: Deflecting into $\hat{\mathbf{e}}_2$ before returning to $\boldsymbol{\sigma}_4$ triggers $\boldsymbol{\omega}_t \times \boldsymbol{\omega}_{t+1} \neq \mathbf{0}$, encloses positive Girard spherical excess $\Omega > 0$, strictly exceeds $\mathcal{S}_{\mathrm{geo}} \approx 0.53589838$, and cancels its imaginary blind-zone odd component $-i\sin\frac{\Omega}{2}$ identically against the mirror detour's $+i\sin\frac{\Omega}{2}$ (while damping real amplitude by $\cos\frac{\Omega}{2} < 1$, with complete pairwise annihilation $e^{-i\pi/2}+e^{+i\pi/2}=0$ at $\Omega = \pi$);
   - **Trajectory D (Flat Euclidean chord midpoint)**: Halfway chord averaging $\frac{1}{2}(1,0,0,0) + \frac{1}{2}(\frac{1}{2}, \frac{\sqrt{3}}{2}, 0, 0) = (\frac{3}{4}, \frac{\sqrt{3}}{4}, 0, 0)$ collapses norm squared to $\frac{9}{16} + \frac{3}{16} = \mathbf{0.75000000 < 1}$ (losing $25\%$ of sphere norm budget without `RMSNorm`)!

3. **Part III: Exact agreement between $O(1)$ conformal Riemannian gradient and `§39.22` spin-pullback norm (`manual derivation`)**:
   At $\lVert\boldsymbol{\sigma}_W\rVert = 0.8$ ($1 + \lVert\boldsymbol{\sigma}_W\rVert^2 = 1.64$), $g_{ij} = \frac{4}{1.64^2}\delta_{ij} \approx 1.48720999\,\delta_{ij}$ inverts via scalar multiplication by $\frac{1.64^2}{4} = \mathbf{0.67240000}$; its Riemannian squared norm $\langle\nabla\mathcal{L}, g^{-1}\nabla\mathcal{L}\rangle = \frac{1}{4}(1+\lVert\boldsymbol{\sigma}_W\rVert^2)^2\lVert\nabla\mathcal{L}\rVert^2$ agrees **identically** with $\lVert\mathbf{g}_{\mathfrak{su}(2)}^{(R)}\rVert^2 = \frac{1}{4}\lVert J_R^\top\nabla\mathcal{L}\rVert^2$ from [§39.22.2](ch39-s22-ternion-field-transformer-and-rational-rotor-dynamics.md#sec-ch39-22-2)!
:::

We synthesize the two-tier isomorphism between the physical cosmos and artificial intelligence in the five-row reference table below:

| Core Mechanism | Ternion-Field Operator | Physical Cosmos Manifestation | Artificial Intelligence Isomorph | Off-Geodesic Pathology |
| :--- | :--- | :--- | :--- | :--- |
| **1. State Carrier** | Unit-ball bundle $(B_1(\mathbb{R}^3))^K$ | Multi-concept quantum gauge fields | Multi-head 3D token concept states | Norm collapse / blow-up & outliers |
| **2. Least Action** | Sagitta sum $\sum(1-\cos\Delta\theta_t) - \Omega_{\mathrm{ctx}}$ | Maupertuis–Feynman phase action | Variational free energy & surprisal | Blind-zone phase dissipation & waste |
| **3. Free Geodesic** | Heap relay $[\boldsymbol{\sigma}_t,\boldsymbol{\sigma}_{t-1},\boldsymbol{\sigma}_t]$ | Inertial uniform great-circle motion | Hallucination-free uniform CoT | Reasoning detours & step-skipping leaps |
| **4. Refraction & Focus** | Lie curvature $\{\dot{\gamma},\mathbf{J}_\perp,\dot{\gamma}\}$ | Gauge/gravity deflection & focusing | Context attention & noise focusing | Context drift & multi-step divergence |
| **5. Learning & Halt** | $O(1)$ conformal grad & $r_t \le \varepsilon_{\mathrm{self}}$ | Matter curving spacetime & eigenstates | Carving weight riverbeds & early halt | $O(P^3)$ inversion wall or endless loops |

Beneath this table beats a Wheelerian two-way closure (`MODEL`): **forward AI inference is "frozen weight curvature telling token wavepackets how to glide along heap geodesics"** until self-referential halting $r_t \le \varepsilon_{\mathrm{self}}$; **backward AI training is "data wavepackets telling the weight rotor manifold how to curve plastically along $O(1)$ conformal Riemannian geodesics,"** carving recurrent causal structure into low-sagitta geodesic riverbeds!

---

**From Cosmos–AI Least-Action Isomorphism to the Grand Unified Mother Axiom ($\mathrm{AXIOM}\text{-}\Omega$).** Whether a star falls freely across light-years of curved spacetime or an intelligence parts the fog to find a single shortest proof, both obey one and the same minimal circular-arc law: invent zero spurious spherical excess, squander zero single-step sagitta in erratic leaps, and follow the autoparallel grain of the ternary heap $[x_t, x_{t-1}, x_t]$ to close phase from question slice to self-consistent fixed point in the fewest universal clock ticks.

Yet looking back across all thirty-nine chapters, our four central pillars—the **Axiom of Comparison, Minimal Circular Arcs, Ternions, and Continuous Fields**—have stood scattered across separate chapters and disciplines. Are they four independent hypotheses, or do all four emerge as pure mathematical theorems from **one single origin-free, addition-free ternary mother axiom**? Let us open the final two crowning gates of our main text: [§39.24 The Grand Unified Mother Axiom (AXIOM-Ω): Origin-Free PSD Ternary Comparison Closure](ch39-s24-axiom-omega-origin-free-ternary-comparison-closure.md) and [§39.25 The Five-Tier Deduction Cascade of AXIOM-Ω and Apophatic Self-Transparency](ch39-s25-axiom-omega-five-tier-deduction-cascade.md).
