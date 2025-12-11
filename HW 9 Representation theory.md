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

Proof

Let $V$ be a completely reducible representation of a group $G$, and let $W \subset V$ be a subrepresentation. We want to show that the quotient representation $V / W$ is also completely reducible.

To prove this, we will use the property that a representation is completely reducible if and only if every subrepresentation has a complement.

Let $U'$ be an arbitrary subrepresentation of $V / W$.

Let $U = \pi^{-1}(U')$ be its preimage in $V$ under the quotient map $\pi: V \rightarrow V / W$. $U$ is a subrepresentation of $V$ containing $W$.

Since $V$ is completely reducible, $U$ has a complement $U''$ in $V$, so $V = U \oplus U''$.

Also, since $U$ is a subrepresentation of a completely reducible representation $V$, $U$ is itself completely reducible. Thus, the subrepresentation $W \subset U$ has a complement $W'$ in $U$, so $U = W \oplus W'$.

Combining these, we get $V = W \oplus W' \oplus U''$.

Let $\pi: V \to V/W$ be the quotient map.

From $V = W \oplus W' \oplus U''$, we see that $V/W = \pi(V) = \pi(W') \oplus \pi(U'')$.

The subrepresentation $U'$ is $U/W = \pi(U) = \pi(W \oplus W') = \pi(W')$.

Therefore, $V/W = U' \oplus \pi(U'')$, which shows that $U'$ has a complement in $V/W$ (namely $\pi(U'')$).

Since every subrepresentation $U'$ of $V / W$ has a complement, $V / W$ is completely reducible.
# 3
Let $V$ be an irreducible finite-dimensional representation of a group $G$. Show that its dual $V^*$ is irreducible as well.

Proof

The dual representation $V^*$ of a representation $V$ of a group $G$ is defined by the action:

$(g \cdot f)(v) = f(g^{-1} \cdot v)$ for all $g \in G$, $f \in V^*$, and $v \in V$.

To show that $`V^*`$ is irreducible, we need to demonstrate that there are no nontrivial proper subrepresentations of $V^*$.

Let $W$ be a subrepresentation of $V^*$. We will show that $W$ is either $`\{0\}`$ or $`V^*`$.

Consider the annihilator of $W$ in $V$:

$`W^\perp = \{v \in V \mid f(v) = 0 \text{ for all } f \in W\}`$.

We first show that $W^\perp$ is a subrepresentation of $V$. Let $v \in W^\perp$ and $g \in G$. We need to show that $g \cdot v \in W^\perp$. This means we must show that $f(g \cdot v) = 0$ for all $f \in W$.

Since $W$ is a subrepresentation of $V^*$, for any $f \in W$, the functional $g^{-1} \cdot f$ is also in $W$.

Because $v \in W^\perp$, we have $(g^{-1} \cdot f)(v) = 0$.

By the definition of the dual action, $(g^{-1} \cdot f)(v) = f(g \cdot v)$.

Therefore, $f(g \cdot v) = 0$ for all $f \in W$, which means $g \cdot v \in W^\perp$.

Thus, $W^\perp$ is a subrepresentation of $V$.

Since $V$ is irreducible, its only subrepresentations are $`\{0\}`$ and $V$. So we have two cases for $W^\perp$:

1.  $W^\perp = V$: This means that for every $f \in W$, $f(v) = 0$ for all $v \in V$. This implies that every functional in $W$ is the zero functional, so $`W = \{0\}`$.
2.  $`W^\perp = \{0\}`$: Since $V$ is finite-dimensional, we have $(W^\perp)^\perp = W$. Therefore, $`W = (\{0\})^\perp = V^*`$.

Thus, $V^*$ is irreducible.

# 4
Suppose that a group $G$ is a product $G=G_1 \times G_2$. Let $V$ be an irreducible representation of $G$ over $\mathbb{C}$. Denote by $\mathrm{res}_{G_1}^G V$ its restriction to $G_1$: it is given by the composition

$G_1 \rightarrow G \rightarrow \mathrm{GL}(V) .$

Show that $\mathrm{res}_{G_1}^G V \simeq\left(V_1\right)^k$ for some irreducible representation $V_1$ of $G_1$ and $k \geq 1$. (In fact, a stronger statement holds: $V \simeq V_1 \otimes V_2$, where $V_1$ is a representation of $G_1$ and $V_2$ is a representation of $G_2$, but you don't need to prove this.)

Proof

Let $\mathrm{res}_{G_1}^G V$ be the restriction of the irreducible representation $V$ of $G = G_1 \times G_2$ to $G_1$. We will show that $\mathrm{res}_{G_1}^G V \simeq (V_1)^k$ for some irreducible representation $V_1$ of $G_1$ and $k \geq 1$.

Since $\mathrm{res}_{G_1}^G V$ is completely reducible (as a representation of $G_1$), it can be decomposed into a direct sum of irreducible representations of $G_1$. Let $`\mathrm{res}_{G_1}^G V = \bigoplus_{i=1}^m V_i`$, where each $V_i$ is an irreducible representation of $G_1$.

$\mathrm{Hom}_{G_1}(V_1, V_2) = \mathbb{C}$ if $V_1 \simeq V_2$ and is zero otherwise. Since $V$ is irreducible as a representation of $G = G_1 \times G_2$, the only non-zero homomorphisms from $V$ to itself are scalar multiples of the identity map.

# 5
Fix $n$, and denote by $X_k$ the set of all $k$-element subsets of $`\{1, \dots, n\}`$ ($k \leq n$). It carries an action of $S_n$, and we can consider the corresponding representation $V_k$ of $S_n$, where $V_k$ is the space of $\mathbb{C}$-valued functions on $X_k$.

Show that $V_k \simeq V_{n-k}$.

# 6. (Continuation of the previous problem)
Show that $S_n$ has irreducible representations $W_0, W_1, W_2, \ldots, W_{\left\lfloor\frac{n}{2}\right\rfloor}$ such that

$V_k \simeq \bigoplus_{i=0}^k W_i$

for all $k \leq \frac{n}{2}$.
