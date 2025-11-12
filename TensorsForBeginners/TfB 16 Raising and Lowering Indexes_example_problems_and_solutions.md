# TfB 16: Raising and Lowering Indexes - Example Problems and Solutions

## Problem 1
Given a covector $\mathbf{f}$ with components $(1, 2)$ in a 2D Euclidean space (metric is the identity matrix), what are the components of the corresponding vector $\mathbf{f}^{\sharp}$?

## Solution 1
In Euclidean space with the identity metric, the components of the vector are the same as the components of the covector. So, $\mathbf{f}^{\sharp}$ has components $(1, 2)$.

## Problem 2
Given a vector $\mathbf{v}$ with components $(3, 4)$ in the same space, what are the components of the corresponding covector $\mathbf{v}^{b}$?

## Solution 2
Similarly, the components of the covector are the same as the components of the vector. So, $\mathbf{v}^{b}$ has components $(3, 4)$.

## Problem 3
In a space with metric 
$$g = \begin{bmatrix} 2 & 0 \\ 0 & 1 \end{bmatrix}$$
lower the index of the vector $\mathbf{v} = (1, 1)$.

## Solution 3
The components of the covector $\mathbf{v}^b$ are given by $v_i = g_{ij} v^j$.

$$v_1 = g_{11}v^1 + g_{12}v^2 = 2 \cdot 1 + 0 \cdot 1 = 2$$

$$v_2 = g_{21}v^1 + g_{22}v^2 = 0 \cdot 1 + 1 \cdot 1 = 1$$

So the covector has components $(2, 1)$.