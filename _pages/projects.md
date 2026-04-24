---
title:
layout: default
permalink: /projects/
published: true
---

<h2 class="page-title">Projects &amp; Research</h2>

<ul class="pub-list">
{% for project in site.projects %}
  {% if project.redirect %}
  <li>
    <a class="pub-item" href="{{ project.redirect }}" target="_blank">
      <div class="pub-body">
        <p class="pub-title">{{ project.title }}</p>
        <p class="pub-venue">{{ project.description }}</p>
      </div>
      <span class="pub-arrow"><i class="fas fa-arrow-up-right-from-square"></i></span>
    </a>
  </li>
  {% else %}
  <li>
    <a class="pub-item" href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
      <div class="pub-body">
        <p class="pub-title">{{ project.title }}</p>
        <p class="pub-venue">{{ project.description }}</p>
      </div>
      <span class="pub-arrow"><i class="fas fa-chevron-right"></i></span>
    </a>
  </li>
  {% endif %}
{% endfor %}
</ul>
