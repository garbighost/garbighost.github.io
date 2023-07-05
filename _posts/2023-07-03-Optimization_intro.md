---
layout: single
title:  "Optimization Intro"
typora-root-url: ../
use_math: true
---

# Terminology Description

- The $l_p$ and $L_p$ Space

  $l_p$ : 수열 공간(sequence space)

  ​	ex) $l_2 = \sqrt{a^2 + b^2+c^2+\cdots}$ 

  $L_p$ : 함수공간

  ​	ex) $L_2$ 성질을 같는 함수 집합 $\Rightarrow \int_{I}{f^2(t)dt}$

  

- Functionals

  Functional : function of function

  ex) functions $\rightarrow$ real :     norm, cost function
  
  
  
- 유리수와 무리수

  셀 수 잇다의 정의 (countable) :

  자연수랑 1:1 매핑이 된다.

  
  
  $유리수 = \frac{자연수}{자연수}$ : 2차원의 자연수
  
  <img src="/images/2023-07-03-Optimization_intro/image-20230703120708441.png" alt="image-20230703120708441" style="zoom:50%;" />
  
  
  
  $f(t) = \begin{cases} 0\quad t \in Q\newline 1\quad t \notin Q \end{cases}$
  
  
  
  $Q$ : 유리수
  
  $t \in Q$ : countable (countably many)
  
  $t \notin Q$ : uncountable
  
  
  
  범위가 [0,1] 이라고 할 때, $\int_I{f(t)}dt$ 를 계산해보자.
  
  $f(t)$ 는 이렇게 표시된다.
  
  <img src="/images/2023-07-03-Optimization_intro/image-20230705125025286.png" alt="image-20230705125025286" style="zoom: 50%;" />
  
  우리가 보통 사용하는 적분법은 Riemann(리만) integration 으로 
  
  <img src="/images/2023-07-03-Optimization_intro/image-20230705125324187.png" alt="image-20230705125324187" style="zoom:50%;" />
  
  현재 $f(t)$에서는 dt를 정의할 수 없다.(한 점마다 넓이를 구해야하는데, 한 점에 대한 dt를 정의할 수 없다.)
  
  
  
  다른 방법으로 Lebesgue(르벡) integration이 있다.
  
  <img src="/images/2023-07-03-Optimization_intro/image-20230705125640856.png" alt="image-20230705125640856" style="zoom:50%;" />
  
  
  
  Lebesgue(르벡) integration 은 가로 줄의 넓이를 구하는 것이라 할 수 있다.
  
  lebsegue integration을 사용하면, $\int_I{f(t)}$를 계산할 수 있다.
  
  <img src="/images/2023-07-03-Optimization_intro/image-20230705125025286.png" alt="image-20230705125025286" style="zoom: 50%;" />
  
  <img src="/images/2023-07-03-Optimization_intro/image-20230705130855554.png" alt="image-20230705130855554" style="zoom:50%;" />
  
  가로 줄을 넓이를 구하려고 할때, $\Delta$ 를 그래프 전체 덩어리로 잡으면, $\Delta = 1$이다.
  
  $\Delta \times$길이 = 넓이 가 된다.
  
  길이 =size of $I$= $1 \times$ size of $Q^c + 0 \times$size of $Q$  
  
  $m(I)$ : measure of $I$
  
  $m(I) = 1 = m(Q) + m(Q^c)$ 
  
  $\Delta \times m(I) = 1$ 이므로, 
  
  $\int_I{f(t)} = 1$
  
  
  
  유리수 구간만의 적분과 무리수 구간만의 적분이 궁금하니, 계산해보자.
  
  $m(Q)$를 계산 하기 위해 첫번째, 두번째, n번째 유리수를 생각해보자.
  
  
  
  첫번째 유리수 : $q_1$
  두번째 유리수 : $q_2$
  
  ​            $\vdots$
  
  n 번째 유리수 : $q_n$
  
  
  
  $q$들 사이사이에 무리수들이 있으므로, 공간을 조금씩 띄어 놓으면
  
  <img src="/images/2023-07-03-Optimization_intro/image-20230705131955875.png" alt="image-20230705131955875" style="zoom:50%;" />

$\epsilon$ : arbitrary positive = 임의의 길이

$m(Q) < \epsilon \cdot \sum_{n+1}^{\infty}{(\frac{1}{2^{n-1}})} = 2\epsilon$ (아무리 $\epsilon$을 작게 선택하여도, 점(유리수)는 커버한다.)

$m(Q)=0$ ($\epsilon$은 arbitrary positive 이므로 $2\epsilon$ 보다 작으려면 0 이어야 한다.)

$m(I) = 1 = m(Q) + m(Q^c) = 0 + m(Q^c)$

$m(Q^c) = 1$

유리수 구간만의 적분 : $\Delta \times m(Q) = 0$

무리수 구간만의 적분 : $\Delta \times m(Q^c) = 1$



#### Sets

- disjoint : Two sets are disjoint if their intersection is empty

- $S\in T$ : 뜻 - **E**lement in

- $S \subset T$ : 뜻 - **C**ontained



- The least upper bound or supremum ($sup\{x:x \in S\}$) 

<img src="/images/2023-07-03-Optimization_intro/image-20230705135537753.png" alt="image-20230705135537753" style="zoom:50%;" />



- The greatest lower bound or infimum ($inf\{x:x\in S\}$) $\fallingdotseq$ supremum



#### Matrices and Vectors

- column vector $x = \begin{bmatrix} x_1\\ x_2\\ \vdots\\ x_n \end{bmatrix}$ = row vectors $x = \begin{bmatrix}x_1 & x_2 & \cdots & x_n\end{bmatrix}$.

But, in matrix multiplication, column vectors are used for convenience.
