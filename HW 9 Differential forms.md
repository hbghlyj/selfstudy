# 1. (Lee 14-1, 4)

(a) Let $V$ be a finite-dimensional vector space and $v_1, \ldots, v_k \in V$. Prove that $v_1, \ldots, v_k$ are linearly dependent if and only if $v_1 \wedge \cdots \wedge v_k=0$.

# 2.
Check directly that the formula for $\mathscr{L}_V A$ in Lee, Corollary 12.33 is $C^{\infty}$-linear in $X_1, \ldots, X_m$. This is for $f_1, \ldots, f_m \in C^{\infty}(M)$ we have 

$\left(\mathscr{L}_V A\right)\left(f_1 X_1, \ldots, f_m X_m\right)=f_1 \cdots f_m\left(\mathscr{L}_V A\right)\left(X_1, \ldots, X_m\right)$.

# 3. (Interior Product)
Define $\iota: \mathscr{X}(M) \times \Omega^k(M) \rightarrow \Omega^{k-1}(M)$ by

$(X, \omega) \mapsto \iota_X \omega=X\lrcorner \omega=\omega(X,-, \ldots,-)$

a) For $X=x \frac{\partial}{\partial y}$ and $\omega=d x \wedge d y$ compute $\iota_X \omega$.

b) Prove that in general $\iota_X(\omega \wedge \eta)=\left(\iota_X \omega\right) \wedge \eta+(-1)^k \omega \wedge \iota_X \eta$.

# 4. (Lee 12-11)
Suppose $M$ is a smooth manifold, $A \in \Omega^k(M)$ and $V, W \in \mathscr{X}(M)$. Show that

$`\mathscr{L}_V \mathscr{L}_W A-\mathscr{L}_W \mathscr{L}_V A=\mathscr{L}_{[V, W]} A`$

Hint: use induction on $k$ starting from the formula in Corollary 12.33 of Lee on 1-forms.
# 5. (Lee 14-6)
Define a 2-form $\omega$ on $\mathbb{R}^3$ by

$\omega=x d y \wedge d z+y d z \wedge d x+z d x \wedge d y$

(a) Compute $\omega$ in spherical coordinates ( $\rho, \varphi, \theta$ ) defined by

$(x, y, z)=(\rho \sin \varphi \cos \theta, \rho \sin \varphi \sin \theta, \rho \cos \varphi)$

(b) Compute $d \omega$ in both Cartesian and spherical coordinates and verify that both expressions represent the same 3-form.

(c) Show that $\iota_{S^2}^* \omega$ is nowhere zero.
