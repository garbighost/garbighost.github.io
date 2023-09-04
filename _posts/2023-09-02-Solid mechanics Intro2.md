---
layout: single
title:  "Solid mechanics Intro2"
typora-root-url: ../
use_math: true
---

# Advanced Solid mechanics Design Intro2

- Engineering Design  vs  Design Optimization

  - Engineering design : Aims to find(determine) a design(demensions and materials) to meet well-defined specifications

    - Procedures

      1. Generate a large number of potential solution (Conceptual design)

      2. Choose few candidates by evaluating cost, weight, max stress, and/or manufacturability

         (size reduction result in cost saving, bus raise possibility of mechanical failure)

      3. Choose one to two candidates, fabricate prototype, and test

         <img src="/images/2023-09-02-Solid mechanics Intro2/4.png" alt="4" style="zoom:50%;" />

         

  - Design Optimization : Aims to find and optimal design for maximizing a specific performance functions 
                                           with meeting the requirement defined as constraint
                                           e.g. 
                                                      Minimize  cost
                                                      Subject to $\sigma_{max} \leq \sigma_{allowalbe}$



- Review of solid mechanics under various loading
  - long, straight, slender members used to support mechanical load.
    - Truss : only axial loading
    - Frame : multi axial loading
    - Beam : Forces at various points
    - Cable : withstand only tension
      <img src="/images/2023-09-02-Solid mechanics Intro2/6 2023-09-02 07_21_47.png" alt="6 2023-09-02 07_21_47" style="zoom: 33%;" />

  - FBD 그리는 법 pdf
    http://contents.kocw.net/KOCW/document/2015/kumoh/ohchungseok/5.pdf



- Axial loading

  <img src="/images/2023-09-02-Solid mechanics Intro2/image-20230904133516955.png" alt="image-20230904133516955" style="zoom:33%;" />

  Axial stress $\sigma = \frac{P}{A}$

  Axial strain $\epsilon = \frac{\sigma}{L}$

  Axial deformation $\sigma = \frac{PL}{AE}$

  

- Shear stress by shear loading

  <img src="/images/2023-09-02-Solid mechanics Intro2/노트 2023. 8. 30. (2) 2023-09-04 04_38_43.png" alt="노트 2023. 8. 30. (2) 2023-09-04 04_38_43" style="zoom:33%;" />

  shear stress $\tau = \frac{VQ}{IT}$

  &#42; Q : first moment above the point (first moment of area) 
  &#42; $I$ : moment of Inertia

  &#42; t : width

  

-  Bending of Beams

  <img src="/images/2023-09-02-Solid mechanics Intro2/노트 2023. 8. 30. (2) 2023-09-04 04_42_49.png" alt="노트 2023. 8. 30. (2) 2023-09-04 04_42_49" style="zoom:33%;" />


  &#42; Neutral plane where $\sigma_{zz} = 0$ is defined as $y=0$

  - Euler-Bernoulli beam

    $\frac{Mx}{Ix} = \frac{\sigma_{zz}}{y} = \frac{E}{R} = -E \frac{d^2 u_y}{dz^2}$

    &#42; R : radius of curvature

    &#42; $I$ : 2nd moment of Inertia

    => can be extended into unsymmetrical bending.



- Torsion of circular bars

  <img src="/images/2023-09-02-Solid mechanics Intro2/노트 2023. 8. 30. (2) 2023-09-04 04_49_20.png" alt="노트 2023. 8. 30. (2) 2023-09-04 04_49_20" style="zoom:33%;" />

  shear stress $\tau$

  $\frac{T}{J}=\frac{\tau}{r} = G\phi$

  &#42; $J$ : polor 2nd moment of inertia

  &#42; $G$ : shear modulus

  &#42; $r$ : radial distance



- Beam under combined loads

  <img src="/images/2023-09-02-Solid mechanics Intro2/노트 2023. 8. 30. (2) 2023-09-04 04_54_10.png" alt="노트 2023. 8. 30. (2) 2023-09-04 04_54_10" style="zoom:33%;" />

  Internal forces : $P_z,\; V_x,\; V_y$

  &#42; $P_z$ : Normal stress

  &#42; $V_x,\; V_y$ : shear stress

  Moments : $M_x,\; M_y,\; M_z$

  &#42; $M_x,\; M_y \propto $ normal stress

  &#42; $M_z \propto$ shear stress

  

-  Statically Indeterminate problem

  <img src="/images/2023-09-02-Solid mechanics Intro2/노트 2023. 8. 30. (2) 2023-09-04 05_08_01.png" alt="노트 2023. 8. 30. (2) 2023-09-04 05_08_01" style="zoom:33%;" />

  Three unknowns : $R_A, M_A, R_B$

  Two static equation : $\begin{align*}
  &\sum{F_y} = 0
  &\sum{M} = 0 \end{align*}$


  How to solve it??

  - Replace redundant reactions with external forces, and apply kinematics conditions.

    <img src="/images/2023-09-02-Solid mechanics Intro2/노트 2023. 8. 30. (2) 2023-09-04 05_13_23.png" alt="노트 2023. 8. 30. (2) 2023-09-04 05_13_23" style="zoom: 50%;" />

    Additional equation : $u_B = 0$

