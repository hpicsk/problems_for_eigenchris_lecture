# Example Problems: Proca Equation and Solutions

The Proca equation describes a massive spin-1 particle. It can be seen as a generalization of the Maxwell equations.

## Problem 1: The Proca Equation

The Proca equation is written in terms of the 4-vector potential $A^\mu$ and the field strength tensor $F^{\mu\nu} = \partial^\mu A^\nu - \partial^\nu A^\mu$.
The equations are:
$\partial_\mu F^{\mu\nu} + m^2 A^\nu = 0$
(where we set $\hbar=c=1$)

a) Show that taking the divergence of this equation ($\partial_\nu$) implies the Lorenz condition $\partial_\mu A^\mu = 0$.
b) Using the Lorenz condition, show that the Proca equation can be rewritten as a Klein-Gordon equation for each component of $A^\mu$:
$(\Box + m^2)A^\mu = 0$

## Problem 2: Plane Wave Solutions

We look for plane wave solutions of the form $A^\mu(x) = \epsilon^\mu e^{-ip\cdot x}$, where $\epsilon^\mu$ is the polarization vector and $p^\mu$ is the 4-momentum.

a) Substitute this into the Klein-Gordon form of the equation from Problem 1b. What condition does this impose on the 4-momentum $p^\mu$?
b) What condition does the Lorenz gauge $\partial_\mu A^\mu = 0$ impose on the relationship between the polarization vector $\epsilon^\mu$ and the momentum $p^\mu$?

## Problem 3: Degrees of Freedom

For a massive vector boson, we expect 3 degrees of freedom (3 spin states).
The polarization vector $\epsilon^\mu$ is a 4-component vector. The condition $p_\mu \epsilon^\mu = 0$ reduces the number of independent components.

Let's work in the rest frame of the particle, where $p^\mu = (m, 0, 0, 0)$.
a) What does the condition $p_\mu \epsilon^\mu = 0$ imply about the component $\epsilon^0$?
b) This leaves three independent components for $\epsilon^i$ (i=1,2,3). We can choose a basis for these three polarization vectors. A standard choice is:
$\epsilon^\mu(1) = (0, 1, 0, 0)$
$\epsilon^\mu(2) = (0, 0, 1, 0)$
$\epsilon^\mu(3) = (0, 0, 0, 1)$
These are the three spin states of the massive vector boson. What are the spin projections along the z-axis for these states? (Hint: think about the angular momentum operator).

## Problem 4: Comparison with Electromagnetism

In the case of electromagnetism, the photon is massless (m=0).
The Maxwell equations in vacuum are $\partial_\mu F^{\mu\nu} = 0$.
This theory has a gauge invariance: $A^\mu \rightarrow A^\mu + \partial^\mu \Lambda$.

a) Show that the Proca equation is NOT invariant under this gauge transformation if $m \neq 0$. This is often summarized as "the Proca mass term breaks gauge invariance".
b) For the massless photon, the condition $p_\mu \epsilon^\mu = 0$ is not sufficient to reduce the degrees of freedom to 2 (the two transverse polarizations). The extra gauge freedom is needed to eliminate one more degree of freedom.
   Explain how the gauge freedom allows us to set $\epsilon^0=0$ and also impose a condition on the spatial components.

## Problem 5: Non-relativistic limit

Consider the Proca field in the non-relativistic limit.
The energy is dominated by the rest mass, $E \approx m$.
The field oscillates very rapidly with frequency $\omega \approx m$.

How do the equations of motion for the spatial components of the Proca field behave in this limit?
Show that they resemble the Schrodinger equation.

# Solutions to Example Problems: Proca Equation and Solutions

## Problem 1: The Proca Equation

a) **Show that taking the divergence of this equation implies the Lorenz condition $\partial_\mu A^\mu = 0$.**
$\partial_\nu(\partial_\mu F^{\mu\nu} + m^2 A^\nu) = 0$. Since $\partial_\nu\partial_\mu$ is symmetric and $F^{\mu\nu}$ is antisymmetric, the first term is zero. So $m^2 \partial_\nu A^\nu = 0$, which implies $\partial_\nu A^\nu = 0$ for $m\neq 0$.

b) **Using the Lorenz condition, show that the Proca equation can be rewritten as a Klein-Gordon equation.**
$\partial_\mu F^{\mu\nu} + m^2 A^\nu = \Box A^\nu - \partial^\nu(\partial_\mu A^\mu) + m^2 A^\nu = 0$. With the Lorenz condition, this becomes $(\Box + m^2)A^\nu = 0$.

## Problem 2: Plane Wave Solutions

a) **What condition does this impose on the 4-momentum $p^\mu$?**
$p^2 = m^2$.

b) **What condition does the Lorenz gauge $\partial_\mu A^\mu = 0$ impose on the relationship between the polarization vector $\epsilon^\mu$ and the momentum $p^\mu$?**
$p_\mu \epsilon^\mu = 0$.

## Problem 3: Degrees of Freedom

a) **What does the condition $p_\mu \epsilon^\mu = 0$ imply about the component $\epsilon^0$?**
In the rest frame, $p^\mu=(m,0,0,0)$, so $\epsilon^0=0$.

b) **What are the spin projections along the z-axis for these states?**
The three polarization vectors correspond to the three projections of a spin-1 particle: +1, -1, and 0.

## Problem 4: Comparison with Electromagnetism

a) **Show that the Proca equation is NOT invariant under this gauge transformation if $m \neq 0$.**
The mass term $m^2 A^\nu$ is not gauge invariant.

b) **Explain how the gauge freedom allows us to set $\epsilon^0=0$ and also impose a condition on the spatial components.**
For a massless photon, we have the gauge freedom $\epsilon^\mu \to \epsilon^\mu + \alpha p^\mu$. We can choose $\alpha$ to eliminate one component of $\epsilon^\mu$. For example, we can set $\epsilon^0=0$. Then the condition $p_\mu\epsilon^\mu=0$ becomes $\vec{p}\cdot\vec{\epsilon}=0$, which means the polarization is transverse. This leaves 2 degrees of freedom.

## Problem 5: Non-relativistic limit

In the non-relativistic limit, the spatial components of the Proca field can be shown to satisfy a Schrodinger-like equation.