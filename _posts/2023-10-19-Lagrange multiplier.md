---
layout: single
title:  "Lagrange multiplier"
categories: Optimal design class
typora-root-url: ../
use_math: true
---

- Necessary condition for equality-constrained problem (ch 4.5)
  - Equality constrained problem
    $\underset{x}{minimize}\; f(x)$ subject to $h_j(x) = 0, \;j=1,2,\cdots,p$
    
    e.g. $\underset{x}{minimize}\; f(x_1,x_2) = (x_1 -1.5)^2 + (x_2 - 1.5)^2$
    
    ​	subject to $h(x_1, x_2) = x_1 + x_2 -2 =0$
    
    1. Graphical solution
       <img src="/images/2023-10-19-Lagrange multiplier/image-20231019133600701.png" alt="image-20231019133600701" style="zoom:50%;" />
       - Regular point : a point $x^*$ satisfying the constraints $h(x^*) = 0$
         if
         (1) $f(x^*) :$ differentiable
         (2) $\underline{\nabla} h(x^*)$ : linearly independent => No gradient can be expressed with a combination  of other gradients if $\sum_{k=1}^{m} \vec\alpha_k \vec{v}_k = 0, all\; \vec\alpha_k = 0$
    2. Solving with the reduced objective function
       $x_2 = \phi(x_1) = -x_1 + 2$
       $\begin{align*}\underset{x}{minimize} \; f(x_1,x_2) = f(x_1, \phi(x_1)) &= (x_1 -1.5)^2 + (-x_1 + 2 -1.5)^2\\ &= 2(x_1 -1)^2 + 0.5 \end{align*}$
       $\Rightarrow \; x^* = (1,1),\; f(x^*) = 0.5$
       Solving with the reduced objective function means that "Equality constrained problem $\Rightarrow \; $Unconstrained problem"
    3. Lagrange multiplier
       - Lagrange multiplier with two design variables
         $\frac{\partial f(x_1^*, x_2^*)}{\partial x_1} + v\frac{\partial h(x_1^*, x_2^*)}{\partial x_1} = 0$
         $v = $