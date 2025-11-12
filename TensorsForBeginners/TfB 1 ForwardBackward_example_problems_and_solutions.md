## Problem 1
Consider a 2D Cartesian coordinate system $(x, y)$. A second coordinate system $(x', y')$ is obtained by rotating the first system by an angle of 30 degrees counterclockwise. A vector $\mathbf{v}$ has components $(2, 3)$ in the $(x, y)$ system. What are the components of $\mathbf{v}$ in the $(x', y')$ system? (Forward transformation)

## Solution 1
The transformation of components for a counter-clockwise rotation of the coordinate system by an angle $\theta$ is:
$$v'_x = v_x \cos(\theta) + v_y \sin(\theta)$$
$$v'_y = -v_x \sin(\theta) + v_y \cos(\theta)$$

For $\theta = 30°$, $\cos(30°) = \frac{\sqrt{3}}{2}$ and $\sin(30°) = \frac{1}{2}$.

$$v'_x = 2 \cdot \frac{\sqrt{3}}{2} + 3 \cdot \frac{1}{2} = \sqrt{3} + \frac{3}{2}$$
$$v'_y = -2 \cdot \frac{1}{2} + 3 \cdot \frac{\sqrt{3}}{2} = -1 + \frac{3\sqrt{3}}{2}$$

So, $\mathbf{v}' = \left(\sqrt{3} + \frac{3}{2}, -1 + \frac{3\sqrt{3}}{2}\right)$.

## Problem 2
Using the same coordinate systems as in problem 1, a vector $\mathbf{u}$ has components $(1, -1)$ in the $(x', y')$ system. What are its components in the $(x, y)$ system? (Backward transformation)

## Solution 2
The backward transformation is a rotation of the components by $30°$.
$$v_x = u_x \cos(\theta) - u_y \sin(\theta)$$
$$v_y = u_x \sin(\theta) + u_y \cos(\theta)$$

For $\theta = 30°$, $\cos(30°) = \frac{\sqrt{3}}{2}$ and $\sin(30°) = \frac{1}{2}$.

$$v_x = 1 \cdot \frac{\sqrt{3}}{2} - (-1) \cdot \frac{1}{2} = \frac{\sqrt{3} + 1}{2}$$
$$v_y = 1 \cdot \frac{1}{2} + (-1) \cdot \frac{\sqrt{3}}{2} = \frac{1 - \sqrt{3}}{2}$$

So, $\mathbf{v} = \left(\frac{\sqrt{3} + 1}{2}, \frac{1 - \sqrt{3}}{2}\right)$.

## Problem 3
What is the difference between a covariant and a contravariant transformation? Give an example of a quantity that transforms covariantly and one that transforms contravariantly.

## Solution 3
- **Contravariant** components transform against the change of basis. For example, the components of a vector are contravariant.
- **Covariant** components transform with the change of basis. For example, the components of the gradient of a function are covariant.