---
title: Learn Computational Geometry - Convex Hull
summary: Easily understand and implement the Convex Hull algorithm in computational geometry.
date: 2023-10-24
type: docs
math: true
tags:
  - Computational Geometry
  - Convex Hull
image:
  caption: 'Learn about Convex Hull and its applications in Computational Geometry'
---
#                                                                                                           *Convex  Set*



- ## 🎈affine and convex sets

- ## 🎈some import examples

- ## 🎈operations that preserve convexity

- ## 🎈generalized inequalities

- ## 🎈separating and supporting hyperplanes

- ## 🎈dual cones and generalized inequalities





## 📚Affine Set

### **line through $x_1$ and $x_2$: all points**:


$$
\large   x = \theta x_1 + (1 - \theta)x_2,\quad ( \theta \in \mathbb{R})
$$
![img](https://fmin.xyz/docs/theory/convex%20sets/line.svg)

> [!IMPORTANT]
>
> #### 🚀 affine set: contains the line through any two distinct points in the set.
>
> #### 🚀example solution set of linear equations  {${x| Ax = b}$}



## 📚Convex Set

### line segment between $x_1$ and $x_2$: all points

$$
\large   x = \theta x_1 + (1 - \theta)x_2,\quad with \quad 0 \leq \theta \leq 1
$$

### convex set: contains line segment between any two points in the set

$$
x_1, x_2 \in C ，0 \leq \theta \leq 1 \quad then \quad \theta x_1 + (1 - \theta) x_2 \in C
$$

### examples (one convex, two nonconvex sets)


