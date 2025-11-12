---
layout: default
title: "Geodesics"
---

# Geodesics - Problems and Solutions

## Problem 1

What is the geodesic equation?

### Solution 1

The geodesic equation describes the path of a freely falling particle in curved spacetime. It represents the equation of motion for a particle that moves under no forces other than gravity (which is represented by spacetime curvature).

The geodesic equation is:
$$\frac{d^2x^{\mu}}{d\tau^2} + \Gamma^{\mu}_{\alpha\beta} \frac{dx^{\alpha}}{d\tau} \frac{dx^{\beta}}{d\tau} = 0$$

where:
- $x^{\mu}(\tau)$ is the worldline of the particle
- $\tau$ is the proper time (for massive particles) or an affine parameter (for massless particles)
- $\Gamma^{\mu}_{\alpha\beta}$ are the Christoffel symbols
- The repeated indices $\alpha$ and $\beta$ are summed over

**Physical interpretation**: This equation says that a freely falling particle follows the "straightest possible path" in curved spacetime. The Christoffel symbol term corrects for the curvature of spacetime.

## Problem 2

Show that a straight line is a geodesic in Euclidean space.

### Solution 2

In Euclidean space with Cartesian coordinates, the metric tensor is:
$$g_{\mu\nu} = \delta_{\mu\nu} = \text{diag}(1, 1, 1, \ldots)$$

Since the metric components are constant, all partial derivatives of the metric vanish:
$$\partial_{\alpha} g_{\mu\nu} = 0 \quad \text{for all } \alpha, \mu, \nu$$

Therefore, all Christoffel symbols are zero:
$$\Gamma^{\mu}_{\alpha\beta} = \frac{1}{2} g^{\mu\rho} \left(\partial_{\alpha} g_{\rho\beta} + \partial_{\beta} g_{\rho\alpha} - \partial_{\rho} g_{\alpha\beta}\right) = 0$$

The geodesic equation becomes:
$$\frac{d^2x^{\mu}}{d\tau^2} = 0$$

The general solution is:
$$x^{\mu}(\tau) = A^{\mu} \tau + B^{\mu}$$

where $A^{\mu}$ and $B^{\mu}$ are constants determined by initial conditions.

This is indeed the equation of a straight line, confirming that straight lines are geodesics in flat Euclidean space.

## Problem 3

Find the geodesics of a 2D sphere.

### Solution 3

The geodesics of a 2D sphere are **great circles**.

**Intuitive explanation**: A great circle is the intersection of the sphere with a plane that passes through the center of the sphere. These represent the shortest paths between two points on the sphere's surface.

**Examples of great circles**:
- All lines of longitude (meridians)
- The equator
- Any circle on the sphere that has the same radius as the sphere itself

**Mathematical approach**: 
For a sphere of radius $R$ with metric:
$$ds^2 = R^2(d\theta^2 + \sin^2\theta \, d\phi^2)$$

The geodesic equations can be solved to show that the solutions are indeed great circles. The key insight is that any geodesic on a sphere lies in a plane that passes through the center of the sphere.

**Physical significance**: This is why airplane routes often appear curved when plotted on flat maps (which use projections of the spherical Earth), but they actually follow the shortest possible paths on the Earth's surface.