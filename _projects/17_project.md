---
layout: page
title: Effects of Wall Heat Transfer on Shock Train Behaviors
description: An investigation of how the mean and unsteady physics of shock train interactions are altered in the presence of wall heat transfer.
img: assets/img/cfd_images/SHOCKTAIN_WALL_TEMP.png
importance: 3
category: Work
---

In hypersonic flight environments, heat transfer along vehicle surfaces becomes the preeminent factor in vehicle design.
This is especially true within the flow paths of supersonic combustion ramjets (scramjets) that are used to power air-breathign vehicles within the hypersonic regime.
To date, minimal effort has been devoted to the study of how heat transfer affects scramjet flow structures, such as the shock train that frequently resides within the isolator subcomponent of these engines.
This work seeks to address this gap, by conducting controlled, high-fidelity simulations that allow the effects of wall heat transfer to be isolated. 
Three shock trains are studied, each defined by a unique wall heating condition.
In each case walls are treated isothermally, with the wall temperature (Tw) set to a fixed multiple of the nominal recovery temperature (Tr); leading to a hot wall case (Tw/Tr=1.20), a nominally adiabatic case (Tw/Tr=1.00), and a cold wall case (Tw/Tr=0.80).
Note that all other boundary conditions are identical across the cases, and the incoming flow is at Mach 2.0.  


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/cfd_images/SHOCKTRAIN_WALL_TEMP.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Instantaneous visualizations of the density fields in spanwise periodic shock trains subject to three different wall heating conditions. From top to bottom are a heated wall, a nominally adiabatic wall, and a cooled wall case. Each heating condition is defined by the ratio of isothermal wall temperature (Tw) to the recovery temperature of the flow (Tr). 
</div>



