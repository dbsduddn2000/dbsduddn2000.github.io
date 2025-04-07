---
title: Projects
nav:
  order: 4
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Projects

{% include tags.html %}

{% assign ongoing_projects = site.data.projects | where: "group", "ongoing" %}
{% assign completed_projects = site.data.projects | where: "group", "completed" %}

## Ongoing Projects

{% assign tag_filter = tag_filter | downcase %}
{% for p in ongoing_projects %}
  {% assign tags = p.tags | join: "," | downcase %}
  {% if tag_filter == "" or tags contains tag_filter %}
    {% include card.html
      title=p.title
      subtitle=p.subtitle
      description=p.description
      image=p.image
      tags=p.tags
      repo=p.repo
      link=p.link
    %}
  {% endif %}
{% endfor %}


{% include section.html %}

## Completed Projects

{% assign tag_filter = tag_filter | downcase %}
{% for p in completed_projects %}
  {% assign tags = p.tags | join: "," | downcase %}
  {% if tag_filter == "" or tags contains tag_filter %}
    {% include card.html
      title=p.title
      subtitle=p.subtitle
      description=p.description
      image=p.image
      tags=p.tags
      repo=p.repo
      link=p.link
      style="small"
    %}
  {% endif %}
{% endfor %}
