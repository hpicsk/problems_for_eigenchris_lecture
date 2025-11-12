---
layout: default
title: "Tensor Product Representations"
---

# Example Problems: Tensor Product Representations

This lecture likely covers how to combine representations of a group, for example, to describe a system with multiple particles.

## Problem 1: Tensor Product of Vector Spaces

Let V and W be two vector spaces. The tensor product $V \otimes W$ is a new vector space.
If {v_i} is a basis for V and {w_j} is a basis for W, then {v_i \otimes w_j} is a basis for $V \otimes W$.

a) If V is a 2-dimensional space (e.g., the spin states of one electron) and W is a 3-dimensional space, what is the dimension of $V \otimes W$?
b) Let V have basis {e_1, e_2} and W have basis {f_1, f_2}.
   A vector in $V \otimes W$ is given by $z = a(e_1\otimes f_1) + b(e_1\otimes f_2) + c(e_2\otimes f_1) + d(e_2\otimes f_2)$.
   Can every vector in $V \otimes W$ be written as a "simple tensor" $v \otimes w$ for some $v \in V, w \in W$?
   (Hint: Consider the vector $e_1\otimes f_2 + e_2\otimes f_1$. This is an entangled state).

## Solution 1: Tensor Product of Vector Spaces

a) **If V is a 2-dimensional space and W is a 3-dimensional space, what is the dimension of $V \otimes W$?**
The dimension is $2 \times 3 = 6$.

b) **Can every vector in $V \otimes W$ be written as a "simple tensor" $v \otimes w$?**
No. A general vector is a linear combination of basis vectors. The vector $e_1\otimes f_2 + e_2\otimes f_1$ is an example of an entangled state that cannot be written as a simple tensor.

## Problem 2: Tensor Product of Group Representations

If $D_1(g)$ and $D_2(g)$ are two representations of a group G, the tensor product representation is given by the Kronecker product of the matrices:
$D(g) = D_1(g) \otimes D_2(g)$

Let's consider the group SU(2). The fundamental representation (spin-1/2) is given by 2x2 matrices $U$.
We want to combine two spin-1/2 particles. The total state space is the tensor product of the individual spaces. The transformation rule is $U \otimes U$.

a) Let $U(\theta) = \exp(-i\frac{\theta}{2}\sigma_3)$ be a rotation around the z-axis. Write down this 2x2 matrix.
b) Calculate the 4x4 matrix for the tensor product representation, $D(\theta) = U(\theta) \otimes U(\theta)$.
c) The character of a representation is the trace of the representation matrix, $\chi(g) = \text{Tr}(D(g))$.
   Calculate the character of the spin-1/2 representation, $\chi_{1/2}(\theta)$.
d) Calculate the character of the tensor product representation, $\chi_{1/2 \otimes 1/2}(\theta)$.
e) Show that $\chi_{1/2 \otimes 1/2}(\theta) = (\chi_{1/2}(\theta))^2$.

## Solution 2: Tensor Product of Group Representations

a) **Write down the 2x2 matrix for $U(\theta)$.**
$U(\theta) = \exp(-i\frac{\theta}{2}\sigma_3) = \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \end{pmatrix}$

b) **Calculate the 4x4 matrix for $D(\theta) = U(\theta) \otimes U(\theta)$.**
$D(\theta) = \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \end{pmatrix} \otimes \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \end{pmatrix} = \begin{pmatrix} e^{-i\theta} & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & e^{i\theta} \end{pmatrix}$

c) **Calculate the character $\chi_{1/2}(\theta)$.**
$\chi_{1/2}(\theta) = \text{Tr}(U(\theta)) = e^{-i\theta/2} + e^{i\theta/2} = 2\cos(\theta/2)$.

d) **Calculate the character $\chi_{1/2 \otimes 1/2}(\theta)$.**
$\chi_{1/2 \otimes 1/2}(\theta) = \text{Tr}(D(\theta)) = e^{-i\theta} + 1 + 1 + e^{i\theta} = 2 + 2\cos(\theta)$.
e) **Show that $\chi_{1/2 \otimes 1/2}(\theta) = (\chi_{1/2}(\theta))^2$.**
This is a general property of characters: $\text{Tr}(A \otimes B) = \text{Tr}(A)\text{Tr}(B)$.
Let's verify: $(\chi_{1/2}(\theta))^2 = (2\cos(\theta/2))^2 = 4\cos^2(\theta/2)$.
Using the identity $\cos(2x) = 2\cos^2(x) - 1$, we have $\cos(\theta) = 2\cos^2(\theta/2) - 1$, which gives $4\cos^2(\theta/2) = 2(\cos(\theta)+1) = 2+2\cos(\theta)$. This matches the result from (d).

## Problem 3: Clebsch-Gordan Decomposition

The tensor product of two irreducible representations (irreps) is generally reducible. It can be decomposed into a direct sum of irreps. For SU(2):
$j_1 \otimes j_2 = (j_1+j_2) \oplus (j_1+j_2-1) \oplus \dots \oplus |j_1-j_2|$

