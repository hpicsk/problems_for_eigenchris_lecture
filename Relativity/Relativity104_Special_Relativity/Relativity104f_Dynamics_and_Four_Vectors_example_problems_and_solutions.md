---
layout: default
title: "Dynamics and Four-Vectors"
---

# Dynamics and Four-Vectors - Problems and Solutions

## Problem 1

Define the four-velocity and four-momentum.

### Solution 1

The **four-velocity** is the four-vector that represents the velocity of a particle in spacetime. It is defined as:
$$U^\mu = \frac{dx^\mu}{d\tau}$$

where $\tau$ is the proper time.

$$U^\mu = (\gamma c, \gamma u_x, \gamma u_y, \gamma u_z)$$

where $\mathbf{u}$ is the ordinary velocity.

The **four-momentum** is the four-vector that represents the momentum of a particle in spacetime. It is defined as:
$$P^\mu = m U^\mu$$

where $m$ is the rest mass of the particle.

$$P^\mu = (\gamma mc, \gamma mu_x, \gamma mu_y, \gamma mu_z)$$

## Problem 2

What is the relationship between the four-momentum and the energy and momentum of a particle?

### Solution 2

The four-momentum is related to the energy and momentum of a particle as follows:
$$P^\mu = (E/c, p_x, p_y, p_z)$$

where:
- $E = \gamma mc^2$ is the energy of the particle
- $\mathbf{p} = \gamma m\mathbf{u}$ is the momentum of the particle

## Problem 3

Show that the square of the four-momentum is a Lorentz invariant. What is its value?

### Solution 3

The square of the four-momentum is:
$$P^\mu P_\mu = g_{\mu\nu} P^\mu P^\nu = -(E/c)^2 + p^2$$

We know that the energy-momentum relation is:
$$E^2 = (pc)^2 + (mc^2)^2$$

So:
$$(E/c)^2 = p^2 + (mc)^2$$

Therefore:
$$P^\mu P_\mu = -(p^2 + (mc)^2) + p^2 = -m^2c^2$$

The square of the four-momentum is a Lorentz invariant, and its value is $-m^2c^2$.