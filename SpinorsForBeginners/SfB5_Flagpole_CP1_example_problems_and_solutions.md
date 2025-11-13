This lecture discusses the complex projective space CP^1, also known as the Riemann sphere, and its relationship to spinors. The "flagpole" refers to the geometric interpretation of a spinor.

## Problem 1: The Riemann Sphere

The complex projective space CP^1 is the space of all complex lines through the origin in C^2. A point in CP^1 can be represented by homogeneous coordinates $[\xi_1, \xi_2]$, where $\xi_1, \xi_2$ are complex numbers, not both zero. This is equivalent to the ratio $\zeta = \xi_1 / \xi_2$, which is a single complex number, or $\infty$. This is the extended complex plane, which can be mapped to the Riemann sphere.

a) A spinor $\xi = \begin{pmatrix} \xi_1 \\ \xi_2 \end{pmatrix}$ defines a point on the Riemann sphere. What point corresponds to the spin-up state $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$?

b) What point corresponds to the spin-down state $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$?

c) What point corresponds to the state $\frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$?

### Solution 1

a) **A spinor $\xi = \begin{pmatrix} \xi_1 \\ \xi_2 \end{pmatrix}$ defines a point on the Riemann sphere. What point corresponds to the spin-up state $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$?**

The ratio is $\zeta = \xi_1 / \xi_2 = 1/0 = \infty$. This corresponds to the North Pole of the Riemann sphere.

b) **What point corresponds to the spin-down state $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$?**

The ratio is $\zeta = \xi_1 / \xi_2 = 0/1 = 0$. This corresponds to the South Pole of the Riemann sphere.

c) **What point corresponds to the state $\frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$?**

The ratio is $\zeta = \xi_1 / \xi_2 = 1/1 = 1$. This is the point $(1,0)$ in the complex plane.

## Problem 2: Stereographic Projection

The mapping from the Riemann sphere to the complex plane is often done via stereographic projection. A point $(X, Y, Z)$ on the unit sphere $X^2+Y^2+Z^2=1$ is mapped to a complex number $\zeta = x+iy$. The projection from the North Pole $(0,0,1)$ is given by:
$$\zeta = \frac{X+iY}{1-Z}$$

A spinor $\xi = \begin{pmatrix} \alpha \\ \beta \end{pmatrix}$ can be associated with a point on the sphere via the expectation values of the Pauli matrices:
$$X = \xi^\dagger \sigma_1 \xi, \quad Y = \xi^\dagger \sigma_2 \xi, \quad Z = \xi^\dagger \sigma_3 \xi$$

Let $\xi = \frac{1}{\sqrt{5}}\begin{pmatrix} 1 \\ 2i \end{pmatrix}$.

a) Calculate the vector $(X, Y, Z)$ on the Bloch sphere corresponding to this spinor.

b) Calculate the complex number $\zeta$ corresponding to this spinor using the ratio of its components.

c) Verify that the stereographic projection formula relates the two results.

### Solution 2

Let $\xi = \frac{1}{\sqrt{5}}\begin{pmatrix} 1 \\ 2i \end{pmatrix}$.

a) **Calculate the vector $(X, Y, Z)$ on the Bloch sphere corresponding to this spinor.**

$$X = \xi^\dagger \sigma_1 \xi = \frac{1}{5}\begin{pmatrix} 1 & -2i \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2i \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 1 & -2i \end{pmatrix} \begin{pmatrix} 2i \\ 1 \end{pmatrix} = \frac{1}{5}(2i - 2i) = 0$$

$$Y = \xi^\dagger \sigma_2 \xi = \frac{1}{5}\begin{pmatrix} 1 & -2i \end{pmatrix} \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2i \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 1 & -2i \end{pmatrix} \begin{pmatrix} 2 \\ i \end{pmatrix} = \frac{1}{5}(2 - 2i^2) = \frac{4}{5}$$

$$Z = \xi^\dagger \sigma_3 \xi = \frac{1}{5}\begin{pmatrix} 1 & -2i \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 2i \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 1 & -2i \end{pmatrix} \begin{pmatrix} 1 \\ -2i \end{pmatrix} = \frac{1}{5}(1 + 4i^2) = -\frac{3}{5}$$

So the vector is $(0, 4/5, -3/5)$.

b) **Calculate the complex number $\zeta$ corresponding to this spinor using the ratio of its components.**

$$\zeta = \xi_1 / \xi_2 = 1 / (2i) = -i/2$$

c) **Verify that the stereographic projection formula relates the two results.**

Using the formula $\zeta = \frac{X+iY}{1-Z}$, we get:
$$\zeta = \frac{0 + i(4/5)}{1 - (-3/5)} = \frac{4i/5}{8/5} = \frac{i}{2}$$

There is a sign difference, which can arise from different conventions for the stereographic projection or the definition of the Stokes parameters. If we use the convention $\zeta = \frac{X-iY}{1-Z}$, we get the correct result.

## Problem 3: The "Flagpole"

The flagpole interpretation associates a spinor with a null vector (the flagpole) and a flag. A spinor $\xi$ defines a null vector $k^\mu = \xi^\dagger \sigma^\mu \xi$. It also defines a "flag" which is a complex plane.

Let $\xi = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$.

a) Calculate the null vector $k^\mu$ associated with this spinor. This is the "flagpole".

b) The spinor itself can be thought of as the "flag". How does the flagpole and flag change if we apply a Lorentz transformation to the spinor?

### Solution 3

a) **Calculate the null vector $k^\mu = \xi^\dagger \sigma^\mu \xi$ associated with this spinor.**

Let $\xi = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$ (normalized).

$$\sigma^\mu = (I, \sigma_x, \sigma_y, \sigma_z)$$

