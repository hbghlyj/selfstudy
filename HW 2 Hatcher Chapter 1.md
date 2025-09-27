# Chapter 1.1
## Exercise 2
Show that the change-of-basepoint homomorphism $\beta_h$ depends only on the homotopy class of $h$.

Proof

The change-of-basepoint homomorphism is defined as $\beta_h\colon\pi_1(X, x_1) \to \pi_1(X,x_0)$ sending $[f] \mapsto [h \cdot f \cdot \overline{h}]$, where $\overline{h}$ is the inverse path of $h$.

To show that $\beta_h$ depends only on the homotopy class of $h$, let $g$ be another path from $x_0$ to $x_1$ such that $h \simeq g$. We must show that $\beta_h = \beta_g$, which means $\beta_h([f]) = \beta_g([f])$ for any $[f] \in \pi_1(X, x_1)$. This is equivalent to showing $[h \cdot f \cdot \overline{h}] = [g \cdot f \cdot \overline{g}]$.

Since path homotopy is a congruence relation with respect to path concatenation and inversion, $h \simeq g$ implies $\overline{h} \simeq \overline{g}$. We can then construct a chain of homotopies:
$$ h \cdot f \cdot \overline{h} \simeq g \cdot f \cdot \overline{h} \quad (\text{since } h \simeq g) $$
$$ g \cdot f \cdot \overline{h} \simeq g \cdot f \cdot \overline{g} \quad (\text{since } \overline{h} \simeq \overline{g}) $$
By transitivity, $h \cdot f \cdot \overline{h} \simeq g \cdot f \cdot \overline{g}$. Therefore, $[h \cdot f \cdot \overline{h}] = [g \cdot f \cdot \overline{g}]$, which proves that $\beta_h = \beta_g$.

## Exercise 5
Show that for a space $X$, the following three conditions are equivalent:
<ol type="a">
<li>
Every map $S^1 \to X$ is homotopic to a constant map, with image a point.
</li>
<li>
Every map $S^1 \to X$ extends to a map $D^2 \to X$.
</li>
<li>
$\pi_1(X, x_0)=0$ for all $x_0 \in X$.
</li>
</ol>

Deduce that a space $X$ is simply-connected iff all maps $S^1 \to X$ are homotopic. [In this problem, 'homotopic' means 'homotopic without regard to basepoints'.]

Proof

<dl>
  <dt>
    (a) &rArr; (b)
  </dt>
  <dd>
    Suppose $f: S^1 \to X$. By hypothesis, there's a homotopy $h: S^1 \times I \to X$ from $f$ to a constant map. That is, $h_0=f$ and there is a point $x \in X$ such that, for all $s \in S^1, h(s, 1)=x$. Because of the latter condition, $h$ factors through the quotient $`S^1 \times I / S^1 \times\{1\}`$. That is, $h$ is equal to a composition

$`S^1 \times I \to S^1 \times I / S^1 \times\{1\} \to X`$

where the first map is the quotient map.

The pair $`(S^1 \times I / S^1 \times\{1\}, S^1 \times\{0\})`$ is homeomorphic to $(D^2, S^1)$. The homeomorphism is induced by the map $\Phi: S^1 \times I \to D^2$ defined by $\Phi(a, x)=a \cdot(1-x)$, where we look at $a$ and $x$ as complex numbers. So the second map above gives a map $D^2 \to X$ such that the restriction to $S^1$ is equal to $f$.
</dd>
  <dt>    
    (b) &rArr; (c)
  </dt>
  <dd>

    As in the next problem, we can regard $\pi_1(X, x_0)$ as the set of basepoint-preserving homotopy classes of maps $(S^1, s_0) \to(X, x_0)$. Suppose $f\colon(S^1, s_0) \to(X, x_0)$ is such a map. By hypothesis, it extends to a map $h\colon(D^2, s_0) \to(X, x_0)$. Let $\phi$ be a deformation-retraction of $D^2$ onto $s_0$. Then

$`\begin{aligned}
S^1 \times I & \to X \\
(s, t) & \mapsto f(\phi_t(s))
\end{aligned}`$

is a basepoint-preserving homotopy of $f$ to the constant map with value $x_0$. So all loops in $X$ are nullhomotopic, and so $\pi_1(X, x_0)$ is trivial.

