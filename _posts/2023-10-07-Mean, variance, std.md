---
layout: single
title:  "Mean, variance std"
categories: study
typora-root-url: ../
use_math: true
---

- 통계 기초 : 평균(mean), 분산(Variance), 표준편차(standard deviation)
  기초 개념
  Mean : 주어진 수의 합을 측정개수로 나눈 값, 대표값 중 하나
  Variance : 변량들이 퍼저있는 정도
  Standard deviation : 쉽게 팔하면 mean에 대한 오차 / 평균으로 부터 원래 데이터에 대한 오차범위의 근사값
  deviation : is a measure of difference between the observed value of a variable and some other value(mean)
  
  deviation은 관측값(observed value)에서 mean을 뺀 값, +도 될 수 있고, -도 될 수 있다.
  
  e.g. $m+1, m-2, m+3, m-4$ 
  평균값이 m 인, 4개의 데이터가 있다. 
  
  sum of deviations : $1+2+3+4 = 10$ 되어야 하지만, 실제값이 $-2, -4$ 가 있기 때문에, (observed value - mean)을 합한 값으로 계산해보면 $1-2+3-4 = -2$로 엉뚱한 값이 나온다.
  그래서 이 음수를 양수화해야하는데, 그러한 방법중의 하나가 제곱이다.
  
  편차들을 합하기전에 제곱을 합하면 $1+4+9+16$이 된다. 이것이 바로 Variance로 "편차의 제곱의 합"이다.
  
  그렇다면 Variance를 바로 쓰지 않고, Standard deviation을 구하는 이유는?
  
  분산은 편차에 제곱을 하여 계산을 하였기 때문에, 실제 값에서 너무 멀어져 있다. 그래서 실제 값으로 근접 시키기 위해서 제곱근(루트)를 씌워준다. 
  
  분산에 루트를 씌운 것이 Standarddeviation 이며, 평균으로 부터 원래 데이터에 대한 오차범위의 근사값이다.
  
  

- 모집단과 표본의 개념
  모집단(population) / 표본(sample)
  통계학이란 굳이 다 조사하지 않더라도, 대충의 결과를 알 수 있다.
  모집단(population) 전체르를 조사하는 경우를 전수조사라고 한다.
  population이 커서 전수조사가 어려운 경우, 집단의 특성을 추정하기 위해 일부 표본(sample)만 추출하여 하는 조사를 표본조사라고 한다.
  이렇게 sample을 조사함으로써, 원래 population의 특성을 추측하는 것을 추정이라고 한다.

- population 에 대한 mean,var,std / sample에 대한 mean, var, std

  |            | mean         | standard deviation | variance   |
  | :--------: | ------------ | ------------------ | ---------- |
  | population | $\mu$ or $m$ | $\sigma$           | $\sigma^2$ |
  |   sample   | $\bar {X}$   | $s$                | $s^2$      |

- 공식

  - $X = \{x_1, x_2, \cdots , x_n\}$
  - Mean
    $E(X) = \frac{\sum^n_{i=1}x_i}{n}$

  - deviation
    Obeserved value - Mean
  - Variation
    $\begin{align*} V(X) &= E[(X - \mu)^2]\\ &= \frac{\sum_{i=1}^n (x_i - \mu)^2}{n}\\ &= E(X^2) - \mu^2 \end{align*}$
  - Standard deviation
    $\sigma(X) = \sqrt{V(X)}$

#### Reference

통계의 기초인 평균, 분산, 표준편차
https://learnx.tistory.com/entry/%ED%86%B5%EA%B3%84%EC%9D%98-%EA%B8%B0%EC%B4%88%EC%9D%B8-%ED%8F%89%EA%B7%A0-%EB%B6%84%EC%82%B0-%ED%91%9C%EC%A4%80%ED%8E%B8%EC%B0%A8

평균,표준편차,분산의 개념
https://bcho.tistory.com/972

