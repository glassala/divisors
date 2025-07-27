# Integer divisibility

*"Number" by itself is always to be taken as meaning "natural number" or "nonzero natural number" when it doesn't make sense for zero to be part of the conversation.*

## 1.

*Elementary properties of integer divisibility.*

1. A nonzero integer $m$ *divides* an integer $n$ if there exists an integer $k$ such that $n = mk.$

2. A number which divides $n$ is called a *divisor* of $n.$

3. The symbol to denote that $n$ divides $m$ is $n \mid m.$

4. If $k$ is nonzero, then $k$ also divides $n.$

5. Division by $0$ is undefined.

6. Every nonzero integer divides $0$: for every integer $n$, $0 = 0n.$

7. If $n$ divides $m$, $-n$ also divides $m.$

8. That is, if $n = mk$, then $n = (-m)(-k).$

9. For this reason, "divisors" is universally shorthand for "positive divisors."

10. $1$ divides every integer, and $1$ uniquely has only $1$ divisor.

11. Every non-zero integer divides itself.

12. If $n$ divides $m$ *and* $m$ divides $n$, then $|m| = |n|.$

13. For integers $a$, $b$, $c$, if $a \mid b$ and $b \mid c$, then $a \mid c.$

14. Consider that if $a \mid b$, then there exists an integer $x$ such that $b = ax$, and if $b \mid c$, then there exists an integer $y$ such that $c = by.$

15. We can write $c = axy$, so $a$ must divide $c.$

16. This is to say, the divisibility relation is reflexive, antisymmetric, and transitive.

17. If $n$ divides $m$, then $|n| \le |m|.$

18. A proper divisor of a number $n$ is a divisor of $n$ which is not itself $n.$

19. If a number $d$ divides $n$, then the set of divisors of $d$ is a subset of the set of divisors of $n.$

20. If $d$ is a proper divisor of $n$, then the set of divisors of $d$ is a proper subset of the divisors of $n.$

21. A proper divisor of a natural number $n$ has strictly fewer divisors than $n.$

22. A characterization of a *prime number* $p$ is that the only proper divisor of $p$ is $1.$

23. If a positive integer $p > 1$ has exactly $2$ divisors, then its divisors are exactly $1$ and $p.$

24. A positive integer with exactly $2$ divisors is called a prime number.

25. A positive integer with more than 2 divisors is called a composite number.

26. $1$ is neither prime nor composite.

27. If a number is divisible by $2$, it is called an *even* number.

28. $0$ is even, but neither prime nor composite.

29. $2$ is the unique even prime number.

30. Any even number $n > 2$ has to have at least $3$ divisors: $1$, $2$, and $n.$

31. If a number is not divisible by $2$, it is called an *odd* number.

32. A perfect square is a positive integer $n$ such that there exists an integer $k$ such that $n = k^2.$

33. If a number has an odd amount of divisors, it must be a perfect square.

34. This is because divisors come in pairs.

35. Consider the meaning of a divisor of a positive integer, i.e. $(\exists{k \in \mathbb{Z}^+} : m = nk)\implies(n \mid m \land k \mid m).$

36. That is, if $n$ divides $m$, there exists some $k$ which divides $m.$

37. So, it is only if $n = k$ that $n$ dividing $m$ does not entail that a *separate* $k$ also divides $m.$

38. The notation for if a number $n$ *doesn't* divide another number $m$is $n \nmid m.$

## 2. 

*Euclidean division and the greatest common divisor. Euclid's algorithm and Bézout's identity.*

1. Suppose one wants to find the *remainder* $r$ of the number $a$ when divided by $b.$

2. If $b$ divides $a$, then $r = 0$, and there exists some unique *quotient* $q$ such that $a = bq.$

3. If $b$ doesn't divide $a$, then there exists some unique quotient $q$ such that $bq < a < b(q+1).$

4. So, there must exist some unique $r$ such that $b > r > 0$ and $a = bq + r.$

5. This is called the lemma of Euclidean division.

6. The remainder $r$ of $a$ when divided by $b$ is also read as $a$ modulo $b.$

7. In symbols, we can write this $r = a \bmod b.$

8. Two integers $a$ and $b$ always have a *greatest common divisor*.

