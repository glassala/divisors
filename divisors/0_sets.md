# 0 - Sets

*A brief primer on the language of sets.*

## 1.

*Elements and subsets of sets. Basic properties of sets.*

1. A set is a collection of elements.

2. An element is an arbitrary object.

3. We write that an element $x$ is in a set $A$ as $x \in A$.

4. If two sets contain the same elements, they are the same set.

5. Any element of a set has an interpretation as a set.

6. For example, any number corresponds to a set given by a particular construction.

7. A *subset* $A$ of a set $B$ can be constructed from an unambiguous property $P$.

8. We write this: $A = \set{x \in B \mid P(x)}$.

9.  A calque of this is: $A$ is the set of elements $x$ in $B$ which satisfy the property described by $P$.

10. We write that $A$ is a subset of $B$ as $A \subseteq B$.

11. A set $A$ is a subset of set $B$ if, for all elements $x$ in $A$, $x$ is also in $B$.

12. We write the condition for $A$ to be a subset of $B$: $\forall{x} \in A, x \in B$.

13. A set *contains* its elements. A set *includes* its subsets.

14. Every set is a subset of itself.

15. This property is called the *reflexivity* of inclusion.

16. If $A$ is a subset of $B$ and $B$ is a subset of $A$, then $A=B.$

17. We can write the above as $(A \subseteq B \land B \subseteq A)\implies (A = B).$

18. This property is called the *antisymmetry* of inclusion.

19. If $A$ is a subset of $B$ and $B$ is a subset of some set $C$, then $A$ is a subset of $C.$

20. We can write the above as $(A \subseteq B \land B \subseteq C)\implies(A \subseteq C).$

21. This property is called the *transitivity* of inclusion.

22. If, for sets $A$ and $B$, $A$ is a subset of $B$, but $A$ is *not* the same set as $B$, then $A$ is called a *proper* subset of $B.$

23. In symbols, $(A \subseteq B \land A \neq B)\implies(A \subset B).$

24. There is a set with no elements in it called the empty set.

25. The symbol for the empty set is $\varnothing.$

26. The empty set is a subset of every set.

27. The *cardinality* of a set is how many elements it contains.

## 2. 

*Basic operations of sets.*

1. If $X$ and $Y$ are sets, then there exists a set $Z$ which contains exactly $X$ and $Y$ as elements.

2. We can write the set $Z$ as $Z = \set {X, Y}$.

3. As a consequence (i.e. suppose $X=Y$), if $X$ is a set, then there exists a set $X' = \set{X}.$

4. Let $A$ and $B$ be sets. There exists a set called the *union* of $A$ and $B$ which contains every element which is in $A$ along with every element which is in $B$. The union of $A$ and $B$ is written $A \cup B.$

5. We can describe the union of two sets using set-builder notation: $A \cup B = \set {x \mid x \in A \lor x \in B}.$

6. We can translate this as "the union of $A$ and $B$ is the set of elements $x$, such that $x$ is in $A$ or $x$ is in $B.$"

7. Set union is commutative.

8. This means that the order of operands with respect to the operation does not matter.

9. In symbols, $A \cup B = B \cup A.$

10. Set union is associative.

11. This means that the grouping of terms with respect to the operation does not matter.

12. In symbols, $A \cup (B \cup C) = (A \cup B) \cup C.$

13. If a set $X$ is not empty, then it contains an element which itself contains no elements in common with $X.$

14. This is called the Axiom of Foundation.

15. This axiom is insurance against paradoxes.

16. To illustrate, suppose $R \in R$. Since $R$ is a set, we can construct a set $R' = \set{R}$. However, $R'$ and $R$ both contain $R$, and $R$ is the only element of $R'$. As such, the idea that some set could contain itself contradicts the Axiom of Foundation.

17. The set of elements common to two sets $A$ and $B$ is called their *intersection*. We write this $A \cap B = \set{x \mid x \in A \land x \in B}.$

18. Set intersection is commutative and associative.

19. If two sets $A$ and $B$ have no elements in common, i.e. $A \cap B = \varnothing,$ then $A$ and $B$ are said to be *disjoint.*

20. The set of elements which are in $A$ and *not* in $B$ is called the *relative complement* of $B$ in $A$.

21. We write this: $A \setminus B = \set{x \mid x \in A \land x \notin B}.$

22. The set of all elements which are in either $A$ or $B$ but *not* both is called the *symmetric difference* of $A$ and $B.$

23. We write this: $A \triangle B = \set {x \mid (x \in A \lor x \in B) \land \lnot (x \in A \land x \in B)}.$

24. This can be "literally translated" as "the symmetric difference of $A$ and $B$ is the set of all elements $x$ such that $x$ is in $A$ *or* $x$ is in $B$ *and* it is *not* the case that $x$ is in $A$  *and* $x$ is in $B.$"

