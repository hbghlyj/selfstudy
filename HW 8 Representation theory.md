# 1
Let $V$ be a finite-dimensional vector space. For any subspace $W \subset V$, put

$`W^{\perp}:=\left\{\phi \in V^*:\phi|_W=0\right\}`$

Construct natural isomorphisms $W^* \simeq V^* / W^{\perp}$ and $(V / W)^* \simeq W^{\perp}$. (The assumption that $V$ is finite-dimensional is not actually required, but it makes the problem easier.)

Proof

First, we will construct the isomorphism $W^* \simeq V^* / W^{\perp}$.

Consider the natural restriction map $`\rho: V^* \to W^*`$ defined by

$`\rho(\phi) = \phi|_W`$

for any $\phi \in V^*$.

The kernel of this map is precisely $W^{\perp}$, since these are the functionals that vanish on $W$. Since any $`\psi \in W^*`$ can be extended to $`\tilde{\psi} \in V^*`$ (e.g., via Hahn-Banach or basis extension), $\rho$ is surjective, so $`\mathrm{Im}(\rho) = W^*`$.
By the First Isomorphism Theorem, we have
$`V^* / W^{\perp} \simeq W^*`$. 

Next, we will construct the isomorphism $`(V / W)^* \simeq W^{\perp}`$.

Consider the map $\lambda: W^{\perp} \to (V / W)^*$ defined by $\lambda(\phi)(v + W) = \phi(v)$ for any $v \in V$ and $\phi \in W^{\perp}$.

1.  **Well-definedness:** If $v + W = v' + W$, then $v - v' \in W$. Since $\phi \in W^{\perp}$, we have $\phi(v - v') = 0$, which implies $\phi(v) = \phi(v')$. Thus, $\lambda(\phi)$ is well-defined on $V/W$.

2.  **Linearity of $\lambda(\phi)$:** For any $c_1, c_2 \in K$ and $v_1+W, v_2+W \in V/W$:
    $\lambda(\phi)(c_1(v_1+W) + c_2(v_2+W)) = \lambda(\phi)((c_1v_1+c_2v_2)+W) = \phi(c_1v_1+c_2v_2) = c_1\phi(v_1) + c_2\phi(v_2) = c_1\lambda(\phi)(v_1+W) + c_2\lambda(\phi)(v_2+W)$.
    So, $\lambda(\phi)$ is a linear functional on $V/W$, meaning $\lambda(\phi) \in (V/W)^*$.

3.  **Linearity of $\lambda$:** For any $c_1, c_2 \in K$ and $\phi_1, \phi_2 \in W^{\perp}$:
    $\lambda(c_1\phi_1 + c_2\phi_2)(v+W) = (c_1\phi_1 + c_2\phi_2)(v) = c_1\phi_1(v) + c_2\phi_2(v) = c_1\lambda(\phi_1)(v+W) + c_2\lambda(\phi_2)(v+W) = (c_1\lambda(\phi_1) + c_2\lambda(\phi_2))(v+W)$.
    Thus, $\lambda$ is a linear map.

4.  **Injectivity:** Suppose $\lambda(\phi) = 0$ for some $\phi \in W^{\perp}$. This means $\lambda(\phi)(v+W) = 0$ for all $v+W \in V/W$. By definition, $\phi(v) = 0$ for all $v \in V$. Therefore, $\phi = 0$. So, $\mathrm{ker}(\lambda) = \{0\}$, and $\lambda$ is injective.

5.  **Surjectivity:** Let $\psi \in (V/W)^*$. Define a functional $\tilde{\psi}: V \to K$ by $\tilde{\psi}(v) = \psi(v+W)$.
    For any $w \in W$, $\tilde{\psi}(w) = \psi(w+W) = \psi(0_{V/W}) = 0$.
    Thus, $\tilde{\psi} \in W^{\perp}$.
    Now, let's check if $\lambda(\tilde{\psi}) = \psi$.
    $\lambda(\tilde{\psi})(v+W) = \tilde{\psi}(v) = \psi(v+W)$.
    So, $\lambda(\tilde{\psi}) = \psi$, which means $\lambda$ is surjective.

Since $\lambda$ is a well-defined linear, injective, and surjective map, it is an isomorphism.

# 2
Let $V$ be a finite-dimensional vector space, $\dim(V)=n$. For $k \geq 0$, let $G(V, k)$ be the set of all the $k$-dimensional subspaces of $V$ (it is called the Grassmannian of $V$). Show that the correspondence

$W \mapsto W^{\perp}$

is a bijection

$G(V, k) \simeq G(V^*, n-k)$

# 3
Let $V$ and $W$ be two vector spaces, not necessarily finite-dimensional. Consider the map

$V^* \otimes W \rightarrow \mathrm{Hom}_K(V, W): \phi \otimes w \mapsto \phi(-) w$

(the map was considered in class). Prove that the map is an isomorphism if either $V$ or $W$ is finite-dimensional. (In fact, this is an "if and only if"; in general, the map is only injective.)

Proof

Let's call the map $\Psi: V^* \otimes W \to \mathrm{Hom}_K(V, W)$. The map acts on a pure tensor $\phi \otimes w$ to produce a linear map $\Psi(\phi \otimes w): V \to W$ defined by:

$(\Psi(\phi \otimes w))(v) = \phi(v)w$

To show that $\Psi$ is an isomorphism when either $V$ or $W$ is finite-dimensional, we will consider both cases separately.

**Case 1: $V$ is finite-dimensional.**

