# TensorCalc 08: Covector Field Transformation Rules (Covariance) - Example Problems and Solutions

## Covariant Vectors (Covectors)

### Problem 1
Show that the components of the gradient of a scalar function transform covariantly.

### Solution 1
Let $f$ be a scalar function. The components of its gradient in the $x^i$ coordinate system are:
$$g_i = \frac{\partial f}{\partial x^i}$$

In a new coordinate system $x'^j$, the components are:
$$g'_j = \frac{\partial f}{\partial x'^j}$$

Using the chain rule:
$$g'_j = \frac{\partial f}{\partial x'^j} = \frac{\partial x^i}{\partial x'^j} \frac{\partial f}{\partial x^i} = \frac{\partial x^i}{\partial x'^j} g_i$$

This is exactly the transformation law for a covariant vector:
$$g'_j = \frac{\partial x^i}{\partial x'^j} g_i$$

### Problem 2
The components of a covector $\boldsymbol{\alpha}$ in the Cartesian $(x, y)$ basis are $(\alpha_x, \alpha_y) = (x, y)$. Find the components of $\boldsymbol{\alpha}$ in the polar $(r, \theta)$ basis.

### Solution 2
Using the covariant transformation rule:
$$\alpha'_j = \frac{\partial x^i}{\partial x'^j} \alpha_i$$

For the $r$-component:
$$\alpha_r = \frac{\partial x}{\partial r}\alpha_x + \frac{\partial y}{\partial r}\alpha_y$$

Since $x = r\cos(\theta)$ and $y = r\sin(\theta)$:
$$\frac{\partial x}{\partial r} = \cos(\theta), \quad \frac{\partial y}{\partial r} = \sin(\theta)$$

Therefore:
$$\alpha_r = \cos(\theta) \cdot x + \sin(\theta) \cdot y$$
$$= \cos(\theta) \cdot (r\cos(\theta)) + \sin(\theta) \cdot (r\sin(\theta))$$
$$= r\cos^2(\theta) + r\sin^2(\theta) = r$$

For the $\theta$-component:
$$\alpha_\theta = \frac{\partial x}{\partial \theta}\alpha_x + \frac{\partial y}{\partial \theta}\alpha_y$$

Since:
$$\frac{\partial x}{\partial \theta} = -r\sin(\theta), \quad \frac{\partial y}{\partial \theta} = r\cos(\theta)$$

Therefore:
$$\alpha_\theta = (-r\sin(\theta)) \cdot x + (r\cos(\theta)) \cdot y$$
$$= -r\sin(\theta) \cdot (r\cos(\theta)) + r\cos(\theta) \cdot (r\sin(\theta))$$
$$= -r^2\sin(\theta)\cos(\theta) + r^2\cos(\theta)\sin(\theta) = 0$$

The components are $(r, 0)$.

### Problem 3
A covector has components $(1, 1)$ in the polar basis at the point $(r, \theta) = (\sqrt{2}, \pi/4)$. What are its components in the Cartesian basis?

### Solution 3
Using the inverse covariant transformation:
$$\alpha_x = \frac{\partial r}{\partial x}\alpha_r + \frac{\partial \theta}{\partial x}\alpha_\theta$$
$$\alpha_y = \frac{\partial r}{\partial y}\alpha_r + \frac{\partial \theta}{\partial y}\alpha_\theta$$

At the point $(\sqrt{2}, \pi/4)$, we have $x = \sqrt{2}\cos(\pi/4) = 1$ and $y = \sqrt{2}\sin(\pi/4) = 1$.

The partial derivatives are:
$$\frac{\partial r}{\partial x} = \frac{x}{r} = \frac{1}{\sqrt{2}}, \quad \frac{\partial r}{\partial y} = \frac{y}{r} = \frac{1}{\sqrt{2}}$$
$$\frac{\partial \theta}{\partial x} = -\frac{y}{r^2} = -\frac{1}{2}, \quad \frac{\partial \theta}{\partial y} = \frac{x}{r^2} = \frac{1}{2}$$

Therefore:
$$\alpha_x = \frac{1}{\sqrt{2}} \cdot 1 + \left(-\frac{1}{2}\right) \cdot 1 = \frac{1}{\sqrt{2}} - \frac{1}{2} = \frac{\sqrt{2} - 1}{\sqrt{2}} \cdot \frac{\sqrt{2}}{\sqrt{2}} = \frac{2 - \sqrt{2}}{2}$$

Wait, let me recalculate this more carefully:
$$\alpha_x = \frac{x/r} \cdot 1 + \frac{(-y/r^2)} \cdot 1 = \frac{1/\sqrt{2}}{\sqrt{2}} - \frac{1/\sqrt{2}}{(\sqrt{2})^2} = \frac{1}{2} - \frac{1}{2} = 0$$

$$\alpha_y = \frac{y/r} \cdot 1 + \frac{x/r^2} \cdot 1 = \frac{1/\sqrt{2}}{\sqrt{2}} + \frac{1/\sqrt{2}}{(\sqrt{2})^2} = \frac{1}{2} + \frac{1}{2} = 1$$

