---
layout: default
title: "Invariance"
---

# Invariance - Example Problems and Solutions

## Problem 1

The spacetime interval is given by the equation $ds^2 = -c^2dt^2 + dx^2 + dy^2 + dz^2$. Show that the spacetime interval is invariant under a Lorentz transformation.

## Solution 1

A Lorentz transformation is a linear transformation that preserves the spacetime interval. Let the coordinates in the new frame be $(t', x', y', z')$. The Lorentz transformation is given by:

$$t' = \gamma \left(t - \frac{vx}{c^2}\right)$$
$$x' = \gamma (x - vt)$$
$$y' = y$$
$$z' = z$$

where $\gamma = \frac{1}{\sqrt{1 - v^2/c^2}}$.

We need to show that $ds'^2 = -c^2dt'^2 + dx'^2 + dy'^2 + dz'^2 = ds^2$.

Taking the differentials:
$$dt' = \gamma \left(dt - \frac{v dx}{c^2}\right)$$
$$dx' = \gamma (dx - v dt)$$
$$dy' = dy$$
$$dz' = dz$$

Substituting into the spacetime interval:
$$ds'^2 = -c^2 \gamma^2 \left(dt - \frac{v dx}{c^2}\right)^2 + \gamma^2 (dx - v dt)^2 + dy^2 + dz^2$$

Expanding the squared terms:
$$ds'^2 = -c^2 \gamma^2 \left(dt^2 - \frac{2v dt \cdot dx}{c^2} + \frac{v^2 dx^2}{c^4}\right) + \gamma^2 (dx^2 - 2v dx \cdot dt + v^2 dt^2) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left(-c^2 dt^2 + 2v dt \cdot dx - \frac{v^2 dx^2}{c^2} + dx^2 - 2v dx \cdot dt + v^2 dt^2\right) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left((-c^2 + v^2)dt^2 + \left(1 - \frac{v^2}{c^2}\right)dx^2\right) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left(-c^2\left(1 - \frac{v^2}{c^2}\right)dt^2 + \left(1 - \frac{v^2}{c^2}\right)dx^2\right) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left(1 - \frac{v^2}{c^2}\right) (-c^2 dt^2 + dx^2) + dy^2 + dz^2$$

Since $\gamma^2 = \frac{1}{1 - v^2/c^2}$, we have:
$$ds'^2 = -c^2 dt^2 + dx^2 + dy^2 + dz^2 = ds^2$$

Therefore, the spacetime interval is invariant under Lorentz transformations.

## Problem 2

The phase of a plane wave is given by $\phi = kx - \omega t$. Show that the phase of a plane wave is a Lorentz invariant.

## Solution 2

The phase of a plane wave can be written as $\phi = k_\mu x^\mu$, where $k_\mu$ is the four-wavevector and $x^\mu$ is the four-position vector.

The four-wavevector is:
$$k_\mu = \left(-\frac{\omega}{c}, k_x, k_y, k_z\right)$$

The four-position vector is:
$$x^\mu = (ct, x, y, z)$$

Therefore:
$$\phi = k_\mu x^\mu = -\frac{\omega}{c} \cdot ct + k_x \cdot x + k_y \cdot y + k_z \cdot z = -\omega t + k_x x + k_y y + k_z z$$

Under a Lorentz transformation, both $k_\mu$ and $x^\mu$ transform as four-vectors. The contraction $k_\mu x^\mu$ is a scalar product between a covariant four-vector and a contravariant four-vector, which is a Lorentz scalar (invariant).

Therefore, the phase $\phi = k_\mu x^\mu$ is a Lorentz invariant.

## Problem 3

Consider the electromagnetic field tensor $F_{\mu\nu}$. The electromagnetic Lagrangian is given by $\mathcal{L} = -\frac{1}{4} F_{\mu\nu} F^{\mu\nu}$. Show that the Lagrangian is a Lorentz invariant.

## Solution 3

The electromagnetic field tensor $F_{\mu\nu}$ transforms as a tensor under a Lorentz transformation:
$$F'_{\mu\nu} = \Lambda_\mu^{\phantom{\mu}\alpha} \Lambda_\nu^{\phantom{\nu}\beta} F_{\alpha\beta}$$

where $\Lambda_\mu^{\phantom{\mu}\alpha}$ are the components of the Lorentz transformation matrix.

The Lagrangian is:
$$\mathcal{L} = -\frac{1}{4} F_{\mu\nu} F^{\mu\nu} = -\frac{1}{4} F_{\mu\nu} g^{\mu\alpha} g^{\nu\beta} F_{\alpha\beta}$$

Under a Lorentz transformation, the metric tensor $g^{\mu\nu}$ is invariant, and we have:
$$\mathcal{L}' = -\frac{1}{4} F'_{\mu\nu} F'^{\mu\nu}$$

$$= -\frac{1}{4} \left(\Lambda_\mu^{\phantom{\mu}\alpha} \Lambda_\nu^{\phantom{\nu}\beta} F_{\alpha\beta}\right) \left(\Lambda^{\mu}_{\phantom{\mu}\gamma} \Lambda^{\nu}_{\phantom{\nu}\delta} F^{\gamma\delta}\right)$$

$$= -\frac{1}{4} \left(\Lambda_\mu^{\phantom{\mu}\alpha} \Lambda^{\mu}_{\phantom{\mu}\gamma}\right) \left(\Lambda_\nu^{\phantom{\nu}\beta} \Lambda^{\nu}_{\phantom{\nu}\delta}\right) F_{\alpha\beta} F^{\gamma\delta}$$

Since $\Lambda_\mu^{\phantom{\mu}\alpha} \Lambda^{\mu}_{\phantom{\mu}\gamma} = \delta^\alpha_\gamma$, we have:
$$\mathcal{L}' = -\frac{1}{4} \delta^\alpha_\gamma \delta^\beta_\delta F_{\alpha\beta} F^{\gamma\delta} = -\frac{1}{4} F_{\alpha\beta} F^{\alpha\beta} = \mathcal{L}$$

Therefore, the electromagnetic Lagrangian is a Lorentz invariant.