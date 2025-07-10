# Extensions

*Vector spaces and properties of vectors. Linear combinations. Linear dependence and independence. Vector subspaces. Span and basis. Steinitz exchange lemma. Dimension of a vector space. Linear maps. Field extensions. Splitting fields. Adjunctions and simple extensions. Integral and algebraic elements. Minimal polynomials. Formal derivative of a polynomial. Splitting field of $x^q.$*

1. A *vector space* $V$ is a set of $n$-tuples called *vectors* whose components are called *scalars*, where scalars are elements from some field $K$.

2. A vector space has a notion of *vector addition,* which is the component-wise addition of vectors.

3. If ${u} = (a_1, a_2, {...}, a_n)$ and ${v} = (b_1, b_2, {...}, b_n)$ are vectors, then their sum ${u} + {v} = (a_1 + b_1, a_2 + b_2, {...}, a_n + b_n)$ is a vector.

4. A vector space has a notion of *scalar multiplication,* which is the multiplication of each component of a vector by some scalar from the scalar field.

5. If $\lambda$ is a scalar and ${v} = (a_1, a_2, {...}, a_n)$ is a vector, then $\lambda{{v}} = (\lambda a_1, \lambda a_2, {...}, \lambda a_n)$.

6. The operations of a vector space must satisfy certain properties.

7. First, vector addition is an abelian group whose identity element is called the *zero vector,* boldly denoted $\mathbf{0},$ and whose components are all $0,$ in the sense of the additive identity of the scalar field.

8. Second, if $a$ and $b$ are scalars from $K$ and ${v} \in V$ is a vector from a vector space over $K,$ then $a(bv) = (ab){v}.$

9. Third, $1{v} = {v}.$

10. Finally, if $a, b$ are scalars and $u, v$ are vectors, then $a(u + {v}) = a{u} + a{v}$ and $(a + b)v = av + bv.$

11. Let $a_i \in K$ and $v_i \in V.$ A *linear combination* of vectors in $V$ is an expression of the form $a_1{v}_1 + a_2{v}_2 + {...} + a_n{v}_n.$

12. A sequence of vectors $\mathbf{v}_i \in V$ is said to have *linear dependence* if there exists a sequence of scalars $a_i \in K$ such that these scalars are not all $0$ and $a_1\mathbf{v}_1 + a_2\mathbf{v}_2 + {...} + a_n\mathbf{v}_n = \mathbf{0}.$

13. Likewise, if all equations of the form $a_1v_1 + a_2v_2 + {...} + a_nv_n = \mathbf{0}$ are satisfied only when each $a_i$ is equal to $0$, then the sequence of vectors $(v_1, v_2, {...}, v_n)$ is said to have *linear independence.*

14. Suppose a vector $v$ can be written in two different ways as a linear combination of vectors $(v_1, v_2, {...}, v_n),$ in the sense that for sequences of scalars $(a_1, a_2, {...}, a_n)$ and $(b_1, b_2, {...}, b_n)$ where $a_i \neq b_i$ for at least one value of $i,$ $v = \sum_{i=1}^n a_i v_i = \sum_{i=1}^n b_i v_i.$

15. Then, one can set a sequence of scalars $(c_1, c_2, {...}, c_n)$ by $a_i - b_i$ such that $\sum_{i=1}^n c_i v_i = \mathbf{0}.$

16. This means that the vectors $(v_1, v_2, {...}, v_n)$ are linearly dependent.

17. Another way of looking at it is as follows: given scalars $d_i$ which are not all $0,$ $\sum_{i=1}^n d_i v_i = \mathbf{0}$ is exactly the condition for the linear dependence of vectors $v_i.$

18. Without loss of generality, let us say $d_n \neq 0.$ Then, $d_nv_n = - \sum_{i=1}^{n-1} d_i v_i.$ Then, we can write $v_n$ as a linear combination $v_n = - \sum_{i=1}^{n-1} \frac{d_i}{d_n} v_i.$

19. If $V$ is a vector space with vectors in $K,$ and $W$ is a non-empty subset of $V,$ and $W$ forms a vector space with the operations of $V,$ then $W$ is a *(vector) subspace* of $V.$

