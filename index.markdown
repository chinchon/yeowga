---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
description: back pain goes away
---
<a href="/">home</a>
{% for section in site.data.toc.sections %}
<details open>
  <summary><a href="{{ section.name }}">{{ section.name }}</a></summary>
  <ul style="padding-left:40px">
  {% for subsection in section.subsections %}
  <li><a href="{{ section.name }}/{{ subsection }}">{{ subsection }}</a></li>
  {% endfor %}
  </ul>
</details>
{% endfor %}