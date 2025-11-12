# SfB 4: Quantum Spin States - Example Problems and Solutions

This lecture introduces the quantum mechanical description of spin-1/2 particles.

## Problem 1: Spin Operators

The spin operators for a spin-1/2 particle are given by $S_i = \frac{\hbar}{2}\sigma_i$, where $\sigma_i$ are the Pauli matrices.

a) Write down the matrices for the spin operators $S_x, S_y, S_z$.

b) What are the eigenvalues and eigenvectors of the $S_z$ operator? What is the physical meaning of these states?

c) These eigenvectors are often denoted as $|+\rangle$ or $|\uparrow\rangle$ (spin up) and $|-\rangle$ or $|\downarrow\rangle$ (spin down). Write these states as 2-component column vectors (spinors).

### Solution 1:

a) **Write down the matrices for the spin operators $S_x, S_y, S_z$.**

$$S_x = \frac{\hbar}{2}\sigma_x = \frac{\hbar}{2}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$$

$$S_y = \frac{\hbar}{2}\sigma_y = \frac{\hbar}{2}\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}$$

$$S_z = \frac{\hbar}{2}\sigma_z = \frac{\hbar}{2}\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$

b) **What are the eigenvalues and eigenvectors of the $S_z$ operator? What is the physical meaning of these states?**

The eigenvalues of $S_z$ are $+\frac{\hbar}{2}$ and $-\frac{\hbar}{2}$.

The eigenvector for $+\frac{\hbar}{2}$ is $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$, which represents the spin-up state along the z-axis.

The eigenvector for $-\frac{\hbar}{2}$ is $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$, which represents the spin-down state along the z-axis.

These states correspond to the two possible outcomes of measuring the spin component along the z-axis.

c) **These eigenvectors are often denoted as $|+\rangle$ or $|\uparrow\rangle$ (spin up) and $|-\rangle$ or $|\downarrow\rangle$ (spin down). Write these states as 2-component column vectors (spinors).**

$$|+\rangle = |\uparrow\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$$

$$|-\rangle = |\downarrow\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$$

## Problem 2: Expectation Values

A particle is in the spin state $|\psi\rangle = \frac{1}{\sqrt{5}}\begin{pmatrix} 1 \\ 2 \end{pmatrix}$.

a) Is this state normalized?

b) Calculate the expectation values of the three spin components: $\langle S_x \rangle, \langle S_y \rangle, \langle S_z \rangle$.
   The expectation value of an operator $A$ is given by $\langle A \rangle = \langle\psi|A|\psi\rangle$.

c) What is the magnitude of the spin vector $(\langle S_x \rangle, \langle S_y \rangle, \langle S_z \rangle)$?

### Solution 2:

a) **Is this state normalized?**

$$|\psi\rangle = \frac{1}{\sqrt{5}}\begin{pmatrix} 1 \\ 2 \end{pmatrix}$$

$$\langle\psi|\psi\rangle = \left(\frac{1}{\sqrt{5}}\right)^2 \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \frac{1}{5}(1+4) = 1$$

Yes, the state is normalized.

b) **Calculate the expectation values of the three spin components: $\langle S_x \rangle, \langle S_y \rangle, \langle S_z \rangle$.**

$$\langle S_x \rangle = \langle\psi|S_x|\psi\rangle = \frac{1}{5} \begin{pmatrix} 1 & 2 \end{pmatrix} \frac{\hbar}{2}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix}$$

$$= \frac{\hbar}{10} \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} 2 \\ 1 \end{pmatrix} = \frac{\hbar}{10}(2+2) = \frac{2\hbar}{5}$$

$$\langle S_y \rangle = \langle\psi|S_y|\psi\rangle = \frac{1}{5} \begin{pmatrix} 1 & 2 \end{pmatrix} \frac{\hbar}{2}\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix}$$

$$= \frac{\hbar}{10} \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} -2i \\ i \end{pmatrix} = \frac{\hbar}{10}(-2i+2i) = 0$$

$$\langle S_z \rangle = \langle\psi|S_z|\psi\rangle = \frac{1}{5} \begin{pmatrix} 1 & 2 \end{pmatrix} \frac{\hbar}{2}\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix}$$

$$= \frac{\hbar}{10} \begin{pmatrix} 1 & 2 \end{pmatrix} \begin{pmatrix} 1 \\ -2 \end{pmatrix} = \frac{\hbar}{10}(1-4) = -\frac{3\hbar}{10}$$

c) **What is the magnitude of the spin vector $(\langle S_x \rangle, \langle S_y \rangle, \langle S_z \rangle)$?**

$$\text{Magnitude} = \sqrt{\left(\frac{2\hbar}{5}\right)^2 + 0^2 + \left(-\frac{3\hbar}{10}\right)^2} = \hbar\sqrt{\frac{4}{25} + \frac{9}{100}} = \hbar\sqrt{\frac{16+9}{100}} = \hbar\sqrt{\frac{25}{100}} = \frac{\hbar}{2}$$

