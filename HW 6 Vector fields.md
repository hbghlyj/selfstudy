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

Proof

<ol type="a">
<li>

Since $F: M \to N$ is a submersion, for each point $p \in M$, there exists a neighborhood $U_p$ of $p$ such that we can choose local coordinates $(x_1, \ldots, x_m)$ on $U_p$ and $(y_1, \ldots, y_n)$ on $F(U_p)$ such that $F$ takes the form of a projection onto the first $n$ coordinates.

In these local coordinates, we can express the vector field $Y$ on $N$ as $Y = \sum_{i=1}^n Y^i(y) \frac{\partial}{\partial y_i}$. We can then define a local vector field $X_p$ on $U_p$ by lifting the components of $Y$ to $M$:

$X_p = \sum_{i=1}^n Y^i(F(x)) \frac{\partial}{\partial x_i}$.

This construction ensures that $X_p$ is $F$-related to $Y$ on $U_p$.

Next, we cover $M$ with such neighborhoods $`\{U_\alpha\}`$, each with a local $F$-related vector field $X_\alpha$. We can then use a partition of unity $`\{\rho_\alpha\}`$ subordinate to this cover to define a global vector field $X$ on $M$ by

$X = \sum_\alpha \rho_\alpha X_\alpha$.

Since each $X_\alpha$ is smooth and the $\rho_\alpha$ are smooth functions, the resulting vector field $X$ is also smooth. Furthermore, $X$ is $F$-related to $Y$. This follows from the linearity of the pushforward map $dF_p$ at each point $p \in M$:

$`dF_p(X_p) = dF_p(\sum_\alpha \rho_\alpha(p) (X_\alpha)_p) = \sum_\alpha \rho_\alpha(p) dF_p((X_\alpha)_p) = (\sum_\alpha \rho_\alpha(p)) Y_{F(p)} = Y_{F(p)}.`$

Thus, we have constructed a global vector field $X$ on $M$ that is $F$-related to the given vector field $Y$ on $N$.
</li>
<li>

First, we establish the relationship between the integral curves. Since $X$ and $Y$ are $F$-related, if $\gamma_X: I_X \to M$ is the maximal integral curve of $X$ through $p$, then $F \circ \gamma_X$ is an integral curve of $Y$ through $F(p)$. By the definition of a maximal integral curve, this implies that $I_X$ is a subinterval of $I_Y$ (the maximal interval for $Y$'s integral curve through $F(p)$), and $F(\gamma_X(t)) = \gamma_Y(t)$ for all $t \in I_X$. 

Now, we prove $I_X = I_Y$ by contradiction. Assume $I_X$ is a proper subinterval of $I_Y$. Let $I_X = (a', b')$ and $I_Y = (a, b)$, and suppose $b' < b$ (the case $a' > a$ is similar). Since $b' < \infty$, Proposition 20.9 implies that the image $\gamma_X([0, b'))$ is not contained in any compact subset of $M$.

On the other hand, consider the interval $[0, b'] \subset I_Y$. Since $\gamma_Y$ is continuous, the image $K = \gamma_Y([0, b'])$ is a compact subset of $N$. For any $t \in [0, b')$, we have $F(\gamma_X(t)) = \gamma_Y(t) \in K$. Thus, the image $F(\gamma_X([0, b')))$ is contained in the compact set $K$.