9. The greatest common divisor of $a$ and $b$ is the largest integer which divides both $a$ and $b.$

10. The greatest common divisor of two integers is always a non-negative integer.

11. The greatest common divisor of an integer $n$ and $0$ is always the absolute value of $n.$

12. Although $0$ divides no integer, $\gcd(0, 0)= 0$ by convention.

13. If $a > b$, then $\gcd(a, b) = \gcd(b, a \bmod b).$

14. Consider that we can rewrite the expression in the division lemma into $r = a - bq.$ Since $bq$ is an integer multiple of $b$, $d \mid bq.$ Since $a$ and $bq$ must be integer multiples of $d$, $d$ must divide $a - bq.$

15. That is, there must exist integers $x$ and $y$ such that $a = dx$ and $b = dy$, and so we can rewrite the division lemma into $r = dx - dyq$ and again into $r = d(x - yq).$

16. So far we have proved that the GCD of $a$ and $b$ divides $r$, but we have not proved that it is the maximal number which divides $r.$

17. Suppose $d' = \gcd(b, r).$ Then, by the same logic applied to $d = \gcd(a, b),$ $d' \mid a.$

18. Since $d'$ divides both $a$ and $b$, it has to be less than or equal to $d = \gcd(a, b).$ Since $d$ divides both $b$ and $r$, it has to be less than or equal to $d' = \gcd(b, r)$, and so, $d = d'.$

19. The properties $\gcd(n, 0) = n$ and $\gcd(a, b) = \gcd(b, a \bmod b)$ provide a base case and a recursive step respectively for an algorithm which computes the greatest common divisor of two numbers.

20. This algorithm is called Euclid's algorithm.

21. Euclid's algorithm always terminates, because $a \bmod b$ is always strictly less than $b.$

22. We can write its steps as a sequence of modified division lemmas: $a = bq_1 + r_1$ -> $b = r_1q_2 + r_2$ -> $r_1 = r_2q_3 + r_3.$.. where, if $r_n = 0$, then the product with $q_n$ (i.e. $r_{n-1}$) is the GCD of $a$ and $b.$

23. Closed form expressions emerge: $r_{n-3} = r_{n-2}q_{n-1} + r_{n-1}$ -> $r_{n-1} = r_{n-3} - r_{n-2}q_{n-1}.$

24. Since $r_n = 0$, $r_{n-1} = \gcd(a, b).$

25. For any integers $a$, $b$, there exist integers $x$ and $y$ such that $ax + by = \gcd(a, b).$

26. This property is called Bézout's identity.

27. We can rewrite $\gcd(a, b) = r_{n-3} - r_{n-2}q_{n-1}.$

28. We can then substitute back until we can express the GCD purely as the multiples of $a$ and $b.$

29. To illustrate, note that $r_1 = a - bq_1$, so we can rewrite $a = bq_1 + r_1$ -> $a = bq_1 + (a - bq_1)$ and $b = r_1q_2 + r_2$ -> $b = (a - bq_1)q_2 + r_2.$

30. Since $r_2 = b - (a - bq_1)q_2$, we can rewrite $b = (a - bq_1)q_2 + r_2$ -> $b = (a - bq_1)q_2 + (b - (a - bq_1)q_2)$, and so on.

31. It is clear that any remainder taken through this process can be expressed as a sum of multiples of $a$ and $b.$

## 3.

*Factorial function and Euclid's theorem.*

1. There is a function of a natural number called the *factorial* function.

2. The factorial of a number $n$ is denoted $n!$ and characterized by a recursive formula: the base case is that $0! = 1$, and the recursive step is that $n! = (n-1)!n.$

3. In practice, for any positive integer $n$, $n!$ is the product of every positive integer less than or equal to $n.$

4. As a consequence of this, for all positive integers $k \le n$, $k$ divides $n!.$

5. There are infinitely many prime numbers.

6. This is called Euclid's theorem.

7. Since $a > b \implies \gcd(a, b) = \gcd(b, a \pmod{b})$, for any number $n$, the only divisor common to $n$ and $n+1$ is $1.$

8. Suppose there is a largest prime number $p.$

9. Then, $p!$ is divisible by every prime number.

10. However, this would imply that $p! + 1$ is divisible by *no* prime number, which cannot be the case.

