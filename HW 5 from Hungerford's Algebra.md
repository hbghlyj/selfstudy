# Section II.5

## Problem 2
If $G$ is a finite $p$-group, $H \triangleleft G$ and $H \neq\langle e\rangle$, then $H \cap C(G) \neq\langle e\rangle$.

Proof

Let $|G|=p^n$ for some $n \geq 1$. Since $H \triangleleft G$ and $H \neq\langle e\rangle$, we have $|H|=p^k$ for some $k \geq 1$.

Consider the action of $G$ on $H$ by conjugation. The orbit-stabilizer theorem tells us that for any $h \in H$, the size of the orbit of $h$ under this action is equal to the index of the stabilizer of $h$ in $G$. Since $H$ is normal, the orbits are contained in $H$.

The size of each orbit divides $|G|=p^n$, so the size of each orbit is a power of $p$. The class equation for this action is:

$`|H| = |H\cap C(G)| + \sum_{i} |O_i|,`$

where $O_i$ are the nontrivial orbits.

Since $|H|=p^k$ is divisible by $p$ and each $|O_i|$ is divisible by $p$, it follows from the class equation that $|H \cap C(G)|$ is divisible by $p$. As $H \cap C(G)$ is a subgroup, its order is at least 1. Therefore, $|H \cap C(G)| \ge p$, so $H \cap C(G) \neq\langle e\rangle$.

## Problem 5
If $P$ is a normal Sylow $p$-subgroup of a finite group $G$ and $f\colon G \to G$ is an endomorphism, then $f(P)\leq P$.

Proof

Let $|G|=p^n m$ with $p \nmid m$.

For any endomorphism $f\colon G \to G$, by the First Isomorphism Theorem, $f(P)\cong P/\ker(f|_P)$. It follows that $|f(P)|$ divides $|P|$, so $|f(P)|=p^k$ for some $k \leq n$.

Thus, $f(P)$ is a $p$-subgroup of $G$.

By the Sylow theorems, $f(P)$ is contained in some Sylow $p$-subgroup of $G$. But since $P$ is the unique Sylow $p$-subgroup of $G$ (as it is normal), we have that $f(P) \leq P$.

## Problem 7
Find the Sylow 2-subgroups and Sylow 3-subgroups of $S_3, S_4, S_5$.

Proof

By the Sylow theorems, all Sylow $p$-subgroups of $S_n$ are conjugate, and therefore have the same cycle structure.

- For $S_3$, the Sylow 2-subgroups are $\langle(12)\rangle, \langle(13)\rangle, \langle(23)\rangle$ and the Sylow 3-subgroup is $\langle(123)\rangle$.
- For $S_4$, the Sylow 2-subgroups are isomorphic to the dihedral group $D_8$ and there are 3 such subgroups:
  1. Stabilizer of \{\{1,2\}, \{3,4\}\}
  2. Stabilizer of \{\{1,3\}, \{2,4\}\}
  3. Stabilizer of \{\{1,4\}, \{2,3\}\}
  
  The Sylow 3-subgroups are $\langle(123)\rangle, \langle(124)\rangle, \langle(134)\rangle, \langle(234)\rangle$.
- For $S_5$, the Sylow 2-subgroups are isomorphic to the dihedral group $D_8$. There are 15 such subgroups, which are the stabilizers of partitions of the set $\{1, \dots, 5\}$ into two pairs and a singleton:
    1. Stabilizer of \{\{1,2\}, \{3,4\}, \{5\}\}
    2. Stabilizer of \{\{1,3\}, \{2,4\}, \{5\}\}
    3. Stabilizer of \{\{1,4\}, \{2,3\}, \{5\}\}
    4. Stabilizer of \{\{1,2\}, \{3,5\}, \{4\}\}
    5. Stabilizer of \{\{1,3\}, \{2,5\}, \{4\}\}
    6. Stabilizer of \{\{1,5\}, \{2,3\}, \{4\}\}
    7. Stabilizer of \{\{1,4\}, \{2,5\}, \{3\}\}
    8. Stabilizer of \{\{1,5\}, \{2,4\}, \{3\}\}
    9. Stabilizer of \{\{1,2\}, \{4,5\}, \{3\}\}
    10. Stabilizer of \{\{1,3\}, \{4,5\}, \{2\}\}
    11. Stabilizer of \{\{1,4\}, \{3,5\}, \{2\}\}
    12. Stabilizer of \{\{1,5\}, \{3,4\}, \{2\}\}
    13. Stabilizer of \{\{2,3\}, \{4,5\}, \{1\}\}
    14. Stabilizer of \{\{2,4\}, \{3,5\}, \{1\}\}
    15. Stabilizer of \{\{2,5\}, \{3,4\}, \{1\}\}
    
    The Sylow 3-subgroups are isomorphic to $C_3$ and there are 10 such subgroups:
    1. $\langle(123)\rangle$
    2. $\langle(124)\rangle$
    3. $\langle(125)\rangle$
    4. $\langle(134)\rangle$
    5. $\langle(135)\rangle$
    6. $\langle(145)\rangle$
    7. $\langle(234)\rangle$
    8. $\langle(235)\rangle$
    9. $\langle(245)\rangle$
    10. $\langle(345)\rangle$

