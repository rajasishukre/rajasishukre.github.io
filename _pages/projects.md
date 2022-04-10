---
layout: page
title: projects
permalink: /projects/
description:  
nav: true
display_categories: [work, fun]
horizontal: false
---

My PhD thesis at TTU is centered on the multifaceted field of adsorption in 3D porous materials such as MOFs, zeolites, and carbon-based materials such as exfoliated graphite and graphitized carbon black. Adsorption-based technologies for chemical separations have higher energy efficiency than distillation-based processes which are the long-standing industrial norm. Thus, to reduce the energy consumption of chemical separations, it is extremely important to understand the adsorption phenomenon of various chemicals on different substrates at the molecular level using tools like MD and MC. There are twofold advantages to such an analysis: 1) the prediction of parameters of thermodynamic models, enabling global optimization of adsorption processes 2) Design of functionalized materials with specific adsorption sites. Alongside the computational study of adsorption phenomenon, it is also equally important to engineer continuous manufacturing techniques for the synthesis of novel adsorbents which have been produced only at the lab-scale. Towards this front, I have developed a reusable, droplet-based millifluidic reactor for the continuous synthesis of high-quality MOFs within minutes. Relying on the principles of process intensification, such single millifluidic reactors can be numbered-up to increase the throughput, while decreasing the consumption of expensive solvents. I have also developed an engineering thermodynamic model that can aid in process simulation of adsorption of liquid mixtures. Please click on the individual project tabs for a more detailed description.

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
