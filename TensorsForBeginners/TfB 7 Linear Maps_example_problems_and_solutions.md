# TfB 7 Linear Maps: Example Problems and Solutions

## Problem 1
A linear map $L$ from $\mathbb{R}^2$ to $\mathbb{R}^2$ is defined as follows: $L(1, 0) = (2, 3)$ and $L(0, 1) = (4, 5)$. What is the matrix representation of $L$ in the standard basis?

## Solution 1
The columns of the matrix are the images of the basis vectors. So, 
$$L = \begin{bmatrix} 2 & 4 \\ 3 & 5 \end{bmatrix}$$

## Problem 2
Using the linear map $L$ from problem 1, what is the image of the vector $(1, 1)$?

## Solution 2
$L(1, 1) = L((1, 0) + (0, 1)) = L(1, 0) + L(0, 1) = (2, 3) + (4, 5) = (6, 8)$.

Alternatively, using the matrix: 
$$\begin{bmatrix} 2 & 4 \\ 3 & 5 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 6 \\ 8 \end{bmatrix}$$

## Problem 3
Is the map $F(x, y) = (x+1, y)$ a linear map? Justify your answer.

## Solution 3
No. A linear map must satisfy $F(0) = 0$. Here, $F(0, 0) = (1, 0)$. So it is not linear.