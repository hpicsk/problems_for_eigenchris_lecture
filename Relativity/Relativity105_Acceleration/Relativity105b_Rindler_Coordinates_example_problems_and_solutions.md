## Problem 1

Write down the transformation from Minkowski coordinates to Rindler coordinates.

### Solution 1

The transformation from Minkowski coordinates $(t, x)$ to Rindler coordinates $(\eta, \rho)$ is:
$$t = \frac{\rho}{g} \sinh(g\eta)$$
$$x = \frac{\rho}{g} \cosh(g\eta)$$

where $g$ is the constant proper acceleration.

## Problem 2

What is the Rindler horizon? What is its physical significance?

### Solution 2

The Rindler horizon is the boundary of the region of spacetime that can be observed by a Rindler observer. It is located at $x = |t|c$. 

Events behind the Rindler horizon cannot influence the Rindler observer. The Rindler horizon is an event horizon - it represents the causal boundary beyond which events cannot communicate with the accelerated observer.

## Problem 3

Calculate the metric tensor in Rindler coordinates.

### Solution 3

Starting with the coordinate transformations:
$$dt = \frac{1}{g} \sinh(g\eta) d\rho + \rho \cosh(g\eta) d\eta$$
$$dx = \frac{1}{g} \cosh(g\eta) d\rho + \rho \sinh(g\eta) d\eta$$

The line element in Minkowski coordinates is:
$$ds^2 = -c^2 dt^2 + dx^2$$

Substituting the coordinate differentials:
$$ds^2 = -c^2 \left[\frac{1}{g^2} \sinh^2(g\eta) d\rho^2 + \frac{2\rho}{g} \sinh(g\eta)\cosh(g\eta) d\rho d\eta + \rho^2 \cosh^2(g\eta) d\eta^2\right]$$
$$+ \left[\frac{1}{g^2} \cosh^2(g\eta) d\rho^2 + \frac{2\rho}{g} \sinh(g\eta)\cosh(g\eta) d\rho d\eta + \rho^2 \sinh^2(g\eta) d\eta^2\right]$$

Simplifying (assuming $g = c = 1$ for convenience):
$$ds^2 = \left(\cosh^2(\eta) - \sinh^2(\eta)\right) d\rho^2 + \rho^2\left(\sinh^2(\eta) - \cosh^2(\eta)\right) d\eta^2$$

Using the identity $\cosh^2(\eta) - \sinh^2(\eta) = 1$:
$$ds^2 = d\rho^2 - \rho^2 d\eta^2$$