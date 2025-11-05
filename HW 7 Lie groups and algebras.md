# 1.
First read example 25.5 and 25.6 in Waldron's notes. Then let

$`I_{p, q}=\begin{pmatrix}
1 & 0 & \cdots & & & \\
0 & \ddots & & & & \\
\vdots & & 1 & & & \\
& & & -1 & & \\
& & & & \ddots & \\
& & & & & -1
\end{pmatrix},`$

where there are $p$ 1's and $q$ -1's. Let

$`\mathrm{O}(p, q)=\left\{A \in \mathrm{GL}(n, \mathbb{R}) \mid A^T I_{p, q} A=I_{p, q}\right\} .`$

(a) Calculate $o(p, q)=T_e \mathrm{O}(p, q)$ and check directly that it is a Lie subalgebra of $g l(n, \mathbb{R})$.

(b) Calculate its dimension.

Solution

(a) Define

$`\begin{aligned}
\Phi: \mathrm{GL}(n, \mathbb{R}) & \rightarrow \mathrm{Mat}_{\mathbb{R}}^{n \times n} \\
A & \mapsto A^T I_{p, q} A .
\end{aligned}`$

Let $\mathrm{GL}(n, \mathbb{R})$ act on itself by right-multiplication, and act on $X \in \mathrm{Mat}_{\mathbb{R}}^{n \times n}$ by:

$X \cdot B=B^T X B .$

We have

$\Phi(A B)=(A B)^T I_{p, q} A B=B^T A^T I_{p, q} A B=B^T \Phi(A) B=\Phi(A) \cdot B,$

so $\Phi$ intertwines the two actions. By the equivariant rank theorem, $\mathrm{O}(p, q)=\Phi^{-1}\left(I_{p, q}\right)$ is a closed Lie subgroup of $\mathrm{GL}(n, \mathbb{R})$ (indeed it is closed in $\mathrm{Mat}_{\mathbb{R}}^{n \times n}$).

To determine the dimension of $\mathrm{O}(p, q)$, we need only calculate the tangent space at the identity element $e=I_n$. Since

$d \Phi_{I_n}(X)=X^T I_{p, q}+I_{p, q} X,$

we have

$`T_e \mathrm{O}(p, q)=\left\{X \in \mathrm{Mat}_{\mathbb{R}}^{n \times n} \mid X^T I_{p, q}+I_{p, q} X=0\right\}=: o(p, q) .`$

This is the set of matrices $X$ such that the $(i, j)$-th entry satisfies

$X_{i j}=-X_{j i}$ if $i, j \leq p$ or $i, j>p,$

$X_{i j}=X_{j i}$ otherwise.

To check directly that it is a Lie subalgebra, let $X, Y \in o(p, q)$. We need to show that their Lie bracket $[X, Y]=X Y-Y X$ is also in $o(p, q)$. From the defining condition of $o(p, q)$, we have

$X^T I_{p, q}+I_{p, q} X=0$ and $Y^T I_{p, q}+I_{p, q} Y=0.$

Taking the transpose, we get

$X^T=-I_{p, q} X I_{p, q}^{-1}$ and $Y^T=-I_{p, q} Y I_{p, q}^{-1}.$

Now, compute the transpose of the Lie bracket:

$[X, Y]^T=(X Y-Y X)^T=Y^T X^T-X^T Y^T.$

Substituting the expressions for $X^T$ and $Y^T$, we have

$[X, Y]^T=-I_{p, q} Y I_{p, q}^{-1}(-I_{p, q} X I_{p, q}^{-1})+I_{p, q} X I_{p, q}^{-1}(-I_{p, q} Y I_{p, q}^{-1})=I_{p, q}(YX-XY) I_{p, q}^{-1}=-I_{p, q} [X, Y] I_{p, q}^{-1}.$

Thus, $[X, Y] \in o(p, q)$, proving that $o(p, q)$ is a Lie subalgebra.

(b) To calculate the dimension of $o(p, q)$, note that

- There are $\frac{p(p-1)}{2}$ free entries above the diagonal in the top-left $p \times p$ block (skew-symmetric).

- There are $\frac{q(q-1)}{2}$ free entries above the diagonal in the bottom-right $q \times q$ block (skew-symmetric).

- There are $p q$ free entries in the off-diagonal blocks (symmetric).

Thus,

