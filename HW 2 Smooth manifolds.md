# Exercise 1
Show that a topological manifold is the same thing as a $C^0$ manifold.

Proof

A map between open subsets of Euclidean space is said to be of class $C^0$ if it is continuous.

If $M$ is a topological manifold, it possesses an atlas in which each chart map $\phi_\alpha$ is a homeomorphism. Consequently, for any two overlapping charts, the transition map $\phi_\beta \circ \phi_\alpha^{-1}$ is a composition of homeomorphisms, making it a homeomorphism. Thus, every transition map is continuous, satisfying the condition for a $C^0$-atlas. This topological atlas can therefore be considered a $C^0$-atlas.

# Exercise 2
Check that the definition of a smooth function makes sense on a smooth manifold.

Proof

Assume $f$ is smooth according to the definition, meaning there exists a smooth chart $(U, \phi)$ around $p$ such that $f \circ \phi^{-1}: \phi(U \cap V) \to \mathbb{R}$ is smooth as a map between open subsets of Euclidean space.

Now, consider any other smooth chart $(U', \phi')$ also containing $p$, belonging to the smooth structure of $M$.
On the overlap region $\phi'(U \cap U' \cap V)$, we can write:

$f \circ (\phi')^{-1} = (f \circ \phi^{-1}) \circ (\phi \circ (\phi')^{-1})$.

The first part, $f \circ \phi^{-1}$, is smooth by our initial assumption.

The second part, $\phi \circ (\phi')^{-1}$, is a transition map between two charts from the smooth atlas of $M$. By the definition of a smooth atlas, all such transition maps are smooth.

Since the composition of two smooth maps between Euclidean spaces is a smooth map, it follows that $f \circ (\phi')^{-1}$ is smooth.

Therefore, if a function is smooth with respect to one smooth chart, it is smooth with respect to any other smooth chart.

# Exercise 3
Write down (with proof) a smooth structure on the Möbius strip.

Proof

# Exercise 4
The stereographic projection maps on $S^n$ are given by

$X \mapsto x=\frac{1}{1-X^{n+1}}\left(X^1, \ldots, X^n\right), \quad X \mapsto y=\frac{1}{1+X^{n+1}}\left(X^1, \ldots, X^n\right)$

from the north and south poles respectively.

The inverse stereographic projection is given by

$x \mapsto X=\frac{1}{1+|x|^2}\left(2 x^1, \ldots, 2 x^n,|x|^2-1\right)$

Derive the formula for the transition map

$x \mapsto y=\frac{x}{|x|^2}$

Proof

$\frac{x}{|x|^2}=\frac{\frac{1}{1-X^{n+1}}\left(X^1, \ldots, X^n\right)}{\left|\frac{1}{1-X^{n+1}}\left(X^1, \ldots, X^n\right)\right|^2}=\frac{\frac{1}{1-X^{n+1}}\left(X^1, \ldots, X^n\right)}{(\frac{1}{1-X^{n+1}})^2(1-(X^{n+1})^2)}=\frac{1}{1+X^{n+1}}\left(X^1, \ldots, X^n\right)=y$

# Exercise 5
Check that the smooth structure on $S^n$ induced by the stereographic charts is equivalent to the smooth structure induced by the hemisphere charts.

Proof

We need to find a diffeomorphism between the two smooth structures. Let $U_1^+=\{X \in S^n: X^{n+1}>0\}$ and $U_1^-=\{X \in S^n: X^{n+1}<0\}$ be the upper and lower hemisphere charts respectively. The chart maps are given by
$\phi_1^+: U_1^+ \to \mathbb{R}^n, \quad X \mapsto (X^1, \ldots, X^n)$
$\phi_1^-: U_1^- \to \mathbb{R}^n, \quad X \mapsto (X^1, \ldots, X^n)$
The stereographic charts are given by $U_2^+=S^n \backslash\{(0, \ldots, 0,1)\}$ and $U_2^-=S^n \backslash\{(0, \ldots, 0,-1)\}$ with chart maps
$\phi_2^+: U_2^+ \to \mathbb{R}^n, \quad X \mapsto \frac{1}{1-X^{n+1}}\left(X^1, \ldots, X^n\right)$
$\phi_2^-: U_2^- \to \mathbb{R}^n, \quad X \mapsto \frac{1}{1+X^{n+1}}\left(X^1, \ldots, X^n\right)$



# Exercise 6
Show that $\mathbb{CP}^n$ is a compact smooth manifold. (Part of this is in [Waldron's notes](https://people.math.wisc.edu/~awaldron3/Notes/761%20notes%20final.pdf).)

Proof

