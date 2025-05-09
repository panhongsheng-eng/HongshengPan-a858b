---
title: Convex Optimization-convex sets
summary: Easily understand and implement the Convex Hull algorithm in computational geometry.
date: 2023-10-24
type: docs
math: true
tags:
  - affine and convex sets
  - some important examples
  - operations that preserve convexity
  - generalized inequalities
  - separating and supporting hyperplanes
  - dual cones and generalized inequalities
image:
  caption: ''
---



## 📚Affine Sets



#### line through $x_1$ and $x_2$: all points**:
$$
\large   x = \theta x_1 + (1 - \theta)x_2,\quad ( \theta \in \mathbb{R})
$$
![image](https://github.com/user-attachments/assets/eeb22ef6-2093-4a9f-a2ed-4e38d1acecf4)
> [!IMPORTANT]
>
> ##### 🚀 affine set: contains the line through any two distinct points in the set.
>
> ##### 🚀example solution set of linear equations  {${x| Ax = b}$}

## 📚Convex Set
#### line segment between $x_1$ and $x_2$: all points

$$
\large   x = \theta x_1 + (1 - \theta)x_2,\quad with \quad 0 \leq \theta \leq 1
$$

#### convex set: contains line segment between any two points in the set

$$
x_1, x_2 \in C ，0 \leq \theta \leq 1 \quad then \quad \theta x_1 + (1 - \theta) x_2 \in C
$$

#### examples (one convex, two nonconvex sets)

![../_images/pacman.svg](https://zh.d2l.ai/_images/pacman.svg)
