## 1.

*Natural numbers.*

1. There is a function of a set called the *successor* function $S(n) = n \cup \set{n}.$

2. If, for sets $n$, $m$, $S(n) = S(m)$, then $n = m.$

3. There is a set $I$ called an *inductive set* such that $\varnothing \in I$ and where an element $n$ being in $I$ implies that $S(n)$ is in $I.$

4. If we restrict $I$ such that it *only* has the empty set and its successors, i.e. we take the intersection of *all* inductive sets, then this restricted set $I'$ is the basis for the counting, or "natural" numbers.

5. One can then say that the natural numbers are the labels for the elements of $I'$ by cardinality.

6. The arithmetic interpretation of the successor of a natural number $n$ emerges as $S(n) = n + 1.$

7. We write the set of natural numbers $\mathbb{N}.$

8. We assign $0$ to $\varnothing.$

9. We assign the natural number $n$ to $S(n-1).$

### Exercises

1. In the set-theoretic construction of the natural numbers, a number $n \in \mathbb{N}$ takes the form $n = \set{0, 1, 2, {...}, n},$ where e.g. $1 = \set{\varnothing},$ $2 = \set{\varnothing, \set{\varnothing}},$ $3 = \set{{\varnothing, \set{\varnothing}},\set{\varnothing, \set{\varnothing}}},$ and so on. Show that the $\le$ relation on $\mathbb{N}$ is the $\subseteq$ relation on the intersection of all inductive sets.

## 2.

*Integers.*

1. Consider the Cartesian product $\mathbb{N} \times \mathbb{N}.$ We can define an equivalence relation $D$ such that, given $(a, b), (c, d) \in \mathbb{N} \times \mathbb{N}$, $(a, b) \sim (c, d)$ if and only if $a + d = b + c.$ 

2. Addition is defined such that $(a, b) + (c, d) = (a + c, b + d).$

3. Multiplication is defined such that $(a, b)(c, d) = (ac + bd, ad + bc).$

4. Then, an equivalence class of pairs in $(\mathbb{N} \times \mathbb{N})/D$ is an integer.

5. The symbol for the set of all integers is $\mathbb{Z}.$

6. An integer $n$ stands for a class of pairs $(a, b)$ which can be intuitively thought to "encode a fixed difference."

7. That is, although it is arguably most direct to think of $n$ as the set of all pairs $(a, b)$ such that $a - b = n,$ this is tautological as a definition, because there is no well-defined pre-existing notion of subtraction of two arbitrary natural numbers. 

8. So, the set-theoretic interpretation of an integer like, e.g. $1 \in \mathbb{Z}$ is $1 = \set{(1, 0), (2, 1), (3, 2), {...}},$ and likewise $-1 = \set{(0, 1), (1, 2), (2, 3), {...}}.$

9. Then, $2 = \set{(2, 0), (3, 1), (4, 2), {...}}$ and $-2 = \set{(0, 2), (1, 3), (2, 4), {...}}$ and so on.

### Exercises

1. Using the given set-theoretic construction, establish a well-defined notion of each of the following (in any order):

- Total ordering of $\mathbb{Z}.$ 
- Positive and negative integers.
- Subtraction of arbitrary integers.

## 3.

*Abelian groups.*

1. A *group* is a structure comprising a set and an operation which together satisfy certain requirements.

2. Let $S$ be an arbitrary set and $*$ be an arbitrary operation.

3. The first requirement is closure under the operation: $\forall{a, b}\in{S}, a * b\in{S}.$

4. The second is that the operation has an identity: $\exists{e}\in{S}:\forall{a}\in{S},a * e = e * a=a.$

5. The third is that the operation is associative: $\forall{a, b, c}\in{S}, a * (b * c)=(a * b) * c.$

6. The fourth (and most restrictive) requirement is that every element in the set has an *inverse* under the operation.

7. That is, $\forall{a}\in S, \exists{a^{-1}} \in S: a * a^{-1}= a^{-1} * a=e.$

8. It follows from the above requirements that the inverse of any element $a$ in a group is uniquely the inverse of $a.$

9. Suppose for some group $G$ with elements $a$, $b$, and $c$ and identity $e$, were to have $b$ and $c$ each be separate inverses of $a.$

10. That is, $a * b = b * a = e$ and $a * c = c * a = e.$

11. We have $(b * a) * c = e * c$, but we also have $b * (a * c) = b * e$, so it follows from the associative property that it must be the case that $b = c.$

