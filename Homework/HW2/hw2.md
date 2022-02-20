---
author: "Luke LaValva"
title: "Modern Algebra Homework 2"
---

## Chapter 10

21) If $\phi$ is a homomorphism from $\mathbb{Z}_{30}$ onto a group of order 5, determine the kernel of $\phi$.

    By the first isomorphism theorem, we know that
    $$
      \begin{aligned}
        \frac{G}{\ker\phi}   & \cong\phi(G)  \\\\
        \left|\frac{G}{\ker\phi}\right| & = |\phi(G)|   \\
                     & = 5           \\\\
        |\ker\phi|   & = \frac{|G|}{5} \\
                     & = \frac{30}{5} \\
                     & = 6.
      \end{aligned}
    $$
    The kernel of a group must be a subgroup, and there is only one subgroup of $\mathbb{Z}_{30}$ that has an order of 6:
    $$
      \langle 5\rangle = \{0,5,10,15,20,25\}
    $$

\

26) Determine all homomorphisms from $\mathbb{Z}_4$ to $\mathbb{Z}_2\oplus\mathbb{Z}_2$.

    Let $\varphi$ be a homomorphism from $\mathbb{Z}_4$ to $\mathbb{Z}_2\oplus\mathbb{Z}_2$. Then
    $$
      \begin{aligned}
        \varphi(0) & = (0,0) \\
        \varphi(1) & = (x, y) \\
        \varphi(2) & = \varphi(1 + 1) \\
                   & = \varphi(1) + \varphi(1) \\
                   & = (2x, 2y) \\
                   & = (0, 0) \\
        \varphi(3) & = \varphi(2 + 1) \\
                   & = \varphi(2) + \varphi(1) \\
                   & = (x, y) \\
      \end{aligned}
    $$
    Using these facts, we can discover that the homomorphisms are
    $$
      \begin{aligned}
        \varphi(1) = (0, 0) & \implies \varphi(n) = (0, 0) \\
        \varphi(1) = (0, 1) & \implies \varphi(n) = (0, n\% 2) \\
        \varphi(1) = (1, 0) & \implies \varphi(n) = (n\% 2, 0) \\
        \varphi(1) = (1, 1) & \implies \varphi(n) = (n\% 2, n\% 2)
      \end{aligned}
    $$
    where $\%$ represents the modulus operator.

\

31) Suppose that $\phi$ is a homomorphism from $U(30)$ to $U(30)$ and that $\ker\phi=\{1, 11\}$. If $\phi(7) = 7$, find all elements of $U(30)$ that map to 7.

    $$
      U(30) = \{1, 7, 11, 13, 17, 19, 23, 29\}
    $$
    Since $\phi(x)=x'\implies\phi^{-1}(x')=x\ker\phi$ and $\phi(7)=7$, we can determine that $\phi^{-1}(7)=7\ker\phi=\{7, 17\}$ and thus 7 and 17 are the values that map to 7.

\

33) Suppose that $\phi$ is a homomorphism from $U(40)$ to $U(40)$ and that $\ker\phi=\{1, 9, 17, 33\}$. If $\phi(11) = 11$, find all elements of $U(40)$ that map to 11.

    $\phi^{-1}(11)=11\ker\phi=\{11, 19, 27, 3\}$.

\

49) (Second Isomorphism Theorem) If $K$ is a subgroup of $G$ and $N$ is a normal subgroup of $G$, prove that $K/(K\cap N)$ is isomorphic to $KN/N$.

    We know that $KN\leq G$ because $N\triangleleft G$. Let us define $\varphi:K\to KN/N$ such that $\varphi(k)=kN$. This is obviously well-defined, and $\varphi(k_1k_2)=k_1k_2N=k_1Nk_2N=\varphi(k_1)\varphi(k_2)$ so it preserves the group operation. Thus, $\varphi$ is a homomorphism. Since $\varphi(k)=N$ iff $k\in N$, we know that $\ker\varphi=K\cap N$. Therefore, by the first isomorphism theorem,
    $$
      \frac{K}{K\cap N}=\frac{K}{\ker\varphi}\cong \varphi(K)=\frac{KN}{N}.
    $$

\

