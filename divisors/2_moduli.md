# Modular arithmetic

*Basic properties of modular arithmetic. Congruence modulo $m.$ Properties of a group. Additive groups modulo $m.$ Order of a group. Non-zero zero divisors. Multiplicative groups modulo $m.$ Sunzi's theorem. Wilson's theorem. Fermat's little theorem. Cyclic groups. Isomorphisms. Subgroups and cosets. Lagrange's theorem. Order of an element. Euler's theorem. Quadratic residues. Euler's criterion. Legendre symbol. Gauss' lemma for quadratic residues.*

1. Modular arithmetic is "wrap-around" arithmetic.

2. Given a positive integer *modulus* $m$, arithmetic operations on numbers "wrap around" at $m.$

3. It is sometimes introduced as "clock arithmetic," because the temporal units which divide a day, half-day, hour, and so on wrap around at $24$, $12$, and $60$ respectively, and so provide natural examples of moduli: if it is $17:00$, waiting for $10$ hours brings one to $3:00$ on the next day, as opposed to some $27:00.$

4. The properties of arithmetic over a modulus $m$ depend on the set of divisors of $m$, so the description "clock arithmetic" has a critical flaw preventing it from being fully faithful to modular arithmetic.

5. That is, for e.g. hours of the day, addition and subtraction are the only arithmetic operations with motivation.

6. The properties which make a modulus $m$ a nice choice to serve as a temporal period are the same properties which make *multiplication* modulo $m$, structurally speaking, "very bad."

7. There is an equivalence relation between integers called *congruence modulo m*, where $m$ is a positive integer.

8. Two integers $a$ and $b$ are congruent modulo $m$ if there exists an integer $k$ such that $a - b = km.$

9. This condition is equivalent to $m$ dividing the difference between $a$ and $b$, and, since if a number divides an integer $n$, it must also divide $-n$, if there exists a $k$ for $a - b = km$, then there must exist a $k$ for $b - a = km.$

10. If integers $a$ and $b$ are congruent over a modulus $m$, we write $a \equiv b \pmod m.$

11. Congruence is reflexive: any number is congruent to itself under any modulus.

12. Congruence is symmetric. If $a \equiv b \pmod m$, then $b \equiv a \pmod m.$

13. Congruence is transitive. If $a \equiv b \pmod m$ and $b \equiv c \pmod m$ then $a \equiv c \pmod m.$

14. We will use $m\mathbb{Z}$ as a symbol meaning "congruence modulo $m.$"

15. For every positive integer $m$, there is a unique quotient set corresponding to the set of equivalence classes of integers when partitioned according to $m\mathbb{Z}.$ We conventionally denote this set $\mathbb{Z}/m\mathbb{Z}.$

16. Conventionally, we often perform modular arithmetic using the *least residue system* of a modulus $m$, which is simply the set of all non-negative integers which are less than $m.$

17. These integers serve as the class representatives of $\mathbb{Z}/m\mathbb{Z}$, and it is frequently convenient to use $\mathbb{Z}/m\mathbb{Z}$ to refer to the set of representatives as opposed to the set of classes.

18. In practice, a modulus is often framed as taking the arithmetic of a set of infinitely many integers and sending it to a finite set of integers.

19. Addition and subtraction work "normally" over any modulus.

20. A better way of saying this is that addition on $\mathbb{Z}/m\mathbb{Z}$ always forms a *group* of order $m$ for any modulus $m.$

21. A group is a structure comprising a set and an operation which together satisfy certain requirements.

22. Let $S$ be an arbitrary set and $*$ be an arbitrary operation.

23. The first requirement is closure under the operation: $\forall{a, b}\in{S}, a * b\in{S}.$

24. The second is that the operation has an identity: $\exists{e}\in{S}:\forall{a}\in{S},a * e = e * a=a.$

25. The third is that the operation is associative: $\forall{a, b, c}\in{S}, a * (b * c)=(a * b) * c.$

26. The fourth (and most restrictive) requirement is that every element in the set has an *inverse* under the operation.

27. That is, $\forall{a}\in S, \exists{a^{-1}} \in S: a * a^{-1}= a^{-1} * a=e.$

28. It follows from the above requirements that the inverse of any element $a$ in a group is unique to $a.$

29. Suppose for some group $G$ with elements $a$, $b$, and $c$ and identity $e$, were to have $b$ and $c$ each be separate inverses of $a.$

30. That is, $a * b = b * a = e$ and $a * c = c * a = e.$

