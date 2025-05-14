---
permalink: /
title: "Hello there, welcome to my webpage!"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

![Illustration of modeling engineering machines using computer](/images/image__my_webpage.jpeg){: .align-right width="250px"}

👨🏻‍💻 I am a PhD in mechanical engineering and an enthusiast of computational modeling for diverse engineering problems. 

🔬 My research interests are in the development of numerical models for solving acoustic problems, with approaches focused on optimizing computational resources.

📚 I am currently working with electromagnetic acoustic transducers (EMATs) in my post-doctoral research, aiming to improve their designs. 

🔩 Also, I'm working with the acoustoelastic effect applied to the non-destructive testing (NDT) area using Lamb waves. 

🧪 Some of my previous creations will be featured on this webpage.

🛠 This page is under construction... so soon, more content will be available!

[//]: # A data-driven personal website
[//]: # ======
[//]: # Under development...

[//]: # Getting started
[//]: # ======
[//]: # 1. Register a GitHub account if you don't have one and confirm your e-mail (required!)

[//]: # Site-wide configuration
[//]: # ------


[//]: # Create content & metadata
[//]: # ------


[//]: # **Markdown generator**


[//]: # How to edit your site's GitHub repository
[//]: # ------

# Some modeling examples

Here, I leave some examples that were constructed during these recent years. Next, each of them will be depicted, and their challenges will be discussed as well.  

## Modeling of an oil well under acoustic logging

This model was developed during my doctorate and was part of a challenging project which consisted of the development of AI models for identifying the integrity of the annular cement of oil wells, based on acoustic logging data. 

So, the model consists of a section of an oil well that undergoes an inspection analysis using acoustic waves. Therefore, an acoustic signal is generated inside the inner tube, at the upper part, and guided waves follow downwards, carrying information from the layers, including those of the cement.

![Image of an oil well](/images/Well_Simulation_Movement.gif){: .align-center width="520px"} 

In more realistic configurations, there is often the presence of eccentricity between the tubes. Therefore, the use of 3D models is mandatory. However, due to the frequencies of the acoustic signals, the mesh tended to be very heavy, requiring a large amount of computational resources. 

During the project, to optimize the usage, avoiding costs with clusters, the same model was constructed using light open-source tools. Therefore, the mesh was constructed using [GMSH](https://gmsh.info/), and the compilation was performed with the [openCFS](https://opencfs.org/) tool, which is based on C++. So, lightweight models could be achieved and run on not very sophisticated computers. 

![Image of a mesh of an oil well](/images/GMSH_3pipes_3D_mesh_eccentricity_cut.png){: .align-center width="460px"} 

Finally, to obtain the information of interest, the [ParaView](https://www.paraview.org/) software was used, and also provided the GIF image on this page. Here, it is interesting to comment that the open-source tools also proved to be a good option for integrating the model as a plug-in on any software, since all the libraries are freely available.

## Modeling the transmission of an acoustic wave from a piezoelectric transducer 

For a more realistic simulation of the generation of the acoustic waves, a piezoelectric transducer, which is commonly used in acoustic logging tools, was modeled. The piezoelectric effect, relating the voltage applied to the produced deformation, was taken into account. So, using an appropriate signal, and taking advantage of the resonance mode of the longest length, nearly omnidirectional waves could be achieved. 

[//]: ![Image of a piezoelectric transducer](/images/Piezo_CFS_acoustic.png){: .align-center width="800px"}

![Image of a piezoelectric transducer](/images/Gif_PiezoAcoustic.gif){: .align-center width="700px"}

To see the waveform created, a probe was placed beside the transducer's wall, leading to the black line plot. In the same plot, the internal damping effect of the transducer could also be observed after the internal reverberations. 

The corresponding mesh in this example was _structured_ and had elements with edge lengths appropriate for this type of acoustic problem. 

![Image of a piezoelectric transducer](/images/Mesh_Piezo_CFS_GMSH.png){: .align-center width="700px"}

## Modeling the transmission of shear waves from an Electromagnetic Acoustic Transducer (EMAT)

![Image of a piezoelectric transducer](/images/StressVonMises_PPM_paper02025.png){: .align-center width="700px"}