Let $\dim(V) = n$ and let $`\{v_1, v_2, \ldots, v_n\}`$ be a basis for $V$. Then, the dual basis $`\{\phi_1, \phi_2, \ldots, \phi_n\}`$ of $V^*$ is defined by $\phi_i(v_j) = \delta_{ij}$.

Any linear map $T \in \mathrm{Hom}_K(V, W)$ is determined by its action on the basis vectors of $V$. Specifically, we can write:

$T(v_j) = w_j \in W$ for each $j = 1, 2, \ldots, n$.

Thus, we can express $T$ as:

$T(v) = \sum_{j=1}^n \phi_j(v) w_j$

for any $v \in V$.

This shows that every linear map $T$ can be expressed as a sum of maps of the form $\phi_j \otimes w_j$. Therefore, $\Psi$ is surjective.

To show injectivity, let an arbitrary element $u \in V^* \otimes W$ be in the kernel of $\Psi$. Since $V$ is finite-dimensional, we can fix a basis $`\{\phi'_1, \ldots, \phi'_n\}`$ for $V^*$ and write $`u = \sum_{j=1}^n \phi'_j \otimes w'_j`$ for some unique vectors $w'_j \in W$.

The condition $\Psi(u) = 0$ means $\sum_{j=1}^n \phi'_j(v) w'_j = 0$ for all $v \in V$.

Let $`\{v_1, \ldots, v_n\}`$ be the basis of $V$ dual to $`\{\phi'_1, \ldots, \phi'_n\}`$. Evaluating at $v_k$ for any $`k \in \{1, \ldots, n\}`$ gives:

$\sum_{j=1}^n \phi'_j(v_k) w'_j = w'_k = 0.$

Since this holds for all $k$, all $w'_j$ are zero, which implies $u=0$. Thus, $\Psi$ is injective.

**Case 2: $W$ is finite-dimensional.**

Let $\dim(W) = m$ and let $\{w_1, w_2, \ldots, w_m\}$ be a basis for $W$. Any linear map $T \in \mathrm{Hom}_K(V, W)$ can be expressed in terms of this basis as:

$T(v) = \sum_{j=1}^m \psi_j(v) w_j$

for some linear functionals $\psi_j \in V^*$.

This shows that every linear map $T$ can be expressed as a sum of maps of the form $\phi \otimes w_j$. Therefore, $\Psi$ is surjective.

To show injectivity, let $u = \sum_{i=1}^k \phi_i \otimes w_i$ be an element in the kernel of $\Psi$. We can assume without loss of generality that the vectors $\{w_1, \ldots, w_k\}$ are linearly independent (otherwise, we can rewrite the sum with fewer terms).

The condition $\Psi(u) = 0$ means $\sum_{i=1}^k \phi_i(v) w_i = 0$ for all $v \in V$.

Since $\{w_1, \ldots, w_k\}$ are linearly independent, this implies that for each $i$, the coefficient $\phi_i(v)$ must be zero for all $v \in V$. Thus, each $\phi_i$ is the zero functional, which means $u=0$. The kernel of $\Psi$ is trivial, and $\Psi$ is injective.

# 4
Let $V$ and $W$ be finite-dimensional vector spaces, and let $\phi: V \rightarrow V$ and $\psi: W \rightarrow W$ be linear transformations. Consider the linear transformation

$\phi \otimes \psi: V \otimes W \rightarrow V \otimes W: v \otimes w \mapsto \phi(v) \otimes \psi(w) .$

Find a formula for $\det(\phi \otimes \psi)$. If you want, you can assume that you work over an algebraically closed field.

Proof

We assume the underlying field is algebraically closed, as suggested in the problem statement. This ensures that $\phi$ and $\psi$ have $n$ and $m$ eigenvalues respectively (counting multiplicities).

Let $\dim(V) = n$ and $\dim(W) = m$. Let the eigenvalues of $\phi$ be $\lambda_1, \lambda_2, \ldots, \lambda_n$ and the eigenvalues of $\psi$ be $\mu_1, \mu_2, \ldots, \mu_m$.

The eigenvalues of the tensor product transformation $\phi \otimes \psi$ are given by all possible products of the eigenvalues of $\phi$ and $\psi$. Specifically, the eigenvalues of $\phi \otimes \psi$ are:

$\lambda_i \mu_j$ for $i = 1, 2, \ldots, n$ and $j = 1, 2, \ldots, m$.

The determinant of a linear transformation is the product of its eigenvalues. Therefore, we have:

$\det(\phi \otimes \psi) = \prod_{i=1}^n \prod_{j=1}^m (\lambda_i \mu_j) = \left( \prod_{i=1}^n \lambda_i \right)^m \left( \prod_{j=1}^m \mu_j \right)^n = (\det(\phi))^m (\det(\psi))^n.

# 5
Let $V$ be a finite-dimensional vector space over $\mathbb{C}$, and let $\phi, \psi: V \rightarrow V$ be two linear operators. Prove that there exists a vector $v \in V, v \neq 0$, that is an eigenvector for both $\phi$ and $\psi$ simultaneously. (Consider the restriction of $\psi$ to the eigenspaces of $\phi$.)

# 6
Let $G$ be an abelian group and $V$ be a finite-dimensional irreducible representation of $G$ over $\mathbb{C}$. Show that $\dim(V)=1$. (This is closely related to the previous problem.)

# 7
Let $V_{d, n}$ be the vector space of homogeneous polynomials of degree $d$ in the variables $x_1, \ldots, x_n$. The group $S_n$ acts on $V_{d, n}$ by permuting the variables. Write this representation as a direct sum of irreducibles for $(d, n)=(2,2),(3,1),(3,2)$. (For extra challenge, try $(3,3)$ : it can be done by brute force, but it is not fun.)
