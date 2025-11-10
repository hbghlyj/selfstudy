# 1.
Let $V$ be an $n$-dimensional vector space, and let $\phi: V \rightarrow V$ be a linear map. Show that, for any $n$-linear antisymmetric form $\beta(v_1, \ldots, v_n)$ on $V$, we have

$\beta(\phi(v_1), \ldots, \phi(v_n))=\det(\phi) \beta(v_1, \ldots, v_n) .$

(This formalizes the following idea: any "unit of volume" on $V$, given by $\beta$, gets scaled by $\det(\phi)$ when we apply $\phi$.
In fact, this can be used as a definition of $\det(\phi)$: this way, some of its properties, such as independence of basis and multiplicativity become clear.)

Proof

Let's define a new form $\beta'(v_1, \ldots, v_n) = \beta(\phi(v_1), \ldots, \phi(v_n))$. Since $\phi$ is linear and $\beta$ is an $n$-linear antisymmetric form, it follows that $\beta'$ is also an $n$-linear antisymmetric form on $V$.

The space of $n$-linear antisymmetric forms on an $n$-dimensional vector space $V$ is one-dimensional. Therefore, $\beta'$ must be a scalar multiple of $\beta$. That is, there exists a scalar $\lambda \in K$ such that:

$\beta' = \lambda \beta$

$\beta(\phi(v_1), \ldots, v_n) = \lambda \beta(v_1, \ldots, v_n)$

To find the value of $\lambda$, we can evaluate this identity on a basis $\{e_1, \ldots, e_n\}$ of $V$:
$\beta(\phi(e_1), \ldots, \phi(e_n)) = \lambda \beta(e_1, \ldots, e_n)$

Let $A = (a_{ij})$ be the matrix representation of $\phi$ with respect to this basis, where $\phi(e_j) = \sum_{i=1}^n a_{ij} e_i$. By substituting this into the left-hand side and using the multilinearity of $\beta$, we get:

$\beta(\phi(e_1), \ldots, \phi(e_n)) = \beta\left(\sum_{i_1=1}^n a_{i_1 1} e_{i_1}, \ldots, \sum_{i_n=1}^n a_{i_n n} e_{i_n}\right)$

$= \sum_{i_1, \ldots, i_n=1}^n a_{i_1 1} \cdots a_{i_n n} \beta(e_{i_1}, \ldots, e_{i_n})$

Since $\beta$ is antisymmetric, $\beta(e_{i_1}, \ldots, e_{i_n})$ is non-zero only if the indices $(i_1, \ldots, i_n)$ are a permutation of $(1, \ldots, n)$. For any permutation $\sigma \in S_n$, we have $\beta(e_{\sigma(1)}, \ldots, e_{\sigma(n)}) = \text{sgn}(\sigma) \beta(e_1, \ldots, e_n)$.


The sum thus simplifies to:
$\left(\sum_{\sigma \in S_n} \text{sgn}(\sigma) a_{\sigma(1) 1} \cdots a_{\sigma(n) n}\right) \beta(e_1, \ldots, e_n)$

The expression in the parentheses is the Leibniz formula for the determinant of $A$. Therefore:

$\beta(\phi(e_1), \ldots, \phi(e_n)) = \det(A) \beta(e_1, \ldots, e_n)$

By comparing this with our earlier equation, we find that $\lambda = \det(A)$. Since the determinant of a linear map is defined as the determinant of its matrix representation, $\det(\phi) = \det(A)$. Thus, $\lambda = \det(\phi)$.

This gives us the final result:

$\beta(\phi(v_1), \ldots, v_n) = \det(\phi) \beta(v_1, \ldots, v_n)$

# 2.
Let $V$ be the space of polynomials of degree at most $n$ (over some field $K$; if you want, you can assume $K=\mathbb{R}$).

Fix $a, b \in \mathbb{R}$ and consider the linear map

$\phi: V \rightarrow V: p(t) \mapsto p(a t+b) .$

Compute $\det(\phi)$.

Proof

