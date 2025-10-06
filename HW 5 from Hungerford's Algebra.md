# Section II.5

## Problem 2
If $G$ is a finite $p$-group, $H \triangleleft G$ and $H \neq\langle e\rangle$, then $H \cap C(G) \neq\langle e\rangle$.

## Problem 5
If $P$ is a normal Sylow $p$-subgroup of a finite group $G$ and $f\colon G \to G$ is an endomorphism, then $f(P)\leq P$.

Proof

Let $|G|=p^n m$ with $p \nmid m$.

For any endomorphism $f\colon G \to G$, we have that $|f(P)|$ divides $|P|$, so $|f(P)|=p^k$ for some $k \leq n$.

Thus, $f(P)$ is a $p$-subgroup of $G$.

By the Sylow theorems, $f(P)$ is contained in some Sylow $p$-subgroup of $G$. But since $P$ is the unique Sylow $p$-subgroup of $G$ (as it is normal), we have that $f(P) \leq P$.

## Problem 7
Find the Sylow 2-subgroups and Sylow 3-subgroups of $S_3, S_4, S_5$.

Proof

- For $S_3$, the Sylow 2-subgroups are $\langle(12)\rangle, \langle(13)\rangle, \langle(23)\rangle$ and the Sylow 3-subgroup is $\langle(123)\rangle$.
- For $S_4$, the Sylow 2-subgroups are isomorphic to the dihedral group $D_8$ and there are 3 such subgroups. The Sylow 3-subgroups are $\langle(123)\rangle, \langle(124)\rangle, \langle(134)\rangle, \langle(234)\rangle$.
- For $S_5$, the Sylow 2-subgroups are isomorphic to the dihedral group $D_8$ and there are 15 such subgroups. The Sylow 3-subgroups are isomorphic to $C_3$ and there are 10 such subgroups.

## Problem 8
If every Sylow $p$-subgroup of a finite group $G$ is normal for every prime $p$, then $G$ is the direct product of its Sylow subgroups.

Proof

Let $|G|=p_1^{n_1} p_2^{n_2} \cdots p_k^{n_k}$ be the prime factorization of $|G|$.

Since each Sylow $p_i$-subgroup $P_i$ is normal, it is the unique Sylow $p_i$-subgroup of $G$. Because the subgroups $P_j$ are normal with pairwise coprime orders, the product $P_1\cdots\hat{P_i}\cdots P_k$ is a subgroup whose order is $\prod_{j \neq i} |P_j|$. Since this order and $|P_i|$ are coprime, the intersection $P_i \cap (P_1\cdots\hat{P_i}\cdots P_k)$ must be trivial.

Now, consider the product subgroup $H = P_1 P_2 \cdots P_k$. Since the subgroups $P_i$ are normal and have pairwise coprime orders, the order of $H$ is the product of their orders: $|H| = |P_1|\cdots|P_k| = |G|$.

Thus, $G = P_1 P_2 \cdots P_k$.

Finally, we have shown $G = P_1 P_2 \cdots P_k$, each $P_i$ is normal, and $P_i \cap (P_1\cdots\hat{P_i}\cdots P_k) = \{e\}$ (since their orders are coprime). These are the conditions for $G$ to be the internal direct product of its Sylow subgroups, so $G \cong P_1 \times P_2 \times \cdots \times P_k$.

## Problem 9
If $|G|=p^n q$, with $p>q$ primes, then $G$ contains a unique normal subgroup of index $q$.

Proof

We are looking for a normal subgroup of index $q$. Such a subgroup would have order $|G|/q = p^n$, which is the order of a Sylow $p$-subgroup. Let's analyze the number of Sylow $p$-subgroups, $n_p$.

By Sylow's theorems, $n_p$ must divide $q$ and satisfy $n_p \equiv 1 \pmod p$. Since $q$ is prime, the only divisors of $q$ are 1 and $q$, so $n_p$ must be 1 or $q$.

Suppose $n_p = q$. Then $q \equiv 1 \pmod p$. This means $q = kp + 1$ for some integer $k \ge 1$. This implies $q > p$, which contradicts the given condition $p > q$.

Therefore, $n_p$ must be 1. This means there is a unique Sylow $p$-subgroup, $P$. A unique Sylow subgroup is always normal in $G$. The index of $P$ is $|G|/|P| = (p^n q) / p^n = q$.

Thus, $G$ has a unique normal subgroup of index $q$.

---
## 1.
Let $G$ be a group and $H_1$ and $H_2$ be two subgroups. Construct bijections between the following sets:
- The quotient of $G / H_1$ by the action of $H_2$ (on the left);
- The quotient of $G / H_2$ by the action of $H_1$ (on the left);
- The quotient of $G$ by the action of $H_1 \times H_2$ with $H_1$ acting on the left and $H_2$ acting on the right (i.e., $H_1 \times H_2$ acts as a subgroup of $G \times G$);
- The quotient of $(G / H_1) \times(G / H_2)$ with $G$ acting on two copies simultaneously (this is called the diagonal action).
(Going between definitions sometimes requires inverting elements of $g$.) The resulting set is the double quotient $H_1⧹G / H_2$; it can be interpreted as the set of double cosets $H_1 g H_2$.

## 2.
Fix $n$ and put $S_n$; for any $m ≤ n$, let $H_m ⊂ S_n$ be the subgroup $S_m \times S_{n-m}$. The quotient $S_n / H_m$ can be identified with the set of $m$-element subsets of the set $`\{1, …, n\}`$. (How?) Show that the double quotient $H_{m_1}⧹S_n / H_{m_2}$ is a finite set with

$\min (m_1, m_2)-\max (0, m_1+m_2-n)+1$

elements. (Hint: the set counts the number of possible relative positions of two subsets of size $m_1$ and $m_2$.)

## 3. (A follow-up to II.5.9)
Suppose $G$ is a finite group, and that $p$ is the smallest prime factor of $|G|$. Show that any subgroup $H \subset G$ of index $p$ is normal. (One possible way to prove this: consider the action of $H$ on $G / H$, and notice that the trivial coset $H$ is a fixed point.)
