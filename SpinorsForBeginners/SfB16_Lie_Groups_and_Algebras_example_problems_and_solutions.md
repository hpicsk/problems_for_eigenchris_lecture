
This lecture introduces the mathematical framework of Lie groups and Lie algebras, which are essential for describing continuous symmetries in physics.

## Problem 1: The Lie Group SU(2)

The special unitary group SU(2) is the group of 2x2 unitary matrices with determinant 1. It is a Lie group.

a) Show that a general element of SU(2) can be written as $U = \begin{pmatrix} a & b \\ -\bar{b} & \bar{a} \end{pmatrix}$ with $|a|^2 + |b|^2 = 1$.

b) The Lie algebra su(2) is the space of 2x2 anti-hermitian matrices with trace 0. Show that the Pauli matrices $\sigma_i$ form a basis for su(2) (multiplied by i).

c) The exponential map connects the Lie algebra to the Lie group. Given $X = i\theta \frac{\sigma_3}{2} \in su(2)$, calculate $U = e^X$. What transformation does this represent?

### Solution 1

a) Let $U = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$. Unitarity means $U^\dagger U = I$, so $\begin{pmatrix} \bar{a} & \bar{c} \\ \bar{b} & \bar{d} \end{pmatrix}\begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$.
This gives $|a|^2+|c|^2=1$, $|b|^2+|d|^2=1$, $\bar{a}b+\bar{c}d=0$. Also $\det(U) = ad-bc=1$.
From the second column of $U^\dagger$, we have $c=-\bar{b}$ and $d=\bar{a}$. Then $|a|^2+|b|^2=1$ is satisfied.

b) An anti-hermitian matrix satisfies $X^\dagger = -X$. A general 2x2 matrix is $X = \begin{pmatrix} z_1 & z_2 \\ z_3 & z_4 \end{pmatrix}$.
$X^\dagger = \begin{pmatrix} \bar{z_1} & \bar{z_3} \\ \bar{z_2} & \bar{z_4} \end{pmatrix} = -X = \begin{pmatrix} -z_1 & -z_2 \\ -z_3 & -z_4 \end{pmatrix}$.
So $z_1$ is purely imaginary, $z_4$ is purely imaginary, and $z_3 = -\bar{z_2}$.
Trace is 0 means $z_1+z_4=0$. So $X = \begin{pmatrix} i c & a+ib \\ -a+ib & -ic \end{pmatrix} = a(-i\sigma_2) + b(i\sigma_1) + c(i\sigma_3)$.
So the matrices $i\sigma_k$ form a basis for su(2).

c) $X = i\theta \frac{\sigma_3}{2}$. $X^n = (i\theta/2)^n \sigma_3^n$. Since $\sigma_3^2=I$, we have
$e^X = \sum_n \frac{X^n}{n!} = \sum_{k, even} \frac{(i\theta/2)^k}{k!} I + \sum_{k, odd} \frac{(i\theta/2)^k}{k!} \sigma_3 = \cos(\theta/2)I + i\sin(\theta/2)\sigma_3 = \begin{pmatrix} e^{i\theta/2} & 0 \\ 0 & e^{-i\theta/2} \end{pmatrix}$.
This represents a rotation by angle $\theta$ around the z-axis.

## Problem 2: Lie Brackets and Structure Constants

The Lie bracket (or commutator) of two elements of a Lie algebra is $[X,Y] = XY-YX$. For su(2), the basis is $J_i = \frac{\sigma_i}{2}$.

a) Calculate the commutation relations for the basis elements of su(2). That is, find $[J_i, J_j]$.

b) The structure constants $f_{ijk}$ are defined by $[J_i, J_j] = i \sum_k \epsilon_{ijk} J_k$. Verify this relationship.

### Solution 2

a) $[J_1, J_2] = [\frac{\sigma_1}{2}, \frac{\sigma_2}{2}] = \frac{1}{4}(\sigma_1\sigma_2 - \sigma_2\sigma_1) = \frac{1}{4}(i\sigma_3 - (-i\sigma_3)) = i\frac{\sigma_3}{2} = iJ_3$.
Similarly, $[J_2, J_3] = iJ_1$ and $[J_3, J_1] = iJ_2$.
In general, $[J_i, J_j] = i \epsilon_{ijk} J_k$.

b) The structure constants are given by the Levi-Civita symbol, $f_{ijk} = \epsilon_{ijk}$.
For example, for i=1, j=2, k=3, we have $[J_1, J_2] = i \epsilon_{123} J_3 = iJ_3$, which is correct.