The space $V$ of polynomials of degree at most $n$ has a basis given by the monomials $`\{1, t, t^2, \ldots, t^n\}`$.

To find the matrix representation of $\phi$ with respect to the ordered basis $`B = \{1, t, t^2, \ldots, t^n\}`$, we note that $\phi(t^k) = (at+b)^k$ is a polynomial of degree $k$. Thus, its expansion only involves basis vectors $t^j$ with $j \le k$. When the matrix of $\phi$ is constructed with columns as the images of the basis vectors, this property ensures the matrix is upper triangular.

The diagonal entry corresponding to $t^k$ is the coefficient of $t^k$ in the expansion of $\phi(t^k) = (a t + b)^k$, which is $a^k$.

The determinant of an upper triangular matrix is the product of its diagonal entries. Thus, we have:

$\det(\phi) = \prod_{k=0}^n a^k = a^{0+1+2+\cdots+n} = a^{\frac{n(n+1)}{2}}$

# 3.
Let $M$ be an $n \times n$ matrix (over some field). Let $V$ be the space of $n \times m$ matrices.

Consider the linear map $m_M: V \rightarrow V$ given by left multiplication by $M:A \mapsto M A$.

Find $\det(m_M)$. (Of course, the answer depends on $M$.)

Proof

For a fixed column index $j$, the subspace $V_j$ of matrices with non-zero entries only in column $j$ is invariant under $m_M$.
The action of the map within this subspace is just $v \mapsto Mv$ (if we identify the subspace with $K^n$ by just looking at the $j$-th column). Therefore, the action of $m_M$ on this $n$-dimensional subspace is represented by the matrix $M$.

Since the whole space $V$ is a direct sum of $m$ such subspaces, the matrix representation of $m_M$ with respect to basis vectors ordered by columns is a block diagonal matrix with $m$ blocks, each being $M$. Therefore, the determinant is the product of the determinants of the blocks: $\det(m_M) = (\det(M))^m$.

# 4.
Let $K$ be a field and $V$ be a finite-dimensional vector space. Let

$\gamma: V \times V \rightarrow K$

be an anti-symmetric bilinear form. Show that there exists $k \leq \frac{n}{2}$ and a basis

$`\left\{a_1, \ldots, a_k, b_1, \ldots, b_k, c_1, \ldots, c_{n-2 k}\right\}`$

of $V$ such that

$\gamma(a_i, b_i)=1, \quad \gamma(b_i, a_i)=-1 \quad(i=1, \ldots, k),$

and $\gamma$ vanishes on all other pairs of basis vectors. (When $n=2 k$, this is called a symplectic basis.)

Proof

We will prove this by induction on the dimension $n$ of the vector space $V$.

Base Case: If $n=0$, the statement is trivially true as there are no vectors to consider.

Inductive Step: Assume the statement holds for all vector spaces of dimension less than $n$. We will show it holds for dimension $n$.

If $\gamma$ is the zero form, then we can take $k=0$ and choose any basis for $V$, and the statement holds.

If $\gamma$ is not the zero form, there exist vectors $u, v \in V$ such that $\gamma(u, v) \neq 0$. We can scale $u$ and $v$ such that $\gamma(u, v) = 1$. Set $a_1 = u$ and $b_1 = v$. Note that $u$ and $v$ must be linearly independent. If $v = c u$ for some scalar $c$, then $\gamma(u, v) = \gamma(u, c u) = c \gamma(u, u) = 0$ (since $\gamma$ is anti-symmetric), which contradicts $\gamma(u, v) \neq 0$. Thus, $`W = \text{span}\{a_1, b_1\}`$ is a 2-dimensional subspace.

Now, consider the subspace $`W = \text{span}\{a_1, b_1\}`$. The restriction of $\gamma$ to $W$ is non-degenerate, and we can define the orthogonal complement of $W$ with respect to $\gamma$:

$`W^\perp = \{x \in V \mid \gamma(x, w) = 0 \text{ for all } w \in W\}`$

