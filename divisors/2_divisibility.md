# Divisors in brief

"Number" by itself is always to be taken as meaning "natural number" or "nonzero natural number" when it doesn't make sense for zero to be part of the conversation.

"->" is usually used to mean "rewrite."

## Elementary divisibility

1. A nonzero integer $m$ *divides* an integer $n$ if there exists an integer $k$ such that $n = mk$.
2. A number which divides $n$ is called a *divisor* of $n$.
3. The symbol to denote that $n$ divides $m$ is $n \mid m$.
4. If $k$ is nonzero, then $k$ also divides $n$.
5. Division by $0$ is undefined.
6. Every nonzero integer divides $0$.
7. That is, for every integer $n$, $0 = 0n$.
8. If $n$ divides $m$, $-n$ also divides $m$.
9. That is, if $n = mk$, then $n = (-m)(-k)$.
10. For this reason, "divisors" is universally shorthand for "positive divisors."
11. Every non-zero integer divides itself.
12. This property is called the *reflexivity* of divisibility.
13. If $n$ divides $m$, then $|n| \le |m|$.
14. If $n$ divides $m$ *and* $m$ divides $n$, then $|m| = |n|$.
15. This property is called the *antisymmetry* of divisibility.
16. For integers $a$, $b$, $c$, if $a \mid b$ and $b \mid c$, then $a \mid c$.
17. Consider that if $a \mid b$, then there exists an integer $x$ such that $b = ax$, and if $b \mid c$, then there exists an integer $y$ such that $c = by$.
18. We can write $c = axy$, so $a$ must divide $c$.
19. This property is called the *transitivity* of divisibility.
20. $1$ divides every integer.
21. $1$ is the unique positive integer which has only $1$ divisor.
22. If a positive integer $p > 1$ has exactly $2$ divisors, then its divisors are exactly $1$ and $p$.
23. A positive integer with exactly $2$ divisors is called a prime number.
24. A positive integer with more than 2 divisors is called a composite number.
25. $1$ is neither prime nor composite.
26. If a number is divisible by $2$, it is called an *even* number.
27. $0$ is even, but neither prime nor composite.
28. $2$ is the unique even prime number.
29. Any even number $n > 2$ has to have at least $3$ divisors: $1$, $2$, and $n$.
30. If a number is not divisible by $2$, it is called an *odd* number.
31. A perfect square is a positive integer $n$ such that there exists an integer $k$ such that $n = k^2$.
32. $1$ is a perfect square.
33. If a number has an odd amount of divisors, it must be a perfect square.
34. This is because divisors come in pairs.
35. Consider the meaning of a divisor of a positive integer, i.e. $(\exists{k \in \mathbb{Z}^+} : m = nk)\implies(n \mid m \land k \mid m)$.
36. That is, if $n$ divides $m$, there exists some $k$ which divides $m$.
37. So, it is only if $n = k$ that $n$ dividing $m$ does not entail that a *separate* $k$ also divides $m$.
38. The notation for if a number $n$ *doesn't* divide another number $m$is $n \nmid m$.
39. This motivates the idea of *division with remainder*.
40. Suppose one wants to find the *remainder* $r$ of the number $a$ when divided by $b$.
41. If $b$ divides $a$, then $r = 0$, and there exists some unique *quotient* $q$ such that $a = bq$.
42. If $b$ doesn't divide $a$, then there exists some unique quotient $q$ such that $bq < a < b(q+1)$.
43. So, there must exist some unique $r$ such that $b > r > 0$ and $a = bq + r$.
44. This is called the lemma of Euclidean division.
45. The remainder $r$ of $a$ when divided by $b$ is also read as $a$ modulo $b$.
46. In symbols, we can write this $r = a \bmod b$.
47. Two integers $a$ and $b$ always have a *greatest common divisor*.
48. The greatest common divisor of $a$ and $b$ is the largest integer which divides both $a$ and $b$.
49. The greatest common divisor of two integers is always a non-negative integer.
50. The greatest common divisor of an integer $n$ and $0$ is always the absolute value of $n$.
51. Although $0$ divides no integer, $\gcd(0, 0)= 0$ by convention.
52. If $a > b$, then $\gcd(a, b) = \gcd(b, a \bmod b)$.
53. Consider that we can rewrite the expression in the division lemma into $r = a - bq$. Since $bq$ is an integer multiple of $b$, $d \mid bq$.
54. Since $a$ and $bq$ must be integer multiples of $d$, $d$ must divide $a - bq$.
55. That is, there must exist integers $x$ and $y$ such that $a = dx$ and $b = dy$, and so we can rewrite the division lemma into $r = dx - dyq$ and again into $r = d(x - yq)$.
56. So far we have proved that the GCD of $a$ and $b$ divides $r$, but we have not proved that it is the maximal number which divides $r$.
57. Suppose $d' = \gcd(b, r)$. Then, by the same logic applied to $d = \gcd(a, b)$, $d' \mid a$.
58. Since $d'$ divides both $a$ and $b$, it has to be less than or equal to $d = \gcd(a, b)$. Since $d$ divides both $b$ and $r$, it has to be less than or equal to $d' = \gcd(b, r)$.
59. So, $d = d'$.
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
