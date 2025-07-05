# Quotient rings

*Quotient rings. Maximal ideals. Finite fields. Polynomials over finite fields. Field with four elements. Gaussian integers. Norm of a Gaussian integer. Fermat's Christmas theorem. Euclid's formula for Pythagorean triples.*

1. Given a commutative ring $R$ and an ideal $I$ in $R$, there exists a *quotient ring* $R/I$ whose elements are the cosets induced by $I$.

2. The equivalence relation which partitions $R$ into $R/I$ can be defined such that for $a, b \in R$, $a \sim b \iff a - b \in I$.

3. If $a \sim b$ is the case, then we can write $a \equiv b \pmod{I}$.

4. The elements of a quotient ring $R/I$ are equivalence classes in the form $[a] = a + I = \set{a + k \mid k \in I}$.

5. For $R/I$, if $a, b \in R$, then addition is in the form $(a + I) + (b + I) = (a + b) + I$.

6. Likewise, multiplication is in the form $(a + I)(b + I) = ab + I$.

7. From this definition, it is apparent that $R/I$ inherits the property of being a commutative ring from $R$.

8. Recall the construction of the field of fractions of an integral domain $R$: let $R' = R \setminus \set{0}$. Then, there is an equivalence relation $Q$ which one can impose on $R \times R'$, defined where $(a, b) \sim (x, y)$ if and only if $ay = bx$.

9. Then $(R \times R') / Q$ is a ring, but $Q$ is an equivalence relation and not an ideal, so $(R \times R') / Q$ is a ring over a quotient set but not a quotient ring.

10. Suppose $R$ is an integral domain and $I$ is a *non-prime* ideal of $R.$

11. Then, $R/I$ is not an integral domain.

12. Since $I$ is not prime, there exists a product $ab \in I$ such that $a \notin I$ and $b \notin I$.

13. So, there exist classes $[a], [b] \in R/I$ where $[a] \neq [0]$ and $[b] \neq [0]$ but $[a][b] = [0]$.

14. For example, take $\mathbb{Z}/(4)$ (which we can write $\mathbb{Z}/4\mathbb{Z}$).

15. $2$ is not a multiple of $4$ so it is not in $(4)$, so $2 + (4) \neq 0 + (4)$.

16. However, $(2 + (4))(2 + (4)) = 4 + (4)$, where, since $4$ is obviously in $(4)$, i.e. $4 + (4) = 0 + (4)$, the class $[2]$ is a zero divisor in $\mathbb{Z}/4\mathbb{Z}.$

17. Likewise, if $I$ is a prime ideal of an integral domain $R$, then $R/I$ is an integral domain.

18. Suppose $ab + I = 0 + I.$ Then, $ab \in I.$

19. Since $I$ is prime, either $a \in I$ or $b \in I.$

20. So, since $R$ is an integral domain and $(a + I)(b + I) = ab + I$, either $a + I = 0 + I$ or $b + I = 0 + I,$ so $R/I$ is an integral domain.

21. If $R$ is a ring and $I$ is a proper ideal of $R$, then $I$ is a *maximal ideal* if there exists no proper ideal $J$ of $R$ such that $I \subset J \subset R$.

22. If $K$ is a field, the only proper ideal in $K$ is the zero ideal, so $(0)$ is maximal in $K$.

23. All maximal ideals are prime ideals.

24. Suppose $I$ is maximal in $R$, where $ab \in I$ for $a, b \in R$ and $a \notin I$.

25. Then, $I + (\mathnormal{a}) = \set{m + a' \mid m \in I \land a' \in (a)}$ is an ideal which strictly contains $I$.

26. Since $I$ is maximal and $I \subset I + (a)$, $I + (\mathnormal{a})$ is the whole ring $R$.

27. Since $I + (\mathnormal{a})$ is the unit ideal, there is an $m \in I$ and some $r \in R$ such that $m + ra = 1$.

28. If we multiply $m + ra = 1$ by $b$, we get $mb + rab = b$.

29. By the definition of ideals, since $r \in R$ and $ab \in I$, $rab \in I$.

