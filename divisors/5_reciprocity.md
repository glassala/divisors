# Reciprocity

*Quadratic residues. Euler's criterion. Legendre symbol. Gauss' lemma for quadratic residues. Zolotarev's lemma. Quadratic reciprocity.*

1. A *quadratic residue* modulo $m$ is an element $n$ of $\mathbb{Z}/m\mathbb{Z}$ where there exists some $k$ such that $k^2 \equiv n \pmod{m}$.

2. Alternatively, a quadratic residue modulo $m$ is some number class $n$ such that the polynomial congruence $k^2 - n \equiv 0 \pmod{m}$ has a solution.

3. Mainly, we will focus on quadratic residues modulo odd primes.

4. Both $0$ and $1$ are quadratic residues modulo $2$.

5. For any $a \in \mathbb{F}_p$, if $a + b \equiv 0 \pmod{p}$, then $a^2 \equiv b^2 \pmod{p}$.

6. The above can be rewritten to $b \equiv -a \pmod{p}$.

7. It is easy to see that $a^2 \pmod{p}$ is a reduction of $(p + a)^2 \pmod{p},$and $b^2 \pmod{p}$ can be written as $(p - a)^2 \pmod{p}$.

8. That is, $(p + a)(p + a)$ can be written as $p^2 + 2pa + a^2$, where only $a^2$ does not vanish modulo $p$.

9. Likewise, $(p - a)(p - a)$ can be written as $p^2 - 2pa + a^2$, where, once again, only $a^2$ does not vanish modulo $p$.

10. Therefore, if $a^2 \equiv n \pmod{p}$, then $-a^2 \equiv n \pmod{p}$.

11. $0$ is a quadratic residue for any modulus, so we can say that the number of unique quadratic residues for an odd prime modulus $p$ is $\frac{p + 1}{2}$.

12. To see why this is the exact number of residues as opposed to the maximum, we can look again at the congruence $a^2 \equiv b^2 \pmod{p}$.

13. Naturally, we can write this as $a^2 - b^2 \equiv 0 \pmod{p}$.

14. By difference of squares factorization, we can rewrite it again as $(a - b)(a + b) \equiv 0 \pmod{p}$, directly indicating that if $a^2 \equiv b^2 \pmod{p}$, then either $a \equiv b \pmod{p}$ or $a \equiv -b \pmod{p}$.

15. There is a congruence called *Euler's criterion* which determines whether or not some $a$ is a quadratic residue for an odd prime modulus $p$ (where $a$ is relatively prime to $p$).

16. If $a^{\frac{p-1}{2}}\equiv 1 \pmod{p}$, then $a$ is a quadratic residue modulo $p$.

17. If $a^{\frac{p-1}{2}}\equiv -1 \pmod{p}$, then $a$ is *not* a quadratic residue modulo $p$.

18. The expression $a^{\frac{p-1}{2}}$ can only be congruent to $1$ or $-1$.

19. Let $g$ be a primitive root of an odd prime modulus $p$. Then, the element $g^{\frac{p-1}{2}}$ is the unique element of order $2$ in $(\mathbb{Z}/p\mathbb{Z})^{\times}$.

20. That is, $g^{\frac{p-1}{2}} \equiv -1 \pmod{p}$.

21. By Euler's theorem, $(g^{\frac{p-1}{2}})^2 \equiv g^{p-1} \equiv 1 \pmod{p}$.

22. However, since $p-1$ is the order of $(\mathbb{Z}/p\mathbb{Z})^{\times}$, $g^{\frac{p-1}{2}}$ is never $g^{p-1}$, meaning $g^{\frac{p-1}{2}}$ is the unique congruence class $-1$ which is not itself $1$ but whose square is $1$.

23. Since $p$ here is an odd prime, $p-1$ must be a positive even number, so $a^{p-1}$ is a perfect square.

24. It follows that we can rewrite $a^{p-1} \equiv 1 \pmod{p}$ as $a^{p-1} - 1 \equiv 0 \pmod{p}$ and apply the difference of squares factorization to get $(a^{\frac{p-1}{2}} - 1)(a^{\frac{p-1}{2}} + 1) \equiv 0 \pmod{p}$.

