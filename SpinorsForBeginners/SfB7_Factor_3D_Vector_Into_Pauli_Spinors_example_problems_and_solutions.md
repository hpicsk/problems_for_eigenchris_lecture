# SfB 7: Factor 3D Vector Into Pauli Spinors - Example Problems and Solutions

This lecture covers the relationship between a 3D vector and a pair of 2-component spinors, sometimes called the "spinor flag". A null vector can be written as an outer product of a spinor with its conjugate.

## Problem 1: From Spinor to Null Vector

Given a 2-component spinor $\xi = \begin{pmatrix} \alpha \\ \beta \end{pmatrix}$, we can form a 4-vector $k^\mu$ by contracting with the Pauli matrices $\sigma^\mu = (I, \sigma_1, \sigma_2, \sigma_3)$.
$$k^\mu = \xi^\dagger \sigma^\mu \xi$$

Let $\xi = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$. Calculate the corresponding 4-vector $k^\mu$. Show that this vector is null, i.e., $k_\mu k^\mu = 0$. (Using metric signature $(+---)$).

### Solution 1

Let $\xi = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

$$k^0 = \xi^\dagger I \xi = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = 1$$

$$k^1 = \xi^\dagger \sigma_1 \xi = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = 0$$

$$k^2 = \xi^\dagger \sigma_2 \xi = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 0 \\ i \end{pmatrix} = 0$$

$$k^3 = \xi^\dagger \sigma_3 \xi = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = 1$$

So $k^\mu = (1, 0, 0, 1)$.

$$k_\mu k^\mu = (k^0)^2 - (k^1)^2 - (k^2)^2 - (k^3)^2 = 1^2 - 0^2 - 0^2 - 1^2 = 0$$

The vector is null.

## Problem 2: From Null Vector to Spinor

Given a null 4-vector $k^\mu = (k^0, k^1, k^2, k^3)$ where $(k^0)^2 = (k^1)^2 + (k^2)^2 + (k^3)^2$, we can form a 2×2 matrix $K = k_\mu \sigma^\mu$.
$$K = k_0 I - k_1 \sigma_1 - k_2 \sigma_2 - k_3 \sigma_3 = \begin{pmatrix} k_0-k_3 & -k_1+ik_2 \\ -k_1-ik_2 & k_0+k_3 \end{pmatrix}$$

a) Show that if $k^\mu$ is a null vector, then $\det(K) = 0$.

b) A matrix with zero determinant can be written as an outer product of two vectors. Find the spinor $\xi$ such that $K = 2 \xi \xi^\dagger$.

Let $k^\mu = (1, 1, 0, 0)$. Find the corresponding spinor $\xi$. Is the solution unique?

### Solution 2

a) **Show that if $k^\mu$ is a null vector, then $\det(K) = 0$.**

$$K = \begin{pmatrix} k_0-k_3 & -k_1+ik_2 \\ -k_1-ik_2 & k_0+k_3 \end{pmatrix}$$

$$\det(K) = (k_0-k_3)(k_0+k_3) - (-k_1+ik_2)(-k_1-ik_2) = k_0^2 - k_3^2 - (k_1^2 + k_2^2) = k_0^2 - (k_1^2+k_2^2+k_3^2)$$

If $k^\mu$ is a null vector with signature $(+---)$, then $k_0^2 - k_1^2 - k_2^2 - k_3^2 = 0$.
So $\det(K) = 0$.

b) **Let $k^\mu = (1, 1, 0, 0)$. Find the corresponding spinor $\xi$. Is the solution unique?**

$$K = \begin{pmatrix} 1-0 & -1+0 \\ -1-0 & 1+0 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix}$$

We want to find $\xi = \begin{pmatrix} \alpha \\ \beta \end{pmatrix}$ such that $K = 2\xi\xi^\dagger = 2\begin{pmatrix} \alpha \\ \beta \end{pmatrix}\begin{pmatrix} \alpha^* & \beta^* \end{pmatrix} = 2\begin{pmatrix} |\alpha|^2 & \alpha\beta^* \\ \beta\alpha^* & |\beta|^2 \end{pmatrix}$.

Comparing with $K$, we have:
$$2|\alpha|^2 = 1 \implies |\alpha| = 1/\sqrt{2}$$
$$2|\beta|^2 = 1 \implies |\beta| = 1/\sqrt{2}$$
$$2\alpha\beta^* = -1$$

Let $\alpha = \frac{1}{\sqrt{2}}e^{i\phi_1}$ and $\beta = \frac{1}{\sqrt{2}}e^{i\phi_2}$.
Then $2(\frac{1}{\sqrt{2}}e^{i\phi_1})(\frac{1}{\sqrt{2}}e^{-i\phi_2}) = e^{i(\phi_1-\phi_2)} = -1 = e^{i\pi}$.

