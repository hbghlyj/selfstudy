# 1
Let $G$ be a finite group. Prove the following 'inverse Schur Lemma': if every $G$-equivariant map $\phi: V \rightarrow V$ is scalar, then $V$ is irreducible. You may need to make additional assumptions on the field for the statement to hold, make sure to clearly state this!

Proof

Let $V$ be a representation of a finite group $G$ over a field $F$. We will assume that the field $F$ is algebraically closed and that the characteristic of $F$ does not divide the order of the group $G$.
Suppose, for the sake of contradiction, that $V$ is not irreducible. Then there exists a nontrivial proper subrepresentation $W ⊂ V$.

Since the characteristic of $F$ does not divide $|G|$, by Maschke's Theorem, $V$ is completely reducible. This means that $W$ has a complement $W'$ which is also a subrepresentation, such that $V = W ⊕ W'$.

Consider the projection map $p: V \rightarrow V$ onto $W$ along $W'$. For any $v = w + w'$ where $w ∈ W$ and $w' ∈ W'$, we define $p(v) = w$.

This map is $G$-equivariant. For any $g ∈ G$, $v = w+w' ∈ V$:
$p(g ⋅ v) = p(g ⋅ (w+w')) = p(g ⋅ w + g ⋅ w') = g ⋅ w$ (since $W, W'$ are subrepresentations, $g ⋅ w ∈ W$ and $g ⋅ w' ∈ W'$).

And $g ⋅ p(v) = g ⋅ w$.

So $p(g ⋅ v) = g ⋅ p(v)$.

The map $p$ is not a scalar multiple of the identity map.
- If $p = 0$, then $`W = \ker(p) = \{0\}`$, which contradicts $W$ being a nontrivial subrepresentation.
- If $p = c ⋅ \text{id}$ for some $c ≠ 0$, then $p$ must be an isomorphism. But the image of $p$ is $W$, which is a proper subspace of $V$, so $p$ is not surjective. This is a contradiction.

Thus, $p$ is a non-scalar $G$-equivariant map from $V$ to itself. This contradicts our assumption that every such map is scalar. Therefore, $V$ must be irreducible.
# 2
Suppose $V$ is a completely reducible representation of a group $G$. Show that for every subrepresentation $W \subset V$, the quotient $V / W$ is completely reducible. (Obviously, we are assuming that Maschke's Theorem does not apply, otherwise the question is trivial.)
# 3
Let $V$ be an irreducible finite-dimensional representation of a group $G$. Show that its dual $V^*$ is irreducible as well.
# 4
Suppose that a group $G$ is a product $G=G_1 \times G_2$. Let $V$ be an irreducible representation of $G$ over $\mathbb{C}$. Denote by $\mathrm{res}_{G_1}^G V$ its restriction to $G_1$ : it is given by the composition

$G_1 \rightarrow G \rightarrow \mathrm{GL}(V) .$

Show that $\mathrm{res}_{G_1}^G V \simeq\left(V_1\right)^k$ for some irreducible representation $V_1$ of $G_1$ and $k \geq 1$. (In fact, a stronger statement holds: $V \simeq V_1 \otimes V_2$, where $V_1$ is a representation of $G_1$ and $V_2$ is a representation of $G_2$, but you don't need to prove this.)

# 5
Fix $n$, and denote by $X_k$ the set of all $k$-element subsets of $`\{1, \dots, n\}`$ ($k \leq n$). It carries an action of $S_n$, and we can consider the corresponding representation $V_k$ of $S_n$, where $V_k$ is the space of $\mathbb{C}$-valued functions on $X_k$.

Show that $V_k \simeq V_{n-k}$.

# 6. (Continuation of the previous problem)
Show that $S_n$ has irreducible representations $W_0, W_1, W_2, \ldots, W_{\left\lfloor\frac{n}{2}\right\rfloor}$ such that

$V_k \simeq \bigoplus_{i=0}^k W_i$

for all $k \leq \frac{n}{2}$.
