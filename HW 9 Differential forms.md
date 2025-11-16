# 1. (Lee 14-1, 4)

Let $V$ be a finite-dimensional vector space and $v_1, \ldots, v_k \in V$. Prove that $v_1, \ldots, v_k$ are linearly dependent if and only if $v_1 \wedge \cdots \wedge v_k=0$.

Proof

($\Rightarrow$) If $v_1, \ldots, v_k$ are linearly dependent, then there exist scalars $a_1, \ldots, a_k$, not all zero, such that

$\sum_{i=1}^k a_i v_i = 0.$

Then, since not all coefficients are zero, we may assume without loss of generality that $a_1 \neq 0$. Wedging the linear dependence equation with $v_2 \wedge \dots \wedge v_k$ gives:

$0 = \left(\sum_{i=1}^k a_i v_i\right) \wedge v_2 \wedge \dots \wedge v_k = a_1(v_1 \wedge v_2 \wedge \dots \wedge v_k)$

All other terms in the expansion are zero because they contain repeated vectors. Since $a_1 \neq 0$, we conclude that $v_1 \wedge \dots \wedge v_k = 0$.

($\Leftarrow$) Conversely, suppose $v_1 \wedge \cdots \wedge v_k = 0$. If $v_1, \ldots, v_k$ were linearly independent, they would form a basis for a $k$-dimensional subspace of $V$. The wedge product of a basis is non-zero, contradicting our assumption. Therefore, $v_1, \ldots, v_k$ must be linearly dependent.

# 2.
Check directly that the formula for $\mathscr{L}_V A$ in Lee, Corollary 12.33 is $C^{\infty}$-linear in $X_1, \ldots, X_m$. This is for $f_1, \ldots, f_m \in C^{\infty}(M)$ we have 

$\left(\mathscr{L}_V A\right)\left(f_1 X_1, \ldots, f_m X_m\right)=f_1 \cdots f_m\left(\mathscr{L}_V A\right)\left(X_1, \ldots, X_m\right)$.

Proof

$`\left(\mathscr{L}_V A\right)\left(f_1 X_1, \ldots, f_m X_m\right) = \lim_{t \to 0} \frac{(\Phi_t^* A)(f_1 X_1, \ldots, f_m X_m) - A(f_1 X_1, \ldots, f_m X_m)}{t} = \lim_{t \to 0} \frac{f_1 \cdots f_m (\Phi_t^* A)(X_1, \ldots, X_m) - f_1 \cdots f_m A(X_1, \ldots, X_m)}{t} = f_1 \cdots f_m \lim_{t \to 0} \frac{(\Phi_t^* A)(X_1, \ldots, X_m) - A(X_1, \ldots, X_m)}{t} = f_1 \cdots f_m (\mathscr{L}_V A)(X_1, \ldots, X_m).`$

# 3. (Interior Product)
Define $\iota: \mathscr{X}(M) \times \Omega^k(M) \rightarrow \Omega^{k-1}(M)$ by

$(X, \omega) \mapsto \iota_X \omega=X\mathbin\lrcorner \omega=\omega(X,-, \ldots,-)$
<ol type="a">
<li>

For $X=x \frac{\partial}{\partial y}$ and $\omega=d x \wedge d y$ compute $\iota_X \omega$.
</li>
<li>

Prove that in general $\iota_X(\omega \wedge \eta)=\left(\iota_X \omega\right) \wedge \eta+(-1)^k \omega \wedge \iota_X \eta$.
</li>
</ol>

Proof
<ol type="a">
<li>

$\iota_X \omega = \iota_{x \frac{\partial}{\partial y}}(dx \wedge dy) = x \cdot \iota_{\frac{\partial}{\partial y}}(dx \wedge dy) = x\left(dx\left(\frac{\partial}{\partial y}\right)dy - dy\left(\frac{\partial}{\partial y}\right)dx\right) = x\left(0 \cdot dy - 1 \cdot dx\right) = -x dx$
</li>
<li>

Using the definition of the wedge product

$(f \wedge g)(v_1,\ldots, v_{k + l}) = \sum_{\sigma \in\text{Sh}(k,l)} \text{sgn}(\sigma) 
f(v_{\sigma(1)},\ldots, v_{\sigma(k)})g(v_{\sigma(k+1)}, \ldots, v_{\sigma(k+l)})$ where $\text{Sh}(k,l)=S_{k+l}/(S_k\times S_l)$ denotes shuffles.

