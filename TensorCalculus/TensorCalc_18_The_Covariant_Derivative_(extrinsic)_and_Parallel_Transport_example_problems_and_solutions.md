---
layout: default
title: "The Covariant Derivative (extrinsic) and Parallel Transport"
---

# Example Problems and Solutions: The Covariant Derivative (extrinsic) and Parallel Transport

## Parallel Transport

### Problem 1
What is parallel transport? How is it related to the covariant derivative?

### Solution 1
Parallel transport is the process of moving a vector along a curve without changing its direction, as determined by the geometry of the space. A vector $V$ is parallel transported along a curve if its covariant derivative along the curve is zero.

### Problem 2
A vector $V$ is parallel transported along a curve $x(t)$ if $D_t V = 0$, where $D_t$ is the covariant derivative along the curve. Write out this condition in terms of components.

### Solution 2
$$\frac{dV^k}{dt} + \Gamma^k_{ij} \frac{dx^i}{dt} V^j = 0$$

### Problem 3
Consider a vector $V = (1, 0)$ at the point $(x, y) = (1, 0)$ in a 2D Cartesian plane. Parallel transport this vector along the x-axis to the point $(x, y) = (2, 0)$. What is the resulting vector?

### Solution 3
In a Cartesian plane, the Christoffel symbols are zero. The parallel transport equation is $\frac{dV^k}{dt} = 0$. This means the components of the vector do not change. The resulting vector is $(1, 0)$.

### Problem 4
Consider a vector $V$ at the north pole of a sphere, pointing towards the prime meridian. Parallel transport this vector along a line of longitude to the equator. Then, parallel transport it along the equator for 90 degrees. Finally, transport it back to the north pole along a line of longitude. What is the resulting vector? What does this tell you about parallel transport in curved spaces?

### Solution 4
The resulting vector will be rotated by 90 degrees compared to the original vector. This phenomenon, called holonomy, shows that in a curved space, parallel transport depends on the path taken. The final orientation of a vector after being transported around a closed loop depends on the curvature of the space enclosed by the loop.

## Covariant Derivative on a Surface

### Problem 5
Let $S$ be a surface embedded in $\mathbb{R}^3$. Let $V$ be a vector field tangent to $S$. The covariant derivative of $V$ on $S$ can be found by taking the derivative of $V$ in $\mathbb{R}^3$ and then projecting the result back onto the tangent plane of $S$.
a) Explain this procedure in your own words.
b) Use this method to calculate the covariant derivative of a vector field on a sphere.

### Solution 5
a) **Explain this procedure in your own words.**

Imagine a vector field on a sphere. To find how a vector changes as we move along a curve, we can think of the sphere sitting in 3D space. We take the usual derivative of the vector field in 3D, which may result in a vector that points off the sphere. We then project this resulting vector back onto the tangent plane of the sphere at that point. This projection gives us the covariant derivative on the sphere.

b) **Use this method to calculate the covariant derivative of a vector field on a sphere.**

This is a lengthy calculation that leads to the Christoffel symbols for the sphere.

## Relationship to Christoffel Symbols

### Problem 6
Explain how the Christoffel symbols arise from the projection method for the covariant derivative.

### Solution 6
The projection of the ordinary derivative back onto the tangent space involves dot products with the basis vectors of the tangent space. This projection introduces terms that depend on the derivatives of the basis vectors, and these terms are precisely the Christoffel symbols.

### Problem 7
How does this extrinsic view of the covariant derivative relate to the intrinsic view?

### Solution 7
The extrinsic view (using an embedding in a higher-dimensional flat space) and the intrinsic view (using the metric and its derivatives) give the same result for the covariant derivative. This is a non-trivial result that shows the consistency of the theory.