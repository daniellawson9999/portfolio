---
layout: about
title: about
permalink: /
subtitle: #<a href='#'>Affiliations</a>. Address. Contacts. Moto. Etc.
years: [2023,2022]
profile:
  align: right
  #image: prof_pic.jpg
  image: me-crop.jpg
  image_circular: false # crops the image to make it circular
  # address: >
  #   <p>555 your office number</p>
  #   <p>123 your address street</p>
  #   <p>Your City, State 12345</p>

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---

Hi, I'm Daniel. I'm currently a senior at Purdue University. I am generally interested in machine learning and reinforcement learning. Currently, I am doing research with [Ahmed Qureshi](https://qureshiahmed.github.io/) in the [Cognitive Robot Autonomy & Learning Lab](https://corallab.net/) related to robotics.

contact: daniellawson9999 (at) gmail.com


<br>
<br>


## Papers

<!-- _pages/publications.md -->

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
Other work can be found [here](https://scholar.google.com/citations?user=yboVGIIAAAAJ).

<br>

## Highlighted Projects 
Additional projects can be found on my [GitHub](https://github.com/daniellawson9999).
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

<br>

### Paper Implementations
- [Online Decision Transformer](https://github.com/daniellawson9999/online-decision-transformer)


