---
title: Projects
nav:
  order: 4
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Projects

{% include tags.html %}

{% include section.html %}

{% assign search_param = page.url | split: '?' | last | uri_decode %}
{% assign tag_filter = "" %}
{% if search_param contains "tag:" %}
  {% assign tag_parts = search_param | split: "tag:" %}
  {% assign tag_filter = tag_parts[1] | downcase | strip | replace: '"', '' %}
{% endif %}

## Ongoing Projects

{% if tag_filter != "" %}
  {% include list.html component="card" data="projects" filter="group == 'ongoing' and tags contains tag_filter" %}
{% else %}
  {% include list.html component="card" data="projects" filter="group == 'ongoing'" %}
{% endif %}

{% include section.html %}

## Completed Projects

{% if tag_filter != "" %}
  {% include list.html component="card" data="projects" filter="group == 'completed' and tags contains tag_filter" style="small" %}
{% else %}
  {% include list.html component="card" data="projects" filter="group == 'completed'" style="small" %}
{% endif %}
