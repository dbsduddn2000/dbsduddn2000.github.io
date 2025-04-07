---
title: Projects
nav:
  order: 4
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Projects

projects page.

{% assign tag_set = "" | split: "," %}
{% for project in site.data.projects %}
  {% if project.tags %}
    {% for tag in project.tags %}
      {% unless tag_set contains tag %}
        {% assign tag_set = tag_set | push: tag %}
      {% endunless %}
    {% endfor %}
  {% endif %}
{% endfor %}

{% assign tag_string = tag_set | join: ", " %}
{% include tags.html tags=tag_string %}

{% include search-info.html %}

{% include section.html %}

## Ongoing Projects

{% include list.html component="card" data="projects" filter="group == 'ongoing'" %}

{% include section.html %}

## Completed Projects

{% include list.html component="card" data="projects" filter="group == 'completed'" style="small" %}
