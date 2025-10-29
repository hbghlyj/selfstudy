# 1. (Lee 8-20)
Define the following three vector fields on $S^2$:

$X=z \frac{\partial}{\partial y}-y \frac{\partial}{\partial z}, \quad Y=x \frac{\partial}{\partial z}-z \frac{\partial}{\partial x}, \quad Z=y \frac{\partial}{\partial x}-x \frac{\partial}{\partial y} .$

Show that these span a 3-dimensional Lie subalgebra of $\mathscr{X}(S^2)$ which is isomorphic to $\mathbb{R}^3$ equipped with the cross product $\times$.

Proof

Let $\varphi: \mathbb{R}^3 \to \mathscr{X}(S^2)$ be defined by

$\varphi(a, b, c)=a X+b Y+c Z .$

It is clear that $\varphi$ is linear. We will show that it is a Lie algebra homomomorphism with trivial kernel, which will prove the result.

First, we compute the Lie brackets of $X, Y, Z$:

$[X, Y]=Z, \quad [Y, Z]=X, \quad [Z, X]=Y .$

From these relations, it follows that for any $(a, b, c),(d, e, f) \in \mathbb{R}^3$,

$`\begin{aligned}{}[\varphi(a, b, c), \varphi(d, e, f)] &= [a X+b Y+c Z, d X+e Y+f Z] \\ &=a d[X, X]+a e[X, Y]+a f[X, Z]+b d[Y, X]+b e[Y, Y]+b f[Y, Z]+c d[Z, X]+c e[Z, Y]+c f[Z, Z] \\ &=a e Z - a f Y - b d Z + b f X + c d Y - c e X \\ &= (bf-ce)X + (cd-af)Y + (ae-bd)Z \\ &= \varphi((a,b,c) \times (d,e,f)).\end{aligned}`$

Thus, $\varphi$ is a Lie algebra homomorphism.

Next, suppose that $\varphi(a, b, c)=0$. Then, for all $p \in S^2$, we have

$a X_p+b Y_p+c Z_p=0 .$

Evaluating this at the point $(1,0,0)$ gives $b=0$ and $c=0$. Evaluating at $(0,1,0)$ then gives $a=0$. Thus, the kernel of $\varphi$ is trivial, so $\varphi$ is injective.

Since the domain of $\varphi$ has dimension 3 and $\varphi$ is injective, its image is also 3-dimensional. It follows that $\varphi$ is an isomorphism onto its image.

Therefore, the image of $\varphi$ is a 3-dimensional Lie subalgebra of $\mathscr{X}(S^2)$ isomorphic to $\mathbb{R}^3$ with the cross product.

# 2.
Prove the Jacobi identity $\mathscr{L}_X[Y, Z]=[\mathscr{L}_X Y, Z]+[Y, \mathscr{L}_X Z]$ (Corollary 21.3b) directly from Definition 21.1.

(Note: you may use the fact that pushforward commutes with the Lie bracket, i.e. Proposition 17.10.)

Proof

By definition, $`(\mathscr{L}_X Y)_p = \lim_{t \to 0} \frac{Y_{\theta_t(p)} - (\theta_t)_* Y_p}{t}`$.
The LHS of the identity is $`(\mathscr{L}_X[Y, Z])_p = \lim_{t \to 0} \frac{[Y, Z]_{\theta_t(p)} - (\theta_t)_*[Y, Z]_p}{t}`$.

Using the hint that pushforward commutes with the Lie bracket, $`(\theta_t)_*[Y, Z]_p = [(\theta_t)_*Y_p, (\theta_t)_*Z_p]`$. The numerator becomes:
$`[Y_{\theta_t(p)}, Z_{\theta_t(p)}] - [(\theta_t)_*Y_p, (\theta_t)_*Z_p]`$

Using bilinearity of the bracket, this is equal to:
$`[Y_{\theta_t(p)}, Z_{\theta_t(p)} - (\theta_t)_*Z_p] + [Y_{\theta_t(p)} - (\theta_t)_*Y_p, (\theta_t)_*Z_p]`$

Substituting this back and taking the limit:
$`\begin{aligned} (\mathscr{L}_X[Y, Z])_p &= \lim_{t \to 0} \frac{[Y_{\theta_t(p)}, Z_{\theta_t(p)} - (\theta_t)_*Z_p] + [Y_{\theta_t(p)} - (\theta_t)_*Y_p, (\theta_t)_*Z_p]}{t} \\ &= \lim_{t \to 0} [Y_{\theta_t(p)}, \frac{Z_{\theta_t(p)} - (\theta_t)_*Z_p}{t}] + \lim_{t \to 0} [\frac{Y_{\theta_t(p)} - (\theta_t)_*Y_p}{t}, (\theta_t)_*Z_p] \\ &= [Y_p, (\mathscr{L}_X Z)_p] + [(\mathscr{L}_X Y)_p, Z_p] \\ &= [\mathscr{L}_X Y, Z]_p + [Y, \mathscr{L}_X Z]_p \end{aligned}`$

