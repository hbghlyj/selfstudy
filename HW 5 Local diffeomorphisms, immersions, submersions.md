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
    
    The rank of this matrix is 2 for all $(u, v)$ in the domain, which can be verified by checking that the determinant of any 2x2 minor is non-zero. Thus, $d\tilde{F}_{(u, v)}$ is injective, and $\tilde{F}$ is a smooth immersion.

    $`\begin{vmatrix}
    -\frac{1}{2} v \cos(u) \sin(u/2) - (1 + v \cos(u/2)) \sin(u) & \cos(u/2) \cos(u) \\
    \frac{1}{2} v \cos(u/2) & \sin(u/2)
    \end{vmatrix} = -\frac{1}{2}v\cos(u) - \sin(u)\sin(u/2)(1 + v\cos(u/2))`$

2. **Homeomorphism onto Image**: To show an embedding, we must prove $\tilde{F}$ is a homeomorphism onto its image. This requires showing both that the map is **injective** (i.e., if $F(u_1, v_1) = F(u_2, v_2)$ then $[u_1, v_1] = [u_2, v_2]$) and that it is a **proper map**.

    - **Injectivity**: Suppose $F(u_1, v_1) = F(u_2, v_2)$. From the first two components, we can deduce that $u_1 = u_2 + 2k\pi$ for some integer $k$. Substituting this into the equations for all three components, we find that we must have $v_2 = (-1)^k v_1$. The condition for points to be identified by $F$ is $(u_2, v_2) = (u_1 - 2k\pi, (-1)^k v_1)$, which is precisely the equivalence relation for the Möbius strip. Thus, the induced map is injective.
    - **Properness**: The induced map $\tilde{F}$ is proper if we consider the compact Möbius strip, constructed as a quotient of the rectangle $[0, 2\pi] \times [-\frac{1}{2}, \frac{1}{2}]$. A continuous map from a compact space to a Hausdorff space (like $\mathbb{R}^3$) is always proper. This is because the preimage of a compact set is closed, and a closed subset of a compact space is compact. Therefore, $\tilde{F}$ is a proper map.

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

Proof
<ol type="a">
<li>

For the case $K=\mathbb{R}$, we work on the open set $`U = \{(x_1, \ldots, x_{n+1}) \in \mathbb{R}^{n+1} \mid x_{n+1} > 0\}`$. We introduce a coordinate change on $U$ via the map $\phi: U \to \mathbb{R}^n \times \mathbb{R}^+$:

$`\phi(x_1, \ldots, x_{n+1}) = (\frac{x_1}{x_{n+1}}, \ldots, \frac{x_n}{x_{n+1}}, \sqrt{x_1^2 + \cdots + x_n^2 + x_{n+1}^2})`$.

Local coordinates on $K \mathbb{P}^n$ are given by the map

$`\psi\colon \{[x_1, \ldots, x_{n+1}] \in K \mathbb{P}^n \mid x_{n+1} \neq 0\} \to K^n`$

$`\psi([x_1, \ldots, x_{n+1}]) = (\frac{x_1}{x_{n+1}}, \ldots, \frac{x_n}{x_{n+1}})`$.

In these coordinates, the map $\pi$ is given by

$`\psi \circ \pi \circ \phi^{-1}(y_1, \ldots, y_n, r) = (y_1, \ldots, y_n)`$.

The differential of this map is

$`d(\psi \circ \pi \circ \phi^{-1})_{(y_1, \ldots, y_n, r)} = \begin{pmatrix}
1 & 0 & \cdots & 0 & 0 \\
0 & 1 & \cdots & 0 & 0 \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & \cdots & 1 & 0
\end{pmatrix}`$.

This matrix has full rank $n$, so the differential is surjective. Since this holds in local coordinates, $\pi$ is a submersion.
</li>
<li>
The kernel of $d\pi_v$ for $v \in K^{n+1} \backslash \{0\}$ is the line spanned by $v$. The tangent space to the sphere at $v$ is the hyperplane orthogonal to $v$. Since the line spanned by $v$ is not contained in this hyperplane, the kernel of $d\pi_v$ is not contained in the tangent space to the sphere. Therefore, the restriction $\pi_0$ is also a submersion.
</li></ol>