$$k^0 = \xi^\dagger I \xi = \frac{1}{2}\begin{pmatrix} 1 & 1 \end{pmatrix}\begin{pmatrix} 1 \\ 1 \end{pmatrix} = 1$$

$$k^1 = \xi^\dagger \sigma_x \xi = \frac{1}{2}\begin{pmatrix} 1 & 1 \end{pmatrix}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1 & 1 \end{pmatrix}\begin{pmatrix} 1 \\ 1 \end{pmatrix} = 1$$

$$k^2 = \xi^\dagger \sigma_y \xi = \frac{1}{2}\begin{pmatrix} 1 & 1 \end{pmatrix}\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}\begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1 & 1 \end{pmatrix}\begin{pmatrix} -i \\ i \end{pmatrix} = 0$$

$$k^3 = \xi^\dagger \sigma_z \xi = \frac{1}{2}\begin{pmatrix} 1 & 1 \end{pmatrix}\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}\begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1 & 1 \end{pmatrix}\begin{pmatrix} 1 \\ -1 \end{pmatrix} = 0$$

So $k^\mu = (1, 1, 0, 0)$. This is a null vector since $(k^0)^2 - (k^1)^2 - (k^2)^2 - (k^3)^2 = 1-1-0-0=0$.

b) **How does the flagpole and flag change if we apply a Lorentz transformation to the spinor?**

The spinor transforms under the spin representation of the Lorentz group. The flagpole, being a 4-vector, transforms as a vector under the same Lorentz transformation. The flag (the spinor itself) transforms as a spinor.

## Problem 4: SU(2) transformations and the Riemann Sphere

An SU(2) transformation on a spinor $\xi$ corresponds to a rotation of the Riemann sphere.
$$U = \begin{pmatrix} a & b \\ -b^* & a^* \end{pmatrix} \text{ with } |a|^2+|b|^2=1$$

The spinor transforms as $\xi' = U\xi$. The complex number $\zeta = \xi_1/\xi_2$ transforms as:
$$\zeta' = \frac{a\zeta + b}{-b^*\zeta + a^*}$$
This is a Möbius transformation.

a) Show that a rotation around the z-axis, $U = \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \end{pmatrix}$, corresponds to a rotation of the complex plane $\zeta' = e^{-i\theta}\zeta$.

b) What is the geometric interpretation of this transformation on the Riemann sphere?

### Solution 4

a) **Show that a rotation around the z-axis, $U = \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \end{pmatrix}$, corresponds to a rotation of the complex plane $\zeta' = e^{-i\theta}\zeta$.**

$$\xi' = U\xi = \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \end{pmatrix} \begin{pmatrix} \xi_1 \\ \xi_2 \end{pmatrix} = \begin{pmatrix} e^{-i\theta/2}\xi_1 \\ e^{i\theta/2}\xi_2 \end{pmatrix}$$

$$\zeta' = \frac{\xi'_1}{\xi'_2} = \frac{e^{-i\theta/2}\xi_1}{e^{i\theta/2}\xi_2} = e^{-i\theta}\frac{\xi_1}{\xi_2} = e^{-i\theta}\zeta$$

b) **What is the geometric interpretation of this transformation on the Riemann sphere?**

This is a rotation of the sphere around the Z-axis by an angle $\theta$.

## Problem 5: Orthogonality of Spinors

Two spinors $\xi$ and $\eta$ are orthogonal if $\xi^\dagger \eta = 0$. Geometrically, two spinors are orthogonal if they point to opposite poles on the Riemann sphere.

a) Let $\xi = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$. Find an orthogonal spinor $\eta$.

b) What are the coordinates of $\xi$ and $\eta$ on the Riemann sphere? Are they antipodal?

c) Let $\xi = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$. Find an orthogonal spinor $\eta$.

d) Verify that the points on the Riemann sphere corresponding to $\xi$ and $\eta$ are antipodal.

### Solution 5

a) **Let $\xi = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$. Find an orthogonal spinor $\eta$.**

We need $\xi^\dagger \eta = 0$. 
$$\begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} \eta_1 \\ \eta_2 \end{pmatrix} = \eta_1 = 0$$

So any spinor of the form $\begin{pmatrix} 0 \\ c \end{pmatrix}$ is orthogonal. The simplest is $\eta = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.

b) **What are the coordinates of $\xi$ and $\eta$ on the Riemann sphere? Are they antipodal?**

For $\xi$, $\zeta = 1/0 = \infty$ (North Pole).
For $\eta$, $\zeta = 0/1 = 0$ (South Pole).
Yes, they are antipodal.

c) **Let $\xi = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$. Find an orthogonal spinor $\eta$.**

We need $\xi^\dagger \eta = 0$. 
$$\frac{1}{\sqrt{2}}\begin{pmatrix} 1 & 1 \end{pmatrix} \begin{pmatrix} \eta_1 \\ \eta_2 \end{pmatrix} = \frac{1}{\sqrt{2}}(\eta_1 + \eta_2) = 0$$

So we need $\eta_1 = -\eta_2$. Let's choose $\eta_1 = 1, \eta_2 = -1$.
Normalized, $\eta = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ -1 \end{pmatrix}$.

d) **Verify that the points on the Riemann sphere corresponding to $\xi$ and $\eta$ are antipodal.**

For $\xi$, $\zeta_1 = 1/1 = 1$.
For $\eta$, $\zeta_2 = 1/(-1) = -1$.

On the Riemann sphere, $\zeta=1$ corresponds to the point $(1,0,0)$.
$\zeta=-1$ corresponds to the point $(-1,0,0)$.
These are antipodal points on the sphere.