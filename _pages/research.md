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
My past research has resulted in the development of a new finite element method, called the <a href="https://link.springer.com/chapter/10.1007/978-3-030-41800-7_2">Automatic Variationally Stable Finite Element (AVS-FE) method</a>.
Currently, much of my research efforts are focused on development of finite element methods and coupling of finite element methods to exploit the properties of individual methods and models across the coastal floodplain. A second ongoing research topic I devote a significant amount of effort to is the verification of new 
 finite element meshes for the <a href="https://adcirc.org">ADCIRC</a> model to be used on the operational forecasting of hurricane storm surge on the US Gulf coast. I am also fortunate to work on a wide array of other smaller and larger projects with talented postdocs and Ph.D. students in the Computational Hydraulics group at the Oden Institute.   
</p>

<p style="text-align: justify">
A significant portion of my work and research requires programming and development of computer codes. These codes are nearly always openly available online, see for example the ADCIRC website and my  <a href="https://github.com/evalseth/Stable_FEMs">code repository</a> of stable finite element methods implemented in <a href="https://fenicsproject.org">FEniCS</a>.
</p>



## Finite Element Methods

<p style="text-align: justify">
My Ph.D. research, supervised by <a href="https://www.sdsmt.edu/Directories/Personnel/Romkes,-Albert/">Albert Romkes</a>, was spent focusing on the 
development of the AVS-FE method. This method is a discontinuous Petrov-Galerkin (DPG) method (developed by <a href="https://users.oden.utexas.edu/~leszek/">Leszek Demkowicz</a> and <a href="http://web.pdx.edu/~gjay/">Jay Gopalakrishnan</a>) making the particular choice of fully continuous trial spaces. 
As the method is still in its early days of development, the focus has been verification of its properties for a wide range of engineering problems 
including convection-dominated diffusion, nearly incompressible elastostatics, Cahn-Hilliard equation, and wave propogation to mention a few.
After starting my postdoctoral research, I have focused on analysis of the method as well as its application to the modeling of hurricane storm surge. 
Additionally, as part of a multi-institution ongoing National Science Foundation sponsored project, my work has also included further development of the existing 
 finite element software named discontinuous Galerkin Shallow Water Equations model (DG-SWEM) for the use in complound flood modeling.
</p>

### The AVS-FE Method

<figure>
  <img src="/assets/images/l2_err_u.png" alt=""> 
  <figcaption style="text-align: justify"> Optimal <em>hp</em>-asymptotic convergence rates for the AVS-FE method applied to a convection-diffusion PDE - <em>L</em><sup>2</sup> error of the PDE base variable. </figcaption>
</figure>
    
<p style="text-align: justify">
The AVS-FE method is uncondtionally stable, regardless of the underlying differential operator and FE mesh. The stability is derived from the DPG concept of 
optimal discontinuous test functions computed on-the-fly, whereas the trial space consist of classical FE basis functions.  
</p>

###### Calo, V.M., Romkes, A., Valseth, E. (2020) Variationally Stable Analysis for Finite Element Computations: An Introduction _Lecture Notes in Computational Science and Engineering_ [[doi](https://doi.org/10.1007/978-3-030-41800-7)]

### Goal-Orietned Error Estimation 
                               
<figure>
  <img src="/assets/images/figs.pdf" alt="">
  <figcaption style="text-align: justify">Goal-oriented mesh refinement for a convection-domainated diffusion problem in the AVS-FE method using a new approach to the solution of the dual problem. The qunatity of interest is the flux across a line segment on the left side of the domain.  Left: Convergence of the estimate and exact error.  Center: Effectivity index of the estimate. Right: Final adapted mesh. </figcaption>
</figure>

<p style="text-align: justify">
The stability property of the AVS-FE allows us to establish approximations of the dual problem to the convection-domainated diffusion PDE which is necessary in goal-oriented error estimation. To ensure a continuous dual solution, we introduce a new approach in which we consider the dual PDE and its AVS-FE approximation. This leads to highly accurate error estimates even for convection dominated scenarios in which classical FE methods suffer from loss of stability. The first-order system description in the AVS-FE method also allows straightforward error estimation of fluxes.   
</p>

###### Valseth, E. and Romkes, A., (2020) Goal-Oriented Error Estimation for the Automatic Variationally Stable FE Method for Convection-Dominated Diffusion Problems  _Accepted to Computers and Mathematics with Applications_ [[preprint](https://arxiv.org/pdf/2003.10904)]


## Applications


### Mineral Separation 