Let's combine two spin-1/2 particles. In the notation above, this is $\frac{1}{2} \otimes \frac{1}{2}$.
a) What is the decomposition of this tensor product into irreps?
b) What are the dimensions of these resulting irreps? (The dimension of the spin-j irrep is 2j+1).
c) Verify that the dimensions add up: $\text{dim}(\frac{1}{2}\otimes\frac{1}{2}) = \text{dim}(\text{result}_1) + \text{dim}(\text{result}_2)$.
d) What is the physical meaning of this decomposition? (Hint: total spin).

## Solution 3: Clebsch-Gordan Decomposition

a) **What is the decomposition of this tensor product into irreps?**
$\frac{1}{2} \otimes \frac{1}{2} = 1 \oplus 0$.

b) **What are the dimensions of these resulting irreps?**
j=1: 3, j=0: 1.

c) **Verify that the dimensions add up.**
$2 \times 2 = 3+1=4$.

d) **What is the physical meaning of this decomposition?**
Combining two spin-1/2 particles gives a total spin of 1 (triplet) or 0 (singlet).

## Problem 4: Finding the Clebsch-Gordan Coefficients

The decomposition involves finding the basis states for the new irreps. These are the states of total angular momentum.
The basis for the tensor product space is $|\\uparrow\\uparrow\rangle, |\uparrow\downarrow\rangle, |\downarrow\uparrow\rangle, |\downarrow\downarrow\rangle$.
The total spin operator is $S_z = S_{1z} \otimes I + I \otimes S_{2z}$.

a) Apply the total $S_z$ operator to each of the four basis states. What are the eigenvalues?
b) The state with the highest $S_z$ eigenvalue must be the highest weight state of the highest irrep.
   Which state is this? This is the $|j=1, m=1\rangle$ state.
c) The other states in the $j=1$ multiplet can be found by applying the lowering operator $S_- = S_{1-} \otimes I + I \otimes S_{2-}$.
   Apply $S_-$ to the $|1,1\rangle$ state to find the $|1,0\rangle$ state.
d) The remaining state, orthogonal to the $|1,0\rangle$ state, must be the $|0,0\rangle$ state (the singlet). Find this state.

## Solution 4: Finding the Clebsch-Gordan Coefficients

a) **Apply the total $S_z$ operator to each of the four basis states.**
Eigenvalues are $\hbar, 0, 0, -\hbar$.

b) **Which state is this? This is the $|j=1, m=1\rangle$ state.**
$|1,1\rangle = |\uparrow\uparrow\rangle$.

c) **Apply $S_-$ to the $|1,1\rangle$ state to find the $|1,0\rangle$ state.**
$|1,0\rangle = \frac{1}{\sqrt{2}}(|\uparrow\downarrow\rangle + |\downarrow\uparrow\rangle)$.

d) **The remaining state, orthogonal to the $|1,0\rangle$ state, must be the $|0,0\rangle$ state.**
$|0,0\rangle = \frac{1}{\sqrt{2}}(|\uparrow\downarrow\rangle - |\downarrow\uparrow\rangle)$.

## Problem 5: Lorentz Group Representations

The same ideas apply to the Lorentz group. The representations are labeled by $(j_L, j_R)$.
The tensor product of two representations $(j_{1L}, j_{1R}) \otimes (j_{2L}, j_{2R})$ decomposes into a direct sum of irreducible representations $(j_L, j_R)$. The possible values for $j_L$ are obtained from the decomposition of the SU(2) tensor product $j_{1L} \otimes j_{2L}$, and similarly the values for $j_R$ are obtained from $j_{1R} \otimes j_{2R}$.

The general rule is:
$(j_{1L}, j_{1R}) \otimes (j_{2L}, j_{2R}) = \bigoplus_{j_L, j_R} (j_L, j_R)$
where $j_L \in \{|j_{1L}-j_{2L}|, \dots, j_{1L}+j_{2L}\}$ and $j_R \in \{|j_{1R}-j_{2R}|, \dots, j_{1R}+j_{2R}\}$.

a) Let's combine a left-handed spinor $(\frac{1}{2}, 0)$ and a right-handed spinor $(0, \frac{1}{2})$.
   What is the decomposition of $(\frac{1}{2}, 0) \otimes (0, \frac{1}{2})$?
   (The SU(2) parts are $\frac{1}{2}\otimes 0 = \frac{1}{2}$ and $0\otimes\frac{1}{2} = \frac{1}{2}$).
b) The result is $(\frac{1}{2}, \frac{1}{2})$. What kind of object does this representation describe?
c) Let's combine two left-handed spinors: $(\frac{1}{2}, 0) \otimes (\frac{1}{2}, 0)$.
   What is the decomposition of this? (Use the SU(2) rule from Problem 3).
d) This shows that the product of two spinors can contain both a scalar part and a "spin-1" part. How is this used to build Lorentz invariant terms in a Lagrangian?

## Solution 5: Lorentz Group Representations

a) **What is the decomposition of $(\frac{1}{2}, 0) \otimes (0, \frac{1}{2})$?**
$(\frac{1}{2}, \frac{1}{2})$.

b) **What kind of object does this representation describe?**
A 4-vector.

c) **Let's combine two left-handed spinors: $(\frac{1}{2}, 0) \otimes (\frac{1}{2}, 0)$. What is the decomposition of this?**
$(1,0) \oplus (0,0)$.

d) **How is this used to build Lorentz invariant terms in a Lagrangian?**
The $(0,0)$ part is a Lorentz scalar. We can form a scalar by taking the product of two spinor fields.
