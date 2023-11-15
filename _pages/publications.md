---
layout: page
permalink: /publications
title: publications
description: publications relavant to the SmartLab network.
years: [2023, 2022, 2021, 2020]
nav: true
impressum_path: /impressum

---
<!-- _pages/publications.md -->
<div class="publications">


{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
