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

$
\left\{\epsilon_{i_1} \wedge \cdots \wedge \epsilon_{i_k} \mid i_1<i_2<\cdots<i_k\right\}
$

(Recall from the last homework that the $\epsilon_i$ form a basis for $V^*$ dual to a basis $`\{e_1, \cdots, e_n\}`$ of $V$.)