## Problem 8
If every Sylow $p$-subgroup of a finite group $G$ is normal for every prime $p$, then $G$ is the direct product of its Sylow subgroups.

Proof

Let $|G|=p_1^{n_1} p_2^{n_2} \cdots p_k^{n_k}$ be the prime factorization of $|G|$.

Since each Sylow $p_i$-subgroup $P_i$ is normal, it is the unique Sylow $p_i$-subgroup of $G$. Because the subgroups $P_j$ are normal with pairwise coprime orders, the product $P_1\cdots\hat{P_i}\cdots P_k$ is a subgroup whose order is $\prod_{j \neq i} |P_j|$. Since this order and $|P_i|$ are coprime, the intersection $P_i \cap (P_1\cdots\hat{P_i}\cdots P_k)$ must be trivial.

Now, consider the product subgroup $H = P_1 P_2 \cdots P_k$. Since the subgroups $P_i$ are normal and have pairwise coprime orders, the order of $H$ is the product of their orders: $|H| = |P_1|\cdots|P_k| = |G|$.

Thus, $G = P_1 P_2 \cdots P_k$.

Finally, we have shown $G = P_1 P_2 \cdots P_k$, each $P_i$ is normal, and $P_i \cap (P_1\cdots\hat{P_i}\cdots P_k) = \langle e\rangle$ (since their orders are coprime). These are the conditions for $G$ to be the internal direct product of its Sylow subgroups, so $G \cong P_1 \times P_2 \times \cdots \times P_k$.

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
1. The quotient of $G / H_1$ by the action of $H_2$ (on the left);
2. The quotient of $G / H_2$ by the action of $H_1$ (on the left);
3. The quotient of $G$ by the action of $H_1 \times H_2$ with $H_1$ acting on the left and $H_2$ acting on the right (i.e., $H_1 \times H_2$ acts as a subgroup of $G \times G$);
4. The quotient of $(G / H_1) \times(G / H_2)$ with $G$ acting on two copies simultaneously (this is called the diagonal action).
(Going between definitions sometimes requires inverting elements of $g$.) The resulting set is the double quotient $H_1⧹G / H_2$; it can be interpreted as the set of double cosets $H_1 g H_2$.

Proof

There is a natural bijection between $H_1⧹G/H_2$ and $H_2⧹G/H_1$ via the map $H_1 g H_2 \mapsto H_2 g^{-1} H_1$. This provides a bijection between sets (1) and (2).

To prove that set (2), which is $H_1⧹(G/H_2)$, the set of orbits of left cosets of $H_2$ under the left action of $H_1$, is bijective to set (3), the set of double cosets $H_1 g H_2$, define a map $f: H_1⧹(G/H_2) \to H_1⧹G/H_2$ by $f(H_1(gH_2)) = H_1 g H_2$. Here, $H_1(gH_2)$ denotes the orbit of the coset $gH_2$ under the action of $H_1$.