31. We have $(b * a) * c = e * c$, but we also have $b * (a * c) = b * e$, so it follows from the associative property that it must be the case that $b = c.$

32. An *abelian* group is a group whose operation is commutative. That is, $\forall{a, b} \in S, a * b = b * a.$

33. Groups from arithmetic tend to be commutative because e.g. addition and multiplication of individual numbers are both commutative, and our focus is largely on groups formed out of these operations, but there are many ways to achieve a group structure without commutativity.

34. For example, the set of all element rearrangements (or permutations) of a set of $n$ elements forms a group under composition of permutations (called the *symmetric group of degree $n$*), but the composition of permutations is not in general commutative.

35. The *order* of a group is the cardinality of its underlying set, or how many elements are in the group.

36. Addition over $\mathbb{Z}$ is an abelian group. Every positive integer $n$ has a corresponding negative integer $-n$ (and vice versa) which serves as its *additive inverse.*

37. $0$ is its own inverse, because it is the additive identity, and it follows from the definition of an identity of a group that a two-sided identity element is always its own inverse.

38. If a set has elements without inverses w/r/t an operation, but retains closure, associativity, and an identity element, then that set and operation form a *monoid* as opposed to a group.

39. Multiplication over $\mathbb{Z}$ is a monoid and *not* a group, because non-unit integers do not have other integers as multiplicative inverses in the confines of this set.

40. For any modulus $m$, any element $n$ of $\mathbb{Z}/m\mathbb{Z}$ has a corresponding element $k = m - n$ such that $n + k \equiv 0 \pmod m$, so an additive inverse is always present.

41. From the clock perspective, this is expressed in the notion that whatever hour it is, there is always some number of hours one can wait until the day ends.

42. From the clock perspective, the more "highly composite" a modulus $m$ is, i.e. the more divisors it has relative to its size, the better it is for convenient time-keeping.

43. For any modulus $m$, the equivalence class whose representative is $0$ is the set of multiples of $m.$

44. Consider $ab \equiv 0 \pmod{p}$, where $p$ is prime: since the divisors of $p$ are exactly $1$ and $p$, for any product of positive integers $a$ and $b$, given $ab = p$, either $a = p$ and $b = 1$ or $a = 1$ and $b = p.$

45. So, effectively, the only way to get a product of $0$ in a prime modulus is to multiply a number by $0$ or a multiple of $p.$

46. Now, consider a product like $ab \equiv 0 \pmod{12}$: $a$ could be $2$ if $b$ is $6$, or $a$ could be $3$ if $b$ is $4$, and vice versa.

47. This is to say, two numbers, of which neither is in the "0 class" of the modulus, can multiply with each other to get 0.

48. We will denote the *multiplicative* group of a modulus $m$ with $(\mathbb{Z}/m\mathbb{Z})^{\times}.$

49. While the order of $(\mathbb{Z}/m\mathbb{Z})^{+}$ is always $m$, the set underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ has to have at most $m-1$ elements, provided $m > 1.$

50. This is because $1$ is the identity element of multiplication, and there is no way to get a number which is not $0$ from a product with $0$ as a term.

51. That is, $0$ can never have a multiplicative inverse, so it is excluded from the set.

52. The exception to this is the case where $m = 1$, since all of $\mathbb{Z}$ is collapsed into a single equivalence class represented by $0$, and $0$ times $0$ is $0$, meaning $(\mathbb{Z}/1\mathbb{Z})^{\times}$ is actually a group of order $1.$

53. So, if $ab \equiv 0 \pmod{m}$, and neither $a$ nor $b$ is $0$, then $a$ and $b$ would violate the closure condition required of a group.

54. For this reason, the set of representatives underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is the set of positive integers less than or equal to $m$ which are relatively prime to $m.$

55. So, it follows that the order of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is $\varphi(m)$, i.e. $m - 1$ if and only if $m$ is prime.

56. It is often useful to consider the *negative* class representatives of a modulus, for the reason that $-a \equiv m-a \pmod{m}.$

57. $1$ is its own multiplicative inverse for any modulus, and since $(-1)(-1) = 1$, $m - 1$ is also its own multiplicative inverse for any modulus.

58. Bézout's identity guarantees that if an integer $a$ is relatively prime to $m$, then there exist integers $x$ and $y$ such that $ax + my = 1.$

59. It follows, then, that $ax \equiv{1} \pmod{m}$, i.e. $x$ is the multiplicative inverse of $a$ modulo $m.$

