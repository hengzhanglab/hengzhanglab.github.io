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

- **Jingjing Song**, Staff
- **Yuan Wang**, Postdoc
- **Minqing Huang**, Visiting graduate student
- **Jingqi Wang**, Undergraduate intern
- **Xuefeng Chen**, Rotation student
- **Xiaoxian Zhu**, Rotation student
- **Xiaojie Zhang**, Summer intern
- **Ali Kiana-Pouya**, Visiting Ph.D. student
- **Fatemeh Rasouli**, Visiting Ph.D. student
- **Yi Xiong**, Visiting Ph.D. student
- **Hehua Zhang**, Staff
- **Yingcun Hao**, Staff
- **Meiling Zhang**, Staff
- **Xiansong Xiong**, Ph.D. student
- **Jianfei Guo**, Ph.D. student
- **Yuwei Jiang**, Ph.D. student
- ...

---
