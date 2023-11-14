---
layout: single
title:  "KKT example"
categories: Optimal_design_class
typora-root-url: ../
use_math: true
---

e.g.) minimize $f(\vec x) = x_1^2 + x_2^2 - 3x_1x_2$
	$s.t. g(\vec x) =  x_1^2 + x_2^2 -6 \leq 0$

Lagrange function $L = x_1^2 + x_2^2 -3x_1x_2 + u(x_1^2 + x_2^2 -6 + S^2)$

1. Stationarity
   $\frac{\partial L}{\partial x_1} = 2x_1 - 3x_2 + 2ux_1 = 0 \cdots (1)$

   $\frac{\partial L}{\partial x_2} = 2x_2 - 3x_1 + u(2x_2) = 0 \cdots (2)$

   $\frac{\partial L}{\partial u} = 0 \Rightarrow x_1^2 + x_2^2 -6 + S^2 = 0 \cdots (3)$

2. Switching condition

   $\frac{\partial L}{\partial S} = 2uS = 0 \cdots (4)$

3. Feasibility check

   $S^2 \geq 0$

4. Non-negativity
   $u \geq 0$

Case 1
$u = 0 $ ($g(x)$ is inactive)

From (1),(2) $x_1 = x_2 = 0$

From (3) $S^2 = 6 \geq 0$

$\therefore x_1^* = x_2^* = 0; \; u^* = 0, f(0,0) = 0$

Case 2

$ S^2 = 0 (u > 0, g(x) = 0 \rightarrow active)$

From (1), $u = -1 + \frac{3x_2}{2x_1} \cdots (5)$

From (2), $2x_2 -3x_1 + (-1 + \frac{3x_2}{2x_1})(2x_2) = 0$
$x_1^2 = x_2^2 $

From (5)

$x_1^2 + x_2^2 = 6 \rightarrow x_1^2 = x_2^2 = 3$



$x_1 = x_2 = \sqrt{3}; u = \frac{1}{2}$

$x_1 = x_2 = -\sqrt 3, u = \frac{1}{2}$

$x_1 = -x_2 = \sqrt 3; u = -\frac{5}{2} \ngeq 0 $ : violates non-negativity

$x_1 = -x_2 = -\sqrt 3; u = -\frac{5}{2} \ngeq 0 $ : violates non-negativity

$\therefore x_1^* = x_2^* = \sqrt3, u^* = \frac{1}{2}, f(x^*) = -3$

$x_1^* = x_2^* = -\sqrt 3, u^* = \frac{1}{2}, f(x^*) = -3$



Case 3

$u = 0, S = 0 $ ($g(x)$ is active)

From (3), $-6 \neq 0 \Leftarrow$ violates stationarity 



Frome the cases, candidate minimum points are

$x_1^* = x_2^* = 0, u^* = 0, f(x^*) = 0$
$x_1^* = x_2^* = \sqrt 3, u^* = \frac{1}{2}, f(x^*) = -3$
$x_1^* = x_2^* = \sqrt3, u^* = \frac{1}{2}, f(x^*) = -3$

- Physical meaning of L.M(Lagrange multiplier) s (ch 4.7)

  - Effect of changing constraint limits
    minimize $f(x)$
    s.t. $h_i(x) = b_i; \; g_j(x) = e_j$

    -> optimal solution $\begin{align*} x^* &= x^*(\vec b, \vec e)\\ f^* &= f^*(\vec b, \vec e) \end{align*}$

    -> constraint variation sensitivity theorem

    $x^*$ : regular point

    $v_i^*, u_j^*$ : L.Ms that satisfy both the KKT necessary and sufficient conditions

    $\frac{\partial f^*}{\partial b_i} = \frac{\partial f^*(x^*(0,0))}{\partial b_i} = -v_i^*, \quad i = 1,\cdots,p$

    

 

