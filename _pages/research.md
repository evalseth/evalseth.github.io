---
title: "Research"
layout: single
sitemap: true
permalink: /research/
author_profile: true
toc: true
toc_label: "Research"
toc_icon: "gear"
---

<p style="text-align: justify">
I consider myself an engineer and scientist within the area of computational mechanics and applied mathematics. 
My research is in the intersection engineering, mathematics, physics, and computational science. In particular, I develop finite element methods for challenging problems in engineering science and physics. 
</p>

<p style="text-align: justify">
My recent research has resulted in the development of a new finite element method, called the <a href="https://link.springer.com/chapter/10.1007/978-3-030-41800-7_2">Automatic Variationally Stable Finite Element (AVS-FE) method</a>.
I am currently working on applying this new method in the modeling of hurricane storm surge, as well as the improvement of existing finite element software 
libraries for the same models.
</p>

## Finite Element Methods

<p style="text-align: justify">
My Ph.D. research, supervised by <a href="https://www.sdsmt.edu/Directories/Personnel/Romkes,-Albert/">Albert Romkes</a>, was spent focusing on the 
development of the AVS-FE method. This method is a discontinuous Petrov-Galerkin (DPG) method (developed by <a href="https://users.oden.utexas.edu/~leszek/">Leszek Demkowicz</a> and <a href="http://web.pdx.edu/~gjay/">Jay Gopalakrishnan</a>) making the particular choice of fully continuous trial spaces. 
As the method is still in its early days of development, the focus has been verification of its properties for a wide range of engineering problems 
including convection-dominated diffusion, nearly incompressible elastostatics, Cahn-Hilliard equation, and wave propogation to mention a few.
After starting my postdoctoral research, I have focused on analysis of the method as well as its application to the modeling of hurricane storm surge. 
Additionally, as part of a National Science Foundation sponsored project, my work has also included further development of the existing finite element software
named discontinuous Galerkin Shallow Water Equations model (DG-SWEM).
</p>

### The AVS-FE Method

<figure>
  <img src="/assets/images/l2_err_u.png" alt=""> 
  <figcaption style="text-align: justify"> Optimal <em>hp</em>-asymptotic convergence rates for the AVS-FE method applied to a convection-diffusion PDE - <em>L<em><sup>2</sup> error of the PDE base variable. </figcaption>
</figure>
    
<p style="text-align: justify">
The AVS-FE method is uncondtionally stable, regardless of the underlying differential operator and FE mesh. The stability is derived from the DPG concept of 
optimal discontinuous test functions computed on-the-fly, whereas the trial space consist of classical FE basis functions.  
</p>

###### Calo, V.M., Romkes, A., Valseth, E. (2020) Variationally Stable Analysis for Finite Element Computations: An Introduction  [[doi](https://doi.org/10.1007/978-3-030-41800-7)]

### Goal-Orietned Error Estimation 
                                
<figure>
  <img src="/assets/images/figs.pdf" alt="">
  <figcaption style="text-align: justify">Goal-oriented mesh refinement. Left:  Center: Right: </figcaption>
</figure>



