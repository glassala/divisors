# Permutations

*Permutations. Fixed points and inversions. Transpositions. Cycles. Decomposition into disjoint cycles. Decomposition into transpositions. Sign of a permutation. Symmetric group of degree $n$. Group homomorphisms. Endomorphisms and automorphisms of a group. Group of automorphisms of $\mathbb{Z}/n\mathbb{Z}^+$.*

1. A *permutation* of a set $A$ is a bijective function from $A$ to itself $\sigma: A \to A$.

2. For example, if $A = \set{a, b, c}$, and $\sigma$ is defined by $\sigma(a) = c$, $\sigma(b) = a$, and $\sigma(c) = b$, then $\sigma$ is a permutation on $A$.

3. A permutation is often viewed as a *reordering of a sequence.*

4. That is, $A$ is a set, meaning it does not have an inherent order to its elements.

5. However, one can naturally index its elements by alphabetic order into an ordered sequence $A_1 = a$, $A_2 = b$, $A_3 = c$.

6. Then we can view the image of $\sigma$ as a new sequence $B_1 = c$, $B_2 = a$, $B_3 = b$.

7. That is, $\sigma$ maps the ordered sequence $[a, b, c]$ into the reordered sequence $[c, a, b]$.

8. If $X_i$ is the $i$-th entry in a sequence $X$ and $\sigma$ is a permutation on $X$, then $\sigma$ gives rise to a rearranged sequence $Y$ which contains exactly the elements in $X$, but where $Y_i = \sigma(X_i)$.

9. The number of permutations of an $n$ element set is given by $n!$.

10. This follows from the principles of counting.

11. There is $1$ permutation of a $1$-element set, namely, the identity permutation, and $1! = 1$.

12. The identity permutation is the permutation that doesn't rearrange any elements.

13. Assume a $k$-element set $I$ has $k!$ permutations for an arbitrary $k > 1.$

14. We can write $I$ as a set of indexed elements $I = \set{i_1, i_2, ..., i_k}$.

15. If one adds an element in the sense of $I' = \set{i_1, i_2, ..., i_{k+1}}$, then the set of all permutations of $I'$ can be split into $k+1$ classes, each of which being the set of all permutations with some given element of $I'$ being assigned to an index fixed across classes.

16. It follows that each of these classes is a set of permutations on $k$ variable indices and $1$ fixed index, so each class has $k!$ elements.

17. Since there are $k+1$ classes which each contain $k!$ elements, the number of permutations of $I'$ is given by $(k+1)!$.

18. A *fixed point* of a permutation is an element which is mapped to itself.

19. We will say that a permutation $\sigma$ *fixes* elements which are mapped to themselves, and *moves* elements which are not.

20. An *inversion* is a property of permutations whereby two elements exchange indices.

21. Strictly speaking, if $i$ and $j$ are indices and $\sigma$ is a permutation, then $(i, j)$ are inverted by $\sigma$ if $i < j$ and $\sigma(i) > \sigma(j)$.

22. A permutation which consists of a single inversion at indices $i$and $j$ is called a *transposition*, and can be written $(ij)$.

23. So, if a permutation $(23)$ maps $[1, 2, 3]$ to $[1, 3, 2]$, $1$ is a fixed point but $2$ and $3$ are inverted.

24. A permutation can be written as a not-necessarily-unique composition (which we call a *product*) of transpositions (and fixed points, when needed for clarity), evaluated from right to left.

25. For example, consider the permutation $[a, b, c, d] \to [c, a, b, d]$.

26. One way we can write this is as $(4)(13)(12)$.

27. First, we evaluate $(12)$: we swap the first and second positions to go from $[a, b, c, d] \to [b, a, c, d]$.

28. Second, we evaluate $(13)$: we swap the first and third positions to go from $[b, a, c, d] \to [c, a, b, d]$.

29. Third, we evaluate $(4)$, which is a fixed point, and in this notation, that represents an identity permutation. This is included in the product so as to cover how all indices are mapped.

30. Note how this composition is not commutative in general.

