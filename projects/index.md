---
title: Projects
nav:
  order: 4
  tooltip: Software, datasets, and more
---
# {% include icon.html icon="fa-solid fa-wrench" %}Projects
projects page
{% include tags.html tags="publication, resource, website" %}
{% include search-info.html %}

{% include section.html %}

## Ongoing Projects
{% include list.html component="card" data="projects" filter="group == 'ongoing'" %}
{% include section.html %}

## Completed Projects
{% include list.html component="card" data="projects" filter="group == 'completed'" style="small" %}