11. As such, for every largest prime number, a larger prime exists.

## 4.

*Relative primality and Euler's phi function. Euclid's lemma and the fundamental theorem of arithmetic.*

1. If two numbers $a$ and $b$ have a GCD of $1$, then $a$ and $b$ are called *relatively prime* to one another. A way to denote that $a$ and $b$ are relatively prime is $a \bot b.$

2. A way to characterize a prime number $n$ is as a number which is relatively prime to every positive integer less than $n.$

3. There is a function defined on positive integers called *Euler's phi function*.

4. For a number $n$, $\varphi(n)$ counts the number of positive integers less than *or equal to* $n$ which are relatively prime to $n.$

5. $1$ is the unique number which is relatively prime to itself, because $\gcd(n, n) = n.$

6. This means that $1$ is the unique value for $n$ such that $\varphi(n) = n.$

7. It is the case that $p$ is a prime number if and only if $\varphi(p) = p - 1.$

8. For $\varphi(p) = p - 1$ to not be the case, then there would have to be a number less than $p$ but greater than $1$ which divides $p.$

9. If a prime number $p$ divides a composite number $ab$, then $p$ divides at least either $a$ or $b.$

10. If $p$ does not divide $a$, then, because $1$ is the only other divisor of $p$, $\gcd(p, a)=1.$

11. So, there must exist integers $x$ and $y$ such that $px + ay = 1.$

12. Suppose we multiply this expression by $b$: $pbx + aby = b.$

13. We know that $p \mid ab$, so we can see that $p$ can be factored out of the left side, and so $p \mid b.$

14. This property is called Euclid's lemma.

15. Every natural number which is greater than $1$ has a unique representation as a product of the powers of prime numbers.

16. The *prime factorization* of a number $n$ is the unique representation of $n$ as a product of powers of prime numbers.

17. If $n$ is prime, then that product is exactly $n.$

18. Since $2$ has a prime factorization, assume every number $2 < n \le k$ for some number $k$ has a prime factorization.

19. If $k + 1$ is prime, then $k + 1$ is its factorization.

20. If $k + 1$ is composite, then there exist numbers $a$, $b$ which are greater than $1$ and less than $k+1$ such that $k+1 = ab.$

21. Since $a$ and $b$ have prime factorizations, $k+1$ must have one as well.

22. Suppose a number $m$ has multiple prime factorizations.

23. Then, there would be products $m = p_{0}p_{1}...p_{j} = q_{0}q_{1}...q_{i}$ for some $i$and $j$, where individual primes in these products are not necessarily unique.

24. By Euclid's lemma, each term of $p_{0}p_{1}...p_{j}$, must divide at least one of $q_{0}q_{1}...q_{i}.$

25. Since the terms of $p_{0}p_{1}...p_{j}$ and $q_{0}q_{1}...q_{i}$ are all prime numbers, however, if one term divides another term, those terms must be equal.

26. So, each term of $p_{0}p_{1}...p_{j}$ corresponds exactly to a term of $q_{0}q_{1}...q_{i}.$

27. As such, the prime factorization of $m$ is unique.

28. This property is called the fundamental theorem of arithmetic.

## 5.

*Small and large omega functions.*

1. There is a function defined on positive integers called the *small omega* function $\omega.$

2. The small omega, $\omega(n)$, counts the number of *unique* prime numbers which divide $n.$

3. Higher powers of a number introduce no new unique prime factors, so for all positive integers $k$, $\omega(n)=\omega(n^k).$

4. There is a function defined on positive integers called the *big omega* function $\Omega.$

5. The big omega, $\Omega(n)$, counts the number of prime numbers which divide $n$, including their multiples.

6. Another way of putting it is that $\Omega(n)$ counts the sum of all powers to which the prime factors of $n$ are taken.

7. That is, $\Omega(n^k)=k\Omega(n).$

8. The small omega function is an *additive* function.

9. An additive function is a function $f$ of a positive integer such that if some numbers $a$ and $b$ are relatively prime, then $f(ab) = f(a) + f(b).$

10. The big omega function is a *completely additive* function.

11. A completely additive function is a function $f$ for which the property $f(ab) = f(a) + f(b)$ holds for *all* positive integers $a$ and $b.$

## 6.

*Square-free numbers.*

