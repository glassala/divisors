# Quotient rings

*Quotient rings. Maximal ideals. Finite fields. Polynomials over finite fields. Field with four elements.*

1. Given a commutative ring $R$ and an ideal $I$ in $R$, there exists a *quotient ring* $R/I$ whose elements are the cosets induced by $I$.

2. The equivalence relation which partitions $R$ into $R/I$ can be defined such that for $a, b \in R$, $a \sim b \iff a - b \in I$.

3. If $a \sim b$ is the case, then we can write $a \equiv b \pmod{I}$.

4. The elements of a quotient ring $R/I$ are equivalence classes in the form $[a] = a + I = \set{a + k \mid k \in I}$.

5. For $R/I$, if $a, b \in R$, then addition is in the form $(a + I) + (b + I) = (a + b) + I$.

6. Likewise, multiplication is in the form $(a + I)(b + I) = ab + I$.

7. From this definition, it is apparent that $R/I$ inherits the property of being a commutative ring from $R$.

8. Suppose $R$ is an integral domain and $I$ is a *non-prime* ideal of $R.$

9. Then, $R/I$ is not an integral domain.

10. Since $I$ is not prime, there exists a product $ab \in I$ such that $a \notin I$ and $b \notin I$.

11. So, there exist classes $[a], [b] \in R/I$ where $[a] \neq [0]$ and $[b] \neq [0]$ but $[a][b] = [0]$.

12. For example, take $\mathbb{Z}/(4)$ (which we can write $\mathbb{Z}/4\mathbb{Z}$).

13. $2$ is not a multiple of $4$ so it is not in $(4)$, so $2 + (4) \neq 0 + (4)$.

14. However, $(2 + (4))(2 + (4)) = 4 + (4)$, where, since $4$ is obviously in $(4)$, i.e. $4 + (4) = 0 + (4)$, the class $[2]$ is a zero divisor in $\mathbb{Z}/4\mathbb{Z}.$

15. If $R$ is a ring and $I$ is a proper ideal of $R$, then $I$ is a *maximal ideal* if there exists no proper ideal $J$ of $R$ such that $I \subset J \subset R$.

16. If $K$ is a field, the only proper ideal in $K$ is the zero ideal, so $(0)$ is maximal in $K$.

17. All maximal ideals are prime ideals.

18. Suppose $I$ is maximal in $R$, where $ab \in I$ for $a, b \in R$ and $a \notin I$.

19. Then, $I + (\mathnormal{a}) = \set{m + a' \mid m \in I \land a' \in (a)}$ is an ideal which strictly contains $I$.

20. Since $I$ is maximal and $I \subset I + (a)$, $I + (\mathnormal{a})$ is the whole ring $R$.

21. Since $I + (\mathnormal{a})$ is the unit ideal, there is an $m \in I$ and some $r \in R$ such that $m + ra = 1$.

22. If we multiply $m + ra = 1$ by $b$, we get $mb + rab = b$.

23. By the definition of ideals, since $r \in R$ and $ab \in I$, $rab \in I$.

24. Since $m \in I$ and $b \in R$, $mb \in I$.

25. Since $mb$ and $rab$ are in $I$, $mb + rab = b$ is in $I$, meaning $I$ is prime.

26. The converse, that all prime ideals are maximal ideals, is *not* universally the case.

27. For example, $(x) \subseteq \mathbb{Z}[x]$ is prime but not maximal.

28. The ideal $(x)$ is straightforwardly the set of all integer polynomials with zero for a constant term.

29. Suppose $AB \in (x)$ for $A, B \in \mathbb{Z}[x]$, and $A$ has a non-zero constant term, i.e. $A \notin (x)$.

30. Via the definition of polynomial multiplication, if $a$ is the constant term of $A$ and $b$ is the constant term of $B$, then the constant term of $AB$ is $ab$.

31. $\mathbb{Z}[x]$ is an integral domain, so if $ab = 0$ and $a \neq 0$, then $b = 0$, and so $B \in (x)$.

32. Then, if $AB \in (x)$, then at least either $A \in (x)$ or $B \in (x)$, and $(x)$ is a prime ideal.

33. However, recall the ideal $(2, x) = \set{(P)(2) + (Q)(x) \mid P, Q \in \mathbb{Z}[x]} \subset \mathbb{Z}[x]$.

34. It is apparent that $(x) \subset (2, x) \subset \mathbb{Z}[x]$, and so $(x)$ is prime but not maximal.

