---
layout: page
title: bachelor thesis projects
permalink: /bachelor_thesis_projects/
description: Collection of bachelor projects supervised by Alexander Heinlein.
nav: false
---

<div class="teaching">
<h2 class="category">ongoing bachelor projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "bachelor_thesis" and teaching.status == "ongoing" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">open bachelor projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "bachelor_thesis" and teaching.status == "open" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">archive bachelor projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "bachelor_thesis" and teaching.status == "archive" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

</div>
