---
title: "Team"
layout: gridlay
excerpt: "Team"
sitemap: false
permalink: /team/
---

# Group Members
<!-- ## Staff -->
{% assign number_printed = 0 %}
{% for member in site.data.team_members %} 
{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" />
  {% if member.webpage == "" %}
  <h4>{{ member.name }}</h4>
  {% else %}
  <h4><a href="{{ member.webpage }}"> {{ member.name }}</a></h4>
  {% endif %}
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

{% if even_odd == 1 %}
</div>
{% endif %}
{% assign number_printed = number_printed | plus: 1 %}

{% endfor %}

[comment]: <> ({% assign even_odd = number_printed | modulo: 2 %})

[comment]: <> ({% if even_odd == 1 %})

[comment]: <> (</div>)

[comment]: <> ({% endif %})



[comment]: <> (## Master students)

[comment]: <> (## Alumni)

[comment]: <> (## Former visitors, BSc/ MSc students)