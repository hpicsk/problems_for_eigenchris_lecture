# Example Problems and Solutions: Polarizations and SU(2)

This lecture connects the Jones calculus for polarization with the mathematics of SU(2), likely via the Poincaré sphere.

## Problem 1: Jones Vectors and SU(2)

The Jones vector for a general elliptical polarization state can be written as $\begin{pmatrix} \cos\alpha \\ e^{i\delta}\sin\alpha \end{pmatrix}$. This is a 2-component complex vector, an element of $\mathbb{C}^2$. The group of transformations that preserve the norm of this vector is $U(2)$. If we ignore the global phase, the transformations are in $SU(2)$.

a) Show that the Jones vectors for horizontal and vertical polarization are orthogonal.

b) Show that the Jones vectors for right and left circular polarization are orthogonal.

c) An arbitrary $SU(2)$ matrix can be written as $U = \begin{pmatrix} a & b \\ -b^* & a^* \end{pmatrix}$ with $|a|^2+|b|^2=1$.
   Let $U$ be a half-wave plate with its fast axis at an angle $\theta$ to the horizontal. Write down the matrix for $U$. Show that it is in $SU(2)$.

### Solution 1:

a) **Show that the Jones vectors for horizontal and vertical polarization are orthogonal.**

Horizontal polarization: $J_H = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

Vertical polarization: $J_V = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.

The inner product is:
$$J_H^\dagger J_V = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = 1 \cdot 0 + 0 \cdot 1 = 0$$

They are orthogonal.

b) **Show that the Jones vectors for right and left circular polarization are orthogonal.**

Right circular polarization: $J_{RCP} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ i \end{pmatrix}$.

Left circular polarization: $J_{LCP} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -i \end{pmatrix}$.

The inner product is:
$$J_{LCP}^\dagger J_{RCP} = \frac{1}{2} \begin{pmatrix} 1 & -i \end{pmatrix} \begin{pmatrix} 1 \\ i \end{pmatrix} = \frac{1}{2}(1 \cdot 1 + (-i) \cdot i) = \frac{1}{2}(1 + 1) = 1$$

Wait, this is incorrect. Let me recalculate:
$$J_{LCP}^\dagger J_{RCP} = \frac{1}{2} \begin{pmatrix} 1 & i \end{pmatrix} \begin{pmatrix} 1 \\ i \end{pmatrix} = \frac{1}{2}(1 \cdot 1 + i \cdot i) = \frac{1}{2}(1 - 1) = 0$$

They are orthogonal.

c) **An arbitrary $SU(2)$ matrix can be written as $U = \begin{pmatrix} a & b \\ -b^* & a^* \end{pmatrix}$ with $|a|^2+|b|^2=1$. Let $U$ be a half-wave plate with its fast axis at an angle $\theta$ to the horizontal. Write down the matrix for $U$. Show that it is in $SU(2)$.**

The Jones matrix for a half-wave plate at angle $\theta$ is:
$$W' = \begin{pmatrix} \cos(2\theta) & \sin(2\theta) \\ \sin(2\theta) & -\cos(2\theta) \end{pmatrix}$$

This matrix is unitary and has determinant $-1$, so it is in $U(2)$ but not $SU(2)$. To make it an $SU(2)$ transformation, we need to multiply by $i$:

$$U = iW' = \begin{pmatrix} i\cos(2\theta) & i\sin(2\theta) \\ i\sin(2\theta) & -i\cos(2\theta) \end{pmatrix}$$

This has determinant $1$ and is unitary. Setting $a = i\cos(2\theta)$ and $b = i\sin(2\theta)$, we have:
- $a^* = -i\cos(2\theta)$
- $-b^* = -i\sin(2\theta)$

The matrix becomes:
$$U = \begin{pmatrix} a & b \\ b & -a \end{pmatrix}$$

This is not quite in the standard $SU(2)$ form, but represents the same transformation up to an overall phase.

## Problem 2: The Poincaré Sphere

Any state of polarization can be mapped to a point on the surface of the Poincaré sphere. The mapping is defined by the Stokes parameters:

