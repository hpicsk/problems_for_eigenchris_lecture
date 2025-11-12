# SfB 20: Lorentz Representations - Example Problems

This lecture covers how different types of fields (scalars, vectors, spinors) transform under Lorentz transformations.

## Problem 1: The Lorentz Group

The Lorentz group is the group of linear transformations $\Lambda$ that preserve the Minkowski metric $\eta$.
$\Lambda^T \eta \Lambda = \eta$
In index notation: $\Lambda^\mu{} _\alpha \Lambda^\nu{} _\beta \eta_{\mu\nu} = \eta_{\alpha\beta}$.

a) A boost in the x-direction is given by the matrix:
   $\Lambda = \begin{pmatrix} \gamma & -\gamma\beta & 0 & 0 \\ -\gamma\beta & \gamma & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$, where $\beta=v/c$ and $\gamma=1/\sqrt{1-\beta^2}$.
   Verify that this matrix is indeed a Lorentz transformation.
b) A rotation around the z-axis is also a Lorentz transformation. Write down the matrix for this transformation and verify it.
c) Show that the set of all Lorentz transformations forms a group.

## Problem 2: Scalar Fields (The Trivial Representation)

A scalar field $\phi(x)$ transforms under a Lorentz transformation $x \rightarrow x'$ = $\Lambda x$ as:
$\phi'(x') = \phi(x)$
or $\phi'(x) = \phi(\Lambda^{-1}x)$.

a) The Klein-Gordon equation is $(\Box + m^2)\phi(x) = 0$. Show that this equation is Lorentz invariant.
   (Hint: Show that the D'Alembertian operator $\Box = \partial_\mu \partial^\mu$ is invariant).
b) Why is this called the "(0,0)" representation?

## Problem 3: Vector Fields (The (1/2, 1/2) Representation)

A 4-vector field $A^\mu(x)$ transforms as:
$A'^\mu(x') = \Lambda^\mu{}_\nu A^\nu(x)$

a) The Maxwell equations in terms of the 4-vector potential are $\Box A^\mu - \partial^\mu(\partial_\nu A^\nu) = j^\mu$.
   Show that if the Lorenz gauge condition $\partial_\nu A^\nu = 0$ is imposed, the equation becomes $\Box A^\mu = j^\mu$.
b) Show that this equation is Lorentz covariant if the current $j^\mu$ also transforms as a vector.
c) The field strength tensor is $F^{\mu\nu} = \partial^\mu A^\nu - \partial^\nu A^\mu$. How does this tensor transform under a Lorentz transformation?
   $F'^{\mu\nu}(x') = ?$

## Problem 4: Spinor Fields (The (1/2, 0) and (0, 1/2) Representations)

The Lorentz algebra has the same complexification as SU(2) x SU(2). This leads to representations labeled by two half-integers $(j_L, j_R)$.
A Dirac spinor $\psi$ is in the $(\frac{1}{2}, 0) \oplus (0, \frac{1}{2})$ representation. It transforms as:
$\Psi'(x') = S[\Lambda] \Psi(x)$
where $S[\Lambda]$ is a 4x4 matrix that depends on the Lorentz transformation $\Lambda$.
$S[\Lambda] = \exp(-\frac{i}{4}\omega_{\mu\nu}\sigma^{\mu\nu})$, where $\sigma^{\mu\nu} = \frac{i}{2}[\gamma^\mu, \gamma^\nu]$ are the generators of the representation.

a) The generators of rotations are $J_i = \frac{1}{2}\epsilon_{ijk}\sigma^{jk}$. The generators of boosts are $K_i = \sigma^{0i}$.
   Calculate the generator for a boost in the x-direction, $K_1$.
b) Calculate the transformation matrix $S[\Lambda]$ for an infinitesimal boost in the x-direction with velocity $\delta v$.
c) The Dirac equation is $(i\gamma^\mu\partial_\mu - m)\Psi = 0$. Show that this equation is Lorentz covariant.
   (Hint: You need to show that $S^{-1}\gamma^\mu S = \Lambda^\mu{}_\nu \gamma^\nu$).

