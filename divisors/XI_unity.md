# Roots of unity

*Algebraic numbers. Roots of unity. Cyclotomic polynomials. Eisenstein's criterion. Product formula for Möbius inversion. Quadratic Gauss sums.*

1. An *algebraic number* is a root of a single-variable rational polynomial.

2. Let $\set{P_1, P_2, P_3, {...}}$ be the set of all irreducible monic polynomials in $\mathbb{Q}$ such that $\text{deg}(P_i) > 1.$

3. Let $K_i$ be the splitting field of $P_i$ over $K_{i-1}$ for $i > 0$ where $\mathbb{Q} = K_0.$

4. If we take the infinite chain of fields $\mathbb{Q} = K_0 \subseteq K_1 \subseteq K_2 \subseteq {...},$ then for any polynomial $P$ in $\mathbb{Q}[x]$ which is irreducible over $\mathbb{Q},$ there exists some $n$ such that $P$ splits in $K_n.$

5. We can then define the set of all algebraic numbers to be $\overline{\mathbb{Q}} = \bigcup^{\infty}_{n = 0}K_n$ which is a field by induction.

6. An algebraic number $\zeta$ which satisfies the equation $\zeta^n = 1$ is called an *$n$-th root of unity.*

7. It follows that if $\zeta^n = 1,$ then $|\zeta| = 1.$

8. If $\zeta$ satisfies $\zeta^n = 1$ but satisfies no equation $\zeta^m = 1$ for positive integers $m < n,$ then $\zeta$ is a *primitive* $n$-th root of unity.

9. An integer power of an $n$-th root of unity is a root of unity.

10. That is, $(\zeta^k)^n = \zeta^{kn} = (\zeta^{n})^k = 1^k.$

11. The reciprocal $\zeta^{-n} = \frac{1}{\zeta^n}$ of a root of unity is also a root of unity, and is the conjugate of $\zeta^n,$ where $\zeta^n \zeta^{-n} = \zeta^{n-n} = 1.$

12. Powers of roots of unity are periodic: if $\zeta$ is an $n$-th root of unity and $a \equiv r \pmod n,$ then $\zeta^a = \zeta^r.$

13. That is, by Euclid's division lemma, we can write $a = qn + r,$ so $\zeta^a = \zeta^{qn + r} = (\zeta^{n})^q \zeta^{r} = \zeta^r.$

14. This implies that each $n$-th root of unity $\zeta^k$ is distinct for integers $0 \le k < n$, and we can be sure that there are exactly $n$ $n$-th roots of unity, since there are at most $n$ roots of a polynomial over a field.

15. It follows from all of this that for primitive $n$-th roots of unity $\zeta^a = \zeta^b \iff a \equiv b \pmod{n}.$

16. If $\zeta$ is not primitive as an $n$-th root of unity, i.e if $0 < m < n$and $\zeta^m = 1,$ then there exists an integer $k$ such that $n = mk,$ and $\zeta^m = \zeta^{mk} = (\zeta^m)^k = \zeta^n$ but $m \not\equiv 0 \pmod{n}.$

17. The set of all $n$-th roots of unity is a cyclic group under multiplication whose generators are the primitive roots of unity.

18. We will denote this group $\mu_n.$

19. If $\zeta^n = 1$ for a primitive $\zeta$ and $\gcd(k, n) = 1,$ then $\zeta^k$ is a generator of this group.

20. That is, consider the map $\rho: \mu_n \to \mathbb{Z}/n\mathbb{Z}^+$ defined as $\rho(\zeta^k) = [k].$

21. The laws of exponentiation tell us that $\rho$ is an isomorphism between groups.

22. It follows that the number of primitive $n$-th roots of unity is given by $\varphi(n).$

23. If $\zeta^n = 1$ and $\omega^m = 1,$ and $k = \text{lcm}(n, m),$ then $(\zeta\omega)^k = 1.$

24. That is, if we can write $k = tn$ and $k = sm$ for integers $t, s,$ then $\zeta^k = (\zeta^n)^t = 1$ and $\omega^k = (\omega^m)^s = 1.$

25. As such, roots of unity are closed under multiplication in general.

26. $1$ is obviously the identity, and for any root of unity $\zeta,$ $\zeta^n\zeta^{-n} = 1.$

27. Then, it is easy to see that the set of all roots of unity is an abelian group under multiplication.

28. The polynomial $x^n - 1$ is not irreducible for $n > 1.$

29. If $k$ divides $n$ for positive integers $k$ and $n,$ then $x^k - 1 \mid x^n - 1.$

30. So, for some positive integer $m,$ $x^n - 1 = (x^k)^m - 1.$