(Here is an easy way to get a deformation-retraction of $D^2$ onto a point $s_0$ in its boundary: Identify $D^2$ with the disk of unit radius in the plane with center at $(1,0)$, so the origin is a boundary point. Let $s_0 = (0,0)$. Then

$`\begin{aligned}
D^2 \times I & \to D^2 \\
\quad(\vec{d}, t) & \mapsto(1-t) \vec{d}
\end{aligned}`$

is the desired deformation-retraction.)
</dd>
  <dt>
    (c) &rArr; (a)
  </dt>
  <dd>

    Let $f: S^1 \to X$ be a map. Choose a basepoint $s_0 \in S^1$ and let $x_0 = f(s_0)$. Then $f$ can be viewed as a map of pairs $f: (S^1, s_0) \to (X, x_0)$. The hypothesis that $\pi_1(X, x_0)=0$ means that $f$ is nullhomotopic via a basepoint-preserving homotopy. This in particular implies that $f$ is homotopic to a constant map (without regard to basepoints), which is (a).
</dd>
</dl>
Finally, if $X$ is simply-connected, then it is path-connected and (c) holds. Thus (a) holds, and every map $f\colon S^1 \to X$ is homotopic to a constant map. And since $X$ is path-connected, all constant maps to $X$ are homotopic.

Conversely, if all maps $S^1 \to X$ are homotopic, then in particular the constant maps are homotopic, so $X$ is path-connected. And since (a) holds, (c) holds as well. Thus $X$ is simply-connected.

## Exercise 6
We can regard $\pi_1(X, x_0)$ as the set of basepoint-preserving homotopy classes of maps $(S^1, s_0) \to(X, x_0)$. Let $[S^1, X]$ be the set of homotopy classes of maps $S^1 \to X$, with no conditions on basepoints. Thus there is a natural map $\Phi\colon\pi_1(X, x_0) \to[S^1, X]$ obtained by ignoring basepoints. Show that $\Phi$ is onto if $X$ is path-connected, and that $\Phi([f])=\Phi([g])$ iff $[f]$ and $[g]$ are conjugate in $\pi_1(X, x_0)$. Hence $\Phi$ induces a one-to-one correspondence between $[S^1, X]$ and the set of conjugacy classes in $\pi_1(X)$, when $X$ is path-connected.

## Exercise 11
If $X_0$ is the path-component of a space $X$ containing the basepoint $x_0$, show that the inclusion $X_0 \hookrightarrow X$ induces an isomorphism $\pi_1(X_0, x_0) \to \pi_1(X, x_0)$.

Proof

We know that $`\iota_*\colon\pi_1(X_0, x_0) \to \pi_1(X, x_0)`$ is a group homomorphism.

- To show it is surjective, consider a loop $f\colon I \to X$ based at $x_0$. Since $I$ is path-connected, its image $f(I)$ is path-connected. As $x_0 \in f(I)$, the image must be contained in the path-component $X_0$. Thus, $f$ is a loop in $X_0$, and its class in $\pi_1(X_0, x_0)$ maps to $[f]$ under $`\iota_*`$.

- To show it is injective, suppose a loop $f$ in $X_0$ is homotopic in $X$ to the constant loop. The homotopy $H\colon I \times I \to X$ has a path-connected image that contains $x_0$, so its image lies in $X_0$. Thus, $f$ is null-homotopic in $X_0$.

Therefore, $\iota_*$ is an isomorphism.

## Exercise 15
Given a map $f\colon X \to Y$ and a path $h\colon I \to X$ from $x_0$ to $x_1$, show that $f_* \beta_h=\beta_{f h} f_*$ in the diagram at the right.

$`\begin{CD}
\pi_{1}(X,x_{1})    @>\beta_{h}>>    \pi_{1}(X,x_{0})   \\
@V f_* VV                        @V f_* VV            \\
\pi_{1}\bigl(Y,f(x_{1})\bigr)  @>\beta_{fh}>> \pi_{1}\bigl(Y,f(x_{0})\bigr)
\end{CD}`$

Proof

Suppose $[\omega]$ is an element in $\pi_1(X, x_1)$, then

$`
\beta_{f \circ h} (f_*([\omega])) = \beta_{f \circ h}([f \circ \omega]) = [(f \circ h) \cdot (f \circ \omega) \cdot \overline{f \circ h}] = [f \circ (h \cdot \omega \cdot \overline{h})] = f_*([h \cdot \omega \cdot \overline{h}]) = f_*(\beta_h([\omega])).
`$

Hence the diagram commutes.
