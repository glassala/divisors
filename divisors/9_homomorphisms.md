# Ring homomorphisms

*Ring homomorphisms. Embeddings. Quotient maps. Kernel and image. First isomorphism theorem. Sunzi's theorem for rings. Second and third isomorphism theorems. Characteristic of a ring. Frobenius endomorphism. Fields with eight and twenty-seven elements.*

1. A *homomorphism* is a map from one instance of a structure to another.

2. That is, a homomorphism is a function between sets which preserves a given sort of structure over those sets.

3. If $R$ and $S$ are rings, then $\phi: R \to S$ is a *ring homomorphism* if, for all $a, b \in R$, certain conditions hold.

4. First, $\phi(a + b) = \phi(a) + \phi(b)$.

5. Second, $\phi(ab) = \phi(a)\phi(b)$.

6. Third, $\phi(1_R) = 1_S$.

7. An *inclusion map* is a function between sets $\iota : A \to B$ where $A \subseteq B$ and $\iota(x) = x.$

8. We can also call $\iota$ the *canonical injection* of $A$ into $B.$

9. A canonical injection between sets $A$ and $B$ can only be bijective if $A = B,$ because of the antisymmetry of set inclusion.

10. Not all maps between rings are ring homomorphisms.

11. Suppose there is a map $\iota : \mathbb{Z}/n\mathbb{Z} \to \mathbb{Z}$, which maps each class in $\mathbb{Z}/n\mathbb{Z}$ to its smallest non-negative representative in $\mathbb{Z}$.

12. This map is injective, because each such representative is a unique integer, but it is *not* a ring homomorphism unless $n = 0$, because the wrap-around property of $\mathbb{Z}/n\mathbb{Z}$ is lost.

13. Consider the product $(n - 1)(n - 1)$. We know that this product is always congruent to $1 \pmod{n}$, because $(n - 1)(n - 1) = n^2 - 2n + 1$, and $n^2$ and $-2n$ both vanish modulo $n$, so this property only holds for exactly $n = 0$ and $n = 2$.

14. For $n = 2$, consider that $1 + 1 = 2$, but $2 \equiv 0 \pmod{2}$.

15. So, ring structure is not preserved.

16. An *embedding* $\phi: A \hookrightarrow B$ of a structure $A$ in a structure $B$ is an injective map from $A$ to $B$ which preserves the structure of $A$ as a substructure of $B$.

17. Any injective map which preserves algebraic structure is an embedding.

18. A natural embedding is the ring homomorphism $\phi : \mathbb{Z} \hookrightarrow \mathbb{Q}$ where $\phi(n) = \frac{n}{1}$.

19. That fractions are fundamentally equivalence classes for which the reduced forms are simply the most natural representatives means that $\psi : \mathbb{Z} \hookrightarrow \mathbb{Q}$ where $\psi(n) = \frac{kn}{k}$ for some $k \in \mathbb{Z}$ defines the same map as $\phi.$

20. Likewise, the function $\phi: \mathbb{Z} \to \mathbb{Z}[i]$ defined by $\phi(n) = n$ is an injective ring homomorphism and therefore an embedding.

21. Let $X$ be a set and let $S$ be an equivalence relation. Then $\kappa: X \to X/S$ is the *quotient map* which maps each element of $X$ to the equivalence class in $X/S$ which contains it.

22. We can also call $\kappa$ the *canonical surjection* of $X$ onto $X/S.$

23. By the definition of a quotient ring, if $R$ is a commutative ring and $I$ is an ideal of $R,$ then the map $\kappa : R \to R/I$ where $\kappa(x) = [x]$ is a ring homomorphism.

24. The *kernel* of a ring homomorphism $\phi : A \to B$ is the set $\text{ker}(\phi)$ of all elements $x$ in $A$ such that $\phi(x) = 0_B.$

25. The *image* of a ring homomorphism $\phi : A \to B$ is the set $\text{im}(\phi) = \set {\phi(a) \mid a \in A}.$