50) (Third Isomorphism Theorem) If $M$ and $N$ are normal subgroups of $G$ and $N\leq M$, prove that $(G/N)/(M/N)\cong G/M$.

    Define $\phi:G/N\to G/M$ such that $\phi(gN)=gM$. Since $N\leq M$, we know that $g_1N=g_2N\implies g_1M=g_2M$ so $\phi$ is well-defined. Also, $\phi$ must preserve the group operation because $\phi(g_1Ng_2N)=\phi(g_1g_2N)=g_1g_2M=g_1Mg_2M=\phi(g_1N)\phi(g_2N)$. Therefore, $\phi$ is a homomorphism. It is also onto because any $gM\in G/M$ can be reached by $\phi(gN)$. If $\phi(g_3N)=M$ then $x\in M$. Thus, $\ker\phi=M/N$. Therefore, by the first isomorphism theorem,
    $$
      \frac{G/N}{M/N}=\frac{G/N}{ker\phi}\cong \phi(G/N)=\frac{G}{M}.
    $$

\

54) Determine all homomorphic images of $D_4$ (up to isomorphism).

    $$
      D_4 = \{e, \omega_{90}, \omega_{180}, \omega_{270}, \rho, \rho\omega_{90}, \rho\omega_{180}, \rho\omega_{270}\}
    $$
    Intuitively, the set of normal subgroups of $D_4$ is
    $$
      \begin{aligned}
        H_1 & = \{e\} \\
        H_2 & = \langle\omega_{90}\rangle = \{e, \omega_{90}, \omega_{180}, \omega_{270}\} \\
        H_3 & = \langle\rho\omega_{90}\rangle = \{e, \rho\omega_{90}, \omega_{180}, \rho\omega_{270}\} \\
        H_4 & = \langle\omega_{180}, \rho\rangle = \{e, \omega_{180}, \rho, \rho\omega_{180}\} \\
        H_5 & = \langle\omega_{180}\rangle = \{e, \omega_{180}\} \\
        H_6 & = D_4.
      \end{aligned}
    $$
    Thus, the homomorphic images of $D_4$ are
    $$
      \begin{aligned}
        \frac{D_4}{H_6} \cong \frac{D_4}{H_1} & \cong D_4 \\
        \frac{D_4}{H_2} \cong \frac{D_4}{H_3} \cong \frac{D_4}{H_4} & \cong \mathbb{Z}_2 \\
        \frac{D_4}{H_5} & \cong \mathbb{Z}_2\oplus\mathbb{Z}_2 \\
      \end{aligned}
    $$

\

55) Suppose that $G$ is a finite group and that $\mathbb{Z}_{10}$ is a homomorphic image of $G$. What can we say about $|G|$? Generalize.

    $G/H\cong\mathbb{Z}_{10}\implies |G|=|\mathbb{Z}_{10}||H|=10|H|$. Thus, $|G|$ must be divisible by 10. In general, if $Z_n$ is a homomorphic image of $G$ then $|G|$ is divisible by $n$.

\

56) Suppose that $\mathbb{Z}_{10}$ and $\mathbb{Z}_{15}$ are both homomorphic images of a finite group $G$. What can be said about $|G|$? Generalize.

    We learned in (55) that $|G|$ must be divisible by both 10 and 15. Therefore, it must be divisble by $\mathrm{lcm}(10, 15)=30$. In general, if $\mathbb{Z}_n$ and $\mathbb{Z}_k$ are both homomorphic images of $G$ then $|G|$ must be divisible by $\mathrm{lcm}(n, k)$.

\

59) Let $N$ be a normal subgroup of a group $G$. Use property 8 of theorem 10.2 to prove that every subgroup of $G/N$ has the form $H/N$, where $H$ is a subgroup of $G$.

    Let $\phi: G\to G/N$ be a homomorphism, and $\overline H\leq G/N$. Then by property 8 of theorem 10.2, $\phi^{-1}(\overline H)=H$, where $H\leq G$. Furthermore,
    $$
      \frac{H}{N}=\phi(H)=\phi(\phi^{-1}(\overline H))=\overline H
    $$

\