31. Take $(4)(12)(13)$, which evaluates as $[a, b, c, d] \to [c, b, a, d] \to [b, c, a, d]$.

32. A *cyclic* permutation is, roughly, a permutation which maps some subset of indices successively amongst themselves.

33. A cyclic permutation is often simply called a cycle.

34. Given a permutation $\sigma$ of the indexed set $A = \set{i_1, i_2, ..., i_n}$ and some subset $B \subseteq A$ where $B = \set{j_1, j_2, ..., j_m}$, $\sigma$ is a cycle if for all indices $k < m$, where $\sigma(j_k) = j_{k+1}$ and $\sigma(j_m) = j_1$, *and*, elements which are in $A$ but not in $B$ are all fixed points.

35. $\sigma$ is then an $m$-cycle.

36. Fixed points themselves are $1$-cycles: a $1$-cycle is always the identity permutation.

37. Transpositions are plainly $2$-cycles.

38. Notation in the form of $(4)(13)(12)$ with only transpositions and fixed points is a special case of *cycle notation.*

39. For example, the permutation $[a, b, c, d] \to [b, c, a, d]$ can also be written as $(132)$, as a single $3$-cycle, with the fixed point omitted.

40. Likewise, $[a, b, c, d] \to [c, a, b, d]$ can be achieved as easily as $(123).$

41. *Every permutation can be written as a non-unique product of disjoint cycles.*

42. Given a permutation $\sigma$ defined on a finite set $A = \set{i_1, i_2, ..., i_n}$, consider the effects of repeated application of $\sigma$ on a single element.

43. Application of $\sigma$ $k$ times can be written as $\sigma^{k}$, where $\sigma^0$ is the identity permutation.

44. Consider the sequence $C = {i_n, \sigma(i_n), \sigma^2(i_n), \sigma^3(i_n), ...}$.

45. If $\sigma(i_n) = i_n$, then $i_n$ is fixed by $\sigma$.

46. Otherwise, this sequence must still eventually return to $i_n$ because $A$ is finite.

47. It follows from the definition of cycles that the powers of a permutation on a single element form a cycle within $\sigma$, and the sequence in $C$ which repeats is the cycle which $i_n$ belongs to.

48. That is, if we say $\sigma(i_n) = j_1$, then $\sigma^2(i_n) = \sigma(j_1)$, and so on.

49. Given the nature of cycles, this cycle is an $m$-cycle, where $m$ is the smallest power of $\sigma$ such that $\sigma^m(i_n) = i_n$.

50. Consider some element $i_a \in A$, where there exists no power $k$ such that $\sigma^{k}(i_n) = i_a$.

51. We can repeat the process above on the powers of $\sigma^k(i_a)$, and find the cycle which $i_a$ belongs to.

52. Since no power $k$ exists such that $\sigma^{k}(i_n) = i_a$, we can rest assured that this cycle is disjoint from the cycle which $i_n$ belongs to.

53. This is to say that given a permutation $\sigma$ on $A$, we can repeatedly choose an element in $A$, "isolate" the cycle containing that element, and then choose another element in $A$ which has not yet been isolated into a cycle, until we have no more elements in $A$ to choose.

54. Since cycles fix all the elements they don't move, we can decompose $\sigma$ into a product of these disjoint cycles.

55. Moreover, on account of this fixing property, we can say that the composition of disjoint cycles is commutative.

56. The decomposition of a permutation into disjoint cycles gives rise to a notion of *cycle type.*

57. If a permutation $\sigma$ decomposes into disjoint cycles of respective lengths $m_1, m_2, ..., m_k$ where $m_n \ge m_{n+1}$, then we say that $(m_1, m_2, ..., m_k)$ is the *cycle type* of $\sigma$.

58. A cycle of arbitrary length can be written as a product of transpositions.

59. One can decompose a cycle of length $n > 2$.

60. For example, consider the cycle $(123{...}n)$, which sends $[1, 2, 3, {...}, n]$ to $[n, 1, 2, {...},n-1]$. It can be written as $(12)(234{...}n)$.

