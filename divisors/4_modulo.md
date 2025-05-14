# Modular arithmetic

1. Modular arithmetic is "wrap-around" arithmetic.
2. Given a *modulus* $m$, arithmetic operations on numbers "wrap around" at $m$.
3. It is sometimes introduced as "clock arithmetic," because the temporal units which divide a day, half-day, hour, and so on wrap around at $24$, $12$, and $60$ respectively, and so provide natural examples of moduli: if it is $17:00$, waiting for $10$ hours brings one to $3:00$ on the next day, as opposed to some $27:00$.
4. The properties of arithmetic over a modulus $m$ depend on the  set of divisors of $m$, so the description "clock arithmetic" has a critical flaw preventing it from being fully faithful to modular arithmetic.
5. That is, for e.g. hours of the day, addition and subtraction are the only arithmetic operations with motivation.
6. The properties which make a modulus $m$ a nice choice to serve as a temporal period are the same properties which make *multiplication* modulo $m$, structurally speaking, "very bad."
7. There is an equivalence relation between integers called *congruence modulo m*, where $m$ is a positive integer.
8. Two integers $a$ and $b$ are congruent modulo $m$ if there exists an integer $k$ such that $a - b = km$.
9. This condition is equivalent to $m$ dividing the difference between $a$ and $b$, and, since if a number divides an integer $n$, it must also divide $-n$, if there exists a $k$ for $a - b = km$, then there must exist a $k$ for $b - a = km$.
10. If integers $a$ and $b$ are congruent over a modulus $m$, we write $a \equiv b \pmod m$.
11. Congruence is reflexive: any number is congruent to itself under any modulus.
12. Congruence is *symmetric*. If $a \equiv b \pmod m$, then $b \equiv a \pmod m$.
13. Congruence is transitive. If $a \equiv b \pmod m$ and $b \equiv c \pmod m$ then $a \equiv c \pmod m$.
14. Reflexivity, symmetry, and transitivity are the conditions for a relation to be an equivalence relation.
15. An equivalence relation splits a set into *equivalence classes.*
16. Equality is obviously an equivalence relation, and it splits the set of integers into equivalence classes which each contain one integer.
17. Another equivalence relation one can impose on the integers is $|n| = |m|$. We will call this relation $A$.
18. If one takes the set of all subsets of $\mathbb{Z}$ where the absolute value of every element of the subset equals the absolute value of every other in the subset, then we can partition $\mathbb{Z}$ into a set of equivalence classes $\mathbb{Z} / A = \set{\set{0}, \set{-1, 1}, \set{-2, 2}, ...}$.
19. If we take the set of non-negative *class representatives* of  $\mathbb{Z}/A$, then we simply get $\mathbb{N}$.
20. The set of equivalence classes one gets from partitioning a set $S$ according to an equivalence relation $R$ is called a *quotient set*, and it is denoted $S / R$.
21. We will use $m\mathbb{Z}$ as a symbol meaning "congruence modulo $m$."
22. For every positive integer $m$, there is a unique quotient set corresponding to the set of equivalence classes of integers when partitioned according to $m\mathbb{Z}$. We conventionally denote this set $\mathbb{Z}/m\mathbb{Z}$.
23. Conventionally, we often perform modular arithmetic using the *least residue system* of a modulus $m$, which is simply the set of all non-negative integers which are less than $m$.
24. These integers serve as the class representatives of $\mathbb{Z}/m\mathbb{Z}$, and it is frequently convenient to use $\mathbb{Z}/m\mathbb{Z}$ to refer to the set of representatives as opposed to the set of classes.
25. In practice, a modulus is often framed as taking the arithmetic of a set of infinitely many integers and sending it to a finite set of integers.
26. Addition and subtraction work "normally" over any modulus.
27. A better way of saying this is that addition on $\mathbb{Z}/m\mathbb{Z}$ always forms a *group* of order $m$ for any modulus $m$.
28. A group is a structure comprising a set and an operation which together satisfy certain requirements.
29. Let $S$ be an arbitrary set and $*$ be an arbitrary operation.
30. The first requirement is closure under the operation: $\forall{a, b}\in{S}, a * b\in{S}$.
31. The second is that the operation has an identity: $\exists{e}\in{S}:\forall{a}\in{S},a * e = e * a=a$.
32. The third is that the operation is associative: $\forall{a, b, c}\in{S}, a * (b * c)=(a * b) * c$
33. The fourth (and most restrictive) requirement is that every element in the set has an *inverse* under the operation.
34. That is, $\forall{a}\in S, \exists{a^{-1}} \in S: a * a^{-1}= a^{-1} * a=e$.
35. It follows from the above requirements that the inverse of any element $a$ in a group is unique to $a$.
36. Suppose for some group $G$ with elements $a$, $b$, and $c$ and identity $e$, were to have $b$ and $c$ each be separate inverses of $a$.
37. That is, $a * b = b * a = e$ and $a * c = c * a = e$.
38. We have $(b * a) * c = e * c$, but we also have $b * (a * c) = b * e$, so it follows from the associative property that it must be the case that $b = c$.
39. An *abelian* group is a group whose operation is commutative. That is, $\forall{a, b} \in S, a * b = b * a$.
40. Groups from arithmetic tend to be commutative because e.g. addition and multiplication of individual numbers are both commutative, and our focus is largely on groups formed out of these operations, but there are many ways to achieve a group structure without commutativity.
41. For example, the set of all element rearrangements (or permutations) of a set of $n$ elements forms a group under composition of permutations (called the *symmetric group of degree $n$*), but the composition of permutations is not in general commutative.
42. The *order* of a group is the cardinality of its underlying set, or how many elements are in the group.
43. Addition over $\mathbb{Z}$ is an abelian group. Every positive integer $n$ has a corresponding negative integer $-n$ (and vice versa) which serves as its *additive inverse.*
44. $0$ is its own inverse, because it is the additive identity, and it follows from the definition of an identity of a group that a two-sided identity element is always its own inverse.
45. If a set has elements without inverses w/r/t an operation, but retains closure, associativity, and an identity element, then that set and operation form a *monoid* as opposed to a group.
46. Multiplication over $\mathbb{Z}$ is a monoid and *not* a group, because non-unit integers do not have other integers as multiplicative inverses.
47. For any modulus $m$, any element $n$ of $\mathbb{Z}/m\mathbb{Z}$ has a corresponding element $k = m - n$ such that $n + k \equiv 0 \pmod m$, so an additive inverse is always present.
48. From the clock perspective, this is expressed in the notion that whatever hour it is, there is always some number of hours one can wait until the day ends.
49. From the clock perspective, the more "highly composite" a modulus $m$ is, i.e. the more divisors it has relative to its size, the better it is for convenient time-keeping.
50. For any modulus $m$, the equivalence class whose representative is $0$ is the set of multiples of $m$.
51. Consider $ab \equiv 0 \pmod{p}$, where $p$ is prime: since the divisors of $p$ are exactly $1$ and $p$, for any product of positive integers $a$ and $b$, given $ab = p$, either $a = p$ and $b = 1$ or $a = 1$ and $b = p$.
52. So, effectively, the only way to get a product of $0$ in a prime modulus is to multiply a number by $0$ or a multiple of $p$.
53. Now, consider a product like $ab \equiv 0 \pmod{12}$: $a$ could be $2$ if $b$ is $6$, or $a$ could be $3$ if $b$ is $4$, and vice versa.
54. This is to say, two numbers, of which neither is in the "0 class" of the modulus, can multiply with each other to get 0.
55. We will denote the *multiplicative* group of a modulus $m$ with $(\mathbb{Z}/m\mathbb{Z})^{\times}$.
56. While the order of $(\mathbb{Z}/m\mathbb{Z})^{+}$ is always $m$, the set underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ has to have at most $m-1$ elements, provided $m > 1$.
57. This is because $1$ is the identity element of multiplication, and there is no way to get a number which is not $0$ from a product with $0$ as a term.
58. That is, $0$ can never have a multiplicative inverse, so it is excluded from the set.
59. The exception to this is the case where $m = 1$, since all of $\mathbb{Z}$ is collapsed into a single equivalence class represented by $0$, and $0$ times $0$ is $0$, meaning $(\mathbb{Z}/1\mathbb{Z})^{\times}$ is actually a group of order $1$.
60. So, if $ab \equiv 0 \pmod{m}$, and neither $a$ nor $b$ is $0$, then $a$ and $b$ violate the closure condition required of a group.
61. For this reason, the set of representatives underlying $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is the set of positive integers less than or equal to $m$ which are relatively prime to $m$.
62. There is a function defined on positive integers called *Euler's phi function*.
63. For a number $n$, $\varphi(n)$ counts the number of positive integers less than *or equal to* $n$ which are relatively prime to $n$.
64. $1$ is the unique number which is relatively prime to itself, because $\gcd(n, n) = n$.
65. This means that $1$ is the unique value for $n$ such that $\varphi(n) = n$.
66. It is the case that $p$ is a prime number if and only if $\varphi(p) = p - 1$.
67. For $\varphi(p) = p - 1$ to not be the case, then there would have to be a number less than $p$ but greater than $1$ which divides $p$.
68. So, it follows that the order of $(\mathbb{Z}/m\mathbb{Z})^{\times}$ is $\varphi(m)$, i.e. $m - 1$ if and only if $m$ is prime.
69. It is often useful to consider the *negative* class representatives of a modulus, for the reason that $-a \equiv m-a \pmod{m}$.
70. $1$ is its own mutiplicative inverse for any modulus, and since $(-1)(-1) = 1$, $m - 1$ is also its own multiplicative inverse for any modulus.
71. Bézout's identity guarantees that if an integer $a$ is relatively prime to $m$, then there exist integers $x$ and $y$ such that $ax + my = 1$.
72. It follows, then, that $ax \equiv{1} \pmod{m}$, i.e. $x$ is the multiplicative inverse of $a$ modulo $m$.
