## Problem 1

Calculate the Jacobian of the transformation from Cartesian coordinates to polar coordinates.

### Solution 1

The transformation is:
$$x = r \cos(\theta)$$
$$y = r \sin(\theta)$$

The Jacobian matrix is:
$$J = \begin{pmatrix}
\frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} \\
\frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta}
\end{pmatrix} = \begin{pmatrix}
\cos(\theta) & -r \sin(\theta) \\
\sin(\theta) & r \cos(\theta)
\end{pmatrix}$$

The Jacobian determinant is:
$$\det(J) = r \cos^2(\theta) + r \sin^2(\theta) = r(\cos^2(\theta) + \sin^2(\theta)) = r$$

## Problem 2

Calculate the Jacobian of the Lorentz transformation.

### Solution 2

The Lorentz transformation is:
$$t' = \gamma \left(t - \frac{vx}{c^2}\right)$$
$$x' = \gamma (x - vt)$$

where $\gamma = \frac{1}{\sqrt{1-v^2/c^2}}$.

The Jacobian matrix is:
$$J = \begin{pmatrix}
\frac{\partial t'}{\partial t} & \frac{\partial t'}{\partial x} \\
\frac{\partial x'}{\partial t} & \frac{\partial x'}{\partial x}
\end{pmatrix} = \begin{pmatrix}
\gamma & -\frac{\gamma v}{c^2} \\
-\gamma v & \gamma
\end{pmatrix}$$

The Jacobian determinant is:
$$\det(J) = \gamma^2 - \gamma^2 \frac{v^2}{c^2} = \gamma^2\left(1 - \frac{v^2}{c^2}\right) = \gamma^2 \cdot \frac{1}{\gamma^2} = 1$$

## Problem 3

How is the Jacobian used to transform volume elements?

### Solution 3

The volume element transforms according to:
$$d^n x' = |\det(J)| \, d^n x$$

where $\det(J)$ is the Jacobian determinant and $n$ is the number of dimensions.

For example:
- In 2D: $dx' dy' = |\det(J)| \, dx \, dy$
- In 3D: $dx' dy' dz' = |\det(J)| \, dx \, dy \, dz$

The absolute value ensures that the volume element remains positive even if the transformation involves reflection (negative determinant).