---
layout: projdefault
projectname: Reactors.IO
projectpath: 
logoname: reactress-mini-logo-flat.png
title: Reactors.IO 0.6 Documentation
permalink: /docs/0.6/index.html
reactressversion: 0.6
---



### General

{% for pg in site.pages %}
  {% if pg.section == "General" and pg.reactressversion == 0.6 and pg.pagetot %}
    {% assign totalPages = pg.pagetot %}
  {% endif %}
{% endfor %}

<ul>
{% for i in (1..totalPages) %}
  {% for pg in site.pages %}
    {% if pg.section == "General" and pg.reactressversion == 0.6 and pg.pagenum and pg.pagenum == i %}
      <li><a href="{{ pg.url }}">{{ pg.title }}</a></li>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>


### Examples

{% for pg in site.pages %}
  {% if pg.section == "Examples" and pg.reactressversion and pg.reactressversion == 0.6 and pg.pagetot %}
    {% assign totalPages = pg.pagetot %}
  {% endif %}
{% endfor %}

<ul>
{% for i in (1..totalPages) %}
  {% for pg in site.pages %}
    {% if pg.section == "Examples" and pg.reactressversion == 0.6 and pg.pagenum and pg.pagenum == i %}
      <li><a href="{{ pg.url }}">{{ pg.title }}</a></li>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>

