---
author: "Luke LaValva"
title: "Normal Subgroups and Factor Groups"
---


## Chapter 9

1) 
    Let $H = \{(1), (12)\}$. is $H$ normal in $S_3$?

    No, let $h=(12)$ and $g=g^{-1}=(13)$. Then
    $$
      ghg^{-1} = (13)(12)(13) = (1)(23)\notin H
    $$

\

6) 
    Let $H = \left\{\left.\begin{bmatrix}a&b\\0&d\end{bmatrix}\right|a,b,d\in\mathbb{R}, ad\neq 0\right\}$. Is $H$ a normal subgroup of $GL(2, \mathbb{R})$?

    No, let $h=\begin{bmatrix}1&1\\0&1\end{bmatrix}\in H$ and $g=\begin{bmatrix}1&0\\1&1\end{bmatrix}\in GL(2, \mathbb{R})$. Then
    $$
      ghg^{-1} =
      \begin{bmatrix}1&0\\1&1\end{bmatrix}
      \begin{bmatrix}1&1\\0&1\end{bmatrix}
      \begin{bmatrix}1&0\\1&1\end{bmatrix}^{-1}
      =
      \begin{bmatrix}0&1\\-1&2\end{bmatrix} \notin H
    $$

\

9) 
    Prove that if $H$ has index 2 in $G$, then $H$ is normal in $G$.

    Let $g\in G$. Then in order to show that $gH=Hg$, we can consider two cases:

    1) $g\in H$ --- Because $H$ is a group, it is given that $gH=H=Hg$. Apply the transitive property.
    2) $g\notin H$ --- Since $H$ has an index of 2 in $G$, we know that there are two left cosets and two right cosets of $H$ in $G$. However, one of those cosets must be equal to $H$ so the other must be equal to $G-H$. Because $g\notin H$, $gH=Hg$.

\

10)
    Let $H=\{(1), (12)(34)\}\in A_4$.

    a)
        Show that $H$ is not normal in $A_4$.

        $$
            ghg^{-1} = (13)((12)(34))(13) = (14)(23) \notin H
        $$

    b)
        Show that, although $\alpha_6H = \alpha_7H$ and $\alpha_9H = \alpha_{11}H$, it is not true that $\alpha_6\alpha_9H=\alpha_7\alpha_{11}H$. Explain why this proves that the left cosets of H do not form a group under coset multiplication.

        $$
        \begin{aligned}
            \alpha_6H & = (243)H & = \{(243), (243)(12)(34) = (142)\} \\
            \alpha_7H & = (142)H & = \{(142), (142)(12)(34) = (243)\} \\
            \therefore \alpha_6H & = \alpha_7H \\
            \\
            \alpha_9H & = (132)H & = \{(132), (132)(12)(34) = (234)\} \\
            \alpha_{11}H & = (234)H & = \{(234), (234)(12)(34) = (132)\} \\
            \therefore \alpha_9H & = \alpha_{11}H \\
            \\
            \alpha_6\alpha_9H & = (243)(132)H & = \{(12)(34), (12)(34)(12)(34) = (1)\} \\
            \alpha_7\alpha_{11}H & = (142)(234)H & = \{(14)(23), (14)(23)(12)(34) = (13)(24)\} \\
            \therefore \alpha_6\alpha_9H & \neq \alpha_7\alpha_{11}H \\
        \end{aligned}
        $$

        For elements $\alpha_x, \alpha_y\in A_4$, we define coset multiplication as $\alpha_xH\cdot\alpha_yH = \alpha_x\alpha_yH$. However, this operation is not well defined because $\alpha_6H\cdot\alpha_9H = \alpha_7H\cdot\alpha_{11}H$ but $\alpha_6\alpha_9H \neq \alpha_7\alpha_{11}H$.

\

12) Prove that a factor group of an Abelian group is Abelian.

    Let $H\leq G$. Then $G/H=\{gH|g\in G\}$. By the group operation of factor groups,
    $$
        (g_1H)(g_2H)=g_1g_2H=g_2g_1H \text{ ($G$ is Abelian)}=(g_2H)(g_1H).
    $$
    Therefore, $G/H$ must be abelian.

\

