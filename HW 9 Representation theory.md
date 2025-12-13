# 1
Let  be a finite group. Prove the following 'inverse Schur Lemma': if every -equivariant map    is scalar, then  is irreducible. You may need to make additional assumptions on the field for the statement to hold, make sure to clearly state this!

Proof

Let  be a representation of a finite group  over a field . We will assume that the field  is algebraically closed and that the characteristic of  does not divide the order of the group .
Suppose, for the sake of contradiction, that  is not irreducible. Then there exists a nontrivial proper subrepresentation  .

Since the characteristic of  does not divide , by Maschke's Theorem,  is completely reducible. This means that  has a complement  which is also a subrepresentation, such that   .

Consider the projection map    onto  along . For any    where   and  , we define  .

This map is -equivariant. For any  ,    :
           (since  are subrepresentations,    and   ).

And    .

So    .

The map  is not a scalar multiple of the identity map.
- If  , then   , which contradicts  being a nontrivial subrepresentation.
- If    for some  , then  must be an isomorphism. But the image of  is , which is a proper subspace of , so  is not surjective. This is a contradiction.

Thus,  is a non-scalar -equivariant map from  to itself. This contradicts our assumption that every such map is scalar. Therefore,  must be irreducible.
# 2
Suppose  is a completely reducible representation of a group . Show that for every subrepresentation  , the quotient  is completely reducible. (Obviously, we are assuming that Maschke's Theorem does not apply, otherwise the question is trivial.)

Proof

Let  be a completely reducible representation of a group , and let   be a subrepresentation. We want to show that the quotient representation  is also completely reducible.

To prove this, we will use the property that a representation is completely reducible if and only if every subrepresentation has a complement.

Let  be an arbitrary subrepresentation of .

Let   be its preimage in  under the quotient map   .  is a subrepresentation of  containing .

Since  is completely reducible,  has a complement  in , so   .

Also, since  is a subrepresentation of a completely reducible representation ,  is itself completely reducible. Thus, the subrepresentation   has a complement  in , so   .

Combining these, we get    .

Let    be the quotient map.

From    , we see that    .

The subrepresentation  is     .

Therefore,   , which shows that  has a complement in  (namely ).

Since every subrepresentation  of  has a complement,  is completely reducible.
# 3
Let  be an irreducible finite-dimensional representation of a group . Show that its dual  is irreducible as well.

Proof

The dual representation  of a representation  of a group  is defined by the action:

    for all  ,  , and  .

To show that  is irreducible, we need to demonstrate that there are no nontrivial proper subrepresentations of .

Let  be a subrepresentation of . We will show that  is either  or .

Consider the annihilator of  in :

     .

We first show that  is a subrepresentation of . Let   and  . We need to show that   . This means we must show that    for all  .

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

The character of $V_k$ evaluated at a permutation $\sigma \in S_n$ is given by the number of $k$-element subsets fixed by $\sigma$. For $j \le k$, the inner product $`\langle \chi_{V_j}, \chi_{V_k} \rangle`$ equals the number of orbits of $S_n$ on $X_j \times X_k$. These orbits are classified by the size of the intersection of the two subsets. Since the problem states $k \le n/2$, we have $j+k \le n$, which ensures that any intersection size from $0$ to $j$ is possible. This gives $j+1$ distinct orbits, so $`\langle \chi_{V_j}, \chi_{V_k} \rangle = j+1`$.

Since a complex representation of a finite group is determined up to isomorphism by its character, we can define the irreducible representations $W_k$ by their characters. We set $\chi_{W_0} = \chi_{V_0}$ and for $k \ge 1$:$$\chi_{W_k} = \chi_{V_k} - \chi_{V_{k-1}}$$We now verify these are distinct irreducible representations by checking orthonormality. Using bilinearity and the formula derived above ($\langle \chi_{V_a}, \chi_{V_b} \rangle = \min(a,b) + 1$):$$\langle \chi_{W_k}, \chi_{W_k} \rangle = \langle \chi_{V_k} - \chi_{V_{k-1}}, \chi_{V_k} - \chi_{V_{k-1}} \rangle$$$$= \langle \chi_{V_k}, \chi_{V_k} \rangle - 2\langle \chi_{V_k}, \chi_{V_{k-1}} \rangle + \langle \chi_{V_{k-1}}, \chi_{V_{k-1}} \rangle$$$$= (k+1) - 2(k) + k = 1$$Similarly, for $j < k$, one can show $\langle \chi_{W_j}, \chi_{W_k} \rangle = 0$. Thus, the $W_i$ are irreducible and distinct. Summing the definition telescopically gives $\chi_{V_k} = \sum_{i=0}^k \chi_{W_i}$, proving the isomorphism:$$V_k \simeq \bigoplus_{i=0}^k W_i$$
