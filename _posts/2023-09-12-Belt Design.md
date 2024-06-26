---
layout: single
title:  "Belt Design"
categories: study
typora-root-url: ../
use_math: true
---

- 벨트의 설계
  - 설계 동력
    설계동력 $H_d$는 전달해야 할 부하동력(전달동력) $H_r$ 보다 크게 정하며, 기계의 운전상태에 따라 다음과 같은 인자를 고려하여 설계한다. 
    $H_d = (K_m + K_i+K_r) \times H_r$
    $H_r$ : 부하동력(전달동력) [kW]
    $K_m$ : 부하보정계수
    $K_i$ : 캐리어 롤러 보정계수
    $K_r$ : 각속도비 보정계수
    - 벨트전동의 특징
      	평행걸기의 경우, 구동풀리로 들어가는 쪽 벨트는 긴장측(tight side)으로서 아래쪽에 위치하고, 구동풀리로부터 나오는 쪽 벨트는 이완측(loose side)으로서 위쪽에 위치한다. 이는 장력차로 인한 접촉각 감소를 방지하기 위한 것이다.
      	풀리에 감긴 벨트부분 중 긴장측에 가까운 부분에서는 많이 신장되고 이완측에 가까운 곳에서는 적게 신장된다. 즉 벨트가 풀리를 따라 회전하는 동안 벨트에 작용하는 인장력이 달라져 변형량도 변화하게 된다. 이완측에 가까운 부분에서 인장력의 감소로 변형량이 줄어들므로



- 토크 테스트기 설계
  - 설계 동력 계산
    $\begin{align*}H_d &= (K_m + K_i+K_r) \times H_r\\
    &= (1.6 + 0.1 + 0.4) \times H_r \\
    & = 2.1\end{align*}$
    &#42; $K_i : 0.1,\; K_m : 1.6,\; K_r : 0.4$

#### Reference

홍장표, 기계설계 이론과 실제, 기계요소편 2