25. Since either $(a^{\frac{p-1}{2}} - 1)$ or $(a^{\frac{p-1}{2}} + 1)$ must be congruent to $0$, $a^{\frac{p-1}{2}}$ must be congruent to either $1$ or $-1$.

26. If $1$, then $a^{\frac{p-1}{2}} \equiv a^{p-1}$, but if $-1$, then note that there is at least one primitive root $g$ in $(\mathbb{Z}/p\mathbb{Z})^{\times}$ and so $a = g^k$ for some integer $k$.

27. Following from this, $a^{\frac{p-1}{2}} = (g^k)^{\frac{p-1}{2}}$.

28. We can rewrite this to $(g^{\frac{p-1}{2}})^k$.

29. Since $g^{\frac{p-1}{2}} \equiv -1 \pmod{p}$ for any odd prime modulus, Euler's criterion essentially reads the parity of the power to which a primitive root is taken.

30. Since $(a^{n})^2 = a^{n}a^{n}=a^{n+n}$, and the sum of two numbers of the same parity is always even, it follows that if a number is an odd power of a primitive root, there is no other power of a primitive root which can be squared in order to arrive at it.

31. If for a number $a = g^k$, $k$ is even, then that means $k = 2n$ for some $n$-th power of a generator $g^n$, and so $a$ is a quadratic residue.

32. If for a number $a = g^k$, $k$ is odd, then there is no such $n$ for which $k = 2n$, i.e. no $k = g^{n}g^{n} = g^{n+n}$.

33. So, Euler's criterion encodes that some $a$ in $(\mathbb{Z}/p\mathbb{Z})^{\times}$ for odd prime $p$ is a quadratic residue in $a^{\frac{p-1}{2}}\equiv 1 \pmod{p}$ and that some $a$is not a quadratic residue in $a^{\frac{p-1}{2}}\equiv -1 \pmod{p}$.

34. There is a function called the *Legendre symbol* $(\frac{a}{p})$ which maps an integer $a$ and an odd prime $p$ to whichever $k \in \set{-1, 0, 1}$ satisfies $a^{\frac{p-1}{2}} \equiv k \pmod{p}$.

35. Like Euler's criterion, $(\frac{a}{p})$ characterizes quadratic residues modulo $p$, evaluating to $1$ if $a$ is one, $-1$ if not, but is additionally defined to be $0$ if $a$ is a multiple of $p$.

36. It follows immediately from Euler's criterion that the Legendre symbol is *completely multiplicative* w/r/t its top argument.

37. That is, for some fixed odd prime $p$, $(\frac{ab}{p})=(\frac{a}{p})(\frac{b}{p})$.

38. Consider the least residue system modulo $p$, where $p$ is an odd prime.

39. Since $p$ is an odd prime, $p - 1$ is the number of non-zero elements in the least residue system, and $\frac{p-1}{2}$ is always an integer.

40. So we can split the set $\set{1, 2, 3, {...}, p-1}$ in half around $\frac{p}{2}$ into $A = \set{1, 2, 3, {...}, \frac{p-1}{2}}$ and $B = \set{\frac{p+1}{2}, \frac{p+3}{2}, {...}, p-1}$.

41. Given the additive inverse property in modular arithmetic, however, one can also write $B = \set{-1, -2, -3, {...}, -\frac{p-1}{2}}$.

42. It follows that one can define a "modular absolute value" function which assigns values in $A$ to themselves and values in $B$ to their additive inverses.

43. For a non-zero least residue $x$ modulo $p$, we can say that $|x| = x$ for $1 \le x \le \frac{p-1}{2}$ and $|x| = p-x$ for $\frac{p+1}{2} \le x \le p-1$.

44. That is, we interpret elements of $A$ in their positive representation, and elements of $B$ as the "absolute value" of their negative representation.

45. For convenience, we will call the non-zero elements of a least residue system modulo $p$ which are less than or equal to $\frac{p-1}{2}$ as the "$A$-side" of the partition, and the elements which are greater than $\frac{p-1}{2}$ as its "$B$-side."

46. Let $p$ be an odd prime, and let $a$ be relatively prime to $p$.

47. Let $L$ be the subset of the least residue system modulo $p$ formed from $\set{a, 2a, 3a, {...}, \frac{p-1}{2}a}$, and let $n$ be the number of elements in $L$ which are greater than $\frac{p-1}{2}$.

