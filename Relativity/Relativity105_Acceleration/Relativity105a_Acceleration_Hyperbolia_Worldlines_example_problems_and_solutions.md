# Acceleration and Hyperbolic Worldlines - Problems and Solutions

## Problem 1

A particle starts from rest and moves with a constant proper acceleration $a$. Find the equation of its worldline.

### Solution 1

The four-acceleration is $A^{\mu} = \frac{dU^{\mu}}{d\tau} = (0, a, 0, 0)$ in the instantaneous rest frame.

In a general frame, the equations of motion are:
$$\frac{dU^0}{d\tau} = \frac{a}{c} U^1$$
$$\frac{dU^1}{d\tau} = \frac{a}{c} U^0$$

The solution is:
$$U^0(\tau) = c \cosh\left(\frac{a\tau}{c}\right)$$
$$U^1(\tau) = c \sinh\left(\frac{a\tau}{c}\right)$$

Integrating with respect to $\tau$, we get the worldline:
$$ct(\tau) = \frac{c^2}{a} \sinh\left(\frac{a\tau}{c}\right)$$
$$x(\tau) = \frac{c^2}{a} \cosh\left(\frac{a\tau}{c}\right)$$

## Problem 2

Show that the worldline of a uniformly accelerated observer is a hyperbola in a spacetime diagram.

### Solution 2

From the previous problem, we have:
$$x(\tau) = \frac{c^2}{a} \cosh\left(\frac{a\tau}{c}\right)$$
$$ct(\tau) = \frac{c^2}{a} \sinh\left(\frac{a\tau}{c}\right)$$

Using the hyperbolic identity $\cosh^2(u) - \sinh^2(u) = 1$:
$$x^2 - (ct)^2 = \left(\frac{c^2}{a}\right)^2 \left(\cosh^2\left(\frac{a\tau}{c}\right) - \sinh^2\left(\frac{a\tau}{c}\right)\right) = \left(\frac{c^2}{a}\right)^2$$

This is the equation of a hyperbola in the $(ct, x)$ spacetime diagram.

## Problem 3

What is the relationship between the proper acceleration and the coordinate acceleration?

### Solution 3

The proper acceleration $a$ is the acceleration measured in the instantaneous rest frame of the particle. The coordinate acceleration $\alpha$ is the acceleration measured by a stationary observer.

The relationship is:
$$\alpha = \frac{a}{\gamma^3}$$

where $\gamma = \frac{1}{\sqrt{1-v^2/c^2}}$ is the Lorentz factor.