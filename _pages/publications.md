---
layout: page
title: Publications
nav_title: Publications
permalink: /publications/
description: My publications.
nav: true
nav_order: 3
hide_bibtex: true
---

<!-- Renders publications from `_bibliography/papers.bib` via jekyll-scholar -->

<div class="publications">
  {% bibliography -f {{ site.scholar.bibliography }} %}
</div>


