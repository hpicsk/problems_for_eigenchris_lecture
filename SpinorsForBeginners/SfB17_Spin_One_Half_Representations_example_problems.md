# Example Problems: Spin-1/2 Representations

This lecture focuses on the fundamental building block of many physical theories: the spin-1/2 representation of the rotation and Lorentz groups.

## Problem 1: The Spin-1/2 Rep of SU(2)

The group SU(2) is the group of 2x2 unitary matrices with determinant 1. This is the spin-1/2 representation.
A general element can be written as $U = \begin{pmatrix} a & b \\ -b^* & a^* \end{pmatrix}$ with $|a|^2+|b|^2=1$.
It can also be parameterized by an angle $\theta$ and a unit vector axis $\hat{n}$:
$U(\hat{n}, \theta) = \exp(-i\frac{\theta}{2} \hat{n}\cdot\vec{\sigma})$

a) Show that $\det(U(\hat{n}, \theta)) = 1$.
b) Show that $U(\hat{n}, \theta)$ is unitary.
c) Calculate the matrix for a rotation of $\pi$ around the x-axis.
d) Calculate the matrix for a rotation of $\pi/2$ around the y-axis.

## Problem 2: The Vector Representation of SO(3)

The group SO(3) is the group of 3x3 real orthogonal matrices with determinant 1. This is the spin-1 (vector) representation.
A rotation by angle $\theta$ around axis $\hat{n}$ can be written using Rodrigues' rotation formula:
$R(\hat{n}, \theta) v = (\cos\theta) v + (1-\cos\theta)(\hat{n}\cdot v)\hat{n} + (\sin\theta) \hat{n}\times v$

a) Let's consider a rotation by $\pi/2$ around the z-axis, $\hat{n}=(0,0,1)$.
   Use the formula to find the images of the basis vectors $e_x, e_y, e_z$.
b) From the results in (a), construct the 3x3 matrix for this rotation.
c) The character of this rotation is the trace of the matrix. What is $\chi_1(\pi/2)$?

## Problem 3: The SU(2) -> SO(3) Homomorphism

There is a 2-to-1 homomorphism from SU(2) to SO(3).
A vector $v=(x,y,z)$ can be represented by a traceless hermitian matrix $V = v\cdot\sigma$.
The rotation is implemented by $V\prime = U V U^\dagger$.
The new vector $v\prime$ is found by decomposing $V\prime$ back into the Pauli basis.

a) Let $U$ be the SU(2) matrix for a rotation of $\pi/2$ around the z-axis.
b) Let $v$ be the vector $(1, 0, 0)$. Write down the matrix $V$.
c) Calculate $V\prime = U V U^\dagger$.
d) From $V\prime$, determine the new vector $v\prime$. Does this match the result of rotating the vector $(1,0,0)$ by 90 degrees around the z-axis?
e) What happens if you use $U$ corresponding to a rotation of $2\pi$? What does $V\prime$ become? What about a rotation of $4\pi$?

## Problem 4: Lorentz Group Spin-1/2 Representations

The proper orthochronous Lorentz group SO+(1,3) has a Lie algebra that is isomorphic to the algebra of SU(2) x SU(2). This means its irreducible representations are labeled by a pair of spins $(j_L, j_R)$.

The fundamental spinor representations are:
- The Left-handed Weyl Spinor: $(\frac{1}{2}, 0)$ representation. Transforms under a matrix $L \in SL(2,C)$.
- The Right-handed Weyl Spinor: $(0, \frac{1}{2})$ representation. Transforms under a matrix $R = (L^\dagger)^{-1}$.

A Lorentz transformation $\Lambda$ is mapped to a matrix $A \in SL(2,C)$.
A left-handed spinor $\psi_L$ transforms as $\psi_L\prime = A \psi_L$.
A right-handed spinor $\psi_R$ transforms as $\psi_R\prime = (A^\dagger)^{-1} \psi_R$.

a) A rotation by angle $\theta$ around axis $\hat{n}$ is represented by $A = \exp(-i\frac{\theta}{2}\hat{n}\cdot\sigma)$.
   How does $(A^\dagger)^{-1}$ relate to A in this case? How do left and right handed spinors transform under rotations?
b) A boost by rapidity $\eta$ along axis $\hat{n}$ is represented by $A = \exp(-\frac{\eta}{2}\hat{n}\cdot\sigma)$.
   How does $(A^\dagger)^{-1}$ relate to A in this case? How do left and right handed spinors transform under boosts?

## Problem 5: Dirac Spinors

A Dirac spinor is a 4-component object that is the direct sum of a left-handed and a right-handed Weyl spinor: $\psi = \begin{pmatrix} \psi_L \\ \psi_R \end{pmatrix}$. This is the $(\frac{1}{2}, 0) \oplus (0, \frac{1}{2})$ representation.

