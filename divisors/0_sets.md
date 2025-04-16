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
27. The *cardinality* of the empty set is 0.
28. The cardinality of a set is how many elements it contains.
29. If $X$ and $Y$ are sets, then there exists a set $Z$ which contains exactly $X$ and $Y$ as elements.
30. We can write the set $Z$ as $Z = \set {X, Y}$.
31. As a consequence (i.e. suppose $X=Y$), if $X$ is a set, then there exists a set $X' = \set{X}$.
32. Let $A$ and $B$ be sets. There exists a set called the *union* of $A$ and $B$ which contains every element which is in $A$ along with every element which is in $B$. The union of $A$ and $B$ is written $A \cup B$. 
33. We can describe the union of two sets using set-builder notation: $A \cup B = \set {x \mid x \in A \lor x \in B}$.
34. We can translate this as "the union of $A$ and $B$ is the set of elements $x$, such that $x$ is in $A$ or $x$ is in $B$."
35. Set union is commutative.
36. This means that the order of operands with respect to the operation does not matter.
37. In symbols, $A \cup B = B \cup A$.
38. Set union is associative.
39. This means that the grouping of terms with respect to the operation does not matter.
40. In symbols, $A \cup (B \cup C) = (A \cup B) \cup C$.
41. If a set $X$ is not empty, then it contains an element which itself contains no elements in common with $X$.
42. This is called the Axiom of Foundation.
43. This axiom is insurance against paradoxes.
44. To illustrate, suppose $R \in R$. Since $R$ is a set, we can construct a set $R' = \set{R}$. However, $R'$ and $R$ both contain $R$, and $R$ is the only element of $R'$. As such, the idea that some set could contain itself contradicts the Axiom of Foundation.
45. The set of elements common to two sets $A$ and $B$ is called their *intersection*. We write this $A \cap B = \set{x \mid x \in A \land x \in B}$.
46. Set intersection is commutative and associative.
47. The set of elements which are in $A$ and *not* in $B$ is called the *relative complement* of $B$ in $A$.
48. We write this: $A \setminus B = \set{x \mid x \in A \land x \notin B}$.
49. The set of all elements which are in either $A$ or $B$ but *not* both is called the *symmetric difference* of $A$ and $B$.
50. We write this: $A \triangle B = \set {x \mid (x \in A \lor x \in B) \land \lnot (x \in A \land x \in B)}$.
51. This can be "literally translated" as "the symmetric difference of $A$ and $B$ is the set of all elements $x$ such that $x$ is in $A$ *or* $x$ is in $B$ *and* it is *not* the case that $x$ is in $A$  *and* $x$ is in $B$."
52. The symmetric difference is commutative and associative.
53. For any set $S$, there exists a set $P(S)$ called the *power set* of $S$.
54. The *subsets* of $S$ are the *elements* of $P(S)$.
55. If a set $S$ has $n$ elements, then $S$ has $2^n$ subsets.
56. In symbols, $|P(S)| = 2^{|S|}$.
57. If the source of a function is a set, then the target of a function is a set.
58. One can also say that if a function $f$ is defined for all elements of a set $A$, then there exists a set $B = \set{f(x) \mid x \in A}$.
59. This set $B$ is called the *image* of $A$ under $f$, where $A$ is the *domain* of $f$.
60. There is a function of a set called the *successor* function $S(n) = n \cup \set{n}$.
61. If, for sets $n$, $m$, $S(n) = S(m)$, then $n = m$.
62. There is a set $I$ such that $\varnothing \in I$ and an element $n$ being in $I$ implies that $S(n)$ is in $I$.
63. If we restrict $I$ such that it *only* has the empty set and its successors, then $I$ is the basis for the counting, or "natural" numbers.
64. One can say that the natural numbers are the labels for the elements of $I$ by cardinality.
65. The arithmetic interpretation of the successor of a natural number $n$ emerges as $S(n) = n + 1$.
66. We write the set of natural numbers $\mathbb{N}$.
67. We assign $0$ to $\varnothing$.
68. We assign $n$ to the $n$-th successor of $S(0)$.
69. This provides a "natural" ordering where $n < S(n)$ and $n < m \land m < k \implies n < k$, and if neither $n < m$ nor $m < n$ then $n = m$.
70. An ordering is not "native" to a set; it must be imposed on it.
71. Any set can have an ordering imposed on it such that each of its non-empty subsets has a minimum element.
72. For any sets $A$ and $B$, there exists the *Cartesian product* $A \times B$, which is the set of ordered pairs $(x,  y)$ such that $x$ is in $A$ and $y$ is in $B$.
