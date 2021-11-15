---
layout: page
title: software
permalink: /software/
description: A compilation of software projects Alexander Heinlein is contributing to.
nav: false
---

<div class="software grid">

  {% assign sorted_software = site.software | sort: "importance" %}
  {% for software in sorted_software %}
  <div class="grid-item">
    {% if software.redirect %}
      {% unless software.nolink %}
        <a href="{{ software.redirect }}" target="_blank">
      {% endunless %}  
    {% else %}
      {% unless software.nolink %}
        <a href="{{ software.url | relative_url }}">
      {% endunless %}    
    {% endif %}
    {% if software.nolink %}
      <div class="card">
    {% else %}
      <div class="card hoverable">
    {% endif %}
        {% if software.img %}
        <div class="row no-gutters">
          <div class="col-md-2">
            <img src="{{ software.img | relative_url }}" class="card-img" alt="software thumbnail">
          </div>        
          <div class="col-md-10">
            <div class="card-body">
              <h4 class="card-title">{{ software.title }}</h4>
              <p class="card-text">{{ software.description }}</p>
            </div>
          </div>
        </div>
        {% else %}
        <div class="card-body">
          <h4 class="card-title">{{ software.title }}</h4>
          <p class="card-text">{{ software.description }}</p>              
        </div>
        {% endif %}
      </div>
    {% unless software.nolink %}
      </a>
    {% endunless %}
  </div>
{% endfor %}

</div>
