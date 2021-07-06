---
layout: page
subtitle: null
title: SUPINE POSES
---

<div class="posts-list text-center">
  {% for section in site.data.toc.sections %}
  {% if section.name == page.title %}
  <article class="post-preview">
    {% assign section_name_link = section.name | downcase | replace: ' ', '-' | replace: '/', '-' %}
      {% if section.subsections %}
      {% for subsection in section.subsections %}
      {% assign subsection_name_link = subsection.name | downcase | replace: ' ', '-' | replace: '/', '-' %}
      <a href="/pages/{{ section_name_link }}/{{ subsection_name_link }}">
          <!-- <h3 class="post-subtitle">{{ subsection.name }}{{ subsection.description }}</h3> -->
          <h3 class="post-subtitle">{{ subsection.name }}{% if subsection.description %} - {% endif %}{{ subsection.description }}</h3>
      </a>
      {% endfor %}
      {% endif %}
  </article>
  {% endif %}    
  {% endfor %}
</div>
