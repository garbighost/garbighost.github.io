---
layout: single
title:  "Energy Method"
typora-root-url: ../
use_math: true
---

&#42; Two approaches in structural Analysis for finding stress and displacement distribution of loaded structure.

1. ​	Direct approach (Related to "Strong Form" approach)
   - Solve equilibrium equation and boundary conditions "Directly" to determine displacement or stress.
   - Equilibrium equation (Governing equation) is derived from linear momentum conversation law (simply $\sum F = ma$)
2. Energy approach (Related to "Weak Form" approach)
   - Subset of broader class of methods based on "Variational method"
   - Fundamentals for "Finite element method (FEM)"

- Concept of two approaches in spring-mass system.
  <img src="/images/2023-09-11-Energy Method/image-20230913113029744.png" alt="image-20230913113029744" style="zoom:50%;" />

  (1) Direct approach
  $\sum F = F - ku = 0\\
  u = \frac{F}{k}$

  (2) Energy approach

  Minimizing  $\frac{1}{2}ku^2 - Fu$
  $\Rightarrow u = \frac{F}{k}$

  

  