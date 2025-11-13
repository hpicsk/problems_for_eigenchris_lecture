# TensorCalc 23: Riemann Curvature Tensor Components - Example Problems and Solutions

## Components of the Riemann Tensor

The components of the Riemann curvature tensor are given by:
$$R^i_{jkl} = \partial_k \Gamma^i_{jl} - \partial_l \Gamma^i_{jk} + \Gamma^i_{km} \Gamma^m_{jl} - \Gamma^i_{lm} \Gamma^m_{jk}$$

### Problem 1
Calculate the components of the Riemann curvature tensor for a 2D flat plane in Cartesian coordinates.

### Solution 1
In Cartesian coordinates, all Christoffel symbols are zero. Therefore, all components of the Riemann tensor are zero.

### Problem 2
Calculate the components of the Riemann curvature tensor for a 2D flat plane in polar coordinates.

### Solution 2
Although the Christoffel symbols are non-zero in polar coordinates, the Riemann tensor is a tensor, and if it is zero in one coordinate system, it must be zero in all coordinate systems. So, the components are all zero. This can be verified by a lengthy but straightforward calculation using the formula for $R^i_{jkl}$.

### Problem 3
Calculate the components of the Riemann curvature tensor for the surface of a sphere of radius $R$.

### Solution 3
The only non-zero independent component is $R^{\theta}_{\phi\theta\phi} = \sin^2(\theta)$. The other non-zero components can be derived from this one using the symmetries of the Riemann tensor. For example, $R_{\theta\phi\theta\phi} = g_{\theta k}R^k_{\phi\theta\phi} = g_{\theta\theta}R^{\theta}_{\phi\theta\phi} = R^2 \sin^2(\theta)$.

## Geodesic Deviation

The equation of geodesic deviation is $\frac{D^2_t S^i}{dt^2} = R^i_{jkl} \frac{dx^j}{dt} S^k \frac{dx^l}{dt}$, where $S$ is the separation vector between two nearby geodesics.

### Problem 4
What is the physical meaning of the geodesic deviation equation?

### Solution 4
The geodesic deviation equation describes how nearby geodesics either converge or diverge. It explains tidal forces in General Relativity. An object in a gravitational field is stretched or squeezed because different parts of it follow slightly different geodesics.

### Problem 5
Consider two nearby geodesics on a flat plane. Show that the separation vector does not change, implying that the geodesics remain parallel.

### Solution 5
On a flat plane, the Riemann tensor is zero, so $\frac{D^2_t S^i}{dt^2} = 0$. This means that the separation vector $S$ changes linearly with time, so the geodesics remain parallel (or move apart at a constant rate).

### Problem 6
Consider two nearby geodesics on a sphere (e.g., two lines of longitude near the equator). Show that they converge, and relate this to the components of the Riemann tensor.

### Solution 6
On a sphere, the Riemann tensor is non-zero. The geodesic deviation equation will show that $\frac{D^2_t S^i}{dt^2}$ is proportional to $-S^i$, indicating that the separation vector decreases, and the geodesics converge. The rate of convergence is determined by the curvature.