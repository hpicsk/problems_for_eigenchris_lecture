# SfB 10: Double Covers - Example Problems and Solutions

This lecture explains the concept of a double cover, focusing on the relationship between SU(2) and SO(3), and Spin(1,3) and SO+(1,3).

## Problem 1: The Circle covering the Circle

Let's start with a simple example.
Consider the map $f: S^1 \rightarrow S^1$ from the unit circle to itself, given by $f(z) = z^2$.
We can parameterize the circle by an angle $\theta \in [0, 2\pi)$, so $z = e^{i\theta}$.

a) The mapping becomes $f(\theta) = e^{i2\theta}$.
   If you trace the input point once around the circle (from $\theta=0$ to $2\pi$), how many times does the output point go around the circle?

b) For any point $w$ on the target circle, how many points on the source circle map to it?
   (i.e., solve $z^2=w$ for z).

c) This is a 2-to-1 map, so the source circle is a "double cover" of the target circle.
   This is analogous to the SU(2) → SO(3) map, but in a lower dimension.

### Solution 1

a) **If you trace the input point once around the circle (from $\theta=0$ to $2\pi$), how many times does the output point go around the circle?**

As $\theta$ goes from 0 to $2\pi$, the output angle $2\theta$ goes from 0 to $4\pi$. The output point goes around the circle twice.

b) **For any point $w$ on the target circle, how many points on the source circle map to it?**

Let $w = e^{i\phi}$. We want to solve $z^2 = e^{i\phi}$.
$$z = (e^{i\phi})^{1/2} = e^{i\phi/2} \text{ and } e^{i(\phi/2 + \pi)} = -e^{i\phi/2}$$

There are two points on the source circle that map to each point on the target circle.

c) **This is a 2-to-1 map, so the source circle is a "double cover" of the target circle.**

This is a correct statement.

## Problem 2: SU(2) and SO(3)

The group SU(2) is the group of 2×2 unitary matrices with determinant 1. Topologically, it is the 3-sphere, $S^3$.
The group SO(3) is the group of 3×3 orthogonal matrices with determinant 1. Topologically, it is the real projective space $\mathbb{R}P^3$.

The homomorphism $\rho: SU(2) \rightarrow SO(3)$ is 2-to-1.

a) A rotation in SO(3) can be specified by an axis (a unit vector, 2 parameters) and an angle $\theta \in [0, \pi]$.
   The space of rotations can be visualized as a solid ball of radius $\pi$ in $\mathbb{R}^3$, where a point represents a rotation by an angle equal to its distance from the origin, around the axis given by its direction.
   What is special about the boundary of this ball (the sphere of radius $\pi$)? A rotation by $\pi$ around $\hat{n}$ is the same as a rotation by $-\pi$ around $\hat{n}$. So, antipodal points on the surface of the ball are identified.

b) This space (a ball with antipodal boundary points identified) is $\mathbb{R}P^3$. Is this space simply connected?
   (Hint: Consider a path from the origin to a point on the boundary, and then from the antipodal point back to the origin. Can this loop be shrunk to a point?). This is the "Dirac belt trick".

c) The group SU(2) is the 3-sphere, $S^3$. Is $S^3$ simply connected?

d) The fact that SU(2) is the simply connected universal cover of SO(3) is crucial for quantum mechanics. Why? Why do we need representations of the covering group?

### Solution 2

a) **What is special about the boundary of this ball (the sphere of radius $\pi$)?**

A rotation by $\pi$ around an axis $\hat{n}$ is the same as a rotation by $-\pi$ around the same axis. A rotation by $-\pi$ around $\hat{n}$ is the same as a rotation by $\pi$ around $-\hat{n}$. So, antipodal points on the surface of the ball are identified.

b) **Is this space (a ball with antipodal boundary points identified) simply connected?**

No. Consider a path from the origin to a point on the boundary (e.g., the north pole). This represents a rotation by $\pi$ around the z-axis. Then, from the antipodal point (south pole), which is identified with the north pole, we can go back to the origin. This is a closed loop. This loop cannot be shrunk to a point. This is the "Dirac belt trick" visualization.

c) **The group SU(2) is the 3-sphere, $S^3$. Is $S^3$ simply connected?**

Yes. Any loop on a 3-sphere can be shrunk to a point.

d) **The fact that SU(2) is the simply connected universal cover of SO(3) is crucial for quantum mechanics. Why?**

In quantum mechanics, physical states are represented by rays in a Hilbert space, which means that the overall phase of a state vector is not physical. This opens the door for projective representations of symmetry groups. The representations of the covering group (like SU(2)) provide the projective representations of the original group (like SO(3)). Spinors are objects that transform under these projective representations.

## Problem 3: The Path from I to R(2π)

