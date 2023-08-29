---
layout: single
title:  "differential & gradient terminology description"
typora-root-url: ../
use_math: true
---

- 편미분

  multivariate calculus

  univariate calculus 에서는 독립변수 하나에 종속 변수가 하나인 함수에 대해서 다루었다.

  multivariate calculus에서는 독립변수가 여러개에 종속변수도 여러 개 일 수 있다.

  일단 독립 변수 (x,y)가 2개이고, 종속 변수(f)가 하나인 multivariate function을 보자.

  $f(x,y)=x^2+xy+y^2$

![Figure_1](/images/2023-08-29-differential & gradient/Figure_1.png)

함수에서 미분(derivative)의 개념은 기울기를 의미한다.

그런데 위 함수에서 지금까지 알고 있는 기울기를 구할 수 있는가? 임의의 점 하나에서 기울기 직선은 하나가 아니라, 무한대의 개수가 나올 수 있다.

편미분(partial derivative)이라는 개념이 필요한 이유는 이러한 상황에서 수직인 두 방향으로만 기울기를 구하고 싶다는 이유에서 출발한다고 할 수 있다.

$f(x,y)$의 $x$ 방향 만으로의 기울기와 y 방향 만으로의 기울기는 각각 구할 수 있기 떼문에, y 또는 x를 상수로 놓고 비분함으로써 x 방향 만으로의 기울기와 y 방향 만으로의 기울기를 구하는 것이다.

** 편미분의 개념

$f(x,y) = x^2+xy+y^2$

$\frac{\partial f}{\partial x} = 2x+y$,   $\frac{\partial f}{\partial y}= 2y + x$

$\frac{\partial f}{\partial x}$ : $x$는 변수, 나머지는 상수로 취급

<img src="/images/2023-08-29-differential & gradient/image-20230829105316931.png" alt="image-20230829105316931" style="zoom: 25%;" />

$\frac{\partial f}{\partial x}$ : (gradient의 x 성분) 을 나타낸 그래프

<img src="https://raw.githubusercontent.com/angeloyeo/angeloyeo.github.io/master/pics/2019-08-25_gradient/noname02.png" alt="img" style="zoom: 67%;" />

$\frac{\partial f}{\partial y}$ : (gradient의 y 성분) 을 나타낸 그래프

<img src="https://raw.githubusercontent.com/angeloyeo/angeloyeo.github.io/master/pics/2019-08-25_gradient/noname03.png" alt="img" style="zoom:67%;" />



- Gradient (기울기)

  gradient는 $x$ 방향으로의 편미분 값과 y 방향으로의 편미분 값을 원소로 하는 벡터를 출력한다.

  $gradient(f) = f_x \hat{i}+f_y \hat{j} = \frac{\partial}{\partial x}f(x,y) \hat{i} + \frac{\partial}{\partial y}f(x,y) \hat{j}$

#### Reference

공돌이의 수학정리노트 (Angelo's Math Notes) - 스칼라장의 기울기(gradient)

https://angeloyeo.github.io/2019/08/25/gradient.html

https://www.youtube.com/watch?v=bUNqn1G1O7E

(공돌이의 수학정리노트 (Angelo's Math Notes)를 베꼈습니다. )