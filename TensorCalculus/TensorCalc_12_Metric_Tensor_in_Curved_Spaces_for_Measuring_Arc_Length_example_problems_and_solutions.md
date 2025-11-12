---
layout: default
title: "Metric Tensor in Curved Spaces for Measuring Arc Length"
---

# Metric Tensor in Curved Spaces for Measuring Arc Length - Problems and Solutions

## Problem 1: Metric on a Sphere

Consider a sphere of radius $R$. The coordinates on the surface of the sphere can be parameterized by the spherical coordinates $\theta$ (polar angle) and $\phi$ (azimuthal angle). The embedding of the sphere in 3D Cartesian space is given by:
$$x = R \sin(\theta) \cos(\phi)$$
$$y = R \sin(\theta) \sin(\phi)$$
$$z = R \cos(\theta)$$

1. Derive the metric tensor $g_{ij}$ for the surface of the sphere.
2. Write down the expression for the infinitesimal arc length $ds$ on the surface of the sphere.
3. Calculate the circumference of the equator of the sphere (where $\theta = \pi/2$).

### Solution 1

1. **Derive the metric tensor $g_{ij}$ for the surface of the sphere.**

$$dx = R(\cos(\theta)\cos(\phi)d\theta - \sin(\theta)\sin(\phi)d\phi)$$
$$dy = R(\cos(\theta)\sin(\phi)d\theta + \sin(\theta)\cos(\phi)d\phi)$$
$$dz = -R\sin(\theta)d\theta$$

$$ds^2 = dx^2+dy^2+dz^2 = R^2 d\theta^2 + R^2 \sin^2(\theta) d\phi^2$$

$$g = \begin{bmatrix} R^2 & 0 \\ 0 & R^2 \sin^2(\theta) \end{bmatrix}$$

2. **Write down the expression for the infinitesimal arc length $ds$ on the surface of the sphere.**

$$ds = \sqrt{R^2 d\theta^2 + R^2 \sin^2(\theta) d\phi^2}$$

3. **Calculate the circumference of the equator of the sphere (where $\theta = \pi/2$).**

At the equator, $\theta = \pi/2$, $d\theta = 0$. $ds^2 = R^2 \sin^2(\pi/2) d\phi^2 = R^2 d\phi^2$. $ds = R d\phi$.

$$\text{Circumference} = \int_0^{2\pi} R \, d\phi = 2\pi R$$

## Problem 2: Metric on a Cylinder

Consider a cylinder of radius $R$. The coordinates on the surface of the cylinder can be parameterized by $\phi$ (azimuthal angle) and $z$ (height). The embedding in 3D Cartesian space is:
$$x = R \cos(\phi)$$
$$y = R \sin(\phi)$$
$$z = z$$

1. Derive the metric tensor $g_{ij}$ for the surface of the cylinder.
2. What is the arc length element $ds$ on the cylinder?
3. Calculate the length of a helical path $\phi(t) = t$, $z(t) = t$ for $t$ from 0 to $2\pi$.

### Solution 2

1. **Derive the metric tensor $g_{ij}$ for the surface of the cylinder.**

$x = R \cos(\phi)$, $y = R \sin(\phi)$, $z = z$

$$dx = -R\sin(\phi)d\phi, \quad dy = R\cos(\phi)d\phi, \quad dz = dz$$

$$ds^2 = dx^2+dy^2+dz^2 = R^2 d\phi^2 + dz^2$$

$$g = \begin{bmatrix} R^2 & 0 \\ 0 & 1 \end{bmatrix} \text{ (in } (\phi, z) \text{ coordinates)}$$

2. **What is the arc length element $ds$ on the cylinder?**

$$ds = \sqrt{R^2 d\phi^2 + dz^2}$$

3. **Calculate the length of a helical path $\phi(t) = t$, $z(t) = t$ for $t$ from 0 to $2\pi$.**

$d\phi = dt$, $dz = dt$. $ds^2 = R^2 dt^2 + dt^2 = (R^2+1)dt^2$. $ds = \sqrt{R^2+1} \, dt$.

$$\text{Length} = \int_0^{2\pi} \sqrt{R^2+1} \, dt = 2\pi \sqrt{R^2+1}$$

## Problem 3: General Curved Spaces

1. The metric for a 2D space is given by $ds^2 = dx^2 + x^2 dy^2$. Is this space flat or curved? Justify your answer.
2. Consider the Poincaré half-plane metric $ds^2 = \frac{dx^2 + dy^2}{y^2}$ for $y > 0$. Calculate the length of the curve $x(t) = t$, $y(t) = 1$ from $t=0$ to $t=1$.

### Solution 3

1. **The metric for a 2D space is given by $ds^2 = dx^2 + x^2 dy^2$. Is this space flat or curved? Justify your answer.**

This space is curved. A simple way to see this is to calculate the Christoffel symbols and the Riemann curvature tensor. A non-zero Riemann tensor indicates curvature. For this metric, the Riemann tensor is non-zero.

2. **Consider the Poincaré half-plane metric $ds^2 = \frac{dx^2 + dy^2}{y^2}$ for $y > 0$. Calculate the length of the curve $x(t) = t$, $y(t) = 1$ from $t=0$ to $t=1$.**

$dx = dt$, $dy = 0$. $ds^2 = \frac{dt^2 + 0}{1^2} = dt^2$. $ds = dt$.

$$\text{Length} = \int_0^1 dt = 1$$