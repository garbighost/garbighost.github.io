---
layout: single
title:  "Make plan"
categories: Research
typora-root-url: ../ 
---

3차원 평면 만들고, 2개의 3차원 평면을 특정 높이에서 사이각 구하기

1. 평면 정의
   3지점을 통과하는 평면은 벡터의 외적을 사용하여 정의할 수 있다. 두 벡터 $\vec u$ 와 $\vec v$를 이용해 평면의 법선 벡터 $\vec n$을 구할 수 있다. 
   예를 들어, 무릎과 종아리을 잇는 벡터(FE - TTC) : $\vec u$, 종아리와 발목을 잇는 벡터(TTC - ANKLE) : $\vec v$ 로 정의하면 $\vec n = \vec u \times \vec v$가 된다. 

2. 벡터 계산
   다리의 3점 FE(무릎) , TTC(종아리), ANKLE(발목) 3점이 주어지면, $\vec u = TTC - FE, \vec v = ANKLE - TTC$
   $\vec n = \vec u \times \vec v =  (TTC - FE) \times (ANKLE - TTC)$

3. 각도 계산 
   두 평면의 법석 벡터 $\vec n_1 과 \vec n_2$가 계산 되면, 두 벡터 사이의 각도$\theta$는 아래의 공식을 사용해 계산할 수 있다.

   $\cos(\theta) = \frac{\vec n_1 \cdot \vec n_2}{|\vec n_1||\vec n_2|}$

