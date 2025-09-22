---
layout: page
title: honors projects
permalink: /honors/
description: Collection of honors projects supervised by Alexander Heinlein.
nav: false
---

<div class="teaching">

<h2 class="category">open honors projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "honors" and teaching.status == "open" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">ongoing honors projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "honors" and teaching.status == "ongoing" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">archive honors projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "honors" and teaching.status == "archive" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

</div>
