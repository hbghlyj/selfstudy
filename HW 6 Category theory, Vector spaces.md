# 1.
Verify that the following construction is a contravariant functor $F$ from the category of sets to itself: for a set $A$, $F(A)$ is the power set of $A$ (that is, the set of all the subsets of $A$), while for a map $f: A \rightarrow B$, the induced map $F(f): F(B) \rightarrow F(A)$ sends $X \subset B$ to $f^{-1}(X) \subset A$.

Proof: To verify that $F$ is a contravariant functor, we need to check two properties:

1. **Preservation of composition**: For any two maps $f: A \rightarrow B$ and $g: B \rightarrow C$, we need to show that $F(g \circ f) = F(f) \circ F(g)$. 

   Let $X \subset C$. Then,
   
   $F(g \circ f)(X) = (g \circ f)^{-1}(X) = f^{-1}(g^{-1}(X)).$

   On the other hand,
   
   $(F(f) \circ F(g))(X) = F(f)(F(g)(X)) = F(f)(g^{-1}(X)) = f^{-1}(g^{-1}(X)).$

   Thus, $F(g \circ f)(X) = (F(f) \circ F(g))(X)$ for all $X \subset C$, confirming that $F$ preserves composition.

2. **Preservation of identity**: For any set $A$, we need to show that $`F(\text{id}_A) = \text{id}_{F(A)}`$.

   Let $X \subset A$. Then $`F(\text{id}_A)(X) = \text{id}_A^{-1}(X) = X`$. The identity map on $F(A)$, $\text{id}_{F(A)}$, also sends $X$ to $X$. Thus, $`F(\text{id}_A) = \text{id}_{F(A)}`$, confirming that $F$ preserves identity morphisms.

# 2.
Let $\mathcal{C}$ be any category. Fix an object $a \in \mathcal{C}$ and suppose that for any object $x \in \mathcal{C}$, the product $a \times x$ exists. Show that the correspondence

$x \mapsto a \times x$

is a functor. (Technically, there is a subtlety here: we know that if a product exists, it is unique up to isomorphism, however, in order to construct a functor, we need to make a specific choice of $a \times x$ for all $x$. It would be better to say that the functor is defined up to a canonical isomorphism, but this detail is usually ignored.)

Proof: To show that the correspondence $F: \mathcal{C} \rightarrow \mathcal{C}$ defined by $F(x) = a \times x$ is a functor, we need to verify two properties:

1. **Preservation of composition**: For any two morphisms $f: x \rightarrow y$ and $g: y \rightarrow z$ in $\mathcal{C}$, we need to show that $F(g \circ f) = F(g) \circ F(f)$.

   The product $a \times x$ comes with projection morphisms $\pi_a: a \times x \rightarrow a$ and $\pi_x: a \times x \rightarrow x$. Given a morphism $f: x \rightarrow y$, the universal property of the product $a \times y$ (with projections $\pi'_a, \pi'_y$) defines a unique morphism $F(f): a \times x \rightarrow a \times y$ such that $\pi'_a \circ F(f) = \pi_a$ and $\pi'_y \circ F(f) = f \circ \pi_x$. 

   To show $F(g \circ f) = F(g) \circ F(f)$, we verify that $F(g) \circ F(f)$ satisfies the universal property that uniquely defines $F(g \circ f)$. The morphism $F(g \circ f)$ is the unique map from $a \times x$ to $a \times z$ such that $\pi''_a \circ F(g \circ f) = \pi_a$ and $\pi''_z \circ F(g \circ f) = (g \circ f) \circ \pi_x$, where $\pi''_a, \pi''_z$ are projections from $a \times z$.

   Let's check the composition $F(g) \circ F(f)$:
   - $\pi''_a \circ (F(g) \circ F(f)) = (\pi''_a \circ F(g)) \circ F(f) = \pi'_a \circ F(f) = \pi_a$.
   - $\pi''_z \circ (F(g) \circ F(f)) = (\pi''_z \circ F(g)) \circ F(f) = (g \circ \pi'_y) \circ F(f) = g \circ (\pi'_y \circ F(f)) = g \circ (f \circ \pi_x) = (g \circ f) \circ \pi_x$.

   Since $F(g) \circ F(f)$ satisfies the same defining properties as $F(g \circ f)$, by uniqueness, they must be equal.

