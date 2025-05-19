# The language of sets

I am not here to justify set theory. I am here to graciously thank others for doing the hard work of justifying set theory, so that I may use the tools it offers for talking about integers and their divisors.

## A terse primer

1. A set is a collection of elements.
2. An element is an arbitrary object.
3. We write that an element $x$ is in a set $A$ as $x \in A$.
4. If two sets contain the same elements, they are the same set.
5. Any element of a set has an interpretation as a set.
6. For example, any number corresponds to a set given by a particular construction.
7. A *subset* $A$ of a set $B$ can be constructed from an unambiguous property $P$.
8. We write this: $A = \set{x \in B \mid P(x)}$.
9. A calque of this is: $A$ is the set of elements $x$ in $B$ which satisfy the property described by $P$.
10. We write that $A$ is a subset of $B$ as $A \subseteq B$.
11. A set $A$ is a subset of set $B$ if, for all elements $x$ in $A$, $x$ is also in $B$.
12. We write the condition for $A$ to be a subset of $B$: $\forall{x} \in A, x \in B$.
13. A set *contains* its elements. A set *includes* its subsets.
14. Every set is a subset of itself.
15. This property is called the *reflexivity* of inclusion.
16. If $A$ is a subset of $B$ and $B$ is a subset of $A$, then $A=B$.
17. We can write the above as $(A \subseteq B \land B \subseteq A)\implies (A = B)$.
18. This property is called the *antisymmetry* of inclusion.
19. If $A$ is a subset of $B$ and $B$ is a subset of some set $C$, then $A$ is a subset of $C$.
20. We can write the above as $(A \subseteq B \land B \subseteq C)\implies(A \subseteq C)$.
21. This property is called the *transitivity* of inclusion.
22. If, for sets $A$ and $B$, $A$ is a subset of $B$, but $A$ is *not* the same set as $B$, then $A$ is called a *proper* subset of $B$.
23. In symbols, $(A \subseteq B \land A \neq B)\implies(A \subset B)$.
24. There is a set with no elements in it called the empty set.
25. The symbol for the empty set is $\varnothing$.
26. The empty set is a subset of every set.
27. The *cardinality* of a set is how many elements it contains.
28. If $X$ and $Y$ are sets, then there exists a set $Z$ which contains exactly $X$ and $Y$ as elements.
29. We can write the set $Z$ as $Z = \set {X, Y}$.
30. As a consequence (i.e. suppose $X=Y$), if $X$ is a set, then there exists a set $X' = \set{X}$.
31. Let $A$ and $B$ be sets. There exists a set called the *union* of $A$ and $B$ which contains every element which is in $A$ along with every element which is in $B$. The union of $A$ and $B$ is written $A \cup B$.
32. We can describe the union of two sets using set-builder notation: $A \cup B = \set {x \mid x \in A \lor x \in B}$.
33. We can translate this as "the union of $A$ and $B$ is the set of elements $x$, such that $x$ is in $A$ or $x$ is in $B$."
34. Set union is commutative.
35. This means that the order of operands with respect to the operation does not matter.
36. In symbols, $A \cup B = B \cup A$.
37. Set union is associative.
38. This means that the grouping of terms with respect to the operation does not matter.
39. In symbols, $A \cup (B \cup C) = (A \cup B) \cup C$.
40. If a set $X$ is not empty, then it contains an element which itself contains no elements in common with $X$.
41. This is called the Axiom of Foundation.
42. This axiom is insurance against paradoxes.
43. To illustrate, suppose $R \in R$. Since $R$ is a set, we can construct a set $R' = \set{R}$. However, $R'$ and $R$ both contain $R$, and $R$ is the only element of $R'$. As such, the idea that some set could contain itself contradicts the Axiom of Foundation.
44. The set of elements common to two sets $A$ and $B$ is called their *intersection*. We write this $A \cap B = \set{x \mid x \in A \land x \in B}$.
45. Set intersection is commutative and associative.
46. If two sets $A$ and $B$ have no elements in common, i.e. $A \cap B = \varnothing$, then $A$ and $B$ are said to be *disjoint*.
47. The set of elements which are in $A$ and *not* in $B$ is called the *relative complement* of $B$ in $A$.
48. We write this: $A \setminus B = \set{x \mid x \in A \land x \notin B}$.
49. The set of all elements which are in either $A$ or $B$ but *not* both is called the *symmetric difference* of $A$ and $B$.
50. We write this: $A \triangle B = \set {x \mid (x \in A \lor x \in B) \land \lnot (x \in A \land x \in B)}$.
51. This can be "literally translated" as "the symmetric difference of $A$ and $B$ is the set of all elements $x$ such that $x$ is in $A$ *or* $x$ is in $B$ *and* it is *not* the case that $x$ is in $A$  *and* $x$ is in $B$."
52. The symmetric difference is commutative and associative.
53. For any set $S$, there exists a set $P(S)$ called the *power set* of $S$.
54. The *subsets* of $S$ are the *elements* of $P(S)$.
55. If a set $S$ has $n$ elements, then $S$ has $2^n$ subsets. In symbols, $|P(S)| = 2^{|S|}$.
56. A function $f: A \to B$ is a map between sets $A$ and $B$, where each element $a \in A$ has only one $f(a) \in B$.
57. If the source of a function is a set, then the target of a function is a set.
58. If $f: A \to B$ is a function, then $A$ is called the *domain* of $f$ while $B$ is the *codomain* of $f$.
59. If a function $f$ is defined for all elements of a set $A$, then there exists a subset of $B$ called the *image* $C$ of $A$ under $f$ defined as $C = \set{f(x) \mid x \in A}$.
60. Any subset of the domain of $f$ can also be said to have an image under $f$.
61. There is a function of a set called the *successor* function $S(n) = n \cup \set{n}$.
62. If, for sets $n$, $m$, $S(n) = S(m)$, then $n = m$.
63. There is a set $I$ called an *inductive set* such that $\varnothing \in I$ and an element $n$ being in $I$ implies that $S(n)$ is in $I$.
64. If we restrict $I$ such that it *only* has the empty set and its successors, then $I$ is the basis for the counting, or "natural" numbers.
65. One can say that the natural numbers are the labels for the elements of $I$ by cardinality.
66. The arithmetic interpretation of the successor of a natural number $n$ emerges as $S(n) = n + 1$.
67. We write the set of natural numbers $\mathbb{N}$.
68. We assign $0$ to $\varnothing$.
69. We assign $n$ to the $n$-th successor of $S(0)$.
70. This provides a "natural" ordering where $n < S(n)$ and $n < m \land m < k \implies n < k$, and if neither $n < m$ nor $m < n$ then $n = m$.
71. An ordering is not "native" to a set; it must be imposed on it.
72. Any set can have an ordering imposed on it such that each of its non-empty subsets has a minimum element.
73. For any sets $A$ and $B$, there exists the *Cartesian product* $A \times B$, which is the set of ordered pairs $(x,  y)$ such that $x$ is in $A$ and $y$ is in $B$.
74. A *relation* between the elements of a set $A$ and the elements of a set $B$ is a subset of the Cartesian product $A \times B$.
75. For example, if we take the *equality* relation on some set $A = \set{a, b}$, it follows that this relation is fully encapsulated by the subset $E \subseteq A \times A$ where $E = \set{(a, a), (b, b)}$, and inequality is fully encapsulated by the relative complement $(A \times A) \setminus E$.
76. *A function is a special case of a relation.*
77. For any function $f: A \to B$, there is a subset $F$ of the Cartesian product $A \times B$ where, for any $a$ in $A$ and some $b$ and $c \neq b$ in $B$ if a pair $(a, b)$ is in $F$, then there is no pair $(a, c)$ in $F$.
78. That is, pairs in $F$ are unique in the first element, but not necessarily in the second.
79. Consider the identity function on integers (where the set of all integers is written $\mathbb{Z}$) $f: \mathbb{Z} \to \mathbb{Z}$, where $f(n) = n + 0$. Then, $f$ is completely described by the subset $E = \set{(n, n) \in \mathbb{Z} \times \mathbb{Z}}$.
80. This set $E$ makes it clear that the equality relation and the identity function are two perspectives on the same abstraction.
81. Whenever some element $a$ is viewed as being "assigned" to some element $b$, this assignment can also be viewed as a static pair $(a, b)$, and vice versa.
82. A function is *injective* if two different elements in its domain must map to two different elements in its codomain.
83. That is, if for every $a$, $b$ in the domain $A$ of $f$, $a \neq b \implies f(a) \neq f(b)$, or equivalently, $a = b \implies f(a) = f(b)$.
84. A function $f : A \to B$ is *surjective* if its codomain $B$ is the image of $A$.
85. A function $f$ is *bijective* if it is both injective and surjective.
86. A function being bijective is equivalent to it being *invertible*.
87. A bijective function is a one-to-one correspondence between each element of its domain and each element of its codomain.
88. The successor function $s : \mathbb{N} \to \mathbb{N}$ where $s(n) = n + 1$ is injective but it is not surjective, since $0$ is in $\mathbb{N}$ but not in the image of $s$.
89. Any function which is not surjective can be redefined as a surjective function by restricting its codomain to be the same as its image.
90. So, the variant of the successor $s : \mathbb{N} \to \mathbb{N}$ is not bijective, but $s : \mathbb{N} \to \mathbb{Z}^{+}$ is (where $\mathbb{Z}^{+}$ is the set of all *positive* integers), even though both are described by $s(n) = n + 1$.

