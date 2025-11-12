## Components of a Covector Field

### Problem 1
A covector field is given by $\boldsymbol{\alpha} = x^2 dx + y^2 dy$. What are the components of this covector field in the Cartesian basis?

### Solution 1
The components are the coefficients of the basis 1-forms $dx$ and $dy$. Therefore:
$$\alpha_x = x^2 \quad \text{and} \quad \alpha_y = y^2$$

### Problem 2
Consider the covector field $\boldsymbol{\beta} = dr$, where $r = \sqrt{x^2 + y^2}$. Find the components of $\boldsymbol{\beta}$ in the Cartesian basis $(dx, dy)$.

### Solution 2
We need to compute the differential of $r$:
$$dr = \frac{\partial r}{\partial x}dx + \frac{\partial r}{\partial y}dy$$

Since $r = \sqrt{x^2 + y^2}$:
$$\frac{\partial r}{\partial x} = \frac{x}{\sqrt{x^2 + y^2}} = \frac{x}{r}$$
$$\frac{\partial r}{\partial y} = \frac{y}{\sqrt{x^2 + y^2}} = \frac{y}{r}$$

Therefore:
$$dr = \frac{x}{r}dx + \frac{y}{r}dy = \frac{x}{\sqrt{x^2+y^2}}dx + \frac{y}{\sqrt{x^2+y^2}}dy$$

The components are:
$$\beta_x = \frac{x}{\sqrt{x^2+y^2}} \quad \text{and} \quad \beta_y = \frac{y}{\sqrt{x^2+y^2}}$$

### Problem 3
A covector field is given in polar coordinates by $\boldsymbol{\gamma} = r^2 d\theta$. Find the components of $\boldsymbol{\gamma}$ in the Cartesian basis $(dx, dy)$.

### Solution 3
We need to express $d\theta$ in terms of $dx$ and $dy$. Since $\theta = \arctan(y/x)$:
$$d\theta = \frac{\partial \theta}{\partial x}dx + \frac{\partial \theta}{\partial y}dy$$

Computing the partial derivatives:
$$\frac{\partial \theta}{\partial x} = \frac{-y}{x^2 + y^2} = -\frac{y}{r^2}$$
$$\frac{\partial \theta}{\partial y} = \frac{x}{x^2 + y^2} = \frac{x}{r^2}$$

Therefore:
$$d\theta = -\frac{y}{r^2}dx + \frac{x}{r^2}dy$$

Substituting into $\boldsymbol{\gamma}$:
$$\boldsymbol{\gamma} = r^2 \left(-\frac{y}{r^2}dx + \frac{x}{r^2}dy\right) = -y \, dx + x \, dy$$

The components are:
$$\gamma_x = -y \quad \text{and} \quad \gamma_y = x$$

## Transformation of Covector Components

### Problem 4
The components of a covector field in Cartesian coordinates are $\alpha_x = 2x$ and $\alpha_y = 2y$. Find the components of this covector field in polar coordinates, $\alpha_r$ and $\alpha_\theta$.

### Solution 4
Using the covariant transformation rule:
$$\alpha'_j = \frac{\partial x^i}{\partial x'^j} \alpha_i$$

For polar coordinates:
$$\alpha_r = \frac{\partial x}{\partial r}\alpha_x + \frac{\partial y}{\partial r}\alpha_y$$
$$\alpha_\theta = \frac{\partial x}{\partial \theta}\alpha_x + \frac{\partial y}{\partial \theta}\alpha_y$$

The partial derivatives are:
$$\frac{\partial x}{\partial r} = \cos(\theta), \quad \frac{\partial y}{\partial r} = \sin(\theta)$$
$$\frac{\partial x}{\partial \theta} = -r\sin(\theta), \quad \frac{\partial y}{\partial \theta} = r\cos(\theta)$$

