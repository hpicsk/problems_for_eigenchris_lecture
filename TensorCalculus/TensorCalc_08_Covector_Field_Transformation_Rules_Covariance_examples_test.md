---
layout: default
title: Covector Field Transformation Rules (Covariance) Example Problems and Solutions (Test)
permalink: /TensorCalculus/TensorCalc_08_Covector_Field_Transformation_Rules_Covariance_examples_test/
---

# Example Problems and Solutions: Covector Field Transformation Rules (Covariance)

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

---
layout: default
title: Covector Field Transformation Rules (Covariance) Example Problems and Solutions (Test)
permalink: /TensorCalculus/TensorCalc_08_Covector_Field_Transformation_Rules_Covariance_examples_test/
---

# Example Problems and Solutions: Covector Field Transformation Rules (Covariance)

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
