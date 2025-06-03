# Modular arithmetic

*Basic properties of modular arithmetic. Congruence modulo $m$. Equivalence relations and classes. Quotient sets. Properties of a group. Additive groups modulo $m$. Order of a group. Non-zero zero divisors. Multiplicative groups modulo $m$. Sunzi's theorem. Wilson's theorem. Fermat's little theorem. Cyclic groups. Isomorphisms. Subgroups and cosets. Lagrange's theorem. Order of an element. Euler's theorem.*

1. Modular arithmetic is "wrap-around" arithmetic.
2. Given a positive integer *modulus* $m$, arithmetic operations on numbers "wrap around" at $m$.
3. It is sometimes introduced as "clock arithmetic," because the temporal units which divide a day, half-day, hour, and so on wrap around at $24$, $12$, and $60$ respectively, and so provide natural examples of moduli: if it is $17:00$, waiting for $10$ hours brings one to $3:00$ on the next day, as opposed to some $27:00$.
4. The properties of arithmetic over a modulus $m$ depend on the set of divisors of $m$, so the description "clock arithmetic" has a critical flaw preventing it from being fully faithful to modular arithmetic.
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
25. In practice, a modulus is often framed as taking the arithmetic of a set of infinitely many integers and sending it to a finite set of integers.
26. Addition and subtraction work "normally" over any modulus.
27. A better way of saying this is that addition on $\mathbb{Z}/m\mathbb{Z}$ always forms a *group* of order $m$ for any modulus $m$.
28. A group is a structure comprising a set and an operation which together satisfy certain requirements.
29. Let $S$ be an arbitrary set and $*$ be an arbitrary operation.
30. The first requirement is closure under the operation: $\forall{a, b}\in{S}, a * b\in{S}$.
31. The second is that the operation has an identity: $\exists{e}\in{S}:\forall{a}\in{S},a * e = e * a=a$.
32. The third is that the operation is associative: $\forall{a, b, c}\in{S}, a * (b * c)=(a * b) * c$
33. The fourth (and most restrictive) requirement is that every element in the set has an *inverse* under the operation.
34. That is, $\forall{a}\in S, \exists{a^{-1}} \in S: a * a^{-1}= a^{-1} * a=e$.
35. It follows from the above requirements that the inverse of any element $a$ in a group is unique to $a$.
36. Suppose for some group $G$ with elements $a$, $b$, and $c$ and identity $e$, were to have $b$ and $c$ each be separate inverses of $a$.
37. That is, $a * b = b * a = e$ and $a * c = c * a = e$.
38. We have $(b * a) * c = e * c$, but we also have $b * (a * c) = b * e$, so it follows from the associative property that it must be the case that $b = c$.
39. An *abelian* group is a group whose operation is commutative. That is, $\forall{a, b} \in S, a * b = b * a$.
40. Groups from arithmetic tend to be commutative because e.g. addition and multiplication of individual numbers are both commutative, and our focus is largely on groups formed out of these operations, but there are many ways to achieve a group structure without commutativity.
41. For example, the set of all element rearrangements (or permutations) of a set of $n$ elements forms a group under composition of permutations (called the *symmetric group of degree $n$*), but the composition of permutations is not in general commutative.
42. The *order* of a group is the cardinality of its underlying set, or how many elements are in the group.
43. Addition over $\mathbb{Z}$ is an abelian group. Every positive integer $n$ has a corresponding negative integer $-n$ (and vice versa) which serves as its *additive inverse.*
44. $0$ is its own inverse, because it is the additive identity, and it follows from the definition of an identity of a group that a two-sided identity element is always its own inverse.
45. If a set has elements without inverses w/r/t an operation, but retains closure, associativity, and an identity element, then that set and operation form a *monoid* as opposed to a group.
46. Multiplication over $\mathbb{Z}$ is a monoid and *not* a group, because non-unit integers do not have other integers as multiplicative inverses in the confines of this set.
47. For any modulus $m$, any element $n$ of $\mathbb{Z}/m\mathbb{Z}$ has a corresponding element $k = m - n$ such that $n + k \equiv 0 \pmod m$, so an additive inverse is always present.
48. From the clock perspective, this is expressed in the notion that whatever hour it is, there is always some number of hours one can wait until the day ends.
49. From the clock perspective, the more "highly composite" a modulus $m$ is, i.e. the more divisors it has relative to its size, the better it is for convenient time-keeping.
50. For any modulus $m$, the equivalence class whose representative is $0$ is the set of multiples of $m$.
51. Consider $ab \equiv 0 \pmod{p}$, where $p$ is prime: since the divisors of $p$ are exactly $1$ and $p$, for any product of positive integers $a$ and $b$, given $ab = p$, either $a = p$ and $b = 1$ or $a = 1$ and $b = p$.
52. So, effectively, the only way to get a product of $0$ in a prime modulus is to multiply a number by $0$ or a multiple of $p$.
53. Now, consider a product like $ab \equiv 0 \pmod{12}$: $a$ could be $2$ if $b$ is $6$, or $a$ could be $3$ if $b$ is $4$, and vice versa.
54. This is to say, two numbers, of which neither is in the "0 class" of the modulus, can multiply with each other to get 0.
55. We will denote the *multiplicative* group of a modulus $m$ with $(\mathbb{Z}/m\mathbb{Z})^{\times}$.
56. While the order of $(\mathbb{Z}/m\mathbb{Z})^{+}$ is always $m$, the set underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ has to have at most $m-1$ elements, provided $m > 1$.
57. This is because $1$ is the identity element of multiplication, and there is no way to get a number which is not $0$ from a product with $0$ as a term.
58. That is, $0$ can never have a multiplicative inverse, so it is excluded from the set.
59. The exception to this is the case where $m = 1$, since all of $\mathbb{Z}$ is collapsed into a single equivalence class represented by $0$, and $0$ times $0$ is $0$, meaning $(\mathbb{Z}/1\mathbb{Z})^{\times}$ is actually a group of order $1$.
60. So, if $ab \equiv 0 \pmod{m}$, and neither $a$ nor $b$ is $0$, then $a$ and $b$ would violate the closure condition required of a group.
61. For this reason, the set of representatives underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is the set of positive integers less than or equal to $m$ which are relatively prime to $m$.
62. So, it follows that the order of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is $\varphi(m)$, i.e. $m - 1$ if and only if $m$ is prime.
63. It is often useful to consider the *negative* class representatives of a modulus, for the reason that $-a \equiv m-a \pmod{m}$.
64. $1$ is its own multiplicative inverse for any modulus, and since $(-1)(-1) = 1$, $m - 1$ is also its own multiplicative inverse for any modulus.
65. Bézout's identity guarantees that if an integer $a$ is relatively prime to $m$, then there exist integers $x$ and $y$ such that $ax + my = 1$.
66. It follows, then, that $ax \equiv{1} \pmod{m}$, i.e. $x$ is the multiplicative inverse of $a$ modulo $m$
67. Let $n$ and $m$ be positive integers which are relatively prime to one another. Then, the system of linear congruences $x \equiv a \pmod{n}; x \equiv b \pmod{m}$ has a unique solution modulo $nm$. Since $n$ and $m$ are relatively prime, then by Bézout's identity, there exist integers $x$ and $y$ such that $nx + my = 1$.
68. As such, $nx \equiv 1 \pmod{m}$ but $nx \equiv 0 \pmod{n}$ and $my \equiv 0 \pmod{m}$ but $my \equiv 1 \pmod{n}$.
69. One can conclude that $x = mya + nxb$, since $x \equiv 1a + 0b \equiv a \pmod{n}$ and $x \equiv 0a + 1b \equiv b \pmod{m}$.
70. Since this property holds for a system of two congruences with relatively prime moduli $n$, $m$, it follows that one can find such a unique solution for a system of any number of congruences whose moduli are all mutually (or *pairwise*) relatively prime to one another.
71. That is, if some modulus $k$ is relatively prime to both $n$ and $m$ (where $n \bot m$), then $k \bot{nm}$, and so one can set up the system of linear congruences $x \equiv p \pmod{nm};x \equiv q \pmod{k}$ for some integers $p$ and $q$.
72. That a unique solution exists for such systems over pairwise relatively prime moduli is called *Sunzi's theorem.*
73. There is another way to characterize the prime numbers.
74. A number $p$ is prime if and only if it is the case that $(p - 1)! \equiv -1 \pmod{p}$.
75. Suppose $(n - 1)! \equiv -1 \pmod{n}$ were the case for some composite $n$.
76. A composite number $n$ is divisible by some number $k$ such that $2 \le k < n$.
77. Therefore, since $(n - 1)!$ is divisible by every number less than $n$, $k$ must divide both $n$ and $(n - 1)!$, and so $\gcd((n - 1)!, n)$ must be at least $k$.
78. However, for $(n - 1)! \equiv -1 \pmod{n}$ to be the case, then $\gcd((n - 1)!, n)$ must equal $1$.
79. Note that for $a \equiv -1 \pmod{m}$ to be the case, then there must exist an integer $k$ such that $a = km - 1$, which can be rewritten as $a - km = -1$.
80. If a number divides both $a$ and $km$, then it must divide $a - km$, i.e. $-1$, and so $\gcd(a, km) = 1$.
81. Since $\gcd((n - 1)!, n) \ge k \ge 2$, $(n - 1)! \equiv -1 \pmod{n}$ cannot hold for composite $n$.
82. If $n$ is $1$, then, trivially, $0! \equiv 0 \pmod{1}$.
83. For prime $n$, consider that every element of $(\mathbb{Z}/n\mathbb{Z})^{\times}$ has a multiplicative inverse.
84. Since $(n - 1)!$ is the product of the entire least residue system of modulo $n$ (excepting $0$), $(n - 1)!$ can be arranged into a product of pairs of elements of $(\mathbb{Z}/n\mathbb{Z})^{\times}$ in the form $ab \equiv 1 \pmod{n}$ and $n - 1 \equiv -1 \pmod {n}$.
85. Since it is only for prime $n$ where every positive integer $\le n$ has a multiplicative inverse modulo $n$, it is only for prime $n$ where the product of every positive integer less than $n$ inevitably takes the form $(1)(1)...(-1)$.
86. As such, $(p - 1)! \equiv -1 \pmod{p}$ holds for all prime $p$ and only for prime $p$.
87. The above property is called Wilson's theorem.
88. If $a$ is a natural number and $p$ is a prime number, then $a^p \equiv a \pmod {p}$.
89. The binomial theorem is so nice that it is worth stating twice: $(x + y)^n$: $(x + y)^n = \sum^{n}_{k=0}\binom{n}{k}x^{k}y^{n-k};\binom{n}{k} = \frac{n!}{k!(n - k)!}$
90. $\binom{n}{k}$ is called a *binomial coefficient,* and is read out as "$n$ choose $k$."
91. A binomial coefficient is always an integer: all multiples of primes in the factorization of $k!(n - k)!$ must also be in the factorization of $n!$
92. If $n$ is prime, then $n$ divides $\binom{n}{k}$ for all $0 < k < n$. This is because $n$ always divides $n!$, but since $n$ is prime, it cannot divide $k!(n - k)!$ unless $k = 0$ or $k = n$.
93. As a consequence of this for prime $n$, the only terms of the sum not "zeroed out" by a coefficient which is a multiple of $n$ are $\binom{n}{0}x^{0}y^{p}$ and $\binom{n}{n}x^{p}y^{0}$.
94. This means that if $n$ is prime, then $(x + y)^n \equiv x^n + y^n \pmod{n}$.
95. It holds that $0^p \equiv 0 \pmod {p}$ for a prime $p$.
96. If we assume that for some positive integer $k$, $k^p \equiv k \pmod {p}$ is the case, then we can say that since the freshman's dream comes true for a prime modulus $p$, i.e. $(k + 1)^p \equiv k^p + 1^p \pmod{p}$, it follows that $(k + 1)^p \equiv k + 1 \pmod{p}$.
97. This is exactly our original statement $a^p \equiv a \pmod {p}$, which is called Fermat's little theorem.
98. A *primitive root* modulo $m$ is a number $n$ in $(\mathbb{Z}/m\mathbb{Z})^{\times}$ which *generates* every element of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ through repeated multiplication.
99. That is, if $c$ being an element of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ implies that there exists an integer $k$ such that $c \equiv n^k \pmod{m}$, then $n$ is a primitive root modulo $m$.
100. Only certain moduli have primitive roots: only if $m$ is $1$, $2$, $4$, $p^k$, or $2p^k$, where $p$ is an odd prime and $k$ is a positive integer, then the modulus $m$ has at least one primitive root.
101. If $n$ is a primitive root modulo $m$, then the multiplicative inverse of $n$ is also a primitive root modulo $m$.
102. A group where all of its elements can be generated by repeat iterations of its operation on a single element and that element's inverse is called a *cyclic* group.
103. The integers under addition form the archetypal infinite cyclic group, since any integer can be reached from a sum of terms of $-1$ and $1$.
104. $(\mathbb{Z}/m\mathbb{Z})^{+}$ is the archetypal finite cyclic group, being cyclic for every modulus: the cyclic group of order $m$ is often denoted simply $\mathbb{Z}_m$.
105. For any modulus $m$, one can get all of the elements in $\mathbb{Z}_m$ from repeated addition by 1.
106. All cyclic groups are abelian, but not every abelian group is cyclic.
107. It follows from the definition of a primitive root that a group $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is cyclic if and only if it has a primitive root.
108. A group $A$ is *isomorphic* to a group $B$ if there exists a one-to-one correspondence (i.e. a bijection) between the elements of the set underlying $A$ and the elements of the set underlying $B$ which preserves group structure in both directions.
109. We write that $A$ is isomorphic to $B$ as $A \cong B$.
110. For example, $\mathbb{Z}_{2} \cong (\mathbb{Z}/3\mathbb{Z})^{\times}$.
111. The representatives of the set underlying $\mathbb{Z}_{2}$ are $\set{0, 1}$, while the corresponding representatives for $(\mathbb{Z}/3\mathbb{Z})^{\times}$ are $\set{1, 2}$.
112. In small groups like these, one can verify the isomorphism simply by exhausting all possible operation outcomes: we match $0$ and $1$ in the former to $1$ and $2$ in the latter respectively, and we match addition in the former to multiplication to the latter.
113. We can then take note that $0 + n \equiv n \pmod{2}$ and $1 + 1 \equiv 0 \pmod{2}$, while $(1)n \equiv n \pmod{3}$ and $(2)(2) \equiv 1 \pmod{3}$.
114. Since this covers every way elements can be combined within these groups, it is apparent that their basic structure is the same.
115. Every finite cyclic group of order $n$ is isomorphic to $(\mathbb{Z}/n\mathbb{Z})^{+}$.
116. This property emerges from the fact that because for any cyclic group, having a single generator $g$, one can write all of its elements as the $k$-th multiple of that generator $kg$ (where $-kg$ denotes the $k$-th multiple of the generator's inverse and $0g$ is the identity).
117. If a group $G$ comprises the set $S$ and the operation $*$, then a *subgroup* of $G$ is a group formed from a subset $S' \subseteq S$ under the same operation $*$.
118. Much like it is often convenient to refer to equivalence classes by their representatives, it is convenient to say "elements of a group" to mean the elements of the group's underlying set.
119. Every group is a subgroup of itself.
120. The one-element *trivial group*, which consists of the identity element, is a subgroup of every group.
121. A group can have at minimum $1$ element.
122. Consider that the empty set can never be the underlying set of a group, because a group requires an identity element, and the empty set has no elements.
123. A subgroup $H$ of a group $G$ partitions the underlying set $S$ of $G$ into a set of *left cosets* and a set of *right cosets.*
124. A left coset of $H$ in $G$ is the set $g*H = \set{g * h \mid h \in H}$ for some fixed $g \in G$.
125. A right coset of $H$ in $G$ is the set $H*g = \set{h * g \mid h \in H}$ for some fixed $g \in G$.
126. Left and right cosets can be viewed as equivalence classes formed out of the relations $g \sim h \iff -g * h \in H$ and $g \sim h \iff h * -g \in H$ (for fixed $g \in G$) respectively.
127. A subgroup always induces the same number of left cosets as it does right cosets.
128. Every coset in a partition is *disjoint* to every other coset in the same partition.
129. If $G$ is abelian, then the left coset partition induced by $H$ is itself the same as the right coset partition induced by $H$.
130. The number of cosets induced in the underlying set of a group $G$ by a subgroup $H$ is called the *index of $H$ in $G$* and is denoted $[G:H]$.
131. $H$ induces its own underlying set as both a left and a right coset.
132. That is, if $e$ is the identity of $G$, then it is apparent that $\set{e * h \mid h \in H} = \set{h * e \mid h \in H}$.
133. Moreover, if $H$ is a subgroup of $G$, then $H$ must contain the identity element of $G$.
134. Given that every coset in a partition is disjoint from every other, the set $H'$ which underlies $H$ is the only set in a coset partition induced by $H$ which can underlie a subgroup of $G$, since $H'$ is the sole possessor of the identity of $G$.
135. Every coset induced by a subgroup $H$ has the same number of elements as $H$.
136. For example, if we take the group $\mathbb{Z}_6$, i.e. the additive group of integers modulo $6$, and its set of representatives $\set{0, 1, 2, 3, 4, 5}$, it is apparent that $\set{0, 2, 4}$ and $\set{0, 3}$ each underlie a subgroup of $\mathbb{Z}_6$.
137. Note that, w/r/t addition modulo $6$, $\set{0, 2, 4}$ is cyclic and of order $3$, and as such must be isomorphic to $\mathbb{Z}_3$.
138. The set $\set{0, 3}$, w/r/t addition modulo $6$, is likewise isomorphic to $\mathbb{Z}_2$.
139. $\mathbb{Z}_3$ induces $2$ cosets in $\mathbb{Z}_6$, while $\mathbb{Z}_2$ induces $3$.
140. More generally, if $H$ is a subgroup of a finite group $G$, and $|G|$ denotes the order of a group, then the number of cosets $H$ induces in $G$ is given by $\frac{|G|}{|H|}$.
141. If $H$ is a subgroup of a group of finite order $G$, then the order of $H$ divides the order of $G$.
142. This stems from the very ideas of subgroup and coset: a coset is an effective "translation" of an entire subgroup by an element in the group.
143. Suppose $H$ is a subgroup of the finite group $G$ and $|H|$ doesn't divide $|G|$.
144. It is insensible for the order of a group to not be an integer, so $|H|$ not dividing $|G|$ would imply that $H$ induces a "remainder coset" in either direction which would have fewer elements than $H$.
145. However, every coset induced by $H$ is an image of $H$ under the group operation, meaning two elements would be mapped to the same element by it, making this so-called "translation" non-invertible.
146. That is, for $|H|$ to not divide $|G|$ there would have to be an element in $G$ without a unique inverse, violating the conditions for a set to be a group under an operation, and so the order of $H$ must divide $|G|$.
147. That $|H|$ must divide $|G|$ if $H$ is a subgroup of a finite group $G$ is one of two theorems called *Lagrange's theorem*.
148. The *order of an element* of a group is the order of the cyclic subgroup generated by that element.
149. If $g$ is an element of a group $G = (G', *)$, then $\langle{g}\rangle = (\set{kg \mid k \in \mathbb{Z}\land g \in G'}, *)$ is the cyclic subgroup generated by $g$.
150. If $\langle{g}\rangle$ is finite, its order is given by the smallest integer $k$ such that $kg = e$, where $e$ is the identity of $G$.
151. Positive integers $a$ and $m > 1$ are relatively prime if and only if it is the case that $a^{\varphi(m)} \equiv 1 \pmod{m}$.
152. This follows directly from Lagrange's theorem and the definition of the order of an element.
153. That is, if $a$ is relatively prime to $m$, then $a$ is a class member of an element of $(\mathbb{Z}/m\mathbb{Z})^{\times}$.
154. As such, $a$ generates a cyclic subgroup of some order $k$ in $(\mathbb{Z}/m\mathbb{Z})^{\times}$.
155. By definition, since $1$ represents the identity class, $a^k\equiv 1 \pmod{m}$.
156. By Lagrange's theorem, since $\varphi(m)$ is the order of $(\mathbb{Z}/m\mathbb{Z})^{\times}$, $k \mid \varphi(m)$, and therefore there must exist some positive integer $n$ such that $\varphi(m) = nk$.
157. Following from this, since $a^{\varphi(m)}$ can be written as $(a^k)^n$, i.e. $1^n$, $a^{\varphi(m)} \equiv 1 \pmod{m}$.
158. In addition, for a power of $a$ to be congruent to $1$ modulo $m$, $a$ must have an inverse modulo $m$, meaning that if $a^{\varphi(m)} \equiv 1 \pmod{m}$ holds, then $a$ must be part of a class in $(\mathbb{Z}/m\mathbb{Z})^{\times}$, i.e. $a$ must be relatively prime to $m$.
159. This property is called *Euler's theorem*.
160. Note that, since for prime $p$, $\varphi(p) = p-1$, so one can write $a^{p-1} \equiv 1 \pmod{p}$ if $a$ is relatively prime to $p$.  
161. This immediately implies Fermat's little theorem, or, one can say that Fermat's little theorem is a special case of Euler's theorem.
162. That is, if one multiplies both sides of $a^{p-1} \equiv 1 \pmod{p}$ by $a$, one gets $a^{p} \equiv a \pmod{p}$.