25) Let $G=U(32)$ and $H={1, 15}$. The group $G/H$ is isomorphic to one of $\mathbb{Z}_8$, $\mathbb{Z}_4\oplus\mathbb{Z}_2$, or $\mathbb{Z}_2\oplus\mathbb{Z}_2\oplus\mathbb{Z}_2$. Determine which one by elimination.
    
    Suppose $G/H$ is defined as $\{3^iH|i\in\mathbb{Z}\}$. It may be observed that $3^2H=9H=\{1,7\}\neq H$ and $3^4H=17H=\{1,31\}\neq H$, but $3^8H=1H=\{1,15\}=H$. Therefore, $G/H\cong\mathbb{Z}_8$.

\

34) In $\mathbb{Z}$, let $H=\langle 5\rangle$ and $K=\langle 7\rangle$. Prove that $\mathbb{Z}=HK$. Does $\mathbb{Z}=H\times K$?

    $2\times 7 - 3\times 5=-1, 3\times 7 - 4\times 5=1$. It is possible to reach all of $\mathbb{Z}$ by using the group operation (addition) on 1 and -1, so it is clear that $HK\cong\mathbb{Z}$. However, inner products require that the two subgroups have an intersection of $\{0\}$, and this is not the case since $H\wedge K=\langle 35\rangle$.

\

49) Suppose that $G$ is a non-Abelian group of order $p^3$, where $p$ is a prime and $Z(G)\neq \{e\}$. Prove that $\lvert Z(G)\rvert = p$.

    Because $Z(G)\leq G$, we know that $|Z(G)|\Big|\left(|G|=p^3\right)$. Therefore, since $p$ is a prime number, there are four options for $|Z(G)|$.

    1) $|Z(G)|\neq 1$, because it must contain the identity and it is given that $Z(G)\neq \{e\}$.
    2) $|Z(G)|\neq p^3$, because if the center contained the entire group then $G$ would be Abelian.
    3) $|Z(G)|\neq p^2$. We will prove this by contradiction. Suppose that $|Z(G)|=p^2$. Then
        $$
        \left|\frac{G}{Z(G)}\right|=\frac{|G|}{|Z(G)|}=\frac{p^3}{p^2}=p,
        $$
        and thus $G/Z(G)$ is cyclic. Then, by the $G/Z$ theorem, $G$ must be abelian. This cannot be, because $G$ is non-Abelian. Conradiction.
    4) $|Z(G)|= p$, by process of elimination.

\

50) If $\lvert G\rvert = pq$, where $p$ and $q$ are primes that are not necessarily distinct, prove that $\lvert Z(G)\rvert=1$ or $pq$.

    Because $Z(G)\leq G$, we know that $|Z(G)|\Big|\left(|G|=pq\right)$. Suppose that $|Z(G)|=p$ and/or $|Z(G)|=q$. If $Z(G)=q$, we swap $p$ and $q$ so that $Z(G)$ is now equal to $p$. Then
    $$
       \left|\frac{G}{Z(G)}\right|=\frac{|G|}{|Z(G)|}=\frac{pq}{p}=q 
    $$
    and thus $G/Z(G)$ is cyclic. However, by the $G/Z$ theorem, this means that $G$ is Abelian. The center of an Abelian group is always the group itself, which has an order of $pq$. This is a contradiction, so $|Z(G)|\neq p$ and $|Z(G)|\neq q$. We are now left with 2 options. If $G$ is abelian, $|Z(G)|=|G|=pq$. Otherwise, $|Z(G)|=|\{e\}|=1$.

\

54) Let $G=\{\pm 1, \pm i, \pm j, \pm k\}$, where $i^2=j^2=k^2=-1, -i=(-1)i, 1^2=-1^2=1, ij=-ji=k, jk=-kj=i$, and $ki=-ik=j$

    a) Show that $H=\{-1,1\}\triangleleft G$

        It is obvious that $H\subset G$ and $H$ is a group with 1 as the identity, so $H\leq G$. In order to determine whether $H\triangleleft G$ it suffices to show that $g(-1)g^{-1}\in H$ and $g(1)g^{-1}\in H$ for all $g\in G$. For the latter case, $g(1)g^{-1}=gg^{-1}=e=1\in H$. In the former case, $g(-1)g^{-1}=g(-1)(-g)=g(g)=g^2=1\forall g\in G$. Therefore, $H\triangleleft G$.

    b) Construct the Cayley table for $G/H$. is $G/H$ isomorphic to $Z_4$ or $Z_2\oplus Z_2$?

        $$
        \begin{array}{c || c | c | c | c | c | c | c | c}
                & 1 & -1 & i & -i & j & -j & k & -k \\
            \hline\hline
            1 & 1 & -1 & i & -i & j & -j & k & -k\\
            \hline
            -1 & -1 & 1 & -i & i & -j & j & -k & k\\
            \hline
            i & i & -i & 1 & -1 & k & -k & -j & j\\
            \hline
            -i & -i & i & -1 & 1 & -k & k & j & -j\\
            \hline
            j & j & -j & -k & k & 1 & -1 & i & -i\\
            \hline
            -j & -j & j & k & -k & -1 & 1 & -i & i\\
            \hline
            k & k & -k & j & -j & -i & i & 1 & -1\\
            \hline
            -k & -k & k & -j & j & i & -i & -1 & 1\\
        \end{array}
        $$
        $G/H$ is isomorphic to $Z_2\oplus Z_2$

