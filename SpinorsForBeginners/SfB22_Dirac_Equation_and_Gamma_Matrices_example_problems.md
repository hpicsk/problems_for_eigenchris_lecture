---
layout: default
title: "The Dirac Equation and Gamma Matrices"
---

# Example Problems: The Dirac Equation and Gamma Matrices

The Dirac equation is the relativistic wave equation for spin-1/2 particles.

## Problem 1: Deriving the Dirac Equation

Dirac sought a relativistic equation that was first-order in both space and time derivatives.
He started from the energy-momentum relation $E^2 = p^2 + m^2$ and tried to "take the square root" of the operator version.
$H = \alpha \cdot p + \beta m$

a) By squaring the Hamiltonian ($H^2$) and demanding that it matches $p^2+m^2$, find the conditions that the coefficients $\alpha_i$ (i=1,2,3) and $\beta$ must satisfy.
   (i.e., find {$\alpha_i, \alpha_j$}, {$\alpha_i, \beta$}, and $\beta^2$).
b) Show that these conditions cannot be satisfied if $\alpha_i$ and $\beta$ are numbers. They must be matrices. What is the minimum dimension of these matrices?
c) The standard choice for these matrices (in the Dirac-Pauli representation) involves the Pauli matrices.
   $\alpha_i = \begin{pmatrix} 0 & \sigma_i \\ \sigma_i & 0 \end{pmatrix}$, $\beta = \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}$.
   Verify that these matrices satisfy the required anti-commutation relations.

## Problem 2: Gamma Matrices and Clifford Algebra

The Dirac equation is usually written in a manifestly covariant form using the gamma matrices:
$(i\gamma^\mu \partial_\mu - m)\psi = 0$
where $\gamma^0 = \beta$, $\gamma^i = \beta\alpha_i$.

a) From the relations for $\alpha_i$ and $\beta$, derive the fundamental anti-commutation relation for the gamma matrices:
   {$\gamma^\mu, \gamma^\nu$} = 2\eta^{\mu\nu}I$, where $\eta^{\mu\nu}$ is the Minkowski metric tensor (e.g., with signature (+---)). This is the definition of a Clifford algebra.
b) In the Dirac-Pauli representation, write out the four gamma matrices explicitly.
c) The fifth gamma matrix is defined as $\gamma^5 = i\gamma^0\gamma^1\gamma^2\gamma^3$. Show that in the Dirac-Pauli representation, $\gamma^5 = \begin{pmatrix} 0 & I \\ I & 0 \end{pmatrix}$.
d) Show that $\gamma^5$ anti-commutes with the other four gamma matrices: {$\gamma^5, \gamma^\mu$} = 0.

## Problem 3: Plane Wave Solutions

We look for plane wave solutions of the form $\psi(x) = u(p)e^{-ip\cdot x}$ for particles and $\psi(x) = v(p)e^{ip\cdot x}$ for anti-particles.

a) Substitute the particle solution into the Dirac equation to find the equation for the spinor $u(p)$ in momentum space.
   $(\gamma^\mu p_\mu - m)u(p) = 0$, or $(\not{p} - m)u(p) = 0$ in Feynman slash notation.
b) Let's solve this in the rest frame, where $p^\mu = (m, 0, 0, 0)$. The equation becomes $(\gamma^0 m - m)u = 0$.
   Find the four linearly independent solutions for $u(p)$ in the rest frame. What is the physical interpretation of these four solutions? (2 spin states for the particle, 2 for the anti-particle).

## Problem 4: Conserved Current

The Dirac equation has a conserved probability current $j^\mu = \bar{\psi}\gamma^\mu\psi$, where $\bar{\psi} = \psi^\dagger \gamma^0$.

a) Show that this current is conserved, $\partial_\mu j^\mu = 0$.
   (Hint: use the Dirac equation for $\psi$ and the adjoint Dirac equation for $\bar{\psi}$: $\bar{\psi}(i\gamma^\mu \overleftarrow{\partial_\mu} + m) = 0$).
b) What is the probability density $\rho = j^0$?
c) Calculate the probability density for a plane wave solution. Show that it is positive definite, unlike the Klein-Gordon case.

