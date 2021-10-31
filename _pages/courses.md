---
layout: page
title: courses
permalink: /courses/
description: Collection of courses taught by Alexander Heinlein.
nav: false
---

<div class="teaching">
<h2 class="category">ongoing courses</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "course" and teaching.status == "ongoing" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">planned courses</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "course" and teaching.status == "planned" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">archive courses</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "course" and teaching.status == "archive" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

</div>
