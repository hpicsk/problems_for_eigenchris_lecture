---
layout: default
title: "Metric Tensor and Arc Lengths (Flat Space)"
---

# Metric Tensor and Arc Lengths (Flat Space) - Problems and Solutions

## Problem 1: The Metric Tensor

1. What is the metric tensor? What does it represent?
2. Write down the components of the metric tensor $g_{ij}$ for:
   a) A 2D Cartesian coordinate system.
   b) A 3D Cartesian coordinate system.
   c) A 2D polar coordinate system.

### Solution 1

1. **What is the metric tensor? What does it represent?**

The metric tensor is a rank-2 tensor that defines the geometry of a space. It allows us to calculate distances, angles, and volumes. It essentially defines the dot product in a given coordinate system.

2. **Write down the components of the metric tensor $g_{ij}$ for:**

a) **A 2D Cartesian coordinate system:** $g = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$

b) **A 3D Cartesian coordinate system:** $g = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$

c) **A 2D polar coordinate system:** $g = \begin{bmatrix} 1 & 0 \\ 0 & r^2 \end{bmatrix}$

## Problem 2: Arc Length

The infinitesimal arc length $ds$ is given by $ds^2 = g_{ij} dx^i dx^j$.

1. Using the metric tensor in polar coordinates, derive the expression for the arc length $ds$ in terms of $dr$ and $d\theta$.
2. Calculate the length of the curve $r(t) = (R\cos(t), R\sin(t))$ for $t$ from 0 to $2\pi$ using:
   a) The Cartesian metric.
   b) The polar metric.
3. Calculate the length of the curve $y = x^2$ from $x=0$ to $x=1$.

### Solution 2

1. **Using the metric tensor in polar coordinates, derive the expression for the arc length $ds$ in terms of $dr$ and $d\theta$.**

$$ds^2 = g_{ij} dx^i dx^j = g_{rr} dr^2 + g_{\theta\theta} d\theta^2 = 1 \cdot dr^2 + r^2 \cdot d\theta^2 = dr^2 + r^2 d\theta^2$$

2. **Calculate the length of the curve $r(t) = (R\cos(t), R\sin(t))$ for $t$ from 0 to $2\pi$ using:**

a) **The Cartesian metric:** $x(t) = R\cos(t)$, $y(t) = R\sin(t)$. $\frac{dx}{dt} = -R\sin(t)$, $\frac{dy}{dt} = R\cos(t)$. 

$$ds^2 = dx^2 + dy^2 = (R^2\sin^2(t) + R^2\cos^2(t))dt^2 = R^2 dt^2$$

$ds = R dt$. 

$$\text{Length} = \int_0^{2\pi} R \, dt = 2\pi R$$

b) **The polar metric:** $r(t) = R$, $\theta(t) = t$. $\frac{dr}{dt} = 0$, $\frac{d\theta}{dt} = 1$. 

$$ds^2 = dr^2 + r^2 d\theta^2 = 0 + R^2 dt^2$$

$ds = R dt$. 

$$\text{Length} = \int_0^{2\pi} R \, dt = 2\pi R$$

3. **Calculate the length of the curve $y = x^2$ from $x=0$ to $x=1$.**

$dy = 2x \, dx$. $ds^2 = dx^2 + dy^2 = dx^2 + (2x \, dx)^2 = (1 + 4x^2) dx^2$. $ds = \sqrt{1+4x^2} \, dx$.

$$\text{Length} = \int_0^1 \sqrt{1+4x^2} \, dx = \left[\frac{1}{2} \cdot x\sqrt{1+4x^2} + \frac{1}{4} \cdot \sinh^{-1}(2x)\right]_0^1 = \frac{1}{2}\sqrt{5} + \frac{1}{4}\sinh^{-1}(2)$$

## Problem 3: Dot Product

The dot product of two vectors $u$ and $v$ is given by $u \cdot v = g_{ij} u^i v^j$.

1. Two vectors are given in polar coordinates at a point $(r, \theta)$ by $u = (u^r, u^\theta)$ and $v = (v^r, v^\theta)$. Write out the expression for their dot product.
2. In a 2D Cartesian coordinate system, $u = (1, 2)$ and $v = (3, -1)$. Calculate their dot product.
3. In a 2D polar coordinate system, at the point $(r, \theta) = (1, \pi/2)$, two vectors are given by $u = (1, 0)$ (pointing in the radial direction) and $v = (0, 1)$ (pointing in the angular direction). Calculate their dot product.

### Solution 3

1. **Two vectors are given in polar coordinates at a point $(r, \theta)$ by $u = (u^r, u^\theta)$ and $v = (v^r, v^\theta)$. Write out the expression for their dot product.**

$$u \cdot v = g_{ij} u^i v^j = g_{rr}u^r v^r + g_{\theta\theta}u^\theta v^\theta = u^r v^r + r^2 u^\theta v^\theta$$

2. **In a 2D Cartesian coordinate system, $u = (1, 2)$ and $v = (3, -1)$. Calculate their dot product.**

$$u \cdot v = 1 \cdot 3 + 2 \cdot (-1) = 1$$

3. **In a 2D polar coordinate system, at the point $(r, \theta) = (1, \pi/2)$, two vectors are given by $u = (1, 0)$ (pointing in the radial direction) and $v = (0, 1)$ (pointing in the angular direction). Calculate their dot product.**

$$u \cdot v = u^r v^r + r^2 u^\theta v^\theta = 1 \cdot 0 + 1^2 \cdot 0 \cdot 1 = 0$$

The basis vectors are orthogonal.