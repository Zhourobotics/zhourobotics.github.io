---
layout: page
permalink: /publications/
title: Publications
description: Publications by categories in reversed chronological order.
years: [Preprint, 2022, 2021, 2020, 2019, 2018, 2017, 2015]
nav: true
nav_order: 2
---

Alternative sources for our publications:

- [Google Scholar](https://scholar.google.com/citations?user=0sNe1G4AAAAJ&hl=en){:target="_blank"}
- [ResearchGate](https://www.researchgate.net/profile/Lifeng-Zhou-3/publications){:target="_blank"}

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>