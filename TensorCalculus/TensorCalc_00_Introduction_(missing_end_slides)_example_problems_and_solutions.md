# TensorCalc 00: Introduction (missing end slides) - Example Problems and Solutions

## Conceptual Questions

### Problem 1
What is a tensor? Explain in your own words.

### Solution 1
A tensor is a mathematical object that generalizes scalars, vectors, and matrices. It is a geometric entity that can be used to describe physical properties and relationships between vectors and other tensors. A tensor is independent of the coordinate system used to describe it, but its components will change in a specific, predictable way when the coordinate system is changed.

### Problem 2
What is the rank of a tensor? Give examples of tensors of rank 0, 1, and 2.

### Solution 2
The rank of a tensor (also called its order) indicates the number of indices needed to specify its components.

- **Rank 0:** A scalar (e.g., temperature, mass). It has only one component and no indices.
- **Rank 1:** A vector (e.g., velocity, force). It has components specified by one index (e.g., $v_i$).
- **Rank 2:** A matrix-like object (e.g., stress tensor, strain tensor). It has components specified by two indices (e.g., $T_{ij}$).

### Problem 3
What is the difference between a scalar, a vector, and a tensor?

### Solution 3
- A **scalar** is a single number that has only magnitude.
- A **vector** is an object that has both magnitude and direction.
- A **tensor** is a more general object. A scalar is a rank-0 tensor, and a vector is a rank-1 tensor. Higher-rank tensors can represent more complex quantities, such as the relationship between different vectors (e.g., how a material deforms - the stress tensor relates the normal vector of a surface to the force acting on that surface).

### Problem 4
Provide an example of a physical quantity that can be represented by:

a) A scalar

b) A vector

c) A tensor of rank 2

### Solution 4
a) **A scalar:** Temperature, mass, speed, energy.

b) **A vector:** Velocity, force, acceleration, displacement.

c) **A tensor of rank 2:** The stress tensor (relates the direction of a surface to the stress on that surface), the strain tensor (describes the deformation of a material), the moment of inertia tensor (relates the angular velocity of a rigid body to its angular momentum).

### Problem 5
Why is tensor calculus important in physics and engineering?

### Solution 5
Tensor calculus is crucial because it provides a framework for expressing physical laws in a way that is independent of the choice of coordinate system. This is essential in fields like General Relativity, where spacetime is curved and there is no single preferred coordinate system. It is also fundamental in continuum mechanics, electromagnetism, and many other areas of physics and engineering where physical properties are anisotropic (direction-dependent).

## Basic Problems

### Problem 1
Given a vector $v$ with components $(v_1, v_2, v_3)$ and a covector $\alpha$ with components $(\alpha_1, \alpha_2, \alpha_3)$, what is the result of their contraction $\alpha(v)$?

### Solution 1
The contraction $\alpha(v)$ is a scalar given by the sum of the products of their corresponding components:

$$\alpha(v) = \alpha_1 v^1 + \alpha_2 v^2 + \alpha_3 v^3 = \sum_{i=1}^{3} \alpha_i v^i$$

### Problem 2
If a tensor $T$ has components $T_{ij}$ in one coordinate system, and we change to a new coordinate system, what is the general form of the transformation rule for the components of $T$?

### Solution 2
Let the transformation from the old coordinates $x^i$ to the new coordinates $x'^k$ be given by $x'^k = x'^k(x^i)$. The components $T'_{kl}$ of the tensor in the new coordinate system are related to the components $T_{ij}$ in the old system by the following transformation rule (for a covariant tensor of rank 2):

$$T'_{kl} = \frac{\partial x^i}{\partial x'^k} \frac{\partial x^j}{\partial x'^l} T_{ij}$$

### Problem 3
What is the Einstein summation convention? Rewrite the following expression using the Einstein summation convention:

$$c = a_1 b_1 + a_2 b_2 + a_3 b_3$$

### Solution 3
The Einstein summation convention states that if an index appears twice in a single term (once as an upper index and once as a lower index, or in some contexts both as lower indices), it implies summation over all possible values of that index.

The expression $c = a_1 b_1 + a_2 b_2 + a_3 b_3$ can be written as:

$$c = a_i b_i$$


### Problem 4
Given a 2nd rank tensor $T$ and a vector $v$, what is the rank of the object $T(v)$?

### Solution 4
When a 2nd rank tensor $T$ (with components $T^i_j$) acts on a vector $v$ (with components $v^j$), the result is a vector. This is a contraction over one index:

$$(T(v))^i = T^i_j v^j$$

The resulting object has one free index ($i$), so it is a rank-1 tensor (a vector).