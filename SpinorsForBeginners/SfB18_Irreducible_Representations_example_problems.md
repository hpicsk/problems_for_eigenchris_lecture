This lecture focuses on the building blocks of representation theory: the irreducible representations (irreps).

## Problem 1: What is a Representation?

Let G be a group. A representation of G is a mapping D from group elements g to a set of linear operators (or matrices) D(g), such that the group multiplication is preserved:
$D(g_1) D(g_2) = D(g_1 g_2)$

a) Consider the group $C_3$, the cyclic group of order 3 (elements {e, a, a^2} with $a^3=e$).
   Show that the following is a representation of $C_3$:
   $D(e) = 1$, $D(a) = e^{i2\pi/3}$, $D(a^2) = e^{i4\pi/3}$.
b) Show that the following is also a representation of $C_3$:
   $D(e) = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$, $D(a) = \begin{pmatrix} \cos(2\pi/3) & -\sin(2\pi/3) \\ \sin(2\pi/3) & \cos(2\pi/3) \end{pmatrix}$, $D(a^2) = D(a)^2$.
c) Is the trivial representation $D(g)=1$ for all g, always a representation? Is it always irreducible?

## Problem 2: Reducibility

A representation D is **reducible** if there is a non-trivial subspace V that is invariant under all the representation matrices. That is, for any vector $v \in V$, $D(g)v$ is also in V for all $g \in G$.
If no such subspace exists, the representation is **irreducible**.

a) Consider the representation from Problem 1b. Is this representation reducible over the complex numbers?
   (Hint: Find the eigenvectors of the matrix D(a). Are the subspaces spanned by these eigenvectors invariant?)
b) Consider the representation of SO(2) (rotations in a plane) by 2x2 rotation matrices. Is this reducible over the real numbers? Is it reducible over the complex numbers?
c) A representation is **completely reducible** if it can be written as a direct sum of irreducible representations. This means all the matrices can be simultaneously brought to a block-diagonal form.
   $D(g) = \begin{pmatrix} D_1(g) & 0 \\ 0 & D_2(g) \end{pmatrix}$
   For finite groups, all representations are completely reducible.

## Problem 3: Schur's Lemma

Schur's Lemma is a fundamental result in representation theory.
Part 1: If D is an irreducible representation, and A is a matrix that commutes with all representation matrices ($A D(g) = D(g) A$ for all g), then A must be a multiple of the identity matrix, $A = \lambda I$.
Part 2: If $D_1$ and $D_2$ are two *inequivalent* irreducible representations, and A is a matrix such that $A D_1(g) = D_2(g) A$ for all g, then A must be the zero matrix.

a) Use Schur's Lemma to show that all irreducible representations of an Abelian group are one-dimensional.
b) Let D be an irrep of a group G. If there is an element $g_0$ in the center of the group (it commutes with all other elements), what can you say about the matrix $D(g_0)$?

## Problem 4: Characters and Orthogonality

The character of a representation is the trace of the matrices: $\chi(g) = \text{Tr}(D(g))$.
Characters are constant on conjugacy classes.
The great orthogonality theorem for characters states that for two irreps $D_i$ and $D_j$:
$\frac{1}{|G|} \sum_{g \in G} \chi_i(g) \chi_j(g)^* = \delta_{ij}$

a) For the group $C_3$, there are three irreps. Two are complex conjugates of each other, and one is the trivial representation. Write down the characters for these three irreps.
b) Verify the orthogonality relation for the characters of $C_3$.
c) A general representation D can be decomposed into a sum of irreps: $D = \bigoplus_i n_i D_i$.
   The character of D is $\chi = \sum_i n_i \chi_i$.
   Show how to use the orthogonality theorem to find the coefficients $n_i$ (the number of times irrep i appears in D).
   $n_i = \frac{1}{|G|} \sum_g \chi(g) \chi_i(g)^*$

## Problem 5: Irreps of SU(2)

