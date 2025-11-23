# 13
Let $X$ be the 2-complex obtained from $S^1$ with its usual cell structure by attaching two 2-cells by maps of degrees 2 and 3, respectively.
<ol type="a">
<li>

Compute the homology groups of all the subcomplexes $A \subset X$ and the corresponding quotient complexes $X / A$.
</li>
<li>

Show that $X \simeq S^2$ and that the only subcomplex $A \subset X$ for which the quotient map $X \rightarrow X / A$ is a homotopy equivalence is the trivial subcomplex, the 0-cell.
</li>
</ol>
Solution:
<ol type="a">
<li>

To compute the homology groups of all the subcomplexes $A \subset X$ and the corresponding quotient complexes $X / A$, we first identify the subcomplexes of $X$. The complex $X$ consists of a 0-cell (point), a 1-cell (circle), and two 2-cells attached to the 1-cell via maps of degrees 2 and 3.

All subcomplexes $A$ of $X$ are:
1. The trivial subcomplex (0-cell only).
2. The 1-cell (the circle).
3. One of the 2-cells.
4. Both 2-cells (the entire complex $X$).

Now, we compute the homology groups for each subcomplex $A$ and the corresponding quotient complexes $X / A$:
1. For the trivial subcomplex:

   $H_0(A) \cong \mathbb{Z}$, $H_n(A) = 0$ for $n > 0$.
2. For the 1-cell:

   $H_0(A) \cong \mathbb{Z}$, $H_1(A) \cong \mathbb{Z}$, $H_n(A) = 0$ for $n > 1$.
3. For one of the 2-cells:

   Since a 2-cell is contractible, we have $H_0(A) \cong \mathbb{Z}$, $H_n(A) = 0$ for $n > 0$.
4. For both 2-cells (the entire complex $X$): Mayer-Vietoris sequence reads
    
    $\dots \rightarrow H_2(S^1) \rightarrow H_2(e^2_1) \oplus H_2(e^2_2) \rightarrow H_2(X) \rightarrow H_1(S^1) \rightarrow H_1(e^2_1) \oplus H_1(e^2_2) \rightarrow H_1(X) \rightarrow H_0(S^1) \rightarrow H_0(e^2_1) \oplus H_0(e^2_2) \rightarrow H_0(X) \rightarrow 0$
   
    After plugin in the known homology groups, we find:

    $\dots \rightarrow 0 \rightarrow 0 \rightarrow H_2(X) \rightarrow \mathbb{Z} \rightarrow 0 \rightarrow H_1(X) \rightarrow \mathbb{Z} \rightarrow \mathbb{Z} \rightarrow H_0(X) \rightarrow 0$

    From this, we deduce that $H_2(X) \cong \mathbb{Z}$, $H_1(X) \cong 0$, and $H_0(X) \cong \mathbb{Z}$.
</li>
<li>

To show that $X$ is homotopy equivalent to the 2-sphere,


The quotient map for the trivial 0-cell subcomplex, $X \to X/\{e^0\}$, is a homotopy equivalence because one is collapsing a contractible subcomplex. For the 1-skeleton subcomplex $S^1$, the quotient map $X \to X/S^1$ is not a homotopy equivalence, since $H_2(X/S^1) \cong \mathbb{Z} \oplus \mathbb{Z}$ while $H_2(X) \cong \mathbb{Z}.

For $X / B$ we cannot use a similar argument, since both $X$ and $X / B$ have the same homology. However, the quotient map $q: X \rightarrow X / B$ is not a homotopy equivalence. To show this, we compare the two cellular chain complexes. The map $q$ induces a commutative diagram

$`\begin{CD}
\mathbb{Z}[e_1^2, e_2^2] @>d_2=(2,3)>> \mathbb{Z}[e^1] @>>> \mathbb{Z}[e^0] @>>> 0 \\
@V{C_2(q)}VV @VVV @VV{\text{id}}V \\
\mathbb{Z}[e_1^2] @>>> 0 @>>> \mathbb{Z}[e^0] @>>> 0
\end{CD}`$

The left-hand vertical map $C_2(q)$ sends the generator corresponding to $e_1^2$ to $e_1^2$ and $e_2^2$ to 0 . But the elements in the kernel of $d_2=(2,3)$ are integer multiples of the element $3e_1^2 - 2e_2^2$. Hence an element $m(3e_1^2 - 2e_2^2)$ in the kernel of $d_2$ is sent to $3 m e_1^2$ by $C_2(q)$. That implies that the image of

$H_2(q): H_2(X) \rightarrow H_2(X / B)$

is isomorphic to $3 \mathbb{Z}$ in $\mathbb{Z}$. Hence $H_2(q)$ is not surjective, and therefore $q$ is not a homotopy equivalence.
A similar argument with the roles of $e_1^2$ and $e_2^2$ reversed yields the result for $X \rightarrow X / A$.
</li>
</ol>

# 16
Let $\Delta^n=\left[v_0, \cdots, v_n\right]$ have its natural $\Delta$-complex structure with $k$-simplices $\left[v_{i_0}, \cdots, v_{i_k}\right]$ for $i_0<\cdots<i_k$.

