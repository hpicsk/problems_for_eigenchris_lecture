---
layout: default
title: "Geodesics Examples on Plane and Sphere"
---

# Geodesics Examples on Plane and Sphere - Problems and Solutions

## Problem 1: Geodesics on a Plane

1. Using the geodesic equations in Cartesian coordinates, show that the geodesics on a flat plane are straight lines of the form $y = mx + c$.
2. Using the geodesic equations in polar coordinates, show that the geodesics on a flat plane are straight lines.

### Solution 1

1. **Using the geodesic equations in Cartesian coordinates, show that the geodesics on a flat plane are straight lines of the form $y = mx + c$.**

In Cartesian coordinates, all Christoffel symbols are zero. The geodesic equations are $\frac{d^2x}{dt^2} = 0$ and $\frac{d^2y}{dt^2} = 0$. Integrating twice gives $x(t) = at+b$ and $y(t) = ct+d$. This is a parametric equation for a straight line.

2. **Using the geodesic equations in polar coordinates, show that the geodesics on a flat plane are straight lines.**

The geodesic equations are $r'' - r(\theta')^2 = 0$ and $\theta'' + \frac{2}{r}r'\theta' = 0$. The second equation gives $r^2 \theta' = L$ (constant). Substituting into the first gives $r'' - \frac{L^2}{r^3} = 0$. The solution to this is $r(\theta) = \frac{1}{A \cos(\theta) + B \sin(\theta)}$, which is the equation of a straight line in polar coordinates.

## Problem 2: Geodesics on a Sphere

The metric on a sphere of radius $R$ is $ds^2 = R^2 d\theta^2 + R^2 \sin^2(\theta) d\phi^2$.

1. Calculate the non-zero Christoffel symbols for the sphere.
2. Write down the geodesic equations for the sphere.
3. Show that the equator ($\theta = \pi/2$) is a geodesic.
4. (Advanced) Show that any great circle is a geodesic on the sphere.

### Solution 2

1. **Calculate the non-zero Christoffel symbols for the sphere.**

Metric: $ds^2 = R^2 d\theta^2 + R^2 \sin^2(\theta) d\phi^2$.

Non-zero Christoffel symbols:
$$\Gamma^\theta_{\phi\phi} = -\sin(\theta)\cos(\theta)$$
$$\Gamma^\phi_{\theta\phi} = \Gamma^\phi_{\phi\theta} = \cot(\theta)$$

2. **Write down the geodesic equations for the sphere.**

- $\theta'' + \Gamma^\theta_{\phi\phi}(\phi')^2 = 0$ ⇒ $\theta'' - \sin(\theta)\cos(\theta)(\phi')^2 = 0$
- $\phi'' + 2\Gamma^\phi_{\theta\phi}\theta'\phi' = 0$ ⇒ $\phi'' + 2\cot(\theta)\theta'\phi' = 0$

3. **Show that the equator ($\theta = \pi/2$) is a geodesic.**

If $\theta = \pi/2$, then $\theta' = 0$ and $\theta'' = 0$. The first geodesic equation becomes $0 - \sin(\pi/2)\cos(\pi/2)(\phi')^2 = 0$, which is true since $\cos(\pi/2)=0$. The second equation becomes $\phi'' = 0$, which means $\phi(t) = at+b$, so the path is along the equator at a constant speed. Thus, the equator is a geodesic.

4. **(Advanced) Show that any great circle is a geodesic on the sphere.**

A great circle is the intersection of the sphere with a plane through the origin. By rotating the coordinate system, any great circle can be made into the equator, which we have already shown to be a geodesic. Since the geodesic equation is coordinate-invariant, all great circles must be geodesics.

## Problem 3: Geodesics on a Cylinder

The metric on a cylinder of radius $R$ is $ds^2 = R^2 d\phi^2 + dz^2$.

1. Calculate the Christoffel symbols for the cylinder.
2. What are the geodesic equations for the cylinder?
3. Solve the geodesic equations to find the general form of a geodesic on a cylinder.

### Solution 3

1. **Calculate the Christoffel symbols for the cylinder.**

Metric: $ds^2 = R^2 d\phi^2 + dz^2$. All metric components are constant, so all Christoffel symbols are zero.

2. **What are the geodesic equations for the cylinder?**

$$\phi'' = 0 \quad \text{and} \quad z'' = 0$$

3. **Solve the geodesic equations to find the general form of a geodesic on a cylinder.**

$\phi(t) = at+b$ and $z(t) = ct+d$. This describes a helix (or a circle if $c=0$, or a straight line if $a=0$).