## Problem 3: Measurement

A particle is in the spin-up state with respect to the z-axis, $|\psi\rangle = |+\rangle_z = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

We now measure the spin in the x-direction.

a) What are the possible outcomes of this measurement?

b) What is the probability of each outcome?
   (Hint: First, find the eigenvectors of $S_x$. Then, express the state $|\psi\rangle$ in the basis of the $S_x$ eigenvectors.)

### Solution 3:

a) **What are the possible outcomes of this measurement?**

The possible outcomes of a spin measurement are the eigenvalues of the corresponding spin operator. For $S_x$, the eigenvalues are $+\frac{\hbar}{2}$ and $-\frac{\hbar}{2}$.

b) **What is the probability of each outcome?**

The eigenvectors of $S_x$ are:

For eigenvalue $+\frac{\hbar}{2}$: $|+\rangle_x = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$.

For eigenvalue $-\frac{\hbar}{2}$: $|-\rangle_x = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ -1 \end{pmatrix}$.

The initial state is $|\psi\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$.

We express $|\psi\rangle$ in the basis of $S_x$ eigenvectors:
$$|\psi\rangle = c_1 |+\rangle_x + c_2 |-\rangle_x$$

$$c_1 = \langle +_x | \psi \rangle = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}}$$

$$c_2 = \langle -_x | \psi \rangle = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & -1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \frac{1}{\sqrt{2}}$$

The probability of measuring $+\frac{\hbar}{2}$ is $|c_1|^2 = \left(\frac{1}{\sqrt{2}}\right)^2 = \frac{1}{2}$.

The probability of measuring $-\frac{\hbar}{2}$ is $|c_2|^2 = \left(\frac{1}{\sqrt{2}}\right)^2 = \frac{1}{2}$.

## Problem 4: Time Evolution

The Hamiltonian for a spin in a magnetic field $B$ is $H = -\gamma \vec{S} \cdot \vec{B}$, where $\gamma$ is the gyromagnetic ratio.
Let the magnetic field be uniform and in the z-direction: $\vec{B} = B_0 \hat{z}$.

a) Write down the Hamiltonian matrix.

b) At time $t=0$, the particle is in the spin-up state with respect to the x-axis: $|\psi(0)\rangle = |+\rangle_x$. Find this state as a spinor.

c) The state evolves according to the Schrödinger equation: $|\psi(t)\rangle = e^{-iHt/\hbar}|\psi(0)\rangle$. Find the state of the system at a later time $t$.

d) Calculate the expectation value of $S_x$ as a function of time. What is the physical interpretation of this result? (Larmor precession).

### Solution 4:

a) **Write down the Hamiltonian matrix.**

$$H = -\gamma B_0 S_z = -\gamma B_0 \frac{\hbar}{2} \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} = -\frac{\gamma B_0 \hbar}{2} \sigma_z$$

Let $\omega_0 = \gamma B_0$. Then $H = -\frac{\hbar\omega_0}{2}\sigma_z$.

b) **At time $t=0$, the particle is in the spin-up state with respect to the x-axis: $|\psi(0)\rangle = |+\rangle_x$. Find this state as a spinor.**

$$|+\rangle_x = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$$

c) **Find the state of the system at a later time $t$.**

$$|\psi(t)\rangle = e^{-iHt/\hbar}|\psi(0)\rangle = e^{i\frac{\omega_0 t}{2}\sigma_z}|\psi(0)\rangle = \left(\cos\left(\frac{\omega_0 t}{2}\right)I + i\sin\left(\frac{\omega_0 t}{2}\right)\sigma_z\right)|\psi(0)\rangle$$

$$|\psi(t)\rangle = \begin{pmatrix} \cos\left(\frac{\omega_0 t}{2}\right) + i\sin\left(\frac{\omega_0 t}{2}\right) & 0 \\ 0 & \cos\left(\frac{\omega_0 t}{2}\right) - i\sin\left(\frac{\omega_0 t}{2}\right) \end{pmatrix} \frac{1}{\sqrt{2}}\begin{pmatrix} 1 \\ 1 \end{pmatrix}$$

$$= \frac{1}{\sqrt{2}} \begin{pmatrix} e^{i\omega_0 t/2} \\ e^{-i\omega_0 t/2} \end{pmatrix}$$

d) **Calculate the expectation value of $S_x$ as a function of time. What is the physical interpretation of this result? (Larmor precession).**

$$\langle S_x(t) \rangle = \langle\psi(t)|S_x|\psi(t)\rangle = \frac{1}{2} \begin{pmatrix} e^{-i\omega_0 t/2} & e^{i\omega_0 t/2} \end{pmatrix} \frac{\hbar}{2}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} e^{i\omega_0 t/2} \\ e^{-i\omega_0 t/2} \end{pmatrix}$$

