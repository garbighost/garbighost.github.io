---
layout: single
title:  "Linear Time Invariant System"
categories: study
typora-root-url: ../
---

# Linear Time Invariant System

- Time Invariant (시불변성)

시간이 바뀌면서 시스템이 바뀌어 버리면, 시스템이 복잡해진다. 매시간 포인트마다 다른 시스템을 생각해야 하기 때문이다.

입력이 $n_0$만큼 지연되었을 때, 출력도 같은 정도로 지연된다면 시불변 시스템이라고 할 수 있다.

$x[n-n_0] -> y[n-n_0]$

시스템의 시불변성을 체크해보기 위해서는 입력 신호에 delay를 먼저 걸고 system을 통과시켜 본 결과와, 입력 신호를 시스템에 통과 시킨 후 delay를 걸어줘서 얻은 결과를 비교해보면 된다.

![image-20240627131709109](/images/image-20240627131709109.png)

아래와 같은 시스템이 있다.

$y[n] = (x[n])^2$

이 시스템이 시불변 시스템인지 확인해보자

$w[n] = (x[n-n_0])^2$

$y[n-n_0] = (x[n-n_0])^2$

$w[n] = y[n-n_0]$







#### Reference

선형 시불변(LTI) 시스템 - 공돌이의 수학정리노트(Angelo's Math Notes)
https://angeloyeo.github.io/2022/01/11/LTI_system.html