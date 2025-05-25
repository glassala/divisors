# Group homomorphisms

1. A normal subgroup of a group is a subgroup for which the set of left cosets it induces is the same as the set of right cosets it induces.
2. That is, under some arbitrary operation $*$, if $H$ is a subgroup of $G$, then $H$ is normal if for all $h$ in $H$ and for all $g$ in $G$, $g * h * -g$ is in $H$.
3. Every subgroup of an abelian group is a normal subgroup.
4. A *quotient group* is a group $G / H$ which is the partition of some group $G$ into *congruence classes* by a normal subgroup $H$.
5. The partitioning subgroup must be normal because otherwise one would need to specify either a left or right coset partition, and such a partition would not be guaranteed to have inverses.
6. A congruence class w/r/t a group is an equivalence class which respects the properties of the group.
7. The groups defined for $\mathbb{Z}/n\mathbb{Z}$ have been introduced as groups over a quotient set.
8. However, one can view $(\mathbb{Z}/n\mathbb{Z})^{+}$, for example, as a *quotient group* of the integers $\mathbb{Z}^{+}$ and the subgroup of the integers $n\mathbb{Z}^{+}$ whose elements are $0$ and the multiples of $n$.
9. The set of congruence classes into which a group is partitioned by $H$ is the set of cosets induced by $H$.
10. A *group homomorphism* is a map from one group to another.
11. Or, one can say it is a map from the elements of the underlying set of one group to the underlying set of another group such that the group structure is preserved through the mapping.
12. The condition for the map $f: G \to H$ to be a homomorphism between groups $(G, *)$ and $(H, \times)$, where $*$ and $\times$ are arbitrary operations, then $f$ has the property that for all $x$, $y$ in $G$, it is the case that $f(x * y) = f(x) \times f(y)$.
13. A group homomorphism maps the identity of $G$ to the identity of $H$ and maps the inverses of elements of $G$ to the inverses of elements of $H$.
14. A homomorphism which is injective, i.e. where distinct elements in its domain always map to distinct elements in its codomain, is called a *monomorphism*. A monomorphism $\phi$ between groups $A$ and $B$ is denoted with a hooked arrow in the form $\phi: A \hookrightarrow B$.
15. A homomorphism $\phi$ between groups $A$ and $B$ which is surjective, i.e. where $\text{im}(\phi) \cong B$ is the case, is called an *epimorphism* and is denoted with a double-headed arrow $\phi: A \twoheadrightarrow B$.
16. A group homomorphism which is both a monomorphism and an epimorphism is an isomorphism. One can say an isomorphism is a special case of a homomorphism which is invertible.
17. The map which sends a set $S$ to a quotient set $S / R$ where $R$ is an equivalence relation on elements of $S$ is called the *canonical projection* $\pi : S \to S/R$.
18. Where $H$ is a normal subgroup of $G$, the canonical projection $\pi: G \to G/H$ is a group homomorphism.
19. By virtue of being the "canonical" mapping of elements to the cosets a normal subgroup induces, this homomorphism is essentially surjective by definition.
20. It is defined as $\pi(g) = \set{g * h \mid h \in H}$ for elements $g \in G$.
21. That is, it maps an element of a group to the left coset formed out of its operation on all the elements of $H$.
22. The *kernel* of a group homomorphism $f: G \to H$ is the set of elements in $G$ which are mapped to the identity in $H$.
23. If the operation of $H$ is $\times$, we can write this as $\text{ker}(f) = \set{g \mid \forall{h \in H}, f(g) \times h = h}$, or, more concisely, if we say that $e_H$ is the identity of $H$, then $\text{ker}(f) = \set{g \mid f(g) = e_{H}}$.
24. The *image* of $f: G \to H$ is the subgroup of $H$ which consists of the elements $\text{im}(f) = \set{f(g) \mid g \in G}$.
25. For example, if $\pi: \mathbb{Z} \to \mathbb{Z}_2$ is a homomorphism between additive groups, then $\text{im}(\pi)$ is a set containing two congruence classes: the set of integers congruent to $0 \pmod{2}$ and the set of integers congruent to $1 \pmod{2}$.
26. Since the $0$ class is the identity, and it is exactly the even numbers which are mapped to it, we can say that $\text{ker}(\pi)$ is the set of all even numbers.
27. The kernel of any group homomorphism is a normal subgroup of its domain.
28. Let $a$ and $b$ be in $\text{ker}(\phi), where $\phi : A \to B$, with $*$ being the operation of $A$ and $\times$ being the operation of $B$.
29. Because $a$ and $b$ are in the kernel, $\phi(a) = \phi(b) = e_B$.
30. By definition of a homomorphism and the kernel, $\phi(a * b) = \phi(a) \times \phi(b) = e_{B}e_{B} = e_{B}$.
31. That is, $a * b$ is in the kernel, and so $\text{ker}(\phi)$ is closed under the operation of $A$.
32. Since homomorphisms preserve the identity, the identity must be in the kernel.
33. Since group homomorphisms always preserve inverses, the inverse of any element in the kernel must itself be in the kernel.
34. This subgroup must always be normal, because $\phi(a * b * -a) = \phi(a) \times \phi(b) \times -\phi(a) = e\phi(a) \times e_B \times -\phi(a) = e_{B}$.
35. It essentially follows from definitions that the image of any group homomorphism is a subgroup of its codomain.
36. Let $\phi: A \to B$ be a homomorphism between groups. Then, $G/\text{ker}(\phi) \cong \text{im}(\phi)$.
37. This is called the *first isomorphism theorem*.
38. Since $\text{ker}(\phi)$ is a normal subgroup of $A$, there exists a canonical projection $\pi: A \to A/\text{ker}(\phi)$.
39. By virtue of the kernel, one can construct an *induced map* $\mu : A/\text{ker}(\phi) \to \text{im}(\phi)$ where $\mu(a * \text{ker}(\phi)) = \phi(a)$ for all $a \in A$.
40. $A/\text{ker}(\phi)$ is the set of congruence classes where for $a, a' \in A$, $a \sim a'$ if $a' = a * k$ for some $k$ in $\text{ker}(\phi)$.
41. Since $\phi$ maps all $k \in \text{ker}(\phi)$ to $e_B$, the value of $\phi(a)$ fully determines the value of $\mu(a * \text{ker}(\phi))$.
42. That is, if $a * \text{ker}(\phi) = a' * \text{ker}(\phi)$, then $\mu(a * \text{ker}(\phi)) = \mu(a' * \text{ker}(\phi))$.
43. We can define the product in $A/\text{ker}(\phi)$ as $(a * a') * \text{ker}(\phi) = (a * \text{ker}(\phi)) * (a' * \text{ker}(\phi))$.
44. That is, $\phi(a * a') = \phi(a) * \phi(a') = \mu((a * a')\text{ker}(\phi)) = \mu(a * \text{ker}(\phi)) * \mu(a' * \text{ker}(\phi))$.
45. This means that $\mu$ is a group homomorphism.
46. If $\mu(a * \text{ker}(\phi)) = e_B$, then $\phi(a) = e_B$, meaning $a \in \text{ker}(\phi)$.
47. So, $a * \text{ker}(\phi) = \text{ker}(\phi)$, i.e $\text{ker}(\mu) = \set{e_{A/\text{ker}(\phi)}}$.
48. If the kernel of a map contains only the identity of its domain, it is injective, i.e. a monomorphism.
49. If $b \in \text{im}(\phi)$, then $b = \phi(a)$ for some $a \in A$.
50. The coset $a * \text{ker}(\phi)$ satisfies $\mu(a * \text{ker}(\phi)) = \phi(a) = b$, so the image of $\mu$ is the full image of $\phi$, meaning $\mu$ is surjective, i.e. an epimorphism.
51. Since $\mu$ is a bijection which preserves group structure, it is an isomorphism $A/\text{ker}(\phi) \cong\text{im}(\phi)$.
52. An endomorphism $\epsilon : A \to A$ is a group homomorphism from a group to a subgroup of itself.
53. The set of endomorphisms of a group $A$ forms a group under pointwise addition if and only if $A$ is abelian. This group will be denoted $\text{End}(A)^+$.
54. Suppose $\phi : A \to A$ and $\psi : A \to A$ are endomorphisms of $A$.
55. For $\text{End}(A)^+$ to be a group, then $\phi + \psi$ must be an endomorphism of $A$.
56. The pointwise addition of endomorphisms $\phi$, $\psi$ of an abelian group $A = (A', *)$ is defined such that for all $a \in A'$,  $(\phi + \psi)(a) = \phi(a) * \psi(a)$.
57. So, for endomorphisms to be themselves a group, it has to be the case that, for all endomorphisms $\phi$, $\psi$ in the set $\text{End}(A)$ and $a$, $b$ in $A$, $(\phi + \psi)(a * b) = (\phi + \psi)(a) * (\phi + \psi)(b)$.
58. This can be rewritten to $\phi(a * b) * \psi(a * b) = \phi(a) * \phi(b) * \psi(a) * \psi(b)$.
59. Via the homomorphism property, this can be rewritten again as $\phi(a) * \psi(a) * \phi(b) * \psi(b) = \phi(a) * \phi(b) * \psi(a) * \psi(b)$.
60. This is to say that the set of endomorphisms of a group $A$ is only closed under pointwise addition in general if $A$ is abelian, and if $\text{End}(A)^+$ is a group, then it is an abelian group.
61. It follows from the definition of pointwise addition that $\text{End}(A)^+$ inherits the associativity of $A$.
62. For any group $A$, there exists a zero endomorphism $\zeta : A \to A$ such that for all $a$ in $A$, $\zeta(a) = e_A$.
63. This is the identity for pointwise addition, since for any endomorphism $\phi$ of $A$ and any $a \in A$, $(\zeta + \phi)(a) = \zeta(a) * \phi(a) = e_A * \phi(a) = \phi(a)$.
64. Finally, there is a well-defined additive inverse such that if $\phi$ is an endomorphism of $A$, then there exists an endomorphism $-\phi$ where $(-\phi)(a) = -\phi(a)$.
65. Therefore, if and only if $A$ is an abelian group, $\text{End}(A)^+$ is also an abelian group.
66. An endomorphism which is also an isomorphism is called an *automorphism*.
67. The automorphisms of a group $A$ form a group under function composition called the *automorphism group* of $A$, denoted $\text{Aut}(A)$.
68. For an endomorphism of a finite group $\epsilon : A \to A$ to be invertible, i.e. for $\epsilon$ to be an automorphism, it must be the case that $\text{im}(\epsilon) \cong A$.
69. $\mathbb{Z}/n\mathbb{Z}^+$ is always cyclic of order $n$, so an endomorphism $\epsilon$ on it is fully determined by $\epsilon(1)$.
70. In a cyclic group $\mathbb{Z}/n\mathbb{Z}^+$, the elements which generate the group through addition are the congruence classes of numbers relatively prime to $n$.
71. An automorphism of an additive group must preserve addition as well as inverses, so $\epsilon(1)$ must be a generator of $\mathbb{Z}/n\mathbb{Z}^+$.
72. This means that the order of $\text{Aut}(\mathbb{Z}/n\mathbb{Z}^+)$ is given by $\varphi(n)$.

## Exercises

1. The canonical projection to a quotient group is always surjective. Is it possible for a canonical projection between groups $\pi : A \to A/B$ to be injective? If so, what sort of group would $B$ have to be?
2. Demonstrate that if $H$ is a subgroup of an abelian group $G$, then $G/H$ is an abelian group.
3. Prove that $\text{Aut}(\mathbb{Z}/n\mathbb{Z}^+) \cong \mathbb{Z}/n\mathbb{Z}^\times$.
