# Integration With Differential Forms Examples - Problems and Solutions

## Problem 1: Work Done by a Force

The work done by a force $F$ along a path $C$ is given by the line integral $W = \int_C F \cdot dr$. In the language of differential forms, the force is represented by a 1-form $\omega_F$, and the work done is $W = \int_C \omega_F$.

A force field is given by $F = (x^2, -xy)$. 
a) Write the corresponding 1-form $\omega_F$.
b) Calculate the work done by this force along the path $c(t) = (t, t^2)$ from $t=0$ to $t=1$.

### Solution 1

**A force field is given by $F = (x^2, -xy)$.**

a) **Write the corresponding 1-form $\omega_F$.**

$$\omega_F = x^2 dx - xy dy$$

b) **Calculate the work done by this force along the path $c(t) = (t, t^2)$ from $t=0$ to $t=1$.**

$x(t) = t$, $y(t) = t^2$. $dx = dt$, $dy = 2t dt$.

$$W = \int_C \omega_F = \int_0^1 (t^2(dt) - t(t^2)(2t dt)) = \int_0^1 (t^2 - 2t^4) dt = \left[\frac{t^3}{3} - \frac{2t^5}{5}\right]_0^1 = \frac{1}{3} - \frac{2}{5} = -\frac{1}{15}$$

## Problem 2: Flux Through a Surface

The flux of a vector field $v$ through a surface $S$ is given by $\text{Flux} = \iint_S v \cdot n \, dS$. In the language of differential forms, this can be written as the integral of a 2-form.

A vector field is given by $v = (x, y, z)$. 
a) Construct the corresponding 2-form $\eta_v$ that represents the flux.
b) Calculate the flux of this vector field through the square in the xy-plane with vertices at (0,0,0), (1,0,0), (1,1,0), and (0,1,0).

### Solution 2

**A vector field is given by $v = (x, y, z)$.**

a) **Construct the corresponding 2-form $\eta_v$ that represents the flux.**

$$\eta_v = x \, dy \wedge dz + y \, dz \wedge dx + z \, dx \wedge dy$$

b) **Calculate the flux of this vector field through the square in the xy-plane with vertices at (0,0,0), (1,0,0), (1,1,0), and (0,1,0).**

On this square, $z=0$ and $dz=0$. So $\eta_v$ simplifies to $x \, dy \wedge dz + y \, dz \wedge dx = 0$. The flux is:

$$\iint_S z \, dx \wedge dy = \int_0^1 \int_0^1 0 \, dx \, dy = 0$$

## Problem 3: Change of Variables in Integration

Evaluate the integral $\iint_D (x^2 + y^2) \, dx \, dy$ where $D$ is the disk of radius 2 centered at the origin. Use a change of variables to polar coordinates and differential forms.

### Solution 3

**Evaluate the integral $\iint_D (x^2 + y^2) \, dx \, dy$ where $D$ is the disk of radius 2 centered at the origin. Use a change of variables to polar coordinates and differential forms.**

$x = r \cos(\theta)$, $y = r \sin(\theta)$. $dx = \cos(\theta)dr - r \sin(\theta)d\theta$, $dy = \sin(\theta)dr + r \cos(\theta)d\theta$.

$$dx \wedge dy = (\cos(\theta)dr - r \sin(\theta)d\theta) \wedge (\sin(\theta)dr + r \cos(\theta)d\theta)$$
$$= r \cos^2(\theta)dr \wedge d\theta - r \sin^2(\theta)d\theta \wedge dr = r \, dr \wedge d\theta$$

$$\iint_D (x^2+y^2) \, dx \wedge dy = \int_0^{2\pi} \int_0^2 (r^2) r \, dr \, d\theta = \int_0^{2\pi} \left[\frac{r^4}{4}\right]_0^2 d\theta = \int_0^{2\pi} 4 \, d\theta = 8\pi$$

## Problem 4: Green's Theorem

Green's theorem is a special case of Stokes' theorem. It states that for a region $D$ in the plane with boundary $C$, $\oint_C L \, dx + M \, dy = \iint_D \left(\frac{\partial M}{\partial x} - \frac{\partial L}{\partial y}\right) dA$.

Use Green's theorem to evaluate the line integral $\oint_C (x - y) \, dx + (x + y) \, dy$ where $C$ is the circle $x^2 + y^2 = 1$.
a) First, define the 1-form $\omega = (x - y) \, dx + (x + y) \, dy$.
b) Calculate $d\omega$.
c) Integrate $d\omega$ over the unit disk.

### Solution 4

**Use Green's theorem to evaluate the line integral $\oint_C (x - y) \, dx + (x + y) \, dy$ where $C$ is the circle $x^2 + y^2 = 1$.**

a) **First, define the 1-form $\omega = (x - y) \, dx + (x + y) \, dy$.**

b) **Calculate $d\omega$.**

$$d\omega = \left(\frac{\partial(x+y)}{\partial x} - \frac{\partial(x-y)}{\partial y}\right) dx \wedge dy = (1 - (-1)) \, dx \wedge dy = 2 \, dx \wedge dy$$

c) **Integrate $d\omega$ over the unit disk.**

$$\iint_D 2 \, dx \wedge dy = 2 \times \text{Area(disk)} = 2\pi$$