30. Since $m \in I$ and $b \in R$, $mb \in I$.

31. Since $mb$ and $rab$ are in $I$, $mb + rab = b$ is in $I$, meaning $I$ is prime.

32. The converse, that all prime ideals are maximal ideals, is *not* universally the case.

33. For example, $(x) \subseteq \mathbb{Z}[x]$ is prime but not maximal.

34. The ideal $(x)$ is straightforwardly the set of all integer polynomials with zero for a constant term.

35. Suppose $AB \in (x)$ for $A, B \in \mathbb{Z}[x]$, and $A$ has a non-zero constant term, i.e. $A \notin (x)$.

36. Via the definition of polynomial multiplication, if $a$ is the constant term of $A$ and $b$ is the constant term of $B$, then the constant term of $AB$ is $ab$.

37. $\mathbb{Z}[x]$ is an integral domain, so if $ab = 0$ and $a \neq 0$, then $b = 0$, and so $B \in (x)$.

38. Then, if $AB \in (x)$, then at least either $A \in (x)$ or $B \in (x)$, and $(x)$ is a prime ideal.

39. However, recall the ideal $(2, x) = \set{(P)(2) + (Q)(x) \mid P, Q \in \mathbb{Z}[x]} \subset \mathbb{Z}[x]$.

40. It is apparent that $(x) \subset (2, x) \subset \mathbb{Z}[x]$, and so $(x)$ is prime but not maximal.

41. In a principal ideal domain which is not a field, however, it *is* the case that all *non-zero* prime ideals are maximal.

42. Suppose $R$ is a principal ideal domain, and $M$ is an ideal of $R$ such that $(p) \subseteq M \subset R$ and $(p)$ is a non-zero prime ideal. Since $R$ is a principal ideal domain, $M = (m)$ for some $m \in R$.

43. It would follow that $(p) \subseteq (m)$ means that there exists some $p = mr$ for some $r \in R$.

44. So, $p \mid mr \implies p\mid m \lor p\mid r$.

45. If $p \mid m$, then, since $(p) \subseteq (m)$ and $m = pk$ for some $k \in R$, $(m) = (pk) \subseteq (p)$, it must be the case that $(p) = (m)$.

46. If $p \mid r$, then $r = pn$ for some $n \in R$, $p = rm = pnm$, one can write $p - pnm = 0$ from which it follows that $p(1 - nm) = 0$.

47. Since $R$ is an integral domain and $p$ is not $0$, it must be so that $nm = 1$ and therefore $(m)$ is the unit ideal, i.e. the whole ring.

48. So, if $R$ is a principal ideal domain but not a field, the non-zero prime ideals of $R$ coincide exactly with the maximal ideals of $R$.

49. Let $R$ be a commutative ring. *A quotient ring $R/I$ is a field if and only if $I$ is a maximal ideal of $R$.*

50. Suppose $r \in R$ but $r \notin I$, i.e. $r + I \neq 0 + I$.

51. $I$ is maximal, so $I + (r) = R$.

52. It follows that there exists some $j \in I$ and some $a \in R$ such that $j + ar = 1$.

53. Then, we can write $(j + I) + (a + I)(r + I) = 1 + I$.

54. Since $j \in I$, $j + I = 0 + I$.

55. $1 + I$ is the multiplicative identity of $R/I$, so every non-zero element of $R/I$ is a unit, and $R/I$ is a field.

56. If $K$ is a field, then $K$ has exactly one maximal ideal, which is $(0)$, and it is straightforward that $K/(0) \cong K$.

57. When $p$ is prime, $(p)$ is a maximal ideal of $\mathbb{Z}$, and so the ring $\mathbb{Z}/p\mathbb{Z}$ is a field. Since the order of $\mathbb{Z}/p\mathbb{Z}$ is finite, it is called a *finite field.*

58. The finite field of order $p$ is denoted $\mathbb{F}_p$.

59. The smallest field is $\mathbb{F}_2$, the field of order $2$.