35. In a principal ideal domain which is not a field, however, it *is* the case that all *non-zero* prime ideals are maximal.

36. Suppose $R$ is a principal ideal domain, and $M$ is an ideal of $R$ such that $(p) \subseteq M \subset R$ and $(p)$ is a non-zero prime ideal. Since $R$ is a principal ideal domain, $M = (m)$ for some $m \in R$.

37. It would follow that $(p) \subseteq (m)$ means that there exists some $p = mr$ for some $r \in R$.

38. So, $p \mid mr \implies p\mid m \lor p\mid r$.

39. If $p \mid m$, then, since $(p) \subseteq (m)$ and $m = pk$ for some $k \in R$, $(m) = (pk) \subseteq (p)$, it must be the case that $(p) = (m)$.

40. If $p \mid r$, then $r = pn$ for some $n \in R$, $p = rm = pnm$, one can write $p - pnm = 0$ from which it follows that $p(1 - nm) = 0$.

41. Since $R$ is an integral domain and $p$ is not $0$, it must be so that $nm = 1$ and therefore $(m)$ is the unit ideal, i.e. the whole ring.

42. So, if $R$ is a principal ideal domain but not a field, the non-zero prime ideals of $R$ coincide exactly with the maximal ideals of $R$.

43. Let $R$ be a commutative ring. *A quotient ring $R/I$ is a field if and only if $I$ is a maximal ideal of $R$.*

44. Suppose $r \in R$ but $r \notin I$, i.e. $r + I \neq 0 + I$.

45. $I$ is maximal, so $I + (r) = R$.

46. It follows that there exists some $j \in I$ and some $a \in R$ such that $j + ar = 1$.

47. Then, we can write $(j + I) + (a + I)(r + I) = 1 + I$.

48. Since $j \in I$, $j + I = 0 + I$.

49. $1 + I$ is the multiplicative identity of $R/I$, so every non-zero element of $R/I$ is a unit, and $R/I$ is a field.

50. If $K$ is a field, then $K$ has exactly one maximal ideal, which is $(0)$, and it is straightforward that $K/(0) \cong K$.

51. When $p$ is prime, $(p)$ is a maximal ideal of $\mathbb{Z}$, and so the ring $\mathbb{Z}/p\mathbb{Z}$ is a field. Since the order of $\mathbb{Z}/p\mathbb{Z}$ is finite, it is called a *finite field.*

52. The finite field of order $p$ is denoted $\mathbb{F}_p$.

53. The smallest field is $\mathbb{F}_2$, the field of order $2$.

54. Addition in $\mathbb{F}_2$ can be fully characterized as an operation where $a + b = 0$ if $a = b$ and $a + b = 1$ if $a \neq b$.

55. Multiplication in $\mathbb{F}_2$ can be fully characterized by the fact that $ab = 1$ if $a = 1$ and $b = 1$ while $ab = 0$ if $a = 0$ or $b = 0$.

56. The polynomial ring $\mathbb{F}_2[X]$ has only $1$ and $0$ as coefficients, so all terms are either powers of $X$ or the constant $1$.

57. The view of $1$ and $0$ in $\mathbb{F}_2$ as "wrap-around-at-$2$ numbers" will be treated interchangeably with the more proper view of them as the "class of odd numbers" and the "class of even numbers" for convenience.

58. Upper case $X$ is used here as the formal indeterminate to more directly emphasize that we are not interested in the *solutions*to polynomial equations over $\mathbb{F}_2$.

59. The difference between $R[x]$ and $R[X]$ is purely notational, and carries no mathematical significance.

60. This is motivated by the fact that the infinitely many unique univariate polynomials in $\mathbb{Z}[x]$, for example, correspond to the infinitely many unique polynomial functions of a single integer.

61. There are also infinitely many polynomials in $\mathbb{F}_2[X]$, but if $x \in \mathbb{F}_2$, then there are exactly four unique univariate functions of $x$.

62. Namely, $f(x) = 0$, $f(x) = 1$, $f(x) = x$, and $f(x) = x + 1$.

63. Though coefficients of the terms of polynomials in $\mathbb{F}_2[X]$ are limited to the $0$ and $1$ classes, the *powers* to which formal indeterminates can be raised are still taken from the natural numbers.

64. It is straightforward that $x^n = x$ for all $x \in \mathbb{F}_2$ and all $n \in \mathbb{Z}^+$.

