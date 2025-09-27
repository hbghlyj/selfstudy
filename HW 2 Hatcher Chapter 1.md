# Chapter 1.1
## Exercise 2
Show that the change-of-basepoint homomorphism $\beta_h$ depends only on the homotopy class of $h$.

Proof

The change-of-basepoint homomorphism is defined as $\beta_h\colon\pi_1(X, x_1) \to \pi_1(X,x_0)$ sending $[f] \mapsto [h \cdot f \cdot \overline{h}]$, where $\overline{h}$ is the inverse path of $h$.

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



## Exercise 6
We can regard $\pi_1(X, x_0)$ as the set of basepoint-preserving homotopy classes of maps $(S^1, s_0) \to(X, x_0)$. Let $[S^1, X]$ be the set of homotopy classes of maps $S^1 \to X$, with no conditions on basepoints. Thus there is a natural map $\Phi\colon\pi_1(X, x_0) \to[S^1, X]$ obtained by ignoring basepoints. Show that $\Phi$ is onto if $X$ is path-connected, and that $\Phi([f])=\Phi([g])$ iff $[f]$ and $[g]$ are conjugate in $\pi_1(X, x_0)$. Hence $\Phi$ induces a one-to-one correspondence between $[S^1, X]$ and the set of conjugacy classes in $\pi_1(X)$, when $X$ is path-connected.

## Exercise 11
If $X_0$ is the path-component of a space $X$ containing the basepoint $x_0$, show that the inclusion $X_0 \hookrightarrow X$ induces an isomorphism $\pi_1(X_0, x_0) \to \pi_1(X, x_0)$.

Proof

We know that $\iota_*: \pi_1(X_0, x_0) \to \pi_1(X, x_0)$ is a group homomorphism. To show it is surjective, consider a loop $f: I \to X$ based at $x_0$. Since $I$ is path-connected, its image $f(I)$ is path-connected. As $x_0 \in f(I)$, the image must be contained in the path-component $X_0$. Thus, $f$ is a loop in $X_0$, and its class in $\pi_1(X_0, x_0)$ maps to $[f]$ under $\iota_*$. To show it is injective, suppose a loop $f$ in $X_0$ is homotopic in $X$ to the constant loop. The homotopy $H: I \times I \to X$ has a path-connected image that contains $x_0$, so its image lies in $X_0$. Thus, $f$ is null-homotopic in $X_0$. Therefore, $\iota_*$ is an isomorphism.

## Exercise 15
Given a map $f: X \to Y$ and a path $h: I \to X$ from $x_0$ to $x_1$, show that $f_* \beta_h=\beta_{f h} f_*$ in the diagram at the right.

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