61. $(234{...}n)$ sends $[1, 2, 3, {...}, n]$ to $[1, n, 2, ..., n-1]$, and then transposing positions $1$ and $2$ with $(12)$ sends $[1, n, 2, ..., n-1]$ to $[n, 1, 2, {...},n-1]$.

62. Similarly, $(234{...}n)$ can be written as $(23)(345{...}n)$, where $(345{...}n)$ sends $[1, 2, 3, {...}, n]$ to $[1, 2, n, ..., n-1]$, and transposing positions $2$ and $3$ sends $[1, 2, n, ..., n-1]$ to $[1, n, 2, ..., n - 1]$, and so on.

63. So, any $n$-cycle $(123{...}n)$ can be written as a product of $n-1$ transpositions in the form $(12)(23)(34)...((n-1)n)$.

64. If $\sigma$ is a permutation, it can be decomposed into a product of disjoint cycles, and each of these cycles can be decomposed into a product of transpositions.

65. The decomposition into transpositions is not unique for a permutation $\sigma$.

66. It follows from the properties of transpositions that an even power of a transposition is always the identity permutation and an odd power of a transposition is always the transposition itself.

67. That is, if $k$ is even, then $(ab)^k = (a)(b)$ and if $k$ is odd, then $(ab)^k = (ab)$.

68. For example, consider $(12)$, which maps $[1, 2] \to [2, 1]$.

69. So, $(12)(12)$ maps $[1, 2] \to [2, 1] \to [1, 2]$, and likewise $(12)(12)(12)(12)$ maps $[1, 2] \to [2, 1] \to [1, 2] \to [2, 1] \to [1, 2]$.

70. Likewise, one can write $(12)$ as $(12)(12)(12)$, or $(12)(12)(12)(12)(12)$ and so on.

71. As such, if $(ij)$ induces an inversion $(i, j)$ in a permutation $\sigma$, then only an odd power of $(ij)$ induces $(i, j)$.

72. This gives rise to a notion of *parity of a permutation,* alternatively called the *sign of a permutation.*

73. The parity of $\sigma$ is the parity of the number of inversions it induces.

74. The parity of $\sigma$ is also the parity of the number of transpositions $\sigma$ decomposes into.

75. Although the decomposition of $\sigma$ into transpositions is not unique, the parity of $\sigma$ is always the same.

76. Consider the effect of a transposition $(ab)$ on the elements $x$ between $a$ and $b$, where $a < b$.

77. For any $x>a, b$ or $x < a, b$, $(ab)$ does not change the number of inversions w/r/t $x$, since $x$ will still be either above or below both $a$ and $b$.

78. Suppose, then, that $a < x < b$. Here, $(ab)$ adds $(a, x)$ and $(x, b)$ as inversions for each $x$, since now $b$ comes before $x$ and $x$ comes before $a$ in position after the swap.

79. The pair $(a, b)$ is also an inversion, so any transposition $(ab)$ inverts $2k + 1$ elements for some $k$, meaning any transposition flips the parity of inversions.

80. If a non-identity permutation $\sigma$ has $k$ transpositions, it straightforwardly takes $k$ transpositions to "undo" $\sigma$.

81. The identity permutation induces an even number of inversions, namely $0$.

82. For example, consider a permutation like $(123)$, mapping $[1, 2, 3] \to [3, 1, 2]$, where $(1, 3)$ and $(2, 3)$ are inversions.

83. It can be broken down into $(12)(23)$, but because any transposition can be "undone," one can write the identity permutation as $(23)(12)(12)(23).$

84. That is, $[1, 2, 3] \to [1, 3, 2] \to [3, 1, 2] \to [1, 3, 2] \to [1, 2, 3]$.

85. Then, by extension, one can also write $(123)$ as $(12)(23)(23)(12)(12)(23).$

86. We can write the parity of a permutation as a sign: if $\sigma$ is even, then we say $\text{sgn}(\sigma) = 1$, and if $\sigma$ is odd, then we say $\text{sgn}(\sigma) = -1$.

