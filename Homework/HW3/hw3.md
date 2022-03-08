---
author: "Luke LaValva"
title: "Modern Algebra II Homework 3"
---

## Chapter 27

4) A benzene molecule can be modeled as siz carbon atoms arranged in a regular hexagon in a plane. At each carbon atom, one of three radicals NH$_2$, COOH, or OH can be attached. How many such componds are possible?

    $G=D_{6}, |G|=12$

    |     $g$     | amount |  $\text{fix}_S(g)$  |
    | :---------: | :----: | :-----------------: |
    |      e      |   1    | $3^6 = 729$         |
    | rot order 2 |   1    | $3^3 = 27$          |
    | rot order 3 |   2    | $3^2 = 9$           |
    | rot order 6 |   2    | $3^1 = 3$           |
    | ref on edge |   3    | $3^3 = 27$          |
    | ref on vert |   3    | $3^4 = 81$          |

    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{12}(729+27+2(9)+2(3)+3(27)+3(81)) \\
          & = \frac{1104}{12} \\
          & = 92
      \end{aligned}
    $$

$%$

5) Suppose that in Exercise 4 we permit only NH$_2$ and COOH for the radicals. How many componds are possible?

    |     $g$     | amount |  $\text{fix}_S(g)$  |
    | :---------: | :----: | :-----------------: |
    |      e      |   1    | $2^6 = 64$          |
    | rot order 2 |   1    | $2^3 = 8$           |
    | rot order 3 |   2    | $2^2 = 4$           |
    | rot order 6 |   2    | $2^1 = 2$           |
    | ref on edge |   3    | $2^3 = 8$           |
    | ref on vert |   3    | $2^4 = 16$          |
    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{12}(64+8+2(4)+2(2)+3(8)+3(16)) \\
          & = \frac{156}{12} \\
          & = 13
      \end{aligned}
    $$

$%$

6) Determine the number of ways in which the faces of a regular dodecahedron can be colored with six colors.


    |     $g$     | amount |  $\text{fix}_S(g)$  |
    | :---------: | :----: | :-----------------: |
    |      e      |   1    | $6^{12} = 2176782336$ |
    | rot order 2 |   15   | $6^6 = 46656$       |
    | rot order 3 |   20   | $6^4 = 1296$        |
    | rot order 5 |   24   | $6^4 = 1296$        |
    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{60}(1(2176782336) + 15(46656) + 20(1296) + 24(1296)) \\
          & = \frac{2177539200}{60} \\
          & = 36292320
      \end{aligned}
    $$

$%$

7) Determine the number of ways in which the edges of a square can be colored with six colors so that no color is used on more than one edge.

    0? Unless I am misunderstanding the question, there are 12 edges on a square so it is not possible to color them uniquely with six colors due to the pidgeonhole principle.

$%$

8) Determine the number of ways in which the edges of a square can be colored with six colors with no restriction placed on the number of times that a color can be used.

    |     $g$     | amount |  $\text{fix}_S(g)$  |
    | :---------: | :----: | :-----------------: |
    |       e      |   1    | $6^{12} = 2176782336$ |
    | erot order 2 |   6    | $6^4 = 216$           |
    | frot order 2 |   3    | $6^4 = 216$           |
    | vrot order 3 |   8    | $6^2 = 36$            |
    | frot order 4 |   6    | $6^2 = 36$            |
    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{24}(1(2176782336) + 6(216) + 3(216) + 8(36) + 6(36)) \\
          & = \frac{2176784784}{24} \\
          & = 90699366
      \end{aligned}
    $$

$%$

9) Determine the number of 11-bead necklaces that can be made using two colors.

    |     $g$      | amount |  $\text{fix}_S(g)$  |
    | :----------: | :----: | :-----------------: |
    |      e       |   1    | $2^{11} = 2048$     |
    | rot order 11 |   10   | $2$                 |
    | reflection   |   11   | $2^6 = 64$          |
    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{22}(2048 + 10(2) + 11(64)) \\
          & = \frac{2772}{22} \\
          & = 126
      \end{aligned}
    $$

$%$

