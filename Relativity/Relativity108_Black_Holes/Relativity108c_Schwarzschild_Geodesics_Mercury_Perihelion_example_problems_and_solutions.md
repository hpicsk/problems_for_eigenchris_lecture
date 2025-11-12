# Relativity 108c: Schwarzschild Geodesics Mercury Perihelion - Example Problems and Solutions

## Problem 1

Derive the geodesic equations for the Schwarzschild metric.

## Solution 1

The geodesic equations can be derived from the Euler-Lagrange equations for the Lagrangian $\mathcal{L} = g_{\mu\nu} \frac{dx^\mu}{d\tau} \frac{dx^\nu}{d\tau}$.

For the Schwarzschild metric, the geodesic equations are:

$$\frac{d}{d\tau} \left[\left(1 - \frac{2GM}{rc^2}\right) \frac{dt}{d\tau}\right] = 0$$

$$\frac{d}{d\tau} \left(r^2 \frac{d\phi}{d\tau}\right) = 0$$

$$\frac{d^2r}{d\tau^2} + \frac{GM}{r^2} - \frac{L^2}{r^3} + \frac{3GM L^2}{c^2 r^4} = 0$$

where $L$ is the angular momentum.

## Problem 2

Calculate the perihelion precession of Mercury using the Schwarzschild metric.

## Solution 2

The perihelion precession of Mercury can be calculated from the geodesic equations. The result is:

$$\Delta\phi = \frac{6\pi GM}{c^2 a (1 - e^2)}$$

where $a$ is the semi-major axis and $e$ is the eccentricity of Mercury's orbit. This result agrees with the observed value.

## Problem 3

What is the effective potential for a particle moving in the Schwarzschild metric?

## Solution 3

The effective potential for a particle moving in the Schwarzschild metric is:

$$V(r) = -\frac{GM}{r} + \frac{L^2}{2r^2} - \frac{GM L^2}{c^2 r^3}$$

The first term is the Newtonian gravitational potential, the second term is the centrifugal barrier, and the third term is a general relativistic correction.