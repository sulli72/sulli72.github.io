---
layout: page
title: Hybridized Finite Difference Scheme for Burgers' Equation
description: An introductory code base designed to teach the hybridization of non-dissipative central schemes with shock capturing schemes 
img: assets/img/cfd_images/hybrid_sensor_snapshot.png
importance: 2
category: Fun
---

[CODE REPOSITORY LINK](https://github.com/sulli72/HYBRID_BURGERS)

This project focuses on the implementation of a hybrid finite difference scheme for hyperbolic systems.
In many simulations, the system being considered has both regions of smooth solution and regions of discontinuous solution.
A prime example of this is the case of a shock wave interacting with turbulence, where near the shock gradients are large and (infinitely) steep and away from the shock the flow varies smoothly in space.
In such settings, it is beneficial to use a non-dissipative central differencing scheme in smooth regions and a shock capturing scheme in shocked regions.
To enable accurate simulation, these two classes of scheme must be coupled to one another or 'hybridized'.
This code base presents a hybrid finite difference approach to solving Burgers' equation on a periodic domain, and allows one to use a central scheme of order 2, 4, 6, or 8 in smooth regions and the WENO5 scheme of Jhang and Shu in shocked regions. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/cfd_images/sensor_evolution.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cfd_images/blowup_sensor_evolution.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Two numerical solutions to the Burgers equation. On the left is a solution that uses the hybrid finite difference approach, with nodes treated using shock capturing being marked in red. On the right is a solution that uses only a central differencing scheme. Note that when shock capturing is not used, the simulation diverges and a wholly incorrect answer is given by the code. When shock capturing is used, the discontinuity in the solution is properly simulated and numerical stability is preserved.  
</div>