\

56) Show that the intersection of two normal subgroups of $G$ is a normal subgroup of $G$. Generalize.

    Let $H, K\triangleleft G$, and $M=H\wedge K$. Then $m\in H, m\in K\forall m\in M$. By definition of normal subgroups, $gmg^{-1}\in H$ and $gmg^{-1}\in K$. Therefore, $gmg^{-1}\in M$. Thus, $M\triangleleft G$.

    This result must be true for the intersection between any $n$ subgroups of $G$. Let these subgroups be defined as $H_1, H_2, \ldots, H_n$. Then $H_1\wedge H_2\wedge \ldots\wedge H_n=(H_1\wedge H_2)\wedge \ldots\wedge H_n$. Since $(H_1\wedge H_2)\triangleleft G$, we can redefine $(H_1\wedge H_2)$ as $H_1$ and $H_{k\geq 3}$ as $H_{k-1}$ to be left with $H_1\wedge H_2\wedge \ldots\wedge H_{n-1}$. We can repeat this step infinitely many times to find that the intersection between all groups is a normal subgroup of $G$.

\

59) Let $N$ be a normal subgroup of a group $G$. If $N$ is cyclic, prove that every subgroup of $N$ is also normal in $G$.

    All cyclic groups are Abelian, and we know that $gNg^{-1}\in N\forall g\in G$. Let $N=\langle n\rangle$ and $H\leq N$. Then $H=\langle n^i\rangle$, where $i\in\mathbb{Z}_{|N|}$. Any element of $H$ can be described as $(n^i)^k$. Using this information, we can show that
    $$
        \begin{aligned}
            g(n^i)^kg^{-1}
             & = gn^{(ik)}g^{-1}\\
             & = gnn\ldots nng^{-1} \\
             & = gnene\ldots eneng^{-1} \\
             & = gngg^{-1}ng\ldots g^{-1}ngg^{-1}ng^{-1} \\
             & = (gng^{-1})^{ik} \\
             & = (n^m)^{ik} \in \langle n^i\rangle = H.
        \end{aligned}
    $$

\

64) Let $G$ be a group and let $G'$ be a subgroup of $G$ generated by the set $S=\left\{x^{-1}y^{-1}xy\middle|x, y\in G\right\}$

    a) Prove that $G'$ is normal in $G$.

        $$
            \begin{aligned}
                gx^{-1}y^{-1}xyg^{-1}
                & = gx^{-1}ey^{-1}exeyg^{-1} \\
                & = gx^{-1}g^{-1}gy^{-1}g^{-1}gxg^{-1}gyg^{-1} \\
                & = (gx^{-1}g^{-1})(gy^{-1}g^{-1})(gxg^{-1})(gyg^{-1}) \\
                & = ((g^{-1})^{-1}xg^{-1})^{-1}((g^{-1})^{-1}yg^{-1})^{-1}(gxg^{-1})(gyg^{-1}) \\
                & = (gxg^{-1})^{-1}(gyg^{-1})^{-1}(gxg^{-1})(gyg^{-1})\in G'
            \end{aligned}
        $$

    b) Prove that $G/G'$ is Abelian.

        Let $xG'$ and $yG'$ be elements of $G/G'$, and let $g=y^{-1}x^{-1}yx\in G'$. Then
        $$
            \begin{aligned}
                (xG')(yG') & = xyG' \\
                           & = xygG' \\
                           & = xyy^{-1}x^{-1}yxG' \\
                           & = yxG' \\
                           & = (yG')(xG')
            \end{aligned}
        $$

    c) If $G/N$ is Abelian, prove that $G'\leq N$.

        Since $G/N$ is Abelian, we know that for all $x,y\in G$, $xNyN=yNxN$. We have shown in part (b) that this is the case for $G'$, so we can be certain that $G'$ is a subgroup of $N$.

    d) Prove that if $H$ is a subgroup of $G$ and $G'\leq H$, then $H$ is normal in $G$.

        Let $h\in H$ and $g\in G$. Then since $h^{-1}\in H$ and $G'\leq H$, $h^{-1}g^{-1}hg\in G'$ must also be in $H$. Since the group is closed under its operation, $h(h^{-1}g^{-1}hg)=g^{-1}hg$ must also be in $H$. Thus, by definition, $H\triangleleft G$.

