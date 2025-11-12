---
layout: default
title: "The Jacobian"
---

# The Jacobian: Example Problems and Solutions

## Jacobian Matrix

### Problem 1
Find the Jacobian matrix of the transformation from Cartesian coordinates to polar coordinates.

### Solution 1
For the transformation:
$$x = r \cos(\theta), \quad y = r \sin(\theta)$$

The Jacobian matrix is:
$$J = \begin{bmatrix} \frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} \\ \frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta} \end{bmatrix} = \begin{bmatrix} \cos(\theta) & -r\sin(\theta) \\ \sin(\theta) & r\cos(\theta) \end{bmatrix}$$

### Problem 2
Find the Jacobian matrix of the transformation from spherical coordinates $(\rho, \theta, \phi)$ to Cartesian coordinates $(x, y, z)$, where:

$$x = \rho \sin(\phi) \cos(\theta)$$
$$y = \rho \sin(\phi) \sin(\theta)$$
$$z = \rho \cos(\phi)$$

### Solution 2
The Jacobian matrix is:
$$J = \begin{bmatrix} \frac{\partial x}{\partial \rho} & \frac{\partial x}{\partial \theta} & \frac{\partial x}{\partial \phi} \\ \frac{\partial y}{\partial \rho} & \frac{\partial y}{\partial \theta} & \frac{\partial y}{\partial \phi} \\ \frac{\partial z}{\partial \rho} & \frac{\partial z}{\partial \theta} & \frac{\partial z}{\partial \phi} \end{bmatrix}$$

$$J = \begin{bmatrix} \sin(\phi)\cos(\theta) & -\rho\sin(\phi)\sin(\theta) & \rho\cos(\phi)\cos(\theta) \\ \sin(\phi)\sin(\theta) & \rho\sin(\phi)\cos(\theta) & \rho\cos(\phi)\sin(\theta) \\ \cos(\phi) & 0 & -\rho\sin(\phi) \end{bmatrix}$$

### Problem 3
Consider the transformation from parabolic coordinates $(u, v)$ to Cartesian coordinates $(x, y)$ given by:

$$x = uv$$
$$y = \frac{v^2 - u^2}{2}$$

Find the Jacobian matrix of this transformation.

### Solution 3
$$J = \begin{bmatrix} \frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\ \frac{\partial y}{\partial u} & \frac{\partial y}{\partial v} \end{bmatrix} = \begin{bmatrix} v & u \\ -u & v \end{bmatrix}$$

## Jacobian Determinant

### Problem 1
Calculate the determinant of the Jacobian matrix for the transformation from Cartesian to polar coordinates. What does this determinant represent?

### Solution 1
$$\det(J) = \cos(\theta) \cdot (r\cos(\theta)) - (-r\sin(\theta)) \cdot \sin(\theta)$$
$$= r\cos^2(\theta) + r\sin^2(\theta) = r(\cos^2(\theta) + \sin^2(\theta)) = r$$

The determinant of the Jacobian represents the scaling factor for the area element when changing coordinates:
$$dA = dx \, dy = r \, dr \, d\theta$$

### Problem 2
Calculate the determinant of the Jacobian matrix for the transformation from spherical to Cartesian coordinates.

### Solution 2
For the spherical coordinate transformation, the determinant is:
$$\det(J) = \rho^2 \sin(\phi)$$

### Problem 3
Use the Jacobian determinant to find the area element $dA = dx \, dy$ in polar coordinates.

### Solution 3
$$dA = |\det(J)| \, dr \, d\theta = r \, dr \, d\theta$$

### Problem 4
Use the Jacobian determinant to find the volume element $dV = dx \, dy \, dz$ in spherical coordinates.

### Solution 4
$$dV = |\det(J)| \, d\rho \, d\theta \, d\phi = \rho^2 \sin(\phi) \, d\rho \, d\theta \, d\phi$$

## Applications

### Problem 1
Use the Jacobian to evaluate the integral $\iint_R (x^2 + y^2) \, dx \, dy$ where $R$ is the region in the first quadrant bounded by the circle $x^2 + y^2 = 4$.

### Solution 1
In polar coordinates, $x^2 + y^2 = r^2$ and $dx \, dy = r \, dr \, d\theta$. The region is $0 \leq r \leq 2$, $0 \leq \theta \leq \pi/2$.

$$\int_0^{\pi/2} \int_0^2 (r^2) \cdot r \, dr \, d\theta = \int_0^{\pi/2} \int_0^2 r^3 \, dr \, d\theta$$

$$= \int_0^{\pi/2} \left[\frac{r^4}{4}\right]_0^2 d\theta = \int_0^{\pi/2} \frac{16}{4} \, d\theta = \int_0^{\pi/2} 4 \, d\theta = 4 \cdot \frac{\pi}{2} = 2\pi$$

### Problem 2
Consider the transformation $u = x + y$, $v = x - y$. Use the Jacobian to evaluate the integral $\iint_R e^{(x-y)/(x+y)} \, dx \, dy$ where $R$ is the triangular region with vertices $(0, 0)$, $(1, 0)$, and $(0, 1)$.

### Solution 2
First, we need the Jacobian of the inverse transformation $x = \frac{u+v}{2}$, $y = \frac{u-v}{2}$.

$$J = \begin{bmatrix} \frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\ \frac{\partial y}{\partial u} & \frac{\partial y}{\partial v} \end{bmatrix} = \begin{bmatrix} 1/2 & 1/2 \\ 1/2 & -1/2 \end{bmatrix}$$

$$\det(J) = \frac{1}{2} \cdot \left(-\frac{1}{2}\right) - \frac{1}{2} \cdot \frac{1}{2} = -\frac{1}{4} - \frac{1}{4} = -\frac{1}{2}$$

So $dx \, dy = \left|-\frac{1}{2}\right| du \, dv = \frac{1}{2} du \, dv$.

The region $R$ in $(u, v)$ coordinates: The vertices $(0,0)$, $(1,0)$, $(0,1)$ transform to $(0,0)$, $(1,1)$, $(1,-1)$ respectively. The region is bounded by $u = |v|$ and $u = 1$.

The integral becomes:
$$\iint_R e^{(x-y)/(x+y)} \, dx \, dy = \iint_{R'} e^{v/u} \cdot \frac{1}{2} \, du \, dv$$

$$= \frac{1}{2} \int_0^1 \int_{-u}^u e^{v/u} \, dv \, du$$

$$= \frac{1}{2} \int_0^1 \left[u \cdot e^{v/u}\right]_{-u}^u du = \frac{1}{2} \int_0^1 u(e^1 - e^{-1}) \, du$$

$$= \frac{1}{2} (e - e^{-1}) \int_0^1 u \, du = \frac{1}{2} (e - e^{-1}) \cdot \frac{1}{2} = \frac{1}{4}(e - e^{-1})$$