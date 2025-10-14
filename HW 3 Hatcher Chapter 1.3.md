# 3
Let $p: \tilde{X} \to X$ be a covering space with $p^{-1}(x)$ finite and nonempty for all $x \in X$.

Show that $\tilde{X}$ is compact Hausdorff iff $X$ is compact Hausdorff.

Proof

* **($\Rightarrow$)** Suppose $\tilde{X}$ is compact Hausdorff. Since $p$ is a continuous surjection, $X$ is compact as the continuous image of a compact space. To show that $X$ is Hausdorff, let $x_1, x_2 \in X$ be distinct points. Since $\tilde{X}$ is Hausdorff, for each pair of points $`\tilde{x}_1 \in p^{-1}(x_1)`$ and $`\tilde{x}_2 \in p^{-1}(x_2)`$, there exist disjoint open neighborhoods $`U_{\tilde{x}_1}`$ and $`U_{\tilde{x}_2}`$ in $\tilde{X}$. The sets $`p(U_{\tilde{x}_1})`$ and $`p(U_{\tilde{x}_2})`$ are open in $X$ and contain $x_1$ and $x_2$, respectively. Since $p^{-1}(x_1)$ and $p^{-1}(x_2)$ are finite, we can take the finite intersection of these neighborhoods to obtain disjoint open neighborhoods of $x_1$ and $x_2$. Thus, $X$ is Hausdorff.

* **($\Leftarrow$)** Conversely, suppose $X$ is compact Hausdorff. First, we show $\tilde{X}$ is Hausdorff. Let $\tilde{x}_1, \tilde{x}_2 \in \tilde{X}$ be distinct points. If $p(\tilde{x}_1) \neq p(\tilde{x}_2)$, since $X$ is Hausdorff, their images have disjoint open neighborhoods $U_1, U_2$. Then $p^{-1}(U_1)$ and $p^{-1}(U_2)$ are disjoint open neighborhoods of $\tilde{x}_1$ and $\tilde{x}_2$. If $p(\tilde{x}_1) = p(\tilde{x}_2)$, they lie in distinct sheets over an evenly covered neighborhood of their image, which provides disjoint neighborhoods. Thus $\tilde{X}$ is Hausdorff. Next, to show $\tilde{X}$ is compact, we use the fact that $p^{-1}$ is continuous. As $X$ is compact, $\tilde{X} = p^{-1}(X)$ is therefore compact.

# 4
Construct a simply-connected covering space of the space $X \subset \mathbb{R}^3$ that is the union of a sphere and a diameter.

Do the same when $X$ is the union of a sphere and a circle intersecting it in two points.

Solution

Consider $\tilde{X}$ which consists of infinitely many copies of $S^2$, stacked vertically in a line, with the south pole of one connected to the north pole of the previous.

The space $\tilde{X}$ is simply-connected because any loop within it is contained in a finite chain of spheres, which is a simply-connected subspace.

