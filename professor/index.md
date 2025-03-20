---
title: Professor
nav:
  order: 6
  tooltip: About Professor
---

# {% include icon.html icon="fa-regular fa-envelope" %}Professor

<div>
  <div>
    {% include portrait.html lookup=page.slug %}
  </div>
  <div>
    fffffff
  </div>
</div>


{%
  include button.html
  type="email"
  text="dglee@knu.ac.kr"
  link="dglee@knu.ac.kr"
%}

{% include float.html content=floatcontent %}

{{ content }}

{% assign aliases = page.aliases
  | default: page.name
  | default: page.title
  | join: ","
  | split: ","
  | array_filter
%}

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
