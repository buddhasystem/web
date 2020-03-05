---
title: PHENIX Photo Gallery
abbrev: phenix_gallery
layout: default
weight: 2
level: 0
---
# PHENIX Photo Gallery

{% assign images = site.data.gallery | sort: 'weight' %}

<table>

{% tablerow image in images cols:2 %}

{% if image.title !='' %}
{{ image.title }}<br/>
{% endif %}

<a href="{{ image.path | relative_url }}">
<img src="{{ image.path | relative_url }}" alt="{{ image.title}}" width="400px"/>&nbsp;<br/><p/>
</a>

{% endtablerow %}

</table>