31. Over $\overline{\mathbb{Q}},$ $x^n - 1$ factors into $(x - 1)(x^{n-1} + x^{n-2} + {...} + 1).$

32. It follows that we can write $(x^k)^m - 1$ as $(x^k - 1)((x^k)^{m-1} + (x^k)^{m-2} + {...} + 1).$

33. Likewise, if $x^k - 1$ divides $x^n - 1,$ then $k \mid n.$

34. That is, $x^k - 1$ dividing $x^n - 1$ necessitates that the $k$-th roots of unity must also be $n$-th roots of unity.

35. Therefore, $k \mid n \iff x^k - 1 \mid x^n - 1.$

36. The $n$-th *cyclotomic polynomial* $\Phi_n$ is the unique irreducible polynomial with integer coefficients which divides $x^n - 1$ but not $x^k - 1$ for any $k < n.$

37. If $\zeta$ is a primitive $n$-th root of unity, then $\Phi_n$ is the minimal polynomial of $\zeta$ over $\mathbb{Q}[x].$

38. The degree of $\Phi_n$ is given by the number of primitive $n$-th roots of unity, and is therefore equal to $\varphi(n).$

39. Where $k \bot {n}$ means $\gcd(k, n) = 1$ and $\zeta^n = 1,$ $\Phi_n$ can be written in the form $\Phi_n = \prod_{k \bot n}^{1 \le k \le n}(x - \zeta^k).$

40. It is straightforward that $\Phi_1 = x - 1,$ since the only first root of unity is $1.$

41. Likewise, difference-of-squares factorization tells us that $x^2 - 1$ factors into $(x - 1)(x + 1).$ Since $1$ is not a primitive 2nd root of unity but $-1$ is, $\Phi_2 = x + 1.$

42. Consider $\Phi_p$ for odd prime $p.$ The only non-primitive $p$-th root is $1,$ so $x^p - 1 = (x - 1)\Phi_p.$

43. The polynomial which satisfies this relationship is exactly $\sum^{p-1}_{k=0}x^k.$

44. We can verify that this polynomial is irreducible by using *Eisenstein's criterion.*

45. Suppose $Q \in \mathbb{Z}[x]$ and $Q = k_nx^n + k_{n-1}x^{n-1} + {...} + k_0.$

46. Then, if there exists a prime number $p$ such that for all non-negative integers $i < n,$ $p \mid k_i,$ but $p \nmid k_n$ and $p^2 \nmid k_0,$ then $Q$ is irreducible over $\mathbb{Q}[x],$ and the primitive part of $Q$ is irreducible over $\mathbb{Z}[x].$

47. Suppose for an arbitrary prime number $p,$ $Q$ meets these conditions but is reducible over the rationals.

48. Then, $Q = AB$ for non-unit polynomials $A, B \in \mathbb{Z}[x].$

49. We can then say that $Q \equiv kx^n \pmod{p}$ for some non-zero residue class $k \in \mathbb{F}_p.$

50. However, $\mathbb{F}_p[x]$ is a unique factorization domain, so $AB \equiv ax^n \pmod{p},$ and both $A$ and $B$ must be monomials modulo $p,$ meaning $p$ divides the constant terms $a_0, b_0$ of both $A$ and $B.$

51. Since $k_0 = a_0b_0,$ then, $p^2 \mid k_0,$ meaning $Q$ is irreducible over the rationals.

52. This criterion may seem to not be especially relevant to a class of polynomials whose coefficients are all $1,$ but one may perform a change of variables in order to exploit the binomial theorem.

53. That is, if we set $x = y + 1,$ then we can write $\sum^{p-1}_{k=0}x^k$ as $\sum^{p}_{k = 1}\binom{p}{p-k}y^{k-1},$ which satisfies Eisenstein's criterion and is therefore irreducible.

54. As such, $\Phi_p = \sum^{p-1}_{k=0}x^k.$

55. It follows from the definition of a cyclotomic polynomial that $x^n - 1 = \prod_{d \mid n}\Phi_d(x).$

56. That is, an $n$-th root of unity $\zeta$ has order $d$ if and only if $d$ is the smallest divisor of $n$ such that $\zeta^d = 1.$

57. So, the roots of order $d$ have the minimal polynomial $\Phi_d.$

58. The $n$-th roots of unity comprise the union of the $d$-th roots of unity for all $d \mid n.$

59. The primitive $d$-th roots of unity are exactly the roots of $\Phi_d.$

60. That only *primitive* roots of unity are the roots of a given $\Phi_d$means that the set of roots of one cyclotomic polynomial must be disjoint from the set of roots of any other.

