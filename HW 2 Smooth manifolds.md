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

Let $\mathcal{A}_H$ be the atlas of hemisphere charts and $\mathcal{A}_S$ be the atlas of stereographic charts.

The hemisphere charts are given by projections. For $i=1, \ldots, n+1$, let

$`U_i^+ = \{X \in S^n \mid X^i > 0\}`$ and $`U_i^- = \{X \in S^n \mid X^i < 0\}`$.

The chart maps $\phi_i^\pm: U_i^\pm \to B^n(0,1)$ are defined by dropping the $i$-th coordinate:

$\phi_i^\pm(X^1, \ldots, X^{n+1}) = (X^1, \ldots, X^{i-1}, X^{i+1}, \ldots, X^{n+1})$.

The inverse maps are:

$(\phi_i^\pm)^{-1}(x_1, \ldots, x_n) = (x_1, \ldots, x_{i-1}, \pm\sqrt{1-|x|^2}, x_i, \ldots, x_n)$, where the $\pm$ sign corresponds to the superscript on $\phi_i^\pm$.

The stereographic charts from the north pole $N=(0,\dots,0,1)$ and south pole $S=(0,\dots,0,-1)$ are $`\psi_N: S^n \setminus \{N\} \to \mathbb{R}^n`$ and $`\psi_S: S^n \setminus \{S\} \to \mathbb{R}^n`$, given by:

$\psi_N(X) = \frac{1}{1-X^{n+1}}(X^1, \ldots, X^n)$

$\psi_S(X) = \frac{1}{1+X^{n+1}}(X^1, \ldots, X^n)$

We need to check the smoothness of the compositions $\psi_N \circ (\phi_i^\pm)^{-1}$ and $\psi_S \circ (\phi_i^\pm)^{-1}$.

1. Transition between $\psi_N$ and $\phi_i^\pm$ for $`i \in \{1, \ldots, n\}`$.

     Let $x \in B^n(0,1)$. The map $(\phi_i^\pm)^{-1}$ sends $x$ to $X = (x_1, \ldots, x_{i-1}, \pm\sqrt{1-|x|^2}, x_i, \ldots, x_n)$.
     
     The $(n+1)$-th component of $X$ is $X^{n+1} = x_n$.
     
     The first $n$ components of $X$ are $(x_1, \ldots, x_{i-1}, \pm\sqrt{1-|x|^2}, x_i, \ldots, x_{n-1})$.
     
     Applying $\psi_N$, we get:
     
     $(\psi_N \circ (\phi_i^\pm)^{-1})(x) = \frac{1}{1-x_n}(x_1, \ldots, x_{i-1}, \pm\sqrt{1-|x|^2}, x_i, \ldots, x_{n-1})$.
     
     The domain is $\phi_i^\pm(U_i^\pm \cap (S^n \setminus \{N\}))$. This map is smooth.

2. Transition between $\psi_S$ and $\phi_i^\pm$ for $`i \in \{1, \ldots, n\}`$.
     
     Similarly, $X^{n+1} = x_n$. Applying $\psi_S$:
     
     $(\psi_S \circ (\phi_i^\pm)^{-1})(x) = \frac{1}{1+x_n}(x_1, \ldots, x_{i-1}, \pm\sqrt{1-|x|^2}, x_i, \ldots, x_{n-1})$.
     
     This is smooth on $B^n(0,1)$ because $x_n > -1$.

3. Transition between $\psi_N$ and $\phi_{n+1}^\pm$.

     Let $x \in B^n(0,1)$. The map $(\phi_{n+1}^\pm)^{-1}$ sends $x$ to $X = (x_1, \ldots, x_n, \pm\sqrt{1-|x|^2})$.
     
     So $X^{n+1} = \pm\sqrt{1-|x|^2}$. The first $n$ components are $(x_1, \ldots, x_n)$.
     
     Applying $\psi_N$:
     
     $(\psi_N \circ (\phi_{n+1}^\pm)^{-1})(x) = \frac{1}{1 \mp \sqrt{1-|x|^2}}(x_1, \ldots, x_n)$.
     
     For $\phi_{n+1}^+$, the map is $\frac{x}{1-\sqrt{1-|x|^2}}$. This is smooth on $`B^n(0,1) \setminus \{0\}`$. The point $x=0$ corresponds to the north pole $N$, which is not in the domain of $\psi_N$.
     
     For $\phi_{n+1}^-$, the map is $\frac{x}{1+\sqrt{1-|x|^2}}$. This is smooth on all of $B^n(0,1)$.

4. Transition between $\psi_S$ and $\phi_{n+1}^\pm$.

     Similarly, $X^{n+1} = \pm\sqrt{1-|x|^2}$. Applying $\psi_S$:
     
     $(\psi_S \circ (\phi_{n+1}^\pm)^{-1})(x) = \frac{1}{1 \pm \sqrt{1-|x|^2}}(x_1, \ldots, x_n)$.
     
     For $\phi_{n+1}^+$, the map is $\frac{x}{1+\sqrt{1-|x|^2}}$, which is smooth on $B^n(0,1)$.
     
     For $\phi_{n+1}^-$, the map is $\frac{x}{1-\sqrt{1-|x|^2}}$, which is smooth on $`B^n(0,1) \setminus \{0\}`$. The point $x=0$ corresponds to the south pole $S$, which is not in the domain of $\psi_S$.

In all cases, the transition maps between charts from $\mathcal{A}_H$ and $\mathcal{A}_S$ are smooth on their domains of definition. Therefore, the atlas $\mathcal{A}_H \cup \mathcal{A}_S$ is a smooth atlas, which implies that the smooth structures induced by $\mathcal{A}_H$ and $\mathcal{A}_S$ are equivalent.

# Exercise 6
Show that $\mathbb{CP}^n$ is a compact smooth manifold. (Part of this is in [Waldron's notes](https://people.math.wisc.edu/~awaldron3/Notes/761%20notes%20final.pdf).)

Proof