87. Since a permutation is a bijection, every permutation has an inverse.

88. That is, if $\iota$ is the identity permutation, then for any permutation $\sigma$, there exists a permutation $\sigma^{-1}$ such that $\sigma \sigma^{-1} = \sigma^{-1} \sigma = \iota$.

89. The inverse $\sigma^{-1}$ of a permutation $\sigma$ always has the same cycle type as $\sigma$.

90. This stems from the fact that for an arbitrary cycle $(abc...z)$, $(abc...z)(zyx...a) = \iota$.

91. That is, the inverse of a cycle is the elements of the cycle in reverse order.

92. So, the disjoint cycle decomposition of $\sigma^{-1}$ consists of cycles of the same length as the cycles in the decomposition of $\sigma.$

93. As such, $\text{sgn}(\sigma) = \text{sgn}(\sigma^{-1})$.

94. Since permutations are bijections from a set to itself, the composition of permutations is particularly nice.

95. First, the composition of two permutations of a set is obviously itself a permutation.

96. Second, permutations are functions, and function composition is associative.

97. That is, if $f, g, h$ are functions of some $x$, then $((f \circ g) \circ h)(x)$ and $(f \circ (g \circ h))(x)$ can both be written as $f(g(h(x)))$.

98. Third, there is an identity permutation $\iota$, which composes with any permutation $\sigma$ such that $\iota \sigma = \sigma \iota = \sigma$.

99. Fourth, since permutations are bijective, any permutation has an inverse.

100. This means that the set of all permutations of a set forms a group under composition.

101. The group of all permutations on an $n$-element set is called the *symmetric group of degree $n$* and is denoted $S_n$.

102. There are symmetric groups for infinite sets, but we really don't need to get into that.

103. Since permutation composition is not in general commutative, $S_n$ is in general non-abelian.

104. The order of $S_n$ is $n!$.

105. A *group homomorphism* is a map from one group to another.

106. Or, one can say it is a map from the elements of the underlying set of one group to the underlying set of another group such that the group structure is preserved through the mapping.

107. The condition for the map $f: G \to H$ to be a homomorphism between groups $(G, *)$ and $(H, \star)$, where $*$ and $\star$ are arbitrary operations, then $f$ has the property that for all $x$, $y$ in $G$, it is the case that $f(x * y) = f(x) \star f(y)$.

108. A group homomorphism maps the identity of $G$ to the identity of $H$ and maps the inverses of elements of $G$ to the inverses of elements of $H$.

109. The function that sends a permutation to its sign is a group homomorphism.

110. It can be equally interpreted as $\text{sgn}: S_n \to \set{1, -1}$ where multiplication is the operation on $\set{1, -1}$ or, alternatively, as $\text{sgn}: S_n \to \mathbb{Z}/2\mathbb{Z}^+.$

111. It satisfies the homomorphism condition because the composition of two even permutations is even, the composition of two odd permutations is even, and the composition of an odd and an even permutation is odd.

112. This matches both addition modulo $2$ and multiplication between elements of $\set{1, -1}$.

113. An isomorphism between groups is a bijective homomorphism.

114. It follows that the map that sends $1$ and $-1$ in $\set{1, -1}^{\times}$ to the $0$and $1$ classes in $\mathbb{Z}/2\mathbb{Z}^+$ respectively is an example of an isomorphism.

115. This isomorphism lets us say that the sign and parity of a permutation are equivalent.

116. An endomorphism $\epsilon : A \to A$ is a group homomorphism from a group to a subgroup of itself.

117. A function $\epsilon: \mathbb{Z}/n\mathbb{Z}^+ \to \mathbb{Z}/n\mathbb{Z}^+$ where for $x \in \mathbb{Z}/n\mathbb{Z}^+$, $\epsilon(x) = 0$ if $x$ is even and $\epsilon(x) = \frac{n}{2}$ if $x$ is odd, is an endomorphism for even $n$.

