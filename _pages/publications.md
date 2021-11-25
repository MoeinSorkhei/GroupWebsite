---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---


# Publications

[comment]: <> ({% assign number_printed = 0 %})
{% for publi in site.data.publist %}

[comment]: <> ({% assign even_odd = number_printed | modulo: 2 %})
{% if publi.highlight == 1 %}

[comment]: <> ({% if even_odd == 0 %})
<div class="row">

[comment]: <> ({% endif %})

<div class="container-fluid">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p><br>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

[comment]: <> ({% assign number_printed = number_printed | plus: 1 %})

[comment]: <> ({% if even_odd == 1 %})
</div>

[comment]: <> ({% endif %})

{% endif %}
{% endfor %}

[comment]: <> ({% assign even_odd = number_printed | modulo: 2 %})

[comment]: <> ({% if even_odd == 1 %})

[comment]: <> (</div>)

[comment]: <> ({% endif %})

[comment]: <> (<p> &nbsp; </p>)

