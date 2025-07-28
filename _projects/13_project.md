---
layout: page
title: Non-Stationary Analysis of Scramjet Unstart
description: another without an image
img: assets/img/cfd_images/emd_schematic.png
importance: 3
category: Work
---

In this work, a novel analysis method for non-stationary flows is presented.
The method is specifically designed to remove translation invariances from a given problem.
Translational invariances occur frequently in wave propagation problems, where wavefronts propagate in various directions in a non-periodic manner.
These invariances hinder the ability of common model order reduction techniques, especially data-driven ones.
The proposed method removes these invariances, and does so in an entirely data-driven fashion.
Furthermore, by removing the translational motion from the system, statistial stationarity is restored and analysis techniques like Proper Orthogonal Decomposition and Dynamic Mode Decomposition can be used.
The process is demonstrated on an upstream propagating shock train, which mimics the dynamics associated with the hazardous problem of scramjet unstart. 
A manuscript detailing the method and its findings can be found on my [ResearchGate](https://www.researchgate.net/profile/Jack_Sullivan22?ev=hdr_xprf) page.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/cfd_images/emd_schematic.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A schematic description of the proposed modal analysis method. Shown are the steps needed to remove the translational invariance associated with the scramjet unstart problem and to subsequently analyze the oscillatory dynamics of the flow.
</div>

