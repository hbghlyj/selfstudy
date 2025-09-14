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
\left(x_1, \dots, x_n\right) & \mapsto (1-t)\left(x_1, \dots, x_n\right)+\frac{t}{\sqrt{x_1^2+\dots+x_n^2}}\left(x_1, \dots, x_n\right)
\end{aligned}`$

It is continuous because every coordinate component is continuous.
*	$F_0(x) = x$ for all $`x ∈ \mathbb{R}^n-\{0\}`$
*	$F_1(x) = \frac{1}{\sqrt{x_1^2+\dots+x_n^2}}(x_1, \dots, x_n) ∈ S^{n-1}$ for all $`x ∈ \mathbb{R}^n-\{0\}`$
*	$F_t(a) = a$ for all $a ∈ S^{n-1}$ and $t ∈ [0, 1]$

therefore the map is a deformation retraction.

# Exercise 3
1. Show that the composition of homotopy equivalences $X \to Y$ and $Y \to Z$ is a homotopy equivalence $X \to Z$. Deduce that homotopy equivalence is an equivalence relation.
2. Show that the relation of homotopy among maps $X \to Y$ is an equivalence relation.
3. Show that a map homotopic to a homotopy equivalence is a homotopy equivalence.

# Exercise 4
A deformation retraction in the weak sense of a space $X$ to a subspace $A$ is a homotopy $f_t: X \to X$ such that $f_0=\mathbb{1}, f_1(X) \subset A$, and $f_t(A) \subset A$ for all $t$. Show that if $X$ deformation retracts to $A$ in this weak sense, then the inclusion $A \hookrightarrow X$ is a homotopy equivalence.

Proof

To show the inclusion $i: A \hookrightarrow X$ is a homotopy equivalence, we need to find a map $g: X \to A$ such that $g \circ i \simeq \mathbb{1}_A$ and $i \circ g \simeq \mathbb{1}_X$.

Let $f_t: X \to X$ be the weak deformation retraction. We define $g: X \to A$ by $g(x) = f_1(x)$. This map is well-defined since $f_1(X) \subset A$.

1.  Consider the composition $i \circ g: X \to X$. We have $(i \circ g)(x) = i(f_1(x)) = f_1(x)$. So, $i \circ g = f_1$. The map $f_t$ is a homotopy from $f_0 = \mathbb{1}_X$ to $f_1$. Thus, $i \circ g \simeq \mathbb{1}_X$.

2.  Consider the composition $g \circ i: A \to A$. We have $(g \circ i)(a) = g(i(a)) = g(a) = f_1(a)$. So $g \circ i$ is the restriction of $f_1$ to $A$. Let's denote this by $f_1|_A$. The condition $f_t(A) \subset A$ for all $t$ means that the restriction of the homotopy $f_t$ to $A$, let's call it $h_t = f_t|_A: A \to A$, is a homotopy within $A$. This homotopy $h_t$ goes from $h_0 = f_0|_A = \mathbb{1}_A$ to $h_1 = f_1|_A = g \circ i$. Thus, $g \circ i \simeq \mathbb{1}_A$.

Since we have found a homotopy inverse $g$ for the inclusion map $i$, $i$ is a homotopy equivalence.

# Exercise 9
Show that a retract of a contractible space is contractible.

Proof

Let $X$ be a contractible space, so its identity map $`\mathbb{1}_X`$ is homotopic to a constant map $c_{x_0}$ via a homotopy $F: X \times I \to X$. Let $A$ be a retract of $X$ with retraction $r: X \to A$. We can define a homotopy on $A$ by $F_A(a, t) = r(F(a, t))$. This map is continuous and provides a homotopy from $F_A(a, 0) = r(F(a, 0)) = r(a) = \mathbb{1}_A(a)$ to the constant map $F_A(a, 1) = r(F(a, 1)) = r(x_0)$. Thus, $A$ is contractible.

# Exercise 10
Show that a space $X$ is contractible iff every map $f: X \to Y$, for arbitrary $Y$, is nullhomotopic. Similarly, show $X$ is contractible iff every map $f: Y \to X$ is nullhomotopic.

Proof

Suppose $X$ is contractible, then there is a point $x_0$, and maps $`h: X \to\{x_0\}, g:\{x_0\} \to X`$ s.t. $`g h \simeq \mathbb{1}_X`$ and $`h g \simeq \mathbb{1}_{\{x_0\}}`$. Denote the homotopy as $F: X \times I \to X$ where $`F|_{X \times\{0\}}=\mathbb{1}_X`$ and $`F|_{X \times\{1\}}=g h`$.
1. For any $f: X \to Y$ where $Y$ is an arbitrary space, let $`y_0=f(g(x_0))`$, and let $G:=f F$. Thus $G: X \times I \to Y$ is continuous since it is the composition of two continuous maps $`G|_{X \times\{0\}}=f \mathbb{1}=f`$ and $`G|_{X \times\{1\}}=f g h`$. But $`f g h(X)=\{y_0\}`$. Therefore $f: X \to Y$ is nullhomotopic.

2. For any $f: Y \to X$ where $Y$ is an arbitrary space, define $G: Y \times I \to X,(y, t) \mapsto F(f(y), t)$. Hence $`G|_{Y \times\{0\}}=f`$ and $`G|_{Y \times\{1\}}=ghf`$. But $`ghf(Y)=\{g(x_0)\}`$. Thus, $f: Y \to X$ is nullhomotopic.

3. Conversely, if every map $f: Y \to X$ is nullhomotopic (for any $Y$), we can choose $Y=X$ and $f=\mathbb{1}_X: X \to X$. Then $\mathbb{1}_X$ is nullhomotopic, which by definition means $X$ is contractible. Similarly, if every map $f: X \to Y$ is nullhomotopic, we can choose $Y=X$ and $f=\mathbb{1}_X$, which again implies $X$ is contractible.

# Exercise 11
Show that $f: X \to Y$ is a homotopy equivalence if there exist maps $g, h: Y \to X$ such that $f g \simeq \mathbb{1}$ and $h f \simeq \mathbb{1}$. More generally, show that $f$ is a homotopy equivalence if $f g$ and $h f$ are homotopy equivalences.

Proof

1. To show that $g \simeq h$, we have $g = \mathbb{1}_X g \simeq (hf)g = h(fg) \simeq h\mathbb{1}_Y = h$. Thus $g \simeq h$. This implies $gf \simeq hf$. Since $hf \simeq \mathbb{1}_X$, we have $gf \simeq \mathbb{1}_X$. With the given $fg \simeq \mathbb{1}_Y$, this shows $f$ is a homotopy equivalence.

2. More generally, if $fg$ and $hf$ are homotopy equivalences, let $k: Y \to Y$ be a homotopy inverse for $fg$ and $l: X \to X$ be a homotopy inverse for $hf$. Define new maps $g' = gk: Y \to X$ and $h' = lh: Y \to X$. Then we have $fg' = f(gk) = (fg)k \simeq \mathbb{1}_Y$ and $h'f = (lh)f = l(hf) \simeq \mathbb{1}_X$. By part 1, using $g'$ and $h'$, it follows that $f$ is a homotopy equivalence.
