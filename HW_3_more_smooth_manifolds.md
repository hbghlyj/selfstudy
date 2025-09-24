1. Let $M=\mathbb{RP}^1$. Define $f: \mathbb{RP}^1 \to \mathbb{RP}^1$ by
   
   $$f([X,Y])=[X^{1/3}, Y^{1/3}]$$
   
   Show that $f: M \to M$ is a homeomorphism but not a diffeomorphism.

   Proof
   
   $M$ has an atlas consisting of two charts $(U_1,\phi_1),(U_2,\phi_2)$, where $`U_1=\{[X,Y]\in \mathbb{RP}^1|X\neq 0\},\phi_1([X,Y])=Y/X`$ and $`U_2=\{[X,Y]\in \mathbb{RP}^1|Y\neq 0\},\phi_2([X,Y])=X/Y`$. The transition map is given by $`\phi_2\circ \phi_1^{-1}(x)=1/x`$ for $`x\in \mathbb{R}\setminus \{0\}`$.
   
   $\phi_1\circ f \circ \phi_1^{-1}(x)=x^{1/3}$ for $x\in \mathbb{R}$, which is continuous and bijective with continuous inverse $`x\mapsto x^3`$. Similarly, $\phi_2 \circ f \circ \phi_2^{-1}(x)=x^{1/3}$ for $x\in \mathbb{R}$. Thus $f$ is a homeomorphism.
   
   However, $`\phi_1\circ f \circ \phi_1^{-1}(x)=x^{1/3}`$ is not differentiable at $0$. Thus $f$ is not differentiable at $[0,1]$. Thus $f$ is not a diffeomorphism.

3. (Lee 2.7) Let $M$ be a nonempty smooth $n$-manifold with $n \geq 1$. Show that the vector space $C^{\infty}(M)$ is infinite-dimensional.

   Proof

   Take a chart $(U,\phi)$ of $M$, $U$ is nonempty, $\phi(U)$ contains a nonempty ball $B$. Let $\psi$ be a smooth bump function for $B$ supported in $\phi(U)$.

   Let $f_k:M\to \mathbb{R},x\mapsto\phi(x)^k\psi(\phi(x))$.

   To show $`\{f_k\mid k=0,1,\dots\}`$ are linearly independent, suppose there exist nonzero $\lambda_1, \dots, \lambda_k \in \mathbb{R}$ such that

   $`\lambda_1 f_{i_1}+\dots+\lambda_k f_{i_k}=0`$

   where $i_1, \ldots, i_k$ are distinct. Since $\psi|_B=1$,

   $`(\lambda_1 x^{i_1}+\dots+\lambda_k x^{i_k})|_B=0`$

   But a nonzero polynomial can have only finitely many zeros. So $\lambda_1=\dots=\lambda_k=0$.

   Therefore, $`\{f_k\mid k=0,1,\dots\}`$ are linearly independent, $C^{\infty}(M)$ is an infinite-dimensional $\mathbb{R}$-vector space.