\

66) Suppose that a group $G$ has a subgroup of order $n$. Prove that the intersection of all subgroups of $G$ of order $n$ is a normal subgroup of $G$.

    Let $H$ be a subgroup of $G$ with order $n$. Since $|H|\big||G|$, we know that $|G|=nk,k\in\mathbb{Z}$. Suppose that $h$ exists within the intersection between all subgroups of order $n$. [TODO: I cannot figure out this part] Then $ghg^{-1}$ must also be in the intersection between all subgroups of order $n$.

\

70) Prove that $A_4$ is the only subgroup of $S_4$ of order 12.

    Let us suppose on the contrary that there is some group $H\neq A_4$ such that $|H|= 12$. Then $H$ must contain at least one odd permutation. Because squaring any odd permutation results in an even permutation and multiplying odd and even permutations together results in odd permutations, it is clear that the number of even and odd permutations must be equal. Therefore, it must be possible to generate an even subgroup of order 6. However, $S_4$ has no even subgroups of order 6. This is a contradiction.

\

73) Prove that $A_5$ cannot have a normal subgroup of order 2.

    Let $H$ be a subgoup of $A_5$ of order 2. Then $H$ may be written as $\{e, h\}$, where $h\in A_5$ and $h^2=e$. Thus, $h$ must be of the form $(ab)(cd)$. Let $g=(abc)$. Then $ghg^{-1}=(abc)(ab)(cd)(acb)=(ad)(bc)\notin H$. 

## Chapter 10

1) Prove that the mapping given in Example 2 is a homomorphism.

    $$
        \begin{aligned}
            AB & = \begin{bmatrix}
                a_1 & a_2 \\
                a_3 & a_4
            \end{bmatrix} \begin{bmatrix}
                b_1 & b_2 \\
                b_3 & b_4
            \end{bmatrix} = \begin{bmatrix}
                a_1b_1+a_2b_3 & a_1b_2+a_2b_4 \\
                a_3b_1+a_4b_3 & a_3b_2+a_4b_4
            \end{bmatrix} \\
            \det(AB)
             & = (a_1b_1+a_2b_3)(a_3b_2+a_4b_4) - (a_1b_2+a_2b_4)(a_3b_1+a_4b_3) \\
             & = a_2a_3b_2b_3 - a_1a_4b_2b_3 - a_2a_3b_1b_4 + a_1a_4b_1b_4 \\
             & = (a_2a_3 - a_1a_4)(b_2b_3 - b_1b_4) \\
             & = \det(A)\det(B)
        \end{aligned}
    $$

\

3) Prove that the mapping given in Example 4 is a homomorphism.

    When two polynomials are added together, the slope at each individual point is equivalent to the sum of the slopes of each function. Thus, for polynomials $f$ and $g$, $(f+g)' = f'+g'$.

\

