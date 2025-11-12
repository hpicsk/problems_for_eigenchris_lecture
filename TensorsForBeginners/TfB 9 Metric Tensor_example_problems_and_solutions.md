# TfB 9 Metric Tensor: Example Problems and Solutions

## Problem 1
In a 2D Euclidean space, the metric tensor is given by the identity matrix. What is the length of the vector $(3, 4)$?

## Solution 1
$$\text{Length}^2 = \mathbf{v}^T g \mathbf{v} = \begin{bmatrix} 3 & 4 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} 3 \\ 4 \end{bmatrix} = 3 \cdot 3 + 4 \cdot 4 = 25$$ 

$$\text{Length} = 5$$

## Problem 2
What is the angle between the vectors $(1, 0)$ and $(1, 1)$ using the Euclidean metric?

## Solution 2
$$\cos(\theta) = \frac{\mathbf{v} \cdot \mathbf{w}}{||\mathbf{v}|| \, ||\mathbf{w}||} = \frac{1 \cdot 1 + 0 \cdot 1}{\sqrt{1^2+0^2} \cdot \sqrt{1^2+1^2}} = \frac{1}{\sqrt{2}}$$

So $\theta = 45°$.

## Problem 3
Consider a non-Euclidean 2D space with a metric tensor 
$$g = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$$
What is the length of the vector $(1, 1)$ in this space?

## Solution 3
$$\text{Length}^2 = \mathbf{v}^T g \mathbf{v} = \begin{bmatrix} 1 & 1 \end{bmatrix} \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 1 & 1 \end{bmatrix} \begin{bmatrix} 3 \\ 3 \end{bmatrix} = 6$$

$$\text{Length} = \sqrt{6}$$