20. That is, $W$ is a subspace of $V$ if for all $u, v \in W$ and for all $a, b \in K,$ $au + bv \in W.$

21. That is, a subset $W \subseteq V$ of a vector space is a subspace if $W$ is closed under linear combinations with scalars from $K.$

22. The set containing only the zero vector is a subspace of every vector space.

23. Every vector space is a subspace of itself.

24. If $S$ is a subset of $V$, then the *linear span* of $S$ is the minimal subspace (in terms of set inclusion) of $V$ which contains $S.$

25. The linear span $\langle{S}\rangle$ of $S$ is then the set of all finite linear combinations of elements of $S,$ and $S$ is considered the *spanning set* of $\langle{S}\rangle.$

26. A *basis* $B$ of a vector space $V$ is a subset of $V$ which is linearly independent and which spans $V,$ in the sense that $\langle{B}\rangle = V.$

27. That is, if $B$ is a basis of $V,$ then every vector in $V$ can be written as a linear combination of vectors in $B.$

28. Let $V$ be a vector space and let $A = \set{u_1, u_2, {...}, u_n}$ be a finite set of linearly independent vectors in $V.$ Suppose $B = \set{v_1, v_2, {...}, v_m}$ spans $V.$

29. Then, $n \le m,$ and there exists a subset $C \subseteq V$ such that $|C| = m - n$and $A \cup C$ spans $V.$

30. This property is called the *Steinitz exchange lemma.*

31. First, it is easy to see that the Steinitz exchange lemma holds for the case $n = 0,$ since this means that $A = \varnothing.$

32. Assume the Steinitz exchange lemma holds for the case where $n - 1.$

33. We can replace $n-1$ vectors in $B$ with the vectors of $A' = \set{u_1, u_2, {...}, u_{n-1}}$ to get a set which we can index as $U = \set{u_1, {...}, u_{n-1}, {...}, v_m}.$

34. By the inductive hypothesis, $U$ spans $V.$

35. So, for $\alpha_i, \beta_j \in K$ we can write $u_n$ as a linear combination $u_n = \sum_{i = 1}^{n-1}\alpha_iu_i + \sum_{j = n}^{m}\beta_j v_j.$

36. Not all scalars $\beta_j$ can be $0$, since that would contradict $A$ being linearly independent; this means that $n \le m.$

37. Since we can allow ourselves the freedom of reordering terms, we will say that $\beta_n \neq 0.$

38. So, we can write $u_n = \sum_{i = 1}^{n-1}\alpha_iu_i + \sum_{j = n + 1}^{m}\beta_j v_j + \beta_n v_n,$ then isolate $v_n$ to get $v_n = \frac{1}{\beta_n}(u_n - \sum_{i = 1}^{n-1}\alpha_iu_i - \sum_{j = n + 1}^{m}\beta_j v_j).$

39. So, $v_n$ is in the span of $\set{u_1, {...}, u_n, v_{n + 1}, {...} v_m},$ and this set spans $V.$

40. The *dimension* $\dim(V)$ of a vector space $V$ is the cardinality of any basis of $V.$

41. Every basis of a finite-dimensional vector space $V$ has the same cardinality.

42. Suppose $B = \set{u_1, u_2, {...}, u_n}$ and $B' = \set{v_1, v_2, {...}, v_m}$ are each a basis of $V.$

43. Via the definition of a basis, $B$ and $B'$ are both linearly independent and span $V,$ so by the Steinitz exchange lemma, $|B| \le |B'|$ and $|B'| \le |B|,$ meaning that $|B| = |B'|.$

44. It is often convenient to consider a vector space in the setting of its *standard basis,* which is a set $B = \set{u_1, u_2, {...}, u_n}$ such that if $u_i = (\lambda_1, \lambda_2, {...}, \lambda_n),$ then, for all $\lambda_j,$ $\lambda_{j=i} = 1$ and $\lambda_{j \neq i} = 0.$

45. Let $V$ and $W$ be vector spaces over a field $K.$ Then, $f : V \to W$ is a *linear map* or *vector space homomorphism* if for any vectors $v, w \in V$ and any scalar $k \in K,$ $f(v + w) = f(v) + f(w)$ and $f(kv) = kf(v).$

46. Scalar multiplication is a linear map, more or less by definition.

