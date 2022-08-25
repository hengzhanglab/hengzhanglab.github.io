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
<h3>{{ publi.year }}</h3>
<hr />
{% else %}
<li> <span style="color:#8B4513">{{ publi.title }}</span> <br />
{{ publi.authors }} ({{ publi.year }}) <br /> 
<a href="https://doi.org/{{ publi.doi }}"><i>{{publi.journal}}</i>, {{ publi.display }}</a>.
{% if publi.pmid != null and publi.pmid != empty %}
[PMID: <a href="https://www.ncbi.nlm.nih.gov/pubmed/{{ publi.pmid }}">{{ publi.pmid }}</a>]
{% endif %}
[<a href="https://badge.dimensions.ai/details/doi/{{ publi.doi }}">Citations</a>]
</li>
{% endif %}

{% endfor %}
</ol>
