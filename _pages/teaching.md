---
layout: page
title: teaching
permalink: /teaching/
description: Collection of the current and previous classes taught by Alexander Heinlein.
nav: true
---

<div class="teaching">
<h2 class="category">open master projects</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "thesis" %}
      {% include theses.html %}
    {% endif %}
  {% endfor %}
</div>

<!-- + [Parallel Multiplicative One-Level Schwarz Preconditioners With FROSch and Trilinos]({{ site.baseurl }}{% link /assets/pdf/thesis_projects/2021-heinlein-frosch_multiplicative_coloring.pdf %}){:target="_blank"} ([Sandia](https://www.sandia.gov/){:target="_blank"})
+ [Overlapping Schwarz Domain Decomposition Methods for Implicit Ocean Models]({{ site.baseurl }}{% link /assets/pdf/thesis_projects/2021-heinlein_thies-frosch_ocean.pdf %}){:target="_blank"} ([Institute for Marine and Atmospheric Modeling](https://www.uu.nl/en/research/institute-for-marine-and-atmospheric-research-imau){:target="_blank"}); Co-Supervisor: Jonas Thies (TU Delft, Numerical Analysis)
+ [Reduced Order Models for Fluid Flow With Generative Adversarial Networks (GANs)]({{ site.baseurl }}{% link /assets/pdf/thesis_projects/2021-heinlein-gan_pdes.pdf %}){:target="_blank"}
+ [Block Preconditioners for Monolithic Solvers of Very Large Floating Structures]({{ site.baseurl }}{% link /assets/pdf/thesis_projects/2021-heinlein_colomes-block_preconditioners_floating_structures.pdf %}){:target="_blank"} ([Mocean](https://www.mocean-offshore.com){:target="_blank"}); Co-Supervisor: Oriol Colomés (TU Delft, Offshore Engineering) -->

<h2 class="category">active</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "active" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

<h2 class="category">archive</h2>
<div class="grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.category == "archive" %}
      {% include courses.html %}
    {% endif %}
  {% endfor %}
</div>

</div>
