---
layout: page
title: Matrix Norms
meta-description: Reference for basic properties of matrix norms.
---

I find myself looking up properties of specific matrix norms on the Wikipedia way too often.  So, I decided to gather some of the key properties and coefficients here for the norms on $`\mathbb{C}^{m\times n}`$.

Note that some authors limit the term matrix norm to only those norms that are also submultiplicative.
Because non-submultiplicative norms have played an important part in numerical linear algebra (particularly the max-norm), I make no such restriction here.

While most properties are only concerned with a single matrix dimension, a few involve multiple matrices.
Technically speaking, a norm is only defined for a single dimension and two norms for different dimensions are different norms; however, it is often easier to think of a single "norm" that applies to different dimensions.
So, in cases where it is relevant, I instead consider dimension-invariant families of norms [\[LLD25\]](#cite-lld25), i.e., a set of matrix norms such that for any matrix $`A`$ and any block partitioning thereof, $`\mathcal{I}\times\mathcal{J}`$, the norms of appropriate size satisfy

$$
\max_{\substack{i\in \mathcal{I}\\j\in\mathcal{J}}} \|A_{i,j}\| \leq \|A\| \leq \sum_{\substack{i\in\mathcal{I}\\j\in\mathcal{J}}} \|A_{i,j}\|.
$$

This is satisfied by the usual norm definitions and provides several intuitive properties such as
* Padding a matrix with zero rows or columns doesn't affect it's norm.
* A matrix with a single nonzero value equal to $`\alpha`$ has a norm equal to $`\|[\alpha]\|`$.

Notably, this definition implies permutation invariance and so excludes some niche matrix norms, such as operator norms that are induced by some vector energy norms.
Additionally, it excludes scaling based on the dimensions, such as when the max norm is scaled to become submultiplicative.



## Definitions of Common Norms

While there are infinitely many ways to define a matrix norm, there's only a small number of parameterized definitions that are used in practice.

### Elementwise Norms

The simplest matrix norm to define are the elementwise norms.
Specifically, for $`1 \leq p < \infty`$ the elementwise $`p`$-norm is defined for $`A\in\mathbb{C}^{m\times n}`$ as

$$
\|A\| = \left( \sum_{i=0}^{m}\sum_{j=0}^{n} A[i, j]^p \right)^{1/p}
$$

Furthermore, taking the limit as $`p`$ goes to infinity gives the elementwise $`\infty`$-norm:

$$
\|A\|_\infty = \max_{i,j}(|A[i, j]|)
$$

These definitions are equivalent to treating an $`m\times n`$ matrix as a vector of length $`mn`$ and applying the corresponding vector $`L^p$` norm.

### $`L^p`$ Induced Norms

The $`L^p`$ induced norms are the operator norms induced by the $`L^p`$ vector norms.
Formulas are only known for the $`L^1`$, $`L^2`$, and $`L^\infty`$ induced norms, so other induced norms are rarely used.

Note that $`L^p`$ vector norms are also called Hölder norms.

### Schatten Norms

The Schatten $`p`$ norm of a matrix $`A`$ is the vector $`L^p`$ norm of of $`A`$'s' singular values.

### Ky Fan Norms

The Ky Fan $`k`$ norm of $`A`$ is the sum of $`A`$'s $`k`$ largest singular values.



### Named Norms

Note that some have multiple equivalent definitions

| Name      | Elementwise $`p`$ | $`Lp`$ Induced | Schatten $`p`$ | Ky Fan $`k`$ norm |
|-----------|-------------------|----------------|----------------|-------------------|
| Sum       | 1                 |                |                |                   |
| Frobenius | 2                 |                | 2              |                   |
| Max       | $`\infty`$        |                |                |                   |
| Nuclear   |                   |                | 1              | $`\min(m, n)`$    |
| Spectral  |                   | 2              | $`\infty`$     | 1                 |



## Basic Properties

The following table describes which matrices have the following properties

* Absolute: $`\||A|\| = \|A\|`$ for any matrix $`A`$
* Submultiplicative: $`\|AB\| \leq \|A\|\|B\|`$ for any conformal matrices $`A, B`$
* Unitary Invariant: $`\|UAV\| = \|A\|`$ for any matrix $`A`$ and conformal, square unitary matrices $`U, V`$
* Conjugate-Transpose Invariant: $`\|A*\| = \|A\|`$ for any matrix $`A`$


| Norm                                                  | Absolute | Submultiplicative | Unitary Invariant | Conjugate-Transpose Invariant |
|-------------------------------------------------------|----------|-------------------|-------------------|-------------------------------|
| elementwise $`p`$ norm                                | Yes      | Varies            | Varies            | Yes                           |
| elementwise 1 norm (sum norm)                         | Yes      | Yes               | No                | Yes                           |
| elementwise 2 norm (Frobenius norm)                   | Yes      | Yes               | Yes               | Yes                           |
| elementwise $`\infty`$ norm (max norm)                | Yes      | No                | No                | Yes                           |
| $`L^p`$ induced norm                                  | Varies   | Yes               | Varies            | Varies*                       |
| $`L^1`$ induced norm                                  | Yes      | Yes               | No                | No*                           |
| $`L^2`$ induced norm (Spectral norm)                  | No       | Yes               | Yes               | Yes*                          |
| $`L^\infty`$ induced norm                             | Yes      | Yes               | No                | No*                           |
| Schatten $`p`$ norm                                   | Varies   | Yes               | Yes               | Yes                           |
| Schatten 1 norm (Nuclear norm)                        | No       | Yes               | Yes               | Yes                           |
| Schatten 2 norm (Frobenius norm)                      | Yes      | Yes               | Yes               | Yes                           |
| Schatten $`\infty`$ norm (Spectral norm)              | No       | Yes               | Yes               | Yes                           |
| Ky Fan $`k`$ norm                                     | No       | Yes               | Yes               | Yes                           |

\* While the Spectral norm is the only $`L^p`$ induced norm that is invariant to conjugate-transposition, \(L^p\) induced norms do satisfy $`\|A^H\|_p = \|A\|_q`$ for $`1/p + 1/q = 1`$ [\[Hig02, (6.21)\]](#cite-hig02).

Note that technically a norm is defined for a single size, so defining submultiplicativity for rectangular matrices is a property of a set of conformal norms.  However, the norms defined here are parameterized on matrix size and behave nicely when moving between sizes.

### Select Justifications
Most of these results are well know or obvious.  However, some are not, so I elucidate a few results.

To see that the Ky Fan norms (including the Spectral and Nuclear norms) are not absolute, note that the Frobenius norm is the only unitary invariant matrix norm that is absolute [\[H&J12, Thm. 7.4.11.1\]](#cite-handj12).

To see that the Ky Fan and Schatten norms are submultiplicative, note that for any matrix $`A`$, its Spectral norm is a lower bound to any Ky Fan or Schatten norm.  Thus, all of those norms are submultiplicative [\[H&J12, Thm. 7.4.10.1\]](#cite-handj12). (Note that Horn and Johnson require submultiplicativity in their definition of a matrix norm.)


## Norm Equivalences

Many norm equivalencies derive from the fact that the vector $`L^p`$ and $`L^q`$ norms with $`p \leq q`$ satisfy

$$
||v||_q \leq ||v||_p \leq n^{1/p - 1/q}||v||_q.
$$


The following table provides the $`\alpha`$ such that $`||A||_r \leq \alpha ||A||_c`$ where $`||\cdot||_r`$ is the norm for the row and $`||\cdot||_c`$ is the norm for the column.

| Norm                                     | elementwise $`q`$ norm | elementwise $`\infty`$ norm (max norm) | $`L^q`$ induced norm | Schatten $`q`$ norm | Ky Fan $`l`$ norm |
|------------------------------------------|------------------------|----------------------------------------|----------------------|---------------------|-------------------|
| elementwise $`p`$ norm                   | $`\begin{cases}(mn)^{1/p - 1/q} & p < q\\1& p \geq q\end{cases}`$ | $`(mn)^{1/p}`$ |   |                     |                   |
| elementwise 1 norm (sum norm)            |   $`(mn)^{1 - 1/q}`$   |              $`mn`$                    |                      |                     |                   |
| elementwise 2 norm (Frobenius norm)      | $`\begin{cases}(mn)^{1/2 - 1/q} & 2 < q\\1& 1/2 \geq q\end{cases}`$ | $`\sqrt{mn}`$ | | $`\begin{cases}\min(m,n)^{(1/2 - 1/q)} & 2 < q\\1& 2 \geq q\end{cases}`$ | $`\min(\min(m,n)^{1/2},\min(m,n)/l)`$\* |
| elementwise $`\infty`$ norm (max norm)   |           $`1`$        |             $`1`$                      |         $`1`$        |          $`1`$      |       $`1`$       |
| $`L^p`$ induced norm                     |                        |   | $`\begin{cases}m^{1/p - 1/q} & p \leq q\\n^{1/q - 1/p}& p > q\end{cases}`$ |    |                   |
| $`L^1`$ induced norm                     |                        |              $`m`$                     |   $`m^{1 - 1/q}`$    |                     |                   |
| $`L^2`$ induced norm (Spectral norm)     |                     | $`\sqrt{mn}`$ | $`\begin{cases}m^{1/2 - 1/q} & 2 \leq q\\n^{1/q - 1/2}& 2 > q\end{cases}`$ | $`1`$ | $`1`$ |
| $`L^\infty`$ induced norm                |                        |              $`n`$                     |      $`n^{1/q}`$     |                     |                   |
| Schatten $`p`$ norm                      |           | | | $`\begin{cases}\min(m,n)^{1/p - 1/q} & p < q\\1& p \geq q\end{cases}`$ | $`\min(\min(m,n)^{1/p},\min(m,n)/l)`$\* |
| Schatten 1 norm (Nuclear norm)           |                        |                                        |                   | $`\min(m,n)^{1 - 1/q} `$ | $`\min(m,n)/l`$ |
| Schatten 2 norm (Frobenius norm)         | $`\begin{cases}(mn)^{1/2 - 1/q} & 2 < q\\1& 1/2 \geq q\end{cases}`$ | $`\sqrt{mn}`$ | | $`\begin{cases}\min(m,n)^{(1/2 - 1/q)} & 2 < q\\1& 2 \geq q\end{cases}`$ | $`\min(\min(m,n)^{1/2},\min(m,n)/l)`$\* |
| Schatten $`\infty`$ norm (Spectral norm) |                     | $`\sqrt{mn}`$ | $`\begin{cases}m^{1/2 - 1/q} & 2 \leq q\\n^{1/q - 1/2}& 2 > q\end{cases}`$ | $`1`$ | $`1`$ |
| Ky Fan $`k`$ norm                        |                        |                                        |           | $`\min(\min{m,n}^{1-1/q},k)`$\* | $`\max(1, k/l)`$ |
| Ky Fan $`1`$ norm (Spectral norm)        |                     | $`\sqrt{mn}`$ | $`\begin{cases}m^{1/2 - 1/q} & 2 \leq q\\n^{1/q - 1/2}& 2 > q\end{cases}`$ | $`1`$ | $`1`$ |
| Ky Fan $`\min(m,n)`$ norm (Nuclear norm) |                        |                                        |                   | $`\min(m,n)^{1 - 1/q} `$ | $`\min(m,n)/l`$ |

\* I'm unsure if this bound is tight.


Finally, there are some irregular inequalities between norms.

For the elementwise, $`L^p`$ induced, and Schatten norms, we have that

$$
\|A\|_2 \leq \sqrt{\|A\|_p \|A\|_q}
$$

where $`1/p + 1/q = 1`$.
For the elementwise version and Schatten version, the result follows from using Hölder's inequality with the vector $`L^p`$ norm of either the elements or singular values, respectively.
Finally, the result for the $`L^p`$ induced norms follows from the Riesz-Thorin theorem and the fact that $`\log(\|A\|_p)`$ is a convex function of $`1/p`$ [\[Hig02, (6.18)\]](#cite-hig02).

### Select Justifications

The relations between Schatten $`p`$ norms and the Ky Fan $`k`$ norm can be bound through either the Nuclear norm or the Spectral norm (which form the end points of both the Schatten and Ky Fan norms).
This gives 2 different bounds for each direction, so we can take the minimum.

For the $`L^p`$ and $`L^q`$ induced norms, note that $`p\leq q`$ implies

$$
\|A\|_p = \max_{x\neq 0} \frac{\|Ax\|_p}{\|x\|_p} \leq m^{1/p - 1/q}\max_{x\neq 0} \frac{\|Ax\|_q}{\|x\|_q} = m^{1/p - 1/q}\|A\|_q
$$

and $`p \geq q`$ implies

$$
\|A\|_p = \max_{x\neq 0} \frac{\|Ax\|_p}{\|x\|_p} \leq n^{1/q - 1/p}\max_{x\neq 0} \frac{\|Ax\|_q}{\|x\|_q} = n^{1/q - 1/p}\|A\|_q
$$

So, we have $`\|A\|_p \leq \begin{cases}m^{1/p - 1/q} & p \leq q\\n^{1/q - 1/p}& p > q\end{cases}\|A\|_q`$


### Speculation and Comments

For an $`L^p`$ induced norm, $`||\cdot||_p`$ and the max norm $`||\cdot||_{\max}`$, the pattern suggests that $`||A||_p \leq (m^{1/p}n^{1-1/p})||A||_{\max}`$.

## References


<a name="cite-handj12">\[H&J12\] R. A. Horn and C. R. Johnson, Matrix analysis, 2nd ed. Cambridge university press, 2012. doi: [10.1017/CBO9780511810817](https://doi.org/10.1017/CBO9780511810817)</a>

<a name="cite-hig02">\[Hig02\] N. J. Higham, Accuracy and stability of numerical algorithms, Second. Philadelphia, PA, USA: Society for Industrial and Applied Mathematics, 2002. doi: [10.1137/1.9780898718027](https://doi.org/10.1137/1.9780898718027).</a>

<a name="cite-lld25">\[LLD25\] [1] N. Lindquist, P. Luszczek, and J. Dongarra, “The stability of block eliminations and additive modifications,” Sep. 09, 2025, [arXiv:2509.07305](http://arxiv.org/abs/2509.07305). </a>
