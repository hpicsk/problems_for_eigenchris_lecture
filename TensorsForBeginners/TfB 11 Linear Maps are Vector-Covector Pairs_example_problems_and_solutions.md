# TfB 11 Linear Maps are Vector-Covector Pairs: Example Problems and Solutions

## Problem 1
Consider a linear map $L(\mathbf{v}) = (\mathbf{v} \cdot \mathbf{u}) \mathbf{w}$, where $\mathbf{u} = (1, 0)$ and $\mathbf{w} = (0, 1)$. Express $L$ as a tensor product of a vector and a covector. What is the rank of this tensor?

## Solution 1
The dot product with $\mathbf{u}$ defines a covector $f(\mathbf{v}) = \mathbf{v} \cdot \mathbf{u}$. So $L(\mathbf{v}) = f(\mathbf{v}) \mathbf{w}$. This is the tensor product of the vector $\mathbf{w}$ and the covector $f$, $L = \mathbf{w} \otimes f$. The rank of this tensor is 1.

## Problem 2
Explain how a matrix can be seen as a (1,1) tensor, which is a vector-covector pair.

## Solution 2
A matrix $A$ acts on a vector $\mathbf{v}$ to produce another vector $\mathbf{w} = A\mathbf{v}$. This is a linear map. A (1,1) tensor is a linear map from the vector space to itself. Thus, a matrix can be interpreted as a (1,1) tensor.