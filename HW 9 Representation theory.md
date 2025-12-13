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

Let $`\mathrm{res}_{G_1}^G V`$ be the restriction of the irreducible representation $V$ of $G = G_1 \times G_2$ to $G_1$. We will show that $\mathrm{res}_{G_1}^G V \simeq (V_1)^k$ for some irreducible representation $V_1$ of $G_1$ and $k \geq 1$.

Since $`\mathrm{res}_{G_1}^G V`$ is completely reducible, we can decompose it into its isotypic components: $`\mathrm{res}_{G_1}^G V = \bigoplus_{i=1}^m W_i`$. For $i \neq j$, the irreducible constituents of $W_i$ and $W_j$ are non-isomorphic.

The action of any $g_2 \in G_2$ on $V$ commutes with the action of $G_1$. Thus, the map $v \mapsto (e, g_2) \cdot v$ is a $G_1$-module endomorphism of $V$. By Schur's Lemma, this map must preserve each isotypic component $W_i$. This means each $W_i$ is a subrepresentation of $V$ under the action of $G_2$.

Since each $W_i$ is also a $G_1$-subrepresentation by definition, it is a subrepresentation of $V$ for the whole group $G = G_1 \times G_2$. But $V$ is irreducible, so it cannot have proper non-trivial subrepresentations. This implies that there can be only one non-zero isotypic component, i.e., $m=1$.

Therefore, $\mathrm{res}_{G_1}^G V$ is isotypic, which means it is a direct sum of $k$ copies of a single irreducible $G_1$-representation $V_1$.

# 5
Fix $n$, and denote by $X_k$ the set of all $k$-element subsets of $`\{1, \dots, n\}`$ ($k \leq n$). It carries an action of $S_n$, and we can consider the corresponding representation $V_k$ of $S_n$, where $V_k$ is the space of $\mathbb{C}$-valued functions on $X_k$.

Show that $V_k \simeq V_{n-k}$.

Proof

The representation $V_k$ is defined as the space of complex-valued functions $f: X_k \rightarrow \mathbb{C}$, where $X_k$ is the set of all $k$-element subsets of $`\{1, \dots, n\}`$. The symmetric group $S_n$ acts on $V_k$ by permuting the elements of the subsets: $(\sigma \cdot f)(A) = f(\sigma^{-1}(A))$ for $\sigma \in S_n$ and $A \in X_k$.

Define a map $\phi: V_k \rightarrow V_{n-k}$ by setting $`\phi(f)(B) = f(\{1, \dots, n\} \setminus B)`$ for any $f \in V_k$ and $B \in X_{n-k}$. Note that if $B$ is an $(n-k)$-element subset, its complement $`\{1, \dots, n\} \setminus B`$ is a $k$-element subset, so it is in $X_k$, and $f$ is defined on it. Thus, $\phi(f)$ is a well-defined function on $X_{n-k}$.

To show that $V_k \simeq V_{n-k}$ as representations, we need to prove that $\phi$ is an isomorphism of $S_n$-representations. This requires showing that $\phi$ is a linear, bijective, and $S_n$-equivariant map.

1.  **Linearity:** For any $f_1, f_2 \in V_k$ and $c \in \mathbb{C}$, and for any $B \in X_{n-k}$:

    $`\phi(f_1 + c f_2)(B) = (f_1 + c f_2)(\{1, \dots, n\} \setminus B) = f_1(\{1, \dots, n\} \setminus B) + c f_2(\{1, \dots, n\} \setminus B) = \phi(f_1)(B) + c \phi(f_2)(B) = (\phi(f_1) + c \phi(f_2))(B)`$.

    Thus, $\phi(f_1 + c f_2) = \phi(f_1) + c \phi(f_2)$, so $\phi$ is linear.

3.  **Bijectivity:** We can define an inverse map $\psi: V_{n-k} \rightarrow V_k$ by $`\psi(h)(A) = h(\{1, \dots, n\} \setminus A)`$ for $h \in V_{n-k}$ and $A \in X_k$.

    For any $f \in V_k$ and $A \in X_k$:

    $`(\psi \circ \phi)(f)(A) = \psi(\phi(f))(A) = \phi(f)(\{1, \dots, n\} \setminus A) = f(\{1, \dots, n\} \setminus (\{1, \dots, n\} \setminus A)) = f(A)`$.

    So, $\psi \circ \phi = \mathrm{id}_{V_k}$. Similarly, $`\phi \circ \psi = \mathrm{id}_{V_{n-k}}`$. Thus, $\phi$ is bijective.