2. **Preservation of identity**: For any object $x \in \mathcal{C}$, we need to show that $F(\text{id}_x) = \text{id}_{F(x)}$.

    The identity morphism $\text{id}_x: x \rightarrow x$ induces a unique morphism $F(\text{id}_x): a \times x \rightarrow a \times x$. By the universal property of the product $a \times x$, this morphism must satisfy:
    1. $\pi_a \circ F(\text{id}_x) = \pi_a$
    2. $\pi_x \circ F(\text{id}_x) = \text{id}_x \circ \pi_x = \pi_x$

    The identity morphism on $F(x) = a \times x$, which is $\text{id}_{a \times x}$, also satisfies these properties:
    1. $\pi_a \circ \text{id}_{a \times x} = \pi_a$
    2. $\pi_x \circ \text{id}_{a \times x} = \pi_x$

    By the uniqueness of the morphism defined by these properties, we must have $F(\text{id}_x) = \text{id}_{a \times x} = \text{id}_{F(x)}$.

# 3.
Let $V$ be a linear space and $P: V \rightarrow V$ be a linear operator such that $P^2=P$. (Operators having this property are called projectors.) Show that $V$ is the internal direct sum of subspaces $\ker(P)$ and $\mathrm{im}(P)$.

Proof: Let $v \in V$. Then $v = P(v) + (v - P(v))$. Since $P^2 = P$, we have $P(v - P(v)) = P(v) - P^2(v) = P(v) - P(v) = 0$, so $v - P(v) \in \ker(P)$. Also, $P(v) \in \mathrm{im}(P)$, so $v = P(v) + (v - P(v))$ is a sum of elements from $\mathrm{im}(P)$ and $\ker(P)$.

To show that the sum is direct, suppose $w \in \mathrm{im}(P) \cap \ker(P)$. Then $w = P(u)$ for some $u \in V$, and $P(w) = 0$. Substituting the first equation into the second gives $P(P(u)) = 0$, so $P^2(u) = 0$. Since $P^2=P$, we have $P(u)=0$. As $w=P(u)$, it follows that $w=0$, so the intersection is trivial.


# 4.
Continuing with the previous problem, suppose that $\dim(V)=n$. Prove that there exists a basis of $V$ such that the matrix of $P$ is of the form $\mathrm{diag}(1,1, \ldots, 1,0, \ldots, 0)$. (diag denotes the diagonal matrix with given entries.)

Proof: Since $V = \ker(P) \oplus \mathrm{im}(P)$, we can form a basis for $V$ by combining a basis for $\ker(P)$ and a basis for $\mathrm{im}(P)$. Let $`\{u_1, \ldots, u_{n-k}\}`$ be a basis for $\ker(P)$ and $`\{v_1, \ldots, v_k\}`$ be a basis for $\mathrm{im}(P)$. For any $u_i$, $P(u_i) = 0$ by definition. For any $v_j \in \mathrm{im}(P)$, we know $v_j = P(w)$ for some $w \in V$. Since $P^2=P$, it follows that $P(v_j) = P(P(w)) = P^2(w) = P(w) = v_j$. Therefore, in the basis $`\{v_1, \ldots, v_k, u_1, \ldots, u_{n-k}\}`$, the matrix of $P$ is $\mathrm{diag}(1, \ldots, 1, 0, \ldots, 0)$, with $k$ ones and $n-k$ zeros.

# 5.
Fix $n$, and consider the vector space

$`V=\{p(t) \in \mathbb{R}[t]: \deg(p) \leq n\}`$

over $\mathbb{R}$. Fix $n+1$ numbers $a_0, \ldots, a_n \in \mathbb{R}$ and consider the map

$\phi: V \rightarrow \mathbb{R}^{n+1}: \phi(p)=\left(p\left(a_0\right), \ldots, p\left(a_n\right)\right) .$

Show that $\phi$ is invertible (and therefore an isomorphism of vector spaces) if and only if $a_i$ 's are all distinct.

Proof: 

(⇒) Suppose $\phi$ is invertible. If the $a_i$'s were not all distinct, say $a_i = a_j$ for some $i \neq j$, then for any polynomial $p(t)$, we would have $p(a_i) = p(a_j)$. This implies the image of $\phi$ is contained in the proper subspace of $\mathbb{R}^{n+1}$ where the $i$-th and $j$-th coordinates are equal. Thus, $\phi$ is not surjective. A linear map between finite-dimensional spaces of the same dimension is invertible if and only if it is surjective, so this contradicts the assumption that $\phi$ is invertible.

