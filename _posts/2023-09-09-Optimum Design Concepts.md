---
layout: single
title:  "Optimum Design Concepts"
typora-root-url: ../
use_math: true
---

# Optimum Deisgn Concepts

- Global and local minima (Ch4.1)

  - Global minimum

    $f(x^*) \leq f(x)$ for all $x$ in the feasible sets

  - Local minimum

    $f(x^*) \leq f(x)$ for all $x$ in a small neighborhood $N$ of $x^*$ in the feasible set S

    $N = \{x|x \in S\; with\; \Vert x -x^* \Vert < \sigma\}\\
     where\; \sigma : small real number$ 
    <img src="/images/2023-09-09-Optimum Design Concepts/09091.png" alt="09091" style="zoom:33%;" />

  

  - Existence of a minimum
    Weier strass theorem : $f(x)$ is continuos on a non-empty feasible set S that
    closed and bounded, then $f(x)$ has a global minimum in S.

    - Set S is closed $\Leftrightarrow a \leq x \leq b$ 

    - Set S is bounded $\Leftrightarrow\; any\; x \in S,\; x^Tx < S$

      &#42; bounded concept : There is a subset S of a 2-dimensional real space $R^2$ constrained by
         tow parabolic curves $x^2 + 1$ and $x^2 - 1$ defined a Cartesian coordinate system is closed by the curves

         but unbounded.

- Basic calculus concepts (ch4.2)

  - Vectors $x = \{x_1, x_2, x_3, \cdots ,x_n\}^T \in R^n$

  - Sets

    close set : $S = \{\vec{x}\mid|x| \leq 1\}$

    open set : $S = \{x \mid |x| < 1\}$

    Bounded Set : for $x \in S,\; x^Tx \leq \infin$

    Compact Set : closed and bounded

  

  - Gradient vector (Partial derivative of a function) AAA

