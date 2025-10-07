# 1
Let $M$ be a nonempty smooth compact manifold. Show that there is no smooth submersion $F\colon M \to \mathbb{R}$.

Proof

Since $M$ is a compact manifold and $F$ is a smooth map, its image $F(M)$ is a compact subset of $\mathbb{R}$. As $M$ is non-empty, $F(M)$ must attain a maximum value at some point $p \in M$. At this maximum, $p$ is a critical point of $F$, meaning its differential $dF_p$ is not surjective. This contradicts the definition of a submersion, which requires $dF_p$ to be surjective for all $p \in M$.

# 2
Let $`M=\mathrm{SL}(n, \mathbb{R}))=\{A \in \mathrm{GL}(n, \mathbb{R}) \mid \det(A)=1\}`$. Show that $M$ is a smooth manifold.

# 3
Show that $F\colon\mathbb{R} \times\left(-\frac{1}{2}, \frac{1}{2}\right) \to \mathbb{R}^3$ induces a smooth embedding of the Möbius strip in $\mathbb{R}^3$.

$`\begin{aligned}
F\colon(u, v) & =\left(\left(1+v \cos \frac{u}{2}\right) \cos u,\left(1+v \cos \frac{u}{2}\right) \sin u, v \sin \frac{u}{2}\right) \\
& =\left(1+v \cos \frac{u}{2}\right)(\cos u, \sin u, 0)+\left(0,0, v \sin \frac{u}{2}\right)
\end{aligned}`$

Note: You can think of the Möbius strip as a quotient of $\mathbb{R} \times\left(-\frac{1}{2}, \frac{1}{2}\right)$.

# 4
Note that $P(X, Y, Z, W)=X^2+Z^2-Y^2-W^2$ is a homogeneous polynomial. Consider the hypersurface $S \subset \mathbb{R P}^3$ defined by $P(X, Y, Z, W)=0$. (This makes sense since $P$ is homogeneous.)

Prove that $S$ is an embedded torus. (Hint: Start with $\tilde{S} \in S^3 \subset \mathbb{R}^4$ defined by the same polynomial.)

# 5
Let $\pi\colon K^{n+1} \backslash\{0\} \to K \mathbb{P}^n$ be the canonical projection for $K=\mathbb{R}, \mathbb{C}$.
<ol type="a">
<li>  

Prove that $\pi$ is a submersion.
</li>
<li>  
Let $\pi_0$ be the restriction of $\pi$ to the sphere $S^n$, for $K=\mathbb{R}$, or $S^{2 n+1}$, for $K=\mathbb{C}$. Prove that $\pi_0$ is also a submersion.

  Hint: To prove (b) using (a), it suffices to show that the kernel of $d \pi$ is not contained in the tangent space to the sphere.
</li>
</ol>
