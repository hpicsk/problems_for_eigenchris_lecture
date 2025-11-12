# SfB 22: Dirac Equation and Gamma Matrices - Example Problems and Solutions


This lecture introduces the Dirac equation, a relativistic wave equation for spin-1/2 particles, and the gamma matrices that are central to it.

## Problem 1: The Dirac Equation

The Dirac equation is $(i\gamma^\mu \partial_\mu - m)\psi = 0$. The gamma matrices satisfy the Clifford algebra relation $\{\gamma^\mu, \gamma^\nu\} = 2\eta^{\mu\nu}$.

a) Show that if $\psi$ is a solution to the Dirac equation, it is also a solution to the Klein-Gordon equation, $(\partial^\mu\partial_\mu + m^2)\psi = 0$.

b) The Dirac adjoint is defined as $\bar{\psi} = \psi^\dagger \gamma^0$. Show that the Dirac adjoint satisfies the equation $i\partial_\mu \bar{\psi} \gamma^\mu + m\bar{\psi} = 0$.

c) From the Dirac equation and its adjoint, show that the current $j^\mu = \bar{\psi}\gamma^\mu\psi$ is conserved, i.e., $\partial_\mu j^\mu = 0$.

### Solution 1

a) Act on the Dirac equation with $(i\gamma^\nu \partial_\nu + m)$ from the left:
$(i\gamma^\nu \partial_\nu + m)(i\gamma^\mu \partial_\mu - m)\psi = (-\gamma^\nu\gamma^\mu \partial_\nu\partial_\mu - m^2)\psi = 0$.
$-\gamma^\nu\gamma^\mu \partial_\nu\partial_\mu = -\frac{1}{2}(\gamma^\nu\gamma^\mu + \gamma^\mu\gamma^\nu)\partial_\nu\partial_\mu = -\frac{1}{2}\{\gamma^\nu, \gamma^\mu\}\partial_\nu\partial_\mu = -\eta^{\mu\nu}\partial_\mu\partial_\nu = -\partial^\mu\partial_\mu$.
So we have $(-\partial^\mu\partial_\mu - m^2)\psi = 0$, which is the Klein-Gordon equation.

b) The Dirac adjoint is defined as $\bar{\psi} = \psi^\dagger \gamma^0$. Show that the Dirac adjoint satisfies the equation $i\partial_\mu \bar{\psi} \gamma^\mu + m\bar{\psi} = 0$.
Start with the Dirac equation: $(i\gamma^\mu \partial_\mu - m)\psi = 0$.
Take the Hermitian conjugate: $(i\gamma^\mu \partial_\mu - m)^\dagger \psi^\dagger = 0 \implies (-i(\gamma^\mu)^\dagger \partial_\mu - m)\psi^\dagger = 0$.
Multiply by $\gamma^0$ from the right: $(-i\partial_\mu \psi^\dagger (\gamma^\mu)^\dagger \gamma^0 - m\psi^\dagger\gamma^0) = 0$.
Use the property $(\gamma^\mu)^\dagger = \gamma^0 \gamma^\mu \gamma^0$:
$-i\partial_\mu \psi^\dagger \gamma^0 \gamma^\mu \gamma^0 \gamma^0 - m\bar{\psi} = 0$.
Since $(\gamma^0)^2=I$ and $\bar{\psi}=\psi^\dagger\gamma^0$, this becomes:
$-i\partial_\mu \bar{\psi} \gamma^\mu - m\bar{\psi} = 0$, which is equivalent to $i\partial_\mu \bar{\psi} \gamma^\mu + m\bar{\psi} = 0$.

c) From the Dirac equation and its adjoint, show that the current $j^\mu = \bar{\psi}\gamma^\mu\psi$ is conserved, i.e., $\partial_\mu j^\mu = 0$.
$\partial_\mu j^\mu = \partial_\mu (\bar{\psi}\gamma^\mu\psi) = (\partial_\mu \bar{\psi})\gamma^\mu\psi + \bar{\psi}\gamma^\mu(\partial_\mu \psi)$.
From the Dirac equation, $i\gamma^\mu\partial_\mu\psi = m\psi$, so $\gamma^\mu\partial_\mu\psi = -im\psi$.
From the adjoint Dirac equation, $i\partial_\mu\bar{\psi}\gamma^\mu = -m\bar{\psi}$, so $(\partial_\mu\bar{\psi})\gamma^\mu = im\bar{\psi}$.
Substituting these into the expression for $\partial_\mu j^\mu$:
$\partial_\mu j^\mu = (im\bar{\psi})\psi + \bar{\psi}(-im\psi) = im\bar{\psi}\psi - im\bar{\psi}\psi = 0$.

