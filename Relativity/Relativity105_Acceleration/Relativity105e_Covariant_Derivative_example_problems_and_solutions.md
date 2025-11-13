# Relativity 105e: Covariant Derivative - Example Problems and Solutions

## Problem 1

What is the covariant derivative? Why is it necessary in curved spacetime?

### Solution 1

The covariant derivative is a generalization of the partial derivative to curved spacetime. It takes into account the change in the basis vectors from point to point. 

In curved spacetime, the basis vectors are not constant, so the partial derivative of a vector field is not a tensor. When we take a partial derivative $\partial_{\mu} V^{\nu}$, we're comparing the vector $V^{\nu}$ at different points using different basis vectors, which doesn't give us a meaningful geometric quantity.

The covariant derivative is defined in such a way that it:

1. **Is a tensor**: It transforms properly under coordinate transformations
2. **Accounts for basis vector changes**: It includes correction terms (Christoffel symbols) that account for how basis vectors change from point to point
3. **Reduces to partial derivative in flat space**: When the space is flat (Christoffel symbols vanish), it becomes the ordinary partial derivative

## Problem 2

Calculate the covariant derivative of a vector field $V^{\mu}$ with respect to $x^{\nu}$.

### Solution 2

**For a contravariant vector field** $V^{\mu}$:
$$\nabla_{\nu} V^{\mu} = \partial_{\nu} V^{\mu} + \Gamma^{\mu}_{\nu\alpha} V^{\alpha}$$

**For a covariant vector field** $V_{\mu}$:
$$\nabla_{\nu} V_{\mu} = \partial_{\nu} V_{\mu} - \Gamma^{\alpha}_{\nu\mu} V_{\alpha}$$

The key differences are:
- Contravariant indices get a **positive** correction term
- Covariant indices get a **negative** correction term
- Each free index gets its own Christoffel symbol correction

**For tensors with multiple indices**, each index contributes its own correction term. For example, for a tensor $T^{\mu}_{\nu}$:
$$\nabla_{\rho} T^{\mu}_{\nu} = \partial_{\rho} T^{\mu}_{\nu} + \Gamma^{\mu}_{\rho\alpha} T^{\alpha}_{\nu} - \Gamma^{\alpha}_{\rho\nu} T^{\mu}_{\alpha}$$

## Problem 3

What are Christoffel symbols? How are they related to the metric tensor?

### Solution 3

**Christoffel symbols** are coefficients that describe the connection on a manifold. They encode information about how basis vectors change from point to point and are used to define the covariant derivative.

The Christoffel symbols of the second kind are defined as:
$$\Gamma^{\alpha}_{\beta\gamma} = \frac{1}{2} g^{\alpha\delta} \left(\partial_{\beta} g_{\delta\gamma} + \partial_{\gamma} g_{\delta\beta} - \partial_{\delta} g_{\beta\gamma}\right)$$

**Key properties:**

1. **Symmetric in lower indices**: $\Gamma^{\alpha}_{\beta\gamma} = \Gamma^{\alpha}_{\gamma\beta}$

2. **Not tensors**: They don't transform as tensors under coordinate changes (they have inhomogeneous transformation terms)

3. **Vanish in flat space**: In Cartesian coordinates on flat space, all Christoffel symbols are zero

4. **Metric compatibility**: The covariant derivative of the metric tensor vanishes:
   $$\nabla_{\rho} g_{\mu\nu} = \partial_{\rho} g_{\mu\nu} - \Gamma^{\alpha}_{\rho\mu} g_{\alpha\nu} - \Gamma^{\alpha}_{\rho\nu} g_{\mu\alpha} = 0$$

The Christoffel symbols are the unique connection coefficients that make the covariant derivative compatible with the metric tensor (preserving lengths and angles).