25. The symmetric difference is commutative and associative.

## 3.

*Functions of sets.*

1. For any set $S$, there exists a set $P(S)$ called the *power set* of $S.$

2. The *subsets* of $S$ are the *elements* of $P(S).$

3. If a set $S$ has $n$ elements, then $S$ has $2^n$ subsets. In symbols, $|P(S)| = 2^{|S|}.$

4. A function $f: A \to B$ is a map between sets $A$ and $B$, where each element $a \in A$ has only one $f(a) \in B.$

5. If the source of a function is a set, then the target of a function is a set.

6. If $f: A \to B$ is a function, then $A$ is called the *domain* of $f$ while $B$ is the *codomain* of $f.$

7. If a function $f$ is defined for all elements of a set $A$, then there exists a subset of $B$ called the *image* $C$ of $A$ under $f$ defined as $C = \set{f(x) \mid x \in A}.$

8. Any subset of the domain of $f$ can also be said to have an image under $f.$

9. There is a function of a set called the *successor* function $S(n) = n \cup \set{n}.$

10. If, for sets $n$, $m$, $S(n) = S(m)$, then $n = m.$

11. There is a set $I$ called an *inductive set* such that $\varnothing \in I$ and an element $n$ being in $I$ implies that $S(n)$ is in $I.$

12. If we restrict $I$ such that it *only* has the empty set and its successors, then $I$ is the basis for the counting, or "natural" numbers.

13. One can say that the natural numbers are the labels for the elements of $I$ by cardinality.

14. The arithmetic interpretation of the successor of a natural number $n$ emerges as $S(n) = n + 1.$

15. We write the set of natural numbers $\mathbb{N}.$

16. We assign $0$ to $\varnothing.$

17. We assign $n$ to the $n$-th successor of $S(0).$

18. This provides a "natural" ordering where $n < S(n)$ and $n < m \land m < k \implies n < k$, and if neither $n < m$ nor $m < n$ then $n = m.$

19. An ordering is not "native" to a set; it must be imposed on it.

20. Any set can have an ordering imposed on it such that each of its non-empty subsets has a minimum element.

21. This is called the *well-ordering theorem* or *Zermelo's theorem,* and can here be treated as an axiom.

### 4.

*Relations between sets.*

1. For any sets $A$ and $B$, there exists the *Cartesian product* $A \times B,$ which is the set of ordered pairs $(x,  y)$ such that $x$ is in $A$ and $y$ is in $B.$

2. A *relation* between the elements of a set $A$ and the elements of a set $B$ is a subset of the Cartesian product $A \times B.$

3. For example, if we take the *equality* relation on some set $A = \set{a, b}$, it follows that this relation is fully encapsulated by the subset $E \subseteq A \times A$ where $E = \set{(a, a), (b, b)}$, and inequality is fully encapsulated by the relative complement $(A \times A) \setminus E.$

4. *A function is a special case of a relation.*

5. For any function $f: A \to B$, there is a subset $F$ of the Cartesian product $A \times B$ where, for any $a$ in $A$ and some $b$ and $c \neq b$ in $B$ if a pair $(a, b)$ is in $F$, then there is no pair $(a, c)$ in $F.$

6. That is, pairs in $F$ are unique in the first element, but not necessarily in the second.

7. Consider the identity function on integers (where the set of all integers is written $\mathbb{Z}$) $f: \mathbb{Z} \to \mathbb{Z}$, where $f(n) = n + 0$. Then, $f$ is completely described by the subset $E = \set{(n, n) \in \mathbb{Z} \times \mathbb{Z}}.$

8. This set $E$ makes it clear that the equality relation and the identity function are two perspectives on the same abstraction.

9. Whenever some element $a$ is viewed as being "assigned" to some element $b$, this assignment can also be viewed as a static pair $(a, b)$, and vice versa.

10. A function is *injective* if two different elements in its domain must map to two different elements in its codomain.

11. That is, if for every $a$, $b$ in the domain $A$ of $f$, $a \neq b \implies f(a) \neq f(b)$, or equivalently, $a = b \implies f(a) = f(b).$

12. A function $f : A \to B$ is *surjective* if its codomain $B$ is the image of $A.$

13. A function $f$ is *bijective* if it is both injective and surjective.

14. A function being bijective is equivalent to it being *invertible.*

15. A bijective function is a one-to-one correspondence between each element of its domain and each element of its codomain.

16. The successor function $s : \mathbb{N} \to \mathbb{N}$ where $s(n) = n + 1$ is injective but it is not surjective, since $0$ is in $\mathbb{N}$ but not in the image of $s.$

