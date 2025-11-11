# 1.
Show that  is isomorphic to the Möbius bundle.

Proof

The tautological line bundle  is the set of pairs  where   is a line through the origin in  and  . The Möbius bundle  can be constructed as the quotient of   by the equivalence relation   for any unit vector    and scalar  . The base space of this bundle is   .

To show these bundles are isomorphic, we construct an explicit map $`\Phi: \mathscr{O}_{\mathbb{RP}^1}(-1) \to M`$.
For any point  , choose a unit vector  that spans the line . Then  can be uniquely written as   for some  . We define the map as:
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

Proof

By Local Frame Criterion for Subbundles, it suffices to show that for each point $p \in S$, there exists a neighborhood $U$ of $p$ in $M$ and smooth local sections $`\{s_1, \ldots, s_k\}`$ of $T M|_U$ such that their restrictions to $S \cap U$ form a local frame for $`T S|_{S \cap U}`$.

Since $S$ is a smooth submanifold of $M$, for each point $p \in S$, there exists a coordinate chart $(U, \varphi)$ around $p$ in $M$ such that $\varphi(U \cap S)$ is given by the vanishing of some coordinates. Without loss of generality, we can assume that in these coordinates, $S$ is defined by the equations $x_{k+1} = x_{k+2} = \ldots = x_n = 0$ for some $k < n$, where $n = \dim M$.

In this coordinate chart, the tangent bundle $T M|_U$ has a local frame given by the coordinate vector fields $`\left\{\frac{\partial}{\partial x_1}, \ldots, \frac{\partial}{\partial x_n}\right\}`$. The tangent bundle $`T S|_{S \cap U}`$ is then spanned by the restrictions of the first $k$ coordinate vector fields:

$`\left\{\frac{\partial}{\partial x_1}, \ldots, \frac{\partial}{\partial x_k}\right\}`$.

These vector fields are smooth sections of $`T M|_U`$, and their restrictions to $S \cap U$ form a local frame for $T S|_{S \cap U}$. Thus, by the Local Frame Criterion for Subbundles, $T S$ is a subbundle of $T M|_S$.

# 5.
Let $E \rightarrow X$ and $F \rightarrow X$ be vector bundles of rank $r$ over the same space. Then $E$ and $F$ are isomorphic if and only if, after passing to a common refinement $`\{U_a\}_{a \in \mathcal{I}}`$, their respective transition functions $\sigma_{a b}$ and $\sigma_{a b}'$ are related by

$\sigma_{a b}=\tau_b^{-1} \sigma_{a b}' \tau_a$

for a collection of matrix-valued functions $`\{\tau_a \in C^0\left(U_a, \mathrm{GL}(r, K)\right)\}_{a \in \mathcal{I}}`$.


Proof

(⇒) Suppose $E$ and $F$ are isomorphic vector bundles over $X$. Then there exists a bundle isomorphism $\Phi: E \to F$. Let $`\{U_a\}_{a \in \mathcal{I}}`$ be a common refinement of the trivializing covers for $E$ and $F$.

Over each $U_a$, we have local trivializations $`\phi_a: E|_{U_a} \to U_a \times K^r`$ and $\psi_a: F|_{U_a} \to U_a \times K^r$. These induce fiber-wise linear isomorphisms $\phi_{a,x}: E_x \to K^r$ and $\psi_{a,x}: F_x \to K^r$ for each $x \in U_a$.

The isomorphism $\Phi$ restricts to a linear isomorphism on fibers $\Phi_x: E_x \to F_x$. We can define a collection of maps $\tau_a: U_a \to \mathrm{GL}(r, K)$ by the composition on each fiber:
$\tau_a(x) = \psi_{a,x} \circ \Phi_x \circ \phi_{a,x}^{-1}$

(⇐) Conversely, suppose the transition functions $\sigma_{ab}$ and $\sigma'_{ab}$ of $E$ and $F$ satisfy the relation

$\sigma_{a b}=\tau_b^{-1} \sigma_{a b}' \tau_a$

for some collection of functions $\tau_a: U_a \to \mathrm{GL}(r, K)$. We can construct a bundle isomorphism $\Phi: E \to F$ by defining it locally on each $U_a$ using the maps $\tau_a$. This will yield a well-defined global isomorphism, completing the proof.

# 6.
Exhibit an isomorphism between $T \mathbb{C P}^1$ and $\mathscr{O}(n)$ for some $n \in \mathbb{Z}$ (please say which).
