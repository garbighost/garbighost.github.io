---
layout: single
title:  "2nd order cartesian tensor"
categories: study
typora-root-url: ../
use_math: true
---

- Tensors

  - concept of tensor
    한 작은 직육면체(점?)에 가해지는(또는 버티는) 응력의 표현

    ![image-20231016233554429](/images/2023-10-16-2nd order cartesian tensor/image-20231016233554429.png)\
    
    $\sigma = \begin{bmatrix} \sigma_{xx} & \sigma_{yx} & \sigma_{zx}\\ \sigma_{xy} & \sigma_{yy} & \sigma_{zy} \\ \sigma_{xz} & \sigma_{yz} & \sigma_{zz}\end{bmatrix}$ : stress tensor
    
    이렇게 표현이 가능하다.
    이 matrix를 tensor라고 부르기로 약속하였다.
    rank 0 tensor: scalar
    
    $\begin{bmatrix} P \end{bmatrix}$ 
    
    
    
    rank 1 tensor : vector
    
    $\begin{bmatrix} P_x & P_y & P_z \end{bmatrix}$
    
    rank 2 tensor : tensor (basis vector가 2개)
    
    $\begin{bmatrix} \sigma_{xx} & \sigma_{yx} & \sigma_{zx}\\ \sigma_{xy} & \sigma_{yy} & \sigma_{zy} \\ \sigma_{xz} & \sigma_{yz} & \sigma_{zz}\end{bmatrix}$
    
    

  - Tensor product (dyad) of two vectors $(\vec{A} = A_i \hat{e}_i, \vec{B} = B_j \hat{e}_j)$
    $\vec{S} = \vec{A} \vec{B} = \vec{A} \otimes \vec{B} = A_i B_j \hat{e}_i \hat{e}_j = S_{ij} \hat{e}_i \hat{e}_j$

    <img src="/images/2023-10-16-2nd order cartesian tensor/image-20231016224715691.png" alt="image-20231016224715691" style="zoom:50%;" />

    

  - Dyad : two vectors standing side by side (2nd order tensor)
    dyadic product of $\vec{a}$ and $\vec{b}$
    $\vec{a} = \begin{bmatrix} a_1 \\ a_2 \\ a_3\end{bmatrix}$, $\vec{b} = \begin{bmatrix}b_1 \\ b_2\\ b_3\end{bmatrix}$
    Dyadic product $\vec{a} \otimes \vec{b} = \vec{a} = \begin{bmatrix} a_1 \\ a_2 \\ a_3\end{bmatrix} \begin{bmatrix}b_1 & b_2 & b_3\end{bmatrix} = \begin{bmatrix}a_1b_1 & a_1b_2 & a_1b_3\\ a_2b_1 & a_2b_2 & a_2b_3\\ a_3b_1 & a_3b_2 & a_3b_3\end{bmatrix}$
    $\begin{bmatrix}a_1b_1 & a_1b_2 & a_1b_3\\ a_2b_1 & a_2b_2 & a_2b_3\\ a_3b_1 & a_3b_2 & a_3b_3\end{bmatrix}$ : Dyad 
    Dyad is quantity with two directions such as stress / strain

  - Tensor rank(order) : indicated by the number of free(unrepeatied index) 3rd order tensor $\hat{e}_i\; \hat{e}_j\; \hat{e}_k$
    In contiuum mechanics, 1st, 2nd, and 4th order tensors appear.
    $\sigma = C\epsilon$ 
    $\sigma$ : 2nd order tensor
    $C$ : 4th order tensor
    $\epsilon$ : 2nd order tensor

  - Unit dyad or unit second order tensor
    $\vec{I} = \delta_{ij}\hat{e}_i\hat{e}_j = \hat{e}_i \hat{e}_i = \hat{e}_1\hat{e}_1+ \hat{e}_2\hat{e}_2 + \hat{e}_3\hat{e}_3$
    $= \begin{bmatrix}\hat{e}_1 \\ \hat{e}_2 \\ \hat{e}_3\end{bmatrix}^T \begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0\\ 0 & 0 & 1\end{bmatrix} \begin{bmatrix}\hat{e}_1 \\ \hat{e}_2 \\ \hat{e}_3\end{bmatrix}$

    $\begin{bmatrix}I\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0\\ 0 & 0 & 1\end{bmatrix}$

  - Vector - dyad product
    ($A,B,C,D : vector, S, T$ : 2nd order tensor)
    $\vec{A} \cdot (\vec{B}\vec{C})$

- Transformation of a 2nd-order cartesian tensor **S**
  $\vec{S} = S_{ij} \hat{e}_i \hat{e}_j = \bar{S}_{mn} \hat{\bar{e}}_m \hat{\bar{e}}_n$
  $(\hat{e}_j = l_{ij} \hat)$

#### Reference

이것이 텐서다!: Tensor!, 텐서 이해 (1) : 사례를 통해 개념 정립 : 텐서의 개념을 자연스럽게 흡수하기
https://www.youtube.com/watch?v=8bVIzSaJRXs