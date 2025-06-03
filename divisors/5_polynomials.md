# Polynomial rings

*Polynomials. Degree of a polynomial. Polynomial addition and multiplication. Factorization of a polynomial. Irreducible elements and associates. Non-principal ideals. Irreducibility and primality. Bézout domains. Euclidean domains. Unique factorization domains. Addition of ideals. Ascending chain condition on principal ideals. Content and primitive part of a polynomial. Gauss' lemmas on primitive and irreducible polynomials. Unique factorization of integer polynomials.*

1. A *monomial* over a (commutative) ring $R$ in *one indeterminate* is  an expression of the form $ax^n$, where $a$ is a fixed *coefficient*  drawn from $R$, $n$ is a fixed non-negative integer, and $x$ is an *indeterminate* or *variable*.
2. A monomial can have any number of indeterminates.
3. If $x$, $y$, $z$  are variables, then $x^2$, $7xy$, and $x^2 y^3 z^5$, for example, are all monomials.
4. The *degree* of a monomial is the sum of the exponents to which its indeterminates are taken.
5. For example, $x^2$ and $7xy$ are both monomials of degree $2$, while $x^2 y^3 z^5$ is a monomial of degree $10$.
6. If $a$ is a non-zero element of $R$, then $a$ is a monomial of degree $0$.
7. That is, $a$ can also be written as $ax^0$ (or $ax^0 y^0$, $ax^0 y^0 z^0$, and so on) and as such is a monomial in any number of indeterminates, all raised to the $0$-th power.
8. A *polynomial* over a ring $R$ is a sum of monomials over $R$.
9. A monomial summand of a polynomial $P$ is called a *term* of $P$.
10. The degree of a polynomial is the degree of its highest-degree term.
11. If the *degree* of a polynomial $P$ is $0$, $P$ is said to be a *constant polynomial.*
12. If the only coefficient in a polynomial is $a = 0$, then $ax^n$ is called the *zero polynomial*.
13. The degree of the zero polynomial is undefined.
14. That is, if $0$ is the coefficient to a monomial, then it could be a monomial in any number of indeterminates raised to arbitrary powers and still always evaluate to $0$.
15. Every monomial is itself a polynomial.
16. A polynomial is conventionally arranged in order from highest-degree term to lowest.
17. Polynomials can be added together to create new polynomials.
18. If $P$ and $Q$ are polynomials, then $P + Q$ is a polynomial consisting of all the terms of $P$ and all the terms of $Q$.
19. If two terms with respective coefficients $a$ and $b$ in a polynomial have the same indeterminates raised to the same power, they can be combined into a single term with the coefficient $a + b$.
20. For polynomials in a single indeterminate, any number of terms with the same degree can be combined into a single term of that degree in this way.
21. That is, $ax^k + bx^k = (a+b)x^k$.
22. It is apparent from this that polynomial addition inherits commutativity, associativity and additive inverses from the ring from which coefficients are drawn, and that the zero polynomial is the additive identity.
23. As such, the set of polynomials in $x$ with coefficients from a commutative ring forms an abelian group under addition.
24. A polynomial $P$ in $x$ of degree $n$ can be written in the form $P = a_n x^n + a_{n-1} x^{n-1} + ... a_{2} x^{2} + a_{1} x + a_0$ for coefficients $\set{a_0, a_1, ... a_n}$.
25. If a non-zero polynomial $P$ has degree $n$, then the coefficient $a_n$ is called the *leading coefficient* of $P$, and the coefficient $a_0$ is called the *constant coefficient* of $P$.
26. If $R$ is a commutative ring, then we will denote the set of all polynomials in $x$, i.e. in one variable, by $R[x]$.
27. Multiplication of one polynomial by another yields a new polynomial.
28. If $P$ and $Q$ are polynomials in $x$ and $P'$ and $Q'$ are their respective sets of terms, there is a set $P' \times Q'$ whose elements are pairs $(p, q)$ where $p$ is a term in $P$ and $q$ is a term in $Q$.
29. If $p$ is a term in the form $ax^n$ and $q$ is a term in the form $bx^k$, then $(p, q)$ corresponds to a term $pq$ in the product of polynomials $PQ$, such that $pq = ax^nbx^k = abx^{n + k}$.
30. $PQ$ is then a polynomial which is the sum of these terms.
31. It follows from definitions and the properties of the ring of coefficients that polynomial multiplication is commutative, associative, and distributive over addition.
32. The polynomial $1$ is the multiplicative identity.
33. As such, if $R$ is a commutative ring, then $R[x]$ is a commutative ring.
34. We call $R[x]$ the *polynomial ring* in $x$ over $R$.
35. There is an idea of *polynomial factorization.*
36. A polynomial like $x^2 - 1$ in $\mathbb{Z}[x]$ can be *factored* into two other polynomials with integer coefficients $(x + 1)(x - 1)$.
37. In a similar vein, a polynomial $3x - 9$ can be factored into a product of elements of $\mathbb{Z}[x]$, namely $(3)(x-3)$.
38. A polynomial like $x^2 - 2$ can be factored into $(x + \sqrt{2})(x - \sqrt{2})$, but this factorization requires the use of coefficients which are irrational numbers.
39. Similarly, the polynomial $x^2 + 1$ factors into $(x + i)(x - i)$, but this factorization requires the use of coefficients which are complex numbers.
40. This is all to say that a non-zero, non-unit polynomial in some ring is *irreducible* in that ring if it is cannot be factored into non-unit polynomials with coefficients in its coefficient ring.
41. So, $x^2 - 2$ and $x^2 + 1$ are irreducible in $\mathbb{Z}[x]$.
42. Irreducibility in a ring does not mean there are no solutions which can be drawn from its coefficient ring, however.
43. For example, $x - 1$ is irreducible in the integers, but it's clear that given the equation $x - 1 = 0$, $x= 1$.
44. Note that $3x - 9$ is reducible in $\mathbb{Z}[x]$ but irreducible in $\mathbb{Q}[x]$ because it factors into $(3)(x - 3)$, and $3$ is a unit in $\mathbb{Q}[x]$ because $(3)(\frac{1}{3}) = 1$.
45. An element $a$ is *associate* to an element $b$ in a ring $R$ if there exists a unit $c$ in $R$ such that $a = bc$.
46. This generalizes the property of integers where $n = (-n)(-1)$.
47. The additive inverse $-n$ is the only associate of an integer $n$.
48. An *irreducible element* of an integral domain $R$ is a non-zero, non-unit element which cannot be written as the product of two non-units.
49. That is, a non-zero, non-unit $a \in R$ is irreducible if, given $a = bc$ for any $b, c \in R$, either $b$ or $c$ is a unit.
50. So, an irreducible element $a$ can only be written as the product of an associate of $a$ and a unit.
51. It follows that the irreducible elements of $\mathbb{Z}$ are exactly the prime numbers and their additive inverses.
52. Likewise, the irreducible elements of a polynomial ring are its irreducible polynomials and their associates.
54. $\mathbb{Z}[x]$ is an integral domain, but it does not inherit from $\mathbb{Z}$ the property of every one of its ideals being principal.
55. In $\mathbb{Z}[x]$, one can define an ideal $I = (a_0, a_{1}x, a_{2}x^2, ..., a_{n}x^{n})$ which is the set of all "$\mathbb{Z}[x]$-linear" combinations of the generators of $I$with "scalar" elements being the polynomials in $\mathbb{Z}[x]$.
56. For example, take the ideal with two generators $(2, x) \in \mathbb{Z}[x]$. If $P, Q$ are polynomials in $\mathbb{Z}[x]$, then the elements of $(2, x)$ are all of the polynomials of the form $(P)(x) + (Q)(2)$.
57. This differs from the principal ideal $(x + 2)$, whose elements are all of the polynomials $(P)(x + 2)$ in $\mathbb{Z}[x]$.
58. $(2, x)$ is a much more expansive set of polynomials than $(x + 2)$.
59. The zero polynomial is in $\mathbb{Z}[x]$, so $(2) \cup (x) \subset (2,x)$.
60. It follows from polynomial multiplication that $(x)$ generates exactly every polynomial in $\mathbb{Z}[x]$ with a constant term of $0$.
61. Similarly, $(2)$ generates exactly every polynomial in $\mathbb{Z}[x]$ with even coefficients.
62. The $\mathbb{Z}[x]$-linear combination property ensures that the relative complement of $(2) \cup (x)$ in $(2,x)$ is the set of polynomials in $\mathbb{Z}[x]$ with an even constant term but with at least one other term with an odd coefficient.
63. A polynomial ring over an integral domain straightforwardly inherits the property of being an integral domain.
64. *In any integral domain, all prime elements are irreducible.*
65. Suppose $(p)$ is a non-zero prime ideal in some integral domain $R$and $p = ab$ for some $a$, $b$ in $R$.
66. By definition of prime ideals, since $ab \in (p)$, either $a \in (p)$ or $b \in (p)$.
67. If we suppose that $a \in P$, then $a = pq$ for some $q \in R$.
68. So, we can write $p = pqb$, meaning $qb = 1$, i.e. $b$ is a unit.
69. As such, $p$ is irreducible.
70. Note that it is not necessarily the case that in any integral domain, all irreducible elements are prime.
71. However, all irreducible elements are prime in any principal ideal domain $R$.
72. First, a generalization of Bézout's identity holds for any principal ideal domain.
73. That is, suppose $(a, b)$ is an ideal in $R$.
74. Then, one can write $(a, b)$ as $\set{ax + by \mid x, y \in R}$.
75. Since every ideal in $R$ is principal, then there must be some ideal $(a, b) = (c) \subseteq R$ where $ax + by = c$.
76. Since $a \in (c)$ and $b \in (c)$, $c$ is a common divisor of $a$ and $b$.
77. Suppose $d$ is some arbitrary common divisor of $a$ and $b$.
78. Then, $a = dn$ and $b = dm$ for some $n, m \in R$.
79. It follows that $c = dnx + dmy = d(nx + my)$.
80. This means that an arbitrary common divisor of $a$ and $b$ must also divide $c$, so $c$ must be their greatest common divisor.
81. An integral domain for which such a generalization of Bézout's identity holds is called a *Bézout domain.*
82. As such, any principal ideal domain is a Bézout domain.
83. In a Bézout domain, any finitely generated ideal is principal.
84. That is, if an ideal $I$ has finitely many generators $I = (a_1, a_2, ..., a_n)$, such that the GCD of those generators is $c$, then by the generalized Bézout's identity, one can write $I = (c)$.
85. In any principal ideal domain, all irreducible elements are prime.
86. Suppose $R$ is a principal ideal domain and there exists some irreducible element $p \in R$ which divides $ab$ for some $a, b \in R$.
87. If $p$ is also prime, then $p \mid ab$ for $a, b \in R$ would imply at least either $p \mid a$ or $p \mid b$.
88. If $p \mid ab$, then there exists some $c \in R$ such that $ab = pc$.
89. Since $R$ is a principal ideal domain, $(p, a)$ can be written as $(d)$ for some greatest common divisor $d \in R$.
90. Then, $d \mid p$ and $d \mid a$.
91. Since $p$ is irreducible and $d$ divides $p$, $d$ must be either an associate of $p$ or a unit.
92. If $d$ is an associate of $p$, then $d \mid a \implies p \mid a$.
93. If $d$ is a unit, then $(p, a) = (d) = R$, i.e. $1 \in (p, a)$.
94. So, one can write $ax + py = 1$.
95. Since $(p, a) = R$, $b \in (p, a)$, and one can write $abx + pby = b$.
96. Remember that $ab = pc$, so we can rewrite to $pcx + pby = b$ and again to $p(cx + by) = b$, from which it is clear that $p \mid b$, and so $p$ must be prime.
97. *In a principal ideal domain, an element is irreducible if and only if it is prime.*
98. Much like rings beyond the integers may have a version of Bézout's identity, rings beyond the integers may also have a notion of Euclidean division.
99. An integral domain $R$ which has such a notion is called a *Euclidean domain*.
100. The condition for $R$ to be a Euclidean domain is that one can define some *Euclidean function* $f : R \setminus \set{0} \to \mathbb{N}$ on elements of $R$.
101. A Euclidean function on a ring need not be the *unique* Euclidean function which can be defined on that ring.
102. A Euclidean function satisfies a certain property: for any $a$ and nonzero $b$ in $R$, there exist $q$ and $r$ in $R$ such that $a = bq + r$ and either $r = 0$ or $f(r) < f(b)$.
103. It follows from Euclid's division lemma that $\mathbb{Z}$ is a Euclidean domain, because one can define $f(n) = |n|$.
104. It follows from the properties of fields that any field $K$ is a Euclidean domain where $r = 0$ is always satisfied, and so any function defined $f : K \setminus \set{0} \to \mathbb{N}$ is a valid Euclidean function.
105. That is, given some $a$ and nonzero $b$ from a field $K$, there is always some $q \in K$ such that $a = bq$.  
106. On account of all nonzero elements in a field being units, one can set $q = ab^{-1}$ -> $a = bab^{-1}$ -> $a = a$.
107. Any polynomial ring whose coefficients come from a field is a Euclidean domain.
108. One can define the Euclidean function of a polynomial as $f(P) = \text{deg}(P)$.
109. Suppose $A$ and $B$ are polynomials with coefficients from some field $K$.
110. For $\text{deg}(A) < \text{deg}(B)$, we can set $q = 0$ and $r = A$, and then one is left with $A = A$.
111. For $\text{deg}(A) \ge \text{deg}(B)$, we can perform induction on $A$.
112. If $\text{deg}(A) = 0$, then $\text{deg}(B) = 0$.
113. Since $K$ is a field and $B$ is constant, $B^{-1} \in K$, and so we can set $r = 0$ and $q = AB^{-1}$, leading to $A = qB = BAB^{-1}$, i.e. $A = A$.
114. Assume there exist polynomials $Q$, $R$ such that $A = BQ + R$ for all polynomials $A$, $B$, where $\text{deg}(B) \le \text{deg}(A) < n$ for an arbitrary natural number $n$.
115. Suppose $\text{deg}(A) = n$ and $\text{deg}(B)= k \le n$.
116. We can write $A = a_{n}x^{n} + A'$ and $B = b_{k}x^{k} + B'$ where $A'$ and $B'$ are polynomials of lower degree than $A$ and $B$ respectively (where for convenience sake we will say $\text{deg}(0) = -1$), and $a_n$ and $b_k$ are non-zero.
117. We can define a polynomial $Q' = \frac{a_n}{b_k}x^{n-k}$, then take $BQ' = a_{n}x^{n} + B'Q'.$
118. Then, we can write $R' = A - BQ'$, and since the leading term of  $A$ is subtracted out, $\text{deg}(R') < \text{deg}(A)$.
119. Since $\text{deg}(R') < n$, we can apply the inductive hypothesis and write $R' = BQ^* + R$ for polynomials $Q^*$ and $R$ and rewrite $A - BQ' = BQ^{*}+ R$ to $A = B(Q' + Q^*) + R$ and set $Q = Q' + Q^{*},$ leaving us with a statement in the form $A = BQ + R$ where $\text{deg}(R) < \text{deg}(B)$.
120. As such, $K[x]$ is a Euclidean domain.
121. Let $I$ be some arbitrary non-zero ideal of a Euclidean domain $R$.
122. The set $\set{f(n) \mid n \in I \setminus \set{0}}$ is a non-empty subset of the natural numbers and therefore, by the well-ordering principle, has a minimal non-zero element.
123. As such, there is some $b \in I$ such that $f(b) \le f(n)$ for all non-zero elements $n \in I$.
124. Since $I$ is an ideal, $b \in I \implies (b) \subseteq I$.
125. Let $a \in I$. We can write $a = bq + r$, and since $r = a - bq$, $r$ must be in $I$.
126. Because $b$ is an element with minimal Euclidean value, $r$ being non-zero would mean that $f(r)$ is not less than $f(b)$, and so it must be the case that $r = 0$.
127. As such, $a = bq \in I$, i.e. any element of $I$ can be written in the form $bq$ for some $q \in R$, and so since $I$ must be a subset of $(b)$, we can conclude that $(b) = I$, and therefore an arbitrary ideal of $R$ must be a principal ideal.
128. That is, any Euclidean domain must also be a principal ideal domain.
129. So, if $K$ is a field, then $K[x]$ is a principal ideal domain.
130. A *unique factorization domain* is an integral domain for which some generalization of the fundamental theorem of arithmetic holds.
131. That is, given a unique factorization domain $R$, every non-zero, non-unit element of $R$ has a unique representation as a product of irreducible elements.
132. The uniqueness is up to the ordering and *association* of irreducible elements.
133. This is to say that the strict form of the fundamental theorem of arithmetic does not hold when all integers are taken into consideration, because given integers $a$, $b$, $c$, if $a = bc$, then $a = (-b)(-c)$.
134. If one takes the associate of an integer as not meaningfully unique in this sense however, then one has unique factorization in the integers, and $\mathbb{Z}$ is a unique factorization domain.
135. Any field is trivially a unique factorization domain, because every non-zero element of a field is a unit.
136. Any principal ideal domain is also a unique factorization domain.
137. First, rings have a notion of addition of ideals.
138. Suppose $\frak{a}$ and $\frak{b}$ are ideals. Then, $\frak{a} + b = \set{\mathnormal{a} + \mathnormal{b} \mid \mathnormal{a} \in \frak{a} \land \mathnormal {b} \in \frak{b}}$, which is an ideal.
139. Let $c = \gcd(a, b)$. Since a principal ideal domain is a Bézout domain, $(a) + (b) = (c)$.
140. In a principal ideal domain $R$, the sum of any number of ideals is a principal ideal generated by the GCD of those ideals.
141. Since $(a) \subseteq (b) \iff b \mid a$, if $(a) \subseteq (b)$ and $(a) + (b) = (a)$, then $(a) = (b)$.
142. If $b \mid a$, then $(a) \subseteq (b)$ and $\gcd(a, b) = b$, and so $(a) + (b) = (b)$.
143. This means that for any sequence of ideals in the form $(a_1) \subseteq (a_2) \subseteq (a_3) \subseteq{...}$., $\gcd(a_k, a_{k+1}) = a_{k+1} \le \gcd(a_{k-1}, a_{k}) = a_{k}$.
144. So, addition of principal ideals where one includes the other is the union of those principal ideals.
145. That is, if $(a) \subseteq (b)$, then $(a) + (b) = (a) \cup (b)$.
146. Second, there is a property called the *ascending chain condition*.
147. That is, a ring satisfies the ascending chain condition if for any sequence of its ideals indexed such that  $I_1 \subseteq I_{2} \subseteq I_{3} \subseteq{...}$, there is eventually an ideal $I_k$ such that the sequence "stabilizes" in the sense that $I_k = I_{k+1} = I_{k+2} = {...}$
148. It follows from the closure of ideals under addition that if one considers an ascending chain of principal ideals $(a_1) \subseteq (a_2) \subseteq (a_3) \subseteq{...}$., the union of all ideals in such a chain $\bigcup^{\infty}_{i = 1}(a_i)$ is an ideal.
149. Since $R$ is a principal ideal domain, $\bigcup^{\infty}_{i = 1}(a_i) = (r)$ for some  $r \in R$. 
150. Since $(r)$ is a union of ideals, $r$ must appear in some ideal in the union which we will designate $(a_k)$.
151. This implies that $(r) \subseteq (a_k)$, but $(r)$ is the entire union of ideals, and so $(a_k) \subseteq (r)$, meaning $(r) = (a_k)$, indicating that the ascending chain stabilizes at $(a_k)$.
152. A ring whose ideals satisfy the ascending chain condition is said to be *Noetherian.*
153. As such, any principal ideal domain is Noetherian.
154. It follows from satisfying the ascending chain condition that a *strictly* ascending chain in the form $I_1 \subset I_{2} \subset I_{3} \subset{...}$ must contain finitely many ideals.
155. For some *reducible* $a$ in a principal ideal domain $R$, $a$ can be written as $a = a_1 b_1$ and $a_1 = a_2 b_2$, and so on, and so $(a) \subset (a_1) \subset (a_2).$
156. Likewise, for some *irreducible* $p$, if $p = p_1 q_1$ and $(p) \subset (p_1)$, then $p_1$ is a unit and $q_1$ is an associate of $p$.
157. A factorization process can be seen as a "binary tree" whose paths from root to leaf are strictly ascending chains which terminate at $(p) \subset (1)$ for some irreducible $p$.
158. This means that any non-zero, non-unit element has a factorization into irreducibles.
159. Suppose some $a$ in $R$ has a factorization with $n$ irreducible factors.
160. If $n = 0$, then $a$ is a unit. If for some $p, q \in R$, $a = pq$, then $p$ and $q$ must be units, and so the factorization of $a$ is unique.
161. Assume that for $n > 0$, any element $a$ with $n-1$ irreducible factors has a unique factorization.
162. Suppose $a$ has two factorizations into irreducible elements indexed $p_i$ and $q_j$, i.e. $a = p_1 p_2 {...} p_n = q_1 q_2 {...} q_k$ where $n > 0$ and $k \ge n$.
163. Since $R$ is a principal ideal domain, the irreducibles of $R$ are exactly the primes of $R$.
164. Since $p_1$ is prime and divides $a$, the generalized "Euclid's lemma" property which defines prime elements means $p_1$ must divide some factor in $\set{q_1 q_2 {...} q_k}$.
165. Since a unique factorization is only necessarily unique up to ordering and association, we can reorder the factors such that $p_1 \mid q_1$.
166. So, there must exist some $v$ such that $q_1 = p_1v$.
167. However, $p_1$ and $q_1$ are irreducible, so $v$ must be a unit, and therefore $p_1$ is associate to $q_1$.
168. On account of $R$ being an integral domain, the cancellation law that $ab = ac \implies b = c$ for $a \neq 0$ holds, given that freedom from non-trivial zero divisors allows one to write $ab = ac \implies ab - ac = 0 \implies a(b - c) = 0 \implies b - c = 0$.
169. So, since $p_1$ is associate to $q_1$, we can say that $p_2 {...} p_n = q'_2 {...} q_k$ where $q'_2$ is associate to $q_2$ because $q'_2 = vq_2$.
170. The product $p_2 {...} p_n$ has $n-1$ factors and so, by the inductive hypothesis, we can say that $n = k$ and match every $p_i$ to an associate $q_i$, concluding that any non-zero, non-unit in $R$ has a unique factorization into irreducibles.
171. It follows from the above that an integral domain for which any non-zero, non-unit element can be factored into irreducibles and for which the prime elements are exactly the irreducible elements is a unique factorization domain.
172. As such, any principal ideal domain is a unique factorization domain.
173. So, if $K$ is a field, then $K[x]$ is a unique factorization domain.
174. The *content* of a polynomial is the greatest common divisor of its coefficients.
175. A *primitive* polynomial is a polynomial whose content is $1$.
176. The constant polynomials $1$ and $-1$ are both primitive.
177. The *primitive part* of a polynomial $P$ is the quotient of $P$ by its content.
178. It follows that any polynomial can be factored into a product of its content and its primitive part.
179. Note that it is equally valid to factor a polynomial into its associate content and primitive part.
180. For example, given $3x - 9$, one can take an associate content $-3$ and get an associate primitive part $-x + 3$.
181. If $P$ and $Q$ are primitive polynomials in $\mathbb{Z}[x]$, then their product $PQ$ is also primitive.
182. Suppose $PQ$ were not primitive. Then, there would be some prime number $m$ which divides every term of $PQ$.
183. This would imply there is a reduction in $\mathbb{Z}/m\mathbb{Z}[x]$ such that $PQ \equiv 0 \pmod{m}$.
184. However, because $m$ is prime, $\mathbb{Z}/m\mathbb{Z}[x]$ is an integral domain,  which is to say $\mathbb{Z}/m\mathbb{Z}[x]$ has no non-trivial zero divisors.
185. It would follow that at least either $P \equiv 0 \pmod{m}$ or $Q \equiv 0 \pmod{m}$.
186. This means that all of its coefficients are divisible by $m$, which means that $m$ can be factored out of it, contradicting the idea that $P$ and $Q$ are both primitive.
187. This is a version of one of several statements called *Gauss' lemma*, which we will call *Gauss' lemma on primitivity*.
188. In addition, if $PQ$ is primitive but reducible, then both $P$ and $Q$ must be primitive.
189. That is, if the content of $P$ is $k$ and the content of $Q$ is $n$, every term of $PQ$ has a coefficient which is a multiple of $kn$, which means $PQ$ would not be primitive if either $k > 1$ or $n > 1$.
190. An integer polynomial must be primitive in order to be irreducible.
191. However, if a polynomial ring draws its coefficients from a   field, then every non-zero constant polynomial in that ring is a unit.
192. That is, if $K$ is a field, then the condition for a polynomial in $K[x]$ to be irreducible is that it cannot be factored into two *non-constant* polynomials.
193. As such, a polynomial in $K[x]$ does not need to be primitive in order to be irreducible.
194. Any polynomial in $\mathbb{Q}[x]$ corresponds to a polynomial in $\mathbb{Z}[x]$.
195. For example, if $Q = \frac{1}{5}x^2 + \frac{1}{3}x + \frac{1}{2}$, then one can get an integer polynomial by multiplying $Q$ by the least common denominator of its coefficients as follows: $(30)(Q) = 6x^2 + 10x + 15$.
196. This is called *clearing denominators*.
197. $\mathbb{Q}$ is the field of fractions of $\mathbb{Z}$, so any polynomial $Q \in \mathbb{Q}[x]$ can be written $Q = (\frac{a}{b})P$ for some $P \in \mathbb{Z}[x]$ and integers $a$ and $b$.
198. It follows that any rational polynomial $Q = (\frac{a}{b})P$ can be "scaled back" into an integer polynomial $bQ = aP$.
199. If $P$ is primitive and reducible in $\mathbb{Z}[x]$, then it is straightforwardly also reducible in $\mathbb{Q}[x]$, since $\mathbb{Z}[x]$ is a subring of $\mathbb{Q}[x]$.
200. Suppose $P$ is primitive in $\mathbb{Z}[x]$. If $P$ is reducible in $\mathbb{Q}[x]$, then there exist non-constant polynomials $Q_1, Q_2 \in \mathbb{Q}[x]$ such that $P =Q_1 Q_2$.
201. Since $Q_1$ and $Q_2$ can be written in the form $Q_1 = (\frac{a}{n})P_1$ and $Q_2 = (\frac{b}{m})P_2$ for primitive integer polynomials $P_1$ and $P_2$, one can write $P = (\frac{ab}{nm})P_1 P_2$.
202. By virtue of Gauss' lemma on primitivity, $P_1 P_2$ is primitive.
203. Since $P$ is also primitive, $\frac{ab}{nm}$ must be $\pm 1$, so $P$ is reducible in $\mathbb{Z}[x]$.
204. So, if and only if a primitive integer polynomial is reducible in $\mathbb{Q}[x]$, it is reducible in $\mathbb{Z}[x]$.
205. This is a version of a statement called *Gauss' lemma on irreducibility.*
206. In $\mathbb{Q}[x]$, polynomials are guaranteed to have a factorization into irreducible elements and irreducibility is equivalent to primality of an element.
207. Recall that for an integral domain $R$ to satisfy these conditions is for $R$ to be a unique factorization domain.
208. So, suppose the polynomial $P$ is primitive and irreducible in $\mathbb{Z}[x]$.
209. Then, $P$ is irreducible in $\mathbb{Q}[x]$ and therefore prime in $\mathbb{Q}[x]$.
210. Suppose $P$ divides $AB$ for polynomials $A, B \in \mathbb{Z}[x]$.
211. $A$ and $B$ are also in $\mathbb{Q}[x]$, so, since $P$ is prime in $\mathbb{Q}[x]$, at least either $P \mid A$ or $P \mid B$.
212. As such, $P$ is prime in $\mathbb{Z}[x]$.
213. Since $\mathbb{Z}[x]$ is an integral domain, "prime" implies "irreducible," and so the primitive prime polynomials are exactly the primitive irreducible polynomials.
214. An integer polynomial has a unique factorization into a content and primitive part: if two polynomials have the same content *and* the same primitive part, then they are the same polynomial.
215. The content $k$ of a polynomial is an integer, so either $k$ is a unit or $k$ has a unique factorization into associates of prime numbers.
216. The primitive part $P \in \mathbb{Z}[x]$ is a primitive polynomial, and via both forms of Gauss' lemma, primitive polynomials in $\mathbb{Z}[x]$ have a unique factorization into prime primitive polynomials in $\mathbb{Q}[x]$and therefore this unique factorization exists up to cleared denominators and associates in $\mathbb{Z}[x]$.
217. Since the content and primitive part of any non-zero, non-unit integer polynomial each have unique factorizations, we can conclude that $\mathbb{Z}[x]$ is a unique factorization domain.

## Exercises

1. Suppose a polynomial $Q$ has no solution in $\mathbb{Z}[x]$ but has a solution in $\mathbb{Q}[x]$. What is the degree of $Q$?
2. Prove that maximal ideals are always prime ideals in any commutative ring.
3. Let $R$ be a unique factorization domain. Demonstrate that Gauss' lemma for primitivity as described for integer polynomials applies for polynomials in $R[x]$.
4. Let $K = \text{Frac}(R)$ for a unique factorization domain $R$. Show that a non-constant polynomial $P$ in $R[x]$ is irreducible if and only if $P$ is primitive in $R[x]$ *and* irreducible in $K[x]$.
5. An *atomic domain* is an integral domain for which any element can be written as a finite but not necessarily unique product of irreducible elements. Prove that, for elements of any atomic Bézout domain, irreducible $\iff$ prime.
