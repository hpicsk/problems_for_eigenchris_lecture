---
layout: default
title: "Pauli, Weyl, and Dirac Spinors"
---

# Example Problems and Solutions: Pauli, Weyl, and Dirac Spinors

## Problem 1: Chirality of Dirac Spinors

A Dirac spinor $\psi$ can be decomposed into its left-handed and right-handed components using the chirality operator $\gamma^5$.
$$\psi_L = \frac{1}{2}(1 - \gamma^5)\psi$$
$$\psi_R = \frac{1}{2}(1 + \gamma^5)\psi$$

Given the Dirac spinor:
$$\psi = \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}$$

And the gamma matrix $\gamma^5$ in the Weyl representation:
$$\gamma^5 = \begin{pmatrix} -I & 0 \\ 0 & I \end{pmatrix} = \begin{pmatrix} -1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$$

Calculate the left-handed ($\psi_L$) and right-handed ($\psi_R$) components of $\psi$.

### Solution 1

Given $\psi = \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}$ and $\gamma^5 = \begin{pmatrix} -1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$.

$$\psi_L = \frac{1}{2}(1 - \gamma^5)\psi = \frac{1}{2}\left(\begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} - \begin{pmatrix} -1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}\right)\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}$$

$$= \frac{1}{2}\begin{pmatrix} 2 & 0 & 0 & 0 \\ 0 & 2 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix}$$

$$\psi_R = \frac{1}{2}(1 + \gamma^5)\psi = \frac{1}{2}\left(\begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} + \begin{pmatrix} -1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}\right)\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}$$

$$= \frac{1}{2}\begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 2 & 0 \\ 0 & 0 & 0 & 2 \end{pmatrix}\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}\begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix}$$

## Problem 2: Weyl Spinors from Dirac Spinors

In the Weyl basis, a Dirac spinor is composed of two 2-component Weyl spinors, $\psi_L$ and $\psi_R$.
$$\psi = \begin{pmatrix} \psi_L \\ \psi_R \end{pmatrix}$$

From the previous problem, what are the corresponding 2-component Weyl spinors $\psi_L$ and $\psi_R$?

### Solution 2

In the Weyl basis, $\psi = \begin{pmatrix} \psi_L \\ \psi_R \end{pmatrix}$.

From the previous problem, the full Dirac spinor is $\psi = \psi_L + \psi_R = \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \end{pmatrix} + \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}$.

The 2-component Weyl spinors are the upper and lower components of the Dirac spinor in the Weyl basis.
From the problem statement, $\psi = \begin{pmatrix} 1 \\ 0 \\ 1 \\ 0 \end{pmatrix}$, so $\psi_L = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and $\psi_R = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

## Problem 3: Mass Terms and Chirality

The mass term in the Dirac Lagrangian couples the left- and right-handed components of the Dirac spinor: $m\bar{\psi}\psi = m(\bar{\psi}_R\psi_L + \bar{\psi}_L\psi_R)$.

Explain why a massive particle cannot be described by a single Weyl spinor. What does this imply about neutrinos if they are massive?

### Solution 3

The mass term $m\bar{\psi}\psi$ mixes the left and right-handed components. A single Weyl spinor is either left-handed or right-handed. If a particle is described by a single Weyl spinor, it cannot have a mass term of this form in the Lagrangian.

If neutrinos are massive, they cannot be described by a single Weyl spinor. They must be Dirac spinors (with both left and right-handed components) or Majorana spinors (where the right-handed component is related to the left-handed one). The existence of neutrino mass implies that there must be a right-handed component, even if it does not interact with the weak force.

## Problem 4: Pauli Spinors

Pauli spinors are 2-component spinors used in non-relativistic quantum mechanics. How are they related to Dirac spinors in the non-relativistic limit?

Consider the Dirac equation for a particle at rest. Show how the upper two components of the Dirac spinor reduce to the Pauli spinor in the low-energy limit.

### Solution 4

In the non-relativistic limit, the energy of a particle is dominated by its rest mass, $E \approx mc^2$.

The Dirac equation is $(i\gamma^\mu\partial_\mu - m)\psi = 0$.

For a particle at rest, $\partial_i \psi = 0$, so the equation becomes $(i\gamma^0\partial_t - m)\psi = 0$.

In the Dirac representation, $\gamma^0 = \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}$.

The equation becomes:
$$\left(i\begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}\partial_t - m\begin{pmatrix} I & 0 \\ 0 & I \end{pmatrix}\right)\psi = 0$$

Let $\psi = \begin{pmatrix} \phi \\ \chi \end{pmatrix}e^{-iEt/\hbar}$.

$$i\begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}(-iE/\hbar)\begin{pmatrix} \phi \\ \chi \end{pmatrix} - m\begin{pmatrix} \phi \\ \chi \end{pmatrix} = 0$$

$$\begin{pmatrix} E & 0 \\ 0 & -E \end{pmatrix}\begin{pmatrix} \phi \\ \chi \end{pmatrix} - m\begin{pmatrix} \phi \\ \chi \end{pmatrix} = 0$$

This gives two equations:
$$E\phi - m\phi = 0 \implies E=m$$
$$-E\chi - m\chi = 0 \implies E=-m$$

For the positive energy solution, $E=m$, we have $\chi=0$.

The Dirac spinor is $\psi = \begin{pmatrix} \phi \\ 0 \end{pmatrix}$, where $\phi$ is a 2-component spinor.

In the low-energy limit, the upper two components $\phi$ behave as a non-relativistic Pauli spinor, and the lower two components are small.

## Problem 5: Lorentz Invariance

Which of the following expressions are Lorentz invariant?

a) $\bar{\psi}\psi$

b) $\bar{\psi}\gamma^5\psi$

c) $\bar{\psi}\gamma^\mu\psi$

d) $\bar{\psi}\gamma^\mu\gamma^5\psi$

e) $\psi^\dagger\psi$

Explain your reasoning for each case.

### Solution 5

a) **$\bar{\psi}\psi$**: Scalar. Lorentz invariant.

b) **$\bar{\psi}\gamma^5\psi$**: Pseudoscalar. Lorentz invariant.

c) **$\bar{\psi}\gamma^\mu\psi$**: Vector. Transforms as a vector under Lorentz transformations. Not invariant, but covariant.

d) **$\bar{\psi}\gamma^\mu\gamma^5\psi$**: Axial vector. Transforms as a pseudovector. Not invariant, but covariant.

e) **$\psi^\dagger\psi$**: Not Lorentz invariant. It is the 0-th component of the vector current $\bar{\psi}\gamma^\mu\psi$.