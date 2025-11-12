---
layout: default
title: "The Abstract Covariant Derivative (Levi-Civita Connection)"
---

# Example Problems and Solutions: The Abstract Covariant Derivative (Levi-Civita Connection)

## The Connection

### Problem 1
What is a connection? What does it allow us to do?

### Solution 1
A connection is a mathematical tool that allows us to differentiate tensor fields on a manifold. It provides a way to compare vectors and other tensors at different points, which is necessary to define a derivative.

### Problem 2
What are the properties that define a Levi-Civita connection?

### Solution 2
A Levi-Civita connection is a connection that is:
- **Torsion-free:** $\nabla_X Y - \nabla_Y X = [X, Y]$
- **Metric-compatible:** $\nabla_X (g(Y, Z)) = g(\nabla_X Y, Z) + g(Y, \nabla_X Z)$

## The Covariant Derivative Operator

The covariant derivative can be seen as an operator $\nabla$ that acts on tensor fields. The covariant derivative in the direction of a vector $X$ is denoted $\nabla_X$.

### Problem 3
What are the properties of the operator $\nabla_X$?
a) $\nabla_X(Y + Z) = \nabla_X Y + \nabla_X Z$
b) $\nabla_{fX + gY} Z = f \nabla_X Z + g \nabla_Y Z$
c) $\nabla_X(fY) = (Xf)Y + f \nabla_X Y$
Explain each of these properties in words.

### Solution 3
a) **$\nabla_X(Y + Z) = \nabla_X Y + \nabla_X Z$**: Linearity in the second argument.
b) **$\nabla_{fX + gY} Z = f \nabla_X Z + g \nabla_Y Z$**: Linearity in the first argument.
c) **$\nabla_X(fY) = (Xf)Y + f \nabla_X Y$**: Leibniz rule (product rule) for a scalar function $f$.

### Problem 4
How is $\nabla_X Y$ related to the component definition of the covariant derivative $\nabla_i Y^j$?

### Solution 4
If $X = X^i \partial_i$ and $Y = Y^j \partial_j$, then $\nabla_X Y = X^i \nabla_i Y^j \partial_j$.

## Torsion-Free and Metric Compatibility

### Problem 5
What does it mean for a connection to be torsion-free? Write the condition in both abstract notation and component notation.

### Solution 5
- **Abstract:** $\nabla_X Y - \nabla_Y X = [X, Y]$. It means that infinitesimal parallelograms close.
- **Component:** $\Gamma^k_{ij} = \Gamma^k_{ji}$. The connection coefficients are symmetric in their lower indices.

### Problem 6
What does it mean for a connection to be metric-compatible? Write the condition in both abstract notation and component notation.

### Solution 6
- **Abstract:** $\nabla_X (g(Y, Z)) = g(\nabla_X Y, Z) + g(Y, \nabla_X Z)$. The metric is constant with respect to the connection.
- **Component:** $\nabla_k g_{ij} = 0$. The covariant derivative of the metric tensor is zero.

### Problem 7
Prove that for a given metric, there is a unique connection that is both torsion-free and metric-compatible (the Levi-Civita connection).

### Solution 7
This is a fundamental theorem of Riemannian geometry. The proof involves writing out the metric compatibility condition for $\nabla_X g(Y,Z)$, $\nabla_Y g(Z,X)$, and $\nabla_Z g(X,Y)$, and using the torsion-free condition to derive the Koszul formula, which gives an explicit and unique expression for the connection in terms of the metric.

## Uniqueness of the Levi-Civita Connection

### Problem 8
The Koszul formula provides an explicit expression for the Levi-Civita connection. Write down the Koszul formula and explain what it means.

### Solution 8
$$2g(\nabla_X Y, Z) = X(g(Y,Z)) + Y(g(X,Z)) - Z(g(X,Y)) - g(Y, [X,Z]) - g(X, [Y,Z]) + g(Z, [X,Y])$$

This formula defines the connection $\nabla$ entirely in terms of the metric $g$ and the Lie bracket of vector fields. It shows that the Levi-Civita connection is unique.

### Problem 9
Use the Koszul formula to derive the Christoffel symbols in terms of the metric tensor.

### Solution 9
By substituting $X = \partial_i$, $Y = \partial_j$, $Z = \partial_k$ into the Koszul formula, and using $[\partial_i, \partial_j] = 0$, we can derive the formula for the Christoffel symbols:
$$\Gamma^k_{ij} = \frac{1}{2} g^{kl} (\partial_i g_{jl} + \partial_j g_{il} - \partial_l g_{ij})$$