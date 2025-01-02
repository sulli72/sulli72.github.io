---
layout: page
title: A Tutorial on Characteristic Boundary Conditions
description: An introductory note set on the theory and implementation of characteristic boundary conditions for hyperbolic conservation laws
img: assets/img/one_in_sketch.png
importance: 2
category: Fun
---

[PDF of Noteset](/assets/pdf/CHARBC_PDF.pdf)

This project focuses on the physical motivation, theoretical background, and numerical implementation of characteristic boundary conditions. The noteset can be found in the linked PDF, and the associated code repository can be found 
[here](https://github.com/sulli72/CHAR_BCS) or in the repositories page.

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

\section*{Overview}

Many interesting physical phenomena in nature can be described by the propagation of waves.
Some of the most prominent examples include the emanation of sound from an instrument, the vibrations of a string, the breaking of waves on the shore, and even the formation of shocks in supersonic flight.
Each of these processes can be expressed mathematically, through the form of a conservation law that describes how individual waves act to transport and preserve quantities like mass, momentum, or energy.

In the absence of dissipative effects such as friction, conservation laws for wave propagation problems are \textit{hyperbolic} in nature, meaning all information within the system is transmitted in a purely convective manner.
Intricate systems such as the equations of gas dynamics, may have multiple types of waves present, with each one affecting a very specific combination of variables in the system.
For example, when an acoustic wave passes through air it induces minute changes in pressure, while leaving the local temperature completely unaltered. 

Using the theory of characteristics, which underpins the broader study of hyperbolic equations, it is possible to derive a form of a given conservation law that reveals the behavior associated with each kind of wave present in a system.
Furthermore, it can be shown that we can actually manipulate these waves, letting us enforce some desired behavior within the physical problem of interest.
This has important consequences when considering cases on finite domains, and leads to elegant and robust boundary condition treatment for problems solved \textit{numerically} on discrete meshes.


\section*{Characteristic Form of Hyperbolic Equations}

It is paramount to note the subsequent derivation and notation was adopted from \citep{thompson1987time}.
We start with a generic hyperbolic conservation law of the form
\begin{equation}
    \mathbf{u}_t + f(\mathbf{u})_x = 0
\end{equation}
where $\mathbf{u}$ is a vector and $f(\mathbf{u})$ is a flux function.
We can rewrite this equation in quasi-linear form, i.e,
\begin{equation}
    \mathbf{u}_t + A\mathbf{u}_x = 0\\
    A = \dydx{f(\mathbf{u})}{\mathbf{u}}
\end{equation}
Furthermore, since the system is hyperbolic it is diagonlizable with strictly real eigenvalues. This leads to the two related eigenvalue problems of
\begin{equation}
    AR = R\Lambda ~~~~~~~~ A^TL = L\Lambda
\end{equation}
where $\Lambda$, $R$, and $L$ contain the eigenvalues, right eigenvectors, and left eigenvectors of $A$ respectively.
The left eigenvectors are attained by considering the transpose of $A$, given by $A^T$.
Physically, each eigenvalue corresponds to the speed at which a specific type of wave is propagated by the system, such as waves traveling at $\pm c$ in the second order wave equation.
Right eigenvectors describe what combination of the variables in $\mathbf{u}$ are propagated by each wave.
Left eigenvectors describe how much of each variable is included in this combination.