$\dim o(p, q)=\frac{p(p-1)}{2}+\frac{q(q-1)}{2}+p q=\frac{(p+q)(p+q-1)}{2}=\frac{n(n-1)}{2} .$

# 2.
(a) Show that the action of $\mathrm{SL}(2, \mathbb{C})$ on $\mathbb{C}^2$ (by left multiplication) descends to a Lie group action on $\mathbb{C P}^1$.

(b) $\mathrm{PSL}(2, \mathbb{C}):=\mathrm{SL}(2, \mathbb{C}) / \pm 1$. Show that the action descends to an action of $\mathrm{PSL}(2, \mathbb{C})$ on $\mathbb{C P}^1$.

(c) Show that this action is faithful and transitive, and identify the stabilizer of a point.

(d) Show that the restriction of this action to $\mathrm{PSL}(2, \mathbb{R})$ has two open orbits and one closed orbit.

(e) Given a point $p$ in one of the open orbits, identify the stabilizer $G_p<\mathrm{PSL}(2, \mathbb{R})$.

(f) Given a point $q$ in the closed orbit, identify the stabilizer $G_q<\mathrm{PSL}(2, \mathbb{R})$.

(g) By restricting the action to a smaller subgroup $\mathrm{PSL}(2, \mathbb{R})$, can you make the action on each open orbit free and transitive? How about on the closed orbit?

Proof

(a) The action of $\mathrm{SL}(2, \mathbb{C})$ on $\mathbb{C}^2$ is given by matrix multiplication. For any $A \in \mathrm{SL}(2, \mathbb{C})$ and $[z_1:z_2] \in \mathbb{C P}^1$, define

$A \cdot [z_1:z_2]=[a_{11} z_1+a_{12} z_2:a_{21} z_1+a_{22} z_2],$

where $`A=\begin{pmatrix}a_{11} & a_{12} \\ a_{21} & a_{22}\end{pmatrix}`$. This action is well-defined on projective space because for any $\lambda \in \mathbb{C}^*$, $A \cdot [\lambda z_1:\lambda z_2]$ represents the same point as $A \cdot [z_1:z_2]$, and since $A$ is invertible, the image is never $[0:0]$. Thus, the action descends to a Lie group action on $\mathbb{C P}^1$.

(b) Since $-I \in \mathrm{SL}(2, \mathbb{C})$ acts trivially on $\mathbb{C P}^1$, the action descends to an action of $\mathrm{PSL}(2, \mathbb{C})=\mathrm{SL}(2, \mathbb{C})/\pm 1$ on $\mathbb{C P}^1$.

(c) The action of $\mathrm{PSL}(2, \mathbb{C})$ is faithful, as the kernel of the $\mathrm{SL}(2, \mathbb{C})$ action is $`\{\pm I\}`$, which is the identity element in the quotient group $\mathrm{PSL}(2, \mathbb{C})$. The action is transitive because for any two points $[z_1:z_2]$ in $\mathbb{C P}^1$, there exists an $A \in \mathrm{SL}(2, \mathbb{C})$ such that $A \cdot [1:0]=[z_1:z_2]$ given by

$`A=\frac{1}{\sqrt{|z_1|^2+|z_2|^2}}\begin{pmatrix}z_1 & -\overline{z_2} \\ z_2 & \overline{z_1}\end{pmatrix}`$

The stabilizer of the point $[1:0]$ is the subgroup of upper triangular matrices in $\mathrm{PSL}(2, \mathbb{C})$.

(d) The restriction of the action to $\mathrm{PSL}(2, \mathbb{R})$ has two open orbits: the upper half-plane and the lower half-plane, and one closed orbit: the real projective line $\mathbb{R P}^1$.

The action of $\mathrm{PSL}(2, \mathbb{R})$ on $\mathbb{C P}^1$ can be analyzed by identifying $\mathbb{C P}^1$ with $\mathbb{C} \cup \{\infty\}$. An element of $\mathrm{PSL}(2, \mathbb{R})$ acts via a Möbius transformation which preserves the sign of the imaginary part of any non-real complex number. This partitions $\mathbb{C P}^1$ into three orbits: the upper half-plane $\mathbb{H}$, the lower half-plane $\mathbb{L}$, and the real projective line $\mathbb{R P}^1 = \mathbb{R} \cup \{\infty\}$. The sets $\mathbb{H}$ and $\mathbb{L}$ are open in $\mathbb{C P}^1$, so they are open orbits. $\mathbb{R P}^1$ is a closed subset, so it is a closed orbit.