48. Then, $(\frac{a}{p}) = (-1)^n$.

49. This is called *Gauss' lemma.*

50. We can write the product of all the elements in $L$ in multiple ways.

51. Directly, we can say that the product of residues in $L$ amounts to $a^{\frac{p-1}{2}}\frac{p-1}{2}! \pmod{p}$.

52. From the definition of the Legendre symbol, we can write $a^{\frac{p-1}{2}}\frac{p-1}{2}! \pmod{p}$$ as $(\frac{a}{p})\frac{p-1}{2}! \pmod{p}$.

53. Consider the product $(|a||2a||3a|...|\frac{p-1}{2}a|)$.

54. Since $|ra| \equiv |sa| \pmod{p}$ implies that $r = \pm s$, the values in $\set{|a|,|2a|,|3a|,... ,|\frac{p-1}{2}a|}$ are all distinct.

55. Since these values are all distinct and all fall into side $A$, they constitute a permutation of $A$.

56. So, we can write the product of residues in $L$ as $(-1)^n(|a||2a||3a|...|\frac{p-1}{2}a|)$, where $n$ is the number of residues in $L$ which would fall on the "$B$-side" of the partition.

57. We can justify $(-1)^n$ because each $B$-side residue in $L$ constitutes a sign change in the product.

58. Then, since we know that $(|a||2a||3a|...|\frac{p-1}{2}a|)$ is a permutation of $A,$we can write our product as $(-1)^{n}\frac{p-1}{2}!$.

59. So, since we have two ways of writing the same product $(\frac{a}{p})\frac{p-1}{2}! \equiv (-1)^{n}\frac{p-1}{2}! \pmod{p}$, we can cancel the factorials, and write $(\frac{a}{p}) = (-1)^n$.

60. We will call this *Gauss' lemma for quadratic residues.*

61. Let $p$ be an odd prime and let $a$ be relatively prime to $p.$ Then, where $\pi_a(x) \equiv ax \pmod{p}$ is a permutation on $\mathbb{Z}/p\mathbb{Z}^{\times}$, $(\frac{a}{p}) = \text{sgn}(\pi_a)$.

62. First, let $k$ be the order of $a$ in $\mathbb{Z}/p\mathbb{Z}^{\times}.$

63. Then, $\pi_a$ decomposes into $\frac{p-1}{k}$ cycles of length $k$.

64. Let us observe that the sign of a cycle of length $k$ is $(-1)^{k-1}.$

65. Since $\pi_a$ has $\frac{p-1}{k}$ such cycles, $\text{sgn}(\pi_a) = (-1)^{k-1\frac{p-1}{k}}$.

66. We can rewrite $k-1\frac{p-1}{k}$ as $\frac{(k-1)(p-1)}{k}$ then as $\frac{k(p-1)-(p-1)}{k}$, and again as $p-1 - \frac{p-1}{k}$.

67. As such, we can write $(-1)^{p-1 - \frac{p-1}{k}}$ as $(-1)^{p-1}(-1)^{-\frac{p-1}{k}}$.

68. Since $p-1$ is even, we can rewrite the above as simply $(-1)^{-\frac{p-1}{k}}$.

69. Because $(-1)^{-n} = \frac{1}{(-1)^n} = (-1)^n,$ we can say that $\text{sgn}(\pi_a) = (-1)^{\frac{p-1}{k}}.$

70. Since an even number divided by an odd number must be even, if $k$ is odd, then $\text{sgn}(\pi_a) = 1$.

71. Note that since $\gcd(2, k) = 1$, $\text{lcm}(2, k) = 2k$, so $2k \mid p-1$.

72. Recall that $(\frac{a}{p}) \equiv a^{\frac{p-1}{2}} \pmod p$.

73. We can write $a^{\frac{p-1}{2}} = (a^k)^{\frac{p-1}{2k}}$.

74. Since $k$ is the multiplicative order of $a$ modulo $p$, we can rewrite to $1^{\frac{p-1}{2k}} = 1$, so $(\frac{a}{p}) = \text{sgn}(\pi_a)$ where $a$ has odd order.

75. If $k$ is even, we can say that $a^{\frac{k}{2}} \equiv -1 \pmod{p}$, since $x^2 \equiv 1 \pmod{p}$implies that $x \equiv \pm 1 \pmod{p},$ and $\frac{k}{2}$ is less than the order of $a,$ i.e. $a^{\frac{k}{2}}$ can't be congruent to $1$ modulo $p.$

