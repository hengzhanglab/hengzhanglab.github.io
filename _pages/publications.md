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
{% if publi.doi != null and publi.doi != empty %}
<a href="https://doi.org/{{ publi.doi }}"><i>{{publi.journal}}</i>, {{ publi.display }}</a>.
{% else %}
<i>{{publi.journal}}</i>, {{ publi.display }}.
{% endif %}
{% if publi.pmid != null and publi.pmid != empty %}
[PMID: <a href="https://www.ncbi.nlm.nih.gov/pubmed/{{ publi.pmid }}">{{ publi.pmid }}</a>]
{% endif %}
{% if publi.doi != null and publi.doi != empty %}
[<a href="https://badge.dimensions.ai/details/doi/{{ publi.doi }}">Citations</a>]
{% endif %}
</li>
{% endif %}

{% endfor %}
</ol>
