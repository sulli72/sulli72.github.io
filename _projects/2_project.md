---
layout: page
title: A Tutorial on Characteristic Boundary Conditions
description: An introductory note set on the theory and implementation of characteristic boundary conditions for hyperbolic conservation laws
img: assets/img/one_in_sketch.png
importance: 2
category: Fun
giscus_comments: true
---

This project focuses on the physical motivation, theoretical background, and numerical implementation of characteristic boundary conditions. The noteset can be found in the linked PDF, and the associated code repository can be found at https://github.com/sulli72/CHAR_BCS or in the repositories page.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/nonreflecting.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/dirichlet.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/neumann.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Different boundary conditions for the second order wave equation. Left, non-reflecting conditions at both ends. Center, Dirichlet at endpoints. Right, Neumann zero-gradient conditions.
</div>
