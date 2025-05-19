# Divisors in brief

"Number" by itself is always to be taken as meaning "natural number" or "nonzero natural number" when it doesn't make sense for zero to be part of the conversation.

"->" is usually used to mean "rewrite."

## Elementary divisibility

1. A nonzero integer $m$ *divides* an integer $n$ if there exists an integer $k$ such that $n = mk$.
2. A number which divides $n$ is called a *divisor* of $n$.
3. The symbol to denote that $n$ divides $m$ is $n \mid m$.
4. If $k$ is nonzero, then $k$ also divides $n$.
5. Division by $0$ is undefined.
6. Every nonzero integer divides $0$: for every integer $n$, $0 = 0n$.
7. If $n$ divides $m$, $-n$ also divides $m$.
8. That is, if $n = mk$, then $n = (-m)(-k)$.
9. For this reason, "divisors" is universally shorthand for "positive divisors."
10. Every non-zero integer divides itself.
11. This property is called the *reflexivity* of divisibility.
12. If $n$ divides $m$ *and* $m$ divides $n$, then $|m| = |n|$.
13. This property is called the *antisymmetry* of divisibility.
14. For integers $a$, $b$, $c$, if $a \mid b$ and $b \mid c$, then $a \mid c$.
15. Consider that if $a \mid b$, then there exists an integer $x$ such that $b = ax$, and if $b \mid c$, then there exists an integer $y$ such that $c = by$.
16. We can write $c = axy$, so $a$ must divide $c$.
17. This property is called the *transitivity* of divisibility.
18. If $n$ divides $m$, then $|n| \le |m|$.
19. A proper divisor of a number $n$ is a divisor of $n$ which is not itself $n$.
20. If a number $d$ divides $n$, then the set of divisors of $d$ is a subset of the set of divisors of $n$.
21. If $d$ is a proper divisor of $n$, then the set of divisors of $d$ is a proper subset of the divisors of $n$.
22. A proper divisor of a natural number $n$ has strictly fewer divisors than $n$.
23. Another characterization of a prime number $p$ is that the only proper divisor of $p$ is $1$.
24. $1$ divides every integer, and uniquely has only $1$ divisor.
25. If a positive integer $p > 1$ has exactly $2$ divisors, then its divisors are exactly $1$ and $p$.
26. A positive integer with exactly $2$ divisors is called a prime number.
27. A positive integer with more than 2 divisors is called a composite number.
28. $1$ is neither prime nor composite.
29. If a number is divisible by $2$, it is called an *even* number.
30. $0$ is even, but neither prime nor composite.
31. $2$ is the unique even prime number.
32. Any even number $n > 2$ has to have at least $3$ divisors: $1$, $2$, and $n$.
33. If a number is not divisible by $2$, it is called an *odd* number.
34. A perfect square is a positive integer $n$ such that there exists an integer $k$ such that $n = k^2$.
35. If a number has an odd amount of divisors, it must be a perfect square.
36. This is because divisors come in pairs.
37. Consider the meaning of a divisor of a positive integer, i.e. $(\exists{k \in \mathbb{Z}^+} : m = nk)\implies(n \mid m \land k \mid m)$.
38. That is, if $n$ divides $m$, there exists some $k$ which divides $m$.
39. So, it is only if $n = k$ that $n$ dividing $m$ does not entail that a *separate* $k$ also divides $m$.
40. The notation for if a number $n$ *doesn't* divide another number $m$is $n \nmid m$.
41. This motivates the idea of *division with remainder*.
42. Suppose one wants to find the *remainder* $r$ of the number $a$ when divided by $b$.
43. If $b$ divides $a$, then $r = 0$, and there exists some unique *quotient* $q$ such that $a = bq$.
44. If $b$ doesn't divide $a$, then there exists some unique quotient $q$ such that $bq < a < b(q+1)$.
45. So, there must exist some unique $r$ such that $b > r > 0$ and $a = bq + r$.
46. This is called the lemma of Euclidean division.
47. The remainder $r$ of $a$ when divided by $b$ is also read as $a$ modulo $b$.
48. In symbols, we can write this $r = a \bmod b$.
49. Two integers $a$ and $b$ always have a *greatest common divisor*.
50. The greatest common divisor of $a$ and $b$ is the largest integer which divides both $a$ and $b$.
51. The greatest common divisor of two integers is always a non-negative integer.
52. The greatest common divisor of an integer $n$ and $0$ is always the absolute value of $n$.
53. Although $0$ divides no integer, $\gcd(0, 0)= 0$ by convention.
54. If $a > b$, then $\gcd(a, b) = \gcd(b, a \bmod b)$.
55. Consider that we can rewrite the expression in the division lemma into $r = a - bq$. Since $bq$ is an integer multiple of $b$, $d \mid bq$. Since $a$ and $bq$ must be integer multiples of $d$, $d$ must divide $a - bq$.
56. That is, there must exist integers $x$ and $y$ such that $a = dx$ and $b = dy$, and so we can rewrite the division lemma into $r = dx - dyq$ and again into $r = d(x - yq)$.
57. So far we have proved that the GCD of $a$ and $b$ divides $r$, but we have not proved that it is the maximal number which divides $r$.
58. Suppose $d' = \gcd(b, r)$. Then, by the same logic applied to $d = \gcd(a, b)$, $d' \mid a$.
59. Since $d'$ divides both $a$ and $b$, it has to be less than or equal to $d = \gcd(a, b)$. Since $d$ divides both $b$ and $r$, it has to be less than or equal to $d' = \gcd(b, r)$, and so, $d = d'$.
60. The properties $\gcd(n, 0) = n$ and $\gcd(a, b) = \gcd(b, a \bmod b)$ provide a base case and a recursive step respectively for an algorithm which computes the greatest common divisor of two numbers.
61. This algorithm is called Euclid's algorithm.
62. Euclid's algorithm always terminates, because $a \bmod b$ is always strictly less than $b$.
63. We can write its steps as a sequence of modified division lemmas: $a = bq_1 + r_1$ -> $b = r_1q_2 + r_2$ -> $r_1 = r_2q_3 + r_3$... where, if $r_n = 0$, then the product with $q_n$ (i.e. $r_{n-1}$) is the GCD of $a$ and $b$.
64. Closed form expressions emerge: $r_{n-3} = r_{n-2}q_{n-1} + r_{n-1}$ -> $r_{n-1} = r_{n-3} - r_{n-2}q_{n-1}$.
65. Since $r_n = 0$, $r_{n-1} = \gcd(a, b)$.
66. For any integers $a$, $b$, there exist integers $x$ and $y$ such that $ax + by = \gcd(a, b)$.
67. This property is called Bézout's identity.
68. We can rewrite $\gcd(a, b) = r_{n-3} - r_{n-2}q_{n-1}$.
69. We can then substitute back until we can express the GCD purely as the multiples of $a$ and $b$.
70. To illustrate, note that $r_1 = a - bq_1$, so we can rewrite $a = bq_1 + r_1$ -> $a = bq_1 + (a - bq_1)$ and $b = r_1q_2 + r_2$ -> $b = (a - bq_1)q_2 + r_2$.
71. Since $r_2 = b - (a - bq_1)q_2$, we can rewrite $b = (a - bq_1)q_2 + r_2$ -> $b = (a - bq_1)q_2 + (b - (a - bq_1)q_2)$, and so on.
72. It is clear that any remainder taken through this process can be expressed as a linear combination of $a$ and $b$.

## Exercises

1. The least common multiple of two integers $a$ and $b$ is the smallest positive integer $c$ such that $a \mid c$ and $b \mid c$. It can be expressed as a ratio in terms of $a$, $b$, and $\gcd(a, b)$. Find and justify the expression for this ratio. Hint: since $\text{lcm}(a, b)$ is always positive, it would not be insensible to consider the absolute value function's involvement.
2. The Fibonacci sequence is defined by a recurrence relation where $F_0 = 0$, $F_1 = 1$, and $F_n = F_{n-1} + F_{n-2}$ for $n > 1$. Show that for $n > 5$, finding $\gcd(F_n, F_{n-1})$ via Euclid's algorithm takes $n - 2$ steps.
3. Given the expression of Bézout's identity, $ax + by = \gcd(a, b)$, the integers $x$ and $y$ are not unique, and are in fact infinite in legion. During the computation of $\gcd(a, b)$ via Euclid's algorithm, the quotient is at each step thrown away while the remainder is carried along to its destination. Using these forlorn quotients, derive an "*extended Euclidean algorithm*," which, given two integers $a$ and $b$, computes not only $\gcd(a, b)$, but also some pair of integers $x$ and $y$ such that $ax + by = \gcd(a, b)$.
