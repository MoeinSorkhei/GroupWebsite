---
title: "Publications"
layout: publay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---


# Publications

{% for publi in site.data.publist %}

<div class="container-fluid">
<div class="row">

<pubtit>{{ publi.title }}</pubtit>
<p>{{ publi.authors }}</p>
<p><em>{{ publi.venue }}</em></p>
<p>
  <a href="{{ publi.url }}"><i class="far fa-file-pdf"></i> PDF</a> &nbsp;&nbsp;&nbsp;&nbsp;
  <a href="/bibtex/{{ publi.id }}.bib"><i class="far fa-file-alt"></i> BibTex</a>&nbsp;&nbsp;&nbsp;&nbsp;
  {% if publi.code %} <a href="{{ publi.code }}"><i class="fas fa-code"></i> Code</a>&nbsp;&nbsp;&nbsp;&nbsp; {% endif %}
</p>
</div>
</div>
{% endfor %}

