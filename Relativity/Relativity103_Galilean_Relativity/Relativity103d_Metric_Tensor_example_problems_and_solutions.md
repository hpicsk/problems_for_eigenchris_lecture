# Metric Tensor - Problems and Solutions

## Problem 1

What is the metric tensor for a 2D Euclidean space in Cartesian coordinates?

## Solution 1

The line element in Cartesian coordinates is $ds^2 = dx^2 + dy^2$.

The metric tensor is:
$$g_{ij} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

## Problem 2

What is the metric tensor for a 2D Euclidean space in polar coordinates?

## Solution 2

The transformation from polar coordinates to Cartesian coordinates is:
$$x = r \cos(\theta)$$
$$y = r \sin(\theta)$$

Taking differentials:
$$dx = \cos(\theta)dr - r \sin(\theta)d\theta$$
$$dy = \sin(\theta)dr + r \cos(\theta)d\theta$$

The line element is:
$$ds^2 = dx^2 + dy^2 = (\cos(\theta)dr - r \sin(\theta)d\theta)^2 + (\sin(\theta)dr + r \cos(\theta)d\theta)^2$$

Expanding:
$$ds^2 = \cos^2(\theta)dr^2 - 2r \sin(\theta)\cos(\theta)dr\,d\theta + r^2 \sin^2(\theta)d\theta^2$$
$$+ \sin^2(\theta)dr^2 + 2r \sin(\theta)\cos(\theta)dr\,d\theta + r^2 \cos^2(\theta)d\theta^2$$

Simplifying:
$$ds^2 = (\cos^2(\theta) + \sin^2(\theta))dr^2 + (r^2 \sin^2(\theta) + r^2 \cos^2(\theta))d\theta^2$$

$$ds^2 = dr^2 + r^2 d\theta^2$$

The metric tensor is:
$$g_{ij} = \begin{pmatrix} 1 & 0 \\ 0 & r^2 \end{pmatrix}$$

## Problem 3

The line element in a certain coordinate system is given by $ds^2 = dr^2 + r^2 d\theta^2$. What is the metric tensor?

## Solution 3

The line element is $ds^2 = g_{ij} dx^i dx^j$.

From the given line element, we can read off the components of the metric tensor:
- $g_{rr} = 1$
- $g_{\theta\theta} = r^2$  
- $g_{r\theta} = 0$

The metric tensor is:
$$g_{ij} = \begin{pmatrix} 1 & 0 \\ 0 & r^2 \end{pmatrix}$$