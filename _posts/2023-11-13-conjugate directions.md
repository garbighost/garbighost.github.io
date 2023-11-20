---
layout: single
title:  "Conjugate directions"
categories: Optimal_design_class
typora-root-url: ../
use_math: true
---

- Conjugate directions
  Given : A : $n \times n$ positive definite symmetric matrix
  &#42; 실제 존재하는 것의 matrix는 symmetric matrix
  $d^j : $ conjugate direction, if $(\vec d^j)^T \vec A \vec d^i = 0 \; \text{for} \; i \neq j$

  e.g.)  $\vec A$ : 3x3 symmetric matrix

  ​	$\vec e_i$ : eigenvector of $\vec A (\vec e_i \vec A \vec e_j \triangleq \delta_{ij})$

  ​	Then $e_1, e_2, e_3 : conjugate directions$

  ​	$e_1 + e_2, e_1 - e_2, e_3$ : conjugate directions

- n iteration convergence

  Then minimum of a quadratic function of n variables is found in n iteration or less.

  1. Consider $Q(x) = \frac{1}{2} \vec x^T \vec A \vec x + \vec B^T \vec x + C$

     $\vec A$ : positive definite, symmetric **matrix**

     $Q(x)$ : Quadratic function ($\fallingdotseq$2차 함수)

     $\vec x^T \vec A \vec x$ : scalar

     $\vec B$ : vector 

     $\vec B^T \vec x$ : scalar

     $\vec x = {x_1, x_2, \cdots , x_n}^T$

     Let $x^* = min. pt. , \text{then}$

     $\vec \nabla Q(\vec x^*) = \vec A x^* + \vec B = 0 \cdots (1)$

     Expand $\vec x^*$ in terms of orthogonal $\vec d^i$ w.r.t $\vec A$ such that

     $x^* = \vec x^0 + \sum_{i=1}^{n-1} \beta^i \vec d^i \cdots (2)$

     $\vec x^0$ : arbitrary starting pt.

     $\beta^i$ : constant

     To determine $\beta^i$, put (2) into (1)

     $\vec A(\vec x^0 + \sum_{i=1}^{n-1}\beta^i \vec d^i) + \vec \beta = 0$

     multiply $(\vec d^j)^T$

     $(\vec d^j)^T (\vec B + \vec A \vec x^0) + \sum_{i=1}^{n-1} \beta^i  (\vec d^j)^T \vec A \vec d^i = 0$

     if $i \neq j, (\vec d^j)^T \vec A \vec d^i = 0$

     if $i = j, (\vec d^j)^T \vec A \vec d^i \Rightarrow (\vec d^j)^T \vec A \vec d^j \neq 0$

     &#42; $(\vec d^i)^T \vec A^T = (\vec d^i)^T\vec A \qquad   b.c.s (A^T = A)$

     $\eqalign{\beta^j &= -\frac{(\vec d^j)^T(\vec B + \vec A \vec x^0)}{(\vec d^j)^T \vec A \vec d^j}\\
     &= -\frac{(\vec B + \vec A \vec x^0)^T \vec d^j}{(\vec d^j)^T \vec A \vec d^j} \; , j= 0,1,\cdots ,n-1 \quad \cdots (3)\\
     &\rightarrow * \; A^Td = d^TA}$
     
     $\Rightarrow$ Message : for any starting point $\vec x^0$, the min. $\vec x^*$ of $Q(\vec x)$ is expressed in terms of **n** conjugate directions $\vec d^i$, expansion coefficients $\beta^i$are computed by (3)
  
  - How to find $\vec d$ ?
  
    For quadratic function $Q(\vec x) = \frac{1}{2} \vec {x}^T \vec A \vec x + \vec B \vec x + C$
  
    $\vec d^0 = -\vec g^0 ; \quad \vec g = \vec \nabla Q$
  
    $\vec d^{k+1} = -\vec g^{k+1} + \beta^k\vec d^k \quad (k \geq 1)$
    where $\beta^k = \frac{(\vec g^{k+1})\vec A \vec d^k}{(\vec d^k)^T \vec A \vec d^k}$
  
    For non-qaudratic function $f(\vec x), \text{replace} \;\; \beta^k \; \text{as} \; \beta^k = \frac{(\vec g^{k+1})^T g^{k+1}}{(\vec g^k)^T \vec g^k}$
  
    &#42; Here, $\beta^k$ is no second - derivative information such Hessian is needed due to Fletcher-Reeve(1964)
  
    &#42; $\vec g$ : first order derivative
  
  - Fletcher - Reeves conjugate gradient method (10.8)
  
    1. Start with any $\vec x^0$
  
    2. Search direction
  
       if $k = 0, \quad \vec d^k = -\vec g ^k = - \vec \nabla f(\vec x^k)$
  
       else ($k \geq 1$), $\vec d^k = -\vec g^k + \beta^{k-1} \vec d^{k+1}$
  
       where $\beta^{k-1} = \frac{+(\vec g^k)^T +\vec g^k}{+(\vec g^{k-1})^T+\vec g^{k-1}} = \frac{||\vec \nabla f(\vec x^k) ||^2}{||\vec \nabla f(\vec x^{k-1}) ||^2}$
  
    3. 1D line search
  
       $\vec x^{k+1} = \vec x^k + \alpha^k \vec d^k$
  
       where $\alpha^k = -\frac{(\vec d^k)^T g^k}{(\vec d^k)\vec A \vec d^k} = \frac{(\vec g^k)^T \vec g^k}{(\vec d^k)^T \vec A d^k}$
  
    Remark
  
    1. This method applies to non-quadratic function minimization.
    2. **n** iteration convergence is valid only for quadratic function
    3. may need to reset $\vec d^k$ for every **n** step
  
    
  
    e.g.) 
  
    $\eqalign{f(\vec x) &= x_1^2 + 4x_2^2\\& = \frac{1}{2} (x_1, x_2) \begin{bmatrix} 2 & 0\\ 0 & 8 \end{bmatrix} \begin{Bmatrix} x_1\\ x_2 \end{Bmatrix} \\
    &= \frac{1}{2} \vec x^T \vec A \vec x }$
  
    $\vec x^0 = (1,1)^T \leftarrow $ starting point 
  
    Iteration 1
  
    1. search direction
  
       $\vec d^0 = - \vec \nabla f(\vec x^0) = - \begin{bmatrix}\partial f / \partial x_1\\ \partial f / \partial x_2\end{bmatrix}_{x = x^0} = - \begin{bmatrix}2x_1 \\ 8x_2\end{bmatrix}_{\vec x = (1, 1)^T} = (-2, -8)^T$
  
    2. 1D line search
  
       $\alpha^0 = \frac{(\vec g^0)^T \vec g^0}{(\vec d^0)^T \vec A \vec d^0} = \frac{(2,8)\begin{pmatrix}2 \\ 8\end{pmatrix} }{(-2, -8) \begin{bmatrix} 2 & 0 \\ 0 & 8 \end{bmatrix}\begin{pmatrix}-2 \\ -8 \end{pmatrix}} = 0.1308$
  
       $\vec x^1 = \vec x^0 + \alpha^0 d^0 = (1,1)^T + 0.1308(-2, -8)^T = \begin{pmatrix}0.7385 \\ -0.0462 \end{pmatrix}$
  
    Iteration 2
  
    1. Search direction
    
       $\vec d^1 = -\vec g^1 + \beta^0 \vec d^0$
    
       $\beta^0 = \frac{||\vec \nabla  f(\vec x^1) ||^2}{||\vec \nabla f(\vec x^0) ||^2} = \frac$
    
       