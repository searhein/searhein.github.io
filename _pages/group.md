---
layout: page
title: group
permalink: /group/
description:
nav: true
nav_order: 1
display_categories: [phd candidates, master students, bachelor students, former members]
horizontal: false
---

<!-- pages/group_members.md -->
<div class="group_members">
  <h2 class="category"></h2>
  {%- assign categorized_group_members = site.group_members | where: "category", "lead" -%}
  {%- assign sorted_group_members = categorized_group_members | sort: "last_name" %}
  {% if page.horizontal -%}
<div class="container">
  <div class="row row-cols-2">
  {%- for group_member in sorted_group_members -%}
    {% include group_members_horizontal.html %}
  {%- endfor %}
  </div>
</div>
{%- else -%}
<div class="grid">
  {%- for group_member in sorted_group_members -%}
    {% include group_members.html %}
  {%- endfor %}
</div>
{%- endif -%}
{%- if site.enable_group_categories and page.display_categories %}
  <!-- Display categorized group_members -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_group_members = site.group_members | where: "category", category -%}
  {%- assign sorted_group_members = categorized_group_members | sort: "last_name" %}
  <!-- Generate cards for each group_member -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for group_member in sorted_group_members -%}
      {% include group_members_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for group_member in sorted_group_members -%}
      {% include group_members.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display group_members without categories -->
  {%- assign sorted_group_members = site.group_members | sort: "importance" -%}
  <!-- Generate cards for each group_member -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for group_member in sorted_group_members -%}
      {% include group_members_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for group_member in sorted_group_members -%}
      {% include group_members.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
