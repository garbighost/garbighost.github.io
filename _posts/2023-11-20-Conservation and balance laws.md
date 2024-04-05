---
layout: single
title:  "Conservation and balance laws"
categories: Advanced_Solid_mechanics
typora-root-url: ../
use_math: true
---

ch5. conservation and balance laws

5.1 Introduction

- Every phenomenon in nature can be described in terms of mathmatical relations among certain physical quantities $\to$ (density, velocity, displacement, stress, strain, temperature)
- Study of fundamental laws of physics and resulting mathematical models for mechanical systems
- principles of mechanics
  1. conservation of mass (continuity equation) ch 5.2
  2. Balance of linear momentum ch 5.3
  3. Balance of angular momentum ch 5.3
  4. Balance of Energy ch 5.3

5.2 Conservation of mass

- Mathematical forms of conservation of mass differ in spatial & material description.

- Material time derivative $\frac{D}{Dt}$(time derivative with the material coordinates)

  - Material description function

    $\phi = \phi(\vec X, t)$   $\vec X$ hold constant w.r.t time.

    $\Rightarrow$ $\frac{D\phi}{Dt} = \left(\frac{\partial \phi}{\partial t}\right)_{X = constant}$

    When $\phi = \vec x(\vec X, t)$	$\eqalign{\frac{D\vec x}{Dt} &= \left(\frac{\partial \vec x}{\partial t}\right)_{X=const} = \vec v(\vec X , t)\\
    \frac{D\vec v}{Dt} &= \left(\frac{\partial \vec v}{\partial t}\right)_{v = const} = \vec a(\vec X, t)}$

  - Spatial description function

    $\phi = \phi(\vec x, t) = \phi(\vec x(\vec X, t), t)$

    $\Rightarrow \frac{D \phi}{D t} = \left(\frac{\partial \phi}{\partial t}\right)_{x = const} + \left(\frac{\partial x_i}{\partial t}\right)_{X=const}\left(\frac{\partial \phi}{\partial x_i}\right) = \left(\frac{\partial \phi}{\partial t}\right)_{x=const} + \vec v \cdot \nabla \phi$

    

    Example 5.2.1)

    A motion is described by $x = (1+t)X \quad (t \geq 0)$

    (a) Determine velocity and acceleration in spatial and material description

    - Velocity

      material	$\vec v = \frac{D\vec x(\vec X, t)}{Dt} = X$

      spatial 	  $\vec v = v(x,t) = X(x,t) = \frac{x}{1+t}$

    - Acceleration

      material	$a = \frac{Dv(X,t)}{Dt} = 0$

      spatial       $\quad \eqalign{a &= \frac{\partial v(x, t)}{\partial t} + \vec v(x,t) \cdot \nabla v(x,t)\\
      & = -\frac{x}{(1+t)^2} + \frac{x}{1+t} \cdot \frac{1}{1+t} = 0}$

    (b) determine time dertivative of a function $\phi(X, t) = Xt^2$ in spatial and material description

    - Matertial	$\frac{D\phi(X,t)}{Dt} = \frac{\partial (Xt^2)}{\partial t} = 2Xt$

    - Spatial            $\frac{D\phi(x,t)}{Dt} = \frac{\partial \phi(x,t)}{\partial t} + \vec v(x,t)\frac{\partial \phi (x,t)}{\partial x}$ 	*$\phi (x,t) = \left(\frac{x}{1+t}\right)t^2$

      ​				      $= \frac{2tx}{1+t} - \frac{xt^2}{(1+t)^2 } + \frac{x}{1+t} \cdot \frac{t^2}{1+t} = \frac{2tx}{1+t}$

  - Continuity equation in spatial description

    - Reynolds transport theorem

    $\frac{D}{Dt}\int {\phi(\vec x , t)dx= \int_\Omega {\frac{\partial \phi}{\partial t}d\vec x} + \oint_\Gamma \phi \hat{\underset{\tilde{}}{n}} \cdot \vec v ds}$

    

    

    

    

    

    

    

    