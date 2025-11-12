# TensorCalc 05.1: Derivatives Transformation Rules Discussion - Example Problems and Solutions

This lecture is a discussion, so the problems here are more conceptual and aim to solidify the understanding of the transformation rules.

## Conceptual Questions

### Problem 1
What is the key difference between contravariance and covariance?

### Solution 1
The key difference lies in how the components of an object transform when the coordinate system changes:

- **Contravariant** components (like the components of a tangent vector) transform in the *opposite* way to the basis vectors. If the basis vectors get longer, the components get smaller to keep the vector the same.

- **Covariant** components (like the components of a gradient) transform in the *same* way as the basis vectors.

Mathematically:
- Contravariant: $v'^i = \frac{\partial x'^i}{\partial x^j} v^j$
- Covariant: $\omega'_i = \frac{\partial x^j}{\partial x'^i} \omega_j$

### Problem 2
Why do the components of a vector transform contravariantly, while the basis vectors transform covariantly?

### Solution 2
A vector is a geometric object that is independent of the coordinate system. Let a vector $\mathbf{v}$ be written as $\mathbf{v} = v^i \mathbf{e}_i$. 

If we change coordinates, the vector $\mathbf{v}$ itself does not change. The new basis vectors $\mathbf{e}'_j$ are related to the old ones by:
$$\mathbf{e}'_j = \frac{\partial x^i}{\partial x'^j} \mathbf{e}_i$$

For the vector to remain the same, $\mathbf{v} = v'^j \mathbf{e}'_j$, the components must transform in the inverse way:
$$v'^j = \frac{\partial x'^j}{\partial x^i} v^i$$

This is the contravariant transformation law. The basis vectors and components must transform inversely to each other to preserve the geometric object.

### Problem 3
Give a geometrical interpretation of contravariance and covariance.

### Solution 3
**Contravariance:** Think of measuring a vector with a ruler. If you change your units on the ruler from centimeters to millimeters (the basis vectors get smaller), the number of units you measure (the component) will get larger. The physical vector remains the same, but you're measuring it with finer units.

**Covariance:** Think of the level surfaces of a function. The gradient is a covector whose components represent the density of these level surfaces along the coordinate axes. If you stretch a coordinate axis (the basis vector gets longer), the level surfaces get further apart, so the component of the gradient in that direction gets smaller.

### Problem 4
When we change coordinate systems, what happens to the underlying physical vector? Does it change? What about its components?

### Solution 4
The underlying physical vector (the geometric object) does not change. It is an invariant quantity that exists independently of any coordinate system chosen to describe it.

However, its components change depending on the coordinate system chosen to represent it. The components are just the "coordinates" we use to describe the vector in a particular basis, much like how the same location on Earth can be described with different latitude/longitude values in different coordinate systems.

### Problem 5
Why is it important to distinguish between contravariant and covariant tensors?

### Solution 5
It is crucial for writing physical laws in a coordinate-independent way. Different physical quantities transform differently, and we need to use the correct type of tensor to represent them. 

Key reasons:
1. **Mathematical consistency:** Contracting a contravariant tensor with a covariant tensor results in a tensor of lower rank, and this operation is coordinate-invariant.
2. **Physical meaning:** Different physical quantities naturally transform differently (e.g., position vs. gradient of potential).
3. **Correct formulation:** If we tried to contract two tensors of the same variance, the result would not be a tensor.
4. **General relativity:** The distinction becomes essential when dealing with curved spacetime.

## Discussion Points

### Problem 6
Discuss the transformation of the gradient of a scalar function. Does it transform contravariantly or covariantly? Why?

### Solution 6
The gradient of a scalar function transforms **covariantly**. 

The components of the gradient are $\frac{\partial f}{\partial x^i}$. Under a coordinate change:
$$\frac{\partial f}{\partial x'^j} = \frac{\partial x^i}{\partial x'^j} \cdot \frac{\partial f}{\partial x^i}$$

This is the transformation law for a covariant vector (covector).

**Physical interpretation:** The gradient measures how rapidly a function changes along coordinate directions. When you stretch a coordinate (making the basis vector longer), the rate of change along that coordinate appears smaller, which is exactly the covariant behavior.

### Problem 7
Consider the dot product of two vectors, $\mathbf{u}$ and $\mathbf{v}$. How does the dot product transform under a change of coordinates? What does this tell you about the nature of the dot product?

### Solution 7
The dot product is a scalar and is **invariant** under coordinate transformations.

To see this, let $\mathbf{u} = u^i \mathbf{e}_i$ and $\mathbf{v} = v^j \mathbf{e}_j$. In the new coordinates:
$$\mathbf{u}' \cdot \mathbf{v}' = u'^i \mathbf{e}'_i \cdot v'^j \mathbf{e}'_j$$

Through the transformation laws and using the metric tensor, this reduces to:
$$\mathbf{u}' \cdot \mathbf{v}' = u^k v^l \mathbf{e}_k \cdot \mathbf{e}_l = \mathbf{u} \cdot \mathbf{v}$$

**What this tells us:** The dot product is a well-defined geometric operation that doesn't depend on our choice of coordinates. This invariance is a fundamental property that makes the dot product physically meaningful.

### Problem 8
Discuss the relationship between the Jacobian matrix and the transformation of contravariant and covariant vectors.

### Solution 8
The Jacobian matrix and its inverse are the key to understanding tensor transformations:

**Jacobian matrix:** $J^i_j = \frac{\partial x^i}{\partial x'^j}$

**Inverse Jacobian:** $(J^{-1})^k_l = \frac{\partial x'^k}{\partial x^l}$

**Transformation rules:**
- **Contravariant vectors** transform with the inverse Jacobian: 
  $$\mathbf{v}' = J^{-1} \mathbf{v} \quad \text{or} \quad v'^i = \frac{\partial x'^i}{\partial x^j} v^j$$

- **Covariant vectors** transform with the transpose of the Jacobian:
  $$\boldsymbol{\omega}' = J^T \boldsymbol{\omega} \quad \text{or} \quad \omega'_i = \frac{\partial x^j}{\partial x'^i} \omega_j$$

**Physical insight:** The Jacobian encodes how the coordinate axes change. Contravariant objects (like displacement vectors) must transform oppositely to the axes to remain geometrically invariant, while covariant objects (like gradients) transform with the axes because they measure rates of change along those axes.