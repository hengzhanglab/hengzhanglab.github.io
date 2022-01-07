---
title: "HengZhang Lab - Publications"
layout: gridlay
excerpt: "HengZhang Lab -- Publications"
sitemap: false
permalink: /publications/
---

<script async src="https://badge.dimensions.ai/badge.js" charset="utf-8"></script>

# Publications

(<sup>#</sup> for equal contribution; <sup>\*</sup> for corresponding authors)

<ul>
{% for publi in site.data.recentpub %}
<li>{{ publi.authors }} ({{ publi.year }}) {{ publi.title }}. <a href="https://doi.org/{{ publi.doi }}"><i>{{publi.journal}}</i>, {{ publi.display }}</a>.
[PMID: <a href="https://www.ncbi.nlm.nih.gov/pubmed/{{ publi.pmid }}">{{ publi.pmid }}</a>]
<span class="__dimensions_badge_embed__" data-doi="{{ publi.doi }}" data-style="small_rectangle"></span>
</li>
{% endfor %}
</ul>