Compute the ranks of the simplicial (or cellular) chain groups $\Delta_i\left(\Delta^n\right)$ and the subgroups of cycles and boundaries. [Hint: Pascal's triangle.]

Apply this to show that the $k$-skeleton of $\Delta^n$ has homology groups $\tilde{H}_i\left(\left(\Delta^n\right)^k\right)$ equal to 0 for $i<k$, and free of rank $\binom{n}{k+1}$ for $i=k$.

Solution:

For the $n$-simplex $\Delta^n$:
- The rank of the simplicial chain group $\Delta_i(\Delta^n)$ is $\binom{n+1}{i+1}$, corresponding to the number of $i$-simplices.
- Since $\Delta^n$ is contractible, its reduced homology groups are trivial: $\tilde{H}_i(\Delta^n) = 0$ for all $i$.
- The ranks of the subgroups of cycles $Z_i(\Delta^n)$ and boundaries $B_i(\Delta^n)$ are:
    - $\operatorname{rank}(B_i(\Delta^n)) = \binom{n}{i+1}$ for $i \ge 0$.
    - $\operatorname{rank}(Z_i(\Delta^n)) = \binom{n}{i+1}$ for $i > 0$.
    - $\operatorname{rank}(Z_0(\Delta^n)) = \binom{n}{1} + 1 = n+1$.

For the $k$-skeleton of $\Delta^n$, denoted $(\Delta^n)^k$, the homology groups $\tilde{H}_i((\Delta^n)^k)$ can be computed as follows:

- For $i < k$: The chain complex of $(\Delta^n)^k$ is identical to that of $\Delta^n$ up to dimension $k-1$. Since $\Delta^n$ is contractible, its reduced homology groups are trivial, so $\tilde{H}_i((\Delta^n)^k) = 0$.

- For $i = k$: The homology group $\tilde{H}_k((\Delta^n)^k)$ is given by $Z_k((\Delta^n)^k) / B_k((\Delta^n)^k)$.
  Since $C_{k+1}((\Delta^n)^k) = 0$, the boundary group $B_k((\Delta^n)^k) = 0$.
  The cycle group $Z_k((\Delta^n)^k) = \operatorname{Ker}(\partial_k: C_k(\Delta^n) \to C_{k-1}(\Delta^n)) = Z_k(\Delta^n)$.
  Therefore, $\tilde{H}_k((\Delta^n)^k) \cong Z_k(\Delta^n)$, and its rank is $\binom{n}{k+1}$.


# 17
Show the isomorphism between cellular and singular homology is natural in the following sense:

A map $f: X \rightarrow Y$ that is cellular - satisfying $f(X^n) \subset Y^n$ for all $n$ - induces a chain map $`f_*`$ between the cellular chain complexes of $X$ and $Y$, and the map $`f_*: H_n^{C W}(X) \rightarrow H_n^{C W}(Y)`$ induced by this chain map corresponds to $f_*: H_n(X) \rightarrow H_n(Y)$ under the isomorphism $H_n^{C W} \approx H_n$.

Solution:

$H_n^{CW}(X) \approx H_n(X)$: $H_n(X)$ can be identified with $H_n\left(X^n\right) / \operatorname{Im} \partial_{n+1}$. Since $j_n$ is injective, it maps $\operatorname{Im} \partial_{n+1}$ isomorphically onto $\operatorname{Im}\left(j_n \partial_{n+1}\right)=\operatorname{Im} d_{n+1}$ and $H_n\left(X^n\right)$ isomorphically onto $\operatorname{Im} j_n=\operatorname{Ker} \partial_n$. Since $j_{n-1}$ is injective, $\operatorname{Ker} \partial_n= \operatorname{Ker} d_n$. Thus $j_n$ induces an isomorphism of the quotient $H_n\left(X^n\right) / \operatorname{Im} \partial_{n+1}$ onto $\operatorname{Ker} d_n / \operatorname{Im} d_{n+1}$.

To show naturality, 

# 23
Show that if the closed orientable surface $M_g$ of genus $g$ is a covering space of $M_h$, then $g=n(h-1)+1$ for some $n$, namely, $n$ is the number of sheets in the covering.

[Conversely, if $g=n(h-1)+1$ then there is an $n$-sheeted covering $M_g \rightarrow M_h$, as we saw in Example 1.41.]

Solution:

For covering spaces, the Euler characteristic satisfies $\chi(M_g) = n \chi(M_h)$, where $n$ is the number of sheets in the covering. The Euler characteristic of a closed orientable surface of genus $g$ is given by $\chi(M_g) = 2 - 2g$. Therefore, we have: $2 - 2g = n(2 - 2h)$. Rearranging this equation gives: $g = n(h - 1) + 1$. This shows that if $M_g$ is a covering space of $M_h$, then $g$ must be of the form $n(h - 1) + 1$ for some integer $n$.

# 29
The surface $M_g$ of genus $g$, embedded in $\mathbb{R}^3$ in the standard way, bounds a compact region $R$.

Two copies of $R$, glued together by the identity map between their boundary surfaces $M_g$, form a closed 3-manifold $X$.

Compute the homology groups of $X$ via the Mayer-Vietoris sequence for this decomposition of $X$ into two copies of $R$.

Also compute the relative groups $H_i(R, M_g)$.

Solution:

The Mayer-Vietoris sequence reads

$\cdots \rightarrow H_n(M_g) \rightarrow H_n(R) \oplus H_n(R) \rightarrow H_n(X) \rightarrow H_{n-1}(M_g) \rightarrow \cdots$