61. So, the roots of the product of all $\Phi_d$ given $d \mid n$ are exactly the $n$-th roots of unity.

62. The formula $x^n - 1 = \prod_{d \mid n}\Phi_d(x)$ leads one to the natural conclusion that if one factors the cyclotomic polynomials indexed at *proper* divisors $d$ of $n$ out of $x^n - 1,$ the resulting polynomial has roots which are precisely the primitive $n$-th roots of unity.

63. Therefore, we can recursively find $\Phi_n$ by taking $\Phi_n = \frac{x^n - 1}{\prod_{d \mid n}^{d \neq n}\Phi_d}.$

64. It follows from this formula that, for example, $\Phi_{2^n} = x^{2^{n-1}} + 1.$

65. Möbius inversion admits a product form.

66. If $a^x = y,$ then we say the *base-$a$ logarithm* is $\log_a(y) = x.$

67. The laws of exponentiation then tell us that $\log_a(nm) = \log_a(n) + \log_a(m).$

68. Suppose an arithmetic function $G$ can be written as $G(n) = \prod_{d \mid n}F(d)$ for some arithmetic function $F.$

69. Then, for some arbitrary base $a,$ we can write $\log_a(G(n)) = \sum_{d \mid n}\log_a(F(d)).$

70. Recall that Möbius inversion takes a function of positive integers of the form $g(n) = \sum_{d \mid n}f(d)$ and "recovers" $f(n)$ as $f(n) = \sum_{d \mid n}g(d)\mu(\frac{n}{d}).$

71. As such, we can write $\log_a(F(n)) = \sum_{d \mid n}\log_a(G(d))\mu(\frac{n}{d}).$

72. Then, if we take $a$ to the power of this expression, we find $F(n) = \prod_{d \mid n}G(d)^{\mu(\frac{n}{d})}.$

73. Since $x^n - 1 = \prod_{d \mid n}\Phi_d(x),$ Möbius inversion tells us that we can write the $n$-th cyclotomic polynomial as $\Phi_n(x) = \prod_{d \mid n}(x^d - 1)^{\mu(\frac{n}{d})}.$

74. Let $p$ be an odd prime. Then, $\Phi_{2p} = \sum_{k=0}^{p-1}(-x)^k.$

75. First, observe that $x^{2p} - 1 = (x^p + 1)(x^p - 1).$

76. So, none of the roots of $x^p - 1$ are roots of $\Phi_{2p}.$

77. Then, we have the factorization $x^p + 1 = (x + 1)\sum_{k=0}^{p-1}(-x)^k.$

78. Since $\Phi_2 = x + 1$ and Eisenstein's criterion (using $x = y + 1$) tells us that $\sum_{k=0}^{p-1}(-x)^k$ is irreducible, it must be the case that $\Phi_{2p} = \sum_{k=0}^{p-1}(-x)^k.$

79. Suppose $a \equiv 0 \pmod{p}.$ Then, $\sum^{p-1}_{n=0}\zeta^{an}_p = p.$ Otherwise, $\sum^{p-1}_{n=0}\zeta^{an}_p = 0.$

80. That is, if $a \equiv 0 \pmod{p},$ then $\zeta^a_p = 1.$

81. If $a \not\equiv 0 \pmod{p},$ then $\zeta^a_p \neq 1$ and so $\sum^{p-1}_{k=0}\zeta^{ak}_p = \frac{\zeta^{ap}_p - 1}{\zeta^{a}_p - 1} = 0.$

82. It then follows that $\frac{1}{p}\sum^{p-1}_{k=0}\zeta_p^{k(a-b)} = \delta_{ab},$ where $\delta_{ab} = 1$ if $a\equiv b \pmod{p}$ and $\delta_{ab} = 0$ otherwise.

83. Let $(\frac{a}{p})$ be the Legendre symbol, where $p$ is an odd prime and $a \in \mathbb{F}_p.$

84. Then, $\sum^{p-1}_{n=0}(\frac{a}{p}) = 0.$ This follows from $(\frac{0}{p}) = 0$ and there being as many quadratic residues as non-residues modulo $p.$

85. A *quadratic Gauss sum* $\gamma$ is a sum of the form $\gamma(a, p) = \sum^{p-1}_{n=0}(\frac{k}{p})\zeta^{ak}_p$ where $p$ is an odd prime, $a$ is an integer, and $\zeta_p$ is a primitive $p$-th root of unity.

86. If $p \mid a,$ then $\zeta^{ak}_p = 1$ and so $\gamma(a, p) = p.$

87. We can reduce the general case of a quadratic Gauss sum to the following form: $\gamma(a, p) = (\frac{a}{p})\gamma(1, p).$

