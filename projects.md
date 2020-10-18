---
layout: page
title: Projects
meta-description: The current projects in progress of Neil Lindquist
---

# Current Projects

### Randomized LU Factorization
##### February 2020 - Present
Experimenting with the use of Randomized Butterfly Transforms to replace pivoting in large scale, distributed gaussian elimination codes.
Replacing pivoting with a simple precondition steps, reduces the amount of communication, particularly from key tight loops.
The current work uses the [SLATE](https://icl.utk.edu/slate) dense linear algebra library.
* [Replacing Pivoting in Distributed Gaussian Elimination with Randomized Techniques](/files/2020-11-12-ScalA20-paper.pdf) - paper at the 11th Workshop on Latest Advances in Scalable Algorithms for Large-Scale Systems

### Mixed precision GMRES
##### August 2019 - Present
Exploring how the use of different precisions for different parts of the solver affects the performance and convergence of GMRES.
The current goal is to be able to achieve the performance of a double precision GMRES implementation while selectively using lower precision in order to reduce data movement costs.

* [Improving the Performance of the GMRES method using Mixed-Precision Techniques](https://www.icl.utk.edu/files/publications/2020/icl-utk-1419-2020.pdf) - paper at the 2020 Smokey Mountains Conference
  * [Presentation](/files/2020-08-27-SMC20-recording.mp4)
* [Improving the Performance of GMRES using Mixed Precision](/files/2020-02-13-SIAM_PP20-slides.pdf) - presented at the 2020 SIAM Conference on Parallel Processing for Scientific Computing

### Atom for Common Lisp
##### April 2019 - Present
I maintain two packages for developing Lisp (especially Common Lisp) in the Atom text editor.
First is SLIMA, which provides interactive Common Lisp development, based on the Emacs plugin SLIME.
This is a fork of [Steve Levine's Atom-Slime](https://github.com/sjlevine/atom-slime).
Second is Lisp-Paredit, which provides commands for editing any S-expression based language, originally developed by [Jon Spalding](https://github.com/jonspalding/).

* [SLIMA package page](https://atom.io/packages/slima)
* [Swank-Client](https://www.npmjs.com/package/swank-client) - The NPM package that handles the underlying swank remote calls for SLIMA.
* [Lisp-Paredit package page](https://atom.io/packages/lisp-paredit)

# Past Projects

### Reducing Memory Access Costs using Data Compression in Conjugate Gradient
##### May 2017 - April 2019
Exploration into whether the performance of sparse linear solvers (specifically Conjugate Gradient) can be improved by reducing data movement using compression.
* [Undergraduate Thesis](https://github.com/neil-lindquist/Undergrad-Thesis/blob/master/thesis.pdf)
* [Presented](/files/2019-04-12-PMEslides.pdf) at the 2019 CSB/SJU Pi Mu Epsilon Conference

### JuliaPetra
##### July 2017 - May 2019
An implementation of Trilinos's Petra Object Model in Julia.
The project tried to understand how well Julia works for distributed, high performance computing.

* [JuliaPetra.jl](https://github.com/collegeville/JuliaPetra.jl) - The implementation
* [Obtaining Performance from a Julia-Implementation of Trilinos Data Librairies](https://www.pathlms.com/siam/courses/10878/sections/14368/video_presentations/127457) - presented at the 2019 SIAM Conference on Computational Science and Engineering
* [TypeStability.jl](https://github.com/collegeville/typestability.jl) - A Julia package to automate type stability checks
