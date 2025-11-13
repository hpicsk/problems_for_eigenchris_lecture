## Problem 1: The Gradient $\nabla f$

1. In Cartesian coordinates, the gradient of a scalar function $f$ is given by $\nabla f = (\partial f/\partial x, \partial f/\partial y, \partial f/\partial z)$. What kind of object is this? (Vector, covector, etc.)
2. How do the components of the gradient transform under a change of coordinates? Are they covariant or contravariant?
3. Given $f(x, y) = x^2 + y^2$, calculate $\nabla f$ in both Cartesian and polar coordinates.

### Solution 1

1. **In Cartesian coordinates, the gradient of a scalar function $f$ is given by $\nabla f = (\partial f/\partial x, \partial f/\partial y, \partial f/\partial z)$. What kind of object is this? (Vector, covector, etc.)**

The gradient $\nabla f$ is a vector (a contravariant tensor of rank 1).

2. **How do the components of the gradient transform under a change of coordinates? Are they covariant or contravariant?**

The components of the gradient vector $\nabla f$ transform contravariantly. However, the components of the exterior derivative $df$ transform covariantly. The two are related by the metric tensor.

3. **Given $f(x, y) = x^2 + y^2$, calculate $\nabla f$ in both Cartesian and polar coordinates.**

- **Cartesian:** $\nabla f = (2x, 2y)$
- **Polar:** $f(r, \theta) = r^2$. $\nabla f = \frac{\partial f}{\partial r}\mathbf{e}_r + \frac{1}{r}\frac{\partial f}{\partial \theta}\mathbf{e}_\theta = 2r \mathbf{e}_r$.

## Problem 2: The Exterior Derivative $df$

1. The exterior derivative of a scalar function $f$ (a 0-form) is a 1-form $df = (\partial f/\partial x) dx + (\partial f/\partial y) dy + (\partial f/\partial z) dz$. What kind of object is this?
2. How do the components of $df$ transform under a change of coordinates? Are they covariant or contravariant?
3. Given $f(x, y) = x^2 + y^2$, calculate $df$ in both Cartesian and polar coordinates.

### Solution 2

1. **The exterior derivative of a scalar function $f$ (a 0-form) is a 1-form $df = (\partial f/\partial x) dx + (\partial f/\partial y) dy + (\partial f/\partial z) dz$. What kind of object is this?**

$df$ is a covector (a covariant tensor of rank 1), also known as a 1-form.

2. **How do the components of $df$ transform under a change of coordinates? Are they covariant or contravariant?**

The components of $df$ transform covariantly.

3. **Given $f(x, y) = x^2 + y^2$, calculate $df$ in both Cartesian and polar coordinates.**

- **Cartesian:** $df = 2x \, dx + 2y \, dy$
- **Polar:** $f(r, \theta) = r^2$. $df = \frac{\partial f}{\partial r}dr + \frac{\partial f}{\partial \theta}d\theta = 2r \, dr$.

## Problem 3: Relationship between $\nabla f$ and $df$

1. What is the relationship between the gradient $\nabla f$ and the exterior derivative $df$?
2. How can you use the metric tensor to convert $df$ into $\nabla f$?
3. For a Euclidean space with the standard metric $g_{ij} = \delta_{ij}$, show that the components of $\nabla f$ are the same as the components of $df$.
4. For the polar coordinate system, the metric is given by $ds^2 = dr^2 + r^2 d\theta^2$. If $df = (\partial f/\partial r) dr + (\partial f/\partial \theta) d\theta$, what are the components of the vector $\nabla f$?

### Solution 3

1. **What is the relationship between the gradient $\nabla f$ and the exterior derivative $df$?**

They are related by the metric tensor. The gradient $\nabla f$ is the vector representation of the covector $df$. In index notation, $(\nabla f)^i = g^{ij} (df)_j$.

2. **How can you use the metric tensor to convert $df$ into $\nabla f$?**

You can raise the index of the covector $df$ using the inverse metric tensor $g^{ij}$.

3. **For a Euclidean space with the standard metric $g_{ij} = \delta_{ij}$, show that the components of $\nabla f$ are the same as the components of $df$.**

In this case, $g^{ij} = \delta^{ij}$. So $(\nabla f)^i = \delta^{ij} (df)_j = (df)_i$. The components are the same.

4. **For the polar coordinate system, the metric is given by $ds^2 = dr^2 + r^2 d\theta^2$. If $df = (\partial f/\partial r) dr + (\partial f/\partial \theta) d\theta$, what are the components of the vector $\nabla f$?**

The metric is $g = \begin{bmatrix} 1 & 0 \\ 0 & r^2 \end{bmatrix}$, so the inverse metric is $g^{-1} = \begin{bmatrix} 1 & 0 \\ 0 & 1/r^2 \end{bmatrix}$.

$$(\nabla f)^r = g^{rr}(df)_r + g^{r\theta}(df)_\theta = 1 \cdot \frac{\partial f}{\partial r} + 0 = \frac{\partial f}{\partial r}$$

$$(\nabla f)^\theta = g^{\theta r}(df)_r + g^{\theta\theta}(df)_\theta = 0 + \frac{1}{r^2} \cdot \frac{\partial f}{\partial \theta} = \frac{1}{r^2}\frac{\partial f}{\partial \theta}$$

So $\nabla f = \frac{\partial f}{\partial r} \mathbf{e}_r + \frac{1}{r^2}\frac{\partial f}{\partial \theta} \mathbf{e}_\theta$. Note that the standard definition of gradient in polar coordinates uses normalized basis vectors, which gives $\nabla f = \frac{\partial f}{\partial r} \mathbf{e}_r + \frac{1}{r}\frac{\partial f}{\partial \theta} \mathbf{e}_\theta$.