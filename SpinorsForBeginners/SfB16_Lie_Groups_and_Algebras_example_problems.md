---
layout: default
title: "Lie Groups and Lie Algebras"
---

# Example Problems: Lie Groups and Lie Algebras

This lecture introduces the mathematical framework for continuous symmetries.

## Problem 1: What is a Lie Group?

A Lie group is a group that is also a differentiable manifold, such that the group operations (multiplication and inversion) are smooth functions.

Which of the following are Lie groups?
a) The set of real numbers under addition, $(\mathbb{R}, +)$.
b) The set of integers under addition, $(\mathbb{Z}, +)$.
c) The set of 2x2 invertible real matrices, GL(2, $\mathbb{R}$).
d) The set of 2x2 real matrices with determinant 1, SL(2, $\mathbb{R}$).
e) The group of rotations in 3D, SO(3).
f) The permutation group of 3 elements, $S_3$.

For those that are Lie groups, what is the dimension of the manifold?

## Problem 2: The Lie Algebra

The Lie algebra is the tangent space of the Lie group at the identity element. It is a vector space equipped with a binary operation called the Lie bracket.
The elements of the Lie algebra are the "generators" of the group transformations.
An element of the group close to the identity can be written as $g = I + \epsilon X + O(\epsilon^2)$, where X is an element of the Lie algebra.
More generally, group elements can be obtained by exponentiating algebra elements: $g = \exp(X)$.

a) The group U(1) is the set of complex numbers $z$ with $|z|=1$. We can write $z=e^{i\theta}$.
   What is the manifold of this group?
   What is the identity element?
   What is the Lie algebra of U(1)? (Hint: consider $\theta$ to be small). What is its dimension?

b) The group SO(2) is the group of 2x2 rotation matrices $R(\theta)$.
   Find the generator of this group by taking the derivative of $R(\theta)$ with respect to $\theta$ at $\theta=0$. Let's call it T.
   Show that any rotation matrix can be written as $R(\theta) = \exp(\theta T)$.

## Problem 3: The Lie Bracket

The Lie bracket (or commutator) of two elements X, Y in the Lie algebra is defined as $[X, Y] = XY - YX$.
The Lie algebra is closed under the Lie bracket: if X and Y are in the algebra, so is [X, Y].
The coefficients in the expansion of the commutator of the basis elements are called the "structure constants".
$[T_a, T_b] = i f_{abc} T_c$

a) The Lie algebra of SU(2) is spanned by the Pauli matrices $\sigma_i$.
   However, the Pauli matrices are Hermitian, while the generators of a Lie algebra are usually defined to be anti-Hermitian for a unitary group. The generators are $T_a = \frac{1}{2}\sigma_a$.
   Calculate the commutator $[T_1, T_2]$.
b) Show that the result is proportional to $T_3$. What are the structure constants $f_{123}$ of SU(2)?
c) The Lie algebra of SO(3) is spanned by three 3x3 matrices $L_x, L_y, L_z$.
   $L_x = \begin{pmatrix} 0 & 0 & 0 \\ 0 & 0 & -1 \\ 0 & 1 & 0 \end{pmatrix}$, $L_y = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ -1 & 0 & 0 \end{pmatrix}$, $L_z = \begin{pmatrix} 0 & -1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}$
   Calculate the commutator $[L_x, L_y]$ and show that it is equal to $L_z$.
d) This shows that the Lie algebras of SU(2) and SO(3) are isomorphic. What does this imply about the relationship between the groups themselves?

## Problem 4: The Adjoint Representation

The Lie algebra itself can form a representation of the group, called the adjoint representation.
For each element g of the group, the action on an element Y of the algebra is given by:
$Y \rightarrow g Y g^{-1}$

Let's consider the group SU(2) and its algebra su(2).
The algebra is a 3D real vector space, spanned by the Pauli matrices. An element of the algebra can be written as $Y = y_i \sigma_i$.
The group acts on this vector of coefficients $(y_1, y_2, y_3)$.

