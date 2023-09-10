---
layout: single
title:  "Optimum Design - Optimality condition"
typora-root-url: ../
use_math: true
---

# Optimality condition

- Necessary and sufficient conditions (ch 4.3)

  - Necessary condition	iif	a point a does not satisfy the necessary conditions, it cannot be an optimum.

  - Sufficent condition : If a candidate optimum point satisfies the sufficient condition, then it is indeed an optimum point.

    <img src="/images/2023-09-11-Optimum Design 0911/09111.png" alt="09111" style="zoom: 33%;" />

- Optimality condition for unconstrained problem (ch 4.4)

  - Unconstrained problem
    minimize f(x) subject to no constraint on x

  - Definition for local minima
    $f(x^*) \leq f(x)$ for all $x$ in the small neighborhood $N$ of $x^*$ in the feasible set.

    

  - Optimality conditions for functions of a single variable

    1. First order necessary condition : $f(x^*) = 0$
       $\begin{align*}f(x) &= f(x^* + d) \qquad \cdots\; d : small\; num\\
       &= f(x^*) + f'(x^*)d + \frac{1}{2}f''(x^*)d^2 + R\\
       &\approx f(x^*) + f'(x^*)d \geq f(x^*) \; \cdots\; (1)\end{align*}$


       To hold (1), $f'(x^*) = 0$

    2. Second order necessary condition : $f''(x) \geq 0$
       $\begin{align*} f(x) &= f(x^* + d)\\
       &= f(x^*) + f'(x^*)d + \frac{1}{2}f''(x^*)d^2 + R \rightarrow f'(x^*) = 0\\
       &\approx f(x^*) + \frac{1}{2}f''(x^*)d^2 \geq f(x^*)\; \cdots \; (2)\end{align*}$
       To hold (2), $f''(x^*) \geq 0$

       3. sufficient condition : $f''(x^*) > 0$
          <img src="/images/2023-09-11-Optimum Design 0911/09115.png" alt="09115" style="zoom:33%;" />
          $f(x) \approx f(x^*) + \frac{1}{2}f''(x^*)d^2 > f(x^*)$
          If $f(x)$ is a convex function
          Local minimum = Global minimum

          $\Rightarrow$ Durign actual numerical optimization, functions can be approximated as a convex function at every iteration step.

          e.g. $\begin{align*}f(x) &= x^2 - 4x + 4\end{align*}$

          (1) $f'(x) = 2x-4 =0 \rightarrow x^* + 2$
          (2) check $f''(x^*) > 0 \rightarrow f''(x^*)=2 > 0$
          From (1), (2) 	$x^* = 2 \Leftarrow $  strong local minimum

          - Optimality condition for functions of multiple variables
            1. Necessary condition : $\nabla f(x^*) = 0$
            2. Sufficient condition : $d^THd > 0 \Leftrightarrow f : P-D$ 

  

  - The matrix H is P-D at the stationary point $x^*$
    $x^* = \{x_1^*, x_2^*, \cdots, x_n^*\}^T$
    $d = \{d_1,d_2,\cdots,d_n\}^T$
    $H$ = [n x n]

    e.g. $f(x) = x_1^2 + 2x_1x_2 + 2x_2^2 -2x_1+x_2+8$
    (1) $\nabla f = \begin{Bmatrix}\frac{\partial f}{\partial x_1}\end{Bmatrix} =
    \begin{Bmatrix}2x_1 + 2x_2 -2\\
    2x_1 + 4x_2 -1\end{Bmatrix} = \begin{Bmatrix}0\\0\end{Bmatrix}$

    ​		$x^* = \begin{Bmatrix}x_1^*\\x_2^*\end{Bmatrix} = \begin{Bmatrix}2.5\\1.5\end{Bmatrix}$
    (2) Check $H(x^*)$ is P-D
    $H = \begin{Bmatrix}\frac{\partial^2 f}{\partial x_1^2} 
    & \frac{\partial^2 f}{\partial x_1 \partial x_2}\\
    \frac{\partial^2 f}{\partial x_2 \partial x_1} & \frac{\partial^2 f}{\partial x_2^2}\end{Bmatrix} = \begin{Bmatrix}2 & 2\\2 & 4\end{Bmatrix}$

    $Hx = \lambda x$

    $(\lambda I - H)x = 0$   -> characteristic equation
    $ = \left|\begin{bmatrix}\lambda -2 & -2\\
    -2&  \lambda - 4\end{bmatrix}\right| = (\lambda - 2)(\lambda -4) - 4$
    $= \lambda^2 -6\lambda +4 = 0$

    $\lambda= 3 \pm \sqrt{5} > 0 \qquad \therefore$  P-D
    From (1), (2) $x^* = \{2.5, -1.5\}^T \Leftarrow$ strong local minimum

