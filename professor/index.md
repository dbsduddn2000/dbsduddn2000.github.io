---
title: Professor
nav:
  order: 6
  tooltip: About Professor
---

# {% include icon.html icon="fa-solid fa-users" %}Professor

<div class="container" style="display: flex; align-items: center; position: relative; gap: 80px;">
  <div style="margin-right: auto;">
    {% include portrait.html lookup=page.slug %}
  </div>
  <div style="display: flex; flex-direction: column; align-items: center; text-align: left; position: absolute; left: 50%">
    fffffff
    {%
      include button.html
      type="email"
      text="dglee@knu.ac.kr"
      link="dglee@knu.ac.kr"
    %}
  </div>
</div>

{% capture search -%}
  research/?search={% for alias in aliases %}"{{ alias }}" {% endfor %}
{%- endcapture %}

<p class="center">
  <a href="{{ search | relative_url | uri_escape }}">
    Search for {{ page.name | default: page.title }}'s papers on the Research page
  </a>
</p>

{% capture search -%}
  blog/?search={{ page.name }}
{%- endcapture %}
