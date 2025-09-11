# Exercise 1
Construct an explicit deformation retraction of the torus with one point deleted
onto a graph consisting of two circles intersecting in a point, namely, longitude and
meridian circles of the torus.

Solution

![](https://i.upmath.me/svgb/rdLBbsIwDADQO1_hy6RWKlU6rbtM5bS_oBxM6kFESCrHrLAo_z5lG0NcOPVm2ZGfbaU_BRJz-LJmy8iXOJD2jGK8C_UR-WDcLqRFv6WdcTE_HI2WE1NaC6MLH56PoNF9Yuhi0Gipe0mbRT8wTuvRB0Gde3XXvlTdgC5egSoHHQqMPphcAlW3LUxG9hB7ZPZTXK1SSmkDhapUCcslFE2lyrc5qNd7yaLQ-Q9rblgzD_Zgr2Zm6sFe_0dUP9gTvDNOIHuCgSwJDTB64-R3CihU3VaqbkvQhrWlnFDPbZ6S3HD3Lb4B)

Define a map $F_t$ from the torus with one point deleted to the boundary of the square (two circles intersecting at a point) as follows:

Draw a ray from the deleted point to each point $x$, intersecting the boundary of the square at $y$.

Define $F_t(x)=(1-t)x+ty$.

This map is continuous because every coordinate component is continuous.

If $x$ is on the boundary of the square, then $y=x$, so $F_t(x)=x$.

# Exercise 2

Construct an explicit deformation retraction of $`\mathbb{R}^n-\{0\}`$ onto $S^{n-1}$.

Solution

Define a map

$`\begin{aligned}
F_t: \mathbb{R}^n-\{0\} & \to S^{n-1} \\
\left(x_1, \cdots, x_n\right) & \mapsto (1-t)\left(x_1, \cdots, x_n\right)+\frac{t}{\sqrt{x_1^2+\cdots+x_n^2}}\left(x_1, \cdots, x_n\right)
\end{aligned}`$

It is continuous because every coordinate component is continuous.
*	$F_0(x) = x$ for all $`x ∈ \mathbb{R}^n-\{0\}`$
*	$F_1(x) ∈ S^{n-1}$ for all $`x ∈ \mathbb{R}^n-\{0\}`$
*	$F_t(a) = a$ for all $a ∈ S^{n-1}$ and $t ∈ [0, 1]$

therefore the map is a deformation retraction.

# Exercise 3
1. Show that the composition of homotopy equivalences $X \to Y$ and $Y \to Z$ is a homotopy equivalence $X \to Z$. Deduce that homotopy equivalence is an equivalence relation.
2. Show that the relation of homotopy among maps $X \to Y$ is an equivalence relation.
3. Show that a map homotopic to a homotopy equivalence is a homotopy equivalence.

# Exercise 4
A deformation retraction in the weak sense of a space $X$ to a subspace $A$ is a homotopy $f_t: X \to X$ such that $f_0=\mathbb{1}, f_1(X) \subset A$, and $f_t(A) \subset A$ for all $t$. Show that if $X$ deformation retracts to $A$ in this weak sense, then the inclusion $A \hookrightarrow X$ is a homotopy equivalence.
 
# Exercise 9
Show that a retract of a contractible space is contractible.

# Exercise 10
Show that a space $X$ is contractible iff every map $f: X \to Y$, for arbitrary $Y$, is nullhomotopic. Similarly, show $X$ is contractible iff every map $f: Y \to X$ is nullhomotopic.

Solution

1. Suppose $X$ is contractible, then there is a point $x_0$, and maps $`h: X \to\left\{x_0\right\}, g:\left\{x_0\right\} \to X`$ s.t. $`\left.g \circ h \simeq \mathrm{id}\right|_X`$ and $`\left.h \circ g \simeq \mathrm{id}\right|_{\left\{x_0\right\}}`$. We denote the homotopy as $F: X \times I \to X$ where $`\left.F\right|_{X \times\{0\}}=\mathrm{id}`$ and $`\left.F\right|_{X \times\{1\}}=g \circ h`$. For any $f: X \to Y$ where $Y$ is an arbitrary space, let $`y_0=f\left(g\left(x_0\right)\right)`$, and let $G:=f \circ F$. Thus $G: X \times I \to Y$ is continuous since it is the composition of two continuous maps. $`\left.G\right|_{X \times\{0\}}=f \circ \mathrm{id}=f`$ and $\left.G\right|_{X \times\{1\}}=f \circ g \circ h$. But $f \circ g \circ h(X)=y_0$. Therefore $f: X \to Y$ is nullhomotopic.
  
  Conversely, put $Y=X$, then we know that $\text{id}:X \to X$ is nullhomotopic. That is, we have a constant map $g: X \to X$ and a homotopy $F: X \times I \to X$ s.t. $`\left.F\right|_{X \times\{0\}}=\text{id}`$ and $`\left.F\right|_{X \times\{1\}}=g`$. $g$ being a constant map means $`g(X)=\{x_0\}`$ for some $x_0 \in X$, so we say $g$ is a map $`X \to\{x_0\}`$ and define $`f:\{x_0\} \to X, x_0 \mapsto x_0`$. Thus $`g \circ f=\text{id}_{\{x_0\}}`$ and $f \circ g=g$. The existence of $F$ implies $f \circ g \simeq \mathrm{id}$.

2. Suppose $X$ is contractible, then there is a point $x_0$, and maps $h: X \to\{x_0\}, g:\{x_0\} \to X$ s.t. $`\left.g \circ h \simeq \mathrm{id}\right|_X`$ and $`\left.h \circ g \simeq \mathrm{id}\right|_{\{x_0\}}`$. We denote the homotopy as $F: X \times I \to X$ where $\left.F\right|_{X \times\{0\}}=\mathrm{id}$ and $`\left.F\right|_{X \times\{1\}}=g \circ h`$. Define $G: Y \times I \to X,(y, t) \mapsto F(f(y), t)$. Hence $`\left.G\right|_{Y \times\{0\}}=F(f(y), 0)=f(y)`$ and $`\left.G\right|_{X \times\{1\}}=F(f(y), 1)=h(g(f(y)))=h(x_0)`$. Thus, $f: X \to Y$ is nullhomotopic.

Conversely, put $Y=X$, then we know that $\text{id}:X \to X$ is nullhomotopic. That is, we have a constant map $g: X \to X$ and a homotopy $F: X \times I \to X$ s.t. $`\left.F\right|_{X \times\{0\}}=\text{id}`$ and $`\left.F\right|_{X \times\{1\}}=g`$. $g$ being a constant map means $`g(X)=\{x_0\}`$ for some $x_0 \in X$, so we say $g$ is a map $`X \to\{x_0\}`$ and define $`f:\{x_0\} \to X, x_0 \mapsto x_0`$. Thus $`g \circ f=\text{id}_{\{x_0\}}`$ and $f \circ g=g$. The existence of $F$ implies $f \circ g \simeq \mathrm{id}$.

# Exercise 11
Show that $f: X \to Y$ is a homotopy equivalence if there exist maps $g, h: Y \to X$ such that $f g \simeq \mathbb{1}$ and $h f \simeq \mathbb{1}$. More generally, show that $f$ is a homotopy equivalence if $f g$ and $h f$ are homotopy equivalences.

Solution