$$S_0 = |E_x|^2 + |E_y|^2$$
$$S_1 = |E_x|^2 - |E_y|^2$$
$$S_2 = 2\text{Re}(E_x^* E_y)$$
$$S_3 = 2\text{Im}(E_x^* E_y)$$

The coordinates on the sphere are $(S_1/S_0, S_2/S_0, S_3/S_0)$.

For the following polarization states, find the Jones vector and the corresponding point on the Poincaré sphere:

a) Horizontally polarized light.

b) Vertically polarized light.

c) Light polarized at 45 degrees to the horizontal.

d) Right-circularly polarized light.

### Solution 2:

a) **Horizontally polarized light.**

Jones vector: $J_H = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

Stokes parameters: $S_0 = 1$, $S_1 = 1$, $S_2 = 0$, $S_3 = 0$.

Poincaré sphere coordinates: $(1, 0, 0)$.

b) **Vertically polarized light.**

Jones vector: $J_V = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.

Stokes parameters: $S_0 = 1$, $S_1 = -1$, $S_2 = 0$, $S_3 = 0$.

Poincaré sphere coordinates: $(-1, 0, 0)$.

c) **Light polarized at 45 degrees to the horizontal.**

Jones vector: $J_{45} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix}$.

Stokes parameters: 
- $S_0 = 1$
- $S_1 = 0$
- $S_2 = 2\text{Re}\left(\frac{1}{\sqrt{2}} \cdot \frac{1}{\sqrt{2}}\right) = 2 \cdot \frac{1}{2} = 1$
- $S_3 = 0$

Poincaré sphere coordinates: $(0, 1, 0)$.

d) **Right-circularly polarized light.**

Jones vector: $J_{RCP} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ i \end{pmatrix}$.

Stokes parameters:
- $S_0 = 1$
- $S_1 = 0$
- $S_2 = 2\text{Re}\left(\frac{1}{\sqrt{2}} \cdot \frac{-i}{\sqrt{2}}\right) = 0$
- $S_3 = 2\text{Im}\left(\frac{1}{\sqrt{2}} \cdot \frac{-i}{\sqrt{2}}\right) = 2 \cdot \left(-\frac{1}{2}\right) = -1$

Poincaré sphere coordinates: $(0, 0, -1)$.

## Problem 3: SU(2) Rotations on the Poincaré Sphere

An $SU(2)$ transformation on the Jones vector corresponds to a rotation of the Poincaré sphere.
The relationship is that the vector of Stokes parameters $(S_1, S_2, S_3)$ transforms as a 3D vector under a rotation in $SO(3)$. The group $SU(2)$ is the double cover of $SO(3)$.

A rotation of the Poincaré sphere by an angle $\Theta$ around an axis $\hat{n}$ corresponds to an $SU(2)$ matrix $U = \exp(-i\frac{\Theta}{2}\hat{n}\cdot\sigma)$.

a) A quarter-wave plate with its fast axis horizontal corresponds to a rotation of the Poincaré sphere by $\pi/2$ around the $S_1$ axis. What is the $SU(2)$ matrix for this operation?

b) How does this matrix act on horizontally polarized light? What is the resulting polarization state?

c) How does this matrix act on light polarized at 45 degrees? What is the resulting polarization state?

### Solution 3:

a) **A quarter-wave plate with its fast axis horizontal corresponds to a rotation of the Poincaré sphere by $\pi/2$ around the $S_1$ axis. What is the $SU(2)$ matrix for this operation?**

The rotation is by $\Theta = \pi/2$ around the axis $\hat{n} = (1,0,0)$.

The $SU(2)$ matrix is:
$$U = \exp(-i\frac{\Theta}{2}\hat{n}\cdot\sigma) = \exp(-i\frac{\pi}{4}\sigma_1)$$

$$U = \cos(\pi/4)I - i\sin(\pi/4)\sigma_1 = \frac{1}{\sqrt{2}}(I - i\sigma_1) = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -i \\ -i & 1 \end{pmatrix}$$

b) **How does this matrix act on horizontally polarized light? What is the resulting polarization state?**

Horizontally polarized light: $J_H = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

