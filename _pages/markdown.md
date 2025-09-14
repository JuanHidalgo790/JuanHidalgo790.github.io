---
permalink: /markdown/
title: "Modeling Background"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

Here, equations behind the examples presented on the homepage are depicted. Soon, other examples and methods will be added.

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

Therefore, the **wave equation**, in terms of pressure, can be found

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

For linear elastic materials, the constitutive equations are given by

$$
\displaylines{
\boldsymbol{\sigma}=\mathbf{c}\boldsymbol{:}\boldsymbol{\varepsilon},
}
$$

where \\(\mathbf{c}\\) is the constitutive fourth-order elasticity tensor of the material and \\(\boldsymbol{\varepsilon}\\) is the strain tensor. In fact, the strain tensor is related to the displacement, in linearized form, by

$$
\displaylines{
\left[\boldsymbol{\varepsilon}\right]=\frac{1}{2}\left([\nabla \mathbf{u}]+\underline{[\nabla \mathbf{u}]}\right),
}
$$

in which the underline \\(\underline{\square}\\) means a transpose operation, in matricial calculations.

The stress and the strain tensors are of second order, however, as they are symmetric, they can be represented as column vectors by using the Voigt notation, in which the indexes equivalence is presented in the following table, for each coordinate system (\\(x,y,z\\) or  \\(r, \theta, z\\)). 

| Coordinates | 1 | 2 | 3 | 4 | 5 | 6 |
|:--------:|:-------:|:--------:|:--------:|:--------:|:--------:|:--------:|
| Cartesian  | \\(xx\\)   | \\(yy\\)   | \\(zz\\)   | \\(yz,zy\\)   | \\(xz,zx\\)   | \\(xy,yx\\)   |
| Cylindrical   | \\(rr\\)   | \\(\theta \theta\\)   | \\(zz\\)   | \\(\theta z, z \theta\\)   | \\(rz,zr\\)   | \\(r \theta,\theta r\\)   |

For the strain components \\(\varepsilon_{4}\\), \\(\varepsilon_{5}\\) and \\(\varepsilon_{6}\\), it is necessary to introduce the factor of 2 to properly carry out the conversion between the systems, as indicated in the following table.  

| Coordinates | 1 | 2 | 3 | 4 | 5 | 6 |
|:--------:|:-------:|:--------:|:--------:|:--------:|:--------:|:--------:|
| Cartesian  | \\(\varepsilon_{xx}\\)   | \\(\varepsilon_{yy}\\)   | \\(\varepsilon_{zz}\\)   | \\(2\varepsilon_{yz}\\)   | \\(2\varepsilon_{xz}\\)   | \\(2\varepsilon_{xy}\\)   |
| Cylindrical   | \\(\varepsilon_{rr}\\)   | \\(\varepsilon_{\theta \theta}\\)   | \\(\varepsilon_{zz}\\)   | \\(2\varepsilon_{\theta z}\\)   | \\(2\varepsilon_{rz}\\)   | \\(2\varepsilon_{r \theta}\\)   |

In an isotropic material, using symmetry considerations, one can represent the fourth-order constitutive tensor as a matrix (Voigt Notation), so that the constitutive equation can be written in matrix form, as:

$$
\displaylines{
\begin{bmatrix}\sigma_{1}\\\sigma_{2}\\\sigma_{3}\\\sigma_{4}\\\sigma_{5}\\\sigma_{6}\end{bmatrix}=\left[\begin{array}{cccccc}\lambda+2\mu&\lambda&\lambda&0&0&0\\
\lambda&\lambda+2\mu&\lambda&0&0&0\\
\lambda&\lambda&\lambda+2\mu&0&0&0\\
0&0&0&\mu&0&0\\
0&0&0&0&\mu&0\\
0&0&0&0&0&\mu\end{array}\right]\begin{bmatrix}\varepsilon_{1}\\\varepsilon_{2}\\\varepsilon_{3}\\\varepsilon_{4}\\\varepsilon_{5}\\\varepsilon_{6}\end{bmatrix},
}
$$

where \\(\lambda\\) and \\(\mu\\) are the first and the second Lamé coefficients, respectively, that define the elastic properties of the isotropic material. This  is valid for both Cartesian and cylindrical coordinates. 

