# TensorCalc 04: Derivatives are Vectors - Example Problems and Solutions

## Directional Derivatives

### Problem 1
Find the directional derivative of the function $f(x, y) = x^2 y$ at the point $(1, 2)$ in the direction of the vector $\mathbf{v} = (3, 4)$.

### Solution 1
First, find the unit vector in the direction of $\mathbf{v}$: 
$$\mathbf{u} = \frac{\mathbf{v}}{|\mathbf{v}|} = \frac{(3, 4)}{\sqrt{3^2 + 4^2}} = \frac{(3, 4)}{5} = \left(\frac{3}{5}, \frac{4}{5}\right)$$

The gradient of $f$ is:
$$\nabla f = \left(\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}\right) = (2xy, x^2)$$

At the point $(1, 2)$:
$$\nabla f(1, 2) = (2 \cdot 1 \cdot 2, 1^2) = (4, 1)$$

The directional derivative is:
$$D_{\mathbf{u}} f = \nabla f \cdot \mathbf{u} = (4, 1) \cdot \left(\frac{3}{5}, \frac{4}{5}\right) = \frac{12}{5} + \frac{4}{5} = \frac{16}{5}$$

### Problem 2
For the function $g(x, y, z) = e^{xyz}$, find the directional derivative at the point $(1, 1, 1)$ in the direction of the vector $\mathbf{u} = \left(\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}\right)$.

### Solution 2
The gradient of $g$ is:
$$\nabla g = \left(\frac{\partial g}{\partial x}, \frac{\partial g}{\partial y}, \frac{\partial g}{\partial z}\right) = (yz \cdot e^{xyz}, xz \cdot e^{xyz}, xy \cdot e^{xyz})$$

At the point $(1, 1, 1)$:
$$\nabla g(1, 1, 1) = (1 \cdot 1 \cdot e^{1 \cdot 1 \cdot 1}, 1 \cdot 1 \cdot e^{1 \cdot 1 \cdot 1}, 1 \cdot 1 \cdot e^{1 \cdot 1 \cdot 1}) = (e, e, e)$$

The directional derivative is:
$$D_{\mathbf{u}} g = \nabla g \cdot \mathbf{u} = (e, e, e) \cdot \left(\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}}\right) = \frac{3e}{\sqrt{3}} = e\sqrt{3}$$

### Problem 3
What is the direction of the maximum rate of increase of the function $h(x, y) = \sin(x) \cos(y)$ at the point $(\pi/4, \pi/4)$? What is the magnitude of this maximum rate of increase?

### Solution 3
The direction of maximum increase is the direction of the gradient $\nabla h$.

$$\nabla h = \left(\frac{\partial h}{\partial x}, \frac{\partial h}{\partial y}\right) = (\cos(x)\cos(y), -\sin(x)\sin(y))$$

At the point $(\pi/4, \pi/4)$:
$$\nabla h\left(\frac{\pi}{4}, \frac{\pi}{4}\right) = \left(\cos\left(\frac{\pi}{4}\right)\cos\left(\frac{\pi}{4}\right), -\sin\left(\frac{\pi}{4}\right)\sin\left(\frac{\pi}{4}\right)\right)$$

$$= \left(\frac{\sqrt{2}}{2} \cdot \frac{\sqrt{2}}{2}, -\frac{\sqrt{2}}{2} \cdot \frac{\sqrt{2}}{2}\right) = \left(\frac{1}{2}, -\frac{1}{2}\right)$$

The direction is $\left(\frac{1}{2}, -\frac{1}{2}\right)$ (or the unit vector $\left(\frac{1}{\sqrt{2}}, -\frac{1}{\sqrt{2}}\right)$).

The magnitude of this maximum rate of increase is:
$$|\nabla h| = \sqrt{\left(\frac{1}{2}\right)^2 + \left(-\frac{1}{2}\right)^2} = \sqrt{\frac{1}{4} + \frac{1}{4}} = \sqrt{\frac{1}{2}} = \frac{1}{\sqrt{2}}$$

## Gradient as a Vector

