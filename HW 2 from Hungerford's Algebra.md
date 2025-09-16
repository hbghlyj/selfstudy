# Section I.5
## Exercise 14
If $N_1 \triangleleft G_1, N_2 \triangleleft G_2$ then $(N_1 \times N_2) \triangleleft(G_1 \times G_2)$ and $(G_1 \times G_2) /(N_1 \times N_2) \cong(G_1 / N_1) \times(G_2 / N_2)$.

Proof

For all $(g_1,g_2)\in G_1\times G_2$, for all $(n_1,n_2)\in N_1\times N_2$ we have $(g_1,g_2)(n_1,n_2)(g_1,g_2)^{-1}=(g_1n_1g_1^{-1},g_2n_2g_2^{-1})\in N_1\times N_2$

To complete the proof, use the First Isomorphism Theorem.

Consider the homomorphism $G_1 \times G_2 \to G_1/N_1,(g_1,g_2)\mapsto g_1N_1$ and the homomorphism $G_1 \times G_2 \to G_1/N_1,(g_1,g_2)\mapsto g_2N_2$.

By Universal Mapping Property we get a homomorphism $\phi: G_1 \times G_2 \to (G_1/N_1) \times (G_2/N_2)$.

Then $(g_1,g_2)\in\ker\phi\iff g_1N_1=N_1\land g_2N_2=N_2\iff g_1\in N_1\land g_2\in N_2$.

So $\ker\phi=N_1\times N_2$.

# Section I.6
## Exercise 11
Find all normal subgroups of $D_n$.

Solution

The conjugacy classes of $D_n$ are:
- $`\{e\}`$.
- $`\{r^k, r^{-k}\}`$ for $1 \leq k < n/2$.
- $`\{r^{n/2}\}`$ if $n$ is even.
- $`\{s r^{2k} : 0 \leq k < n/2\}`$ if $n$ is even.
- $`\{s r^{2k+1} : 0 \leq k < n/2\}`$ if $n$ is even.
- $`\{s r^k : 0 \leq k < n\}`$ if $n$ is odd.

Any normal subgroup must be a union of conjugacy classes.

The normal subgroups of $D_n$ are:

1.  Subgroups of $\langle r \rangle$: $\langle r^d \rangle$ for any divisor $d$ of $n$.
2.  If $n$ is even, the subgroups $\langle r^2, s \rangle$ and $\langle r^2, rs \rangle$ are also normal.


# Section I.8
## Exercise 2
If $f: A \to B$ is an equivalence in a category $\mathcal{C}$ and $g: B \to A$ is the morphism such that $g \circ f=1_A, f \circ g=1_B$, show that $g$ is unique.

Proof

Suppose there is another morphism $g': B \to A$ such that $g' \circ f=1_A$ and $f \circ g'=1_B$. Then we have:

$g' = g' \circ 1_B = g' \circ (f \circ g) = (g' \circ f) \circ g = 1_A \circ g = g$

Thus, $g$ is unique.

## Exercise 3
Let $G$ be an (additive) abelian group with subgroups $H$ and $K$. Show that $G \cong H \oplus K$ if and only if there are homomorphisms $H \overunderset{\pi_1}{\iota_1}{\leftrightarrows} G \overunderset{\pi_2}{\iota_2}{\rightleftarrows} K$ such that $\pi_1 \iota_1=1_H, \pi_2 \iota_2=1_K, \pi_1 \iota_2=0$ and $\pi_2 \iota_1=0$, where 0 is the map sending every element onto the zero (identity) element, and $\iota_1 \pi_1(x)+\iota_2 \pi_2(x)=x$ for all $x \in G$.

Proof

## Exercise 5
Let $G, H$ be finite cyclic groups. Then $G \times H$ is cyclic if and only if $(|G|,|H|)=1$.

Proof

## Exercise 9
If a group $G$ is the (internal) direct product of its subgroups $H, K$, then $H \cong G / K$ and $G / H \cong K$.

Proof

# Section I.9
## Exercise 1
Every nonidentity element in a free group $F$ has infinite order.

Proof

## Exercise 4
Let $F$ be the free group on the set $X$, and let $Y \subset X$. If $H$ is the smallest normal subgroup of $F$ containing $Y$, then $F / H$ is a free group.

Proof