65. So, if, for $P, Q \in \mathbb{F}_2[X]$, $P = X^2 + X + 1$ and $Q = X^3 + X + 1$, $P$ and $Q$ are fully distinct polynomials, even though from the "function on elements of $\mathbb{F}_2$" perspective, $P(x) = x^2 + x + 1$ and $Q(x) = x^3 + x + 1$define exactly the same map $\mathbb{F}_2 \to \mathbb{F}_2$ as the constant function $f(x) = 1$.

66. The particularities of arithmetic of "parity classes" in $\mathbb{F}_2$ reveal themselves in the factorization of polynomials in $\mathbb{F}_2[X]$.

67. In $\mathbb{F}_2$, addition is the same as subtraction because $0$ and $1$ are each their own additive inverse.

68. So, a polynomial like $X^2 + 1$, while irreducible over $\mathbb{Z}$, can be factored into $(X + 1)(X + 1)$ over $\mathbb{F}_2$.

69. Intuitively, consider that over the integers, $(X + 1)(X + 1) = X^2 + 2X + 1$.

70. Since the linear term of $X^2 + 2X + 1$ is $2X$, and $2 \equiv 0 \pmod{2}$, $2X$ effectively "vanishes" in $\mathbb{F}_2[X]$.

71. $\mathbb{F}_2[X]$ is a polynomial ring over a field, so it is a Euclidean domain.

72. As such, for $\mathbb{F}_2[X]$, every ideal is principal, factorization into irreducibles is guaranteed for non-units, irreducible elements are exactly prime elements, and non-zero prime ideals are exactly maximal ideals.

73. It follows that if $Q$ is irreducible in $\mathbb{F}_2[X]$, then $\mathbb{F}_2[X]/(Q)$ is a field.

74. The degree of $Q$ determines the order of $\mathbb{F}_2[X]/(Q)$.

75. Consider the ideal $(X) \subset \mathbb{F}_2[X]$. $X$ is irreducible, so $(X)$ is the maximal ideal of all polynomials in $\mathbb{F}_2[X]$ with $0$ for a constant term.

76. Since a constant term can be exactly either $0$ or $1$ in $\mathbb{F}_2[X]$, $(X)$ induces exactly two equivalence classes of polynomials in $\mathbb{F}_2[X]/(X),$ the class of polynomials which are in $(X)$, i.e. polynomials with $0$ for a constant term, and polynomials which have $1$ for a constant term.

77. So, taking the quotient of $\mathbb{F}_2[X]$ by $(X)$ "recovers" $\mathbb{F}_2,$ in the sense that $\mathbb{F}_2[X]/(X) \cong \mathbb{F}_2$.

78. There is exactly one irreducible polynomial of degree $2$ in $\mathbb{F}_2[X],$ $X^2 + X + 1$.

79. It would follow that $\mathbb{F}_2[X]/(X^2 + X + 1)$ is a field.

80. The ideal $(X)$ is so big that the equivalence classes it imposes on $\mathbb{F}_2[X]$ are not too arcane to understand.

81. However, how polynomials "wrap around" at $X^2 + X + 1$ may not be so immediately apparent.

82. Via the Euclidean division property for polynomials, any polynomial $A$, given a modulus $M$, has a quotient $Q$ and remainder $R$, such that $A = MQ + R$ and either $R = 0$ or $\text{deg}(R) < \text{deg}(M)$.

83. That $M$ induces a zero class on multiples of itself means that the highest degree term of $M$ can be written in terms of the additive inverses of the other terms of $M$, allowing for the reduction of $A$ into a polynomial whose degree is less than that of $M$.

84. For example, we can take advantage of the fact that $X^2 \equiv X + 1 \pmod{(X^2 + X + 1)}$.

85. Then, we can replace instances of $X^2$ with $X + 1$.

86. So, given $X^3$, we can rewrite $X(X + 1)$, $X^2 + X$, $(X + 1) + X$ to arrive at $X^3 \equiv 1 \pmod{(X^2 + X + 1)}$.

87. Since $X^4 = X(X^3),$ it is straightforward that $X^4 \equiv X \pmod{(X^2 + X + 1)}$.

88. Likewise, $X^5 = X(X^4) \equiv X^2 \equiv X + 1 \pmod{(X^2 + X + 1)}$.

89. The polynomials $0$, $1$, $X$, and $X + 1$ are exactly the four polynomials whose degree is less than that of $X^2 + X + 1$.

