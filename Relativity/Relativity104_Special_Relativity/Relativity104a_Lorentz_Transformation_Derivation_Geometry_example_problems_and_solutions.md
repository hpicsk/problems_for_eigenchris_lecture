# Lorentz Transformation Derivation Geometry - Problems and Solutions

## Problem 1

Using a spacetime diagram, derive the Lorentz transformations for a boost in the x-direction.

### Solution 1

Consider a spacetime diagram with coordinates $(ct, x)$. The worldline of a particle moving with velocity $v$ is a line with slope $c/v$. The axes of a moving frame $(ct', x')$ are tilted with respect to the $(ct, x)$ axes. The $ct'$ axis is the worldline of the origin of the moving frame, so it has a slope of $c/v$. The $x'$ axis is the line of simultaneous events for an observer in the moving frame. It can be shown that the $x'$ axis has a slope of $v/c$. By projecting a point $(ct, x)$ onto the tilted axes, we can derive the Lorentz transformations.

## Problem 2

Show that the Lorentz transformation can be represented as a rotation in spacetime.

### Solution 2

A rotation in Euclidean space is given by:
$$x' = x \cos(\theta) + y \sin(\theta)$$
$$y' = -x \sin(\theta) + y \cos(\theta)$$

This transformation preserves the quantity $x^2 + y^2$.

A Lorentz transformation is given by:
$$x' = \gamma (x - vt)$$
$$t' = \gamma (t - vx/c^2)$$

This transformation preserves the spacetime interval $s^2 = -c^2t^2 + x^2$.

If we make the substitution $ict = w$, the spacetime interval becomes $x^2 + w^2$, which is analogous to the Euclidean distance. The Lorentz transformation can then be written as a rotation in the $(x, w)$ plane. This is called a Wick rotation.

## Problem 3

What is the rapidity? How is it related to the velocity?

### Solution 3

The rapidity $\phi$ is defined as $\tanh(\phi) = v/c$.

The Lorentz transformation can be written in terms of the rapidity as:
$$x' = x \cosh(\phi) - ct \sinh(\phi)$$
$$ct' = -x \sinh(\phi) + ct \cosh(\phi)$$

This is a hyperbolic rotation. The rapidity is useful because it is additive under successive Lorentz transformations. If a frame $S'$ moves with rapidity $\phi_1$ with respect to $S$, and a frame $S''$ moves with rapidity $\phi_2$ with respect to $S'$, then the rapidity of $S''$ with respect to $S$ is $\phi = \phi_1 + \phi_2$.