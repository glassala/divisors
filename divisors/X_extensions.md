# Field extensions

*Vector spaces and properties of vectors. Linear combinations. Linear dependence and independence. Vector subspaces. Span and basis. Steinitz exchange lemma. Dimension of a vector space. Linear maps. Field extensions. Splitting fields. Adjunctions and simple extensions. Algebraic elements. Minimal polynomials. Formal derivative of a polynomial. Splitting field of $x^q$*

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

52. If $K$ and $L$ are fields such that $K \subseteq L$, then $K$ is a *subfield* of $L$, and $L$ is said to be an *extension* of $K$.

53. If $L$ is an extension of a field $K$, we can write $L : K$, which can be read as "$L$ over $K$."

54. A field which has no proper subfields is called a *prime field.*

55. The archetypal examples are $\mathbb{F}_p$ for prime $p$ and the field of rational numbers $\mathbb{Q}.$

56. If $L$ extends $K,$ then $L$ is a vector space with scalars in $K.$

57. The degree $[L:K]$ of the field extension $L : K$ is the dimension of $L$ considered as a vector space over $K.$

58. For example, $\mathbb{Q}[i]$ is an extension of $\mathbb{Q}.$

59. Every element of $\mathbb{Q}[i]$ can be written as a linear combination of $1$ and $i$ with scalars drawn from $\mathbb{Q}.$

60. That is, one can view $a + bi \in \mathbb{Q}[i]$ as a vector $(a, b),$ and, as such, $\set{1, i}$ is a standard basis for the space $\mathbb{Q}[i].$

61. Then, $[\mathbb{Q}[i]: \mathbb{Q}] = 2.$

62. Given a polynomial $P$ with coefficients in a field $K,$ the *splitting field* of $P$ is the smallest field extension of $K$ in which $P$ factors into a product of linear polynomials.

63. That is, if $L$ is the minimal-degree extension $L : K$ such that a polynomial $P$ in $K[x]$ factors into the product $P(x) = k\prod^{\text{deg}(P)}_{i = 1}(x - a_i)$ for $k \in K$ and $a_i \in L,$ then $L$ is the splitting field of $P.$

64. For example, $\mathbb{Q}[i]$ is the splitting field for $x^2 + 1 \in \mathbb{Q}[x].$

65. Let $L : K$ be a field extension. If $\lambda \in L$ is algebraic over $K,$ then the *adjunction* $K[\lambda]$ of $\lambda$ to $K$ is the set of all linear combinations in the form $a + b\lambda$ for $a, b \in K.$

66. A field extension consisting of a single adjunction $K[\lambda] : K$ is called a *simple* extension.

67. $\mathbb{Q}[i]$ and $\mathbb{Q}[\sqrt{2}]$ are examples of simple extensions.

68. Much like we could construct $\mathbb{Z}[i]$ via the quotient of $\mathbb{Z}[x]$ and the ideal generated by the irreducible polynomial $x^2 + 1,$ we can construct a ring $\mathbb{Z}[x]/(x^2 - 2)$ which is governed by a rule such that $x^2 \equiv 2 \pmod{x^2 - 2}.$

69. In the ring $\mathbb{Z}[x]/(x^2 - 2),$ we can then write every element in the form $q = a + b\sqrt{2}$ for integers $a$ and $b.$

70. As such, we write $\mathbb{Z}[x]/(x^2 - 2)$ as $\mathbb{Z}[\sqrt{2}].$

71. Since $x^2 - 2$ is irreducible in $\mathbb{Z}[x],$ it generates a prime ideal $(x^2 - 2)$ so $\mathbb{Z}[\sqrt{2}]$ is an integral domain.

72. Then, like with $\mathbb{Q}[i]$ from $\mathbb{Z}[i],$ we can construct a field of fractions $\mathbb{Q}[\sqrt{2}]$ from $\mathbb{Z}[\sqrt{2}].$

73. We have $(a + b\sqrt{2}) + (c + d\sqrt{2}) = (a + c) + (b + d)\sqrt{2}$ for addition and $(a + b\sqrt{2})(c + d\sqrt{2}) = (ac + 2bd) + (ad + bc)\sqrt{2}.$

74. The field extension $\mathbb{Q}[\sqrt{2}]: \mathbb{Q}$ has a basis of $\set{1, \sqrt{2}}$ and as such also has a degree of $2.$

75. Suppose an element $r$ is the root of a non-zero polynomial in $K[x]$ for a field $K.$ Then, $r$ is said to be *algebraic over $K.$*

76. Let $L : K$ be a field extension. If every element of $L$ is algebraic over $K[x],$ then $L : K$ is an *algebraic extension.*

77. If $K$ is a field, then the set of all roots of polynomials in $K[x]$ is called the *algebraic closure* of $K.$

