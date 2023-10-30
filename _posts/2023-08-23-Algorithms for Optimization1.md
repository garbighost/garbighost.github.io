---
layout: single
title:  "Algorithms for Optimization 1"
categories: study
typora-root-url: ../
use_math: true

---

# Optimization

- Optimization Process

  ![image-20230823152714230](/images/2023-08-23-Algorithms for Optimization1/image-20230823152714230.png)

- Basic Optimization Problem

  $minimize \quad f(x)$

  $\qquad x$

  $subject\, to\; x \in X$

  

  * $X$ : feasible set  --- feasible : 그럴듯한

  <img src="/images/2023-08-23-Algorithms for Optimization1/image-20230825084326098.png" alt="image-20230825084326098" style="zoom: 33%;" />

  $\underset{x_1,x_2}{minimize} \quad f(x_1, x_2)$

  $\begin{align*} subject\; to \quad &x_1 \geq 0\newline &x_2 \geq 0\newline & x_1 + x_2 \leq 1 \end{align*}$

  

  $f(x_1, x_2) \Rightarrow a_1x_1 + a_2x_2$ 라면, 위 Optimization Problem은 Linear Programing 이다.

  Linear Programing(LP) 이면,

  <img src="/images/2023-08-23-Algorithms for Optimization1/image-20230825090936829.png" alt="image-20230825090936829" style="zoom:33%;" /> 

  

  feasible Set의 꼭지점 - 빨간 3점을 확인하면, Solution을 찾을 수 있다.

  Polytope : 꼭지점에서 solution이 나오는 경우?

  Linear Programing에서는 최적화가 되려면, 극점으로 가야한다.(한 쪽으로 쭉 밀어야한다.) -> 꼭지점 찾으면, 답이 나온다.

  

- Critical Points

  : local 에서 미분 값이 0 (기울기가 0) 이면서, 아래 볼록($f''(x) > 0$) 인 점들 + inflection 

  <img src="/images/2023-08-23-Algorithms for Optimization1/image-20230825092251801.png" alt="image-20230825092251801" style="zoom: 33%;" />

- Conditions of local minima (Univariate : 변수 1 개)

  - Strong local minima
    1. $f(x^*) = 0$
    2. $f''(x^*) > 0$

  - Conditions of local minima
  
    1. $f'(x^*) = 0$, the first-order necessary condition (FONC)
  
    2. $f''(x^*) \geq 0$, the second-order necessary condition (SONC)
  
       -- $f''(x^*) > 0$ 는 the second-order sufficient condition (SOSC) 라고 부른다.



- Conditions of local minima (Multivariate : 변수 여러개)
  1. $\nabla f(x) = 0$, the first-order necessary condition (FONC)
  
  2. $\nabla^2 f(x)$ is positive semidefinite (SONC)
  
     -- $\nabla^2 f(x)$ is positive definite, the second-order sufficient condition (SOSC)