26. The kernel of a homomorphism between commutative rings $\phi : R \to S$ is an ideal of $R.$

27. Suppose $a$ and $b$ are in the kernel of $\phi,$ so $\phi(a) = \phi(b) = 0_S.$ Then, $\phi(a + b) = \phi(a) + \phi(b),$ meaning $a + b$ is also in $\text{ker}(\phi).$ Similarly, if $a$ is in $\text{ker}(\phi),$ then so is $-a.$ Obviously $0_R$ is in the kernel of $\phi,$ so $\text{ker}(\phi)$ is an additive subgroup of $R$.

28. Likewise, if $a \in \text{ker}(\phi),$ then $\phi(a) = 0_S,$ so for all $r \in R,$ $\phi(ra) = \phi(r)0_S = 0_S,$ and $ra \in \text{ker}(\phi),$ meaning $\text{ker}(\phi)$ is an ideal of $R.$

29. It follows from definitions that the image of a ring homomorphism $\phi : R \to S$ is a subring of $S.$

30. Let $\phi : R \to S$ be a ring homomorphism. Then, $R/\text{ker}(\phi) \cong \text{im}(\phi).$

31. By virtue of the kernel, one can construct an *induced map* $\mu : R/\text{ker}(\phi) \to \text{im}(\phi)$ where $\mu(r + \text{ker}(\phi)) = \phi(r)$ for all $r \in R$.

32. $R/\text{ker}(\phi)$ is the set of congruence classes where for $r, r' \in R$, $r \sim r'$if $r' = r + k$ for some $k$ in $\text{ker}(\phi)$.

33. Since $\phi$ maps all $k \in \text{ker}(\phi)$ to $0_S$, the value of $\phi(r)$ fully determines the value of $\mu(r + \text{ker}(\phi))$.

34. That is, if $r + \text{ker}(\phi) = r' + \text{ker}(\phi)$, then $\mu(r + \text{ker}(\phi)) = \mu(r' + \text{ker}(\phi))$.

35. The product in $R/\text{ker}(\phi)$ is $rr' + \text{ker}(\phi) = (r + \text{ker}(\phi))(r' + \text{ker}(\phi))$.

36. That is, $\phi(rr') = \phi(r)\phi(r') = \mu(rr' + \text{ker}(\phi)) = \mu(r + \text{ker}(\phi))\mu(r' + \text{ker}(\phi)),$ meaning $\mu$ is a ring homomorphism.

37. If $\mu(r + \text{ker}(\phi)) = 0_S$, then $\phi(r) = 0_S,$ meaning $r \in \text{ker}(\phi)$.

38. So, $r + \text{ker}(\phi) = \text{ker}(\phi)$, i.e $\text{ker}(\mu) = \set{0_{R/\text{ker}(\phi)}},$ meaning the induced map $\mu$ is injective.

39. Since $\mu$ is surjective by definition, it is an isomorphism, and $R/\text{ker}(\phi) \cong \text{im}(\phi)$ holds.

40. This is called the *first isomorphism theorem* for rings.

41. Let $R$ and $S$ be rings, and let $r_i \in R$ and $s_j \in S$. Then, the Cartesian product $R \times S$ is a ring whose operations are $(r_1, s_1) + (r_2, s_2) = (r_1 + r_2, s_1 + s_2)$ and $(r_1, s_1)(r_2, s_2) = (r_1r_2, s_1s_2).$

42. The ring $R \times S$ is called the *direct product* of $R$ and $S.$

43. Ideals also have a notion of product.

44. Let $I$ and $J$ be ideals of a ring $R.$ Then the product of $I$ and $J$ $IJ = \set{\sum_{i=1}^{n}a_ib_i \mid a_i \in I, b_i \in J, n \in \mathbb{N}}.$

45. That is, $IJ$ contains all products of elements in $I$ by elements in $J.$ If $I$ and $J$ are each generated by finitely many elements $I' = \set{a_1, a_2, {...}, a_n}$ and $J' = \set{b_1, b_2, {...}, b_m},$ then the generators of $IJ$ are all in the form $a_ib_j$ for some $(a_i, b_j)$ in the Cartesian product $I' \times J.$