With some manipulations in Newton's second law, one obtains, for an isotropic material, the Navier-Cauchy equations (with body forces neglected)

$$
\displaylines{
(\lambda +2\mu)\nabla(\nabla\cdot\mathbf{u})-\mu\nabla\times\nabla\times\mathbf{u}=\rho\frac{\partial^{2}\mathbf{u}}{\partial t^{2}}.
}
$$

The displacement vector \\(\mathbf{u}(\mathbf{x},t)\\) can be decomposed, due to Helmholtz decomposition, as 

$$
\displaylines{
\mathbf{u}(\mathbf{x},t)=\mathbf{u}_{\mathrm{L}}(\mathbf{x},t)+\mathbf{u}_{\mathrm{T}}(\mathbf{x},t),
}
$$

such that

$$
\displaylines{
\nabla \times \mathbf{u}_{\mathrm{L}}&=0,\\
\nabla \cdot \mathbf{u}_{\mathrm{T}}&=0,
}
$$

where \\(\mathbf{u}\_{\mathrm{L}} \\) is the irrotational part of displacement, and represents the longitudinal displacement of the continuum, and \\( \mathbf{u}\_{\mathrm{T}} \\) is a divergence-free vector field that preserves the volume, representing the transversal component of the displacement (shearing motion). 

Manipulation of the Navier-Cauchy equations leads to the following **wave equations**

$$
\displaylines{
\nabla^{2}\mathbf{u}_{\mathrm{L}}-\frac{1}{c_{\mathrm{L}}^{2}}\frac{\partial^{2}\mathbf{u}_{\mathrm{L}}}{\partial t^{2}}=0,
}
$$

and 

$$
\displaylines{
\nabla^{2}\mathbf{u}_{\mathrm{T}}-\frac{1}{c_{\mathrm{T}}^{2}}\frac{\partial^{2}\mathbf{u}_{\mathrm{T}}}{\partial t^{2}}=0,
}
$$

where 

$$
\displaylines{
c_{\mathrm{L}}=\sqrt{\frac{\lambda+2\mu}{\rho}}
}
$$

and

$$
\displaylines{
c_{\mathrm{T}}=\sqrt{\frac{\mu}{\rho}}
}
$$

are the **longitudinal** and **transversal** bulk wave speeds of the material, respectively.

## Piezoelectric Effect

Piezoelectric materials have the characteristic of presenting an electrical polarization under deformation (**direct** piezoelectric effect), and deformation when subjected to an electric field (**inverse** piezoelectric effect).

![Image of the piezoelectric effect](/images/PiezoEffectJuan.png){: .align-center width="750px"}

The piezoelectric effect can be explained by the appearance of electric dipoles inside the crystalline structure of the material. The application of mechanical stress, and consequently a deformation, changes the intensity of polarization.

![Image of the piezoelectric effect](/images/PiezoEffectJuanCharges.png){: .align-center width="600px"}

The governing equations for piezoelectric materials are given by (stress-charge form):

$$
\displaylines{
\mathbf{D}&=\boldsymbol{\epsilon}^{\varepsilon}\boldsymbol{\cdot}\mathbf{E}+\mathbf{e}\boldsymbol{:}\boldsymbol{\varepsilon},\\
\boldsymbol{\sigma}&=-{\mathbf{e}}\boldsymbol{\cdot}\mathbf{E}+\mathbf{c}^{E}\boldsymbol{:}\boldsymbol{\varepsilon}
}
$$

where \\(\mathbf{D}\\) is the electric displacement vector, \\(\boldsymbol{\epsilon}\\) is the dielectric permittivity second order tensor, \\(\mathbf{E}\\) is the electric field vector, and \\(\mathbf{e}\\) represents the piezoelectric coupling third-order tensor, with components being _piezoelectric stress constants_. The superscripts \\(\varepsilon\\) and \\(E\\) were added to the dielectric permittivity tensor  \\(\boldsymbol{\epsilon}\\) and to the elastic tensor \\(\mathbf{c}\\) to indicate that their components are measured under conditions of constant strain and constant electric field, respectively. 

