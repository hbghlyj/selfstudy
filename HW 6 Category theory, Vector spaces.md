# 1.
Verify that the following construction is a contravariant functor $F$ from the category of sets to itself: for a set $A, F(A)$ is the power set of $A$ (that is, the set of all the subsets of $A$ ), while for a map $f: A \rightarrow B$, the induced map $F(f): F(B) \rightarrow F(A)$ sends $X \subset B$ to $f^{-1}(X) \subset A$.

# 2.
Let $\mathcal{C}$ be any category. Fix an object $a \in \mathcal{C}$ and suppose that for any object $x \in \mathcal{C}$, the product $a \times x$ exists. Show that the correspondence

$x \mapsto a \times x$

is a functor. (Technically, there is a subtlety here: we know that if a product exists, it is unique up to isomorphism, however, in order to construct a functor, we need to make a specific choice of $a \times x$ for all $x$. It would be better to say that the functor is defined up to a canonical isomorphism, but this detail is usually ignored.)

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

(⇐) Now suppose the $a_i$'s are all distinct. Since $V$ is the space of polynomials of degree at most $n$, any polynomial is uniquely determined by its values at $n+1$ distinct points since Vandermonde matrices are invertible. Thus, for any vector in $\mathbb{R}^{n+1}$, there exists a unique polynomial in $V$ that maps to it under $\phi$. This shows that $\phi$ is invertible.

# 6.
Let $V$ be a vector space over a field $K$. A (linear) functional on $V$ is a linear operator $\phi: V \rightarrow K$. Show that if two functionals $\phi, \psi: V \rightarrow K$ satisfy $\ker(\phi) \subset \ker(\psi)$, there exists $a \in K$ such that $\psi=a \phi$. (If you need to, you can assume that $V$ is finite-dimensional, but it should not be necessary.)

# 7.
Let $K$ be a field and $L \subset K$ be a smaller field (e.g., $L=\mathbb{R}$ and $K=\mathbb{C}$ ). Given a $K$-vector space $V$, we can also consider it as a $L$-vector space, so we get two notions of dimension: as a vector space over $K$ and as a vector space over $L$. Denote them by $\dim_K V$ and $\dim_L V$, respectively. Show that

$\dim_L(V)=\dim_K(V) \cdot \dim_L(K) .$
