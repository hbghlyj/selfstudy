1. Let $M=\mathbb{RP}^1$. Define $f: \mathbb{RP}^1 \to \mathbb{RP}^1$ by
   
   $$f([X,Y])=[X^{1/3}, Y^{1/3}]$$
   
   Show that $f: M \to M$ is a homeomorphism but not a diffeomorphism.

   Proof
   
   $M$ has an atlas consisting of two charts $(U_1,\phi_1),(U_2,\phi_2)$, where $`U_1=\{[X,Y]\in \mathbb{RP}^1|X\neq 0\},\phi_1([X,Y])=Y/X`$ and $`U_2=\{[X,Y]\in \mathbb{RP}^1|Y\neq 0\},\phi_2([X,Y])=X/Y`$. The transition map is given by $`\phi_2\circ \phi_1^{-1}(x)=1/x`$ for $x\in \mathbb{R}\setminus \{0\}$.
   
   $\phi_1\circ f \circ \phi_1^{-1}(x)=x^{1/3}$ for $x\in \mathbb{R}$, which is continuous and bijective with continuous inverse $`x\mapsto x^3`$. Similarly, $\phi_2 \circ f \circ \phi_2^{-1}(x)=x^{1/3}$ for $x\in \mathbb{R}$. Thus $f$ is a homeomorphism.
   
   However, $`(\phi_1\circ f \circ \phi_1^{-1})'(x)=\frac{1}{3}x^{-2/3}`$, which is not continuous at $0$. Thus $f$ is not a diffeomorphism.

3. (Lee 2.7) Let $M$ be a nonempty smooth $n$-manifold with $n \geq 1$. Show that the vector space $C^{\infty}(M)$ is infinite-dimensional.

   Proof

   Take a chart $(U,\phi)$ of $M$, $U$ is nonempty, $\phi(U)$ contains a nonempty ball $B$.

   Let the cutoff function $`\psi:M\to \mathbb{R}`$ be such that $\psi=1$ on $\phi^{-1}(B)$ and $\psi=0$ outside $\phi^{-1}(B)$.

   For each nonnegative integer $k$, define $`f_k:M\to \mathbb{R},x\mapsto \psi(x)\phi(x)^{2k}`$.

   Then each $f_k$ is smooth and the set $`\{f_k|k=0,1,2,\ldots\}`$ is linearly independent: suppose $`a_0f_0+a_1f_1+\cdots +a_mf_m\equiv0`$ for some $m\geq 0$ and $a_i\in \mathbb{R}$.

   Then for any $x\in \phi^{-1}(B)$, we have $`a_0+a_1\phi(x)^2+\cdots +a_m\phi(x)^{2m}=0`$.

   Thus the polynomial $`a_0+a_1x^2+\cdots +a_mx^{2m}`$ has infinitely many roots in $B$, which implies that $`a_0=a_1=\cdots =a_m=0`$. Therefore, $C^{\infty}(M)$ is infinite-dimensional.

5. (Lee 2.9) Let $p(z)$ be a degree $d$ polynomial in one complex variable. Show that the map $p: \mathbb{C} \rightarrow \mathbb{C}$ extends to a smooth map from $\mathbb{C P}^1 \rightarrow \mathbb{C P}^1$, where we take $\mathbb{C} \subset \mathbb{CP}^1$ to be a standard coordinate chart.

6. (Lee 2.10) Let $M$ and $N$ be smooth manifolds. Given a continuous map $F: M \to N$, consider the map

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
