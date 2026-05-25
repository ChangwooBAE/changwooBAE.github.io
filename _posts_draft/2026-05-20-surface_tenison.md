---
layout: post
title: Surface tension
date: 2026-05-20
description:
tags: knowledge science
categories: 
image_path: assets/img/post/2026-05-20-surface_tension
thumbnail: assets/img/post/2026-05-20-surface_tension/tension_molecule.jpg
---




### Surface tension - Energy perspective

In a liquid, intermolecular attraction is stronger than thermal motion, allowing molecules to remain bound together. If thermal motion were dominant over these attractive forces, the substance would exist in the gaseous phase. Within the bulk liquid, molecular interactions are isotropic, so each molecule experiences balanced forces from its surroundings, giving rise to zero net force. In contrast, molecules located at **an interface** lose roughly half of their cohesive interactions, as illustrated in `Fig. 1`. To reduce the energetic penalty associated with this imbalance, the liquid surface deforms to minimize its area, which gives rise to **surface tension**.

{% include post_image.liquid
  filename="tension_molecule.jpg"
  alt="Surface tension"
  max_width="500px"
  width="50%"
  loading="eager"
  centered="true"
  figure_num="1"
  caption="Molecules in the bulk and at the liquid/gas interface. While the one in the bulk is in the presence of isotropic interactions with adjacent molecules, the one at the interface is in the absence of half its cohesive interactions."
%}

When a liquid molecule is positioned at the surface, it experiences an unfavorable energy state. Within the liquid, if the cohesion energy per molecule is $$U$$, a molecule at the surface lacks approximately half of this energy, or $$U/2$$. Given that the typical molecular size is $$a$$, the energy per molecular area is written as $$E_m=U/2a^2$$. The total energy, $$E_s$$, over the whole surface area, $$S$$, is called **"surface energy"** and is simply $$E_s = S E_m = S~U/2a^2$$. Here, the coefficient of the surface area is what we call **"surface tension"**, which is $$\gamma=U/2a^2$$.


In my favorite book, [`Capillarity and Wetting Phenomena`](https://link.springer.com/book/10.1007/978-0-387-21656-0) [1], the authors estimated the surface tensions of different liquids very simply. For most oils, where van der Waals forces dominate, $$U$$ is roughly equal to the thermal energy $$kT$$. At $$25^\circ \mathrm{C}$$, $$kT$$ is approximately $$1/40~\mathrm{eV}$$, resulting in a surface tension $$\gamma$$ of about $$20~\mathrm{mJ/m^2}$$. Water, due to its hydrogen bonding, has a higher surface tension of approximately $$72~\mathrm{mJ/m^2}$$. Mercury, a liquid metal with strong cohesive forces and U around $$1~\mathrm{eV}$$, has a surface tension close to $$500~\mathrm{mJ/m^2}$$.









<div style="margin-bottom: 6rem;"></div>

### References

[1] Gennes, P. G., Brochard-Wyart, F., & Quéré, D. (2004). Capillarity and wetting phenomena: drops, bubbles, pearls, waves (pp. 7-9). Springer New York.