60. Addition in $\mathbb{F}_2$ can be fully characterized as an operation where $a + b = 0$ if $a = b$ and $a + b = 1$ if $a \neq b$.

61. Multiplication in $\mathbb{F}_2$ can be fully characterized by the fact that $ab = 1$ if $a = 1$ and $b = 1$ while $ab = 0$ if $a = 0$ or $b = 0$.

62. The polynomial ring $\mathbb{F}_2[X]$ has only $1$ and $0$ as coefficients, so all terms are either powers of $X$ or the constant $1$.

63. The view of $1$ and $0$ in $\mathbb{F}_2$ as "wrap-around-at-$2$ numbers" will be treated interchangeably with the more proper view of them as the "class of odd numbers" and the "class of even numbers" for convenience.

64. Upper case $X$ is used here as the formal indeterminate to more directly emphasize that we are not interested in the *solutions*to polynomial equations over $\mathbb{F}_2$.

65. The difference between $R[x]$ and $R[X]$ is purely notational, and carries no mathematical significance.

66. This is motivated by the fact that the infinitely many unique univariate polynomials in $\mathbb{Z}[x]$, for example, correspond to the infinitely many unique polynomial functions of a single integer.

67. There are also infinitely many polynomials in $\mathbb{F}_2[X]$, but if $x \in \mathbb{F}_2$, then there are exactly four unique univariate functions of $x$.

68. Namely, $f(x) = 0$, $f(x) = 1$, $f(x) = x$, and $f(x) = x + 1$.

69. Though coefficients of the terms of polynomials in $\mathbb{F}_2[X]$ are limited to the $0$ and $1$ classes, the *powers* to which formal indeterminates can be raised are still taken from the natural numbers.

70. It is straightforward that $x^n = x$ for all $x \in \mathbb{F}_2$ and all $n \in \mathbb{Z}^+$.

71. So, if, for $P, Q \in \mathbb{F}_2[X]$, $P = X^2 + X + 1$ and $Q = X^3 + X + 1$, $P$ and $Q$ are fully distinct polynomials, even though from the "function on elements of $\mathbb{F}_2$" perspective, $P(x) = x^2 + x + 1$ and $Q(x) = x^3 + x + 1$define exactly the same map $\mathbb{F}_2 \to \mathbb{F}_2$ as the constant function $f(x) = 1$.

72. The particularities of arithmetic of "parity classes" in $\mathbb{F}_2$ reveal themselves in the factorization of polynomials in $\mathbb{F}_2[X]$.

73. In $\mathbb{F}_2$, addition is the same as subtraction because $0$ and $1$ are each their own additive inverse.

74. So, a polynomial like $X^2 + 1$, while irreducible over $\mathbb{Z}$, can be factored into $(X + 1)(X + 1)$ over $\mathbb{F}_2$.

75. Intuitively, consider that over the integers, $(X + 1)(X + 1) = X^2 + 2X + 1$.

76. Since the linear term of $X^2 + 2X + 1$ is $2X$, and $2 \equiv 0 \pmod{2}$, $2X$ effectively "vanishes" in $\mathbb{F}_2[X]$.

77. $\mathbb{F}_2[X]$ is a polynomial ring over a field, so it is a Euclidean domain.

78. As such, for $\mathbb{F}_2[X]$, every ideal is principal, factorization into irreducibles is guaranteed for non-units, irreducible elements are exactly prime elements, and non-zero prime ideals are exactly maximal ideals.

79. It follows that if $Q$ is irreducible in $\mathbb{F}_2[X]$, then $\mathbb{F}_2[X]/(Q)$ is a field.

80. The degree of $Q$ determines the order of $\mathbb{F}_2[X]/(Q)$.

81. Consider the ideal $(X) \subset \mathbb{F}_2[X]$. $X$ is irreducible, so $(X)$ is the maximal ideal of all polynomials in $\mathbb{F}_2[X]$ with $0$ for a constant term.

82. Since a constant term can be exactly either $0$ or $1$ in $\mathbb{F}_2[X]$, $(X)$ induces exactly two equivalence classes of polynomials in $\mathbb{F}_2[X]/(X),$ the class of polynomials which are in $(X)$, i.e. polynomials with $0$ for a constant term, and polynomials which have $1$ for a constant term.

