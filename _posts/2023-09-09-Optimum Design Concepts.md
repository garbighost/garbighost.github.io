---
layout: single
title:  "Optimum Design Concepts"
categories: Optimal design class
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

    - Set S is bounded $\Leftrightarrow\; any\; x \in S,\; x^Tx < c$

      <img src="/images/2023-09-09-Optimum Design Concepts/09112 2023-09-10 16_25_15.png" alt="09112 2023-09-10 16_25_15" style="zoom: 33%;" />
      &#42; bounded concept : There is a subset S of a 2-dimensional real space $R^2$ constrained by
         tow parabolic curves $x^2 + 1$ and $x^2 - 1$ defined a Cartesian coordinate system is closed by the curves
      
         but unbounded.
      
      <img src="/images/2023-09-09-Optimum Design Concepts/09113.png" alt="09113" style="zoom:50%;" />

- Basic calculus concepts (ch4.2)

  - Vectors $x = \{x_1, x_2, x_3, \cdots ,x_n\}^T \in R^n$

  - Sets

    close set : $S = \{\vec{x}\mid|x| \leq 1\}$

    open set : $S = \{x \mid |x| < 1\}$

    Bounded Set : for $x \in S,\; x^Tx \leq \infty$

    Compact Set : closed and bounded

  

  - Gradient vector (Partial derivative of a function)
  
    $\nabla f = \begin{bmatrix}
    \frac{\partial f}{\partial x_1} \\
    \frac{\partial f}{\partial x_2} \\ 
    \vdots\\
    \frac{\partial f}{\partial x_n}
    \end{bmatrix}$
  
  - Hassian matrix (Second order partial derivative)
  
    $\nabla^2 = H = \begin{bmatrix}
    \frac{\partial^2 f}{\partial x_1 \partial x_1} & \frac{\partial^2 f}{\partial x_1 \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_1 \partial x_n}\\
    \frac{\partial^2 f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2 \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_2 \partial x_n}\\
    \vdots\\
    \frac{\partial^2 f}{\partial x_n \partial x_1} & \frac{\partial^2 f}{\partial x_n \partial x_2} & \cdots & \frac{\partial^2 f}{\partial x_n \partial x_n}
    \end{bmatrix}$
  
    $H = H^T$ (symmetric matrix always)
  
  - Taylor's expansion
    1. single variable x
       $f(x) = f(x^*) + \frac{df(x^*)}{dx}(x-x^*) + \frac{1}{2}\frac{d^2f(x^*)}{dx^2}(x-x^*)^2$
       Let = $x-x^* = d$
       $f(x^*+d) = f(x^*) + \frac{df(x^*)}{dx}d + \frac{1}{2}\frac{d^2f(x^*)}{dx^2}d^2+ \cdots$
    
    2. Two variables $x_1, x_2$
    
       $\begin{align*}
       f(x_1^* + d_1, x_2^* + d_2) = &f(x_1^*, x_2^*) + \frac{\partial f}{\partial x_1}d_1 + \frac{\partial f}{\partial x_2}d_2\\
       &+\frac{1}{2}\{\frac{\partial^2 f}{\partial x_1^2}d_1^2 + 
       2\frac{\partial^2 f}{\partial x_1 \partial x_2}d_1d_2 +
       \frac{\partial^2 f}{\partial x_2^2}d_2^2\}\\
       &+ \cdots \end{align*}$
       Using summation notation
    
       $= f(x_1^*, x_2^*) + \sum_{i=1}^{2} \frac{\partial f}{\partial x_i}d_id_j + \cdots$
    
       Using matrix notation
    
       $f(\vec{x^*} + \vec{d}) = f(\vec{x^*}) + (\vec{\nabla} f)^Td + \frac{1}{2}\vec{d^T}\vec{H}\vec{d} + \cdots$
    
       Let $\vartriangle f = f(\vec{x^*}+\vec{d}) - f(x^*)$
    
       $\vartriangle f = (\vec{\nabla} f)^T\vec{d} + \frac{1}{2}\vec{d}^T\vec{H}\vec{d} + \cdots$
  
  
  
  - Quadratic form (Q-form) and definite matrix
  
    1. Q-form
       $f = \sum_{i=1}^n\sum_{j=1}^n P_{ij}x_ix_j = \vec{x}^T\vec{P}\vec{x}$
  
       e.g. 
       $\begin{align*}f &=x_1^2 -6x_1x_2 + 9x_2^2\\
       &= \{x_1,x_2\}\begin{bmatrix}
       1&-3\\
       -3&9\end{bmatrix}\begin{Bmatrix}
       x_1\\
       x_2\end{Bmatrix}\end{align*} = \vec{x}^T \vec{P}\vec{x}$
  
    2. Positive definiteness (P-D) of Q form
       P - D if $f(\vec{x}) > 0$ for all non zero $\vec{x}$
  
       P - Semi D if $f(\vec{x}) \geq 0$ for all $\vec{x}$
  
       <img src="/images/2023-09-09-Optimum Design Concepts/09114.png" alt="09114" style="zoom: 25%;" />
  
       e.g. $f = \frac{1}{3} x^2$ : P - D
       $f > 0 \quad for \; x \neq0$
  
       $f = 0 \quad iff \; x=0$
       
  
       $f = \frac{1}{3}x_1^2 + \frac{3}{2}x_2^2$ : P - D
  
       $f > 0 \; for \; x_1 = x_2 \neq 0$
  
       $f = 0 \quad iff \; x_1 = x_2=0$
  
       Then, What is the P-D or P-semiD ?
       $f = x_1^2 -2x_1x_2 + 2x_2^2$ (?) $\rightarrow$ P-semiD
  
       $f=x_1^2 -2x_1x_2 + x_2^2$ (?) $\rightarrow$ P-D
  
       
  
       How to check P-D of $x^T P x$ ?
  
       1. Check eigenvalues of P
       2. Sylvecter's test (Using principal minors)
  
  
  
    Q-form $f(x) = x^TAx$    -> (x에 대해 2차 함수)
  
  ​	$\Leftrightarrow$ P-D  if $f(x) > 0, x \neq 0$
  
  ​	$\Leftrightarrow$ eigenvalue $\lambda_i > 0$
  ​    
  $Ax = \lambda x$    
  $f(x) = x^T\lambda x = \{x_1, x_2\}
  \begin{bmatrix}\lambda_1 & 0\\
  0 & \lambda_2\end{bmatrix}\begin{Bmatrix}x_1 \\ x_2\end{Bmatrix} = \lambda_1x_1^2 + \lambda_2x_2^2 > 0 \Rightarrow (\lambda_1>0, \lambda_2 > 0)$
  
  
