# SfB 2: Jones Vectors - Example Problems and Solutions

This lecture introduces the Jones calculus, a mathematical framework for describing the polarization of light.

## Problem 1: Basic Jones Vectors

Write down the normalized Jones vectors for the following states of linear polarization:

a) Horizontally polarized light (along the x-axis).

b) Vertically polarized light (along the y-axis).

c) Linearly polarized light at an angle of +45 degrees to the x-axis.

d) Linearly polarized light at an angle of -45 degrees to the x-axis.

e) Linearly polarized light at an angle $\theta$ to the x-axis.

### Solution 1:

a) **Horizontally polarized light (along the x-axis).**

The electric field oscillates along the x-axis. The Jones vector is:
$$\begin{pmatrix} 1 \\ 0 \end{pmatrix}$$

b) **Vertically polarized light (along the y-axis).**

The electric field oscillates along the y-axis. The Jones vector is:
$$\begin{pmatrix} 0 \\ 1 \end{pmatrix}$$

c) **Linearly polarized light at an angle of +45 degrees to the x-axis.**

The components are equal and in phase. The normalized Jones vector is:
$$\frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix}$$

d) **Linearly polarized light at an angle of -45 degrees to the x-axis.**

The y-component is 180 degrees out of phase with the x-component. The normalized Jones vector is:
$$\frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -1 \end{pmatrix}$$

e) **Linearly polarized light at an angle $\theta$ to the x-axis.**

The components are given by the projection of a unit vector at angle $\theta$. The Jones vector is:
$$\begin{pmatrix} \cos\theta \\ \sin\theta \end{pmatrix}$$

## Problem 2: Circular and Elliptical Polarization

The general form of a Jones vector is $\begin{pmatrix} E_x \\ E_y \end{pmatrix}$, where $E_x$ and $E_y$ are complex numbers representing the amplitude and phase of the electric field components.

$$\vec{E}(t) = \text{Re}\left( \begin{pmatrix} E_x \\ E_y \end{pmatrix} e^{-i\omega t} \right)$$

a) Write down the Jones vector for right-circularly polarized (RCP) light.

b) Write down the Jones vector for left-circularly polarized (LCP) light.

c) Show that RCP and LCP vectors are orthogonal.

d) What is the Jones vector for light that is right-elliptically polarized, with the major axis horizontal and twice the length of the vertical minor axis?

### Solution 2:

a) **Write down the Jones vector for right-circularly polarized (RCP) light.**

For RCP light, the y-component leads the x-component by 90 degrees ($e^{i\pi/2} = i$). The normalized Jones vector is:
$$\frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ i \end{pmatrix}$$

b) **Write down the Jones vector for left-circularly polarized (LCP) light.**

For LCP light, the y-component lags the x-component by 90 degrees ($e^{-i\pi/2} = -i$). The normalized Jones vector is:
$$\frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -i \end{pmatrix}$$

c) **Show that RCP and LCP vectors are orthogonal.**

To check for orthogonality, we take the Hermitian inner product (dot product of one vector with the complex conjugate of the other). Let $J_{RCP}$ and $J_{LCP}$ be the Jones vectors for RCP and LCP light.

$$J_{LCP}^\dagger J_{RCP} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -i \end{pmatrix} \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ -i \end{pmatrix} = \frac{1}{2}(1 \cdot 1 + (-i) \cdot (-i)) = \frac{1}{2}(1 - 1) = 0$$

Since the inner product is zero, the vectors are orthogonal.

d) **What is the Jones vector for light that is right-elliptically polarized, with the major axis horizontal and twice the length of the vertical minor axis?**

The amplitude of the horizontal component is twice the amplitude of the vertical component. For right-elliptical polarization, the y-component lags the x-component by 90 degrees.

The unnormalized Jones vector is $\begin{pmatrix} 2 \\ -i \end{pmatrix}$.

Normalizing this gives:
$$\frac{1}{\sqrt{2^2 + (-i)(i)}} \begin{pmatrix} 2 \\ -i \end{pmatrix} = \frac{1}{\sqrt{5}} \begin{pmatrix} 2 \\ -i \end{pmatrix}$$

## Problem 3: Jones Matrices for Optical Elements

Optical elements are represented by $2 \times 2$ Jones matrices.

a) Write down the Jones matrix for a linear polarizer that transmits only horizontally polarized light.

b) Write down the Jones matrix for a linear polarizer that transmits only vertically polarized light.

c) Write down the Jones matrix for a linear polarizer that transmits light polarized at +45 degrees.
   (Hint: rotate the horizontal polarizer matrix).

### Solution 3:

a) **Write down the Jones matrix for a linear polarizer that transmits only horizontally polarized light.**

This matrix should project any Jones vector onto the horizontal direction.
$$P_H = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$$

b) **Write down the Jones matrix for a linear polarizer that transmits only vertically polarized light.**

This matrix should project any Jones vector onto the vertical direction.
$$P_V = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}$$

c) **Write down the Jones matrix for a linear polarizer that transmits light polarized at +45 degrees.**

We can obtain this by rotating the horizontal polarizer matrix by +45 degrees. The rotation matrix is $R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$.

$$P_{45} = R(45°) P_H R(-45°) = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix} \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ -1 & 1 \end{pmatrix}$$

$$= \frac{1}{2} \begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 0 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}$$

## Problem 4: Wave Plates

Wave plates introduce a phase shift between the two orthogonal components of the electric field.

