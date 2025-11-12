# TfB 13 Tensor Product vs Kronecker Product: Example Problems and Solutions

## Problem 1
Given the matrices 
$$A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \quad \text{and} \quad B = \begin{bmatrix} 0 & 5 \\ 6 & 7 \end{bmatrix}$$
compute their tensor product and their Kronecker product.

## Solution 1
The Kronecker product is a specific way of arranging the tensor product into a matrix.

$$A \otimes B = \begin{bmatrix} 1 \cdot B & 2 \cdot B \\ 3 \cdot B & 4 \cdot B \end{bmatrix}$$

$$= \begin{bmatrix} 1 \cdot 0 & 1 \cdot 5 & 2 \cdot 0 & 2 \cdot 5 \\ 1 \cdot 6 & 1 \cdot 7 & 2 \cdot 6 & 2 \cdot 7 \\ 3 \cdot 0 & 3 \cdot 5 & 4 \cdot 0 & 4 \cdot 5 \\ 3 \cdot 6 & 3 \cdot 7 & 4 \cdot 6 & 4 \cdot 7 \end{bmatrix}$$

$$= \begin{bmatrix} 0 & 5 & 0 & 10 \\ 6 & 7 & 12 & 14 \\ 0 & 15 & 0 & 20 \\ 18 & 21 & 24 & 28 \end{bmatrix}$$

## Problem 2
What is the key difference between the tensor product and the Kronecker product in the context of linear algebra and tensor analysis?

## Solution 2
The tensor product is a more general concept that combines two vector spaces to create a new one. The Kronecker product is a specific matrix representation of the tensor product of two linear operators (matrices).