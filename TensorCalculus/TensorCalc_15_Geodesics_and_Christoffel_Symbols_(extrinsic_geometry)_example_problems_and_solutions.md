---
layout: default
title: "Geodesics and Christoffel Symbols (extrinsic geometry)"
---

# Geodesics and Christoffel Symbols (extrinsic geometry) - Problems and Solutions

## Problem 1: Geodesics

1. What is a geodesic? Give a qualitative description.
2. What is the geodesic equation?
3. Show that a straight line in Euclidean space is a geodesic.

### Solution 1

1. **What is a geodesic? Give a qualitative description.**

A geodesic is the shortest path between two points on a manifold. In flat space, this is a straight line. In curved space, it is a curve that is as "straight as possible". For example, on a sphere, geodesics are great circles.

2. **What is the geodesic equation?**

The geodesic equation is a set of second-order differential equations that describes the path of a geodesic. In terms of a parameter $t$, it is:

$$\frac{d^2x^k}{dt^2} + \Gamma^k_{ij} \frac{dx^i}{dt} \frac{dx^j}{dt} = 0$$

where $\Gamma^k_{ij}$ are the Christoffel symbols.

3. **Show that a straight line in Euclidean space is a geodesic.**

In Euclidean space, the Christoffel symbols are all zero. The geodesic equation becomes $\frac{d^2x^k}{dt^2} = 0$. Integrating twice gives $x^k(t) = a^k t + b^k$, which is the equation of a straight line.

## Problem 2: Christoffel Symbols

1. What do the Christoffel symbols represent? How are they related to the metric tensor?
2. The Christoffel symbols of the first kind are defined as $\Gamma_{ijk} = \frac{1}{2} (\partial_j g_{ik} + \partial_i g_{jk} - \partial_k g_{ij})$. The Christoffel symbols of the second kind are $\Gamma^k_{ij} = g^{kl} \Gamma_{lij}$.
   a) Calculate the Christoffel symbols for a 2D Cartesian coordinate system.
   b) Calculate the Christoffel symbols for a 2D polar coordinate system.

### Solution 2

1. **What do the Christoffel symbols represent? How are they related to the metric tensor?**

The Christoffel symbols are correction terms that appear in the covariant derivative. They account for the fact that the basis vectors change from point to point in a general coordinate system. They are derived from the metric tensor and its derivatives.

2. **Calculate the Christoffel symbols:**

a) **For a 2D Cartesian coordinate system:**

The metric is $g = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$. All components are constant, so all derivatives of the metric are zero. Therefore, all Christoffel symbols are zero.

b) **For a 2D polar coordinate system:**

The metric is $g = \begin{bmatrix} 1 & 0 \\ 0 & r^2 \end{bmatrix}$. The non-zero Christoffel symbols are:

$$\Gamma^r_{\theta\theta} = -r$$
$$\Gamma^\theta_{r\theta} = \Gamma^\theta_{\theta r} = \frac{1}{r}$$

## Problem 3: Geodesic Equation with Christoffel Symbols

The geodesic equation is given by $\frac{d^2x^k}{dt^2} + \Gamma^k_{ij} \frac{dx^i}{dt} \frac{dx^j}{dt} = 0$.

1. Write out the geodesic equations for a 2D polar coordinate system.
2. Solve the geodesic equations for a flat plane in polar coordinates to show that the geodesics are straight lines.

### Solution 3

1. **Write out the geodesic equations for a 2D polar coordinate system.**

- $k=r$: $\frac{d^2r}{dt^2} + \Gamma^r_{\theta\theta}\left(\frac{d\theta}{dt}\right)^2 = 0$ ⇒ $\frac{d^2r}{dt^2} - r\left(\frac{d\theta}{dt}\right)^2 = 0$

- $k=\theta$: $\frac{d^2\theta}{dt^2} + 2\Gamma^\theta_{r\theta}\frac{dr}{dt}\frac{d\theta}{dt} = 0$ ⇒ $\frac{d^2\theta}{dt^2} + \frac{2}{r}\frac{dr}{dt}\frac{d\theta}{dt} = 0$

2. **Solve the geodesic equations for a flat plane in polar coordinates to show that the geodesics are straight lines.**

This is a non-trivial calculation. The second equation can be rewritten as $\frac{1}{r^2} \frac{d}{dt}\left(r^2 \frac{d\theta}{dt}\right) = 0$, which implies $r^2 \frac{d\theta}{dt} = \text{constant} = L$ (conservation of angular momentum). Substituting this into the first equation gives a differential equation for $r(t)$ which can be solved to show that the path is a straight line.

## Problem 4: Extrinsic vs. Intrinsic Geometry

1. What is the difference between extrinsic and intrinsic geometry?
2. Are the Christoffel symbols an intrinsic or extrinsic property of a manifold?

### Solution 4

1. **What is the difference between extrinsic and intrinsic geometry?**

- **Extrinsic geometry** depends on how the manifold is embedded in a higher-dimensional space. For example, the curvature of a sphere as seen from 3D space.
- **Intrinsic geometry** is the geometry of the manifold itself, without reference to any embedding. An inhabitant of the 2D surface of a sphere could measure its curvature without ever knowing about the 3rd dimension.

2. **Are the Christoffel symbols an intrinsic or extrinsic property of a manifold?**

The Christoffel symbols themselves are not tensors and are coordinate-dependent. However, they are derived from the metric tensor, which is an intrinsic property of the manifold. Therefore, the geometry they describe is intrinsic.