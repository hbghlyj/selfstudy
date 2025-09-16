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

The Möbius strip is the quotient space of the rectangle $[0,1] \times [-1,1]$ by the equivalence relation that identifies the points $(0,y)$ and $(1,-y)$ for all $y \in [-1,1]$.

To define a smooth structure on the Möbius strip, we can use the following charts:

1. Define $U_1 = (0,1) \times (-1,1)$ and the chart map $\phi_1: U_1 \to \mathbb{R}^2$ by $\phi_1(x,y) = (x,y)$. This chart covers the interior of the rectangle and is clearly a homeomorphism onto its image.
2. Define $`U_2 = \{(x,y) \in [0,1] \times [-1,1] \mid x < 0.5\} \cup \{(x,y) \in [0,1] \times [-1,1] \mid x > 0.5\}`$ and the chart map $\phi_2: U_2 \to \mathbb{R}^2$ by
   - For $(x,y)$ with $x < 0.5$, let $\phi_2(x,y) = (x,y)$.
   - For $(x,y)$ with $x > 0.5$, let $\phi_2(x,y) = (x-1,-y)$.
   
    This chart covers the regions near the edges of the rectangle and respects the identification of the edges.

The transition map between the two charts on the overlap $U_1 \cap U_2$ is given by:
- For $(x,y)$ with $x < 0.5$, $\phi_2 \circ \phi_1^{-1}(x,y) = (x,y)$, which is smooth.
- For $(x,y)$ with $x > 0.5$, $\phi_2 \circ \phi_1^{-1}(x,y) = (x-1,-y)$, which is also smooth.

Since both charts are homeomorphisms onto their images and the transition maps are smooth, the collection of these charts forms a smooth atlas on the Möbius strip. Thus, the Möbius strip is a smooth manifold.

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

Define $\mathbb{CP}^n$ as the set of complex lines in $\mathbb{C}^{n+1}$ with homogeneous coordinates $[z_0:\cdots:z_n]$, not all zero, modulo scalar multiplication by $\lambda\in\mathbb{C}^\times$.

For $k=0,\dots,n$ set
$`U_k=\{[z]\in\mathbb{CP}^n:\ z_k\neq 0\},`$

$\iota_k:U_k\to\mathbb{C}^n,$

$\iota_k([z])=(z_0/z_k,\ldots,z_{k-1}/z_k,z_{k+1}/z_k,\ldots,z_n/z_k).$

Each $\iota_k$ is a homeomorphism with inverse

$\iota_k^{-1}(w_0,\ldots,w_{n-1})=[w_0:\cdots:w_{k-1}:1:w_k:\cdots:w_{n-1}],$

so $\{(U_k,\iota_k)\}_{k=0}^n$ is an atlas with model space $\mathbb{C}^n\cong\mathbb{R}^{2n}$.

On overlaps $U_j\cap U_k$ the transition maps are holomorphic (hence smooth). Writing $w=(w_0,\ldots,w_{n-1})=\iota_k([z])$:
- If $j<k$, then $z_j=w_j$ and
$(\iota_j\circ\iota_k^{-1})(w)=\Big(\tfrac{w_0}{w_j},\ldots,\tfrac{w_{j-1}}{w_j},\tfrac{1}{w_j},\tfrac{w_{j+1}}{w_j},\ldots,\tfrac{w_{k-1}}{w_j},\tfrac{w_k}{w_j},\ldots,\tfrac{w_{n-1}}{w_j}\Big).$
- If $j>k$, then $z_j=w_{j-1}$ and
$(\iota_j\circ\iota_k^{-1})(w)=\Big(\tfrac{w_0}{w_{j-1}},\ldots,\tfrac{w_{k-1}}{w_{j-1}},\tfrac{1}{w_{j-1}},\tfrac{w_k}{w_{j-1}},\ldots,\tfrac{w_{j-2}}{w_{j-1}},\tfrac{w_j}{w_{j-1}},\ldots,\tfrac{w_{n-1}}{w_{j-1}}\Big)$.

In each case the denominator is nonzero on $U_j\cap U_k$, so these maps are rational holomorphic functions.

Thus $`\{\iota_k\}`$ defines the default smooth (indeed complex) structure on $\mathbb{CP}^n$, making it a $2n$-dimensional smooth manifold.

Compactness: consider the Hopf fibration $\pi:S^{2n+1}\subset\mathbb{C}^{n+1}\to\mathbb{CP}^n$, $\pi(z)=[z]$. The fiber is $S^1$, the map is continuous and surjective, and $S^{2n+1}$ is compact. Hence $\mathbb{CP}^n\cong S^{2n+1}/S^1$ is compact (and Hausdorff). Therefore $\mathbb{CP}^n$ is a compact smooth manifold.
