# Example Problems and Solutions: Integration With Differential Forms

## Integration of k-forms

### Problem 1
Evaluate the integral of the 1-form $\omega = y \, dx - x \, dy$ over the curve $\mathbf{c}(t) = (\cos(t), \sin(t))$ for $t$ from $0$ to $2\pi$.

### Solution 1
For the parametric curve $\mathbf{c}(t) = (\cos(t), \sin(t))$:
$$x(t) = \cos(t), \quad y(t) = \sin(t)$$
$$dx = -\sin(t) \, dt, \quad dy = \cos(t) \, dt$$

The integral becomes:
$$\int_C \omega = \int_0^{2\pi} [y \, dx - x \, dy]$$
$$= \int_0^{2\pi} [\sin(t)(-\sin(t) \, dt) - \cos(t)(\cos(t) \, dt)]$$
$$= \int_0^{2\pi} [-\sin^2(t) - \cos^2(t)] \, dt$$
$$= \int_0^{2\pi} -1 \, dt = -2\pi$$

### Problem 2
Evaluate the integral of the 2-form $\eta = x \, dx \wedge dy$ over the unit square in the xy-plane (i.e., the region $0 \leq x \leq 1$, $0 \leq y \leq 1$).

### Solution 2
For a 2-form $\eta = x \, dx \wedge dy$ over a region in the xy-plane:
$$\iint_S \eta = \iint_S x \, dx \wedge dy = \int_0^1 \int_0^1 x \, dx \, dy$$

$$= \int_0^1 \left[\frac{x^2}{2}\right]_0^1 dy = \int_0^1 \frac{1}{2} \, dy = \frac{1}{2} \cdot 1 = \frac{1}{2}$$

### Problem 3
Evaluate the integral of the 3-form $\tau = z \, dx \wedge dy \wedge dz$ over the cube defined by $0 \leq x \leq 1$, $0 \leq y \leq 1$, $0 \leq z \leq 1$.

### Solution 3
For the 3-form over the unit cube:
$$\iiint_V \tau = \iiint_V z \, dx \wedge dy \wedge dz = \int_0^1 \int_0^1 \int_0^1 z \, dx \, dy \, dz$$

$$= \int_0^1 \int_0^1 [x]_0^1 \, z \, dy \, dz = \int_0^1 \int_0^1 z \, dy \, dz$$

$$= \int_0^1 [y]_0^1 \, z \, dz = \int_0^1 z \, dz = \left[\frac{z^2}{2}\right]_0^1 = \frac{1}{2}$$

## Stokes' Theorem

Stokes' theorem for differential forms states that $\int_M d\omega = \int_{\partial M} \omega$, where $M$ is a manifold and $\partial M$ is its boundary.

### Problem 4
Let $\omega = x \, dy - y \, dx$ be a 1-form in $\mathbb{R}^2$. Let $M$ be the unit disk $x^2 + y^2 \leq 1$. Verify Stokes' theorem for this case.

### Solution 4
First, compute the exterior derivative:
$$d\omega = d(x) \wedge dy - d(y) \wedge dx = dx \wedge dy - dy \wedge dx = dx \wedge dy + dx \wedge dy = 2 \, dx \wedge dy$$

The left side of Stokes' theorem:
$$\int_M d\omega = \iint_{x^2+y^2 \leq 1} 2 \, dx \wedge dy = 2 \cdot \text{Area}(\text{disk}) = 2\pi$$

For the right side, the boundary $\partial M$ is the unit circle, parameterized by $\mathbf{c}(t) = (\cos(t), \sin(t))$ for $t \in [0, 2\pi]$:
$$x(t) = \cos(t), \quad y(t) = \sin(t)$$
$$dx = -\sin(t) \, dt, \quad dy = \cos(t) \, dt$$

$$\int_{\partial M} \omega = \int_0^{2\pi} [x \, dy - y \, dx]$$
$$= \int_0^{2\pi} [\cos(t) \cdot \cos(t) \, dt - \sin(t) \cdot (-\sin(t) \, dt)]$$
$$= \int_0^{2\pi} [\cos^2(t) + \sin^2(t)] \, dt = \int_0^{2\pi} 1 \, dt = 2\pi$$

