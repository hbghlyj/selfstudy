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

$M$ is the union of the open sets $`U_1 =\{(x,y)\in M:x\ne0\}`$ and $`U_2 =\{(x,y)\in M:x\ne\frac12\}`$. The restriction of the quotient map to $U_i$ is a homeomorphism onto an open subset $V_i$ of $\mathbb{R}^2$.
</dd>
<dt>Second-countable</dt>
<dd>

Since $[0,1] \times \left(-\frac{1}{2}, \frac{1}{2}\right)$ is second-countable and the quotient map is open, it follows that $M$ is second-countable.
</dd>
<dt>Hausdorff</dt>
<dd>

Let $[(x_1,y_1)],[(x_2,y_2)]$ be two distinct points in $M$.

* If $y_1\ne y_2$, then $`\{(x,y)\in M:y<\frac{y_1+y_2}2\}`$ and $`\{(x,y)\in M:y>\frac{y_1+y_2}2\}`$ are disjoint open neighborhoods of the two points.
* If $y_1=y_2$, the two points lie on the circle $`\{(x,y)\in M:y=y_1\}`$. Since the circle is Hausdorff, there exist disjoint open neighborhoods $W_i$ of the two points in $`\{(x,y)\in M:y=y_1\}`$. Set $U_i=W_i\times\left(-\frac{1}{2}, \frac{1}{2}\right)$. Then $U_i$ are disjoint open neighborhoods of the two points in $M$.
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

Let $`\{U_n\}_{n \in \mathbb{N}}`$ be a countable basis for $\mathbb{S}^2$. Then the sets $p(U_n)$ form a countable basis for the topology on $\mathbb{RP}^2$, since the quotient map $p$ is open.
</dt>
<dt>Hausdorff</dt><dd>

Let $[x],[y] \in \mathbb{RP}^2$ be two distinct points. Then $x \neq \pm y$. Without loss of generality, assume $x \neq 0$. We can find open neighborhoods $U$ of $x$ and $V$ of $y$ in $\mathbb{S}^2$ such that $U \cap V = \emptyset$ and $U \cap -V = \emptyset$. The images of these neighborhoods under the quotient map $p$ are open neighborhoods of $[x]$ and $[y]$ in $\mathbb{RP}^2$, respectively, and they are disjoint.
</dd>
</dl>

<li>

Prove that $\mathbb{RP}^2$ is homeomorphic to the closed 2-disk with opposite boundary points identified:

$$\mathbb{RP}^2 \cong \overline{\mathbb{D}^2} /(\cos \theta, \sin \theta) \sim(\cos (\theta+\pi), \sin (\theta+\pi)) .$$

Proof.
Define a map $f:\mathbb{RP}^2 \to \overline{\mathbb{D}^2}/\sim$ by

$`f([(x,y,z)]) = \begin{cases}{}[(x,y)]&z\ge 0\\{}[(-x,-y)]&z<0\end{cases}`$

To show that $f$ is well-defined,

$$f(-x,-y,-z) = f(x,y,z)$$

To show that $f$ is continuous, we note that $f$ is continuous and the identification is done in a way that respects the topology of $\overline{\mathbb{D}^2}$.

To show that $f$ is a homeomorphism, we need to show that it is bijective and that its inverse is continuous. $f^{-1}$ can be constructed by lifting points from $\overline{\mathbb{D}^2}/\sim$ back to $\mathbb{RP}^2$

$$f^{-1}([(x,y)]) = [(x,y,\sqrt{1-x^2-y^2})]$$

This map is well-defined and continuous, as it respects the identification in $\overline{\mathbb{D}^2}/\sim$.
