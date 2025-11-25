# 13
Verify that $f \simeq g$ implies $`f_*=g_*`$ for induced homomorphisms of reduced homology groups.

Proof

Given a homotopy $F: X \times I \rightarrow Y$ from $f$ to $g$ and a singular simplex $\sigma: \Delta^n \rightarrow X$, we can form the composition $F \circ(\sigma \times \mathbb{1}): \Delta^n \times I \rightarrow X \times I \rightarrow Y$. Using this, we can define prism operators $P: C_n(X) \rightarrow C_{n+1}(Y)$. These prism operators satisfy the basic relation

$$ \partial P = g_{\sharp} - f_{\sharp} - P \partial $$

which implies that for a cycle $c$ (where $\partial c = 0$), $f_{\sharp}(c)$ and $g_{\sharp}(c)$ are homologous because their difference is a boundary: $g_{\sharp}(c) - f_{\sharp}(c) = \partial(P(c))$. Therefore:

$`f_*([c]) = [f_{\sharp}(c)] = [g_{\sharp}(c)] = g_*([c])`$

# 16
<ol type="a">
<li>

Show that $H_0(X, A)=0$ iff $A$ meets each path-component of $X$.
</li>
<li>
  
Show that $H_1(X, A)=0$ iff $H_1(A) \rightarrow H_1(X)$ is surjective and each path-component of $X$ contains at most one path-component of $A$.
</li>
</ol>

# 17
<ol type="a">
<li>

Compute the homology groups $H_n(X, A)$ when $X$ is $S^2$ or $S^1 \times S^1$ and $A$ is a finite set of points in $X$.
</li>
<li>

Compute the groups $H_n(X, A)$ and $H_n(X, B)$ for $X$ a closed orientable surface of genus two with $A$ and $B$ the circles shown. [What are $X / A$ and $X / B$?]
</li>
</ol>

# 23
Show that the second barycentric subdivision of a $\Delta$-complex is a simplicial complex.

Namely, show that the first barycentric subdivision produces a $\Delta$-complex with the property that each simplex has all its vertices distinct, then show that for a $\Delta$-complex with this property, barycentric subdivision produces a simplicial complex.

# 29
Show that $S^1 \times S^1$ and $S^1 \vee S^1 \vee S^2$ have isomorphic homology groups in all dimensions, but their universal covering spaces do not.