14) Let $G$ be a finite group, let $H$ be a subgroup of $G$, and let $S$ be the set of left cosets of $H$ in $G$. For each $g$ in $G$, let $\gamma_g$ denote the element of $\text{sym}(S)$ defined by $\gamma_g(xH)=gxH$. Show that $G$ acts on $S$ under the action $g\to\gamma_g$.

    For any $g_1$ and $g_2$, it is clear that $\gamma_{g_1}(xH)=g_1xH$, $\gamma_{g_2}(xH)=g_2xH$ and also that $\gamma_{g_1g_2}(xH)=g_1g_2xH$. This is sufficient to show that $G$ acts on $S$.

$%$

15) For a fixed square, let $L_1$ be the perpendicular bisector of the top and bottom of the square and let $L_2$ be the perpendicular bisector of the left and right sides. Show that $D_4$ acts on $\{L_1, L_2\}$ and determine the kernel of the mapping $g\to\gamma_g$.
    $$
      D_4=\{R_0, R_{90}, R_{180}, R_{270}, \rho_H, \rho_V, \rho_{D_1}, \rho_{D_2}\}
    $$
    $\ker(\gamma_g)=\{R_0, R_{180}, \rho_H, \rho_V\}$, and all other elements swap the two perpendicular bisectors. 

## Chapter 11

1) What is the smallest integer $n$ such that there are two nonisomorphic groups of order $n$? Name the two groups.

    $n=4$. The two groups are $\mathbb{Z}_4$ and $\mathbb{Z}_2\oplus\mathbb{Z}_2$.

$%$

2) What is the smallest positive integer $n$ such that there are three nonisomorphic Abelian groups of order $n$? Name the three groups.

    $n=8$. The three groups are $\mathbb{Z}_8$, $\mathbb{Z}_4\oplus\mathbb{Z}_2$, and $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$.

$%$

3) What is the smallest positive integer $n$ such that there are exactly four nonisomorphic Abliean groups of order $n$? Name the four groups.

    $n=36$. The four groups are 
    $$
      \begin{aligned}
        \mathbb{Z}_9 & \oplus\mathbb{Z}_4 \\
        \mathbb{Z}_9 & \oplus\mathbb{Z}_2\oplus\mathbb{Z}_2 \\
        \mathbb{Z}_3\oplus\mathbb{Z}_3 & \oplus\mathbb{Z}_4 \\
        \mathbb{Z}_3\oplus\mathbb{Z}_3 & \oplus\mathbb{Z}_2\oplus\mathbb{Z}_2
      \end{aligned}
    $$
$%$

5) Prove that every Abelian group of order 45 has an element of order 15. Does every Abelian group of order 45 have an element of order 9?

    The only Abelian groups of order 45 are $\mathbb{Z}_9\oplus\mathbb{Z}_5$ and $\mathbb{Z}_3\oplus\mathbb{Z}_3\oplus\mathbb{Z}_5$. In the first group $|(3, 1)|=15$ and in the second one $|(1, 1, 1)|=15$. However, there are no elements of order 9 in the second of the two isomorphism classes.

$%$

6) Show that there are two Abelian groups of order 108 that have exactly one subgroup of order 3.

    | Group Isomorphism Class | Generators of unique order 3 subgroups | num subgroups |
    | :---------------------: | :------------------- | :--:|
    | $\mathbb{Z}_4\oplus\mathbb{Z}_{27}$ | $\{(0, 9)\}$ | 1 |
    | $\mathbb{Z}_4\oplus\mathbb{Z}_9\oplus\mathbb{Z}_{3}$ | $\{(0, 0, 1),$ $(0, 3, 0),$ $(0, 3, 1),$ $(0, 3, 2)\}$ | 4 |
    | $\mathbb{Z}_4\oplus\mathbb{Z}_3\oplus\mathbb{Z}_{3}\oplus\mathbb{Z}_3$ | $\{(0, 0, 0, 1),$ $(0, 0, 1, 0),$ $(0, 1, 0, 0),$ $(0, 0, 1, 1),(0, 0, 1, 2),$ $(0, 1, 0, 1),$ $(0, 1, 0, 2),$ $(0, 1, 1, 0),(0, 1, 2, 0),$ $(0, 1, 1, 1),$ $(0, 1, 1, 2),$ $(0, 1, 2, 1),(0, 2, 1, 1)\}$ | 13 |
    | $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_{27}$ | $\{(0, 0, 9)\}$ | 1 |
    | $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_9\oplus\mathbb{Z}_{3}$ | $\{(0, 0, 0, 1),$ $(0, 0, 3, 0),$ $(0, 0, 3, 1),$ $(0, 0, 3, 2)\}$ | 4 |
    | $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_3\oplus\mathbb{Z}_{3}\oplus\mathbb{Z}_3$ | $\{(0, 0, 0, 0, 1),$ $(0, 0, 0, 1, 0),$ $(0, 0, 1, 0, 0),$ $(0, 0, 0, 1, 1),(0, 0, 0, 1, 2),$ $(0, 0, 1, 0, 1),$ $(0, 0, 1, 0, 2),$ $(0, 0, 1, 1, 0),(0, 0, 1, 2, 0),$ $(0, 0, 1, 1, 1),$ $(0, 0, 1, 1, 2),$ $(0, 0, 1, 2, 1),(0, 0, 2, 1, 1)\}$ | 13 |

