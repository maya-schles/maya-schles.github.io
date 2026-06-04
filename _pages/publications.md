---
layout: default
permalink: /papers/
title: papers
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

{% capture working_count %}{% bibliography_count --query @*[working=true]* %}{% endcapture %}
{% if working_count != "0" %}
# Working Papers
<div class="publications">
  {% bibliography --group_by none --query @*[working=true]* %}
</div>
{% endif %}

# Publications
<div class="publications">
  {% bibliography --group_by none --query @*[working=false]* %}
</div>