1. A *square-free* number is a positive integer such that no prime in its factorization is raised to a power higher than $1.$

2. $1$ is square-free, because there are no primes in its factorization.

3. Every prime number is square-free.

4. If a composite number $ab$ is square-free, then $a \bot b.$

5. However, if $a \bot b$, it is not necessarily the case that $ab$ is square-free, as $a$ and/or $b$ could themselves contain higher powers of primes in their factorizations.

6. Given a set $S$, a $k$-combination of elements of $S$ is a subset of $S$ with $k$ elements.

7. The products of numbers $a$ and $b$ which are relatively prime to one another have nicer combinatorial properties around the sets of divisors of $a$ and $b$ as opposed to products of numbers which are not relatively prime.

8. For example, suppose $x = ab$ and $y = cd$ for some prime numbers $a$, $b,$ $c$, and $d.$

9. Then, $xy = abcd$, and as such, the divisors of $xy$ are exactly the $16$ products of $k$-combinations of its prime factors $a$, $b$, $c$, and $d,$ where $1$ is the product of a $0$-combination.

10. Since the set of all $k$-combinations of the elements of a set $S$ is effectively the power set of $S$, if $S$ has $n$ elements, then there are $2^n$ $k$-combinations of elements of $S.$

11. If a number $a$ has $n$ prime factors and a number $b$ has $m$ prime factors, and $a$ is relatively prime to $b$, then $ab$ has $n + m$ prime factors.

12. This is a restatement of the additivity of the small omega function.

13. Suppose that $n = ab$ and $m = ac$ for some prime numbers $a$, $b$, and $c.$

14. Then, $nm = a^2bc$, i.e. $\omega(n) = 2$ and $\omega(m) = 2$, but $\omega(nm) = 3$: this is an example of how the additive function property fails to hold for numbers which are not relatively prime.

15. As such, the divisors of $nm$ are not exactly the products of the $k$-combinations of its prime factors $a$, $b$, and $c.$

16. Moreover, while e.g. $\Omega(abc) = \Omega(a^2b) = 3$, the latter has fewer divisors than the former.

17. Starting from $ab$, we have the divisors $1$, $a$, $b$, and $ab.$

18. Multiplying $c$ by $ab$, we gain $c$, $ac$, $bc$, and $abc$ as new divisors.

19. However, multiplying $a$ by $ab$, we only gain $a^2$ and $a^2b$ as new divisors.

20. The set of divisors of a square-free number $n$ has the same structure as the power set of the prime factors of $n.$

21. If a number $n$ is *not* square-free, then the set of divisors of $n$ lacks this correspondence to the power set of its prime factors.

## 7.

*Multiplicative functions.*

1. A *multiplicative function* is a function $f$ of a positive integer such that for relatively prime numbers $n$ and $m$, $f(nm)=f(n)f(m)$.

2. If the property $f(nm)=f(n)f(m)$ holds even when $n$ and $m$ are not relatively prime, then $f$ is called *completely multiplicative.*
  
3. There is a family of multiplicative functions $\sigma_{k}$ of a positive integer which are called the *$k$th-power divisor sigma* functions.

4. The $k$th-power divisor sigma function at a number $n$ is the sum of the $k$-th powers of the positive divisors of $n$.

5. In the case where $k=0$, since any number taken to the $0$-th power is $1$, $\sigma_{0}(n)$ is often called the *divisor-counting function*, and it is also denoted $\tau(n)$.

6. To account for the multiplicativity of these functions, we can look at the correspondence between products of numbers $n$, $m$ and the Cartesian products of their divisor sets $D_n$, $D_m$.

7. For example, suppose $n = ab$ and $m = xy$, so $D_n = \set{1, a, b, ab}$ and $D_m = \set{1, x, y, xy}$, where $n$ and $m$ are relatively prime.

8. Consider the set of products of all pairs in $D_n \times D_m$; this set is exactly the set $D_{nm}$:

| $D_{nm}$ | $1$ | $x$ | $y$ | $xy$ |

| -------- | ---- | ----- | ----- | ------ |

| $1$ | $1$ | $x$ | $y$ | $xy$ |

| $a$ | $a$ | $ax$ | $ay$ | $axy$ |

