This is an introductory lecture, so the problems will be conceptual and aim to set the stage for the topics to come.

## Problem 1: What is a Spinor?

This is a trick question, as the answer is complex. But based on the introduction, try to answer the following:

a) How is a spinor different from a vector or a tensor?

b) A key property of spinors is how they behave under rotations. Describe the difference between a vector rotating by 360 degrees and a spinor rotating by 360 degrees.

c) Give a physical example of a quantity that is described by a spinor.

d) Give a physical example of a quantity that is described by a vector.

### Solution 1:

a) **How is a spinor different from a vector or a tensor?**

A spinor is a mathematical object that transforms differently than a vector or a tensor under a rotation. While vectors and tensors are defined by their transformation properties under the standard representations of the rotation group $SO(n)$, spinors transform under a different representation called the spin representation. This means that when you rotate the coordinate system, the components of a spinor change in a way that is distinct from how the components of a vector or tensor would change.

b) **A key property of spinors is how they behave under rotations. Describe the difference between a vector rotating by 360 degrees and a spinor rotating by 360 degrees.**

When a vector is rotated by 360 degrees, it returns to its original orientation. However, when a spinor is rotated by 360 degrees, it is multiplied by $-1$, meaning it becomes its own negative. It takes a 720-degree rotation to bring a spinor back to its original state. This is often visualized with the "plate trick" or "belt trick".

c) **Give a physical example of a quantity that is described by a spinor.**

The most common example is the spin of an electron. The electron's spin is a quantum mechanical property that is described by a 2-component spinor.

d) **Give a physical example of a quantity that is described by a vector.**

Velocity is a good example. It has both a magnitude (speed) and a direction, and it transforms as a vector under rotations.

## Problem 2: Rotations in 3D

Rotations in 3D are described by the group $SO(3)$.

a) A rotation by an angle $\theta$ around the z-axis is given by the matrix $R_z(\theta)$. Write down this $3 \times 3$ matrix.

b) Show that the product of two rotation matrices is another rotation matrix.

c) Show that every rotation matrix has a determinant of $+1$.

d) Is the group $SO(3)$ commutative? (i.e., does the order of rotations matter?). Give an example by rotating a book 90 degrees about the x-axis and then 90 degrees about the y-axis, and comparing with the reverse order.

### Solution 2:

a) **A rotation by an angle $\theta$ around the z-axis is given by the matrix $R_z(\theta)$. Write down this $3 \times 3$ matrix.**

The matrix for a rotation by an angle $\theta$ around the z-axis is:
$$R_z(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta & 0 \\ \sin\theta & \cos\theta & 0 \\ 0 & 0 & 1 \end{pmatrix}$$

b) **Show that the product of two rotation matrices is another rotation matrix.**

Let $R_1$ and $R_2$ be two rotation matrices. Their product is $R_3 = R_1 R_2$. Since rotation matrices are orthogonal ($R^T R = I$) and have determinant $+1$, we can check if $R_3$ has these properties.

- Orthogonality: $(R_1 R_2)^T (R_1 R_2) = R_2^T R_1^T R_1 R_2 = R_2^T I R_2 = R_2^T R_2 = I$. So $R_3$ is orthogonal.
- Determinant: $\det(R_1 R_2) = \det(R_1) \det(R_2) = 1 \cdot 1 = 1$.

Since the product is an orthogonal matrix with determinant 1, it is also a rotation matrix.

c) **Show that every rotation matrix has a determinant of $+1$.**

A rotation matrix $R$ is an orthogonal matrix, which means $R^T R = I$.
Taking the determinant of both sides, we get $\det(R^T R) = \det(I) = 1$.
Since $\det(R^T) = \det(R)$, we have $\det(R)^2 = 1$. This means $\det(R) = \pm 1$.
A rotation is a continuous transformation from the identity matrix (which has determinant $+1$). Since the determinant is a continuous function of the matrix entries, the determinant of a rotation matrix must be $+1$. The matrices with determinant $-1$ represent reflections, not rotations.

d) **Is the group $SO(3)$ commutative? (i.e., does the order of rotations matter?). Give an example by rotating a book 90 degrees about the x-axis and then 90 degrees about the y-axis, and comparing with the reverse order.**

No, $SO(3)$ is not commutative. The order of rotations matters.

Let's take the example of a book.

- **Rotation 1 ($R_x$ then $R_y$):**
  1. Place the book flat on a table with the cover facing up and the spine towards you. This is the initial state.
  2. Rotate the book 90 degrees about the x-axis (the axis pointing to your right). The book is now standing on its spine, with the cover facing right.
  3. Now, rotate the book 90 degrees about the y-axis (the axis pointing away from you). The book is now lying flat on the table again, but with the spine facing away from you.

- **Rotation 2 ($R_y$ then $R_x$):**
  1. Start with the book in the initial state (flat on the table, spine towards you).
  2. Rotate the book 90 degrees about the y-axis. The book is now standing on its right edge, with the cover facing up.
  3. Now, rotate the book 90 degrees about the x-axis. The book is now standing on its spine, with the cover facing away from you.

The final orientation of the book is different in the two cases, which demonstrates that rotations in 3D do not commute.

## Problem 3: The Double Cover: SU(2)

The group $SU(2)$ is the group of $2 \times 2$ unitary matrices with determinant 1. It is intimately related to $SO(3)$.
An $SU(2)$ matrix can be written as $U = \exp(-i\frac{\theta}{2} \hat{n}\cdot\sigma)$, where $\sigma$ are the Pauli matrices. This corresponds to a rotation in $SO(3)$ by an angle $\theta$ around the axis $\hat{n}$.

a) What is the $SU(2)$ matrix for a 360-degree ($2\pi$) rotation about the z-axis?

