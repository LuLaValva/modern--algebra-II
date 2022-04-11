---
author: "Luke LaValva"
title: "Modern Algebra II Homework 5"
---

## Chapter 24

1) Prove that there is no simple group of order $210=2\cdot 3\cdot 5\cdot 7$.

    $210=2\cdot 105$ so, by the 2-odd theorem, no group of order $210$ is simple.

$%$

2) Prove that there is no simple group of order $280=2^3\cdot 5\cdot 7$.

    By the Sylow theorems,
    $$
    \begin{aligned}
      s_2 & \in \{1, 5, 7, 35\} \\
      s_5 & \in \{1, 56\} \\
      s_7 & \in \{1, 8\}
    \end{aligned}
    $$
    If there is a unique Sylow $k$-subgroup, then it is a nontrivial normal subgroup of $G$ and $G$ is not normal.
    
    If the number of Sylow 5-subgroups is 56 and the number of Sylow 7-subgroups is 8, then there must be $4\cdot 56=224$ elements of order 5 and $6\cdot 8=48$ elements of order 7. However, $224+48=272$. Then there are 8 elements leftover, one of which is the identity, so there must be exactly 1 Sylow 2-subgroup that has an order of 8. Since this subgroup is unique, it must be nontrivial and normal so $G$ cannot be a simple group.

$%$

3) Prove that there is no simple group or order $216=2^3\cdot 3^3$.

    By the Sylow theorems,
    $$
    \begin{aligned}
      s_2 & \in \{3, 9, 27\} \\
      s_3 & \in \{4\}.
    \end{aligned}
    $$
    The option of unique Sylow $k$-subgroups has been eliminated, because if a Sylow subgroup is unique then its group is not simple. Thus, a simple group of order 216 must have 4 Sylow 3-subgroups. Let $H$ be the normalizer of $_1S_3$. We know that $[G:H]=4$ and $|G|/4!=216/24\in\mathbb{Z}$, so by the index theorem there must be a nontrivial normal subgroup of $G$. Thus, $G$ is not simple.

$%$

15) Show that $A_5$ does not contain a subgroup of 30, 20, or 15.

    We know that $A_5$ is a simple group of order 60, so if $H$ is a subgroup of $A_5$ then $|A_5|\nmid [A_5:H]!$. However, the index of subgroups with order 30, 20, and 15 are 2, 3, and 4, respectively. Sixty divides all of these indices.

$%$

21) Prove that the only nontrivial proper subgroup of $S_5$ is $A_5$.

    Clearly, $A_5$ is a normal subgroup of $S_5$. Since $A_5$ is simple, any $H\lneq G$ must either only intersect with $A_5$ on the identity element or contain all of $A_5$.
    
    If $A_5\subseteq H$, then we know that $H=A_5$ because $H$ is a proper subgroup of $S_5$ and $|S_5|=2\cdot|A_5|$.
    
    Otherwise, $H$ must intersect with $A_5$ only at the identity element. If this is the case and $H$ is nontrivial, then $|H|=2$. This is impossible, because all of the elements with order 2 are in $A_5$. Thus, $A_5$ is the only nontrivial proper subgroup of $S_5$.

$%$

24) Show that the permutations of $(12)$ and $(12345)$ generate $S_5$.

    Since all permutations in a permutation group can be represented as a set of 2-cycles that are multiplied together, it is clear that if a group contains all single-element two-cycles it must also contain all of $S_5$. Here is the method for finding all single-element two-cycles in $S_5$:

    $$
    \begin{aligned}
      (12)                    & = (12) \\
      (12345)(12)(12345)^{-1} & = (23) \\
      (12345)(23)(12345)^{-1} & = (34) \\
      (12345)(34)(12345)^{-1} & = (45) \\
      (12345)(45)(12345)^{-1} & = (15) \\
      (12)(15)(12)^{-1}       & = (25) \\
      (23)(25)(23)^{-1}       & = (35) \\
      (45)(15)(45)^{-1}       & = (14) \\
      (12)(14)(12)^{-1}       & = (24) \\
      (34)(14)(34)^{-1}       & = (13) \\
    \end{aligned}
    $$

$%$

28) Prove that a simple group cannot have a subgroup of index 4.

    Suppose that $G$ is a simple group, and $H\leq G$ such that $[G:H]=4$. We know that all groups of order 4 are Abelian, so $G/H$ must be an Abelian group. This implies that $H$ is normal in $G$. However, if $H$ is normal in $G$ and it is non-trivial then $G$ must not be a simple group.
    
    This leaves only the case where $|G|=4$. However, we know that this group is Abelian, so it must have a normal subgroup with an order of 2. Thus, $G$ must not be a simple group.