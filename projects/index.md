---
title: Projects
nav:
  order: 4
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %} Projects

{% assign query = page.url | split: '?' | last | uri_decode %}
{% assign tag_filter = "" %}
{% if query contains "tag%3A" %}
  {% assign tag_filter = query | split: "tag%3A" | last | split: "&" | first | strip | downcase %}
{% elsif query contains "tag:" %}
  {% assign tag_filter = query | split: "tag:" | last | split: "&" | first | strip | downcase %}
{% endif %}

{% assign ongoing_projects = site.data.projects | where: "group", "ongoing" %}
{% assign completed_projects = site.data.projects | where: "group", "completed" %}

{% include tags.html data=site.data.projects %}

## Ongoing Projects

{% include list.html data=ongoing_projects component="card" tag_filter=tag_filter %}

{% include section.html %}

## Completed Projects

{% include list.html data=completed_projects component="card" tag_filter=tag_filter style="small" %}
