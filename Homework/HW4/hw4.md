---
author: "Luke LaValva"
title: "Modern Algebra II Homework 4"
---

## Chapter 23

6) Show that $\text{cl}(a) = \{a\}$ if and only if $a\in Z(G)$.

    We know that $\text{cl}_G(a)=\{xax^{-1}|x\in G\}$. If $a\in Z(G)$, then $xax^{-1}=xx^{-1}a=ea=a$, and thus $\text{cl}(a)=\{a|x\in G\}=\{a\}$.

$%$

11) If $G$ is a group of odd order and $x\in G$, show that $x^{-1}$ is not in $\text{cl}(x)$.

    Suppose on the contrary that $x^{-1}\in\text{cl}(x)$. Then there exists some $g\in G$ such that $x^{-1}=gxg^{-1}$. With some simple algebra, we can show that
    $$
      \begin{aligned}
         x^{-1}       & =  gxg^{-1}       \\
        gx^{-1}g^{-1} & = ggxg^{-1}g^{-1} \\
         x            & = g^2xg^{-2}      \\
         x^{-1}       & = g^3xg^{-3}      \\
         x            & = g^4xg^{-4}      \\
                      & \ \ \vdots \\
         x            & = g^{2k}xg^{-2k}  \\
         x^{-1}       & = g^{2k+1}xg^{-2k+1}
      \end{aligned}
    $$
    We know that $|g|$ divides $|G|$, so $|g|$ must also be odd. Let us represent $|g|$ as $2m + 1$, where $m\in\mathbb{N}$. Therefore, if we set $k=m$ then $x^{-1} = g^{2m+1}xg^{-2m+1} = exe = x$. This cannot be except in the trivial case, so it is a contradiction.

$%$

12) Determine the class equation for non-Abelian groups of orders 39 and 55.
    $$
      \begin{aligned}
        |G| & = 39 = 3\cdot 13 \\
            & = |Z(G)| + \sum_{\text{cl}(a)\neq 1}[G:C_G(a)] \\
            & = 1 + 13 + 13 + 3 + 3 + 3 + 3
      \end{aligned}
    $$
    $$
      \begin{aligned}
        |G| & = 55 = 5\cdot 11 \\
            & = |Z(G)| + \sum_{\text{cl}(a)\neq 1}[G:C_G(a)] \\
            & = 1 + 11 + 11 + 11 + 11 + 5 + 5
      \end{aligned}
    $$

$%$

13) Determine which of the equations below could be the class equation given in the proof of Theorem 23.2. For each part, provide your reasoning.
    1)  $9  = 3+3+3$
        
        This cannot be used, because all groups of order $p^2$ are abelian and therefore $|Z(G)|=9$. Then the equation would be $9=9$.
    2)  $21 = 1+1+3+3+3+3+7$
        
        This cannot be used, because any conjugacy class of order 1 is in $Z(G)$.
    3)  $10 = 1+2+2+5$

        This is a valid class equation.
    4)  $18 = 1+3+6+8$

        This cannot be used, because $8\nmid 18$ and it cannot represent a conjugacy class.

$%$

14) Determine the class equation for $D_6$.
    $$
      \begin{aligned}
        |D_6| & = 12 = 3\cdot 2\cdot 2 \\
            & = |Z(G)| + \sum_{\text{cl}(a)\neq 1}[G:C_G(a)] \\
            & = 1 + 1 + 4 + 3 + 3
      \end{aligned}
    $$

$%$

16) If $a$ and $b$ are group elements and $i$ and $k$ are positive integers, prove that $bab^{-1}=a^i$ implies that $b^kab^{-k}=a^{i^k}$.
    $$
      \begin{aligned}
         bab^{-1}       & = a^i \\
        bbab^{-1}b^{-1} & = ba^ib^{-1} \\
        b^2ab^{-2}      & = baa\ldots aab^{-1} \\
          & = baeae\ldots eaeab^{-1} \\
          & = bab^{-1}bab^{-1}\ldots bab^{-1}bab^{-1} \\
          & = a^ia^i\ldots a^ia^i \\
          & = a^{ii} =a^{i^2} \\
        b^3ab^{-3}      & = a^{iii} = a^{i^3} \\
        b^kab^{-k}      & = a^{i^k}
      \end{aligned}
    $$

