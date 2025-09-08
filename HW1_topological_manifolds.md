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

$M$ is the union of the open sets $`U_1 =\{[(x,y)]\in M:x\ne0,1\}`$ and $`U_2 =\{[(x,y)]\in M:x\ne\frac12\}`$.

$V_1=(0,1)\times\left(-\frac{1}{2}, \frac{1}{2}\right)$ and $V_2=(0,1)\times\left(-\frac{1}{2}, \frac{1}{2}\right)$ are open set in $\mathbb{R}^2$.

The maps $\phi_i:U_i\to V_i$ are homeomorphisms

$`\begin{array}{ll}\phi_1([(x,y)])=(x,y)&\phi_1^{-1}(x,y)=[(x,y)]\\\phi_2([(x,y)])=\begin{cases}(x+\frac12,y)&x<\frac12\\(x-\frac12,-y)&x>\frac12\end{cases}&\phi_2^{-1}(x,y)=\begin{cases}{}[(x-\frac12,y)]&x\ge\frac12\\{}[(x+\frac12,-y)]&x\le\frac12\end{cases}\end{array}`$
</dd>
<dt>Second-countable</dt>
<dd>

By [Compact metric spaces is second countable](https://math.stackexchange.com/questions/573787), $M$ is second countable.
</dd>
<dt>Hausdorff</dt>
<dd>

Let $[(x_1,y_1)],[(x_2,y_2)]$ be two distinct points in $M$.

* If $y_1\ne y_2$, then $`\{[(x,y)]\in M:y<\frac{y_1+y_2}2\}`$ and $`\{[(x,y)]\in M:y>\frac{y_1+y_2}2\}`$ are disjoint open neighborhoods of the two points.
* If $y_1=y_2$, the two points lie on the circle $`\{[(x,y)]\in M:y=y_1\}`$. Since the circle is Hausdorff, there exist disjoint open neighborhoods $W_i$ of the two points in $`\{[(x,y)]\in M:y=y_1\}`$. Set $`U_i=\{[(x,y)]:x\in W_i\}`$. Then $U_i$ are disjoint open neighborhoods of the two points in $M$.
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

Since $\mathbb{S}^2$ is second-countable and the quotient map $p: \mathbb{S}^2 \to \mathbb{RP}^2$ is local homeomorphism, the image of a countable basis in $\mathbb{S}^2$ under $p$ is a countable basis in $\mathbb{RP}^2$, so $\mathbb{RP}^2$ is second-countable.
</dt>
<dt>Hausdorff</dt><dd>

Let $[x],[y] \in \mathbb{RP}^2$ be two distinct points. Then $x \neq \pm y$. By Hausdorffness of $\mathbb{S}^2$ we can find open neighborhoods $U$ of $x$ and $V$ of $y$ in $\mathbb{S}^2$ such that $U \cap(V\cup(-V)) = \emptyset$. Then $p(U),p(V)$ are open neighborhoods of $[x]$ and $[y]$ in $\mathbb{RP}^2$, respectively, and they are disjoint.
</dd>
</dl>

<li>

Prove that $\mathbb{RP}^2$ is homeomorphic to the closed 2-disk with opposite boundary points identified:

$$\mathbb{RP}^2 \cong \overline{\mathbb{D}^2} /(\cos \theta, \sin \theta) \sim(\cos (\theta+\pi), \sin (\theta+\pi)) .$$

Proof.
$$\mathbb{RP}^2$$ is defined as the quotient of $S^2$ under the equivalence relation $(x,y,z)\sim(-x,-y,-z)$.

Define a map $f:\mathbb{RP}^2 \to \overline{\mathbb{D}^2}/\sim$ by

$`f([(x,y,z)]) = \begin{cases}{}[(x,y)]&z\ge 0\\{}[(-x,-y)]&z<0\end{cases}`$

To show that $f$ is well-defined,

$`f([(-x,-y,-z)]) = f([(x,y,z)])`$

To show that $f$ is continuous, note that the preimage of an open ball in $\overline{\mathbb{D}^2}/\sim$ is open in $\mathbb{RP}^2$.

To show that $f$ is a homeomorphism, we need to show that its inverse is continuous.

Define $g:\overline{\mathbb{D}^2}/\sim\to\mathbb{RP}^2$

$$g([(x,y)]) = [(x,y,\sqrt{1-x^2-y^2})]$$

where on the boundary $x^2+y^2=1$ we get $g([(x,y)])=f^{-1}([(-x,-y)])$, so $g$ is well-defined.

We can verify that $fg=\text{id},gf=\text{id}$ and $g$ is continuous.
