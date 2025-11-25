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

Proof

<ol type="a">
<li>

From the long exact sequence of the pair $(X, A)$, we have the segment

$$ \cdots \rightarrow H_1(X, A) \rightarrow H_0(A) \xrightarrow{i_*} H_0(X) \rightarrow H_0(X, A) \rightarrow 0 $$

If $H_0(X, A) = 0$, then the map $`i_*`$ is surjective. Since $H_0(X)$ is a free abelian group with rank equal to the number of path-components of $X$, for $i_*$ to be surjective, each path-component of $X$ must contain at least one point from $A$.

Conversely, if $A$ meets each path-component of $X$, then $`i_*: H_0(A) \to H_0(X)`$ is surjective. From the exactness of the sequence $`H_0(A) \xrightarrow{i_*} H_0(X) \to H_0(X, A) \to 0`$, surjectivity of $i_*$ implies the map $H_0(X) \to H_0(X,A)$ is the zero map. Since this map is also surjective (by exactness), $H_0(X,A)$ must be 0.
</li>
<li>

From the long exact sequence of the pair $(X, A)$, we have the segment

$`\cdots \rightarrow H_1(A) \xrightarrow{i_*} H_1(X) \xrightarrow{j_*} H_1(X, A) \xrightarrow{\partial_*} H_0(A) \xrightarrow{i_*} H_0(X) \rightarrow \cdots`$

If $H_1(X, A) = 0$, then from the exact sequence, the map $i_*: H_1(A) \to H_1(X)$ is surjective, and the map $i_*: H_0(A) \to H_0(X)$ is injective. The injectivity of the latter map implies that each path-component of $X$ contains at most one path-component of $A$.

Conversely, if $H_1(A) \rightarrow H_1(X)$ is surjective and each path-component of $X$ contains at most one path-component of $A$, then $`i_*: H_1(A) \to H_1(X)`$ is surjective and $i_*: H_0(A) \to H_0(X)$ is injective. From the exact sequence, this means the map $`j_*: H_1(X) \to H_1(X,A)`$ is zero, and the map $`\partial_*: H_1(X,A) \to H_0(A)`$ is zero. Exactness at $H_1(X,A)$ implies $`\text{Im}(j_*) = \ker(\partial_*)`$, so $0 = H_1(X,A)$.
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
