---
layout: page
title: Research
permalink: /research/
description: 
nav: true
nav_order: 1
display_categories: [current, past]
horizontal: false
---
Today, robotics and autonomous systems have been increasingly used in various areas such as manufacturing, military, agriculture, medical sciences, and environmental monitoring. However, most of these systems are fragile and vulnerable to adversarial attacks and uncertain environmental conditions. In most cases, even if a part of the system fails, the entire system performance can be significantly undermined. As robots start to coexist with humans, we need algorithms that can be trusted under real-world (not just ideal) conditions. To this end, our research focuses on enabling **security, trustworthiness, and long-term autonomy** in robotics and autonomous systems. We devise _efficient coordination algorithms with rigorous theoretical guarantees_ to make robots resilient to attacks and aware of the loss from uncertainty. Our long-term goal is to investigate **secure, reliable, and scalable multi-robot autonomy** when robots use data-driven machine learning techniques in the areas of **cyber-physical systems, the Internet of Things, precision agriculture, and smart cities**.

[Current Robotics Reports](https://link.springer.com/article/10.1007/s43154-021-00046-5): a survery of multi-robot coordination and planning in uncertain and adversarial environments.


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