Let $v_1, \ldots, v_{k+l-1}$ be arbitrary vector fields.

$(\iota_X(\omega \wedge \eta))(v_1, \ldots, v_{k+l-1}) = (\omega \wedge \eta)(X, v_1, \ldots, v_{k+l-1})$

Partitioning terms where $X$ is an argument of $\omega$ and where $X$ is an argument of $\eta$,

$= \sum_{\sigma \in\text{Sh}(k-1,l)} \text{sgn}(\sigma) \omega(X, v_{\sigma(1)}, \ldots, v_{\sigma(k-1)}) \eta(v_{\sigma(k)}, \ldots, v_{\sigma(k+l-1)}) + (-1)^k \sum_{\sigma \in\text{Sh}(k,l-1)} \text{sgn}(\sigma) \omega(v_{\sigma(1)}, \ldots, v_{\sigma(k)}) \eta(X, v_{\sigma(k+1)}, \ldots, v_{\sigma(k+l-1)})$

$= ((\iota_X \omega) \wedge \eta + (-1)^k \omega \wedge (\iota_X \eta))(v_1, \ldots, v_{k+l-1})$
</li>
</ol>

# 4. (Lee 12-11)
Suppose $M$ is a smooth manifold, $A \in \Omega^k(M)$ and $V, W \in \mathscr{X}(M)$. Show that

$`\mathscr{L}_V \mathscr{L}_W A-\mathscr{L}_W \mathscr{L}_V A=\mathscr{L}_{[V, W]} A`$

Hint: use induction on $k$ starting from the formula in Corollary 12.33 of Lee on 1-forms.

Proof

We proceed by induction on $k$.

Base Case ($k=1$): For a 1-form $A$, we have

$\left(\mathscr{L}_V \mathscr{L}_W A\right)(X) - \left(\mathscr{L}_W \mathscr{L}_V A\right)(X) = V\left((\mathscr{L}_W A)(X)\right) - W\left((\mathscr{L}_V A)(X)\right) - (\mathscr{L}_W A)([V, X]) + (\mathscr{L}_V A)([W, X])$

$$= V(W(A(X)) - A([W,X])) - W(V(A(X)) - A([V,X])) - (W(A([V,X])) - A([W,[V,X]])) + (V(A([W,X])) - A([V,[W,X]])) \\n= (VW-WV)(A(X)) - A([V,[W,X]]) + A([W,[V,X]]) \\n= [V,W](A(X)) - A([V,[W,X]] - [W,[V,X]]) \\n= [V,W](A(X)) - A([[V,W],X])  (\text{by Jacobi identity}) \\n= (\mathscr{L}_{[V,W]} A)(X) $$

Inductive Step: Assume the statement holds for $(k-1)$-forms. Let $A$ be a $k$-form. Then, for vector fields $X_1, \ldots, X_k$, we have

$\left(\mathscr{L}_V \mathscr{L}_W A\right)(X_1, \ldots, X_k) - \left(\mathscr{L}_W \mathscr{L}_V A\right)(X_1, \ldots, X_k)$

$= V\left((\mathscr{L}_W A)(X_1, \ldots, X_k)\right) - W\left((\mathscr{L}_V A)(X_1, \ldots, X_k)\right) - (\mathscr{L}_W A)([V, X_1], X_2, \ldots, X_k) + (\mathscr{L}_V A)([W, X_1], X_2, \ldots, X_k) + \cdots + (\text{similar terms for } X_2, \ldots, X_k)$

By the inductive hypothesis and properties of Lie derivatives, this expression simplifies to $\left(\mathscr{L}_{[V, W]} A\right)(X_1, \ldots, X_k)$. Thus, the statement holds for $k$-forms.

# 5. (Lee 14-6)
Define a 2-form $\omega$ on $\mathbb{R}^3$ by

$\omega=x d y \wedge d z+y d z \wedge d x+z d x \wedge d y$
<ol type="a">
<li>

Compute $\omega$ in spherical coordinates ($\rho, \varphi, \theta$) defined by

$(x, y, z)=(\rho \sin \varphi \cos \theta, \rho \sin \varphi \sin \theta, \rho \cos \varphi)$
</li>
<li>

Compute $d \omega$ in both Cartesian and spherical coordinates and verify that both expressions represent the same 3-form.
</li>
</li>
<li>

Show that $\iota_{S^2}^* \omega$ is nowhere zero.
</li>
</ol>
