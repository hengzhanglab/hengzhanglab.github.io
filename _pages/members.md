---
title: "Members"
layout: gridlay
excerpt: "Members"
sitemap: false
permalink: /members/
---

# Group Members

{% assign number_printed = 0 %}
{% for member in site.data.members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  <ul style="overflow: hidden">

  {% for record in member.info2 %}
  <li>{{ record }}</li>
  {% endfor %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

---

- Former members
  - **Ali Kiana-Pouya**
  - **Fatemeh Rasouli**
  - **Yi Xiong**
  - **Hehua Zhang**
  - **Yingcun Hao**
  - **Meiling Zhang**
  - ...

---
