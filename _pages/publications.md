---
title: "Publications"
layout: gridlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

# Publications

(<sup>#</sup> for equal contribution; <sup>\*</sup> for corresponding authors)

<ol>
{% for publi in site.data.publications %}

{% if publi.title == "year" %}
<h4>{{ publi.year }}</h4>
{% else %}
<li>{{ publi.authors }} ({{ publi.year }}) {{ publi.title }}. <a href="https://doi.org/{{ publi.doi }}"><i>{{publi.journal}}</i>, {{ publi.display }}</a>.
[PMID: <a href="https://www.ncbi.nlm.nih.gov/pubmed/{{ publi.pmid }}">{{ publi.pmid }}</a>][<a href="https://badge.dimensions.ai/details/doi/{{ publi.doi }}">Citations</a>]
</li>
{% endif %}

{% endfor %}
</ol>
