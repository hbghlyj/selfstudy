# 1.
Let $V$ be an $n$-dimensional vector space, and let $\phi: V \rightarrow V$ be a linear map. Show that, for any $n$-linear antisymmetric form $\beta(v_1, \ldots, v_n)$ on $V$, we have

$\beta(\phi(v_1), \ldots, \phi(v_n))=\det(\phi) \beta(v_1, \ldots, v_n) .$

(This formalizes the following idea: any "unit of volume" on $V$, given by $\beta$, gets scaled by $\det(\phi)$ when we apply $\phi$.
In fact, this can be used as a definition of $\det(\phi)$: this way, some of its properties, such as independence of basis and multiplicativity become clear.)

Proof

Let $`\{e_1, e_2, \ldots, e_n\}`$ be a basis of $V$. Since $\beta$ is an $n$-linear antisymmetric form, it is completely determined by its value on the basis vectors. Let $\beta(e_1, e_2, \ldots, e_n) = c$ for some scalar $c \in K$.

Now, consider the linear map $\phi: V \rightarrow V$. The action of $\phi$ on the basis vectors can be expressed as:

$\phi(e_i) = \sum_{j=1}^{n} a_{ji} e_j,$

where $A = (a_{ji})$ is the matrix representation of $\phi$ with respect to the basis $\{e_1, e_2, \ldots, e_n\}$.

To compute $\beta(\phi(v_1), \ldots, \phi(v_n))$, we can express each $v_i$ in terms of the basis:$v_i = \sum_{k=1}^{n} x_{ki} e_k,$

for some scalars $x_{ki} \in K$. Then,

$\phi(v_i) = \phi\left(\sum_{k=1}^{n} x_{ki} e_k\right) = \sum_{k=1}^{n} x_{ki} \phi(e_k) = \sum_{k=1}^{n} x_{ki} \sum_{j=1}^{n} a_{jk} e_j = \sum_{j=1}^{n} \left(\sum_{k=1}^{n} a_{jk} x_{ki}\right) e_j.$

Now, we can write:

$\beta(\phi(v_1), \ldots, \phi(v_n)) = \beta\left(\sum_{j=1}^{n} \left(\sum_{k=1}^{n} a_{jk} x_{k1}\right) e_j, \ldots, \sum_{j=1}^{n} \left(\sum_{k=1}^{n} a_{jk} x_{kn}\right) e_j\right).$

Using the multilinearity and antisymmetry of $\beta$, we can expand this expression. The only non-zero contributions come from terms where we select one $e_j$ from each $\phi(v_i)$, leading to:

$\beta(\phi(v_1), \ldots, \phi(v_n)) = \sum_{\sigma \in S_n} \text{sgn}(\sigma) \prod_{i=1}^{n} \left(\sum_{k=1}^{n} a_{\sigma(i)k} x_{ki}\right) \beta(e_{\sigma(1)}, e_{\sigma(2)}, \ldots, e_{\sigma(n)}).$

Since $\beta$ is antisymmetric, we have $\beta(e_{\sigma(1)}, e_{\sigma(2)}, \ldots, e_{\sigma(n)}) = \text{sgn}(\sigma) \beta(e_1, e_2, \ldots, e_n) = \text{sgn}(\sigma) c$. Thus, we can factor out $c$:

$\beta(\phi(v_1), \ldots, \phi(v_n)) = c \sum_{\sigma \in S_n} \text{sgn}(\sigma)^2 \prod_{i=1}^{n} \left(\sum_{k=1}^{n} a_{\sigma(i)k} x_{ki}\right).$

Recognizing that $\text{sgn}(\sigma)^2 = 1$, we can rewrite this as:

$\beta(\phi(v_1), \ldots, \phi(v_n)) = c \det(A) \prod_{i=1}^{n} x_{ii} = \det(\phi) \beta(v_1, \ldots, v_n).$

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
