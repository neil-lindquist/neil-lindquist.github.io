---
layout: page
title: Curriculum Vitae
meta-description: The Curriculum Vitae of Neil Lindquist
---

<h2 class="visible-print-block">
  Neil Lindquist
</h2>

<p class="visible-print-block">
  NeilLindquist5@gmail.com
</p>

# Research Interests
Numerical Linear Algebra

Effects of data representation on performance and accuracy

Approximate computing algorithms

High performance computing


# Education

Ph.D. in Computer Science, University of Tennessee, 2023
* Advised by Dr. Jack Dongarra
* Dissertation: [Reducing Communication in the Solution of Linear Systems](/files/2023-07-18-Lindquist-Dissertation.pdf)

M.S. in Computer Science, University of Tennessee, 2022

B.A. *magna cum laude* in Math and Computer Science, Saint John's University, 2019

* Advised by Dr. Mike Heroux
* Thesis: [Reducing Memory Access Latencies using Data Compression in Sparse, Iterative Linear Solvers](https://github.com/neil-lindquist/Undergrad-Thesis/blob/master/thesis.pdf)


# Professional Experience

Developer Technology Engineer - NVIDIA (January 2024 - Present)
* Implementing and optimizing functionality in math libraries including cuSolverDx, cuSolver, and cuPQC.
* Providing guidance in linear algebra and GPU performance optimization to customers and internal teams.
* Benchmarking and optimizing customer codes, including for supercomputer RFPs.

Research Associate - University of Tennessee (August 2023 - December 2023)
 * Debugged and optimized [SLATE](http://icl.utk.edu/slate/) (a distributed, heterogeneous, dense linear algebra library) on the Frontier supercomputer.
 * Polished LU alternatives from my graduate work for inclusion in SLATE.

Graduate Research Assistant - University of Tennessee (July 2019 - July 2023)
 * Developed optimizations and algorithms to address the performance of pivoting in dense, distributed LU factorizations.
   * Primarily focused on [SLATE](http://icl.utk.edu/slate/).
   * Approaches include randomization, relaxing pivoting criteria, and additive perturbations.
 * Experimented with mixing double and single floating point precision in GMRES, a sparse, iterative linear solver.
 * Contributed to a machine learning based workflow for classification of protein structures from XFEL diffraction patterns.

Intern - MathWorks (May 2022 - August 2022)
 * Contributed to the development and optimization of MATLAB linear algebra routines, including sparse-matrix-multiplication, least-squares, and eigenvalue problems.

Givens Associate - Argonne National Laboratory (May 2021 - August 2021)
 * Ported interpolation routines to GPU accelerators using the [OCCA](https://libocca.org) runtime in [NekRS](https://github.com/Nek5000/nekRS), a spectral-element based fluid dynamics code.
 * Implemented particle-tracking and overlapping simulation domains functionalities in NekRS using the new interpolation routines.

Research Assistant - Saint John's University (May 2017 - May 2019)
 * Explored using data compression in Conjugate Gradient on distributed CPU clusters.
 * Investigated using the Julia language for distributed-memory sparse linear algebra.


# Honors and Awards

Nominated for the Best Paper Award of ICS'23

Tennessee's Top 100 Fellowship, University of Tennessee (August 2019 - July 2024)

Pi Mu Epsilon Mathematics Honor Society (inducted May 2019)

Phi Beta Kappa Honors Society (inducted April 2019)

Eagle Scout (awarded June 2014)

# Publications

M. Gates et al., “Evolution of the SLATE linear algebra library,” The Intl. J. of High Performance Computing Applications. vol 39, no 1, pp. 3-17, Jan. 2025 DOI: [10.1177/10943420241286531](https://doi.org/10.1177/10943420241286531)

**N. Lindquist**, P. Luszczek, and J. Dongarra, “Generalizing Random Butterfly Transforms to Arbitrary Matrix Sizes,” ACM Trans. Math. Softw. vol. 50, no 4, pp. 26:1-26:23, Dec. 2024 DOI: <a href="https://dl.acm.org/doi/10.1145/3699714?cid=99659486680" referrerpolicy="no-referrer-when-downgrade">10.1145/3699714</a>

**N. Lindquist**, P. Luszczek, and J. Dongarra, “Using Additive Modifications in LU Factorization Instead of Pivoting,” presented at the 2023 ACM International Conference on Supercomputing (ICS), Orlando, FL, USA, June 2023, DOI: <a href="https://dl.acm.org/doi/10.1145/3577193.3593731?cid=99659486680" referrerpolicy="no-referrer-when-downgrade">10.1145/3577193.3593731</a>

**N. Lindquist**, M. Gates, P. Luszczek, and J. Dongarra, “Threshold Pivoting for Dense LU Factorization,” presented at the 2022 IEEE/ACM 13th Workshop on Latest Advances in Scalable Algorithms for Large-Scale Heterogeneous Systems (ScalAH), Dallas, TX, USA, Nov. 2022, DOI: [10.1109/ScalAH56622.2022.00010](https://doi.org/10.1109/ScalAH56622.2022.00010)
* [Preprint PDF](https://icl.utk.edu/files/publications/9998/icl-utk-1572-9998.pdf)

**N. Lindquist**, P. Luszczek, and J. Dongarra, “Accelerating Restarted GMRES With Mixed Precision Arithmetic,” in IEEE Transactions on Parallel and Distributed Systems, vol. 33, no. 4, pp. 1027-1037, April 2022, DOI: [10.1109/TPDS.2021.3090757](https://doi.org/10.1109/TPDS.2021.3090757)
* [Preprint PDF](https://www.icl.utk.edu/files/publications/2021/icl-utk-1547-2021.pdf)

**N. Lindquist**, P. Luszczek, and J. Dongarra, “Replacing Pivoting in Distributed Gaussian Elimination with Randomized Techniques,” presented at the 2020 IEEE/ACM 11th Workshop on Latest Advances in Scalable Algorithms for Large-Scale Systems (ScalA), Atlanta, GA, USA, Nov. 2020, DOI: [10.1109/ScalA51936.2020.00010](https://doi.org/10.1109/ScalA51936.2020.00010)
* [Preprint PDF](https://www.icl.utk.edu/files/publications/2020/icl-utk-1440-2020.pdf)

P. Luszczek, Y. Tsai, **N. Lindquist**, H. Anzt, and J. Dongarra, “Scalable Data Generation for Evaluating Mixed-Precision Solvers,” presented at the 2020 IEEE High Performance Extreme Computing Conference (HPEC), Waltham, MA, USA, Sep. 2020, pp. 1–6, DOI: [10.1109/HPEC43674.2020.9286145](https://doi.org/10.1109/HPEC43674.2020.9286145).
* [Preprint PDF](https://www.icl.utk.edu/files/publications/2020/icl-utk-1484-2020.pdf)

**N. Lindquist**, P. Luszczek, and J. Dongarra, “Improving the Performance of the GMRES Method using Mixed-Precision Techniques,” presented at the 17th Smoky Mountains Computational Sciences and Engineering Conference, SMC 2020, Oak Ridge, TN, USA, Aug. 2020, DOI: [10.1007/978-3-030-63393-6_4](https://doi.org/10.1007/978-3-030-63393-6_4)
* [Preprint PDF](https://www.icl.utk.edu/files/publications/2020/icl-utk-1419-2020.pdf)

**N. Lindquist**, “Replicated Computational Results (RCR) Report for ‘Code Generation for Generally Mapped Finite Elements,’” ACM Trans. Math. Softw., vol. 45, no. 4, pp. 42:1–42:7, Dec. 2019, DOI: <a href="https://dl.acm.org/doi/10.1145/3360984?cid=99659486680" referrerpolicy="no-referrer-when-downgrade">10.1145/3360984</a>

# Presentations

[Portable C++ for Modern, Heterogenous Mixed-Precision Methods](/files/2023-03-01-SIAM_CSE23-slides.pdf)
* 2023 SIAM Conference on Computational Science and Engineering

[Modern Mixed-Precision Methods in Portable C++ for Accelerated Hardware Platforms](/files/2022-02-26-SIAM_PP22-slides.pdf)
* 2022 SIAM Conference on Parallel Processing for Scientific Computing

[Replacing Pivoting in Distributed Gaussian Elimination with Randomized Techniques](/files/2021-07-23-SIAM_AN21-slides.pdf)
* 2021 SIAM Annual Meeting
* 13th JLESC workshop

[Multiprecision Approach in GMRES and its Effects on Performance](/files/2021-05-18-SIAM_LA21-slides.pdf)
* 2021 SIAM Conference on Applied Linear Algebra

[Accelerating GMRES via Mixed Precision](/files/2021-02-25-JLESC-slides.pdf)
* 12th JLESC workshop

[Improve the Performance of GMRES using Mixed Precision](/files/2020-02-13-SIAM_PP20-slides.pdf)
* 2020 SIAM Conference of Parallel Processing for Scientific Computing

[Reducing Memory Access Latencies using Data Compression in Sparse, Iterative Linear Solvers](/files/2019-04-12-PMEslides.pdf)
 * 2019 CSB/SJU Pi Mu Epsilon Conference

[Obtaining Performance from a Julia-Implementation of Trilinos Data Librairies](https://www.pathlms.com/siam/courses/10878/sections/14368/video_presentations/127457)
 * 2019 SIAM Conference on Computational Science and Engineering

# Teaching and Mentorship Experience

Hackathon mentor (June 2024, Sep. 2024, Feb. 2025)

Graduate Teaching Assistant - Scientific Computing For Engineers (Spring 2020, Spring 2021)
