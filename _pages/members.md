---
title: "Members"
layout: gridlay
excerpt: "Members"
sitemap: false
permalink: /members/
---

# Group Members

{% for member in site.data.members %}

 {% if member.name == "row" %}
  {% if rowopen == 1 %}
   </div>
   {% assign rowopen = 0 %}
  {% endif %}
  <hr />
  <div class="row"><h2>{{ member.info }}</h2></div>
  {% continue %}
 {% endif %}

 {% if rowopen != 1 %}
  <div class = "row">
  {% assign rowopen = 1 %}
  {% assign i = 0 %}
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

 {% assign i = i | plus: 1 %}
 {% if i == 2 %}
  </div>
  {% assign rowopen = 0 %}
 {% endif %}

{% endfor %}

{% if rowopen == 1 %}
 </div>
{% endif %}

---

<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/teamphoto.jpeg" class="img-responsive"/>
<p align="right">This photo was taken on 2022.1.6 in Shanghai Chenshan Botanical Garden.</p>

---

## Former members

- **Yuan Wang**
- **Minqing Huang**
- **Jingqi Wang**
- **Xuefeng Chen**
- **Xiaoxian Zhu**
- **Xiaojie Zhang**
- **Ali Kiana-Pouya**
- **Fatemeh Rasouli**
- **Yi Xiong**
- **Hehua Zhang**
- **Yingcun Hao**
- **Meiling Zhang**
- **Jianfei Guo**
- **Yuwei Jiang**
- ...

---
