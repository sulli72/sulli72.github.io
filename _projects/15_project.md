---
layout: page
title: Orr-Sommerfeld Discretizations with Finite Differences
description: A sample hydrodynamic stability code base for introductions to the Orr-Sommerfeld operator  
img: assets/img/cfd_images/ORR_SOMMERFELD_SPECTRUM.png
importance: 2
category: Fun
---

[CODE REPOSITORY LINK](https://github.com/sulli72/ORR_SOMMERFELD_FD)

This project focuses on the discretization of the Orr-Sommerfeld operator used in hydrodynamic stability theory. Finite difference matrices are used to approximate the needed derivatives in the linear operator, which is subsequently eigendecomposed and its spectrum examined.The code has been validated against the reference eigenvalues in Appendix A of the textbook 'Stability and Transition in Shear Flows' by Schmid and Henningson, 2001. Furthermore, the code faithfully reproduces the well known result of plane Poiseuille flow becoming unstable at Re = 5772.22 and at a streamwise wavenumber of alpha ~ 1.02. The spectrum of this unstable channel case is presented in the attached figure. Note that this code was written to help teach computational hydrodynamic stability to myself, as the theory has made conceptual sense to me (after extensive reading and admittedly large amounts of initial frustration) but the act of discretizing and solving the eigenvalue problem did not quite click. In order to remedy this, the present code was written to help learn. It is hoped that the code will serve a similar purpose for others - though it must be clearly disclaimed that this is NOT a research caliber code and should not be used as such.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/cfd_images/ORR_SOMMERFELD_SPECTRUM.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Specrtum of Orr-Sommerfeld operator at critical Reynolds number of Re = 5772.22, and the critical streamwise wavenumber.  
</div>


