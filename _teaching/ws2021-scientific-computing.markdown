---
layout: page_teaching
university: ust
semester: WS 2020/2021
title: Scientific Computing
description: An advanced class about domain decomposition methods and parallel computing.
runningindex: 12
archive: true
---

### Time and Location

**Lecture**
+ Pre-recorded videos

**First Lecture**: Tuesday, 03.11.2020, 09.45 -- 11.15 (online)

**Exercise Class**
+ Wednesday 09.45 -- 11.15 (online)

### Summary

In this course, numerical methods for the solution of large sparse linear systems of equations are treated. While direct solvers are not feasible due their superlinear complexity and memory consumption, the convergence of simple iterative methods deteriorates with an increasing problem size. Therefore, we will discuss domain decomposition methods, which are hybrid approaches combining the advantages of both direct and iterative methods.

Domain decomposition methods are divide-and-conquer algorithms, which are well suited for current parallel hardware architectures, ranging from tablet computers to large supercomputers with CPU or GPU architectures. The key idea for these approaches is to divide the initial large problem into smaller subproblems, which can be solved independently. Then, the solution of the full problem is computed in an iterative scheme. The best performance is typically obtained by adding an additional small but global problem to couple the local subproblems.

List of topics:
+ Krylov methods for symmetric and nonsymmetric problems
+ C/C++, MPI, and [Trilinos](https://trilinos.github.io) programming crash courses
+ Domain decomposition methods:
    + Classical nonoverlapping and overlapping domain decomposition methods
    + Abstract Schwarz theory
    + One-level and multi-level Schwarz methods
+ Optional / depending on the audience:
    + Node-level parallelization using OpenMP
    + Nonoverlapping domain decomposition methods: BDDC (Balancing domain decomposition by constraints) and FETI-DP (ﬁnite element tearing and interconnecting dual-primal) methods

### Goals

The goal of this course is discuss the theory of domain decomposition methods and to develop an MPI-parallel code containing both a parallel ﬁnite element implementation as well as a parallel domain decomposition solver. As the basis, the parallel linear algebra packages from the library Trilinos
(https://trilinos.github.io) will be used.

### Prior knowledge

Some knowledge of Numerics for PDEs, e.g. PDEMAS (Bachelor) or Einführung in die Numerik partieller Differentialgleichungen (Master)

### Remarks

The lectures will be pre-recorded and made available on Ilias. Note that the **first lecture (Tuesday, 03.11.2020, 9.45 -- 11.15) will be held online via WebEx** to clarify organizational issues.


Instead of weekly exercises, the lecture will be **accompanied by smaller projects** (involving theory and implementation). The **exercise sessions will be used for discussing the progress of the projects using the videoconference tool WebEx**. If more time is needed, the timeslots for the lectures may be used for discussions as well.

### Literature

+ Saad, Yousef. Iterative methods for sparse linear systems. Society for Industrial and Applied Mathematics, 2003.
+ Smith, Barry, Petter Bjorstad, and William Gropp. Domain decomposition: parallel multilevel methods for elliptic partial differential equations. Cambridge university press, 2004.
+ Toselli, Andrea, and Olof Widlund. Domain decomposition methods-algorithms and theory. Vol. 34. Springer Science & Business Media, 2006.
+ More literature will be announced in the lecture.
