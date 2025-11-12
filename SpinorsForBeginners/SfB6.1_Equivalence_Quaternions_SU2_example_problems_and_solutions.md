---
layout: default
title: "Equivalence of Quaternions and SU(2)"
---

# Example Problems and Solutions: Equivalence of Quaternions and SU(2)

This lecture explores the isomorphism between the group of unit quaternions and the special unitary group SU(2).

## Problem 1: Basic Quaternion Multiplication

The quaternions are an extension of complex numbers with three imaginary units i, j, k such that:
$$i^2 = j^2 = k^2 = ijk = -1$$

From these, derive the following relations:

a) $ij = k$, $ji = -k$

b) $jk = i$, $kj = -i$

c) $ki = j$, $ik = -j$

Now, multiply two quaternions:
$$q_1 = 1 + 2i + 3j + 4k$$
$$q_2 = 5 + 6i + 7j + 8k$$

Calculate the product $q_1 q_2$.

### Solution 1

a) **$ij = k$, $ji = -k$**

From $ijk=-1$, multiply by $k$ on the right: $ijkk = -k \implies ij(-1) = -k \implies ij=k$.

From $ij=k$, multiply by $i$ on the left: $iij = ik \implies -j=ik$.

From $ij=k$, multiply by $j$ on the right: $ij^2=kj \implies -i=kj$.

From $ijk=-1$, multiply by $i$ on the left: $iijk=-i \implies -jk=-i \implies jk=i$.

From $jk=i$, multiply by $j$ on the left: $j^2k=ji \implies -k=ji$.

b) **$jk = i$, $kj = -i$**

From $ijk=-1$, multiply by $i$ on the left: $-jk=-i \implies jk=i$.

From $jk=i$, multiply by $k$ on the right: $jk^2=ik \implies -j=ik$.

From $jk=i$, multiply by $j$ on the left: $-k=ji$.

c) **$ki = j$, $ik = -j$**

Let's use cyclic relations: $ij=k, jk=i, ki=j$.

**Calculate the product $q_1 q_2$:**

$$q_1 q_2 = (1 + 2i + 3j + 4k)(5 + 6i + 7j + 8k)$$

Expanding:
$$= 5 + 6i + 7j + 8k$$
$$+ 10i + 12i^2 + 14ij + 16ik$$
$$+ 15j + 18ji + 21j^2 + 24jk$$
$$+ 20k + 24ki + 28kj + 32k^2$$

$$= 5 + 6i + 7j + 8k$$
$$+ 10i - 12 + 14k - 16j$$
$$+ 15j - 18k - 21 + 24i$$
$$+ 20k + 24j - 28i - 32$$

$$= (5-12-21-32) + i(6+10+24-28) + j(7-16+15+24) + k(8+14-18+20)$$
$$= -60 + 12i + 30j + 24k$$

## Problem 2: Representing Quaternions as Matrices

A quaternion $q = a + bi + cj + dk$ can be represented as a 2×2 complex matrix:
$$Q = \begin{pmatrix} a+bi & c+di \\ -c+di & a-bi \end{pmatrix}$$

a) Write the matrices corresponding to the quaternion units 1, i, j, k.
   (Hint: set a=1, b=c=d=0 for 1; set b=1, a=c=d=0 for i, etc.)

b) Show that the matrix for $i$ is proportional to $\sigma_3$, $j$ to $\sigma_2$, and $k$ to $\sigma_1$. What is the relationship?

c) Using the matrix representation, calculate the product $ij$ and show that it equals the matrix for $k$.

### Solution 2

a) **Write the matrices corresponding to the quaternion units 1, i, j, k.**

$$1: a=1, b=c=d=0 \implies \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$$

$$i: b=1, a=c=d=0 \implies \begin{pmatrix} i & 0 \\ 0 & -i \end{pmatrix} = i\sigma_3$$

$$j: c=1, a=b=d=0 \implies \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix} = i\sigma_2$$

$$k: d=1, a=b=c=0 \implies \begin{pmatrix} 0 & i \\ i & 0 \end{pmatrix} = i\sigma_1$$

b) **Show that the matrix for $i$ is proportional to $\sigma_3$, $j$ to $\sigma_2$, and $k$ to $\sigma_1$. What is the relationship?**

The relationship is that the quaternion units are represented by the Pauli matrices multiplied by $i$. A more standard mapping is $i \to -i\sigma_1, j \to -i\sigma_2, k \to -i\sigma_3$. The representation in this problem is unusual.

c) **Using the matrix representation, calculate the product $ij$ and show that it equals the matrix for $k$.**

$i \to i\sigma_3$, $j \to i\sigma_2$.

Product: $(i\sigma_3)(i\sigma_2) = -\sigma_3\sigma_2 = -(-i\sigma_1) = i\sigma_1$.

The matrix for $k$ is $i\sigma_1$. So it works.

## Problem 3: Unit Quaternions and SU(2)

A unit quaternion has norm 1: $N(q) = a^2+b^2+c^2+d^2 = 1$.
The group SU(2) consists of 2×2 unitary matrices with determinant 1.
$$U^\dagger U = I, \quad \det(U) = 1$$

a) Take the matrix representation of a general quaternion $q$ from Problem 2. Calculate its determinant.

b) Show that if $q$ is a unit quaternion, the corresponding matrix has determinant 1.

c) Show that if $q$ is a unit quaternion, the corresponding matrix is unitary.

d) Therefore, show that the group of unit quaternions is equivalent to SU(2).

### Solution 3

a) **Take the matrix representation of a general quaternion $q$ from Problem 2. Calculate its determinant.**

