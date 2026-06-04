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

{% capture working_papers %}{% bibliography --group_by none --query @*[working=true]* %}{% endcapture %}
{% assign working_papers_stripped = working_papers | strip %}
{% if working_papers_stripped != "" %}
# Working Papers
<div class="publications">
  {{ working_papers }}
</div>
{% endif %}

# Publications
<div class="publications">
  {% bibliography --group_by none --query @*[working=false]* %}
</div>
