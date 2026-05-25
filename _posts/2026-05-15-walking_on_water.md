---
layout: post
title: Walking on Water
date: 2026-05-15
description: How do water striders walk on water?
tags: knowledge science
categories: 
image_path: assets/img/post/2026-05-15-walking_on_water
thumbnail: assets/img/post/2026-05-15-walking_on_water/waterstrider.jpg
---

## Walking on water?

Have you ever seen water striders floating effortlessly on a puddle after the rain? Found on almost every continent, these insects primarily feed on other bugs that fall onto the water and struggle to escape. For most insects, the water's surface is like a swamp—once trapped, it is nearly impossible to move or escape. Yet, for the water strider, it is a free-roaming playground. Why is it that the water strider can "walk on water" while other insects or humans cannot?

<div style="margin-bottom: 4rem;"></div>

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

<div style="margin-bottom: 4rem;"></div>

While there are many factors at play, the funadamental requirement for walking on water is offsetting gravity (body weight). Without this, one simply sinks. Many textbooks oversimplify this fundamental principle by stating, "The high surface tension of water allows the water strider to float." While not entirely wrong, surface tension alone is an insufficient explanation. Why? If surface tension were the only factor, every organism with a mass similar to or smaller than a water strider should be able to float. However, we know from experience that this is not the case.

In my opinion, three primary factors enable water striders to stay afloat:

1. Surface tension of water
2. Hydrophobic (water-repellent) surface
3. Wide contact area

We will explore the surface tension in depth later, but the essential principle is that surface tension creates a pressure difference between internal and external pressures, $\Delta P = p_i-p_o$, across any curved interface. This is governed by the Young-Laplace equation. Named after the British scientist Thomas Young and the French scientist Pierre-Simon Laplace, the fundamental relationship is:

$$
\Delta P = \gamma \left( \frac{1}{R_1} + \frac{1}{R_2} \right),
$$

where $R_1$ and $R_2$ are radii of curvature, and $\gamma$ is the surface tension of the water.

{% include post_image.liquid
  filename="radius_of_curvature.png"
  alt="Water strider"
  max_width="100px"
  width="30%"
  loading="eager"
  centered="true"
  figure_num="2"
  caption="A schematic illustraiton of the radius of curvature: $R$, the radius of the contact area: $r$, the contact angle: $\theta$, and internal and external pressures: $p_i$ and $p_o$."
%}

With $R_1 = R_2 = r/\cos{\theta}$, the equation turns into:

$$
\Delta P = \frac{2\gamma \cos{\theta}}{r}.
$$

Here, $r$ is the radius of the cross-section in contact with the water, and $\theta$ is the contact angle between the water and the solid surface. The force resulting from this Young-Laplace pressure, $F_s$, is the pressure multiplied by the contact area (A):

$$
F_s = \Delta P A = \frac{2\gamma \cos{\theta}}{r}A.
$$

Earlier, I mentioned three most important factors for water striders, and we have all these three in the equation with the surface of water: $\gamma$, the area: $A$, and the hydrophobicity: $\cos{\theta}<0$. Having the surface "hydrophobic" is very important. As shown in the figure below, if the surface is hydrophobic ($\theta > 90^\circ$), $F_s$ acts in the opposite direction of gravity, effectively canceling it out. Conversely, if the surface is hydrophilic ($\theta < 90^\circ$), $F_s$ acts in the same direction as gravity, causing the forces to overlap downwards. If a hydrophilic object is seen floating, it is likely staying afloat due to buoyancy rather than surface forces.

<div style="margin-bottom: 4rem;"></div>

{% include post_image.liquid
  filename="Laplace_force.png"
  alt="Surface force acting on a solid body"
  max_width="700px"
  width="70%"
  loading="eager"
  centered="true"
  figure_num="3"
  caption="An example of the difference of the surface force between hydrophobic and hydrophilic surfaces."
%}

I would also like to briefly address <u>the effect of soap</u>. You may have seen or learned that water striders can no longer stay afloat if soap is added. This is because soap (a surfactant or surfactants), which consists molecules with one side hydrophilic and the other hydrophobic, adsorbs onto both the water strider's legs and water/air interface. Consequently, the legs—originally hydrophobic—become coated with soap molecules that bridge with the water, thereby reducing the contact angle to $\theta < 90^{\circ}$. To make matters worse, the soap simultaneously lowers the surface tension of the water. So, what I would like to point out is that <u>the decrease in the contact angle</u> is the primary factor, while the decrease in surface tension is secondary.

<div style="margin-bottom: 4rem;"></div>

Before warping up, I want to lastly address this question: "can animals much larger than water striders walk on water?" My answer is: Yes, of course it is possible—provided <u>they can strike the water "hard" enough, a force equivalent to gravity.</u> A prime example is the Basilisk lizard, also known as the "Jesus Christ lizard." Because the gravitational force ($F_g$) acting on this lizard is much larger than the surface tension force ($F_s$), it cannot stand still on water like a water strider. Instead, it must continuously strike the water to stay afloat. Let's watch this nice video:

<div style="width: 70%; margin: auto;">
  <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
    <iframe
      src="https://www.youtube.com/embed/tayZBgQki5g"
      style="position: absolute; top:0; left:0; width:100%; height:100%;"
      frameborder="0"
      allowfullscreen>
    </iframe>
  </div>
</div>

<div style="margin-bottom: 4rem;"></div>

What happens here is that this lizard kicks the water really hard within a very short time (impulse), and as a result, an air pocket forms inside the water. The lizard must pull its foot out before the air pocket closes and immediately repeat the action with the other foot to offset gravity. According to the research by Glasheen and McMahon [1], the power required to apply this instantaneous force is approximately $29~\mathrm{W/kg}$. Considering that a top-tier human athlete produces about $20~\mathrm{W/kg}$ when running uphill, it seems impossible for humans to walk on water.

Just to give you an idea how high this power is: assuming the average weight of the athelets 80 kg, they produced 1600 W, which is more than 2 horse power. One horse power is about 740 W.

**Author's note on this:**
However, just as stated in the bible that Jesus walked on water, perhaps <u>the reason we cannot do so is simply that we lack the strength?</u> 😏

<div style="margin-bottom: 6rem;"></div>

### References

[1] Glasheen, J. W., & McMahon, T. A. (1996). A hydrodynamic model of locomotion in the basilisk lizard. Nature, 380(6572), 340-342.
