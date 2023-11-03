---
layout: single
title:  "Strain measure"
categories: Advanced_Solid_mechanics
typora-root-url: ../
use_math: true
---

Ch 3.4 Strain measures

- Cauch-Green deformation tensors :
  General measure of "deformation" of a medium indepent of both translation and rotation
  <img src="/images/2023-10-30-Strain measure/image-20231030203417905.png" alt="image-20231030203417905" style="zoom:50%;" />
  two material particles $P$ and $Q$ are deformed into $\bar{P}$ and $\bar{Q}$
  distance between $P$ and $Q$ $\Rightarrow$ vector $d\vec X$
  distance between $\bar{P}$ and $\bar{Q} \Rightarrow$ vector $d\vec x$
  - Change in distances
    $(dS)^2 = d\vec X \cdot d\vec X$
    $(ds)^2 = d\vec x \cdot d\vec x = d\vec X \cdot (\vec F^T \cdot \vec F) \cdot d\vec X$    &#42; $(d\vec x = d\vec X \cdot \vec F^T)$
    	   $= d\vec X \cdot \vec C \cdot d\vec X$
    $\vec C = \vec F^T \cdot \vec F \Rightarrow$ right Cauchy-Green deformation tensor
    $\vec C :$ 2nd order symmetric tensor
    $\vec B = \vec F \cdot \vec F^T \Rightarrow $ left Cauchy-Greeen deformation tensor

- Green-Lagrange strain tensor(Material description)

  - Change in squarred length before and after deformation
    $(ds)^2 - (dS)^2 = d\vec X \cdot (\vec F^T \cdot \vec F) \cdot dX - d\vec X \cdot d\vec X\; \text{(Lagrangian description)}$

    $ = 2d\vec X \cdot \vec E \cdot d\vec X \qquad \text{related}\quad  \epsilon = \frac{dl - dL}{L}$

  - $\eqalign{\vec E &= \frac{1}{2}(\vec F^T \cdot \vec F - \vec I) = \frac{1}{2} (\vec C - \vec I) \\
     &= \frac{1}{2}((\vec I + \nabla_0 \vec u)\cdot (\vec I + \nabla_o \vec u)^T)\\
    & = \frac{1}{2}(\nabla_0 \vec u + (\nabla_0 \vec u)^T + (\nabla_0 \vec u)\cdot (\nabla_0 \vec u)^T)}$

    If no deformation, $\vec C = \vec I \Rightarrow E = 0 \quad \text{because } (d\vec s)^2  - (d\vec S)^2 = 0$

  - In component form

    $\vec E = \frac{1}{2}\left(\frac{\partial u_I}{\partial X_J}+ \frac{\partial u_I}{\partial X_I} + \frac{\partial u_k}{\partial X_I}\frac{\partial u_k}{\partial X_J}\right)$