64) Prove that the mapping from $\mathbb{R}$ under addition to $SL(2, \mathbb{R})$ that takes $x$ to
    $$
      \begin{bmatrix}
        \cos x & \sin x \\
        -\sin x & \cos x
      \end{bmatrix}
    $$
    is a group homomorphism. What is the kernel of the homomorphism?

    Define $\phi$ as this mapping. Then
    $$
      \begin{aligned}
        \phi(x)\phi(y) & = \begin{bmatrix}
                              \cos x & \sin x \\
                              -\sin x & \cos x
                            \end{bmatrix}\times \begin{bmatrix}
                              \cos y & \sin y \\
                              -\sin y & \cos y
                            \end{bmatrix} \\
          & = \begin{bmatrix}
            \cos(x)\cos(y) - \sin(x)\sin(y) & \sin(x)\cos(y) + \cos(x)\sin(y) \\
            -\sin(x)\cos(y) - \cos(x) \sin(y) & \cos(x)\cos(y) - \sin(x) \sin(y)
          \end{bmatrix} \\
          & = \begin{bmatrix}
                      \cos(x + y) & \sin(x + y) \\
                      -\sin(x + y) & \cos(x + y)
                    \end{bmatrix} \\
          & = \phi(x+y)
      \end{aligned}
    $$
    so $\phi$ preserves the group operation. Since $\sin$ and $\cos$ are both well-defined, $\phi$ must also be well-defined.

    The kernel of this group is all real numbers which map to the identity matrix, which is in this case $2\pi n|n\in\mathbb{Z}$

\

72) Determine all homomorphisms from $\mathbb{Z}$ onto $S_3$. Determine all homomorphisms from $\mathbb{Z}$ to $S_3$.

    Let $\varphi:\mathbb{Z}\to S_3$ be a homomorphism. Then $\varphi(\mathbb{Z})$ must be abelian because
    $$
      \varphi(x)\varphi(y) = \varphi(x+y) = \varphi(y+x) = \varphi(y)\varphi(x).
    $$
    However, $S_3$ is not an abelian group so $\varphi$ cannot be onto.

    Since $\mathbb{Z}=\langle 1\rangle$, we can define any element of $\varphi(\mathbb{Z})$ as
    $$
      \varphi(k) = \varphi(1+1+\ldots + 1) = \phi(1)^k
    $$
    so the entire group is determined by the value that is mapped to by $1$. Thus, since $|S_3|=6$ there are 6 possible functions for $\varphi$.



## Chapter 7

67) Let $G$ be a group of permutations of a set $S$. Prove that the orbits of the members of $S$ constitute a partition of $S$.

    Suppose that $g\in\text{orb}_G(a)$ and $g\in\text{orb}_G(b)$ for elements $g, a, b\in G$. Then there must be some $a_g, b_g\in G$ so that $a_ga=b_gb=g$. Define $a_b=b_g^{-1}a_g$ and $b_a=a_g^{-1}b_g$. Obviously, $a_b, b_a\in G$. Then
    $$
      \begin{aligned}
          a_ga & = b_gb \\
          b_g^{-1}a_ga & = b_g^{-1}b_gb \\
          a_ba & = b \implies b\in\text{orb}_G(a) \\
          \\
          a_ga & = b_gb \\
          a_g^{-1}a_ga & = a_g^{-1}b_gb \\
          a & = b_ab \implies a\in\text{orb}_G(b).
      \end{aligned}
    $$
    Thus, $\text{orb}_G(a)=\text{orb}_G(b)$.

\

69) Let $G=\{(1), (12)(34), (1234)(56), (13)(24), (1432)(56), (56)(13), (14)(23), (24)(56)\}$. Find the stabilizers and orbits for 1, 3, and 5.

    $$
      \begin{aligned}
        \text{stab}_G(1) & = \{(1), (24)(56)\} \\
        \text{orb}_G(1)  & = \{1, 2, 3, 4\} \\
        \text{stab}_G(3) & = \{(1), (24)(56)\} \\
        \text{orb}_G(3)  & = \{3, 4, 1, 2\} \\
        \text{stab}_G(5) & = \{(1), (12)(34), (13)(24), (14)(23)\} \\
        \text{orb}_G(5)  & = \{5, 6\} \\
      \end{aligned}
    $$

\

72) Let $G$ be the group of rotations of a plane about a point $P$ in the plane. Thinking of $G$ as a group of permutations of the plane, describe the orbit of a point $Q$ in the plane.

    The orbit of a point $Q$ is a circle centered at $P$ with a radius of $|\overline{PQ}|$.

\