88. Since $a$ is a unit, we can comfortably map $k$ to $a^{-1}k,$ and transform $\sum^{p-1}_{k=0}(\frac{k}{p})\zeta^{ak}_p$ into $\sum^{p-1}_{k=0}(\frac{a^{-1}k}{p})\zeta^{k}_p.$

89. Since $(\frac{a^{-1}k}{p}) = (\frac{a^{-1}}{p})(\frac{k}{p})$ and $(\frac{a^{-1}}{p}) = (\frac{a}{p}),$ we can rearrange $\sum^{p-1}_{k=0}(\frac{a^{-1}k}{p})\zeta^{k}_p$into $(\frac{a}{p})\sum^{p-1}_{k=0}(\frac{k}{p})\zeta^{k}_p.$

90. As such, we can write $\sum^{p-1}_{k=0}(\frac{k}{p})\zeta^{ak}_p = (\frac{a}{p})\sum^{p-1}_{k=0}(\frac{k}{p})\zeta^{k}_p,$ i.e. $\gamma(a, p) = (\frac{a}{p})\gamma(1, p).$

91. The square of a Gauss sum can be written as $\gamma(a, p)^2 = (-1)^{\frac{p-1}{2}}p.$

92. First, it follows that $\gamma(a, p)\gamma(-a, p) = (\frac{a}{p})(\frac{-a}{p})\gamma(1, p)^2 = (\frac{-1}{p})\gamma(1, p)^2.$

93. Then, $\sum^{p-1}_{a = 0}\gamma(a, p)\gamma(-a, p) = (\frac{-1}{p})(p-1)\gamma(1, p)^2.$

94. Moreover, $\gamma(a, p)\gamma(-a, p) = \sum^{p-1}_{x=0}\sum^{p-1}_{y=0}(\frac{x}{p})(\frac{y}{p})\zeta^{a(x-y)}_p.$

95. As such, $\sum^{p-1}_{a=0}\gamma(a, p)\gamma(-a, p) = \sum^{p-1}_{x=0}\sum^{p-1}_{y=0}(\frac{x}{p})(\frac{y}{p})\delta_{xy}p = (p-1)p.$

96. So, $(\frac{-1}{p})(p-1)\gamma(1, p)^2 = (p-1)p.$

97. Finally, we can then write $\gamma(1, p)^2 = (\frac{-1}{p})p = (-1)^{\frac{p-1}{2}}p.$

98. Since $(\frac{a}{p})^2 = 1$ for non-zero $a,$ the case of $\gamma(1, p)^2$ is the same as that of $\gamma(a, p)^2.$

99. In the following section we will use $\gamma$ as shorthand for $\gamma(1, p)$ and $\gamma_n = \gamma(n, p).$

100. Let $p \neq q$ be odd primes and let $s = \gamma^2 = (-1)^{\frac{p-1}{2}}p.$

101. Then, $\gamma^{q-1} = s^{\frac{q-1}{2}}.$

102. As such, $\gamma^{q-1} \equiv (\frac{s}{q}) \pmod{q}.$

103. It follows that $\gamma^q \equiv (\frac{s}{q})\gamma \pmod{q}.$

104. By the freshman's dream and a reindexing/change of variables, we can write $\gamma^q = (\sum^{p-1}_{k=0}(\frac{k}{p})\zeta_p^{k})^q \equiv \sum_{k=0}^{p-1}(\frac{k}{p})^q\zeta_p^{qk} \equiv \gamma_q \pmod{q}.$

105. So, $(\frac{q}{p})\gamma \equiv (\frac{s}{q})\gamma \pmod{q}.$

106. Then, if we multiply both sides of the congruence by $\gamma,$ we get $(\frac{q}{p})s \equiv (\frac{s}{q})s \pmod{q}$ and so $(\frac{q}{p}) \equiv (\frac{s}{q}) \pmod{q}.$

107. Because of the values the Legendre symbol takes, then, $(\frac{q}{p}) = (\frac{s}{q}).$

108. Note that $(\frac{s}{q})$ can be expanded into $(\frac{(-1)^{\frac{p-1}{2}}p}{q}).$

109. By multiplicativity of the Legendre symbol, $(\frac{(-1)^{\frac{p-1}{2}}p}{q}). = (\frac{(-1)^{\frac{p-1}{2}}}{q})(\frac{p}{q}).$

110. Then, $(\frac{(-1)^{\frac{p-1}{2}}}{q}) = (\frac{-1}{q})^{\frac{p-1}{2}} = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}.$

111. As such, $(\frac{q}{p}) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}(\frac{p}{q}).$

112. So, we can finally write $(\frac{p}{q})(\frac{q}{p}) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}.$
