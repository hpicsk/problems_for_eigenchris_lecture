
This lecture covers the concept of irreducible representations (irreps) of Lie groups, which are the building blocks of all representations.

## Problem 1: Reducibility of a Representation

A representation D is reducible if there exists a subspace that is invariant under the action of the group. Otherwise, it is irreducible.

a) Consider the representation of SO(2) acting on $\mathbb{R}^2$: $D(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$. Is this representation reducible over the real numbers?

b) Is it reducible over the complex numbers? (Hint: find the eigenvectors of the matrix).

### Solution 1

a) No. There is no 1D subspace (a line through the origin) that is mapped to itself by all rotations. Any line is rotated to another line.

b) Yes. The eigenvectors of the rotation matrix are $v_\pm = \begin{pmatrix} 1 \\ \mp i \end{pmatrix}$ with eigenvalues $e^{\pm i\theta}$.
The subspaces spanned by $v_+$ and $v_-$ are 1D complex subspaces that are invariant under the rotation. So the representation is reducible over $\mathbb{C}$.
$D = D_+ \oplus D_-$, where $D_\pm(\theta) = e^{\pm i\theta}$.

## Problem 2: Irreducible Representations of SU(2)

The irreducible representations of SU(2) are labeled by a half-integer $j=0, 1/2, 1, 3/2, ...$. The dimension of the representation is $2j+1$.

a) What is the dimension of the j=1 representation? What physical system does this describe?

b) The basis states for the j=1 representation are $|1,1\rangle, |1,0\rangle, |1,-1\rangle$. The angular momentum operators are given by the 3x3 matrices:
$J_z = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & -1 \end{pmatrix}$, $J_x = \frac{1}{\sqrt{2}}\begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 1 \\ 0 & 1 & 0 \end{pmatrix}$, $J_y = \frac{1}{\sqrt{2}}\begin{pmatrix} 0 & -i & 0 \\ i & 0 & -i \\ 0 & i & 0 \end{pmatrix}$.
Verify that these matrices satisfy the su(2) commutation relations, e.g., $[J_x, J_y] = iJ_z$.

### Solution 2

a) The dimension is $2(1)+1=3$. This describes a spin-1 particle, like a photon or W boson. The representation space is spanned by the three possible spin projections.

b) The solution correctly notes that the matrices in the problem statement are incorrect. Using the correct matrices for the spin-1 representation of the su(2) algebra:
$J_z = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & -1 \end{pmatrix}$, $J_x = \frac{1}{\sqrt{2}}\begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 1 \\ 0 & 1 & 0 \end{pmatrix}$, $J_y = \frac{i}{\sqrt{2}}\begin{pmatrix} 0 & -1 & 0 \\ 1 & 0 & -1 \\ 0 & 1 & 0 \end{pmatrix}$.
Let's verify the commutation relation $[J_x, J_y] = iJ_z$.
$[J_x, J_y] = J_x J_y - J_y J_x$
$J_x J_y = \frac{1}{\sqrt{2}}\begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 1 \\ 0 & 1 & 0 \end{pmatrix} \frac{i}{\sqrt{2}}\begin{pmatrix} 0 & -1 & 0 \\ 1 & 0 & -1 \\ 0 & 1 & 0 \end{pmatrix} = \frac{i}{2}\begin{pmatrix} 1 & 0 & -1 \\ 0 & 0 & 0 \\ 1 & 0 & -1 \end{pmatrix}$.
$J_y J_x = \frac{i}{\sqrt{2}}\begin{pmatrix} 0 & -1 & 0 \\ 1 & 0 & -1 \\ 0 & 1 & 0 \end{pmatrix} \frac{1}{\sqrt{2}}\begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 1 \\ 0 & 1 & 0 \end{pmatrix} = \frac{i}{2}\begin{pmatrix} -1 & 0 & -1 \\ 0 & 0 & 0 \\ 1 & 0 & 1 \end{pmatrix}$.
$[J_x, J_y] = \frac{i}{2} [(\begin{pmatrix} 1 & 0 & -1 \\ 0 & 0 & 0 \\ 1 & 0 & -1 \end{pmatrix}) - (\begin{pmatrix} -1 & 0 & -1 \\ 0 & 0 & 0 \\ 1 & 0 & 1 \end{pmatrix})] = \frac{i}{2} \begin{pmatrix} 2 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & -2 \end{pmatrix} = i \begin{pmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & -1 \end{pmatrix} = iJ_z$.

