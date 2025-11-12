# TfB 4: What are Covectors - Example Problems and Solutions

## Problem 1
What is a covector, and how is it different from a vector?

## Solution 1
A covector is a linear map from the vector space to its field of scalars. It takes a vector and produces a number. A vector is an element of the vector space itself.

## Problem 2
A covector $\mathbf{f}$ is defined by its action on the basis vectors of a 2D space: $f(\mathbf{e_1}) = 2$ and $f(\mathbf{e_2}) = -1$. If a vector $\mathbf{v}$ is given by $\mathbf{v} = 3\mathbf{e_1} + 4\mathbf{e_2}$, what is the value of $f(\mathbf{v})$?

## Solution 2
By linearity, $f(\mathbf{v}) = f(3\mathbf{e_1} + 4\mathbf{e_2}) = 3f(\mathbf{e_1}) + 4f(\mathbf{e_2}) = 3(2) + 4(-1) = 6 - 4 = 2$.

## Problem 3
What is the dual space of a vector space? What is its dimension?

## Solution 3
The dual space $V^*$ is the space of all covectors on $V$. It has the same dimension as $V$.

## Problem 4
Explain why covectors are sometimes called linear functionals.

## Solution 4
They are "functionals" because they map vectors to scalars. They are "linear" because they satisfy the property $f(a\mathbf{v} + b\mathbf{w}) = af(\mathbf{v}) + bf(\mathbf{w})$.