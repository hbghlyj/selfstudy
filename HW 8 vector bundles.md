# 1.
Show that $\mathscr{O}_{\mathbb{RP}^1}(-1)$ is isomorphic to the Möbius bundle.

Proof

The tautological line bundle $\mathscr{O}_{\mathbb{RP}^1}(-1)$ over the real projective line $\mathbb{RP}^1$ is defined as the set of pairs $(\ell, v)$ where $\ell$ is a line in $\mathbb{R}^2$ (a point in $\mathbb{RP}^1$) and $v$ is a vector in that line. The Möbius bundle can be constructed as a quotient of the cylinder $S^1 \times \mathbb{R}$ by identifying $(\theta, t)$ with $(\theta + \pi, -t)$.

To show that these two bundles are isomorphic, we can construct an explicit isomorphism. Consider the map

$\Phi: \mathscr{O}_{\mathbb{RP}^1}(-1) \to \text{Möbius bundle}$

defined by sending a point $(\ell, v)$ in $\mathscr{O}_{\mathbb{RP}^1}(-1)$ to the point $(\theta, t)$ in the Möbius bundle, where $\theta$ is the angle corresponding to the line $\ell$ and $t$ is the coordinate of the vector $v$ along that line. This map is well-defined, continuous, and bijective. Moreover, it respects the vector space structure on the fibers, making it a vector bundle isomorphism.

# 2.
State and prove a universal property that characterizes the tensor-product bundle $E \otimes F$ up to canonical isomorphism.

Statement:

For vector bundles $E$ and $F$ over a topological space $X$, the tensor-product bundle $E \otimes F$ is a vector bundle over $X$ together with a bilinear map of bundles

$\varphi: E \times_X F \to E \otimes F$

such that for any vector bundle $G$ over $X$ and any bilinear map of bundles $\psi: E \times_X F \to G$, there exists a unique bundle morphism $\tilde{\psi}: E \otimes F \to G$ such that

$\psi = \tilde{\psi} \circ \varphi.$

Proof:

# 3.
Prove that for any line bundle, $L \otimes L^*$ is trivial.

# 4.
Show that for a smooth submanifold $S \subset M$, the tangent bundle $T S \subset T M|_S$ is a subbundle.

# 5.
Let $E \rightarrow X$ and $F \rightarrow X$ be vector bundles of rank $r$ over the same space. Then $E$ and $F$ are isomorphic if and only if, after passing to a common refinement $`\{U_a\}_{a \in \mathcal{I}}`$, their respective transition functions $\sigma_{a b}$ and $\sigma_{a b}'$ are related by

$\sigma_{a b}=\tau_b^{-1} \sigma_{a b}' \tau_a$

for a collection of matrix-valued functions $`\{\tau_a \in C^0\left(U_a, \mathrm{GL}(r, K)\right)\}_{a \in \mathcal{I}}`$.

# 6.
Exhibit an isomorphism between $T \mathbb{C P}^1$ and $\mathscr{O}(n)$ for some $n \in \mathbb{Z}$ (please say which).