$%$

1) Show that there are two Abelian groups of order 108 that have exactly four subgroups of order 3.

    Refer to chart in question (6).

$%$

8) Show that there are two Abelian groups of order 108 that have exactly 13 subgroups of order 3.

    Refer to chart in question (6).

$%$

9) Suppose that $G$ is an Abelian group of order 120 and that $G$ has exactly three elements of order 2. Determine the isomorphism class of $G$.

    The possible isomorphism classes of order 120 are as follows:

    - $\mathbb{Z}_8\oplus\mathbb{Z}_3\oplus\mathbb{Z}_5$ only has one element of order 2, so this is not the group.
    - $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_3\oplus\mathbb{Z}_5$ has more than three elements of order 2, so it cannot be the group.
    - $\mathbb{Z}_4\oplus\mathbb{Z}_2\oplus\mathbb{Z}_3\oplus\mathbb{Z}_5$ has three elements of order 2 $\{(2, 0, 0, 0), (0, 1, 0, 0), (2, 1, 0, 0)\}$, so this must be it!

$%$

10) Find all Abelian groups (up to isomorphism) of order 360.

    $$
      \begin{matrix}
        \mathbb{Z}_8 & \oplus & \mathbb{Z}_9 & \oplus & \mathbb{Z}_5 \\
        \mathbb{Z}_4\oplus\mathbb{Z}_2 & \oplus & \mathbb{Z}_9 & \oplus & \mathbb{Z}_5 \\
        \mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2 & \oplus & \mathbb{Z}_9 & \oplus & \mathbb{Z}_5 \\
        \mathbb{Z}_8 & \oplus & \mathbb{Z}_3\oplus\mathbb{Z}_3 & \oplus & \mathbb{Z}_5 \\
        \mathbb{Z}_4\oplus\mathbb{Z}_2 & \oplus & \mathbb{Z}_3\oplus\mathbb{Z}_3 & \oplus & \mathbb{Z}_5 \\
        \mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2 & \oplus & \mathbb{Z}_3\oplus\mathbb{Z}_3 & \oplus & \mathbb{Z}_5 \\
      \end{matrix}
    $$

$%$

12) Suppose that the order of some finite Abelian group is divisible by 10. Prove that the group has a cyclic subgroup of order 10.

    Since the order of the group is divisible by 10, it is possible to represent the order as $2\times5\times n$, where $n\in\mathbb{Z}$. Since 2 and 5 are distinct primes, there must be at least one element in the group which has an order of both 2 and 5. Then that element may be used to generate a cyclic subgroup of order 10.

$%$

15) How many Abelian groups (up to isomorphism) are there
    a) of order 6?

        1
    b) of order 15?

        1
    c) of order 42?

        1
    d) of order $pq$, where $p$ and $q$ are distinct primes?

        1
    e) of order $pqr$, where $p$, $q$, and $r$ are distinct primes?

        1
    f) Generalize parts (d) and (e).

        If the prime factorization of a number contains all unique primes, then there is only one isomorphism class of Abelian groups which has that order.

$%$

19) The symmetry group of a nonsquare rectangle is an Abelian group of order 4. Is it isomorphic to $\mathbb{Z}_4$ or $\mathbb{Z}_2\oplus\mathbb{Z}_2$?

    This symmetry group may be shown as $\{R_0, R_{180}, \rho_H, \rho_V\}$. All elements of this group have an order of 1 or 2, so it must be isomorphic to $\mathbb{Z}_2\oplus\mathbb{Z}_2$.

$%$