12. An *abelian* group is a group whose operation is commutative. That is, $\forall{a, b} \in S, a * b = b * a.$

13. This book is mainly about addition and multiplication, with some function convolution thrown in for flavor; all of these are, in the cases relevant here, commutative operations.

14. As such, the group theory at hand will largely be limited to  topics relevant to abelian groups.

### Exercises

1. Consider the following tables which respectively define the XOR, AND, and OR operations on two bits, i.e. which assign two values from $\set{0, 1}$ to an element of $\set{0, 1}.$ Which of these operations on $\set{0, 1}$ form groups? If an operation doesn't form a group on $\set{0, 1},$ which condition(s) does it fail to satisfy?

| $A \oplus B$ | $0$ | $1$ |
| ------------ | --- | --- |
| $0$          | $0$ | $1$ |
| $1$          | $1$ | $0$ |

| $A \land B$ | $0$ | $1$ |
| ----------- | --- | --- |
| $0$         | $0$ | $0$ |
| $1$         | $0$ | $1$ |

| $A \lor B$ | $0$ | $1$ |
| ---------- | --- | --- |
| $0$        | $0$ | $1$ |
| $1$        | $1$ | $1$ |


## 4. 

*Additive group of integers.*

1. If a set and an operation have closure, associativity, and an identity, but there is no guarantee that every element has an inverse, then that set and operation form a *monoid.*

2. The natural numbers, having no idea of "negative number," guarantee an inverse under addition for no element except $0.$

3. That is, addition of natural numbers is closed, associative, and has an identity element $0.$

4. However, for natural numbers $a, b,$ the only solution to $a + b = 0$ is to set $a = b = 0.$

5. So, the natural numbers form a monoid under addition.

6. Likewise, we can note that for natural numbers $a,b,$ the equation $ab = 1$ has exactly $1$ solution, where $a = b = 1,$ meaning that $\mathbb{N}$ is also a monoid under multiplication.

7. In $\mathbb{Z},$ however, supposing $a$ is fixed and $n$ is an indeterminate, $a + n = 0$ can always be solved by setting $n = -a.$

8. So, integers, having closure, associativity, and the identity $0,$ form a group under addition.

9. Negative numbers, alas, do not remedy the inverse shortage felt by integer multiplication, so $\mathbb{Z}^{\times}$ stays a monoid.

10. When $\mathbb{Z}$ is said or written simply to be a group, this is a reference to the group under addition.

11. One can notice that the multiples of some fixed integer comprise a subset of $\mathbb{Z}$ which in itself satisfies the requirements for a group under addition.

12. Suppose $G$ is a group under some arbitrary operation $*$ and $H$ is a subset of $G.$ $H$ is then a *subgroup* of $G$ if $H$ is a group under $*.$

13. It is frequently convenient to not specify the operation for arbitrary groups, and write $gh$ to mean e.g. $g * h.$

14. So, the set of multiples of each integer $n$ uniquely, up to inverses, defines a subgroup of $\mathbb{Z}$ which we can write as $n\mathbb{Z}.$

15. The subgroup $n\mathbb{Z}$ and the structure which stems from the properties of $n$ comprise the periodically-beating heart of everything to follow.

### Exercises

1. Show that $0\mathbb{Z}$ is a subgroup of $\mathbb{Z}.$

2. If one were to take the Cartesian product of two sets that each formed groups under an arbitrary operation (that is, the operation need not be the same for both), such a product would trivially posse up under those operations applied component-wise. Devise a well-defined notion of *direct product* $G \times H$ for groups $(G, \star), (H, \diamond),$ in the sense that $(G \times H, (\star, \diamond))$ is always a group.

## 5.

*Quotient groups.*

1. A normal subgroup[^1] $H$ of a group $G$ induces an equivalence relation: let $a, b \in G.$ Then, $a \sim b \iff a^{-1}b \in H.$

2. This relation partitions $G$ into *left cosets.*[^2]

3. Given some $g \in G$ and subgroup $H$ of $G,$ a left coset $gH$ is an equivalence class of the form $\set{gh \mid h \in H}.$

4. The number of cosets induced in the underlying set of a group $G$ by a subgroup $H$ is called the *index of $H$ in $G$* and is denoted $[G:H].$

5. For example, consider $3\mathbb{Z} = \set{{...}, -6, -3, 0, 3, 6, {...}},$ the subgroup of $\mathbb{Z}$ consisting of all multiples of $3.$