118. That this function is a well-defined endomorphism exactly for even $n$ leads us to the conclusion that if $n$ is even, $\mathbb{Z}/2\mathbb{Z}^+$ is a subgroup of $\mathbb{Z}/n\mathbb{Z}^+$.

119. An endomorphism which is also an isomorphism is called an *automorphism.*

120. Since an isomorphism is a bijection, one can say that a finite group automorphism is a permutation which preserves group structure.

121. For elements $a, b$ in an additive group $\mathbb{Z}/n\mathbb{Z}^+$, this means that in order for a function $\phi$ to be an automorphism, $\phi(a + b) = \phi(a) + \phi(b)$.

122. Consider the function $\pi_k : \mathbb{Z}/n\mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$, defined on elements $k, x$ as $\pi_k(x) = k + x$.

123. On account of the uniqueness of additive inverses, this function is a permutation of the elements of $\mathbb{Z}/n\mathbb{Z}$, but it is *not* in general an automorphism of the group $\mathbb{Z}/n\mathbb{Z}^+$.

124. To illustrate, suppose for some $\pi_k : \mathbb{Z}/n\mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$, $a$ is non-zero, and $b = -a$.

125. Then, $\pi_k(a + b) = k$.

126. However, $\pi_k(a) = k + a$ and $\pi_k(b) = k + b$, so $\pi_k(a) + \pi_k(b) = 2k$, so $\pi_k$ can only be a homomorphism in the narrow case that $k \equiv 2k \pmod{n}.$

127. Since $\mathbb{Z}/n\mathbb{Z}^+$ is a cyclic group, all of its possible endomorphisms $\epsilon$ are fully determined by where $\epsilon$ sends a generator, along with the requirement that $\epsilon(a + b) = \epsilon(a) + \epsilon(b).$

128. There are $n$ possible values for, e.g. $\epsilon(1)$, and for each possible value of $\epsilon(1)$, there is only $1$ way to map all the other elements in $\mathbb{Z}/n\mathbb{Z}^+$ consistently with the requirement of a group homomorphism, so there are exactly $n$ endomorphisms of $\mathbb{Z}/n\mathbb{Z}^+$.

129. The generators of $\mathbb{Z}/n\mathbb{Z}^+$ are the residue classes which are relatively prime to $n$, and for an endomorphism $\epsilon$ on $\mathbb{Z}/n\mathbb{Z}^+$ to be bijective, $\epsilon$ must send generators to generators.

130. That is, $\epsilon(1)$ must be relatively prime to $n$ in order for $\epsilon$ to be an automorphism.

131. The requirement for a homomorphism defined on $\mathbb{Z}/n\mathbb{Z}^+$, that $\epsilon(a + b) = \epsilon(a) + \epsilon(b)$, describes the distributivity of multiplication over addition.

132. So, the set of all group automorphisms of $\mathbb{Z}/n\mathbb{Z}^+$ is the set of functions in the form $\phi_k(x) = kx$, where $k$ is relatively prime to $n$.

133. As such, there are $\varphi(n)$ automorphisms of the group $\mathbb{Z}/n\mathbb{Z}^+.$

134. The set of automorphisms of a group $G$ is itself a group under composition, denoted by $\text{Aut}(G).$

135. Suppose $a, b \in \mathbb{Z}/n\mathbb{Z}^+$ and both $a$ and $b$ are relatively prime to $n$. Then, the composition of the automorphisms defined by $\phi_a(x)$ and $\phi_b(x)$ for some $x \in \mathbb{Z}/n\mathbb{Z}^+$ takes the form $\phi_a(\phi_b(x)) = \phi_b(\phi_a(x)) =  abx$, and can be written $\phi_{ab}(x) = abx.$

136. It is clear from this that composition of automorphisms of $\mathbb{Z}/n\mathbb{Z}^+$ inherits the group properties of $\mathbb{Z}/n\mathbb{Z}^{\times},$ and we can conclude that $\text{Aut}(\mathbb{Z}/n\mathbb{Z}^+) \cong \mathbb{Z}/n\mathbb{Z}^{\times}$.
