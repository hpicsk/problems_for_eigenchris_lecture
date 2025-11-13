# TensorCalc 01: Multi-Variable Calculus Review - Example Problems and Solutions

## Partial Derivatives

### Problem 1
Find all first and second partial derivatives of the following functions:

a) $f(x, y) = x^3 y^2 + 2y^3$

b) $g(x, y, z) = \sin(xy) + \cos(yz)$

c) $h(x, y) = e^{x^2 y}$

### Solution 1

a) $f(x, y) = x^3 y^2 + 2y^3$

- $\frac{\partial f}{\partial x} = 3x^2 y^2$
- $\frac{\partial f}{\partial y} = 2x^3 y + 6y^2$
- $\frac{\partial^2 f}{\partial x^2} = 6x y^2$
- $\frac{\partial^2 f}{\partial y^2} = 2x^3 + 12y$
- $\frac{\partial^2 f}{\partial x \partial y} = 6x^2 y$

b) $g(x, y, z) = \sin(xy) + \cos(yz)$

- $\frac{\partial g}{\partial x} = y \cos(xy)$
- $\frac{\partial g}{\partial y} = x \cos(xy) - z \sin(yz)$
- $\frac{\partial g}{\partial z} = -y \sin(yz)$
- $\frac{\partial^2 g}{\partial x^2} = -y^2 \sin(xy)$
- $\frac{\partial^2 g}{\partial y^2} = -x^2 \sin(xy) - z^2 \cos(yz)$
- $\frac{\partial^2 g}{\partial z^2} = -y^2 \cos(yz)$
- $\frac{\partial^2 g}{\partial x \partial y} = \cos(xy) - xy \sin(xy)$
- $\frac{\partial^2 g}{\partial x \partial z} = 0$
- $\frac{\partial^2 g}{\partial y \partial z} = -\sin(yz) - yz \cos(yz)$

c) $h(x, y) = e^{x^2 y}$

- $\frac{\partial h}{\partial x} = 2xy e^{x^2 y}$
- $\frac{\partial h}{\partial y} = x^2 e^{x^2 y}$
- $\frac{\partial^2 h}{\partial x^2} = 2y e^{x^2 y} + 4x^2y^2 e^{x^2 y}$
- $\frac{\partial^2 h}{\partial y^2} = x^4 e^{x^2 y}$
- $\frac{\partial^2 h}{\partial x \partial y} = 2x e^{x^2 y} + 2x^3y e^{x^2 y}$

## Gradient, Divergence, and Curl

### Problem 1
Find the gradient of the following functions:

a) $f(x, y) = x^2 + y^2$ at the point (1, 2)

b) $g(x, y, z) = xyz$ at the point (1, 2, 3)

### Solution 1

a) $f(x, y) = x^2 + y^2$ at the point (1, 2)

$$\nabla f = \left(\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}\right) = (2x, 2y)$$

$$\nabla f(1, 2) = (2 \cdot 1, 2 \cdot 2) = (2, 4)$$

b) $g(x, y, z) = xyz$ at the point (1, 2, 3)

$$\nabla g = \left(\frac{\partial g}{\partial x}, \frac{\partial g}{\partial y}, \frac{\partial g}{\partial z}\right) = (yz, xz, xy)$$

$$\nabla g(1, 2, 3) = (2 \cdot 3, 1 \cdot 3, 1 \cdot 2) = (6, 3, 2)$$

### Problem 2
Find the divergence and curl of the following vector fields:

a) $\mathbf{F}(x, y, z) = (x^2, y^2, z^2)$

b) $\mathbf{G}(x, y, z) = (y, -x, 0)$

### Solution 2

a) $\mathbf{F}(x, y, z) = (x^2, y^2, z^2)$

$$\nabla \cdot \mathbf{F} = \frac{\partial(x^2)}{\partial x} + \frac{\partial(y^2)}{\partial y} + \frac{\partial(z^2)}{\partial z} = 2x + 2y + 2z$$

$$\nabla \times \mathbf{F} = \left(\frac{\partial(z^2)}{\partial y} - \frac{\partial(y^2)}{\partial z}, \frac{\partial(x^2)}{\partial z} - \frac{\partial(z^2)}{\partial x}, \frac{\partial(y^2)}{\partial x} - \frac{\partial(x^2)}{\partial y}\right) = (0, 0, 0)$$

b) $\mathbf{G}(x, y, z) = (y, -x, 0)$

$$\nabla \cdot \mathbf{G} = \frac{\partial(y)}{\partial x} + \frac{\partial(-x)}{\partial y} + \frac{\partial(0)}{\partial z} = 0 + 0 + 0 = 0$$

