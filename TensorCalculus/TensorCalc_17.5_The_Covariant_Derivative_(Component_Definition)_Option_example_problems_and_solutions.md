---
layout: default
title: "The Covariant Derivative (Component Definition) Option"
---

# The Covariant Derivative (Component Definition) Option - Problems and Solutions

This lecture focuses on the component definition of the covariant derivative. The problems will be similar to the previous lecture, but with a focus on the component-based calculations.

## Problem 1: Covariant Derivative of a Vector

1. A vector field in polar coordinates is given by $V = r \mathbf{e}_r$. 
   a) What are the components $V^r$ and $V^\theta$?
   b) Calculate all the components of the covariant derivative $\nabla_i V^j$.
2. A vector field in Cartesian coordinates is given by $V = (x, y)$. Calculate the components of the covariant derivative $\nabla_i V^j$.

### Solution 1

1. **A vector field in polar coordinates is given by $V = r \mathbf{e}_r$.**

a) **What are the components $V^r$ and $V^\theta$?**

$$V^r = r, \quad V^\theta = 0$$

b) **Calculate all the components of the covariant derivative $\nabla_i V^j$.**

$$\nabla_r V^r = \partial_r V^r = 1$$
$$\nabla_\theta V^r = \partial_\theta V^r - r V^\theta = 0$$
$$\nabla_r V^\theta = \partial_r V^\theta + \frac{1}{r}V^\theta = 0$$
$$\nabla_\theta V^\theta = \partial_\theta V^\theta + \frac{1}{r}V^r = 1$$

2. **A vector field in Cartesian coordinates is given by $V = (x, y)$. Calculate the components of the covariant derivative $\nabla_i V^j$.**

$$\nabla_x V^x = \partial_x x = 1$$
$$\nabla_y V^x = \partial_y x = 0$$
$$\nabla_x V^y = \partial_x y = 0$$
$$\nabla_y V^y = \partial_y y = 1$$

## Problem 2: Covariant Derivative of a Covector

1. A covector field in polar coordinates is given by $\alpha = dr$. 
   a) What are the components $\alpha_r$ and $\alpha_\theta$?
   b) Calculate all the components of the covariant derivative $\nabla_i \alpha_j$.
2. A covector field in Cartesian coordinates is given by $\alpha = (x, y)$. Calculate the components of the covariant derivative $\nabla_i \alpha_j$.

### Solution 2

1. **A covector field in polar coordinates is given by $\alpha = dr$.**

a) **What are the components $\alpha_r$ and $\alpha_\theta$?**

$$\alpha_r = 1, \quad \alpha_\theta = 0$$

b) **Calculate all the components of the covariant derivative $\nabla_i \alpha_j$.**

$$\nabla_r \alpha_r = \partial_r \alpha_r = 0$$
$$\nabla_\theta \alpha_r = \partial_\theta \alpha_r - \frac{1}{r}\alpha_\theta = 0$$
$$\nabla_r \alpha_\theta = \partial_r \alpha_\theta - \frac{1}{r}\alpha_\theta = 0$$
$$\nabla_\theta \alpha_\theta = \partial_\theta \alpha_\theta + r \alpha_r = r$$

2. **A covector field in Cartesian coordinates is given by $\alpha = (x, y)$. Calculate the components of the covariant derivative $\nabla_i \alpha_j$.**

$$\nabla_x \alpha_x = \partial_x x = 1$$
$$\nabla_y \alpha_x = \partial_y x = 0$$
$$\nabla_x \alpha_y = \partial_x y = 0$$
$$\nabla_y \alpha_y = \partial_y y = 1$$

## Problem 3: Covariant Divergence and Curl

1. The covariant divergence of a vector field $V$ is $\nabla_i V^i$. Calculate the divergence of the vector field $V = r \mathbf{e}_r$ in polar coordinates.
2. The curl of a vector field can also be expressed using the covariant derivative. For a 2D vector field $V$, the curl is related to $\nabla_1 V^2 - \nabla_2 V^1$. Calculate the curl of the vector field $V = (-y, x)$ in Cartesian coordinates.

### Solution 3

1. **The covariant divergence of a vector field $V$ is $\nabla_i V^i$. Calculate the divergence of the vector field $V = r \mathbf{e}_r$ in polar coordinates.**

$$\text{div}(V) = \nabla_r V^r + \nabla_\theta V^\theta = 1 + 1 = 2$$

Note: The standard formula for divergence in polar coordinates is $\frac{1}{r}\frac{\partial}{\partial r}(r V^r) + \frac{1}{r}\frac{\partial V^\theta}{\partial \theta}$. For $V=r \mathbf{e}_r$, this gives $\frac{1}{r}\frac{\partial}{\partial r}(r^2) = \frac{2r}{r} = 2$.

2. **The curl of a vector field can also be expressed using the covariant derivative. For a 2D vector field $V$, the curl is related to $\nabla_1 V^2 - \nabla_2 V^1$. Calculate the curl of the vector field $V = (-y, x)$ in Cartesian coordinates.**

$$\nabla_x V^y - \nabla_y V^x = \partial_x(x) - \partial_y(-y) = 1 - (-1) = 2$$

This is the standard curl in 2D.