*   **Well-defined:** Suppose we have two representatives for the same orbit, i.e., $H_1(gH_2) = H_1(g'H_2)$. This means $g'H_2$ is in the orbit of $gH_2$, so there exists an $h_1 \in H_1$ such that $g'H_2 = h_1(gH_2) = (h_1g)H_2$. This implies $g' = h_1 g h_2$ for some $h_2 \in H_2$. We must show that $f(H_1(gH_2)) = f(H_1(g'H_2))$.
    Let's compute the image of the orbit represented by $g'$:
    $f(H_1(g'H_2)) = H_1 g' H_2 = H_1 (h_1 g h_2) H_2$.
    Since $h_1 \in H_1$ and $h_2 \in H_2$, we have $H_1 h_1 = H_1$ and $h_2 H_2 = H_2$.
    Thus, $H_1 (h_1 g h_2) H_2 = H_1 g H_2 = f(H_1(gH_2))$.
    The map $f$ is well-defined.

*   **Injective:** Suppose $f(H_1(gH_2)) = f(H_1(g'H_2))$. This means $H_1 g H_2 = H_1 g' H_2$.
    This equality implies that $g' \in H_1 g H_2$, so $g' = h_1 g h_2$ for some $h_1 \in H_1$ and $h_2 \in H_2$.
    We need to show that the orbits are the same: $H_1(gH_2) = H_1(g'H_2)$.
    The orbit of $g'H_2$ is $H_1(g'H_2) = H_1((h_1 g h_2)H_2)$. Since $h_2 H_2 = H_2$, this is $H_1((h_1 g)H_2)$.
    An element in this orbit has the form $h'_1(h_1 g)H_2 = (h'_1 h_1)g H_2$ for some $h'_1 \in H_1$. Since $h'_1 h_1 \in H_1$, this element is also in the orbit $H_1(gH_2)$. Thus, $H_1(g'H_2) \subseteq H_1(gH_2)$.
    By a symmetric argument (starting with $g = h_1^{-1}g'h_2^{-1}$), we get $H_1(gH_2) \subseteq H_1(g'H_2)$.
    Therefore, $H_1(gH_2) = H_1(g'H_2)$, and $f$ is injective.

*   **Surjective:** For any double coset $H_1 g H_2$ in the codomain, consider the orbit $H_1(gH_2)$ in the domain. Its image under $f$ is $f(H_1(gH_2)) = H_1 g H_2$. Thus, every element in the codomain has a preimage, and $f$ is surjective.

Since $f$ is a bijection, the set of orbits $H_1⧹(G/H_2)$ is in one-to-one correspondence with the set of double cosets $H_1⧹G/H_2$.

To prove a bijection between set (3) and set (4), we define a map from set (4) to set (3): $\phi(\text{Orbit}(g_1H_1,g_2H_2)) = H_1 g_1^{-1} g_2 H_2$.

*   **Well-defined:** Suppose we have two representatives for the same orbit, i.e., $\text{Orbit}(g_1H_1,g_2H_2) = \text{Orbit}(g'_1H_1,g'_2H_2)$. This means there exists a $g \in G$ such that $(g g_1 H_1, g g_2 H_2) = (g'_1 H_1, g'_2 H_2)$. This implies $g'_1 = g g_1 h_1$ for some $h_1 \in H_1$ and $g'_2 = g g_2 h_2$ for some $h_2 \in H_2$. We must show that $\phi(\text{Orbit}(g_1H_1,g_2H_2)) = \phi(\text{Orbit}(g'_1H_1,g'_2H_2))$.

    $`\phi(\text{Orbit}(g'_1H_1,g'_2H_2)) = H_1 (g'_1)^{-1} g'_2 H_2 = H_1 (g g_1 h_1)^{-1} (g g_2 h_2) H_2 = H_1 (h_1^{-1} g_1^{-1} g^{-1})(g g_2 h_2) H_2`$

    Since $h_1^{-1} \in H_1$ and $h_2 \in H_2$, we have $H_1 h_1^{-1} = H_1$ and $h_2 H_2 = H_2$.

*   **Injective:** Suppose $\phi(\text{Orbit}(g_1H_1,g_2H_2)) = \phi(\text{Orbit}(g'_1H_1,g'_2H_2))$. This means $H_1 g_1^{-1} g_2 H_2 = H_1 g'^{-1}_1 g'_2 H_2$.

    This equality implies that $g'^{-1}_1 g'_2 = h_1 (g_1^{-1} g_2) h_2$ for some $h_1 \in H_1$ and $h_2 \in H_2$. We need to show that the orbits are the same: $\text{Orbit}(g_1H_1,g_2H_2) = \text{Orbit}(g'_1H_1,g'_2H_2)$.

    To do this, we show that $(g'_1H_1, g'_2H_2)$ is in the orbit of $(g_1H_1, g_2H_2)$. This requires finding a $g \in G$ such that $g'_1H_1 = g g_1 H_1$ and $g'_2H_2 = g g_2 H_2$.

    From the assumption, we can write $g'_2 = g'_1 h_1 g_1^{-1} g_2 h_2$. Let $g = g'_1 h_1 g_1^{-1}$.
    
    Then $g g_1 H_1 = (g'_1 h_1 g_1^{-1}) g_1 H_1 = g'_1 h_1 H_1 = g'_1 H_1$.
    Also, using $g'_1 h_1 g_1^{-1} g_2 = g'_2 h_2^{-1}$, we have $g g_2 H_2 = (g'_1 h_1 g_1^{-1}) g_2 H_2 = (g'_2 h_2^{-1}) H_2 = g'_2 H_2$.

    Since such a $g$ exists, $(g'_1H_1, g'_2H_2)$ is in the orbit of $(g_1H_1, g_2H_2)$. Because orbits that share an element are identical, the two orbits are equal, and $\phi$ is injective.
*   **Surjective:** For any double coset $H_1 g H_2$, consider the orbit $\text{Orbit}(H_1, gH_2)$. Its image under $\phi$ is $\phi(\text{Orbit}(H_1, gH_2)) = H_1 e^{-1} g H_2 = H_1 g H_2$. Thus, $\phi$ is surjective.

## 2.
Fix $n$ and put $S_n$; for any $m ≤ n$, let $H_m ⊂ S_n$ be the subgroup $S_m \times S_{n-m}$. The quotient $S_n / H_m$ can be identified with the set of $m$-element subsets of the set $`\{1, …, n\}`$. (How?) Show that the double quotient $H_{m_1}⧹S_n / H_{m_2}$ is a finite set with

$\min (m_1, m_2)-\max (0, m_1+m_2-n)+1$

elements. (Hint: the set counts the number of possible relative positions of two subsets of size $m_1$ and $m_2$.)

Proof

To show the identification of the quotient $S_n / H_m$ with the set of $m$-element subsets of $`\{1, \ldots, n\}`$, we can use the Orbit-Stabilizer Theorem. Consider the natural action of $S_n$ on the set of all $m$-element subsets of $`\{1, \ldots, n\}`$. The subgroup $H_m = S_m \times S_{n-m}$ is precisely the stabilizer of the specific subset $`\{1, \ldots, m\}`$. The orbit of this subset under the action of $S_n$ is the set of all $m$-element subsets, as the action is transitive. By the Orbit-Stabilizer Theorem, there is a natural bijection between the set of left cosets of the stabilizer, $S_n / H_m$, and the orbit. This establishes the desired identification, where a coset $\sigma H_m$ is mapped to the subset $`\sigma(\{1, \ldots, m\})`$.

Now, we need to determine the number of elements in the double quotient $H_{m_1}⧹S_n / H_{m_2}$. This double quotient can be interpreted as the set of orbits of the action of $H_{m_1}$ on the set of $m_2$-element subsets of $`\{1, \ldots, n\}`$. Two $m_2$-element subsets are in the same orbit under this action if one can be transformed into the other by a permutation that only rearranges the first $m_1$ elements and the last $n - m_1$ elements separately. The invariant that characterizes these orbits is the size of the intersection of an $m_2$-element subset with the specific subset $`\{1, \ldots, m_1\}`$ stabilized by $H_{m_1}$.


## 3. (A follow-up to II.5.9)
Suppose $G$ is a finite group, and that $p$ is the smallest prime factor of $|G|$. Show that any subgroup $H \subset G$ of index $p$ is normal. (One possible way to prove this: consider the action of $H$ on $G / H$, and notice that the trivial coset $H$ is a fixed point.)

Proof

Consider the action of $H$ on the set of left cosets $G/H$ by left multiplication. The class equation for this action is:

$`|G/H| = |(G/H)^H| + \sum_{i} |O_i|,`$

where $|G/H|=p$, $(G/H)^H$ is the set of fixed points, and $O_i$ are non-trivial orbits.

The size of any orbit $|O_i|$ must divide $|H|$. Since $p$ is the smallest prime factor of $|G| = |H| \cdot p$, any prime factor of $|H|$ is $\ge p$. Thus, if $|O_i|>1$, then $|O_i| \ge p$. The coset $H$ is a fixed point, so $|(G/H)^H| \ge 1$. If there were any non-trivial orbit, the class equation $p = |(G/H)^H| + \sum |O_i|$ would lead to $p \ge 1 + p$, a contradiction. Therefore, all orbits must be of size 1, meaning all cosets are fixed points. This implies that for any $g \in G$, $g^{-1}Hg \subseteq H$, so $H$ is normal in $G$.