Stokes' theorem is verified: $\int_M d\omega = \int_{\partial M} \omega = 2\pi$.

### Problem 5
Let $\eta = z \, dx$ be a 1-form in $\mathbb{R}^3$. Let $S$ be the hemisphere $x^2 + y^2 + z^2 = 1$, $z \geq 0$. Verify Stokes' theorem for this case.

### Solution 5
First, compute the exterior derivative:
$$d\eta = d(z) \wedge dx = dz \wedge dx = -dx \wedge dz$$

The boundary $\partial S$ is the circle $x^2 + y^2 = 1$ in the $z = 0$ plane. On this boundary, $z = 0$, so:
$$\eta|_{\partial S} = 0 \cdot dx = 0$$

Therefore:
$$\int_{\partial S} \eta = 0$$

By Stokes' theorem, we must have:
$$\int_S d\eta = \int_S (-dx \wedge dz) = 0$$

This can be verified by noting that the integral of $dx \wedge dz$ over a surface where $z$ is a function of $x$ and $y$ (like our hemisphere) is indeed zero due to the geometry.

### Problem 6
Use Stokes' theorem to evaluate the line integral $\oint_C (x^2y \, dx + 2xy^2 \, dy)$ where $C$ is the boundary of the square $[0,1] \times [0,1]$ oriented counterclockwise.

### Solution 6
Let $\omega = x^2y \, dx + 2xy^2 \, dy$. 

Compute the exterior derivative:
$$d\omega = \left(\frac{\partial(2xy^2)}{\partial x} - \frac{\partial(x^2y)}{\partial y}\right) dx \wedge dy$$
$$= (2y^2 - x^2) dx \wedge dy$$

By Stokes' theorem:
$$\oint_C \omega = \iint_S d\omega = \int_0^1 \int_0^1 (2y^2 - x^2) \, dx \, dy$$

$$= \int_0^1 \left[2y^2x - \frac{x^3}{3}\right]_0^1 dy = \int_0^1 \left(2y^2 - \frac{1}{3}\right) dy$$

$$= \left[\frac{2y^3}{3} - \frac{y}{3}\right]_0^1 = \frac{2}{3} - \frac{1}{3} = \frac{1}{3}$$

## Applications

### Problem 7
Show how Maxwell's equations can be written in terms of differential forms.

### Solution 7
Maxwell's equations can be elegantly expressed using differential forms:

Let $F$ be the Faraday 2-form representing the electromagnetic field:
$$F = E \wedge dt + B$$

where $E$ is the electric field 1-form and $B$ is the magnetic field 2-form.

**Two of Maxwell's equations** are given by:
$$dF = 0$$

This single equation encapsulates:
- Faraday's law: $\nabla \times E + \frac{\partial B}{\partial t} = 0$
- Gauss's law for magnetism: $\nabla \cdot B = 0$

**The other two equations** involve the Hodge dual $*F$:
$$d(*F) = *J$$

where $J$ is the current 3-form. This gives:
- Ampère's law: $\nabla \times B - \frac{\partial E}{\partial t} = J$
- Gauss's law: $\nabla \cdot E = \rho$

### Problem 8
Explain how the concept of work in physics can be expressed as the integral of a 1-form.

### Solution 8
In physics, work is defined as $W = \int \mathbf{F} \cdot d\mathbf{r}$, where $\mathbf{F}$ is the force vector and $d\mathbf{r}$ is the displacement vector.

This can be naturally expressed using differential forms:

The force field $\mathbf{F} = (F_x, F_y, F_z)$ can be represented as a 1-form:
$$\omega_F = F_x \, dx + F_y \, dy + F_z \, dz$$

The work done by the force along a path $C$ is then:
$$W = \int_C \omega_F = \int_C (F_x \, dx + F_y \, dy + F_z \, dz)$$

This formulation has several advantages:
- It's coordinate-independent
- It naturally extends to higher dimensions
- It connects to conservation laws through exact differentials
- Conservative forces correspond to exact 1-forms ($\omega_F = df$ for some potential $f$)