47. That is, let $V$ be a vector space over $K,$ and let $S_k : V \to V$ where $S_k(v) = kv.$

48. By the rules of the operations of a vector space and the properties of fields, $S_k$ is a linear map, and it is a linear automorphism for nonzero $k.$

49. Addition by a fixed vector is not a linear map, however.

50. That is, suppose $\alpha_u : V \to V$ is a map $\alpha(v) = u + v.$ Then, $\alpha(v) + \alpha(w) = 2u + v + w \neq u + v + w.$

51. Suppose $V$ is a two-dimensional vector space over a field $K,$ where $a, b, c, d \in K.$ Then, a linear map $f : V \to V$ can be written in the general form $f(x, y) = (ax + by, cx + dy)$ for basis vectors $x, y.$

52. If the dimension of a vector space $V$ is a non-negative integer $n,$ then an endomorphism of $V$ can be written as an $n$-tuple of linear combinations of $n$ basis vectors, where each vector is scaled by some factor in $K.$

53. It is left to the doubly-indexed-sum-loving reader to derive the $n$-dimensional general form.

54. Linear maps of a given vector space can be added together.

55. For example, if $f(x, y) = (a_1 x + b_1 y, c_1 x + d_1 y)$ and $g(x, y) = (a_2 x + b_2 y, c_2 x + d_2 y)$ for basis vectors $x, y \in V,$ then $(f + g)(x, y) = ((a_1 + a_2)x + (b_1 + b_2)y, (c_1 + c_2)x + (d_1 + d_2)y).$

56. Let $V$ be a vector space over a field $K$ such that $\dim(V) = 2.$ Then, the subspaces of $V$ which are not $\set{0}$ or $V$ itself are exactly the sets of the form $\set{kv \mid k \in K}$ for a fixed vector $V.$

57. Likewise, if we suppose $V$ is a three-dimensional vector space over $K$ and $x, y \in V$ are fixed and linearly independent, then the non-trivial proper subspaces of $V$ take the form $\set{ax + by \mid a, b \in K}.$

58. Any field $K$ can be interpreted as a one-dimensional vector space over itself.

59. As such, if $V$ is a vector space over $K,$ then a function $f : V \to K$ which satisfies $f(v + w) = f(v) + f(w)$ and $f(kv) = kf(v)$ for $v, w \in V$ and $k \in K$ is a linear map.

60. A linear map from a vector space to its field of scalars is called a *linear form.*

61. Suppose $1 \le k \le n$ are integers and $\pi_k : V \to K$ for a vector space $V$over a field $K.$ If we define $\pi_k$ as $\pi_k(x_1, x_2, {...}, x_n) = x_k,$ then $\pi_k$ is an example of a linear form.

62. There is a notion of a *quotient space* of a vector space.

63. Let $V$ be a vector space and let $S$ be a subspace of $V.$ Then, elements of $V/S$ are classes of the form $[v] = v + S = \set{v + s \mid s \in S}$ for $v \in V.$

64. For $u, v \in V$ and $k \in K,$ we define vector addition on $V/S$ as $[u] + [v] = [u + v]$ and scalar multiplication by $k[v] = [kv].$

65. Linear maps have a notion of kernel and image: the kernel of a linear map $f : V \to W$ is the subspace of $V$ which maps to the zero vector under $f$, and $\text{im}(f) = \set{f(v) \mid v \in V}$ is a subspace of $W.$

66. It follows that we have $V/\text{ker}(f) \cong \text{im}(f).$

67. A polynomial ring over a field can be seen to satisfy the axioms of a vector space.

68. That is, polynomial addition is vector addition and polynomials respect scalar multiplication and the distributive laws.

69. A polynomial ring over a field is an infinite-dimensional vector space.

70. That is, the standard basis for a polynomial ring in $x$ is $\set{1, x, x^2, x^3, {...}}.$

71. Since a polynomial is a finite sum of monomials, a polynomial as an infinite-dimensional vector has finitely many non-zero elements.

72. Suppose $L$ is a field. The evaluation map $\text{ev}_k : L[x] \to L$ at a fixed element $k \in L$ defined as $\text{ev}_k(P) = P(k)$ is a linear form.

