---
layout: page
title: Orr-Sommerfeld Discretizations with Finite Differences
description: A sample hydrodynamic stability code base for introductions to the Orr-Sommerfeld operator  
img: assets/img/cfd_images/ORR_SOMMERFELD_SPECTRUM.png
importance: 2
category: Fun
---

[CODE REPOSITORY LINK](https://github.com/sulli72/TRANSIENT_GROWTH_FD)

This project focuses on the analysis of transient growth for linear disturbances in hydrodynamic stability theory. Finite difference matrices are used to approximate the needed derivatives in the linear operators, which are used to assess the induced energy growth of infinitesimal disturbances by the non-normal operators governing the perturbations.The code has been validated against the reference solutions in Chapter 4 of the textbook 'Stability and Transition in Shear Flows' by Schmid and Henningson, 2001. This code was written by me to help 'lift the veil' on transient growth analysis, as the topic had always both fascinated and confused me. To help learn, I coded up the needed discretizations by hand using finite difference schemes. Research grade codes should likely make use of spectral approaches, on account of their superior accuracy, enhanced  efficiency, and the incredibly sensitivity of numerical stability analyses. However, for pedagogical purposes simple finite difference approaches suffice and can lead to insights into both theory and practice.  

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/cfd_images/ORR_STRUCTURES.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Optimal initial conditions that lead to maximum transient growth for 2D disturances at streamwise wavenumber alpha=1.0.  
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/cfd_images/ENERGY_GROWTH_CURVE.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Gain of disturbance energy over time within plane Poiseuille flow at Re = 1000. Note the initial disturbace is normalized to be unit amplitude, highlighting that transient growth mechanisms can inject huge perturbation energies even in a linearized setting.
</div>

