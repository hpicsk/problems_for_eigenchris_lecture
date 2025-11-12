# Example Problems and Solutions: Pauli Vectors

This lecture introduces the Pauli matrices and how they can be used to represent vectors and perform rotations.

## Problem 1: Pauli Matrix Properties

The three Pauli matrices are:
$$\sigma_1 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad \sigma_2 = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad \sigma_3 = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$

Verify the following properties:

a) They are Hermitian: $\sigma_i^\dagger = \sigma_i$

b) They are traceless: $\text{Tr}(\sigma_i) = 0$

c) $\sigma_1^2 = \sigma_2^2 = \sigma_3^2 = I$ (where I is the 2×2 identity matrix)

### Solution 1

a) **They are Hermitian: $\sigma_i^\dagger = \sigma_i$**

$$\sigma_1^\dagger = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}^\dagger = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = \sigma_1$$

$$\sigma_2^\dagger = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}^\dagger = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} = \sigma_2$$

$$\sigma_3^\dagger = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}^\dagger = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} = \sigma_3$$

All are Hermitian.

b) **They are traceless: $\text{Tr}(\sigma_i) = 0$**

$$\text{Tr}(\sigma_1) = 0+0 = 0$$
$$\text{Tr}(\sigma_2) = 0+0 = 0$$
$$\text{Tr}(\sigma_3) = 1-1 = 0$$

All are traceless.

c) **$\sigma_1^2 = \sigma_2^2 = \sigma_3^2 = I$**

$$\sigma_1^2 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$$

$$\sigma_2^2 = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$$

$$\sigma_3^2 = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$$

## Problem 2: Commutation and Anti-commutation Relations

Calculate the following:

a) The commutator $[\sigma_1, \sigma_2]$.

b) The anti-commutator $\{\sigma_1, \sigma_2\}$.

Show that the general relations hold:
$$[\sigma_i, \sigma_j] = 2i \sum_k \epsilon_{ijk} \sigma_k$$
$$\{\sigma_i, \sigma_j\} = 2\delta_{ij} I$$

### Solution 2

a) **The commutator $[\sigma_1, \sigma_2]$.**

$$[\sigma_1, \sigma_2] = \sigma_1\sigma_2 - \sigma_2\sigma_1 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} - \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$$

$$= \begin{pmatrix} i & 0 \\ 0 & -i \end{pmatrix} - \begin{pmatrix} -i & 0 \\ 0 & i \end{pmatrix} = \begin{pmatrix} 2i & 0 \\ 0 & -2i \end{pmatrix} = 2i\sigma_3$$

b) **The anti-commutator $\{\sigma_1, \sigma_2\}$.**

$$\{\sigma_1, \sigma_2\} = \sigma_1\sigma_2 + \sigma_2\sigma_1 = \begin{pmatrix} i & 0 \\ 0 & -i \end{pmatrix} + \begin{pmatrix} -i & 0 \\ 0 & i \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = 0$$

**Show that the general relations hold:**

We have shown this for $i=1, j=2$. $\epsilon_{123}=1$, so $[\sigma_1, \sigma_2] = 2i\sigma_3$.

For $i=j$, $[\sigma_i, \sigma_i] = 0$. $\epsilon_{iik}=0$.

For $i=1, j=1$, $\{\sigma_1, \sigma_1\} = 2\sigma_1^2 = 2I$. $\delta_{11}=1$.

For $i=1, j=2$, $\{\sigma_1, \sigma_2\} = 0$. $\delta_{12}=0$.

The relations hold.

## Problem 3: Representing a Vector

A 3D vector $v = (x, y, z)$ can be associated with a 2×2 matrix $V = v \cdot \sigma = x\sigma_1 + y\sigma_2 + z\sigma_3$.

a) Write out the matrix $V$ explicitly in terms of x, y, and z.

b) Given the vector $v = (3, 4, 5)$, write down the corresponding matrix $V$.

c) Show that $\det(V) = -\|v\|^2$.

### Solution 3

a) **Write out the matrix $V$ explicitly in terms of x, y, and z.**

$$V = x\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} + y\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} + z\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} z & x-iy \\ x+iy & -z \end{pmatrix}$$

b) **Given the vector $v = (3, 4, 5)$, write down the corresponding matrix $V$.**

$$V = \begin{pmatrix} 5 & 3-4i \\ 3+4i & -5 \end{pmatrix}$$

c) **Show that $\det(V) = -\|v\|^2$.**

$$\det(V) = -z^2 - (x-iy)(x+iy) = -z^2 - (x^2+y^2) = -(x^2+y^2+z^2) = -\|v\|^2$$

## Problem 4: Rotations with Pauli Vectors

An SU(2) rotation can be represented by a unitary matrix $U = \exp(-i\frac{\theta}{2} \hat{n}\cdot\sigma)$, where $\hat{n}$ is a unit vector giving the axis of rotation.