73. If $K$ and $L$ are fields such that $K \subseteq L$, then $K$ is a *subfield* of $L$, and $L$ is said to be an *extension* of $K$.

74. If $L$ is an extension of a field $K$, we can write $L : K$, which can be read as "$L$ over $K$."

75. A field which has no proper subfields is called a *prime field.*

76. The archetypal examples are $\mathbb{F}_p$ for prime $p$ and the field of rational numbers $\mathbb{Q}.$

77. If $L$ extends $K,$ then $L$ is a vector space with scalars in $K.$

78. The degree $[L:K]$ of the field extension $L : K$ is the dimension of $L$ considered as a vector space over $K.$

79. For example, $\mathbb{Q}[i]$ is an extension of $\mathbb{Q}.$

80. Every element of $\mathbb{Q}[i]$ can be written as a linear combination of $1$ and $i$ with scalars drawn from $\mathbb{Q}.$

81. That is, one can view $a + bi \in \mathbb{Q}[i]$ as a vector $(a, b),$ and, as such, $\set{1, i}$ is a standard basis for the space $\mathbb{Q}[i].$

82. Then, $[\mathbb{Q}[i]: \mathbb{Q}] = 2.$

83. Given a polynomial $P$ with coefficients in a field $K,$ the *splitting field* of $P$ is the smallest field extension of $K$ in which $P$ factors into a product of linear polynomials.

84. That is, if $L$ is the minimal-degree extension $L : K$ such that a polynomial $P$ in $K[x]$ factors into the product $P(x) = k\prod^{\text{deg}(P)}_{i = 1}(x - a_i)$ for $k \in K$ and $a_i \in L,$ then $L$ is the splitting field of $P.$

85. For example, $\mathbb{Q}[i]$ is the splitting field for $x^2 + 1 \in \mathbb{Q}[x].$

86. Let $L : K$ be a field extension. If $\lambda \in L$ is algebraic over $K,$ then the *adjunction* $K[\lambda]$ of $\lambda$ to $K$ is the set of all linear combinations in the form $a + b\lambda$ for $a, b \in K.$

87. A field extension consisting of a single adjunction $K[\lambda] : K$ is called a *simple* extension.

88. $\mathbb{Q}[i]$ and $\mathbb{Q}[\sqrt{2}]$ are examples of simple extensions.

89. If $k$ is a positive integer, we can define the *square root* $\sqrt{k}$ as the value $x$ such that $x^2 = k.$

90. By the laws of exponents, we can write a square root $\sqrt{k}$ as a fractional power $k^{\frac{1}{2}}.$

91. We also say that if $x^n = k,$ then $\sqrt[n]{k} = k^{\frac{1}{n}} = x,$ and $x$ is an $n$-th root of $k.$

92. Similarly for the square roots of negative numbers, because $(-i)^2 = i^2 = -1,$ we refer to a *principal square root* such that $\sqrt{-n} = i\sqrt{n}.$

93. It follows from this that we can also write $\mathbb{Q}[i]$ as $\mathbb{Q}[\sqrt{-1}].$

94. Much like we could construct $\mathbb{Z}[i]$ via the quotient of $\mathbb{Z}[x]$ and the ideal generated by the irreducible polynomial $x^2 + 1,$ we can construct a ring $\mathbb{Z}[x]/(x^2 - 2)$ which is governed by a rule such that $x^2 \equiv 2 \pmod{x^2 - 2}.$

95. In the ring $\mathbb{Z}[x]/(x^2 - 2),$ we can then write every element in the form $q = a + b\sqrt{2}$ for integers $a$ and $b.$

96. As such, we write $\mathbb{Z}[x]/(x^2 - 2)$ as $\mathbb{Z}[\sqrt{2}].$

97. Since $x^2 - 2$ is irreducible in $\mathbb{Z}[x],$ it generates a prime ideal $(x^2 - 2)$ so $\mathbb{Z}[\sqrt{2}]$ is an integral domain.

98. Then, like with $\mathbb{Q}[i]$ from $\mathbb{Z}[i],$ we can construct a field of fractions $\mathbb{Q}[\sqrt{2}]$ from $\mathbb{Z}[\sqrt{2}].$

