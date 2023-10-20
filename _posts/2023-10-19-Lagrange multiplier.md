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
         (2) $\underline{\nabla} h(x^*)$ : linearly independent => No gradient can be expressed with a combination  of other gradients if 
    
         ------
    
         $\sum_{k=1}^{m} \vec\alpha_k \vec{v}_k = 0, all\; \vec\alpha_k = 0$​
    
    2. Solving with the reduced objective function
       $x_2 = \phi(x_1) = -x_1 + 2$
       $\begin{align*}\underset{x}{minimize} \; f(x_1,x_2) = f(x_1, \phi(x_1)) &= (x_1 -1.5)^2 + (-x_1 + 2 -1.5)^2\\ &= 2(x_1 -1)^2 + 0.5 \end{align*}$
       $\Rightarrow \; x^* = (1,1),\; f(x^*) = 0.5$
       Solving with the reduced objective function means that "Equality constrained problem $\Rightarrow \; $Unconstrained problem"
    
    3. Lagrange multiplier
    
       - Lagrange multiplier with two design variables
    
         $\frac{\partial f(x_1^*, x_2^*)}{\partial x_1} + v\frac{\partial h(x_1^*, x_2^*)}{\partial x_1} = 0$
    
         $v = -\frac{\partial f(x_1^*, x_2^*) / \partial x_2}{\partial h(x_1^*, x_2^*)/\partial x_2}$
    
       - Derivation
    
         &#42; chain rule 
         $\frac{dz}{dt} = \frac{\partial z}{\partial x}\frac{dx}{dt} + \frac{\partial z}{\partial y}\frac{dy}{dt}$
    
         Chain rule of $\frac{df}{dx}$ **at the optimum point.** $(x_1^*, x_2^*)$
    
         $\frac{df(x_1^*, x_2^*)}{dx_1} = \frac{\partial f(x_1^*, x_2^*)}{\partial x_1} + \frac{\partial f(x_1^*, x_2^*)}{\partial x_2}\frac{dx_2}{dx_1} = 0 \cdots (1)$
    
         Since $x_2 = \phi(x_1)$
    
         $\frac{\partial f(x_1^*, x_2^*)}{\partial x_1} + \frac{\partial f(x_1^*, x_2^*)}{\partial x_2}\frac{d \phi}{dx_1} = 0 \; \cdots (2)$ 
         From (2) $\frac{d \phi}{dx_1} = -\frac{\partial h(x_1^*, x_2^*)/\partial x_1}{\partial h(x_1^*, x_2^*)/\partial x_2} \cdots (3)$
         Put (3) into (2)
         $\frac{\partial f(x_1^*, x_2^*)}{\partial x_1} + \frac{\partial f()x_1^*, x_2^*}{\partial x_2}\left(-\frac{\partial h(x_1^*, x_2^*)/\partial x_1}{\partial h(x_1^*, x_2^*)/\partial x_2}\right) = 0 \cdots (4)$
    
         $v = -\frac{\partial f(x_1^*, x_2^*)/\partial x_2}{\partial h(x_1^*, x_2^*)/\partial x_2} \cdots (5)$
         
    
         $\frac{\partial f(x_1^*, x_2^*)}{\partial x_1} + v\frac{\partial h(x_1^*, x_2^*)}{\partial x_1} = 0 \cdots (6)$
         
    
         Rearranging (5) $\frac{\partial f(x_1^*, x_2^*)}{\partial x_2} + v\frac{\partial h(x_1^*, x_2^*)}{\partial x_2} = 0 \cdots (7)$
         (6),(7) in the vector notation
    
         $\nabla f(x^*) + v \nabla h(x^*) = 0$
    
         
    
       - Lagrange multiplier theorem (<= Necessary Condition)
         If $x^*$ is a regular point and a local minimum for the problem, then there exist a vector $v_j^*$ such that
         $\frac{\partial f(x^*)}{\partial x_i} + \sum_{j=1}^{p} v_j^* \frac{\partial h_j(x^*)}{\partial x_i} =0, \; i=1,\cdots,n$
         $h_j(x^*) = 0,\; j=1,\cdots,p$
         $v_j^*$ are called the lagrange multipliers.
    
       - e.g.) minimize $f(x_1, x_2) = (x_1 -1.5)^2 + (x_2 -1.5)^2$
         subject to $h(x_1, x_2) = x_1 + x_2 - 2 = 0$
         $\frac{\partial f}{\partial x_1} + v\frac{\partial h}{\partial x_1} = 0 \rightarrow \; 2(x_1 - 1.5) + v(1) = 0$
    
         $\frac{\partial f}{\partial x_2} + v\frac{\partial h}{\partial x_2} = 0 \rightarrow \; 2(x_2 - 1.5) + v(1) = 0$
         $h = 0 \rightarrow \; x_1 + x_2 -2 = 0$
         Solving above equations
         $x^* = (1,1), v = 1, f(x^*) = 0.5$
         this is necessary condition.
         So we have to check that this is satisfied with sufficient condition.
    
         $\nabla f = \begin{bmatrix}\frac{\partial f}{\partial x_1} \\ \frac{\partial f}{\partial x_2}\end{bmatrix}$ $\nabla f(\vec x^*) = \begin{bmatrix}-1 \\ -1 \end{bmatrix}$
    
         $\nabla h = \begin{bmatrix}\frac{\partial h}{\partial x_1}\\ \frac{\partial h}{\partial x_2}\end{bmatrix}$ $\nabla h(\vec x^*) = \begin{bmatrix}1 \\ 1\end{bmatrix}$
    
         cf. $\nabla f(0.4, 1.6) = \begin{bmatrix}-2.2 \\ 0.2\end{bmatrix}$
    
         $\nabla h (0.4,1.6) = \begin{bmatrix}1 \\ 1\end{bmatrix}$
    
         $\nabla f(0.4, 1.6) \neq v\nabla h(0.4, 1.6)$
    
         <img src="/images/2023-10-19-Lagrange multiplier/image-20231020221108351.png" alt="image-20231020221108351" style="zoom:67%;" />
    
         &#42; Remark : By Lagrange's theorem, constrained problems are treated as unconstrained  problems.
    
         Lagrange multiplier theorem in therms of a lagrange function
    
         $L(\vec x, \vec v) = f(\vec x)   + \sum_{j=1}^{p}v_j h_j(x)$
    
         $= f(\vec x) + \vec v^T h(\vec x)$
    
         $\frac{\partial L(x^*, v^*)}{\partial x_i} = 0, \; i=1,\cdots, n$
    
         $\frac{\partial L(x^*, v^*)}{\partial v_j} = 0 \Rightarrow h_j(x^*) = 0, \; j=1,\cdots,p$
    
         
    
         How to make an inequality constrainnt to an equality constraint
    
         $x_1^2 + 2x_2^2 \leq 0$ : inequality const
         $\Downarrow$
         $x_1^2 + 2x_2^2 + S^2 = 0$ : equality const
    
       - Necessary condition for a general constrained problem(4.6)
         &#42; Standard design optimization model
         $\underset{x}{minimize} \; f(\vec x)$
         $s.t. h_j(\vec x)= 0,\; j=1,\cdots,p, \; g_k(\vec x )\leq 0,\; k=1,\cdots,m$
    
         e.g.) minimize $f(\vec x) = (x_1 -14)^2 + (x_2 - 11)^2$
    
         $g_1(x) = x_1 + x_2 - 19 \leq 0$
    
         $g_2(x) = (x_1 -11)^2 + (x_2-13)^2 -7^2 \leq 0$
    
         <img src="/images/2023-10-19-Lagrange multiplier/image-20231020224050078.png" alt="image-20231020224050078" style="zoom: 67%;" />
    
         observation at $x = x^*$
         (1) $g_1(x^*) = 0 \rightarrow$ active constraint
    
         (2) $g_2(x^*) = -24 \neq 0 \rightarrow$ Inactive constraint
    
         Need to consider active constraints
    
         only ignore inactive constraints
    
         $\downarrow$ 
    
         Rewrite the problem
    
         minimize $f(\vec x) = (x_1-14)^2 + (x_2-11)^2$
    
         $s.t. g_1(x) = x_1 + x_2 - 19 = 0$
    
         -> But how to find which constraints are active at optimality?
    
         -> Switching condition : $u_j^* S_j = 0$
         	$g_1(\vec x) + S_1^2 = 0$
    
         if $S_1^2 = 0 \Rightarrow g_1(x) = 0$ (active), $u_1 \geq 0 \cdots (1)$
    
         if $S_1^2 > 0 \Rightarrow g_1(\vec x) < 0$ (inactvie), $u_1 = 0 \cdots (2)$
    
         From (1),(2)  $u_1^* S_1 = 0$
    
         $u_j^*$ : Lagrange multiplier for the $j$th inequality constraint. 
    
         $u_j^* \geq 0; \; j = 1, \cdots, m$
    
    4. Karush - Kuhn - Tucker (KKT) condition (<= Necessary condition)
       $x^*$ is a regular point of the feasible set and a local minimum for $f(\vec x) \; s.t. h_j(\vec x) = 0, \; g_j(x) \leq 0$
       The Lagrange function L is given by
       $L(\vec x, \vec v, \vec u, \vec s) = f(\vec x) + \sum_{i=1}^p v_ih_i(x) + \sum_{j=1}^m u_j(g_j(x) + S_j^2)$
    
       $= f(\vec x) + \vec{v}^Th(\vec x) + \vec u^T(g(\vec x) + S^2)$ 
    
       KKT  conditions are
    
       1. Stationary
          $\frac{\partial L}{\partial x_k} = \frac{\partial f}{\partial x_k} + \sum_{i=1}^p v_i^* \frac{\partial h_i}{\partial x_k} + \sum_{j=1}^m u_j^* \frac{\partial g_i}{\partial x_k} = 0; \; k=1,\cdots,n$
    
          $\frac{\partial L}{\partial v_i} = 0 \quad (\Rightarrow h_i(\vec x^*)); \; i=1,\cdots,p$
    
          $\frac{\partial L}{\partial u_j} = 0 (\Rightarrow g_i(x^*) + S_j^2 = 0); \; j=1,\cdots,m$
    
       2. Switching conditions
          $\frac{\partial L}{\partial S_j} = 0 (\Rightarrow 2u_j ^* S_j = 0)$                       * : 내적 일듯?
    
       3. Feasibility check $S_j^2 \geq 0 (\Rightarrow g_j \leq 0)$
    
       4. Non-negativity check $u_j^* \geq 0$
       
       