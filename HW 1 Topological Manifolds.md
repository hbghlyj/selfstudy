<ol>
<li>Prove that the Möbius strip

$$M=[0,1] \times\left(-\frac{1}{2}, \frac{1}{2}\right) /(0, y) \sim(1,-y)$$

is a topological manifold.

Proof.
<dl>
<dt>

Locally homeomorphic to $\mathbb{R}^2$
</dt>
<dd>

$M$ is the union of the open sets $`U_1=M\setminus\{[(0,y)]\in M\}`$ and $`U_2 =M\setminus\{[(\frac12,y)]\in M\}`$.

$V_1=V_2=(0,1)\times\left(-\frac{1}{2}, \frac{1}{2}\right)$ are open sets in $\mathbb{R}^2$.

The maps $\phi_i:U_i\to V_i$ are homeomorphisms

$`\begin{array}{ll}\phi_1([(x,y)])=(x,y)&\phi_1^{-1}(x,y)=[(x,y)]\\\phi_2([(x,y)])=\begin{cases}(x+\frac12,y)&x<\frac12\\(x-\frac12,-y)&x>\frac12\end{cases}&\phi_2^{-1}(x,y)=\begin{cases}{}[(x-\frac12,y)]&x\ge\frac12\\{}[(x+\frac12,-y)]&x\le\frac12\end{cases}\end{array}`$
</dd>
<dt>Second-countable</dt>
<dd>

$M$ has a finite atlas $`\{(U_i,\phi_i):i=1,2\}`$. Pull back a countable base from each chart $U_i$ and take the finite union—this gives a countable base for $M$.
In general, [Manifold is 2nd countable iff it has a countable atlas](https://math.stackexchange.com/q/653183).
</dd>
<dt>Hausdorff</dt>
<dd>

Let $[(x_1,y_1)],[(x_2,y_2)]$ be two distinct points in $M$. Pick $x_3\in(0,1)$ different from $x_1,x_2$.

Let $`U=M\setminus\{[(x_3,y)]\in M\}`$ and $\phi:U\to(0,1)\times\left(-\frac{1}{2}, \frac{1}{2}\right)$ be a homeomorphism. Then the chart $U$ contains both points.

Let $U_i$ be disjoint Euclidean neighborhoods of $\phi([(x_i,y_i)])$, then $\phi^{-1}(U_1),\phi^{-1}(U_2)$ are disjoint open neighborhoods of $[(x_1,y_1)],[(x_2,y_2)]$ in $M$, respectively.
</dd>
</dl>
<li>

Prove that $\mathbb{RP}^2$ is Hausdorff, second-countable, and compact.

Proof.
<dl>
<dt>Compact</dt>
<dd>

$\mathbb{S}^2$ is compact, and the quotient map $p: \mathbb{S}^2 \to \mathbb{RP}^2$ is continuous and surjective. From Continuous Image of Compact Space is Compact, $\mathbb{RP}^2$ is compact.
</dd>
<dt>Second-countable</dt><dd>

Since $\mathbb{S}^2$ is second-countable and the quotient map $p: \mathbb{S}^2 \to \mathbb{RP}^2$ is local homeomorphism (in particular, $p$ is open), the image of a countable basis in $\mathbb{S}^2$ under $p$ is a countable basis in $\mathbb{RP}^2$, so $\mathbb{RP}^2$ is second-countable. In general, [Compact metric spaces is second countable](https://math.stackexchange.com/questions/573787).
</dt>
<dt>Hausdorff</dt><dd>

Let $[x],[y] \in \mathbb{RP}^2$ be two distinct points. Then $x \neq \pm y$. By Hausdorffness of $\mathbb{S}^2$ we can find disjoint open neighborhoods $U$ of $\{x,-x\}$ and $V$ of $`\{y,-y\}`$ in $\mathbb{S}^2$. Then $p(U),p(V)$ are disjoint open neighborhoods of $[x]$ and $[y]$ in $\mathbb{RP}^2$, respectively.
</dd>
</dl>

<li>

Prove that $\mathbb{RP}^2$ is homeomorphic to the closed 2-disk with opposite boundary points identified:

$$\mathbb{RP}^2 \cong \overline{\mathbb{D}}^2 /(\cos \theta, \sin \theta) \sim(\cos (\theta+\pi), \sin (\theta+\pi)) .$$

Proof.
$$\mathbb{RP}^2$$ is defined as the quotient of $S^2$ under the equivalence relation $(x,y,z)\sim(-x,-y,-z)$.

Define a map $f:\mathbb{RP}^2 \to \overline{\mathbb{D}}^2/\sim$ by

$`f([(x,y,z)]) = \begin{cases}{}[(x,y)]&z\ge 0\\{}[(-x,-y)]&z<0\end{cases}`$

To show that $f$ is well-defined,

$`f([(-x,-y,-z)]) = f([(x,y,z)])`$

To show that $f$ is continuous, note that the preimage of an open ball in $\overline{\mathbb{D}}^2/\sim$ is open in $\mathbb{RP}^2$.

To show that $f$ is a homeomorphism, we need to show that its inverse is continuous.

Define $g:\overline{\mathbb{D}}^2/\sim\to\mathbb{RP}^2$

$$g([(x,y)]) = [(x,y,\sqrt{1-x^2-y^2})]$$

where on the boundary $x^2+y^2=1$ we get $g([(x,y)])=g([(-x,-y)])$, so $g$ is well-defined.

We can verify that $fg=\text{id},gf=\text{id}$ and $g$ is continuous.
