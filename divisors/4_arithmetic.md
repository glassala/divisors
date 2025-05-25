# Arithmetic functions

1. Functions of positive integers are also called *arithmetic functions.*
2. While the domain of arithmetic functions is the set of positive integers, the image of an arithmetic function can be any subset of the complex numbers.
3. A *multiplicative function* is a function $f$ of a positive integer such that for relatively prime numbers $n$ and $m$, $f(nm)=f(n)f(m)$.
4. If the property $f(nm)=f(n)f(m)$ holds even when $n$ and $m$ are not relatively prime, then $f$ is called *completely multiplicative.*
5. Euler's phi function is multiplicative.
6. This is because if a number $a$ is relatively prime to numbers $n$ and $m$, then it must also be relatively prime to their product $nm$.
7. There is a family of multiplicative functions $\sigma_{k}$ of a positive integer which are called the *$k$th-power divisor sigma* functions.
8. The $k$th-power divisor sigma function at a number $n$ is the sum of the $k$-th powers of the positive divisors of $n$.
9. In the case where $k=0$, since any number taken to the $0$-th power is $1$, $\sigma_{0}(n)$ is often called the *divisor-counting function*, and it is also denoted $\tau(n)$.
10. To account for the multiplicativity of these functions, we can look at the correspondence between products of numbers $n$, $m$ and the Cartesian products of their divisor sets $D_n$, $D_m$.
11. Suppose $n = ab$ and $m = xy$, so $D_n = \set{1, a, b, ab}$ and $D_m = \set{1, x, y, xy}$, where $n$ and $m$ are relatively prime.
12. Consider the set of products of all pairs in $D_n \times D_m$; this set is exactly the set $D_{nm}$:

| $D_{nm}$ | $1$  | $x$   | $y$   | $xy$   |
| -------- | ---- | ----- | ----- | ------ |
| $1$      | $1$  | $x$   | $y$   | $xy$   |
| $a$      | $a$  | $ax$  | $ay$  | $axy$  |
| $b$      | $b$  | $bx$  | $by$  | $bxy$  |
| $ab$     | $ab$ | $abx$ | $aby$ | $abxy$ |

12. Since every divisor except $1$ is unique to $m$ or $n$, there are exactly as many unique products in $D_{nm}$ as there are pairs in $D_n \times D_m$.
13. Suppose, however, instead, that $n = ab$ and $m = ax$:

| $D_{nm}$ | $1$  | $a$    | $x$   | $ax$    |
| -------- | ---- | ------ | ----- | ------- |
| $1$      | $1$  | $a$    | $x$   | $ax$    |
| $a$      | $a$  | $a^2$  | $ax$  | $a^2x$  |
| $b$      | $b$  | $ab$   | $bx$  | $abx$   |
| $ab$     | $ab$ | $a^2b$ | $abx$ | $a^2bx$ |

