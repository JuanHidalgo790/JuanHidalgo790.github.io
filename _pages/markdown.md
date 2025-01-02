---
permalink: /markdown/
title: "Examples"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

Here, the idea is to show equations and modeling examples 

## Acoustic Waves in Fluids

An inviscid fluid under a pressure field \\(p(\mathbf{x},t)\\) has its motion governed by the Euler equation 

$$
\displaylines{
\rho \frac{D\mathbf{v}}{Dt}=-\nabla p,
}
$$

where \\(\mathbf{v}(\mathbf{x},t)\\) is the fluid velocity field, \\(\rho(\mathbf{x},t)\\) is the density field, \\(\nabla p\\) is the gradient of the scalar function \\(p(\mathbf{x},t)\\), and \\(D\mathbf{v}/Dt\\) is the material derivative of \\(\mathbf{v}\\), defined as

$$
\displaylines{
\frac{D\mathbf{v}}{Dt} &= \frac{\partial \mathbf{v}}{\partial t}+(\mathbf{v}\cdot\nabla)\mathbf{v}.
}
$$

The second governing equation is the mass conservation, or continuity equation, given by

$$
\displaylines{
\frac{\partial \rho}{\partial t}=-\nabla \cdot (\rho \mathbf{v}),
}
$$

where the operation \\(\nabla \cdot[ \phantom{ii} ]\\) indicates divergence of the argument vector.

Considering small oscillations in the fluid

$$
\displaylines{
\frac{D\mathbf{v}}{Dt} \approx \frac{d\mathbf{v}}{dt}.
}
$$

On the other hand, the pressure and the density can be assumed as

$$
\displaylines{
&p(\mathbf{x},t)=p_{0}+\bar{p}(\mathbf{x},t),\\
&\rho(\mathbf{x},t)=\rho_{0}+\bar{\rho}(\mathbf{x},t),
}
$$

in which \\(p_{0}\\) and \\(\rho_{0}\\) are, respectively, the ambient pressure and density of the fluid when static, and \\(\bar{p}(\mathbf{x},t)\\) and \\(\bar{\rho}(\mathbf{x},t)\\) are their small variations, due to small oscillations. 

Performing the appropriate substitutions, dropping all higher order terms, one can find the following linearized governing equations for the fluid motion

$$
\displaylines{
&\rho_{0}\frac{d\mathbf{v}}{dt}=-\nabla\bar{p},\\
&\frac{d\bar{\rho}}{dt}=-\rho_{0}\nabla \cdot \mathbf{v}.
}
$$

Assuming a general relation between pressure and density, one can write

$$
\displaylines{
p_{0}+\bar{p}\approx p(\rho_{0})+\frac{dp}{d\rho}\bigg|_{\rho_{0}} \bar{\rho},
}
$$

resulting in 

$$
\displaylines{
\bar{p}=\frac{dp}{d\rho}\bigg|_{\rho=\rho_{0}}\bar{\rho}=c_{f}^{2}\bar{\rho},
}
$$

where \\(c_{f}\\) is the acoustic wave speed in the fluid. 

Performing appropriate substitutions, and differentiating the resultant equation with respect to time, yields the linearized equation

$$
\displaylines{
\frac{d^{2}\bar{p}}{dt^{2}}=-c_{f}^{2}\rho_{0}\nabla\cdot\frac{d\mathbf{v}}{dt}.
}
$$

Therefore, the wave equation, in terms of pressure, can be found

$$
\displaylines{
\nabla^{2}\bar{p}-\frac{1}{c_{f}^{2}}\frac{d^{2}\bar{p}}{dt^{2}}=0.
}
$$

## Waves in Elastic Solids

For an elastic media, one can apply Newton's second law, for each infinitesimal particle, to obtain the governing equations

$$
\displaylines{
\nabla \cdot \boldsymbol{\sigma}=\rho\frac{\partial^{2}\mathbf{u}}{\partial t^{2}},
}
$$

where \\(\boldsymbol{\sigma}\\) is the stress tensor, \\(\mathbf{u}(\mathbf{x},t)\\) is the displacement vector, \\(\rho\\) is the density, and the body forces, in this case, are neglected. 

For linear elastic materials the constitutive equations are given by

$$
\displaylines{
\boldsymbol{\sigma}=\mathbf{c}\boldsymbol{:}\boldsymbol{\varepsilon},
}
$$

where \\(\mathbf{c}\\) is the constitutive fourth order elasticity tensor of the material and \\(\boldsymbol{\varepsilon}\\) is the strain tensor. In fact, the strain tensor is related to the displacement, in linearized form, by

$$
\displaylines{
\left[\boldsymbol{\varepsilon}\right]=\frac{1}{2}\left([\nabla \mathbf{u}]+\underline{[\nabla \mathbf{u}]}\right),
}
$$

in which the underline \\(\underline{\square}\\) means a transpose operation, in matricial calculations.

(...)

Manipulation of Navier-Cauchy equations, leads to the following wave equations

$$
\displaylines{
\nabla^{2}\mathbf{u}_{\mathrm{L}}-\frac{1}{c_{\mathrm{L}}^{2}}\frac{\partial^{2}\mathbf{u}_{\mathrm{L}}}{\partial t^{2}}=0
}
$$

and 

$$
\displaylines{
\nabla^{2}\mathbf{u}_{\mathrm{T}}-\frac{1}{c_{\mathrm{T}}^{2}}\frac{\partial^{2}\mathbf{u}_{\mathrm{T}}}{\partial t^{2}}=0
}
$$

where 

$$
\displaylines{
c_{\mathrm{L}}=\sqrt{\frac{\lambda+2\mu}{\rho}},
}
$$

and

$$
\displaylines{
c_{\mathrm{T}}=\sqrt{\frac{\mu}{\rho}}.
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
