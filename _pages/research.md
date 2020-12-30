---
layout: page
title: research
permalink: /research/
description: Collection of Alexander Heinlein's research topics.
nav: true
---

<div class="research grid">

  {% assign sorted_research = site.research | sort: "importance" %}
  {% for research in sorted_research %}
  <div class="grid-item">
    {% if research.redirect %}
      {% unless research.nolink %}
        <a href="{{ research.redirect }}" target="_blank">
      {% endunless %}  
    {% else %}
      {% unless research.nolink %}
        <a href="{{ research.url | relative_url }}">
      {% endunless %}    
    {% endif %}
    {% if research.nolink %}
      <div class="card">
    {% else %}
      <div class="card hoverable">
    {% endif %}
        {% if research.img %}
        <div class="row no-gutters">
          <div class="col-md-2">
            <img src="{{ research.img | relative_url }}" class="card-img" alt="research thumbnail">
          </div>        
          <div class="col-md-10">
            <div class="card-body">
              <h4 class="card-title">{{ research.title }}</h4>
              <p class="card-text">{{ research.description }}</p>
            </div>
          </div>
        </div>
        {% else %}
        <div class="card-body">
          <h4 class="card-title">{{ research.title }}</h4>
          <p class="card-text">{{ research.description }}</p>              
        </div>
        {% endif %}
      </div>
    {% unless research.nolink %}
      </a>
    {% endunless %}
  </div>
{% endfor %}

</div>

<!-- <div class="research grid">

  {% assign sorted_research = site.research | sort: "importance" %}
  {% for project in sorted_research %}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h4 class="card-title text-lowercase">{{ project.title }}</h4>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if project.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ project.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div> -->
