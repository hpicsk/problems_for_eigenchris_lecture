# TensorCalc 02: Cartesian Polar Coordinates and Basis Vectors - Example Problems and Solutions

## Coordinate Transformations

### Problem 1
Convert the following points from Cartesian coordinates $(x, y)$ to polar coordinates $(r, \theta)$: 

a) $(1, 1)$

b) $(-3, 4)$

c) $(0, -2)$

### Solution 1

a) $(1, 1)$
$$r = \sqrt{1^2 + 1^2} = \sqrt{2}$$
$$\theta = \arctan\left(\frac{1}{1}\right) = \frac{\pi}{4}$$
$$\left(\sqrt{2}, \frac{\pi}{4}\right)$$

b) $(-3, 4)$
$$r = \sqrt{(-3)^2 + 4^2} = \sqrt{9 + 16} = 5$$
$$\theta = \arctan\left(\frac{4}{-3}\right) + \pi = \pi - \arctan\left(\frac{4}{3}\right)$$
$$\left(5, \pi - \arctan\left(\frac{4}{3}\right)\right)$$

c) $(0, -2)$
$$r = \sqrt{0^2 + (-2)^2} = 2$$
$$\theta = \frac{3\pi}{2}$$
$$\left(2, \frac{3\pi}{2}\right)$$

### Problem 2
Convert the following points from polar coordinates $(r, \theta)$ to Cartesian coordinates $(x, y)$: 

a) $(2, \pi/4)$

b) $(5, -\pi/6)$

c) $(1, 3\pi/2)$

### Solution 2

a) $(2, \pi/4)$
$$x = 2 \cos\left(\frac{\pi}{4}\right) = 2 \cdot \frac{\sqrt{2}}{2} = \sqrt{2}$$
$$y = 2 \sin\left(\frac{\pi}{4}\right) = 2 \cdot \frac{\sqrt{2}}{2} = \sqrt{2}$$
$$(\sqrt{2}, \sqrt{2})$$

b) $(5, -\pi/6)$
$$x = 5 \cos\left(-\frac{\pi}{6}\right) = 5 \cdot \frac{\sqrt{3}}{2} = \frac{5\sqrt{3}}{2}$$
$$y = 5 \sin\left(-\frac{\pi}{6}\right) = 5 \cdot \left(-\frac{1}{2}\right) = -\frac{5}{2}$$
$$\left(\frac{5\sqrt{3}}{2}, -\frac{5}{2}\right)$$

c) $(1, 3\pi/2)$
$$x = 1 \cos\left(\frac{3\pi}{2}\right) = 1 \cdot 0 = 0$$
$$y = 1 \sin\left(\frac{3\pi}{2}\right) = 1 \cdot (-1) = -1$$
$$(0, -1)$$

## Basis Vectors

### Problem 1
Express the Cartesian basis vectors $(\boldsymbol{e}_{x}, \boldsymbol{e}_{y})$ in terms of the polar basis vectors $(\boldsymbol{e}_{r}, \boldsymbol{e}_{\theta})$.

### Solution 1
$$\boldsymbol{e}_{x} = \cos(\theta) \boldsymbol{e}_{r} - \sin(\theta) \boldsymbol{e}_{\theta}$$
$$\boldsymbol{e}_{y} = \sin(\theta) \boldsymbol{e}_{r} + \cos(\theta) \boldsymbol{e}_{\theta}$$

### Problem 2
Express the polar basis vectors $(\boldsymbol{e}_{r}, \boldsymbol{e}_{\theta})$ in terms of the Cartesian basis vectors $(\boldsymbol{e}_{x}, \boldsymbol{e}_{y})$.

### Solution 2
$$\boldsymbol{e}_{r} = \cos(\theta) \boldsymbol{e}_{x} + \sin(\theta) \boldsymbol{e}_{y}$$
$$\boldsymbol{e}_{\theta} = -\sin(\theta) \boldsymbol{e}_{x} + \cos(\theta) \boldsymbol{e}_{y}$$

