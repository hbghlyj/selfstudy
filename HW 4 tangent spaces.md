# 1
Show that the map $`\mathbb{R}_p^n \to T_p \mathbb{R}^n`$ given by $\vec{v} \mapsto D_{\vec{v}}\bigr|_p$ is surjective. i.e that every derivation comes from a directional derivative. (Hint: To find $\vec{v}$ apply $w \in T_p \mathbb{R}^n$ to the coordinate functions. Then for any smooth function $f$ use Taylor's theorem on $f$ and the Leibniz property.)

Proof

Let $w \in T_p \mathbb{R}^n$ be an arbitrary derivation at the point $p$. We want to show that there exists a vector $\vec{v} \in \mathbb{R}^n$ such that $`w = D_{\vec{v}}|_p`$, where $`D_{\vec{v}}|_p`$ is the directional derivative at $p$ in the direction of $\vec{v}$.

To find such a vector $\vec{v}$, we can apply the derivation $w$ to the coordinate functions $x^i: \mathbb{R}^n \to \mathbb{R}$, where $x^i(p) = p^i$. By the definition of a derivation, we have:

$`w(x^i) = D_{\vec{v}}|_p(x^i) = \frac{d}{d t}\bigr|_{t=0} x^i(p + t\vec{v}) = \frac{d}{d t}\bigr|_{t=0} (p^i + t v^i) = v^i.`$

Thus, we can define the vector $\vec{v} = (w(x^1), w(x^2), \ldots, w(x^n)) \in \mathbb{R}^n$. We claim that $`w = D_{\vec{v}}|_p`$.

To verify this, we need to show that for any smooth function $f: \mathbb{R}^n \to \mathbb{R}$, we have:

$`w(f) = D_{\vec{v}}|_p(f).`$

By definition, the directional derivative is $`D_{\vec{v}}|_p(f) = \left.\frac{d}{dt}\right|_{t=0} f(p+t\vec{v})`$. Applying the chain rule, this becomes:

$`D_{\vec{v}}|_p(f) = \sum_{i=1}^n \frac{\partial f}{\partial x^i}(p) \frac{d(p^i+tv^i)}{dt}\bigr|_{t=0} = \sum_{i=1}^n v^i \frac{\partial f}{\partial x^i}(p).`$

On the other hand, by Taylor's theorem, we can write:

$`f(p + t\vec{v}) = f(p) + t \sum_{i=1}^n v^i \frac{\partial f}{\partial x^i}(p) + O(t^2).`$

Since $w$ is a derivation, we have:

$`w(f) = \sum_{i=1}^n w(x^i) \frac{\partial f}{\partial x^i}(p) = \sum_{i=1}^n v^i \frac{\partial f}{\partial x^i}(p) = D_{\vec{v}}|_p(f).`$

This shows that $`w = D_{\vec{v}}|_p`$, and thus the map $`\vec{v} \mapsto D_{\vec{v}}|_p`$ is surjective.

# 2
Prove Proposition 3.6 from Lee (Properties of Differentials). Let $M, N$, and $P$ be smooth manifolds, let $F: M \to N$ and $G: N \to P$ be smooth maps, and let $p \in M$.
<ol type="a">
<li>
  $d F_p: T_p M \to T_{F(p)} N$ is linear.
</li>
<li>
  $d(G \circ F)_p=d G_{F(p)} \circ d F_p: T_p M \to T_{G(F(p))} P$.
</li>
<li>
  $d\left(\text{Id}_M\right)_p=\text{Id}_{T_p M}: T_p M \to T_p M$.
</li>
<li>
  If $F$ is a diffeomorphism, then $d F_p: T_p M \to T_{F(p)} N$ is an isomorphism, and
  
  $(d F_p)^{-1}=d(F^{-1})_{F(p)}$
</li>
</ol>

# 3
Note that if $M$ is a smooth manifold and $U$ is an open subset then $U$ is also a smooth manifold with smooth structure from $M$ (i.e. charts on U are given by intersecting $U$ with charts on $M$). We say $U$ is an open submanifold of $M$. Show that for $p \in U$ there is an isomorphism $T_p M$ to $T_p U$.

Proof

Let $i: U \to M$ be the inclusion map. Since $i$ is a smooth embedding, the differential $di_p: T_p U \to T_p M$ is injective. To show that $di_p$ is also surjective, let $v \in T_p M$. We need to show that there exists a vector $u \in T_p U$ such that $di_p(u) = v$.

Since $U$ is an open subset of $M$, there exists a chart $(V, \phi)$ of $M$ such that $p \in V$ and $V \cap U$ is non-empty. The restriction of $\phi$ to $V \cap U$ gives a chart $(V \cap U, \phi|_{V \cap U})$ for $U$.

Now, consider the vector $v \in T_p M$. By the definition of the tangent space, there exists a curve $\gamma: (-\epsilon, \epsilon) \to M$ such that $\gamma(0) = p$ and $\gamma'(0) = v$. Since $U$ is open in $M$, we can choose $\epsilon$ small enough so that $\gamma(t) \in U$ for all $t$ in some interval around 0. Thus, we can define a curve $\tilde{\gamma}: (-\epsilon, \epsilon) \to U$ by restricting $\gamma$ to this interval.

The tangent vector $u = \tilde{\gamma}'(0)$ is then an element of $T_p U$. By construction, we have $di_p(u) = v$. Therefore, $di_p$ is surjective.

Since $di_p$ is both injective and surjective, it is an isomorphism. Hence, we have shown that $T_p M$ is isomorphic to $T_p U$.

# 4
Show that for a vector space $V$ (with its canonical smooth structure) and any point $p \in V$, the tangent space $T_p V$ is canonically isomorphic to $V$.

Proof

Let $v \in V$. Define a map $\phi: V \to T_p V$ by its action on an arbitrary smooth function $f: V \to \mathbb{R}$ as $`\phi(v)(f) = \left.\frac{d}{d t}\right|_{t=0} f(p+t v)`$. We will show that this map is a linear isomorphism.

To show that $\phi$ is linear, let $v_1, v_2 \in V$ and $a, b \in \mathbb{R}$. For any smooth function $f: V \to \mathbb{R}$, we show linearity by applying the chain rule to the definition of $\phi$:

$`\phi(a v_1 + b v_2)(f) = \left.\frac{d}{d t}\right|_{t=0} f(p+t(a v_1 + b v_2)) = df_p(a v_1 + b v_2).`$

Then, by the linearity of the differential $df_p$:

$`df_p(a v_1 + b v_2) = a \, df_p(v_1) + b \, df_p(v_2) = a \, \phi(v_1)(f) + b \, \phi(v_2)(f).`$

Since this holds for all $f$, $\phi(a v_1 + b v_2) = a \phi(v_1) + b \phi(v_2)$, and $\phi$ is linear.

To show that $\phi$ is injective, suppose $\phi(v) = 0$. This means $`\phi(v)(f) = 0`$ for all smooth $f$. In particular, for any linear functional $`\lambda \in V^*`$, which is smooth, we have $`0 = \phi(v)(\lambda) = \left.\frac{d}{d t}\right|_{t=0} \lambda(p + t v) = \lambda(v)`$. Since $\lambda(v)=0$ for all $\lambda \in V^*$, we must have $v=0$. Thus $\phi$ is injective. Since $\dim(V) = \dim(T_p V)$, an injective linear map between same-dimension vector spaces is an isomorphism.

# 5
Let $(x, y)$ denote the standard coordinates on $\mathbb{R}^2$. Verify that $(\tilde{x}, \tilde{y})$ are global smooth coordinates on $\mathbb{R}^2$, where

$\tilde{x}=x, \quad \tilde{y}=y+x^3$

Let $p$ be the point $(1,0) \in \mathbb{R}^2$ (in standard coordinates), and show that

$`\left.\frac{\partial}{\partial x}\right|_p \neq\left.\frac{\partial}{\partial \tilde{x}}\right|_p`$

Proof

To verify that $(\tilde{x}, \tilde{y})$ are global smooth coordinates on $\mathbb{R}^2$, we need to show that the map $\Phi: \mathbb{R}^2 \to \mathbb{R}^2$ defined by $\Phi(x, y) = (\tilde{x}, \tilde{y}) = (x, y + x^3)$ is a diffeomorphism.

First, we compute the Jacobian matrix of $\Phi$:

$`J_\Phi = \begin{pmatrix}
\frac{\partial \tilde{x}}{\partial x} & \frac{\partial \tilde{x}}{\partial y} \\
\frac{\partial \tilde{y}}{\partial x} & \frac{\partial \tilde{y}}{\partial y}
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
3x^2 & 1
\end{pmatrix}`$

The determinant of this Jacobian is $1 \cdot 1 - 0 \cdot 3x^2 = 1$, which is non-zero for all $(x, y) \in \mathbb{R}^2$. Therefore, by the Inverse Function Theorem, $\Phi$ is a local diffeomorphism everywhere. Since $\Phi$ is also bijective (its inverse is given by $\Phi^{-1}(\tilde{x}, \tilde{y}) = (\tilde{x}, \tilde{y} - \tilde{x}^3)$), it follows that $\Phi$ is a global diffeomorphism. Thus, $(\tilde{x}, \tilde{y})$ are indeed global smooth coordinates on $\mathbb{R}^2$.

Next, we need to show that $\left.\frac{\partial}{\partial x}\right|_p \neq \left.\frac{\partial}{\partial \tilde{x}}\right|_p$ at the point $p = (1, 0)$.
To do this, we will compute the action of both vector fields on a smooth function $f: \mathbb{R}^2 \to \mathbb{R}$.
Let $f(x, y)$ be a smooth function. Then,

$`\left.\frac{\partial}{\partial x}\right|_p f = \left.\frac{\partial f}{\partial x}\right|_{(1, 0)}`$

To compute $\left.\frac{\partial}{\partial \tilde{x}}\right|_p f$, we use the chain rule:

$`\left.\frac{\partial}{\partial \tilde{x}}\right|_p f = \left.\frac{\partial f}{\partial x}\right|_{(1, 0)} \cdot \left.\frac{\partial x}{\partial \tilde{x}}\right|_p + \left.\frac{\partial f}{\partial y}\right|_{(1, 0)} \cdot \left.\frac{\partial y}{\partial \tilde{x}}\right|_p`$

To find the partial derivatives of the original coordinates with respect to the new ones, we use the inverse map $\Phi^{-1}(\tilde{x}, \tilde{y}) = (x, y) = (\tilde{x}, \tilde{y} - \tilde{x}^3)$.

$`\frac{\partial x}{\partial \tilde{x}} = 1, \quad \frac{\partial y}{\partial \tilde{x}} = -3\tilde{x}^2`$ 

Since $x=\tilde{x}$, we have $\frac{\partial y}{\partial \tilde{x}} = -3x^2$.

At the point $p = (1, 0)$, we have $\frac{\partial y}{\partial \tilde{x}} = -3(1)^2 = -3$.

Thus,

$`\left.\frac{\partial}{\partial \tilde{x}}\right|_p f = \left.\frac{\partial f}{\partial x}\right|_{(1, 0)} \cdot 1 + \left.\frac{\partial f}{\partial y}\right|_{(1, 0)} \cdot (-3) = \left.\frac{\partial f}{\partial x}\right|_{(1, 0)} - 3 \left.\frac{\partial f}{\partial y}\right|_{(1, 0)}`$

Now, we can see that:

$`\left.\frac{\partial}{\partial x}\right|_p f = \left.\frac{\partial f}{\partial x}\right|_{(1, 0)}`$

$`\left.\frac{\partial}{\partial \tilde{x}}\right|_p f = \left.\frac{\partial f}{\partial x}\right|_{(1, 0)} - 3 \left.\frac{\partial f}{\partial y}\right|_{(1, 0)}`$

For the operators to be equal, their actions on any smooth function $f$ must be identical. However, we can see the expressions differ if $\left.\frac{\partial f}{\partial y}\right|_{(1, 0)} \neq 0$. For a concrete example, let $f(x,y)=y$. Then $\left.\frac{\partial}{\partial x}\right|_p f = 0$, while $\left.\frac{\partial}{\partial \tilde{x}}\right|_p f = -3$. Since the results differ, we conclude that

$`\left.\frac{\partial}{\partial x}\right|_p \neq \left.\frac{\partial}{\partial \tilde{x}}\right|_p`$
