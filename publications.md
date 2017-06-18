---
layout: page
title: Publications
header: Publications
group: navigation
---
{% comment %}
{% include JB/setup %}
{% endcomment %}

{% for y in site.data.papers %}
  <p>
  <b>{{ y.year }}</b>
  {% for p in y.papers %}
    <p>
    <i>{{ p.title }}</i>
    {{ p.authors }}.
    {{ p.venue }}.

    {% if p.year != null %}
    {{ p.year }}.
    {% endif %}

    {% if p.pdf != null %}
    <a href="{{ p.pdf }}">[pdf]</a>
    {% endif %}

    {% if p.bib != null %}
    <a href="{{ p.bib }}">[bib]</a>
    {% endif %}

    {% if p.code != null %}
    <a href="{{ p.code }}">[code]</a>
    {% endif %}

    {% if p.data != null %}
    <a href="{{ p.data }}">[data]</a>
    {% endif %}
   
    </p>
  {% endfor %}
  </p>
{% endfor %}

