---
layout: single
title:  "Steepest descent method"
categories: Optimal_design_class
typora-root-url: ../
use_math: true
---

- Steepest descent method (continually)

  - Trick to improve convergence : Scaling

    <img src="/images/2023-11-08-steep descent method/image-20231120231130072.png" alt="image-20231120231130072" style="zoom: 50%;" />
    
    Scaling을 통해, 타원에서 원으로 바꿈. $-\nabla f$ 가 바로 min. 값으로 향함.
    
    $\eqalign{\begin{bmatrix}x_1 \\ x_2\end{bmatrix} = \begin{bmatrix}1 & 0\\ 0 & \frac{1}{\sqrt{a}}\end{bmatrix} \begin{bmatrix}y_1 \\ y_2\end{bmatrix} \triangleq T \begin{bmatrix}y_1 \\ y_2\end{bmatrix}}$
    
  - Numerical example of the steepest descent method
  
    $f(x_1, x_2) = (x_1 - 2)^4 - (x_1 - 2x_2)^2$
  
    $\eqalign{\vec x_0 = (0,3)^T, \; f(\vec x_0) = 52}$
  
    $\vec \nabla f = [4(x_1 -2)^3 + 2(x_1-2x_2), -4(x_1 - 2x_2)]^T$
  
    1. Direction of the steepest descent
  
       $\vec d_0 = -\vec \nabla f(\vec x_0) = (44, -24)^T \underset{\text{normalize}}{=} (0.8779, -0.4789)^T$
  
    2. $\alpha$ to minimize $f(\vec x_0 + \alpha \vec d_0); \;$1D line search
  
       $\alpha = 3.0841$
  
    3. Update the search point
    
       $\vec x_1 = \vec x_0 + \alpha \vec d_0 = (2.707, 1.523)^T$
    
       <img src="/images/2023-11-08-steep descent method/image-20231120233428624.png" alt="image-20231120233428624" style="zoom: 33%;" />
    