90. Since $(X^2 + X + 1)$ is maximal in $\mathbb{F}_2[X]$, we already know that $\mathbb{F}_2[x]/(X^2 + X + 1)$ is a field. Since this field has four elements, we denote it by $\mathbb{F}_4$.

91. In a finite field $\mathbb{F}_p[X]$, there are $p^k$ polynomials of degree less than $k$.

92. It can help to look at this from the view of a polynomial as a list of coefficients indexed by power.

93. Accounting for terms with a coefficient of $0$, for each term of a polynomial, there are $p$ choices for the coefficient of that term.

94. That is, if $k$ is the degree of a polynomial, the set of all polynomials with degree less than $k$ in $\mathbb{F}_p[X]$ is effectively the set of all ordered $k$-tuples of the form $(a_0, a_1, {...}, a_{k-1})$, where $a_i \in \mathbb{F}_p.$

95. The essential principles of products and counting tell us that if each of the $k$ indices in an ordered $k$-tuple has $p$ possible options for its entry, then there are $p^k$ possible such tuples.

96. Given $\mathbb{F}_p[X]/(Q)$, where $Q$ is an irreducible polynomial of degree $k$, $\mathbb{F}_p[X]/(Q) \cong \mathbb{F}_{p^k}$.

97. That is, the least residue system of $\mathbb{F}_p[X]/(Q)$ is the set of all polynomials in $\mathbb{F}_p[X]$ whose degree is less than $\text{deg}(Q)$.

98. Suppose $P_1, P_2 \in \mathbb{F}_p[X]/(Q)$, where $\text{deg}(P_1) < k$ and $\text{deg}(P_2) < k,$ and $P_1 \equiv P_2 \pmod{(Q)}$.

99. Then, $P_1 - P_2 \equiv 0 \pmod{(Q)}$, and so $Q$ divides their difference.

100. However, $\text{deg}(P_1 - P_2) < k$, so we can say that $P_1 = P_2$.

101. It follows, then, that if $p$ is a prime number and $k$ is the degree of an irreducible polynomial in $\mathbb{F}_{p}[X]$, that there exists a finite field $\mathbb{F}_{p^k}$ of order $p^k$.

102. If the leading coefficient of a polynomial $P$ is $1$, $P$ is said to be *monic*.

103. Let $p$ be a prime number. From Fermat's little theorem, we know that, for all $x \in \mathbb{F}_p$, $x^p - x \equiv 0 \pmod{p}$.

104. Then, $X^p - X$ factors into a product of all monic linear polynomials in $\mathbb{F}_p[X]$.

105. Suppose $a \in \mathbb{F}_p$. Since $\mathbb{F}_p$ is a field, polynomials over it have Euclidean division, and so we can write $X^p - X = (X - a)Q + R$ for polynomials $Q, R \in \mathbb{F}_p[x]$.

106. We can substitute in $a$, and, knowing that $a^p - a \equiv 0 \pmod{p},$ we can write $(a - a)Q + R \equiv 0 \pmod{p}$.

107. $(a - a)Q$ is obviously $0$, so we are left with $R \equiv 0 \pmod{p}$, meaning $X - a$ divides $X^p - X$.

108. We can use product notation to write $X^p - X = \prod_{a \in \mathbb{F}_p}(X - a)$.

109. There is a second Lagrange's theorem.

110. Suppose $P \in \mathbb{F}_p[x]$ and $\text{deg}(P) = n$ for some prime $p$. Then, either $P$ is the zero polynomial, or $P$ has at most $n$ roots.

111. If the degree of a polynomial is $0$, it has $0$ roots.

112. Assume that for $k > 0$, if a polynomial $Q \in \mathbb{F}_p[x]$ has degree $k$, it has at most $k$ roots.

113. Suppose $A \in \mathbb{F}_p[x]$ and $\text{deg}(A) = k + 1$, where $A$ has at least one root $r \in \mathbb{F}_p$.

114. Then, we know that $(x - r) \mid A$, so we can write $A = (x - r)B$ for some $B \in \mathbb{F}_p[x]$.

115. Since $\text{deg}(A) = k + 1$, the degree of $B$ must be $k$.

116. If $A$ has a root $s \neq r$, then $b$ is a root of $B$.

117. By the inductive hypothesis, $B$ has at most $k$ roots.

118. So, we can conclude that $A$ has at most $k + 1$ roots, and the degree of a non-zero polynomial in $\mathbb{F}_p[x]$ is the maximum number of roots it can have.
