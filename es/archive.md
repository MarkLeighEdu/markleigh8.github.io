---
layout: page
title: "Archivo"
description: "Blog de Mark Leigh Trading Education"
hide-in-nav: true
lang: es
permalink: /es/archive/
---
<!-- Spanish content here -->
<div class="archive-section">
  <h2>Comentario Diario</h2>
  <ul>
    {% assign report1_files = site.static_files | where_exp: "file", "file.path contains 'mark-report/daily1'" %}
    {% assign sorted_report1 = report1_files | sort: 'modified_time' %}
    {% for file in sorted_report1 %}
      <li><a href="{{ file.path }}" target="_blank">{{ file.name }}</a></li>
    {% endfor %}
  </ul>
</div>
