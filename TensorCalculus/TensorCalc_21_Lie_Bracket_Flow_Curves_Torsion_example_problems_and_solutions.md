## Flow Curves

### Problem 1
What is a flow curve of a vector field?

### Solution 1
A flow curve of a vector field $X$ is a curve $\gamma(t)$ whose tangent vector at each point is equal to the vector field at that point: $\frac{d\gamma}{dt} = X(\gamma(t))$.

### Problem 2
Given the vector field $X = -y \partial_x + x \partial_y$, find the flow curves. What do they represent geometrically?

### Solution 2
$\frac{dx}{dt} = -y$, $\frac{dy}{dt} = x$. Differentiating the first gives $\frac{d^2x}{dt^2} = -\frac{dy}{dt} = -x$, so $x'' + x = 0$. The solution is $x(t) = A \cos(t) + B \sin(t)$. Then $y(t) = -\frac{dx}{dt} = A \sin(t) - B \cos(t)$. These are circles centered at the origin.

### Problem 3
Given the vector field $Y = \partial_x$, find the flow curves.

### Solution 3
$\frac{dx}{dt} = 1$, $\frac{dy}{dt} = 0$. $x(t) = t + c_1$, $y(t) = c_2$. These are horizontal lines.

## The Lie Bracket

The Lie bracket of two vector fields $X$ and $Y$ is $[X, Y] = XY - YX$.

### Problem 4
Calculate the Lie bracket $[X, Y]$ for the vector fields $X = -y \partial_x + x \partial_y$ and $Y = \partial_x$.

### Solution 4
$$[X, Y]f = X(Yf) - Y(Xf) = X(\partial_x f) - \partial_x(-y \partial_x f + x \partial_y f)$$
$$= (-y \partial_x + x \partial_y)(\partial_x f) - (-y \partial_x(\partial_x f) + \partial_y(x) \partial_y f + x \partial_y(\partial_x f))$$
$$= -y \partial_x^2 f + x \partial_y \partial_x f + y \partial_x^2 f - \partial_y f - x \partial_x \partial_y f = -\partial_y f$$

So $[X, Y] = -\partial_y$.

### Problem 5
Show that the Lie bracket is anti-symmetric: $[X, Y] = -[Y, X]$.

### Solution 5
$$[X, Y] = XY - YX = -(YX - XY) = -[Y, X]$$

### Problem 6
Show that the Lie bracket satisfies the Jacobi identity: $[X, [Y, Z]] + [Y, [Z, X]] + [Z, [X, Y]] = 0$.

### Solution 6
This can be shown by expanding the definitions of the Lie brackets. It is a fundamental identity in Lie algebra.

### Problem 7
What is the geometric interpretation of the Lie bracket? What does it mean if $[X, Y] = 0$?

### Solution 7
The Lie bracket measures the failure of the flows of two vector fields to commute. If $[X, Y] = 0$, then flowing along $X$ for a short time and then $Y$ for a short time gets you to the same point as flowing along $Y$ and then $X$.

## Torsion

The torsion tensor of a connection $\nabla$ is defined as $T(X, Y) = \nabla_X Y - \nabla_Y X - [X, Y]$.

### Problem 8
What does the torsion tensor measure?

### Solution 8
The torsion tensor measures the failure of infinitesimal parallelograms to close. If the torsion is zero, then moving along $X$ then $Y$ and back along $X$ and $Y$ will form a closed loop.

### Problem 9
Show that for a Levi-Civita connection, the torsion tensor is zero.

### Solution 9
The Levi-Civita connection is defined to be torsion-free.

### Problem 10
In component form, the torsion tensor is $T^k_{ij} = \Gamma^k_{ij} - \Gamma^k_{ji}$. Show that this is equivalent to the abstract definition.

### Solution 10
This can be shown by substituting $X = \partial_i$ and $Y = \partial_j$ into the abstract definition $T(X, Y) = \nabla_X Y - \nabla_Y X - [X, Y]$ and using $[\partial_i, \partial_j] = 0$.