The vector $v$ transforms as $V' = U V U^\dagger$.

Let's perform a rotation of $\pi$ around the y-axis.

a) What is the unit vector $\hat{n}$?

b) Calculate the rotation matrix $U = \exp(-i\frac{\pi}{2} \sigma_2)$. Hint: use the Taylor expansion of the exponential and $\sigma_2^2=I$.

c) Let $v = (1, 0, 0)$, so $V = \sigma_1$. Calculate the new matrix $V' = U \sigma_1 U^\dagger$.

d) From $V'$, what is the new vector $v'$? Does this match your expectation for the rotation?

### Solution 4

a) **What is the unit vector $\hat{n}$?**

For a rotation around the y-axis, $\hat{n} = (0, 1, 0)$.

b) **Calculate the rotation matrix $U = \exp(-i\frac{\pi}{2} \sigma_2)$.**

$$U = \cos(\pi/2)I - i\sin(\pi/2)\sigma_2 = -i\sigma_2 = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$$

c) **Let $v = (1, 0, 0)$, so $V = \sigma_1$. Calculate the new matrix $V' = U \sigma_1 U^\dagger$.**

$$U^\dagger = (-i\sigma_2)^\dagger = i\sigma_2^\dagger = i\sigma_2 = -U$$

$$V' = U \sigma_1 U^\dagger = (-i\sigma_2) \sigma_1 (i\sigma_2) = \sigma_2 \sigma_1 \sigma_2 = (i\sigma_3)\sigma_2 = i(i\sigma_1) = -\sigma_1$$

d) **From $V'$, what is the new vector $v'$? Does this match your expectation for the rotation?**

$V' = -\sigma_1$, so $v' = (-1, 0, 0)$.

A rotation of $(1,0,0)$ by $\pi$ around the y-axis gives $(-1,0,0)$. This is correct.

## Problem 5: Completeness Relation

The Pauli matrices, along with the identity matrix, form a basis for the space of 2×2 matrices. Any 2×2 matrix M can be written as:
$$M = c_0 I + c_1 \sigma_1 + c_2 \sigma_2 + c_3 \sigma_3$$

Find a formula for the coefficients $c_i$ in terms of M.
Hint: Use the property $\text{Tr}(\sigma_i \sigma_j) = 2\delta_{ij}$.

Use your formula to decompose the matrix $M = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}$ into the Pauli basis.

### Solution 5

**Find a formula for the coefficients $c_i$ in terms of M.**

$$M = c_0 I + \sum_j c_j \sigma_j$$

Multiply by $\sigma_i$ and take the trace:
$$\text{Tr}(M\sigma_i) = \text{Tr}(c_0 \sigma_i) + \sum_j c_j \text{Tr}(\sigma_j\sigma_i) = c_0 \text{Tr}(\sigma_i) + \sum_j c_j (2\delta_{ji}) = 0 + 2c_i$$

So $c_i = \frac{1}{2}\text{Tr}(M\sigma_i)$ for $i=1,2,3$.

For $c_0$, we take the trace of M:
$$\text{Tr}(M) = \text{Tr}(c_0 I) + \sum_j c_j \text{Tr}(\sigma_j) = 2c_0$$

So $c_0 = \frac{1}{2}\text{Tr}(M)$.

**Use your formula to decompose the matrix $M = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}$ into the Pauli basis.**

$$c_0 = \frac{1}{2}\text{Tr}(M) = \frac{1}{2}(1+4) = \frac{5}{2}$$

$$c_1 = \frac{1}{2}\text{Tr}(M\sigma_1) = \frac{1}{2}\text{Tr}\left(\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\right) = \frac{1}{2}\text{Tr}\left(\begin{pmatrix} 2 & 1 \\ 4 & 3 \end{pmatrix}\right) = \frac{1}{2}(2+3) = \frac{5}{2}$$

$$c_2 = \frac{1}{2}\text{Tr}(M\sigma_2) = \frac{1}{2}\text{Tr}\left(\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}\right) = \frac{1}{2}\text{Tr}\left(\begin{pmatrix} 2i & -i \\ 4i & -3i \end{pmatrix}\right) = \frac{1}{2}(2i-3i) = -\frac{i}{2}$$

$$c_3 = \frac{1}{2}\text{Tr}(M\sigma_3) = \frac{1}{2}\text{Tr}\left(\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}\right) = \frac{1}{2}\text{Tr}\left(\begin{pmatrix} 1 & -2 \\ 3 & -4 \end{pmatrix}\right) = \frac{1}{2}(1-4) = -\frac{3}{2}$$

So:
$$M = \frac{5}{2}I + \frac{5}{2}\sigma_1 - \frac{i}{2}\sigma_2 - \frac{3}{2}\sigma_3$$