5.  **$S_n$-equivariance:** We need to show that $\phi(\sigma \cdot f) = \sigma \cdot \phi(f)$ for any $\sigma \in S_n$ and $f \in V_k$.

    For any $B \in X_{n-k}$:

    $`(\phi(\sigma \cdot f))(B) = (\sigma \cdot f)(\{1, \dots, n\} \setminus B) = f(\sigma^{-1}(\{1, \dots, n\} \setminus B))`$.

    Since $\sigma^{-1}$ is a permutation, it commutes with the complement operation: $`\sigma^{-1}(\{1, \dots, n\} \setminus B) = \{1, \dots, n\} \setminus \sigma^{-1}(B)`$.

    So, $`(\phi(\sigma \cdot f))(B) = f(\{1, \dots, n\} \setminus \sigma^{-1}(B))`$.

    On the other hand:

    $`(\sigma \cdot \phi(f))(B) = (\phi(f))(\sigma^{-1}(B)) = f(\{1, \dots, n\} \setminus \sigma^{-1}(B))`$.

    Since both sides are equal, $\phi$ is $S_n$-equivariant.

Since $\phi$ is a linear, bijective, and $S_n$-equivariant map, it is an isomorphism of representations. Therefore, $V_k \simeq V_{n-k}$.

# 6. (Continuation of the previous problem)
Show that $S_n$ has irreducible representations $W_0, W_1, W_2, \ldots, W_{\left\lfloor\frac{n}{2}\right\rfloor}$ such that

$V_k \simeq \bigoplus_{i=0}^k W_i$

for all $k \leq \frac{n}{2}$.

Proof

The space $V_k$ consists of all functions $f: X_k \to \mathbb{C}$. To write this as a matrix, we need to choose a basis. The most natural basis is the set of "indicator functions" (or delta functions). For every subset $A \in X_k$, we define a function $\delta_A$ such that:

$\delta_A(B) = 1$ if $B = A$

$\delta_A(B) = 0$ if $B \neq A$

The set of these functions $`\{\delta_A \mid A \in X_k\}`$ forms a basis for $V_k$. The group action is defined as $(\sigma \cdot f)(B) = f(\sigma^{-1} B)$. Let's see what happens when $\sigma$ acts on a basis vector $\delta_A$:

$`(\sigma \cdot \delta_A)(B) = \delta_A(\sigma^{-1} B)`$

This value is $1$ only when $\sigma^{-1} B = A$, which is equivalent to $B = \sigma A$.
Therefore, $\sigma \cdot \delta_A = \delta_{\sigma A}$.
The matrices in such representations are permutation matrices. Their trace equals the number of fixed points of the action.
By Burnside's lemma, the inner product of two permutation characters $\langle \chi_1, \chi_2 \rangle$ equals the number of orbits of the group acting on the product set $X_j \times X_k$.

Compute the inner product of characters to verify the decomposition. The character of $V_k$ evaluated at a permutation $\sigma \in S_n$ is given by the number of $k$-element subsets fixed by $\sigma$. For $j \le k$, the inner product $`\langle \chi_{V_j}, \chi_{V_k} \rangle`$ equals the number of orbits of $S_n$ on $X_j \times X_k$. These orbits are classified by the size of the intersection of the two subsets. Since the problem states $k \le n/2$, we have $j+k \le n$, which ensures that any intersection size from $0$ to $j$ is possible. This gives $j+1$ distinct orbits, so $`\langle \chi_{V_j}, \chi_{V_k} \rangle = j+1`$.

Define the characters $\chi_{W_i}$ inductively:

$`\chi_{W_k} = \chi_{V_k} - \chi_{V_{k-1}}`$ for $k \ge 1$ and $`\chi_{W_0} = \chi_{V_0}`$.

Then need to show that $`\langle \chi_{W_i}, \chi_{W_j} \rangle = \delta_{ij}`$, which proves that the $W_i$ are distinct irreducible representations.

Finally, summing the character definitions telescopically gives $`\chi_{V_k} = \sum_{i=0}^k \chi_{W_i}`$, which proves the desired isomorphism.
