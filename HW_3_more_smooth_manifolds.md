1. Let $M=\mathbb{RP}^1$. Define $f: \mathbb{RP}^1 \to \mathbb{RP}^1$ by
   
   $$f([X,Y])=[X^{1/3}, Y^{1/3}]$$
   
   Show that $f: M \to M$ is a homeomorphism but not a diffeomorphism.

   Proof
   
   $M$ has an atlas consisting of two charts $(U_1,\phi_1),(U_2,\phi_2)$, where $`U_1=\{[X,Y]\in \mathbb{RP}^1|X\neq 0\},\phi_1([X,Y])=Y/X`$ and $`U_2=\{[X,Y]\in \mathbb{RP}^1|Y\neq 0\},\phi_2([X,Y])=X/Y`$. The transition map is given by $`\phi_2\circ \phi_1^{-1}(x)=1/x`$ for $x\in \mathbb{R}\setminus \{0\}$.
   
   $\phi_1\circ f \circ \phi_1^{-1}(x)=x^{1/3}$ for $x\in \mathbb{R}$, which is continuous and bijective with continuous inverse $`x\mapsto x^3`$. Similarly, $\phi_2 \circ f \circ \phi_2^{-1}(x)=x^{1/3}$ for $x\in \mathbb{R}$. Thus $f$ is a homeomorphism.
   However, $`(\phi_1\circ f \circ \phi_1^{-1})'(x)=\frac{1}{3}x^{-2/3}`$, which is not continuous at $0$. Thus $f$ is not a diffeomorphism.

2. (Lee 2.7) Let $M$ be a nonempty smooth $n$-manifold with $n \geq 1$. Show that the vector space $C^{\infty}(M)$ is infinite-dimensional.

3. (Lee 2.9) Let $p(z)$ be a degree $d$ polynomial in one complex variable. Show that the map $p: \mathbb{C} \rightarrow \mathbb{C}$ extends to a smooth map from $\mathbb{C P}^1 \rightarrow \mathbb{C P}^1$, where we take $\mathbb{C} \subset \mathbb{C P}^1$ to be a standard coordinate chart.

4. (Lee 2.10) Let $M$ and $N$ be smooth manifolds. Given a continuous map $F: M \to N$, consider the map
    $`\begin{aligned}F^* & : C^0(N) \to C^0(M) \\f & \mapsto f \circ F\end{aligned}`$

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
   
   Take a smooth partition of unity $`\{\psi,\phi\}`$ subordinate to the open cover $`\{M\setminus A,M\setminus B\}`$ of $M$. Define $`f:M\to [0,1],x\mapsto1-\mathbb{1}_A(x)\phi(x)`$. Then $f$ is smooth, $0\leq f(x)\leq \phi(x)\leq 1$ for all $x\in M$. Moreover, $`f^{-1}(0)=\{x\in M:\phi(x)=1\}\cup A=M\setminus \text{supp}(\phi)\cup A=A`$, and $`f^{-1}(1)=\{x\in M:\phi(x)=1\}=M\setminus \text{supp}(\psi)=B`$.

6. Construct a diffeomorphism between $`\mathrm{Gr}_k(\mathbb{R}^n)`$ and $`\mathrm{Gr}_{n-k}(\mathbb{R}^n)`$. (Hint: use an inner product on $\mathbb{R}^n$.)
   
   Proof
   
   Define the map $`f:\mathrm{Gr}_k(\mathbb{R}^n)\to \mathrm{Gr}_{n-k}(\mathbb{R}^n),V\mapsto V^{\perp}`$, where $V^{\perp}$ is the orthogonal complement of $V$ with respect to the standard inner product on $\mathbb{R}^n$. Since $V$ is a $k$-dimensional subspace of $\mathbb{R}^n$, its orthogonal complement $V^{\perp}$ is an $(n-k)$-dimensional subspace of $\mathbb{R}^n$. The inverse map of $f$ is given by $`f^{-1}:\mathrm{Gr}_{n-k}(\mathbb{R}^n)\to \mathrm{Gr}_k(\mathbb{R}^n),W\mapsto W^{\perp}`$. Thus $f$ is a bijection.
