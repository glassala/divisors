# Integer divisibility

*Divisor of an integer. Prime and composite numbers. Euclidean division. Greatest common divisor. Euclid's algorithm. Bézout's identity. Factorial function. Euclid's theorem. Euler's phi function. Euclid's lemma. Fundamental theorem of arithmetic. Prime omega functions. Square-free numbers.*

"Number" by itself is always to be taken as meaning "natural number" or "nonzero natural number" when it doesn't make sense for zero to be part of the conversation.

1. A nonzero integer $m$ *divides* an integer $n$ if there exists an integer $k$ such that $n = mk.$

2. A number which divides $n$ is called a *divisor* of $n.$

3. The symbol to denote that $n$ divides $m$ is $n \mid m.$

4. If $k$ is nonzero, then $k$ also divides $n.$

5. Division by $0$ is undefined.

6. Every nonzero integer divides $0$: for every integer $n$, $0 = 0n.$

7. If $n$ divides $m$, $-n$ also divides $m.$

8. That is, if $n = mk$, then $n = (-m)(-k).$

9. For this reason, "divisors" is universally shorthand for "positive divisors."

10. Every non-zero integer divides itself.

11. This property is called the *reflexivity* of divisibility.

12. If $n$ divides $m$ *and* $m$ divides $n$, then $|m| = |n|.$

13. This property is called the *antisymmetry* of divisibility.

14. For integers $a$, $b$, $c$, if $a \mid b$ and $b \mid c$, then $a \mid c.$

15. Consider that if $a \mid b$, then there exists an integer $x$ such that $b = ax$, and if $b \mid c$, then there exists an integer $y$ such that $c = by.$

16. We can write $c = axy$, so $a$ must divide $c.$

17. This property is called the *transitivity* of divisibility.

18. If $n$ divides $m$, then $|n| \le |m|.$

19. A proper divisor of a number $n$ is a divisor of $n$ which is not itself $n.$

20. If a number $d$ divides $n$, then the set of divisors of $d$ is a subset of the set of divisors of $n.$

21. If $d$ is a proper divisor of $n$, then the set of divisors of $d$ is a proper subset of the divisors of $n.$

22. A proper divisor of a natural number $n$ has strictly fewer divisors than $n.$

23. A characterization of a *prime number* $p$ is that the only proper divisor of $p$ is $1.$

24. $1$ divides every integer, and uniquely has only $1$ divisor.

25. If a positive integer $p > 1$ has exactly $2$ divisors, then its divisors are exactly $1$ and $p.$

26. A positive integer with exactly $2$ divisors is called a prime number.

27. A positive integer with more than 2 divisors is called a composite number.

28. $1$ is neither prime nor composite.

29. If a number is divisible by $2$, it is called an *even* number.

30. $0$ is even, but neither prime nor composite.

31. $2$ is the unique even prime number.

32. Any even number $n > 2$ has to have at least $3$ divisors: $1$, $2$, and $n.$

33. If a number is not divisible by $2$, it is called an *odd* number.

34. A perfect square is a positive integer $n$ such that there exists an integer $k$ such that $n = k^2.$

35. If a number has an odd amount of divisors, it must be a perfect square.

36. This is because divisors come in pairs.

37. Consider the meaning of a divisor of a positive integer, i.e. $(\exists{k \in \mathbb{Z}^+} : m = nk)\implies(n \mid m \land k \mid m).$

38. That is, if $n$ divides $m$, there exists some $k$ which divides $m.$

39. So, it is only if $n = k$ that $n$ dividing $m$ does not entail that a *separate* $k$ also divides $m.$

40. The notation for if a number $n$ *doesn't* divide another number $m$is $n \nmid m.$

41. This motivates the idea of *division with remainder.*

42. Suppose one wants to find the *remainder* $r$ of the number $a$ when divided by $b.$

43. If $b$ divides $a$, then $r = 0$, and there exists some unique *quotient* $q$ such that $a = bq.$

44. If $b$ doesn't divide $a$, then there exists some unique quotient $q$ such that $bq < a < b(q+1).$

45. So, there must exist some unique $r$ such that $b > r > 0$ and $a = bq + r.$

46. This is called the lemma of Euclidean division.

47. The remainder $r$ of $a$ when divided by $b$ is also read as $a$ modulo $b.$

