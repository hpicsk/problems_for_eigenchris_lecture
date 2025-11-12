# TfB 5,6 Covector Basis and Transformation Rules - Example Problems and Solutions

## Problem 1
A covector $\mathbf{f}$ has components $(2, -1)$ in the dual basis $\{\mathbf{e^*_1}, \mathbf{e^*_2}\}$ corresponding to the standard basis $\{\mathbf{e_1}, \mathbf{e_2}\}$. Consider the new basis from problem 1 in "TfB 2,3". What are the components of $\mathbf{f}$ in the dual basis corresponding to this new basis?

## Solution 1
The transformation matrix for the basis vectors is 
$$P = \begin{bmatrix} 2 & 1 \\ 1 & -1 \end{bmatrix}$$
The components of the covector transform by $P^T$.

$$P^T = \begin{bmatrix} 2 & 1 \\ 1 & -1 \end{bmatrix}^T = \begin{bmatrix} 2 & 1 \\ 1 & -1 \end{bmatrix}$$

$$\mathbf{f}' = P^T \mathbf{f} = \begin{bmatrix} 2 & 1 \\ 1 & -1 \end{bmatrix} \begin{bmatrix} 2 \\ -1 \end{bmatrix} = \begin{bmatrix} 3 \\ 3 \end{bmatrix}$$

The new components are $(3, 3)$.

## Problem 2
The components of a covector in the dual basis $B^*$ are $\mathbf{f}_{B^*}$. The components in the dual basis $B'^*$ are $\mathbf{f}_{B'^*}$. Find the transformation matrix that relates $\mathbf{f}_{B^*}$ to $\mathbf{f}_{B'^*}$.

## Solution 2
If $P$ is the change of basis matrix from $B'$ to $B$, then $\mathbf{f}_{B'^*} = P^T \mathbf{f}_{B^*}$.

## Problem 3
How do the transformation rules for covectors differ from those for vectors?

## Solution 3
Vector components are contravariant (transform with $P^{-1}$). Covector components are covariant (transform with $P^T$).