83. So, taking the quotient of $\mathbb{F}_2[X]$ by $(X)$ "recovers" $\mathbb{F}_2,$ in the sense that $\mathbb{F}_2[X]/(X) \cong \mathbb{F}_2$.

84. There is exactly one irreducible polynomial of degree $2$ in $\mathbb{F}_2[X],$ $X^2 + X + 1$.

85. It would follow that $\mathbb{F}_2[X]/(X^2 + X + 1)$ is a field.

86. The ideal $(X)$ is so big that the equivalence classes it imposes on $\mathbb{F}_2[X]$ are not too arcane to understand.

87. However, how polynomials "wrap around" at $X^2 + X + 1$ may not be so immediately apparent.

88. Via the Euclidean division property for polynomials, any polynomial $A$, given a modulus $M$, has a quotient $Q$ and remainder $R$, such that $A = MQ + R$ and either $R = 0$ or $\text{deg}(R) < \text{deg}(M)$.

89. That $M$ induces a zero class on multiples of itself means that the highest degree term of $M$ can be written in terms of the additive inverses of the other terms of $M$, allowing for the reduction of $A$ into a polynomial whose degree is less than that of $M$.

90. For example, we can take advantage of the fact that $X^2 \equiv X + 1 \pmod{(X^2 + X + 1)}$.

91. Then, we can replace instances of $X^2$ with $X + 1$.

92. So, given $X^3$, we can rewrite $X(X + 1)$, $X^2 + X$, $(X + 1) + X$ to arrive at $X^3 \equiv 1 \pmod{(X^2 + X + 1)}$.

93. Since $X^4 = X(X^3),$ it is straightforward that $X^4 \equiv X \pmod{(X^2 + X + 1)}$.

94. Likewise, $X^5 = X(X^4) \equiv X^2 \equiv X + 1 \pmod{(X^2 + X + 1)}$.

95. The polynomials $0$, $1$, $X$, and $X + 1$ are exactly the four polynomials whose degree is less than that of $X^2 + X + 1$.

96. Since $(X^2 + X + 1)$ is maximal in $\mathbb{F}_2[X]$, we already know that $\mathbb{F}_2[x]/(X^2 + X + 1)$ is a field. Since this field has four elements, we denote it by $\mathbb{F}_4$.

97. In a finite field $\mathbb{F}_p[X]$, there are $p^k$ polynomials of degree less than $k$.

98. It can help to look at this from the view of a polynomial as a list of coefficients indexed by power.

99.  Accounting for terms with a coefficient of $0$, for each term of a polynomial, there are $p$ choices for the coefficient of that term.

100. That is, if $k$ is the degree of a polynomial, the set of all polynomials with degree less than $k$ in $\mathbb{F}_p[X]$ is effectively the set of all ordered $k$-tuples of the form $(a_0, a_1, {...}, a_{k-1})$, where $a_i \in \mathbb{F}_p.$

101. The essential principles of products and counting tell us that if each of the $k$ indices in an ordered $k$-tuple has $p$ possible options for its entry, then there are $p^k$ possible such tuples.

102. Given $\mathbb{F}_p[X]/(Q)$, where $Q$ is an irreducible polynomial of degree $k$, $\mathbb{F}_p[X]/(Q) \cong \mathbb{F}_{p^k}$.

103. That is, the least residue system of $\mathbb{F}_p[X]/(Q)$ is the set of all polynomials in $\mathbb{F}_p[X]$ whose degree is less than $\text{deg}(Q)$.

104. Suppose $P_1, P_2 \in \mathbb{F}_p[X]/(Q)$, where $\text{deg}(P_1) < k$ and $\text{deg}(P_2) < k,$ and $P_1 \equiv P_2 \pmod{(Q)}$.

105. Then, $P_1 - P_2 \equiv 0 \pmod{(Q)}$, and so $Q$ divides their difference.

