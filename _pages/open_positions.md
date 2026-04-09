---
layout: page
title: open positions
permalink: /open_positions/
description: Current openings in the group.
nav: false
---

<div class="teaching">

<p>
  This page collects the currently advertised opportunities in the group.
  Each entry links to a project description or the corresponding external posting when available.
</p>

{% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
{% assign open_master_projects = sorted_teaching | where: "category", "master_thesis" | where: "status", "open" %}
{% assign open_internships = sorted_teaching | where: "category", "internship" | where: "status", "open" %}
{% assign open_honors_projects = sorted_teaching | where: "category", "honors" | where: "status", "open" %}
{% assign open_bachelor_projects = sorted_teaching | where: "category", "bachelor_thesis" | where: "status", "open" %}

{% if open_master_projects.size > 0 %}
<h2 class="category">open master thesis projects</h2>
<div class="grid">
  {% for teaching in open_master_projects %}
    {% include theses.html %}
  {% endfor %}
</div>
{% endif %}

{% if open_internships.size > 0 %}
<h2 class="category">open internships</h2>
<div class="grid">
  {% for teaching in open_internships %}
    {% include theses.html %}
  {% endfor %}
</div>
{% endif %}

{% if open_honors_projects.size > 0 %}
<h2 class="category">open honors projects</h2>
<div class="grid">
  {% for teaching in open_honors_projects %}
    {% include theses.html %}
  {% endfor %}
</div>
{% endif %}

{% if open_bachelor_projects.size > 0 %}
<h2 class="category">open bachelor thesis projects</h2>
<div class="grid">
  {% for teaching in open_bachelor_projects %}
    {% include theses.html %}
  {% endfor %}
</div>
{% endif %}

{% if open_master_projects.size == 0 and open_internships.size == 0 and open_honors_projects.size == 0 and open_bachelor_projects.size == 0 %}
<p>
  There are currently no advertised openings. If you are interested in joining the group,
  feel free to get in touch directly.
</p>
{% endif %}

</div>