60. Let $n$ and $m$ be positive integers which are relatively prime to one another. Then, the system of linear congruences $x \equiv a \pmod{n}; x \equiv b \pmod{m}$ has a unique solution modulo $nm.$ Since $n$ and $m$ are relatively prime, then by Bézout's identity, there exist integers $x$ and $y$ such that $nx + my = 1.$

61. As such, $nx \equiv 1 \pmod{m}$ but $nx \equiv 0 \pmod{n}$ and $my \equiv 0 \pmod{m}$ but $my \equiv 1 \pmod{n}.$

62. One can conclude that $x = mya + nxb$, since $x \equiv 1a + 0b \equiv a \pmod{n}$ and $x \equiv 0a + 1b \equiv b \pmod{m}.$

63. Since this property holds for a system of two congruences with relatively prime moduli $n$, $m$, it follows that one can find such a unique solution for a system of any number of congruences whose moduli are all mutually (or *pairwise*) relatively prime to one another.

64. That is, if some modulus $k$ is relatively prime to both $n$ and $m$ (where $n \bot m$), then $k \bot{nm}$, and so one can set up the system of linear congruences $x \equiv p \pmod{nm};x \equiv q \pmod{k}$ for some integers $p$ and $q.$

65. That a unique solution exists for such systems over pairwise relatively prime moduli is called *Sunzi's theorem.*

66. There is another way to characterize the prime numbers.

67. A number $p$ is prime if and only if it is the case that $(p - 1)! \equiv -1 \pmod{p}.$

68. Suppose $(n - 1)! \equiv -1 \pmod{n}$ were the case for some composite $n.$

69. A composite number $n$ is divisible by some number $k$ such that $2 \le k < n.$

70. Therefore, since $(n - 1)!$ is divisible by every number less than $n$, $k$ must divide both $n$ and $(n - 1)!$, and so $\gcd((n - 1)!, n)$ must be at least $k.$

71. However, for $(n - 1)! \equiv -1 \pmod{n}$ to be the case, then $\gcd((n - 1)!, n)$ must equal $1.$

72. Note that for $a \equiv -1 \pmod{m}$ to be the case, then there must exist an integer $k$ such that $a = km - 1$, which can be rewritten as $a - km = -1.$

73. If a number divides both $a$ and $km$, then it must divide $a - km$, i.e. $-1$, and so $\gcd(a, km) = 1.$

74. Since $\gcd((n - 1)!, n) \ge k \ge 2$, $(n - 1)! \equiv -1 \pmod{n}$ cannot hold for composite $n.$

75. If $n$ is $1$, then, trivially, $0! \equiv 0 \pmod{1}.$

76. For prime $n$, consider that every element of $(\mathbb{Z}/n\mathbb{Z})^{\times}$ has a multiplicative inverse.

77. Since $(n - 1)!$ is the product of the entire least residue system of modulo $n$ (excepting $0$), $(n - 1)!$ can be arranged into a product of pairs of elements of $(\mathbb{Z}/n\mathbb{Z})^{\times}$ in the form $ab \equiv 1 \pmod{n}$ and $n - 1 \equiv -1 \pmod {n}.$

78. Since it is only for prime $n$ where every positive integer $\le n$ has a multiplicative inverse modulo $n$, it is only for prime $n$ where the product of every positive integer less than $n$ inevitably takes the form $(1)(1)...(-1).$

79. As such, $(p - 1)! \equiv -1 \pmod{p}$ holds for all prime $p$ and only for prime $p.$

80. The above property is called Wilson's theorem.

81. If $a$ is a natural number and $p$ is a prime number, then $a^p \equiv a \pmod {p}.$

82. The binomial theorem is so nice that it is worth stating twice: $(x + y)^n$: $(x + y)^n = \sum^{n}_{k=0}\binom{n}{k}x^{k}y^{n-k};\binom{n}{k} = \frac{n!}{k!(n - k)!}.$

83. $\binom{n}{k}$ is called a *binomial coefficient,* and is read out as "$n$ choose $k.$"

84. A binomial coefficient is always an integer: all multiples of primes in the factorization of $k!(n - k)!$ must also be in the factorization of $n!.$

85. If $n$ is prime, then $n$ divides $\binom{n}{k}$ for all $0 < k < n.$ This is because $n$ always divides $n!$, but since $n$ is prime, it cannot divide $k!(n - k)!$ unless $k = 0$ or $k = n.$

