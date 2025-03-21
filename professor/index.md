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
  <div style="display: flex; flex-direction: column; align-items: flex-start; text-align: left; position: absolute; left: 28%">
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
  research/?search="Dong-Gyu%20Lee"
{%- endcapture %}

<p class="center">
  <a href="{{ search | relative_url | uri_escape }}">
    Search for {{ page.name | default: page.title }}'s papers on the Research page
  </a>
</p>

## Work Experiences

<div style="flex-direction: column;">
  <div style="display: flex;align-items: center;">
    <span style="min-width: 150px; text-align: left;">2024.10 ~ Current</span>
    <span>▶︎ Associate professor, School of Electronics Engineering, Kyungpook National University.</span>
  </div>
  <div style="display: flex;align-items: center;">
    <span style="min-width: 150px; text-align: left;">2024.10 ~ Current</span>
    <span>▶︎ Associate professor, Department of Artificial Intelligence, Kyungpook National University.</span>
  </div>
  <div style="display: flex;align-items: center;">
    <span style="min-width: 150px; text-align: left;">2023.02 ~ 2024.09</span>
    <span>▶︎ Assistant professor, School of Electronics Engineering, Kyungpook National University.</span>
  </div>
  <div style="display: flex;align-items: center;">
    <span style="min-width: 150px; text-align: left;">2020.09 ~ 2024.09</span>
    <span>▶︎ Assistant professor, Department of Artificial Intelligence, Kyungpook National University.</span>
  </div>
  <div style="display: flex;align-items: center;">
    <span style="min-width: 150px; text-align: left;">2020.03 ~ 2020.08</span>
    <span>▶︎ Research professor, Department of Artificial Intelligence, Korea University.</span>
  </div>
  <div style="display: flex;align-items: center;">
    <span style="min-width: 150px; text-align: left;">2019.03 ~ 2020.03</span>
    <span>▶︎ Research engineer, SK Holdings C&C.</span>
  </div>
  <div style="display: flex;align-items: center;">
    <span style="min-width: 150px; text-align: left;">2014.06 ~ 2014.08</span>
    <span>▶︎ Visiting research scholar, University of California, Riverside.</span>
  </div>
</div>

## Education
▶︎ Ph. D. in Computer Science and Engineering, Korea University, 2019. (Supervisor: Prof.Seong-Whan Lee)<br>
▶︎ B. S. in Computer Science and Engineering, Kwangwoon University, 2011.<br>

## Professional Services