(⇐) Now suppose the $a_i$'s are all distinct. Since $V$ is the space of polynomials of degree at most $n$, any polynomial is uniquely determined by its values at $n+1$ distinct points, as the determinant of the corresponding Vandermonde matrix is non-zero. Thus, for any vector in $\mathbb{R}^{n+1}$, there exists a unique polynomial in $V$ that maps to it under $\phi$. This shows that $\phi$ is invertible.

# 6.
Let $V$ be a vector space over a field $K$. A (linear) functional on $V$ is a linear operator $\phi: V \rightarrow K$. Show that if two functionals $\phi, \psi: V \rightarrow K$ satisfy $\ker(\phi) \subset \ker(\psi)$, there exists $a \in K$ such that $\psi=a \phi$. (If you need to, you can assume that $V$ is finite-dimensional, but it should not be necessary.)

Proof: If $\phi$ is the zero functional, then $\ker(\phi) = V$, and since $\ker(\phi) \subset \ker(\psi)$, it follows that $\ker(\psi) = V$, which means $\psi$ is also the zero functional. In this case, we can take $a=0$.

Now, assume $\phi$ is not the zero functional. Then there exists some $v_0 \in V$ such that $\phi(v_0) \neq 0$. Define $a = \frac{\psi(v_0)}{\phi(v_0)}$. We will show that $\psi = a \phi$. For any $v \in V$, we can write

$v = v_1 + \frac{\phi(v)}{\phi(v_0)} v_0$,

where $v_1 \in \ker(\phi)$. Then,

$\psi(v) = \psi(v_1) + \frac{\phi(v)}{\phi(v_0)} \psi(v_0) = 0 + \frac{\phi(v)}{\phi(v_0)} \cdot a \phi(v_0) = a \phi(v)$.

Thus, $\psi = a \phi$.

# 7.
Let $K$ be a field and $L \subset K$ be a smaller field (e.g., $L=\mathbb{R}$ and $K=\mathbb{C}$ ). Given a $K$-vector space $V$, we can also consider it as a $L$-vector space, so we get two notions of dimension: as a vector space over $K$ and as a vector space over $L$. Denote them by $\dim_K V$ and $\dim_L V$, respectively. Show that

$\dim_L(V)=\dim_K(V) \cdot \dim_L(K) .$

Proof: Let $\dim_K(V) = m$ and $\dim_L(K) = n$. Let $`\{v_1, v_2, \ldots, v_m\}`$ be a basis of $V$ over $K$, and $`\{k_1, k_2, \ldots, k_n\}`$ be a basis of $K$ over $L$. We claim that the set

$`\{k_i v_j : 1 \leq i \leq n, 1 \leq j \leq m\}`$

is a basis of $V$ over $L$.

To show that this set spans $V$ over $L$, take any $v \in V$. Since $`\{v_1, \ldots, v_m\}`$ is a basis over $K$, we can write

$v = \sum_{j=1}^m a_j v_j$

for some $a_j \in K$. Each $a_j$ can be expressed as a linear combination of the basis elements of $K$ over $L$:

$a_j = \sum_{i=1}^n b_{ij} k_i$

for some $b_{ij} \in L$. Substituting this back, we have

$v = \sum_{j=1}^m \left( \sum_{i=1}^n b_{ij} k_i \right) v_j = \sum_{i=1}^n \sum_{j=1}^m b_{ij} (k_i v_j)$,

which shows that $v$ is in the span of $`\{k_i v_j\}`$ over $L$.

To show linear independence, suppose we have a linear combination over $L$ that equals zero:

$\sum_{i=1}^n \sum_{j=1}^m c_{ij} (k_i v_j) = 0$

for some $c_{ij} \in L$. Grouping terms by $v_j$, we get

$\sum_{j=1}^m \left( \sum_{i=1}^n c_{ij} k_i \right) v_j = 0$.

Since $`\{v_1, \ldots, v_m\}`$ is a basis over $K$, each coefficient must be zero:

$\sum_{i=1}^n c_{ij} k_i = 0$ for all $j$.

Since $`\{k_1, \ldots, k_n\}`$ is a basis of $K$ over $L$, it follows that each $c_{ij} = 0$. Thus, the set $`\{k_i v_j\}`$ is linearly independent over $L$.

Having shown that the set $`\{k_i v_j : 1 \leq i \leq n, 1 \leq j \leq m\}`$ spans $V$ over $L$ and is linearly independent, it forms a basis for $V$ over $L$. This basis contains $m \cdot n$ elements, so we conclude that $\dim_L(V) = m \cdot n = \dim_K(V) \cdot \dim_L(K)$.
