# 1
Let $V$ be a finite-dimensional vector space. For any subspace $W \subset V$, put

$`W^{\perp}:=\left\{\phi \in V^*:\phi|_W=0\right\}`$

Construct natural isomorphisms $W^* \simeq V^* / W^{\perp}$ and $(V / W)^* \simeq W^{\perp}$. (The assumption that $V$ is finite-dimensional is not actually required, but it makes the problem easier.)

Proof

First, we will construct the isomorphism $W^* \simeq V^* / W^{\perp}$.

Consider the natural restriction map $`\rho: V^* \to W^*$ defined by

$`\rho(\phi) = \phi|_W`$

for any $\phi \in V^*$.

The kernel of this map is precisely $W^{\perp}$, since these are the functionals that vanish on $W$. By the First Isomorphism Theorem, we have

$V^* / W^{\perp} \simeq \mathrm{Im}(\rho) = W^*$.

Next, we will construct the isomorphism $`(V / W)^* \simeq W^{\perp}`$. Consider the natural projection map $\pi: V \to V / W$ defined by

$\pi(v) = v + W$

for any $v \in V$.

Any functional $\psi \in (V / W)^*$ can be lifted to a functional $`\tilde{\psi} \in V^*`$ by defining

$\tilde{\psi}(v) = \psi(\pi(v))$.

The kernel of this lifting map consists of those functionals in $V^*$ that vanish on $W$, which is exactly $W^{\perp}$. Thus, we have

$(V / W)^* \simeq W^{\perp}$.

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
$$ (\Psi(\phi \otimes w))(v) = \phi(v)w $$

# 4
Let $V$ and $W$ be finite-dimensional vector spaces, and let $\phi: V \rightarrow V$ and $\psi: W \rightarrow W$ be linear transformations. Consider the linear transformation

$\phi \otimes \psi: V \otimes W \rightarrow V \otimes W: v \otimes w \mapsto \phi(v) \otimes \psi(w) .$

Find a formula for $\det(\phi \otimes \psi)$. If you want, you can assume that you work over an algebraically closed field.

# 5
Let $V$ be a finite-dimensional vector space over $\mathbb{C}$, and let $\phi, \psi: V \rightarrow V$ be two linear operators. Prove that there exists a vector $v \in V, v \neq 0$, that is an eigenvector for both $\phi$ and $\psi$ simultaneously. (Consider the restriction of $\psi$ to the eigenspaces of $\phi$.)

# 6
Let $G$ be an abelian group and $V$ be a finite-dimensional irreducible representation of $G$ over $\mathbb{C}$. Show that $\dim(V)=1$. (This is closely related to the previous problem.)

# 7
Let $V_{d, n}$ be the vector space of homogeneous polynomials of degree $d$ in the variables $x_1, \ldots, x_n$. The group $S_n$ acts on $V_{d, n}$ by permuting the variables. Write this representation as a direct sum of irreducibles for $(d, n)=(2,2),(3,1),(3,2)$. (For extra challenge, try $(3,3)$ : it can be done by brute force, but it is not fun.)
