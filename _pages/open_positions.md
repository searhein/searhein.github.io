---
layout: page
title: open positions
permalink: /open_positions/
description: 
nav: false
---

<div class="teaching">

{% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
{% assign open_phd_positions = sorted_teaching | where: "category", "phd_position" | where: "status", "open" %}
{% assign open_postdoc_positions = sorted_teaching | where: "category", "postdoc_position" | where: "status", "open" %}

{% if open_phd_positions.size > 0 %}
<h2 class="category">open PhD positions</h2>
<div class="grid">
  {% for teaching in open_phd_positions %}
    {% include theses.html %}
  {% endfor %}
</div>
{% endif %}

{% if open_postdoc_positions.size > 0 %}
<h2 class="category">open postdoc positions</h2>
<div class="grid">
  {% for teaching in open_postdoc_positions %}
    {% include theses.html %}
  {% endfor %}
</div>
{% endif %}

{% if open_phd_positions.size == 0 and open_postdoc_positions.size == 0 %}
<p>There are currently no open PhD and postdoc positions.</p>
{% endif %}

</div>