48. In symbols, we can write this $r = a \bmod b.$

49. Two integers $a$ and $b$ always have a *greatest common divisor*.

50. The greatest common divisor of $a$ and $b$ is the largest integer which divides both $a$ and $b.$

51. The greatest common divisor of two integers is always a non-negative integer.

52. The greatest common divisor of an integer $n$ and $0$ is always the absolute value of $n.$

53. Although $0$ divides no integer, $\gcd(0, 0)= 0$ by convention.

54. If $a > b$, then $\gcd(a, b) = \gcd(b, a \bmod b).$

55. Consider that we can rewrite the expression in the division lemma into $r = a - bq.$ Since $bq$ is an integer multiple of $b$, $d \mid bq.$ Since $a$ and $bq$ must be integer multiples of $d$, $d$ must divide $a - bq.$

56. That is, there must exist integers $x$ and $y$ such that $a = dx$ and $b = dy$, and so we can rewrite the division lemma into $r = dx - dyq$ and again into $r = d(x - yq).$

57. So far we have proved that the GCD of $a$ and $b$ divides $r$, but we have not proved that it is the maximal number which divides $r.$

58. Suppose $d' = \gcd(b, r).$ Then, by the same logic applied to $d = \gcd(a, b)$, $d' \mid a.$

59. Since $d'$ divides both $a$ and $b$, it has to be less than or equal to $d = \gcd(a, b).$ Since $d$ divides both $b$ and $r$, it has to be less than or equal to $d' = \gcd(b, r)$, and so, $d = d'.$

60. The properties $\gcd(n, 0) = n$ and $\gcd(a, b) = \gcd(b, a \bmod b)$ provide a base case and a recursive step respectively for an algorithm which computes the greatest common divisor of two numbers.

61. This algorithm is called Euclid's algorithm.

62. Euclid's algorithm always terminates, because $a \bmod b$ is always strictly less than $b.$

63. We can write its steps as a sequence of modified division lemmas: $a = bq_1 + r_1$ -> $b = r_1q_2 + r_2$ -> $r_1 = r_2q_3 + r_3.$.. where, if $r_n = 0$, then the product with $q_n$ (i.e. $r_{n-1}$) is the GCD of $a$ and $b.$

64. Closed form expressions emerge: $r_{n-3} = r_{n-2}q_{n-1} + r_{n-1}$ -> $r_{n-1} = r_{n-3} - r_{n-2}q_{n-1}.$

65. Since $r_n = 0$, $r_{n-1} = \gcd(a, b).$

66. For any integers $a$, $b$, there exist integers $x$ and $y$ such that $ax + by = \gcd(a, b).$

67. This property is called Bézout's identity.

68. We can rewrite $\gcd(a, b) = r_{n-3} - r_{n-2}q_{n-1}.$

69. We can then substitute back until we can express the GCD purely as the multiples of $a$ and $b.$

70. To illustrate, note that $r_1 = a - bq_1$, so we can rewrite $a = bq_1 + r_1$ -> $a = bq_1 + (a - bq_1)$ and $b = r_1q_2 + r_2$ -> $b = (a - bq_1)q_2 + r_2.$

71. Since $r_2 = b - (a - bq_1)q_2$, we can rewrite $b = (a - bq_1)q_2 + r_2$ -> $b = (a - bq_1)q_2 + (b - (a - bq_1)q_2)$, and so on.

72. It is clear that any remainder taken through this process can be expressed as a sum of multiples of $a$ and $b.$

73. There is a function of a natural number called the *factorial* function.

74. The factorial of a number $n$ is denoted $n!$ and characterized by a recursive formula: the base case is that $0! = 1$, and the recursive step is that $n! = (n-1)!n.$

75. In practice, for any positive integer $n$, $n!$ is the product of every positive integer less than or equal to $n.$

76. As a consequence of this, for all positive integers $k \le n$, $k$ divides $n!.$

77. There are infinitely many prime numbers.

78. This is called Euclid's theorem.

79. Since $a > b \implies \gcd(a, b) = \gcd(b, a \pmod{b})$, for any number $n$, the only divisor common to $n$ and $n+1$ is $1.$

80. Suppose there is a largest prime number $p.$

81. Then, $p!$ is divisible by every prime number.

82. However, this would imply that $p! + 1$ is divisible by *no* prime number, which cannot be the case.

