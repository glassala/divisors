# Gaussian integers

*Gaussian integers. Norm of a Gaussian integer. Fermat's Christmas theorem. Euclid's formula for Pythagorean triples.*

1. Consider the quotient ring $\mathbb{Z}[X]/(X^2 + 1)$.

2. This ring is straightforwardly the set of all linear integer polynomials.

3. Reduction of polynomials modulo $X^2 + 1$ is governed by the rule that $X^2 \equiv -1 \pmod{X^2 + 1}$.

4. Addition is the ordinary addition of linear polynomials: for polynomials $z, w \in \mathbb{Z}[X]/(X^2 + 1)$, where $z = a + bX$ and $w = c + dX,$ $z+q = (a + c) + (b + d)X.$

5. The reduction rule leads to a peculiar rule of multiplication, however, where $zw = (ac - bd) + (ad + bc)X$, since the $X^2$ in the term $bdX^2$ is reduced to a $-1$.

6. The ability for a squared indeterminate to equal $-1$ is of very great consequence in arithmetic, and the value $i$ such that $i^2 = -1$is called the *imaginary unit.*

7. The arithmetic of polynomials in $\mathbb{Z}[X]/(X^2 + 1)$ is the arithmetic of the ring of *Gaussian integers,* denoted $\mathbb{Z}[i]$.

8. A Gaussian integer $z$ is a number of the form $z = a + bi$, where $a \in \mathbb{Z}$is the *real* part of $z$ and $b \in \mathbb{Z}$ is the *imaginary* part of $z$, and where $i^2 = -1.$

9. This property means that $i$ and $-i$ are units in $\mathbb{Z}[i]$.

10. Every Gaussian integer $z = a + bi$ has a *conjugate* $\bar{z} = a - bi.$

11. The product of a Gaussian integer $z = a + bi$ and its conjugate $(a + bi)(a - bi) = a^2 + b^2$ is an integer and is called the *norm* $N(z)$ of $z.$

12. Observe that the set of sums of two squares is closed under multiplication. That is, $(a^2 + b^2)(c^2 + d^2) = (ac - bd)^2 + (ad + bc)^2.$

13. This formula is called *Diophantus' identity.*

14. Expanding each side, we arrive at $a^2c^2 + a^2d^2 + b^2c^2 + b^2d^2.$

15. This also leads us to the conclusion that for Gaussian integers $z$ and $w$, $N(z)N(w) = N(zw).$

16. The norm of a Gaussian integer is a Euclidean function.

17. Recall that the condition for the norm to be a Euclidean function is that for any two Gaussian integers $z, w$ where $w \neq 0,$ Gaussian integers $q$ and $r$ exist such that $z = wq + r$ and either $r = 0$ or $N(r) < N(w).$

18. It helps to consider $\frac{z}{w}$ as being in $\mathbb{Q}[i],$ the Gaussian rationals (i.e. the field of fractions of the Gaussian integers), since $\mathbb{Z}[i],$ like $\mathbb{Z}$, is not closed under division.

19. First, for Gaussian rationals $z = a + bi$ and $w = c + di,$ then $\frac{z}{w} = \frac{a + bi}{c + di} = \frac{\bar{w}}{\bar{w}}\frac{a + bi}{c + di} = \frac{ac + bd}{c^2 + d^2} + \frac{bc - ad}{c^2 + d^2}i.$

20. Then, we can set $\frac{z}{w} = x + yi$ for $x, y \in \mathbb{Q}.$ By the nature of rational numbers, we can always find $n, m \in \mathbb{Z}$ such that $|x - n| \le \frac{1}{2}$and $|y - m| \le \frac{1}{2}.$

21. We can then set $q \in \mathbb{Z}[i]$ where $q = n + mi,$ meaning $r = z - wq,$ so we can say $N(r) = N(z - wq) = N(w)N(\frac{z}{w} - q).$

22. Since $\frac{z}{w} - q = (x - n) + (y - m)i$, we can write $N(\frac{z}{w} - q) = (x - n)^2 + (y - m)^2,$ which must be less than or equal to $(\frac{1}{2})^2 + (\frac{1}{2})^2 = \frac{1}{2}.$

23. Since $N(w)$ is a positive integer, we can write $N(r) \le \frac{1}{2}N(w) < N(w),$ meaning $\mathbb{Z}[i]$ is a Euclidean domain.

24. If $p$ is an odd prime number, then $p = a^2 + b^2$ for integers $a$ and $b$is the case if and only if $p \equiv 1 \pmod 4.$

25. It can be straightforwardly checked that $0$ and $1$ are the only quadratic residues modulo $4.$

26. So, since $p$ is odd, then it cannot be congruent to $0$ or $2$ modulo $4,$ and $a^2 + b^2$ can never be congruent to $3$ modulo $4.$

