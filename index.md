---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Yeowga!
subtitle: ouch.. back pain
---
<div class="posts-list text-center">
  {% for section in site.data.toc.sections %}
  <article class="post-preview">
    <a href="pages/{{ section.name }}">
      <h2 class="post-title">{{ section.name }}</h2>
    </a>
    {% if section.subsections %}
      {% for subsection in section.subsections %}
      <a href="pages/{{ section.name }}/{{ subsection }}">
        <h3 class="post-subtitle">{{ subsection }}</h3>
      </a>
      {% endfor %}
    {% endif %}
  </article>
  {% endfor %}
</div>
