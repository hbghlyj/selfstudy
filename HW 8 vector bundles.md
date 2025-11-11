# 1.
Show that $\mathscr{O}_{\mathbb{RP}^1}(-1)$ is isomorphic to the Möbius bundle.

Proof

The tautological line bundle $\mathscr{O}_{\mathbb{RP}^1}(-1)$ is the set of pairs $(\ell, v)$ where $\ell \in \mathbb{RP}^1$ is a line through the origin in $\mathbb{R}^2$ and $v \in \ell$. The Möbius bundle $M$ can be constructed as the quotient of $S^1 \times \mathbb{R}$ by the equivalence relation $(u, t) \sim (-u, -t)$ for any unit vector $u \in S^1 \subset \mathbb{R}^2$ and scalar $t \in \mathbb{R}$. The base space of this bundle is $\mathbb{RP}^1 = S^1 / \{u \sim -u\}$.

To show these bundles are isomorphic, we construct an explicit map $`\Phi: \mathscr{O}_{\mathbb{RP}^1}(-1) \to M`$.
For any point $(\ell, v) \in \mathscr{O}_{\mathbb{RP}^1}(-1)$, choose a unit vector $u$ that spans the line $\ell$. Then $v$ can be uniquely written as $v = tu$ for some $t \in \mathbb{R}$. We define the map as:
$\Phi(\ell, v) = [u, t]$, where $[u, t]$ is the equivalence class of $(u, t)$ in $M$.

This map is well-defined because if we chose $-u$ to span $\ell$ instead, the vector $v$ would be written as $v = (-t)(-u)$. The map would then yield $[-u, -t]$. By the definition of the equivalence relation on $M$, $[-u, -t] = [u, t]$, so the map's output is independent of our choice of spanning vector.

The map $\Phi$ is a bijection which is linear on each fiber. It is also continuous, and thus defines a vector bundle isomorphism.

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

Proof

A vector bundle is trivial if and only if it has a set of transition functions that can all be chosen to be the identity on the overlaps of the trivializing neighborhoods. We will show this is the case for $L \otimes L^*$.

Let $L$ be a line bundle over a space $X$. Let $`\{U_\alpha\}_{\alpha \in I}`$ be an open cover of $X$ such that $L$ is trivial over each $U_\alpha$. The bundle $L$ is defined by a set of transition functions

$g_{\alpha\beta}: U_\alpha \cap U_\beta \to \text{GL}(1, \mathbb{R})$.

The dual bundle $L^*$ has transition functions $h_{\alpha\beta}$ given by the inverse transpose of $g_{\alpha\beta}$. Since the rank is 1, this is simply the inverse:

$h_{\alpha\beta} = (g_{\alpha\beta}^T)^{-1} = g_{\alpha\beta}^{-1}$

The tensor product bundle $`L \otimes L^*`$ has transition functions $t_{\alpha\beta}$ given by the tensor product of the transition functions of $L$ and $L^*$.

For rank 1 bundles, this corresponds to the product of the scalar-valued functions:

$t_{\alpha\beta}(x) = g_{\alpha\beta}(x) \otimes h_{\alpha\beta}(x) = g_{\alpha\beta}(x) \cdot g_{\alpha\beta}(x)^{-1} = 1$

for all $x \in U_\alpha \cap U_\beta$.

Since all transition functions for $L \otimes L^*$ can be chosen to be the identity map, the bundle is globally trivial.

# 4.
Show that for a smooth submanifold $S \subset M$, the tangent bundle $T S \subset T M|_S$ is a subbundle.

# 5.
Let $E \rightarrow X$ and $F \rightarrow X$ be vector bundles of rank $r$ over the same space. Then $E$ and $F$ are isomorphic if and only if, after passing to a common refinement $`\{U_a\}_{a \in \mathcal{I}}`$, their respective transition functions $\sigma_{a b}$ and $\sigma_{a b}'$ are related by

$\sigma_{a b}=\tau_b^{-1} \sigma_{a b}' \tau_a$

for a collection of matrix-valued functions $`\{\tau_a \in C^0\left(U_a, \mathrm{GL}(r, K)\right)\}_{a \in \mathcal{I}}`$.

# 6.
Exhibit an isomorphism between $T \mathbb{C P}^1$ and $\mathscr{O}(n)$ for some $n \in \mathbb{Z}$ (please say which).