86. As a consequence of this for prime $n$, the only terms of the sum not "zeroed out" by a coefficient which is a multiple of $n$ are $\binom{n}{0}x^{0}y^{p}$ and $\binom{n}{n}x^{p}y^{0}.$

87. This means that if $n$ is prime, then $(x + y)^n \equiv x^n + y^n \pmod{n}.$

88. It holds that $0^p \equiv 0 \pmod {p}$ for a prime $p.$

89. If we assume that for some positive integer $k$, $k^p \equiv k \pmod {p}$ is the case, then we can say that since the freshman's dream comes true for a prime modulus $p$, i.e. $(k + 1)^p \equiv k^p + 1^p \pmod{p}$, it follows that $(k + 1)^p \equiv k + 1 \pmod{p}.$

90. This is exactly our original statement $a^p \equiv a \pmod {p}$, which is called Fermat's little theorem.

91. A *primitive root* modulo $m$ is a number $n$ in $(\mathbb{Z}/m\mathbb{Z})^{\times}$ which *generates* every element of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ through repeated multiplication.

92.  That is, if $c$ being an element of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ implies that there exists an integer $k$ such that $c \equiv n^k \pmod{m}$, then $n$ is a primitive root modulo $m.$

93.  Only certain moduli have primitive roots: only if $m$ is $1$, $2$, $4$, $p^k$, or $2p^k$, where $p$ is an odd prime and $k$ is a positive integer, then the modulus $m$ has at least one primitive root.

94.  If $n$ is a primitive root modulo $m$, then the multiplicative inverse of $n$ is also a primitive root modulo $m.$

95.  A group where all of its elements can be generated by repeat iterations of its operation on a single element and that element's inverse is called a *cyclic* group.

96.  The integers under addition form the archetypal infinite cyclic group, since any integer can be reached from a sum of terms of $-1$ and $1.$

97.  $(\mathbb{Z}/m\mathbb{Z})^{+}$ is the archetypal finite cyclic group, being cyclic for every modulus: the cyclic group of order $m$ is often denoted simply $\mathbb{Z}_m.$

98.  For any modulus $m$, one can get all of the elements in $\mathbb{Z}_m$ from repeated addition by 1, or, more generally, a class which is relatively prime to $m.$

99.  All cyclic groups are abelian, but not every abelian group is cyclic.

100. It follows from the definition of a primitive root that a group $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is cyclic if and only if it has a primitive root.

101. A group $A$ is *isomorphic* to a group $B$ if there exists a one-to-one correspondence (i.e. a bijection) between the elements of the set underlying $A$ and the elements of the set underlying $B$ which preserves group structure in both directions.

102. We write that $A$ is isomorphic to $B$ as $A \cong B.$

103. For example, $\mathbb{Z}_{2} \cong (\mathbb{Z}/3\mathbb{Z})^{\times}.$

104. The representatives of the set underlying $\mathbb{Z}_{2}$ are $\set{0, 1}$, while the corresponding representatives for $(\mathbb{Z}/3\mathbb{Z})^{\times}$ are $\set{1, 2}.$

105. In small groups like these, one can verify the isomorphism simply by exhausting all possible operation outcomes: we match $0$ and $1$ in the former to $1$ and $2$ in the latter respectively, and we match addition in the former to multiplication to the latter.

106. We can then take note that $0 + n \equiv n \pmod{2}$ and $1 + 1 \equiv 0 \pmod{2}$, while $(1)n \equiv n \pmod{3}$ and $(2)(2) \equiv 1 \pmod{3}.$

107. Since this covers every way elements can be combined within these groups, it is apparent that their basic structure is the same.

108. Every finite cyclic group of order $n$ is isomorphic to $(\mathbb{Z}/n\mathbb{Z})^{+}.$

