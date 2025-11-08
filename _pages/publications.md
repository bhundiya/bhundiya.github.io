---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 4
# {% bibliography %}
_styles: |
  /* Styled headings for publication sections */
  .publications .pub-section-heading {
    font-size: 1.6rem;
    margin: 2rem 0 1rem;
    color: var(--global-theme-color);
    text-align: center;
    font-weight: 600;
    letter-spacing: 0.5px;
  }
---
Please see Prof. Bhundiya's [Google Scholar page](https://scholar.google.com/citations?user=1wCSzO0AAAAJ&hl=en) for the latest publications.

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->
{% include bib_search.liquid %}

<div class="publications">
<h3 class="pub-section-heading">Journal Articles</h3>
{% bibliography --file papers --group_by none --query @article %}
<h3 class="pub-section-heading">Conference Papers</h3>
{% bibliography --file papers --group_by none --query @inproceedings %}
</div>
