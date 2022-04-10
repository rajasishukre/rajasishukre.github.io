---
layout: page
title: projects
permalink: /projects/
description:  
nav: true
display_categories: [work, fun]
horizontal: false
---

My PhD thesis at TTU is centered on the multifaceted field of adsorption in 3D porous materials such as MOFs, zeolites, and carbon-based materials such as exfoliated graphite and graphitized carbon black. Adsorption-based technologies for chemical separations have higher energy efficiency than distillation-based processes which are the long-standing industrial norm. Thus, to reduce the energy consumption of chemical separations, it is extremely important to understand the adsorption phenomenon of various chemicals on different substrates at the molecular level using tools like MD and MC. There are twofold advantages to such an analysis:
1) The prediction of parameters of thermodynamic models, enabling global optimization of adsorption processes 
2) Design of functionalized materials with specific adsorption sites. Alongside the computational study of adsorption phenomenon, it is also equally important to engineer continuous manufacturing techniques for the synthesis of novel adsorbents which have been produced only at the lab-scale. Towards this front, I have developed a reusable, droplet-based millifluidic reactor for the continuous synthesis of high-quality MOFs within minutes. Relying on the principles of process intensification, such single millifluidic reactors can be numbered-up to increase the throughput, while decreasing the consumption of expensive solvents. I have also developed an engineering thermodynamic model that can aid in process simulation of adsorption of liquid mixtures. Please click on the individual project tabs for a more detailed description.


** 1. Molecular simulations**

**Estimation of the binary interaction parameter of the aNRTL model using molecular simulations**

</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/P_197_CH4_143_t0001.png" title="Molecular simulation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Propane molecular simulation snapshot
</div>

The equilibrium molecular snapshots of gas molecules (pure component and binary mixtures) adsorbed inside the 3D pores of various adsorbents such as MOFs and zeolites as well as on the surface of exfoliated graphite are captured using simulation tools such as Molecular Dynamics and Monte Carlo simulations. The configurational and energetic landscape of the adsorbed phase generated in the simulations enables the estimation of the binary interaction parameter of the adsorption Non-Random Two-Liquid (aNRTL) model. This is a thermodynamic model, and it successfully represents both ideal and non-ideal binary gas adsorption over various adsorbent structures with low deviations in comparison to the experimental data. The adsorbed phase for a binary gas mixture can be both ideal and non-ideal, depending on the competitive interactions of the two gas molecules with the atoms of the adsorbent. This nature of the adsorbed phase is captured by the regression of the binary interaction parameter of the aNRTL model. The formulation of the model is based on the local composition theory, which is well-rooted in Statistical Thermodynamics. Thus, the molecular simulations are an ideal tool to identify the various adsorption sites and determine the specific site selectivity for a particular gas molecule, depending on the potential energy and configuration of the molecules surrounding the given site. This is an ongoing project and the manuscript will be submitted soon.


**2. Experimental**

**Batch-Screening Guided Continuous Flow Synthesis of the Metal-organic Framework HKUST-1 in a Millifluidic Droplet Reactor**
Metal-organic frameworks (MOFs) are a class of crystalline and porous adsorbents, with wide-ranging applications in gas separations, membrane materials as well as sensors. Commonly used batch synthesis techniques for MOF production are limited by low productivity, high operating costs, and slow crystallization timescales, severely impeding the large-scale manufacturing of these materials. However, batch synthesis is a useful and easy technique to screen multiple reaction parameters to find an optimal chemistry. Therefore, in this study, we have used the batch process and screened a multidimensional reaction space consisting of 45 sample variations based on the crystallinity, yield and instantaneous precipitation, which could lead to tube clogging under flow conditions. We have found one optimized reaction chemistry, that could be used in flow conditions, which in this study is a novel millifluidic droplet-based reactor for the continuous synthesis of HKUST-1 crystals. The biphasic flow in the millifluidic reactor consisted of droplets of the reactant solution, dispersed in a continuous phase of silicone oil. We investigate the differences in the quality and quantity of HKUST-1 synthesized via the continuous and batch techniques. Moreover, we have demonstrated that the HKUST-1 samples prepared via the continuous synthesis in a droplet based millifluidic reactor, at an ultra-low residence time exhibit excellent physical properties comparable to that obtained for the samples prepared by the traditional batch process. A clean, easy-to-install, and reusable millifluidic reactor presented in this work may pave the path for an economically viable, large-scale synthesis of HKUST-1.


**3. Thermodynamic modeling**

**3.1 Thermodynamic modeling of adsorption at the liquid-solid interface**

Adsorption based separation techniques are significantly energy efficient in comparison to the conventional thermal separation techniques such as distillation. Despite the extensive esearch and development activities undertaken for mixed gas adsorption, the use of adsorption techniques for the separation of multicomponent liquid mixtures is still limited. This is due to the lack of accurate adsorption thermodynamic models, which form the scientific foundation of process simulation of such systems, making the translation to the industrial scale challenging. In this work, we have rigorously computed the surface excess of adsorption for six binary liquid mixtures on silica gel at 303 K using the frameworks of the adsorbed solution theory and the generalized Langmuir isotherm model. The six binary liquid mixtures studied in this work were formed by the pair-wise combinations of four components: benzene, 1,2-dichloroethane, cyclohexane and n-heptane. We have based our calculations by considering simultaneous equilibria of three phases: saturated binary vapor phase, binary liquid phase and the adsorbed phase. The composition of the corresponding saturated vapor phase was determined by correlating the experimental vapor-liquid equilibria data using the Non-Random Two-Liquid activity coefficient model. The activity coefficients of the adsorbed phase were calculated using the adsorption Non-Random Two-Liquid activity coefficient model. Devoid of simplifying assumptions, our methodology for computing the surface excess of binary liquid adsorption should be applicable for the adsorption from a wide variety of liquid mixtures.

**3.2 Development of a thermophysical properties model for flowsheet simulation of biomass pyrolysis processes **

A properties model was developed for use in commercial process simulators to model pyrolysis of lignocellulosic biomass. The component list was chosen to enable process simulations based on a recently published lumped pyrolysis kinetics model. Since many of the compounds involved in pyrolysis are not found in simulator
databanks, estimation based on available literature data was used to establish missing parameters. Standard solid enthalpy of formation, solid heat capacity, and solid density estimates calculated from the limited experimental data available were prepared for six biomass constituents and nine intermediate and end-products of their pyrolysis. Ideal gas enthalpy of formation and heat capacity, critical property, and vapor pressure estimates were prepared for another four pyrolysis end-products and one biomass component. The estimates were all validated against the closest available experimental data in the literature. The addition of these new components and properties allows thermodynamically rigorous simulation of lumped biomass pyrolysis reactions with accurate energy balances. Enthalpies of reaction calculated from the properties model were compared with reported reaction enthalpies for the same lumped biomass pyrolysis reactions and found to be in general agreement.











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