(e) The stabilizer $G_p$ of a point $p$ in one of the open orbits (e.g., the upper half-plane) is isomorphic to the group of rotations, $\mathrm{PSO}(2)$, which can be represented by matrices of the form $`\begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix}`$.

(f) The stabilizer $G_q$ of a point $q$ in the closed orbit $\mathbb{R P}^1$ is isomorphic to the group of upper triangular matrices with positive diagonal entries, which can be represented by the set of matrices $`\left\{\begin{pmatrix}a & b \\ 0 & a^{-1}\end{pmatrix} \mid a \in \mathbb{R}^+, b \in \mathbb{R}\right\}`$.

(g) Yes, this is possible for both orbit types, by using the stabilizer of a point in the *other* type of orbit.

For an open orbit like $\mathbb{H}$, the affine subgroup from (f) acts freely and transitively because any point in $\mathbb{H}$ can be reached from $i$ by a unique affine transformation:
$`\begin{pmatrix} a & b \\ 0 & a^{-1} \end{pmatrix} \cdot [i:1] = [a i + b : a^{-1}]`$
This corresponds to the complex number $a^2i+ab$, which can represent any point $x+iy \in \mathbb{H}$ by uniquely choosing $a=\sqrt{y}$ and $b=x/\sqrt{y}$.

For the closed orbit $\mathbb{R P}^1$, the compact subgroup $\mathrm{PSO}(2)$ from (e) acts freely and transitively because every point can be reached by a unique rotation:
$`\begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix} \cdot [1:0] = [\cos\theta : -\sin\theta]`$

# 3.
Suppose that $G$ acts transitively on two manifolds $M$ and $N$, and that for some $p \in M$ and $q \in N$, we have $G_p=G_q$.

(a) Prove that $M$ and $N$ are diffeomorphic.

Hint: Use Theorem 12.10 in the notes.

(b) Use this result to give a proof that $S^2$ is diffeomorphic to $\mathbb{C P}^1$.

Proof

(a) Consider the maps

$`\pi_M: G \rightarrow M, \quad g \mapsto g \cdot p`$

and

$`\pi_N: G \rightarrow N, \quad g \mapsto g \cdot q`$.

Both maps are surjective submersions, and their fibers coincide since $\pi_M^{-1}(p)=G_p=G_q=\pi_N^{-1}(q)$. By Theorem 12.10, there exists a unique diffeomorphism $f: M \rightarrow N$ such that $f \circ \pi_M = \pi_N$. Thus, $M$ and $N$ are diffeomorphic.

(b) We know that $\mathrm{SU}(2)$ acts transitively on both $S^2$ and $\mathbb{C P}^1$. For a suitable choice of points $p \in S^2$ and $q \in \mathbb{C P}^1$, the stabilizer subgroups $G_p$ and $G_q$ are identical. For instance, the stabilizer of $[1:0] \in \mathbb{C P}^1$ is the subgroup of diagonal matrices in $\mathrm{SU}(2)$, which is the same subgroup that stabilizes the north pole in $S^2$ under the adjoint action. Since the stabilizers are the same subgroup, by part (a), we conclude that $S^2$ is diffeomorphic to $\mathbb{C P}^1$.

# 4.
Suppose that $G \circlearrowright M$ is a transitive left Lie-group action. Let $G_p$ be the stabilizer of $p \in M$. Let $X$ be any vector field on $G$ which is invariant under $(R_g)_*$ for all $g \in G_p$. Prove that $X$ descends to a vector field on $M$. In particular, any right-invariant vector field on $G$ descends to a vector field on $M$.

Proof

According to Proposition 18.1 (Smooth descent by submersions), a vector field $X \in \mathfrak{X}(G)$ descends to a smooth vector field on $M$ if $d\pi_g(X_g)$ is constant on the fibers of the submersion $\pi: G \rightarrow M$, defined by $\pi(g) = g \cdot p$. The fibers of $\pi$ are the left cosets of the stabilizer $G_p$.

Let $g_1, g_2$ be in the same fiber, so $g_2 = g_1 h$ for some $h \in G_p$. We need to show $d\pi_{g_1}(X_{g_1}) = d\pi_{g_2}(X_{g_2})$.

