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

{%- comment -%}
Tag 필터링 파싱: ?search="tag:software" 또는 ?search=tag%3Asoftware 모두 지원
{%- endcomment -%}
{% assign query = page.url | split: '?' | last | uri_decode %}
{% assign tag_filter = "" %}
{% if query contains "tag%3A" %}
  {% assign tag_filter = query | split: "tag%3A" | last | split: "&" | first | strip | downcase %}
{% elsif query contains "tag:" %}
  {% assign tag_filter = query | split: "tag:" | last | split: "&" | first | strip | downcase %}
{% endif %}

{% assign tag_filter = tag_filter | downcase %}

---

## Ongoing Projects

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