Therefore:
$$\alpha_r = \cos(\theta)(2x) + \sin(\theta)(2y) = 2(x\cos(\theta) + y\sin(\theta))$$

Since $x = r\cos(\theta)$ and $y = r\sin(\theta)$:
$$\alpha_r = 2(r\cos^2(\theta) + r\sin^2(\theta)) = 2r$$

$$\alpha_\theta = -r\sin(\theta)(2x) + r\cos(\theta)(2y) = 2r(-x\sin(\theta) + y\cos(\theta))$$
$$= 2r(-r\cos(\theta)\sin(\theta) + r\sin(\theta)\cos(\theta)) = 0$$

The components are $(2r, 0)$.

### Problem 5
A covector field has components $\beta_r = 1$ and $\beta_\theta = r$ in polar coordinates. Find its components in Cartesian coordinates.

### Solution 5
Using the covariant transformation rule in the reverse direction:
$$\beta_x = \frac{\partial r}{\partial x}\beta_r + \frac{\partial \theta}{\partial x}\beta_\theta$$
$$\beta_y = \frac{\partial r}{\partial y}\beta_r + \frac{\partial \theta}{\partial y}\beta_\theta$$

We have:
$$\frac{\partial r}{\partial x} = \frac{x}{r}, \quad \frac{\partial r}{\partial y} = \frac{y}{r}$$
$$\frac{\partial \theta}{\partial x} = -\frac{y}{r^2}, \quad \frac{\partial \theta}{\partial y} = \frac{x}{r^2}$$

Therefore:
$$\beta_x = \frac{x}{r} \cdot 1 + \left(-\frac{y}{r^2}\right) \cdot r = \frac{x}{r} - \frac{y}{r} = \frac{x-y}{r}$$

$$\beta_y = \frac{y}{r} \cdot 1 + \frac{x}{r^2} \cdot r = \frac{y}{r} + \frac{x}{r} = \frac{x+y}{r}$$

The components are:
$$\left(\frac{x-y}{\sqrt{x^2+y^2}}, \frac{x+y}{\sqrt{x^2+y^2}}\right)$$

## Line Integrals of Covector Fields

### Problem 6
Evaluate the line integral of the covector field $\boldsymbol{\alpha} = y \, dx - x \, dy$ along the path $\mathbf{c}(t) = (\cos(t), \sin(t))$ from $t=0$ to $t=\pi$.

### Solution 6
For the parametric path $\mathbf{c}(t) = (\cos(t), \sin(t))$:
$$x(t) = \cos(t), \quad y(t) = \sin(t)$$
$$dx = -\sin(t) \, dt, \quad dy = \cos(t) \, dt$$

The line integral is:
$$\int_C \boldsymbol{\alpha} = \int_0^\pi [y \, dx - x \, dy]$$
$$= \int_0^\pi [\sin(t)(-\sin(t) \, dt) - \cos(t)(\cos(t) \, dt)]$$
$$= \int_0^\pi [-\sin^2(t) - \cos^2(t)] \, dt$$
$$= \int_0^\pi -1 \, dt = -\pi$$

### Problem 7
Consider the covector field $\boldsymbol{\beta} = df$ where $f(x, y, z) = xyz$. Evaluate the line integral of $\boldsymbol{\beta}$ from the point $(0, 0, 0)$ to $(1, 2, 3)$ along the straight line path connecting them.

### Solution 7
Since $\boldsymbol{\beta} = df$ is an exact differential, we can use the fundamental theorem of calculus for line integrals:

$$\int_C df = f(\text{end point}) - f(\text{start point})$$

Evaluating $f$ at the endpoints:
$$f(1, 2, 3) = 1 \cdot 2 \cdot 3 = 6$$
$$f(0, 0, 0) = 0 \cdot 0 \cdot 0 = 0$$

Therefore:
$$\int_C \boldsymbol{\beta} = 6 - 0 = 6$$

This result is independent of the specific path taken, as long as it connects the two points.