a) Write down the Jones matrix for a quarter-wave plate with its fast axis along the x-axis.

b) Write down the Jones matrix for a half-wave plate with its fast axis along the y-axis.

c) A half-wave plate has its fast axis at an angle $\theta$ to the horizontal. What is its Jones matrix?
   (Hint: Rotate into the basis of the wave plate, apply the wave plate matrix, and rotate back).

### Solution 4:

a) **Write down the Jones matrix for a quarter-wave plate with its fast axis along the x-axis.**

A quarter-wave plate introduces a phase shift of $\pi/2$ between the components. If the fast axis is horizontal, the x-component is advanced by $\pi/4$ and the y-component is retarded by $\pi/4$. The relative phase shift is $\pi/2$.

The matrix is:
$$e^{i\pi/4} \begin{pmatrix} e^{-i\pi/4} & 0 \\ 0 & e^{i\pi/4} \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & e^{i\pi/2} \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & i \end{pmatrix}$$

(Note: The overall phase factor $e^{i\pi/4}$ is often omitted, as it does not affect the polarization state.)

b) **Write down the Jones matrix for a half-wave plate with its fast axis along the y-axis.**

A half-wave plate introduces a phase shift of $\pi$. If the fast axis is vertical, the y-component is advanced by $\pi/2$ and the x-component is retarded by $\pi/2$. The relative phase shift is $\pi$.

The matrix is:
$$e^{-i\pi/2} \begin{pmatrix} e^{-i\pi/2} & 0 \\ 0 & e^{i\pi/2} \end{pmatrix} = \begin{pmatrix} e^{-i\pi} & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}$$

c) **A half-wave plate has its fast axis at an angle $\theta$ to the horizontal. What is its Jones matrix?**

We rotate into the basis of the wave plate, apply the wave plate matrix for a horizontal fast axis, and then rotate back.

The matrix for a half-wave plate with horizontal fast axis is $W = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$.

The rotated matrix is $W' = R(\theta) W R(-\theta)$.

$$W' = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix}$$

$$= \begin{pmatrix} \cos\theta & \sin\theta \\ \sin\theta & -\cos\theta \end{pmatrix} \begin{pmatrix} \cos\theta & \sin\theta \\ -\sin\theta & \cos\theta \end{pmatrix}$$

$$= \begin{pmatrix} \cos^2\theta - \sin^2\theta & 2\sin\theta\cos\theta \\ 2\sin\theta\cos\theta & \sin^2\theta - \cos^2\theta \end{pmatrix} = \begin{pmatrix} \cos(2\theta) & \sin(2\theta) \\ \sin(2\theta) & -\cos(2\theta) \end{pmatrix}$$

## Problem 5: System of Optical Elements

A beam of unpolarized light can be considered as an incoherent sum of horizontal and vertical polarizations. Let's start with horizontally polarized light with intensity $I_0$.

The light passes through the following sequence of elements:

1. A linear polarizer at +45 degrees.
2. A quarter-wave plate with its fast axis horizontal.
3. A linear polarizer at -45 degrees.

a) What is the Jones vector of the light after passing through the first element? What is its intensity?

b) What is the Jones vector of the light after passing through the second element? What is its polarization state?

c) What is the Jones vector of the light after passing through the final element? What is the final intensity of the light?

### Solution 5:

Initial light is horizontally polarized: $J_{in} = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$. Initial intensity is $I_0$.

a) **1. A linear polarizer at +45 degrees.**

The Jones matrix is $P_{45} = \frac{1}{2} \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}$.

The Jones vector after the polarizer is:
$$J_1 = P_{45} J_{in} = \frac{1}{2} \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 1 \\ 1 \end{pmatrix}$$

This is light linearly polarized at +45 degrees.

The intensity is proportional to the squared norm of the Jones vector.
$$I_1 = |J_1|^2 = \left(\frac{1}{2}\right)^2 (1^2 + 1^2) = \frac{1}{4} \cdot 2 = \frac{1}{2}$$

The intensity is $I_0/2$.

b) **2. A quarter-wave plate with its fast axis horizontal.**

The Jones matrix is $W_{Q} = \begin{pmatrix} 1 & 0 \\ 0 & i \end{pmatrix}$.

The Jones vector after the wave plate is:
$$J_2 = W_Q J_1 = \begin{pmatrix} 1 & 0 \\ 0 & i \end{pmatrix} \frac{1}{2} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 1 \\ i \end{pmatrix}$$

This is left-circularly polarized light (up to a normalization factor).

c) **3. A linear polarizer at -45 degrees.**

The Jones matrix for a polarizer at -45 degrees is $P_{-45} = \frac{1}{2} \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix}$.

The final Jones vector is:
$$J_3 = P_{-45} J_2 = \frac{1}{2} \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix} \frac{1}{2} \begin{pmatrix} 1 \\ i \end{pmatrix} = \frac{1}{4} \begin{pmatrix} 1-i \\ -1+i \end{pmatrix} = \frac{1-i}{4} \begin{pmatrix} 1 \\ -1 \end{pmatrix}$$

This is light linearly polarized at -45 degrees.

The final intensity is:
$$I_3 = |J_3|^2 = \left|\frac{1-i}{4}\right|^2 (1^2 + (-1)^2) = \left(\frac{\sqrt{2}}{4}\right)^2 \cdot 2 = \frac{2}{16} \cdot 2 = \frac{4}{16} = \frac{1}{4}$$

The final intensity is $I_0/4$.