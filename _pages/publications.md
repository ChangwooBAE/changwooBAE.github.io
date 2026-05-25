---
layout: page
permalink: /publications/
title: publications
description: 
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->


<div class="publications">

  <!-- 1. Search Bar (if you want it between sections or at the top) -->

{% include bib_search.liquid %}

  <div style="margin-top: 5rem; margin-bottom: 2rem;"></div>

  <!-- 2. All other Publications -->
  <h2 class="category font-weight-bold">Journal Articles</h2>
  {% bibliography --query @article | @unpublished %}
  <!-- {% bibliography --query @ %} -->
  
  <div style="margin-top: 5rem; margin-bottom: 2rem;"></div>

  <!-- 3. Thesis Section -->
  <h2 class="category font-weight-bold">Thesis</h2>
  {% bibliography --query @phdthesis %}

</div>
