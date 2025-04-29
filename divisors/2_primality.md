# Primality

1. There are infinitely many prime numbers.
2. Since $a > b \implies \gcd(a, b) = \gcd(b, a \bmod b)$, for any number $n$, the only divisor common to $n$ and $n+1$ is $1$.
3. There is a function of a natural number called the *factorial* function.
4. The factorial of a number $n$ is denoted $n!$.
5. The factorial is characterized by a recursive formula: the base case is that $0! = 1$, and the recursive step is that $n! = (n-1)!n$.
6. In practice, for any positive integer $n$, $n!$ is the product of every positive integer less than or equal to $n$.
7. As a consequence of this, for all positive integers $k \le n$, $k$ divides $n!$.
8. Suppose there is a largest prime number $p$.
9. Then, $p!$ is divisible by every prime number.
10. However, this would imply that $p! + 1$ is divisible by *no* prime number, which cannot be the case.
11. As such, for every largest prime number which is found, a larger prime awaits.
12. This is called Euclid's theorem.
13. If two numbers $a$ and $b$ have a GCD of $1$, then $a$ and $b$ are called *relatively prime* to one another.
14. A way to characterize a prime number $n$ is as a number which is  relatively prime to every positive integer less than $n$.
15. If a prime number $p$ divides a composite number $ab$, then $p$ divides at least either $a$ or $b$.
16. If $p$ does not divide $a$, then, because $1$ is the only other divisor of $p$, $\gcd(p, a)=1$.
17. So, there must exist integers $x$ and $y$ such that $px + ay = 1$.
18. Suppose we multiply this expression by $b$: $pbx + aby = b$.
19. We know that $p \mid ab$, so we can see that $p$ can be factored out of the left side, and so $p \mid b$.
20. This property is called Euclid's lemma.
21. This lemma is indeed a lemma about division attributed to Euclid, but it is not to be confused with Euclid's division lemma.
22. Every natural number which is greater than $1$ has a unique representation as a product of the powers of prime numbers.
23. A proper divisor of a number $n$ is a divisor of $n$ which is not itself $n$.
24. Every divisor of a number has its own set of divisors.
25. If a number $d$ divides $n$, then the set of divisors of $d$ is a subset of the set of divisors of $n$.
26. If $d$ is a proper divisor of $n$, then the set of divisors of $d$ is a proper subset of the divisors of $n$.
27. A proper divisor of a natural number $n$ has strictly fewer divisors than $n$.
28. Another characterization of a prime number $p$ is that the only proper divisor of $p$ is $1$.
29. The *prime factorization* of a number $n$ is the unique representation of $n$ as a product of powers of prime numbers.
30. If $n$ is prime, then that product is exactly $n$.
31. Since $2$ has a prime factorization, assume every number $2 < n \le k$for some number $k$ has a prime factorization.
32. If $k + 1$ is prime, then $k + 1$ is its factorization.
33. If $k + 1$ is composite, then there exist numbers $a$, $b$ which are greater than $1$ and less than $k+1$ such that $k+1 = ab$.
34. Since $a$ and $b$ have prime factorizations, $k+1$ must have one as well.
35. Suppose a number $m$ has multiple prime factorizations.
36. Then, there would be products $m = p_{0}p_{1}...p_{j} = q_{0}q_{1}...q_{i}$ for some $i$and $j$, where individual primes in these products are not necessarily unique.
37. By Euclid's lemma, each term of $p_{0}p_{1}...p_{j}$, must divide at least one of $q_{0}q_{1}...q_{i}$.
38. Since the terms of $p_{0}p_{1}...p_{j}$ and $q_{0}q_{1}...q_{i}$ are all prime numbers, however, if one term divides another term, those terms must be equal.
39. So, each term of $p_{0}p_{1}...p_{j}$ corresponds exactly to a term of $q_{0}q_{1}...q_{i}$.
40. As such, the prime factorization of $m$ is unique.
41. This property is called the fundamental theorem of arithmetic.
42. There is a function defined on positive integers called the *small omega* function $\omega$.
43. The small omega, $\omega(n)$, counts the number of *unique* prime numbers which divide $n$.
44. Higher powers of a number introduce no new unique prime factors, so for all positive integers $k$, $\omega(n)=\omega(n^k)$.
45. There is a function defined on positive integers called the *big omega* function $\Omega$.
46. The big omega, $\Omega(n)$, counts the number of prime numbers which divide $n$, including their multiples.
47. Another way of putting it is that $\Omega(n)$ counts the sum of all powers to which the prime factors of $n$ are taken.
48. That is, $\Omega(n^k)=k\Omega(n)$.
49. The small omega function is an *additive* function.
50. An additive function is a function $f$ of a positive integer such that if some numbers $a$ and $b$ are relatively prime, then $f(ab) = f(a) + f(b)$.
51. The big omega function is a *completely additive* function.
52. A completely additive function is a function $f$ for which the property $f(ab) = f(a) + f(b)$ holds for *all* positive integers $a$ and $b$.
53. A *square-free* number is a positive integer such that no prime in its factorization is raised to a power higher than $1$.
54. $1$ is square-free, because there are no primes in its factorization.
55. Every prime number is square-free.
56. If a composite number $ab$ is square-free, then $a$ must be relatively prime to $b$.
57. However, if $a$ is relatively prime to $b$, it is not necessarily the case that $ab$ is square-free, as $a$ and/or $b$ could themselves contain higher powers of primes in their factorizations.
58. Given a set $S$, a $k$-combination of elements of $S$ is a subset of $S$ with $k$ elements.
59. The products of numbers $a$ and $b$ which are relatively prime to one another have nicer combinatorial properties around the sets of divisors of $a$ and $b$ as opposed to products of numbers which are not relatively prime.
60. For example, suppose $x = ab$ and $y = cd$ for some prime numbers $a$,  $b$, $c$, and $d$.
61. Then, $xy = abcd$, and as such, the divisors of $xy$ are exactly the $16$ products of $k$-combinations of its prime factors $a$, $b$, $c$, and $d$, where $1$ is the product of a $0$-combination.
62. Since the set of all $k$-combinations of the elements of a set $S$ is effectively the power set of $S$, if $S$ has $n$ elements, then there are $2^n$ $k$-combinations of elements of $S$.
63. If a number $a$ has $n$ prime factors and a number $b$ has $m$ prime factors, and $a$ is relatively prime to $b$, then $ab$ has $n + m$ prime factors.
64. This is a restatement of the additivity of the small omega function.
65. Suppose that $n = ab$ and $m=ac$ for some prime numbers $a$, $b$, and  $c$.
66. Then, $nm = a^2bc$, i.e. $\omega(n) = 2$ and $\omega(m) = 2$, but $\omega(nm) = 3$: this is an example of how the additive function property fails to hold for numbers which are not relatively prime.
67. As such, the divisors of $nm$ are not exactly the products of the $k$-combinations of its prime factors $a$, $b$, and $c$.
68. Moreover, while e.g. $\Omega(abc) = \Omega(a^2b) = 3$, the latter has fewer divisors than the former.
69. Starting from $ab$, we have the divisors $1,$ $a$, $b$, and $ab$. Multiplying $c$ by $ab$, we gain $c$, $ac$, $bc$, and $abc$ as new divisors.
70. However, multiplying $a$ by $ab$, we only gain $a^2$ and $a^2b$ as new divisors.
71. The set of divisors of a square-free number $n$ has the same structure as the power set of the prime factors of $n$.
72. If a number $n$ is *not* square-free, then the set of divisors of $n$lacks this correspondence to the power set of its prime factors.
