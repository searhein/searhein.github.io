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
    <td><a href="#published">journal publications: {% bibliography_count -f papers --query @article[keywords ~= published] %}</a></td>
    <td><a href="#published">book chapters and conference proceedings: {% bibliography_count -f papers --query @inproceedings[keywords ~= published] %}</a></td>
    <td><a href="#phdthesis">phd thesis: {% bibliography_count -f papers --query @phdthesis[keywords ~= published] %}</a></td>    
    <td><a href="#accepted">accepted: {% bibliography_count -f papers --query @*[keywords ~= accepted] %}</a></td>
    <td><a href="#submitted">submitted: {% bibliography_count -f papers --query @*[keywords ~= submitted] %}</a></td>
  </tr>
</table>

{% if page.selected_papers %}
  {% include selected_papers.html %}
{% endif %}

<p id="published">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers --query @article[year={{y}}, keywords ~= published]* %}
  {% bibliography -f papers --query @inproceedings[year={{y}}, keywords ~= published]* %}
{% endfor %}
</p>

<p id="phdthesis">
<h2 class="year">phd thesis</h2>
{% bibliography -f papers --query @phdthesis[keywords ~= published]* %}
</p>

<p id="accepted">
<h2 class="year">accepted</h2>
{% bibliography -f papers --query @*[keywords ~= accepted]* %}
</p>

<p id="submitted">
<h2 class="year">submitted</h2>
{% bibliography -f papers --query @*[keywords ~= submitted]* %}
</p>

</div>
