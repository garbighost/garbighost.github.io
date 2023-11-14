---
layout: single
title:  "Optimum Design Intro"
categories: Optimal_design_class
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
  
     
  
  - $f(x), \; g_i(x), h_j(x)$ are linear
  
    $\rightarrow$ Linear programming (LP)
  
  - Any of $f(x), g_i(x), h_j(x)$ is nonlinear
  
    $\rightarrow$ Nonlinear programming problem (NLP)
  
    &#42; programming 번역 뜻 : 계획법, (코딩 x)
  
  
  
  - Feasible Set
  
    $S = (x | h_j(x)=0, \; g_i(x) \leq 0)$
  
  

Ch 3. Graphical Solution Method

-  eg. profit maximization problem

  1.  A company manufactures 2 machines A and B

  2. 28A or 14B can be manufactured daily

  3. 14A or 24B can be sold daily

  4. 16 machines can be handled daily

  5. \$400 profit / A , \$600 profit / B

     

  - How many A and B machines should be the company manufacture everyday 

    to maximize its profit?

  

  - Mathematical formulation (this is not 'standard design optimization model')


    manufacturing constraint : $\frac{A}{28} + \frac{B}{14} \leq 1$
    
    sales constraint : $\frac{A}{14} + \frac{B}{24} \leq 1$
    
    shipping and handling constraint : $A+B\leq16$
    
    non-negative constraint : $A \geq 0,\; B\geq 0$


    profit P = $400 A + 600 B$
    
    <img src="/images/2023-08-28-Optimum Design Intro/abc.png" alt="abc" style="zoom: 33%;" />

  - Standard design optimization model

    $\underset{x}{minimize} \quad f(x)$   subject to   $g_i(x) \leq 0, \; i = 1,2, \cdots, 5$

    design variable :    $x = {x_1, x_2}$

    objective function :    $f(x) = -p = -400x_1 -600x_2$

    inequality constraints :

    - $g_1(x) = \frac{x_1}{28} + \frac{x_2}{14} - 1\leq 0$
    - $g_2(x) = \frac{x_1}{14} + \frac{x_2}{28} - 1 \leq 0$
    - $g_3(x) = x_1 + x_2 -16 \leq 0$
    - $g_4(x) = -x_1 \leq 0$
    - $g_5(x) = -x_2 \leq 0$

<img src="/images/2023-08-28-Optimum Design Intro/2.png" alt="2" style="zoom:33%;" />



<img src="/images/2023-08-28-Optimum Design Intro/3.png" alt="3" style="zoom: 33%;" />
