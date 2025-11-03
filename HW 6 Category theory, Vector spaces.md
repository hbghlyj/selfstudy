# 1.
Verify that the following construction is a contravariant functor $F$ from the category of sets to itself: for a set $A, F(A)$ is the power set of $A$ (that is, the set of all the subsets of $A$ ), while for a map $f: A \rightarrow B$, the induced map $F(f): F(B) \rightarrow F(A)$ sends $X \subset B$ to $f^{-1}(X) \subset A$.

# 2.
Let $\mathcal{C}$ be any category. Fix an object $a \in \mathcal{C}$ and suppose that for any object $x \in \mathcal{C}$, the product $a \times x$ exists. Show that the correspondence

$x \mapsto a \times x$

is a functor. (Technically, there is a subtlety here: we know that if a product exists, it is unique up to isomorphism, however, in order to construct a functor, we need to make a specific choice of $a \times x$ for all $x$. It would be better to say that the functor is defined up to a canonical isomorphism, but this detail is usually ignored.)

# 3.
Let $V$ be a linear space and $P: V \rightarrow V$ be a linear operator such that $P^2=P$. (Operators having this property are called projectors.) Show that $V$ is the internal direct sum of subspaces $\ker(P)$ and $\mathrm{im}(P)$.

# 4.
Continuing with the previous problem, suppose that $\dim(V)=n$. Prove that there exists a basis of $V$ such that the matrix of $P$ is of the form $\mathrm{diag}(1,1, \ldots, 1,0, \ldots, 0)$. (diag denotes the diagonal matrix with given entries.)

# 5.
Fix $n$, and consider the vector space

$V=\{p(t) \in \mathbb{R}[t]: \deg(p) \leq n\}$

over $\mathbb{R}$. Fix $n+1$ numbers $a_0, \ldots, a_n \in \mathbb{R}$ and consider the map

$\phi: V \rightarrow \mathbb{R}^{n+1}: \phi(p)=\left(p\left(a_0\right), \ldots, p\left(a_n\right)\right) .$

Show that $\phi$ is invertible (and therefore an isomorphism of vector spaces) if and only if $a_i$ 's are all distinct.

# 6.
Let $V$ be a vector space over a field $K$. A (linear) functional on $V$ is a linear operator $\phi: V \rightarrow K$. Show that if two functionals $\phi, \psi: V \rightarrow K$ satisfy $\ker(\phi) \subset \ker(\psi)$, there exists $a \in K$ such that $\psi=a \phi$. (If you need to, you can assume that $V$ is finite-dimensional, but it should not be necessary.)

# 7.
Let $K$ be a field and $L \subset K$ be a smaller field (e.g., $L=\mathbb{R}$ and $K=\mathbb{C}$ ). Given a $K$-vector space $V$, we can also consider it as a $L$-vector space, so we get two notions of dimension: as a vector space over $K$ and as a vector space over $L$. Denote them by $\dim_K V$ and $\dim_L V$, respectively. Show that

$\dim_L(V)=\dim_K(V) \cdot \dim_L(K) .$