106. However, $\text{deg}(P_1 - P_2) < k$, so we can say that $P_1 = P_2$.

107. It follows, then, that if $p$ is a prime number and $k$ is the degree of an irreducible polynomial in $\mathbb{F}_{p}[X]$, that there exists a finite field $\mathbb{F}_{p^k}$ of order $p^k$.

108. If the leading coefficient of a polynomial $P$ is $1$, $P$ is said to be *monic*.

109. Let $p$ be a prime number. From Fermat's little theorem, we know that, for all $x \in \mathbb{F}_p$, $x^p - x \equiv 0 \pmod{p}$.

110. Then, $X^p - X$ factors into a product of all monic linear polynomials in $\mathbb{F}_p[X]$.

111. Suppose $a \in \mathbb{F}_p$. Since $\mathbb{F}_p$ is a field, polynomials over it have Euclidean division, and so we can write $X^p - X = (X - a)Q + R$ for polynomials $Q, R \in \mathbb{F}_p[x]$.

112. We can substitute in $a$, and, knowing that $a^p - a \equiv 0 \pmod{p},$ we can write $(a - a)Q + R \equiv 0 \pmod{p}$.

113. $(a - a)Q$ is obviously $0$, so we are left with $R \equiv 0 \pmod{p}$, meaning $X - a$ divides $X^p - X$.

114. We can use product notation to write $X^p - X = \prod_{a \in \mathbb{F}_p}(X - a)$.

115. There is a second Lagrange's theorem.

116. Suppose $P \in \mathbb{F}_p[x]$ and $\text{deg}(P) = n$ for some prime $p$. Then, either $P$ is the zero polynomial, or $P$ has at most $n$ roots.

117. If the degree of a polynomial is $0$, it has $0$ roots.

118. Assume that for $k > 0$, if a polynomial $Q \in \mathbb{F}_p[x]$ has degree $k$, it has at most $k$ roots.

119. Suppose $A \in \mathbb{F}_p[x]$ and $\text{deg}(A) = k + 1$, where $A$ has at least one root $r \in \mathbb{F}_p$.

120. Then, we know that $(x - r) \mid A$, so we can write $A = (x - r)B$ for some $B \in \mathbb{F}_p[x]$.

121. Since $\text{deg}(A) = k + 1$, the degree of $B$ must be $k$.

122. If $A$ has a root $s \neq r$, then $b$ is a root of $B$.

123. By the inductive hypothesis, $B$ has at most $k$ roots.

124. So, we can conclude that $A$ has at most $k + 1$ roots, and the degree of a non-zero polynomial in $\mathbb{F}_p[x]$ is the maximum number of roots it can have.

125. Consider the quotient ring $\mathbb{Z}[X]/(X^2 + 1)$.

126. This ring is straightforwardly the set of all linear integer polynomials.

127. Reduction of polynomials modulo $X^2 + 1$ is governed by the rule that $X^2 \equiv -1 \pmod{X^2 + 1}$.

128. Addition is the ordinary addition of linear polynomials: for polynomials $z, w \in \mathbb{Z}[X]/(X^2 + 1)$, where $z = a + bX$ and $w = c + dX,$ $z+q = (a + c) + (b + d)X.$

129. The reduction rule leads to a peculiar rule of multiplication, however, where $zw = (ac - bd) + (ad + bc)X$, since the $X^2$ in the term $bdX^2$ is reduced to a $-1$.

130. The ability for a squared indeterminate to equal $-1$ is of very great consequence in arithmetic, and the value $i$ such that $i^2 = -1$is called the *imaginary unit.*

131. The arithmetic of polynomials in $\mathbb{Z}[X]/(X^2 + 1)$ is the arithmetic of the ring of *Gaussian integers,* denoted $\mathbb{Z}[i]$.

132. A Gaussian integer $z$ is a number of the form $z = a + bi$, where $a \in \mathbb{Z}$is the *real* part of $z$ and $b \in \mathbb{Z}$ is the *imaginary* part of $z$, and where $i^2 = -1.$

133. This property means that $i$ and $-i$ are units in $\mathbb{Z}[i]$.

