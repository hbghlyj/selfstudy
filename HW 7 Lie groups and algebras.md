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

# 3.
Suppose that $G$ acts transitively on two manifolds $M$ and $N$, and that for some $p \in M$ and $q \in N$, we have $G_p=G_q$.
(a) Prove that $M$ and $N$ are diffeomorphic.

Hint: Use Theorem 12.10 in the notes.
(b) Use this result to give a proof that $S^2$ is diffeomorphic to $\mathbb{C P}^1$.

# 4.
Suppose that $G \circlearrowright M$ is a transitive left Lie-group action. Let $G_p$ be the stabilizer of $p \in M$. Let $X$ be any vector field on $G$ which is invariant under $\left(R_g\right)_*$ for all $g \in G_p$. Prove that $X$ descends to a vector field on $M$. In particular, any right-invariant vector field on $G$ descends to a vector field on $M$.

# 5.
As in class, define the exponential map $\exp : T_e G \rightarrow G$ by $\exp (\xi)=\gamma_e^{X_{\xi}}(1)$.
(a) Prove that any left-invariant vector field on a Lie group is complete. (So that this definition makes sense).
(b) Prove that $\exp t \xi=\gamma_e^{X_{\xi}}(t)$.
(c) Prove that $\exp (t+s) \xi=\exp (t \xi) \exp (s \xi)$.
(d) Show that for $\mathrm{GL}(n, K)$, the map so defined agrees with the ordinary exponential map of matrices.
Hint: Compare with Example 19.4 in the notes.

# 6.
Multilinear algebra needed later. Review the last question on last week's homework. Recall that any permutation $\sigma \in S_k$ can be written as product of $s$ transpositions. The sign of a permutation $\mathrm{sgn}(\sigma)$ is 1 if $s$ is even and -1 if odd. Let $V$ be a vector space. We say that a multilinear map ( $k$-tensor) $f: V^k \rightarrow \mathbb{R}$ is alternating if for all $\sigma \in S_k$

$
f\left(v_{\sigma(1)}, \ldots, v_{\sigma(k)}\right)=\mathrm{sgn}(\sigma) f\left(v_1, \ldots, v_k\right)
$

We can make an alternating $k$ tensor Alt $f: V^k \rightarrow \mathbb{R}$ from $f$ by setting

$
\mathrm{Alt} f=\frac{1}{k!} \sum_{\sigma \in S_k} \mathrm{sgn}(\sigma) f\left(v_{\sigma(1)}, \ldots, v_{\sigma(k)}\right)
$

We denote $`\Lambda^k V^*`$ to be the set of all alternating $k$ tensors. For $`\omega \in \Lambda^k V^*`$ and $`\eta \in \Lambda^{\ell} V^*`$ we define the wedge product

$
\omega \wedge \eta:=\frac{(k+\ell)!}{k!\ell!} \mathrm{Alt}(\omega \otimes \eta) \in \Lambda^{k+\ell} V^*
$

Show that a basis for $\omega \in \Lambda^k V^*$ is given by

$`\left\{\epsilon_{i_1} \wedge \cdots \wedge \epsilon_{i_k} \mid i_1<i_2<\cdots<i_k\right\}`$

(Recall from the last homework that the $\epsilon_i$ form a basis for $V^*$ dual to a basis $`\{e_1, \cdots, e_n\}`$ of $V$.)
