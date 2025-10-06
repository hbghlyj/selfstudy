# Section II.5

## Problem 2
If $G$ is a finite $p$-group, $H \triangleleft G$ and $H \neq\langle e\rangle$, then $H \cap C(G) \neq\langle e\rangle$.

## Problem 5
If $P$ is a normal Sylow $p$-subgroup of a finite group $G$ and $f: G \rightarrow G$ is an endomorphism, then $f(P)<P$.

## Problem 7
Find the Sylow 2-subgroups and Sylow 3-subgroups of $S_3, S_4, S_5$.

## Problem 8
If every Sylow $p$-subgroup of a finite group $G$ is normal for every prime $p$, then $G$ is the direct product of its Sylow subgroups.

## Problem 9
If $|G|=p^n q$, with $p>q$ primes, then $G$ contains a unique normal subgroup of index $q$.

---
# 1.
Let $G$ be a group and $H_1$ and $H_2$ be two subgroups. Construct bijections between the following sets:
- The quotient of $G / H_1$ by the action of $H_2$ (on the left);
- The quotient of $G / H_2$ by the action of $H_1$ (on the left);
- The quotient of $G$ by the action of $H_1 \times H_2$ with $H_1$ acting on the left and $H_2$ acting on the right (i.e., $H_1 \times H_2$ acts as a subgroup of $G \times G$ );
- The quotient of $\left(G / H_1\right) \times\left(G / H_2\right)$ with $G$ acting on two copies simultaneously (this is called the diagonal action).
(Going between definitions sometimes requires inverting elements of $g$.) The resulting set is the double quotient $H_1 \backslash G / H_2$; it can be interpreted as the set of double cosets $H_1 g H_2$.

# 2.
Fix $n$ and put $S_n$; for any $m \leq n$, let $H_m \subset S_n$ be the subgroup $S_m \times S_{n-m}$. The quotient $G / H_m$ can be identified with the set of $m$-element subsets of the set $\{1, \ldots, n\}$. (How?) Show that the double quotient $H_{m_1} \backslash S_n / H_{m_2}$ is a finite set with

$\min \left(m_1, m_2\right)-\max \left(0, m_1+m_2-n\right)+1$

elements. (Hint: the set counts the number of possible relative positions of two subsets of size $m_1$ and $m_2$.)

# 3. (A follow-up to II.5.9)
Suppose $G$ is a finite group, and that $p$ is the smallest prime factor of $|G|$. Show that any subgroup $H \subset G$ of index $p$ is normal. (One possible way to prove this: consider the action of $H$ on $G / H$, and notice that the trivial coset $H$ is a fixed point.)