a) Let $g = \exp(-i\frac{\theta}{2}\sigma_3)$ be a rotation around the z-axis.
b) Let $Y = \sigma_1$. Calculate the transformed algebra element $Y\prime = g \sigma_1 g^{-1}$.
c) Express $Y\prime$ as a linear combination of the Pauli matrices to find the new vector of coefficients $(y_1\prime, y_2\prime, y_3\prime)$.
d) Show that this transformation corresponds to a rotation of the vector $(1,0,0)$ by an angle $\theta$ around the z-axis.
e) This shows that the adjoint representation of SU(2) is the 3D vector representation, SO(3).

## Problem 5: From Algebra to Group

Not every Lie algebra corresponds to a unique Lie group. For example, the same Lie algebra so(3) ~ su(2) corresponds to both SO(3) and SU(2).
The exponential map takes the algebra to the group, but it may not be surjective (cover the whole group) or injective (one-to-one).

a) For the group U(1), the algebra is $\mathbb{R}$. The exponential map is $\theta \rightarrow e^{i\theta}$. Is this map surjective? Is it injective?
b) For the group SO(3), the algebra is the space of 3x3 anti-symmetric matrices. Any rotation can be written as $\exp(X)$ for some X in the algebra. Is the map injective? (Hint: consider a rotation by $2\pi$).
c) The groups with the same Lie algebra are locally isomorphic. One of them is "simply connected" (has no holes), and is called the universal covering group. All other groups with the same algebra are quotients of the universal cover.
   Which is the universal covering group for the so(3) algebra: SO(3) or SU(2)?

# Solutions to Example Problems: Lie Groups and Lie Algebras

## Problem 1: What is a Lie Group?

a) **(\mathbb{R}, +)**: Yes. Dimension 1.
b) **(\mathbb{Z}, +)**: No. It is not a differentiable manifold.
c) **GL(2, $\mathbb{R}$)**: Yes. Dimension 4.
d) **SL(2, $\mathbb{R}$)**: Yes. Dimension 3.
e) **SO(3)**: Yes. Dimension 3.
f) **$S_3$**: No. It is a finite group, not a manifold.

## Problem 2: The Lie Algebra

a) **U(1)**:
- Manifold: The unit circle $S^1$.
- Identity element: $z=1$.
- Lie algebra: The tangent space at $z=1$ is the imaginary axis. The algebra is $i\mathbb{R}$, isomorphic to $\mathbb{R}$. Dimension 1.

b) **SO(2)**:
- Generator: $T = \frac{dR}{d\theta}|_{\theta=0} = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$.
- Exponentiation: $\exp(\theta T) = I(\cos\theta) + T(\sin\theta) = R(\theta)$.

## Problem 3: The Lie Bracket

a) **Calculate the commutator $[T_1, T_2]$.**
$[T_1, T_2] = \frac{1}{4}[\sigma_1, \sigma_2] = \frac{1}{4}(2i\sigma_3) = iT_3$.

b) **What are the structure constants $f_{123}$ of SU(2)?**
$[T_a, T_b] = i f_{abc} T_c$. So $f_{123}=1$. The structure constants are $\epsilon_{abc}$.

c) **Calculate the commutator $[L_x, L_y]$ and show that it is equal to $L_z$.**
$[L_x, L_y] = L_z$.

d) **This shows that the Lie algebras of SU(2) and SO(3) are isomorphic.**
This implies the groups are locally isomorphic.

## Problem 4: The Adjoint Representation

b) **Let $Y = \sigma_1$. Calculate the transformed algebra element $Y' = g \sigma_1 g^{-1}$.**
$Y' = \sigma_1\cos\theta + \sigma_2\sin\theta$.

c) **Express $Y'$ as a linear combination of the Pauli matrices.**
The new vector of coefficients is $(\cos\theta, \sin\theta, 0)$.

d) **Show that this corresponds to a rotation of the vector $(1,0,0)$ by an angle $\theta$ around the z-axis.**
This is the correct transformation for a vector.

## Problem 5: From Algebra to Group

a) **For the group U(1), is the map surjective? Is it injective?**
Surjective: Yes. Injective: No ($\theta$ and $\theta+2\pi n$ map to the same element).

b) **For the group SO(3), is the map injective?**
No. A rotation by $2\pi$ around any axis is the identity.

c) **Which is the universal covering group for the so(3) algebra: SO(3) or SU(2)?**
SU(2) is simply connected, so it is the universal covering group.