76. Since $k$ is even, we can then write $a^{\frac{p-1}{2}} = (a^{\frac{k}{2}})^{\frac{p-1}{k}} = (-1)^{\frac{p-1}{k}}.$

77. We know that $\text{sgn}(\pi_a) = (-1)^{\frac{p-1}{k}},$ so for both odd and even orders of $a,$ $(\frac{a}{p}) = \text{sgn}(\pi_a).$

78. This is called *Zolotarev's lemma.*

79. Following from this, let $p \neq q$ be odd primes, and let $a \in \mathbb{Z}/q\mathbb{Z}$ and $b \in \mathbb{Z}/p\mathbb{Z}.$ Then, where $\alpha_p(x) \equiv a + px \pmod{q}$ and $\beta_q(x) \equiv b + qx \pmod{p}$ are permutations on $\mathbb{Z}/q\mathbb{Z}$ and $\mathbb{Z}/p\mathbb{Z}$ respectively, $(\frac{p}{q}) = \text{sgn}(\alpha_p)$ and $(\frac{q}{p}) = \text{sgn}(\beta_q).$

80. It suffices to demonstrate this for $(\frac{p}{q}) = \text{sgn}(\alpha_p)$ due to symmetry.

81. Let $\sigma_a$ for some $a \in \mathbb{Z}/q\mathbb{Z}$ be defined as $\sigma_a \equiv a + x \pmod{q}.$ If $a = 0,$ then $\sigma_a$ is the identity permutation and $\text{sgn}(\sigma_a) = 1.$ Otherwise, $\sigma_a$ is a $q$-cycle, and as such decomposes into $q-1$ transpositions, so $\text{sgn}(\sigma_a) = 1.$

82. If we take $\pi_p(x) \equiv px \pmod{q},$ we can see that $\alpha_p$ is a composition of $\sigma_a$ and $\pi_p,$ i.e. $\alpha_p = \sigma_a \pi_p,$ and so $\text{sgn}(\alpha_p) = \text{sgn}(\sigma_a)\text{sgn}(\pi_p).$

83. Since $\text{sgn}(\sigma_a) = 1$, $\text{sgn}(\alpha_p) = \text{sgn}(\pi_p),$ and by Zolotarev's lemma, $\text{sgn}(\alpha_p) = (\frac{p}{q}),$ and by extension, $\text{sgn}(\beta_q) = (\frac{q}{p}).$

84. (...)

85. By Sunzi's theorem, the function $\sigma: \mathbb{Z}/pq\mathbb{Z} \to \mathbb{Z}/p\mathbb{Z} \times \mathbb{Z}/q\mathbb{Z}$ defined as $\sigma(x) = (x, x)$ can be treated as a permutation.

86. We can view it as a map from some $x \bmod{pq}$ to the ordered pair $(x \bmod p, x \bmod q).$

87. $\sigma^{-1}$ can then be said to map the pair $(x \bmod p, x \bmod q)$ to the unique solution that satisfies both modulo $pq.$

88. Consider the function $\lambda : \mathbb{Z}/p\mathbb{Z} \times \mathbb{Z}/q\mathbb{Z} \to \mathbb{Z}/p\mathbb{Z} \times \mathbb{Z}/q\mathbb{Z}$ defined as $\lambda(a, b) = (a, a + pb);$ by Euclid's division lemma this function is well-defined if we consider $a + pb$ a least residue modulo $q.$

89. Likewise, consider $\psi : \mathbb{Z}/p\mathbb{Z} \times \mathbb{Z}/q\mathbb{Z} \to \mathbb{Z}/p\mathbb{Z} \times \mathbb{Z}/q\mathbb{Z},$ defined as $\psi(a, b) = (b + qa, b).$

90. Let us define yet another function $\phi: \mathbb{Z}/pq\mathbb{Z} \to \mathbb{Z}/pq\mathbb{Z}$ where $\phi(a + pb) = qa + b.$

91. Once again, this function is well defined because $a + pb$ and $qa + b$ both correspond to least residues modulo $pq.$

92. Note that, to maintain bijectivity, $a$ must be considered as a least residue modulo $p$ and $b$ as a least residue modulo $q$, because otherwise there would be remainders left from non-unique multiples.

