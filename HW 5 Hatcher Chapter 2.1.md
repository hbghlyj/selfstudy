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

$`\cdots \rightarrow H_1(X, A) \rightarrow H_0(A) \xrightarrow{i_*} H_0(X) \rightarrow H_0(X, A) \rightarrow 0`$

If $H_0(X, A) = 0$, then the map $`i_*`$ is surjective. Since $H_0(X)$ is a free abelian group with rank equal to the number of path-components of $X$, for $i_*$ to be surjective, each path-component of $X$ must contain at least one point from $A$.

Conversely, if $A$ meets each path-component of $X$, then $`i_*: H_0(A) \to H_0(X)`$ is surjective. From the exactness of the sequence $`H_0(A) \xrightarrow{i_*} H_0(X) \to H_0(X, A) \to 0`$, surjectivity of $i_*$ implies the map $H_0(X) \to H_0(X,A)$ is the zero map. Since this map is also surjective (by exactness), $H_0(X,A)$ must be 0.
</li>
<li>

From the long exact sequence of the pair $(X, A)$, we have the segment

$`\cdots \rightarrow H_1(A) \xrightarrow{i_*} H_1(X) \xrightarrow{j_*} H_1(X, A) \xrightarrow{\partial_*} H_0(A) \xrightarrow{i_*} H_0(X) \rightarrow \cdots`$

If $H_1(X, A) = 0$, then from the exact sequence, the map $`i_*: H_1(A) \to H_1(X)`$ is surjective, and the map $i_*: H_0(A) \to H_0(X)$ is injective. The injectivity of the latter map implies that each path-component of $X$ contains at most one path-component of $A$.

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

Proof

<ol type="a">
<li>

The pair $(S^2, A)$, where $A$ is a finite set of points, is a good pair, so $`H_n(S^2, A) \cong \tilde{H}_n(S^2/A)`$. The quotient space $S^2/A$ is homotopy equivalent to $S^2 \vee (\bigvee_{|A|-1} S^1)$. Therefore, the homology groups are:

$`H_n(S^2, A) \cong \begin{cases} \mathbb{Z} & n = 2 \\ \mathbb{Z}^{|A| - 1} & n = 1 \\ 0 & \text{otherwise} \end{cases}`$

For the pair $(S^1 \times S^1, A)$, the quotient space $(S^1 \times S^1)/A$ is homotopy equivalent to $(S^1 \times S^1) \vee (\bigvee_{|A|-1} S^1)$. Thus, the homology groups are:

$`H_n(S^1 \times S^1, A) \cong \begin{cases} \mathbb{Z} & n = 2 \\ \mathbb{Z}^{|A|+1} & n = 1 \\ 0 & \text{otherwise} \end{cases}`$
</li>
<li>

For the pair $(X, A)$, where $A$ is a non-separating circle on the genus-2 surface $X$, the quotient space $X/A$ is homotopy equivalent to $(S^1 \times S^1) \vee S^1$. Since $(X,A)$ is a good pair, the relative homology groups are:

$`H_n(X, A) \cong \tilde{H}_n(X/A) \cong \begin{cases} \mathbb{Z} & n = 2 \\ \mathbb{Z}^3 & n = 1 \\ 0 & \text{otherwise} \end{cases}`$

For the pair $(X, B)$, where $B$ is a separating circle, the quotient space $X/B$ is homotopy equivalent to $(S^1 \times S^1) \vee (S^1 \times S^1)$. Thus, the homology groups are:

$`H_n(X, B) \cong \tilde{H}_n(X/B) \cong \begin{cases} \mathbb{Z}^2 & n = 2 \\ \mathbb{Z}^4 & n = 1 \\ 0 & \text{otherwise} \end{cases}`$

</li>
</ol>

# 23
Show that the second barycentric subdivision of a $\Delta$-complex is a simplicial complex.

Namely, show that the first barycentric subdivision produces a $\Delta$-complex with the property that each simplex has all its vertices distinct, then show that for a $\Delta$-complex with this property, barycentric subdivision produces a simplicial complex.

Proof

From the definitions in the book, "A simplicial complex is a $\Delta$-complex such that all the vertices for any given simplex are distinct and if two simplices have the same set of vertices, then they are the same simplex." Let us first show that barycentric subdivision leads to a $\Delta$-complex such that each simplex has distinct vertices. Note that $B(X)$ for a $\Delta$-complex $X$ simply means "the barycentric subdivision of $X$."

> Claim. Given a $\Delta$-complex $X$ with $k$-simplices (i.e. $k$-skeleton) $X^k$, then $B\left(X^k\right)$ is comprised of simplices with distinct vertices.

Proof. The vertices of any simplex in $B(X)$ are, by definition, the barycenters of a chain of strictly nested faces of $X$. Since the faces in the chain are all distinct, their barycenters are distinct, and thus the vertices of any simplex in $B(X)$ are distinct.

> Claim. Given a $\Delta$-complex $X$ such that each $k$-simplex has its vertices distinct, then $B(X)$ is a simplicial complex.

Proof. Let $X^n$ be the $n$-skeleton of $X$. We proceed by induction.

Base Case:

By hypothesis, $X^1$ comprises 1-simplices $X_i^1$. Suppose that $X_i^1, X_j^1$ are 1-simplices such that $`\partial X_i^1=\partial X_j^1=\{a, b\}`$ for some $a, b \in X^0$. Under barycentric subdivision, for each $X_k^1$ (where $k \in \{i, j\}$), we introduce a barycenter $c_k \in X_k^1$. The barycentric subdivision of $X_k^1$ consists of two 1-simplices: $[a, c_k]$ and $[c_k, b]$. Since $c_i \neq c_j \neq a \neq b$, this implies that $B\left(X_i^1\right)$ has distinct vertices and simplices are determined by their vertex sets. Thus $B\left(X^1\right)$ is a simplicial complex.

Inductive Step:

Assume that $B(X^{n-1})$ is a simplicial complex. We must show that $B(X^n)$ is a simplicial complex. Since we have already established that vertices in any simplex of $B(X)$ are distinct, we only need to show that any simplex in $B(X^n)$ is uniquely determined by its vertex set.

Let $\sigma$ be an $n$-simplex in $X^n$ with barycenter $b_\sigma$. The barycentric subdivision $B(\sigma)$ is defined as the cone with apex $b_\sigma$ over the barycentric subdivision of its boundary, $B(\partial \sigma)$. That is, every simplex $\tau$ in $B(\sigma)$ is of the form $[b_\sigma, \rho]$, where $\rho$ is a simplex in $B(\partial \sigma)$.

Suppose $\tau_1, \tau_2$ are two simplices in $B(X^n)$ that share the same vertex set $V$.

1.  **Case 1:** $V$ contains no barycenters of any $n$-simplices.
    Then $\tau_1$ and $\tau_2$ must lie entirely within $B(X^{n-1})$. By the inductive hypothesis, $B(X^{n-1})$ is a simplicial complex, so $\tau_1 = \tau_2$.

2.  **Case 2:** $V$ contains a barycenter $b_\sigma$ of an $n$-simplex $\sigma$.
    Because simplices in $B(X)$ correspond to chains of strictly nested faces, a simplex can contain at most one barycenter of an $n$-simplex (since no two $n$-simplices can be properly nested). Thus, both $\tau_1$ and $\tau_2$ must belong to the subdivision of the same $n$-simplex $\sigma$.
    
    We can write $\tau_1 = [b_\sigma, \rho_1]$ and $\tau_2 = [b_\sigma, \rho_2]$, where $\rho_1, \rho_2$ are simplices in $B(\partial \sigma)$. The vertex set $V$ is the disjoint union $\{b_\sigma\} \cup V'$, where $V'$ is the vertex set of both $\rho_1$ and $\rho_2$.
    
    Since $\partial \sigma \subset X^{n-1}$, we know $\rho_1, \rho_2 \in B(X^{n-1})$. By the inductive hypothesis, simplices in $B(X^{n-1})$ are determined by their vertices. Therefore, $\rho_1 = \rho_2$.
    
    This implies $\tau_1 = [b_\sigma, \rho_1] = [b_\sigma, \rho_2] = \tau_2$.

Since simplices are uniquely determined by their vertices, $B(X^n)$ is a simplicial complex.

Therefore, $B(X)$ is a simplicial complex by induction. Any $\Delta$-complex can be transformed into a simplicial complex via two subsequent barycentric subdivisions.

# 29
Show that $S^1 \times S^1$ and $S^1 \vee S^1 \vee S^2$ have isomorphic homology groups in all dimensions, but their universal covering spaces do not.

Proof

Both spaces have the same homology groups. The homology of the torus $S^1 \times S^1$ is found using the Künneth formula, and the homology of the wedge sum $S^1 \vee S^1 \vee S^2$ is found using the property of homology for wedge sums of good pairs:

$`H_n(S^1 \times S^1) \cong \begin{cases} \mathbb{Z} & n = 0 \\ \mathbb{Z}^2 & n = 1 \\ \mathbb{Z} & n = 2 \\ 0 & \text{otherwise} \end{cases}`$

$`\tilde{H}_n(S^1 \vee S^1 \vee S^2) \cong \tilde{H}_n(S^1) \oplus \tilde{H}_n(S^1) \oplus \tilde{H}_n(S^2) \implies H_n(S^1 \vee S^1 \vee S^2) \cong \begin{cases} \mathbb{Z} & n = 0 \\ \mathbb{Z}^2 & n = 1 \\ \mathbb{Z} & n = 2 \\ 0 & \text{otherwise} \end{cases}`$

The universal covering spaces are

$`U(S^1 \times S^1) = \mathbb{R}^2`$

$`U(S^1 \vee S^1 \vee S^2)`$ is the universal cover of $S^1 \vee S^1$ (an infinite tree) with an $S^2$ attached at each vertex.

These two universal covering spaces are not homeomorphic. For example, $\mathbb{R}^2$ is contractible, so its homology groups are trivial for $n>0$. The universal cover of $S^1 \vee S^1 \vee S^2$ is an infinite wedge of 2-spheres, so its second homology group is a free abelian group on infinitely many generators. Since their homology groups differ, they are not homotopy equivalent, and therefore not homeomorphic.