73) Let $G$ be the rotation group of a cube. Label the faces of the cube 1 through 6, and let $H$ be the subgroup of elements of $G$ that carry face 1 to itself. If $\sigma$ is a rotation that carries face 2 to face 1, give a physical description of the coset $H\sigma$.

    Let 6 be the face on the opposite side of 1. Then there are 4 operations in $H$: the null operation and rotations by 90, 180, and 270 degrees about the axis from 1 to 6. The coset $H\sigma$ is all cubes which have face 1 on the bottom and 6 on the top.

\

74) A soccer ball has 20 faces that are regular hexagons and 12 faces that are regular pentagons. Use Theorem 7.4 to explain why a soccer ball cannot have a $60^\circ$ rotational symmetry about a line through the centers of two opposite hexagonal faces.

    The order of this symmetry group would have to be $6\cdot 20=120$, but this cannot be the case <!-- TODO: Expand on this -->

\

76) Calculate the orders of the following:
    1) The group of rotations of a regular tetrahedron
        $$
          |\text{orb}_G(i)|\cdot|\text{stab}_G(i)| = 4\cdot 3 = 12
        $$
    2) The group of rotations of a regular octahedron
        $$
          |\text{orb}_G(i)|\cdot|\text{stab}_G(i)| = 8\cdot 3 = 24
        $$
    3) The group of rotations of a regular dodecahedron
        $$
          |\text{orb}_G(i)|\cdot|\text{stab}_G(i)| = 12\cdot 5 = 60
        $$
    4) The group of rotations of a regular icosahedron
        $$
          |\text{orb}_G(i)|\cdot|\text{stab}_G(i)| = 20\cdot 3 = 60
        $$

\

64) Suppose that $\alpha\in S_n(n\geq 3)$ and $\alpha(1)=3$. Let $H=\text{stab}(1)$. Prove that $\alpha H$ is the set of all elements of $S_n$ that send 1 to 3. Generalize.

    $H$ is the set of all of the elements of $S_n$ that send 1 to itself, so for any $\beta\in H$,
    $$
      \alpha\beta(1)=\alpha(\beta(1))=\alpha(1)=3.
    $$
    In general, for any $s\in S_n$ it can be shown that $sH(1)=s(1)$.



## Chapter 27

1) Determine the number of ways in which the four corners of a square can be colored with two colors.

    $G=D_4, |G|=8$

    |     $g$     | amount | $\text{fix}_S(g)$ |
    | :---------: | :----: | :---------------: |
    |      e      | 1      | $2^4=16$          |
    | rot order 2 | 1      | $2^2=4$           |
    | rot order 4 | 2      | $2^1=2$           |
    | ref on edge | 2      | $2^2=4$           |
    | ref on vert | 2      | $2^3=8$           |

    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{8}(16 + 4 + 2(2) + 2(4) + 2(8)) \\
          & = \frac{48}{8} \\
          & = 6
      \end{aligned}
    $$

\

2) Determine the number of different necklaces that can be made using 13 white beads and 3 black beads. 

    $G=D_{16}, |G|=32$

    |     $g$      | amount |  $\text{fix}_S(g)$  |
    | :----------: | :----: | :-----------------: |
    |      e       |   1    | $\binom{16}{3}=560$ |
    | rot order 2  |   1    | $0$                 |
    | rot order 4  |   2    | $0$                 |
    | rot order 8  |   4    | $0$                 |
    | rot order 16 |   8    | $0$                 |
    | ref on edge  |   8    | $0$                 |
    | ref on vert  |   8    | $7\cdot 2=14$      |

    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{32}(560+8(14)) \\
          & = \frac{672}{32} \\
          & = 21
      \end{aligned}
    $$

\

3) Determine the number of ways in which the vertices of an equilateral triangle can be colored with five colors so that at least two colors are used.

    $G=D_{3}, |G|=6$

    |     $g$     | amount |  $\text{fix}_S(g)$  |
    | :---------: | :----: | :-----------------: |
    |      e      |   1    | $5^3-5=120$         |
    | rot order 3 |   2    | $0$                 |
    | reflection  |   3    | $5\cdot 4=20$       |

    $$
      \begin{aligned}
        N & = \frac{1}{|G|}\sum_{g\in G}|\text{fix}_S(g)| \\
          & = \frac{1}{6}(120+3(20)) \\
          & = \frac{180}{6} \\
          & = 30
      \end{aligned}
    $$