---
title: "Members"
layout: gridlay
excerpt: "Members"
sitemap: false
permalink: /members/
---

# Group Members

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

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

<div class="col-sm-1"></div>

<div class="col-sm-9 clearfix">



- Current members
  - **Zhaohai Zhu** • Staff • <zhzhu@psc.ac.cn>
  - **Jiangmei Sun** • Postdoctoral Fellow • <jmsun@psc.ac.cn>
  - **Yuan Wang** • Postdoctoral Fellow • <yuanwang@psc.ac.cn>
  - **Leiting Li** • Postdoctoral Fellow • <ltli@psc.ac.cn>
  - **Chana Borjigin** • Postdoctoral Fellow • <chana@psc.ac.cn>
  - **Ai Zeng** • Staff • <aizeng@psc.ac.cn>
  - **Hongwei Wang** • Staff • <hwwang@psc.ac.cn>
  - **Mingsuo Cheng** • Staff
  - **Jingjing Song** • Staff • <jjsong@psc.ac.cn>
  - **Zheting Zhang** • Graduate student • <ztzhang@psc.ac.cn>
  - **Xueqin Li** • Graduate student • <xqli@psc.ac.cn>
  - **Juan Huang** • Graduate student • <juanhuang@psc.ac.cn>
  - **Jiahong Chen** • Graduate student • <jhchen@psc.ac.cn>
  - **Tian Dai** • Graduate student • <tiandai@psc.ac.cn>
  - **Qingbing Wu** • Graduate student • <qbwu@psc.ac.cn>
  - **Ruoyun Chen** • Graduate student • <rychen@psc.ac.cn>
  - **Yu Tan** • Graduate student • <yutan@psc.ac.cn>
  - **Yuwei Wang** • Graduate student • <ywwang@psc.ac.cn>
  - **Lishuo Wang** • Graduate student
  - **Yuan Long** • Graduate student
  - **Yuanhao Zhu** • Graduate student
  - **Minqing Huang** • Visiting student

---

- Former members
  - **Ali Kiana-Pouya**
  - **Fatemeh Rasouli**
  - **Yi Xiong**
  - **Hehua Zhang**
  - **Yingcun Hao**
  - **Meiling Zhang**
  - ...

</div>
<div class="col-sm-2"></div>

---
