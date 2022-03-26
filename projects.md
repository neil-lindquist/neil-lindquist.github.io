---
layout: page
title: Projects
meta-description: The current projects in progress of Neil Lindquist
---

# Current Projects

### Scalable LU Factorizations
##### February 2020 - Present
Experimenting with the use of various approaches to improve the performance of distributed, GPU-accelerated LU factorizations.
Such factorizations require partial pivoting for numerical stability; however, this introduces significant overheads to search for and apply such pivots.
The primary branch of this work to date involves the use of Randomized Butterfly Transforms to shuffle the matrix in such a way that pivoting is unnecessary.
Other efforts have included optimizing the pivoted and non-pivoted implementations of LU in SLATE, a dense linear algebra library for distributed, heterogenous systems.
The current work uses the [SLATE](https://icl.utk.edu/slate) dense linear algebra library.
* [Replacing Pivoting in Distributed Gaussian Elimination with Randomized Techniques](/files/2020-11-12-ScalA20-paper.pdf) - paper at the 11th Workshop on Latest Advances in Scalable Algorithms for Large-Scale Systems

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

### Scalable Interpolation for Thermal-Fluids Applications
#### May 2021 - September 2021
Ported interpolation routines to the OCCA runtime system in NekRS, a GPU-accelerated, spectral-element code for simulation fluids and their temperature.
These routines were used to implement both particle tracking and multiple, overlapped meshes.


### Mixed precision GMRES
##### August 2019 - June 2021
Exploration of the use of different precisions for different parts of the solver affects the performance and convergence of GMRES.
The work primarily focused on achieving the accuracy of a double precision GMRES implementation while selectively using lower precision to reduce data movement costs.

* [Accelerating Restarted GMRES with Mixed Precision Arithmetic](https://www.icl.utk.edu/files/publications/2021/icl-utk-1547-2021.pdf) - paper in the IEEE Transactions on Parallel and Distributed Systems
* [Improving the Performance of the GMRES method using Mixed-Precision Techniques](https://www.icl.utk.edu/files/publications/2020/icl-utk-1419-2020.pdf) - paper at the 2020 Smokey Mountains Conference
  * [Presentation](/files/2020-08-27-SMC20-recording.mp4)

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