## Problem 2: Chiral representation of gamma matrices

In the chiral (or Weyl) representation, the gamma matrices are:
$\gamma^0 = \begin{pmatrix} 0 & I \\ I & 0 \end{pmatrix}$, $\gamma^i = \begin{pmatrix} 0 & \sigma^i \\ -\sigma^i & 0 \end{pmatrix}$.
Also, $\gamma^5 = i\gamma^0\gamma^1\gamma^2\gamma^3 = \begin{pmatrix} -I & 0 \\ 0 & I \end{pmatrix}$.

a) Show that these matrices satisfy the Clifford algebra.

b) The projectors onto left-handed and right-handed components are $P_L = \frac{1}{2}(1-\gamma^5)$ and $P_R = \frac{1}{2}(1+\gamma^5)$.
Let $\psi = \begin{pmatrix} \psi_L \\ \psi_R \end{pmatrix}$ where $\psi_L, \psi_R$ are 2-component spinors. Show that $P_L \psi = \begin{pmatrix} \psi_L \\ 0 \end{pmatrix}$ and $P_R \psi = \begin{pmatrix} 0 \\ \psi_R \end{pmatrix}$.

c) Write the Dirac equation in terms of $\psi_L$ and $\psi_R$. Show that for a massless particle (m=0), the equations for left and right handed spinors decouple.

### Solution 2

a) This is a matter of matrix multiplication. For example, $(\gamma^0)^2 = \begin{pmatrix} 0 & I \\ I & 0 \end{pmatrix}\begin{pmatrix} 0 & I \\ I & 0 \end{pmatrix} = \begin{pmatrix} I & 0 \\ 0 & I \end{pmatrix} = I = \eta^{00}$.
$(\gamma^1)^2 = \begin{pmatrix} 0 & \sigma^1 \\ -\sigma^1 & 0 \end{pmatrix}\begin{pmatrix} 0 & \sigma^1 \\ -\sigma^1 & 0 \end{pmatrix} = \begin{pmatrix} -(\sigma^1)^2 & 0 \\ 0 & -(\sigma^1)^2 \end{pmatrix} = -I = \eta^{11}$.
$\{\gamma^0, \gamma^1\} = \gamma^0\gamma^1 + \gamma^1\gamma^0 = \begin{pmatrix} -\sigma^1 & 0 \\ 0 & \sigma^1 \end{pmatrix} + \begin{pmatrix} \sigma^1 & 0 \\ 0 & -\sigma^1 \end{pmatrix} = 0$.

b) $P_L = \frac{1}{2}(1-\gamma^5) = \frac{1}{2}(\begin{pmatrix} I & 0 \\ 0 & I \end{pmatrix} - \begin{pmatrix} -I & 0 \\ 0 & I \end{pmatrix}) = \begin{pmatrix} I & 0 \\ 0 & 0 \end{pmatrix}$.
$P_L \psi = \begin{pmatrix} I & 0 \\ 0 & 0 \end{pmatrix}\begin{pmatrix} \psi_L \\ \psi_R \end{pmatrix} = \begin{pmatrix} \psi_L \\ 0 \end{pmatrix}$.
Similarly for $P_R$.

c) $(i\gamma^0\partial_0 + i\gamma^i\partial_i - m)\psi = 0$
$i\begin{pmatrix} 0 & I \\ I & 0 \end{pmatrix}\begin{pmatrix} \partial_0 \psi_L \\ \partial_0 \psi_R \end{pmatrix} + i\begin{pmatrix} 0 & \sigma^i \\ -\sigma^i & 0 \end{pmatrix}\begin{pmatrix} \partial_i \psi_L \\ \partial_i \psi_R \end{pmatrix} - m\begin{pmatrix} \psi_L \\ \psi_R \end{pmatrix} = 0$
$i(\partial_0 + \sigma^i\partial_i)\psi_R = m\psi_L$
$i(\partial_0 - \sigma^i\partial_i)\psi_L = m\psi_R$
If m=0, the equations become independent: $(\partial_0 + \vec{\sigma}\cdot\vec{\nabla})\psi_R = 0$ and $(\partial_0 - \vec{\sigma}\cdot\vec{\nabla})\psi_L = 0$. These are the Weyl equations.