6. If we interpret $\mathbb{Z}/3\mathbb{Z}$ as the quotient set partitioned by $a \sim b \iff -a + b \in 3\mathbb{Z},$ then it contains the following three sets: $\set{{...}, -6, -3, 0, 3, 6, {...}},$ $\set{{...}, -5, -2, 1, 4, 7, {...}},$ and $\set{{...}, -4, -1, 2, 5, 8, {...}}.$ 

7. Since these cosets are the sets of all integers in the forms $3k,$ $3k + 1,$ and $3k + 2$ respectively, it is clear that they form a complete partition of $\mathbb{Z}.$

8. In general, $\mathbb{Z}/n\mathbb{Z},$ for a positive integer $n,$ consists of $n$ disjoint cosets of the form $\set{{...}, -2n + k, -n + k, k, n + k, 2n + k, {...}}$ for each non-negative $k < n.$

9. Intuitively, each element of $\mathbb{Z}/n\mathbb{Z}$ (which we will also here write as $\mathbb{Z}_n$) is the set of all multiples of $n$ "offset" by one of the $k < n.$

10. The definition of the operation on cosets of a group modulo a normal subgroup ensures that the operation on the base group retains the group property on the cosets, i.e. 

11. That is, suppose $H$ is a normal subgroup of $G$ under an arbitrary $+,$ and let $a, b \in G.$ Then, $(a + H) + (b + H) = (a + b) + H.$

12. It is for this reason that the equivalence classes comprising $\mathbb{Z}_n$ are often treated as if they were each a particular numerical representative of themselves, i.e. one of the non-negative integers $k < n.$

13. A complete set of (non-redundant) equivalence class representatives of a group $\mathbb{Z}_n$ is called a *residue system modulo $n.$*

14. The set of non-negative integers less than $n$ comprise the *least residue system modulo $n.$*

15. This is to say it frequently alleviates headaches to refer to an equivalence class like $\set{{...}, -2n + k, -n + k, k, n + k, 2n + k, {...}}$ in the context of some $\mathbb{Z}_n$ as simply the number $k$.

16. This is analogous to how in practice we use concise single-number notation to describe integers, even though integers are formally constructed as equivalence classes of pairs.

## 6.

*Subgroups and cosets.*

1. Every group is a subgroup of itself.

2. The one-element *trivial group*, which consists of the identity element, is a subgroup of every group.

3. A group must have at least $1$ element.

4. Consider that the empty set can never be the underlying set of a group, because a group requires an identity element, and the empty set has no elements.

5. The identity element of a quotient group $G/H$ is the coset $H.$

6. $G$ is a group, so it has an identity element $e.$

7. Then, $G/H$ contains a coset $e + H = \set{e + h \mid h \in H},$ which is plainly $H.$

8. It is also for this reason that $H$ is the *only* coset of $G/H$ which forms a subgroup.

9. That is, $H$ contains the element $e + e,$ and the sets which are in $G/H$ are all disjoint from one another, so only $H$ has an identity among its elements.

## 8.

*Cyclic groups.*

1. A *cyclic group* is a group whose elements can all be written as "multiples" or "powers" (in a generalized sense) of a single element and its inverse.

2. That is, if $G$ is a cyclic group, then each element of $G$ can be written as $gk$ for some *generator* $g$ and some integer $k$, where $0g = e,$ as in the group's identity.

3. This notation is chosen to emphasize that a product of integers $g$ and $k$ is of course the $k$-fold addition of $g$ to $0.$

4. It is an equally valid stylistic choice to write the elements of an arbitrary cyclic group as $g^k$ for some generator $g$ and integer $k,$ where $g^0 = e;$ this is simply multiplicative as opposed to additive convention.

5. The integers $\mathbb{Z}$ and their quotients $\mathbb{Z}_n$ are all additive cyclic groups: in each case, every element can be written as an integer multiple of $1.$

6. Every cyclic group is abelian.

7. Suppose $a, b \in G$ where $G$ is cyclic. Then, for some integers $n, m,$ we can write the product $ab = g^n g^m.$ It follows, then, that $ab = g^{n+m}.$

8. So, from the commutativity of integer addition, $ab = g^{n + m} = g^{m + n} = g^m g^n = ba.$

9. This argument works equally well in additive notation: $a + b = ng + mg = (n + m)g = (m + n)g = mg + ng = b + a.$