14. Since multiplication is commutative, unique pairs in $D_n \times D_m$ in the form $(p, q)$ and $(q, p)$ both map to the product $pq$ in $D_{nm}$.
15. This leads one to the conclusion that it is only if $n$ and $m$ are relatively prime that $|D_{nm}| = |D_n||D_m| = |D_n \times D_m|$.
16. This means that $\tau$ is multiplicative.
17. A similar principle underlies why $\sigma_1$, or the sum of divisors function (also denoted simply $\sigma$) is multiplicative.
18. Suppose $n = ab$ and $m = xy$ for primes $a$, $b$, $x$, $y$. Then, $\sigma(n)=1+a+b+ab$ and $\sigma(m) = 1 + x + y + xy$.
19. From the first table, one can independently verify that the sum of divisors of $nm$ is exactly the FOIL expansion of $(1+a+b+ab)(1+x+y+xy)$.
20. However, from the second table and its duplicate divisors, one can see that there will be terms like $2a$, $2ab$, $2ax$, and $2abx$ which cannot be present in $\sigma(nm)$.
21. Suppose $n$ is prime. Then $\sigma(n)=n + 1$.
22. It follows that $\sigma(n)^2 = n^2 + 2n + 1$, but $\sigma(n^2) = n^2 + n + 1$.
23. So, if $n$ and $m$ are not relatively prime, then $\sigma(n)\sigma(m)$ must be greater than $\sigma(nm)$, as each shared divisor is "overcounted" in the former.
24. If $f$ is a multiplicative but not a completely multiplicative function, then it is usually the case that $f$ is sensitive to the "overcounting" of divisors which occurs in $f(n)f(m)$ but not in $f(nm)$.
25. There is a function of a positive integer $n$ denoted $1(n)$, which always evaluates to $1$ for any $n$.
26. This function is trivially completely multiplicative.
27. There is a function of a positive integer $n$ denoted $\varepsilon(n)$ which evaluates to $1$ exactly when $n=1$ and which evaluates to $0$ otherwise.
28. This function is also trivially completely multiplicative.
29. The identity function $\text{Id}(n)$ of a positive integer $n$ is completely multiplicative.
30. On account of the property $a^{n}a^{m}=a^{n+m}$, a constant taken to the power of an additive function is a multiplicative function.
31. The Liouville function is a function of a positive integer $n$ defined as $\lambda(n)=(-1)^{\Omega(n)}$.
32. The Liouville function indicates via sign whether $n$ is the product of evenly or oddly many prime numbers.
33. It is a constant raised to the power of a completely additive function, so it is completely multiplicative.
34. There is a function of two variables from any set whose members $n$, $m$ admit an idea of equality called the *Kronecker delta* $\delta_{nm}$.
35. The Kronecker delta $\delta_{nm}$ is $1$ if $n = m$ and $0$ if $n\neq m$.
36. The Kronecker delta helps in the definition of a very (say it with me) $\text{important}$ function, the *Möbius function* $\mu$.
37. $\mu(n)$ evaluates to $1$ if $n$ is square-free and has evenly many prime factors.
38. $\mu(n)$ evaluates to $0$ if $n$ is not square-free.
39. $\mu(n)$ evaluates to $-1$ if $n$ is square-free and has oddly many prime factors.
40. A way to state that a number $n$ is square-free is that  $\omega(n)=\Omega(n)$.
41. It follows, then, that we can write the Möbius function as $\mu(n)=\delta_{\omega(n)\Omega(n)}\lambda(n)$, or, to emphasize that $\mu$ is multiplicative but *not* completely multiplicative, as $\mu(n)=\delta_{\omega(n)\Omega(n)}(-1)^{\omega(n)}$.
42. Consider that for $n$ and $m$ which are square-free but not relatively prime, then $nm$ has at least one squared prime factor, i.e. $|\mu(n)\mu(m)| = 1$ but $\mu(nm)=0$.
43. There is an operation of two functions of a positive integer $f$ and $g$ which yields a new function of a positive integer called the *Dirichlet convolution* of $f$ and $g$, denoted $f * g$.
44. The Dirichlet convolution $f * g$ at $n$ is the sum $(f*g)(n)=\sum_{d\mid{n}}f(d)g(\frac{n}{d})$, where $\sum_{d\mid{n}}$ is a sum indexed by the divisors of $n$.
45. The Dirichlet convolution of two multiplicative functions is always multiplicative. However, the convolution of two completely multiplicative functions is *not necessarily* completely multiplicative.
46. Suppose $f$, $g$ are multiplicative functions and $n$, $m$ are relatively prime positive integers.
47. Since $\gcd(n, m) = 1$, every divisor $d$ of the product $nm$ can be written as $d = xy$ where $x \mid n$ and $y \mid m$.
48. So, we can write $(f * g)(nm) = \sum_{x \mid n \land y \mid m}f(xy)g(\frac{nm}{xy})$.
49. Since $f$ and $g$ are multiplicative, we can rewrite the above as $(f * g)(nm) = \sum_{x \mid n \land y \mid m}f(x)f(y)g(\frac{n}{x})g(\frac{m}{y})$.
50. We can reorganize this sum into $\sum_{x \mid n}f(x)g(\frac{n}{x}) \sum_{y \mid m}f(y)g(\frac{m}{y})$, which is exactly $(f*g)(n)(f*g)(m)$, meaning $(f*g)$ is multiplicative.
51. This means that the set of multiplicative functions is closed under Dirichlet convolution.
52. Dirichlet convolution is commutative.
53. This is because, by the nature of sets of divisors, the sum always counts both $f(d)g(\frac{n}{d})$ and $f(\frac{n}{d})g(d)$.
54. Dirichlet convolution is associative.
55. Consider that an alternative way of writing $(f*g)(n)$ is as $\sum_{xy = n}f(x)g(y)$.
56. Then, we can write $(f * (g * h))(n) = \sum_{xw = n}f(x)\sum_{yz = w}g(y)h(z)$.
57. This can be rearranged into $\sum_{xw = n}\sum_{yz = w}f(x)g(y)h(z)$.
58. Similarly, we can directly write $((f * g) * h)(n) = \sum_{xw = n}\sum_{yz = w}f(x)g(y)h(z)$.
59. Dirichlet convolution is what motivates certain completely multiplicative functions like $1(n)$, the function which always evaluates to $1$, and $\varepsilon(n)$, the function which is only $1$ if $n = 1$, and $0$ otherwise.
60. Convolution by $\varepsilon$ is the identity convolution: $(f*\varepsilon)(n)=f(n)$.
61. This is because in the summation operation, for some positive integer $n$, if $d$ is $1$, then $(\frac{n}{d}) = n$, and likewise if $(\frac{n}{d}) = 1$, then $d = n$, i.e. the only term in the sum not canceled out by being a product with $0$.
62. Convolution by $1$ is a special case, in that $(f*1)(n)=\sum_{d\mid{n}}f(d)$.
63. For example, $\mu * 1 = \varepsilon$.
64. Any positive integer $n$ has a *square-free radical* $\text{rad}(n)$.
65. If $n$ is square-free, then $\text{rad}(n) = n$.
66. If $n$ is not square-free, then $\text{rad}(n)$ is the number $r$ which has exactly the same unique prime factors as $n$, but with no duplicates, i.e. $\omega(r) = \Omega(r)$.
67. Consider that for a square-free integer, its divisors correspond exactly to the $k$-combinations of its prime factors.
68. The binomial theorem is a statement about expressions of the form: $(x + y)^n$: $(x + y)^n = \sum^{n}_{k=0}\binom{n}{k}x^{k}y^{n-k};\binom{n}{k} = \frac{n!}{k!(n - k)!}$
69. $\binom{n}{k}$ is called a *binomial coefficient,* and is read out as "$n$ choose $k$."
70. The binomial coefficient $\binom{n}{k}$ represents the number of unique $k$-element subsets (or $k$-*combinations*) in an $n$-element set.
71. So, if $n$ is a square-free integer and $k$ is a non-negative integer less than or equal to $\omega(n)$, then $n$ has $\binom{\omega(n)}{k}$ divisors $d$ for which $\omega(d) = k$.
72. It follows that $\sum_{d\mid{n}}\mu(d) = \sum_{d\mid{n}}(-1)^{\omega(d)} = \sum_{k=0}^{\omega(n)}\binom{\omega(n)}{k}(-1)^{k}$.
73. If we consider the structure of the binomial theorem's statement, the sum $\sum_{k=0}^{\omega(n)}\binom{\omega(n)}{k}(-1)^{k}$ emerges from the binomial $(1+(-1))^{\omega(n)}$, which can be restated as $0^{\omega(n)}$.
74. This is $0$ for all square-free integers $n > 1$.
75. For the case where $n = 1$, note that, by combinatorial convention, $0^0 = 1$.
76. Since $1$ is the unique positive integer with no prime factors, $1$is the unique $n$ for which $\omega(n) = 0$.
77. As such, $\sum_{d\mid{n}}\mu(d) = 0$ for all square-free integers $n > 1$ and $\sum_{d\mid{n}}\mu(d) = 1$ exactly in the case where $n=1$.
78. If $n$ is not square-free, then $n$ still has a square-free radical.
79. Since for non-square-free divisors $d$, $\mu(d) = 0$, and so $\sum_{d\mid{n}}\mu(d) = \sum_{d\mid{\text{rad}(n)}}\mu(d)$.
80. Therefore, $\mu * 1 = \varepsilon$.
81. It also follows from the argument above that $|\mu| * 1 = 2^{\omega}$, since the sum of all binomial coefficients $\binom{n}{k}$ for some positive integer $n$ is $2^n$.
82. That is, instead of the binomial $(1+(-1))^{\omega(n)}$, we get $(1+1)^{\omega(n)} = 2^{\omega(n)} = \sum_{k=0}^{\omega(n)}\binom{\omega(n)}{k}$.
83. Since $\varepsilon$ is the identity element of the set of arithmetic functions under Dirichlet convolution, if for two such functions $f$, $g$, it is the case that $f * g = \varepsilon$, then $f$ and $g$ are called *Dirichlet inverses* of one another.
84. For an arithmetic function $f$ to have a Dirichlet inverse, however, it only has to have the property that $f(1) \neq 0$.
85. This is because there is a recursive formula to construct a Dirichlet inverse for any arithmetic function with that property.
86. The base case is that $f^{-1}(1)=\frac{1}{f(1)}$.
87. The recursive step is that, for $n > 1$, $f^{-1}(n)=-\frac{1}{f(1)}\sum_{d<n\mid n}f(d)f^{-1}(\frac{n}{d})$.
88. For $n = 1$, the problem of finding the Dirichlet inverse of a function $f$ is an equation where $(f^{-1} * f)(1) = \varepsilon(1) = 1$; this is solved by the base case.
89. Otherwise, the problem of finding the Dirichlet inverse of $f$ is an equation where $(f^{-1} * f)(n) = \varepsilon(n) = 0$ for all $n > 1$.
90. Another way of writing this is $\sum_{d \mid n}f(d)f^{-1}(\frac{n}{d}) = 0$.
91. This can be rewritten, remarkably, as $f(1)f^{-1}(n) + \sum_{d < n \mid n}f^{-1}(d)f(\frac{n}{d}) = 0$ -> $f^{-1}(n) = \frac{-1}{f(1)}\sum_{d < n \mid n}f^{-1}(d)f(\frac{n}{d})$. [^1]
92. It is straightforward to define arbitrary arithmetic functions which satisfy the inverse condition.
93. For example, for any non-zero complex number $z$, one can define a function $c_{z}(n) = z$ for all positive integers $n$.
94. Since $\mu$ is the inverse of $1$, if an arithmetic function $g$ takes the form $g = f * 1$, then $g * \mu = f * 1 * \mu = f * \varepsilon = f$.
95. This is called *Möbius inversion*.
96. Möbius inversion can be thought to "recover" one function from another.
97. The form of Dirichlet convolution itself, which is to say, as a sum over the divisors of a number, makes it clear that $\sigma = \text{Id} * 1$.
98. Then, $1$ can be "recovered" from $\mu * \tau$, and the identity function can be "recovered" from $\sigma * \mu$.
99. Less obvious, perhaps, is that $\varphi * 1 = \text{Id}$, i.e. $\varphi = \text{Id} * \mu$.
100. We can write $(\varphi * 1)(n) = \sum_{d \mid n}\varphi(d) = n$.
101. Since $\varphi$ is multiplicative, its behavior over positive integers is fully determined by its behavior at powers of prime numbers.
102. If we have some $p^k$ for some prime $p$ and positive integer $k$, the divisors of $p^k$ are $\set{1, p, p^2, p^3, ..., p^k}$.
103. For a prime power $p^k$, $\varphi(p^k) = p^{k} - p^{k-1}$.
104. This stems from the fact that the numbers not relatively prime to $p$ are exactly the multiples of $p$.
105. Since, for example, $p^2$ is the $p$-th multiple of $p$, then there are exactly $p$ positive integers less than or equal to $p^2$ which are not relatively prime to $p$, and so $\varphi(p^2) = p^2 - p$.
106. Likewise, $p^3$ is the $p^2$-th multiple of $p$, and so on.
107. Therefore, $\sum_{d \mid p^k}\varphi(d) = 1 + (p - 1) + (p^2 - p) + (p^3 - p^2) + ... + (p^{k} - p^{k-1})$.
108. It is apparent that each term is subtracted by the next, leaving only $p^k$, meaning $(\varphi * 1)(n) = n$.

