## Problem 1

Given a contravariant vector $A^{\mu} = (A^0, A^1, A^2, A^3)$, find the corresponding covariant vector $A_{\mu}$.

### Solution 1

The covariant vector $A_{\mu}$ is obtained by lowering the index of the contravariant vector $A^{\mu}$ using the metric tensor $g_{\mu\nu}$:

$$A_{\mu} = g_{\mu\nu} A^{\nu}$$

In special relativity, the metric tensor is the Minkowski metric $\eta_{\mu\nu} = \text{diag}(-1, 1, 1, 1)$.

Computing each component:
- $A_0 = \eta_{0\nu} A^{\nu} = \eta_{00} A^0 = -A^0$
- $A_1 = \eta_{1\nu} A^{\nu} = \eta_{11} A^1 = A^1$
- $A_2 = \eta_{2\nu} A^{\nu} = \eta_{22} A^2 = A^2$
- $A_3 = \eta_{3\nu} A^{\nu} = \eta_{33} A^3 = A^3$

Therefore, $A_{\mu} = (-A^0, A^1, A^2, A^3)$.

---

## Problem 2

The metric tensor in 3D Euclidean coordinates is given by $g_{\mu\nu} = \text{diag}(1, 1, 1)$. Find the corresponding contravariant metric tensor $g^{\mu\nu}$.

### Solution 2

The contravariant metric tensor $g^{\mu\nu}$ is the inverse of the covariant metric tensor $g_{\mu\nu}$:

$$g^{\mu\nu} g_{\nu\alpha} = \delta^{\mu}_{\alpha}$$

Since $g_{\mu\nu}$ is the 3D identity matrix, its inverse is also the identity matrix:

$$g^{\mu\nu} = \text{diag}(1, 1, 1)$$

This means that for Euclidean space, raising and lowering indices doesn't change the components of vectors.

---

## Problem 3

The gradient of a scalar field $\phi$ is given by $\partial_{\mu} \phi$. Is the gradient a covariant or a contravariant vector? Explain why.

### Solution 3

The gradient of a scalar field $\phi$ is:

$$\partial_{\mu} \phi = \left(\frac{\partial\phi}{\partial x^0}, \frac{\partial\phi}{\partial x^1}, \frac{\partial\phi}{\partial x^2}, \frac{\partial\phi}{\partial x^3}\right)$$

Under a coordinate transformation $x^{\mu} \rightarrow x'^{\mu}$, the partial derivative transforms as:

$$\frac{\partial}{\partial x'^{\mu}} = \frac{\partial x^{\nu}}{\partial x'^{\mu}} \frac{\partial}{\partial x^{\nu}}$$

Therefore:

$$\partial'_{\mu} \phi = \frac{\partial x^{\nu}}{\partial x'^{\mu}} \partial_{\nu} \phi$$

This is the transformation law for a **covariant vector** (note the derivative $\frac{\partial x^{\nu}}{\partial x'^{\mu}}$ in the transformation). 

The gradient of a scalar field is always a covariant vector because it naturally arises from partial derivatives with respect to coordinates, and partial derivatives transform covariantly.