## Exercises

1. Prove that for any modulus $m$, if $a \equiv -b pmod{m}$, then $a^2 \equiv b^2 \pmod{m}$. Note that any $a \equiv -b pmod{m}$ can be written as $nm + a = km - b$ for some integers $n$, $k$.
2. Demonstrate that $\mathbb{Q} \setminus \set{0}$, the set of non-zero rational numbers (that is, fractions $\frac{p}{q}$ of two integers $p$ and $q$, where $p$ and $q$ are both non-zero) forms a group under multiplication.
3. Prove that if $a$ is not relatively prime to $n$, then $a$ has no multiplicative inverse modulo $n$.
4. If a group $G$ is cyclic of prime order, what are the subgroups of $G$?
5. Does the converse of Lagrange's theorem hold true for abelian groups in particular? That is, if $G$ is a finite abelian group, and some number $n$ divides $|G|$, must there exist a subgroup of $G$ whose order is $n$?
6. Demonstrate that if $H$ is a subgroup of the finite group $G$ with operation $*$, and the set of left cosets induced by $H$ is not the same as the set of right cosets induced by $H$, then the quotient set $G/H$ cannot form a group under $\circ$, defined here as $\forall a, b \in G$, $(a * H) \circ (b * H) = (a * b) * H$, where $*$ is the operation of $G$. Hint: if the sets of left and right cosets are different, can this operation be well-defined?
