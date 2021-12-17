---
layout: page
title: My Projects
carousels:
  - images:
    - image: /images/bubble.png
    - image: /images/khi.png
    - image: /images/cube.png
  - images:
    - image: /images/dragon.png
    - image: /images/sloshing2.png
---
## Surface tension modelling in SPH

While doing some work on computer graphics schemes used in SPH, I became interested in multiphase flows and in particular how surface tension is modelled in SPH. There are 2 standard ways to modelling surface tension in SPH, the Continuum Surface Force Model and the Inter-particle force model. While comparisons have been carried out between the basic variations of these two models, no work has been done to compare the various other models based of the same fundamental idea. Through my work I hope to a have clear answer to the question "which surface tension model should I use for my particular SPH simulation?". I have carried out tests of 6 different models against a variety of standard benchmark problems and am now testing out the effectiveness of the models on mre real world applications like air bubble rising in water.

<p float="left">
  <img src="/images/bubble_rise.gif" width="225" />
  <img src="/images/khi.png" width="225" />
  <img src="/images/cube.png" width="225" />
</p>


<!-- {% include carousel.html height="500" unit="px" duration="7" number="1" %} -->
## Dam break and Sloshing tank simulations

Carried out various simulations of <a target="_blank" href="https://github.com/pypr/pysph/pull/263">dam break </a> in 2D and 3D and <a target="_blank" href="https://github.com/pypr/pysph/pull/272">sloshing tank</a> problems under horizontal and pitch excitement. These were added to the PySPH examples suite to be used as benchmark cases to test out new schemes. Through carrying out these simulations I gained a much better understanding of the WCSPH, $\delta$-SPH and EDAC schemes. Post-processing was done to compare these simulation results with experimental data to show the validity of the implemented schemes.

<!-- {% include carousel.html height="50" unit="%" duration="7" number="2" %} -->
<p float="left">
  <img src="\images\sloshing.gif" width="350"/>
  <img src="\images\dam_break.gif" width="350"/>
</p>

<!-- ![Sloshing tank]|(\images\sloshing.gif) -->

## PySPH and Mayavi

<a target="_blank" href="https://github.com/pypr/pysph">PySPH </a> is an open source framework for Smoothed Particle Hydrodynamics. We regularly import various geometry into SPH simulations. To get accurate simulations we require that the geometry be imported as a uniform distribution of particles. I improved the previous algorithm on PySPH to support this using ideas from geometry and nearest neighbour particle search, and you can find it <a target="_blank" href="https://github.com/pypr/pysph/blob/master/pysph/tools/mesh_tools.pyx">here</a>. This was initially supported for STL files and was later extended to multiple mesh file formats by making use of <a target="_blank" href="https://github.com/pypr/pysph/blob/master/pysph/tools/read_mesh.py">meshio</a>.

While working on STL files I developed <a target="_blank" href="https://github.com/enthought/mayavi/blob/master/examples/mayavi/data_interaction/normal_flipping_stl.py">code </a> that allowed you to visualize STL files and their normals and allow you to modify the direction of the normals using mouse interaction. This was done using Mayavi, a tool for scientific data visualization. I also wrote <a target="_blank" href="https://github.com/amalss18/mayavi/blob/484d3a567f25bca28ec1a604ed0053be6ec71539/tvtk/pyface/picker.py">code </a> to display the picker information on the scene rather than in a popup GUI.

<p float="left">
  <img src="/images/bunny1.png" width="225" />
  <img src="/images/bunny2.png" width="225" />
  <img src="/images/cube_stl.gif" width="225" />
</p>


