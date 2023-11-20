---
layout: single
title:  "Polynomial interpolation method"
categories: Optimal_design_class
typora-root-url: ../
use_math: true
---

3. Polynomial interpolation method (Ch 11. 1)

   Instead of the golden section method, polynomial interpolation method can be used

   ![image-20231114205115102](/images/2023-11-06-Polynomial interpolation method/image-20231114205115102.png)

   (1) Approximate $f(x)$ in polynomial

   (2) Analytically determine min. pt

   $\rightarrow$ fast near min. pt.

   $\rightarrow$ Three points quadratic approximation is popular 

   $q(x) = a_0 + a_1 x + a_2 x^2$

   $(x_l, f(x_l)) \Rightarrow f(x_l) = a_0 + a_1 x_l +a_2 x_l^2 \cdots(1)$

   $(x_i, f(x_i)) \Rightarrow f(x_i) = a_0 + a_1 x_i + a_2 x_i^2 \cdots (2)$

   $(x_u, f(x_u)) \Rightarrow f(x_u) = a_0 + a_1x_u + a_2x_u^2 \cdots (3)$


   Solving (1), (2), (3)

   $a_2 = \frac{1}{x_u - x_i}\left[\frac{f(x_u) - f(x_l)}{x_u - x_l} - \frac{f(x_i)- f(x_l)}{x_i - x_l}\right] \rightarrow $ 여기에 들어가는 모든 f(x), x가 다 상수이므로 다 구할 수 있음


$a_1 = \frac{f(x_i) - f(x_l)}{x_i - x_l} - a_2(x_l -x_i)$

$a_0 = f(x_l) - a_1x_l - a_2x_l^2$

Minimum point $\bar{x}$ of the quadratic function $q(x)$

$\bar{x} = -\frac{a_1}{2a_2} ; \;\text{if}\quad \frac{d^2 q}{dx^2} = 2a_2 > 0$ : 아래로 볼록할 때

"Robust quadratic fit-sectioning algorithm" By brent(1973)

$\to$ Idea : use quadratic polynomial approximation whenever possible.
		Otherwise, use golden section method

- Steepest decent method (Ch 10.6)

  - Typical search method

    1) Look for the direction of the steepest descent.

    2) Find $\alpha$ to minimize $f(x_0 + \alpha d_0)$

       $\llcorner $ 1D min. prob.

    3. Update the search point $\vec x_{new} = \vec x_{old} +\alpha \vec d_0$
    4. Repeat 1. to 3. until convergence

  - Consider the update rule $\vec x^{k+1} = \vec x^k + \alpha \vec d^k (\alpha > 0)$

    To reduce the function value, $f(\vec x^{k+1}) < f(\vec x^k)$

    $\eqalign{f(\vec x^{k+1}) &= f(\vec x^k + \alpha \vec d^k)\\
    & = f(\vec x^k) + (\nabla f^T(\vec x^k) \cdot \vec d^k)\alpha + 0 (\alpha ^2)}$

    To satisfy $f(\vec x^{k+1} < f(\vec x^k), \nabla f^T(\vec x^k) \cdot \vec d^k < 0$

    <img src="/images/2023-11-06-Polynomial interpolation method/image-20231117183009114.png" alt="image-20231117183009114" style="zoom: 33%;" />

    $\nabla f$ : function increasing direction $\cdots$ (1)
    	 Orthogonal to the contour of f = const $\cdots (2)$   (i.e.    iso - cost line)

    from (1), (2), $\vec \nabla f$ is the direction of the fastest function increase $\to$ Steepest ascent direction

    $- \nabla f$ : steepest descent direction $(= \vec d^k)$

    $\vec d^k = - \nabla f(\vec x^k) \underset {\text{normaliz}e }{\Rightarrow } \frac{- \vec \nabla f(\vec x^k)}{||\vec \nabla f(\vec x^k)||}$

  - Convergence property for the steepest descent method
    (무조건 steepest descent method를 사용한다고 하면, 언제 해를 잘 찾을 수 있는가?)

    <img src="/images/2023-11-06-Polynomial interpolation method/image-20231117184624869.png" alt="image-20231117184624869" style="zoom:50%;" />

    1. Every search direction is orthogonal to the previous search direction

       $\vec d^{k+1} \bot \vec d^k \; ;  \; (\vec d^{k+1})^T \cdot \vec d^k = 0$ 

    2. What controls the convergence rate of the steepest descent method?

       e.g.) $f(x_1, x_2) = x_1^2 + a x_2^2 (a \geq 1)$

       <img src="/images/2023-11-06-Polynomial interpolation method/image-20231117185600544.png" alt="image-20231117185600544" style="zoom:50%;" />

        많이 찌그러져 있을수록 많은 iteration 필요

       $\to$ 얼마나 많이 찌그러졌는지 정량화

       Condition number of Hessian Matrix   $\underline{H} = \frac{|\lambda_{max}|}{|\lambda_{min}|}$

       $\lambda_{max}, \lambda_{min}$ : max and min values of eigenvalues of $\underline H$

       $\underline H = \begin{bmatrix} \frac{\partial^2 f}{\partial x_1^2} & \frac{\partial^2 f}{\partial x_1 \partial x_2} \\ \frac{\partial f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2^2} \end{bmatrix} = \begin{bmatrix} 2 & 0 \\ 0 & 2a\end{bmatrix}$

       Eigenvalue of $\underline H$

       $\underline H \vec z - \lambda \underline I \vec z = 0, \begin{bmatrix} 2-\lambda & 0 \\ 0 & 2a-\lambda \end{bmatrix}\begin{bmatrix}z_1 \\ z_2\end{bmatrix} = 0$
       
       $det(\underline{H} - \lambda \underline{I}) = (2-\lambda)(2a-\lambda) = 0$
       
       $\lambda  = 2, 2a$
       
       Condition number = $\frac{|\lambda_{max}|}{|\lambda_{min}|} = \frac{2a}{2} = a$
       
       1. a = 1 이면 condition number = 1 $\to $ best
       2. a =2 이면 $\underline{H} = 2$
       
       condition number는 최소 1.
       
       0.4, 0.5 이런거 될 수 없음
  
  