$$= \frac{\hbar}{4} \begin{pmatrix} e^{-i\omega_0 t/2} & e^{i\omega_0 t/2} \end{pmatrix} \begin{pmatrix} e^{-i\omega_0 t/2} \\ e^{i\omega_0 t/2} \end{pmatrix} = \frac{\hbar}{4} \left(e^{-i\omega_0 t} + e^{i\omega_0 t}\right) = \frac{\hbar}{2}\cos(\omega_0 t)$$

The expectation value of the spin in the x-direction oscillates with frequency $\omega_0$. This is Larmor precession: the spin vector is precessing around the magnetic field in the z-direction.

## Problem 5: Entanglement

Consider a system of two spin-1/2 particles in the singlet state:

$$|\Psi\rangle = \frac{1}{\sqrt{2}}(|\uparrow\downarrow\rangle - |\downarrow\uparrow\rangle) = \frac{1}{\sqrt{2}}\left(\begin{pmatrix} 1 \\ 0 \end{pmatrix} \otimes \begin{pmatrix} 0 \\ 1 \end{pmatrix} - \begin{pmatrix} 0 \\ 1 \end{pmatrix} \otimes \begin{pmatrix} 1 \\ 0 \end{pmatrix}\right)$$

a) Write the state vector $|\Psi\rangle$ as a single 4-component vector.

b) Suppose we measure the spin of the first particle in the z-direction and find it to be spin-up. What is the state of the second particle immediately after the measurement?

c) Suppose we measure the spin of the first particle in the x-direction and find it to be spin-up. What is the state of the second particle?

d) Is it possible to write the singlet state as a simple product of the states of the two individual particles, $|\Psi\rangle = |\psi_1\rangle \otimes |\psi_2\rangle$? Explain why this state is called "entangled".

### Solution 5:

a) **Write the state vector $|\Psi\rangle$ as a single 4-component vector.**

$$|\Psi\rangle = \frac{1}{\sqrt{2}}\left(\begin{pmatrix} 1 \\ 0 \end{pmatrix} \otimes \begin{pmatrix} 0 \\ 1 \end{pmatrix} - \begin{pmatrix} 0 \\ 1 \end{pmatrix} \otimes \begin{pmatrix} 1 \\ 0 \end{pmatrix}\right) = \frac{1}{\sqrt{2}}\left(\begin{pmatrix} 0 \\ 1 \\ 0 \\ 0 \end{pmatrix} - \begin{pmatrix} 0 \\ 0 \\ 1 \\ 0 \end{pmatrix}\right) = \frac{1}{\sqrt{2}}\begin{pmatrix} 0 \\ 1 \\ -1 \\ 0 \end{pmatrix}$$

b) **Suppose we measure the spin of the first particle in the z-direction and find it to be spin-up. What is the state of the second particle immediately after the measurement?**

If the first particle is spin-up, we have projected the state onto the subspace where the first particle is $|\uparrow\rangle$. The term in the singlet state is $\frac{1}{\sqrt{2}}|\uparrow\downarrow\rangle$. After normalization, the state of the two-particle system is $|\uparrow\downarrow\rangle$. The state of the second particle is $|\downarrow\rangle$.

c) **Suppose we measure the spin of the first particle in the x-direction and find it to be spin-up. What is the state of the second particle?**

The singlet state can be written in the x-basis as $|\Psi\rangle = \frac{1}{\sqrt{2}}(|+-\rangle_x - |-+\rangle_x)$.

If we measure the first particle to be spin-up in the x-direction ($|+\rangle_x$), the state of the system collapses to $|+-\rangle_x$. The state of the second particle is spin-down in the x-direction ($|-\rangle_x$).

d) **Is it possible to write the singlet state as a simple product of the states of the two individual particles, $|\Psi\rangle = |\psi_1\rangle \otimes |\psi_2\rangle$? Explain why this state is called "entangled".**

No, it is not possible. A general product state is:

$$|\psi_1\rangle \otimes |\psi_2\rangle = \begin{pmatrix} a \\ b \end{pmatrix} \otimes \begin{pmatrix} c \\ d \end{pmatrix} = \begin{pmatrix} ac \\ ad \\ bc \\ bd \end{pmatrix}$$

For the singlet state $\frac{1}{\sqrt{2}}\begin{pmatrix} 0 \\ 1 \\ -1 \\ 0 \end{pmatrix}$, we would need $ac=0$ and $bd=0$. If $a=0$, then $ad=0$, but we need $ad=1/\sqrt{2}$. If $c=0$, then $bc=0$, but we need $bc=-1/\sqrt{2}$. So it is not possible to write it as a product state.

This is the definition of an entangled state: a state of a multi-particle system that cannot be written as a product of the states of the individual particles. The measurement outcomes for the two particles are correlated, no matter how far apart they are.