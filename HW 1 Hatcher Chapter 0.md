# Exercise 1
Construct an explicit deformation retraction of the torus with one point deleted
onto a graph consisting of two circles intersecting in a point, namely, longitude and
meridian circles of the torus.

Solution

![](https://i.upmath.me/svgb/rdLBbsIwDADQO1_hy6RWKlU6rbtM5bS_oBxM6kFESCrHrLAo_z5lG0NcOPVm2ZGfbaU_BRJz-LJmy8iXOJD2jGK8C_UR-WDcLqRFv6WdcTE_HI2WE1NaC6MLH56PoNF9Yuhi0Gipe0mbRT8wTuvRB0Gde3XXvlTdgC5egSoHHQqMPphcAlW3LUxG9hB7ZPZTXK1SSmkDhapUCcslFE2lyrc5qNd7yaLQ-Q9rblgzD_Zgr2Zm6sFe_0dUP9gTvDNOIHuCgSwJDTB64-R3CihU3VaqbkvQhrWlnFDPbZ6S3HD3Lb4B)

Define a map $F_t$ from the torus with one point deleted to the boundary of the square ($S^1\vee S^1$) as follows:

Draw a ray from the deleted point to each point $x$, intersecting the boundary of the square at $y$.

Define $F_t(x)=(1-t)x+ty$.

This map is continuous because every coordinate component is continuous.
* $F_0(x)=x$
* $F_1(x)=y∈S^1\vee S^1$
* If $x∈S^1\vee S^1$, then $y=x$, so $F_t(x)=x$

# Exercise 2

Construct an explicit deformation retraction of $`\mathbb{R}^n-\{0\}`$ onto $S^{n-1}$.

Solution

Define a map

$`\begin{aligned}
F_t: \mathbb{R}^n-\{0\} & \to \mathbb{R}^n-\{0\} \\
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

Proof

Let $X$ be a contractible space, so its identity map $\mathbb{1}_X$ is homotopic to a constant map $c_{x_0}$ via a homotopy $F: X \times I \to X$. Let $A$ be a retract of $X$ with retraction $r: X \to A$. We can define a homotopy on $A$ by $F_A(a, t) = r(F(a, t))$. This map is continuous and provides a homotopy from $F_A(a, 0) = r(F(a, 0)) = r(a) = \mathbb{1}_A(a)$ to the constant map $F_A(a, 1) = r(F(a, 1)) = r(x_0)$. Thus, $A$ is contractible.

# Exercise 10
Show that a space $X$ is contractible iff every map $f: X \to Y$, for arbitrary $Y$, is nullhomotopic. Similarly, show $X$ is contractible iff every map $f: Y \to X$ is nullhomotopic.

Proof

Suppose $X$ is contractible, then there is a point $x_0$, and maps $`h: X \to\{x_0\}, g:\{x_0\} \to X`$ s.t. $`g h \simeq \mathbb{1}_X`$ and $`h g \simeq \mathbb{1}_{\{x_0\}}`$. Denote the homotopy as $F: X \times I \to X$ where $`F|_{X \times\{0\}}=\mathbb{1}_X`$ and $`F|_{X \times\{1\}}=g h`$.
1. For any $f: X \to Y$ where $Y$ is an arbitrary space, let $`y_0=f(g(x_0))`$, and let $G:=f F$. Thus $G: X \times I \to Y$ is continuous since it is the composition of two continuous maps $`G|_{X \times\{0\}}=f \mathbb{1}=f`$ and $`G|_{X \times\{1\}}=f g h`$. But $`f g h(X)=\{y_0\}`$. Therefore $f: X \to Y$ is nullhomotopic.

2. For any $f: Y \to X$ where $Y$ is an arbitrary space, define $G: Y \times I \to X,(y, t) \mapsto F(f(y), t)$. Hence $`G|_{Y \times\{0\}}=f`$ and $`G|_{Y \times\{1\}}=ghf`$. But $`ghf(Y)=\{g(x_0)\}`$. Thus, $f: Y \to X$ is nullhomotopic.

3. Conversely, put $Y=X$, then we know that $\mathbb{1}:X \to X$ is nullhomotopic. That is, we have a constant map $`g: X \to X,g(X)=\{x_0\}`$ and a homotopy $F: X \times I \to X$ s.t. $`F|_{X \times\{0\}}=\mathbb{1}_X`$ and $`F|_{X \times\{1\}}=g`$, define $`f:\{x_0\} \to X, x_0 \mapsto x_0`$. Thus $`g f=\mathbb{1}_{\{x_0\}}`$ and $f g \overset{F}\simeq \mathbb{1}_X$.

# Exercise 11
Show that $f: X \to Y$ is a homotopy equivalence if there exist maps $g, h: Y \to X$ such that $f g \simeq \mathbb{1}$ and $h f \simeq \mathbb{1}$. More generally, show that $f$ is a homotopy equivalence if $f g$ and $h f$ are homotopy equivalences.

Proof

1. To show that $g \simeq h$, we have $g = \mathbb{1}_X g \simeq (hf)g = h(fg) \simeq h\mathbb{1}_Y = h$. Thus $g \simeq h$. This implies $gf \simeq hf$. Since $hf \simeq \mathbb{1}_X$, we have $gf \simeq \mathbb{1}_X$. With the given $fg \simeq \mathbb{1}_Y$, this shows $f$ is a homotopy equivalence.

2. More generally, if $fg$ and $hf$ are homotopy equivalences, let $k: Y \to Y$ be a homotopy inverse for $fg$ and $l: X \to X$ be a homotopy inverse for $hf$. Define new maps $g' = gk: Y \to X$ and $h' = lh: Y \to X$. Then we have $fg' = f(gk) = (fg)k \simeq \mathbb{1}_Y$ and $h'f = (lh)f = l(hf) \simeq \mathbb{1}_X$. By part 1, using $g'$ and $h'$, it follows that $f$ is a homotopy equivalence.