| $b$ | $b$ | $bx$ | $by$ | $bxy$ |

| $ab$ | $ab$ | $abx$ | $aby$ | $abxy$ |

9. Since every divisor except $1$ is unique to $m$ or $n$, there are exactly as many unique products in $D_{nm}$ as there are pairs in $D_n \times D_m$.

10. Suppose, however, instead, that $n = ab$ and $m = ax$:

| $D_{nm}$ | $1$ | $a$ | $x$ | $ax$ |

| -------- | ---- | ------ | ----- | ------- |

| $1$ | $1$ | $a$ | $x$ | $ax$ |

| $a$ | $a$ | $a^2$ | $ax$ | $a^2x$ |

| $b$ | $b$ | $ab$ | $bx$ | $abx$ |

| $ab$ | $ab$ | $a^2b$ | $abx$ | $a^2bx$ |

11. Since multiplication is commutative, unique pairs in $D_n \times D_m$ in the form $(p, q)$ and $(q, p)$ both map to the product $pq$ in $D_{nm}$.

12. This leads one to the conclusion that it is only if $n$ and $m$ are relatively prime that $|D_{nm}| = |D_n||D_m| = |D_n \times D_m|$.

13. This means that $\tau$ is multiplicative.

14. A similar principle underlies why $\sigma_1$, or the sum of divisors function (also denoted simply $\sigma$) is multiplicative.

15. Suppose $n = ab$ and $m = xy$ for primes $a$, $b$, $x$, $y$. Then, $\sigma(n)=1+a+b+ab$ and $\sigma(m) = 1 + x + y + xy$.

16. From the first table, one can independently verify that the sum of divisors of $nm$ is exactly the FOIL expansion of $(1+a+b+ab)(1+x+y+xy)$.

17. However, from the second table and its duplicate divisors, one can see that there will be terms like $2a$, $2ab$, $2ax$, and $2abx$ which cannot be present in $\sigma(nm)$.

18. Suppose $n$ is prime. Then $\sigma(n)=n + 1$.

19. It follows that $\sigma(n)^2 = n^2 + 2n + 1$, but $\sigma(n^2) = n^2 + n + 1$.

20. So, if $n$ and $m$ are not relatively prime, then $\sigma(n)\sigma(m)$ must be greater than $\sigma(nm)$, as each shared divisor is "overcounted" in the former.

21. If $f$ is a multiplicative but not a completely multiplicative function, then it is usually the case that $f$ is sensitive to the "overcounting" of divisors which occurs in $f(n)f(m)$ but not in $f(nm)$.

22. There is a function of a positive integer $n$ denoted $1(n)$, which always evaluates to $1$ for any $n$.

23. This function is trivially completely multiplicative.

24. There is a function of a positive integer $n$ denoted $\varepsilon(n)$ which evaluates to $1$ exactly when $n=1$ and which evaluates to $0$ otherwise.

25. This function is also trivially completely multiplicative.

26. The identity function $\text{Id}(n)$ of a positive integer $n$ is completely multiplicative.

27. On account of the property $a^{n}a^{m}=a^{n+m}$, a constant taken to the power of an additive function is a multiplicative function.

## 8.

*Liouville function and Kronecker delta. Möbius function.*


1. The Liouville function is a function of a positive integer $n$ defined as $\lambda(n)=(-1)^{\Omega(n)}$.

2. The Liouville function indicates via sign whether $n$ is the product of evenly or oddly many prime numbers.

3. It is a constant raised to the power of a completely additive function, so it is completely multiplicative.

4. There is a function of two variables from any set whose members $n$, $m$ admit an idea of equality called the *Kronecker delta* $\delta_{nm}$.

5. The Kronecker delta $\delta_{nm}$ is $1$ if $n = m$ and $0$ if $n\neq m$.

6. The Kronecker delta helps in the definition of a function called the *Möbius function* $\mu$.

7. $\mu(n)$ evaluates to $1$ if $n$ is square-free and has evenly many prime factors.

8. $\mu(n)$ evaluates to $0$ if $n$ is not square-free.

9. $\mu(n)$ evaluates to $-1$ if $n$ is square-free and has oddly many prime factors.

10. A way to state that a number $n$ is square-free is that $\omega(n)=\Omega(n).$