5. (Lee 2.9) Let $p(z)$ be a degree $d$ polynomial in one complex variable. Show that the map $p\colon\mathbb{C} \to \mathbb{C}$ extends to a smooth map from $\mathbb{CP}^1 \to \mathbb{CP}^1$, where we take $\mathbb{C} \subset \mathbb{CP}^1$ to be a standard coordinate chart.

   Proof
   
   $\mathbb{CP}^1$ has a smooth atlas $`\{(U_1,\phi_1),(U_2,\phi_2)\}'$ where $U_1=\{[z:1]:z \in \mathbb{C}\}$, $U_2=\{[1:w]:w \in \mathbb{C}\}$, $\phi_1([z:1])=z$ and $\phi_2([1:w])=w$.

   Let $q(z)=z^d p(1/z)$. Then $q(z)$ is a polynomial of degree at most $d$. Define $\tilde{p}:\mathbb{CP}^1 \to \mathbb{CP}^1$ by
   
   $\tilde{p}([z:1])=[p(z):1]$ on $U_1$ and $\tilde{p}([1:w])=[q(w):w^d]$ on $U_2$.

   We need to show the two definitions agree on the overlap $`U_1 \cap U_2=\{[z:1]:z \neq 0\}=\{[1:w]:w \neq 0\}`$. If $[z:1]=[1:w]$, then $w=1/z$. Thus
   
   $[q(w):w^d]=[(1/z)^d p(z):(1/z)^d]=[p(z):1]$
   
   So $\tilde{p}$ is well-defined.
   
   To show $\tilde{p}$ is smooth, we need to show that the coordinate representations $\phi_1 \circ \tilde{p} \circ \phi_1^{-1}$, $\phi_2 \circ \tilde{p} \circ \phi_2^{-1}$ are smooth.
   
   $\phi_1 \circ \tilde{p} \circ \phi_1^{-1}(z)=\phi_1(\tilde{p}([z:1]))=\phi_1([p(z):1])=p(z)$, which is smooth.
   
   $\phi_2 \circ \tilde{p} \circ \phi_2^{-1}(w)=\phi_2(\tilde{p}([1:w]))=\phi_2([q(w):w^d])=w^d/q(w)$, which is smooth since $\deg q(w)\leq d$.

   Thus $\tilde{p}$ is a smooth extension of $p$ to $\mathbb{CP}^1$.

7. (Lee 2.10) Let $M$ and $N$ be smooth manifolds. Given a continuous map $F: M \to N$, consider the map

    $`\begin{aligned}F^*\colon C^0(N) &\to C^0(M) \\f & \mapsto f \circ F\end{aligned}`$
      
      <ol type="a">
      <li>
      Show that $F^*$ is a linear map
      </li>
      <li>
      Show that $F$ is smooth if and only if $F^*(C^\infty(N)) \subset C^\infty(M)$.
      </li>
      <li>
      Suppose that $F$ is a homeomorphism. Prove that $F$ is a diffeomorphism if and only if $F^*$ induces an isomorphism from $C^{\infty}(N)$ to $C^{\infty}(M)$.
      </li>
      </ol>
      
      Proof
      
      <ol type="a">
      <li>
      Show that $F^*$ is a linear map
      </li>
      <li>
      Show that $F$ is smooth if and only if $F^*(C^\infty(N)) \subset C^\infty(M)$.
      </li>
      <li>
      Suppose that $F$ is a homeomorphism. Prove that $F$ is a diffeomorphism if and only if $F^*$ induces an isomorphism from $C^{\infty}(N)$ to $C^{\infty}(M)$.
      </li>
      </ol>
5. (Lee 2-14) Suppose that $A$ and $B$ are disjoint closed subsets of a smooth manifold $M$. Show that there exists $f \in C^{\infty}(M)$ such that $0 \leq f(x) \leq 1$ for all $x \in M$, $f^{-1}(0)=A$, and $f^{-1}(1)=B$.
   
   Proof
   
   By Theorem 2.29 (Level Sets of Smooth Functions) for any closed set $C$ in a smooth manifold $M$, there exists a non-negative smooth function $g: M\to R$ such that $g^{-1}(0) = C$.

   Using this, let $g_A$ and $g_B$ be such smooth functions for the closed sets $A$ and $B$.

   Define $f(x) = g_A(x) / (g_A(x) + g_B(x))$. This function is well-defined (denominator is never zero since $A$ and $B$ are disjoint) and smooth.

   $x\in f^{-1}(0)\iff g_A(x)=0\iff x\in A$

   $x\in f^{-1}(1)\iff g_B(x)=0\iff x\in B$

7. Construct a diffeomorphism between $`\mathrm{Gr}_k(\mathbb{R}^n)`$ and $`\mathrm{Gr}_{n-k}(\mathbb{R}^n)`$. (Hint: use an inner product on $\mathbb{R}^n$.)
   
   Proof
      
   Define $`F:\mathrm{Gr}_k(\mathbb{R}^n)\to \mathrm{Gr}_{n-k}(\mathbb{R}^n)`$ by $F(V)=V^\perp$ (orthogonal complement w.r.t. the Euclidean inner product). Then $F$ is a bijection with inverse $F^{-1}(W)=W^\perp$. It remains to prove $F$ and $F^{-1}$ are smooth.

   Fix a decomposition $\mathbb{R}^n=E\oplus F$ with $\dim E=k$, $\dim F=n-k$, and $E\perp F$. Let
   
   $`\mathcal{U}_{E,F}=\{W\in \mathrm{Gr}_k(\mathbb{R}^n)\mid W \text{ is transverse to } F\}.`$
   
   Each $W\in \mathcal{U}_{E,F}$ can be written uniquely as a graph $`W = \{ x + A x : x\in E\}`$ for a linear map $A:E\to F$.

   Define the chart

   $\chi_{E,F}:\mathcal{U}_{E,F}\to \mathrm{Hom}(E,F),\quad W\mapsto A.$

   These charts form a smooth atlas of $\mathrm{Gr}_k(\mathbb{R}^n)$.

   Similarly, for $\mathrm{Gr}_{n-k}(\mathbb{R}^n)$ use the (swapped) orthogonal decomposition $\mathbb{R}^n=F\oplus E$ to get charts
   
   $`\chi'_{F,E}:\mathcal{U}'_{F,E}\to \mathrm{Hom}(F,E)`$
   
   where a subspace $Z$ transverse to $E$ is written as $`\{ y + B y : y\in F\}`$ with $B:F\to E$.

   Take the chart $\chi_{E,F}$ around $E$ (so $E$ corresponds to $A=0$). Let $W=\mathrm{graph}(A)$ with $A:E\to F$. Its orthogonal complement is

   $W^\perp = \{ -A^T y + y : y\in F\}$
   
   (where $A^T:F\to E$ is the transpose w.r.t. the inner product).

   $\langle x+Ax,-A^Ty+y\rangle=-\langle x,A^Ty\rangle+\langle x,y\rangle-\langle Ax,A^Ty\rangle+\langle Ax,y\rangle=0$

   since $-\langle x,A^Ty\rangle+\langle Ax,y\rangle=0$ by definition of adjoint, and $\langle x,y\rangle=\langle Ax,A^Ty\rangle=0$ since they live in orthogonal subspaces.
   
   Regard $W^\perp$ inside the decomposition $F\oplus E$; thus in the chart $\chi'_{F,E}$ it is the graph of $-A^T$. Therefore on these overlapping charts the coordinate representation of $F$ is
   
   $\mathrm{Hom}(E,F)\to \mathrm{Hom}(F,E),\quad A\mapsto -A^T,$

   a linear (hence smooth) map with linear (hence smooth) inverse $B\mapsto -B^T$.