17. Any function which is not surjective can be redefined as a surjective function by restricting its codomain to be the same as its image.

## 5.

*Equivalence relations and quotient sets. Construction of the integers.*

1. Reflexivity, symmetry, and transitivity are the conditions for a relation to be an equivalence relation.

2. Equality is an equivalence relation.

3. An equivalence relation splits a set into *equivalence classes.*

4. The set of equivalence classes one gets from partitioning a set $S$ according to an equivalence relation $R$ is called a *quotient set*, and it is denoted $S / R.$

5. The set of integers $\mathbb{Z}$ can be constructed via the imposition of an equivalence relation on $\mathbb{N} \times \mathbb{N}.$ 

6. Suppose $R$ stands for the relation where for $(a, b), (c, d) \in \mathbb{N} \times \mathbb{N},$ $(a, b) = (c, d)$ if $a + d = b + c.$

7. Addition is defined such that $(a, b) + (c, d) = (a + c, b + d).$

8. Multiplication is defined such that $(a, b)(c, d) = (ac + bd, ad + bc).$ 

9. Then, an equivalence class of pairs in $(\mathbb{N} \times \mathbb{N})/R$ is an integer.

10. Intuitively, an integer $n$ stands for a class of pairs $(a, b)$ where $n = a - b.$

11. Then, if $a > b,$ then $n$ is positive.

12. If $a < b,$ then $n$ is negative.

13. Finally, if $a = b,$ then $n = 0.$ 

14. An integer $n$ has an *absolute value* $|n|,$ where if $n \ge 0,$ then $|n| = n,$ and if $n < 0,$ then $|n| = -n.$

15. An equivalence relation one can impose on the integers is $|n| = |m|.$ We will call this relation $A.$

16. If one takes the set of all subsets of $\mathbb{Z}$ where the absolute value of every element of the subset equals the absolute value of every other in the subset, then we can partition $\mathbb{Z}$ into a set of equivalence classes $\mathbb{Z} / A = \set{\set{0}, \set{-1, 1}, \set{-2, 2}, ...}.$

17. When one has a set of equivalence classes, it is often frequent to treat a class as if it were a particular *class representative.*

18. That is, in a set like $\mathbb{Z} / A = \set{\set{0}, \set{-1, 1}, \set{-2, 2}, ...},$ it can be seen as natural to treat each class in the set as the non-negative element of the class.

19. So, if we take the set of non-negative *class representatives* of $\mathbb{Z}/A$, then we get $\mathbb{N}.$

## 6.

*Induction.*

1. The well-ordering theorem (or, alternatively, the existence of inductive sets) gives rise to the method of *induction,* one of the most powerful ways to prove things about numbers.

2. One of the most common forms of induction is "weak" induction on natural numbers, which takes $3$ steps.

3. If one wants to prove some property $P$ holds for all natural numbers, first, one proves a base case.

4. That is, depending on the property, one demonstrates that $P$ is the case for $0$ or $1,$ or even some other number when appropriate.

5. Second, one makes an assumption called the *inductive hypothesis,* that $P$ holds for some arbitrary natural number $k.$

6. Finally, one proves that if $P$ is the case for $k,$ then $P$ must be the case for $k + 1.$

7. Then, it follows that $P$ holds for natural numbers greater than or equal to the number featured in the base case.

8. That is, one proves a specific case, then one proves a general implication: if $P$ holding for $k$ implies $P$ holds for $k + 1,$ and we can point to a value $b$ for which $P$ holds, then it follows that $P$ must hold for $b + 1,$ which implies that $P$ holds for $b + 2,$ ad infinitum.

9. There are numerous variants and generalizations of induction, including the "strong" form, which makes an inductive hypothesis that $P$ holds *for all* values less than some $k,$ and is ultimately logically equivalent to weak induction, but makes certain arguments easier to make. 

### Exercises

1. Prove that if $a$ and $b$ are positive integers, then there exists a positive integer $n$ such that $na \ge b.$ This is called the *Archimedean property.*

2. A function between infinite sets is one of infinitely many rules of element assignment, but a function is fully determined by the assignment of elements from one set to the other, as opposed to the abstract rule. So, a function between finite sets is one of finitely many regimes of element assignment. If $A$ and $B$ are each sets with finitely many elements, how many possible functions are there from $A$ to $B$?

3. Using induction, prove that the sum of the first $n$ odd numbers is equal to $n^2$. 

4. An axiom which is part of the standard set-theoretic formulation of mathematics is called the *axiom of choice.* The axiom of choice states that, given a collection of non-empty sets, it is possible to "choose" some element from each set in the collection and construct a new set consisting exactly of the chosen elements. Demonstrate that the axiom of choice is equivalent to the well-ordering theorem.