The irreducible representations of SU(2) are labeled by a half-integer $j = 0, 1/2, 1, 3/2, \dots$.
The dimension of the spin-j representation is $2j+1$.

a) What are the dimensions of the first four irreps of SU(2)?
b) The character of the spin-j representation for a rotation by an angle $\theta$ is given by:
   $\\chi_j(\theta) = \frac{\sin((j+1/2)\theta)}{\sin(\theta/2)}$
   Verify this formula for the spin-1/2 (j=1/2) and spin-1 (j=1) cases.
   (For spin-1, the representation is the 3D rotation matrices of SO(3)).
c) Use the character formula to verify the Clebsch-Gordan decomposition for $\frac{1}{2} \otimes \frac{1}{2} = 1 \oplus 0$.
   (Show that $\chi_{1/2}(\theta) \cdot \chi_{1/2}(\theta) = \chi_1(\theta) + \chi_0(\theta)$).

# Solutions to Example Problems: Irreducible Representations

## Problem 1: What is a Representation?

a) **Show that the following is a representation of $C_3$:**
It is a representation.

b) **Show that the following is also a representation of $C_3$:**
It is a representation.

c) **Is the trivial representation $D(g)=1$ for all g, always a representation? Is it always irreducible?**
Yes, it is always a representation and always irreducible.

## Problem 2: Reducibility

a) **Consider the representation from Problem 1b. Is this representation reducible over the complex numbers?**
Yes. The eigenvectors of D(a) span 1D invariant subspaces.

b) **Consider the representation of SO(2) by 2x2 rotation matrices. Is this reducible over the real numbers? Is it reducible over the complex numbers?**
Irreducible over the reals, reducible over the complexes.

## Problem 3: Schur's Lemma

a) **Use Schur's Lemma to show that all irreducible representations of an Abelian group are one-dimensional.**
In an Abelian group, all elements commute with each other. So for any element h, D(h) commutes with all matrices of the representation. If the representation is irreducible, D(h) must be a multiple of the identity. This must hold for all h. A representation where all matrices are multiples of the identity is reducible unless it is 1-dimensional.

b) **Let D be an irrep of a group G. If there is an element $g_0$ in the center of the group, what can you say about the matrix $D(g_0)$?**
By Schur's Lemma, $D(g_0)$ must be a multiple of the identity matrix.

## Problem 4: Characters and Orthogonality

a) **For the group $C_3$, write down the characters for these three irreps.**
$\chi_1 = (1,1,1)$, $\chi_2 = (1, e^{i2\pi/3}, e^{i4\pi/3})$, $\chi_3 = (1, e^{-i2\pi/3}, e^{-i4\pi/3})$.

b) **Verify the orthogonality relation for the characters of $C_3$.**
The relations hold.

c) **Show how to use the orthogonality theorem to find the coefficients $n_i$.**
$n_i = \frac{1}{|G|} \sum_g \chi(g) \chi_i(g)^*$.

## Problem 5: Irreps of SU(2)

a) **What are the dimensions of the first four irreps of SU(2)?**
j=0: 1, j=1/2: 2, j=1: 3, j=3/2: 4.

b) **Verify this formula for the spin-1/2 (j=1/2) and spin-1 (j=1) cases.**
j=1/2: $\chi_{1/2}(\theta) = 2\cos(\theta/2)$. Correct.
j=1: $\chi_1(\theta) = 1+2\cos\theta$. Correct.

c) **Use the character formula to verify the Clebsch-Gordan decomposition for $\frac{1}{2} \otimes \frac{1}{2} = 1 \oplus 0$.**
$\chi_{1/2}(\theta) \cdot \chi_{1/2}(\theta) = (2\cos(\theta/2))^2 = 2(1+\cos\theta)$.
$\chi_1(\theta) + \chi_0(\theta) = (1+2\cos\theta) + 1 = 2+2\cos\theta$. The relation holds.