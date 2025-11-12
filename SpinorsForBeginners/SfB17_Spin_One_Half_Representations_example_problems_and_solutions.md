---
layout: default
title: "Spin 1/2 Representations"
---

# Example Problems: Spin 1/2 Representations

This lecture focuses on the spin 1/2 representation of the SU(2) group, which describes the behavior of spin 1/2 particles like electrons.

## Problem 1: Wigner D-matrix for spin 1/2

The rotation operator for a spin 1/2 particle is given by $D(R) = e^{-i\frac{\theta}{2} \hat{n} \cdot \vec{\sigma}}}$, where R is a rotation by angle $\theta$ about the axis $\hat{n}$.

a) A rotation by angle $\alpha$ about the z-axis is given by $R_z(\alpha)$. Write down the corresponding D-matrix.

b) A rotation by angle $\beta$ about the y-axis is given by $R_y(\beta)$. Write down the corresponding D-matrix.

c) A general rotation can be parameterized by Euler angles $(\alpha, \beta, \gamma)$ as $R(\alpha, \beta, \gamma) = R_z(\alpha)R_y(\beta)R_z(\gamma)$. Find the D-matrix for this general rotation.

### Solution 1

a) $D(R_z(\alpha)) = e^{-i\frac{\alpha}{2}\sigma_z} = \cos(\alpha/2)I - i\sin(\alpha/2)\sigma_z = \begin{pmatrix} e^{-i\alpha/2} & 0 \\ 0 & e^{i\alpha/2} \end{pmatrix}$.

b) $D(R_y(\beta)) = e^{-i\frac{\beta}{2}\sigma_y} = \cos(\beta/2)I - i\sin(\beta/2)\sigma_y = \begin{pmatrix} \cos(\beta/2) & -\sin(\beta/2) \\ \sin(\beta/2) & \cos(\beta/2) \end{pmatrix}$.

c) $D(\alpha, \beta, \gamma) = D(R_z(\alpha))D(R_y(\beta))D(R_z(\gamma))$
$= \begin{pmatrix} e^{-i\alpha/2} & 0 \\ 0 & e^{i\alpha/2} \end{pmatrix} \begin{pmatrix} \cos(\beta/2) & -\sin(\beta/2) \\ \sin(\beta/2) & \cos(\beta/2) \end{pmatrix} \begin{pmatrix} e^{-i\gamma/2} & 0 \\ 0 & e^{i\gamma/2} \end{pmatrix}$
$= \begin{pmatrix} e^{-i(\alpha+\gamma)/2}\cos(\beta/2) & -e^{-i(\alpha-\gamma)/2}\sin(\beta/2) \\ e^{i(\alpha-\gamma)/2}\sin(\beta/2) & e^{i(\alpha+\gamma)/2}\cos(\beta/2) \end{pmatrix}$.
This is the Wigner D-matrix for j=1/2.

## Problem 2: Transformation of Spin States

Let the spin-up and spin-down states be $|\uparrow\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and $|\downarrow\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.

a) What is the state of a spin-up particle after a rotation by 90 degrees about the y-axis?

b) What is the probability of measuring the particle to be spin-up after this rotation?

c) What is the state of a spin-up particle after a rotation by 360 degrees about the z-axis? What is the physical significance of this?

### Solution 2

a) The rotation matrix is $D(R_y(\pi/2)) = \begin{pmatrix} \cos(\pi/4) & -\sin(\pi/4) \\ \sin(\pi/4) & \cos(\pi/4) \end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix}$.
The new state is $|\psi'\rangle = D|\uparrow\rangle = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix}\begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{1}{\sqrt{2}}(|\uparrow\rangle + |\downarrow\rangle)$.
This is a spin-up state in the x-direction.

b) The probability of measuring spin-up is $|\langle\uparrow|\psi'\rangle|^2 = |\frac{1}{\sqrt{2}}|^2 = 1/2$.

c) The rotation matrix is $D(R_z(2\pi)) = \begin{pmatrix} e^{-i\pi} & 0 \\ 0 & e^{i\pi} \end{pmatrix} = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} = -I$.
The new state is $-|\uparrow\rangle$. The state acquires a phase of -1. This is a characteristic feature of spinors and has observable consequences in interference experiments.