Since $F$ is a proper map, the preimage $F^{-1}(K)$ is a compact subset of $M$. We have $\gamma_X([0, b')) \subseteq F^{-1}(F(\gamma_X([0, b')))) \subseteq F^{-1}(K)$. This shows that $\gamma_X([0, b'))$ is contained in a compact set in $M$, which contradicts the conclusion from Proposition 20.9.

Therefore, the assumption $b' < b$ must be false. This means $b' = b$. A similar argument for the lower bound shows $a' = a$. We conclude that $I_X = I_Y$.
</li>
</ol>

# 4.
Suppose that $X, Y$ are smooth vector fields on $M$ with associated flows $\theta: \mathbb{R} \times M \rightarrow M$ and $\eta: \mathbb{R} \times M \rightarrow M$. Show that $X, Y$ commute if and only if $\theta_t \circ \eta_s=\eta_s \circ \theta_t$ for all $t, s \in \mathbb{R}$.

# 5. (Lee 9-17b)
Define two vector fields on $\mathbb{R}^2$ by

$X=(x+1) \frac{\partial}{\partial x}-(y+1) \frac{\partial}{\partial y}, \quad Y=(x+1) \frac{\partial}{\partial x}+(y+1) \frac{\partial}{\partial y} .$

Check that $X$ and $Y$ commute, and find coordinates $u, v$ in a neighborhood of $(1,0)$ such that $X=\frac{\partial}{\partial u}$ and $Y=\frac{\partial}{\partial v}$.

(Hint: Follow example 9.47 in Lee)

Solution

The formula for the Lie bracket is $[X, Y] = (X(Y^1) - Y(X^1)) \frac{\partial}{\partial x} + (X(Y^2) - Y(X^2)) \frac{\partial}{\partial y}$.

Calculating the components, we have:

$X^1 = x + 1, \quad X^2 = -(y + 1), \quad Y^1 = x + 1, \quad Y^2 = y + 1$.

$X(Y^1) = X(x + 1) = (x + 1) \cdot 1 - (y + 1) \cdot 0 = x + 1$,

$Y(X^1) = Y(x + 1) = (x + 1) \cdot 1 + (y + 1) \cdot 0 = x + 1$.

Thus, $X(Y^1) - Y(X^1) = 0$.

$X(Y^2) = X(y + 1) = (x + 1) \cdot 0 - (y + 1) \cdot 1 = -(y + 1)$,

$Y(X^2) = Y(-(y + 1)) = (x + 1) \cdot 0 + (y + 1) \cdot (-1) = -(y + 1)$.

Thus, $X(Y^2) - Y(X^2) = 0$.

Combining these results, we find that $[X, Y] = 0$, confirming that $X$ and $Y$ commute.

Let $\theta_t(x, y)$ be the flow of $X$. Then $\frac{d}{dt}\theta_t(x, y) = X(x, y)$.

Let $\theta_t(x, y) = (x(t), y(t))$. Then:

$\frac{dx}{dt} = x + 1$,

$\frac{dy}{dt} = -(y + 1)$.

Solving these ODEs:

$\frac{dx}{dt} = x + 1 \Rightarrow \frac{dx}{x + 1} = dt \Rightarrow \ln|x + 1| = t + C_1 \Rightarrow x(t) = C_2 e^t - 1$.

$\frac{dy}{dt} = -(y + 1) \Rightarrow \frac{dy}{y + 1} = -dt \Rightarrow \ln|y + 1| = -t + C_3 \Rightarrow y(t) = C_4 e^{-t} - 1$.

Therefore, the flow is $\theta_t(x, y) = (C_2 e^t - 1, C_4 e^{-t} - 1)$.

To find the constants $C_2$ and $C_4$, we use the initial conditions $\theta_0(x, y) = (x, y)$:

$C_2 = x + 1$, $C_4 = y + 1$.

Thus, the flow of $X$ is:

$\theta_t(x, y) = ((x + 1)e^t - 1, (y + 1)e^{-t} - 1)$.

Let $\eta_s(x, y)$ be the flow of $Y$. Then $\frac{d}{ds}\eta_s(x, y) = Y(x, y)$.

Let $\eta_s(x, y) = (\tilde{x}(s), \tilde{y}(s))$. Then:

$\frac{d\tilde{x}}{ds} = \tilde{x} + 1$,

$\frac{d\tilde{y}}{ds} = \tilde{y} + 1$.

Solving these ODEs:

$\frac{d\tilde{x}}{ds} = \tilde{x} + 1 \Rightarrow \frac{d\tilde{x}}{\tilde{x} + 1} = ds \Rightarrow \ln|\tilde{x} + 1| = s + D_1 \Rightarrow \tilde{x}(s) = D_2 e^s - 1$.

$\frac{d\tilde{y}}{ds} = \tilde{y} + 1 \Rightarrow \frac{d\tilde{y}}{\tilde{y} + 1} = ds \Rightarrow \ln|\tilde{y} + 1| = s + D_3 \Rightarrow \tilde{y}(s) = D_4 e^s - 1$.

Note: In a neighborhood of $(1,0)$, the initial conditions $(x,y)$ have $x+1>0$ and $y+1>0$. By continuity, $\tilde{x}(s)+1$ and $\tilde{y}(s)+1$ remain positive along the flow, so we can drop the absolute value signs.

Therefore, the flow is $\eta_s(x, y) = (D_2 e^s - 1, D_4 e^s - 1)$.

To find the constants $D_2$ and $D_4$, we use the initial conditions $\eta_0(x, y) = (x, y)$:

$D_2 = x + 1$, $D_4 = y + 1$.

Thus, the flow of $Y$ is:

$\eta_s(x, y) = ((x + 1)e^s - 1, (y + 1)e^s - 1)$.

Define the coordinate map: At $p = (1, 0)$, define $\Phi(u,v) = \eta_v(\theta_u(1,0))$.

Calculating $\theta_u(1,0)$:

$\theta_u(1,0) = ((1 + 1)e^u - 1, (0 + 1)e^{-u} - 1) = (2e^u - 1, e^{-u} - 1)$.

Now compute $\Phi(u,v) = \eta_v(\theta_u(1,0))$:

$\Phi(u,v) = \eta_v(2e^u - 1, e^{-u} - 1) = ((2e^u - 1 + 1)e^v - 1, (e^{-u} - 1 + 1)e^v - 1)$

$= (2e^{u+v} - 1, e^{v-u} - 1)$.

Find the inverse of $\Phi$:

Let $(x,y) = \Phi(u,v) = (2e^{u+v} - 1, e^{v-u} - 1)$.

From the second equation, we have $y + 1 = e^{v-u} \Rightarrow v - u = \ln(y + 1)$.

From the first equation, we have $x + 1 = 2e^{u+v} \Rightarrow u + v = \ln\left(\frac{x + 1}{2}\right)$.

Solving these two equations for $u$ and $v$:

Adding the two equations:

$2v = \ln\left(\frac{x + 1}{2}\right) + \ln(y + 1) \Rightarrow v = \frac{1}{2} \ln\left(\frac{(x + 1)(y + 1)}{2}\right)$.

Subtracting the second from the first:

$2u = \ln\left(\frac{x + 1}{2}\right) - \ln(y + 1) \Rightarrow u = \frac{1}{2} \ln\left(\frac{x + 1}{2(y + 1)}\right)$.

Thus, the inverse map is:

$\Phi^{-1}(x,y) = \left(\frac{1}{2} \ln\left(\frac{x + 1}{2(y + 1)}\right), \frac{1}{2} \ln\left(\frac{(x + 1)(y + 1)}{2}\right)\right)$.

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
