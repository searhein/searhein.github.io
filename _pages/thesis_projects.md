---
layout: page
title: thesis projects
permalink: /thesis_projects/
description: Collection of master projects supervised by Alexander Heinlein.
nav: false
---

<div class="teaching">
<h2 class="category">ongoing master projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "thesis" and teaching.status == "ongoing" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">open master projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "thesis" and teaching.status == "open" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">archive master projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "thesis" and teaching.status == "archive" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

</div>
