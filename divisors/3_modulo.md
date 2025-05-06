# Modular arithmetic

1. Modular arithmetic is "wrap-around" arithmetic.
2. Given a *modulus* $m$, arithmetic operations on numbers "wrap around" at $m$.
3. It is sometimes introduced as "clock arithmetic," because the temporal units which divide a day, half-day, hour, and so on wrap around at $24$, $12$, and $60$ respectively, and so provide natural examples of moduli: if it is $17:00$, waiting for $10$ hours brings one to $3:00$ on the next day, as opposed to some $27:00$.
4. The properties of arithmetic over a modulus $m$ depend on the  set of divisors of $m$, so the description "clock arithmetic" has a critical flaw preventing it from being fully faithful to modular arithmetic.
5. That is, for e.g. hours of the day, addition and subtraction are the only arithmetic operations with motivation.
6. The properties which make a modulus $m$ a nice choice to serve as a temporal period are the same properties which make *multiplication* modulo $m$, structurally speaking, "very bad."
7. There is an equivalence relation between integers called *congruence modulo m*, where $m$ is a positive integer.
8. Two integers $a$ and $b$ are congruent modulo $m$ if there exists an integer $k$ such that $a - b = km$.
9. This condition is equivalent to $m$ dividing the difference between $a$ and $b$, and, since if a number divides an integer $n$, it must also divide $-n$, if there exists a $k$ for $a - b = km$, then there must exist a $k$ for $b - a = km$.
10. If integers $a$ and $b$ are congruent over a modulus $m$, we write $a \equiv b \pmod m$.
11. Congruence is reflexive: any number is congruent to itself under any modulus.
12. Congruence is *symmetric*. If $a \equiv b \pmod m$, then $b \equiv a \pmod m$.
13. Congruence is transitive. If $a \equiv b \pmod m$ and $b \equiv c \pmod m$ then $a \equiv c \pmod m$.
14. Reflexivity, symmetry, and transitivity are the conditions for a relation to be an equivalence relation.
15. An equivalence relation splits a set into *equivalence classes.*
16. Equality is obviously an equivalence relation, and it splits the set of integers into equivalence classes which each contain one integer.
17. Another equivalence relation one can impose on the integers is $|n| = |m|$. We will call this relation $A$.
18. If one takes the set of all subsets of $\mathbb{Z}$ where the absolute value of every element of the subset equals the absolute value of every other in the subset, then we can partition $\mathbb{Z}$ into a set of equivalence classes $\mathbb{Z} / A = \set{\set{0}, \set{-1, 1}, \set{-2, 2}, ...}$.
19. If we take the set of non-negative *class representatives* of  $\mathbb{Z}/A$, then we simply get $\mathbb{N}$.
20. The set of equivalence classes one gets from partitioning a set $S$ according to an equivalence relation $R$ is called a *quotient set*, and it is denoted $S / R$.
21. We will use $m\mathbb{Z}$ as a symbol meaning "congruence modulo $m$."
22. For every positive integer $m$, there is a unique quotient set corresponding to the set of equivalence classes of integers when partitioned according to $m\mathbb{Z}$. We conventionally denote this set $\mathbb{Z}/m\mathbb{Z}$.
23. Conventionally, we often perform modular arithmetic using the *least residue system* of a modulus $m$, which is simply the set of all non-negative integers which are less than $m$.
24. These integers serve as the class representatives of $\mathbb{Z}/m\mathbb{Z}$, and it is frequently convenient to use $\mathbb{Z}/m\mathbb{Z}$ to refer to the set of representatives as opposed to the set of classes.
25. In practice, a modulus takes the arithmetic of a set of infinitely many integers and sends it to a finite set of integers.
26. Addition and subtraction work "normally" over any modulus.
27. A better way of saying this is that addition on $\mathbb{Z}/m\mathbb{Z}$ always forms a *group* of order $m$ for any modulus $m$.
28. A group is a structure comprising a set and an operation which together satisfy certain requirements.
29. Let $S$ be an arbitrary set and $*$ be an arbitrary operation.
30. The first requirement is closure under the operation: $\forall{a, b}\in{S}, a * b\in{S}$.
31. The second is that the operation has an identity: $\exists{e}\in{S}:\forall{a}\in{S},a*e=e*a=a$.
32. The third is that the operation is associative: $\forall{a, b, c}\in{S}, a * (b*c)=(a*b)*c$
33. The fourth (and most restrictive) requirement is that every element in the set has an *inverse* under the operation.
34. That is, $\forall{a}\in S, \exists{a^{-1}} \in S: a * a^{-1}= a^{-1} * a=e$.
35. An *abelian* group is a group whose operation is commutative.
36. That is, $\forall{a, b} \in S, a * b = b * a$.
37. Groups from arithmetic tend to be commutative because e.g. addition and multiplication of individual numbers are both commutative, and our focus is largely on groups formed out of these operations, but there are many ways to achieve a group structure without commutativity.
38. For example, the set of all element rearrangements (or permutations) of a set of $n$ elements forms a group under composition of permutations (called the *symmetric group of degree $n$*), but the composition of permutations is not in general commutative.
39. The *order* of a group is the cardinality of its underlying set, or how many elements are in the group.
40. Addition over $\mathbb{Z}$ is an abelian group. Every positive integer $n$ has a corresponding negative integer $-n$ (and vice versa) which serves as its *additive inverse.*
41. $0$ is its own inverse, because it is the additive identity, and it follows from the definition of an identity of a group that a two-sided identity element is always its own inverse.
42. If a set has elements without inverses w/r/t an operation, but retains closure, associativity, and an identity element, then that set and operation form a *monoid* as opposed to a group.
43. Multiplication over $\mathbb{Z}$ is a monoid and *not* a group, because non-unit integers do not have other integers as multiplicative inverses.
44. For any modulus $m$, any element $n$ of $\mathbb{Z}/m\mathbb{Z}$ has a corresponding element $k = m - n$ such that $n + k \equiv 0 \pmod m$, so an additive inverse is always present.
45. From the clock perspective, this is expressed in the notion that whatever hour it is, there is always some number of hours one can wait until the day ends.
46. From the clock perspective, the more "highly composite" a modulus $m$ is, i.e. the more divisors it has relative to its size, the better it is for convenient time-keeping.
47. For any modulus $m$, the equivalence class whose representative is $0$ is the set of multiples of $m$.
48. Consider $ab \equiv 0 \pmod{p}$, where $p$ is prime: since the divisors of $p$ are exactly $1$ and $p$, for any product of positive integers $a$ and $b$, given $ab = p$, either $a = p$ and $b = 1$ or $a = 1$ and $b = p$.
49. So, effectively, the only way to get a product of $0$ in a prime modulus is to multiply a number by $0$ or a multiple of $p$.
50. Now, consider a product like $ab \equiv 0 \pmod{12}$: $a$ could be $2$ if $b$ is $6$, or $a$ could be $3$ if $b$ is $4$, and vice versa.
51. This is to say, two numbers, of which neither is in the "0 class" of the modulus, can multiply with each other to get 0.
52. We will denote the *multiplicative* group of a modulus $m$ with $(\mathbb{Z}/m\mathbb{Z})^{\times}$.
53. While the order of $(\mathbb{Z}/m\mathbb{Z})^{+}$ is always $m$, the set underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ has to have at most $m-1$ elements, provided $m > 1$.
54. This is because $1$ is the identity element of multiplication, and there is no way to get a number which is not $0$ from a product with $0$ as a term.
55. That is, $0$ can never have a multiplicative inverse, so it is excluded from the set.
56. The exception to this is the case where $m = 1$, since all of $\mathbb{Z}$ is collapsed into a single equivalence class represented by $0$, and $0$ times $0$ is $0$, meaning $(\mathbb{Z}/1\mathbb{Z})^{\times}$ is actually a group of order $1$.
57. So, if $ab \equiv 0 \pmod{m}$, and neither $a$ nor $b$ is $0$, then $a$ and $b$ violate the closure condition required of a group.
58. For this reason, the set of representatives underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is the set of positive integers less than or equal to $m$ which are relatively prime to $m$.
59. There is a function defined on positive integers called *Euler's phi function*.
60. For a number $n$, $\varphi(n)$ counts the number of positive integers less than *or equal to* $n$ which are relatively prime to $n$.
61. $1$ is the unique number which is relatively prime to itself, because $\gcd(n, n) = n$.
62. This means that $1$ is the unique value for $n$ such that $\varphi(n) = n$.
63. It is the case that $p$ is a prime number if and only if $\varphi(p) = p - 1$.
64. For $\varphi(p) = p - 1$ to not be the case, then there would have to be a number less than $p$ but greater than $1$ which divides $p$.
65. So, it follows that the order of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is $\varphi(m)$, i.e. $m - 1$ if and only if $m$ is prime.
66. It is often useful to consider the *negative* class representatives of a modulus, for the reason that $-a \equiv m-a \pmod{m}$.
67. $1$ is its own mutiplicative inverse for any modulus, and since $(-1)(-1) = 1$, $m - 1$ is also its own multiplicative inverse for any modulus.
68. Bézout's identity guarantees that if an integer $a$ is relatively prime to $m$, then there exist integers $x$ and $y$ such that $ax + my = 1$.
69. It follows, then, that $ax \equiv{1} \pmod{m}$, i.e. $x$ is the multiplicative inverse of $a$ modulo $m$.
70. There is yet another way to characterize the prime numbers, equivalent to the previous characterizations.
71. A number $p$ is prime if and only if it is the case that $(p - 1)! \equiv -1 \pmod{p}$.
72. Suppose $(n - 1)! \equiv -1 \pmod{n}$ were the case for some composite $n$.
73. A composite number $n$ is divisible by some number $k$ such that $2 \le k < n$.
74. Therefore, since $(n - 1)!$ is divisible by every number less than $n$, $k$ must divide both $n$ and $(n - 1)!$, and so $\gcd((n - 1)!, n)$ must be at least $k$.
75. However, for $(n - 1)! \equiv -1 \pmod{n}$ to be the case, then $\gcd((n - 1)!, n)$ must equal $1$.
76. Note that for $a \equiv -1 \pmod{m}$ to be the case, then there must exist an integer $k$ such that $a = km - 1$.
77. This can be rewritten as $a - km = -1$.
78. If a number divides both $a$ and $km$, then it must divide $a - km$, i.e. $-1$, and so $\gcd(a, km) = 1$.
79. Since $\gcd((n - 1)!, n) \ge k \ge 2$, $(n - 1)! \equiv -1 \pmod{n}$ cannot hold for composite $n$.
80. If $n$ is $1$, then, trivially, $0! \equiv 0 \pmod{1}$.
81. For prime $n$, consider that every element of $(\mathbb{Z}/n\mathbb{Z})^{\times}$ has a multiplicative inverse.
82. Since $(n - 1)!$ is the product of the entire least residue system of modulo $n$ (excepting $0$), $(n - 1)!$ can be arranged into a product of pairs of elements of $(\mathbb{Z}/n\mathbb{Z})^{\times}$ in the form $ab \equiv 1 \pmod{n}$ and $n - 1 \equiv -1 \pmod {n}$.
83. Since it is only for prime $n$ where every positive integer $\le n$ has a multiplicative inverse modulo $n$, it is only for prime $n$ where the product of every positive integer less than $n$ inevitably takes the form $(1)(1)...(-1)$.
84. As such, $(p - 1)! \equiv -1 \pmod{p}$ holds for all prime $p$ and only for prime $p$.
85. The above property is called Wilson's theorem.
86. If $a$ is an integer and $p$ is a prime number, then $a^p \equiv a \pmod {p}$.
87. The binomial theorem is a statement about the expansion of expressions in the form $(x + y)^n$:$$(x + y)^n = \sum^{n}_{k=0}\binom{n}{k}x^{k}y^{n-k};\binom{n}{k} = \frac{n!}{k!(n - k)!}$$
88. $\binom{n}{k}$ is called a *binomial coefficient,* and is read out as "$n$ choose $k$."
89. A binomial coefficient is always an integer: all multiples of primes in the factorization of $k!(n - k)!$ must also be in the factorization of $n!$.
90. If $n$ is prime, then $n$ divides $\binom{n}{k}$ for all $0 < k < n$. This is because $n$ always divides $n!$, but since $n$ is prime, it cannot divide $k!(n - k)!$ unless $k = 0$ or $k = n$.
91. As a consequence of this for prime $n$, the only terms of the sum not "zeroed out" by a coefficient which is a multiple of $n$ are $\binom{n}{0}x^{0}y^{p}$ and $\binom{n}{n}x^{p}y^{0}$.
92. This means that if $n$ is prime, then $(x + y)^n \equiv x^n + y^n \pmod{n}$.
93. Trivially, it holds that $1^p \equiv 1 \pmod {p}$ for a prime $p$.
94. If we assume that for some integer $k$, $k^p \equiv k \pmod {p}$ is the case, then we can say that since the freshman's dream comes true for a prime modulus $p$, i.e. $(k + 1)^p \equiv k^p + 1^p \pmod{p}$, it follows that $(k + 1)^p \equiv k + 1 \pmod{p}$.
95. This is exactly our original statement $a^p \equiv a \pmod {p}$, which is called Fermat's little theorem.
96. A *primitive root* modulo $m$ is a number $n$ in $(\mathbb{Z}/m\mathbb{Z})^{\times}$ which *generates* every element of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ through repeated multiplication.
97. That is, if $c$ being an element of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ implies that there exists an integer $k$ such that $c \equiv n^k \pmod{m}$, then $n$ is a primitive root modulo $m$.
98. Only certain moduli have primitive roots: only if $m$ is $1$, $2$, $4$, $p^k$, or $2p^k$, where $p$ is an odd prime and $k$ is a positive integer, then the modulus $m$ has at least one primitive root.
99. If $n$ is a primitive root modulo $m$, then the multiplicative inverse of $n$ is also a primitive root modulo $m$.
100. A group where all of its elements can be generated by repeat iterations of its operation on a single element and that element's inverse is called a *cyclic* group.
101. The integers under addition form the archetypal infinite cyclic group, since any integer can be reached from a sum of terms of $-1$ and $1$.
102. $(\mathbb{Z}/m\mathbb{Z})^{+}$ is the archetypal finite cyclic group, being cyclic for every modulus: the cyclic group of order $m$ is often denoted simply $\mathbb{Z}_m$.
103. For any modulus $m$, one can get all of the elements in $\mathbb{Z}_m$ from repeated addition by 1.
104. All cyclic groups are abelian, but not every abelian group is cyclic.
105. It follows from the definition of a primitive root that a group $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is cyclic if and only if it has a primitive root.
106. The primitive roots of a modulus give rise to the idea of the *index of a residue,* or its generalization for any finite group, the "discrete logarithm."
107. The index of a residue $a$ with respect to a base $b$ and modulus $m$ is the power $k$ to which $b$ must be raised such that $b^k \equiv a \pmod{m}$.
108. That is, if one knows only $b$ and $k$ for some modulus $m$, it is easy to find $a$, but if one knows only $b$ and $a$, it is much harder to find $k$.