## Problem 5: Classifying Representations

The representations of the Lorentz group are classified by $(j_L, j_R)$.
- (0,0): Scalar
- $(\frac{1}{2}, 0)$: Left-handed Weyl spinor
- $(0, \frac{1}{2})$: Right-handed Weyl spinor
- $(\frac{1}{2}, \frac{1}{2})$: 4-vector
- $(\frac{1}{2}, 0) \oplus (0, \frac{1}{2})$: Dirac spinor
- $(1,0) \oplus (0,1)$: Antisymmetric tensor (like $F^{\mu\nu}$)

a) How many components does a field in the $(j_L, j_R)$ representation have?
b) What is the representation for a symmetric, traceless 2-index tensor?
c) Can you construct a Lorentz invariant quantity from a left-handed and a right-handed spinor?
d) Can you construct a Lorentz invariant quantity from two left-handed spinors?

# Solutions to Example Problems: Representations of the Lorentz Group

## Problem 1: The Lorentz Group

a) **Verify that this matrix is indeed a Lorentz transformation.**
$\Lambda^T \eta \Lambda = \eta$. Yes, it is.

b) **A rotation around the z-axis is also a Lorentz transformation. Write down the matrix for this transformation and verify it.**
$\Lambda$ for a z-rotation is a block matrix with 1 in the top-left and a 2D rotation matrix in the xy-block. It preserves the metric.

c) **Show that the set of all Lorentz transformations forms a group.**
Closure, Identity, Inverse, Associativity all hold.

## Problem 2: Scalar Fields (The Trivial Representation)

a) **Show that the Klein-Gordon equation is Lorentz invariant.**
The D'Alembertian operator $\Box = \partial_\mu \partial^\mu$ is a scalar product of two 4-vectors, so it is Lorentz invariant.

b) **Why is this called the "(0,0)" representation?**
Because it corresponds to the irrep of the Lorentz algebra with $j_L=0$ and $j_R=0$.

## Problem 3: Vector Fields (The (1/2, 1/2) Representation)

a) **Show that if the Lorenz gauge condition $\partial_\nu A^\nu = 0$ is imposed, the equation becomes $\Box A^\mu = j^\mu$.**
This is immediate from the given equation.

b) **Show that this equation is Lorentz covariant.**
$\Box$ is invariant. If $A^\mu$ and $j^\mu$ transform as vectors, then both sides of the equation transform in the same way.

c) **How does this tensor transform under a Lorentz transformation?**
$F'^{\mu\nu}(x\') = \Lambda^\mu_\alpha \Lambda^\nu_\beta F^{\alpha\beta}(x)$.

## Problem 4: Spinor Fields

a) **Calculate the generator for a boost in the x-direction, $K_1$.**
$K_1 = \sigma^{01} = \frac{i}{2}[\gamma^0, \gamma^1]$.

b) **Calculate the transformation matrix $S[\Lambda]$ for an infinitesimal boost.**
$S = I - \frac{i}{2}\eta \sigma^{01} = I + \frac{\eta}{4}[\gamma^0, \gamma^1]$.

c) **Show that the Dirac equation is Lorentz covariant.**
This requires showing that $S^{-1}\gamma^\mu S = \Lambda^\mu{}_\nu \gamma^\nu$. This is a standard result.

## Problem 5: Classifying Representations

a) **How many components does a field in the $(j_L, j_R)$ representation have?**
$(2j_L+1)(2j_R+1)$ components.

b) **What is the representation for a symmetric, traceless 2-index tensor?**
This is the (1,1) representation.

c) **Can you construct a Lorentz invariant quantity from a left-handed and a right-handed spinor?**
Yes. $\psi_L^\dagger \psi_R$ is Lorentz invariant.

d) **Can you construct a Lorentz invariant quantity from two left-handed spinors?**
Yes. $\psi_L^T \sigma_2 \psi_L$ is Lorentz invariant. This is a Majorana mass term.