109. This property emerges from the fact that because for any cyclic group, having a single generator $g$, one can write all of its elements as the $k$-th multiple of that generator $kg$ (where $-kg$ denotes the $k$-th multiple of the generator's inverse and $0g$ is the identity).

110. If a group $G$ comprises the set $S$ and the operation $*$, then a *subgroup* of $G$ is a group formed from a subset $S' \subseteq S$ under the same operation $*.$

111. Much like it is often convenient to refer to equivalence classes by their representatives, it is convenient to say "elements of a group" to mean the elements of the group's underlying set.

112. Every group is a subgroup of itself.

113. The one-element *trivial group*, which consists of the identity element, is a subgroup of every group.

114. A group can have at minimum $1$ element.

115. Consider that the empty set can never be the underlying set of a group, because a group requires an identity element, and the empty set has no elements.

116. A subgroup $H$ of a group $G$ partitions the underlying set $S$ of $G$ into a set of *left cosets* and a set of *right cosets.*

117. A left coset of $H$ in $G$ is the set $g*H = \set{g * h \mid h \in H}$ for some fixed $g \in G.$

118. A right coset of $H$ in $G$ is the set $H*g = \set{h * g \mid h \in H}$ for some fixed $g \in G.$

119. Left and right cosets can be viewed as equivalence classes formed out of the relations $g \sim h \iff -g * h \in H$ and $g \sim h \iff h * -g \in H$ (for fixed $g \in G$) respectively.

120. A subgroup always induces the same number of left cosets as it does right cosets.

121. Every coset in a partition is *disjoint* to every other coset in the same partition.

122. If $G$ is abelian, then the left coset partition induced by $H$ is itself the same as the right coset partition induced by $H.$

123. The number of cosets induced in the underlying set of a group $G$ by a subgroup $H$ is called the *index of $H$ in $G$* and is denoted $[G:H].$

124. $H$ induces its own underlying set as both a left and a right coset.

125. That is, if $e$ is the identity of $G$, then it is apparent that $\set{e * h \mid h \in H} = \set{h * e \mid h \in H}.$

126. Moreover, if $H$ is a subgroup of $G$, then $H$ must contain the identity element of $G.$

127. Given that every coset in a partition is disjoint from every other, the set $H'$ which underlies $H$ is the only set in a coset partition induced by $H$ which can underlie a subgroup of $G$, since $H'$ is the sole possessor of the identity of $G.$

128. Every coset induced by a subgroup $H$ has the same number of elements as $H.$

129. For example, if we take the group $\mathbb{Z}_6$, i.e. the additive group of integers modulo $6$, and its set of representatives $\set{0, 1, 2, 3, 4, 5}$, it is apparent that $\set{0, 2, 4}$ and $\set{0, 3}$ each underlie a subgroup of $\mathbb{Z}_6.$

130. Note that, w/r/t addition modulo $6$, $\set{0, 2, 4}$ is cyclic and of order $3$, and as such must be isomorphic to $\mathbb{Z}_3.$

131. The set $\set{0, 3}$, w/r/t addition modulo $6$, is likewise isomorphic to $\mathbb{Z}_2.$

132. $\mathbb{Z}_3$ induces $2$ cosets in $\mathbb{Z}_6$, while $\mathbb{Z}_2$ induces $3.$

133. More generally, if $H$ is a subgroup of a finite group $G$, and $|G|$ denotes the order of a group, then the number of cosets $H$ induces in $G$ is given by $\frac{|G|}{|H|}.$

134. If $H$ is a subgroup of a group of finite order $G$, then the order of $H$ divides the order of $G.$

135. This stems from the very ideas of subgroup and coset: a coset is an effective "translation" of an entire subgroup by an element in the group.

136. Suppose $H$ is a subgroup of the finite group $G$ and $|H|$ doesn't divide $|G|.$

137. It is insensible for the order of a group to not be an integer, so $|H|$ not dividing $|G|$ would imply that $H$ induces a "remainder coset" in either direction which would have fewer elements than $H.$

138. However, every coset induced by $H$ is an image of $H$ under the group operation, meaning two elements would be mapped to the same element by it, making this so-called "translation" non-invertible.

139. That is, for $|H|$ to not divide $|G|$ there would have to be an element in $G$ without a unique inverse, violating the conditions for a set to be a group under an operation, and so the order of $H$ must divide $|G|.$

140. That $|H|$ must divide $|G|$ if $H$ is a subgroup of a finite group $G$ is one of two theorems called *Lagrange's theorem*.

141. The *order of an element* of a group is the order of the cyclic subgroup generated by that element.

142. If $g$ is an element of a group $G = (G', *)$, then $\langle{g}\rangle = (\set{kg \mid k \in \mathbb{Z}\land g \in G'}, *)$ is the cyclic subgroup generated by $g.$

143. If $\langle{g}\rangle$ is finite, its order is given by the smallest integer $k$ such that $kg = e$, where $e$ is the identity of $G.$

144. Positive integers $a$ and $m > 1$ are relatively prime if and only if it is the case that $a^{\varphi(m)} \equiv 1 \pmod{m}.$

