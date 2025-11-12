# TensorCalc 06: Differential Forms are Covectors - Example Problems and Solutions

## Covectors (1-forms)

### Problem 1
What is a covector (or 1-form)? How is it different from a vector?

### Solution 1
A covector (or 1-form) is a linear map from the space of vectors to the real numbers. While a vector can be visualized as an arrow pointing in a direction, a covector can be visualized as a set of parallel planes or level surfaces.

The key differences:
- **Vector**: Has magnitude and direction, transforms contravariantly
- **Covector**: Is a linear functional that assigns numbers to vectors, transforms covariantly

The value of the covector acting on a vector represents how many "surfaces" the vector pierces. Geometrically, if we think of a covector as level surfaces of a function, then applying the covector to a vector gives the rate of change of that function along the vector direction.

### Problem 2
Given a covector $df$ defined as the gradient of a function $f(x, y) = x^2y$, and a vector $\mathbf{v} = (3, 2)$, calculate $df(\mathbf{v})$.

### Solution 2
The differential of $f$ is:
$$df = \frac{\partial f}{\partial x}dx + \frac{\partial f}{\partial y}dy = 2xy \, dx + x^2 \, dy$$

This gives us the covector with components $(2xy, x^2)$ in the coordinate basis $\{dx, dy\}$.

To compute $df(\mathbf{v})$, we need to specify a point. Let's evaluate at the point $(x,y) = (1,1)$:
$$df|_{(1,1)} = 2 \cdot 1 \cdot 1 \, dx + 1^2 \, dy = 2 \, dx + 1 \, dy$$

Therefore:
$$df(\mathbf{v}) = (2, 1) \cdot (3, 2) = 2 \cdot 3 + 1 \cdot 2 = 8$$

### Problem 3
The components of a covector $\boldsymbol{\alpha}$ in the Cartesian basis are $(2, 1)$. What are the components of $\boldsymbol{\alpha}$ in the polar basis at the point $(r, \theta) = (1, \pi/4)$?

### Solution 3
Covector components transform according to:
$$\alpha'_j = \frac{\partial x^i}{\partial x'^j} \alpha_i$$

For the transformation from Cartesian to polar coordinates:
- $x = r\cos(\theta)$, $y = r\sin(\theta)$

The partial derivatives are:
$$\frac{\partial x}{\partial r} = \cos(\theta), \quad \frac{\partial y}{\partial r} = \sin(\theta)$$
$$\frac{\partial x}{\partial \theta} = -r\sin(\theta), \quad \frac{\partial y}{\partial \theta} = r\cos(\theta)$$

At the point $(r, \theta) = (1, \pi/4)$:
$$\alpha_r = \frac{\partial x}{\partial r}\alpha_x + \frac{\partial y}{\partial r}\alpha_y = \cos(\pi/4) \cdot 2 + \sin(\pi/4) \cdot 1$$
$$= \frac{\sqrt{2}}{2} \cdot 2 + \frac{\sqrt{2}}{2} \cdot 1 = \frac{3\sqrt{2}}{2}$$

$$\alpha_\theta = \frac{\partial x}{\partial \theta}\alpha_x + \frac{\partial y}{\partial \theta}\alpha_y = -r\sin(\pi/4) \cdot 2 + r\cos(\pi/4) \cdot 1$$
$$= -1 \cdot \frac{\sqrt{2}}{2} \cdot 2 + 1 \cdot \frac{\sqrt{2}}{2} \cdot 1 = -\frac{\sqrt{2}}{2}$$

The components are $\left(\frac{3\sqrt{2}}{2}, -\frac{\sqrt{2}}{2}\right)$.

## Differential Forms

### Problem 4
What is a differential k-form? Give examples for k=0, 1, and 2.

### Solution 4
A differential k-form is a totally antisymmetric tensor field of rank k that can be integrated over k-dimensional manifolds.

Examples:
- **k=0**: A scalar function (0-form), e.g., $f(x,y,z) = x^2 + y^2 + z^2$
- **k=1**: A covector field (1-form), e.g., $\omega = A_x dx + A_y dy + A_z dz$
- **k=2**: A 2-form, e.g., $\eta = B_{xy} dx \wedge dy + B_{xz} dx \wedge dz + B_{yz} dy \wedge dz$

### Problem 5
What is the wedge product? Calculate the wedge product of the 1-forms $dx$ and $dy$.

### Solution 5
The wedge product $\wedge$ is an antisymmetric product for differential forms. It satisfies:
- Antisymmetry: $\alpha \wedge \beta = (-1)^{pq} \beta \wedge \alpha$ where $\alpha$ is a p-form and $\beta$ is a q-form
- $\alpha \wedge \alpha = 0$ for any odd-degree form

