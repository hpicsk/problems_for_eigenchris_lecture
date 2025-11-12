# SfB 23: Klein-Gordon Solutions - Example Problems

The Klein-Gordon equation is the relativistic wave equation for a spin-0 particle.

## Problem 1: The Klein-Gordon Equation

The Klein-Gordon equation is $(\Box + m^2)\phi = 0$, where $\Box = \partial_\mu \partial^\mu = \frac{\partial^2}{\partial t^2} - \nabla^2$ (in natural units c=1, h_bar=1).

a) Look for plane wave solutions of the form $\phi(x) = N e^{-ip\cdot x} = N e^{-i(Et - \vec{p}\cdot\vec{x})}$.
   Substitute this into the Klein-Gordon equation and show that it leads to the energy-momentum relation $E^2 = p^2 + m^2$.
b) This relation allows for both positive and negative energy solutions ($E = \pm\sqrt{p^2+m^2}$). What was the historical problem with the negative energy solutions, and how was it eventually resolved?

## Problem 2: Conserved Current

The Klein-Gordon equation has a conserved current associated with it. The current is given by:
$j_\mu = i(\phi^* \partial_\mu \phi - \phi \partial_\mu \phi^*)$

a) Show that this current is conserved, i.e., $\partial^\mu j_\mu = 0$.
   (Hint: Use the Klein-Gordon equation for $\phi$ and its complex conjugate).
b) The zeroth component of the current, $j_0$, is interpreted as a probability density (or charge density).
   Calculate $j_0$ for a plane wave solution $\phi = N e^{-i(Et - \vec{p}\cdot\vec{x})}$.
c) For a negative energy solution, $E < 0$, what is the sign of the probability density $\rho = j_0$? What problem does this pose for interpreting $\rho$ as a probability density? (This is another historical issue with the KG equation).

## Problem 3: The Klein-Gordon Field

The modern interpretation of the Klein-Gordon equation is as a field equation. The field $\phi(x)$ is promoted to an operator, which can be expanded in terms of creation and annihilation operators:
$\phi(x) = \int \frac{d^3p}{(2\pi)^3} \frac{1}{\sqrt{2E_p}} (a_p e^{-ipx} + b_p^\dagger e^{ipx})$
Here, $a_p$ annihilates a particle with momentum p, and $b_p^\dagger$ creates an anti-particle with momentum p.

a) What is the role of the negative-frequency (positive exponent) solutions in this field expansion?
b) The canonical commutation relations for the field are $[[\phi(x), \pi(y)]] = i\delta(x-y)$, where $\pi = \dot{\phi}$ is the conjugate momentum. How does this lead to commutation relations for the creation and annihilation operators?
c) What is the vacuum state $|0\rangle$? How do you create a one-particle state from the vacuum?

## Problem 4: Interaction with Electromagnetism

The Klein-Gordon equation for a charged particle in an electromagnetic field is obtained by the minimal coupling prescription: $\partial_\mu \rightarrow D_\mu = \partial_\mu + iqA_\mu$.

a) Write down the Klein-Gordon equation with minimal coupling.
b) Consider a static, uniform magnetic field $B$ along the z-axis. What is a suitable vector potential $A_\mu$ for this field?
c) Look for solutions of the form $\phi(x,y,z,t) = e^{-iEt} e^{ik_z z} \psi(x,y)$. What is the equation for $\psi(x,y)$? Show that it is related to the problem of a quantum harmonic oscillator. The energy levels are the Landau levels for a scalar particle.

## Problem 5: Feynman Propagator

The Feynman propagator $D_F(x-y)$ is the Green's function for the Klein-Gordon equation.
$(\Box + m^2)D_F(x-y) = -i\delta^4(x-y)$

It can be expressed as a Fourier integral:
$D_F(x-y) = \int \frac{d^4p}{(2\pi)^4} \frac{i}{p^2 - m^2 + i\epsilon} e^{-ip\cdot(x-y)}$

a) The $i\epsilon$ prescription is crucial. Where are the poles of the integrand in the complex $p_0$ plane?
b) Explain how the $i\epsilon$ tells you how to deform the integration contour to handle these poles.
c) What is the physical meaning of the Feynman propagator? How is it related to the propagation of particles and anti-particles?

# Solutions to Example Problems: Klein-Gordon Equation and Solutions

## Problem 1: The Klein-Gordon Equation

a) **Substitute this into the Klein-Gordon equation and show that it leads to the energy-momentum relation $E^2 = p^2 + m^2$.**
This gives $(-E^2+p^2+m^2)\phi=0$, which implies the energy-momentum relation.

b) **What was the historical problem with the negative energy solutions, and how was it eventually resolved?**
The negative energy solutions seemed to imply that the system was unstable. This was resolved by reinterpreting the negative energy solutions as positive energy anti-particles.

## Problem 2: Conserved Current

a) **Show that this current is conserved, i.e., $\partial^\mu j_\mu = 0$.**
This follows from the Klein-Gordon equation and its complex conjugate.

b) **Calculate $j_0$ for a plane wave solution.**
$j_0 = 2E|N|^2$.

c) **For a negative energy solution, $E < 0$, what is the sign of the probability density $\rho = j_0$?**
The density is negative, which is a problem for a probability density.

## Problem 3: The Klein-Gordon Field

a) **What is the role of the negative-frequency (positive exponent) solutions in this field expansion?**
They are associated with the creation of anti-particles.

b) **How does this lead to commutation relations for the creation and annihilation operators?**
By inverting the Fourier expansion and applying the canonical commutation relations, one can derive the commutation relations for $a_p, b_p$.

c) **What is the vacuum state $|0\rangle$? How do you create a one-particle state from the vacuum?**
The vacuum state is annihilated by all annihilation operators. A one-particle state is created by acting on the vacuum with a creation operator.

## Problem 4: Interaction with Electromagnetism

a) **Write down the Klein-Gordon equation with minimal coupling.**
$(D_\mu D^\mu + m^2)\phi = 0$, where $D_\mu = \partial_\mu + iqA_\mu$.

b) **Consider a static, uniform magnetic field $B$ along the z-axis. What is a suitable vector potential $A_\mu$ for this field?**
$A_\mu = (0, -By/2, Bx/2, 0)$.

c) **What is the equation for $\psi(x,y)$?**
This leads to a 2D quantum harmonic oscillator problem, and the energy levels are the Landau levels.

## Problem 5: Feynman Propagator

The Feynman propagator $D_F(x-y)$ is the Green's function for the Klein-Gordon equation.
$(\Box + m^2)D_F(x-y) = -i\delta^4(x-y)$

It can be expressed as a Fourier integral:
$D_F(x-y) = \int \frac{d^4p}{(2\pi)^4} \frac{i}{p^2 - m^2 + i\epsilon} e^{-ip\cdot(x-y)}$

a) The $i\epsilon$ prescription is crucial. Where are the poles of the integrand in the complex $p_0$ plane?
b) Explain how the $i\epsilon$ tells you how to deform the integration contour to handle these poles.
c) What is the physical meaning of the Feynman propagator? How is it related to the propagation of particles and anti-particles?