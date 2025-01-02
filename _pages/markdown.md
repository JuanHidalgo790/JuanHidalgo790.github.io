---
permalink: /markdown/
title: "Examples"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

Here, equations and modeling examples are intended to be here soon...

## Acoustic Waves 

An inviscid fluid under a pressure field \\(p(\mathbf{x},t)\\) has its motion governed by the Euler equation 

$$
\displaylines{
\rho \frac{Dv}{Dt}=-\nabla p
}
$$

where \\(\mathbf{v}(\mathbf{x},t)\\) is the fluid velocity field, \\(\rho(\mathbf{x},t)\\) is the density field, \\(\nabla p\\) is the gradient of the scalar function \\(p(\mathbf{x},t)\\), and \\(D\mathbf{v}/Dt\\) is the material derivative of \\(\mathbf{v}\\), defined as

$$
\displaylines{
\frac{D\mathbf{v}}{Dt} &= \frac{\partial \mathbf{v}}{\partial t}+(\mathbf{v}\cdot\nabla)\mathbf{v}.
}
$$

## Piezoelectric Effect

Piezoelectric materials have the characteristic of presenting an electrical polarization under deformation (**direct** piezoelectric effect), and deformation when subjected to an electric field (**inverse** piezoelectric effect).

![Image of the piezoelectric effect](/images/PiezoEffectJuan.png){: .align-center width="750px"}

The governing equations for piezoelectric materials are given by (stress-charge form):

$$
\displaylines{
\mathbf{D}&=\boldsymbol{\epsilon}^{\varepsilon}\boldsymbol{\cdot}\mathbf{E}+\mathbf{e}\boldsymbol{:}\boldsymbol{\varepsilon}, \label{eq:const_piez_D}\\
\boldsymbol{\sigma}&=-{\mathbf{e}}\boldsymbol{\cdot}\mathbf{E}+\mathbf{c}^{E}\boldsymbol{:}\boldsymbol{\varepsilon}
}
$$

where \\(\mathbf{D}\\) is the electric displacement vector, \\(\boldsymbol{\epsilon}\\) is the dielectric permittivity second order tensor, \\(\mathbf{E}\\) is the electric field vector, and \\(\mathbf{e}\\) represents the piezoelectric coupling third order tensor, with components being _piezoelectric stress constants_. The superscripts \\(\varepsilon\\) and \\(E\\) were added to the dielectric permittivity tensor  \\(\boldsymbol{\epsilon}\\) and to the elastic tensor \\(\mathbf{c}\\) to indicate that their components are measured under conditions of constant strain and constant electric field, respectively. 


## Cylindrical Waves 

An so we have the wave equation in cylindrical coordinates:

$$
\displaylines{
\frac{\partial^{2}u_{r}}{\partial r^{2}}+\frac{\partial}{\partial r}\left(\frac{1}{r}u_{r}\right)-\frac{1}{c_{\mathrm{L}}^{2}}\frac{\partial^{2}u_{r}}{\partial t^{2}}=0
}
$$


## References