134. Every Gaussian integer $z = a + bi$ has a *conjugate* $\bar{z} = a - bi.$

135. The product of a Gaussian integer $z = a + bi$ and its conjugate $(a + bi)(a - bi) = a^2 + b^2$ is an integer and is called the *norm* $N(z)$ of $z.$

136. Observe that the set of sums of two squares is closed under multiplication. That is, $(a^2 + b^2)(c^2 + d^2) = (ac - bd)^2 + (ad + bc)^2.$

137. This formula is called *Diophantus' identity.*

138. Expanding each side, we arrive at $a^2c^2 + a^2d^2 + b^2c^2 + b^2d^2.$

139. This also leads us to the conclusion that for Gaussian integers $z$ and $w$, $N(z)N(w) = N(zw).$

140. The norm of a Gaussian integer is a Euclidean function.

141. Recall that the condition for the norm to be a Euclidean function is that for any two Gaussian integers $z, w$ where $w \neq 0,$ Gaussian integers $q$ and $r$ exist such that $z = wq + r$ and either $r = 0$ or $N(r) < N(w).$

142. It helps to consider $\frac{z}{w}$ as being in $\mathbb{Q}[i],$ the Gaussian rationals (i.e. the field of fractions of the Gaussian integers), since $\mathbb{Z}[i],$ like $\mathbb{Z}$, is not closed under division.

143. First, for Gaussian rationals $z = a + bi$ and $w = c + di,$ then $\frac{z}{w} = \frac{a + bi}{c + di} = \frac{\bar{w}}{\bar{w}}\frac{a + bi}{c + di} = \frac{ac + bd}{c^2 + d^2} + \frac{bc - ad}{c^2 + d^2}i.$

144. Then, we can set $\frac{z}{w} = x + yi$ for $x, y \in \mathbb{Q}.$ By the nature of rational numbers, we can always find $n, m \in \mathbb{Z}$ such that $|x - n| \le \frac{1}{2}$and $|y - m| \le \frac{1}{2}.$

145. We can then set $q \in \mathbb{Z}[i]$ where $q = n + mi,$ meaning $r = z - wq,$ so we can say $N(r) = N(z - wq) = N(w)N(\frac{z}{w} - q).$

146. Since $\frac{z}{w} - q = (x - n) + (y - m)i$, we can write $N(\frac{z}{w} - q) = (x - n)^2 + (y - m)^2,$ which must be less than or equal to $(\frac{1}{2})^2 + (\frac{1}{2})^2 = \frac{1}{2}.$

147. Since $N(w)$ is a positive integer, we can write $N(r) \le \frac{1}{2}N(w) < N(w),$ meaning $\mathbb{Z}[i]$ is a Euclidean domain.

148. If $p$ is an odd prime number, then $p = a^2 + b^2$ for integers $a$ and $b$is the case if and only if $p \equiv 1 \pmod 4.$

149. It can be straightforwardly checked that $0$ and $1$ are the only quadratic residues modulo $4.$

150. So, since $p$ is odd, then it cannot be congruent to $0$ or $2$ modulo $4,$ and $a^2 + b^2$ can never be congruent to $3$ modulo $4.$

151. Therefore, if $p$ is the sum of two squares, then $p \equiv 1 \pmod 4.$

152. If $p \equiv 1 \pmod{4},$ $\frac{p-1}{2}$ is even, so, by Euler's criterion, $-1$ is a quadratic residue modulo $p.$

153. So, there exists some $k$ such that $k^2 \equiv -1 \pmod{p}.$

154. This implies that $p$ divides $k^2 + 1.$

155. $k^2 + 1$ factors into the product of Gaussian integers $(k+i)(k-i),$ but $p$ does not divide either $k+i$ or $k - i,$ so we know that $p$ is not a prime element of $\mathbb{Z}[i].$

156. Since $\mathbb{Z}[i]$ is a Euclidean domain and therefore a unique factorization domain, we know that $p$ is reducible in $\mathbb{Z}[i].$

