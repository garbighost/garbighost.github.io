---
layout: single
title:  "Solid mechanics Intro"
categories: study
typora-root-url: ../
use_math: true
---

# Advanced Solid mechanics Design Intro

- The flow of the lecture

  Rigid Body       $\Rightarrow$                    Deformable Body                            $\Rightarrow$                Fluids

  (Statics,  Dynamics)             (Solid mechanics, Vibration)                           (fluid mechanics)

  

  Long, Straight, slender   structual member (ex. Truss, Frame, beam, cable) $\rightarrow$ (solid machanics)

  Arbitrary-shaped body $\rightarrow$ (continuum mechanics)



- Part 1 (Textbook 1) : Ch 1. Review of elementary solid mechanics
  - Mechanics : Behaviour of physical bodies subjected to forces

<img src="/images/2023-08-28-Solid mechanics Intro/image-20230828154138938.png" alt="image-20230828154138938" style="zoom:33%;" />

  - Stress : Enable to determine loading condition under which material failure occurs (related to strength)

    - nominal stress & true stress

      $\bar \sigma \equiv \frac{P}{A_0}$ : nominal stress

      $A_0 = \frac{\pi d^2_0}{4}$ : initial area

      
      
      $\sigma \equiv \frac{P}{A}$ : true stress
      
      $A = \frac{\pi d^2}{4}$ : deformed area
      
      
      
      nominal stress 는 변형 전의 단면적을 이용해 계산한 응력.
      
      실제로는 힘이 가해지면, 길이가 늘어나면서  단면적이 조금 줄어들므로, 실제 응력돠 차이가 있다.
      그러나 변형이 아주 작다면, 단면적이 비슷하기 때문에, nominal stress $\fallingdotseq$ true stress
      
      true stress는 변형 후의 단면적을 이용해 계산한 응력이다. 


  - Deformation : Affect kinematics function of a structure (related to stiffness)

    $\Rightarrow$ Guideline for design process of physical devices such as cars, airplanes, and electronics.
    
    
    
    Solid mechanics 에서는 Stress와 Deformation이 관찰하고자하는 주요 특성(?)이다.

- Strain

  - nominal strain & true strain

    $\epsilon = \frac{L-L_0}{L_0} = \frac{\delta}{L_0}$ : nominal strain

    $\delta = L-L_0$ : elongation

    $L_0$ : initial length

    $\bar \epsilon = \frac{L-L_0}{L} = \frac{\delta}{L}$ : true strain

    $\delta = L-L_0$ : elongation

    $L$ : deformed length
  
  -  nominal strain 과 true stain의 관계
  
    미소진변형률 (derivative true strain) : $d\bar{e} = \frac{dL}{L}$
  
    이 derivative true strain($d\bar{e}$)을 길이가 변화한 전체 구간에 대해 적분해보자.
  
    $\begin{align*}
    \bar{\epsilon} &= \int^L_{L_0}{\frac{dL}{L}}\\
    &=[\ln{L}]^L_{L_0}\\
    &= \ln{\frac{L}{L_0}}\\
    &= \ln{\frac{L_0 + \delta}{L_0}}\\
    & = \ln{\left(1 + \frac{\delta}{L_0}\right)}\\
    & = \ln{(1+\epsilon)}\end{align*}$
  
  - $\bar{\epsilon} = \ln(1 + \epsilon)$
  
    

#### Reference

응력-변형률 선도 (Stress-Strain Diagram)  - 영구노트

https://satlab.tistory.com/127