For the basis 1-forms:
$$dx \wedge dy = -dy \wedge dx$$

This is a 2-form that represents an oriented area element.

### Problem 6
Given the 1-form $\omega = x \, dx - y \, dy$ and the 1-form $\eta = y \, dx + x \, dy$, calculate $\omega \wedge \eta$.

### Solution 6
$$\omega \wedge \eta = (x \, dx - y \, dy) \wedge (y \, dx + x \, dy)$$

Expanding using the distributive property:
$$= x \, dx \wedge (y \, dx + x \, dy) - y \, dy \wedge (y \, dx + x \, dy)$$
$$= xy \, dx \wedge dx + x^2 \, dx \wedge dy - y^2 \, dy \wedge dx - yx \, dy \wedge dy$$

Using $dx \wedge dx = 0$, $dy \wedge dy = 0$, and $dy \wedge dx = -dx \wedge dy$:
$$= 0 + x^2 \, dx \wedge dy - y^2 (-dx \wedge dy) - 0$$
$$= x^2 \, dx \wedge dy + y^2 \, dx \wedge dy$$
$$= (x^2 + y^2) dx \wedge dy$$

### Problem 7
What is the exterior derivative $d$? Calculate the exterior derivative of the following forms:

a) $f(x, y) = x^2y$ (a 0-form)

b) $\omega = x^2 dx + y^2 dy$ (a 1-form)

c) $\eta = xy \, dx \wedge dy$ (a 2-form)

### Solution 7
The exterior derivative $d$ takes a k-form to a (k+1)-form and satisfies $d^2 = 0$.

a) For a 0-form (scalar function):
$$df = \frac{\partial f}{\partial x}dx + \frac{\partial f}{\partial y}dy = 2xy \, dx + x^2 \, dy$$

b) For the 1-form $\omega = x^2 dx + y^2 dy$:
$$d\omega = d(x^2) \wedge dx + d(y^2) \wedge dy$$
$$= (2x \, dx) \wedge dx + (2y \, dy) \wedge dy$$
$$= 2x \, dx \wedge dx + 2y \, dy \wedge dy = 0$$

(since $dx \wedge dx = 0$ and $dy \wedge dy = 0$)

c) For the 2-form $\eta = xy \, dx \wedge dy$:
$$d\eta = d(xy) \wedge dx \wedge dy$$
$$= (y \, dx + x \, dy) \wedge dx \wedge dy$$
$$= y \, dx \wedge dx \wedge dy + x \, dy \wedge dx \wedge dy$$

Since $dx \wedge dx = 0$ and $dy \wedge dx \wedge dy = -dx \wedge dy \wedge dy = 0$:
$$d\eta = 0$$

## Covectors as Linear Functionals

### Problem 8
Explain how a covector can be thought of as a linear functional that acts on vectors to produce a scalar.

### Solution 8
A covector is defined as a linear map from the vector space to the real numbers. This means that for any vector $\mathbf{v}$, the covector $\boldsymbol{\alpha}$ produces a number $\boldsymbol{\alpha}(\mathbf{v})$, and this map is linear:

$$\boldsymbol{\alpha}(a\mathbf{v} + b\mathbf{w}) = a\boldsymbol{\alpha}(\mathbf{v}) + b\boldsymbol{\alpha}(\mathbf{w})$$

In component notation, if $\boldsymbol{\alpha}$ has components $\alpha_i$ and $\mathbf{v}$ has components $v^i$, then:
$$\boldsymbol{\alpha}(\mathbf{v}) = \alpha_i v^i$$

This is the natural pairing between covectors and vectors that produces a scalar invariant under coordinate transformations.

### Problem 9
Let $df$ be the differential of the function $f(x,y) = x^2 + y^2$. Let $\mathbf{v}$ be the vector field $\mathbf{v} = x \frac{\partial}{\partial x} + y \frac{\partial}{\partial y}$. Compute $df(\mathbf{v})$.

### Solution 9
First, find the differential:
$$df = \frac{\partial f}{\partial x}dx + \frac{\partial f}{\partial y}dy = 2x \, dx + 2y \, dy$$

The vector $\mathbf{v}$ has components $(x, y)$ in the coordinate basis $\{\frac{\partial}{\partial x}, \frac{\partial}{\partial y}\}$.

Therefore:
$$df(\mathbf{v}) = (2x \, dx + 2y \, dy)\left(x \frac{\partial}{\partial x} + y \frac{\partial}{\partial y}\right)$$

Using the fact that $dx\left(\frac{\partial}{\partial x}\right) = 1$, $dx\left(\frac{\partial}{\partial y}\right) = 0$, etc.:
$$df(\mathbf{v}) = 2x \cdot x + 2y \cdot y = 2x^2 + 2y^2 = 2(x^2 + y^2)$$