1) If $\phi$ is a homomorphism from $G$ to $H$ and $\sigma$ is a homomorphism from $H$ to $K$, show that $\sigma\phi$ is a homomorphism from $G$ to $K$. How are $\ker\phi$ and $\ker\sigma\phi$ related? If $\phi$ and $\sigma$ are onto and $G$ is finite, describe $[\ker\sigma\phi:\ker\phi]$ in terms of $|H|$ and $|K|$.

    $\sigma(\phi(g_1g_2))=\sigma(\phi(g_1)\phi(g_2))=\sigma(\phi(g_1))\sigma(\phi(g_2))$, therefore $\sigma\phi$ is a homomorphism.
    
    Because $\ker\phi$ contains all elements of $G$ for which $\phi$ maps to $e$ and $\sigma(e)=e$, $\ker\phi\subseteq \ker\sigma\phi$.

    By the first isomorphism theorem, we know that $G/\ker\phi\cong\phi(g)$ and thus $|G/\ker\phi|=|H|$. By the same logic, $|G/\ker\sigma\phi|=|K|$. Then we can determine that
    $$
        \begin{aligned}
            \lbrack\ker\sigma\phi : \ker\phi\rbrack
            & = \left|\frac{\ker\sigma\phi}{\ker\phi}\right| \\
            & = \left|\frac{G\ker\sigma\phi}{G\ker\phi}\right| \\
            & = \left|\frac{G}{\ker\phi}\frac{\ker\sigma\phi}{G}\right| \\
            & = \left|\frac{G}{\ker\phi}\right|\left|\frac{\ker\sigma\phi}{G}\right| \\
            & = \frac{|H|}{|K|}
        \end{aligned}
    $$

\

8) Let $G$ be a group of permutations. For each $\sigma$ in $G$, define
    $$
        \text{sgn}(\sigma) =\begin{cases}
            +1 \text{ if $\sigma$ is an even permutation,} \\
            -1 \text{ if $\sigma$ is an odd permutation.}
        \end{cases}
    $$
    Prove that sgn is a homomorphism from $G$ to the multiplicative group $\{-1, 1\}$. What is the kernel? Why does this homomorphism allow you to conclude that $A_n$ is a normal subgroup of $S_n$ of index 2? Why does this prove Exercise 27 of Chapter 5?

    Let $x\in S_n$ be even and $y\in S_n$ be odd. Then $\text{sgn}(xx)=\text{sgn}(yy)=1=\text{sgn}(x)\text{sgn}(x)=\text{sgn}(y)\text{sgn}(y)$ and $\text{sgn}(xy)=\text{sgn}(yx)=-1=\text{sgn}(x)\text{sgn}(y)=\text{sgn}(y)\text{sgn}(x)$. Thus, sgn is a homomorphism.

    The kernel of this homomorphism is all even permutations, $A_n$.

    All subgroups of index 2 are normal, and sgn shows that $A_n$ has an index of 2 in $S_n$.

    This homomorphism trivializes Exercise 30 from Chapter 3, because all elements which map to -1 can multiply with all elements which map to 1, and this must result in -1.

\

10) Let $G$ be a subgroup of some dihedral group. For each $x$ in $G$, define
    $$
        \phi(x)=\begin{cases}
            +1 \text{ if $x$ is a rotation,} \\
            -1 \text{ if $x$ is a reflection.}
        \end{cases}
    $$
    Prove that $\phi$ is a homomorphism from $G$ to the multiplicative group $\{-1, 1\}$. What is the kernel? Why does this prove Exercise 30 from Chapter 3?

    We know that the application of two subsequent rotations results in a rotation, and the application of two reflections also results in a rotation. The only way to acheive a reflection with two subsequent applications is with one rotation and one reflection. This shows that $\phi(xy)=\phi(x)\phi(y)$.

    The Kernel of this homomorphism is the set of all rotations.

    This homomorphism trivializes Exercise 30 from Chapter 3, because all elements which map to -1 can multiply with all elements which map to 1, and this must result in -1.

\

14) Explain why the correspondence of $x\to 3x$ from $\mathbb{Z}_{12}$ to $\mathbb{Z}_{10}$ is not a homomorphism.

    Let $\varphi:\mathbb{Z}_{12}\to\mathbb{Z}_{10}=x\to 3x$. Then $\phi(6+6)=\phi(0)=0$ but $\phi(6)+\phi(6)=8+8=6\ (\mod 10)$. Therefore, $\varphi$ is not a homomorphism.

\

19) Suppose there is a homomorphism $\phi$ from $\mathbb{Z}_{17}$ to some group and that $\phi$ is not one-to-one. Determine $\phi$.

    Let $G$ be the group that is being mapped to by $\phi$. Since $\phi$ is not one-to-one, $|G|\neq 17$. However, $|G|\big||\mathbb{Z}_{17}|=17$. Since 17 is a prime number, $|G|$ must be 1. Thus, $\varphi(n)=e'\forall n\in \mathbb{Z}_{17}$.