For any $g \in G$ and $h \in G_p$, we have $\pi(g h) = (g h) \cdot p = g \cdot (h \cdot p) = g \cdot p = \pi(g)$. Thus, $\pi \circ R_h = \pi$. Differentiating gives $`d\pi_{gh} \circ (dR_h)_g = d\pi_g`$.

By hypothesis, $X_{gh} = (dR_h)_g(X_g)$.

So, $`d\pi_{g_2}(X_{g_2}) = d\pi_{g_1 h}(X_{g_1 h}) = d\pi_{g_1 h}((dR_h)_{g_1}(X_{g_1})) = (d\pi_{g_1 h} \circ (dR_h)_{g_1})(X_{g_1}) = d\pi_{g_1}(X_{g_1})`$.

This shows the condition is met, so $X$ descends.

In particular, any right-invariant vector field on $G$ is invariant under $(R_g)_*$ for all $g \in G$, so it is for $g \in G_p$. Thus it descends to a vector field on $M$.

# 5.
As in class, define the exponential map $\exp : T_e G \rightarrow G$ by $\exp (\xi)=\gamma_e^{X_{\xi}}(1)$.

(a) Prove that any left-invariant vector field on a Lie group is complete. (So that this definition makes sense).

(b) Prove that $\exp t \xi=\gamma_e^{X_{\xi}}(t)$.

(c) Prove that $\exp (t+s) \xi=\exp (t \xi) \exp (s \xi)$.

(d) Show that for $\mathrm{GL}(n, K)$, the map so defined agrees with the ordinary exponential map of matrices.

Hint: Compare with Example 19.4 in the notes.

Proof

(a) Suppose $X$ is a left-invariant vector field on $G$. We first show the integral curve through the identity, $\gamma_e^X(t)$, is defined for all $t \in \mathbb{R}$. Let its maximal domain be $(a,b)$. Assume $b < \infty$. By local existence, $\gamma_e^X(t)$ exists for $t \in (-\epsilon, \epsilon)$ for some $\epsilon > 0$. For any $t_0 \in (b-\epsilon, b)$, the curve $\tilde{\gamma}(t) = \gamma_e^X(t_0) \cdot \gamma_e^X(t-t_0)$ is an integral curve that matches $\gamma_e^X(t)$ on their common domain, but is defined on $(t_0-\epsilon, t_0+\epsilon)$, which extends beyond $b$. This contradicts maximality, so $b=\infty$. A similar argument shows $a=-\infty$.

For any $g \in G$, the integral curve $\gamma_g^X(t)$ is given by $\gamma_g^X(t) = L_g(\gamma_e^X(t))$. Since $\gamma_e^X(t)$ is defined for all $t \in \mathbb{R}$ and $L_g$ is a diffeomorphism, $\gamma_g^X(t)$ is also defined for all $t \in \mathbb{R}$. Thus, $X$ is complete.

(b) By definition, $\exp(t \xi) = \gamma_e^{X_{t\xi}}(1)$. By Lemma 9.3 (Rescaling Lemma) in Lee's *Introduction to Smooth Manifolds*, $\gamma_e^{X_{t \xi}}(s) = \gamma_e^{X_{\xi}}(t s)$. Evaluating at $s=1$, we get $\exp(t \xi) = \gamma_e^{X_{\xi}}(t)$.

(c) By Naturality of integral curves, $L_{\exp(s \xi)}(\gamma_e^{X_{\xi}}(t))$ is an integral curve of $X_{\xi}$ starting at $\exp(s \xi)$. Thus,

$`\gamma_e^{X_{\xi}}(t+s) = L_{\exp(s \xi)}(\gamma_e^{X_{\xi}}(t)) = \gamma_e^{X_{\xi}}(s) \cdot \gamma_e^{X_{\xi}}(t)`$.

Setting $t=1$ gives $\exp((t+s) \xi) = \exp(t \xi) \exp(s \xi)$.

(d) For $G = \mathrm{GL}(n, K)$, the left-invariant vector field corresponding to $`\xi \in T_e G \cong \mathrm{Mat}_{K}^{n \times n}`$ is given by $X_{\xi}(A) = A \xi$ for $A \in \mathrm{GL}(n, K)$. The integral curve through the identity is given by the solution to the matrix differential equation
$\frac{d}{dt} \gamma_e^{X_{\xi}}(t) = \gamma_e^{X_{\xi}}(t) \xi$ with initial condition $\gamma_e^{X_{\xi}}(0) = I_n$. The solution to this equation is the matrix exponential $\gamma_e^{X_{\xi}}(t) = e^{t \xi}$. Therefore, by part (b), we have $\exp(\xi) = \gamma_e^{X_{\xi}}(1) = e^{\xi}$, which agrees with the ordinary exponential map of matrices.

