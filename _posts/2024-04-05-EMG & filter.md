---
layout: single
title:  "EMG & filter"
categories: Research
typora-root-url: ../
---

240405 JC 복습 - EMG & filter

EMG

- EMG 사용시 노이즈는 반드시 발생한다.
  - EMG 사용시 노이즈 종류
    - 살 떨림에 의한 EMG 신호의 진동 노이즈
    - 공기 중 교류 전류 노이즈 (60Hz) ???
    - EMG와 피부간 접촉 면적 실시간 변화 , 접촉이 떨어지는 시간 발생으로 인한 노이즈
  - EMG 노이즈 filtering
    - Low pass filter : 400~450 Hz 컷 오프 추천
    - Hihg pass fitler : 5~30 Hz 컷 오프 추천
      : 보통 5~30 hz에서 artefact noize (살 떨림 등) 발생
- Isometric / esentric? / consentric?
  공부하자~~~



filter

- adaptive filter : 240405 JC 24년 논문에 설명
- combo filter
- butter filter

