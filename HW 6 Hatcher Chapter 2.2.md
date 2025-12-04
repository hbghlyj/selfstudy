# 1
Prove the Brouwer fixed point theorem for maps $f: D^n \rightarrow D^n$ by applying degree theory to the map $S^n \rightarrow S^n$ that sends both the northern and southern hemispheres of $S^n$ to the southern hemisphere via $f$. [This was Brouwer's original proof.]

Proof

Assume for contradiction that there exists a continuous map $f: D^n \rightarrow D^n$ without a fixed point.

Since $S^n$ can be viewed as the union of two hemispheres $D^n_+$ and $D^n_-$, we can define a map $F: S^n \rightarrow S^n$ as follows:
We identify $D^n$ with the southern hemisphere $D^n_-$, so $f$ is a map $f: D^n_- \to D^n_-$. 
- For $x \in D^n_+$ (the northern hemisphere), define $F(x) = f(\text{Reflect}_{z=0}(x))$.
- For $x \in D^n_-$ (the southern hemisphere), define $F(x) = f(x)$.
 
The definitions agree on $D^n_+\cap D^n_-$, so $F$ is well-defined. The image of both hemispheres under $F$ lies in the southern hemisphere of $S^n$. Since the map is not surjective onto $S^n$, the degree of $F$ must be zero.

To arrive at a contradiction, we exhibit a homotopy between $F$ and the antipodal map $A: S^n \rightarrow S^n$ defined by $A(x) = -x$. The antipodal map has degree $(-1)^{n+1}$, which is non-zero for all $n \geq 1$.

Define a homotopy $H: S^n \times [0,1] \rightarrow S^n$ by

$`H(x,t) = \frac{(1-t)F(x) + tA(x)}{\|(1-t)F(x) + tA(x)\|}.`$

The homotopy $H$ is well-defined if the denominator is never zero, which requires $F(x) \ne -A(x) = x$ for all $x \in S^n$. This condition holds by the assumption that $f$ has no fixed points. For $x \in D^n_-$, we have $F(x) = f(x) \ne x$. For $x \in D^n_+$, we have $F(x) \in D^n_-$ while $x \in D^n_+$, so $F(x) \ne x$ (the case of $x$ on the equator is covered by the first case). Therefore, the homotopy is well-defined.

# 9(a)
Compute the homology groups of the following 2-complex:

The quotient of $S^2$ obtained by identifying north and south poles to a point.

Proof

The given space is homotopy equivalent to $S^2 \vee S^1$. This is because identifying two points in a path-connected space is homotopy equivalent to attaching a 1-cell between them. The resulting space, $S^2$ with an arc connecting the poles, deformation retracts to $S^2 \vee S^1$.

$\tilde{H}_n(S^2 \vee S^1) \cong \tilde{H}_n(S^2) \oplus \tilde{H}_n(S^1)$.

Thus, the homology groups are:
- $H_0 \cong \mathbb{Z}$
- $H_1 \cong \mathbb{Z}$
- $H_2 \cong \mathbb{Z}$
- $H_n = 0$ for $n > 2$.

# 9(d)
Compute the homology groups of the following 2-complex:

The quotient space of $S^1 \times S^1$ obtained by identifying points in the circle $`S^1 \times\{x_0\}`$ that differ by $2 \pi / m$ rotation and identifying points in the circle $`\{x_0\} \times S^1`$ that differ by $2 \pi / n$ rotation.

# 14
A map $f: S^n \rightarrow S^n$ satisfying $f(x)=f(-x)$ for all $x$ is called an even map. Show that an even map $S^n \rightarrow S^n$ must have even degree, and that the degree must in fact be zero when $n$ is even. When $n$ is odd, show there exist even maps of any given even degree.

[Hints: If $f$ is even, it factors as a composition $S^n \rightarrow \mathbb{R} P^n \rightarrow S^n$. Using the calculation of $`H_n(\mathbb{R} P^n)`$ in the text, show that the induced map $`H_n(S^n) \rightarrow H_n(\mathbb{R} P^n)`$ sends a generator to twice a generator when $n$ is odd. It may be helpful to show that the quotient map $\mathbb{R} P^n \rightarrow \mathbb{R} P^n / \mathbb{R} P^{n-1}$ induces an isomorphism on $H_n$ when $n$ is odd.]

# 15
Show that if $X$ is a CW complex then $H_n(X^n)$ is free by identifying it with the kernel of the cellular boundary map $H_n(X^n, X^{n-1}) \rightarrow H_{n-1}(X^{n-1}, X^{n-2})$.

# 20
For finite CW complexes $X$ and $Y$, show that $\chi(X \times Y)=\chi(X) \chi(Y)$.

Proof

Let $X$ and $Y$ be finite CW complexes. The Euler characteristic $\chi(X)$ is defined as the alternating sum of the number of $n$-cells in $X$:

$\chi(X) = \sum_{n=0}^{\infty} (-1)^n c_n(X)$,

where $c_n(X)$ is the number of $n$-cells in $X$. Similarly, we have

$\chi(Y) = \sum_{m=0}^{\infty} (-1)^m c_m(Y)$.

The product space $X \times Y$ has a CW structure where the $k$-cells are formed by taking the product of an $i$-cell from $X$ and a $j$-cell from $Y$ such that $i + j = k$. Therefore, the number of $k$-cells in $X \times Y$ is given by

$c_k(X \times Y) = \sum_{i+j=k} c_i(X) c_j(Y)$.

Thus, the Euler characteristic of $X \times Y$ can be computed as follows:

$`\begin{align*}
\chi(X \times Y) &= \sum_{k=0}^{\infty} (-1)^k c_k(X \times Y) \\
&= \sum_{k=0}^{\infty} (-1)^k \sum_{i+j=k} c_i(X) c_j(Y) \\
&= \sum_{i=0}^{\infty} \sum_{j=0}^{\infty} (-1)^{i+j} c_i(X) c_j(Y) \\
&= \left( \sum_{i=0}^{\infty} (-1)^i c_i(X) \right) \left( \sum_{j=0}^{\infty} (-1)^j c_j(Y) \right) \\
&= \chi(X) \chi(Y)
\end{align*}`$

# 22
For $X$ a finite CW complex and $p: \tilde{X} \rightarrow X$ an $n$-sheeted covering space, show that $\chi(\tilde{X})=n \chi(X)$.

Proof

The Euler characteristic of a CW complex $X$ is given by

$\chi(X) = \sum_{n=0}^{\infty} (-1)^n c_n(X)$,

where $c_n(X)$ is the number of $n$-cells in $X$.

The Euler characteristic of the covering space $\tilde{X}$ can be computed similarly:

$\chi(\tilde{X}) = \sum_{n=0}^{\infty} (-1)^n c_n(\tilde{X})$.

Since $p: \tilde{X} \rightarrow X$ is an $n$-sheeted covering space, each $k$-cell in $X$ lifts to $n$ distinct $k$-cells in $\tilde{X}$. Therefore, we have:

$c_k(\tilde{X}) = n \cdot c_k(X)$ for all $k \ge 0$.

Thus, the Euler characteristic of $\tilde{X}$ can be computed as follows:

$\chi(\tilde{X}) = \sum_{k=0}^{\infty} (-1)^k c_k(\tilde{X}) = \sum_{k=0}^{\infty} (-1)^k (n \cdot c_k(X)) = n \left( \sum_{k=0}^{\infty} (-1)^k c_k(X) \right) = n \chi(X)$.

# 28(a)
Use the Mayer-Vietoris sequence to compute the homology groups of the space obtained from a torus $S^1 \times S^1$ by attaching a Möbius band via a homeomorphism from the boundary circle of the Möbius band to the circle $`S^1 \times\{x_0\}`$ in the torus.

Proof

The Mayer-Vietoris sequence for the decomposition of the space $X$ into the torus $T = S^1 \times S^1$ and the Möbius band $M$ is given by:

$`\cdots \rightarrow H_n(S^1) \xrightarrow{(i_*, j_*)} H_n(T) \oplus H_n(M) \xrightarrow{k_* - l_*} H_n(X) \xrightarrow{\delta} H_{n-1}(S^1) \rightarrow \cdots`$

where $`i_*`$ and $`j_*`$ are induced by the inclusion maps of the boundary circle into the torus and the Möbius band, respectively, and $`k_*`$ and $`l_*`$ are induced by the inclusion maps of the torus and the Möbius band into $X$.

*   **Case n > 2:**
    
    Since both $`H_n(T)`$ and $H_n(M)$ are zero for $n > 2$, it follows from the exactness of the sequence that $H_n(X) = 0$ for $n > 2$.
*   **Case n = 2:**
    
    The sequence gives $`\dots \to H_2(T)\oplus H_2(M) \to H_2(X) \xrightarrow{\delta} H_1(S^1) \xrightarrow{(i_*,j_*)} \dots`$. The map $`(i_*,j_*)`$ is injective, so its kernel is trivial. By exactness, the image of $\delta$ is trivial, so $\delta$ is the zero map. The preceding term in the sequence, $H_2(S^1)$, is 0. This implies the map $H_2(T)\oplus H_2(M) \to H_2(X)$ is an isomorphism. Therefore, $H_2(X) \cong H_2(T) \oplus H_2(M) \cong \mathbb{Z}$.
*   **Case n = 1:**
    
    The map $`(i_*, j_*): H_1(S^1) \to H_1(T) \oplus H_1(M)`$ sends the generator of $H_1(S^1)$ to an element represented by $((1,0), 2)$ in $\mathbb{Z}^2 \oplus \mathbb{Z}$. The $(1,0)$ component is because the boundary is attached to the circle $`S^1 \times \{x_0\}`$ in the torus. The $2$ component is because the boundary of a Möbius band wraps twice around its core circle, which generates $H_1(M)$. The next part of the sequence is $H_1(X) \to H_0(S^1) \to H_0(T) \oplus H_0(M)$. The last map is injective, so from exactness, $H_1(X)$ is the cokernel of $`(i_*, j_*)`$. Thus, $H_1(X) \cong (\mathbb{Z}^2 \oplus \mathbb{Z}) / \langle(1,0,2)\rangle \cong \mathbb{Z}^2$.
*   **Case n = 0:**
    
    Since $X$ is path-connected, $H_0(X) \cong \mathbb{Z}$.

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
2. The 0-cell and the 1-cell (the 1-skeleton, which is $S^1$).
3. The 1-skeleton and one of the 2-cells.
4. Both 2-cells (the entire complex $X$).

Now, we compute the homology groups for each subcomplex $A$ and the corresponding quotient complexes $X / A$:
1. For the trivial subcomplex:

   $X/A = X$.

   $H_0(A) \cong \mathbb{Z}$, $H_n(A) = 0$ for $n > 0$.
2. For the 1-skeleton $S^1$:

   $X/A = S^2 \vee S^2$.
   
   $H_0(A) \cong \mathbb{Z}$, $H_1(A) \cong \mathbb{Z}$, $H_n(A) = 0$ for $n > 1$.
3. For the subcomplex $S^1 \cup e^2_1$ (attached via degree 2 map):

   $X/A = S^2$.
   
   The homology groups of the quotient are $H_0(X/A) \cong \mathbb{Z}$, $H_2(X/A) \cong \mathbb{Z}$, and $H_n(X/A) = 0$ for $`n \notin \{0, 2\}`$.

   The subcomplex $A = S^1 \cup e^2_1$ is homeomorphic to the real projective plane, $\mathbb{RP}^2$. Its homology groups, computed via cellular homology, are $H_0(A) \cong \mathbb{Z}$, $H_1(A) \cong \mathbb{Z}/2\mathbb{Z}$, and $H_n(A) = 0$ for $n > 1$.

4. For the subcomplex $S^1 \cup e^2_2$ (attached via degree 3 map):

   $X/A = S^2$.
   
   The homology groups of the quotient are $H_0(X/A) \cong \mathbb{Z}$, $H_2(X/A) \cong \mathbb{Z}$, and $H_n(X/A) = 0$ for $`n \notin \{0, 2\}`$.

   The subcomplex $A = S^1 \cup e^2_2$ is obtained by attaching a 2-cell to $S^1$ via a map of degree 3. Its homology groups are $H_0(A) \cong \mathbb{Z}$, $H_1(A) \cong \mathbb{Z}/3\mathbb{Z}$, and $H_n(A) = 0$ for $n > 1$.

6. For the entire complex $X$:
    
   $X/A = \text{a single point}$.

   The homology of $X$ is computed using its cellular chain complex $0 \to \mathbb{Z}^2 \xrightarrow{d_2} \mathbb{Z} \xrightarrow{d_1} \mathbb{Z} \to 0$, where the boundary map $d_2$ sends the generators of the two 2-cells to $2$ and $3$ times the generator of the 1-cell, respectively.
   
   This gives the homology groups:

   $H_0(X) \cong \mathbb{Z}$

   $H_1(X) = \ker(d_1)/\mathrm{im}(d_2) = \mathbb{Z}/\langle 2,3 \rangle\mathbb{Z} = 0$

   $H_2(X) = \ker(d_2) = \langle (3,-2) \rangle \cong \mathbb{Z}$
</li>
<li>

To show that $X$ is homotopy equivalent to the 2-sphere, consider the attaching maps of the 2-cells. The degrees of the attaching maps (2 and 3) imply that the fundamental group of $X$ is trivial, as the relations imposed by the attaching maps kill all loops in $S^1$. Since $X$ is a simply connected CW complex with the same homology groups as $S^2$, it follows from Whitehead's theorem that $X$ is homotopy equivalent to $S^2$. 

To construct an explicit homotopy equivalence, we can define a map $f: X \to S^2$ that induces an isomorphism on all homology groups. By Whitehead's theorem, such a map is a homotopy equivalence. We construct $f$ as a composition $f = h \circ q$.

1. **The Quotient Map $q$**
   
   First, consider the quotient map $q: X \to X / S^1$ that collapses the 1-skeleton $S^1$ to a point. The quotient space $X / S^1$ is the wedge sum of two 2-spheres, $S^2 \vee S^2$. Let's denote these spheres as $S^2_1$ and $S^2_2$, corresponding to the 2-cells $e^2_1$ and $e^2_2$.
2. **The Map $h$**
   
   Next, define a map $h: S^2_1 \vee S^2_2 \to S^2$. We can specify this map by its degrees on each sphere. Let the degree of $h$ on $S^2_1$ be $k_1$ and on $S^2_2$ be $k_2$.

3. **The Composition $f$ and Homology**
   
   The composite map is $f = h \circ q: X \to S^2$. We need to choose $k_1$ and $k_2$ such that $f$ induces an isomorphism on homology. The only non-trivial group to check is $H_2$.
   
   The generator of $`H_2(X) \cong \mathbb{Z}`$ is represented by the cellular chain $`3e_1^2 - 2e_2^2`$. The map $`q_*`$ on $H_2$ sends this generator to the element $(3, -2)$ in $`H_2(S^2 \vee S^2) \cong \mathbb{Z} \oplus \mathbb{Z}`$. The map $`h_*`$ sends an element $(n, m) \in \mathbb{Z} \oplus \mathbb{Z}$ to $`k_1 n + k_2 m \in H_2(S^2) \cong \mathbb{Z}`$.
   
   Therefore, the induced map $`f_* = h_* \circ q_*`$ sends the generator of $H_2(X)$ to $`k_1(3) + k_2(-2) = 3k_1 - 2k_2`$. For $f_*$ to be an isomorphism, we need this value to be a generator of $\mathbb{Z}$, i.e., $`3k_1 - 2k_2 = \pm 1`$. A simple integer solution is $`k_1=1, k_2=1`$. With this choice, $f$ is a homotopy equivalence.

The quotient map for the trivial 0-cell subcomplex, $`X \to X/\{e^0\}`$, is a homotopy equivalence because one is collapsing a contractible subcomplex.

For the 1-skeleton subcomplex $S^1$, the quotient map $X \to X/S^1$ is not a homotopy equivalence, since $`H_2(X/S^1) \cong \mathbb{Z} \oplus \mathbb{Z}`$ while $`H_2(X) \cong \mathbb{Z}`$.
Similarly, the quotient map $`X \to X/X`$ is not a homotopy equivalence, since $`X/X`$ is a point and thus has $`H_2(X/X) = 0`$, while $`H_2(X) \cong \mathbb{Z}`$.

For $X / S^1\cup e_2^2$ we cannot use a similar argument, since both $X$ and $X / S^1\cup e_2^2$ have the same homology. However, the quotient map $q: X \rightarrow X / S^1\cup e_2^2$ is not a homotopy equivalence. To show this, we compare the two cellular chain complexes. The map $q$ induces a commutative diagram

$`\begin{CD}
\mathbb{Z}[e_1^2, e_2^2] @>d_2=(2,3)>> \mathbb{Z}[e^1] @>>> \mathbb{Z}[e^0] @>>> 0 \\
@V{C_2(q)}VV @VVV @VV{\text{id}}V \\
\mathbb{Z}[e_1^2] @>>> 0 @>>> \mathbb{Z}[e^0] @>>> 0
\end{CD}`$

The left-hand vertical map $C_2(q)$ sends the generator corresponding to $e_1^2$ to $e_1^2$ and $e_2^2$ to 0. But the elements in the kernel of $d_2=(2,3)$ are integer multiples of the element $3e_1^2 - 2e_2^2$. Hence an element $m(3e_1^2 - 2e_2^2)$ in the kernel of $d_2$ is sent to $3 m e_1^2$ by $C_2(q)$. That implies that the image of

$H_2(q): H_2(X) \rightarrow H_2(X / S^1\cup e_2^2)$

is isomorphic to $3 \mathbb{Z}$ in $\mathbb{Z}$. Hence $H_2(q)$ is not surjective, and therefore $q$ is not a homotopy equivalence.
A similar argument with the roles of $e_1^2$ and $e_2^2$ reversed yields the result for $X \rightarrow X / S^1\cup e_1^2$.
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
    - $\mathrm{rank}(B_i(\Delta^n)) = \binom{n}{i+1}$ for $i \ge 0$.
    - $\mathrm{rank}(Z_i(\Delta^n)) = \binom{n}{i+1}$ for $i > 0$.
    - $\mathrm{rank}(Z_0(\Delta^n)) = \binom{n}{1} + 1 = n+1$.

For the $k$-skeleton of $\Delta^n$, denoted $(\Delta^n)^k$, the homology groups $\tilde{H}_i((\Delta^n)^k)$ can be computed as follows:

- For $i < k$: The chain complex of $(\Delta^n)^k$ is identical to that of $\Delta^n$ up to dimension $k-1$. Since $\Delta^n$ is contractible, its reduced homology groups are trivial, so $\tilde{H}_i((\Delta^n)^k) = 0$.

- For $i = k$: The homology group $`\tilde{H}_k((\Delta^n)^k)`$ is given by $Z_k((\Delta^n)^k) / B_k((\Delta^n)^k)$.
  Since $C_{k+1}((\Delta^n)^k) = 0$, the boundary group $B_k((\Delta^n)^k) = 0$.
  The cycle group $Z_k((\Delta^n)^k) = \mathrm{Ker}(\partial_k: C_k(\Delta^n) \to C_{k-1}(\Delta^n)) = Z_k(\Delta^n)$.
  Therefore, $\tilde{H}_k((\Delta^n)^k) \cong Z_k(\Delta^n)$, and its rank is $\binom{n}{k+1}$.


# 17
Show the isomorphism between cellular and singular homology is natural in the following sense:

A map $f: X \rightarrow Y$ that is cellular - satisfying $f(X^n) \subset Y^n$ for all $n$ - induces a chain map $`f_*`$ between the cellular chain complexes of $X$ and $Y$, and the map $`f_*: H_n^{C W}(X) \rightarrow H_n^{C W}(Y)`$ induced by this chain map corresponds to $f_*: H_n(X) \rightarrow H_n(Y)$ under the isomorphism $H_n^{C W} \approx H_n$.

Solution:

$H_n^{CW}(X) \approx H_n(X)$: $H_n(X)$ can be identified with $H_n\left(X^n\right) / \mathrm{Im} \partial_{n+1}$. Since $j_n$ is injective, it maps $\mathrm{Im} \partial_{n+1}$ isomorphically onto $\mathrm{Im}\left(j_n \partial_{n+1}\right)=\mathrm{Im} d_{n+1}$ and $H_n\left(X^n\right)$ isomorphically onto $\mathrm{Im} j_n=\mathrm{Ker} \partial_n$. Since $j_{n-1}$ is injective, $\mathrm{Ker} \partial_n= \mathrm{Ker} d_n$. Thus $j_n$ induces an isomorphism of the quotient $H_n\left(X^n\right) / \mathrm{Im} \partial_{n+1}$ onto $\mathrm{Ker} d_n / \mathrm{Im} d_{n+1}$.

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
