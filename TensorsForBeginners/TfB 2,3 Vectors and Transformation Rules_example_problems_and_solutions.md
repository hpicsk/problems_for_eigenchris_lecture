# TfB 2,3 Vectors and Transformation Rules - Example Problems and Solutions

## Problem 1
A vector $\mathbf{v}$ has components $(1, 2)$ in the standard basis $\{\mathbf{e_1}, \mathbf{e_2}\}$. A new basis $\{\mathbf{e'_1}, \mathbf{e'_2}\}$ is given by $\mathbf{e'_1} = 2\mathbf{e_1} + \mathbf{e_2}$ and $\mathbf{e'_2} = \mathbf{e_1} - \mathbf{e_2}$. What are the components of $\mathbf{v}$ in this new basis?

## Solution 1
The change of basis matrix from the new basis to the old is 
$$P = \begin{bmatrix} 2 & 1 \\ 1 & -1 \end{bmatrix}$$
The new components $\mathbf{v}'$ are given by $\mathbf{v}' = P^{-1} \mathbf{v}$.

$$P^{-1} = \frac{1}{(-2-1)} \begin{bmatrix} -1 & -1 \\ -1 & 2 \end{bmatrix} = \frac{1}{3} \begin{bmatrix} 1 & 1 \\ 1 & -2 \end{bmatrix}$$

$$\mathbf{v}' = \frac{1}{3} \begin{bmatrix} 1 & 1 \\ 1 & -2 \end{bmatrix} \begin{bmatrix} 1 \\ 2 \end{bmatrix} = \frac{1}{3} \begin{bmatrix} 3 \\ -3 \end{bmatrix} = \begin{bmatrix} 1 \\ -1 \end{bmatrix}$$

The new components are $(1, -1)$.

## Problem 2
The components of a vector in basis $B$ are $\mathbf{v}_B$. The components in basis $B'$ are $\mathbf{v}_{B'}$. Find the transformation matrix that relates $\mathbf{v}_B$ to $\mathbf{v}_{B'}$.

## Solution 2
If $P$ is the change of basis matrix from $B'$ to $B$, then $\mathbf{v}_B = P \mathbf{v}_{B'}$.

## Problem 3
Show that the length of a vector is invariant under a rotation transformation.

## Solution 3
Let $\mathbf{v} = (x, y)$. Length squared is $L^2 = x^2 + y^2$. A rotation $R$ transforms $\mathbf{v}$ to $\mathbf{v}' = R\mathbf{v}$.

$$\mathbf{v}' = (x \cos\theta - y \sin\theta, x \sin\theta + y \cos\theta)$$

$$L'^2 = (x \cos\theta - y \sin\theta)^2 + (x \sin\theta + y \cos\theta)^2$$

$$= x^2\cos^2\theta - 2xy\sin\theta\cos\theta + y^2\sin^2\theta + x^2\sin^2\theta + 2xy\sin\theta\cos\theta + y^2\cos^2\theta$$

$$= x^2(\cos^2\theta + \sin^2\theta) + y^2(\sin^2\theta + \cos^2\theta)$$

$$= x^2 + y^2 = L^2$$

So the length is invariant.