
This lecture discusses the representations of the Lorentz group, which are crucial for classifying elementary particles.

## Problem 1: The Lie Algebra of the Lorentz Group

The Lie algebra of the Lorentz group SO(1,3) is denoted so(1,3). It is a 6-dimensional algebra whose elements can be seen as generators of rotations and boosts.
The generators can be written as $M_{\mu\nu}$ with the commutation relations:
$[M_{\mu\nu}, M_{\rho\sigma}] = i(\eta_{\mu\sigma}M_{\nu\rho} - \eta_{\mu\rho}M_{\nu\sigma} - \eta_{\nu\sigma}M_{\mu\rho} + \eta_{\nu\rho}M_{\mu\sigma})$

a) The generators of rotations are $J_i = \frac{1}{2}\epsilon_{ijk}M_{jk}$ and the generators of boosts are $K_i = M_{0i}$. Show that the commutation relations for the $J_i$ are the same as for su(2), i.e., $[J_i, J_j] = i\epsilon_{ijk}J_k$.

b) Calculate the commutation relations for boosts, $[K_i, K_j]$.

c) Calculate the commutation relations between rotations and boosts, $[J_i, K_j]$.

### Solution 1

a) This is a standard but lengthy calculation involving the epsilon tensor identities. The result is that the rotation generators form a closed subalgebra, which is the Lie algebra of SO(3).

b) $[K_i, K_j] = [M_{0i}, M_{0j}] = i(\eta_{0j}M_{i0} - \eta_{00}M_{ij} - \eta_{ij}M_{00} + \eta_{i0}M_{0j}) = i(-M_{ij}) = -i\epsilon_{ijk}J_k$.
This shows that boosts do not form a closed subalgebra.

c) $[J_i, K_j] = i\epsilon_{ik\ell}K_\ell$. This means that the boost generators transform as a vector under rotations, as expected.

## Problem 2: Decomposing the Lorentz Algebra

The Lorentz algebra so(1,3) can be decomposed into two copies of su(2).
Define $A_i = \frac{1}{2}(J_i + iK_i)$ and $B_i = \frac{1}{2}(J_i - iK_i)$.

a) Show that the A operators and B operators satisfy the su(2) commutation relations, i.e., $[A_i, A_j] = i\epsilon_{ijk}A_k$ and $[B_i, B_j] = i\epsilon_{ijk}B_k$.

b) Show that $[A_i, B_j] = 0$. This means that the Lorentz algebra is a direct sum of two su(2) algebras: $so(1,3) \cong su(2) \oplus su(2)$.

### Solution 2

a) $[A_i, A_j] = \frac{1}{4}[J_i+iK_i, J_j+iK_j] = \frac{1}{4}([J_i,J_j] - [K_i,K_j] + i[J_i,K_j] + i[K_i,J_j])$.
Using the results from Problem 1:
$[J_i,J_j] = i\epsilon_{ijk}J_k$
$[K_i,K_j] = -i\epsilon_{ijk}J_k$
$[J_i,K_j] = i\epsilon_{ijk}K_k$
$[K_i,J_j] = -[J_j,K_i] = -i\epsilon_{jik}K_k = i\epsilon_{ijk}K_k$
Substituting these into the expression for $[A_i, A_j]$:
$[A_i, A_j] = \frac{1}{4}(i\epsilon_{ijk}J_k - (-i\epsilon_{ijk}J_k) + i(i\epsilon_{ijk}K_k) + i(i\epsilon_{ijk}K_k))$
$= \frac{1}{4}(2i\epsilon_{ijk}J_k - 2\epsilon_{ijk}K_k) = \frac{i\epsilon_{ijk}}{2}(J_k + iK_k) = i\epsilon_{ijk}A_k$.
The calculation for B is similar.

b) $[A_i, B_j] = \frac{1}{4}[J_i+iK_i, J_j-iK_j] = \frac{1}{4}([J_i,J_j] + [K_i,K_j] - i[J_i,K_j] + i[K_i,J_j])$.
$= \frac{1}{4}(i\epsilon_{ijk}J_k - i\epsilon_{ijk}J_k - i(i\epsilon_{ijk}K_k) + i(-i\epsilon_{ijk}K_k)) = 0$.

## Problem 3: Representations of the Lorentz Group

The irreducible representations of the Lorentz group can be labeled by a pair of half-integers $(j_A, j_B)$ corresponding to the two su(2) algebras.

a) The scalar representation corresponds to $(0,0)$. What is its dimension?

b) The left-handed Weyl spinor representation is $(1/2, 0)$. What is its dimension? How does it transform under rotations and boosts?

c) The right-handed Weyl spinor representation is $(0, 1/2)$.

d) The Dirac spinor is a combination of a left-handed and a right-handed Weyl spinor: $(1/2,0) \oplus (0,1/2)$. What is its dimension?

### Solution 3

a) Dimension is $(2(0)+1)(2(0)+1)=1$. It is invariant under all Lorentz transformations.

b) Dimension is $(2(1/2)+1)(2(0)+1)=2$. It transforms as a spin-1/2 object under rotations, but feels boosts in a complex way.

c) Dimension is $(2(0)+1)(2(1/2)+1)=2$.

d) Dimension is $2+2=4$. This is the familiar 4-component Dirac spinor.

