# Exercise 1
Construct an explicit deformation retraction of the torus with one point deleted
onto a graph consisting of two circles intersecting in a point, namely, longitude and
meridian circles of the torus.

Solution

View the torus with one point deleted as the quotient of the square with one point deleted, $I^2 - {(1/2, 1/2)}$, by identifying opposite edges.

![](https://i.upmath.me/svgb/rdLBbsIwDADQO1_hy6RWKlU6rbtM5bS_oBxM6kFESCrHrLAo_z5lG0NcOPVm2ZGfbaU_BRJz-LJmy8iXOJD2jGK8C_UR-WDcLqRFv6WdcTE_HI2WE1NaC6MLH56PoNF9Yuhi0Gipe0mbRT8wTuvRB0Gde3XXvlTdgC5egSoHHQqMPphcAlW3LUxG9hB7ZPZTXK1SSmkDhapUCcslFE2lyrc5qNd7yaLQ-Q9rblgzD_Zgr2Zm6sFe_0dUP9gTvDNOIHuCgSwJDTB64-R3CihU3VaqbkvQhrWlnFDPbZ6S3HD3Lb4B)

Draw a ray from the deleted point to each point $x$, intersecting the boundary of the square at $y$.

Define a map $F_t(x)=(1-t)x+ty$ from the torus with one point deleted to the boundary of the square.

This map is continuous because it respects the edge identifications.
* $F_0(x)=x$
* $F_1(x)=y$ in the boundary of the square
* For $x$ in the boundary of the square, $y=x$, so $F_t(x)=x$

# Exercise 2

Construct an explicit deformation retraction of $`\mathbb{R}^n-\{0\}`$ onto $S^{n-1}$.

Solution

Define a map

$`\begin{aligned}
F_t\colon \mathbb{R}^n-\{0\} & \to \mathbb{R}^n-\{0\} \\
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

Proof
1. Let $f\colon X \to Y$ and $g\colon Y \to Z$ be homotopy equivalences. Then there exist maps $f'\colon Y \to X$ and $g'\colon Z \to Y$ such that $f f' \simeq \mathbb{1}_Y$, $f' f \simeq \mathbb{1}_X$, $g g' \simeq \mathbb{1}_Z$, and $g' g \simeq \mathbb{1}_Y$. We need to show that the composition $g f\colon X \to Z$ is a homotopy equivalence. Define the map $h = f' g'\colon Z \to X$.
    *	$(g f) h = g (f f') g' \simeq g \mathbb{1}_Y g' = g g' \simeq \mathbb{1}_Z$
    *	$h (g f) = f' (g' g) f \simeq f' \mathbb{1}_Y f = f' f \simeq \mathbb{1}_X$

    Thus, $g f$ is a homotopy equivalence with homotopy inverse $h$. This proves transitivity. Homotopy equivalence is an equivalence relation because it is also reflexive (the identity map is a homotopy equivalence) and symmetric (if $f$ is a homotopy equivalence with inverse $g$, then $g$ is a homotopy equivalence with inverse $f$).
2. Let $f, g, h\colon X \to Y$ be continuous maps. We need to show that homotopy is reflexive, symmetric, and transitive.
    * Reflexive: The homotopy $F(x, t) = f(x)$ shows that $f \simeq f$.
    * Symmetric: If $f \simeq g$ via a homotopy $F(x, t)$, then the homotopy $G(x, t) = F(x, 1 - t)$ shows that $g \simeq f$.
    * Transitive: If $f \simeq g$ via a homotopy $F(x, t)$ and $g \simeq h$ via a homotopy $G(x, t)$, the homotopy $`H(x, t) = \begin{cases} F(x, 2t) & \text{if } 0 \leq t \leq 0.5 \\ G(x, 2t - 1) & \text{if } 0.5 < t \leq 1 \end{cases}`$ shows that $f \simeq h$.

    Thus, homotopy is an equivalence relation.
3. Let $f\colon X \to Y$ be a homotopy equivalence with homotopy inverse $g\colon Y \to X$, and let $h\colon X \to Y$ be a map homotopic to $f$ via a homotopy $F(x, t)$.
    *    $h g \simeq f g \simeq \mathbb{1}_Y$
    *    $g h \simeq g f \simeq \mathbb{1}_X$
    
    Thus, $h$ is a homotopy equivalence with homotopy inverse $g$.

# Exercise 4
A deformation retraction in the weak sense of a space $X$ to a subspace $A$ is a homotopy $f_t\colon X \to X$ such that $f_0=\mathbb{1}, f_1(X) \subset A$, and $f_t(A) \subset A$ for all $t$. Show that if $X$ deformation retracts to $A$ in this weak sense, then the inclusion $A \hookrightarrow X$ is a homotopy equivalence.

Proof

To show the inclusion $i\colon A \hookrightarrow X$ is a homotopy equivalence, we need to find a map $g\colon X \to A$ such that $g i \simeq \mathbb{1}_A$ and $i g \simeq \mathbb{1}_X$.

Let $f_t\colon X \to X$ be the weak deformation retraction. We define $g\colon X \to A$ by $g(x) = f_1(x)$. This map is well-defined since $f_1(X) \subset A$.

1.  Consider the composition $i g\colon X \to X$. We have $(i g)(x) = i(f_1(x)) = f_1(x)$. So, $i g = f_1$. The map $f_t$ is a homotopy from $f_0 = \mathbb{1}_X$ to $f_1$. Thus, $i g \simeq \mathbb{1}_X$.

2.  Consider the composition $g i\colon A \to A$. We have $(g i)(a) = g(i(a)) = g(a) = f_1(a)$. So $g i$ is the restriction of $f_1$ to $A$. Denote this by $f_1|_A$. The condition $f_t(A) \subset A$ for all $t$ means that the restriction of the homotopy $f_t$ to $A$, call it $h_t = f_t|_A\colon A \to A$, is a homotopy within $A$. This homotopy $h_t$ goes from $h_0 = f_0|_A = \mathbb{1}_A$ to $h_1 = f_1|_A = g i$. Thus, $g i \simeq \mathbb{1}_A$.

Since we have found a homotopy inverse $g$ for the inclusion map $i$, $i$ is a homotopy equivalence.

# Exercise 9
Show that a retract of a contractible space is contractible.

Proof

Let $X$ be a contractible space, so its identity map $`\mathbb{1}_X`$ is homotopic to a constant map $c_{x_0}$ via a homotopy $F\colon X \times I \to X$. Let $A$ be a retract of $X$ with retraction $r\colon X \to A$. We can define a homotopy on $A$ by $F_A(a, t) = r(F(a, t))$. This map is continuous and provides a homotopy from $F_A(a, 0) = r(F(a, 0)) = r(a) = \mathbb{1}_A(a)$ to the constant map $F_A(a, 1) = r(F(a, 1)) = r(x_0)$. Thus, $A$ is contractible.

# Exercise 10
Show that a space $X$ is contractible iff every map $f\colon X \to Y$, for arbitrary $Y$, is nullhomotopic. Similarly, show $X$ is contractible iff every map $f\colon Y \to X$ is nullhomotopic.

Proof

Suppose $X$ is contractible, then there is a point $x_0$, and maps $`h\colon X \to\{x_0\}, g\colon\{x_0\} \to X`$ s.t. $`g h \simeq \mathbb{1}_X`$ and $`h g \simeq \mathbb{1}_{\{x_0\}}`$. Denote the homotopy as $F\colon X \times I \to X$ where $`F|_{X \times\{0\}}=\mathbb{1}_X`$ and $`F|_{X \times\{1\}}=g h`$.
1. For any $f\colon X \to Y$ where $Y$ is an arbitrary space, let $`y_0=f(g(x_0))`$, and let $G≔f F$. Thus $G\colon X \times I \to Y$ is continuous since it is the composition of two continuous maps $`G|_{X \times\{0\}}=f \mathbb{1}=f`$ and $`G|_{X \times\{1\}}=f g h`$. But $`f g h(X)=\{y_0\}`$. Therefore $f\colon X \to Y$ is nullhomotopic.

2. For any $f\colon Y \to X$ where $Y$ is an arbitrary space, define $G\colon Y \times I \to X,(y, t) \mapsto F(f(y), t)$. Hence $`G|_{Y \times\{0\}}=f`$ and $`G|_{Y \times\{1\}}=ghf`$. But $`ghf(Y)=\{g(x_0)\}`$. Thus, $f\colon Y \to X$ is nullhomotopic.

3. Conversely, if every map $f\colon Y \to X$ is nullhomotopic (for any $Y$), we can choose $Y=X$ and $f=\mathbb{1}_X\colon X \to X$. Then $\mathbb{1}_X$ is nullhomotopic, which by definition means $X$ is contractible. Similarly, if every map $f\colon X \to Y$ is nullhomotopic, we can choose $Y=X$ and $f=\mathbb{1}_X$, which again implies $X$ is contractible.

# Exercise 11
Show that $f\colon X \to Y$ is a homotopy equivalence if there exist maps $g, h\colon Y \to X$ such that $f g \simeq \mathbb{1}$ and $h f \simeq \mathbb{1}$. More generally, show that $f$ is a homotopy equivalence if $f g$ and $h f$ are homotopy equivalences.

Proof

1. To show that $g \simeq h$, we have $g = \mathbb{1}_X g \simeq (hf)g = h(fg) \simeq h\mathbb{1}_Y = h$. Thus $g \simeq h$. This implies $gf \simeq hf$. Since $hf \simeq \mathbb{1}_X$, we have $gf \simeq \mathbb{1}_X$. With the given $fg \simeq \mathbb{1}_Y$, this shows $f$ is a homotopy equivalence.

2. More generally, if $fg$ and $hf$ are homotopy equivalences, let $k\colon Y \to Y$ be a homotopy inverse for $fg$ and $l\colon X \to X$ be a homotopy inverse for $hf$. Define new maps $g' = gk\colon Y \to X$ and $h' = lh\colon Y \to X$. Then we have $fg' = f(gk) = (fg)k \simeq \mathbb{1}_Y$ and $h'f = (lh)f = l(hf) \simeq \mathbb{1}_X$. By part 1, using $g'$ and $h'$, it follows that $f$ is a homotopy equivalence.
