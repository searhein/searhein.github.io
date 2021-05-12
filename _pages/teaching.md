---
layout: page
title: teaching
permalink: /teaching/
description: Collection of the current and previous classes taught by Alexander Heinlein.
nav: true
---

<h2>open master projects</h2>

+ [Parallel Multiplicative One-Level Schwarz Preconditioners With FROSch and Trilinos]({{ site.baseurl }}{% link /assets/pdf/thesis_projects/2021-heinlein-frosch_multiplicative_coloring.pdf %}){:target="_blank"} ([Sandia](https://www.sandia.gov/){:target="_blank"})
+ [Overlapping Schwarz Domain Decomposition Methods for Implicit Ocean Models]({{ site.baseurl }}{% link /assets/pdf/thesis_projects/2021-heinlein_thies-frosch_ocean.pdf %}){:target="_blank"} ([Institute for Marine and Atmospheric Modeling](https://www.uu.nl/en/research/institute-for-marine-and-atmospheric-research-imau){:target="_blank"})
+ [Reduced Order Models for Fluid Flow With Generative Adversarial Networks (GANs)]({{ site.baseurl }}{% link /assets/pdf/thesis_projects/2021-heinlein-gan_pdes.pdf %}){:target="_blank"}

<h2>current teaching</h2>
<div class="teaching grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% unless teaching.archive %}
    <div class="grid-item">
      {% if teaching.redirect %}
        {% unless teaching.nolink %}
         <a href="{{ teaching.redirect }}" target="_blank">
        {% endunless %}
      {% else %}
        {% unless teaching.nolink %}
          <a href="{{ teaching.url | relative_url }}">
        {% endunless %}
      {% endif %}
        {% if teaching.nolink %}
          <div class="card">
        {% else %}
          <div class="card hoverable">
        {% endif %}  
          <div class="row no-gutters">
            <div class="col-md-4">          
              <div class="card-header {{ teaching.university }}">
                {% if teaching.university == "ude" %}
                  <p class="card-text">University of Duisburg-Essen</p>
                {% endif %}
                {% if teaching.university == "uzk" %}
                  <p class="card-text">University of Cologne</p>
                {% endif %}
                {% if teaching.university == "ust" %}
                  <p class="card-text">University of Stuttgart</p>
                {% endif %}
                {% if teaching.university == "tud" %}
                  <p class="card-text">TU Delft</p>
                {% endif %}
                <p class="card-text">{{ teaching.semester }}</p>
              </div>
            </div>
            <div class="col-md-8">
              <div class="card-body">
                <p class="card-title">{{ teaching.title }}</p>
                <!-- <p class="card-text">{{ teaching.description }}</p>               -->
              </div>
            </div>
          </div>
        </div>
      {% unless teaching.nolink %}
        </a>
      {% endunless %}
    </div>
    {% endunless %}
  {% endfor %}
</div>

<h2>archive</h2>
<div class="teaching grid">
  {% assign sorted_teaching = site.teaching | sort: "runningindex" | reverse %}
  {% for teaching in sorted_teaching %}
    {% if teaching.archive == true %}
    <div class="grid-item">
      {% if teaching.redirect %}
        {% unless teaching.nolink %}
          <a href="{{ teaching.redirect }}" target="_blank">
        {% endunless %}
      {% else %}
        {% unless teaching.nolink %}
          <a href="{{ teaching.url | relative_url }}">
        {% endunless %}
      {% endif %}
        {% if teaching.nolink %}
          <div class="card">
        {% else %}
          <div class="card hoverable">
        {% endif %}        
          <div class="row no-gutters">
            <div class="col-md-4">          
              <div class="card-header {{ teaching.university }}">
                {% if teaching.university == "ude" %}
                  <p class="card-text">University of Duisburg-Essen</p>
                {% endif %}
                {% if teaching.university == "uzk" %}
                  <p class="card-text">University of Cologne</p>
                {% endif %}
                {% if teaching.university == "ust" %}
                  <p class="card-text">University of Stuttgart</p>
                {% endif %}              
                <p class="card-text">{{ teaching.semester }}</p>
              </div>
            </div>
            <div class="col-md-8">
              <div class="card-body">
                <p class="card-title">{{ teaching.title }}</p>
                <!-- <p class="card-text">{{ teaching.description }}</p>               -->
              </div>
            </div>
          </div>
        </div>
      {% unless teaching.nolink %}
        </a>
      {% endunless %}
    </div>
    {% endif %}
  {% endfor %}
</div>
