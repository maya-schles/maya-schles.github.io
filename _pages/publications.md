---
layout: page
permalink: /publications/
title: papers
description: 
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

### Working Papers
<div class="publications">
  {% bibliography --group_by none --query @*[working=true]* %}
</div>

### Publications
<div class="publications">
  {% bibliography --group_by none --query @*[working=false]* %}
</div>