11. It follows, then, that we can write the Möbius function as $\mu(n)=\delta_{\omega(n)\Omega(n)}\lambda(n)$, or, to emphasize that $\mu$ is multiplicative but *not* completely multiplicative, as $\mu(n)=\delta_{\omega(n)\Omega(n)}(-1)^{\omega(n)}$.

12. Consider that for $n$ and $m$ which are square-free but not relatively prime, then $nm$ has at least one squared prime factor, i.e. $|\mu(n)\mu(m)| = 1$ but $\mu(nm)=0$.

## 9.

*Dirichlet convolution.*


1. There is an operation of two functions of a positive integer $f$ and $g$ which yields a new function of a positive integer called the *Dirichlet convolution* of $f$ and $g$, denoted $f * g$.

2. The Dirichlet convolution $f * g$ at $n$ is the sum $(f*g)(n)=\sum_{d\mid{n}}f(d)g(\frac{n}{d})$, where $\sum_{d\mid{n}}$ is a sum indexed by the divisors of $n$.

3. The Dirichlet convolution of two multiplicative functions is always multiplicative. However, the convolution of two completely multiplicative functions is *not necessarily* completely multiplicative.

4. Suppose $f$, $g$ are multiplicative functions and $n$, $m$ are relatively prime positive integers.

5. Since $\gcd(n, m) = 1$, every divisor $d$ of the product $nm$ can be written as $d = xy$ where $x \mid n$ and $y \mid m$.

6. So, we can write $(f * g)(nm) = \sum_{x \mid n \land y \mid m}f(xy)g(\frac{nm}{xy})$.

7. Since $f$ and $g$ are multiplicative, we can rewrite the above as $(f * g)(nm) = \sum_{x \mid n \land y \mid m}f(x)f(y)g(\frac{n}{x})g(\frac{m}{y})$.

8. We can reorganize this sum into $\sum_{x \mid n}f(x)g(\frac{n}{x}) \sum_{y \mid m}f(y)g(\frac{m}{y})$, which is exactly $(f*g)(n)(f*g)(m)$, meaning $(f*g)$ is multiplicative.

9. This means that the set of multiplicative functions is closed under Dirichlet convolution.

10. Dirichlet convolution is commutative.

11. This is because, by the nature of sets of divisors, the sum always counts both $f(d)g(\frac{n}{d})$ and $f(\frac{n}{d})g(d)$.

12. Dirichlet convolution is associative.

13. Consider that an alternative way of writing $(f*g)(n)$ is as $\sum_{xy = n}f(x)g(y)$.

14. Then, we can write $(f * (g * h))(n) = \sum_{xw = n}f(x)\sum_{yz = w}g(y)h(z)$.

15. This can be rearranged into $\sum_{xw = n}\sum_{yz = w}f(x)g(y)h(z)$.

16. Similarly, we can directly write $((f * g) * h)(n) = \sum_{xw = n}\sum_{yz = w}f(x)g(y)h(z)$.

17. Dirichlet convolution is what motivates certain completely multiplicative functions like $1(n)$, the function which always evaluates to $1$, and $\varepsilon(n)$, the function which is only $1$ if $n = 1$, and $0$ otherwise.

18. Convolution by $\varepsilon$ is the identity convolution: $(f*\varepsilon)(n)=f(n)$.

19. This is because in the summation operation, for some positive integer $n$, if $d$ is $1$, then $(\frac{n}{d}) = n$, and likewise if $(\frac{n}{d}) = 1$, then $d = n$, i.e. the only term in the sum not canceled out by being a product with $0$.

20. Convolution by $1$ is a special case, in that $(f*1)(n)=\sum_{d\mid{n}}f(d)$.

21. For example, $\mu * 1 = \varepsilon$.

22. Any positive integer $n$ has a *square-free radical* $\text{rad}(n)$.

23. If $n$ is square-free, then $\text{rad}(n) = n$.

24. If $n$ is not square-free, then $\text{rad}(n)$ is the number $r$ which has exactly the same unique prime factors as $n$, but with no duplicates, i.e. $\omega(r) = \Omega(r)$.

25. Consider that for a square-free integer, its divisors correspond exactly to the $k$-combinations of its prime factors.

## 10.

*Binomial theorem.*

