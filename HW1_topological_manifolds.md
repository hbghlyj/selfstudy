1. Prove that the Möbius strip

$$M=[0,1] \times\left(-\frac{1}{2}, \frac{1}{2}\right) /(0, y) \sim(1,-y)$$

is a topological manifold.

2. Prove that $\mathbb{RP}^2$ is Hausdorff, second-countable, and compact.

3. Prove that $\mathbb{RP}^2$ is homeomorphic to the closed 2-disk with opposite boundary points identified:

$$\mathbb{RP}^2 \cong \overline{\mathbb{D}}^2 /(\cos \theta, \sin \theta) \sim(\cos (\theta+\pi), \sin (\theta+\pi)) .$$

Proof.
Consider the map $f:S^2 \to D^2$ defined by

$$f(x,y,z) = \begin{cases}(x,y)&z>0\cr (-x,-y)&z<0\end{cases}$$

$$f(-x,-y,-z) = (x,y)$$

Thus, $f$ induces a well-defined map $\tilde{f}: \mathbb{RP}^2 \to D^2/\sim$, where $(x,y) \sim (-x,-y)$.

To show that $\tilde{f}$ is continuous, we note that $f$ is continuous and the identification is done in a way that respects the topology of $D^2$.

To show that $\tilde{f}$ is a homeomorphism, we need to show that it is bijective and that its inverse is continuous. $\tilde{f}^{-1}$ can be constructed by lifting points from $D^2/\sim$ back to $\mathbb{RP}^2$

$$\tilde{f}^{-1}([(x,y)]) = [(x,y,\sqrt{1-x^2-y^2})]$$

This map is well-defined and continuous, as it respects the identification in $D^2/\sim$.
