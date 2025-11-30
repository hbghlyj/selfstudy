# 13
Verify that   implies $`f_*=g_*`$ for induced homomorphisms of reduced homology groups.

Proof

Given a homotopy     from  to  and a singular simplex   , we can form the composition        . Using this, we can define prism operators   . These prism operators satisfy the basic relation



which implies that for a cycle  (where  ),  and  are homologous because their difference is a boundary:   . Therefore:

$`f_*([c]) = [f_{\sharp}(c)] = [g_{\sharp}(c)] = g_*([c])`$

# 16
<ol type="a">
<li>

Show that   iff  meets each path-component of .
</li>
<li>
  
Show that   iff   is surjective and each path-component of  contains at most one path-component of .
</li>
</ol>

Proof

<ol type="a">
<li>

From the long exact sequence of the pair , we have the segment

     

If  , then the map  is surjective. Since  is a free abelian group with rank equal to the number of path-components of , for  to be surjective, each path-component of  must contain at least one point from .

Conversely, if  meets each path-component of , then    is surjective. From the exactness of the sequence    , surjectivity of  implies the map   is the zero map. Since this map is also surjective (by exactness),  must be 0.
</li>
<li>

From the long exact sequence of the pair , we have the segment

      

If  , then from the exact sequence, the map    is surjective, and the map    is injective. The injectivity of the latter map implies that each path-component of  contains at most one path-component of .

Conversely, if   is surjective and each path-component of  contains at most one path-component of , then    is surjective and    is injective. From the exact sequence, this means the map    is zero, and the map    is zero. Exactness at  implies  , so  .
</li>
</ol>

# 17
<ol type="a">
<li>

Compute the homology groups  when  is  or   and  is a finite set of points in .
</li>
<li>

Compute the groups  and  for  a closed orientable surface of genus two with  and  the circles shown. [What are  and ?]
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

# 29
Show that $S^1 \times S^1$ and $S^1 \vee S^1 \vee S^2$ have isomorphic homology groups in all dimensions, but their universal covering spaces do not.

Proof

Both spaces have the same homology groups:

$`H_n(S^1 \times S^1) \cong \begin{cases} \mathbb{Z} & n = 0 \\ \mathbb{Z}^2 & n = 1 \\ \mathbb{Z} & n = 2 \\ 0 & \text{otherwise} \end{cases}`$

$`H_n(S^1 \vee S^1 \vee S^2) \cong \begin{cases} \mathbb{Z} & n = 0 \\ \mathbb{Z}^2 & n = 1 \\ \mathbb{Z} & n = 2 \\ 0 & \text{otherwise} \end{cases}`$

The universal covering spaces are

$`U(S^1 \times S^1) = \mathbb{R}^2`$

$`U(S^1 \vee S^1 \vee S^2) = \mathbb{R}^2 \vee \bigvee_{\alpha \in \pi_1(S^1 \vee S^1)} S^2_{\alpha}`$

where $\pi_1(S^1 \vee S^1)$ is the free group on two generators, which is infinite. Thus, $U(S^1 \vee S^1 \vee S^2)$ has infinitely many $S^2$ components, while $U(S^1 \times S^1)$ is simply $\mathbb{R}^2$. Therefore, the universal covering spaces are not homotopy equivalent, despite having isomorphic homology groups.
