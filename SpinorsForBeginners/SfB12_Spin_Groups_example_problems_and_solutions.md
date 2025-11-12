# Example Problems and Solutions: Spin Groups

This lecture introduces the Spin group, which is the double cover of the special orthogonal group SO(n).

## Problem 1: The Pin and Spin Groups

The Pin group, Pin(V,q), is a subgroup of the Clifford algebra Cl(V,q) consisting of products of vectors with norm +/-1.
The Spin group, Spin(V,q), is the subgroup of Pin(V,q) consisting of products of an even number of vectors.

Let's consider Euclidean 3D space, and the Clifford algebra $Cl_{3,0}$.
The Spin group is $Spin(3)$.

a) An element of Spin(3) can be written as $R = \exp(-\frac{\theta}{2} \hat{n} \cdot \sigma_{123})$, where $\sigma_{123}$ is a bivector for the plane of rotation.
   In $Cl_{3,0}$, the bivectors are $e_1e_2, e_2e_3, e_3e_1$. These behave like the Pauli matrices (up to a factor of i).
   A rotation is given by $R = \cos(\theta/2) - \sin(\theta/2) e_1e_2$. (This is for a rotation in the 1-2 plane).

b) How does this element act on a vector $v$? The action is given by the "twisted" adjoint action: $v' = R v R^{-1}$.
   Let $v = e_1$. Calculate $v'$ for a rotation of $\theta=\pi/2$ in the 1-2 plane.

c) The elements of Spin(3) are isomorphic to the unit quaternions, and also to SU(2).
   Show that $R = \cos(\theta/2) - \sin(\theta/2) e_1e_2$ squares to -1 for $\theta=\pi$.
   What is the relationship between the element $e_1e_2$ in the Clifford algebra and the imaginary unit 'i' in complex numbers?

### Solution 1

a) **An element of Spin(3) can be written as $R = \cos(\theta/2) - \sin(\theta/2) e_1e_2$.**

This is a rotor for a rotation by $\theta$ in the 1-2 plane.

b) **Let $v = e_1$. Calculate $v'$ for a rotation of $\theta=\pi/2$ in the 1-2 plane.**

$$R = \cos(\pi/4) - \sin(\pi/4)e_1e_2 = \frac{1}{\sqrt{2}}(1-e_1e_2)$$

$$R^{-1} = \frac{1}{\sqrt{2}}(1+e_1e_2)$$

$$v' = R v R^{-1} = \frac{1}{2}(1-e_1e_2)e_1(1+e_1e_2) = e_2$$

c) **Show that $R = \cos(\theta/2) - \sin(\theta/2) e_1e_2$ squares to -1 for $\theta=\pi$.**

For $\theta=\pi$, $R = -e_1e_2$. $R^2 = (-e_1e_2)^2 = e_1e_2e_1e_2 = -1$.

**What is the relationship between the element $e_1e_2$ in the Clifford algebra and the imaginary unit 'i' in complex numbers?**

The element $e_1e_2$ squares to -1, just like the imaginary unit $i$. It generates rotations in the 1-2 plane, just as $i$ generates rotations in the complex plane.

## Problem 2: The Double Cover

The map from the Spin group to the rotation group is 2-to-1.
The map $\rho: Spin(n) \rightarrow SO(n)$ is given by $\rho(R)v = R v R^{-1}$.

a) In Spin(3), consider the element $R_{2\pi}$ corresponding to a rotation by $2\pi$.
   From the formula $R = \cos(\theta/2) - \sin(\theta/2) \hat{n}\cdot\sigma_{123}$, what is $R_{2\pi}$?

b) How does this element act on a vector v? i.e., what is $\rho(R_{2\pi})$?

c) Now consider the element $R_{4\pi}$. What is this element in Spin(3)?

d) This shows that there are two elements in Spin(3) (R=1 and R=-1) that map to the identity rotation in SO(3). This is the essence of the double cover.

### Solution 2

a) **In Spin(3), consider the element $R_{2\pi}$ corresponding to a rotation by $2\pi$. What is $R_{2\pi}$?**

$$R_{2\pi} = \cos(\pi) - \sin(\pi)e_1e_2 = -1$$

b) **How does this element act on a vector v? i.e., what is $\rho(R_{2\pi})$?**

$$v' = R_{2\pi} v R_{2\pi}^{-1} = (-1)v(-1) = v$$

The action is the identity transformation.

c) **Now consider the element $R_{4\pi}$. What is this element in Spin(3)?**

$$R_{4\pi} = \cos(2\pi) - \sin(2\pi)e_1e_2 = 1$$

d) **This shows that there are two elements in Spin(3) (R=1 and R=-1) that map to the identity rotation in SO(3).**

This is correct.

## Problem 3: The Spin Group of Minkowski Spacetime