1. The binomial theorem is a statement about expressions of the form: $(x + y)^n$: $(x + y)^n = \sum^{n}_{k=0}\binom{n}{k}x^{k}y^{n-k};\binom{n}{k} = \frac{n!}{k!(n - k)!}$

2. $\binom{n}{k}$ is called a *binomial coefficient,* and is read out as "$n$ choose $k$."

3. The binomial coefficient $\binom{n}{k}$ represents the number of unique $k$-element subsets (or $k$-*combinations*) in an $n$-element set.

4. So, if $n$ is a square-free integer and $k$ is a non-negative integer less than or equal to $\omega(n)$, then $n$ has $\binom{\omega(n)}{k}$ divisors $d$ for which $\omega(d) = k$.

5. It follows that $\sum_{d\mid{n}}\mu(d) = \sum_{d\mid{n}}(-1)^{\omega(d)} = \sum_{k=0}^{\omega(n)}\binom{\omega(n)}{k}(-1)^{k}$.

6. If we consider the structure of the binomial theorem's statement, the sum $\sum_{k=0}^{\omega(n)}\binom{\omega(n)}{k}(-1)^{k}$ emerges from the binomial $(1+(-1))^{\omega(n)}$, which can be restated as $0^{\omega(n)}$.

7. This is $0$ for all square-free integers $n > 1$.

8. For the case where $n = 1$, note that, by combinatorial convention, $0^0 = 1$.

9. Since $1$ is the unique positive integer with no prime factors, $1$is the unique $n$ for which $\omega(n) = 0$.

10. As such, $\sum_{d\mid{n}}\mu(d) = 0$ for all square-free integers $n > 1$ and $\sum_{d\mid{n}}\mu(d) = 1$ exactly in the case where $n=1$.

11. If $n$ is not square-free, then $n$ still has a square-free radical.

12. Since for non-square-free divisors $d$, $\mu(d) = 0$, and so $\sum_{d\mid{n}}\mu(d) = \sum_{d\mid{\text{rad}(n)}}\mu(d)$.

13. Therefore, $\mu * 1 = \varepsilon$.

14. It also follows from the argument above that $|\mu| * 1 = 2^{\omega}$, since the sum of all binomial coefficients $\binom{n}{k}$ for some positive integer $n$ is $2^n$.

15. That is, instead of the binomial $(1+(-1))^{\omega(n)}$, we get $(1+1)^{\omega(n)} = 2^{\omega(n)} = \sum_{k=0}^{\omega(n)}\binom{\omega(n)}{k}$.

## 11.

*Dirichlet inverses.*

1. Since $\varepsilon$ is the identity element of the set of arithmetic functions under Dirichlet convolution, if for two such functions $f$, $g$, it is the case that $f * g = \varepsilon$, then $f$ and $g$ are called *Dirichlet inverses* of one another.

2. For an arithmetic function $f$ to have a Dirichlet inverse, however, it only has to have the property that $f(1) \neq 0$.

3. This is because there is a recursive formula to construct a Dirichlet inverse for any arithmetic function with that property.

4. The base case is that $f^{-1}(1)=\frac{1}{f(1)}$.

5. The recursive step is that, for $n > 1$, $f^{-1}(n)=-\frac{1}{f(1)}\sum_{d<n\mid n}f(d)f^{-1}(\frac{n}{d})$.

6. For $n = 1$, the problem of finding the Dirichlet inverse of a function $f$ is an equation where $(f^{-1} * f)(1) = \varepsilon(1) = 1$; this is solved by the base case.

7. Otherwise, the problem of finding the Dirichlet inverse of $f$ is an equation where $(f^{-1} * f)(n) = \varepsilon(n) = 0$ for all $n > 1$.

8. Another way of writing this is $\sum_{d \mid n}f(d)f^{-1}(\frac{n}{d}) = 0$.

9. This can be rewritten, remarkably, as $f(1)f^{-1}(n) + \sum_{d < n \mid n}f^{-1}(d)f(\frac{n}{d}) = 0$ -> $f^{-1}(n) = \frac{-1}{f(1)}\sum_{d < n \mid n}f^{-1}(d)f(\frac{n}{d})$. [^1]

10. It is straightforward to define arbitrary arithmetic functions which satisfy the inverse condition.