21) The set $\{1, 9, 16, 22, 29, 53, 74, 79, 81\}$ is a group under multiplication modulo 91. Determine the isomorphism class of this group.

    I set up this script that finds the order of each element of the group, check it out:
    ```js
      order = (size, element) => {
        let order = 1, curr = 1;
        while ((curr = (curr * element) % size) !== 1) order++;
        return order;
      }

      [1, 9, 16, 22, 29, 53, 74, 79, 81].map((element) => order(91, element));
      // output: [1, 3, 3, 3, 3, 3, 3, 3, 3]
    ```

    All of the elements in this group (except for the identity) have an order of 3, which implies that there are 4 unique orbits within this group. Thus, the isomorphism class can be defined as $\mathbb{Z}_3\oplus\mathbb{Z}_3$.

$%$

26) Let $G=\{1, 7, 17, 23, 49, 55, 65, 71\}$ be a group under multiplication modulo 96. Express $G$ as an external and an internal direct product of cyclic groups.

    ```js
      [1, 7, 17, 23, 49, 55, 65, 71].map((element) => order(96, element));
      // [1, 4, 2, 4, 2, 4, 2, 4]
    ```
    This group has an order of 8, so it must be congruent to either $\mathbb{Z}_8$, $\mathbb{Z}_4\oplus\mathbb{Z}_2$, or $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$. There is are no elements of order 8 and 7 has an order of 4, so the group must be isomorphic to $\mathbb{Z}_4\oplus\mathbb{Z}_2$.

$%$

27) Let $G=\{1, 7, 43, 49, 51, 57, 93, 99, 101, 107, 143, 149, 151, 157, 193, 199\}$ under multiplication modulo 200. Express $G$ as an external and an internal direct product of cyclic groups.

    ```js
      [1, 7, 43, 49, 51, 57, 93, 99, 101, 107, 143, 149, 151, 157, 193, 199].map((element) => order(200, element));
      // [1, 4, 4, 2, 2, 4, 4, 2, 2, 4, 4, 2, 2, 4, 4, 2]
    ```
    This group has an order of 16, so it must be isomorphic to either $\mathbb{Z}_{16}$, $\mathbb{Z}_8\oplus\mathbb{Z}_2$, $\mathbb{Z}_4\oplus\mathbb{Z}_4$, $\mathbb{Z}_4\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$, or $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$. There are no elements of order 16 or 8 but there are elements of orders 4 and 2, so we know that it must be isomorphic to either $\mathbb{Z}_4\oplus\mathbb{Z}_4$ or $\mathbb{Z}_4\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$. We also can see that there are 8 elements of order 4 and 7 of order 2, so by process of elimination the group is isomorphic to $\mathbb{Z}_4\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$.

$%$

28) The set $G=\{1, 4, 11, 14, 16, 19, 26, 29, 31, 34, 41, 44\}$ is a group under multiplication modulo 45. Write $G$ as an external and an internal direct product of cyclic groups of prime-power order.

    The group has an order of 12 and it has elements of order 2, 3, and 6 but none of order 4, so it must be isomorphic to $\mathbb{Z}_3\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$. One possible IDP is $\langle 19\rangle\times\langle 26\rangle\times\langle 31\rangle$.

$%$

34) Prove that an Abelian group of order $2^n (n\geq 1)$ must have an odd number of elements of order 2.

    Base case: order is $2^1=2$, so the group is isomorphic to $\mathbb{Z}_2$. Then there is one element of order of 2.

    Any group $G$ of order $2^n$ is isomorphic to
    $$
      \bigoplus_{i=0}^k\mathbb{Z}_{2^{a_i}},
    $$
    where $a$ is a set of integers of length $k$ and $\sum_{i=0}^ka_i=n$. Then in order to double the order of $G$, we may either set $a_{k+1}=2$ or set any $a_k=2a_k$. In the former case, the number of elements of order 2 is doubled and one additional element of order 2 is added. In the latter, the number of elements of order two remains the same.

$%$

35) Without using Lagrange's Theorem, show that an Abelian group of odd order cannot have an element of even order.

  Since the Abelian group has an odd order, it can be written as
  $$
    \bigoplus_{i=0}^k\mathbb{Z}_{p_i^{a_i}},
  $$
  where $p_i$ represents an odd prime. We know that the order of every element divides all $p_i^{a_i}$, each of which are odd, so the order of each element must also be odd.