### Problem 4
Explain why the gradient of a scalar function is a vector.

### Solution 4
The gradient of a scalar function represents the direction and magnitude of the steepest ascent of the function. Since it has both magnitude and direction, it is a vector. More formally, the components of the gradient transform as a vector under coordinate transformations, specifically as a covector (covariant vector).

### Problem 5
Show that the gradient of a function $f$ is always perpendicular to the level surfaces of $f$.

### Solution 5
Let $\mathbf{r}(t)$ be a curve on a level surface $f = c$. Then $f(\mathbf{r}(t)) = c$ (a constant). 

Differentiating with respect to $t$ using the chain rule gives:
$$\frac{d}{dt}[f(\mathbf{r}(t))] = \nabla f(\mathbf{r}(t)) \cdot \mathbf{r}'(t) = 0$$

Since $\mathbf{r}'(t)$ is a tangent vector to the level surface, this shows that the gradient $\nabla f$ is orthogonal to any tangent vector on the level surface, and thus is perpendicular to the surface itself.

### Problem 6
Given the function $f(x, y) = x^2 - y^2$, sketch the level curves and the gradient vector at several points.

### Solution 6
The level curves are hyperbolas $x^2 - y^2 = c$. 

The gradient is:
$$\nabla f = (2x, -2y)$$

At a point $(a, b)$, the gradient vector is $(2a, -2b)$, which is perpendicular to the hyperbola at that point.

For example:
- At $(1, 0)$: $\nabla f = (2, 0)$ (pointing in positive $x$ direction)
- At $(0, 1)$: $\nabla f = (0, -2)$ (pointing in negative $y$ direction)
- At $(1, 1)$: $\nabla f = (2, -2)$ (pointing southeast)

## Tangent Vectors to Curves

### Problem 7
Consider the parametric curve $\mathbf{r}(t) = (\cos(t), \sin(t), t)$.

a) Find the tangent vector to the curve at $t = \pi/2$.

b) Find the derivative of the function $f(x, y, z) = x^2 + y^2 + z^2$ along this curve.

### Solution 7
a) The tangent vector is:
$$\mathbf{r}'(t) = (-\sin(t), \cos(t), 1)$$

At $t = \pi/2$:
$$\mathbf{r}'\left(\frac{\pi}{2}\right) = \left(-\sin\left(\frac{\pi}{2}\right), \cos\left(\frac{\pi}{2}\right), 1\right) = (-1, 0, 1)$$

b) The derivative of $f$ along the curve is:
$$\frac{df}{dt} = \nabla f \cdot \mathbf{r}'(t)$$

where $\nabla f = (2x, 2y, 2z)$.

Along the curve, $\nabla f = (2\cos(t), 2\sin(t), 2t)$.

$$\frac{df}{dt} = (2\cos(t), 2\sin(t), 2t) \cdot (-\sin(t), \cos(t), 1)$$
$$= -2\sin(t)\cos(t) + 2\sin(t)\cos(t) + 2t = 2t$$

### Problem 8
The trajectory of a particle is given by $\mathbf{r}(t) = (t, t^2, t^3)$. The temperature in space is given by $T(x, y, z) = xyz$. What is the rate of change of temperature that the particle experiences at $t = 1$?

### Solution 8
The rate of change of temperature along the trajectory is:
$$\frac{dT}{dt} = \nabla T \cdot \mathbf{r}'(t)$$

where:
$$\nabla T = (yz, xz, xy)$$
$$\mathbf{r}'(t) = (1, 2t, 3t^2)$$

At $t = 1$, the particle is at $\mathbf{r}(1) = (1, 1, 1)$.

$$\nabla T(1,1,1) = (1 \cdot 1, 1 \cdot 1, 1 \cdot 1) = (1, 1, 1)$$
$$\mathbf{r}'(1) = (1, 2 \cdot 1, 3 \cdot 1^2) = (1, 2, 3)$$

Therefore:
$$\frac{dT}{dt}\bigg|_{t=1} = (1, 1, 1) \cdot (1, 2, 3) = 1 + 2 + 3 = 6$$