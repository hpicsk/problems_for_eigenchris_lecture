# Relativity 106a: Covectors Doppler Effect - Example Problems and Solutions

## Problem 1

What is a covector? How is it different from a vector?

### Solution 1

A covector, or a one-form, is a linear map from the vector space to the field of scalars. A vector is an element of a vector space. In a space with a metric, there is a natural isomorphism between vectors and covectors. A covector transforms differently from a vector under a change of basis. A vector transforms contravariantly, while a covector transforms covariantly.

## Problem 2

The frequency of a light wave is given by the covector $k_u$. How is this related to the wave vector $k^u$?

### Solution 2

The wave covector $k_u$ is related to the wave vector $k^u$ by the metric tensor:
$$k_u = g_{uv} k^v$$

In special relativity, with the Minkowski metric $\eta_{uv} = \text{diag}(-1, 1, 1, 1)$, we have:
$$k_0 = -k^0 = -\frac{\omega}{c}$$
$$k_i = k^i \quad \text{for } i = 1, 2, 3$$

So, $k_u = \left(-\frac{\omega}{c}, k_x, k_y, k_z\right)$.

## Problem 3

Derive the relativistic Doppler effect using the covector formalism.

### Solution 3

The frequency of a light wave as measured by an observer with four-velocity $U^u$ is:
$$\omega = -k_u U^u$$

Consider a source emitting light with frequency $\omega_s$ and an observer moving with velocity $v$ with respect to the source.

The four-velocity of the source is:
$$U_s^u = (c, 0, 0, 0)$$

The four-velocity of the observer is:
$$U_o^u = \gamma (c, v, 0, 0)$$

The wave covector is:
$$k_u = \left(-\frac{\omega_s}{c}, k_x, k_y, k_z\right)$$

The frequency measured by the observer is:
$$\omega_o = -k_u U_o^u = -\left(-\frac{\omega_s}{c} \cdot \gamma c + k_x \cdot \gamma v\right) = \gamma (\omega_s - v k_x)$$

For light propagating in the $x$-direction, $k_x = \frac{\omega_s}{c}$.

Therefore:
$$\omega_o = \gamma \left(\omega_s - v \cdot \frac{\omega_s}{c}\right) = \gamma \omega_s \left(1 - \frac{v}{c}\right)$$

Using the identity $\gamma = \frac{1}{\sqrt{1-v^2/c^2}}$ and simplifying:
$$\omega_o = \omega_s \sqrt{\frac{1-v/c}{1+v/c}}$$

This is the relativistic Doppler effect formula.