99. We have $(a + b\sqrt{2}) + (c + d\sqrt{2}) = (a + c) + (b + d)\sqrt{2}$ for addition and $(a + b\sqrt{2})(c + d\sqrt{2}) = (ac + 2bd) + (ad + bc)\sqrt{2}.$

100. The field extension $\mathbb{Q}[\sqrt{2}]: \mathbb{Q}$ has a basis of $\set{1, \sqrt{2}}$ and as such also has a degree of $2.$

101. Let $S$ be a subring of $R$. Then, an element $r \in R$ is *integral over*$S$ if $r$ is the root to a monic polynomial in $S[x].$

102. The set of elements $r$ in $R$ which are integral over $S$ is called the *integral closure* of $S$ in $R.$

103. We can also say that, if every element of $R$ is integral over $S,$then $R$ is an *integral extension* of $S.$

104. Suppose $K$ is the field of fractions of an integral domain $R.$ Then, if the integral closure of $R$ in $K$ is $R$ itself, then $R$ is an *integrally closed domain.*

105. Any unique factorization domain is integrally closed.

106. To illustrate, suppose $R$ is a unique factorization domain, $K = \text{Frac}(R),$ and $k \in K$ is integral over $R.$

107. We can write $k = \frac{a}{b}$ for relatively prime $a,b \in R.$

108. Since $k$ is integral over $R,$ we can write $k^n + c_{n-1}k^{n-1} + {...} + c_0 = 0$ for $c_i \in R.$

109. It follows that we can rewrite this as $\frac{a^n}{b^n} + c_{n-1}\frac{a^{n-1}}{b^{n-1}} + {...} + c_0 = 0,$ then clear denominators and rearrange terms to get $a^n = -b(c_{n-1}a^{n-1} + {...} + c_0 b^{n-1}),$ which means $b$ divides $a^n,$ indicating that $b$ is a unit, since otherwise this would mean either $a$ is not relatively prime to $b$ or unique factorization fails.

110. The fact that unique factorization domains are always integrally closed implies that if the square root of an integer is not an integer, it is not a rational number either.

111. An example of a ring which is not integrally closed is the ring $\mathbb{Z}[\sqrt{5}],$ which one can naturally construct by taking the quotient $\mathbb{Z}[x]/(x^2 - 5).$

112. The field of fractions of $\mathbb{Z}[\sqrt{5}]$ is called the *golden field* $\mathbb{Q}[\sqrt{5}],$where every element can be written $a + b\sqrt{5}$ for $a, b \in \mathbb{Q}.$

113. Since $x^2 - x - 1$ is a polynomial with all coefficients in $\mathbb{Z}[\sqrt{5}],$ but the value $\frac{1}{2} + \frac{1}{2}\sqrt{5}$ (aka, the *golden ratio* $\varphi = \frac{1 + \sqrt{5}}{2}$) is a root of this polynomial, and $\varphi$ is in $\mathbb{Q}[\sqrt{5}]$ but not in $\mathbb{Z}[\sqrt{5}],$ we can say that $\mathbb{Z}[\sqrt{5}]$ is not integrally closed.

114. Suppose an element $r$ is the root of a non-zero polynomial in $K[x]$ for a field $K.$ Then, $r$ is said to be *algebraic over $K.$*

115. Let $L : K$ be a field extension. If every element of $L$ is algebraic over $K[x],$ then $L : K$ is an *algebraic extension.*

116. If $K$ is a field, then the set of all roots of polynomials in $K[x]$ is called the *algebraic closure* of $K.$

117. Suppose $L$ extends the field $K$ and $a \in L.$ If $a$ is algebraic over $K,$ then the *minimal polynomial* of $a$ is the (non-zero) monic polynomial $P$ of lowest degree in $K[x]$ such that $a$ is a root of $P.$

118. For example, the minimal polynomial of $i$ in $\mathbb{Q}$ is $x^2 + 1$ and the minimal polynomial of $\sqrt{2}$ in $\mathbb{Q}$ is $x^2 - 2.$

119. Note that the minimal polynomial of $1 + i$ in $\mathbb{Q}$ is also $x^2 - 2.$

120. A minimal polynomial is always irreducible.

121. That is, if $P = AB$ for non-unit polynomials over a field, then the integral domain property ensures that if $a$ is a root of $P$, then it must be a root of either $A$ or $B.$