27. Therefore, if $p$ is the sum of two squares, then $p \equiv 1 \pmod 4.$

28. If $p \equiv 1 \pmod{4},$ $\frac{p-1}{2}$ is even, so, by Euler's criterion, $-1$ is a quadratic residue modulo $p.$

29. So, there exists some $k$ such that $k^2 \equiv -1 \pmod{p}.$

30. This implies that $p$ divides $k^2 + 1.$

31. $k^2 + 1$ factors into the product of Gaussian integers $(k+i)(k-i),$ but $p$ does not divide either $k+i$ or $k - i,$ so we know that $p$ is not a prime element of $\mathbb{Z}[i].$

32. Since $\mathbb{Z}[i]$ is a Euclidean domain and therefore a unique factorization domain, we know that $p$ is reducible in $\mathbb{Z}[i].$

33. Since $p$ is prime in $\mathbb{Z},$ it can only be the case that $p$ is the product of two Gaussian integers whose imaginary parts cancel.

34. Then, $p = zw$ for Gaussian integers $z$ and $w,$ and therefore $N(p) = N(z)N(w).$

35. $N(p) = p^2,$ however, so $z$ must be the conjugate of $w$.

36. Therefore, $p$ must be the norm of a Gaussian integer, and as such, $p$ is the sum of two squares.

37. That an odd prime $p$ is the sum of two squares if and only if $p \equiv 1 \pmod{4}$ is called *Fermat's Christmas theorem.*

38. A prime element of the ring of Gaussian integers is called a *Gaussian prime.*

39. Note that $2$ is not a Gaussian prime, since $2 = (1 + i)(1 - i).$

40. It is clear that a prime number $p \in \mathbb{Z}$ is only prime in $\mathbb{Z}[i]$ if $p \equiv 3 \pmod{4}.$

41. A Gaussian integer $z = a + bi$ with nonzero $b$ is a Gaussian prime if and only if $N(z)$ is prime.

42. This is a natural consequence of the property that for Gaussian integers $z, w,$ $N(zw) = N(z)N(w).$

43. The Gaussian integers do not have a linear ordering. Ordinary integers have the property that if $a \neq b,$ then either $a < b$ or $b < a.$

44. The geometric interpretation is that an integer $n$ specifies a single coordinate, and as such all integers fit as evenly spaced points in a one-dimensional space, i.e. a number line.

45. A Gaussian integer $z = a + bi$, having a real part and an imaginary part, specifies a pair of coordinates $(a, b),$ with $a$ representing distance along a (conventionally horizontal) *real axis* and $b$ representing distance along a (conventionally vertical) *imaginary axis.*

46. The two-dimensionality of Gaussian integers requires that they be geometrically represented as evenly spaced points in a number *plane,* which is called the *complex plane.*

47. While one can say that e.g. $1 + 2i$ is higher on the imaginary axis than $2 + i,$ the latter is further right on the real axis, and both have the same norm.

48. So, there is no natural way to impose a linear ordering between these elements.

49. Despite this, Gaussian integers, having Euclidean division, have a notion of greatest common divisor.

50. "Greatest," in this sense, is with respect to the set inclusion of divisors: the greatest common divisor of two Gaussian integers is the common divisor with the most divisors.

51. For ordinary integers, this notion of greatest coincides with "greatest" in the sense of size/arithmetic order.

52. The GCD of two Gaussian integers is interchangeable with its associates.

53. One can find it using a modified Euclidean algorithm.

54. For example, given $\alpha = 8 + 4i$ and $\beta = 7 + 5i$, if one wants to find the maximally divided Gaussian integer which divides both $\alpha$ and $\beta,$ one begins by finding the rationalization $\frac{\alpha}{\beta}.$

55. Recall that for Gaussian rationals $z = a + bi$ and $w = c + di,$ then $\frac{z}{w} = \frac{a + bi}{c + di} = \frac{\bar{w}}{\bar{w}}\frac{a + bi}{c + di} = \frac{ac + bd}{c^2 + d^2} + \frac{bc - ad}{c^2 + d^2}i.$

56. So, we have $\frac{\alpha}{\beta} = \frac{38}{37} - \frac{6}{37}i.$ We find the closest integers to the real and imaginary parts of our Gaussian rational ($1$ and $0$ respectively), and get a quotient value of $\kappa = 1.$

57. As such, we take the remainder $\rho = \alpha - \kappa \beta = \alpha - \beta = 8 + 4i - 7 + 5i,$ and end up with $\rho = 1 - i.$

58. So, we repeat, taking $\frac{\beta}{\rho} = \frac{7 + 5i}{1 - i} = 1 + 6i.$ We find the new remainder $\rho_2 = \beta - \kappa_2\rho = 7 + 5i - (1 - i)(1 + 6i) = 7 + 5i - 7 + 5i = 0.$

