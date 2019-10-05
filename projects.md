---
layout: page
title: Projects
meta-description: The current projects in progress of Neil Lindquist
---

# Current Projects


### Mixed precision GMRES
##### August 2019 - Present
Understanding how using different precisions for different values affects the performance and convergence of GMRES.


### SLIMA
##### April 2019 - Present
An Atom package for interactive Common Lisp development, based on the Emacs plugin SLIME.
This is a fork of [Steve Levine's Atom-Slime](https://github.com/sjlevine/atom-slime).

* [Atom package page](https://atom.io/packages/slima) - The package page
* [Swank-Client](https://www.npmjs.com/package/swank-client) - The NPM package that handles the actual swank remote calls.

# Past Projects

### Reducing Memory Access Latencies using Data Compression in Sparse, Iterative Linear Solvers
##### May 2017 - April 2019
Determining whether the performance of sparse linear solvers (specifically Conjugate Gradient) can be improved by reducing memory access latencies using data compression.
* [Undergraduate Thesis](https://github.com/neil-lindquist/Undergrad-Thesis/blob/master/thesis.pdf)
* [Presented](/files/2019-04-12-PMEslides.pdf) at the 2019 CSB/SJU Pi Mu Epsilon Conference

### JuliaPetra
##### July 2017 - May 2019
An implementation of Trilinos's Petra Object Model in Julia.
The project is trying to understand how well Julia works for distributed, high performance computing.

* [JuliaPetra.jl](https://github.com/collegeville/JuliaPetra.jl) - The implementation
* [Obtaining Performance from a Julia-Implementation of Trilinos Data Librairies](https://www.pathlms.com/siam/courses/10878/sections/14368/video_presentations/127457) - presented at the 2019 SIAM Conference on Computational Science and Engineering
* (In progress) JuliaPetra: An Implementation of the Petra Object Model in Julia
  * Coauthoring with [Dr. Mike Heroux](https://maherou.github.io/) and [Katherine Mendel](https://github.com/katmendy)
* [TypeStability.jl](https://github.com/collegeville/typestability.jl) - A Julia package to automate type stability checks
