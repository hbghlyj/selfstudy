# 1.
Let $V$ be an $n$-dimensional vector space, and let $\phi: V \rightarrow V$ be a linear map. Show that, for any $n$-linear antisymmetric form $\beta(v_1, \ldots, v_n)$ on $V$, we have

$\beta(\phi(v_1), \ldots, \phi(v_n))=\det(\phi) \beta(v_1, \ldots, v_n) .$

(This formalizes the following idea: any "unit of volume" on $V$, given by $\beta$, gets scaled by $\det(\phi)$ when we apply $\phi$.
In fact, this can be used as a definition of $\det(\phi)$: this way, some of its properties, such as independence of basis and multiplicativity become clear.)
Proof

Let's define a new form $\beta'(v_1, \ldots, v_n) = \beta(\phi(v_1), \ldots, \phi(v_n))$. Since $\phi$ is linear and $\beta$ is an $n$-linear antisymmetric form, it follows that $\beta'$ is also an $n$-linear antisymmetric form on $V$.

Proof

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

# 3.
Let $M$ be an $n \times n$ matrix (over some field). Let $V$ be the space of $n \times m$ matrices.

Consider the linear map $m_M: V \rightarrow V$ given by left multiplication by $M:A \mapsto M A$.

Find $\det(m_M)$. (Of course, the answer depends on $M$.)

# 4.
Let $K$ be a field and $V$ be a finite-dimensional vector space. Let

$\gamma: V \times V \rightarrow K$

be an anti-symmetric bilinear form. Show that there exists $k \leq \frac{n}{2}$ and a basis

$`\left\{a_1, \ldots, a_k, b_1, \ldots, b_k, c_1, \ldots, c_{n-2 k}\right\}`$

of $V$ such that

$\gamma(a_i, b_i)=1, \quad \gamma(b_i, a_i)=-1 \quad(i=1, \ldots, k),$

and $\gamma$ vanishes on all other pairs of basis vectors. (When $n=2 k$, this is called a symplectic basis.)

# 5.
Consider $\det(A)$ as a multivariable function of the entries of a real matrix $A$.
Compute the directional derivative of this function at the point $A=I$ in the direction of some matrix $B$.
(Equivalently, find the linear approximation for $f(t)=\det(I+B t)$ at $t=0$.)

# 6.
Let $A$ be a square $n \times n$ matrix whose characteristic polynomial has $n$ roots in $K$, counting with multiplicity.
Consider the Jordan form of $A$: suppose that it consists of blocks $J_{\lambda_i, n_i}$, where $\lambda_i$ is the eigenvalue and $n_i$ is the size of the block.

Express the following invariants of $A$ in terms of $n_i$ and $\lambda_i$: its characteristic polynomial, its minimal polynomial, the dimension of eigenspace for each $\lambda$ (this is called "the geometric multiplicity of an eigenvalue") and rank. (No explanation is required.)

# 7.
Following up on the previous problem, let us go in the opposite direction: explain how to find $\lambda_i$ and $n_i$ from the data of $\operatorname{rk}(A-\lambda I)^k$ for all $\lambda \in K$ and $k>0$.
In particular, this implies that the Jordan form is unique.