157. Since $p$ is prime in $\mathbb{Z},$ it can only be the case that $p$ is the product of two Gaussian integers whose imaginary parts cancel.

158. Then, $p = zw$ for Gaussian integers $z$ and $w,$ and therefore $N(p) = N(z)N(w).$

159. $N(p) = p^2,$ however, so $z$ must be the conjugate of $w$.

160. Therefore, $p$ must be the norm of a Gaussian integer, and as such, $p$ is the sum of two squares.

161. That an odd prime $p$ is the sum of two squares if and only if $p \equiv 1 \pmod{4}$ is called *Fermat's Christmas theorem.*

162. A prime element of the ring of Gaussian integers is called a *Gaussian prime.*

163. Note that $2$ is not a Gaussian prime, since $2 = (1 + i)(1 - i).$

164. It is clear that a prime number $p \in \mathbb{Z}$ is only prime in $\mathbb{Z}[i]$ if $p \equiv 3 \pmod{4}.$

165. A Gaussian integer $z = a + bi$ with nonzero $b$ is a Gaussian prime if and only if $N(z)$ is prime.

166. This is a natural consequence of the property that for Gaussian integers $z, w,$ $N(zw) = N(z)N(w).$

167. The Gaussian integers do not have a linear ordering. Ordinary integers have the property that if $a \neq b,$ then either $a < b$ or $b < a.$

168. The geometric interpretation is that an integer $n$ specifies a single coordinate, and as such all integers fit as evenly spaced points in a one-dimensional space, i.e. a number line.

169. A Gaussian integer $z = a + bi$, having a real part and an imaginary part, specifies a pair of coordinates $(a, b),$ with $a$ representing distance along a (conventionally horizontal) *real axis* and $b$ representing distance along a (conventionally vertical) *imaginary axis.*

170. The two-dimensionality of Gaussian integers requires that they be geometrically represented as evenly spaced points in a number *plane,* which is called the *complex plane.*

171. While one can say that e.g. $1 + 2i$ is higher on the imaginary axis than $2 + i,$ the latter is further right on the real axis, and both have the same norm.

172. So, there is no natural way to impose a linear ordering between these elements.

173. Despite this, Gaussian integers, having Euclidean division, have a notion of greatest common divisor.

174. "Greatest," in this sense, is with respect to the set inclusion of divisors: the greatest common divisor of two Gaussian integers is the common divisor with the most divisors.

175. For ordinary integers, this notion of greatest coincides with "greatest" in the sense of size/arithmetic order.

176. The GCD of two Gaussian integers is interchangeable with its associates.

177. One can find it using a modified Euclidean algorithm.

178. For example, given $\alpha = 8 + 4i$ and $\beta = 7 + 5i$, if one wants to find the maximally divided Gaussian integer which divides both $\alpha$ and $\beta,$ one begins by finding the rationalization $\frac{\alpha}{\beta}.$

179. Recall that for Gaussian rationals $z = a + bi$ and $w = c + di,$ then $\frac{z}{w} = \frac{a + bi}{c + di} = \frac{\bar{w}}{\bar{w}}\frac{a + bi}{c + di} = \frac{ac + bd}{c^2 + d^2} + \frac{bc - ad}{c^2 + d^2}i.$

180. So, we have $\frac{\alpha}{\beta} = \frac{38}{37} - \frac{6}{37}i.$ We find the closest integers to the real and imaginary parts of our Gaussian rational ($1$ and $0$ respectively), and get a quotient value of $\kappa = 1.$

181. As such, we take the remainder $\rho = \alpha - \kappa \beta = \alpha - \beta = 8 + 4i - 7 + 5i,$ and end up with $\rho = 1 - i.$

182. So, we repeat, taking $\frac{\beta}{\rho} = \frac{7 + 5i}{1 - i} = 1 + 6i.$ We find the new remainder $\rho_2 = \beta - \kappa_2\rho = 7 + 5i - (1 - i)(1 + 6i) = 7 + 5i - 7 + 5i = 0.$

183. Since this remainder is $0,$ the greatest common divisor (up to associates) of $8 + 4i$ and $7 + 5i$ is $1 - i.$

