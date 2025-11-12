---
layout: default
title: "TfB 10 Bilinear Forms"
---

# TfB 10 Bilinear Forms: Example Problems and Solutions

## Problem 1
A bilinear form $B$ is represented by the matrix 
$$M = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$$
Given two vectors $\mathbf{v} = (1, 1)$ and $\mathbf{w} = (2, 0)$, compute $B(\mathbf{v}, \mathbf{w})$.

## Solution 1
$$B(\mathbf{v}, \mathbf{w}) = \mathbf{v}^T M \mathbf{w} = \begin{bmatrix} 1 & 1 \end{bmatrix} \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \begin{bmatrix} 2 \\ 0 \end{bmatrix} = \begin{bmatrix} 1 & 1 \end{bmatrix} \begin{bmatrix} 2 \\ 6 \end{bmatrix} = 1 \cdot 2 + 1 \cdot 6 = 8$$

## Problem 2
Given the bilinear form $B(\mathbf{v}, \mathbf{w}) = v_1w_1 + 2v_1w_2 + 3v_2w_1 + 4v_2w_2$, what is the matrix of $B$ in the standard basis?

## Solution 2
The matrix components are given by $M_{ij} = B(\mathbf{e_i}, \mathbf{e_j})$.

$M_{11} = B((1,0), (1,0)) = 1$

$M_{12} = B((1,0), (0,1)) = 2$

$M_{21} = B((0,1), (1,0)) = 3$

$M_{22} = B((0,1), (0,1)) = 4$

So, 
$$M = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$$

## Problem 3
Is the dot product a bilinear form? Justify your answer.

## Solution 3
Yes. The dot product $\mathbf{v} \cdot \mathbf{w} = v_1w_1 + v_2w_2$ is linear in both $\mathbf{v}$ and $\mathbf{w}$.