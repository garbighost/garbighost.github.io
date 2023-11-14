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

   $a_2 = \frac{1}{x_u - x_i}\left[\frac{f(x_u) - f(x_l)}{x_u - x_l} - \frac{f(x_i)- f(x_l)}{x_i - x_l}\right] \rightarrow $ 여기에 들어가는 모든 f(x)가 다 상수이므로 다 구할 수 있음