<figure>
  <img src="/assets/images/figs2.pdf" alt="">
  <figcaption style="text-align: justify">Phase evolution of a binary liquid towards the lowest energy state governed by the Cahn-Hilliard equation.  Left: Initial state.  Center: 0.0015 seconds into evolution process. Right: Final state after 0.015 seconds. </figcaption>
</figure>
    

<p style="text-align: justify">
The extraction and refinement of minerals is generally requires vast amounts of water, in some cases up to 60,000 m<sup>3</sup>  per day.
In an effort to reduce this amount of water a team of researchers at <a href="https://www.sdsmt.edu/">South Dakota School of Mines and Technology</a> is working on novel refinement techniques under a NSF grant titeled <a href="https://www.nsf.gov/awardsearch/showAward?AWD_ID=1805550&HistoricalAwards=false"> Sustainable System for Mineral Beneficiation
</a>. 
As a mathematical model for the mineral separation, we use the Cahn-Hilliard equation and develop corresponding space-time finite element approximations in an effort to predict the mineral separation process. Working with metallurgists and mineral separation experts, a space-time AVS-FE method will be used to predict the mineral separation process and guide the design process of a new mineral separator.
</p>


###### Valseth, E., Romkes, A., and Kaul, A., (2020) A Stable FE Method For the Space-Time Solution of the Cahn-Hilliard Equation  _Accepted in Journal of Computational Physics_ [[preprint](https://arxiv.org/pdf/2006.02283.pdf)]

### Water Wave Propagation

<figure>
  <img src="/assets/images/figs3.pdf" alt="">
  <figcaption style="text-align: justify"> One dimensional surface water wave propagation governed by the Korteweg-de Vries equation. Left: Space-time solution of the Korteweg-de Vries equation, the colorbar represents the elevation of the surface in space (x-axis) and time (y-axis). Right: Final adaptively refined mesh. </figcaption>
</figure>
    

<p style="text-align: justify">
In an ongoing sequence of papers, <a href="https://www.oden.utexas.edu/people/36/">Clint Dawson</a> and I are developing DPG methods for the mathematical modeling of hurricane storm surge. 
As an initial verification, we considered the Korteweg-de Vries equation, one of the simplest water wave mathematical models. Currently, we are working on more complex mathematical models such as the shallow water equations.
</p>


###### Valseth, E., Dawson, C. (2020) An Unconditionally Stable Space-Time FE Method for the Korteweg-de Vries Equation. _Computer Methods in Applied Mechanics and Engineering_ 371:113297, [[doi](https://doi.org/10.1016/j.cma.2020.113297)]


### Shallow Water Flow

<figure>
  <img src="/assets/images/SW_figs.pdf" alt="">
  <figcaption style="text-align: justify"> Adaptive mesh refinement for the limiting case of purely convective flow. Left: x component of the depth-averaged velocity field. Center: Adaptively refined mesh Right: Convergence history. </figcaption>
</figure>
    

<p style="text-align: justify">
 In the second paper in this sequence, we considered the 2D shallow water equations. We establish a priori error estimates as well a multiple numerical 
 experiments to verify converegence behavior of our space-time FE approximations. 
We perform multiple verifiactions of physical benchmarks such as dam break and tidal fluctuations. Additionally, we confirm the well-balanced property of the
 method for the important lake-at-rest case.
</p>



###### Valseth, E., Dawson, C., (2020) An Adaptive Stable Space-Time FE Method for the Shallow Water Equations  _Submitted_ [[preprint](https://arxiv.org/pdf/2011.04786.pdf)] 


### Nearly Incompressible Materials

<figure>
  <img src="/assets/images/elastic_figs.pdf" alt="">
  <figcaption style="text-align: justify"> Adaptive mesh refinement for a composite material consisting of a stiff inclusion and a nearly incompressible rubber matrix. Left: Problem definition. Center: Adaptively refined mesh Right: x-component of the normal stress. </figcaption>
</figure>
    

<p style="text-align: justify">
For modern enginerering materials such as polymers and composite materials, classical finite element methods often suffer from a loss of stability when the Poisson's ratio approach the incompressible limit. To present a robust method that does not loose stability in this limit, we introduce a weighted least squares FE method for nearly incompressible linear elastostatics. We establish a priori error bounds and several numerical verifications comparing our method to the classical Bubnov-Galerkiun and least squares FE methods. Numerical verifications exploiting a built-in error indicator in adaptive mesh refinements and consideration of a classical engineering structure, a beam, show the applicability of the method to challenging engineering applications. 
</p>



###### Valseth, E., Romkes, R., Kaul, A., Dawson, C., (2021) A Stable Mixed FE Method for Nearly Incompressible Linear Elastostatics  _International Journal for Numerical Methods in Engineering_ [[doi](https://doi.org/10.1002/nme.6743)] 