![](https://i.upmath.me/svgb/hZNBi9swEIXv_hVz2ILdxCYJhB4CC6U59tZTqfagSON4WHvkynJCavzfi6SEON7A3qxB75uZ5ydxwCPx4Oj9X0vK9RbHBOAL7LEkRnAVAvfNAS2YErq2QotdAiA0loL75lesDNsPqhNaR0rWoKlzkhXCAd0ZkeeUeNxT54bNmATMT2NacAa0lecAu0pAsgZlmFE54iPUxJFTGotSVSAIiGFYL4uiWE7mG2FIADz6h6xVX0sXh7zkyhiriX2hNDYUFbKL-95bB7Voj2UjXdWha6SyZhCXcUgF5evsaz7ZY7z22j-OHxlhp3S1BHHJQJFVNUK6KrbZbq7Cv710xk5l-arYRmVReCOcNXUXyptQ9x9ZcCl9LBVFaBK0uzvxj5Zdhfrtc_LiI3nxhDzfYf6z4EyuAmmtOXdxDCq5bwS9rsPxmcmtxdPvaPTmmdG3XfLXJbiK1Pvb1d-FtxXyPB4DJr87LUpKAK6J-641aOM6nzpiTeqWEOKSmBwCS_84bqlQlST2yWOjEaQLLVbFt20Gw4s4edTLuJtfGPJ0Ekofm8kykAfA-EgQyPrhdf4H)

The covering projection $p: \tilde{X} \to X$ can be defined by mapping each sphere $S_n$ in $\tilde{X}$ to the sphere in $X$ with an alternating orientation. For spheres $S_n$ with even $n$, the map is orientation-preserving, sending the north and south poles of $S_n$ to the north and south poles of $X$, respectively. For spheres $S_n$ with odd $n$, the map is orientation-reversing, sending the north pole of $S_n$ to the south pole of $X$ and the south pole of $S_n$ to the north pole of $X$. This ensures the map is well-defined on the identified poles.

To see that $p$ is a covering map, note that for any point $x$ in $S^2$ that is not the north or south pole, there exists an open neighborhood $U$ of $x$ in $S^2$ such that $p^{-1}(U)$ is a disjoint union of open sets in $\tilde{X}$, each of which is homeomorphic to $U$. For the north and south poles, we can take small neighborhoods around them that do not include the other pole of $S^2$, and similarly, their preimages in $\tilde{X}$ will be a disjoint union of open sets homeomorphic to these neighborhoods. Thus, $p$ satisfies the definition of a covering map.

For the second part of the problem (a sphere and a circle intersecting it in two points), take the universal cover of $S^1 \vee S^1$ (an infinite 4-valent tree) and attach a sphere to each vertex.

![](https://i.upmath.me/svgb/rZbfb9s2EMff9VfcugSzF0mVtBnb4vlhaDCgQIoCbd-iYKDJU0SEIj2SspcI-t8HkrZ-JOm6FfOTeOTdfb53R8lla9Dy-0fBt5roh44SQfsoKrd4x2Xndnac2lZjfxMBAJhdjRr_0ITx1rxOjVUagctNGTaCPX5-dJOlxYo20x3n_SBw03mb-1GuqcB4WDNNDuOq4kJstqLFb4pstDZc8qZtwPBH3BTfv8DhflxK1GBwt8l21lv76DaKzuEdoVqBVT4X2BqPcHDgtgb8syVW6aiUeKCqaYhkXelOhkP9TX4b6L0RFt_my6MIWMxIlmt_7ByuTmlOoSfeZ97_AhbJXEW2PFtCmgJV0molzPRklq6eaE6y9Me5ybkTySZu_9YrTSdOz6HWI_0NI6ZGdvt_qfgqEV-noXdzkCQJfERrubwzUCkNjBtLJEUDxAISWoPAPQp3MCoZVqVfvpd4xY3tinTVT8yfDsqb87RYDeE_KGXhY5guH0UqhjcB6BYWWim7dMkWWZwtoevX0WTUOredUpQWdb8-hbz2SLkvTHguQuhKac9c7ohGaX-Td8JdU-iyGH7JYsh_zmIofsp6OM7vnOU6DyRT98uZ4gA4tP8IeZ2PiONo7FE_gK05vR9kJolPso7CsQF3q4mk9YibOFjPfCL156lSmnFJLMLiukj8MhCfefaLOfrFNO7lrEXDFL9UhSLEHDOcND_TXcx1f0a7Q_PKi0nS4eEcflc6jNorgaR6FQgcUwyEMWDKGlcVbg38AKq1B6IZMK6RWq6kGVMP9WTKfqmY3mF3VzXE1gZt416IXVlxScTV0bvvPlvNiyFFP484bRFTNtkpM3SoCB2a5bjM0pVvxizM6eZsW2OB1kjv_eXco7acEgF7k0KtNH9U0pJwOefub4igrXAUVBkuEVTlX7_E5UzhbQXcfmdAItHwiFrFfneoKXAzJEu_UDKLxr5Rpu_I1iyoMk8ELpdPKsQrxpuTF-ws_ApZmsPx-_RERoDnR9IsBqMCORmLMVA_C-AH21d_aEVXasIN5mmBf5V7N1qT2fU-KAz-M4qyL-BM2vEfgcRLFBUf1v3xw91HJUo2-3PyNw)

The covering map takes each sphere onto the sphere in $X$, and the line segments onto the two arcs of the circle in $X$. This is a covering space for reasons analogous to the previous example. Moreover, the space is simply connected since contracting the line segments yields an infinite wedge of spheres. 

# 8
Let $\tilde{X}$ and $\tilde{Y}$ be simply-connected covering spaces of the path-connected, locally path-connected spaces $X$ and $Y$.

Show that if $X \simeq Y$ then $\tilde{X} \simeq \tilde{Y}$. [Exercise 11 in Chapter 0 may be helpful.]
 
# 12
Let $a$ and $b$ be the generators of $\pi_1(S^1 \vee S^1)$ corresponding to the two $S^1$ summands.

Draw a picture of the covering space of $S^1 \vee S^1$ corresponding to the normal subgroup generated by $a^2, b^2$, and $(a b)^4$, and prove that this covering space is indeed the correct one.

# 17
Given a group $G$ and a normal subgroup $N$, show that there exists a normal covering space $\tilde{X} \to X$ with $\pi_1(X) \cong G, \pi_1(\tilde{X}) \cong N$, and deck transformation group $G(\tilde{X}) \cong G / N$.

Proof

By Corollary 1.28, there exists a 2-dimensional cell complex $X$ with $\pi_1(X) \cong G$. As a cell complex, $X$ is path-connected, locally path-connected, and semilocally simply-connected. We can therefore apply Proposition 1.36, which guarantees a covering space $p: \tilde{X} \to X$ such that $p_*(\pi_1(\tilde{X})) = N$. For any covering space, the induced homomorphism $p_*$ is injective, so $\pi_1(\tilde{X}) \cong N$. Since $N$ is a normal subgroup of $G$, Proposition 1.39 implies the covering is normal and the deck transformation group $G(\tilde{X})$ is isomorphic to the quotient group $G/N$.

# 18
For a path-connected, locally path-connected, and semilocally simply-connected space $X$, call a path-connected covering space $\tilde{X} \to X$ abelian if it is normal and has abelian deck transformation group.

Show that $X$ has an abelian covering space that is a covering space of every other abelian covering space of $X$, and that such a 'universal' abelian covering space is unique up to isomorphism. Describe this covering space explicitly for $X=S^1 \vee S^1$ and $X=S^1 \vee S^1 \vee S^1$.

Proof

Since the space $X$ is path-connected, locally path-connected, and semilocally simply-connected, there exists a universal covering space $X_0 \to X$.

Let $[\pi_1(X), \pi_1(X)]$ be the commutator subgroup of $\pi_1(X)$. This is a normal subgroup.

By Proposition 1.36, there is a covering space $p: \tilde{X} \to X$ such that $p_*(\pi_1(\tilde{X}))=[\pi_1(X), \pi_1(X)]$.

Since the subgroup is normal, by Proposition 1.39, this covering is normal and its deck transformation group is $G(\tilde{X}) \cong \pi_1(X) / [\pi_1(X), \pi_1(X)]$, which is the abelianization of $\pi_1(X)$.

Thus, $\tilde{X}$ is an abelian covering space.

To show that $\tilde{X}$ is universal, let $p': X' \to X$ be any other path-connected abelian covering space.

Its deck transformation group $`G(X') \cong \pi_1(X) / p'_*(\pi_1(X'))`$ is abelian.

This implies that the subgroup $`p'_*(\pi_1(X'))`$ must contain the commutator subgroup $`[\pi_1(X), \pi_1(X)]`$.

We have $p_*(\pi_1(\tilde{X})) = [\pi_1(X), \pi_1(X)] \subset p'_*(\pi_1(X'))$.

