# Exercise 1
Show that a topological manifold is the same thing as a $C^0$ manifold.

Proof

# Exercise 2
Check that the definition of a smooth function makes sense on a smooth manifold.

Proof

Assume $f$ is smooth according to the definition, meaning there exists a smooth chart $(U, \phi)$ around $p$ such that $f \circ \phi^{-1}: \phi(U \cap V) \to \mathbb{R}$ is smooth as a map between open subsets of Euclidean space.

Now, consider any other smooth chart $(U', \phi')$ also containing $p$, belonging to the smooth structure of $M$. Our goal is to demonstrate that $f \circ (\phi')^{-1}: \phi'(U' \cap V) \to \mathbb{R}$ is also smooth.

On the overlap region $\phi'(U \cap U' \cap V)$, we can express the composition $f \circ (\phi')^{-1}$ using the original chart $(U, \phi)$ and the transition map between $(U, \phi)$ and $(U', \phi')$. Specifically, we can write: $f \circ (\phi')^{-1} = (f \circ \phi^{-1}) \circ (\phi \circ (\phi')^{-1})$.

The first part, $f \circ \phi^{-1}$, is smooth by our initial assumption.

The second part, $\phi \circ (\phi')^{-1}$, is a transition map between two charts from the smooth atlas of $M$. By the very definition of a smooth atlas, all such transition maps are diffeomorphisms, and thus, they are smooth.

Since the composition of two smooth maps between Euclidean spaces is itself a smooth map, it follows that $f \circ (\phi')^{-1}$ is smooth.

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

# Exercise 5
Check that the smooth structure on $S^n$ induced by the stereographic charts is equivalent to the smooth structure induced by the hemisphere charts.

Proof

# Exercise 6
Show that $\mathbb{CP}^n$ is a compact smooth manifold. (Part of this is in [Waldron's notes](https://people.math.wisc.edu/~awaldron3/Notes/761%20notes%20final.pdf).)

Proof