## Exercises

1. In order for an arithmetic function $f$ to be multiplicative, it must be the case that $f(1) = 1$. Why?
2. Find functions $f$ and $g$ such that $f$ and $g$ are both completely multiplicative, but $(f * g)$ is not completely multiplicative.
3. Find the function $f$ such that $f = 1 * 1$.
4. Show that $\lambda * |\mu| = \varepsilon$.
5. Let $q(n)$ be the arithmetic function which evaluates to $1$ if $n$ is a perfect square and $0$ if $n$ is not a perfect square. Find the function $f$ such that $f * 1 = q$.
6. Prove that if an arithmetic function $f$ is multiplicative, then its Dirichlet inverse $f^{-1}$ is also multiplicative.
7. Let $g_{k}$ be an arithmetic function such that $g_{k}(n) = \gcd(n, k)$ for some fixed integer $k$. Demonstrate whether or not $g_{k}$ is multiplicative for all $k$.
8. A perfect number is a number $n$ such that the sum of the proper divisors of $n$ is equal to $n$. Equivalently, $n$ is perfect if $\sigma(n) = 2n$. Where $k$ is a positive integer, prove that if $2^k - 1$ is prime, then $2^{k-1}(2^{k} - 1)$ is perfect.[^2]

## Notes

[^1]: As much as I would love to take credit for this ingenious derivation of the Dirichlet inverse formula, that particular argument was fully adapted from section 2.7 of Tom M. Apostol's *Introduction to Analytic Number Theory* (1976).
[^2]: See also exercise 18, chapter 2, Apostol.
