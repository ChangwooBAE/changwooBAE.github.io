---
layout: post
title: About surface tension
date: 2025-04-13
description: How far do you understand surface tension?
tags: knowledge
categories: science
image_path: assets/img/post/2025-04-13-surface_tension
thumbnail: assets/img/post/2025-04-13-surface_tension/waterstrider.jpg
---

### -- Surface tension?

{% include post_image.liquid
  filename="waterstrider.jpg"
  alt="Water strider"
  max_width="100px"
  width="30%"
  loading="eager"
  centered="true"
  figure_num="1"
  caption="A water strider standing on a water interface thanks to surface tension of water. Although its weight creates an indentation, the surface tension is sufficient to sustain the insect without breaking the interface."
%}

Have you ever seen water striders floating on a puddle after raining? Water striders can be found in most of the continents, and their main food source is other insects that fall onto water struggling to escape from water surface. Oh wait, other insects cannot easily escape or move on water surface, while it is a playground for water striders? Why are these water striders able to walk on water surface while some insects or humans are not?

Water strider is one of the example to introduce `surface tension` in science textbook for middle or high school students. One of the other good example of surface tension is a floating metalic needle on water surface. Although any metal (except for 3 metals in 1st group: Lithium, Sodium, Potassium. Even if they are denser than water, they would just "explode" instead of "floating".) is denser than water, it can stay on water surface thanks to surface tension of water.

Actually, there are some animals besides water striders able to kick water

<div class="video-wrapper">
  <div class="video-container">
    <iframe 
      src="https://www.youtube.com/embed/2tlHBxJS5ac" 
      frameborder="0" 
      allowfullscreen>
    </iframe>
  </div>
</div>

<style>
.video-wrapper {
  width: 50%;
  margin: 2rem auto;
}
.video-container {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 aspect ratio */
  height: 0;
  overflow: hidden;
}
.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>

{% include post_image.liquid
  filename="tension_molecule.jpg"
  alt="Surface tension"
  max_width="500px"
  width="50%"
  loading="eager"
  centered="true"
  figure_num="2"
  caption="Molecules in the bulk and at the liquid/gas interface. While the one in the bulk is in the presence of isotropic interactions with adjacent molecules, the one at the interface is in the absence of half its cohesive interactions."
%}

Molecules in a liquid state attract each other with forces stronger than thermal agitation. In the bulk of the liquid, these interactions are isotropic, meaning a molecule experiences equal forces from all neighboring molecules, resulting in a net force of zero. However, a molecule at the surface loses half of its cohesive interactions as depicted in `Fig. 2` To compensate for this loss, the liquid surface adjusts its shape to minimize surface area, which is the fundamental cause of surface tension.

When a liquid molecule is positioned at the surface, it experiences an unfavorable energy state. Within the liquid, if the cohesion energy per molecule is U, a molecule at the surface lacks approximately half of this energy, or $$U/2$$. Surface tension quantifies this energy deficit per unit area. Given the molecular size a and its exposed surface area $$a^2$$, the surface tension can be estimated as $$\gamma=U/2a^2$$.

In my favorite book,
