---
layout: page
title: Research
permalink: /projects/
description: A growing collection of our cool projects.
nav: true
nav_order: 2
display_categories: [Materials Sciences , AI & methods]
horizontal: false
---
****
# Research  Expertise
- Computational chemistry
- AI & Machine Learning
- Materials Sciences, electrochemistry and surface sciences
- Nonlinear Optics,
- Vibrational and Electronic Spectroscopies
- First Principle Calculations, Molecular Dynamics
- Monte Carlo Simulation, Microkinetic Modeling
- High performance computing and software development
- Data solutions for sciences



****
# Research  Interests
- Accelerating Materials Discovery with AI
    - High entropy alloys
    - Mixed metal oxides
- Computational design of Innovative Materials
    - Gas sensors for breath diagnosis
    - Storing Hydrogen in Metal Hydrides
    - Solid-state batteries
    - Na-ion batteries
    - Electroreduction of nitrogen to ammonia
- Deep Learning
    - Graph Neural Network
    - Generative Model
    - Dynamics systems
    - Representations of molecules and materials for ML  

- Data solutions for sciences
    - Facilitate and standardize new innovative data solutions for science
    - Building agile and flexible digital infrastructure to allow autonomy and scalability



****
# Projects

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
