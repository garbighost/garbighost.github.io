---
layout: single
title:  "KKT example"
categories: Optimal design class
typora-root-url: ../
use_math: true
---

e.g.) minimize $f(\vec x) = x_1^2 + x_2^2 - 3x_1x_2$
	$s.t. g(\vec x) =  x_1^2 + x_2^2 -6 \leq 0$

Lagrange function $L = x_1^2 + x_2^2 -3x_1x_2 + u(x_1^2 + x_2^2 -6 + S^2)$

1. Stationarity
   $\frac{\partial L}{\partial x_1} = 2x_1 - 3x_2 + 2ux_1$