The dimension of $W^\perp$ is $n-2$. This follows from the fact that the restriction of $\gamma$ to $W$ is non-degenerate, implying $V = W \oplus W^\perp$. Since $\dim(V) = n$ and $\dim(W) = 2$ (as $a_1$ and $b_1$ are linearly independent), we have $\dim(W^\perp) = \dim(V) - \dim(W) = n - 2$. By the inductive hypothesis, there exists a basis for $W^\perp$ of the form:

$`\{a_2, \ldots, a_k, b_2, \ldots, b_k, c_1, \ldots, c_{n-2k}\}`$

such that $\gamma(a_i, b_i) = 1$, $\gamma(b_i, a_i) = -1$ for $i=2, \ldots, k$, and $\gamma$ vanishes on all other pairs of basis vectors in $W^\perp$.

Combining the basis $`\{a_1, b_1\}`$ with the basis of $W^\perp$, we obtain a basis for $V$:

$`\{a_1, b_1, a_2, \ldots, a_k, b_2, \ldots, b_k, c_1, \ldots, c_{n-2k}\}`$

This basis satisfies the required properties, completing the inductive step.

# 5.
Consider $\det(A)$ as a multivariable function of the entries of a real matrix $A$.
Compute the directional derivative of this function at the point $A=I$ in the direction of some matrix $B$.
(Equivalently, find the linear approximation for $f(t)=\det(I+B t)$ at $t=0$.)

Proof

By Leibniz formula, we have

$f(t) = \det(I + tB) = \sum_{\sigma \in S_n} \text{sgn}(\sigma) \prod_{i=1}^n (I + tB)_{i, \sigma(i)}$

where $`(I + tB)_{i, \sigma(i)} = \delta_{i, \sigma(i)} + t B_{i, \sigma(i)}`$.

The derivative at $t=0$ is the coefficient of the linear term in $t$. For the term linear in $t$ to be non-zero in the expansion of $\prod_{i=1}^n (\delta_{i, \sigma(i)} + t B_{i, \sigma(i)})$, at most one of the $\delta_{i, \sigma(i)}$ terms can be zero. This condition is only met by the identity permutation ($\sigma = \text{id}$). For any other permutation, at least two indices are not fixed, causing the linear term to vanish. For $\sigma = \text{id}$, the linear term's coefficient is $\sum_{i=1}^n B_{i,i}$, so:

$f'(0) = \sum_{i=1}^n B_{i, i} = \text{tr}(B)$

# 6.
Let $A$ be a square $n \times n$ matrix whose characteristic polynomial has $n$ roots in $K$, counting with multiplicity.
Consider the Jordan form of $A$: suppose that it consists of blocks $J_{\lambda_i, n_i}$, where $\lambda_i$ is the eigenvalue and $n_i$ is the size of the block.

Express the following invariants of $A$ in terms of $n_i$ and $\lambda_i$: its characteristic polynomial, its minimal polynomial, the dimension of eigenspace for each $\lambda$ (this is called "the geometric multiplicity of an eigenvalue") and rank. (No explanation is required.)

Proof

- Characteristic Polynomial:
  $`p_A(t) = \prod_{i} (t - \lambda_i)^{n_i}`$
- Minimal Polynomial:
  $`m_A(t) = \prod_{i} (t - \lambda_i)^{m_i}`$, where $m_i$ is the size of the largest Jordan block corresponding to $\lambda_i$.
- Geometric Multiplicity of Eigenvalue $\lambda$:
  $`g_\lambda = \text{number of Jordan blocks corresponding to } \lambda`$
- Rank of $A$:
  $`\text{rk}(A) = n - \sum_{i} (n_i - 1)`$, where the sum is taken over all Jordan blocks.

# 7.
Following up on the previous problem, let us go in the opposite direction: explain how to find $\lambda_i$ and $n_i$ from the data of $\mathrm{rk}(A-\lambda I)^k$ for all $\lambda \in K$ and $k>0$.
In particular, this implies that the Jordan form is unique.
