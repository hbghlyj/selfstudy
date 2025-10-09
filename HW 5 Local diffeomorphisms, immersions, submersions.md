# 1
Let $M$ be a nonempty smooth compact manifold. Show that there is no smooth submersion $F\colon M \to \mathbb{R}$.

Proof

Since $M$ is a compact manifold and $F$ is a smooth map, its image $F(M)$ is a compact subset of $\mathbb{R}$. As $M$ is non-empty, $F(M)$ must attain a maximum value at some point $p \in M$. At this maximum, $p$ is a critical point of $F$, meaning its differential $dF_p$ is not surjective. This contradicts the definition of a submersion, which requires $dF_p$ to be surjective for all $p \in M$.

# 2
Let $`M=\mathrm{SL}(n, \mathbb{R}))=\{A \in \mathrm{GL}(n, \mathbb{R}) \mid \det(A)=1\}`$. Show that $M$ is a smooth manifold.

Proof

The determinant map $\det\colon \mathrm{GL}(n, \mathbb{R}) \to \mathbb{R}^*$ is smooth and surjective,

$d(\det)_A(H) = \det(A) \mathrm{tr}(A^{-1}H)$

Since $\det(A) \neq 0$ for any $A \in \mathrm{GL}(n, \mathbb{R})$, the differential $d(\det)_A$ is always surjective.

Thus, the determinant map $\det\colon \mathrm{GL}(n, \mathbb{R}) \to \mathbb{R}^*$ is a submersion.

By Corollary 5.13 (Submersion Level Set Theorem), the preimage $\mathrm{SL}(n, \mathbb{R}) = \det^{-1}(1)$ is a smooth submanifold of $\mathrm{GL}(n, \mathbb{R})$ of codimension 1.

# 3
Show that $F\colon\mathbb{R} \times\left(-\frac{1}{2}, \frac{1}{2}\right) \to \mathbb{R}^3$ induces a smooth embedding of the Möbius strip in $\mathbb{R}^3$.

$`\begin{aligned}
F\colon(u, v) & =\left(\left(1+v \cos \frac{u}{2}\right) \cos u,\left(1+v \cos \frac{u}{2}\right) \sin u, v \sin \frac{u}{2}\right) \\
& =\left(1+v \cos \frac{u}{2}\right)(\cos u, \sin u, 0)+\left(0,0, v \sin \frac{u}{2}\right)
\end{aligned}`$

Note: You can think of the Möbius strip as a quotient of $\mathbb{R} \times\left(-\frac{1}{2}, \frac{1}{2}\right)$.

Proof

$`F(u+2\pi, -v) = \left(\left(1-v \cos \frac{u+2\pi}{2}\right) \cos(u+2\pi),\left(1-v \cos \frac{u+2\pi}{2}\right) \sin(u+2\pi), -v \sin \frac{u+2\pi}{2}\right)=F(u,v)`$

so $F$ respects the identification $(u, v) \sim (u + 2\pi, -v)$, so it induces a well-defined map from the Möbius strip into $\mathbb{R}^3$.

$\tilde{F}([u, v]) = F(u,v)$.

To show that $F$ induces an embedding, we need to check that it is a smooth immersion and that the induced map is a homeomorphism onto its image.

1. **Smooth Immersion**: We compute the differential $`d\tilde{F}_{(u, v)}\colon T_{(u, v)}\left(\mathbb{R} \times\left(-\frac{1}{2}, \frac{1}{2}\right)\right) \to T_{\tilde{F}(u, v)}\mathbb{R}^3`$. The Jacobian matrix of $\tilde{F}$ is given by

$`d\tilde{F}_{(u, v)}=\begin{pmatrix}
    -\frac{1}{2} v \cos(u) \sin(u/2) - (1 + v \cos(u/2)) \sin(u) & \cos(u/2) \cos(u) \\
    \cos(u) + v \cos(u/2) \cos(u) - \frac{1}{2} v \sin(u/2) \sin(u) & \cos(u/2) \sin(u) \\
    \frac{1}{2} v \cos(u/2) & \sin(u/2)
\end{pmatrix}`$.

2. **Homeomorphism onto Image**: To complete the proof, we must show the induced map on the Möbius strip is a homeomorphism onto its image. This requires proving that the map is injective on the quotient space and is a proper map.

# 4
Note that $P(X, Y, Z, W)=X^2+Z^2-Y^2-W^2$ is a homogeneous polynomial. Consider the hypersurface $S \subset \mathbb{R P}^3$ defined by $P(X, Y, Z, W)=0$. (This makes sense since $P$ is homogeneous.)

Prove that $S$ is an embedded torus. (Hint: Start with $\tilde{S} \in S^3 \subset \mathbb{R}^4$ defined by the same polynomial.)

Proof

We start by considering the set $`\tilde{S} = \{(X, Y, Z, W) \in S^3 \subset \mathbb{R}^4 \mid P(X, Y, Z, W) = 0\}`$.

The equation $P(X, Y, Z, W) = 0$ can be rewritten as $X^2 + Z^2 = Y^2 + W^2$. But since we are on the unit sphere $S^3$, we also have $X^2 + Y^2 + Z^2 + W^2 = 1$. Combining these two equations, we find that $X^2 + Z^2 = \frac{1}{2}$ and $Y^2 + W^2 = \frac{1}{2}$.

This describes a product of two circles, each of radius $\frac{1}{\sqrt{2}}$, which is topologically a torus $S^1 \times S^1$.

The projection map $\pi\colon S^3 \to \mathbb{R P}^3$ is a 2-to-1 covering map that identifies antipodal points. The set $\tilde{S}$ is invariant under the antipodal map, since $P(-v) = P(v)$ for any $v \in \mathbb{R}^4$. The antipodal map has no fixed points on $\tilde{S}$. The induced map from the quotient manifold $`\tilde{S}/\{\pm I\}`$ to $\mathbb{R P}^3$ is an injective immersion from a compact space, hence a smooth embedding. Therefore, $S$ is a smooth embedded submanifold of $\mathbb{R P}^3$.

To show $S$ is a torus, we identify the quotient manifold. On $\tilde{S} \cong S^1 \times S^1$, the antipodal map corresponds to $(\theta_1, \theta_2) \mapsto (\theta_1+\pi, \theta_2+\pi)$ in angular coordinates. The quotient of the torus $S^1 \times S^1$ by this fixed-point-free involution is diffeomorphic to a torus. Thus, $S$ is an embedded torus in $\mathbb{R P}^3$.

# 5
Let $`\pi\colon K^{n+1} \backslash\{0\} \to K \mathbb{P}^n`$ be the canonical projection for $K=\mathbb{R}, \mathbb{C}$.
<ol type="a">
<li>  

Prove that $\pi$ is a submersion.
</li>
<li>  
Let $\pi_0$ be the restriction of $\pi$ to the sphere $S^n$, for $K=\mathbb{R}$, or $S^{2 n+1}$, for $K=\mathbb{C}$. Prove that $\pi_0$ is also a submersion.

  Hint: To prove (b) using (a), it suffices to show that the kernel of $d \pi$ is not contained in the tangent space to the sphere.
</li>
</ol>
