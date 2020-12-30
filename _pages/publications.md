---
layout: page
permalink: /publications/
title: publications
description: Alexander Heinlein's publications in reversed chronological order.
years: [2020, 2019, 2018, 2017, 2016, 2015, 2014]
nav: true
selected_papers: false # includes a list of papers marked as "selected={true}"
---

<div class="publications">

<table style="width:100%">
  <tr>
    <td><a href="#published">journal publications: {% bibliography_count -f papers --query @article[group=published] %}</a></td>
    <td><a href="#published">book chapters and conference proceedings: {% bibliography_count -f papers --query @inproceedings[group=published] %}</a></td>
    <td><a href="#phdthesis">phd thesis: {% bibliography_count -f papers --query @phdthesis[group=published] %}</a></td>    
    <td><a href="#accepted">accepted: {% bibliography_count -f papers --query @*[group=accepted] %}</a></td>
    <td><a href="#submitted">submitted: {% bibliography_count -f papers --query @*[group=submitted] %}</a></td>
  </tr>
</table>

{% if page.selected_papers %}
  {% include selected_papers.html %}
{% endif %}

<p id="published">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @article[year={{y}}, group=published]* %}
  {% bibliography -f papers -q @inproceedings[year={{y}}, group=published]* %}
{% endfor %}
</p>

<p id="phdthesis">
<h2 class="year">phd thesis</h2>
{% bibliography -f papers -q @phdthesis[group=published]* %}
</p>

<p id="accepted">
<h2 class="year">accepted</h2>
{% bibliography -f papers -q @*[group=accepted]* %}
</p>

<p id="submitted">
<h2 class="year">submitted</h2>
{% bibliography -f papers -q @*[group=submitted]* %}
</p>

</div>
