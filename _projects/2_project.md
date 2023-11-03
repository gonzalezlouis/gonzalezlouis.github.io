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

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig1.pdf" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/ncell_advdiff_800s.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    N-body advection diffusion equation simulation for N = 250 cells. The concentration saturates the finite domain, causing the box to become more and more redder over time. This saturation causes the individual cells in the box to ineffectively determine the fluid flow direction. In the context of cancer, this stops tumor cells from traveling downstream towards the vessel. 
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/autologous/fig2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (Left) A monte-carlo simulation of cells that are initialized as a cluster and allowed to undergo chemotaxis, a biased random walk where the cells are following spatial graidents $\psi_g$ and concentration gradients $\psi_c$. The former causes cells to travel in the direction of fluid flow while the latter is what allows the cells to stick together. (Right) The difference in individual vs collective autologous chemosensing. If cells compute the concentration signal as individuals, they are fundamentally limited in their measurement by the spatial gradient within the finite box, which homogenizes as cell density increases. However, if they compute the concnetration as a collective, they instead improve their measurement the higher the number of individual agents participating in the concentration. This is akin as a camera's ability to resolve an image is dependent on how many pixels are in its image sensor. 
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:


```
{% endraw %}