83. As such, for every largest prime number, a larger prime exists.

84. If two numbers $a$ and $b$ have a GCD of $1$, then $a$ and $b$ are called *relatively prime* to one another. A way to denote that $a$ and $b$ are relatively prime is $a \bot b.$

85. A way to characterize a prime number $n$ is as a number which is relatively prime to every positive integer less than $n.$

86. There is a function defined on positive integers called *Euler's phi function*.

87. For a number $n$, $\varphi(n)$ counts the number of positive integers less than *or equal to* $n$ which are relatively prime to $n.$

88. $1$ is the unique number which is relatively prime to itself, because $\gcd(n, n) = n.$

89. This means that $1$ is the unique value for $n$ such that $\varphi(n) = n.$

90. It is the case that $p$ is a prime number if and only if $\varphi(p) = p - 1.$

91. For $\varphi(p) = p - 1$ to not be the case, then there would have to be a number less than $p$ but greater than $1$ which divides $p.$

92. If a prime number $p$ divides a composite number $ab$, then $p$ divides at least either $a$ or $b.$

93. If $p$ does not divide $a$, then, because $1$ is the only other divisor of $p$, $\gcd(p, a)=1.$

94. So, there must exist integers $x$ and $y$ such that $px + ay = 1.$

95. Suppose we multiply this expression by $b$: $pbx + aby = b.$

96. We know that $p \mid ab$, so we can see that $p$ can be factored out of the left side, and so $p \mid b.$

97. This property is called Euclid's lemma.

98. This lemma is indeed a lemma about division attributed to Euclid, but it is not to be confused with Euclid's division lemma.

99. Every natural number which is greater than $1$ has a unique representation as a product of the powers of prime numbers.

100. The *prime factorization* of a number $n$ is the unique representation of $n$ as a product of powers of prime numbers.

101. If $n$ is prime, then that product is exactly $n.$

102. Since $2$ has a prime factorization, assume every number $2 < n \le k$ for some number $k$ has a prime factorization.

103. If $k + 1$ is prime, then $k + 1$ is its factorization.

104. If $k + 1$ is composite, then there exist numbers $a$, $b$ which are greater than $1$ and less than $k+1$ such that $k+1 = ab.$

105. Since $a$ and $b$ have prime factorizations, $k+1$ must have one as well.

106. Suppose a number $m$ has multiple prime factorizations.

107. Then, there would be products $m = p_{0}p_{1}...p_{j} = q_{0}q_{1}...q_{i}$ for some $i$and $j$, where individual primes in these products are not necessarily unique.

108. By Euclid's lemma, each term of $p_{0}p_{1}...p_{j}$, must divide at least one of $q_{0}q_{1}...q_{i}.$

109. Since the terms of $p_{0}p_{1}...p_{j}$ and $q_{0}q_{1}...q_{i}$ are all prime numbers, however, if one term divides another term, those terms must be equal.

110. So, each term of $p_{0}p_{1}...p_{j}$ corresponds exactly to a term of $q_{0}q_{1}...q_{i}.$

111. As such, the prime factorization of $m$ is unique.

112. This property is called the fundamental theorem of arithmetic.

113. There is a function defined on positive integers called the *small omega* function $\omega.$

114. The small omega, $\omega(n)$, counts the number of *unique* prime numbers which divide $n.$

115. Higher powers of a number introduce no new unique prime factors, so for all positive integers $k$, $\omega(n)=\omega(n^k).$

116. There is a function defined on positive integers called the *big omega* function $\Omega.$

117. The big omega, $\Omega(n)$, counts the number of prime numbers which divide $n$, including their multiples.

118. Another way of putting it is that $\Omega(n)$ counts the sum of all powers to which the prime factors of $n$ are taken.

119. That is, $\Omega(n^k)=k\Omega(n).$

120. The small omega function is an *additive* function.

121. An additive function is a function $f$ of a positive integer such that if some numbers $a$ and $b$ are relatively prime, then $f(ab) = f(a) + f(b).$

122. The big omega function is a *completely additive* function.

123. A completely additive function is a function $f$ for which the property $f(ab) = f(a) + f(b)$ holds for *all* positive integers $a$ and $b.$

124. A *square-free* number is a positive integer such that no prime in its factorization is raised to a power higher than $1.$

