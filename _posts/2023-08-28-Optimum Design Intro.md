---
layout: single
title:  "Optimum Design Intro"
typora-root-url: ../
use_math: true
---



- Engineering design

  To calculate the size and shapes.

- Engineering analysis

  To determine the behavior of an existing system.



Ch 2 Optimum Design Problem Formulation

- Example : Design of a can (ch 2.2)

<img src="/images/2023-08-28-Optimum Design Intro/image-20230828131207770.png" alt="image-20230828131207770" style="zoom:33%;" />

Volume V must be at least 400mL

$3.5cm \leq D \leq 8cm$

$8cm \leq H \leq 18cm$

Cost of metal sheet : $ \$0.008/cm^2$

-- Build a can with minimum cost

​                        $\Downarrow$ formulate

- Mathmatical formulation

  Object function $f(D, L) = [\pi DH + 2\left(\frac{\pi}{4}D^2)\right]\times 0.008$

  
  
  constraints 
  
  1. $\frac{\pi}{4}D^2H \geq 400cm^3$
  1. $3.5cm \leq D \leq 8cm$
  1. $8 \leq H \leq 18cm$

 

- General Mathematical Model (ch 2.11)

  - Standard design optimization model

    $\underset{x}{minimize} \quad f(x)$   $\leftarrow$  objective function (or cost, loss)
    
    $\begin{align*} 
    subject\;to\; &g_i(x) \leq 0,\; i=1,2,\cdots,m\\
    &h_j(x)=0, \; j=1,2,\cdots,p
    \end{align*}$
    
    
    
    &#42; $x$ : design variable, $x = \{x_1, x_2, \cdots, x_n\}$
    
       n : # of design variable
    
       $g_i(x) \leq 0$ : inequality constraints
    
       $h_j(x) = 0$ : equality constraints
    
       m : # of inequality constraints
    
       p  : # of equality constraints
    
    
    
  
   Note that design optimization problems from different field of engineering can be transcribed into the standard form.
  
  - Minimization of $f(x)$                     $\Leftrightarrow$                 maximization of $F(x) = -f(x)$
  
    <img src="/images/2023-08-28-Optimum Design Intro/IMG_0339 2023-08-30 02_10_09.jpg" alt="IMG_0339 2023-08-30 02_10_09" style="zoom:50%;" />
  
  - Scaling of $f(x)$ : identical $x^*$
  
    $\begin{align*}
    \underset{x}{minimize} \quad f(x) \qquad & \Leftrightarrow \qquad af(x)\\ 
    & \Leftrightarrow \qquad [f(x) + c]
    \end{align*}$
  
  - $g_i(x) \leq 0 \quad \Leftrightarrow \quad G_i(x) \geq 0, \; when \; G_i(x) = - g_i(x) $ 
  
  - **p** should be less than or equal to **n**     i.e. $p \leq n$ 
  
    1.  $p < n$ : the optimal solution is possible
    2.  $p =n$ : no optimal solution is necessary
    3.  $p > n$ : no solution ( redundant constraints should be deleted)
    
     
  
  - $f(x), \; g_i(x), h_j(x)$
  
  
  
  





