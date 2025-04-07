---
title: Projects
nav:
  order: 4
  tooltip: Software, datasets, and more
---
# {% include icon.html icon="fa-solid fa-wrench" %}Projects
Projects page

{%- assign all_tags = "" | split: "," -%}
{%- for item in site.data.projects -%}
  {%- if item.tags -%}
    {%- for tag in item.tags -%}
      {%- unless all_tags contains tag -%}
        {%- assign all_tags = all_tags | push: tag -%}
      {%- endunless -%}
    {%- endfor -%}
  {%- endif -%}
{%- endfor -%}
{%- assign all_tags = all_tags | sort -%}

{% include tags.html tags=all_tags %}

{% include search-info.html %}

{% include section.html %}

## Ongoing Projects

{% include list.html component="card" data="projects" filter="group == 'ongoing'" %}

{% include section.html %}

## Completed Projects

{% include list.html component="card" data="projects" filter="group == 'completed'" style="small" %}
