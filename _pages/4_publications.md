---	
layout: page
permalink: /publications/
title: Publications
description: 
years: [2025, 2024, 2023, 2022, 2021, 2019, 2018, 2017, 2016, 2015, 2011]
idx: [1, 2]
nav: true
---

For citation information, please visit my Google Scholar [page](https://scholar.google.com/citations?user=_AYu5NMAAAAJ&hl=en&oi=ao){:target="\_blank"}.

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>