184. A *Diophantine equation* is a polynomial equation (usually with integer coefficients) in some number of indeterminates whose solutions are integers.

185. For example, the expression $ax + by = c$ which underlies Bézout's identity is a Diophantine equation.

186. The Pythagorean formula $a^2 + b^2 = c^2$ has a very old interpretation as a Diophantine equation, the solutions to which being called *Pythagorean triples.*

187. It is apparent that the problem of finding Pythagorean triples is the problem of finding sums of two squares which are themselves squares.

188. Pythagorean triples $(a, b, c)$ such that $\gcd(a, b, c) = 1$ are called *primitive.*

189. We can solely focus on primitive triples because if $\gcd(a, b, c) = k,$then we can write $a = kx,$ $b = ky,$ and $c = kz$ for integers $x, y, z$ where $\gcd(x, y) = \gcd(x, z) = \gcd(y, z) = 1.$

190. Then, if $(a, b, c)$ is a solution to some $a^n + b^n = c^n,$ we can rewrite it as $k^n x^n + k^n y^n = k^n z^n,$ implying that $x^n + y^n = z^n$ also has a solution.

191. This condition implies that $a$ and $b$ differ in parity, because if $a$ and $b$ are both even, then $c^2$ is even, and $\gcd(a, b, c)$ is at least $2.$

192. If $a$ and $b$ are both odd, then $c^2 \equiv 2 \pmod 4,$ and $2$ is not a quadratic residue modulo $4$.

193. We can move the problem of $a^2 + b^2 = c^2$ to the Gaussian integers and rephrase it as $(a + bi)(a - bi) = c^2.$

194. Note that $a^2 + b^2 = c^2$ can also be stated as $N(a + bi) = c^2.$

195. If $a$ is relatively prime to $b$ in the integers, then $a + bi$ is relatively prime to $a - bi$ in the Gaussian integers.

196. Let $d$ be a greatest common divisor of $a + bi$ and $a - bi.$

197. Then, $d$ divides their sum $2a$ and their difference $2bi.$

198. We know that $a$ is relatively prime to $b,$ so at most $d$ must divide $2.$

199. $2$ factors into $(1 + i)(1 - i).$

200. $1 + i$ divides a Gaussian integer $a + bi$ if and only if $a \equiv b \pmod{2}.$

201. That is, $z = \frac{a+bi}{1+i} = \frac{(a + bi)(1 - i)}{2} = \frac{a + b}{2} + \frac{b - a}{2}i,$ so $z$ is only an integer if $a$ has the same parity as $b.$

202. Likewise for $1 - i,$ in that $w = \frac{a+bi}{1-i} = \frac{(a + bi)(1 - i)}{2} = \frac{a - b}{2} + \frac{a + b}{2}i.$

203. So, $a + bi$ and $a - bi$ share only unit divisors.

204. This leads to the conclusion that, due to unique factorization, if $(a + bi)(a - bi) = c^2,$ then $(a + bi)$ and $(a - bi)$ are perfect squares.

205. So, we can write $a + bi = v(m + ni)^2$ for integers $m$ and $n$ and a unit $v$ (which we can set to $1$ for our purposes without loss of generality.)

206. We can write $(m + ni)^2 = m^2 - n^2 + 2mni,$ and say that $a = m^2 - n^2$ and $b = 2mn.$

207. We can then observe that the norm of $m + ni$ is $m^2 + n^2.$

208. Since $a + bi = (m + ni)^2,$ $N(a + bi) = a^2 + b^2 = N(m + ni)^2.$

209. So, we are left with $(m^2 - n^2)^2 + (2mn)^2 = (m^2 + n^2)^2,$ which indicates that we can set $c = m^2 + n^2.$

210. It follows from this that if we select an $m$ and $n$ which are relatively prime and not both odd, where $m > n > 0,$ we can find a Pythagorean triple $(a, b, c) = (m^2 - n^2, 2mn, m^2 + n^2).$

211. This is called *Euclid's formula* for Pythagorean triples.