46. Let $I$ and $J$ be ideals of a ring $R.$ If $I + J = (1),$ then $I$ and $J$ are said to be *relatively maximal* ideals of $R.$

47. If $I$ and $J$ are relatively maximal, then $IJ = I \cap J.$

48. First, it is always the case that $IJ \subseteq I \cap J.$

49. That is, each element of $IJ$ is a product in the form $ab$ for some $a \in I$ and $b \in J,$ and, since $I$ and $J$ are ideals, i.e. since $a, b \in R,$ it must be the case that $ab \in I$ and $ab \in J,$ so $IJ$ is a subset of $I \cap J.$

50. Likewise, since $I$ and $J$ are relatively maximal, there must exist $x \in I$ and $y \in J$ such that $x + y = 1.$

51. So, let $z \in I \cap J.$ Since $x + y = 1,$ we can write $z = z(x + y) = zx + zy,$ and, since $z$ is in both $I$ and $J,$ $zx \in IJ$ and $zy \in IJ,$ so $z \in IJ.$

52. Let $R$ be a ring with relatively maximal ideals $I, J.$

53. For $r \in R,$ we can define the ring homomorphism $\pi : R \to R/I \times R/J$ by $\pi(r) = (r + I, r + J).$

54. Since $I + J = (1),$ there exist $x$ in $I$ and $y$ in $J$ such that $x + y = 1.$

55. For any $(a + I, b + J) \in R/I \times R/J,$ we can then set some $r \in R$ as $r = ay + bx.$

56. Since $x \in I,$ we can say $r \equiv ay \pmod{I},$ and, since $y = 1 - x,$ $r \equiv a \pmod I.$

57. Likewise, since $y \in J,$ we can say that $r \equiv bx \pmod{J},$ and, since $x = 1 - y,$ $r \equiv b \pmod J.$

58. As such, $\pi$ is surjective, so $\text{im}(\pi) = R/I \times R/J.$

59. It follows from the properties of ideals that $\text{ker}(\pi) = I \cap J.$

60. So, by the first isomorphism theorem, we can say that $R/(I \cap J) \cong R/I \times R/J.$

61. This is a generalization of Sunzi's theorem to rings.

62. A natural consequence of this is that if $n, m$ are relatively prime positive integers, then $\mathbb{Z}/nm\mathbb{Z} \cong \mathbb{Z}/n\mathbb{Z} \times \mathbb{Z}/m\mathbb{Z}.$

63. Let $R$ be a ring, where $S$ is a subring of $R$ and $I$ is an ideal of $R.$ Then, $S + I = \set{s + a \mid s \in S, a \in I}$ is a subring of $R.$

64. Suppose $s_i \in S$ and $a_j \in I.$ Then, $(s_1 + a_1) + (s_2 + a_2) = (s_1 + s_2) + (a_1 + a_2),$ i.e. $S + I$ is closed under addition.

65. Moreover, $(s_1 + a_1)(s_2 + a_2) = s_1s_2 + s_1a_2 + a_1s_2 + a_1a_2.$ Since $s_1s_2$ is in $S$ and $s_1a_2, a_1s_2, a_1a_2 \in I,$ $S + I$ is closed under multiplication. Obviously, $0 \in S \cap I,$ so $S + I$ is a subring of $R.$

66. For any $s + a \in S + I$ and $b \in I,$ $(s + a)b \in I$ since $sb$ and $ab$ are each in $I.$ So, we can say that $I$ is also an ideal of $S + I.$[^1]

67. Via the definitions of subrings and ideals, $S \cap I$ is an ideal of $S.$

68. That is, if $a, b \in S \cap I,$ then $a,b \in S$ and $a, b \in I,$ so $a + b \in S \cap I$ and $-a \in S \cap I.$

