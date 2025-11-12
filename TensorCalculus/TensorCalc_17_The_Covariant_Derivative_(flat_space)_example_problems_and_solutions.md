# Example Problems and Solutions: The Covariant Derivative (flat space)

## The Covariant Derivative

### Problem 1
What is the motivation for defining the covariant derivative? Why can't we just use the partial derivative?

### Solution 1
The partial derivative of a vector field's components does not transform as a tensor. This is because the basis vectors themselves change from point to point. The covariant derivative includes correction terms (the Christoffel symbols) to account for the changing basis, ensuring that the result is a well-behaved tensor.

### Problem 2
The covariant derivative of a vector field $V$ with components $V^j$ is given by $\nabla_i V^j = \partial_i V^j + \Gamma^j_{ik} V^k$. 
a) Calculate the covariant derivative of a vector field $V$ in 2D Cartesian coordinates.
b) Calculate the covariant derivative of a vector field $V$ in 2D polar coordinates.

### Solution 2
a) **Calculate the covariant derivative of a vector field $V$ in 2D Cartesian coordinates.**

In Cartesian coordinates, all Christoffel symbols are zero. So, $\nabla_i V^j = \partial_i V^j$. The covariant derivative is the same as the partial derivative.

b) **Calculate the covariant derivative of a vector field $V$ in 2D polar coordinates.**

$$\nabla_r V^r = \partial_r V^r + \Gamma^r_{rr}V^r + \Gamma^r_{r\theta}V^{\theta} = \partial_r V^r$$
$$\nabla_{\theta} V^r = \partial_{\theta} V^r + \Gamma^r_{\theta r}V^r + \Gamma^r_{\theta \theta}V^{\theta} = \partial_{\theta} V^r - r V^{\theta}$$
$$\nabla_r V^{\theta} = \partial_r V^{\theta} + \Gamma^{\theta}_{rr}V^r + \Gamma^{\theta}_{r\theta}V^{\theta} = \partial_r V^{\theta} + \frac{1}{r}V^{\theta}$$
$$\nabla_{\theta} V^{\theta} = \partial_{\theta} V^{\theta} + \Gamma^{\theta}_{\theta r}V^r + \Gamma^{\theta}_{\theta \theta}V^{\theta} = \partial_{\theta} V^{\theta} + \frac{1}{r}V^r$$

### Problem 3
The covariant derivative of a covector field $\alpha$ with components $\alpha_j$ is given by $\nabla_i \alpha_j = \partial_i \alpha_j - \Gamma^k_{ij} \alpha_k$.
a) Calculate the covariant derivative of a covector field $\alpha$ in 2D Cartesian coordinates.
b) Calculate the covariant derivative of a covector field $\alpha$ in 2D polar coordinates.

### Solution 3
a) **Calculate the covariant derivative of a covector field $\alpha$ in 2D Cartesian coordinates.**

$\nabla_i \alpha_j = \partial_i \alpha_j$. Same as the partial derivative.

b) **Calculate the covariant derivative of a covector field $\alpha$ in 2D polar coordinates.**

$$\nabla_r \alpha_r = \partial_r \alpha_r - \Gamma^r_{rr}\alpha_r - \Gamma^{\theta}_{rr}\alpha_{\theta} = \partial_r \alpha_r$$
$$\nabla_{\theta} \alpha_r = \partial_{\theta} \alpha_r - \Gamma^r_{\theta r}\alpha_r - \Gamma^{\theta}_{\theta r}\alpha_{\theta} = \partial_{\theta} \alpha_r - \frac{1}{r}\alpha_{\theta}$$
$$\nabla_r \alpha_{\theta} = \partial_r \alpha_{\theta} - \Gamma^r_{r\theta}\alpha_r - \Gamma^{\theta}_{r\theta}\alpha_{\theta} = \partial_r \alpha_{\theta} - \frac{1}{r}\alpha_{\theta}$$
$$\nabla_{\theta} \alpha_{\theta} = \partial_{\theta} \alpha_{\theta} - \Gamma^r_{\theta \theta}\alpha_r - \Gamma^{\theta}_{\theta \theta}\alpha_{\theta} = \partial_{\theta} \alpha_{\theta} + r \alpha_r$$

## Properties of the Covariant Derivative

### Problem 4
Show that the covariant derivative is linear.

### Solution 4
$$\nabla_i (aV^j + bW^j) = \partial_i(aV^j + bW^j) + \Gamma^j_{ik}(aV^k + bW^k)$$
$$= a(\partial_iV^j + \Gamma^j_{ik}V^k) + b(\partial_iW^j + \Gamma^j_{ik}W^k) = a\nabla_iV^j + b\nabla_iW^j$$

### Problem 5
Show that the covariant derivative obeys the product rule for a tensor product of a vector and a covector.

### Solution 5
$$\nabla_k (V^i \alpha_j) = \partial_k(V^i \alpha_j) + \Gamma^i_{kl}V^l \alpha_j - \Gamma^l_{kj}V^i \alpha_l$$
$$= (\partial_k V^i)\alpha_j + V^i(\partial_k \alpha_j) + \Gamma^i_{kl}V^l \alpha_j - \Gamma^l_{kj}V^i \alpha_l$$
$$= (\nabla_k V^i)\alpha_j + V^i(\nabla_k \alpha_j)$$

### Problem 6
What is the covariant derivative of the metric tensor $g_{ij}$? (This is known as metric compatibility.)

### Solution 6
The covariant derivative of the metric tensor is zero: $\nabla_k g_{ij} = 0$. This is a fundamental property of the Levi-Civita connection.

## Covariant Derivative of Higher-Rank Tensors

### Problem 7
Write down the formula for the covariant derivative of a rank-2 tensor $T^{ij}$.

### Solution 7
$$\nabla_k T^{ij} = \partial_k T^{ij} + \Gamma^i_{kl} T^{lj} + \Gamma^j_{kl} T^{il}$$

### Problem 8
Write down the formula for the covariant derivative of a rank-2 tensor $T_{ij}$.

### Solution 8
$$\nabla_k T_{ij} = \partial_k T_{ij} - \Gamma^l_{ki} T_{lj} - \Gamma^l_{kj} T_{il}$$

### Problem 9
Write down the formula for the covariant derivative of a mixed tensor $T^i_j$.

### Solution 9
$$\nabla_k T^i_j = \partial_k T^i_j + \Gamma^i_{kl} T^l_j - \Gamma^l_{kj} T^i_l$$