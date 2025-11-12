---
layout: default
title: "Gradient Explanation and Examples"
---

# Gradient Explanation and Examples - Problems and Solutions

## Problem 1: Geometric Interpretation of the Gradient

1. The gradient $\nabla f$ of a scalar function $f$ points in the direction of the greatest rate of increase of $f$.
   a) Prove this statement.
   b) What is the magnitude of the gradient $|\nabla f|$?
2. Show that the gradient $\nabla f$ at a point $P$ is perpendicular to the level surface of $f$ that passes through $P$.

### Solution 1

1. **The gradient $\nabla f$ of a scalar function $f$ points in the direction of the greatest rate of increase of $f$.**

a) **Prove this statement.**

The directional derivative of $f$ in the direction of a unit vector $\mathbf{u}$ is $D_{\mathbf{u}} f = \nabla f \cdot \mathbf{u} = |\nabla f| |\mathbf{u}| \cos(\theta) = |\nabla f| \cos(\theta)$, where $\theta$ is the angle between $\nabla f$ and $\mathbf{u}$. This is maximized when $\cos(\theta) = 1$, i.e., when $\mathbf{u}$ is in the same direction as $\nabla f$.

b) **What is the magnitude of the gradient $|\nabla f|$?**

The magnitude of the gradient is the maximum rate of increase of the function.

2. **Show that the gradient $\nabla f$ at a point $P$ is perpendicular to the level surface of $f$ that passes through $P$.**

Let $\mathbf{r}(t)$ be a curve on a level surface $f(c)$. Then $f(\mathbf{r}(t)) = c$. Differentiating with respect to $t$ gives $\nabla f(\mathbf{r}(t)) \cdot \mathbf{r}'(t) = 0$. Since $\mathbf{r}'(t)$ is a tangent vector to the level surface, $\nabla f$ is orthogonal to the surface.

## Problem 2: Examples in Cartesian Coordinates

1. Let $f(x, y) = 9 - x^2 - y^2$.
   a) Find $\nabla f$.
   b) Sketch the level curves for $f = 0, 5, 9$.
   c) Sketch the gradient vector at the points (1, 2) and (3, 0).
2. A hiker is on a mountain whose elevation is given by $h(x, y) = 1000 - 0.01x^2 - 0.02y^2$. The hiker is at the point (50, 100).
   a) In which direction should the hiker move to ascend the fastest?
   b) What is the slope of the mountain in that direction?

### Solution 2

1. **Let $f(x, y) = 9 - x^2 - y^2$.**

a) **Find $\nabla f$.**

$$\nabla f = (-2x, -2y)$$

b) **Sketch the level curves for $f = 0, 5, 9$.**

- $f=0$: $x^2+y^2=9$ (circle of radius 3)
- $f=5$: $x^2+y^2=4$ (circle of radius 2)
- $f=9$: $x^2+y^2=0$ (the origin)

c) **Sketch the gradient vector at the points (1, 2) and (3, 0).**

- $\nabla f(1, 2) = (-2, -4)$
- $\nabla f(3, 0) = (-6, 0)$

The gradient vectors point towards the origin, perpendicular to the level circles.

2. **A hiker is on a mountain whose elevation is given by $h(x, y) = 1000 - 0.01x^2 - 0.02y^2$. The hiker is at the point (50, 100).**

a) **In which direction should the hiker move to ascend the fastest?**

The direction of fastest ascent is $\nabla h = (-0.02x, -0.04y)$. 

$$\nabla h(50, 100) = (-1, -4)$$

The hiker should move in the direction $(-1, -4)$.

b) **What is the slope of the mountain in that direction?**

The slope is $|\nabla h(50, 100)| = \sqrt{(-1)^2 + (-4)^2} = \sqrt{17}$.

## Problem 3: Examples in Other Coordinate Systems

1. The temperature in a room is given by $T(r, \theta) = 10 + r \cos(\theta)$. 
   a) Find the gradient of the temperature in polar coordinates.
   b) At the point $(r, \theta) = (2, \pi/4)$, in which direction is the temperature increasing the most rapidly?
2. The gravitational potential of a point mass at the origin is $\Phi(r) = -\frac{GM}{r}$, where $r$ is the distance from the origin. The gravitational force is given by $\mathbf{F} = -\nabla\Phi$. Find the gravitational force in spherical coordinates.

### Solution 3

1. **The temperature in a room is given by $T(r, \theta) = 10 + r \cos(\theta)$.**

a) **Find the gradient of the temperature in polar coordinates.**

$$\nabla T = \frac{\partial T}{\partial r}\mathbf{e}_r + \frac{1}{r}\frac{\partial T}{\partial \theta}\mathbf{e}_\theta = \cos(\theta) \mathbf{e}_r - \sin(\theta) \mathbf{e}_\theta$$

b) **At the point $(r, \theta) = (2, \pi/4)$, in which direction is the temperature increasing the most rapidly?**

$$\nabla T(2, \pi/4) = \cos(\pi/4) \mathbf{e}_r - \sin(\pi/4) \mathbf{e}_\theta = \frac{\sqrt{2}}{2}\mathbf{e}_r - \frac{\sqrt{2}}{2}\mathbf{e}_\theta$$

2. **The gravitational potential of a point mass at the origin is $\Phi(r) = -\frac{GM}{r}$, where $r$ is the distance from the origin. The gravitational force is given by $\mathbf{F} = -\nabla\Phi$. Find the gravitational force in spherical coordinates.**

In spherical coordinates, $\nabla\Phi = \frac{\partial \Phi}{\partial r}\mathbf{e}_r = \frac{GM}{r^2}\mathbf{e}_r$.

$$\mathbf{F} = -\nabla\Phi = -\frac{GM}{r^2}\mathbf{e}_r$$

This is the familiar inverse-square law for gravity.