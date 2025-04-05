---
layout: page
title: internships
permalink: /internships/
description: Annoucements of internships.
nav: false
---

<div class="teaching">

<h2 class="category">open internships</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "internship" and teaching.status == "open" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">ongoing internships</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "internship" and teaching.status == "ongoing" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">archive internships</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "internship" and teaching.status == "archive" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

</div>