This completes the proof.

# 3.
<ol type="a">
<li>
    
Let $F: M \to N$ be a submersion and let $Y$ be a vector field on $N$. Prove that there exists a vector field $X$ on $M$ which is $F$-related to $Y$.
</li>
<li>

Suppose that $F$ is proper and surjective. Given $p \in M$, show that the maximal integral curve of $X$ through $p$ is defined on the same interval as the maximal integral curve of $Y$ through $F(p)$.
</li>
</ol>

# 4.
Suppose that $X, Y$ are smooth vector fields on $M$ with associated flows $\theta: \mathbb{R} \times M \rightarrow M$ and $\eta: \mathbb{R} \times M \rightarrow M$. Show that $X, Y$ commute if and only if $\theta_t \circ \eta_s=\eta_s \circ \theta_t$ for all $t, s \in \mathbb{R}$.

# 5. (Lee 9-17b)
Define two vector fields on $\mathbb{R}^2$ by

$X=(x+1) \frac{\partial}{\partial x}-(y+1) \frac{\partial}{\partial y}, \quad Y=(x+1) \frac{\partial}{\partial x}+(y+1) \frac{\partial}{\partial y} .$

Check that $X$ and $Y$ commute, and find coordinates $u, v$ in a neighborhood of $(1,0)$ such that $X=\frac{\partial}{\partial u}$ and $Y=\frac{\partial}{\partial v}$.

(Hint: Follow example 9.47 in Lee)

# 6. Multilinear algebra needed later.
Recall that the dual space $V^*$ of a vector space $V$ is the set of linear maps $\omega: V \to \mathbb{R}$ (also called covectors).
Recall that if $`\{e_1, \ldots, e_n\}`$ is a basis for $V$ then $`\{\epsilon_1, \ldots, \epsilon_n\}`$ is a basis for $`V^*`$ where $\epsilon_i(e_j)=\delta_{i j}$.

The tensor product of $`\omega, \eta \in V^*`$ is defined to be $\omega \otimes \eta(v_1, v_2)=\omega(v_1) \eta(v_2)$.
This generalizes to $\omega_1 \otimes \cdots \otimes \omega_k$ for $\omega_i \in V^*$. Let $W=L(V^n ; \mathbb{R})$ be the vector space of multilinear maps from $V^n \to \mathbb{R}$.
Find a basis for $W$ in terms of tensors of $\epsilon_i$ (and prove it).

Proof

Consider the set of all possible tensor products of the form $\epsilon_{i_1} \otimes \epsilon_{i_2} \otimes \cdots \otimes \epsilon_{i_n}$, where each $i_j$ ranges from $1$ to $n$.

There are $n^n$ such tensor products, as each of the $n$ positions can be filled with any of the $n$ basis covectors.

We will show that these tensor products form a basis for $W$.

To show that these tensor products span $W$, let $T \in W$ be a multilinear map. For any vectors $v_k = \sum_j v_k^j e_j$, we can expand $T$ by multilinearity:

$T(v_1, \ldots, v_n) = \sum_{i_1, \ldots, i_n} v_1^{i_1} \cdots v_n^{i_n} T(e_{i_1}, \ldots, e_{i_n})$

Since $v_k^{i_k} = \epsilon_{i_k}(v_k)$, this is equivalent to $T = \sum_{i_1, \ldots, i_n} T(e_{i_1}, \ldots, e_{i_n}) \epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_n}$. This proves that the set spans $W$.

To show that these tensor products are linearly independent, suppose we have a linear combination

$\sum_{i_1, \ldots, i_n} c_{i_1, \ldots, i_n} \epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_n} = 0$

for some coefficients $c_{i_1, \ldots, i_n} \in \mathbb{R}$.

We can evaluate this expression on a set of basis vectors $(e_{j_1}, \ldots, e_{j_n})$:

$0 = \left(\sum_{i_1, \ldots, i_n} c_{i_1, \ldots, i_n} \epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_n}\right)(e_{j_1}, \ldots, e_{j_n}) = \sum_{i_1, \ldots, i_n} c_{i_1, \ldots, i_n} \delta_{i_1 j_1} \cdots \delta_{i_n j_n} = c_{j_1, \ldots, j_n}$.

Since this holds for any choice of indices $(j_1, \ldots, j_n)$, all coefficients must be zero, proving linear independence.

Thus, we conclude that the set of tensor products $`\{\epsilon_{i_1} \otimes \cdots \otimes \epsilon_{i_n}\}`$ forms a basis for $W$.
