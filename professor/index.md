---
title: Professor
nav:
  order: 6
  tooltip: About Professor
---

# {% include icon.html icon="fa-solid fa-users" %}Professor

<div class="container" style="display: flex; align-items: center; position: relative;">
  <div style="display: flex;">
    {% include portrait.html lookup=page.slug %}
  </div>
  <div style="display: flex; flex-direction: column; align-items: flex-start; text-align: left; position: absolute; left: 20%">
    <b>Dong-Gyu Lee, Ph.D. (이동규)</b><br>
    ➤ Department of Artificial Intelligence (인공지능학과) & School of Electronics Engineering (전자공학부)<br>
    ➤ Kyungpook National University (경북대학교), South Korea<br>
    ➤ Office: Room 512, Techno Bldg., KNU
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