$%$

21) Suppose that $G$ is a group of order 168. If $G$ has more than one Sylow 7-subgroup, exactly how many does it have?
    
    Sylow's Third Theorem states that if 7 divides $|G|$, then the number of Sylow 7-subgroups must divide $168/7=24$ and it must be equal to $1\mod 7$. Thus, if $|G|\neq 1$ it must be $8$.

$%$

22) Show that every group of order 56 has a proper nontrivial normal subgroup.

    $|G|=56=2^3\cdot 7$. By Sylow's Third Theorem, we know that the number of Sylow 2-subgroups $s_2$ must be equal to either 1 or 7 and the number of Sylow 7-subgroups $s_7$ must be equal to either 1 or 8.
    
    If $s_7=1$, then there is a proper nontrivial subgroup because all unique Sylow $p$-subgroups are normal.

    If $s_7=8$, then there must be $6\cdot 8=48$ elements of order 7. Then since the identity has order 1, there are $56-48-1=7$ elements left that have an order of $2^k$. Then $s_2=1$, so it must be normal.

$%$

23) What is the smallest composite integer $n$ such that there is a unique group of order $n$?

    All even numbers have both cyclic and dihedral groups, so $n$ cannot be even. It cannot be 9 because $\mathbb{Z}_9$ and $\mathbb{Z}_3\oplus\mathbb{Z}_3$ are distinct. Let us assume, then, that $n=15$.

    $|G| = 15 = 3\cdot 5$. By Sylow's third theorem, we know that $s_3$ must divide $5$ and be equal to $1\mod 3$, so it can only be $1$. In addition, $s_5$ must divide $3$ and be divisible by $1\mod 5$, so it must also be equal to 1. Therefore, there is only 1 conjugacy class of order 15.

$%$

24) Let $G$ be a noncyclic group of order 21. How many Sylow 3-subgroups does $G$ have?

    By Sylow's third theorem, we know that the number of Sylow 3-subgroups $s_3$ must divide 7 and it must be divisible by 1 mod 3. Therefore, $s_3$ must be equal to either 1 or 7.
    
    If $s_3$ is 1 then there must be 2 elements of order 3, and this is not possible if $|Z(G)|=1$ because then the class equation would be impossible to fill. Therefore, if $s_3$ is 1 the group is Abelian.

    Thus, $s_3$ must be equal to 7.

$%$

27) What do the Sylow theorems tell you about any group of order 100?

    $100=2^2+5^2$. By Sylow's third theorem, the number of Sylow 2-subgroups $s_2$ must be divisible by 25 and be equal to $1\mod 2$. Thus, $s_2$ must be equal to 1, 5, or 25. Using the same theorem, $s_5$ can only be equal to 1.

    Since there is only one Sylow 5-subgroup, it is a subgroup of order 25 and it must be normal.

    Based on this information, we know that there is 1 element of order 1 (the identity), 24 elements of order 5 or 25, and 75 elements of order 2 or 4. 

$%$

28) Prove that a group of order 175 is Abelian.

    Sylow's third theorem tells us that if $|G|=175=5^2\cdot 7$ then the number of Sylow 5-subgroups $s_5$ in $G$ must be divisible by 7 and be congruent to $1\mod 5$. This is only true when $s_5=1$. In addition, $s_7$ must be divisible by 25 and congruent to $1\mod 7$. This is only true when $s_7=1$. All distinct Sylow $p$-subgroups are normal, so $G$ can be represented as the product of two Abelian groups. Thus, $G$ must be abelian.

$%$

35) Without using Theorem 23.6, prove that a group of order 15 is cyclic.

    By Sylow's third theorem, we know that if $|G|=15=5\cdot 3$ then the number of Sylow 5-subgroups $s_5$ and 3-subgroups $s_3$ in $G$ must both be equal to 1. Since all unique Sylow $p$-subgroups are normal, $G$ may be represented as the product of two Abelian groups. We also know that $G$ must have 1 element of order 1, 2 of order 3, and 4 of order 5. Then there must be $15-1-2-4=8$ elements of order 15, so $G$ must be cyclic.

$%$