69. Furthermore, if $s \in S,$ then both $S$ and $I$ contain every element of the form $sa,$ so $sa \in S \cap I.$

70. We can take the canonical surjection $\kappa : S \to (S + I )/ I$ where $\kappa(s) = s + I.$

71. By the properties of quotient rings, $\kappa$ is a homomorphism, and it is surjective since if we take each element of $S + I$ to be $s + a$ for $s \in S$ and $a \in I,$ then, since $a \in I,$ $a + I = 0 + I,$ so $(s + a) + I = s + I.$

72. It follows that the kernel of $\kappa$ is the set of all elements in both $S$ and $I$, so $\text{ker}(\kappa) = S \cap I.$

73. By the first isomorphism theorem, then, $S / (S \cap I) \cong (S + I)/I.$

74. This statement is called the *second isomorphism theorem* for rings.

75. Let $R$ be a ring and let $I$ and $J$ be ideals of $R$ such that $I \subseteq J \subseteq R.$ Then, $J/I$ is an ideal of $R/I$ and $(R/I)/(J/I) \cong R/J.$

76. Since $I$ is a subset of $J,$ we can write $J/I = \set{j + I \mid j \in J},$ so $J/I \subseteq R/I.$

77. Let $a + I, b + I \in J/I.$ Since $J$ is an ideal, $(a + b) + I \in J/I$ and $0 + I \in J/I.$

78. Let $r + I \in R/I$ and $s + I \in J / I.$ Since J is an ideal, $(r + I)(s + I) \in J / I.$ So, $J/I$ is an ideal of $R/I.$

79. Let $\pi : R/I \to R/J$ be the ring homomorphism defined as $\pi(r + I) = r + J.$

80. Since $I \subseteq J,$ $\pi$ is surjective.

81. Since $\pi$ can be thought to "hand off" a coset by one ideal to a coset by another, it plainly preserves the ring operations.

82. That is, for elements $a, b \in R,$ $\pi((a + I) + (b + I)) = \pi((a + b) + I)) = (a + b) + J,$ and likewise $\pi(a + I) + \pi(b + I) = (a + J) + (b + J) = (a + b) + J.$

83. Similarly, $\pi((a + I)(b + I)) = \pi(ab + I) = ab + J$ and $\pi(a + I)\pi(b + I) = (a + J)(b + J) = ab + J.$

84. The kernel of $\pi$ is the set $\text{ker}(\pi)=\set{r \in R \mid r \in J}$ which is exactly the ideal $J/I.$

85. Since $\pi$ is surjective and $\text{im}(\pi) = \set{r + J \mid r \in R},$ i.e. $\text{im}(\pi) = R/J,$ then via the first isomorphism theorem, we can conclude that $(R/I)/(J/I) \cong R/J.$

86. This is called the *third isomorphism theorem* for rings.

87. The *characteristic* of a ring $R$ is the number $\text{char}(R) = n$ such that $\sum_{i=1}^{n}1 = 0,$ if such a value exists. If no such $n$ exists, then $\text{char}(R) = 0.$

88. For example, if $p^k$ is the $k$-th power of a prime number, then $\text{char}(\mathbb{F}_{p^k}) = p.$

89. Consider that $\mathbb{F}_{p^k}$ for $k > 1$ arises out of a quotient of $\mathbb{F}_{p}[x]$ by a (maximal) ideal generated by an irreducible polynomial of degree $k.$

90. So, while, for each increment in $k,$ the order of $\mathbb{F}_{p^k}$ increases, this is because each element of $\mathbb{F}_{p^{k+1}}$ has an additional "polynomial term" over the elements of $\mathbb{F}_{p^k},$ and the characteristic of a finite field can be seen as only caring about its "constant term."

91. Let $F$ be a ring of characteristic $p,$ where $p$ is prime. The *Frobenius endomorphism* $\phi : F \to F$ is a map defined such that $\phi(a) = a^p.$

92. By the binomial theorem, $(x + y)^p = x^p + y^p$ holds for a field of prime characteristic $p.$