93. Then, $\phi$ = $\sigma^{-1} \circ \psi \circ \lambda^{-1} \circ \sigma.$

94. We can say that $\sigma(a + pb) = (a + pb, a + pb),$ and $\lambda^{-1}(a + pb, a + pb) = \lambda^{-1}(a, a + pb) = (a, b),$ since components of these pairs are treated modulo $p$ and modulo $q$ respectively.

95. Then, $\psi(a, b) = (qa + b, b).$

96. $b \equiv qa + b \pmod q,$ so we can finally write $\sigma^{-1}(qa + b, b) = \sigma^{-1}(qa + b, qa + b) = qa + b,$ and so $\phi(a + pb) = \sigma^{-1}(\psi(\lambda^{-1}(\sigma(a + pb)))) = qa + b.$

97. It follows that $\text{sgn}(\phi) = \text{sgn}(\sigma^{-1})\text{sgn}(\psi)\text{sgn}(\lambda^{-1})\text{sgn}(\sigma),$ and, since permutations share signs with their inverses, $\text{sgn}(\phi) = \text{sgn}(\psi)\text{sgn}(\lambda).$

98. For each $a \in Z/p\mathbb{Z},$ we can restrict $\lambda$ to $\lambda_a: \set{a} \times \mathbb{Z}/q\mathbb{Z}.$

99. Then, by Zolotarev's lemma, $\lambda_a(b) \equiv a + pb \pmod{q}$ is a permutation whose sign equals $(\frac{p}{q}).$

100. The sign of $\lambda_a$ is the same as the sign of unrestricted $\lambda.$

101. Consider that there are $p$ such $\lambda_a$ permutations total, and $\lambda$ is the identity of $a$ in its first position.

102. So, the permutation acting identically on $p$ disjoint subsets of $\mathbb{Z}/p\mathbb{Z} \times \mathbb{Z}/q\mathbb{Z}$ means that we can view $\lambda$ as the $p$-fold composition of some $\lambda_a$ and write $\text{sgn}(\lambda) = (\frac{p}{q})^p,$ so, since $p$ is odd, $\text{sgn}(\lambda) = (\frac{p}{q}).$

103. A similar argument affords the result that $\text{sgn}(\psi)=(\frac{q}{p}),$ and so we can say that because $\text{sgn}(\phi) = \text{sgn}(\lambda)\text{sgn}(\psi),$ $\text{sgn}(\phi) = (\frac{p}{q})(\frac{q}{p}).$

104. We can now look at the sign of $\phi$ from the point of view of its inversions.

105. Recall that a pair $(i, j)$ is an inversion under $\phi$ if $i < j$ and $\phi(j) < \phi(i).$

106. So, if $a_1 + pb_1 < a_2 + pb_2$ and $\phi(a_2 + pb_2) < \phi(a_1 + pb_1),$ then $(a_1 + pb_1, a_2 + pb_2)$ is an inversion under $\phi$.

107. Another way of putting it is that, by the definition of $\phi,$ $(a_1 + pb_1, a_2 + pb_2)$ is an inversion if $a_1 + pb_1 < a_2 + pb_2$ and $b_2 + qa_2 < b_1 + qa_1.$

108. Observe that if $a_1 + pb_1 < a_2 + pb_2$ and $b_2 + qa_2 < b_1 + qa_1,$ then $a_1 - a_2 < p(b_2 - b_1) < pq(a_1 - a_2).$

109. Subtracting $a_2$ and $pb_1$ from both sides of the first inequality yields $a_1 - a_2 < p(b_2 - b_1).$

110. Subtracting $b_1$ and $qa_2$ from both sides of the second inequality yields $b_2 - b_1 < q(a_1 - a_2).$

111. Multiplying both sides by $p$, we get $p(b_2 - b_1) < pq(a_1 - a_2),$ completing the third inequality.

112. Since $a_1 - a_2 < pq(a_1 - a_2)$ and $pq$ is positive, this inequality only holds if $a_1 - a_2 > 0,$ which requires that $b_2 - b_1 > 0,$ i.e. $a_1 > a_2$ and $b_2 > b_1.$

113. Moreover, if it is the case that $a_1 > a_2$ and $b_2 > b_1,$ then $(a_1 + pb_1, a_2 + pb_2)$ is an inversion under $\phi.$

