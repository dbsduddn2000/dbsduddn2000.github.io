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
  {% assign tag_filter = tag_parts[1] | downcase | strip | remove: '"' | remove: '&quot;' %}
{% endif %}

## Ongoing Projects

{% include list.html component="card" data="project" filter="group == 'ongoing'" tag_filter=tag_filter %}

{% include section.html %}

## Completed Projects

{% include list.html component="card" data="project" filter="group == 'completed'" tag_filter=tag_filter style="small" %}