## On exercises

The methodology of solving exercises (including the trivial methodology of not solving them) is to be treated at the reader's discretion. It is at the very least recommended to read them over and it is gently suggested to give them the old college try. It is not ever out of bounds to look things up. For one, finding the right textbooks is its own exercise. For another, learning how to read Wikipedia pages on math is its own hard-won skill. And if you have the mathematical ability required in order to parse nLab or the like, then this whole text is likely so much babbling of a small child who is only now learning to count. As hard as any given exercise may end up being, trying to write the blasted things to broadly appropriate difficulty levels is surely at least as hard.

## Exercises

1. A function between infinite sets is one of infinitely many rules of element assignment, but a function is fully determined by the assignment of elements from one set to the other, as opposed to the abstract rule. So, a function between finite sets is one of finitely many regimes of element assignment. If $A$ and $B$ are each sets with finitely many elements, how many possible functions are there from $A$ to $B$?
2. Prove that the sum of the first $n$ odd numbers is equal to $n^2$. Hint: *Induction* is one of the most powerful methods for proving things about numbers. Induction takes 3 steps. If one wants to prove P by (weak) induction, first, one proves a base case. For number theory problems, this is usually to prove P holds for 0 or 1. Second, one *assumes* $P$ is true for an arbitrary natural number $k$. This is called an *inductive hypothesis*. Third, one proves that $P$ holding true for $k$ implies that $P$ is also true for $k + 1$. This proves $P$ for all natural numbers.
3. A permutation $\sigma : A \to A$ is a bijective function from a set $A$ to itself. A permutation is often thought about as a rearrangement, since the domain and image are entirely the same, but elements of $A$ are assigned to elements of $A$. If $A$ is a finite set with $n$ elements, how many permutations of $A$ exist?
