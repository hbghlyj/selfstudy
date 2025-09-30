# 1
Show that the map $`\mathbb{R}_p^n \to T_p \mathbb{R}^n`$ given by $\left.\vec{v} \mapsto D_{\vec{v}}\right|_p$ is surjective. i.e that every derivation comes from a directional derivative. (Hint: To find $\vec{v}$ apply $w \in T_p \mathbb{R}^n$ to the coordinate functions. Then for any smooth function $f$ use Taylor's theorem on $f$ and the Leibniz property.)
# 2
Prove Proposition 3.6 from Lee (Properties of Differentials). Let $M, N$, and $P$ be smooth manifolds, let $F: M \to N$ and $G: N \to P$ be smooth maps, and let $p \in M$.
<ol type="a">
<li>
  $d F_p: T_p M \to T_{F(p)} N$ is linear.
</li>
<li>
  $d(G \circ F)_p=d G_{F(p)} \circ d F_p: T_p M \to T_{G(F(p))} P$.
</li>
<li>
  $d\left(\text{Id}_M\right)_p=\text{Id}_{T_p M}: T_p M \to T_p M$.
</li>
<li>
  If $F$ is a diffeomorphism, then $d F_p: T_p M \to T_{F(p)} N$ is an isomorphism, and
  
  $(d F_p)^{-1}=d(F^{-1})_{F(p)}$
</li>
</ol>

# 3
Note that if $M$ is a smooth manifold and $U$ is an open subset then $U$ is also a smooth manifold with smooth structure from $M$ (i.e. charts on U are given by intersecting $U$ with charts on $M$ ). We say $U$ is an open submanifold of $M$. Show that for $p \in U$ there is an isomorphism $T_p M$ to $T_p U$.
# 4
Show that for a vector space $V$ (with its canonical smooth structure) and any point $p \in V$, the tangent space $T_p V$ is canonically isomorphic to $V$.
# 5
Let $(x, y)$ denote the standard coordinates on $\mathbb{R}^2$. Verify that $(\tilde{x}, \tilde{y})$ are global smooth coordinates on $\mathbb{R}^2$, where

$\tilde{x}=x, \quad \tilde{y}=y+x^3$

Let $p$ be the point $(1,0) \in \mathbb{R}^2$ (in standard coordinates), and show that

$\left.\frac{\partial}{\partial x}\right|_p \neq\left.\frac{\partial}{\partial \tilde{x}}\right|_p$
