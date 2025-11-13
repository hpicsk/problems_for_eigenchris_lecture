
This lecture builds upon the previous one, defining spinors as elements of minimal left ideals of a Clifford algebra.

## Problem 1: Spinor as a minimal left ideal

In $Cl_{3,0}(\mathbb{C})$, which is isomorphic to $M(2, \mathbb{C})$, we have the projector $p = \frac{1}{2}(1 + \sigma_3)$.
The minimal left ideal is $S = Cl_{3,0}p$.

a) Show that any element $\psi \in S$ can be written as a linear combination of $p$ and $\sigma_1 p$.

b) Express $p$ and $\sigma_1 p$ in the standard basis
$\begin{pmatrix} 1 \\ 0 \end{pmatrix}, \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.

### Solution 1

a) An arbitrary element of $Cl_{3,0}$ can be written as $a = c_0 + c_i \sigma_i + d_i \sigma_j \sigma_k + d_0 \sigma_1 \sigma_2 \sigma_3$. Since $\sigma_j \sigma_k = i \epsilon_{jk\ell} \sigma_\ell$ and $\sigma_1 \sigma_2 \sigma_3 = i$, this simplifies to $a = z_0 + z_i \sigma_i$ where $z_\mu$ are complex numbers.
So $\psi = ap = (z_0 + z_i \sigma_i)p = z_0 p + z_1 \sigma_1 p + z_2 \sigma_2 p + z_3 \sigma_3 p$.
We know that $\sigma_3 p = p$. Also $\sigma_2 p = \sigma_2 \frac{1}{2}(1+\sigma_3) = \frac{1}{2}(\sigma_2 + \sigma_2\sigma_3) = \frac{1}{2}(\sigma_2 + i\sigma_1) = i\sigma_1 \frac{1}{2}(1+\sigma_3) - i\sigma_1\sigma_3 \frac{1}{2}(1+\sigma_3) = i\sigma_1 p - i\sigma_1 p = i \sigma_1 p$.
So $\psi = (z_0+z_3)p + (z_1+iz_2)\sigma_1 p$. This is a linear combination of $p$ and $\sigma_1 p$.

b) Using the standard representation of Pauli matrices:
$p = \frac{1}{2}(1 + \sigma_3) = \frac{1}{2}(\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} + \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}) = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$.
This matrix acting on any vector projects it onto the space spanned by $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$.
$\sigma_1 p = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 0 & 0 \\ 1 & 0 \end{pmatrix}$.
This matrix maps the spin-up basis vector to the spin-down basis vector.

## Problem 2: Dirac Spinors

The Clifford algebra $Cl_{1,3}$ is the algebra of spacetime. It is isomorphic to $M(4, \mathbb{C})$. The generators are the gamma matrices, $\gamma_\mu$, satisfying $\{\gamma_\mu, \gamma_\nu\} = 2\eta_{\mu\nu}$.
In the Dirac representation:
$\gamma_0 = \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}$, $\gamma_i = \begin{pmatrix} 0 & \sigma_i \\ -\sigma_i & 0 \end{pmatrix}$.

a) Construct the projector $P_+ = \frac{1}{2}(1 + \gamma_0)$. Show it is a projector.

b) The ideal $S_+ = Cl_{1,3}P_+$ is a spinor space. Show that any $\psi \in S_+$ satisfies $\gamma_0 \psi = \psi$.

c) What is the dimension of this spinor space over $\mathbb{C}$?

### Solution 2

a) $P_+^2 = \frac{1}{4}(1+\gamma_0)(1+\gamma_0) = \frac{1}{4}(1 + 2\gamma_0 + \gamma_0^2)$.
Since $\gamma_0^2 = \eta_{00} = 1$, this becomes $P_+^2 = \frac{1}{4}(1 + 2\gamma_0 + 1) = \frac{1}{2}(1+\gamma_0) = P_+$.

b) The ideal $S_+ = Cl_{1,3}P_+$ is the spinor space. In a matrix representation, the spinors can be taken as the column vectors of the elements of the ideal. The simplest element of the ideal is the projector $P_+$ itself. Let's find the column space of $P_+$.
In the Dirac representation, $P_+ = \frac{1}{2}(1 + \gamma_0) = \frac{1}{2}(\begin{pmatrix} I & 0 \\ 0 & I \end{pmatrix} + \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}) = \begin{pmatrix} I & 0 \\ 0 & 0 \end{pmatrix}$.
The column space of this matrix is spanned by vectors of the form $\begin{pmatrix} a \\ b \\ 0 \\ 0 \end{pmatrix}$.
Let $\psi$ be a spinor in this space. Then $\gamma_0 \psi = \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix} \begin{pmatrix} a \\ b \\ 0 \\ 0 \end{pmatrix} = \begin{pmatrix} a \\ b \\ 0 \\ 0 \end{pmatrix} = \psi$.
This means the spinors in this ideal are eigenstates of $\gamma_0$ with eigenvalue +1 (positive energy).

c) The algebra $M(4, \mathbb{C})$ has dimension 16. A minimal left ideal is the space of matrices with 3 columns equal to zero. This has dimension 4. So a Dirac spinor has 4 complex components.

