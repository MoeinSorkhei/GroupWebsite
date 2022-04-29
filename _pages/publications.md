---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---


# Publications

{% for publi in site.data.publist %}

<div class="row">
<div class="container-fluid">

<div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <p><em>{{ publi.authors }}</em></p>
  <p>
    <a href="{{ publi.url }}"><i class="far fa-file-pdf"></i> PDF</a> &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="{{ publi.citation }}"><i class="far fa-file-alt"></i> BibTex</a>&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="{{ publi.github }}"><i class="fas fa-code"></i> GitHub</a>&nbsp;&nbsp;&nbsp;&nbsp;
  </p>
</div>

</div>
</div>

{% endfor %}

