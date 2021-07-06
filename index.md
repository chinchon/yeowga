---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
# title: Yeowga!
# subtitle: ouch.. back pain
---
<div class="posts-list text-center">
  {% for section in site.data.toc.sections %}
  <article class="post-preview">
    {% assign section_name_link = section.name | downcase | replace: ' ', '-' | replace: '/', '-' %}
    <a href="pages/{{ section_name_link }}">
      <h2 class="post-title">{{ section.name }}</h2>
    </a>
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
  {% endfor %}
</div>

<!-- 
TODO: make search center and focus
TODO: add content 
TODO: add thumnails to homepage, stronger call to action
-->