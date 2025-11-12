---
layout: default
title: "Ricci Tensor, Sectional Curvature"
---

# Example Problems and Solutions: Ricci Tensor, Sectional Curvature

## The Ricci Tensor

The Ricci tensor is obtained by contracting the Riemann tensor: $R_{jk} = R^i_{jik}$.

### Problem 1
What is the Ricci tensor? What kind of information does it capture about the curvature of the manifold?

### Solution 1
The Ricci tensor is a contraction of the Riemann tensor. It captures information about the change in volume of a small ball of geodesics. It represents a kind of average curvature.

### Problem 2
Calculate the components of the Ricci tensor for a 2D flat plane.

### Solution 2
Since the Riemann tensor is zero, the Ricci tensor is also zero.

### Problem 3
Calculate the components of the Ricci tensor for the surface of a sphere of radius $R$.

### Solution 3
$$R_{\theta\theta} = 1$$
$$R_{\phi\phi} = \sin^2(\theta)$$
In general, $R_{ij} = \frac{1}{R^2} g_{ij}$.

### Problem 4
Is the Ricci tensor symmetric? Prove your answer.

### Solution 4
Yes, the Ricci tensor is symmetric, $R_{jk} = R_{kj}$. This can be proven using the symmetries of the Riemann tensor.

## The Ricci Scalar

The Ricci scalar is obtained by contracting the Ricci tensor with the inverse metric: $R = g^{jk} R_{jk}$.

### Problem 5
What is the Ricci scalar? What does it represent?

### Solution 5
The Ricci scalar is the trace of the Ricci tensor with respect to the metric. It is a single number at each point that represents the overall curvature of the manifold at that point.

### Problem 6
Calculate the Ricci scalar for a 2D flat plane.

### Solution 6
The Ricci tensor is zero, so the Ricci scalar is zero.

### Problem 7
Calculate the Ricci scalar for the surface of a sphere of radius $R$.

### Solution 7
$$R = g^{\theta\theta}R_{\theta\theta} + g^{\phi\phi}R_{\phi\phi} = \frac{1}{R^2} \cdot 1 + \frac{1}{R^2\sin^2(\theta)} \cdot \sin^2(\theta) = \frac{1}{R^2} + \frac{1}{R^2} = \frac{2}{R^2}$$

## Sectional Curvature

The sectional curvature $K(X, Y)$ is the Gaussian curvature of the 2D surface spanned by the vectors $X$ and $Y$.
$$K(X, Y) = \frac{R_{ijkl} X^i Y^j X^k Y^l}{(g_{ik}g_{jl} - g_{il}g_{jk})X^i Y^j X^k Y^l}$$

### Problem 8
What is the geometric interpretation of sectional curvature?

### Solution 8
The sectional curvature of a 2D plane within the tangent space is the Gaussian curvature of the 2D surface formed by geodesics starting in those directions. It is a more refined measure of curvature than the Ricci scalar.

### Problem 9
If the sectional curvature is constant for all planes at all points, the manifold is a space of constant curvature.
a) What is the sectional curvature of a sphere?
b) What is the sectional curvature of a flat plane?

### Solution 9
a) **What is the sectional curvature of a sphere?**

The sectional curvature of a sphere of radius $R$ is $\frac{1}{R^2}$.

b) **What is the sectional curvature of a flat plane?**

The sectional curvature of a flat plane is 0.