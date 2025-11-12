---
layout: default
title: "Solutions to the Klein-Gordon Equation"
---

# Example Problems: Solutions to the Klein-Gordon Equation

This lecture is about finding and interpreting the solutions to the Klein-Gordon equation, which describes spin-0 particles.

## Problem 1: Plane Wave Solutions

The Klein-Gordon equation is $(\partial^\mu\partial_\mu + m^2)\phi = 0$. Let's look for plane wave solutions of the form $\phi(x) = A e^{-ip_\mu x^\mu}$.

a) Substitute this into the Klein-Gordon equation to find the condition on the four-momentum $p_\mu$.

b) The energy-momentum relation is $E^2 = p^2 + m^2$. This allows for both positive and negative energy solutions. What is the physical interpretation of the negative energy solutions?

### Solution 1

a) $\partial_\mu \phi = -ip_\mu \phi$. So $\partial^\mu\partial_\mu \phi = -p^\mu p_\mu \phi = -p^2 \phi$.
The equation becomes $(-p^2 + m^2)\phi = 0$. This requires $p^2 = m^2$, which is the relativistic energy-momentum relation.
$p^\mu p_\mu = E^2 - \vec{p}^2 = m^2$.

b) The negative energy solutions were initially problematic. The modern interpretation, due to Feynman and Stueckelberg, is that a negative energy particle moving forward in time is equivalent to a positive energy antiparticle moving backward in time. So the negative energy solutions describe antiparticles.

## Problem 2: Conserved Current

For a complex scalar field $\phi$, the Klein-Gordon equation has a conserved current associated with a U(1) global symmetry.
The current is $j_\mu = i(\phi^* \partial_\mu \phi - (\partial_\mu \phi^*)\phi)$.

a) Show that this current is conserved, i.e., $\partial^\mu j_\mu = 0$, using the Klein-Gordon equation for $\phi$ and $\phi^*$.

b) The conserved charge is $Q = \int j_0 d^3x$. Calculate the charge for a plane wave solution $\phi = A e^{-ipx}$.

### Solution 2

a) $\partial^\mu j_\mu = i(\partial^\mu\phi^* \partial_\mu\phi + \phi^* \partial^\mu\partial_\mu\phi - \partial^\mu\partial_\mu\phi^* \phi - \partial_\mu\phi^* \partial^\mu\phi) = i(\phi^*(-m^2\phi) - (-m^2\phi^*)\phi) = 0$.

b) $j_0 = i(\phi^* \partial_0 \phi - (\partial_0 \phi^*)\phi) = i(\phi^*(-iE)\phi - (iE\phi^*)\phi) = 2E|\phi|^2 = 2E|A|^2$.
$Q = \int 2E|A|^2 d^3x$. This is proportional to the energy and the probability density. For a single particle, we can normalize it to be the elementary charge.

