---
layout: page
permalink: /talks/
title: talks
description: Alexander Heinlein's talks in reversed chronological order.
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014]
nav: true
# selected_talks: false # includes a list of talks marked as "selected={true}"
---

<div class="publications">

{% if page.selected_papers %}
  {% include selected_papers.html %}
{% endif %}

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f talks --query @misc[year={{y}}]* %}
{% endfor %}

</div>