122. If an element of a field extension $L : K$ has a minimal polynomial, then that element has only one minimal polynomial.

123. Suppose $r \in L$ has minimal polynomials $M_1, M_2 \in K[x].$

124. Consider the evaluation map $\alpha_r : K[x] \to L$ defined by $\alpha(P) = P(r),$ i.e. sending any $P \in K[x]$ to the value of the polynomial function of $P$ at $r.$

125. Polynomial arithmetic tells us that this map is a ring homomorphism, so the kernel of $\alpha_r$ must be an ideal of $K[x].$

126. By definition, $M_1, M_2 \in \text{ker}(\alpha_r).$

127. Since $K$ is a field, $\text{ker}(\alpha_r)$ must be a principal ideal.

128. So, $M_1$ and $M_2$ must be multiples of the generator of $\text{ker}(\alpha_r).$

129. However, $M_1$ and $M_2$ are both irreducible, so $M_1$ must be an associate of $M_2.$

130. Since $M_1$ and $M_2$ must be monic, $M_1 = M_2.$

131. There is a notion of a *formal derivative* of a polynomial. Given a polynomial of the form $P = a_n x^n + a_{n-1} x^{n-1} + {...} + a_0,$ the formal derivative of $P$ is the polynomial $P' = na_n x^{n-1} + (n-1)a_{n-1}x^{n-2} + {...} + a_1.$

132. If $a, b$ are elements of a ring $R$ and $P, Q \in R[x],$ then $(aP + bQ)' = aP' + bQ'.$

133. The formal derivative of a polynomial which is the product of polynomials satisfies the *product rule,* where $(PQ)' = P'Q + PQ'.$

134. The proof of this is annoying enough that it is left as an exercise for the reader.

135. By the Euclidean algorithm, if $K$ is a field and $P \in K[x],$ then for a root $r$ of $P$ and a non-zero polynomial $Q \in K[x],$ we can write $P$ as a product $P = (x - r)^{m}Q,$ where $m$ is the *multiplicity* of $r$ as a root of $P.$

136. The product rule tells us we can write the formal derivative $P' = m(x-r)^{m-1}Q + (x - r)^m Q.$ If we factor out $(x-r)^{m-1},$ we get a polynomial $A = mQ + (x - r)Q.$

137. Then, we can write $P' = (x - r)^{m-1}A.$

138. So, if and only if a polynomial $P$ has multiple roots $r$ (i.e. if $m > 1$) then the polynomial function $P'(r) = 0.$

139. Consider the polynomial $x^q - x$ in $\mathbb{F}_p[x]$ where $q = p^k$ for some prime $p$ and positive integer $k.$

140. The formal derivative of this polynomial is $qx^{q-1} - 1.$ Since $q$ is a multiple of $p$, $qx^{q-1}$ vanishes modulo $p,$ and we are left with $-1.$

141. Since $-1 \neq 0$, $x^q - x$ has no repeated roots in $\mathbb{F}_p[x].$

142. Then, $x^q - x$ has exactly $q$ roots, so the splitting field of $x^q - x$must contain at least these $q$ elements.

143. Let $K$ be the splitting field of $x^q - x \in \mathbb{F}_p[x].$ By definition, all of the roots of $x^q - x$ are in $K$, so let $R = \set{r \in K \mid r^q = r}$ be that set of $q$ roots.

144. Since $(ab)^q = a^q b^q$ generally, and $q = p^k$ means $(a + b)^q = a^q + b^q,$ $a + b, ab \in R.$

145. Since $(-r)^q = (-1)^q r^q,$ and $(-1)^q = -1,$ $-r \in R.$

146. Since $(r^q)^{-1} = (r^{-1})^q$ and $r^q = r,$ $r^{-1} \in R.$

147. By Fermat's little theorem, $\mathbb{F}_p$ is a subfield of $R.$

148. Since $R$ is a field which includes and $\mathbb{F}_p$ and contains exactly the $q$ roots of $x^q - x,$ it must be the splitting field $K$ of $x^q - x \in \mathbb{F}_p[x].$

149. Since $K$ is a field with $q$ elements, $K \cong \mathbb{F}_q.$
