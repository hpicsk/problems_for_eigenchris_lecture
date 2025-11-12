
This lecture deals with the Proca equation, which describes massive spin-1 particles (vector bosons).

## Problem 1: The Proca Equation

The Proca equation for a vector field $A_\mu$ is $\partial_\mu F^{\mu\nu} + m^2 A^\nu = 0$, where $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu$.

a) Show that the Proca equation implies the Lorenz condition $\partial_\mu A^\mu = 0$.

b) Using the Lorenz condition, show that the Proca equation can be written as $(\partial^2 + m^2)A^\nu = 0$. This means each component of the field satisfies the Klein-Gordon equation.

### Solution 1

a) Take the divergence of the Proca equation: $\partial_\nu(\partial_\mu F^{\mu\nu} + m^2 A^\nu) = 0$.
$\partial_\nu\partial_\mu F^{\mu\nu} + m^2 \partial_\nu A^\nu = 0$.
Since $F^{\mu\nu}$ is antisymmetric, $\partial_\nu\partial_\mu F^{\mu\nu} = 0$. So we are left with $m^2 \partial_\nu A^\nu = 0$. If $m \neq 0$, this implies $\partial_\nu A^\nu = 0$.

b) $\partial_\mu F^{\mu\nu} = \partial_\mu(\partial^\mu A^\nu - \partial^\nu A^\mu) = \partial^2 A^\nu - \partial^\nu(\partial_\mu A^\mu)$.
Using the Lorenz condition $\partial_\mu A^\mu = 0$, this becomes $\partial^2 A^\nu$.
So the Proca equation becomes $\partial^2 A^\nu + m^2 A^\nu = 0$.

## Problem 2: Plane Wave Solutions and Polarization

Let's look for plane wave solutions of the form $A_\mu(x) = \epsilon_\mu e^{-ipx}$, where $\epsilon_\mu$ is the polarization vector.

a) What conditions does the Proca equation impose on the polarization vector $\epsilon_\mu$ and the momentum $p_\mu$?

b) How many independent polarization states are there for a massive vector boson? (Hint: work in the rest frame of the particle).

### Solution 2

a) From Problem 1, we know that $p^2=m^2$ and $\partial_\mu A^\mu = 0$. The second condition translates to $-ip_\mu \epsilon^\mu = 0$, so $p \cdot \epsilon = 0$.

b) In the rest frame, the momentum is $p = (m, 0, 0, 0)$. The condition $p \cdot \epsilon = 0$ becomes $m \epsilon_0 = 0$, so $\epsilon_0=0$.
This leaves the 3 spatial components of $\epsilon$. So there are 3 independent polarization states. These can be chosen to be the three orthonormal vectors in 3D space, e.g., $(0,1,0,0), (0,0,1,0), (0,0,0,1)$. These correspond to the three possible spin projections of a spin-1 particle.

