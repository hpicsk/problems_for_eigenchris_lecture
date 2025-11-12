---
layout: default
title: "TfB 8 Linear Map Transformation Rules"
---

# TfB 8 Linear Map Transformation Rules: Example Problems and Solutions

## Problem 1
The matrix of a linear map $L$ in the standard basis is 
$$\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$$
What is the matrix of $L$ in a basis obtained by rotating the standard basis by 45 degrees?

## Solution 1
The change of basis matrix is:
$$P = \begin{bmatrix} \cos(45°) & -\sin(45°) \\ \sin(45°) & \cos(45°) \end{bmatrix} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}$$

The new matrix $A'$ is given by $A' = P^{-1} A P$.

$$P^{-1} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\ -1 & 1 \end{bmatrix}$$

$$A' = \frac{1}{2} \begin{bmatrix} 1 & 1 \\ -1 & 1 \end{bmatrix} \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} \begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}$$

$$= \frac{1}{2} \begin{bmatrix} 3 & 3 \\ -1 & 1 \end{bmatrix} \begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}$$

$$= \frac{1}{2} \begin{bmatrix} 6 & 0 \\ 0 & 2 \end{bmatrix} = \begin{bmatrix} 3 & 0 \\ 0 & 1 \end{bmatrix}$$

## Problem 2
If $A$ is the matrix of a linear map in basis $B$, and $A'$ is the matrix of the same linear map in basis $B'$, find the relationship between $A$ and $A'$.

## Solution 2
$A' = P^{-1} A P$, where $P$ is the change of basis matrix from $B'$ to $B$.