By the lifting criterion (Proposition 1.34), there is a covering map $q: \tilde{X} \to X'$ such that $p' \circ q = p$.

This shows that $\tilde{X}$ is a covering space of $X'$, and is therefore universal. Uniqueness up to isomorphism is a standard result for such universal objects.

* **For $X=S^1 \vee S^1$:**
  The fundamental group is $\pi_1(X) \cong F_2$, the free group on two generators. The universal abelian cover is the covering space corresponding to the commutator subgroup $`[F_2, F_2]`$. The deck transformation group is $`F_2/[F_2, F_2] \cong \mathbb{Z}^2`$. The covering space itself is the Cayley graph of $\mathbb{Z}^2$, which is the infinite grid of points $(m,n) \in \mathbb{Z}^2$ in the plane, with edges connecting adjacent integer points.
* **For $X=S^1 \vee S^1 \vee S^1$:**
  Similarly, $\pi_1(X) \cong F_3$. The universal abelian cover corresponds to the subgroup $`[F_3, F_3]`$ and has deck transformation group $`F_3/[F_3, F_3] \cong \mathbb{Z}^3`$. The covering space is the Cayley graph of $\mathbb{Z}^3$, which is the 3D integer lattice.

# 19
Use the preceding problem to show that a closed orientable surface $M_g$ of genus $g$ has a connected normal covering space with deck transformation group isomorphic to $\mathbb{Z}^n$ (the product of $n$ copies of $\mathbb{Z}$) iff $n \leq 2 g$.

For $n=3$ and $g \geq 3$, describe such a covering space explicitly as a subspace of $\mathbb{R}^3$ with translations of $\mathbb{R}^3$ as deck transformations.

Show that such a covering space in $\mathbb{R}^3$ exists iff there is an embedding of $M_g$ in the 3-torus $T^3=S^1 \times S^1 \times S^1$ such that the induced map $\pi_1\left(M_g\right) \to \pi_1\left(T^3\right)$ is surjective.

# 23
Show that if a group $G$ acts freely and properly discontinuously on a Hausdorff space $X$, then the action is a covering space action. (Here 'properly discontinuously' means that each $x \in X$ has a neighborhood $U$ such that $`\{g \in G \mid U \cap g(U) \neq \varnothing\}`$ is finite.)

In particular, a free action of a finite group on a Hausdorff space is a covering space action.

# 27
For a universal cover $p: \tilde{X} \to X$ there are two actions of $\pi_1\left(X, x_0\right)$ on the fiber $p^{-1}\left(x_0\right)$. The first is the action defined on page 69 in which the element of $\pi_1\left(X, x_0\right)$ determined by a loop $\gamma$ sends $\tilde{\gamma}(1)$ to $\tilde{\gamma}(0)$ for each lift $\tilde{\gamma}$ of $\gamma$ to $\tilde{X}$, and the second is the action given by restricting deck transformations to the fiber (see Proposition 1.39). Show that these two actions are different when $X=S^1 \vee S^1$ and when $X=S^1 \times S^1$ and determine when the two actions are the same. [This is a revised version of the original form of this exercise.]

# 30
Draw the Cayley graph of the group $\mathbb{Z} * \mathbb{Z}_2=\langle a, b \mid b^2\rangle$.