93. Since $(xy)^p = x^py^p$ and $1^p = 1,$ the Frobenius endomorphism is a ring homomorphism.

94. By Fermat's little theorem, if $p$ is prime, then the Frobenius endomorphism is the identity function on $\mathbb{F}_p.$

95. The Frobenius endomorphism $\phi$ is always an automorphism on finite fields.

96. A finite field, being a field, has only the zero and unit ideals. So, $\text{ker}(\phi) = (0).$

97. Since the kernel of $\phi$ contains only $0,$ $\phi$ is injective.

98. It follows from Dirichlet's box principle that if a function from a finite set to itself is injective, it must be surjective.

99. That is, if $p$ objects each require a unique box, then there must be at least $p$ available boxes.

100. Therefore, $\phi$ is an automorphism when defined on a finite field.

101. Let $p$ be an odd prime. Then, because there are always $\frac{p-1}{2}$ quadratic non-residues modulo $p,$ there always exists at least one irreducible polynomial in the form $x^2 - n$ for some $n \in \mathbb{F}_p.$

102. Then, if we construct $\mathbb{F}_{p^2}$ via $\mathbb{F}_p[x]/(x^2 - n)$ for a quadratic non-residue $n$ and designate $\omega$ as the symbol defined such that $\omega^2 = n,$ we can write every element of $\mathbb{F}_{p^2}$ as $a + b\omega$ for some $a, b \in \mathbb{F}_p.$

103. Consider the quotient ring $\mathbb{F}_2[x]/(x^3 + x + 1).$ Since $x^3 + x + 1$ is irreducible in $\mathbb{F}_2[x],$ this quotient ring is a field.

104. On account of the Euclidean algorithm and the fact that if $p$ is prime and $Q$ is an irreducible polynomial, then the order of $\mathbb{F}_p[x]/(Q)$ is $p^{\text{deg}(Q)},$ the field $\mathbb{F}_2[x]/(x^3 + x + 1)$ has $8$ elements, and we write $\mathbb{F}_2[x]/(x^3 + x + 1) \cong \mathbb{F}_8.$

105. It then follows that every element of $\mathbb{F}_8$ can be written in the form $a + b\gamma + c\gamma^2$ for $a, b, c \in \mathbb{F}_2$ and where $\gamma^3 = \gamma + 1,$ once again, because $x + 1 \equiv x - 1 \pmod{2}.$

106. Likewise, $x^3 - x - 1$ is irreducible modulo $3,$ so we can construct the field with $27$ elements in an all but identical way, in that $\mathbb{F}_3[x]/(x^3 - x - 1) \cong \mathbb{F}_{27},$ and every element in $\mathbb{F}_{27}$ can be written as $a + b\gamma + c\gamma^2$ for $a, b, c \in \mathbb{F}_3$ and where $\gamma^3 = \gamma + 1.$

107. We can compute the Frobenius automorphism for elements in this form: by the freshman's dream property, we can apply the exponents directly as opposed to doing tedious multiplication: $(a + b\gamma + c\gamma^2)^3 = a^3 + b^3 \gamma^3 + c^3\gamma^6 = a + b \gamma^3 + c\gamma^6.$

108. We can then apply the reduction rule to our "formal cube roots" such that $b\gamma^3 = b(\gamma + 1) = b\gamma + b$ and $c\gamma^6 = c\gamma^3(\gamma + 1) = c\gamma^4 + c\gamma^3 = c\gamma(\gamma + 1) + c(\gamma + 1) = c\gamma^2 + c\gamma + c\gamma + c.$

109. Rearranging and combining terms, we are left with an element in the form $(a + b + c) + (b + 2c)\gamma + c\gamma^2.$

110. Where $q = p^k$ for a prime $p$ and positive integer $k,$ the elements of $\mathbb{F}_q$ which are fixed by the Frobenius automorphism are exactly the $p$ elements of $\mathbb{F}_p \cap \mathbb{F}_q.$