145. This follows directly from Lagrange's theorem and the definition of the order of an element.

146. That is, if $a$ is relatively prime to $m$, then $a$ is a class member of an element of $(\mathbb{Z}/m\mathbb{Z})^{\times}.$

147. As such, $a$ generates a cyclic subgroup of some order $k$ in $(\mathbb{Z}/m\mathbb{Z})^{\times}.$

148. By definition, since $1$ represents the identity class, $a^k\equiv 1 \pmod{m}.$

149. By Lagrange's theorem, since $\varphi(m)$ is the order of $(\mathbb{Z}/m\mathbb{Z})^{\times}$, $k \mid \varphi(m)$, and therefore there must exist some positive integer $n$ such that $\varphi(m) = nk.$

150. Following from this, since $a^{\varphi(m)}$ can be written as $(a^k)^n$, i.e. $1^n$, $a^{\varphi(m)} \equiv 1 \pmod{m}.$

151. In addition, for a power of $a$ to be congruent to $1$ modulo $m$, $a$ must have an inverse modulo $m$, meaning that if $a^{\varphi(m)} \equiv 1 \pmod{m}$ holds, then $a$ must be part of a class in $(\mathbb{Z}/m\mathbb{Z})^{\times}$, i.e. $a$ must be relatively prime to $m.$

152. This property is called *Euler's theorem*.

153. Note that, since for prime $p$, $\varphi(p) = p-1$, so one can write $a^{p-1} \equiv 1 \pmod{p}$ if $a$ is relatively prime to $p.$

154. This immediately implies Fermat's little theorem, or, one can say that Fermat's little theorem is a special case of Euler's theorem.

155. That is, if one multiplies both sides of $a^{p-1} \equiv 1 \pmod{p}$ by $a$, one gets $a^{p} \equiv a \pmod{p}.$

156. A *quadratic residue* modulo $m$ is an element $n$ of $\mathbb{Z}/m\mathbb{Z}$ where there exists some $k$ such that $k^2 \equiv n \pmod{m}$.

157. Alternatively, a quadratic residue modulo $m$ is some number class $n$ such that the polynomial congruence $k^2 - n \equiv 0 \pmod{m}$ has a solution.

158. Mainly, we will focus on quadratic residues modulo odd primes.

159. Both $0$ and $1$ are quadratic residues modulo $2$.

160. For any $a \in \mathbb{F}_p$, if $a + b \equiv 0 \pmod{p}$, then $a^2 \equiv b^2 \pmod{p}$.

161. The above can be rewritten to $b \equiv -a \pmod{p}$.

162. It is easy to see that $a^2 \pmod{p}$ is a reduction of $(p + a)^2 \pmod{p},$and $b^2 \pmod{p}$ can be written as $(p - a)^2 \pmod{p}$.

163. That is, $(p + a)(p + a)$ can be written as $p^2 + 2pa + a^2$, where only $a^2$ does not vanish modulo $p$.

164. Likewise, $(p - a)(p - a)$ can be written as $p^2 - 2pa + a^2$, where, once again, only $a^2$ does not vanish modulo $p$.

165. Therefore, if $a^2 \equiv n \pmod{p}$, then $-a^2 \equiv n \pmod{p}$.

166. $0$ is a quadratic residue for any modulus, so we can say that the number of unique quadratic residues for an odd prime modulus $p$ is $\frac{p + 1}{2}$.

167. To see why this is the exact number of residues as opposed to the maximum, we can look again at the congruence $a^2 \equiv b^2 \pmod{p}$.

168. Naturally, we can write this as $a^2 - b^2 \equiv 0 \pmod{p}$.

169. By difference of squares factorization, we can rewrite it again as $(a - b)(a + b) \equiv 0 \pmod{p}$, directly indicating that if $a^2 \equiv b^2 \pmod{p}$, then either $a \equiv b \pmod{p}$ or $a \equiv -b \pmod{p}$.

170. There is a congruence called *Euler's criterion* which determines whether or not some $a$ is a quadratic residue for an odd prime modulus $p$ (where $a$ is relatively prime to $p$).

171. If $a^{\frac{p-1}{2}}\equiv 1 \pmod{p}$, then $a$ is a quadratic residue modulo $p$.

172. If $a^{\frac{p-1}{2}}\equiv -1 \pmod{p}$, then $a$ is *not* a quadratic residue modulo $p$.

173. The expression $a^{\frac{p-1}{2}}$ can only be congruent to $1$ or $-1$.

