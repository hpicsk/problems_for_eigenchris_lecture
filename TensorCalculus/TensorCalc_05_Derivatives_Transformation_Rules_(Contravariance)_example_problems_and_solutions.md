---
layout: default
title: "Derivatives Transformation Rules (Contravariance)"
---

# Example Problems and Solutions: Derivatives Transformation Rules (Contravariance)

## Transformation of Basis Vectors

### Problem 1
Consider the transformation from Cartesian coordinates $(x, y)$ to polar coordinates $(r, \theta)$. How do the basis vectors $(\mathbf{e}_x, \mathbf{e}_y)$ transform?

### Solution 1
The basis vectors transform covariantly. The new basis vectors $(\mathbf{e}_r, \mathbf{e}_\theta)$ are related to the old ones $(\mathbf{e}_x, \mathbf{e}_y)$ by:

$$\mathbf{e}_r = \frac{\partial x}{\partial r}\mathbf{e}_x + \frac{\partial y}{\partial r}\mathbf{e}_y = \cos(\theta)\mathbf{e}_x + \sin(\theta)\mathbf{e}_y$$

$$\mathbf{e}_\theta = \frac{\partial x}{\partial \theta}\mathbf{e}_x + \frac{\partial y}{\partial \theta}\mathbf{e}_y = -r\sin(\theta)\mathbf{e}_x + r\cos(\theta)\mathbf{e}_y$$

### Problem 2
For the transformation from Cartesian to spherical coordinates, find the transformation matrix for the basis vectors.

### Solution 2
The transformation equations are:
$$x = \rho \sin(\phi) \cos(\theta), \quad y = \rho \sin(\phi) \sin(\theta), \quad z = \rho \cos(\phi)$$

The new basis vectors $(\mathbf{e}_\rho, \mathbf{e}_\theta, \mathbf{e}_\phi)$ are given by the partial derivatives:

$$\mathbf{e}_\rho = \sin(\phi)\cos(\theta)\mathbf{e}_x + \sin(\phi)\sin(\theta)\mathbf{e}_y + \cos(\phi)\mathbf{e}_z$$

$$\mathbf{e}_\theta = -\rho\sin(\phi)\sin(\theta)\mathbf{e}_x + \rho\sin(\phi)\cos(\theta)\mathbf{e}_y$$

$$\mathbf{e}_\phi = \rho\cos(\phi)\cos(\theta)\mathbf{e}_x + \rho\cos(\phi)\sin(\theta)\mathbf{e}_y - \rho\sin(\phi)\mathbf{e}_z$$

## Contravariant Vectors

### Problem 3
Show that the components of a tangent vector to a curve transform contravariantly.

### Solution 3
Let a curve be parameterized by $x^i(t)$. The tangent vector has components $V^i = \frac{dx^i}{dt}$. 

In a new coordinate system $x'^j$, the tangent vector components are $V'^j = \frac{dx'^j}{dt}$. 

Using the chain rule:
$$\frac{dx'^j}{dt} = \frac{\partial x'^j}{\partial x^i} \cdot \frac{dx^i}{dt} = \frac{\partial x'^j}{\partial x^i} V^i$$

Therefore:
$$V'^j = \frac{\partial x'^j}{\partial x^i} V^i$$

This is the transformation law for a contravariant vector.

### Problem 4
A vector $\mathbf{v}$ has components $(1, 1)$ in Cartesian coordinates. What are its components in polar coordinates at the point $(1, 1)$? Use the transformation rules for contravariant vectors.

### Solution 4
At $(x,y) = (1,1)$, we have $r = \sqrt{1^2 + 1^2} = \sqrt{2}$ and $\theta = \arctan(1/1) = \frac{\pi}{4}$.

The transformation is $v'^j = \frac{\partial x'^j}{\partial x^i} v^i$.

For the $r$-component:
$$v^r = \frac{\partial r}{\partial x}v^x + \frac{\partial r}{\partial y}v^y$$

Since $r = \sqrt{x^2 + y^2}$:
$$\frac{\partial r}{\partial x} = \frac{x}{r} = \frac{1}{\sqrt{2}}, \quad \frac{\partial r}{\partial y} = \frac{y}{r} = \frac{1}{\sqrt{2}}$$

Therefore:
$$v^r = \frac{1}{\sqrt{2}} \cdot 1 + \frac{1}{\sqrt{2}} \cdot 1 = \frac{2}{\sqrt{2}} = \sqrt{2}$$

For the $\theta$-component:
$$v^\theta = \frac{\partial \theta}{\partial x}v^x + \frac{\partial \theta}{\partial y}v^y$$

Since $\theta = \arctan(y/x)$:
$$\frac{\partial \theta}{\partial x} = -\frac{y}{x^2 + y^2} = -\frac{1}{2}, \quad \frac{\partial \theta}{\partial y} = \frac{x}{x^2 + y^2} = \frac{1}{2}$$

Therefore:
$$v^\theta = -\frac{1}{2} \cdot 1 + \frac{1}{2} \cdot 1 = 0$$

The components are $(\sqrt{2}, 0)$.

### Problem 5
The components of a vector $\mathbf{A}$ in the $x_i$ coordinate system are $A^i$. The coordinates $x_i$ are related to the coordinates $x'_j$ by $x_i = M_{ij} x'_j$ where $M$ is a constant matrix. How do the components $A^i$ transform? What are the components $A'^j$ in the new coordinate system?

### Solution 5
From the contravariant transformation rule:
$$A'^j = \frac{\partial x'^j}{\partial x^i} A^i$$

From $x = M x'$, we have $x' = M^{-1} x$. Therefore:
$$\frac{\partial x'^j}{\partial x^i} = (M^{-1})_{ji}$$

So:
$$A'^j = (M^{-1})_{ji} A^i$$

In matrix notation: $\mathbf{A}' = M^{-1} \mathbf{A}$.

## Contravariant Tensors

### Problem 6
A second-rank tensor $T$ has components $T^{ij}$ in the $x_i$ coordinate system. How do the components of $T$ transform under a change of coordinates?

### Solution 6
For a second-rank contravariant tensor, the transformation rule is:
$$T'^{kl} = \frac{\partial x'^k}{\partial x^i} \frac{\partial x'^l}{\partial x^j} T^{ij}$$

This extends naturally from the contravariant vector transformation rule, with one transformation factor for each index.

### Problem 7
Let $A^i$ and $B^j$ be the components of two contravariant vectors. Show that the outer product $T^{ij} = A^i B^j$ transforms as a second-rank contravariant tensor.

### Solution 7
Under a coordinate transformation:
$$T'^{kl} = A'^k B'^l$$

Using the contravariant transformation rules for vectors:
$$A'^k = \frac{\partial x'^k}{\partial x^i} A^i, \quad B'^l = \frac{\partial x'^l}{\partial x^j} B^j$$

Therefore:
$$T'^{kl} = \left(\frac{\partial x'^k}{\partial x^i} A^i\right) \left(\frac{\partial x'^l}{\partial x^j} B^j\right)$$

$$= \frac{\partial x'^k}{\partial x^i} \frac{\partial x'^l}{\partial x^j} A^i B^j$$

$$= \frac{\partial x'^k}{\partial x^i} \frac{\partial x'^l}{\partial x^j} T^{ij}$$

This is exactly the transformation rule for a rank-2 contravariant tensor, proving that the outer product of two contravariant vectors is indeed a contravariant tensor of rank 2.