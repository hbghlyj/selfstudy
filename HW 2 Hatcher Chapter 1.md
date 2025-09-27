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

Suppose $f\colon S^1 \to X$. By hypothesis, there's a homotopy $h\colon S^1 \times I \to X$ from $f$ to a constant map. That is, $h_0=f$ and there is a point $x \in X$ such that, for all $s \in S^1, h(s, 1)=x$. Because of the latter condition, $h$ factors through the quotient $`S^1 \times I / S^1 \times\{1\}`$. That is, $h$ is equal to a composition

$`S^1 \times I \to S^1 \times I / S^1 \times\{1\} \to X`$

where the first map is the quotient map.

The pair $(S^1 \times I / S^1 \times\{1\}, S^1 \times\{0\})$ is homeomorphic to $(D^2, S^1)$. The homeomorphism is induced by the map $\Phi\colon S^1 \times I \to D^2$ defined by $\Phi(a, x)=a \cdot(1-x)$, where we look at $a$ and $x$ as complex numbers. So the second map above gives a map $D^2 \to X$ such that the restriction to $S^1$ is equal to $f$.
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
</dd>
  <dt>
    (c) &rArr; (a)
  </dt>
  <dd>

Let $f\colon S^1 \to X$ be a map. Choose a basepoint $s_0 \in S^1$ and let $x_0 = f(s_0)$. Then $f$ can be viewed as a map of pairs $f\colon(S^1, s_0) \to (X, x_0)$. The hypothesis that $\pi_1(X, x_0)=0$ means that $f$ is nullhomotopic via a basepoint-preserving homotopy. This in particular implies that $f$ is homotopic to a constant map (without regard to basepoints), which is (a).
</dd>
</dl>
Finally, if $X$ is simply-connected, then it is path-connected and (c) holds. Thus (a) holds, and every map $f\colon S^1 \to X$ is homotopic to a constant map. And since $X$ is path-connected, all constant maps to $X$ are homotopic.

Conversely, if all maps $S^1 \to X$ are homotopic, then in particular the constant maps are homotopic, so $X$ is path-connected. And since (a) holds, (c) holds as well. Thus $X$ is simply-connected.

## Exercise 6
We can regard $\pi_1(X, x_0)$ as the set of basepoint-preserving homotopy classes of maps $(S^1, s_0) \to(X, x_0)$. Let $[S^1, X]$ be the set of homotopy classes of maps $S^1 \to X$, with no conditions on basepoints. Thus there is a natural map $\Phi\colon\pi_1(X, x_0) \to[S^1, X]$ obtained by ignoring basepoints. Show that $\Phi$ is onto if $X$ is path-connected, and that $\Phi([f])=\Phi([g])$ iff $[f]$ and $[g]$ are conjugate in $\pi_1(X, x_0)$. Hence $\Phi$ induces a one-to-one correspondence between $[S^1, X]$ and the set of conjugacy classes in $\pi_1(X)$, when $X$ is path-connected.

Proof

$\pi_1(X,x_0)$ is the set of endpoint-preserving homotopy classes of loops in $X$ based at $x_0$. A loop is a path $f\colon I \to X$ with $f(0)=f(1)$. The question states we can regard $\pi_1(X, x_0)$ as the set of basepoint-preserving homotopy classes of maps $(S^1, s_0) \to (X, x_0)$.

Note that $I/(0 \sim 1) \cong S^1$ is a homeomorphism. If you have a continuous map $f\colon I \to X$ such that $f(0)=f(1)=x_0$, this factors through the above quotient map, giving a map $f'\colon I/(0 \sim 1) \to X$, with $f'([0]) = x_0$.

Conversely, given a based map $f\colon(S^1, s_0) \to (X,x_0)$, you can obtain a loop $f'\colon I \to X$ with $f'(0)=f'(1)=x_0$ by pre-composing $f$ with the canonical quotient map $I \to I/(0 \sim 1) \cong S^1$.

- To show $\Phi$ is surjective, consider a map $g\colon S^1 \to X$. Pick a basepoint $s_0 \in S^1$ and let $x_1 = g(s_0)$. Let $g'\colon I\to X$ be the loop in $X$ based at $x_1$ corresponding to $g$.

  Since $X$ is path-connected, there is a path $h$ from $x_1$ to $x_0$.
  
  Let $h_t$ be the restriction of $h$ to the interval $[0, t]$, with a reparametrization so that the domain of $h_t$ is still $[0,1]$. Explicitly, we can take $h_t(s)=h(t s)$.
  
  The loop $f' =h \cdot g' \cdot \bar{h}$ is based at $x_0$.
  
  The product $h_t \cdot g'\cdot \bar{h}_t$ gives a free homotopy from $g'$ to $f'$.
  
  Since $f'$ is freely homotopic to $g'$, the class $[f'] \in \pi_1(X, x_0)$ maps to the free homotopy class of $g$ under $\Phi$. Thus $\Phi$ is surjective.

- Suppose $\Phi([f]) = \Phi([g])$. This means $f$ and $g$ are freely homotopic. Let $H: S^1 \times I \to X$ be a free homotopy from $f$ to $g$. \nIdentifying the basepoint with $0$, the path $\alpha(t) \coloneqq H(0, t)$ is a loop at $x_0$ since $\alpha(0) = f(0) = x_0$ and $\alpha(1) = g(0) = x_0$.

  For each $t\in I$, define $\alpha_t(u)\coloneqq H(0,tu)$ (a path from $x_0$ to $H(0,t)$), and a loop
  
  $L_t \coloneqq \alpha_t \star \big(s\mapsto H(s,t)\big) \star \alpha_t^{-1}$
  
  Then $L_t$ is a based loop at $x_0$ depending continuously on $t$, with
  
  $L_0=f$ (since $\alpha_0$ is constant at $x_0$) and $L_1=\alpha\star g\star \alpha^{-1}$.
  
  Thus $f\simeq \alpha\star g\star \alpha^{-1}$ rel endpoints, so in $\pi_1(X,x_0)$
  
  $[f]=[\alpha]\,[g]\,[\alpha]^{-1}\quad\text{equivalently}\quad [g]=[\alpha]^{-1}[f][\alpha]$
  
  Hence $[f]$ and $[g]$ are conjugate.

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
