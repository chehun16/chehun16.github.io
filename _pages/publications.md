---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="pub-category-header">International</h2>

{% bibliography --query @*[category=international] %}

<h2 class="pub-category-header">Domestic</h2>

{% bibliography --query @*[category=domestic] %}

</div>
