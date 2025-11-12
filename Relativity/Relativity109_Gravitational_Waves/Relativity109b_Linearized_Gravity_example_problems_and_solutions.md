# Relativity 109b: Linearized Gravity - Example Problems and Solutions

## Problem 1

What is linearized gravity? What are its assumptions?

## Solution 1

Linearized gravity is an approximation scheme in general relativity in which the spacetime metric is written as the sum of the Minkowski metric and a small perturbation: $g_{\mu\nu} = \eta_{\mu\nu} + h_{\mu\nu}$, where $|h_{\mu\nu}| \ll 1$. This approximation is valid in the weak field limit.

## Problem 2

Derive the linearized Einstein field equations.

## Solution 2

Starting from the Einstein field equations $R_{\mu\nu} - \frac{1}{2} g_{\mu\nu} R = \frac{8\pi G}{c^4} T_{\mu\nu}$, we expand the Ricci tensor and Ricci scalar in terms of $h_{\mu\nu}$ and keep only the terms that are linear in $h_{\mu\nu}$. This gives the linearized Einstein field equations:

$$\Box h_{\mu\nu} - \partial_\mu \partial^\alpha h_{\alpha\nu} - \partial_\nu \partial^\alpha h_{\mu\alpha} + \partial_\mu \partial_\nu h = -\frac{16\pi G}{c^4} T_{\mu\nu}$$

where $h = h^\alpha_\alpha$ is the trace of the perturbation.

## Problem 3

Show that in linearized gravity, the metric perturbation $h_{\mu\nu}$ satisfies a wave equation.

## Solution 3

In vacuum, $T_{\mu\nu} = 0$. The linearized Einstein field equations become:

$$\Box h_{\mu\nu} - \partial_\mu \partial^\alpha h_{\alpha\nu} - \partial_\nu \partial^\alpha h_{\mu\alpha} + \partial_\mu \partial_\nu h = 0$$

By choosing the Lorentz gauge $\partial^\alpha h_{\alpha\nu} = \frac{1}{2} \partial_\nu h$, the equations simplify to:

$$\Box h_{\mu\nu} = 0$$

This is a wave equation for the metric perturbation $h_{\mu\nu}$.