37) Prove that a group of order 595 has a normal Sylow 17-subgroup.

    By Sylow's third theorem, if $|G|=595=5\cdot 7\cdot 17$ then the number of Sylow 17-subgroups $s_{17}$ in $G$ must be divisible by 35 and congruent to $1\mod 17$. Therefore, $s_{17}$ can be either 1 or 35.

    Suppose that $s_{17}=35$. Then the number of elements with order 17 must be equal to $16\cdot 35=560$. By Sylow's third theorem, we know that $s_5$ must be 1. This tells us that there exists a normal subgroup of $G$ that has an order of 5. Then $_{17}S_1\times\ _5S_1$ forms a cyclic subgroup of order 85. This subgroup must have 1 element of order 1, 4 of order 5, 16 of order 17, and $85-17-4-1=63$ elements of order 85. However, this tells us that $|G|\geq 1+560+4+63=628>595$. Obviously, this cannot be true. Contradiction!

    Thus, $s_{17}=1$.

$%$

39) Show that the center of a group of order 60 cannot have order 4.

    Since $|Z(G)|=4$, we know that $|G/Z(G)|=60/4=15$. We know from exercise 35 that this must a cyclic group. Then by the $G/Z$ theorem, $G$ must be Abelian. However, if $G$ is Abelian then $Z(G)=G$. $60\neq 4$. Contradiction!

$%$

40) Suppose that $G$ is a group of order 60 and $G$ has a normal subgroup $N$ of order 2. Show that
    1) $G$ has normal subgroups of orders 6, 10, and 30.

        Let $H=G/N$. Then $|N|=30=5\cdot 3\cdot 2$. By Sylow's third theorem, $N$ has either 1 or 10 Sylow 3-subgroups and either 1 or 6 Sylow 5-subgroups. These cannot both be non-unique, because $4\times 6 + 2\times 10>30$. Thus, there exists a unique Sylow $p$-subgroup that is Abelian of order 3 or order 5. Then $K=\ _3S_1\times\ _5S_1\leq N$ and $|K|=15$. All groups of order 15 are Abelian, and since $[K:H]=2$, we know that $K\triangleleft H$.

        Since $K\triangleleft H$ and $|K|=15$, there must also be subgroups $K_3, K_5\leq K\leq H$ such that $|K_3|=3$ and $|K_5|=5$. Thus, $H$ has normal subgroups of orders 3, 5, and 15.

        I don't fully understand the next step, but my understanding is that the subgroups of $H$ can be brought into $G$ and multiplied by $N$ to get normal subgroups of orders 6, 10, and 30.

    2) $G$ has subgroups of orders 12 and 20.

        Since there are normal subgroups of order 6 and 10 which we will label $X$ and $T$, respectively, and at least one Sylow 2-subgroup $_2S_1$, we can find $|X\times\ _2S_1|=12$ and $|T\times\ _2S_1|=20$
    3) $G$ has a cyclic subgroup of order 30.

        Since there is a normal subgroup of order 30, we already know that it is Abelian. To show that it is cyclic we need to find one element within the subgroup that has an order of 30. This is trivially true.

$%$

54) Let $G$ be a group of order $p^2q^2$, where $p$ and $q$ are distinct primes, $q\nshortmid p^2-1$, and $p\nshortmid q^2-1$. Prove that $G$ is Abelian. List three pairs of primes that satisfy these conditions.

    I don't know where to begin with proving that this is an Abelian group, but I can certainly list three pairs of primes that satisfy these conditions:
    $$
      \begin{aligned}
        5  & , 7  \\
        7  & , 11 \\
        11 & , 13 
      \end{aligned}
    $$

$%$

57) Show that a group of order 12 cannot have nine elements of order 2.

    By Sylow's second theorem, we know that any subgroup of order 2 must be contained within a Sylow 2-subgroup of order 2. Since $|G|=12$, these Sylow 2-subgroups each have an order of 4. By Sylow's third theorem, we know that there are either 1 or 3 Sylow 2-subgroups. Since each of these subgroups contains 3 elements and there are more than 3 elements of order 2, we can be certain that there are 3 Sylow 2-subgroups. Each of these subgroups contains at least 1 element of order 4, so this group must at least have 9 elements of order 2, 3 of order 4, and 1 of order 1 (the identity). However, $9+3+1=13>12$. This cannot be! Contradiction!