Let's trace a path in SO(3) corresponding to a full $2\pi$ rotation.
Let $R_z(\theta)$ be a rotation around the z-axis. The path is from $\theta=0$ to $\theta=2\pi$.
In SO(3), $R_z(0) = I$ and $R_z(2\pi) = I$. This is a closed loop.

a) In the covering group SU(2), the corresponding path is $U_z(\theta) = \exp(-i\frac{\theta}{2}\sigma_3)$.
   What is $U_z(0)$?

b) What is $U_z(2\pi)$?

c) Is the path in SU(2) a closed loop?

d) What is $U_z(4\pi)$? The loop closes in SU(2) only after a $4\pi$ rotation.

### Solution 3

a) **What is $U_z(0)$?**

$$U_z(0) = \exp(0) = I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

b) **What is $U_z(2\pi)$?**

$$U_z(2\pi) = \exp(-i\pi\sigma_3) = \cos(-\pi)I - i\sin(-\pi)\sigma_3 = -I = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$$

c) **Is the path in SU(2) a closed loop?**

No. It starts at I and ends at -I.

d) **What is $U_z(4\pi)$? The loop closes in SU(2) only after a $4\pi$ rotation.**

$$U_z(4\pi) = \exp(-i2\pi\sigma_3) = \cos(-2\pi)I - i\sin(-2\pi)\sigma_3 = I$$

The path closes after a $4\pi$ rotation.

## Problem 4: The Lorentz Group and its Cover

The proper orthochronous Lorentz group, $SO^+(1,3)$, is the group of rotations and boosts that preserves orientation and the direction of time.
This group is not simply connected.
Its universal covering group is $Spin(1,3)$, which is isomorphic to $SL(2, \mathbb{C})$.

a) What is the dimension of the manifold of $SO^+(1,3)$? (3 rotations + 3 boosts).

b) What is the dimension of the manifold of $SL(2, \mathbb{C})$? (A 2×2 complex matrix has 8 real parameters. The determinant=1 condition imposes how many constraints?).

c) The center of $SL(2, \mathbb{C})$ is the set of matrices that commute with all other matrices. Show that the center is {I, -I}.

d) The Lorentz group is the quotient of its cover by the center: $SO^+(1,3) \cong SL(2, \mathbb{C}) / \{I, -I\}$.
   This is the formal statement of the double cover.

### Solution 4

a) **What is the dimension of the manifold of $SO^+(1,3)$?**

3 rotations + 3 boosts = 6 dimensions.

b) **What is the dimension of the manifold of $SL(2, \mathbb{C})$?**

A 2×2 complex matrix has 4 complex entries, so 8 real parameters. The condition $\det(U)=1$ is one complex equation, which is two real constraints. So the dimension is $8-2=6$.

c) **Show that the center of $SL(2, \mathbb{C})$ is {I, -I}.**

Let $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ be in the center. It must commute with all matrices in $SL(2, \mathbb{C})$. After testing with a few matrices, one can show that $b=c=0$ and $a=d$. The determinant condition $a^2=1$ implies $a=\pm 1$. So the center is {I, -I}.

d) **The Lorentz group is the quotient of its cover by the center: $SO^+(1,3) \cong SL(2, \mathbb{C}) / \{I, -I\}$.**

This is a correct statement of the 2-to-1 homomorphism.

## Problem 5: Physical Consequences

Why does this mathematical structure matter?

a) In quantum mechanics, states are rays in a Hilbert space, so an overall phase factor doesn't matter. $\psi$ and $-\psi$ represent the same physical state.

b) When we have a system that rotates, its wavefunction might be a representation of SO(3) or its double cover SU(2).

c) If the wavefunction transforms under SO(3) (like a vector), what happens to it after a $2\pi$ rotation?

d) If the wavefunction transforms under SU(2) (like a spinor), what happens to it after a $2\pi$ rotation?

e) This sign change is experimentally observable in interference experiments with neutrons. What does this tell us about the nature of the neutron's wavefunction?

### Solution 5

a) **In quantum mechanics, states are rays in a Hilbert space, so an overall phase factor doesn't matter. $\psi$ and $-\psi$ represent the same physical state.**

Correct.

b) **When we have a system that rotates, its wavefunction might be a representation of SO(3) or its double cover SU(2).**

Correct.

c) **If the wavefunction transforms under SO(3) (like a vector), what happens to it after a $2\pi$ rotation?**

It returns to its original state.

d) **If the wavefunction transforms under SU(2) (like a spinor), what happens to it after a $2\pi$ rotation?**

It acquires a minus sign.

e) **This sign change is experimentally observable in interference experiments with neutrons. What does this tell us about the nature of the neutron's wavefunction?**

It tells us that the neutron's wavefunction is described by a spinor, and that it transforms under the SU(2) representation of the rotation group. This is a direct confirmation of the reality of the double cover structure in quantum mechanics.