The components are $(0, 1)$.

## Covariant Tensors

### Problem 4
A second-rank tensor $T$ has components $T_{ij}$ in the $x_i$ coordinate system. How do the components of $T$ transform under a change of coordinates?

### Solution 4
For a second-rank covariant tensor, each index transforms according to the covariant rule:
$$T'_{kl} = \frac{\partial x^i}{\partial x'^k} \frac{\partial x^j}{\partial x'^l} T_{ij}$$

This extends naturally from the covariant vector transformation rule, with one transformation factor for each covariant index.

### Problem 5
Let $\alpha_i$ and $\beta_j$ be the components of two covectors. Show that the outer product $T_{ij} = \alpha_i \beta_j$ transforms as a second-rank covariant tensor.

### Solution 5
Under a coordinate transformation:
$$T'_{kl} = \alpha'_k \beta'_l$$

Using the covariant transformation rules for covectors:
$$\alpha'_k = \frac{\partial x^i}{\partial x'^k} \alpha_i, \quad \beta'_l = \frac{\partial x^j}{\partial x'^l} \beta_j$$

Therefore:
$$T'_{kl} = \left(\frac{\partial x^i}{\partial x'^k} \alpha_i\right) \left(\frac{\partial x^j}{\partial x'^l} \beta_j\right)$$
$$= \frac{\partial x^i}{\partial x'^k} \frac{\partial x^j}{\partial x'^l} \alpha_i \beta_j$$
$$= \frac{\partial x^i}{\partial x'^k} \frac{\partial x^j}{\partial x'^l} T_{ij}$$

This is exactly the transformation rule for a rank-2 covariant tensor.

### Problem 6
The metric tensor $g_{ij}$ is a second-rank covariant tensor. If the metric tensor in Cartesian coordinates is given by the identity matrix, what are the components of the metric tensor in polar coordinates?

### Solution 6
Using the covariant tensor transformation rule:
$$g'_{kl} = \frac{\partial x^i}{\partial x'^k} \frac{\partial x^j}{\partial x'^l} g_{ij}$$

Since $g_{ij} = \delta_{ij}$ in Cartesian coordinates, we have:
$$g'_{kl} = \frac{\partial x^i}{\partial x'^k} \frac{\partial x^i}{\partial x'^l}$$

For polar coordinates:
$$g'_{rr} = \left(\frac{\partial x}{\partial r}\right)^2 + \left(\frac{\partial y}{\partial r}\right)^2 = \cos^2(\theta) + \sin^2(\theta) = 1$$

$$g'_{\theta\theta} = \left(\frac{\partial x}{\partial \theta}\right)^2 + \left(\frac{\partial y}{\partial \theta}\right)^2 = (-r\sin(\theta))^2 + (r\cos(\theta))^2 = r^2$$

$$g'_{r\theta} = \frac{\partial x}{\partial r}\frac{\partial x}{\partial \theta} + \frac{\partial y}{\partial r}\frac{\partial y}{\partial \theta}$$
$$= \cos(\theta)(-r\sin(\theta)) + \sin(\theta)(r\cos(\theta)) = -r\cos(\theta)\sin(\theta) + r\sin(\theta)\cos(\theta) = 0$$

The metric tensor in polar coordinates is:
$$g'_{ij} = \begin{pmatrix} 1 & 0 \\ 0 & r^2 \end{pmatrix}$$

## Mixed Tensors

### Problem 7
How does a mixed tensor with components $T^i_j$ transform?

### Solution 7
A mixed tensor has both contravariant and covariant indices. The transformation rule combines both types:
$$T'^k_l = \frac{\partial x'^k}{\partial x^i} \frac{\partial x^j}{\partial x'^l} T^i_j$$

The contravariant index (upper) transforms with $\frac{\partial x'^k}{\partial x^i}$, while the covariant index (lower) transforms with $\frac{\partial x^j}{\partial x'^l}$.

### Problem 8
If $A^i$ is a contravariant vector and $B_j$ is a covariant vector, show that $T^i_j = A^i B_j$ is a mixed tensor of rank $(1, 1)$.

### Solution 8
Under a coordinate transformation:
$$T'^k_l = A'^k B'_l$$

Using the transformation rules for vectors:
$$A'^k = \frac{\partial x'^k}{\partial x^i} A^i, \quad B'_l = \frac{\partial x^j}{\partial x'^l} B_j$$

Therefore:
$$T'^k_l = \left(\frac{\partial x'^k}{\partial x^i} A^i\right) \left(\frac{\partial x^j}{\partial x'^l} B_j\right)$$
$$= \frac{\partial x'^k}{\partial x^i} \frac{\partial x^j}{\partial x'^l} A^i B_j$$
$$= \frac{\partial x'^k}{\partial x^i} \frac{\partial x^j}{\partial x'^l} T^i_j$$

This is exactly the transformation rule for a mixed tensor of rank $(1, 1)$.