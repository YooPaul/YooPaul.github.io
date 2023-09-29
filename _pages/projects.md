---
title:
layout: default
permalink: /projects/
published: true
---


<div class="ProjectContainer">

	<div class="gallery">


  {% for project in site.projects %}

  {% if project.redirect %}
  <div class="projectTile">
          <a href="{{ project.redirect }}" target="_blank">
          <span>
            <figure>
              <img src="{{ project.thumbnail | prepend: '/assets/images/' | prepend: site.baseurl | prepend: site.url }}">
              <figcaption> {{project.title}}</figcaption>
            </figure>
              <!--
              <h2>{{ project.title }}</h2>
              <br/>
              <p>{{ project.description }}</p>
              -->
          </span>
          </a>
  </div>

  {% else %}

  <div class="projectTile">
          <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
            <figure>
              <img src="{{ project.thumbnail | prepend: '/assets/images/' | prepend: site.baseurl | prepend: site.url }}">
              <figcaption> {{project.title}}</figcaption>
            </figure>
              <!--
              <h2>{{ project.title }}</h2>
              <br/>
              <p>{{ project.description }}</p>
              -->
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