174. Let $g$ be a primitive root of an odd prime modulus $p$. Then, the element $g^{\frac{p-1}{2}}$ is the unique element of order $2$ in $(\mathbb{Z}/p\mathbb{Z})^{\times}$.

175. That is, $g^{\frac{p-1}{2}} \equiv -1 \pmod{p}$.

176. By Euler's theorem, $(g^{\frac{p-1}{2}})^2 \equiv g^{p-1} \equiv 1 \pmod{p}$.

177. However, since $p-1$ is the order of $(\mathbb{Z}/p\mathbb{Z})^{\times}$, $g^{\frac{p-1}{2}}$ is never $g^{p-1}$, meaning $g^{\frac{p-1}{2}}$ is the unique congruence class $-1$ which is not itself $1$ but whose square is $1$.

178. Since $p$ here is an odd prime, $p-1$ must be a positive even number, so $a^{p-1}$ is a perfect square.

179. It follows that we can rewrite $a^{p-1} \equiv 1 \pmod{p}$ as $a^{p-1} - 1 \equiv 0 \pmod{p}$ and apply the difference of squares factorization to get $(a^{\frac{p-1}{2}} - 1)(a^{\frac{p-1}{2}} + 1) \equiv 0 \pmod{p}$.

180. Since either $(a^{\frac{p-1}{2}} - 1)$ or $(a^{\frac{p-1}{2}} + 1)$ must be congruent to $0$, $a^{\frac{p-1}{2}}$ must be congruent to either $1$ or $-1$.

181. If $1$, then $a^{\frac{p-1}{2}} \equiv a^{p-1}$, but if $-1$, then note that there is at least one primitive root $g$ in $(\mathbb{Z}/p\mathbb{Z})^{\times}$ and so $a = g^k$ for some integer $k$.

182. Following from this, $a^{\frac{p-1}{2}} = (g^k)^{\frac{p-1}{2}}$.

183. We can rewrite this to $(g^{\frac{p-1}{2}})^k$.

184. Since $g^{\frac{p-1}{2}} \equiv -1 \pmod{p}$ for any odd prime modulus, Euler's criterion essentially reads the parity of the power to which a primitive root is taken.

185. Since $(a^{n})^2 = a^{n}a^{n}=a^{n+n}$, and the sum of two numbers of the same parity is always even, it follows that if a number is an odd power of a primitive root, there is no other power of a primitive root which can be squared in order to arrive at it.

186. If for a number $a = g^k$, $k$ is even, then that means $k = 2n$ for some $n$-th power of a generator $g^n$, and so $a$ is a quadratic residue.

187. If for a number $a = g^k$, $k$ is odd, then there is no such $n$ for which $k = 2n$, i.e. no $k = g^{n}g^{n} = g^{n+n}$.

188. So, Euler's criterion encodes that some $a$ in $(\mathbb{Z}/p\mathbb{Z})^{\times}$ for odd prime $p$ is a quadratic residue in $a^{\frac{p-1}{2}}\equiv 1 \pmod{p}$ and that some $a$is not a quadratic residue in $a^{\frac{p-1}{2}}\equiv -1 \pmod{p}$.

189. There is a function called the *Legendre symbol* $(\frac{a}{p})$ which maps an integer $a$ and an odd prime $p$ to whichever $k \in \set{-1, 0, 1}$ satisfies $a^{\frac{p-1}{2}} \equiv k \pmod{p}$.

190. Like Euler's criterion, $(\frac{a}{p})$ characterizes quadratic residues modulo $p$, evaluating to $1$ if $a$ is one, $-1$ if not, but is additionally defined to be $0$ if $a$ is a multiple of $p$.

191. It follows immediately from Euler's criterion that the Legendre symbol is *completely multiplicative* w/r/t its top argument.

192. That is, for some fixed odd prime $p$, $(\frac{ab}{p})=(\frac{a}{p})(\frac{b}{p})$.

193. Consider the least residue system modulo $p$, where $p$ is an odd prime.

194. Since $p$ is an odd prime, $p - 1$ is the number of non-zero elements in the least residue system, and $\frac{p-1}{2}$ is always an integer.

195. So we can split the set $\set{1, 2, 3, {...}, p-1}$ in half around $\frac{p}{2}$ into $A = \set{1, 2, 3, {...}, \frac{p-1}{2}}$ and $B = \set{\frac{p+1}{2}, \frac{p+3}{2}, {...}, p-1}$.

