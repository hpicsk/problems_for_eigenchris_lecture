# Lorentz Gauge - Example Problems and Solutions

## Problem 1

What is a gauge transformation in the context of linearized gravity?

## Solution 1

A gauge transformation in linearized gravity is a coordinate transformation that changes the form of the metric perturbation $h_{\mu\nu}$ but does not change the underlying physics. It is given by:

$$h_{\mu\nu} \to h'_{\mu\nu} = h_{\mu\nu} - \partial_\mu \xi_\nu - \partial_\nu \xi_\mu$$

where $\xi_\mu$ is an arbitrary vector field.

## Problem 2

What is the Lorentz gauge? What is its advantage?

## Solution 2

The Lorentz gauge is a specific choice of gauge in which the metric perturbation satisfies the condition $\partial^\alpha h_{\alpha\nu} = \frac{1}{2} \partial_\nu h$. The advantage of the Lorentz gauge is that it simplifies the linearized Einstein field equations to a wave equation.

## Problem 3

Show that it is always possible to choose the Lorentz gauge.

## Solution 3

Given an arbitrary metric perturbation $h_{\mu\nu}$, we can always find a gauge transformation $\xi_\mu$ such that the new metric perturbation $h'_{\mu\nu}$ satisfies the Lorentz gauge condition. This is done by choosing $\xi_\mu$ to be a solution of the wave equation:

$$\Box \xi_\nu = \partial^\alpha h_{\alpha\nu} - \frac{1}{2} \partial_\nu h$$