The **constitutive piezoelectric equations** can be written in **matrix form** by using symmetry considerations and Voigt notation, with the appropriate conventions for strain and stress tensors conversion to column vectors. For a 6mm crystal class, one has, in Cartesian coordinates, the following matrix equations

$$
\displaylines{
\begin{bmatrix}D_{x}\\D_{y}\\D_{z}\end{bmatrix}=\left[\begin{array}{ccc}\epsilon_{xx}^{\varepsilon}&0&0\\0&\epsilon_{yy}^{\varepsilon}&0\\0&0&\epsilon_{zz}^{\varepsilon}\end{array}\right]\begin{bmatrix}E_{x}\\E_{y}\\E_{z}\end{bmatrix} \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \\ \qquad \qquad +\left[\begin{array}{cccccc}0&0&0&0&e_{x5}&0\\0&0&0&e_{x5}&0&0\\e_{z1}&e_{z1}&e_{z3}&0&0&0\end{array}\right]\begin{bmatrix}\varepsilon_{xx}\\\varepsilon_{yy}\\\varepsilon_{zz}\\2\varepsilon_{yz}\\2\varepsilon_{xz}\\2\varepsilon_{xy}\end{bmatrix},\\\\
    \begin{bmatrix}\sigma_{xx}\\\sigma_{yy}\\\sigma_{zz}\\\sigma_{yz}\\\sigma_{xz}\\\sigma_{xy}\end{bmatrix}=-\left[\begin{array}{ccc}0&0&e_{z1}\\0&0&e_{z1}\\0&0&e_{z3}\\0&e_{x5}&0\\e_{x5}&0&0\\0&0&0\end{array}\right]\begin{bmatrix}E_{x}\\E_{y}\\E_{z}\end{bmatrix} \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad  \\ \qquad \qquad \qquad \qquad +\left[\begin{array}{cccccc}c_{11}^{E}&c_{12}^{E}&c_{13}^{E}&0&0&0\\c_{12}^{E}&c_{11}^{E}&c_{13}^{E}&0&0&0\\c_{13}^{E}&c_{13}^{E}&c_{33}^{E}&0&0&0\\0&0&0&c_{44}^{E}&0&0\\0&0&0&0&c_{44}^{E}&0\\0&0&0&0&0&\frac{1}{2}(c_{11}^{E}-c_{12}^{E})\end{array}\right]\begin{bmatrix}\varepsilon_{xx}\\\varepsilon_{yy}\\\varepsilon_{zz}\\2\varepsilon_{yz}\\2\varepsilon_{xz}\\2\varepsilon_{xy}\end{bmatrix}.
}
$$

## Lorentz Forces

Electromagnetic Acoustic Transducers (EMATs) are devices that operate through the Lorentz force by using the magnetorestrictive effect. Therefore, EMATs generate vibrations directly inside the material, allowing, with appropriate conditions, the generation of ultrasonic waves. This occurs through the interaction between a static magnetic field and an alternating induced current (Eddy's current), which generates a Lorentz Force causing vibrations in the material, consequently, the propagation of ultrasonic waves. It is worth mentioning that, compared to the piezoelectric transducer, no contact with the plate is required here.

![Image of the Lorentz effect](/images/EMAT_draw.png){: .align-center width="650px"}

So, the Lorentz forces can be calculated by the following vectorial product:

$$
\displaylines{
\mathbf{F} = \mathbf{J} \times \mathbf{B}_{0},
}
$$

where \\(\mathbf{F}\\) is the Lorentz force per volume unit, \\(\mathbf{J}\\) is the induced dynamic current density, and \\(\mathbf{B}_{0}\\) is the static magnetic field. 


<!--## Cylindrical Waves 

And so we have the wave equation in cylindrical coordinates:

$$
\displaylines{
\frac{\partial^{2}u_{r}}{\partial r^{2}}+\frac{\partial}{\partial r}\left(\frac{1}{r}u_{r}\right)-\frac{1}{c_{\mathrm{L}}^{2}}\frac{\partial^{2}u_{r}}{\partial t^{2}}=0
}
$$ 


## References -->

**References:**
*   [Auld]. "[Wave Motion]." *[Book]*, [1974], [URL]. Accessed on [21 June 2025].