196. Given the additive inverse property in modular arithmetic, however, one can also write $B = \set{-1, -2, -3, {...}, -\frac{p-1}{2}}$.

197. It follows that one can define a "modular absolute value" function which assigns values in $A$ to themselves and values in $B$ to their additive inverses.

198. For a non-zero least residue $x$ modulo $p$, we can say that $|x| = x$ for $1 \le x \le \frac{p-1}{2}$ and $|x| = p-x$ for $\frac{p+1}{2} \le x \le p-1$.

199. That is, we interpret elements of $A$ in their positive representation, and elements of $B$ as the "absolute value" of their negative representation.

200. For convenience, we will call the non-zero elements of a least residue system modulo $p$ which are less than or equal to $\frac{p-1}{2}$ as the "$A$-side" of the partition, and the elements which are greater than $\frac{p-1}{2}$ as its "$B$-side."

201. Let $p$ be an odd prime, and let $a$ be relatively prime to $p$.

202. Let $L$ be the subset of the least residue system modulo $p$ formed from $\set{a, 2a, 3a, {...}, \frac{p-1}{2}a}$, and let $n$ be the number of elements in $L$ which are greater than $\frac{p-1}{2}$.

203. Then, $(\frac{a}{p}) = (-1)^n$.

204. This is called *Gauss' lemma.*

205. We can write the product of all the elements in $L$ in multiple ways.

206. Directly, we can say that the product of residues in $L$ amounts to $a^{\frac{p-1}{2}}\frac{p-1}{2}! \pmod{p}$.

207. From the definition of the Legendre symbol, we can write $a^{\frac{p-1}{2}}\frac{p-1}{2}! \pmod{p}$$ as $(\frac{a}{p})\frac{p-1}{2}! \pmod{p}$.

208. Consider the product $(|a||2a||3a|...|\frac{p-1}{2}a|)$.

209. Since $|ra| \equiv |sa| \pmod{p}$ implies that $r = \pm s$, the values in $\set{|a|,|2a|,|3a|,... ,|\frac{p-1}{2}a|}$ are all distinct.

210. Since these values are all distinct and all fall into side $A$, they constitute a permutation of $A$.

211. So, we can write the product of residues in $L$ as $(-1)^n(|a||2a||3a|...|\frac{p-1}{2}a|)$, where $n$ is the number of residues in $L$ which would fall on the "$B$-side" of the partition.

212. We can justify $(-1)^n$ because each $B$-side residue in $L$ constitutes a sign change in the product.

213. Then, since we know that $(|a||2a||3a|...|\frac{p-1}{2}a|)$ is a permutation of $A,$ we can write our product as $(-1)^{n}\frac{p-1}{2}!$.

214. So, since we have two ways of writing the same product $(\frac{a}{p})\frac{p-1}{2}! \equiv (-1)^{n}\frac{p-1}{2}! \pmod{p}$, we can cancel the factorials, and write $(\frac{a}{p}) = (-1)^n$.

215. We will call this *Gauss' lemma for quadratic residues.*

## Exercises

1. Prove that for any modulus $m$, if $a \equiv -b pmod{m}$, then $a^2 \equiv b^2 \pmod{m}.$ Note that any $a \equiv -b pmod{m}$ can be written as $nm + a = km - b$ for some integers $n$, $k.$

2. Demonstrate that $\mathbb{Q} \setminus \set{0}$, the set of non-zero rational numbers (that is, fractions $\frac{p}{q}$ of two integers $p$ and $q$, where $p$ and $q$ are both non-zero) forms a group under multiplication.

3. Prove that if $a$ is not relatively prime to $n$, then $a$ has no multiplicative inverse modulo $n.$

4. If a group $G$ is cyclic of prime order, what are the subgroups of $G$?

5. Does the converse of Lagrange's theorem hold true for abelian groups in particular? That is, if $G$ is a finite abelian group, and some number $n$ divides $|G|$, must there exist a subgroup of $G$ whose order is $n$?

6. Demonstrate that if $H$ is a subgroup of the finite group $G$ with operation $*$, and the set of left cosets induced by $H$ is not the same as the set of right cosets induced by $H$, then the quotient set $G/H$ cannot form a group under $\circ$, defined here as $\forall a, b \in G$, $(a * H) \circ (b * H) = (a * b) * H$, where $*$ is the operation of $G.$ Hint: if the sets of left and right cosets are different, can this operation be well-defined?