$$Q = \begin{pmatrix} a+bi & c+di \\ -c+di & a-bi \end{pmatrix}$$

$$\det(Q) = (a+bi)(a-bi) - (c+di)(-c+di) = (a^2+b^2) - (-(c-di)(c+di)) = a^2+b^2+c^2+d^2$$

b) **Show that if $q$ is a unit quaternion, the corresponding matrix has determinant 1.**

If $q$ is a unit quaternion, $a^2+b^2+c^2+d^2=1$. So $\det(Q)=1$.

c) **Show that if $q$ is a unit quaternion, the corresponding matrix is unitary.**

$$Q^\dagger = \begin{pmatrix} a-bi & -c-di \\ c-di & a+bi \end{pmatrix}$$

$$Q Q^\dagger = \begin{pmatrix} a+bi & c+di \\ -c+di & a-bi \end{pmatrix} \begin{pmatrix} a-bi & -c-di \\ c-di & a+bi \end{pmatrix}$$

$$= \begin{pmatrix} (a^2+b^2)+(c^2+d^2) & 0 \\ 0 & (c^2+d^2)+(a^2+b^2) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$$

So the matrix is unitary.

d) **Therefore, show that the group of unit quaternions is equivalent to SU(2).**

We have shown that any unit quaternion corresponds to a matrix in SU(2). The mapping is a homomorphism. It is also a bijection. Therefore, the two groups are isomorphic.

## Problem 4: Rotations using Quaternions

A rotation of a 3D vector $v = (x, y, z)$ can be performed using quaternion multiplication. First, represent the vector as a pure quaternion $p = xi + yj + zk$. Then, use a unit quaternion $q = \cos(\theta/2) + \sin(\theta/2)(n_x i + n_y j + n_z k)$ representing a rotation by $\theta$ around the axis $\hat{n}$.

The rotated vector is given by the vector part of $p' = q p q^{-1}$, where $q^{-1}$ is the conjugate $q^* = \cos(\theta/2) - \sin(\theta/2)(n_x i + n_y j + n_z k)$.

Let's rotate the vector $v=(1, 0, 0)$ by an angle of $\pi/2$ around the z-axis.

a) Write the vector $v$ as a pure quaternion $p$.

b) Write the unit quaternion $q$ for this rotation.

c) Calculate the rotated quaternion $p' = q p q^{-1}$.

d) Extract the vector part of $p'$ to find the rotated vector $v'$.

### Solution 4

a) **Write the vector $v$ as a pure quaternion $p$.**

$$p = 1i + 0j + 0k = i$$

b) **Write the unit quaternion $q$ for this rotation.**

Rotation by $\pi/2$ around the z-axis. $\theta=\pi/2, \hat{n}=(0,0,1)$.

$$q = \cos(\pi/4) + \sin(\pi/4)k = \frac{1}{\sqrt{2}}(1+k)$$

c) **Calculate the rotated quaternion $p' = q p q^{-1}$.**

$$q^{-1} = q^* = \frac{1}{\sqrt{2}}(1-k)$$

$$p' = \frac{1}{2}(1+k)i(1-k) = \frac{1}{2}(i+ki)(1-k) = \frac{1}{2}(i+j)(1-k) = \frac{1}{2}(i-ik+j-jk) = \frac{1}{2}(i+j+j-i) = j$$

d) **Extract the vector part of $p'$ to find the rotated vector $v'$.**

$p' = j$, so the vector is $(0,1,0)$.

A rotation of $(1,0,0)$ by $\pi/2$ around the z-axis is $(0,1,0)$. Correct.

## Problem 5: Composition of Rotations

Composition of rotations corresponds to multiplication of quaternions.

a) Find the quaternion $q_1$ for a 90-degree rotation around the x-axis.

b) Find the quaternion $q_2$ for a 90-degree rotation around the y-axis.

c) Calculate the quaternion $q_3 = q_2 q_1$. This represents doing rotation 1, then rotation 2.

d) What is the axis and angle of the single rotation described by $q_3$?

### Solution 5

a) **Find the quaternion $q_1$ for a 90-degree rotation around the x-axis.**

$\theta=\pi/2, \hat{n}=(1,0,0)$.

$$q_1 = \cos(\pi/4) + \sin(\pi/4)i = \frac{1}{\sqrt{2}}(1+i)$$

b) **Find the quaternion $q_2$ for a 90-degree rotation around the y-axis.**

$\theta=\pi/2, \hat{n}=(0,1,0)$.

$$q_2 = \cos(\pi/4) + \sin(\pi/4)j = \frac{1}{\sqrt{2}}(1+j)$$

c) **Calculate the quaternion $q_3 = q_2 q_1$.**

$$q_3 = \frac{1}{2}(1+j)(1+i) = \frac{1}{2}(1+i+j+ji) = \frac{1}{2}(1+i+j-k)$$

d) **What is the axis and angle of the single rotation described by $q_3$?**

$$q_3 = \cos(\theta/2) + \sin(\theta/2)(n_x i + n_y j + n_z k)$$

$$\cos(\theta/2) = 1/2 \implies \theta/2 = \pi/3 \implies \theta=2\pi/3 = 120°$$

$$\sin(\theta/2) = \sqrt{3}/2$$

So:
$$\frac{\sqrt{3}}{2}(n_x i + n_y j + n_z k) = \frac{1}{2}(i+j-k)$$

$$(n_x, n_y, n_z) = \frac{1}{\sqrt{3}}(1, 1, -1)$$

Axis is $(1,1,-1)/\sqrt{3}$, angle is $120°$.