59. Since this remainder is $0,$ the greatest common divisor (up to associates) of $8 + 4i$ and $7 + 5i$ is $1 - i.$

60. A *Diophantine equation* is a polynomial equation (usually with integer coefficients) in some number of indeterminates whose solutions are integers.

61. For example, the expression $ax + by = c$ which underlies Bézout's identity is a Diophantine equation.

62. The Pythagorean formula $a^2 + b^2 = c^2$ has a very old interpretation as a Diophantine equation, the solutions to which being called *Pythagorean triples.*

63. It is apparent that the problem of finding Pythagorean triples is the problem of finding sums of two squares which are themselves squares.

64. Pythagorean triples $(a, b, c)$ such that $\gcd(a, b, c) = 1$ are called *primitive.*

65. We can solely focus on primitive triples because if $\gcd(a, b, c) = k,$then we can write $a = kx,$ $b = ky,$ and $c = kz$ for integers $x, y, z$ where $\gcd(x, y) = \gcd(x, z) = \gcd(y, z) = 1.$

66. Then, if $(a, b, c)$ is a solution to some $a^n + b^n = c^n,$ we can rewrite it as $k^n x^n + k^n y^n = k^n z^n,$ implying that $x^n + y^n = z^n$ also has a solution.

67. This condition implies that $a$ and $b$ differ in parity, because if $a$ and $b$ are both even, then $c^2$ is even, and $\gcd(a, b, c)$ is at least $2.$

68. If $a$ and $b$ are both odd, then $c^2 \equiv 2 \pmod 4,$ and $2$ is not a quadratic residue modulo $4$.

69. We can move the problem of $a^2 + b^2 = c^2$ to the Gaussian integers and rephrase it as $(a + bi)(a - bi) = c^2.$

70. Note that $a^2 + b^2 = c^2$ can also be stated as $N(a + bi) = c^2.$

71. If $a$ is relatively prime to $b$ in the integers, then $a + bi$ is relatively prime to $a - bi$ in the Gaussian integers.

72. Let $d$ be a greatest common divisor of $a + bi$ and $a - bi.$

73. Then, $d$ divides their sum $2a$ and their difference $2bi.$

74. We know that $a$ is relatively prime to $b,$ so at most $d$ must divide $2.$

75. $2$ factors into $(1 + i)(1 - i).$

76. $1 + i$ divides a Gaussian integer $a + bi$ if and only if $a \equiv b \pmod{2}.$

77. That is, $z = \frac{a+bi}{1+i} = \frac{(a + bi)(1 - i)}{2} = \frac{a + b}{2} + \frac{b - a}{2}i,$ so $z$ is only an integer if $a$ has the same parity as $b.$

78. Likewise for $1 - i,$ in that $w = \frac{a+bi}{1-i} = \frac{(a + bi)(1 - i)}{2} = \frac{a - b}{2} + \frac{a + b}{2}i.$

79. So, $a + bi$ and $a - bi$ share only unit divisors.

80. This leads to the conclusion that, due to unique factorization, if $(a + bi)(a - bi) = c^2,$ then $(a + bi)$ and $(a - bi)$ are perfect squares.

81. So, we can write $a + bi = v(m + ni)^2$ for integers $m$ and $n$ and a unit $v$ (which we can set to $1$ for our purposes without loss of generality.)

82. We can write $(m + ni)^2 = m^2 - n^2 + 2mni,$ and say that $a = m^2 - n^2$ and $b = 2mn.$

83. We can then observe that the norm of $m + ni$ is $m^2 + n^2.$

84. Since $a + bi = (m + ni)^2,$ $N(a + bi) = a^2 + b^2 = N(m + ni)^2.$

85. So, we are left with $(m^2 - n^2)^2 + (2mn)^2 = (m^2 + n^2)^2,$ which indicates that we can set $c = m^2 + n^2.$

86. It follows from this that if we select an $m$ and $n$ which are relatively prime and not both odd, where $m > n > 0,$ we can find a Pythagorean triple $(a, b, c) = (m^2 - n^2, 2mn, m^2 + n^2).$

87. This is called *Euclid's formula* for Pythagorean triples.

## Exercises

1. Prove that Euclid's formula generates all primitive Pythagorean triples and only primitive Pythagorean triples.

2. Demonstrate that there are no integer triples $(a, b, c)$ such that $a^4 + b^4 = c^4.$

3. Bonus! Prove that there are no integer triples $(a, b, c)$ such that $a^n + b^n = c^n$ for all integers $n > 2.$ Alternatively: choose an odd prime $p.$ Prove that $x^p + y^p = z^p$ has no solutions where $x, y, z$ are all integers.