$$\nabla \times \mathbf{G} = \left(\frac{\partial(0)}{\partial y} - \frac{\partial(-x)}{\partial z}, \frac{\partial(y)}{\partial z} - \frac{\partial(0)}{\partial x}, \frac{\partial(-x)}{\partial x} - \frac{\partial(y)}{\partial y}\right) = (0, 0, -1 - 1) = (0, 0, -2)$$

## Integrals

### Problem 1
Evaluate the line integral of the vector field $\mathbf{F}(x, y) = (-y, x)$ along the path $\mathbf{r}(t) = (\cos(t), \sin(t))$ from $t = 0$ to $t = 2\pi$.

### Solution 1
$$\mathbf{F}(\mathbf{r}(t)) = (-\sin(t), \cos(t))$$
$$\mathbf{r}'(t) = (-\sin(t), \cos(t))$$
$$\int_C \mathbf{F} \cdot d\mathbf{r} = \int_0^{2\pi} \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}'(t) dt = \int_0^{2\pi} (\sin^2(t) + \cos^2(t)) dt = \int_0^{2\pi} 1 dt = 2\pi$$

### Problem 2
Evaluate the surface integral of the vector field $\mathbf{F}(x, y, z) = (x, y, z)$ over the surface of a unit sphere centered at the origin.

### Solution 2
Using the divergence theorem: $\iint_S \mathbf{F} \cdot d\mathbf{S} = \iiint_V \nabla \cdot \mathbf{F} dV$

$$\nabla \cdot \mathbf{F} = 1 + 1 + 1 = 3$$

$$\iiint_V 3 dV = 3 \cdot (\text{Volume of unit sphere}) = 3 \cdot \left(\frac{4}{3} \pi \cdot 1^3\right) = 4\pi$$

### Problem 3
Use the divergence theorem to evaluate the flux of the vector field $\mathbf{F}(x, y, z) = (x^3, y^3, z^3)$ through the surface of a cube with side length 2 centered at the origin.

### Solution 3
$$\nabla \cdot \mathbf{F} = 3x^2 + 3y^2 + 3z^2$$

$$\text{Flux} = \iiint_V (3x^2 + 3y^2 + 3z^2) dV$$

where $V$ is the cube $[-1, 1] \times [-1, 1] \times [-1, 1]$

$$= \int_{-1}^1 \int_{-1}^1 \int_{-1}^1 (3x^2 + 3y^2 + 3z^2) dx dy dz$$

$$= 3 \cdot \left[\frac{x^3}{3}\right]_{-1}^1 \cdot 2 \cdot 2 + 3 \cdot 2 \cdot \left[\frac{y^3}{3}\right]_{-1}^1 \cdot 2 + 3 \cdot 2 \cdot 2 \cdot \left[\frac{z^3}{3}\right]_{-1}^1$$

$$= 3 \cdot \frac{2}{3} \cdot 4 + 3 \cdot 4 \cdot \frac{2}{3} + 3 \cdot 4 \cdot \frac{2}{3} = 8 + 8 + 8 = 24$$

### Problem 4
Use Stokes' theorem to evaluate the line integral of the vector field $\mathbf{F}(x, y, z) = (y^2, z^2, x^2)$ around the triangle with vertices (1, 0, 0), (0, 1, 0), and (0, 0, 1).

### Solution 4
$$\nabla \times \mathbf{F} = \left(\frac{\partial(x^2)}{\partial y} - \frac{\partial(z^2)}{\partial z}, \frac{\partial(y^2)}{\partial z} - \frac{\partial(x^2)}{\partial x}, \frac{\partial(z^2)}{\partial x} - \frac{\partial(y^2)}{\partial y}\right) = (-2z, -2x, -2y)$$

The triangle lies on the plane $x + y + z = 1$. The normal to this plane is $\mathbf{n} = \frac{(1, 1, 1)}{\sqrt{3}}$.

$$\int_C \mathbf{F} \cdot d\mathbf{r} = \iint_S (\nabla \times \mathbf{F}) \cdot d\mathbf{S} = \iint_S (-2z, -2x, -2y) \cdot \mathbf{n} dS$$

$$= \iint_S \frac{(-2z - 2x - 2y)}{\sqrt{3}} dS = \iint_S \frac{-2(x+y+z)}{\sqrt{3}} dS$$

Since $x+y+z=1$ on the surface, this is $\iint_S \frac{-2}{\sqrt{3}} dS = \frac{-2}{\sqrt{3}} \cdot \text{Area}(\text{Triangle})$

The area of the triangle is $\frac{\sqrt{3}}{2}$. So the integral is $\frac{-2}{\sqrt{3}} \cdot \frac{\sqrt{3}}{2} = -1$.