b) How does this matrix act on a 2-component column vector (a spinor)?

c) What is the $SU(2)$ matrix for a 720-degree ($4\pi$) rotation about the z-axis?

d) This "sign change on $2\pi$ rotation" is the hallmark of a spinor. Why don't we observe this in everyday life?

### Solution 3:

a) **What is the $SU(2)$ matrix for a 360-degree ($2\pi$) rotation about the z-axis?**

The $SU(2)$ matrix for a rotation by $\theta$ around the axis $\hat{n}$ is $U = \exp(-i\frac{\theta}{2} \hat{n}\cdot\sigma)$.
For a rotation of $2\pi$ about the z-axis, $\theta = 2\pi$ and $\hat{n} = (0,0,1)$. The Pauli matrix for the z-direction is $\sigma_z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$.

So, $U = \exp(-i\frac{2\pi}{2} \sigma_z) = \exp(-i\pi \sigma_z)$. Using the formula $\exp(i\alpha A) = I\cos(\alpha) + iA\sin(\alpha)$ for a matrix $A$ such that $A^2=I$, and noting that $(\sigma_z)^2=I$, we have:

$$\exp(-i\pi \sigma_z) = I\cos(-\pi) -i\sigma_z\sin(-\pi) = -I = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$$

b) **How does this matrix act on a 2-component column vector (a spinor)?**

Let the spinor be $\psi = \begin{pmatrix} a \\ b \end{pmatrix}$.
The action of the matrix is:
$$\begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} -a \\ -b \end{pmatrix} = -\psi$$

The spinor is negated.

c) **What is the $SU(2)$ matrix for a 720-degree ($4\pi$) rotation about the z-axis?**

For a rotation of $4\pi$ about the z-axis, $\theta = 4\pi$.
$$U = \exp(-i\frac{4\pi}{2} \sigma_z) = \exp(-i2\pi \sigma_z) = \cos(-2\pi)I - i\sin(-2\pi)\sigma_z = I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

This is the identity matrix.

d) **This "sign change on $2\pi$ rotation" is the hallmark of a spinor. Why don't we observe this in everyday life?**

Observable physical quantities in quantum mechanics are typically given by expressions of the form $\langle\psi|O|\psi\rangle$, where $O$ is an operator. If the state $|\psi\rangle$ picks up a minus sign, so it becomes $-|\psi\rangle$, the observable becomes $\langle-\psi|O|-\psi\rangle = (-1)(-1)\langle\psi|O|\psi\rangle = \langle\psi|O|\psi\rangle$. The observable is unchanged. Since we only measure observables, the sign change is not directly observed.

## Problem 4: Complex Numbers and Quaternions

Spinors are deeply connected to the structure of numbers.

a) A complex number $z = x+iy$ can be used to represent a point in a 2D plane. How can you represent a rotation of this point by an angle $\theta$ using complex number multiplication?

b) Quaternions are an extension of complex numbers, of the form $q = a + bi + cj + dk$. Unit quaternions can be used to represent rotations in 3D.
   What is the quaternion equivalent of the "rotation by $\theta$" operator you found in part (a)?

c) The relationship between $SU(2)$ and quaternions is another key theme. What is the dimension of the space of quaternions? What is the dimension of the space of $2 \times 2$ complex matrices?

### Solution 4:

a) **A complex number $z = x+iy$ can be used to represent a point in a 2D plane. How can you represent a rotation of this point by an angle $\theta$ using complex number multiplication?**

A rotation of a point $z$ by an angle $\theta$ can be represented by multiplying $z$ by another complex number $e^{i\theta} = \cos\theta + i\sin\theta$.
The rotated point is $z' = e^{i\theta}z$.

b) **What is the quaternion equivalent of the "rotation by $\theta$" operator you found in part (a)?**

In 3D, a rotation by an angle $\theta$ about a unit vector axis $\hat{n} = (n_x, n_y, n_z)$ can be represented by a unit quaternion:
$$q = \cos(\theta/2) + (n_x i + n_y j + n_z k)\sin(\theta/2)$$

The equivalent of the 2D rotation operator is a unit quaternion.

c) **The relationship between $SU(2)$ and quaternions is another key theme. What is the dimension of the space of quaternions? What is the dimension of the space of $2 \times 2$ complex matrices?**

The space of quaternions has dimension 4 (a basis is $\{1, i, j, k\}$).
A $2 \times 2$ complex matrix has 4 entries, and each entry is a complex number (with a real and imaginary part). So the dimension of the space of $2 \times 2$ complex matrices over the real numbers is $4 \times 2 = 8$. Over the complex numbers, the dimension is 4.

## Problem 5: Why Spinors?

Based on the introduction, what are some of the physical or mathematical problems that motivated the development of spinor theory?

- The square root of the Klein-Gordon equation.
- The description of electron spin in quantum mechanics.
- The representation of rotations in a more fundamental way.
- The structure of spacetime itself.

### Solution 5:

Based on the introduction, what are some of the physical or mathematical problems that motivated the development of spinor theory?

- **The square root of the Klein-Gordon equation:** The Klein-Gordon equation is a second-order differential equation. Finding its "square root" led to the Dirac equation, which naturally involves spinors.
- **The description of electron spin in quantum mechanics:** Electron spin is an intrinsic angular momentum that cannot be described by classical vectors but requires spinor formalism.
- **The representation of rotations in a more fundamental way:** Spinors provide a more fundamental description of rotational symmetry than vectors, revealing the double-valued nature of rotations.
- **The structure of spacetime itself:** In relativity, spinors are essential for describing the fundamental structure of spacetime and the behavior of matter under Lorentz transformations.