The transformation law is:
$\psi\prime = S \psi = \begin{pmatrix} A & 0 \\ 0 & (A^\dagger)^{-1} \end{pmatrix} \psi$

a) Write down the transformation matrix S for a rotation around the z-axis.
b) Write down the transformation matrix S for a boost along the z-axis.
c) The Dirac mass term in the Lagrangian is $m\bar{\psi}\psi = m(\psi_L^\dagger \psi_R + \psi_R^\dagger \psi_L)$.
   Show that this term is Lorentz invariant.
   (Hint: Show that $\psi_L\prime^† \psi_R\prime$ = $\psi_L^\dagger \psi_R$).
d) Can you construct a Lorentz-invariant mass term using only left-handed spinors? Why is this important for the Standard Model (before neutrino masses were discovered)? 

# Solutions to Example Problems: Spin-1/2 Representations

## Problem 1: The Spin-1/2 Rep of SU(2)

a) **Show that $\det(U(\hat{n}, \theta)) = 1$.**
$\det(\exp(M)) = \exp(\text{Tr}(M))$. The Pauli matrices are traceless, so the trace of the exponent is zero. So the determinant is 1.

b) **Show that $U(\hat{n}, \theta)$ is unitary.**
$U^\dagger = \exp(i\frac{\theta}{2} \hat{n}\cdot\vec{\sigma}) = U^{-1}$.

c) **Calculate the matrix for a rotation of $\pi$ around the x-axis.**
$U = -i\sigma_1 = \begin{pmatrix} 0 & -i \\ -i & 0 \end{pmatrix}$.

d) **Calculate the matrix for a rotation of $\pi/2$ around the y-axis.**
$U = \frac{1}{\sqrt{2}}(I - i\sigma_2) = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix}$.

## Problem 2: The Vector Representation of SO(3)

a) **Let's consider a rotation by $\pi/2$ around the z-axis, $\hat{n}=(0,0,1)$.**
$R(e_x) = e_y$. $R(e_y) = -e_x$. $R(e_z) = e_z$.

b) **From the results in (a), construct the 3x3 matrix for this rotation.**
$R = \begin{pmatrix} 0 & -1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix}$.

c) **The character of this rotation is the trace of the matrix. What is $\chi_1(\pi/2)$?**
$\chi_1(\pi/2) = 1$.

## Problem 3: The SU(2) -> SO(3) Homomorphism

a) **Let $U$ be the SU(2) matrix for a rotation of $\pi/2$ around the z-axis.**
$U = \exp(-i\frac{\pi/2}{2}\sigma_3) = \frac{1}{\sqrt{2}}(I-i\sigma_3)$.

b) **Let $v$ be the vector $(1, 0, 0)$. Write down the matrix $V$.**
$V = \sigma_1$.

c) **Calculate $V' = U V U^\dagger$.**
$V' = \sigma_2$.

d) **From $V'$, determine the new vector $v'$.**
$v'=(0,1,0)$. This is correct.

e) **What happens if you use $U$ corresponding to a rotation of $2\pi$?**
$U=-I$. $V' = V$. The vector is unchanged.

## Problem 4: Lorentz Group Spin-1/2 Representations

a) **How does $(A^\dagger)^{-1}$ relate to A in this case?**
For a rotation, $A$ is unitary, so $(A^\dagger)^{-1} = A$. Left and right handed spinors transform in the same way.

b) **How does $(A^\dagger)^{-1}$ relate to A in this case?**
For a boost, $A$ is Hermitian, so $(A^\dagger)^{-1} = A^{-1}$. Left and right handed spinors transform differently.

## Problem 5: Dirac Spinors

a) **Write down the transformation matrix S for a rotation around the z-axis.**
$S = \begin{pmatrix} A & 0 \\ 0 & A \end{pmatrix}$ where $A = \exp(-i\frac{\theta}{2}\sigma_3)$.

b) **Write down the transformation matrix S for a boost along the z-axis.**
$S = \begin{pmatrix} A & 0 \\ 0 & A^{-1} \end{pmatrix}$ where $A = \exp(-\frac{\eta}{2}\sigma_3)$.

c) **Show that this term is Lorentz invariant.**
$\psi_L'^\dagger \psi_R' = (A\psi_L)^\dagger (A^\dagger)^{-1}\psi_R = \psi_L^\dagger A^\dagger (A^\dagger)^{-1}\psi_R = \psi_L^\dagger \psi_R$.

d) **Can you construct a Lorentz-invariant mass term using only left-handed spinors?**
No. A term like $\psi_L^\dagger\psi_L$ is not Lorentz invariant. This is why Weyl spinors must be massless.