---
layout: page
title: Autologous Chemotaxis
description: What condition do cells fail at autologous chemosensing and how that failure can be overcome 
img: assets/img/autologous/250cellwake.png
importance: 1
category: past work
giscus_comments: false
related_publications: vennettilli2022autologous, gonzalez2023collective
---

Autologous chemotaxis is the process in which a cell secretes diffusible ligand that is then biased in the direction of some oncoming fluid flow. The cell then binds to that autocrine and the asymmetry in concentration on its upstream and downstream side is what leads to downstream migration. 

This is was originally discovered in tumors where it is advantageous of a tumor cell to exploit physiological drainage into vessels to continue the process of cancer metastasis. 


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig1.pdf" title="" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig3.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/250cellwake.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (Left) Concentration field saturates in a finite domain. (Middle) Autocrine signals are also paracrine in clusters, causing cells to sense the contribution of other cells secreting the same ligand. (Right) Steady state solution of the N = 250 advection diffusion equation. Gradient decreases as cell density increases.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/ncell_advdiff_800s.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    N-body advection diffusion equation simulation for N = 250 cells. The concentration saturates the finite domain, causing the box to become more and more redder over time. This saturation causes the individual cells in the box to ineffectively determine the fluid flow direction. In the context of cancer, this stops tumor cells from traveling downstream towards the vessel. 
</div>

If one where to track how the surface concentration asymmetry (anisotropy) changes as a function of increasing cell density, one would find an explicitly inverse dependence. The cell does not improve, but rather worsens, in its flow-sensing ability as one increases the amount of cells in the finite chamber. This follows from experiments done that motivated this work. Please see the referenced papers.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig2.pdf" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    N-body advection diffusion equation simulation for N = 250 cells. The concentration saturates the finite domain, causing the box to become more and more redder over time. This saturation causes the individual cells in the box to ineffectively determine the fluid flow direction. In the context of cancer, this stops tumor cells from traveling downstream towards the vessel. 
</div>

While experimentally, cells are shown to be increasingly unsuccessful in sensing flow direction with the increase of cell density, and that is confirmed through simulations above, cells could theoretically overcome this failure. If cells where to perform a collective computation where this collective (or cluster, in the case of tumor cells) tracks the temporal change in concentration (signal strength $ \psi_c $) and the spatial change ($ \psi_g $), then they would be able to resolve the concentration field more effectively and continue traversing towards the endothelium to enter the next phase of metastasis. 

A good way to put this is: imagine a camera. In low light conditions, the camera is not effective at being able to give a clear picture. However, the more pixels there are in the sensor, the better the image will be as more pixels are collecting photons, decreasing the loss (improving the signal-to-noise ratio for the sensor). The low light condition reflects the inherently low-signal nature of the cell environment, where single molecules are released per second per cell. 

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (Left) A monte-carlo simulation of cells that are initialized as a cluster and allowed to undergo chemotaxis, a biased random walk where the cells are following spatial graidents and concentration gradients. The former causes cells to travel in the direction of fluid flow while the latter is what allows the cells to stick together. (Right) The difference in individual vs collective autologous chemosensing. If cells compute the concentration signal as individuals, they are fundamentally limited in their measurement by the spatial gradient within the finite box, which homogenizes as cell density increases. However, if they compute the concnetration as a collective, they instead improve their measurement the higher the number of individual agents participating in the concentration. This is akin as a camera's ability to resolve an image is dependent on how many pixels are in its image sensor. 
</div>

Below are selected publications related to this work. Feel free to explore further. 