So $\phi_1 - \phi_2 = \pi$. Let's choose $\phi_1=0, \phi_2=-\pi$. Then $\alpha=1/\sqrt{2}, \beta=-1/\sqrt{2}$.

$$\xi = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ -1 \end{pmatrix}$$

The solution is not unique, as we can choose any phase for $\alpha$ and then determine the phase of $\beta$.

## Problem 3: Factoring a 3D Vector

A general 3D vector $v = (x, y, z)$ is not null. However, we can associate it with a 2×2 matrix $V = v \cdot \sigma$.
$$V = \begin{pmatrix} z & x-iy \\ x+iy & -z \end{pmatrix}$$

The determinant of this matrix is $-|v|^2$. This matrix can be "factored" by finding its eigenvalues and eigenvectors. The eigenvectors are the spinors associated with the vector.

Find the eigenvalues and normalized eigenvectors (spinors) for the vector $v = (0, 0, 1)$.
What do these spinors represent physically? (Think about spin up/down).

### Solution 3

**Find the eigenvalues and normalized eigenvectors (spinors) for the vector $v = (0, 0, 1)$.**

$$V = v \cdot \sigma = \sigma_3 = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$

The eigenvalues are clearly 1 and -1.

The eigenvector for eigenvalue 1 is $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

The eigenvector for eigenvalue -1 is $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$.

These are the spin-up and spin-down states along the z-axis.

## Problem 4: The "Spinor Flag"

A 3D vector defines a direction. The two spinors found in the previous problem are aligned with this direction. This is part of the "spinor flag" concept, where a vector (the flagpole) is associated with a spinor (the flag).

Let the vector be $v = (1, 0, 0)$. Find the corresponding matrix $V$ and its eigenspinors.
How are these spinors related to the spinors for $v = (0, 0, 1)$? (Hint: think about rotations).

### Solution 4

**Let the vector be $v = (1, 0, 0)$. Find the corresponding matrix $V$ and its eigenspinors.**

$$V = v \cdot \sigma = \sigma_1 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$$

To find the eigenvalues, $\det(V-\lambda I) = \det\begin{pmatrix} -\lambda & 1 \\ 1 & -\lambda \end{pmatrix} = \lambda^2-1=0$. So $\lambda = \pm 1$.

For $\lambda=1$: $\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} y \\ x \end{pmatrix} = \begin{pmatrix} x \\ y \end{pmatrix}$. So $x=y$.

The normalized eigenvector is $\frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$.

For $\lambda=-1$: $\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} y \\ x \end{pmatrix} = -\begin{pmatrix} x \\ y \end{pmatrix}$. So $y=-x$.

The normalized eigenvector is $\frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ -1 \end{pmatrix}$.

**How are these spinors related to the spinors for $v = (0, 0, 1)$?**

The spinors for $v=(0,0,1)$ are the z-basis spinors. The spinors for $v=(1,0,0)$ are the x-basis spinors.
They are related by a rotation. A rotation by $\pi/2$ around the y-axis takes the z-axis to the x-axis.

The rotation matrix is $U = \exp(-i\frac{\pi/2}{2}\sigma_2) = \frac{1}{\sqrt{2}}(I-i\sigma_2) = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix}$.

Let's apply this to the z-spinors:
$$U\begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$$
This is the x-up spinor.

$$U\begin{pmatrix} 0 \\ 1 \end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix} -1 \\ 1 \end{pmatrix} = -\frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ -1 \end{pmatrix}$$
This is the x-down spinor (up to a phase).

## Problem 5: Uniqueness and Phase

When factoring a vector into spinors, there is a phase ambiguity.
If $\xi$ is a solution, then $e^{i\phi}\xi$ is also a solution.

Show that this phase ambiguity does not change the vector that is constructed from the spinor.
i.e., show that if $k^\mu = \xi^\dagger \sigma^\mu \xi$, then using $\xi' = e^{i\phi}\xi$ results in the same $k^\mu$.
What is the geometric interpretation of this phase?

### Solution 5

**Show that if $k^\mu = \xi^\dagger \sigma^\mu \xi$, then using $\xi' = e^{i\phi}\xi$ results in the same $k^\mu$.**

Let $k'^\mu = (\xi')^\dagger \sigma^\mu \xi' = (e^{i\phi}\xi)^\dagger \sigma^\mu (e^{i\phi}\xi) = (e^{-i\phi}\xi^\dagger) \sigma^\mu (e^{i\phi}\xi) = e^{-i\phi}e^{i\phi} \xi^\dagger \sigma^\mu \xi = k^\mu$.

The phase cancels out.

**What is the geometric interpretation of this phase?**

The spinor corresponds to a point on the Riemann sphere. The overall phase of the spinor is not represented on the sphere. The Riemann sphere represents the space of physical states, which are independent of the overall phase. This is related to the fact that in quantum mechanics, the global phase of a state is not observable.