114. That is, the expression $a_1 - a_2 < p(b_2 - b_1)$ leads us back to $a_1 + pb_1 < a_2 + pb_2,$ since we know that $a_1 - a_2$ is at most $p-1$ and $b_2 - b_1$ is positive.

115. A similar argument holds for $b_2 + qa_2 < b_1 + qa_1$ and so $(a_1 + pb_1, a_2 + pb_2)$ is an inversion under $\phi$ if and only if $a_1 > a_2$ and $b_2 > b_1.$

116. So, each inversion induced by $\phi$ is a pair of pairs in the form $(a_1, a_2), (b_1, b_2)$ where $a_1, a_2 \in \mathbb{Z}/p\mathbb{Z}$, $b_1, b_2 \in \mathbb{Z}/q/\mathbb{Z},$ $a_1 > a_2$ and $b_2 > b_1,$ and where $(a_i, a_j)$ and $(a_j, a_i)$ are different only with respect to notation (but not to the inversion count).

117. Since there are $\binom{p}{2}$ such pairs in $\mathbb{Z}/p\mathbb{Z}$ and $\binom{q}{2}$ such pairs in $\mathbb{Z}/q\mathbb{Z},$ by Sunzi's theorem, there are $\binom{p}{2}\binom{q}{2}$ such inversions induced in $\mathbb{Z}/pq\mathbb{Z}$ by $\phi.$

118. Recall that $\binom{n}{2} = \frac{n!}{2!(n-2)!}.$ Because of the divisibility properties of the factorial, we can factor $(n-2)!$ out to get $\frac{n(n-1)}{2}.$

119. So, we can write $\binom{p}{2}\binom{q}{2} = \frac{p(p-1)}{2}\frac{q(q-1)}{2} = p\frac{p-1}{2}q\frac{q-1}{2}.$ Both $p$ and $q$ are odd, so $\binom{p}{2}\binom{q}{2} \equiv \frac{p-1}{2}\frac{q-1}{2} \pmod{2}.$

120. Since $a \equiv b \pmod{2} \implies (-1)^a =(-1)^b,$ we can comfortably write $\text{sgn}(\phi) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}.$

121. Since $\text{sgn}(\phi) = (\frac{p}{q})(\frac{q}{p}),$ we can finally say that $(\frac{p}{q})(\frac{q}{p}) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}$.

122. It follows that $(\frac{p}{q}) = (\frac{q}{p})$ if either $p$ or $q$ is congruent to $1 \pmod{4}$, but $(\frac{p}{q}) = -(\frac{q}{p})$ only if both $p$ and $q$ are congruent to $3 \pmod{4}$.

123. First, let us look at the right side $(-1)^{\frac{p-1}{2}\frac{q-1}{2}}$.

124. Consider that, by virtue of the modulus of $4$ and the denominator of $2$, $\frac{p-1}{2}$ is even when $p \equiv 1 \pmod{4},$ and $\frac{p-1}{2}$ is odd when $p \equiv 3 \pmod{4}$.

125. So, the product $\frac{p-1}{2}\frac{q-1}{2}$ is odd exactly when both $p$ and $q$ are congruent to $3 \pmod{4}$, and even otherwise.

126. If $p$ and $q$ are odd primes, then $(\frac{p}{q})$ and $(\frac{q}{p})$ can only take values of $1$ and $-1$.

127. So, it is exactly when $(\frac{p}{q}) = (\frac{q}{p})$ that $(\frac{p}{q})(\frac{q}{p}) = 1$, and exactly when $(\frac{p}{q}) \neq (\frac{q}{p})$ that $(\frac{p}{q})(\frac{q}{p}) = -1$.

128. That $(\frac{p}{q})(\frac{q}{p}) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}$ for distinct odd primes $p$ and $q$ is called the law of *quadratic reciprocity.*[^1]

## Footnotes

[^1]: I am not sure if these proofs of Zolotarev's lemma and the law of quadratic reciprocity are widely known, but at any rate they are heavily indebted to the proofs at: David Reed (https://math.stackexchange.com/users/444890/david-reed), Zolotarev's Lemma and Quadratic Reciprocity, URL (version: 2025-06-15): https://math.stackexchange.com/q/2529197