## Coastal Modeling

<p style="text-align: justify">
In a sequence of projects and papers, we model and investiate the impacts of dredging a ship channel on the Texas Coast. We first consider the effects on estuarine dependent fish larvae through modeling coastal circulation and Lagrangian particle transport. In the second case, we consider the effects on hurricane storm surge magnitude and inundation. In particular, we study the impacts of Hurricane Harvey and synthesized versions of Harvey. 
</p>

### Modeling of Fish Larvae Transport 

<p style="text-align: justify">
The Port of Corpus Christi is a busy shipping hub for shipping goods and materials to and from the United States. To reach the port, ships must travel through the 47 ft. deep man made ship channel which extends from the Aransas Pass to the port. To accomodate larger ships, an increase in the depth of this ship channel has been proposed. In collaboration with <a href="https://utmsi.utexas.edu/component/cobalt/item/9-marine-science/320-buskey-edward-j?Itemid=550">Ed Buskey</a> of The Univeristy of Texas at Austin Marine Science Institute, we develop mathematical models governing the transport of Red drum fish larvae, modeled as passive Lagrangian particles. Our numerical models indicate negligible impacts of the proposed deeper channel on the transport of Red drum larvae from offshore breeding grounds through Aransas Pass to appropriate nursing grounds. 
</p>


###### Valseth, E., Loveland, M., Dawson, C., Buskey, E., (2021) A Study of the Potential Impact of Dredging the Corpus Christi Ship Channel on Passive Particle Transport. _Journal of Marine Science and Engineering_ [[doi](https://doi.org/10.3390/jmse9090935)]

### Modeling of Storm Surge

<p style="text-align: justify">
The Port of Corpus Christi is a busy shipping hub for shipping goods and materials to and from the United States. To reach the port, ships must travel through the 47 ft. deep man made ship channel which extends from the Aransas Pass to the port. To accomodate larger ships, an increase in the depth of this ship channel has been proposed. In collaboration with <a href="https://utmsi.utexas.edu/component/cobalt/item/9-marine-science/320-buskey-edward-j?Itemid=550">Ed Buskey</a> of The Univeristy of Texas at Austin Marine Science Institute, we develop mathematical models governing hurricane storm surge. We apply the National Hurricane Center best track model and a Generalized Asymmetric Holland Model for hurricane wind and pressure fields. For the condisdered Hurricane Harvey and synthesized versions of Harvey, our model finds that most of the area near Corpus Christi will experience a reduced maximum surge magnitude, whereas some localized areas will see increased suge up to 15cm. 
</p>


###### Valseth, E., Dawson, C., Buskey, E., (2023) A Study of the Potential Effects of Deepening the Corpus Christi Ship Channel on Hurricane Storm Surge. _Journal of Computational Science_ 

<p style="text-align: justify">
Accurate, efficient numerical models for storm surge are critical for both long-term risk assesment and to guide emergency management decisions during and before events. While high-fidelity hydrodynamic models such as the ADvanced CIRCulation (ADCIRC) model can accurately predict storm surge, they are very computationally expensive. In this paper, we develop a novel surrogate for the prediction of peak storm surge based on a multi-stage approach. In the first stage, points are classified as inundated or not. In the second, the level of inundation is predicted for each point. Within the new fromulation, we propose a surrogate in which storm surge is predicted independently for each point. This allows for predictions to be made directly for locations not present in the training data, and leads to a reductuib in the number of required model parameters. We our  framework on two vastly diffrent study areas: the Texas coast and the northern portion of the Alaskan coast. For Texas, the model is trained with a large database of synthetic hurricanes, whereas for Alaska, the model is trained on a dataset of 109 historical surge events. We test the surrogate model on actual surge events including the recent Typhoon Merbok (2022) in Alsaska and Hurricane Harvey (2017) in Texas that take place after the events in the training data. 
</p>


###### Pachev, B., Arora, P., del-Castillo-Negrete, C., Valseth, E., & Dawson, C., (2023) A framework for flexible peak storm surge prediction. _Coastal engineering_ [[doi](https://doi.org/10.1016/j.coastaleng.2023.104406)]

## Disease and Flood Modeling

<p style="text-align: justify">
A recent report by the <a href="https://www.who.int/news-room/fact-sheets/detail/climate-change-and-health">World Health Organization</a>, noted the effects of the changing climate on the spread of infectious diseases. For example, after flooding events, increased transmission of diseases such as <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5079365/">Malaria</a> has been frequently noted and observed.   
In a project recently funded by the <a href="https://wellcome.org">Wellcome Trust</a>, we investigate and seek to develop new integrated flood and disease models to better predict and understand the interplay between the two processes.  
</p>


