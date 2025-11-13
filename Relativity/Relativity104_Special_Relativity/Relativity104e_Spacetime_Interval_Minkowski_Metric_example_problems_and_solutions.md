# Relativity 104e: Spacetime Interval Minkowski Metric - Example Problems and Solutions

## Problem 1

What is the Minkowski metric? Write it down in matrix form.

### Solution 1

The Minkowski metric is a metric tensor used in special relativity. It describes the geometry of spacetime. In Cartesian coordinates, the Minkowski metric is:

$$\eta_{\mu\nu} = \begin{pmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}$$

(Note: the sign convention $(+,-,-,-)$ is also used).

## Problem 2

What is the spacetime interval? What are the three types of spacetime intervals?

### Solution 2

The spacetime interval $ds^2$ between two events is given by:
$$ds^2 = -c^2 dt^2 + dx^2 + dy^2 + dz^2$$

There are three types of spacetime intervals:

- $ds^2 < 0$: **timelike interval**. The two events can be causally connected.

- $ds^2 > 0$: **spacelike interval**. The two events cannot be causally connected.

- $ds^2 = 0$: **lightlike interval**. The two events can be connected by a light signal.

## Problem 3

Show that the spacetime interval is invariant under a Lorentz transformation.

### Solution 3

A Lorentz transformation is a linear transformation that preserves the spacetime interval. Let the coordinates in the new frame be $(t', x', y', z')$. The Lorentz transformation is given by:
$$t' = \gamma (t - vx/c^2)$$
$$x' = \gamma (x - vt)$$
$$y' = y$$
$$z' = z$$

where $\gamma = 1/\sqrt{1 - v^2/c^2}$.

We need to show that $ds'^2 = -c^2dt'^2 + dx'^2 + dy'^2 + dz'^2 = ds^2$.

$$dt' = \gamma (dt - vdx/c^2)$$
$$dx' = \gamma (dx - vdt)$$
$$dy' = dy$$
$$dz' = dz$$

$$ds'^2 = -c^2 \gamma^2 (dt - vdx/c^2)^2 + \gamma^2 (dx - vdt)^2 + dy^2 + dz^2$$

$$ds'^2 = -c^2 \gamma^2 \left(dt^2 - 2v\frac{dt \cdot dx}{c^2} + \frac{v^2dx^2}{c^4}\right) + \gamma^2 (dx^2 - 2vdx \cdot dt + v^2dt^2) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left(-c^2dt^2 + 2vdt \cdot dx - \frac{v^2dx^2}{c^2} + dx^2 - 2vdx \cdot dt + v^2dt^2\right) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left((-c^2 + v^2)dt^2 + \left(1 - \frac{v^2}{c^2}\right)dx^2\right) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left(-c^2\left(1 - \frac{v^2}{c^2}\right)dt^2 + \left(1 - \frac{v^2}{c^2}\right)dx^2\right) + dy^2 + dz^2$$

$$ds'^2 = \gamma^2 \left(1 - \frac{v^2}{c^2}\right) (-c^2dt^2 + dx^2) + dy^2 + dz^2$$

Since $\gamma^2 = 1/(1 - v^2/c^2)$, we have:
$$ds'^2 = -c^2dt^2 + dx^2 + dy^2 + dz^2 = ds^2$$