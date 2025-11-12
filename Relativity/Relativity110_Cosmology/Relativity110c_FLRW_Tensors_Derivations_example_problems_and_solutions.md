---
layout: default
title: "FLRW Tensors Derivations"
---

# FLRW Tensors Derivations - Example Problems and Solutions

## Problem 1

Calculate the Christoffel symbols for the FLRW metric.

## Solution 1

The non-zero Christoffel symbols for the FLRW metric are:

$$\Gamma^1_{11} = \frac{kr}{1-kr^2}$$

$$\Gamma^1_{22} = -r(1-kr^2)$$

$$\Gamma^1_{33} = -r(1-kr^2)\sin^2\theta$$

$$\Gamma^2_{12} = \frac{1}{r}$$

$$\Gamma^2_{33} = -\sin\theta\cos\theta$$

$$\Gamma^3_{13} = \frac{1}{r}$$

$$\Gamma^3_{23} = \cot\theta$$

$$\Gamma^0_{11} = \frac{a\dot{a}}{c^2(1-kr^2)}$$

$$\Gamma^0_{22} = \frac{a\dot{a}r^2}{c^2}$$

$$\Gamma^0_{33} = \frac{a\dot{a}r^2\sin^2\theta}{c^2}$$

$$\Gamma^1_{01} = \frac{\dot{a}}{a}$$

$$\Gamma^2_{02} = \frac{\dot{a}}{a}$$

$$\Gamma^3_{03} = \frac{\dot{a}}{a}$$

where $\dot{a} = \frac{da}{dt}$.

## Problem 2

Calculate the Ricci tensor for the FLRW metric.

## Solution 2

The non-zero components of the Ricci tensor are:

$$R_{00} = -3\frac{\ddot{a}}{a}$$

$$R_{ij} = \frac{a\ddot{a} + 2\dot{a}^2 + 2kc^2}{c^2} g_{ij}$$

## Problem 3

Calculate the Ricci scalar for the FLRW metric.

## Solution 3

The Ricci scalar is:

$$R = \frac{6}{c^2} \cdot \frac{a\ddot{a} + \dot{a}^2 + kc^2}{a^2}$$