125. $1$ is square-free, because there are no primes in its factorization.

126. Every prime number is square-free.

127. If a composite number $ab$ is square-free, then $a \bot b.$

128. However, if $a \bot b$, it is not necessarily the case that $ab$ is square-free, as $a$ and/or $b$ could themselves contain higher powers of primes in their factorizations.

129. Given a set $S$, a $k$-combination of elements of $S$ is a subset of $S$ with $k$ elements.

130. The products of numbers $a$ and $b$ which are relatively prime to one another have nicer combinatorial properties around the sets of divisors of $a$ and $b$ as opposed to products of numbers which are not relatively prime.

131. For example, suppose $x = ab$ and $y = cd$ for some prime numbers $a$, $b$, $c$, and $d.$

132. Then, $xy = abcd$, and as such, the divisors of $xy$ are exactly the $16$ products of $k$-combinations of its prime factors $a$, $b$, $c$, and $d$, where $1$ is the product of a $0$-combination.

133. Since the set of all $k$-combinations of the elements of a set $S$ is effectively the power set of $S$, if $S$ has $n$ elements, then there are $2^n$ $k$-combinations of elements of $S.$

134. If a number $a$ has $n$ prime factors and a number $b$ has $m$ prime factors, and $a$ is relatively prime to $b$, then $ab$ has $n + m$ prime factors.

135. This is a restatement of the additivity of the small omega function.

136. Suppose that $n = ab$ and $m = ac$ for some prime numbers $a$, $b$, and $c.$

137. Then, $nm = a^2bc$, i.e. $\omega(n) = 2$ and $\omega(m) = 2$, but $\omega(nm) = 3$: this is an example of how the additive function property fails to hold for numbers which are not relatively prime.

138. As such, the divisors of $nm$ are not exactly the products of the $k$-combinations of its prime factors $a$, $b$, and $c.$

139. Moreover, while e.g. $\Omega(abc) = \Omega(a^2b) = 3$, the latter has fewer divisors than the former.

140. Starting from $ab$, we have the divisors $1$, $a$, $b$, and $ab.$

141. Multiplying $c$ by $ab$, we gain $c$, $ac$, $bc$, and $abc$ as new divisors.

142. However, multiplying $a$ by $ab$, we only gain $a^2$ and $a^2b$ as new divisors.

143. The set of divisors of a square-free number $n$ has the same structure as the power set of the prime factors of $n.$

144. If a number $n$ is *not* square-free, then the set of divisors of $n$ lacks this correspondence to the power set of its prime factors.

## Exercises

1. The least common multiple of two integers $a$ and $b$ is the smallest positive integer $c$ such that $a \mid c$ and $b \mid c.$ It can be expressed as a ratio in terms of $a$, $b$, and $\gcd(a, b).$ Find and justify the expression for this ratio. Hint: since $\text{lcm}(a, b)$ is always positive, it would not be insensible to consider the absolute value function's involvement.

2. The Fibonacci sequence is defined by a recurrence relation where $F_0 = 0$, $F_1 = 1$, and $F_n = F_{n-1} + F_{n-2}$ for $n > 1.$ Show that for $n > 5$, finding $\gcd(F_n, F_{n-1})$ via Euclid's algorithm takes $n - 2$ steps.

3. Given the expression of Bézout's identity, $ax + by = \gcd(a, b)$, the integers $x$ and $y$ are not unique, and are in fact infinite in legion. During the computation of $\gcd(a, b)$ via Euclid's algorithm, the quotient is at each step thrown away while the remainder is carried along to its destination. Using these forlorn quotients, derive an "*extended Euclidean algorithm*," which, given two integers $a$ and $b$, computes not only $\gcd(a, b)$, but also some pair of integers $x$ and $y$ such that $ax + by = \gcd(a, b).$

4. If $p^k$ is a prime power, i.e. $p$ is a prime number and $k$ is a positive integer, how many divisors does $p^k$ have?

5. Show that if a prime number $p$ is greater than $3$, then it is the case that either $p = 6k + 1$ or $p = 6k - 1$ for some positive integer $k.$

6. Demonstrate that, if $k$ is a fixed integer, then $f(n) = k^{\omega(n)}$ has the property that, for relatively prime $n$, $m$, $f(nm) = f(n)f(m).$
