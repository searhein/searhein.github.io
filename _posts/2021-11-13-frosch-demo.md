---
layout: post
title: Demonstration - Parallel Preconditioning with FROSch
date: 2021-11-13 11:00:00
description: Exercise session 2 for the Summer school on advanced DD methods at the Politecnico di Milano from 24.11.2021 to 26.11.2021
tags: frosch trilinos tutorial docker
categories: FROSch
---

**Abstract:** *Schwarz methods are an algorithmic framework for a large class of domain decomposition methods. The software FROSch (Fast and Robust Overlapping Schwarz), which is part of the Trilinos package ShyLU, provides a highly scalable implementation of the Schwarz framework, and the resulting solvers are based on the construction and combination of the relevant Schwarz operators. FROSch currently focusses on Schwarz operators that are algebraic in the sense that they can be constructed from a fully assembled, parallel distributed matrix. This is facilitated by the use of extension-based coarse spaces, such as generalized Dryja-Smith-Widlund (GDSW) type coarse spaces.*

*In this lab session, the FROSch software framework will be introduced, and its usage will be explained based on simple model problems. The examples provided will allow investigating the influence of important algorithmic aspects of Schwarz methods, such as the variation of the width of the overlap or adding a coarse level, on the convergence of a preconditioned Krylov solver.*
