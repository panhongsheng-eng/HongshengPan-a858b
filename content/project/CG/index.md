---
title: Computational Geometry
date: 2024-10-26
external_link: 
tags:
  - Introduction
  - Convex Hulls
  - Line Segment Intersection
  - Polygon Triangulation
  - Delaunay Triangulations
  - Voronoi Diagrams
  - Orthogonal Range Searching
  - Arrangements and Duality
summary: >
  This column delves into the fundamental concepts and wide-ranging applications of computational geometry, covering everything from basic geometric representations to complex algorithms and real-world use cases. From convex hulls and Voronoi diagrams to Delaunay triangulations and the closest pair problem, readers will gain a solid grasp of the cornerstones of computational geometry. The column also explores advanced topics such as polygon intersection, point set covering, range queries, and motion planning. By examining applications in computer graphics, computer vision, geographic information systems, bioinformatics, financial engineering, operations research, machine learning, big data analytics, cloud computing, and the Internet of Things, this column showcases the powerful role of computational geometry in modern technologies.
---

## Introduction

Imagine you are walking on the campus of a university and suddenly realize you need to make an urgent phone call. There are many public phones, and you naturally want to find the nearest one. Ideally, you'd have a map showing a subdivision of the campus into regions, with each region indicating the nearest phone. This subdivision is known as a **Voronoi diagram** — a fundamental geometric concept used in various applications, from urban planning and robotics to simulating crystal growth. We'll explore this in Chapter 7.

But finding the closest phone is only part of the challenge. Suppose you've found it — how do you actually get there, avoiding buildings and obstacles? For a human, that's intuitive. But for a robot, this requires **motion planning** — a core geometric problem addressed in Chapters 13 and 15.

Now imagine you have two maps: one showing buildings and phones, another showing roads. To guide a robot, you'd need to overlay the maps, combining and analyzing their features. This task, critical in geographic information systems (GIS), involves **map overlay algorithms**, and it's tackled in Chapter 2.

These are just a few of the many problems addressed by **computational geometry** — the study of algorithms and data structures for solving geometric problems, especially those requiring efficiency and precision.

Emerging in the 1970s, the field has grown rapidly, yielding elegant, efficient solutions to complex problems in robotics, computer graphics, CAD/CAM, and GIS. This book presents the essential concepts, algorithms, and data structures that power these solutions. Each chapter begins with a real-world motivation and leads into the theory and algorithmic techniques behind the solution.

## An Example: Convex Hulls

One of the earliest and most fundamental problems in computational geometry is computing the **convex hull** of a set of points.

> A subset \( S \) of the plane is **convex** if for any two points \( p, q \in S \), the line segment \( \overline{pq} \) lies entirely within \( S \).  
> The **convex hull** \( CH(S) \) is the smallest convex set that contains all points in \( S \).

A great way to visualize this: imagine the points as nails on a board, and you stretch a rubber band around them. When released, it wraps around the outermost points — this shape is the convex hull.

Given a set of \( n \) points, how do we compute their convex hull? A brute-force solution — called the **Slow Convex Hull algorithm** — checks all \( O(n^2) \) pairs of points and determines if all other points lie on one side of the directed line segment. If so, that edge is part of the convex hull.

### Pseudocode: Slow Convex Hull

```text
Algorithm SLOW_CONVEX_HULL(P)
Input: A set P of n points in the plane.
Output: A list L of convex hull vertices in clockwise order.

1. E ← ∅
2. For all ordered pairs (p,q) ∈ P×P with p ≠ q:
3.     valid ← true
4.     For all r ∈ P \ {p,q}:
5.         If r lies to the left of directed line pq:
6.             valid ← false
7.     If valid:
8.         Add directed edge pq to E
9. From edges in E, construct list L of CH(P) in clockwise order.
