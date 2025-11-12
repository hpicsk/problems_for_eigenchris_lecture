# Example Problems and Solutions: The Covariant Derivative (intrinsic) and Geodesics

## Intrinsic Covariant Derivative

### Problem 1
What does it mean for the covariant derivative to be an "intrinsic" concept?

### Solution 1
It means that the covariant derivative can be defined purely in terms of the geometry of the manifold itself, using the metric tensor, without any reference to an embedding in a higher-dimensional space.

### Problem 2
The intrinsic covariant derivative is defined by a set of axioms (linearity, product rule, metric compatibility, torsion-free). Explain the meaning of each of these axioms.

### Solution 2
- **Linearity:** The derivative of a sum is the sum of the derivatives.
- **Product rule:** The derivative of a product of tensors follows a rule similar to the product rule in ordinary calculus.
- **Metric compatibility:** The covariant derivative of the metric tensor is zero. This means that lengths and angles are preserved under parallel transport.
- **Torsion-free:** The connection is symmetric in its lower indices ($\Gamma^k_{ij} = \Gamma^k_{ji}$). This means that infinitesimal parallelograms close.

## Geodesics and the Covariant Derivative

### Problem 3
A geodesic can be defined as a curve whose tangent vector is parallel transported along itself. Write this definition as an equation using the covariant derivative.

### Solution 3
Let $u$ be the tangent vector to the curve. The condition is $\nabla_u u = 0$.

### Problem 4
Show that this definition of a geodesic is equivalent to the geodesic equation involving Christoffel symbols.

### Solution 4
$$\nabla_u u = u^i \nabla_i u^j = u^i \left(\partial_i u^j + \Gamma^j_{ik} u^k\right)$$
$$= \frac{dx^i}{dt} \left(\partial_i\frac{dx^j}{dt} + \Gamma^j_{ik}\frac{dx^k}{dt}\right) = \frac{d^2x^j}{dt^2} + \Gamma^j_{ik}\frac{dx^i}{dt}\frac{dx^k}{dt} = 0$$

### Problem 5
If a curve is a geodesic, what can you say about the magnitude of its tangent vector?

### Solution 5
The magnitude of the tangent vector is constant along a geodesic. This can be shown using metric compatibility: 
$$\frac{d}{dt}(g(u,u)) = g(\nabla_u u, u) + g(u, \nabla_u u) = 0$$

## Auto-parallel Curves

### Problem 6
What is an auto-parallel curve? How is it related to a geodesic?

### Solution 6
An auto-parallel curve is a curve whose tangent vector is parallel transported along itself. For a Levi-Civita connection (which is torsion-free), auto-parallel curves are the same as geodesics.

### Problem 7
In a space with a metric, are auto-parallel curves always geodesics? Why or why not?

### Solution 7
Yes, if the connection is the Levi-Civita connection derived from the metric. The Levi-Civita connection is the unique torsion-free, metric-compatible connection. The geodesic equation is the equation for auto-parallel curves for this connection.

## Applications

### Problem 8
In General Relativity, the paths of particles in free-fall are geodesics in spacetime. Explain what this means.

### Solution 8
This is the principle of equivalence. A particle that is not subject to any non-gravitational forces follows a path that is as "straight as possible" through curved spacetime. This path is a geodesic. Gravity is not seen as a force, but as a manifestation of the curvature of spacetime.

### Problem 9
Why is the concept of an intrinsic covariant derivative important for theories like General Relativity?

### Solution 9
General Relativity describes the universe as a 4-dimensional manifold (spacetime). There is no higher-dimensional space to embed it in. Therefore, all the tools used to describe the geometry of spacetime must be intrinsic. The intrinsic covariant derivative is essential for defining concepts like parallel transport, geodesics, and curvature in a coordinate-independent way.