$$U J_H = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -i \\ -i & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -i \end{pmatrix}$$

This is right-circularly polarized light.

c) **How does this matrix act on light polarized at 45 degrees? What is the resulting polarization state?**

Light polarized at 45 degrees: $J_{45} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix}$.

$$U J_{45} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -i \\ -i & 1 \end{pmatrix} \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 1-i \\ 1-i \end{pmatrix} = \frac{1-i}{2} \begin{pmatrix} 1 \\ 1 \end{pmatrix}$$

This is still light polarized at 45 degrees, but with a phase shift. The polarization state is unchanged because the axis of rotation is along the direction of the state on the Poincaré sphere.

## Problem 4: Decomposing Optical Elements

Any $SU(2)$ transformation can be decomposed into a sequence of wave plates and rotators. An arbitrary $SU(2)$ element can be parameterized with Euler angles:

$$U = R_z(\alpha) R_y(\beta) R_z(\gamma)$$

where $R_y$ and $R_z$ are rotations about the y and z axes.

a) What optical elements correspond to $R_y$ and $R_z$ rotations on the Poincaré sphere?

b) This shows that any polarization state can be reached from any other using a sequence of these elements. Design a system of optical elements that converts horizontally polarized light into right-circularly polarized light.

### Solution 4:

a) **What optical elements correspond to $R_y$ and $R_z$ rotations on the Poincaré sphere?**

- $R_z(\gamma)$ corresponds to a rotation around the $S_3$ axis (the axis connecting the circular polarizations). This transformation changes the phase between the linear components, which is what an optical rotator does.

- $R_y(\beta)$ corresponds to a rotation around the $S_2$ axis (the axis connecting the +45 and -45 degree linear polarizations). This can be achieved with a combination of wave plates, for example a half-wave plate with its axis at an angle.

b) **Design a system of optical elements that converts horizontally polarized light into right-circularly polarized light.**

We want to transform horizontally polarized light ($S_1=1$) to right-circularly polarized light ($S_3=-1$). 

To get from horizontal to RCP, we need to rotate the Poincaré sphere by $\pi/2$ around the $S_2$ axis. This is a rotation from the x-axis to the -z-axis. The optical element that does this is a quarter-wave plate with its fast axis at 45 degrees to the horizontal.

## Problem 5: The Double Cover

The $SU(2)$-$SO(3)$ relationship is 2-to-1. This means that a rotation of $2\pi$ in $SU(2)$ corresponds to a rotation of $4\pi$ on the Poincaré sphere (which is the identity). A rotation of $2\pi$ on the Poincaré sphere (the identity) corresponds to a rotation of $\pi$ in $SU(2)$.

a) What is the $SU(2)$ matrix for a $2\pi$ rotation around the z-axis?

b) How does this matrix affect a general Jones vector?

c) What is the physical significance of this sign change? (This is the spinorial nature of polarization).

d) Can this overall sign be detected in a simple intensity measurement? Why or why not?

### Solution 5:

a) **What is the $SU(2)$ matrix for a $2\pi$ rotation around the z-axis?**

$$U = \exp(-i\frac{2\pi}{2}\sigma_3) = \exp(-i\pi\sigma_3) = \cos(-\pi)I - i\sin(-\pi)\sigma_3 = -I = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$$

b) **How does this matrix affect a general Jones vector?**

It multiplies the Jones vector by $-1$.

c) **What is the physical significance of this sign change? (This is the spinorial nature of polarization).**

The state of polarization is described by a spinor, which acquires a phase of $-1$ under a $2\pi$ rotation. This is a fundamental property of spin-1/2 systems, and polarization of light provides an accessible classical system that exhibits this quantum-like behavior.

d) **Can this overall sign be detected in a simple intensity measurement? Why or why not?**

No. The intensity is proportional to $|E_x|^2 + |E_y|^2$. If the Jones vector is multiplied by $-1$, the intensity is $|-E_x|^2 + |-E_y|^2 = |E_x|^2 + |E_y|^2$. The intensity is unchanged. To detect the sign change, one would need to perform an interference experiment where the rotated beam is compared to an unrotated reference beam.