11. For example, for any non-zero complex number $z$, one can define a function $c_{z}(n) = z$ for all positive integers $n$.

## 12.

*Möbius inversion.*

1. Since $\mu$ is the inverse of $1$, if an arithmetic function $g$ takes the form $g = f * 1$, then $g * \mu = f * 1 * \mu = f * \varepsilon = f$.

2. This is called *Möbius inversion*.

3. Möbius inversion can be thought to "recover" one function from another.

4. The form of Dirichlet convolution itself, which is to say, as a sum over the divisors of a number, makes it clear that $\sigma = \text{Id} * 1$.

5. Then, $1$ can be "recovered" from $\mu * \tau$, and the identity function can be "recovered" from $\sigma * \mu$.

6. Less obvious, perhaps, is that $\varphi * 1 = \text{Id}$, i.e. $\varphi = \text{Id} * \mu$.

7. We can write $(\varphi * 1)(n) = \sum_{d \mid n}\varphi(d) = n$.

8. Since $\varphi$ is multiplicative, its behavior over positive integers is fully determined by its behavior at powers of prime numbers.

9. If we have some $p^k$ for some prime $p$ and positive integer $k$, the divisors of $p^k$ are $\set{1, p, p^2, p^3, ..., p^k}$.

10. For a prime power $p^k$, $\varphi(p^k) = p^{k} - p^{k-1}$.

11. This stems from the fact that the numbers which are not relatively prime to $p$ are exactly the multiples of $p$.

12. Since, for example, $p^2$ is the $p$-th multiple of $p$, then there are exactly $p$ positive integers less than or equal to $p^2$ which are not relatively prime to $p$, and so $\varphi(p^2) = p^2 - p$.

13. Likewise, $p^3$ is the $p^2$-th multiple of $p$, and so on.

14. Therefore, $\sum_{d \mid p^k}\varphi(d) = 1 + (p - 1) + (p^2 - p) + (p^3 - p^2) + ... + (p^{k} - p^{k-1})$.

15. It is apparent that each term is subtracted by the next, leaving only $p^k$, meaning $(\varphi * 1)(n) = n$.

## Exercises

1. Demonstrate that if for some natural numbers $n$ and $k,$ $n! \ge n^k,$ then $m! \ge m^k$ for all $m > n.$

2. Prove that, for all positive integers $n,$ $1(1!) + 2(2!) + {...} + n(n!) = (n + 1)! - 1.$

3. Prove that $\sum_{k=0}^n\binom{n}{k} = 2^n.$

4. The least common multiple of two integers $a$ and $b$ is the smallest positive integer $c$ such that $a \mid c$ and $b \mid c.$ It can be expressed as a ratio in terms of $a$, $b$, and $\gcd(a, b).$ Find and justify the expression for this ratio. Hint: since $\text{lcm}(a, b)$ is always positive, it would not be insensible to consider the absolute value function's involvement.

5. The Fibonacci sequence is defined by a recurrence relation where $F_0 = 0$, $F_1 = 1$, and $F_n = F_{n-1} + F_{n-2}$ for $n > 1.$ Show that for $n > 5$, finding $\gcd(F_n, F_{n-1})$ via Euclid's algorithm takes $n - 2$ steps.

6. Given the expression of Bézout's identity, $ax + by = \gcd(a, b)$, the integers $x$ and $y$ are not unique, and are in fact infinite in legion. During the computation of $\gcd(a, b)$ via Euclid's algorithm, the quotient is at each step thrown away while the remainder is carried along to its destination. Using these forlorn quotients, derive an "*extended Euclidean algorithm*," which, given two integers $a$ and $b$, computes not only $\gcd(a, b)$, but also some pair of integers $x$ and $y$ such that $ax + by = \gcd(a, b).$

7. If $p^k$ is a prime power, i.e. $p$ is a prime number and $k$ is a positive integer, how many divisors does $p^k$ have?

8. Show that if a prime number $p$ is greater than $3$, then it is the case that either $p = 6k + 1$ or $p = 6k - 1$ for some positive integer $k.$

9. Demonstrate that, if $k$ is a fixed integer, then $f(n) = k^{\omega(n)}$ has the property that, for relatively prime $n$, $m$, $f(nm) = f(n)f(m).$