# 6. Multilinear algebra needed later.
Review the last question on last week's homework. Recall that any permutation $\sigma \in S_k$ can be written as product of $s$ transpositions. The sign of a permutation $\mathrm{sgn}(\sigma)$ is 1 if $s$ is even and -1 if odd. Let $V$ be a vector space. We say that a multilinear map ($k$-tensor) $f: V^k \rightarrow \mathbb{R}$ is alternating if for all $\sigma \in S_k$

$`f\left(v_{\sigma(1)}, \ldots, v_{\sigma(k)}\right)=\mathrm{sgn}(\sigma) f\left(v_1, \ldots, v_k\right)`$

We can make an alternating $k$ tensor $\mathrm{Alt} f: V^k \rightarrow \mathbb{R}$ from $f$ by setting

$`\mathrm{Alt} f=\frac{1}{k!} \sum_{\sigma \in S_k} \mathrm{sgn}(\sigma) f\left(v_{\sigma(1)}, \ldots, v_{\sigma(k)}\right)`$

We denote $`\Lambda^k V^*`$ to be the set of all alternating $k$ tensors. For $`\omega \in \Lambda^k V^*`$ and $`\eta \in \Lambda^{\ell} V^*`$ we define the wedge product

$`\omega \wedge \eta:=\frac{(k+\ell)!}{k!\ell!} \mathrm{Alt}(\omega \otimes \eta) \in \Lambda^{k+\ell} V^*`$

Show that a basis for $\omega \in \Lambda^k V^*$ is given by

$`\left\{\epsilon_{i_1} \wedge \cdots \wedge \epsilon_{i_k} \mid i_1<i_2<\cdots<i_k\right\}`$

(Recall from the last homework that the $\epsilon_i$ form a basis for $V^*$ dual to a basis $`\{e_1, \cdots, e_n\}`$ of $V$.)

Proof

Since $`\Lambda^k V^*`$ is the image of the map $`\mathrm{Alt}: (V^*)^{\otimes k} \rightarrow (V^*)^{\otimes k}`$, and the image of a basis under a linear map spans the image, we can find a spanning set for $`\Lambda^k V^*`$ by projecting a basis of $`(V^*)^{\otimes k}`$. A basis for $`(V^*)^{\otimes k}`$ is given by

$`\left\{\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k} \mid 1 \leq i_1, \ldots, i_k \leq n\right\}`$.

so the set $`\left\{\mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right) \mid 1 \leq i_1, \ldots, i_k \leq n\right\}`$ spans $`\Lambda^k V^*`$. 

Note that if any two indices $i_j = i_m$ for $j \neq m$, then $\mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right) = 0$.

Therefore, the set $`\left\{\mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right) \mid i_1<i_2<\cdots<i_k\right\}`$ spans $`\Lambda^k V^*`$.

By definition of the wedge product, we have
$`\epsilon_{i_1} \wedge \cdots \wedge \epsilon_{i_k} = k! \mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right)`$,
so the set $`\left\{\epsilon_{i_1} \wedge \cdots \wedge \epsilon_{i_k} \mid i_1<i_2<\cdots<i_k\right\}`$ also spans $`\Lambda^k V^*`$.

Next, we show that these elements are linearly independent. Suppose we have a linear combination
$`\sum_{i_1 < i_2 < \cdots < i_k} c_{i_1, \ldots, i_k} \mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right) = 0`$.

Then for any $v_1, \ldots, v_k \in V$, we have
$`\sum_{i_1 < i_2 < \cdots < i_k} c_{i_1, \ldots, i_k} \mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right)(v_1, \ldots, v_k) = 0`$.

Choosing $v_j = e_{i_j}$ for $j=1, \ldots, k$, we find that only the term with indices $i_1, \ldots, i_k$ contributes to the sum, yielding
$`c_{i_1, \ldots, i_k} \mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right)(e_{i_1}, \ldots, e_{i_k}) = 0`$.

Since $\mathrm{Alt}\left(\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_k}\right)(e_{i_1}, \ldots, e_{i_k}) = 1$, it follows that $c_{i_1, \ldots, i_k} = 0$.

Thus, all coefficients must be zero, proving linear independence.