For Minkowski spacetime, we are interested in $Spin(1,3)$.
This group is the double cover of the proper orthochronous Lorentz group, $SO^+(1,3)$.
The group $Spin(1,3)$ is isomorphic to $SL(2, \mathbb{C})$, the group of 2×2 complex matrices with determinant 1.

a) An element of $SL(2, \mathbb{C})$ can be parameterized by a complex 3-vector $\vec{w} = \vec{\theta} + i\vec{\eta}$.
   $A = \exp(-i\vec{w}\cdot\vec{\sigma}/2)$.
   What do the real part ($\vec{\theta}$) and imaginary part ($\vec{\eta}$) of this vector correspond to physically?

b) How does an element $A \in SL(2, \mathbb{C})$ act on a 4-vector?
   A 4-vector $x^\mu$ can be represented as a 2×2 Hermitian matrix $X = x^\mu \sigma_\mu$.
   The transformation is $X' = A X A^\dagger$.
   Let A correspond to a boost in the z-direction. $A = \exp(-\eta/2 \sigma_3)$.
   Let $X = \sigma_0 = I$. Calculate $X'$ and show that it corresponds to the 4-vector of a boosted observer.

### Solution 3

a) **What do the real part ($\vec{\theta}$) and imaginary part ($\vec{\eta}$) of this vector correspond to physically?**

The real part $\vec{\theta}$ corresponds to rotations, and the imaginary part $\vec{\eta}$ corresponds to boosts.

b) **Let A correspond to a boost in the z-direction. $A = \exp(-\eta/2 \sigma_3)$. Let $X = \sigma_0 = I$. Calculate $X'$ and show that it corresponds to the 4-vector of a boosted observer.**

For a boost, we use $A = \exp(\eta/2 \sigma_3) = \begin{pmatrix} e^{\eta/2} & 0 \\ 0 & e^{-\eta/2} \end{pmatrix}$.

$$X' = A X A^\dagger = A I A^\dagger = A A^\dagger = \begin{pmatrix} e^{\eta} & 0 \\ 0 & e^{-\eta} \end{pmatrix} = \cosh\eta I + \sinh\eta \sigma_3$$

This corresponds to the 4-vector $(\cosh\eta, 0, 0, \sinh\eta)$.

## Problem 4: Spinor Representations

The Spin group acts naturally on spinors. Spinors are, by definition, objects that transform under the spin representation of the Spin group.
In the Clifford algebra picture, spinors are elements of a minimal left ideal, and the Spin group is a subset of the algebra, so it acts on the ideal by left multiplication.

a) For Spin(3) ~ SU(2), the fundamental representation is the 2-component Pauli spinors.
   How does the element $R = \cos(\theta/2) - \sin(\theta/2) e_1e_2$ act on a spinor $\psi$?

b) For Spin(1,3) ~ SL(2,C), there are two fundamental representations, the left- and right-handed Weyl spinors.
   How does an element $A \in SL(2, \mathbb{C})$ act on a left-handed spinor $\psi_L$?
   How does it act on a right-handed spinor $\psi_R$? (Hint: the transformation is different).

### Solution 4

a) **For Spin(3) ~ SU(2), how does the element $R = \cos(\theta/2) - \sin(\theta/2) e_1e_2$ act on a spinor $\psi$?**

It acts by left multiplication. The spinor is an element of a minimal left ideal of the Clifford algebra.

b) **For Spin(1,3) ~ SL(2,C), how does an element $A \in SL(2, \mathbb{C})$ act on a left-handed spinor $\psi_L$? How does it act on a right-handed spinor $\psi_R$?**

A left-handed spinor transforms as $\psi_L' = A\psi_L$.

A right-handed spinor transforms as $\psi_R' = (A^\dagger)^{-1}\psi_R$.

## Problem 5: Topology of Spin Groups

The topological properties of the Spin groups are crucial.

a) The group SO(3) is not simply connected. You can't shrink a loop that corresponds to a $2\pi$ rotation to a point. (This is the "Dirac belt trick").

b) The group SU(2) ~ Spin(3) *is* simply connected. It is the universal cover of SO(3).
   What is the manifold of SU(2)? (Hint: it's the 3-sphere $S^3$).

c) The Lorentz group $SO^+(1,3)$ is also not simply connected.

d) Its universal cover is $Spin(1,3) \cong SL(2, \mathbb{C})$. What is the manifold of $SL(2, \mathbb{C})$?

### Solution 5

a) **The group SO(3) is not simply connected.**

Correct.

b) **The group SU(2) ~ Spin(3) *is* simply connected. What is the manifold of SU(2)?**

The manifold of SU(2) is the 3-sphere $S^3$.

c) **The Lorentz group $SO^+(1,3)$ is also not simply connected.**

Correct.

d) **Its universal cover is $Spin(1,3) \cong SL(2, \mathbb{C})$. What is the manifold of $SL(2, \mathbb{C})$?**

The manifold of $SL(2, \mathbb{C})$ is $\mathbb{R}^3 \times S^3$. It is simply connected.