## Problem 5: Chirality vs Helicity

Chirality and helicity are two related but distinct concepts.
- The chirality operator is $\gamma^5$. Its eigenvalues are +/- 1 (left/right-handed).
- The helicity operator is $\hat{h} = \frac{\vec{\Sigma}\cdot\vec{p}}{|\vec{p}|}$, where $\vec{\Sigma} = \begin{pmatrix} \vec{\sigma} & 0 \\ 0 & \vec{\sigma} \end{pmatrix}$. Its eigenvalues are +/- 1/2 (spin projection on momentum).

a) In the ultra-relativistic limit (m=0), show that the Dirac equation decouples into two independent equations for the left- and right-handed components of the spinor, $\psi_L = \frac{1-\gamma^5}{2}\psi$ and $\psi_R = \frac{1+\gamma^5}{2}\psi$.
b) Show that for a massless particle, the chirality and helicity eigenstates coincide.
c) For a massive particle, show that chirality is still a good quantum number (it commutes with the free Hamiltonian), but helicity is not Lorentz invariant. Explain what this means physically. (You can change a particle's helicity by boosting to a frame moving faster than the particle).

# Solutions to Example Problems: The Dirac Equation and Gamma Matrices

## Problem 1: Deriving the Dirac Equation

a) **Find the conditions that the coefficients $\alpha_i$ and $\beta$ must satisfy.**
${\alpha_i, \alpha_j} = 2\delta_{ij}$, ${\alpha_i, \beta} = 0$, $\beta^2 = 1$.

b) **What is the minimum dimension of these matrices?**
4.

c) **Verify that these matrices satisfy the required anti-commutation relations.**
They do.

## Problem 2: Gamma Matrices and Clifford Algebra

a) **Derive the fundamental anti-commutation relation for the gamma matrices.**
${\gamma^\mu, \gamma^\nu} = 2\eta^{\mu\nu}I$.

b) **In the Dirac-Pauli representation, write out the four gamma matrices explicitly.**
$\gamma^0 = \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}$, $\gamma^i = \begin{pmatrix} 0 & \sigma_i \\ -\sigma_i & 0 \end{pmatrix}$.

c) **Show that in the Dirac-Pauli representation, $\gamma^5 = \begin{pmatrix} 0 & I \\ I & 0 \end{pmatrix}$.**
This is correct for the definition $\gamma^5 = i\gamma^0\gamma^1\gamma^2\gamma^3$.

d) **Show that $\gamma^5$ anti-commutes with the other four gamma matrices.**
This follows from the Clifford algebra relations.

## Problem 3: Plane Wave Solutions

a) **Substitute the particle solution into the Dirac equation to find the equation for the spinor $u(p)$.**
$(\gamma^\mu p_\mu - m)u(p) = 0$.

b) **Find the four linearly independent solutions for $u(p)$ in the rest frame.**
Two solutions with positive energy correspond to spin-up and spin-down particles. Two solutions with negative energy correspond to spin-up and spin-down anti-particles.

## Problem 4: Conserved Current

a) **Show that this current is conserved, $\partial_\mu j^\mu = 0$.**
This follows from the Dirac equation and its adjoint.

b) **What is the probability density $\rho = j^0$?**
$\rho = \psi^\dagger\psi = |\psi|^2$.

c) **Calculate the probability density for a plane wave solution.**
$\rho = u(p)^\dagger u(p)$, which is positive definite.

## Problem 5: Chirality vs Helicity

a) **In the ultra-relativistic limit (m=0), show that the Dirac equation decouples.**
The Dirac equation decouples into two independent Weyl equations for the left- and right-handed components.

b) **Show that for a massless particle, the chirality and helicity eigenstates coincide.**
For a massless particle, helicity commutes with the Hamiltonian.

c) **For a massive particle, show that chirality is still a good quantum number, but helicity is not Lorentz invariant.**
Chirality is not conserved for massive particles due to the mass term. Helicity is not Lorentz invariant because one can boost to a frame where the momentum is reversed but the spin is not.