### Problem 3
Given a vector $\boldsymbol{v} = 3\boldsymbol{e}_{x} + 4\boldsymbol{e}_{y}$, express $\boldsymbol{v}$ in terms of the polar basis vectors $(\boldsymbol{e}_{r}, \boldsymbol{e}_{\theta})$ at the point $(1, 1)$.

### Solution 3
At the point $(1, 1)$, we have $r = \sqrt{2}$ and $\theta = \pi/4$.

The radial component is:
$$v_r = \boldsymbol{v} \cdot \boldsymbol{e}_{r} = (3\boldsymbol{e}_{x} + 4\boldsymbol{e}_{y}) \cdot (\cos(\theta)\boldsymbol{e}_{x} + \sin(\theta)\boldsymbol{e}_{y}) = 3\cos(\theta) + 4\sin(\theta)$$

At $\theta = \pi/4$:
$$v_r = 3 \cdot \frac{\sqrt{2}}{2} + 4 \cdot \frac{\sqrt{2}}{2} = \frac{7\sqrt{2}}{2}$$

The angular component is:
$$v_{\theta} = \boldsymbol{v} \cdot \boldsymbol{e}_{\theta} = (3\boldsymbol{e}_{x} + 4\boldsymbol{e}_{y}) \cdot (-\sin(\theta)\boldsymbol{e}_{x} + \cos(\theta)\boldsymbol{e}_{y}) = -3\sin(\theta) + 4\cos(\theta)$$

At $\theta = \pi/4$:
$$v_{\theta} = -3 \cdot \frac{\sqrt{2}}{2} + 4 \cdot \frac{\sqrt{2}}{2} = \frac{\sqrt{2}}{2}$$

Therefore:
$$\boldsymbol{v} = \frac{7\sqrt{2}}{2} \boldsymbol{e}_{r} + \frac{\sqrt{2}}{2} \boldsymbol{e}_{\theta}$$

## Vector Transformations

### Problem 1
A vector $\boldsymbol{v}$ has components $(2, 3)$ in the Cartesian basis. What are its components in the polar basis at the point $(1, \pi/4)$?

### Solution 1
The transformation from Cartesian to polar components is given by:
$$\begin{pmatrix} v_r \\ v_{\theta} \end{pmatrix} = \begin{pmatrix} \cos(\theta) & \sin(\theta) \\ -\sin(\theta) & \cos(\theta) \end{pmatrix} \begin{pmatrix} v_x \\ v_y \end{pmatrix}$$

At $\theta = \pi/4$:
$$v_r = 2\cos\left(\frac{\pi}{4}\right) + 3\sin\left(\frac{\pi}{4}\right) = 2 \cdot \frac{\sqrt{2}}{2} + 3 \cdot \frac{\sqrt{2}}{2} = \frac{5\sqrt{2}}{2}$$

$$v_{\theta} = -2\sin\left(\frac{\pi}{4}\right) + 3\cos\left(\frac{\pi}{4}\right) = -2 \cdot \frac{\sqrt{2}}{2} + 3 \cdot \frac{\sqrt{2}}{2} = \frac{\sqrt{2}}{2}$$

The components are $\left(\frac{5\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right)$.

### Problem 2
A vector field is given by $\boldsymbol{F} = r^2 \boldsymbol{e}_{r}$. Express this vector field in Cartesian coordinates.

### Solution 2
$$\boldsymbol{F} = r^2 (\cos(\theta) \boldsymbol{e}_{x} + \sin(\theta) \boldsymbol{e}_{y})$$

$$\boldsymbol{F} = (r^2 \cos(\theta)) \boldsymbol{e}_{x} + (r^2 \sin(\theta)) \boldsymbol{e}_{y}$$

Since $x = r\cos(\theta)$ and $y = r\sin(\theta)$, we have $r^2 = x^2 + y^2$ and $r = \sqrt{x^2 + y^2}$.

Therefore:
$$\boldsymbol{F} = (r \cdot x) \boldsymbol{e}_{x} + (r \cdot y) \boldsymbol{e}_{y} = \sqrt{x^2 + y^2} (x \boldsymbol{e}_{x} + y \boldsymbol{e}_{y})$$
