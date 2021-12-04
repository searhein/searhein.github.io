---
layout: post
title: Exercise Session - Parallel Preconditioning with FROSch
date: 2021-11-13 11:00:00
description: Summer school on advanced DD methods at the Politecnico di Milano from 24.11.2021 to 26.11.2021
tags: frosch trilinos tutorial docker
categories: FROSch
---

### Abstract

*Schwarz methods are an algorithmic framework for a large class of domain decomposition methods. The software FROSch (Fast and Robust Overlapping Schwarz), which is part of the Trilinos package ShyLU, provides a highly scalable implementation of the Schwarz framework, and the resulting solvers are based on the construction and combination of the relevant Schwarz operators. FROSch currently focusses on Schwarz operators that are algebraic in the sense that they can be constructed from a fully assembled, parallel distributed matrix. This is facilitated by the use of extension-based coarse spaces, such as generalized Dryja-Smith-Widlund (GDSW) type coarse spaces.*

*In this lab session, the FROSch software framework will be introduced, and its usage will be explained based on simple model problems. The examples provided will allow investigating the influence of important algorithmic aspects of Schwarz methods, such as the variation of the width of the overlap or adding a coarse level, on the convergence of a preconditioned Krylov solver.*

### Additional Information

The *Summer school on advanced DD methods* will take place at the Politecnico di Milano from November 26 - 26, 2021; see the [website of the school](https://gciara.wordpress.com/summer-school-on-dd-methods/). In exercise session 2 on Thursday, November 25, the participants will learn the **basic usage of the FROSch (Fast and Robust Overlapping Schwarz) domain decomposition solver package** based on some simple exercises. After finishing the exercises, they will have written an MPI-parallel code based on Trilinos for solving a simple Laplace or elasticity model problem in two or three dimensions. Within this code, the discrete linear system will be assembled using the Trilinos package *Galeri*, solved with an iterative solver from *Belos*, and preconditioned by a one- or two-level Schwarz preconditioner from the *FROSch* package. As the parallel linear algebra framework, *Tpetra* will be used through the *Xpetra* interface.

The **material for the exercise session is available on the [FROSch demo](https://github.com/searhein/frosch-demo#docker-container) GitHub repository**, which also provides a Dockerfile for setting up the required software environment; the version of the repository at the time of the exercise session can be found [here](https://github.com/searhein/frosch-demo/tree/65638f98a61959eef1fd8e04c08c85a3f62d858e). The instructions for installing the material and the exercises themselves are given in the descriptions within the repository (see also the `README.md` files).