78. Suppose $L$ extends the field $K$ and $a \in L.$ If $a$ is algebraic over $K,$ then the *minimal polynomial* of $a$ is the (non-zero) monic polynomial $P$ of lowest degree in $K[x]$ such that $a$ is a root of $P.$

79. For example, the minimal polynomial of $i$ in $\mathbb{Q}$ is $x^2 + 1$ and the minimal polynomial of $\sqrt{2}$ in $\mathbb{Q}$ is $x^2 - 2.$

80. Note that the minimal polynomial of $1 + i$ in $\mathbb{Q}$ is also $x^2 - 2.$

81. A minimal polynomial is always irreducible.

82. That is, if $P = AB$ for non-unit polynomials over a field, then the integral domain property ensures that if $a$ is a root of $P$, then it must be a root of either $A$ or $B.$

83. If an element of a field extension $L : K$ has a minimal polynomial, then that element has only one minimal polynomial.

84. Suppose $r \in L$ has minimal polynomials $M_1, M_2 \in K[x].$

85. Consider the evaluation map $\alpha_r : K[x] \to L$ defined by $\alpha(P) = P(r),$ i.e. sending any $P \in K[x]$ to the value of the polynomial function of $P$ at $r.$

86. Polynomial arithmetic tells us that this map is a ring homomorphism, so the kernel of $\alpha_r$ must be an ideal of $K[x].$

87. By definition, $M_1, M_2 \in \text{ker}(\alpha_r).$

88. Since $K$ is a field, $\text{ker}(\alpha_r)$ must be a principal ideal.

89. So, $M_1$ and $M_2$ must be multiples of the generator of $\text{ker}(\alpha_r).$

90. However, $M_1$ and $M_2$ are both irreducible, so $M_1$ must be an associate of $M_2.$

91. Since $M_1$ and $M_2$ must be monic, $M_1 = M_2.$

92. There is a notion of a *formal derivative* of a polynomial. Given a polynomial of the form $P = a_n x^n + a_{n-1} x^{n-1} + {...} + a_0,$ the formal derivative of $P$ is the polynomial $P' = na_n x^{n-1} + (n-1)a_{n-1}x^{n-2} + {...} + a_1.$

93. If $a, b$ are elements of a ring $R$ and $P, Q \in R[x],$ then $(aP + bQ)' = aP' + bQ'.$

94. The formal derivative of a polynomial which is the product of polynomials satisfies the *product rule,* where $(PQ)' = P'Q + PQ'.$

95. The proof of this is annoying enough that it is left as an exercise for the reader.

96. By the Euclidean algorithm, if $K$ is a field and $P \in K[x],$ then for a root $r$ of $P$ and a non-zero polynomial $Q \in K[x],$ we can write $P$ as a product $P = (x - r)^{m}Q,$ where $m$ is the *multiplicity* of $r$ as a root of $P.$

97. The product rule tells us we can write the formal derivative $P' = m(x-r)^{m-1}Q + (x - r)^m Q.$ If we factor out $(x-r)^{m-1}$ we get a polynomial $A = mQ + (x - r)Q.$

98. Then, we can write $P' = (x - r)^{m-1}A.$

99. So, if and only if a polynomial $P$ has multiple roots $r$ (i.e. if $m > 1$) then the polynomial function $P'(r) = 0.$

100. Consider the polynomial $x^q - x$ in $\mathbb{F}_p[x]$ where $q = p^k$ for some prime $p$ and positive integer $k.$

101. The formal derivative of this polynomial is $qx^{q-1} - 1.$ Since $q$ is a multiple of $p$, $qx^{q-1}$ vanishes modulo $p,$ and we are left with $-1.$

102. Since $-1 \neq 0$, $x^q - x$ has no repeated roots in $\mathbb{F}_p[x].$

103. Then, $x^q - x$ has exactly $q$ roots, so the splitting field of $x^q - x$must contain at least these $q$ elements.

104. Let $K$ be the splitting field of $x^q - x \in \mathbb{F}_p[x].$ By definition, all of the roots of $x^q - x$ are in $K$, so let $R = \set{r \in K \mid r^q = r}$ be that set of $q$ roots.

105. Since $(ab)^q = a^q b^q$ generally, and $q = p^k$ means $(a + b)^q = a^q + b^q,$ $a + b, ab \in R.$

106. Since $(-r)^q = (-1)^q r^q,$ and $(-1)^q = -1,$ $-r \in R.$

107. Since $(r^q)^{-1} = (r^{-1})^q$ and $r^q = r,$ $r^{-1} \in R.$

108. By Fermat's little theorem, $\mathbb{F}_p$ is a subfield of $R.$

109. Since $R$ is a field which includes and $\mathbb{F}_p$ and contains exactly the $q$ roots of $x^q - x,$ it must be the splitting field $K$ of $x^q - x \in \mathbb{F}_p[x].$

110. Since $K$ is a field with $q$ elements, $K \cong \mathbb{F}_q.$
